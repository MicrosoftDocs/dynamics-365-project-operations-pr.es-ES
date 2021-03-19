---
title: Actualización de la página principal
description: En este tema se muestra dónde encontrar la información importante sobre las características nuevas y modificadas en Dynamics 365 Project Service Automation y el proceso para actualizar a la versión más reciente.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 838eecb1229ea20106c7d5487dc37a81e8df501b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281724"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="61802-103">Actualización de la página principal</span><span class="sxs-lookup"><span data-stu-id="61802-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="61802-104">Actualización desde la versión 2.x o 1.x de PSA a la versión 3.x</span><span class="sxs-lookup"><span data-stu-id="61802-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="61802-105">Instancias nuevas</span><span class="sxs-lookup"><span data-stu-id="61802-105">New instances</span></span>

<span data-ttu-id="61802-106">A partir del 17 de mayo de 2019, cuando se selecciona Project Service Automation durante el aprovisionamiento de una nueva instancia, se instala la versión 3.x de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="61802-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="61802-107">Instancias existentes</span><span class="sxs-lookup"><span data-stu-id="61802-107">Existing instances</span></span>

<span data-ttu-id="61802-108">Anteriormente, los clientes que tuvieran una instancia de la versión 2.x de PSA y que necesitaran actualizar a la versión 3.x, que es la versión de PSA basada en la interfaz de cliente unificada (UCI), tenían que ponerse en contacto con el departamento de soporte técnico y proporcionar los detalles de su instancia, para que ese departamento pudiera habilitar la instancia para la actualización a la versión 3.x.</span><span class="sxs-lookup"><span data-stu-id="61802-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="61802-109">Desde el 1 de marzo de 2020, los clientes con una instancia de la versión 2.xy de PSA que tengan que actualizar a la versión 3.x, podrán actualizar sus instancias directamente desde el portal de administración sin tener que ponerse en contacto con el soporte de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61802-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="61802-110">La versión 3.x de PSA incluye cambios significativos.</span><span class="sxs-lookup"><span data-stu-id="61802-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="61802-111">Se ha creado en el marco de la interfaz unificada para ayudar a proporcionar una experiencia de usuario mejorada.</span><span class="sxs-lookup"><span data-stu-id="61802-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="61802-112">La aplicación rediseñada ofrece una interfaz de usuario (IU) coherente y uniforme, y sigue principios de diseño receptivos para una visualización óptima en cualquier tamaño de pantalla o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61802-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="61802-113">Se han producido otros cambios en toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="61802-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="61802-114">Algunas de las áreas que se han modificado incluyen precios, reservas y asignación de recursos, tiempo, gastos y aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="61802-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="61802-115">Antes de comenzar el proceso de actualización, le recomendamos que complete las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="61802-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="61802-116">Verifique que tanto Dynamics 365 Field Service como Project Service Automation estén instalados en la instancia identificada.</span><span class="sxs-lookup"><span data-stu-id="61802-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="61802-117">Si ambas soluciones están instaladas, debe planear actualizar ambas antes de reanudar el uso regular de la instancia.</span><span class="sxs-lookup"><span data-stu-id="61802-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="61802-118">Revise atentamente los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="61802-118">Carefully review the following topics.</span></span> <span data-ttu-id="61802-119">El conocimiento y la comprensión de los cambios entre versiones le ayudarán con el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="61802-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="61802-120">Estos temas proporcionan información sobre los principales cambios en PSA, junto con consideraciones y recomendaciones para planificar su actualización a la versión 3.x.</span><span class="sxs-lookup"><span data-stu-id="61802-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="61802-121">Novedades o cambios en la versión 3 de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61802-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="61802-122">Consideraciones de actualización: De la versión 2.x o 1.x a la versión 3 de Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61802-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="61802-123">Actualice su instancia de espacio aislado para evaluar los cambios en su implementación antes de actualizar su instancia de producción.</span><span class="sxs-lookup"><span data-stu-id="61802-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="61802-124">Una vez que haya revisado los temas mencionados anteriormente y esté listo para actualizar a la versión 3.x de PSA o a la versión basada en UCI, envíe una solicitud a Soporte técnico de Microsoft para que la actualización esté disponible desde el Centro de administración.</span><span class="sxs-lookup"><span data-stu-id="61802-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="61802-125">En su solicitud, proporcione los detalles de su instancia.</span><span class="sxs-lookup"><span data-stu-id="61802-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="61802-126">Versiones anteriores de PSA (versión 2.x de PSA) en una instancia recién creada</span><span class="sxs-lookup"><span data-stu-id="61802-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="61802-127">A partir del 17 de mayo de 2019, todas las nuevas instancias tendrán UCI como cliente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="61802-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="61802-128">Para la alineación con este cambio, se aprovisionarán la versión 3.x de PSA y la versión 8.x de Field Service de forma predeterminada, ya que estas versiones están diseñadas para funcionar con el cliente UCI.</span><span class="sxs-lookup"><span data-stu-id="61802-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="61802-129">A partir del 1 de marzo de 2020, los clientes de Dynamics PSA ya no podrán crear un nuevo entorno con versiones anteriores de PSA, como PSA versión 2.x o inferior.</span><span class="sxs-lookup"><span data-stu-id="61802-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="61802-130">Cualquier entorno nuevo será para obtener solo la versión 3.x de PSA.</span><span class="sxs-lookup"><span data-stu-id="61802-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="61802-131">Para obtener la mejor experiencia cuando utilice versiones anteriores de las aplicaciones PSA y Field Service, vaya a la página **Configuración del sistema** y para el campo, **Usar solo la nueva interfaz unificada (recomendado)**, seleccione **No**, ya que estas versiones no están diseñadas para su carga correcta en UCI.</span><span class="sxs-lookup"><span data-stu-id="61802-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="61802-132">Después de desactivar UCI, podrá abrir y ejecutar esas versiones de Field Service y PSA mediante el cliente web antiguo.</span><span class="sxs-lookup"><span data-stu-id="61802-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]