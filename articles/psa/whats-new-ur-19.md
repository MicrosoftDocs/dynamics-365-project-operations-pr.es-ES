---
title: Novedades o cambios en la versión de actualización 19, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 19, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006622"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="4ce4e-103">Versión de actualización de Project Service Automation 19, V3</span><span class="sxs-lookup"><span data-stu-id="4ce4e-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4ce4e-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4ce4e-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4ce4e-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4ce4e-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4ce4e-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4ce4e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4ce4e-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 19.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="4ce4e-110">Esta versión tiene un número de compilación V3.10.30.41 y generalmente está disponible a través de una actualización automática de mayo de 2020.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="4ce4e-111">Versión de actualización 19</span><span class="sxs-lookup"><span data-stu-id="4ce4e-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4ce4e-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="4ce4e-112">Bug fixes</span></span>

<span data-ttu-id="4ce4e-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="4ce4e-113">**Time and Expense**</span></span>

<span data-ttu-id="4ce4e-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="4ce4e-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4ce4e-115">Errores derivados de que las importaciones de entrada de tiempo no se muestran correctamente.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="4ce4e-116">Cuadrícula de entrada de tiempo no admite el comportamiento de campo **Solo fecha**.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="4ce4e-117">Los recursos del proyecto no pueden crear un gasto con un proyecto.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="4ce4e-118">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="4ce4e-118">**Project Management**</span></span>

<span data-ttu-id="4ce4e-119">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="4ce4e-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="4ce4e-120">La tarea descendiente de la secundaria provoca una estimación de esfuerzo incorrecta durante el Cálculo de finalización (EAF).</span><span class="sxs-lookup"><span data-stu-id="4ce4e-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="4ce4e-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4ce4e-121">**Sales**</span></span>

<span data-ttu-id="4ce4e-122">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="4ce4e-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4ce4e-123">La acción **Recalcular** no funciona con detalles de línea de contrato de gastos o detalles de línea de presupuesto.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="4ce4e-124">**Actualizar precios** falta para las estimaciones de gastos.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="4ce4e-125">Los clientes no pueden seleccionar los motivos del estado del contrato personalizados desde la página **Contrato del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="4ce4e-126">Los clientes experimentan un rendimiento degradado al crear una lista de precios personalizada a partir de un presupuesto.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="4ce4e-127">Los clientes experimentan incoherencias con las **unidades** predeterminadas en **Detalles de línea de presupuesto** y las páginas **Detalles de línea de contrato**.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="4ce4e-128">La adición de elementos de categoría de transacción imputable a una línea de contrato imputable no respetará el tipo de facturación **No cargable** de la categoría de transacción.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="4ce4e-129">Los clientes no pueden usar los roles y la categoría recién agregados en los contratos creados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="4ce4e-130">Los clientes experimentan un rendimiento degradado por recuperación innecesaria en PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="4ce4e-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="4ce4e-131">Los roles configurados como no cargables en la lista **Categorías de recursos** deberían agregarse a la pestaña **Roles cargables** como **No cargable** en la línea del contrato para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="4ce4e-132">Los clientes pueden experimentar un rendimiento degradado al crear un proyecto porque **GetBookableResourceIdFromUser** recupera todas las columnas de recursos reservables en lugar de solo el identificador principal.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="4ce4e-133">La entidad **Tipo de transacción** carece del complemento de actualización de prevalidación para evitar que los usuarios ingresen **Unidades** y **Grupos de unidades** no válidos para los tipos de transacción.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="4ce4e-134">El paso **Eliminar** no funciona para la importación de entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4ce4e-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]