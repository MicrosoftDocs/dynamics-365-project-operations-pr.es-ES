---
title: Unidades y unidades de venta
description: Este tema proporciona información sobre cómo crear unidades y unidades de venta en Dynamics 365 Project Operations.
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
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996092"
---
# <a name="units-and-unit-groups"></a>Unidades y unidades de venta

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las unidades son las cantidades o medidas en las que vende sus productos o servicios. Por ejemplo, si vende suministros para jardinería, es posible que venda semillas en unidades de paquetes, cajas y pallets. Una unidad de venta constituye el conjunto de estas diferentes unidades.

Para completar los pasos de este tema, asegúrese de que se le haya asignado el rol de Administrador del sistema o Administrador de Sales Professional o tenga permisos equivalentes.

## <a name="create-a-unit-group"></a>Creación de unidades de venta

1. En el mapa del sitio, seleccione **Unidades**.
2. Seleccione **Nuevo** y, en el cuadro de diálogo, **Crear unidad de venta**, introduzca el nombre de la unidad.
3. En el campo **Unidad principal**, introduzca la unidad de medida mínima común por la que se venderá el producto. Por ejemplo, puede introducir "pieza" u "onza".
4. Seleccione **Aceptar**.

## <a name="add-units-to-a-unit-group"></a>Agregar unidades a una unidad de venta

1. Abra una unidad de venta y en la pestaña **Relacionado**, seleccione **Unidades**. Verá que la unidad principal ya está agregada.
2. Seleccione **Agregar nueva unidad** y, en la página **Creación rápida: unidad**, en el campo **Nombre**, introduzca el nombre de la unidad.
3. En el campo **Cantidad**, introduzca la cantidad que contendrá la unidad. Por ejemplo, si una caja contiene dos piezas, introduzca "2". 
4. En el campo **Unidad base**, seleccione una unidad base para establecer la unidad de medida más baja para la unidad. Por ejemplo, puede seleccionar "Pieza".
5. Seleccione **Guardar**:


[!INCLUDE[footer-include](../includes/footer-banner.md)]