---
title: Líneas de factura de proveedor de hitos
description: Este tema explica cómo crear líneas de factura de proveedor para hitos en un subcontrato.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590643"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Líneas de factura de proveedor de hitos

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una factura de proveedor en Microsoft Dynamics 365 Project Operations puede tener líneas de factura de proveedor para hitos definidos en una línea de subcontrato. Los administradores de proyecto pueden usar líneas de factura de proveedor para hitos, para registrar los costos de los servicios que se adquieren como costos basados en hitos en los que se incurre en los servicios o productos que se adquieren para el proyecto.

Las líneas de factura de proveedor para hitos siempre deben hacer referencia a una línea de subcontrato que tenga un método de facturación de precio fijo. Si una línea de factura de proveedor para hitos hace referencia a una línea de subcontrato, los administradores de proyectos podrán comparar y verificar los costes de tiempo, gastos o materiales subyacentes que hacen referencia a la línea de subconttrato frente al hito que factura el proveedor.

La siguiente tabla proporciona información sobre los campos de las líneas de factura de proveedor para hitos.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | El nombre de la línea de factura de proveedor, para ayudar con la identificación. | Este nombre se mostrará como la primera columna en todas las búsquedas basadas en líneas de factura de proveedor. |
| Description | Una breve descripción de los servicios que se facturan por parte del proveedor en la línea de factura del proveedor. | None |
| Subcontrato | El subcontrato en el que se pidieron originalmente los servicios. | Cuando se selecciona un subcontrato para la factura del proveedor, todas las líneas de la factura del proveedor heredarán esa selección. Una factura de proveedor no puede tener líneas de factura de proveedor que hagan referencia a diferentes subcontratos. |
| Línea de subcontrato | La línea de subcontrato en la que se pidieron los servicios. La lista de líneas de subcontrato que se pueden seleccionar se limita a las líneas del subcontrato seleccionado. | Cuando se selecciona una línea de subcontrato en una línea de factura de proveedor para hitos, los campos **Rol** y **Categoría de transacción** y los campos relacionados con el producto son irrelevantes y no están disponibles. Los campos **Cantidad**, **Unidad** y **Unidad de venta** tampoco son relevantes para las líneas de factura de proveedor basadas en hitos. |
| Fecha de la transacción | La fecha en que se registrará en el proyecto el costo real de la línea de factura del proveedor. | None |
| Clase de transacción | Seleccione **Hito** para registrar una factura de proveedor para un hito completado que se definió en una línea de subcontrato. | None |
| Hito | Seleccione el hito que se define en la línea de subcontrato relacionada marcada como **Listo para Facturar**. | No se pueden seleccionar hitos de línea de subcontrato con un estado **Listo para facturar** en una línea de factura de proveedor. |
| Project | El nombre del proyecto en el que se utilizaron los servicios que se están facturando. | Este campo es obligatorio y no se puede dejar en blanco. |
| Task | El nombre de la tarea del proyecto en la que se utilizaron los servicios que se están facturando. Este campo está disponible solo si se selecciona un proyecto. La selección de una tarea de proyecto es opcional. | Si este campo se deja en blanco, el director del proyecto puede hacer coincidir la línea de la factura del proveedor con la clase de transacciones de la línea d subcontratista relacionada que se registra en cualquier tarea del proyecto. Si la línea de factura del proveedor no hace referencia a una línea de subcontrato y este campo se deja en blanco, el costo real creado por la línea de factura del proveedor no se vinculará a ningún dato real de ventas no facturado. En este caso, si se configura la facturación basada en tareas, es posible que los costos no se puedan facturar al cliente final. |
| Importe del hito | Introduzca el valor del hito que se define en la línea de subcontrato relacionadaque está lista para facturar. | None |
| Impuesto sobre las ventas | Especifique el importe del impuesto sobre las ventas. | None |
| Importe total | El importe total de la línea de factura del proveedor, incluidos los impuestos. Este campo se calcula como *Importe de hito* + *impuestos*. | None |

> [!NOTE]
> Cuando se crea una línea de factura de proveedor que hace referencia a un hito de línea de subcontrato, el estado del hito de subcontrato se actualiza a **Factura de proveedor creada**. Luego, cuando se confirma la factura del proveedor, el estado del hito de la línea de subcontrato se actualiza a **Factura del proveedor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
