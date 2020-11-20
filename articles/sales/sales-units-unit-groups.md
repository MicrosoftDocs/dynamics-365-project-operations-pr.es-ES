---
title: Unidades y unidades de venta
description: En este tema se proporciona información sobre cómo crear unidades y unidades de venta en Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131049"
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
