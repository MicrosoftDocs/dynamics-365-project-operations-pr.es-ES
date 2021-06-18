---
title: Novedades o cambios en la versión de actualización 24, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 24, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
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
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000277"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="cbd2d-103">Versión de actualización de Project Service Automation 24, V3</span><span class="sxs-lookup"><span data-stu-id="cbd2d-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cbd2d-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cbd2d-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cbd2d-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cbd2d-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cbd2d-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cbd2d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cbd2d-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 24.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="cbd2d-110">Esta versión tiene un número de compilación de V 3.10.42.43 y está disponible con carácter general a través de una actualización automática en octubre de 2020.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="cbd2d-111">Versión de actualización 24</span><span class="sxs-lookup"><span data-stu-id="cbd2d-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cbd2d-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="cbd2d-112">Bug fixes</span></span>

<span data-ttu-id="cbd2d-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-113">**Sales**</span></span>

<span data-ttu-id="cbd2d-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cbd2d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbd2d-115">Problema al establecer la lista de precios predeterminada de productos.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="cbd2d-116">El rendimiento de Ganar una oferta es lento debido a la lista de precios incorporada y la copia de registros de precios de rol.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="cbd2d-117">**Contrato de proyecto/Centro de ventas** > **Elemento de línea de productos/Cantidad de línea de pedido** se redondea automáticamente al número entero más cercano.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="cbd2d-118">Eleve a privilegios del sistema al leer listas de precios.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="cbd2d-119">Copie los campos de la dirección del cliente **address1_freighttermscode** y **address1_shippingmethodcode** en Oferta/Pedido.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="cbd2d-120">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-120">**Time and Expense**</span></span>

<span data-ttu-id="cbd2d-121">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cbd2d-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbd2d-122">La **Cuadrícula de entrada de tiempo** no es compatible con el comportamiento de fecha **Solo fecha**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="cbd2d-123">La **Entrada de tiempo** no se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="cbd2d-124">Se requiere una actualización manual.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-124">A manual refresh is required.</span></span>
- <span data-ttu-id="cbd2d-125">No se pueden importar las entradas de tiempo de una asignación cuando haya una pausa (0 horas) en las asignaciones de un recurso.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="cbd2d-126">Al crear una entrada de tiempo, establezca el inicio lo mismo que **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="cbd2d-127">Vuelva a habilitar la edición masiva para la entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="cbd2d-128">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-128">**Resource Management**</span></span>

<span data-ttu-id="cbd2d-129">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cbd2d-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbd2d-130">Intentar actualizar el estado de una reserva entre días sin un requisito lanzará una excepción de referencia nula.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="cbd2d-131">Error al cargar la **Vista de conciliación**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="cbd2d-132">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-132">**Project Management**</span></span>

<span data-ttu-id="cbd2d-133">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cbd2d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="cbd2d-134">En la **Programación del proyecto**, al cambiar de **Manual** a **Automático**, el autoguardado no se completa.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="cbd2d-135">Los costes de gastos no deben calcularse en función de la variación en la **Cuadrícula de seguimiento de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="cbd2d-136">Un comportamiento incoherente para la columna **Etiqueta de estimaciones** durante la carga en comparación con cambiar el tipo **Fases temporales**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="cbd2d-137">El coste real de un proyecto puede que no refleje los totales de **Datos reales**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="cbd2d-138">**Fecha de finalización estimada** en la pestaña **Resumen** no coincide con la **Programación de WBS**.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="cbd2d-139">**Actualizar horas reales** en una sangría anulada no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="cbd2d-140">Un jefe de proyecto fuera de la raíz **BU** no puede crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="cbd2d-141">Los cambios en la tarea o categoría de **Estimaciones de gastos** no se conservan.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="cbd2d-142">**Copia de contrato** copia las programaciones de facturación y el estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="cbd2d-143">El botón **Actualizar datos reales** calcula incorrectamente las tareas de resumen.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="cbd2d-144">Complemento de Microsoft Project: corrige el error de referencia nula si algún miembro del equipo tiene una unidad de recursos vacía.</span><span class="sxs-lookup"><span data-stu-id="cbd2d-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]