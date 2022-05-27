---
title: Configurar tarifas de costes y ventas para materiales
description: Este tema proporciona información sobre cómo configurar los costes y las tasas de ventas de los materiales utilizados en los proyectos.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576889"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Configurar tarifas de costes y ventas para materiales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede configurar precios de costes y ventas para productos en Dynamics 365 Project Operations. Los precios de coste y venta de los productos solo se pueden enumerar en una divisa, que debe ser la divisa en el encabezado de la lista de precios.

Para configurar los costes y las tasas de ventas de los productos, complete los siguientes pasos. 

1. Vaya a **Ventas** > **Clientes** > **Lista de precios** y seleccione **Nuevo** para crear una nueva lista de precios. 
2. En **Elementos de lista de precios**, en el menú de la subcuadrícula, seleccione **Nuevo elemento de lista de precios**. 
3. En la página **Creación rápida**, especifique el producto y la unidad para los que está creando el nuevo precio.

Para obtener más información sobre cómo definir precios para artículos de catálogo, consulte [Definir precios de productos con listas de precios y elementos de lista de precios](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) y [Precisión decimal en moneda y precio](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations no admite todos los métodos de fijación de precios para productos como Dynamics 365 Sales. El único método de fijación de precios admitido para los productos que se utilizarán en proyectos es *Importe de divisa*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
