---
title: Desactivar listas de precios
description: Este tema explica cómo desactivar o eliminar listas de precios antiguas o no utilizadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001357"
---
# <a name="deactivate-price-lists"></a>Desactivar listas de precios 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Para eliminar listas de precios antiguas o no utilizadas en Dynamics 365 Project Operations, hay dos pasos que debe completar. 

1. Quite o elimine la lista de precios de páginas específicas.
2. Desactive o elimine la lista de precios de las listas de precios activas en la página **Lista de precios**.

>[!IMPORTANT]
> Debe completar ambos pasos para eliminar por completo una lista de precios. No basta con realizar el paso 2, que consiste en eliminar o desactivar directamente la lista de precios de la vista Listas de precios activas. También debe eliminar la asociación de esta lista de precios de todos los lugares mencionados en el paso 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Eliminar la lista de precios de páginas específicas
1. Para eliminar una lista de precios de Project Operations, vaya a las siguientes páginas:  

      - Página **Parámetros del proyecto** > pestaña **Listas de precios**
      - Página **Unidad organizativa** > cuadrícula **Lista de precios**
      - Página **Cuenta** > cuadrícula **Listas de precios del proyecto**
      - Página **Cotizaciones del proyecto** > cuadrícula **Listas de precios del proyecto**: esto se aplica a todas las cotizaciones de proyectos activos.
      - Página **Contratos del proyecto** > cuadrícula **Listas de precios del proyecto**: esto se aplica a todos los contratos de proyectos activos.

 2. Para cada página, debe seleccionar la lista de precios que desea eliminar y luego seleccionar **Eliminar**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Desactivar o eliminar la lista de precios de la página Lista de precios
 
1. Para eliminar una lista de precios de las listas de precios activas, vaya a **Ventas** > **Clientes** > **Lista de precios**. 
2. Seleccione la lista de precios que desea eliminar y, a continuación, seleccione **Eliminar**. Si se hace referencia a la lista de precios en cualquier transacción existente, no podrá eliminarla. Si esto sucede, puede desactivar la lista de precios para que no aparezca en ninguna vista. 
3. Para desactivar la lista de precios, seleccione la lista de precios nuevamente y luego seleccione **Desactivar**.   
