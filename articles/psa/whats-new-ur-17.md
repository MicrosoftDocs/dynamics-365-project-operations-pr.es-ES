---
title: Novedades o cambios en la versión de actualización 17, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 17, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085104"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="2e9ee-103">Versión de actualización de Project Service Automation 17, V3</span><span class="sxs-lookup"><span data-stu-id="2e9ee-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="2e9ee-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2e9ee-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="2e9ee-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2e9ee-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2e9ee-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2e9ee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2e9ee-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 17.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="2e9ee-110">Esta versión tiene un número de compilación de V3.10.6.34 y está disponible con carácter general a través de una actualización automática en marzo de 2020.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="2e9ee-111">Versión de actualización 17</span><span class="sxs-lookup"><span data-stu-id="2e9ee-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2e9ee-112">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="2e9ee-112">Bug fixes</span></span>

<span data-ttu-id="2e9ee-113">**Generales**</span><span class="sxs-lookup"><span data-stu-id="2e9ee-113">**General**</span></span>

- <span data-ttu-id="2e9ee-114">Corregido: Actualizar Project Service Automation para que se apliquen las licencias de Team Member (el Centro de recursos de proyecto incluirá metadatos del plan de Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="2e9ee-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="2e9ee-115">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="2e9ee-115">**Time and Expense**</span></span>

- <span data-ttu-id="2e9ee-116">Corregido: No es posible cambiar una estimación de gastos a partir de un precio distinto de cero a cero (0).</span><span class="sxs-lookup"><span data-stu-id="2e9ee-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="2e9ee-117">Se omite el cambio.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-117">The change is ignored.</span></span>

<span data-ttu-id="2e9ee-118">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="2e9ee-118">**Project Management**</span></span>

- <span data-ttu-id="2e9ee-119">Corregido: Se ha agregado una comprobación para valores nulos en el nombre de puesto de un miembro del equipo.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="2e9ee-120">Corregido: El campo **msdyn_userresourceid** de la entidad **msdyn_resourceassignment** ha quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="2e9ee-121">Corregido: Actualizar de 2.x a 3.x ahora maneja los contornos de esfuerzo vacíos en las asignaciones de tareas.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="2e9ee-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2e9ee-122">**Sales**</span></span>

- <span data-ttu-id="2e9ee-123">Corregido: **Invoice.PreValidateInvoiceUpdate** ahora controla el escenario de la reasignación de propietarios de registros de manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="2e9ee-124">Corregido: Cuando la clase de transacción es **Hora** , **UnitGroup** es no editable para todas las entidades, incluyendo, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** y **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="2e9ee-125">Sin embargo, **Unidad** es no editable solo para **JournalLine** y **FacturaLíneaDetalles**.</span><span class="sxs-lookup"><span data-stu-id="2e9ee-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


