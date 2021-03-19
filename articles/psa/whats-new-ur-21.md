---
title: Novedades o cambios en la versión de actualización 21, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 21, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280644"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="54149-103">Versión de actualización de Project Service Automation 21, V3</span><span class="sxs-lookup"><span data-stu-id="54149-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="54149-104">Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="54149-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="54149-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="54149-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="54149-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="54149-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="54149-107">Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="54149-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="54149-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="54149-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="54149-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 21.</span><span class="sxs-lookup"><span data-stu-id="54149-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="54149-110">Esta versión tiene un número de compilación V 3.10.32.50 y generalmente está disponible a través de una actualización automática en junio de 2020.</span><span class="sxs-lookup"><span data-stu-id="54149-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="54149-111">Versión de actualización 21</span><span class="sxs-lookup"><span data-stu-id="54149-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="54149-112">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="54149-112">Bug fixes</span></span>

<span data-ttu-id="54149-113">**Tiempo y gasto**</span><span class="sxs-lookup"><span data-stu-id="54149-113">**Time and Expense**</span></span>

<span data-ttu-id="54149-114">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54149-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="54149-115">Al hospedar el **Control de cuadrícula de entrada de tiempo** en Paneles, la cuadrícula no utiliza todo el ancho del contenedor de la cuadrícula del panel.</span><span class="sxs-lookup"><span data-stu-id="54149-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="54149-116">Para zonas horarias específicas, el control de cuadrícula **Entrada de tiempo** no muestra registros.</span><span class="sxs-lookup"><span data-stu-id="54149-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="54149-117">Las entradas de tiempo posteriores a las 9:00 p. m. aparecen en el día incorrecto.</span><span class="sxs-lookup"><span data-stu-id="54149-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="54149-118">Los usuarios no pueden enviar gastos si la categoría de gastos **Se requiere recibo de gastos** no tiene ningún valor.</span><span class="sxs-lookup"><span data-stu-id="54149-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="54149-119">**Administración de recursos**</span><span class="sxs-lookup"><span data-stu-id="54149-119">**Resource Management**</span></span>

<span data-ttu-id="54149-120">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54149-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="54149-121">Las reservas inactivas se muestran en la vista **Conciliación**.</span><span class="sxs-lookup"><span data-stu-id="54149-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="54149-122">Falta la validación del cumplimiento de recursos genéricos para garantizar que exista un estado de reserva válido.</span><span class="sxs-lookup"><span data-stu-id="54149-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="54149-123">**Administración del proyecto**</span><span class="sxs-lookup"><span data-stu-id="54149-123">**Project Management**</span></span>

<span data-ttu-id="54149-124">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54149-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="54149-125">Las cuadrículas del formulario **Proyecto** (**Asignación de recursos**, **Tarea**, la vista **Conciliación**, **Estimaciones de gastos**) permanecen editables incluso cuando un proyecto no está activo.</span><span class="sxs-lookup"><span data-stu-id="54149-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="54149-126">Los clientes duplicados no se pueden fusionar con los clientes que están vinculados a contratos de proyecto confirmados.</span><span class="sxs-lookup"><span data-stu-id="54149-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="54149-127">Cuando se agrega un recurso que no tiene un calendario válido, el sistema no devuelve un mensaje de error descriptivo.</span><span class="sxs-lookup"><span data-stu-id="54149-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="54149-128">El botón **Agregar tarea** en la cuadrícula de tareas está habilitado cuando el proyecto está vinculado al **complemento de Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="54149-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="54149-129">El esfuerzo crece de manera incontrolable cuando se asigna una tarea con una categoría a un recurso con un rol para el que hay un precio de coste definido.</span><span class="sxs-lookup"><span data-stu-id="54149-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="54149-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="54149-130">**Sales**</span></span>

<span data-ttu-id="54149-131">Se han realizado las siguientes mejoras:</span><span class="sxs-lookup"><span data-stu-id="54149-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="54149-132">**Frecuencia de la factura** e **Inicio de facturación** se han trasladado a la pestaña **Programación de facturas**.</span><span class="sxs-lookup"><span data-stu-id="54149-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="54149-133">Se han solucionado los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="54149-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="54149-134">**Precio de venta total** es cero (0) para **Categoría** aunque el **Rol** tenga un precio de venta total que no sea cero.</span><span class="sxs-lookup"><span data-stu-id="54149-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="54149-135">Los clientes no pueden cambiar el valor del campo **Estado de la factura** a **Listo para facturación** cuando otro proceso personalizado está actualizando un campo adicional.</span><span class="sxs-lookup"><span data-stu-id="54149-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="54149-136">El botón **Actualizar líneas de factura** puede crear varias líneas duplicadas si se selecciona repetidamente.</span><span class="sxs-lookup"><span data-stu-id="54149-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="54149-137">El botón **Actualizar precios** no funciona en la subcuadrícula **Precios de roles** en el formulario **Vista rápida**.</span><span class="sxs-lookup"><span data-stu-id="54149-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="54149-138">La lógica **Resolución de lista de precios de venta** maneja incorrectamente las zonas horarias, lo que resulta en una selección incorrecta de listas de precios.</span><span class="sxs-lookup"><span data-stu-id="54149-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="54149-139">El **Coste real total** de un proyecto puede quedar fuera por un importe fraccionario después de que se aprueba una sola entrada de tiempo.</span><span class="sxs-lookup"><span data-stu-id="54149-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="54149-140">La lógica de **Resolución de precios** no proporciona un mensaje de error descriptivo si el **Precio de rol recuperado** no tiene valores en los campos **Unidad principal** y **Precio en unidad principal**.</span><span class="sxs-lookup"><span data-stu-id="54149-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]