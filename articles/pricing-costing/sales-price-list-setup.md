---
title: Configuración de lista de precios de venta
description: En este tema se proporciona información sobre las listas de precios de ventas para precios de proyecto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896482"
---
# <a name="sales-price-list-setup"></a>Configuración de lista de precios de venta

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
