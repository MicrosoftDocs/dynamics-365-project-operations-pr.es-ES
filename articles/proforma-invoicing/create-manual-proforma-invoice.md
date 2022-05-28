---
title: Facturas proforma
description: Este tema proporciona información sobre las facturas proforma en Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e20ea17691c592493a790fb38451b35db03416be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600073"
---
# <a name="proforma-invoices"></a>Facturas proforma

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

La facturación proforma proporciona a los jefes de proyecto un segundo nivel de aprobación antes de crear las facturas para los clientes. El primer nivel de aprobación se completa cuando se aprueban las entradas de tiempo, gastos y material que envían los miembros del proyecto. Las facturas proforma confirmadas están disponibles en el módulo Contabilidad de proyectos de Project Operations. Los contables de proyectos pueden realizar actualizaciones adicionales, como impuestos sobre las ventas, contabilidad y diseño de facturas.


## <a name="creating-project-invoices"></a>Creación de facturas de proyecto

Las facturas de proyecto se pueden de una en una o de forma masiva. Puede crearlas manualmente, o bien se pueden configurar para que se generen en ejecuciones automatizadas.

### <a name="manually-create-project-invoices"></a>Crear manualmente facturas de proyectos 

En la página lista **Contratos de proyecto**, podrá crear facturas de proyecto por separado para cada contrato de proyecto, o bien puede crear facturas de forma masiva para varios contratos de proyecto.

Siga este paso para crear una factura para un contrato de proyecto específico.

- En la página de lista **Contratos de proyecto**, abra un contrato de proyecto y luego seleccione **Crear factura**.

    El sistema genera una factura para todas las transacciones del contrato de proyecto seleccionado que tienen el estado **Listo para facturar**. Estas transacciones incluyen tiempo, gastos, materiales, hitos y otras líneas del diario de ventas no facturadas.

Siga estos pasos para crear facturas de forma masiva.

1. En la página de lista **Contratos de proyecto**, seleccione uno o varios contratos de proyecto para los que desee crear una factura y después seleccione **Crear facturas de proyecto**.

    Un mensaje de advertencia le indicará que puede haber una demora antes de que se creen las facturas. También se muestra el proceso.

2. Seleccione **Aceptar** para cerrar el cuadro de mensaje.

    El sistema genera una factura para todas las transacciones de una línea de contrato con el estado **Listo para facturar**. Estas transacciones incluyen tiempo, gastos, materiales, hitos y otras líneas del diario de ventas no facturadas.

3. Para ver las facturas que se generan, vaya a **Ventas** \> **Facturación** \> **Facturas**. Se mostrará una factura para cada contrato de proyecto.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar la creación automática de facturas de proyecto 

Siga estos pasos para configurar la ejecución automática de facturas.

1. Vaya a **Configuración** \> **Trabajos por lotes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**. El nombre del trabajo por lotes debe incluir el término "Creación de facturas".
3. En el campo **Tipo de trabajo**, seleccione **Ninguno**. De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registro**, aparecerán tres flujos de trabajo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y luego elija **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. Al flujo de trabajo **Suspensión** le sigue el flujo de trabajo **Proceso**.

    También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea realmente las facturas. Pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas. Para determinar para qué líneas de contrato deben crearse facturas, el trabajo examina las fechas de ejecución de facturas de las líneas de contrato. Si detecta líneas de contrato que pertenecen a un mismo contrato con la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para las que crear facturas, el trabajo omitirá la creación de facturas.

Cuando **ProcessRunner** termina de ejecutarse, llama a **ProcessRunCaller**, proporciona la hora de finalización y se cierra. **ProcessRunCaller**, a su vez, inicia un temporizador que se ejecuta durante 24 horas a partir de la hora de finalización especificada. Cuando el temporizador marque el final, **ProcessRunCaller** se cerrará.

El trabajo de proceso por lotes de creación de facturas es periódico. Si este proceso por lotes se ejecuta muchas veces, se crean numerosas instancias del trabajo y se producen errores. Por lo tanto, debe iniciar el proceso por lotes solo una vez y debe reiniciarlo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha. Lo mismo se aplica a una línea de contrato basada en proyectos.      
 
### <a name="edit-a-draft-invoice"></a>Editar un borrador de factura

Cuando se crea un borrador de factura de proyecto, todas las transacciones de venta sin facturar que se crearon cuando se aprobaron las entradas de tiempo, gastos y utilización de material se incluyen en la factura. Puede realizar los siguientes ajustes mientras facturación aún está en fase de borrador:

- Eliminar o editar los detalles de la línea de factura.
- Editar y ajustar la cantidad y el tipo de facturación.

Seleccione **Confirmar** para confirmar una factura. La acción Confirmar es una acción unidireccional. Cuando se selecciona **Confirmar**, el sistema convierte la factura en factura de solo lectura y crea datos reales de ventas facturadas de todos los detalles de cada línea de factura. Si el detalle de la línea de factura hace referencia a un dato real de ventas sin facturar, el sistema también revierte el dato real de ventas sin facturar. (Los detalles de línea de factura que se crearon a partir de una entrada de tiempo o gasto harán referencia a un dato real de ventas sin facturar.) Los sistemas de integración de contabilidad general pueden usar esta reversión para revertir trabajo de un proyecto en proceso (WIP) con propósitos de contabilidad.

> [!NOTE]
> Las facturas proforma confirmadas y los registros relacionados, como líneas de factura y detalles de líneas de factura, no se pueden editar ni eliminar. 

### <a name="correct-a-confirmed-invoice"></a>Corregir una factura confirmada

Las facturas confirmadas se pueden editar (corregir). Cuando se corrige una factura confirmada, se crea un nuevo borrador de factura correctiva. Puesto que se da por sentado que desea revertir todas las transacciones y las cantidades de factura original, esta factura correctiva incluye todas las transacciones de la factura original y todas sus cantidades son iguales a 0 (cero).

Si alguna transacción no requiere corrección, puede quitarla del borrador de la factura correctiva. Si desea revertir o devolver solo una cantidad parcial, puede editar el campo **Cantidad** en el detalle de la línea. Si abre el detalle de la línea de factura, podrá ver la cantidad de la factura original. A continuación, podrá editar la cantidad de la factura actual para que sea superior o inferior a la cantidad de la factura original.

Cuando se confirma una factura correctiva, el dato real de ventas facturadas originales se revierte y se crea un nuevo dato real de ventas facturadas. Si la cantidad se redujo, la diferencia también generará un nuevo dato real de ventas sin facturar. Por ejemplo, si la venta facturada original ascendía a ocho horas y el detalle de línea de factura correctiva tenía una cantidad reducida de seis horas, se revierte la línea de ventas facturadas originales y se crean dos nuevos datos reales:

- Un dato real de ventas facturadas por seis horas.
- Un dato real de ventas sin facturar por las dos horas restantes. Esta transacción se puede facturar más adelante o se puede marcar como no imputable, en función de las negociaciones con el cliente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
