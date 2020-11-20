---
title: Líneas de oferta basadas en producto
description: En este tema se proporciona información sobre líneas de oferta basadas en productos.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123236"
---
# <a name="product-based-quote-lines"></a>Líneas de oferta basadas en producto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Puede crear líneas de oferta basadas en productos en Dynamics 365 Project Service Automation. Las líneas de oferta basadas en productos pueden ser líneas de "escritura" o artículos del catálogo de productos.

## <a name="product-catalog"></a>Catálogo de productos

Los productos de un catálogo de productos de Dynamics 365 tienen una unidad de venta y una unidad predeterminada. Si varios productos comparten el mismo conjunto de atributos, puede crear una familia de productos que también tenga esos atributos. Todos los productos de una familia de productos heredan el mismo conjunto de atributos.

Por ejemplo, una empresa vende licencias de suscripción para una variedad de software. Por lo tanto, todo el software de suscripción tendrá los siguientes dos atributos:

- Número de usuarios 
- Duración de la suscripción (en meses)

Una buena forma de mantener este tipo de catálogo es crear una familia de productos que se denomine **Software de suscripción** y que tenga como atributos **Número de usuarios** y **Duración de la suscripción**. A continuación, puede agregar productos individuales, como **Dynamics 365 Sales** o **Dynamics 365 Field Service** a la familia de productos de **Software de suscripción**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Adición de artículos del catálogo de productos a una oferta de proyecto

Las páginas de oferta y contrato de proyecto tienen secciones para dos tipos de líneas: líneas basadas en proyectos y líneas basadas en productos. Para líneas basadas en productos, Dynamics 365 se usa para agregar artículos de un catálogo de productos a una oferta. La lista desplegable en la línea de oferta o en la línea de contrato del proyecto incluye todos los productos y unidades en la lista de precios de productos que se adjunta a la oferta o contrato del proyecto. También puede agregar productos que no forman parte de la lista de precios de productos de la oferta.

Además, puede seleccionar productos de otras listas de precios, o puede elegir productos directamente desde el catálogo de productos. Cuando seleccione productos directamente de un catálogo de productos, la lista de precios predeterminada de ese producto se utilizará para obtener el precio de venta del producto. Si no se establece una lista de precios predeterminada, el precio se establece en 0 (cero).

Si una línea de oferta se basa en un catálogo de productos, puede reemplazar el precio de venta directamente en la línea de oferta. Tenga en cuenta que una línea de oferta en Dynamics 365 tiene un campo **Precios**. Hay dos valores disponibles:

- Reemplazar precio  
- Usar valor predeterminado

Si establece este campo en **Reemplazar precio**, Dynamics 365 no establece un precio predeterminado. Debe escribir un precio para el producto en la línea de oferta. Si establece este campo en **Usar valor predeterminado**, Dynamics 365 usa el precio de venta predeterminado y bloquea el campo para evitar la edición.

Después de instalar PSA, los precios de venta predeterminados se introducen en las líneas basadas en productos en una oferta. El campo **Precios** se establece en **Reemplazar precio** para que pueda editar el precio predeterminado en las líneas de oferta.

> ![Configuración de Reemplazar precio](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Factores de cantidad para productos

PSA utiliza factores de cantidad para respaldar la venta de productos basados ​​en suscripción. Para productos basados ​​en suscripción, la cantidad en la línea de oferta o contrato del proyecto se expresa como el número de meses de usuario.

Por lo general, el precio del software de suscripción se almacena en el catálogo como el precio por usuario por mes. Sin embargo, puede utilizar otras descripciones de tiempo en su lugar. Durante el proceso de venta, el precio en la línea de oferta suele ser el precio por usuario, por mes que negoció y descontó el agente de ventas de TI. Cada operación tiene un número diferente de usuarios y un número diferente de meses de suscripción. La cantidad que se utiliza para calcular la cantidad de la línea de oferta es un producto de la cantidad de usuarios y la cantidad de meses de suscripción.

Para respaldar este tipo de venta, PSA introdujo el concepto de factores de cantidad. Los factores de cantidad dependen de los atributos del producto en Dynamics 365. Cuando configura propiedades específicas para un producto, PSA le permite marcar un subconjunto de esas propiedades, o todas las propiedades, como factores de cantidad.

PSA valida que solo las propiedades numéricas o las propiedades del producto que tienen un tipo de datos numéricos se marcan como factores de cantidad. Cuando un producto para el que se configuran los factores de cantidad se agrega a una línea de oferta, el campo **Cantidad** en la línea de oferta se convierte en un campo de solo lectura. Después de introducir valores para las propiedades del producto que son factores de cantidad, PSA calcula la cantidad de la línea de oferta.

Por ejemplo, Dynamics 365 podría tener las siguientes propiedades: 

- **Número de usuarios**: el número de usuarios. 
- **Número de meses**: el número de meses de suscripción.
- **SKU de producto** 

Las propiedades **Número de usuarios** y **Número de meses** se pueden marcar como factores de cantidad editando las propiedades de la línea de productos. 

> ![Marcado de Número de usuarios y Número de meses como factores de calidad](media/basic-guide-11.png)
 
