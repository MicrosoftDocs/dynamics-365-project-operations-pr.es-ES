---
title: Crear una lista de precios
description: Cómo crear una lista de precios en Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290335"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="09dc3-103">Crear una lista de precios (Project Service)</span><span class="sxs-lookup"><span data-stu-id="09dc3-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="09dc3-104">Las listas de precios proporcionan una plantilla que los administradores de cuentas pueden usar para crear ofertas y proyectos, y para establecer los costos de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="09dc3-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="09dc3-105">Ofrecen una lista de elementos de línea de roles y gastos, y el precio que se cobrará por cada uno.</span><span class="sxs-lookup"><span data-stu-id="09dc3-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="09dc3-106">Puede crear varias listas de precios para mantener las estructuras de precios por separado para distintas regiones donde vende sus productos o para distintos canales de ventas.</span><span class="sxs-lookup"><span data-stu-id="09dc3-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="09dc3-107">Se recomienda crear al menos una lista de precios para cada divisa en la que planee facturar a los clientes.</span><span class="sxs-lookup"><span data-stu-id="09dc3-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="09dc3-108">Para crear estimaciones financieras para el trabajo que se realizará, asegúrese de que cada proyecto tiene un coste de apoyo y una lista de precios de ventas.</span><span class="sxs-lookup"><span data-stu-id="09dc3-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="09dc3-109">Configure una lista de precios de ventas y costes predeterminadas que se aplique a todos los proyectos creados en su organización.</span><span class="sxs-lookup"><span data-stu-id="09dc3-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="09dc3-110">Las listas de precios se basan en roles y categorías de gastos, por lo que antes de crear una lista de precios, asegúrese de que ya ha configurado los roles y las categorías de gastos que desea usar al crear la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="09dc3-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="09dc3-111">Vaya a **Project Service > Listas de precios**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="09dc3-112">Haga clic en **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="09dc3-113">En **Contexto**, seleccione si esta lista de precios es para **Coste**, **Compra** o **Ventas**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="09dc3-114">En **Nombre**, escriba un nombre para la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="09dc3-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="09dc3-115">En **Divisa**, seleccione la divisa que va a usar para facturar o contabilizar como coste.</span><span class="sxs-lookup"><span data-stu-id="09dc3-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="09dc3-116">En **Unidad de tiempo**, especifique el período de tiempo al que se aplica el precio, como día u hora.</span><span class="sxs-lookup"><span data-stu-id="09dc3-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="09dc3-117">Rellene **Fecha de inicio**, **Fecha de finalización** y **Descripción** según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="09dc3-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="09dc3-118">Haga clic en **Guardar** para crear el registro para que pueda seguir editándolo.</span><span class="sxs-lookup"><span data-stu-id="09dc3-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="09dc3-119">Para agregar un rol de precio a la lista de precios, haga clic en **+** en **Rol de precios**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="09dc3-120">En el panel **Precio de rol**, complete los detalles y, a continuación haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="09dc3-121">Siga agregando precios de rol si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09dc3-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="09dc3-122">Cuando termine, haga clic en **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="09dc3-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="09dc3-123">Para agregar un precio de categoría de gasto a la lista de precios, haga clic en **+** en **Precios de categorías**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="09dc3-124">En el panel **Precio de categoría de transacciones**, complete los detalles y, a continuación haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="09dc3-125">Siga agregando precios de categorías si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09dc3-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="09dc3-126">Cuando termine, haga clic en **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="09dc3-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="09dc3-127">Para agregar elementos de lista de precios a la lista de precios, haga clic en **+** en **Elementos de lista de precios**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="09dc3-128">En el panel **Elemento de lista de precios**, complete los detalles y, a continuación haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="09dc3-129">Siga agregando elementos de lista de precios si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09dc3-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="09dc3-130">Cuando termine, haga clic en **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="09dc3-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="09dc3-131">Para agregar relaciones de zona a la lista de precios, haga clic en **+** en **Relaciones de zonas**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="09dc3-132">En la ventana **Nueva conexión**, complete los detalles y, a continuación haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="09dc3-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="09dc3-133">Seguir agregando relaciones de zonas de ventas si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09dc3-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="09dc3-134">Cuando termine, haga clic en **Guardar** en la esquina inferior derecha de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="09dc3-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="09dc3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="09dc3-135">See Also</span></span>  
 [<span data-ttu-id="09dc3-136">Configurar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="09dc3-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]