---
title: Uso de la categoría de transacción como una dimensión de precios
description: En este tema se proporciona información sobre el uso de una categoría de transacción como dimensión de precios.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 00214aa2b514da71b331073cd0eeb5320c03e7d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150779"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Uso de la categoría de transacción como una dimensión de precios

[!include [banner](../includes/psa-now-project-operations.md)]

En este tema se muestra cómo usar una categoría de transacción como dimensión de precios. Antes de comenzar, si aún no ha creado una solución de dimensión de precios, deberá crear una nueva. Si ya tiene una solución de dimensión de precios, puede realizar los cambios en esa solución. Si no ha creado una nueva solución de dimensión de precios para su organización, complete los procedimientos en el tema [Creación de campos y entidades](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Adición de la categoría de transacciones para formularios y vistas
Para que la categoría de transacción sea visible en la interfaz de usuario en la solución de dimensión de precios, deberá recorrer todos los formularios y las vistas de las entidades clave de Project Service y agregar estos campos a los formularios y las vistas de dichas entidades.
La tabla siguiente es una lista completa de los formularios y las vistas estándar por entidad que deberán actualizarse con los nuevos campos. Si hay formularios o vistas adicionales en sus personalizaciones acerca de estas entidades, agregue también los campos nuevos.

|  Entidad        | Formularios     |Vistas        |
| ------------------------------|---------------------------------|----------------------------------|
|  Precio de rol|• Información |• Precios de categorías de recursos activos<br> • Vista asociada de precios de categorías de recursos|
|  Incremento del precio de rol|• Información|• Incremento del precio de rol activo<br>• Vista asociada del incremento del precio de rol|
|  Detalle de línea de oferta|• Información del proyecto<br>• Creación rápida de proyecto|• Detalle de línea de oferta activo<br>• Detalles de líneas de oferta combinadas<br>• Vista asociada de detalles de líneas de oferta|
|  Detalle de línea de contrato del proyecto|• Información del proyecto<br>• Creación rápida de proyecto|• Detalles de línea de contrato combinados<br>• Detalles de línea de contrato activos<br>• Vista asociada de detalles de línea de contrato|
|  Tarea de proyecto|• Información<br>• Nuevo formulario||
|  Miembro del equipo del proyecto|• Información<br>• Nuevo formulario|• Miembros del equipo del proyecto activos<br>• Miembros del equipo del proyecto<br>• Vista asociada de miembros del equipo del proyecto|
|  Entrada de tiempo|• Información<br>• Crear entrada de tiempo|• Mis entradas de tiempo por fecha<br>• Mis entradas de tiempo para esta semana<br>• Entradas de tiempo pendientes de aprobación|
|  Línea del diario|• Información<br>• Creación rápida|• Líneas de diario activas<br>• Vista asociada de líneas de diario|
|  Detalle de línea de factura|• Información<br>• Creación rápida|• Detalles de líneas de factura activos<br>• Transacciones de facturas imputables<br>• Transacciones de facturas gratuitas<br>• Vista asociada de detalle de línea de factura<br>• Transacciones de facturas no imputables|
|  Real|• Información<br>• Datos reales activos|• Vista asociada de datos reales|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configuración de la categoría de transacción como una dimensión de precios

1. En la interfaz web, vaya a **Project Service** > **Configuración** > **Parámetros**. 
2. En la página **Parámetros**, en la pestaña **Dimensiones de precios basadas en el importe**, observe que la cuadrícula de la pestaña muestra los registros en la entidad **Dimensiones de precios**.
3. Agregue **Categoría de transacciones** a esta lista y establezca los campos **Aplicable a costes** y **Aplicable a ventas** en **Sí**.
4. En el campo **Tipo de dimensión**, seleccione **Basado en el importe** y, a continuación, seleccione la prioridad para **Categoría de transacción** relacionada con el coste y las ventas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]