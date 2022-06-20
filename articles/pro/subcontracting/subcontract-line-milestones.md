---
title: Hitos de línea de subcontrato
description: Este artículo explica cómo crear y mantener un calendario de facturas basado en hitos para un subcontrato con un proveedor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b146bf0becff5d0fa0da59f50c0d04aafaf5115f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927625"
---
# <a name="subcontract-line-milestones"></a>Hitos de línea de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

En Dynamics 365 Project Operations, una línea de subcontratos con un método de facturación de precio fijo puede especificar un programa de facturación basado en hitos con el proveedor.

Los hitos para la facturación de proveedores se pueden generar automáticamente usando una frecuencia establecida, o puede crearlos manualmente.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Cree automáticamente un programa de facturación basado en hitos para una línea de subcontrato

Complete los siguientes pasos para generar automáticamente un programa de facturación basado en hitos para un conjunto fijo de hitos distribuidos equitativamente.

1. Vaya a **Ajustes** > **Frecuencias de facturas** y configure la frecuencia de facturación para las líneas de subcontrato.
2. Abra la página **Subcontratos**, abra el subcontrato con el que desea trabajar y luego abra la línea de subcontrato de precio fijo para la que va a crear un cronograma de hitos.
3. En la pestaña **Hitos de la línea de subcontratación**, seleccione **Generar hitos periódicos**.
4. En el cuadro de diálogo, introduzca o seleccione un rango de fechas, el número de hitos y la frecuencia de facturación. Puede seleccionar una fecha de inicio, o puede seleccionar el número de hitos y la frecuencia de facturación o la fecha de inicio, o puede seleccionar la fecha de finalización y la frecuencia de facturación. No puede seleccionar la fecha de finalización y el número de hitos.
Con esta información, el sistema genera hitos y registros que se muestran en la cuadrícula **Hitos**.

   - **Nombre del hito**: el nombre del hito se establece en la fecha del hito en función de la frecuencia de facturación.
   - **Fecha del hito**: la fecha basada en la frecuencia de facturación.
   - **Importe del hito**: se calcula dividiendo la cantidad del importe en la línea de subcontrato por el número de hitos.

Si la línea de subcontrato tiene un valor en el campo **Importe de impuestos estimado**, este valor se agrega a cada hito por igual al generar hitos periódicos.

La suma de los importes de los hitos de la línea del subcontrato debe ser igual al valor de la línea de subcontratación. Si no son iguales, se produce un error. Puede corregir el error y verificar que el total de hitos sea igual al valor de la línea de subcontrato creando, editando o eliminando los importes de hitos e impuestos. Una vez realizados los cambios, guarde y actualice la página para asegurarse de que no haya más errores.

## <a name="manually-create-subcontract-line-milestones"></a>Crear manualmente hitos de líneas de subcontratos

Los hitos de precio fijo en una línea de subcontrato se pueden generar manualmente cuando no se dividen periódicamente. Para crear manualmente un hito de línea de subcontrato, siga estos pasos.

1. En el panel de navegación, seleccione **Subcontratos** y abra el subcontrato con el que quiere trabajar.
2. Abra la línea de subcontrato de precio fijo para la que desea crear un hito.
3. En la pestaña **Hitos de línea de subcontrato**, en la subcuadrícula, seleccione **+ Nuevo hito de línea de subcontrato**.
4. En la página **Nuevo hito de línea de subcontrato**, introduzca la información requerida basada en la tabla siguiente.

    | Campo | Descripción |Impacto funcional|
    | --- | --- |----------------------|
    | Nombre del hito | El nombre del hito. |Esto se mostrará como la primera columna en todas las búsquedas basadas en hitos de la línea de subcontratación. La línea de la factura de proveedor que se crea en base a este hito también utilizará el nombre del hito de la línea de subcontratación como nombre predeterminado de la línea de factura de proveedor.|
    | Descripción | Una descripción del hito. |La línea de la factura de proveedor que se crea en base a este hito también utilizará la descripción del hito de la línea de subcontratación como descripción predeterminada de la línea de factura de proveedor.|
    | Fecha de hito | La fecha en la que el proceso de creación automática de facturas debe buscar el estado de este hito para considerarlo para la facturación.| Este valor se utilizará como la fecha predeterminada de la línea de factura del proveedor al facturar esta línea de subcontratación. |
    | Cantidad | El importe o valor del hito que se facturará al cliente. |Este valor se utiliza como importe predeterminado en la línea de factura del proveedor al facturar esta línea de subcontratación. |
    | Impuestos | La cantidad del impuesto aplicado al hito.| Este valor se utiliza como importe de impuesto predeterminado en la línea de factura del proveedor al facturar esta línea de subcontratación. |
    | Importe después de impuestos | Este campo de solo lectura se calcula como importe contratado + impuestos.|Este valor se utiliza como predeterminado en la línea de factura del proveedor al facturar esta línea de subcontratación. |
    | Estado de la factura | Cuando se crea el hito, este estado siempre se establece en **No listo para facturar**.|  Cuando el estado es **Listo para facturar**, la creación de la factura del proveedor incluye este hito en la factura del proveedor. |

5. Seleccione **Guardar y cerrar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
