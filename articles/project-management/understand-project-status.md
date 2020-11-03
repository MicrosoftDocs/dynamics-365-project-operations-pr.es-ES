---
title: Conocer el estado del proyecto
description: Este tema proporciona información sobre el estado asignado a proyectos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085020"
---
# <a name="understand-project-status"></a><span data-ttu-id="03f15-103">Conocer el estado del proyecto</span><span class="sxs-lookup"><span data-stu-id="03f15-103">Understand project status</span></span>

<span data-ttu-id="03f15-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="03f15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="03f15-105">La sección **Estado** de la página **Entidad del proyecto** proporciona un resumen del estado de un proyecto según el coste y el esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="03f15-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="03f15-106">Campos de resumen de estado</span><span class="sxs-lookup"><span data-stu-id="03f15-106">Status summary fields</span></span>

- <span data-ttu-id="03f15-107">El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto.</span><span class="sxs-lookup"><span data-stu-id="03f15-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="03f15-108">Este campo utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente.</span><span class="sxs-lookup"><span data-stu-id="03f15-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="03f15-109">El campo **Comentarios** permite al administrador de proyecto introducir comentarios específicos sobre el estado.</span><span class="sxs-lookup"><span data-stu-id="03f15-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="03f15-110">El campo **Estado actualizado en fecha de** no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="03f15-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="03f15-111">El valor de este campo es una marca de tiempo que indica cuándo se actualizó por última vez el estado.</span><span class="sxs-lookup"><span data-stu-id="03f15-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="03f15-112">Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la cuadrícula de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="03f15-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="03f15-113">Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, estos campos se actualizan a **Adelantado**.</span><span class="sxs-lookup"><span data-stu-id="03f15-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="03f15-114">Cuando la programación y la variación de coste para el nodo raíz son negativas, estos campos se establecen en **Retrasado**.</span><span class="sxs-lookup"><span data-stu-id="03f15-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
