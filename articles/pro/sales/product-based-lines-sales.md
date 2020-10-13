---
title: Líneas de oportunidad basadas en productos
description: Este tema proporciona información sobre artículos de líneas de oportunidades basadas en proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896257"
---
# <a name="product-based-opportunity-lines"></a>Líneas de oportunidad basadas en productos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las líneas de oportunidad basadas en productos son elementos de línea de la oportunidad. Estas líneas se entregan al cliente como artículos de línea distintos en la factura final sin ningún otro servicio de valor agregado. El gasto y el consumo asociados no se registran en las tareas de ningún proyecto relacionado.

Las líneas basadas en productos pueden ser artículos de catálogo o productos fuera de catálogo. La mayor parte de la funcionalidad de las líneas basadas en productos de una oportunidad sigue la funcionalidad proporcionada por la aplicación Dynamics 365 Sales. Para obtener más información sobre las líneas de oportunidad basadas en productos, consulte [Agregar productos a una oportunidad](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Un concepto sobre las líneas de oportunidades basadas en productos que es específico de las oportunidades basadas en proyectos es **Presupuesto del cliente**. Utilice este campo para realizar un seguimiento de la cantidad que el cliente está dispuesto a pagar por el artículo de línea.

Si el método de ingresos del resumen de oportunidades se establece en **Calculado por el sistema**, los valores del presupuesto del cliente en las líneas basadas en productos y proyectos se resumen para calcular los ingresos estimados.
