---
title: Novedades o cambios en la versión de actualización 14, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 14 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085106"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="cb324-103">Versión de actualización de Project Service Automation 14, V3</span><span class="sxs-lookup"><span data-stu-id="cb324-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="cb324-104">Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="cb324-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="cb324-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="cb324-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cb324-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cb324-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cb324-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="cb324-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="cb324-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cb324-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cb324-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 14.</span><span class="sxs-lookup"><span data-stu-id="cb324-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="cb324-110">Esta versión tiene un número de compilación de V3.10.4.21 y está disponible en la siguiente programación:</span><span class="sxs-lookup"><span data-stu-id="cb324-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="cb324-111">**Disponibilidad general (actualización automática):** enero de 2020</span><span class="sxs-lookup"><span data-stu-id="cb324-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="cb324-112">**Actualización automática:** febrero de 2020</span><span class="sxs-lookup"><span data-stu-id="cb324-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="cb324-113">Versión de actualización 14</span><span class="sxs-lookup"><span data-stu-id="cb324-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="cb324-114">Mejoras</span><span class="sxs-lookup"><span data-stu-id="cb324-114">Enhancements</span></span>

- <span data-ttu-id="cb324-115">Sales</span><span class="sxs-lookup"><span data-stu-id="cb324-115">Sales</span></span>

     - <span data-ttu-id="cb324-116">Los valores de campo personalizados de **Detalles de línea de oferta** se copian en **Detalles de línea de contrato de proyecto** cuando una oferta se actualiza a **cerrada como lograda**.</span><span class="sxs-lookup"><span data-stu-id="cb324-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="cb324-117">Los proyectos confirmados pueden ser **cerrados como perdidos**.</span><span class="sxs-lookup"><span data-stu-id="cb324-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="cb324-118">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="cb324-118">Resource Management</span></span>

     - <span data-ttu-id="cb324-119">Al ampliar las reservas, los usuarios recibirán un cuadro de diálogo de confirmación para resumir los resultados de la reserva y proporcionar un vínculo para Mantener reservas.</span><span class="sxs-lookup"><span data-stu-id="cb324-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="cb324-120">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="cb324-120">Bug fixes</span></span>

- <span data-ttu-id="cb324-121">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="cb324-121">Time and Expense</span></span>

     - <span data-ttu-id="cb324-122">Corregido: Se mejoró la experiencia del usuario cuando el usuario no ha seleccionado ninguna entrada para corregirla.</span><span class="sxs-lookup"><span data-stu-id="cb324-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="cb324-123">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="cb324-123">Resource Management</span></span>

     - <span data-ttu-id="cb324-124">Corregido: La reserva de un recurso varias veces desborda el nombre del recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="cb324-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="cb324-125">Sales</span><span class="sxs-lookup"><span data-stu-id="cb324-125">Sales</span></span>

     - <span data-ttu-id="cb324-126">Corregido: El precio de venta total no se calcula hasta que el usuario también introduce un precio de coste para las estimaciones de gastos en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="cb324-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="cb324-127">Corregido: Se produce un error al cerrar una oferta como **Lograda** si el contrato del proyecto asociado no está en un estado **Borrador**.</span><span class="sxs-lookup"><span data-stu-id="cb324-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

