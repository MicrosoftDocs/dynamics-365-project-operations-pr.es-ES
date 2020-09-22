---
title: Agregar nuevos formularios de entidad personalizada (Project Service Automation 2.x)
description: En este tema se proporciona información sobre cómo agregar formularios de entidad personalizada para oportunidades, ofertas, pedidos o facturas en Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755917"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="55b20-103">Agregar nuevos formularios de entidad personalizada (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="55b20-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="55b20-104">Campo Tipo</span><span class="sxs-lookup"><span data-stu-id="55b20-104">Type field</span></span> 

<span data-ttu-id="55b20-105">Dynamics 365 Project Service Automation utiliza el campo **Tipo** (**msdyn\_ordertype**) de las entidades Oportunidad, Oferta, Pedido y Factura para distinguir las versiones **basadas en el trabajo** de dichas entidades de las versiones **basadas en elementos** y **basadas en servicios**.</span><span class="sxs-lookup"><span data-stu-id="55b20-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="55b20-106">PSA gestiona las versiones basadas en el trabajo de estas entidades.</span><span class="sxs-lookup"><span data-stu-id="55b20-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="55b20-107">Gran parte de la lógica de negocios de los lados del cliente y del servidor de la solución dependen del campo **Tipo**.</span><span class="sxs-lookup"><span data-stu-id="55b20-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="55b20-108">Por lo tanto, es importante que el campo se inicialice con un valor correcto cuando se crean las entidades.</span><span class="sxs-lookup"><span data-stu-id="55b20-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="55b20-109">Un valor incorrecto puede generar comportamientos incorrectos y puede hacer que parte de la lógica de negocios no se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="55b20-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="55b20-110">Cambio de formulario automático</span><span class="sxs-lookup"><span data-stu-id="55b20-110">Automatic form switching</span></span>

<span data-ttu-id="55b20-111">Para evitar posibles daños en los datos y comportamientos inesperados ocasionados por errores en la inicialización y la edición de registros de entidad de ventas, PSA ahora incluye lógica para el cambio de formulario automático en formularios predefinidos.</span><span class="sxs-lookup"><span data-stu-id="55b20-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="55b20-112">Esta lógica lleva a los usuarios al formato correcto para utilizar la versión basada en el trabajo de cualquier otro tipo de entidad de oportunidad, oferta, pedido o factura.</span><span class="sxs-lookup"><span data-stu-id="55b20-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="55b20-113">Cuando un usuario abra la versión basada en el trabajo de una entidad de oportunidad, oferta, pedido o factura, el formulario cambiará a **Información del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="55b20-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="55b20-114">La lógica de cambio automático de formulario se basa en la asignación entre el valor **formId** y el campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="55b20-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="55b20-115">Todos los formularios predefinidos se han agregado a dicha asignación.</span><span class="sxs-lookup"><span data-stu-id="55b20-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="55b20-116">Sin embargo, los formularios personalizados deben agregarse manualmente para indicar la versión de la entidad que gestionan.</span><span class="sxs-lookup"><span data-stu-id="55b20-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="55b20-117">Esto se basa en el campo **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="55b20-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="55b20-118">Si la asignación no incluye el cambio de formulario, la lógica cambiará al formulario predefinido en función del valor guardado en el campo **msdyn\_ordertype** de la entidad.</span><span class="sxs-lookup"><span data-stu-id="55b20-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="55b20-119">Agregar formularios personalizados y activar la lógica de cambio de formularios</span><span class="sxs-lookup"><span data-stu-id="55b20-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="55b20-120">El siguiente ejemplo muestra cómo agregar un formulario personalizado, **Información de mi proyecto**, para que funcione con oportunidades basadas en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="55b20-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="55b20-121">El mismo proceso se usa para agregar formularios personalizados para que funcionen con ofertas, pedidos y facturas.</span><span class="sxs-lookup"><span data-stu-id="55b20-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="55b20-122">Siga estos pasos para crear una versión personalizada del formulario **Información del proyecto**.</span><span class="sxs-lookup"><span data-stu-id="55b20-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="55b20-123">En la entidad Oportunidad, abra el formulario **Información del proyecto** y guarde una copia con el nombre **Información de mi proyecto**.</span><span class="sxs-lookup"><span data-stu-id="55b20-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="55b20-124">Abra el nuevo formulario y después, en las propiedades, asegúrese de que las secuencias de comandos de inicialización del formulario **Información del proyecto** están presentes.</span><span class="sxs-lookup"><span data-stu-id="55b20-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="55b20-125">No quite las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="55b20-125">Don't remove the scripts.</span></span> <span data-ttu-id="55b20-126">De lo contrario, es posible que algunos datos se inicialicen de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="55b20-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="55b20-127">Compruebe que el campo **Tipo** (**msdyn\_ordertype**) se encuentra presente en el formulario.</span><span class="sxs-lookup"><span data-stu-id="55b20-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="55b20-128">No quite este campo.</span><span class="sxs-lookup"><span data-stu-id="55b20-128">Don't remove this field.</span></span> <span data-ttu-id="55b20-129">De lo contrario, se producirán errores en las secuencias de comandos de inicialización.</span><span class="sxs-lookup"><span data-stu-id="55b20-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="55b20-130">Busque el valor **formId** del nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="55b20-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="55b20-131">Puede completar este paso de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="55b20-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="55b20-132">Exporte el formulario **Información de mi proyecto** como parte de una solución no administrada y después busque el valor **formId** en el archivo customization.xml de la solución exportada.</span><span class="sxs-lookup"><span data-stu-id="55b20-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="55b20-133">Abra el formulario **Información de mi proyecto** en el editor de formularios y después busque el identificador único global (GUID) situado junto al parámetro **fromId** en la dirección URL, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="55b20-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Valor formId del nuevo formulario en la URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="55b20-135">Cree una asignación **msdyn\_ordertype** para el valor **formId** editando el recurso web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="55b20-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="55b20-136">Quite el código del recurso y reemplácelo con el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="55b20-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="55b20-137">Guarde y publique las personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="55b20-137">Save and then publish the customizations.</span></span>
