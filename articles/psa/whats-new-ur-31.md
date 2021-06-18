---
title: Novedades o cambios en la versión de actualización 31, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 31, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999152"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="7fea6-103">Novedades o cambios en la versión de actualización 31, V3, de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7fea6-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7fea6-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7fea6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7fea6-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="7fea6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7fea6-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7fea6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7fea6-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="7fea6-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7fea6-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7fea6-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7fea6-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 31.</span><span class="sxs-lookup"><span data-stu-id="7fea6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="7fea6-110">Esta versión tiene un número de compilación V3.10.52.77 y generalmente está disponible a través de una actualización automática de mayo de 2021.</span><span class="sxs-lookup"><span data-stu-id="7fea6-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="7fea6-111">Versión de actualización 31</span><span class="sxs-lookup"><span data-stu-id="7fea6-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7fea6-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="7fea6-112">Bug fixes</span></span>

<span data-ttu-id="7fea6-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="7fea6-113">**Time and Expense**</span></span>

<span data-ttu-id="7fea6-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="7fea6-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="7fea6-115">Los botones de comando de control de entrada de tiempo en la página **Recurso que se puede reservar** eran confusos.</span><span class="sxs-lookup"><span data-stu-id="7fea6-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="7fea6-116">Se generó una excepción de referencia nula en **Project.SetTrackingFields** al aprobar una entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="7fea6-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="7fea6-117">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="7fea6-117">**Resource Management**</span></span>

<span data-ttu-id="7fea6-118">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="7fea6-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="7fea6-119">**Crear miembro del equipo** no muestra correctamente la configuración de metadatos de configuración de reserva para **Estado confirmado de la reserva predeterminada**.</span><span class="sxs-lookup"><span data-stu-id="7fea6-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="7fea6-120">Al actualizar de PSA 1.X a 3.X, el proceso de actualización falla en **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="7fea6-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="7fea6-121">**Ventas**</span><span class="sxs-lookup"><span data-stu-id="7fea6-121">**Sales**</span></span>

<span data-ttu-id="7fea6-122">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="7fea6-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="7fea6-123">Los ingresos reales convierten los importes a la moneda del proyecto en la cuadrícula de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7fea6-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="7fea6-124">La moneda predeterminada no está clara al crear líneas de diario, líneas de ofertas y líneas de contrato en escenarios donde la moneda base de una organización difiere de la moneda del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fea6-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="7fea6-125">La consulta **Validación del diario pendiente de corrección** no se filtra por proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fea6-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="7fea6-126">Las ventas restantes se calculan incorrectamente en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="7fea6-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="7fea6-127">Las ofertas basadas en un contacto fallan cuando se crean sin una lista de precios.</span><span class="sxs-lookup"><span data-stu-id="7fea6-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="7fea6-128">No se muestra ningún indicador giratorio de procesamiento cuando selecciona **Confirmar factura**.</span><span class="sxs-lookup"><span data-stu-id="7fea6-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="7fea6-129">No se muestra ningún indicador giratorio de procesamiento cuando selecciona **Crear factura**.</span><span class="sxs-lookup"><span data-stu-id="7fea6-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="7fea6-130">Cerrar una oferta como perdida no cancela las reservas.</span><span class="sxs-lookup"><span data-stu-id="7fea6-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







