---
title: Notas de desarrollador para aprobaciones
description: En este tema se proporciona información adicional para el desarrollador sobre el trabajo con aprobaciones.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579741"
---
# <a name="developer-notes-for-approvals"></a>Notas de desarrollador para aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations incluye una lógica de validación que garantiza la correcta transición de registros a través de las etapas de aprobación. Las transiciones de registro correctas garantizan: 

  - Todas las filas de apoyo se crean en tablas relacionadas, como diarios y datos reales.
  - El aprobador está marcado como **Aprobador de proyectos** en el proyecto antes de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]