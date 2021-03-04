---
title: Facturación en Project Service Automation
description: En este tema se proporciona información sobre la facturación.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0855e85c1f09d29d3ecb49ba517fd3043ae11140
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151409"
---
# <a name="invoicing-in-project-service-automation"></a>Facturación en Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La facturación en Dynamics 365 Project Service Automation es útil porque proporciona a los jefes de proyecto un segundo nivel de aprobación antes de crear las facturas para los clientes. El primer nivel de aprobación se completa cuando se aprueban las entradas de tiempo y gastos que envían los miembros del proyecto.

PSA no está diseñado para generar facturas de cara al cliente por las siguientes razones:

- No contiene información fiscal.
- No puede convertir otras divisas a la divisa de facturación con tipos de cambio configurados correctamente.
- No puede dar el formato correcto a las facturas para que se puedan imprimir.

En su lugar, puede usar un sistema de contabilidad financiero para crear facturas de cara al cliente que utilicen la información de las propuestas de factura que se generan en PSA.

## <a name="creating-project-invoices-in-psa"></a>Creación de facturas de proyecto en PSA

Las facturas de proyecto se pueden de una en una o de forma masiva. Puede crearlas manualmente, o bien se pueden configurar para que se generen de forma automática.

### <a name="manually-create-project-invoices-in-psa"></a>Crear facturas de proyecto manualmente en PSA

En la página lista **Contratos de proyecto**, podrá crear facturas de proyecto por separado para cada contrato de proyecto, o bien puede crear facturas de forma masiva para varios contratos de proyecto.

Siga este paso para crear una factura para un contrato de proyecto específico.

- En la página de lista **Contratos de proyecto**, abra un contrato de proyecto y después seleccione **Crear factura**.

    ![Creación de facturas de proyecto para un contrato de proyecto específico](media/CreateProjectInvoicesOneByOne.png)

    El sistema genera una factura para todas las transacciones del contrato de proyecto seleccionado que tienen el estado **Listo para facturar**. Estas transacciones incluyen datos de tiempo, gastos, hitos y líneas de contrato basadas en producto.

Siga estos pasos para crear facturas de forma masiva.

1. En la página de lista **Contratos de proyecto**, seleccione uno o varios contratos de proyecto para los que desee crear una factura y después seleccione **Crear facturas de proyecto**.

    ![Creación de facturas de proyecto de forma masiva](media/CreateProjectInvoicesBulk.png)

    Un mensaje de advertencia le informará de que es posible que haya un retraso antes de que se creen las facturas. También se muestra el proceso.

2. Seleccione **Aceptar** para cerrar el cuadro del mensaje.

    El sistema genera una factura para todas las transacciones de una línea de contrato con el estado **Listo para facturar**. Estas transacciones incluyen datos de tiempo, gastos, hitos y líneas de contrato basadas en producto.

3. Para ver las facturas que se generan, vaya a **Ventas** \> **Facturación** \> **Facturas**. Se mostrará una factura para cada contrato de proyecto.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurar la creación automática de facturas de proyecto en PSA

Siga estos pasos para configurar la ejecución automática de facturas en PSA.

1. Vaya a **Project Service** \> **Configuración** \> **Trabajos por lotes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de PSA**. El nombre del trabajo por lotes debe incluir el término "Creación de facturas".
3. En el campo **Tipo de trabajo**, seleccione **Ninguno**. De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registros**, se mostrarán tres flujos de trabajo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y después seleccione **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. El flujo de trabajo **Reposo** va seguido de un flujo de trabajo **Proceso**.

    También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea realmente las facturas. Pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas. Para determinar las líneas de contrato para las que se deben crear facturas, el trabajo busca fechas de ejecución de facturas para las líneas de contrato. Si hay líneas de contrato que pertenecen a un contrato que tiene la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para crear facturas, el trabajo omite la creación de factura.

