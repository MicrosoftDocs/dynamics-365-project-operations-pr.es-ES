---
title: Divisa
description: En este tema se proporciona información sobre cómo agregar y quitar tipos de divisa en Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 093eaa78b5f88aee364a753374a56c33e20a5ce3
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642294"
---
# <a name="currency"></a>Divisa

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Las divisas determinan los precios de los productos en el catálogo de productos y el coste de las transacciones, como los pedidos de ventas. Si sus clientes están distribuidos por distintas geografías, agregue las divisas para administrar sus transacciones. Agregue las divisas que sean más apropiadas para sus necesidades de negocio actuales y futuras.  

> [!NOTE]
> Si su entorno es un entorno de Common Data Service, se encuentra en el Centro de administración de Power Platform y selecciona la página **Divisas** (**Entornos** > [seleccionar ambiente] > **Configuración** >  **Empresa** > **Divisas**), la página estará en blanco. Esto se debe a que en entornos de Common Data Service no se admite la configuración de una divisa.

## <a name="add-a-currency"></a>Agregar una divisa  
Antes de comenzar este procedimiento, verifique que su rol de seguridad incluye permisos de administrador del sistema. 

1. En el centro de administración de Power Platform, seleccione un entorno. 
2. Seleccione **Configuración** > **Empresa**.
3. Seleccione **Divisas**.  
4. Seleccione **Nuevo**.  
5. Complete la información según corresponda.  


   |          Campo          |                                                                                                                                                                                                                                                                                                                                                                            Descripción                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipo de divisa**    | - **Sistema**: seleccione esta opción si desea usar las divisas disponibles en aplicaciones basadas en modelos de Dynamics 365. Para buscar una divisa, seleccione **Búsqueda**. Cuando selecciona un código de divisa, **Nombre de divisa** y **Símbolo de divisa** se agregan automáticamente para la divisa seleccionada.<br />- **Personalizar**: seleccione esta opción si desea agregar una divisa que no está disponible en aplicaciones basadas en modelos de Dynamics 365. En este caso, debe especificar manualmente los valores de **Código de divisa**, **Precisión de divisa**, **Nombre de divisa**, **Símbolo de divisa** y **Conversión de divisa**. |
   |    **Código de divisa**    |                                                                                                                                                                                                                                                                                                                                            Formulario corto de la divisa. Por ejemplo, **USD** para dólar estadounidense.                                                                                                                                                                                                                                                                                                                                            |
   | **Precisión de divisa**  |                                                                                                                                                                                  Escriba el número de decimales que desea usar para la divisa.  Puede agregar un valor entre 0 y 4. **Nota:** Si ha establecido un valor de precisión en el cuadro de diálogo **Configuración del sistema**, ese valor aparecerá aquí.                                                                                                                                                                                  |
   |    **Nombre de divisa**    |                                                                                                                                                                                                                                         Si ha seleccionado un código de divisa en la lista de divisas disponibles en las aplicaciones basadas en modelos en Dynamics 365, el nombre de la divisa para el código seleccionado se muestra aquí. Si seleccionó **Personalizado** como tipo de divisa, escriba el nombre de la divisa.                                                                                                                                                                                                                                          |
   |   **Símbolo de divisa**   |                                                                                                                                                                                                                                                                      Si ha seleccionado un código de divisa en la lista de divisas disponibles, el símbolo para la divisa seleccionada se muestra aquí. Si seleccionó **Personalizado** como tipo de divisa, introduzca el símbolo para la nueva divisa.                                                                                                                                                                                                                                                                       |
   | **Conversión de divisas** |                                                                                                                                                                                                                                     Escriba el valor de la divisa seleccionada en términos de un dólar estadounidense. Este es el importe en el que la divisa seleccionada se convierte a la divisa base. **Importante:** asegúrese de actualizar este valor con la frecuencia necesaria para evitar cualquier cálculo impreciso en sus transacciones.                                                                                                                                                                                                                                      |


6. Cuando haya terminado, seleccione **Guardar** o **Guardar y cerrar** en la barra de comandos.  

   > [!TIP]
   >  Para editar una divisa, seleccione la divisa y escriba o seleccione los nuevos valores.  

## <a name="delete-a-currency"></a>Eliminar una divisa  

1. En el centro de administración de Power Platform, seleccione un entorno. 
2. Seleccione **Configuración** > **Empresa**.
3. Seleccione **Divisas**.  
4. En la lista de divisas que se muestra, seleccione la divisa para eliminar.  
5. Seleccione **Eliminar**.  
6. Confirme la eliminación.  

> [!IMPORTANT]
>  No puede eliminar divisas que se encuentran en uso por otros registros; solo puede desactivarlas. Al desactivar los registros de divisa, no se quita la información de divisa almacenada en los registros existentes, como las oportunidades o los pedidos. Sin embargo, no podrá seleccionar la divisa desactivada para nuevas transacciones.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]