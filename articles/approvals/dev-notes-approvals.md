---
title: Notas de desarrollador para aprobaciones
description: En este tema se proporciona información adicional para el desarrollador sobre el trabajo con aprobaciones.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996812"
---
# <a name="developer-notes-for-approvals"></a>Notas de desarrollador para aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations incluye una lógica de validación que garantiza la correcta transición de registros a través de las etapas de aprobación. Las transiciones de registro correctas garantizan: 

  - Todas las filas de apoyo se crean en tablas relacionadas, como diarios y datos reales.
  - El aprobador está marcado como **Aprobador de proyectos** en el proyecto antes de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]