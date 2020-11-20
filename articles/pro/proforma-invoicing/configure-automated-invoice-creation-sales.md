---
title: Configurar la creación automática de facturas (lite)
description: En este tema se proporciona información sobre cómo configurar la creación automática de facturas proforma.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176587"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Configurar la creación automática de facturas (lite)
 
_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Puede configurar la creación automática de facturas en Dynamics 365 Project Operations. El sistema crea un borrador de factura proforma basada en la programación de facturas para cada contrato de proyecto y línea de contrato. Los programas de facturación se configuran a nivel de línea de contrato. Cada línea de un contrato puede tener una programación de facturas distinta, o se puede incluir la misma programación de facturas en cada línea del contrato.

Cuando crea una factura, el sistema siempre crea al menos una factura por contrato de proyecto. En algunos casos, puede haber varias facturas creadas.

Por ejemplo, si el contrato tiene varios clientes, se creará el mismo número de facturas que el número de clientes que tienen transacciones facturables para facturar en ese contrato de proyecto.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Comprender cómo se incluyen las transacciones en una factura 

A veces, cada línea de contrato basada en el proyecto especifica un cronograma de facturación por separado. Por ejemplo, los servicios de implementación para el contrato Adatum tienen las siguientes líneas de contrato:

- Prototipo de trabajo a precio fijo con dos hitos creados manualmente.
- Trabajos de implementación que incluyen horas y se facturarán quincenalmente los lunes.
- Gastos incurridos que deben facturarse mensualmente el primer lunes de cada mes.

Los programas de facturación definidos en cada una de estas dos líneas de pedido se parecen a la siguiente tabla:

| Línea de contrato | Fecha de ejecución de la factura | Fecha límite de la transacción | Fecha de hito | Importe del hito |
| --- | --- | --- | --- | --- |
| Prototipo de trabajo | Lunes 5 de octubre | - | Lunes 5 de octubre | 5000 USD |
| - | Martes 3 de diciembre | - | Martes 3 de diciembre | 12 000 USD |
| Trabajo de implementación | Lunes 5 de octubre | Domingo 4 de octubre | - | - |
| - | Lunes 19 de octubre | Domingo 18 de octubre | - | - |
| - | Lunes 2 de noviembre | Domingo 1 de noviembre | - | - |
| - | Lunes 16 de noviembre | Domingo 15 de noviembre | - | - |
| Gastos incurridos | Lunes 5 de octubre | Domingo 4 de octubre | - | - |
| - | Lunes 2 de noviembre | Domingo 1 de noviembre | - | - |

En este ejemplo, cuando la facturación automática se ejecuta en:

- **4 de octubre o cualquier fecha anterior**: no se genera ninguna factura para este contrato porque la tabla de **Programación de facturas** para cada una de estas líneas de contrato no indica el 4 de octubre, domingo, como fecha de ejecución de la factura.
- **5 de octubre lunes**: se genera una factura para:

    - Trabajo de prototipo que incluye el hito, si está marcado como **Listo para facturar**.
    - Trabajo de implementación que incluye todas las transacciones de horas creadas antes de la fecha de cierre de la transacción del 4 de octubre, domingo, que está marcada como **Listo para facturar**.
    - Gastos incurridos que incluye todas las transacciones de gastos creadas antes de la fecha de cierre de la transacción del 4 de octubre, domingo, que está marcada como **Listo para facturar**.
  
- **6 de octubre o cualquier fecha anterior al 19 de octubre**: no se genera ninguna factura para este contrato ya que la tabla de **Programación de facturas** para cada una de estas líneas de contrato no indica el 6 de octubre o cualquier fecha previa al 19 de octubre, como fecha de ejecución de la factura.
- **19 de ocutbre, lunes:** se genera una factura para implementación que incluye todas las transacciones de horas creadas antes de la fecha de cierre de la transacción del 18 de octubre, domingo, que está marcada como **Listo para facturar**.
- **2 de noviembre lunes**: se genera una factura para:

    - Trabajo de implementación que incluye todas las transacciones de horas creadas antes de la fecha de cierre de la transacción del 1 de noviembre, domingo, que está marcada como **Listo para facturar**.
    - Gastos incurridos que incluye todas las transacciones de gastos creadas antes de la fecha de cierre de la transacción del 1 de noviembre, domingo, que está marcada como **Listo para facturar**.

- **martes 3 de noviembre**: se genera una factura para el trabajo de prototipo que incluye el hito de 12 000 USD, si está marcado como **Listo para facturar**.

## <a name="configure-automatic-invoicing"></a>Configurar facturación automática

Complete estos pasos para configurar la ejecución automática de facturas.

1. En **Operaciones de proyecto**, vaya a **Configuración** > **Configuración de facturas recurrentes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**. El nombre del trabajo por lotes debe incluir las palabras "creación de facturas".
3. En el campo **Tipo de trabajo**, seleccione **Ninguno**. De forma predeterminada, laos campos **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registros**, se mostrarán tres flujos de trabajo:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y después seleccione **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. El flujo de trabajo **Reposo** va seguido de un flujo de trabajo **Proceso**. 

> [!NOTE]
> También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea realmente las facturas. El flujo de trabajo pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas. Para determinar las líneas de contrato para las que se deben crear facturas, el trabajo busca fechas de ejecución de facturas para las líneas de contrato. Si hay líneas de contrato que pertenecen a un contrato que tiene la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para crear facturas, el trabajo omite la creación de una factura.

Cuando finaliza la ejecución de **ProcessRunner**, se llama al flujo de trabajo **ProcessRunCaller**, que proporciona la hora de finalización y después se cierra. A continuación, **ProcessRunCaller** pone en marcha un temporizador que se ejecuta durante 24 horas desde la hora de finalización especificada. Cuando se agota el tiempo del temporizador, el flujo de trabajo **ProcessRunCaller** se cierra.

El trabajo del proceso por lotes para la creación de facturas es un trabajo recurrente. Si este proceso por lotes se ejecuta muchas veces, se crean varias instancias del trabajo y se generan errores. Por lo tanto, debe iniciar el proceso por lotes solo una vez y después reiniciarlo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes en Project Operations solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha.