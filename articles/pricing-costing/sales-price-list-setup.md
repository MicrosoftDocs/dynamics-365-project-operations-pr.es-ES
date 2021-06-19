---
title: Configurar una lista de precios de venta
description: En este tema se proporciona información sobre las listas de precios de ventas para precios de proyecto.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004912"
---
# <a name="set-up-a-sales-price-list"></a>Configurar una lista de precios de venta

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Para los contratos y las ofertas de proyecto, la lista de precios de proyectos cuenta con un patrón de reemplazo de precios distinto que el de la lista de precios de productos. En una línea de oferta basada en un catálogo de productos, puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta, porque cada línea de la oferta apunta exactamente a un elemento del catálogo. Sin embargo, en una línea de oferta basada en un proyecto, no puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta. Puede utilizar la lista de precios de proyecto para trabajar con los dos patrones de reemplazo distintos.

> [!NOTE]
> Se recomienda disponer de una lista de precios independiente para sus recursos de proyecto y sus elementos del catálogo debido a las diferencias de comportamiento entre las dos al reemplazar el cálculo de precios.

Cada una de las siguientes entidades puede tener una o varias listas de precios de ventas asociadas para el cálculo de precios de proyecto:

- Cliente (cuenta) 
- Oportunidad 
- Oferta 
- Contrato de proyecto

La asociación de estas entidades a una lista de precios se indica con las listas de precios de proyecto. Puede asociar una o más listas de precios a las entidades de ventas Cliente, Oportunidad, Oferta y Contrato de proyecto.

La lista de precios de proyecto predeterminada no se introduce automáticamente en los registros de cliente. Sin embargo, puede adjuntar manualmente una lista de precios de proyecto al registro de cliente. No obstante, deberá adjuntar manualmente una lista de precios de proyecto solo cuando tenga un acuerdo de precios personalizado con el cliente. 

Cuando una lista de precios de proyecto se adjunta una entidad de ventas, se valida la información siguiente:

- Si la lista de precios tiene un contexto de **Ventas**. 
- Si la divisa de la lista de precios coincide con la divisa del cliente. 

En un contrato de proyecto, se usa el siguiente orden de precedencia para establecer automáticamente las listas de precios de proyecto relacionadas:

1. Oferta
2. Oportunidad
3. Cliente 
4. Configuración global 

Cuando una lista de precios de proyecto se especifica de forma predeterminada, el sistema valida que la divisa coincida con la divisa del cliente y que las listas de precios predeterminadas que se han especificado tengan un contexto de **Ventas**.

Puede asociar varias listas de precios de proyecto a las entidades Cliente, Oportunidad, Oferta y Contrato de proyecto. Esta funcionalidad admite precios predeterminados con fecha específica para contratos de proyectos de larga duración en los que es posible que necesite más de una lista de precios para las actualizaciones de precios que se producen debido a la inflación. Sin embargo, si las listas de precios que asocie con las entidades Cliente, Oportunidad, Oferta o Contrato de proyecto tienen validez de fecha que se solapan, es posible que los precios predeterminados sean incorrectos. Por lo tanto, debe asegurarse de que no se asocian a dichas entidades listas de precios de proyecto que tienen fechas de validez que se solapan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]