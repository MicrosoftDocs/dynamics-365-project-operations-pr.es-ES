---
title: Tipos de período
description: En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287304"
---
# <a name="period-types"></a>Tipos de período

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Un tipo de período define la frecuencia con la que se estiman los ingresos de un proyecto. En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos. 

## <a name="create-and-work-with-period-types"></a>Crear y trabajar con tipos de períodos
Para crear y trabajar con tipos de período, complete los siguientes pasos:

1. En su entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Estimaciones** > **Tipos de período**.
2. Seleccione **Nuevo** para crear un nuevo tipo de período. Escriba un nombre y una descripción.
3. En el campo **Frecuencia**, seleccione un valor:

    - Si selecciona **Semana**,**Quincenal**, **Semimensual**, **Mes**, **Día**, **Trimestre** o **Año**, el calendario se utilizará para generar los períodos. 
    - Si selecciona **Período contable**, los períodos contables de la configuración de Contabilidad general se utilizarán para generar períodos.
    - Si selecciona **Sin límite**, puede especificar períodos personalizados.
4. Seleccione el registro de tipo de período y, a continuación, **Generar períodos** para crear períodos para el tipo de período. Según la frecuencia del período que haya seleccionado, es posible que tenga la opción de especificar una fecha de inicio o el número de períodos para generar.
5. Seleccione **Períodos** para revisar periodos generados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]