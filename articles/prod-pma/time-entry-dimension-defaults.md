---
title: Aplicar dimensiones financieras predeterminadas para las entradas de tiempo del proyecto
description: En este artículo se proporciona información sobre cómo se aplican dimensiones financieras predeterminadas para las entradas de tiempo.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916585"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Aplicar dimensiones financieras predeterminadas para las entradas de tiempo del proyecto

[!include [banner](../includes/banner.md)]

Al utilizar dimensiones financieras para las entradas de tiempo del proyecto, el valor de dimensión predeterminado se evalúa en el siguiente orden:

1. Recurso
2. Project
3. Fuente de financiación

Por ejemplo, si la dimensión predeterminada se especifica en un recurso, el valor predeterminado se aplica sobre un valor predeterminado que se especifica para el proyecto. De igual modo, si la dimensión predeterminada se especifica en un proyecto, el valor predeterminado se aplica sobre el valor predeterminado que se especifica para la fuente de financiación.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
