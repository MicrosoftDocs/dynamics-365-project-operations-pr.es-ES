---
title: 'Novedades de septiembre de 2022: implementación de Project Operations Lite'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de septiembre de 2022 de la implementación simplificada de Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634874"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novedades de septiembre de 2022: implementación de Project Operations Lite

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.46.0.60

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

| Área de características | Nombre de característica | Más información |
| --- | --- | --- |
| Administración de oportunidades | **Revisión y activación de ofertas**<br>Project Operations brinda el soporte completo del proceso de ventas. Las cotizaciones de proyectos se pueden activar para representar un estado en el que la cotización es de solo lectura y se está revisando. Las cotizaciones activadas se pueden revisar para crear nuevas cotizaciones que tengan un número de revisión incrementado. Las cotizaciones de proyectos activadas o las revisiones de cotizaciones se pueden cerrar como ganadas o perdidas. | [Activar y revisar una oferta de proyecto](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturación y precios | **Incumplimiento de precio agnóstico de zona horaria**<br>Project Operations ha introducido el concepto de una fecha agnóstica de zona horaria en todos los datos reales del proyecto. Un campo nuevo, **Fecha de transacción**, ahora está disponible en líneas de diario y datos reales, y se usará para almacenar la fecha en que ocurrió la transacción, pero sin convertir esa fecha a la hora universal coordinada. Esta fecha se utilizará para procesos posteriores, como el incumplimiento de precios y la creación de facturas. | <p>[Determinar tasas de costes para estimaciones y datos reales que se basan en proyectos](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar precios de venta para estimaciones y datos reales de proyectos](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturación y precios | **Sustituciones de precios con fecha de vigencia en Project Operations**<br>Reemplazos de precios de la fecha de vigencia proporciona una forma de anular o cambiar precios específicos en la lista de precios. | [Reemplazos de precios de la fecha de vigencia](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Tiempo y gasto | **Aprobador global**<br>Esta función permite la aprobación centralizada de proveedores de software independientes (ISV), independientemente del estado del proyecto o del miembro del equipo en el proyecto. | [Seguridad y aprobaciones](/dynamics365/project-operations/approvals/approvals-security) |
|Planificación y seguimiento de proyectos|**Usar las API de programación de proyectos para realizar operaciones con entidades de programación** </br> </br>La API de edición de contorno de asignación de recursos permite a los desarrolladores especificar mediante programación el esfuerzo de un asignado a la tarea en cualquier intervalo de fechas compatible para una planificación de esfuerzo por fases más granular.|[Usar las API de programación de proyectos para realizar operaciones con entidades de programación](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2754422 | Las estimaciones de gastos y materiales no fluyen a Dynamics 365 Finance cuando los proyectos se copian en Dataverse. |
| Tiempo y gasto | 2787409 | Un aprobador no válido puede aprobar una entrada de tiempo que no sea de proyecto. |
| Administración de oportunidades | 2788907 | Mensaje de error actualizado sobre la validación de exclusividad para líneas de pedido que incluyen marcas. |
| Tiempo y gasto | 2842253 | Manejo de excepciones nulas para aprobación de tiempo. |
| Facturación y precios | 2844181 | Si no se obtiene el ID de correlación, se bloquea la creación de facturas. |
| Facturación y precios | 2876628 | QLD, CLD: la resolución estimada de la lista de precios debe usar campos de rango de fechas heredados de la lista de precios. |
| Subcontratación | 2893222 | Si no se especifica un rol para una línea de subcontrato, debería ser posible seleccionar esa línea en un miembro del equipo para cualquier rol. |
