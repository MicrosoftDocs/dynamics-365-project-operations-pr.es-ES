---
title: Actualización de atributos de complementos con nuevas dimensiones de precios
description: En este artículo se proporciona información sobre cómo actualizar los atributos del complemento para las dimensiones de precios.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920035"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualizar atributos de complementos con nuevas dimensiones de precios

En este artículo se proporciona información sobre cómo actualizar los atributos del complemento para las dimensiones de precios.

> [!NOTE]
> Este artículo sólo es aplicable a las características de cotización y contrato en Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Requisitos previos
Antes de que pueda completar los pasos de este artículo, debe completar los procedimientos de los siguientes artículos:

  - [Crear campos y entidades personalizados](create-custom-fields-entities-pricing-dimensions.md) 
  - [Agregar de campos personalizados a la configuración de precios y entidades transaccionales ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurar campos personalizados como dimensiones de precios](set-up-custom-fields-pricing-dimensions.md). 
  
Si no ha completado esos procedimientos, complételos y, a continuación, regrese a este artículo.

## <a name="register-a-plug-in"></a>Registrar un complemento
Cuando se crea un detalle de línea de oferta en la página **Línea de oferta** para una línea de oferta de proyecto, el sistema crea dos líneas de estimaciones. Una línea es para el lado del coste de la estimación y la otra línea es para el lado de las ventas. Esto es lo mismo para las líneas de contrato del proyecto.

Cuando realiza un cambio en la cantidad o en un campo en la parte del coste, ese cambio también se realiza en la parte de las ventas. Esto es posible porque los complementos de PreOperation en Quotelinedetail y las entidades de detalle de línea de contractline conectan atributos específicos en el lado del costo con el lado de las ventas de la transacción. Si necesita que se realicen cambios en los valores de dimensión de precios en el lado de las ventas también en el lado de los costes, los siguientes complementos deben volver a registrarse tras realizar cambios en una dimensión de precios.

Estos son los complementos para actualizar y volver a registrar:

- PreOperationContractLineDetailUpdate: **Actualizar msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate: **Actualiza msdyn_quotelinetransaction**

Complete los siguientes pasos para actualizar y volver a registrar los complementos.

1. Abra **PluginRegistrationTool** y conéctese a su entorno de Dataverse de Project Operations.
2. Seleccione **Buscar** y escriba las primeras letras del complemento que se actualizará.
3. Después de que se encuentre el complemento, selecciónelo y, a continuación, haga clic en **Seleccionar en el formulario principal**.
4. Seleccione el paso **Actualizar msdyn_orderlinetransaction**, haga clic con el botón secundario y después seleccione **Actualizar**.
5. En la página de diálogo **Actualizar**, seleccione los tres puntos (**...**) en los atributos de filtrado.
6. Se abre la ventana de atributos de filtrado y proporciona una lista de todos los atributos de la entidad y las dimensiones de precios. Seleccione las casillas para los atributos de dimensión de precios.
7. Seleccione **Aceptar** para cerrar la página y, a continuación, seleccione **Actualizar paso**.
8. Repita los pasos del 2 al 7 para el segundo complemento, **PreOperationQuoteLineDetail**. Para este complemento, tiene que actualizar el paso **Actualización de msdyn_quotelinetransaction**.
9. Cierre **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]