---
title: Actualización de atributos de complemento para incluir nuevas dimensiones de precios
description: En este tema se proporciona información sobre la actualización de los atributos del complemento para las dimensiones de precios.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756043"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Actualización de atributos de complemento para incluir nuevas dimensiones de precios

> [!NOTE]
> Si no está utilizando las características Oferta y Contrato de Project Service Automation (PSA), puede omitir este tema.

En este tema se presupone que ha completado los procedimientos en los temas [Creación de campos y entidades personalizados](create-custom-fields-entities.md), [Adición de campos personalizados a la configuración de precios y entidades transaccionales](field-references.md) y [Configuración de campos personalizados como dimensiones de precios](set-up-pricing-dimensions.md). Si no ha completado esos procedimientos, vuelva y complételos y, a continuación, regrese a este tema.

Cuando se crea un detalle de línea de oferta en la página **Línea de oferta** para una línea de oferta de proyecto, el sistema crea dos líneas de estimación en segundo plano: una línea para la parte del coste de la estimación y otra para la parte de las ventas. Esto es lo mismo para las líneas de contrato del proyecto.

Cuando realiza un cambio en la cantidad o en un campo en la parte del coste, ese cambio se propaga en la parte de las ventas. Esto es posible debido a los siguientes complementos que deben volver a registrarse después de un cambio en las dimensiones de precios.

- PreOperationContractLineDetailUpdate: actualizaciones **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate: actualizaciones **msdyn_quotelinetransaction**.

Los siguientes pasos le guían a través del proceso de registro de los complementos.

1. Abra **PluginRegistrationTool** y conéctese a su instancia en línea.
2. Haga clic en **Buscar** y busque el complemento que se va a actualizar.

 ![Captura de pantalla del árbol de búsqueda](media/PRT-1.png)

3. Después de que se encuentre el complemento, selecciónelo y, a continuación, haga clic en **Seleccionar en el formulario principal**.

4. Seleccione el paso del complemento que se va a actualizar, haga clic con el botón secundario y, a continuación, seleccione **Actualizar**.

 ![Captura de pantalla del complemento que se va a actualizar](media/PRT-2.png)
 
5. En la ventana de actualización, haga clic en los tres puntos (**...**) en los atributos de filtrado.

 ![Captura de pantalla de la información de configuración del paso existente de actualización](media/PRT-3.png)
 
6. Seleccione las casillas de atributos de precios.

 ![Captura de pantalla con la selección de la casilla para los atributos de precios](media/PRT-4.png)

7. Haga clic en **Aceptar** para cerrar la página y, a continuación, seleccione **Actualizar paso**.

 ![Captura de pantalla con el botón "Actualizar paso"](media/PRT-5.png)
 
8. Repita este proceso para el segundo complemento, **PreOperationQuoteLineDetail: actualización de msdyn_quotelinetransaction**.

9. Cierre la herramienta de registro del complemento.

