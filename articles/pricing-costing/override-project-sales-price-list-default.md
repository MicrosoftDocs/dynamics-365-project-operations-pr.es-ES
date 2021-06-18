---
title: Reemplazar listas de precios de venta de proyecto
description: Este tema proporciona información sobre cómo crear listas de precios de venta personalizadas.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995102"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="c3bb8-103">Reemplazar listas de precios de venta de proyecto</span><span class="sxs-lookup"><span data-stu-id="c3bb8-103">Override project sales price lists</span></span>

<span data-ttu-id="c3bb8-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="c3bb8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="c3bb8-105">Listas de precios de proyecto específicas del cliente</span><span class="sxs-lookup"><span data-stu-id="c3bb8-105">Customer-specific project price lists</span></span>

<span data-ttu-id="c3bb8-106">Los acuerdos de precios específicos del cliente se pueden configurar como listas de precios de proyectos en un registro de cuenta en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="c3bb8-107">Para configurar una lista de precios de proyecto específica del cliente, en el área **Ventas**, navegue hasta el registro de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="c3bb8-108">Abra la página de lista **Cuentas**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="c3bb8-109">Busque y haga doble clic en un registro de cliente para abrir la página de detalles **Cuenta**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="c3bb8-110">En la pestaña **Listas de precios de proyectos**, seleccione **+ Nueva de lista de precios de proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="c3bb8-111">Sobre la página **Lista de precios del nuevo proyecto**, seleccione una lista de precios en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="c3bb8-112">Solo las listas de precios que tienen el contexto establecido en **Ventas** y cuya moneda coincide con la moneda de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="c3bb8-113">Dé un nombre a la asociación y luego y seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="c3bb8-114">Se crea una lista de precios de proyecto específica del cliente.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="c3bb8-115">Esta lista de precios se utilizará para predeterminar los precios del proyecto en las cotizaciones del proyecto o los contratos creados para este cliente cuando la fecha de creación de la cotización o el contrato del proyecto se encuentre dentro de la fecha de vigencia de la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="c3bb8-116">Precios personalizados en cotizaciones de proyectos</span><span class="sxs-lookup"><span data-stu-id="c3bb8-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="c3bb8-117">En las cotizaciones de proyectos, puede tener precios de proyectos que comiencen con una lista de precios estándar predeterminada que se establece por defecto del cliente o de los parámetros del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="c3bb8-118">Cuando necesite precios personalizados para trabajos relacionados con el proyecto en una cotización en particular, puede obtenerlos de la entidad asociada de listas de precios del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="c3bb8-119">Complete los siguientes pasos para configurar precios de proyecto específicos de cotización.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="c3bb8-120">Abra la oferta del proyecto y seleccione la pestaña **Listas de precios de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="c3bb8-121">En la subcuadrícula, seleccione **Crear precios personalizados**.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="c3bb8-122">Todas las listas de precios del proyecto que se adjuntan a la cotización se copian en nuevas listas de precios.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="c3bb8-123">Los nombres de las nuevas listas de precios reflejan el nombre de la cotización con un sello de fecha y hora para cuando se crearon estas listas de precios.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="c3bb8-124">Puede utilizar cada una de esas listas de precios y actualizar los precios de mano de obra (precio de función) y de gastos (precio de categoría).</span><span class="sxs-lookup"><span data-stu-id="c3bb8-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="c3bb8-125">Estos precios se aplicarán únicamente a esta oferta de proyecto.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="c3bb8-126">Listas de precios de un contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="c3bb8-126">Price lists on a project contract</span></span>

<span data-ttu-id="c3bb8-127">En un contrato de proyecto, el precio del proyecto siempre se establece de forma predeterminada como una lista de precios personalizada con el nombre del contrato y el sello de fecha y hora creado adjunto al nombre.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="c3bb8-128">Esto es cierto si el contrato se creó cuando se ganó la cotización o si el contrato se creó desde cero.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="c3bb8-129">Si es necesario, puede eliminar esta asociación a la lista de precios personalizada y asociar una lista de precios estándar al contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="c3bb8-130">Cuando asocia una lista de precios estándar a las listas de precios del proyecto en la cotización o el contrato, cualquier cambio realizado en los precios en la lista de precios afectará a todas las cotizaciones y contratos que utilizan la lista de precios.</span><span class="sxs-lookup"><span data-stu-id="c3bb8-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]