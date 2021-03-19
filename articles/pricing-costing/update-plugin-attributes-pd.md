---
title: Actualización de atributos de complementos con nuevas dimensiones de precios
description: En este tema se proporciona información sobre cómo actualizar atributos del complemento para las dimensiones de precios.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274704"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="644c6-103">Actualizar atributos de complementos con nuevas dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="644c6-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="644c6-104">En este tema se proporciona información sobre cómo actualizar atributos del complemento para las dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="644c6-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="644c6-105">Este tema solo se aplica a las características de oferta y contrato en Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="644c6-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="644c6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="644c6-106">Prerequisites</span></span>
<span data-ttu-id="644c6-107">Antes de completar los pasos de este tema, debe haber completado los procedimientos de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="644c6-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="644c6-108">Crear campos y entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="644c6-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="644c6-109">Agregar de campos personalizados a la configuración de precios y entidades transaccionales</span><span class="sxs-lookup"><span data-stu-id="644c6-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="644c6-110">[Configurar campos personalizados como dimensiones de precios](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="644c6-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="644c6-111">Si no ha completado esos procedimientos, complételos y, a continuación, regrese a este tema.</span><span class="sxs-lookup"><span data-stu-id="644c6-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="644c6-112">Registrar un complemento</span><span class="sxs-lookup"><span data-stu-id="644c6-112">Register a plug-in</span></span>
<span data-ttu-id="644c6-113">Cuando se crea un detalle de línea de oferta en la página **Línea de oferta** para una línea de oferta de proyecto, el sistema crea dos líneas de estimaciones.</span><span class="sxs-lookup"><span data-stu-id="644c6-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="644c6-114">Una línea es para el lado del coste de la estimación y la otra línea es para el lado de las ventas.</span><span class="sxs-lookup"><span data-stu-id="644c6-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="644c6-115">Esto es lo mismo para las líneas de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="644c6-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="644c6-116">Cuando realiza un cambio en la cantidad o en un campo en la parte del coste, ese cambio también se realiza en la parte de las ventas.</span><span class="sxs-lookup"><span data-stu-id="644c6-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="644c6-117">Esto es posible porque los complementos de PreOperation en Quotelinedetail y las entidades de detalle de línea de contractline conectan atributos específicos en el lado del costo con el lado de las ventas de la transacción.</span><span class="sxs-lookup"><span data-stu-id="644c6-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="644c6-118">Si necesita que se realicen cambios en los valores de dimensión de precios en el lado de las ventas también en el lado de los costes, los siguientes complementos deben volver a registrarse tras realizar cambios en una dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="644c6-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="644c6-119">Estos son los complementos para actualizar y volver a registrar:</span><span class="sxs-lookup"><span data-stu-id="644c6-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="644c6-120">PreOperationContractLineDetailUpdate: **Actualizar msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="644c6-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="644c6-121">PreOperationQuoteLineDetailUpdate: **Actualiza msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="644c6-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="644c6-122">Complete los siguientes pasos para actualizar y volver a registrar los complementos.</span><span class="sxs-lookup"><span data-stu-id="644c6-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="644c6-123">Abra **PluginRegistrationTool** y conéctese a su entorno de Dataverse de Project Operations.</span><span class="sxs-lookup"><span data-stu-id="644c6-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="644c6-124">Seleccione **Buscar** y escriba las primeras letras del complemento que se actualizará.</span><span class="sxs-lookup"><span data-stu-id="644c6-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="644c6-125">Después de que se encuentre el complemento, selecciónelo y, a continuación, haga clic en **Seleccionar en el formulario principal**.</span><span class="sxs-lookup"><span data-stu-id="644c6-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="644c6-126">Seleccione el paso **Actualizar msdyn_orderlinetransaction**, haga clic con el botón secundario y después seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="644c6-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="644c6-127">En la página de diálogo **Actualizar**, seleccione los tres puntos (**...**) en los atributos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="644c6-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="644c6-128">Se abre la ventana de atributos de filtrado y proporciona una lista de todos los atributos de la entidad y las dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="644c6-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="644c6-129">Seleccione las casillas para los atributos de dimensión de precios.</span><span class="sxs-lookup"><span data-stu-id="644c6-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="644c6-130">Seleccione **Aceptar** para cerrar la página y, a continuación, seleccione **Actualizar paso**.</span><span class="sxs-lookup"><span data-stu-id="644c6-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="644c6-131">Repita los pasos del 2 al 7 para el segundo complemento, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="644c6-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="644c6-132">Para este complemento, tiene que actualizar el paso **Actualización de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="644c6-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="644c6-133">Cierre **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="644c6-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]