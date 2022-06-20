---
title: Facturas de proyecto proforma
description: Este artículo proporciona información sobre las facturas de proyectos proforma en Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934571"
---
# <a name="proforma-project-invoices"></a>Facturas de proyecto proforma

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

La facturación proforma de proyectos proporciona a los jefes de proyecto un segundo nivel de aprobación antes de crear las facturas para los clientes. El primer nivel de aprobación se completa cuando se aprueban las entradas de tiempo, gastos y material que envían los miembros del proyecto.

La implementación simplificada de Dynamics 365 Project Operations no está diseñada para generar facturas de cara al cliente. La siguiente lista muestra por qué no se pueden generar facturas:

- No contiene información fiscal.
- No pueden convertir otras divisas a la divisa de facturación.
- No puede formatear correctamente las facturas para imprimir.

En su lugar, puede usar un sistema de contabilidad financiero para crear facturas de cara al cliente que utilicen la información en las propuestas de factura generadas.

## <a name="creating-project-invoices"></a>Creación de facturas de proyecto

Las facturas de proyecto se pueden de una en una o de forma masiva. Puede crearlas manualmente, o bien se pueden configurar para que se generen de forma automática.

### <a name="manually-create-project-invoices"></a>Crear facturas de proyecto manualmente 

En la página lista **Contratos de proyecto**, podrá crear facturas de proyecto por separado para cada contrato de proyecto, o bien puede crear facturas de forma masiva para varios contratos de proyecto.

   - Para crear una factura para un contrato de proyecto específico, en la página de lista **Contratos de proyecto**, abra un contrato de proyecto y después seleccione **Crear factura**.

   El sistema genera una factura para todas las transacciones del contrato de proyecto seleccionado que tienen el estado **Listo para facturar**. Estas transacciones incluyen tiempo, gastos, materiales, hitos, líneas de contrato basadas en productos y otras líneas del diario de ventas no facturadas que pueden haber sido confirmadas.

Para crear facturas de forma masiva:

1. En la página de lista **Contratos de proyecto**, seleccione uno o varios contratos de proyecto para crear una factura y después seleccione **Crear facturas de proyecto**.
2. Un mensaje de advertencia le indicará que puede haber una demora antes de que se creen las facturas. También se muestra el proceso. Seleccione **Aceptar** para cerrar el cuadro de mensaje.

   El sistema genera una factura para todas las transacciones de una línea de contrato con el estado **Listo para facturar**. Estas transacciones incluyen tiempo, gastos, materiales, hitos, líneas de contrato basadas en productos y otras líneas del diario de ventas no facturadas que pueden haber sido confirmadas.

3. Vea las facturas que se generan, para ello, vaya a **Ventas** \> **Facturación** \> **Facturas**. Se mostrará una factura para cada contrato de proyecto.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar la creación automática de facturas de proyecto 

Siga estos pasos para configurar la ejecución automática de facturas.

1. Vaya a **Configuración** \> **Trabajos por lotes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**. El nombre del trabajo por lotes debe incluir el término "Creación de facturas".
3. En el campo **Tipo de trabajo**, seleccione **Ninguno**. De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registro**, aparecerán los siguientes flujos de trabajo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y luego elija **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. Al flujo de trabajo **Suspensión** le sigue el flujo de trabajo **Proceso**.

    También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea las facturas. Este flujo de trabajo pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas. Para determinar las líneas de contrato para las que se deben crear facturas, el flujo de trabajo busca fechas de ejecución de facturas para las líneas de contrato. Si hay líneas de contrato que pertenecen a un contrato que tiene la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para crear facturas, no se crean facturas.

Cuando finaliza la ejecución de **ProcessRunner**, se llama al flujo de trabajo **ProcessRunCaller**, que proporciona la hora de finalización y después se cierra. **ProcessRunCaller**, a su vez, inicia un temporizador que se ejecuta durante 24 horas a partir de la hora de finalización especificada. Cuando el temporizador marque el final, **ProcessRunCaller** se cerrará.

El trabajo de proceso por lotes de creación de facturas es periódico. Si este proceso por lotes se ejecuta muchas veces, se crean varias instancias del trabajo y pueden producirse errores. Para solucionar este problema, inicie el proceso por lotes solo una vez y reinícielo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha. Lo mismo se aplica a una línea de contrato basada en proyectos.      
 
### <a name="edit-a-draft-invoice"></a>Editar un borrador de factura

Cuando se crea un borrador de factura de proyecto, todas las transacciones de venta sin facturar que se crearon cuando se aprobaron las entradas de tiempo y gastos se incluyen en la factura. Puede realizar los siguientes ajustes mientras facturación aún está en fase de borrador:

- Eliminar o editar los detalles de la línea de factura.
- Editar y ajustar la cantidad y el tipo de facturación.
- Agregar directamente a la factura el tiempo, los gastos, el material y las tarifas como transacciones. Puede usar esta característica si la línea de la factura se asigna a una línea de contrato que permita estas clases de transacciones.

Seleccione **Confirmar** para confirmar una factura. Esta acción es unidireccional. Cuando se selecciona **Confirmar**, la factura se convierte en factura de solo lectura y crea datos reales de ventas facturadas de todos los detalles de cada línea de factura. Si el detalle de la línea de factura hace referencia a un dato real de ventas sin facturar, se revierte el dato real de ventas sin facturar. Cualquier detalle de línea de factura que se haya creado a partir de una entrada de tiempo, gasto o utilización de material hará referencia a un valor real de ventas no facturadas. Los sistemas de integración de contabilidad general pueden utilizar esta reversión para revertir el trabajo en curso del proyecto (Trabajo en curso) con fines contables.

### <a name="correct-a-confirmed-invoice"></a>Corregir una factura confirmada

Las facturas confirmadas se pueden editar. Cuando se corrige una factura confirmada, se crea un nuevo borrador de factura correctiva. Puesto que se da por sentado que desea revertir todas las transacciones y las cantidades de factura original, esta factura correctiva incluye todas las transacciones de la factura original y todas sus cantidades son iguales a cero.

Si hay transacciones que no requieren corrección, puede quitarla del borrador de la factura correctiva. Si desea revertir o devolver solo una cantidad parcial, puede editar el campo **Cantidad** en el detalle de la línea. Si abre el detalle de la línea de factura, podrá ver la cantidad de la factura original. A continuación, podrá editar la cantidad de la factura actual para que sea superior o inferior a la cantidad de la factura original.

Cuando se confirma una factura correctiva, el dato real de ventas facturadas originales se revierte y se crea un nuevo dato real de ventas facturadas. Si la cantidad se redujo, la diferencia generará un nuevo dato real de ventas sin facturar. Por ejemplo, si la venta facturada original ascendía a ocho horas y el detalle de línea de factura correctiva tenía una cantidad reducida de seis horas, se revierte la línea de ventas facturadas originales y se crean dos nuevos datos reales:

- Un dato real de ventas facturadas por seis horas.
- Un dato real de ventas sin facturar por las dos horas restantes. Esta transacción se puede facturar más adelante o se puede marcar como no imputable, en función de las negociaciones con el cliente.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
