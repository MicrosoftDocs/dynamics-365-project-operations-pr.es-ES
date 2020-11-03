---
title: Configurar tarifas de costes y ventas para productos de catálogo
description: Este tema proporciona información sobre cómo configurar las tasas de costes y ventas para las elementos en un catálogo de producto.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085215"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Configurar tarifas de costes y ventas para productos de catálogo

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


La configuración de precios para los artículos del catálogo de productos en Dynamics 365 Project Operations es la misma que en Dynamics 365 Sales.

Debido a que los productos no se pueden estimar ni utilizar en proyectos en Project Operations, no es necesario establecer precios de catálogo de productos en las listas de precios del proyecto para cotizaciones y contratos.

Los precios del catálogo de productos deben configurarse en el campo **Precio del producto** de una cotización, contrato o cuenta. No configure precios de catálogo de productos en las listas de precios del proyecto para estas entidades. Las listas de precios del proyecto son exclusivas de Project Operations. Existe una lógica empresarial específica de la aplicación que copia las listas de precios de una cotización a un contrato. El resultado es una lista de precios de un proyecto específico del contrato. La operación de copia puede retrasar el proceso de obtención de cotización si la lista de precios del proyecto en la cotización es demasiado grande. Las listas de precios de productos no se copian para crear listas de precios personalizadas en los contratos. Esto significa que las listas de precios de los productos no afectan el rendimiento del proceso de cotización.
