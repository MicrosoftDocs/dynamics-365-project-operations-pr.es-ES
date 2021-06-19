---
title: Configurar tarifas de costes y ventas para productos de catálogo (lite)
description: Este tema proporciona información sobre cómo configurar las tasas de costes y ventas para las elementos en un catálogo de producto.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004362"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar tarifas de costes y ventas para productos de catálogo (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


La configuración de precios para artículos del catálogo de productos de Dynamics 365 Project Operations es la misma que en Dynamics 365 Sales.

En Project Operations, los productos no se pueden estimar ni usar en proyectos, por lo que no es necesario establecer los precios del catálogo de productos en las listas de precios de proyecto para ofertas y contratos.

Use el campo **Precio del producto** de una oferta, un contrato o una cuenta para configurar los precios del catálogo de productos. No configure los precios de catálogo de productos en las listas de precios de proyecto. Las listas de precios del proyecto son exclusivas de Project Operations. La lógica empresarial específica de la aplicación copia las listas de precios de una oferta a un contrato. El resultado es una lista de precios de un proyecto específico del contrato. La operación de copia puede retrasar el proceso de obtención de cotización si la lista de precios del proyecto en la cotización es demasiado grande. Las listas de precios de productos no se copian para crear listas de precios personalizadas en los contratos. Como no se realiza una copia, el rendimiento del proceso de oferta no se ve afectado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]