---
title: Verificación de facturas de proveedores con datos reales aprobados
description: Este artículo explica cómo Microsoft Dynamics 365 Project Operations permite a los gerentes de proyecto verificar las facturas de los proveedores con los datos reales que se aprobaron cuando los contratistas realizaron el trabajo y registraron el tiempo, y los gastos y materiales que usaron los miembros del equipo del proyecto.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914239"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificación de facturas de proveedores con datos reales aprobados

[!include [banner](../../includes/dataverse-preview.md)]

**Se aplica a:** implementación simplificada: del acuerdo a la facturación proforma

Microsoft Dynamics 365 Project Operations permite a los gerentes de proyecto verificar las líneas de factura de proveedor de las siguientes maneras:

- Utilizar el campo **Estado de verificación** en las líneas de factura de proveedor.
- Si las líneas de factura del proveedor hacen referencia a una línea de subcontrato, vincule los datos reales de costos de la actividad del subcontratista a esas líneas de factura del proveedor. El enlace se crea haciendo coincidir los datos reales de costos con las líneas de factura del proveedor.

    > [!NOTE]
    > Aunque se puede realizar un seguimiento del estado de verificación de las líneas de factura del proveedor que no hacen referencia a un subcontrato, los datos reales de costos no se pueden vincular a esas líneas de factura del proveedor.

## <a name="verification-status"></a>Estado de la verificación

El campo **Estado de verificación** en una línea de factura de proveedor indica el estado de la verificación. Se admiten los siguientes estados:

1. Sin iniciar
2. En curso
3. Completa

Pueden editarse las líneas de factura de proveedor que tengan un estado de verificación **No iniciado**.

Ya no pueden editarse las líneas de factura de proveedor que tengan un estado de verificación **En curso**. Para una línea de factura de proveedor que hace referencia a un subcontrato, el estado de verificación se establece automáticamente en **En curso** tan pronto como el primer costo real coincida con la línea de factura del proveedor.

Ya no pueden editarse las líneas de factura de proveedor que tengan un estado de verificación **Completado**. Cuando todas las líneas de una factura de proveedor tienen este estado de verificación, puede confirmarse la factura del proveedor.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Hacer coincidir los datos reales de coste con las líneas de factura de proveedor

La conciliación de los datos reales de costos ayuda con el proceso de verificación de una línea de factura de proveedor. Para hacer coincidir los datos reales de costos con una línea de factura de proveedor, siga estos pasos.

1. Abra la línea de factura de proveedor y seleccione la pestaña **Datos reales de costos no coincidentes**. Una cuadrícula muestra una lista de datos reales de costos que hacen referencia a la misma línea de subcontrato que la línea de factura del proveedor.
2. Seleccione uno o más de los costos reales y luego seleccione **Coincidencia** en la barra de herramientas de encima de la cuadrícula. El sistema valida que se puedan conciliar los datos reales de costos seleccionados. Después de pasar la validación, los datos reales de costos se vinculan a la línea de factura del proveedor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criterios de validación que se utilizan para vincular datos reales de costos a líneas de factura de proveedor

Durante el proceso de coincidencia, se puede establecer un vínculo entre un costo real y una línea de factura de proveedor solo si se cumplen las dos condiciones siguientes:

- El campo **Estado de ajuste** de cada costo real seleccionado debe estar en blanco. En otras palabras, los costos reales no deben haberse reemplazado por otros costos reales durante un proceso de coincidencia, cancelación de aprobación o diario de corrección.
- Los valores de los siguientes campos se comparan entre la línea de factura del proveedor y el costo real seleccionado. Si algún campo no está configurado en la línea de la factura del proveedor, no se considera para la conciliación.

    - Contrato de proyecto
    - Línea de contrato de proyecto
    - Clase de transacción
    - Project
    - Task
    - Categoría de recursos
    - Categoría de transacción
    - Producto
    - Línea de subcontrato
    - Recurso que se puede reservar

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Hacer no coincidir los datos reales de coste con una línea de factura de proveedor

La desvinculación de los costos reales también puede ayudar con el proceso de verificación en una factura de proveedor al permitir que se eliminen los enlaces establecidos previamente. Los datos reales de coste pueden hacerse dejar de coincidir en las líneas de factura de proveedor que tengan un estado de verificación **En curso**. Para dejar de hacer coincidir los datos reales de costos de una línea de factura de proveedor, siga estos pasos.

1. Abra la línea de factura de proveedor y seleccione la pestaña **Datos reales de costos coincidentes**. Una cuadrícula muestra una lista de datos reales de costos que hacen referencia a la misma línea de subcontrato que la línea de factura del proveedor.
2. Seleccione uno o más de los costos reales y luego seleccione **Dejar de coincidir** en la barra de herramientas de encima de la cuadrícula.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
