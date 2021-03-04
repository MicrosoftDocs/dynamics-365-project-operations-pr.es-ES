---
title: Novedades o cambios en la versión de actualización 20, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones disponibles en la Versión de actualización de Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147134"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="4bb3c-103">Versión de actualización de Project Service Automation 20, V3</span><span class="sxs-lookup"><span data-stu-id="4bb3c-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4bb3c-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4bb3c-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4bb3c-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4bb3c-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4bb3c-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4bb3c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4bb3c-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 20.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="4bb3c-110">Esta versión tiene un número de compilación V 3.10.31.37 y generalmente está disponible a través de una actualización automática en junio de 2020.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="4bb3c-111">Versión de actualización 20</span><span class="sxs-lookup"><span data-stu-id="4bb3c-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4bb3c-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="4bb3c-112">Bug fixes</span></span>

<span data-ttu-id="4bb3c-113">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="4bb3c-113">**Project Management**</span></span>

<span data-ttu-id="4bb3c-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="4bb3c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4bb3c-115">La importación de miembros del equipo del proyecto con un método de asignación que requiere horas da como resultado un mensaje de error poco claro cuando las horas especificadas son cero.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="4bb3c-116">Los usuarios reciben un error incorrecto cuando se ha ingresado el número máximo de caracteres en el campo **Descripción** para una tarea de proyecto.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="4bb3c-117">La página **Descargar complemento Microsoft Dynamics 365 Project Service Automation** redirige a la página de descarga en inglés cuando la configuración de idioma del usuario está establecida en japonés.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="4bb3c-118">Cuando se produce un error del servidor, la etiqueta de sincronización de la pestaña **Calendario** del formulario **Proyectos** a veces permanece.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="4bb3c-119">Las actualizaciones de tareas redundantes se envían al servidor cuando se modifica una tarea.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="4bb3c-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4bb3c-120">**Sales**</span></span>

<span data-ttu-id="4bb3c-121">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="4bb3c-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="4bb3c-122">En el formulario **Contrato**, haciendo doble clic en **Crear factura**, se crean dos facturas para un único registro de datos reales.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="4bb3c-123">En Internet Explorer 11, los usuarios no pueden crear entradas de gastos.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="4bb3c-124">La reversión de costos y la reversión de ventas reales no facturadas no están vinculadas.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="4bb3c-125">El botón **Actualizar datos reales** del formulario **Proyecto** no actualiza **Horas reales de la tarea**.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="4bb3c-126">El complemento **PreValidateProjectTeamMemberCreate** puede crear recursos duplicables genéricos que se pueden reservar cuando el atributo **msdyn_isgenericresourceprojectscoped** se establece en **Falso**.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="4bb3c-127">**Recalcular** borra los costos imputables de los detalles de la línea de presupuesto basada en el producto y los detalles de la línea del contrato.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="4bb3c-128">En escenarios específicos, el complemento **PostEstimateLineUpdate** muestra un error de excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="4bb3c-129">La duración de la fase de tiempo en **Cuadro de análisis de rentabilidad** no coincide con la duración de los costos en el detalle de la línea de presupuesto de precio fijo del presupuesto.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="4bb3c-130">Los valores de unidad y grupo de unidades no se predeterminan correctamente para categorías de gastos en los formularios **Detalles de línea de contrato** y **Detalles de línea de presupuesto**.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="4bb3c-131">La lista **Precio de coste de unidad de organización** permite superposiciones en la vigencia de la fecha.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="4bb3c-132">Los usuarios no pueden cambiar **OrgUnit** cuando el tipo de pedido no está basado en el trabajo porque dará lugar a un error de excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="4bb3c-133">Al intentar navegar desde el formulario **Detalles de línea de presupuesto**, de vuelta a la pestaña **Presupuesto**, el formulario se actualiza y muestra la pestaña **Resumen**.</span><span class="sxs-lookup"><span data-stu-id="4bb3c-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
