---
title: Pedidos de venta de proyectos para proyectos de tiempo y materiales
description: Este tema explica cómo crear pedidos de cliente basados en proyectos para proyectos de tiempo y materiales.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085133"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Pedidos de venta de proyectos para proyectos de tiempo y materiales

[!include[banner](../includes/banner.md)]

Este tema describe cómo crear un pedido de cliente para un proyecto. Los pedidos de venta solo se pueden crear para proyectos de tipo **tiempo y material**.

Si un proyecto de tiempo y material tiene varias fuentes de financiación en el contrato del proyecto, debe habilitar el parámetro **Permitir pedidos de ventas para proyectos con múltiples fuentes de financiación** en la página **Parámetros de gestión de proyectos y contabilidad**. 

> [!NOTE]
> - El soporte para pedidos de ventas de proyectos con múltiples fuentes de financiación está disponible a partir de la versión de aplicación 10.0.2 y superiores.
> - El parámetro para habilitar el soporte para pedidos de ventas de proyectos con múltiples fuentes de financiación se eliminará en el lanzamiento de versiones de abril de 2020, después de lo cual la funcionalidad siempre estará habilitada.

Puede crear pedidos de cliente basados en proyectos de dos formas:

- Vaya al propio proyecto. En el panel de acciones, seleccione **Administrar > Tareas de artículo > Pedido de venta**. La información del proyecto se establecerá de forma predeterminada en el pedido de venta del proyecto. Si el contrato del proyecto tiene más de una fuente de financiación, deberá seleccionar la fuente de financiación para configurar el cliente para el pedido de venta. Si solo hay una fuente de financiación para el proyecto, el cliente se configurará automáticamente.
- Vaya la página de la lista **Todos los pedidos de venta** y cree un nuevo pedido de venta. Deberá seleccionar el proyecto para el pedido de venta. Después de seleccionar el proyecto, el cliente se establecerá a partir de la fuente de financiación o deberá seleccionar la fuente de financiación si el contrato del proyecto tiene varias fuentes de financiación.
