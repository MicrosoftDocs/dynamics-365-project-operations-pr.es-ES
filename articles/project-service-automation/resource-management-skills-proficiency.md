---
title: Habilidades y modelos de competencia
description: Este tema proporciona información sobre cómo usar las habilidades y los modelos de competencia.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756082"
---
# <a name="skills-and-proficiency-models"></a>Habilidades y modelos de competencia

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Las habilidades son características de recursos que se comparten entre Dynamics 365 Project Service Automation y, si está presente, Dynamics 365 Field Service. 

Para mantener el repositorio de habilidades en Project Service Automation, vaya a **Recursos** \> **Cualificaciones de recursos**. 

> ![Cualificaciones de recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Uso de modelos de competencia para calificar recursos

Las habilidades para los recursos se clasifican según los modelos de competencia. Las calificaciones individuales se encuentran en un modelo de competencia. 

1. Para crear un modelo de competencia, vaya a **Recursos** \> **Modelos de competencia** y, a continuación, seleccione **Nuevo**.
2. En el nuevo modelo de calificación, especifique el valor mínimo y máximo de calificación y la entidad que se está calificando.
3. En la subcuadrícula **Valores de calificación**, puede definir los diferentes valores de calificación, desde el mínimo hasta el máximo.

> ![Calificaciones mínimas y máximas definidas](media/Resource-Management-image85.png)

Estos valores de calificación se muestran en los filtros **Requisitos de recursos**, **Tablero de programación** y **Asistente de programación**.