---
title: Agregar nuevos formularios de entidad personalizada (Project Service Automation 2.x)
description: En este tema se proporciona información sobre cómo agregar formularios de entidad personalizada para oportunidades, ofertas, pedidos o facturas en Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144614"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Agregar nuevos formularios de entidad personalizada (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Campo Tipo 

Dynamics 365 Project Service Automation utiliza el campo **Tipo** (**msdyn\_ordertype**) de las entidades Oportunidad, Oferta, Pedido y Factura para distinguir las versiones **basadas en el trabajo** de dichas entidades de las versiones **basadas en elementos** y **basadas en servicios**. PSA gestiona las versiones basadas en el trabajo de estas entidades. Gran parte de la lógica de negocios de los lados del cliente y del servidor de la solución dependen del campo **Tipo**. Por lo tanto, es importante que el campo se inicialice con un valor correcto cuando se crean las entidades. Un valor incorrecto puede generar comportamientos incorrectos y puede hacer que parte de la lógica de negocios no se ejecute correctamente.

## <a name="automatic-form-switching"></a>Cambio de formulario automático

Para evitar posibles daños en los datos y comportamientos inesperados ocasionados por errores en la inicialización y la edición de registros de entidad de ventas, PSA ahora incluye lógica para el cambio de formulario automático en formularios predefinidos. Esta lógica lleva a los usuarios al formato correcto para utilizar la versión basada en el trabajo de cualquier otro tipo de entidad de oportunidad, oferta, pedido o factura. Cuando un usuario abra la versión basada en el trabajo de una entidad de oportunidad, oferta, pedido o factura, el formulario cambiará a **Información del proyecto**.

La lógica de cambio automático de formulario se basa en la asignación entre el valor **formId** y el campo **msdyn\_ordertype**. Todos los formularios predefinidos se han agregado a dicha asignación. Sin embargo, los formularios personalizados deben agregarse manualmente para indicar la versión de la entidad que gestionan. Esto se basa en el campo **msdyn\_ordertype**. Si la asignación no incluye el cambio de formulario, la lógica cambiará al formulario predefinido en función del valor guardado en el campo **msdyn\_ordertype** de la entidad.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Agregar formularios personalizados y activar la lógica de cambio de formularios

El siguiente ejemplo muestra cómo agregar un formulario personalizado, **Información de mi proyecto**, para que funcione con oportunidades basadas en el trabajo. El mismo proceso se usa para agregar formularios personalizados para que funcionen con ofertas, pedidos y facturas.

Siga estos pasos para crear una versión personalizada del formulario **Información del proyecto**.

1. En la entidad Oportunidad, abra el formulario **Información del proyecto** y guarde una copia con el nombre **Información de mi proyecto**.
2. Abra el nuevo formulario y después, en las propiedades, asegúrese de que las secuencias de comandos de inicialización del formulario **Información del proyecto** están presentes. 

    > [!IMPORTANT]
    > No quite las secuencias de comandos. De lo contrario, es posible que algunos datos se inicialicen de forma incorrecta.

3. Compruebe que el campo **Tipo** (**msdyn\_ordertype**) se encuentra presente en el formulario. 

    > [!IMPORTANT]
    > No quite este campo. De lo contrario, se producirán errores en las secuencias de comandos de inicialización.

4. Busque el valor **formId** del nuevo formulario. Puede completar este paso de dos maneras:

    - Exporte el formulario **Información de mi proyecto** como parte de una solución no administrada y después busque el valor **formId** en el archivo customization.xml de la solución exportada.
    - Abra el formulario **Información de mi proyecto** en el editor de formularios y después busque el identificador único global (GUID) situado junto al parámetro **fromId** en la dirección URL, tal como se muestra en la siguiente ilustración.

    ![Valor formId del nuevo formulario en la URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Cree una asignación **msdyn\_ordertype** para el valor **formId** editando el recurso web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Quite el código del recurso y reemplácelo con el siguiente código.

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

6. Guarde y publique las personalizaciones.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]