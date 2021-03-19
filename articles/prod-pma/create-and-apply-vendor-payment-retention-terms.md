---
title: Crear y aplicar términos de retención de pagos de proveedores
description: Este tema proporciona información sobre cómo configurar y mantener los términos de retención para los pagos a proveedores.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270969"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Crear y aplicar términos de retención de pagos de proveedores

[!include [banner](../includes/banner.md)] 

La configuración de los términos de retención de pagos de proveedores para un proyecto es útil cuando su organización desea retener parte de los pagos realizados a un proveedor. Por ejemplo, cuando desee retener el pago a un proveedor hasta que los productos entregados cumplan con sus expectativas. Los términos de retención de pago del proveedor se pueden especificar cuando se negocia un contrato con el proveedor.

## <a name="create-vendor-payment-retention-terms"></a>Crear términos de retención de pagos de proveedores

Puede introducir el porcentaje del pago del proveedor para la retención y el porcentaje de las cantidades retenidas previamente que se liberarán. Los importes se retienen automáticamente en las facturas del proveedor hasta que el contrato alcanza el estado especificado de finalización. Después de configurar los términos de retención, puede aplicarlos a cualquier proyecto para ese proveedor.

Utilice los siguientes pasos para configurar y mantener los términos de retención para los pagos a proveedores. 

1. Vaya a **Gestión de proyectos y contabilidad** > **Retencion** > **Condiciones de retención de pago del proveedor**.
2. Seleccione **Nuevo** para agregar un nuevo plazo de retención de proveedores. El valor **Identificador de regla** para el nuevo término se ingresa automáticamente. 
3. Introduzca una breve descripción en el campo **Descripción** y en la ficha desplegable **Términos**, seleccione **Agregar línea** para ingresar valores de término para lo siguiente:

   - **Porcentaje de unidades entregadas**: introduzca un porcentaje de finalización del período. Los importes se retienen automáticamente en las facturas del proveedor hasta que la fase de finalización del proyecto iguale al porcentaje especificado. Por ejemplo, si introduce 50,00, las cantidades se retienen hasta que el proyecto se completa en un 50 por ciento.
   - **Porcentaje a retener**: introduzca un porcentaje del monto de la factura del proveedor que se retendrá. Por ejemplo, si introduce 10,00, el 10 por ciento del monto de la factura de un proveedor se retiene hasta que el proyecto alcanza el porcentaje de finalización establecido en el **Campo Porcentaje de unidades entregadas**.
   - **Porcentaje para liberar**: seleccione **Agregar línea** para introducir un porcentaje de los montos retenidos previamente que se liberarán para el nivel seleccionado de finalización del proyecto.

> [!NOTE]
> Si tiene más de un hito para diferentes niveles de finalización del proyecto, ingrese una línea de plazo de retención de proveedor separada para cada regla de retención. Cada línea puede especificar un porcentaje de retención diferente y un porcentaje de liberación diferente para cada nivel designado de finalización del proyecto.

Después de crear los términos de retención de proveedor para un proveedor, puede aplicar los términos a un proyecto.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicar términos de retención de proveedores a un proyecto

1. Vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos** y abra un proyecto desde la página de lista de proyectos.
2. En la ficha desplegable **Acuerdos de proveedor**, seleccione **Agregar línea**.
3. En el campo **Código de cuenta**, seleccione una de las siguientes opciones: 

   - **Tabla**: los términos de retención de proveedor se aplican a un solo proveedor.
   - **Grupo**: los términos de retención de proveedor se aplican a todos los proveedores de un grupo de proveedores.
   - **Todos**: los términos de retención de proveedor se aplican a todos los proveedores.

4. En el **Proveedor/ campo de grupo de proveedores**, seleccione el proveedor o el grupo de proveedores al que se aplican los términos de retención de proveedores. Si seleccionó **Todos** en el paso anterior, este campo no está disponible.
5. En el campo **Términos de retención de proveedores**, seleccione los términos de retención que creó en el procedimiento anterior.
6. Si el proyecto también tiene términos de pago cuando se paga (PWP) configurados para el proveedor, introduzca el porcentaje de umbral para el proyecto en el campo **Porcentaje de umbral de PWP**.

Los términos de retención de proveedores también se muestran en las órdenes de compra que crea para el proveedor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]