---
title: Actualización de atributos de complemento para incluir nuevas dimensiones de precios
description: En este tema se proporciona información sobre la actualización de los atributos del complemento para las dimensiones de precios.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281814"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="62de3-103">Actualización de atributos de complemento para incluir nuevas dimensiones de precios</span><span class="sxs-lookup"><span data-stu-id="62de3-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="62de3-104">Si no está utilizando las características Oferta y Contrato de Project Service Automation (PSA), puede omitir este tema.</span><span class="sxs-lookup"><span data-stu-id="62de3-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="62de3-105">En este tema se presupone que ha completado los procedimientos en los temas [Creación de campos y entidades personalizados](create-custom-fields-entities.md), [Adición de campos personalizados a la configuración de precios y entidades transaccionales](field-references.md) y [Configuración de campos personalizados como dimensiones de precios](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="62de3-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="62de3-106">Si no ha completado esos procedimientos, vuelva y complételos y, a continuación, regrese a este tema.</span><span class="sxs-lookup"><span data-stu-id="62de3-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="62de3-107">Cuando se crea un detalle de línea de oferta en la página **Línea de oferta** para una línea de oferta de proyecto, el sistema crea dos líneas de estimación en segundo plano: una línea para la parte del coste de la estimación y otra para la parte de las ventas.</span><span class="sxs-lookup"><span data-stu-id="62de3-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="62de3-108">Esto es lo mismo para las líneas de contrato del proyecto.</span><span class="sxs-lookup"><span data-stu-id="62de3-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="62de3-109">Cuando realiza un cambio en la cantidad o en un campo en la parte del coste, ese cambio se propaga en la parte de las ventas.</span><span class="sxs-lookup"><span data-stu-id="62de3-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="62de3-110">Esto es posible debido a los siguientes complementos que deben volver a registrarse después de un cambio en las dimensiones de precios.</span><span class="sxs-lookup"><span data-stu-id="62de3-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="62de3-111">PreOperationContractLineDetailUpdate: actualizaciones **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="62de3-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="62de3-112">PreOperationQuoteLineDetailUpdate: actualizaciones **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="62de3-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="62de3-113">Los siguientes pasos le guían a través del proceso de registro de los complementos.</span><span class="sxs-lookup"><span data-stu-id="62de3-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="62de3-114">Abra **PluginRegistrationTool** y conéctese a su instancia en línea.</span><span class="sxs-lookup"><span data-stu-id="62de3-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="62de3-115">Haga clic en **Buscar** y busque el complemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="62de3-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captura de pantalla del árbol de búsqueda](media/PRT-1.png)

3. <span data-ttu-id="62de3-117">Después de que se encuentre el complemento, selecciónelo y, a continuación, haga clic en **Seleccionar en el formulario principal**.</span><span class="sxs-lookup"><span data-stu-id="62de3-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="62de3-118">Seleccione el paso del complemento que se va a actualizar, haga clic con el botón secundario y, a continuación, seleccione **Actualizar**.</span><span class="sxs-lookup"><span data-stu-id="62de3-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captura de pantalla del complemento que se va a actualizar](media/PRT-2.png)
 
5. <span data-ttu-id="62de3-120">En la ventana de actualización, haga clic en los tres puntos (**...**) en los atributos de filtrado.</span><span class="sxs-lookup"><span data-stu-id="62de3-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captura de pantalla de la información de configuración del paso existente de actualización](media/PRT-3.png)
 
6. <span data-ttu-id="62de3-122">Seleccione las casillas de atributos de precios.</span><span class="sxs-lookup"><span data-stu-id="62de3-122">Select the pricing attribute check boxes.</span></span>

 ![Captura de pantalla con la selección de la casilla para los atributos de precios](media/PRT-4.png)

7. <span data-ttu-id="62de3-124">Haga clic en **Aceptar** para cerrar la página y, a continuación, seleccione **Actualizar paso**.</span><span class="sxs-lookup"><span data-stu-id="62de3-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captura de pantalla con el botón "Actualizar paso"](media/PRT-5.png)
 
8. <span data-ttu-id="62de3-126">Repita este proceso para el segundo complemento, **PreOperationQuoteLineDetail: actualización de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="62de3-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="62de3-127">Cierre la herramienta de registro del complemento.</span><span class="sxs-lookup"><span data-stu-id="62de3-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]