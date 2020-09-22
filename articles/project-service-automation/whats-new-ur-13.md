---
title: Novedades en la versión de actualización 13, de Project Service Automation V3
description: Este tema proporciona información sobre las novedades de la versión de actualización 13 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756005"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="02b1a-103">Versión de actualización 13 Project Service Automation V3</span><span class="sxs-lookup"><span data-stu-id="02b1a-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="02b1a-104">Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="02b1a-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="02b1a-105">Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="02b1a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="02b1a-106">Esta versión es compatible con Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="02b1a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="02b1a-107">Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización.</span><span class="sxs-lookup"><span data-stu-id="02b1a-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="02b1a-108">Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="02b1a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="02b1a-109">En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 13.</span><span class="sxs-lookup"><span data-stu-id="02b1a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="02b1a-110">Esta versión tiene un número de compilación de V3.10.3.18 y está disponible en la siguiente programación:</span><span class="sxs-lookup"><span data-stu-id="02b1a-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="02b1a-111">**Disponibilidad general (actualización automática):** noviembre de 2019</span><span class="sxs-lookup"><span data-stu-id="02b1a-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="02b1a-112">**Actualización automática:** diciembre de 2019</span><span class="sxs-lookup"><span data-stu-id="02b1a-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="02b1a-113">Versión de actualización 13</span><span class="sxs-lookup"><span data-stu-id="02b1a-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="02b1a-114">Solución de errores</span><span class="sxs-lookup"><span data-stu-id="02b1a-114">Bug fixes</span></span>

- <span data-ttu-id="02b1a-115">Tiempo y gasto</span><span class="sxs-lookup"><span data-stu-id="02b1a-115">Time and Expense</span></span>

     - <span data-ttu-id="02b1a-116">Corregido: La funcionalidad de búsqueda en la página **Aprobación de gastos** no funciona al buscar por propósito de gasto.</span><span class="sxs-lookup"><span data-stu-id="02b1a-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="02b1a-117">Administración de recursos</span><span class="sxs-lookup"><span data-stu-id="02b1a-117">Resource Management</span></span>

     - <span data-ttu-id="02b1a-118">Corregido: Los números en la conciliación se han actualizado para justificarse a la derecha.</span><span class="sxs-lookup"><span data-stu-id="02b1a-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="02b1a-119">Corregido: Los recursos con nombre no se pueden asignar a tareas a través de la pestaña **Programación**.</span><span class="sxs-lookup"><span data-stu-id="02b1a-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="02b1a-120">Administración del proyecto</span><span class="sxs-lookup"><span data-stu-id="02b1a-120">Project Management</span></span>

     - <span data-ttu-id="02b1a-121">Corregido: La excepción de referencia nula al asignar un miembro de equipo cuando falta información de configuración en el **TransactionType** para **Unidad** y **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="02b1a-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="02b1a-122">Sales</span><span class="sxs-lookup"><span data-stu-id="02b1a-122">Sales</span></span>

     - <span data-ttu-id="02b1a-123">Corregido: Los registros de tipo de transacción duplicados devuelven un error cuando se crean registros de precios de roles.</span><span class="sxs-lookup"><span data-stu-id="02b1a-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="02b1a-124">Corregido: Los botones adicionales para **Nueva oportunidad**, **Oferta**, **Línea de pedido** y **Agregar producto** son visibles en comandos para Oportunidades, Ofertas, Pedidos de productos y la subcuadrícula de líneas basadas en proyectos.</span><span class="sxs-lookup"><span data-stu-id="02b1a-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