Cuando finaliza la ejecución de **ProcessRunner**, se llama al flujo de trabajo **ProcessRunCaller**, que proporciona la hora de finalización y después se cierra. A continuación, **ProcessRunCaller** pone en marcha un temporizador que se ejecuta durante 24 horas desde la hora de finalización especificada. Cuando se agota el tiempo del temporizador, el flujo de trabajo **ProcessRunCaller** se cierra.

El trabajo del proceso por lotes para la creación de facturas es un trabajo recurrente. Si este proceso por lotes se ejecuta muchas veces, se crean varias instancias del trabajo y se generan errores. Por lo tanto, debe iniciar el proceso por lotes solo una vez y debe reiniciarlo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes en Project Service Automation solo se ejecuta para las líneas de contrato del proyecto que están configuradas por programaciones de facturas. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha. La información sobre la configuración de frecuencias de facturación en el contexto de un proyecto que se basa en una línea de cotización se proporciona en el tema [Cotizaciones y líneas de cotización](basic-quote-lines.md#invoice-schedule). Lo mismo se aplica a una línea de contrato basada en proyectos.      
 
### <a name="edit-a-draft-psa-invoice"></a>Editar un borrador de factura de PSA

Cuando se crea un borrador de factura de proyecto, todas las transacciones de venta sin facturar que se crearon cuando se aprobaron las entradas de tiempo y gastos se incluyen en la factura. Puede realizar los siguientes ajustes mientras facturación aún está en fase de borrador:

- Eliminar o editar los detalles de la línea de factura.
- Editar y ajustar la cantidad y el tipo de facturación.
- Agregar directamente a la factura el tiempo, los gastos y las tarifas como transacciones. Puede usar esta característica si la línea de la factura se asigna a una línea de contrato que permita estas clases de transacciones.

Seleccione **Confirmar** para confirmar una factura. La acción Confirmar es una acción unidireccional. Cuando se selecciona **Confirmar**, el sistema convierte la factura en factura de solo lectura y crea datos reales de ventas facturadas de todos los detalles de cada línea de factura. Si el detalle de la línea de factura hace referencia a un dato real de ventas sin facturar, el sistema también revierte el dato real de ventas sin facturar. (Los detalles de línea de factura que se crearon a partir de una entrada de tiempo o gasto harán referencia a un dato real de ventas sin facturar.) Los sistemas de integración de contabilidad general pueden usar esta reversión para revertir trabajo de un proyecto en proceso (WIP) con propósitos de contabilidad.

### <a name="correct-a-confirmed-psa-invoice"></a>Corregir una factura de PSA confirmada

Las facturas de PSA confirmadas se pueden editar (corregir). Cuando se corrige una factura confirmada, se crea un nuevo borrador de factura correctiva. Puesto que se da por sentado que desea revertir todas las transacciones y las cantidades de factura original, esta factura correctiva incluye todas las transacciones de la factura original y todas sus cantidades son iguales a 0 (cero).

Si alguna transacción no requiere corrección, puede quitarla del borrador de la factura correctiva. Si desea revertir o devolver solo una cantidad parcial, puede editar el campo **Cantidad** en el detalle de la línea. Si abre el detalle de la línea de factura, podrá ver la cantidad de la factura original. A continuación, podrá editar la cantidad de la factura actual para que sea superior o inferior a la cantidad de la factura original.

Cuando se confirma una factura correctiva, el dato real de ventas facturadas originales se revierte y se crea un nuevo dato real de ventas facturadas. Si la cantidad se redujo, la diferencia también generará un nuevo dato real de ventas sin facturar. Por ejemplo, si las ventas facturadas originales ascendían a ocho horas y el detalle de línea de factura correctiva tenía una cantidad reducida de seis horas, PSA revertirá la línea de ventas facturadas originales y creará dos nuevos datos reales:

- Un dato real de ventas facturadas por seis horas.
- Un dato real de ventas sin facturar por las dos horas restantes. Esta transacción se puede facturar más adelante o se puede marcar como no imputable, en función de las negociaciones con el cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]