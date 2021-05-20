---
title: Novedades o cambios en la versión de actualización 22, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 22, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949025"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="109d4-103">Versión de actualización de Project Service Automation 22, V3</span><span class="sxs-lookup"><span data-stu-id="109d4-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="109d4-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="109d4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="109d4-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="109d4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="109d4-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="109d4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="109d4-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="109d4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="109d4-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="109d4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="109d4-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 22.</span><span class="sxs-lookup"><span data-stu-id="109d4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="109d4-110">Esta versión tiene un número de compilación V 3.10.33.48 y generalmente está disponible a través de una actualización automática en junio de 2020.</span><span class="sxs-lookup"><span data-stu-id="109d4-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="109d4-111">Versión de actualización 22</span><span class="sxs-lookup"><span data-stu-id="109d4-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="109d4-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="109d4-112">Bug fixes</span></span>



<span data-ttu-id="109d4-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="109d4-113">**Time and Expense**</span></span>

<span data-ttu-id="109d4-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="109d4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="109d4-115">Las **entradas de tiempo** no se agregan automáticamente en la programación de entradas de tiempo después de la importación.</span><span class="sxs-lookup"><span data-stu-id="109d4-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="109d4-116">El selector de fechas de cuadrícula **Entrada de tiempo** no reconoce la configuración regional de un usuario.</span><span class="sxs-lookup"><span data-stu-id="109d4-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="109d4-117">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="109d4-117">**Resource Management**</span></span>

<span data-ttu-id="109d4-118">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="109d4-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="109d4-119">En modo manual, los cambios en los contornos de **Asignación de recursos** no se reconocen al generar **Requerimientos de recursos**.</span><span class="sxs-lookup"><span data-stu-id="109d4-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="109d4-120">Las **solicitudes de recursos** no admiten estados de solicitud personalizados.</span><span class="sxs-lookup"><span data-stu-id="109d4-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="109d4-121">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="109d4-121">**Project Management**</span></span>

<span data-ttu-id="109d4-122">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="109d4-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="109d4-123">Al hacer doble clic en EstimateGridControl no se analizan correctamente los números con formato neerlandés.</span><span class="sxs-lookup"><span data-stu-id="109d4-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="109d4-124">Las horas asignadas no se actualizan correctamente cuando se cambian las asignaciones mediante el complemento de cliente de escritorio de Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="109d4-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="109d4-125">Las cuadrículas de Seguimiento del proyecto y Estimaciones muestran un código de divisa de ventas incorrecto cuando la divisa del contrato es diferente a la divisa del cliente y la organización está configurada para mostrar códigos de divisa en lugar de símbolos de divisa.</span><span class="sxs-lookup"><span data-stu-id="109d4-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="109d4-126">La fecha de finalización de un miembro del equipo agregará un día si el horario de trabajo es de 24 horas al día.</span><span class="sxs-lookup"><span data-stu-id="109d4-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="109d4-127">En la programación del proyecto, al agregar una categoría de transacción a una tarea no se activa el guardado automático.</span><span class="sxs-lookup"><span data-stu-id="109d4-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="109d4-128">Se muestra el siguiente error al agregar un miembro del equipo a la plantilla de proyecto: "Los requisitos de recursos no se pueden asociar con las plantillas de proyecto".</span><span class="sxs-lookup"><span data-stu-id="109d4-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="109d4-129">El script de regla de cinta "msdyn.Approval.CanApproveOrReject" muestra un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="109d4-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="109d4-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="109d4-130">**Sales**</span></span>

<span data-ttu-id="109d4-131">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="109d4-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="109d4-132">El mensaje de error de validación no se muestra cuando se selecciona una lista de precios de coste en la búsqueda de lista de precios en el formulario/entidad "Nueva lista de precios del proyecto de cotización".</span><span class="sxs-lookup"><span data-stu-id="109d4-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="109d4-133">Al cerrar la cotización como ganada no se navega hasta el contrato creado si un BPF adjunto a la cotización se encuentra en la etapa final.</span><span class="sxs-lookup"><span data-stu-id="109d4-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="109d4-134">Al revertir las **Ventas no facturadas**, se vinculan al coste original cuando se recupera una entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="109d4-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="109d4-135">Después de seleccionar el botón **Confirmar**, el estado de la factura no cambia a **Confirmado** a menos que se actualice la factura.</span><span class="sxs-lookup"><span data-stu-id="109d4-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]