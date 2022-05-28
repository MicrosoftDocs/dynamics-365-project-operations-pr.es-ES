---
title: Aplicar dimensiones financieras predeterminadas para las entradas de tiempo del proyecto
description: En este tema se proporciona información sobre cómo se aplican dimensiones financieras predeterminadas para las entradas de tiempo.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597957"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Aplicar dimensiones financieras predeterminadas para las entradas de tiempo del proyecto

[!include [banner](../includes/banner.md)]

Al utilizar dimensiones financieras para las entradas de tiempo del proyecto, el valor de dimensión predeterminado se evalúa en el siguiente orden:

1. Recurso
2. Project
3. Fuente de financiación

Por ejemplo, si la dimensión predeterminada se especifica en un recurso, el valor predeterminado se aplica sobre un valor predeterminado que se especifica para el proyecto. De igual modo, si la dimensión predeterminada se especifica en un proyecto, el valor predeterminado se aplica sobre el valor predeterminado que se especifica para la fuente de financiación.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
