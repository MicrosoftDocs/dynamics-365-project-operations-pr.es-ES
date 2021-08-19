---
title: Revisión del trabajo pendiente de facturación en proyectos y contratos de proyecto
description: En este tema se proporciona información sobre cómo revisar los trabajos pendientes en los productos, los gastos y el tiempo, y cómo marcarlos como listos para la facturación.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: fb2f267c626126302a6afb6adba6070dedce4b030abc761e32b23df174d49ecb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006987"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Revisión del trabajo pendiente de facturación en proyectos y contratos de proyecto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Cuando una transacción está lista para crear y procesar una factura, la transacción debe marcarse como **Listo para facturar**. Este tema describe los tipos de transacciones que se pueden crear.

## <a name="review-the-time-and-material-billing-backlog"></a>Revisión del tiempo y trabajo pendiente de facturación de material

Cuando se presenta y aprueba una entrada de tiempo o gasto para un proyecto, PSA crea un proyecto real. Si la combinación del proyecto y la clase de transacción se asignan a una línea de contrato para un proyecto de tiempo y materiales, se crean dos datos reales cuando se aprueba la entrada:

- Coste real 
- Dato real de ventas sin facturar

Los datos reales de ventas sin facturar representan el trabajo pendiente de facturación y su estado de facturación debe establecerse en **Listo para facturar**. Cuando se crea una factura de proyecto, los datos reales de ventas sin facturar que están marcados como **Listo para facturar** se copian como detalles de línea de factura.

Para revisar el trabajo pendiente de facturación de tiempo y materiales, vaya a **Ventas** \> **Facturación** \> **Trabajo pendiente de facturación de tiempo y material**. Seleccione todos los datos reales de ventas sin facturar que estén listos para facturar y, a continuación, seleccione **Listo para facturar**. El estado de facturación de esos datos reales cambia a **Listo para facturar**.

![Trabajo pendiente de facturación de tiempo y material.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Revisión del trabajo pendiente de facturación de productos

En PSA, cuando un contrato de proyecto tiene líneas de contrato basadas en productos, esas líneas se consideran para facturación cada vez que se crea una factura para el contrato de proyecto. Cualquier producto que tenga líneas contractuales marcadas **Listo para facturar** se copiará en la factura del proyecto como líneas de factura del proyecto.

Para revisar la cartera de facturación de productos, vaya a **Ventas** \> **Facturación** \> **Trabajo pendiente de facturación de productos**. Seleccione todas las líneas de contrato basadas en productos que estén listas para facturarse, y, a continuación, seleccione **Listo para facturar**. El estado de facturación de estas líneas cambia a **Listo para facturar**.

![Trabajo pendiente de facturación de productos.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Revisión de hitos de facturación en contratos de precio fijo

Las líneas de contrato de proyecto que tienen un método de facturación de precio fijo deben definir hitos del contrato. Estos hitos del contrato solo se pueden facturar si están marcados como **Listo para facturar**. 

Para revisar los hitos de facturación, vaya a **Ventas** \> **Facturación** \> **Hitos de precio fijo**. Seleccione los hitos que están listos para facturar y, a continuación seleccione **Listo para facturar**. El estado de facturación de estos hitos cambia a **Listo para facturar**.

![Hitos de precio fijo.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]