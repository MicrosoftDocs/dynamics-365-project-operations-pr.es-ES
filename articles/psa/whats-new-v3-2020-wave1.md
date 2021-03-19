---
title: Novedades o cambios del primer lanzamiento de 2020 de la versión 3.x de Project Service Automation
description: Este tema proporciona información sobre las novedades y los cambios en el primer lanzamiento de Project Service Automation versión 3, 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280194"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="3384b-103">Novedades o cambios del primer lanzamiento de 2020 de la versión 3 de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3384b-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3384b-104">El tema resalta las consideraciones de actualización clave al pasar a la última versión del primer lanzamiento de Project Service Automation (PSA) versión 3.x, 2020.</span><span class="sxs-lookup"><span data-stu-id="3384b-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="3384b-105">Entrada de tiempo</span><span class="sxs-lookup"><span data-stu-id="3384b-105">Time entry</span></span>
<span data-ttu-id="3384b-106">La experiencia de entrada de tiempo se ha ampliado para ofrecer capacidades para ampliar la entrada de tiempo en más escenarios de clientes.</span><span class="sxs-lookup"><span data-stu-id="3384b-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="3384b-107">Esto incluye la capacidad de agregar tipos de entrada, que ahora impulsan un comportamiento específico basado en el nombre del esquema de campo **Configuración de entrada de tiempo**, que se muestra como **Origen de la hora**.</span><span class="sxs-lookup"><span data-stu-id="3384b-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="3384b-108">Se ha agregado una nueva solución, llamada Tiempo, Gasto, Estado y Aprobaciones (TESA) para admitir esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3384b-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="3384b-109">Consideración sobre actualizaciones</span><span class="sxs-lookup"><span data-stu-id="3384b-109">Upgrade consideration</span></span>
<span data-ttu-id="3384b-110">Para admitir esta funcionalidad, se han actualizado los roles dentro de PSA para incluir nuevos privilegios.</span><span class="sxs-lookup"><span data-stu-id="3384b-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="3384b-111">Estos privilegios conceden acceso de lectura a la nueva entidad, **Configuración de entrada de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="3384b-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="3384b-112">A los usuarios que requieren la capacidad de registrar el tiempo se les debe conceder el rol de usuario **Usuario de entrada de tiempo** además de los roles existentes.</span><span class="sxs-lookup"><span data-stu-id="3384b-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="3384b-113">Este rol incluye la nueva funcionalidad y garantiza que la entrada de tiempo continuará funcionando.</span><span class="sxs-lookup"><span data-stu-id="3384b-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="3384b-114">Además, si tiene algún módulo de aplicación personalizado que incluya todos los formularios para la entidad de entrada de tiempo, deberá eliminar el **Formulario de creación rápida de entrada de tiempo TESA** del módulo.</span><span class="sxs-lookup"><span data-stu-id="3384b-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="3384b-115">Cambios de entrada de tiempo actualmente ampliados</span><span class="sxs-lookup"><span data-stu-id="3384b-115">Currently extended time entry changes</span></span>
<span data-ttu-id="3384b-116">Para minimizar el impacto en los usuarios actuales de la entrada de tiempo, este cambio de rol es el único requisito central necesario para continuar utilizando la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3384b-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="3384b-117">Si ha creado vistas personalizadas o experiencias de entrada de tiempo independientes, debe establecer los campos **Configuración de entrada de tiempo** al valor de PSA correcto.</span><span class="sxs-lookup"><span data-stu-id="3384b-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]