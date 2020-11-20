---
title: Notas de desarrollador para aprobaciones
description: En este tema se proporciona información adicional para el desarrollador sobre el trabajo con aprobaciones.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483969"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="1783e-103">Notas de desarrollador para aprobaciones</span><span class="sxs-lookup"><span data-stu-id="1783e-103">Developer notes for Approvals</span></span>

<span data-ttu-id="1783e-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="1783e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1783e-105">Dynamics 365 Project Operations incluye una lógica de validación que garantiza la correcta transición de registros a través de las etapas de aprobación.</span><span class="sxs-lookup"><span data-stu-id="1783e-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="1783e-106">Las transiciones de registro correctas garantizan:</span><span class="sxs-lookup"><span data-stu-id="1783e-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="1783e-107">Todas las filas de apoyo se crean en tablas relacionadas, como diarios y datos reales.</span><span class="sxs-lookup"><span data-stu-id="1783e-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="1783e-108">El aprobador está marcado como **Aprobador de proyectos** en el proyecto antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="1783e-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
