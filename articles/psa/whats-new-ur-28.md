---
title: Novedades o cambios en la versión de actualización 28, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 28, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010537"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="e8f11-103">Novedades o cambios en la versión de actualización 28, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e8f11-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e8f11-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e8f11-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e8f11-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="e8f11-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e8f11-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e8f11-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e8f11-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="e8f11-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e8f11-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e8f11-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e8f11-109">Este tema enumera las características y correcciones nuevas o modificadas para Project Service Automation V3, Update Release 28. Esta versión tiene un número de compilación de V3.10.46.32 y generalmente está disponible a través de una actualización automática en enero de 2021.</span><span class="sxs-lookup"><span data-stu-id="e8f11-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="e8f11-110">Versión de actualización 28</span><span class="sxs-lookup"><span data-stu-id="e8f11-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e8f11-111">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="e8f11-111">Bug fixes</span></span>

<span data-ttu-id="e8f11-112">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="e8f11-112">**Time and Expense**</span></span>

<span data-ttu-id="e8f11-113">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="e8f11-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f11-114">Los usuarios disponen de la opción **Edición masiva** para actualizar las entradas de tiempo aprobadas y enviadas.</span><span class="sxs-lookup"><span data-stu-id="e8f11-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="e8f11-115">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="e8f11-115">**Project Management**</span></span>

<span data-ttu-id="e8f11-116">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="e8f11-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f11-117">En aquellos casos en los que el GUID de la tarea se interprete como un número, las tareas no se podrán abrir para edición mediante **Editar tarea** en la cinta de la página **Estructura de descomposición del trabajo**.</span><span class="sxs-lookup"><span data-stu-id="e8f11-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="e8f11-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e8f11-118">**Sales**</span></span>

<span data-ttu-id="e8f11-119">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="e8f11-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="e8f11-120">Se genera una excepción de referencia nula cuando se invoca el complemento **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="e8f11-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="e8f11-121">La opción **Marcar como listo para facturar** de la cuadrícula de hitos solo actualiza parcialmente los atributos, con la excepción del atributo **InvoiceStatus**, que se actualiza.</span><span class="sxs-lookup"><span data-stu-id="e8f11-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]