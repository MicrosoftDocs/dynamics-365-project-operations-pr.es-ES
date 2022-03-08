---
title: Utilizar un recurso que se puede reservar como dimensión de precios
description: En este tema se proporciona información sobre el uso de un recurso que se puede reservar como dimensión de precios.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c551673708ae2d965979136e92326be98252304a601964c1fbc52a329c592712
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988987"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utilizar un recurso que se puede reservar como dimensión de precios

[!include [banner](../includes/psa-now-project-operations.md)]

En este tema se proporciona información sobre el uso de un recurso que se puede reservar como dimensión de precios. Antes de comenzar, si aún no ha creado una solución de dimensión de precios, deberá crear una nueva. Si ya tiene una solución de dimensión de precios, puede realizar los cambios en esa solución. Si no ha creado una nueva solución de dimensión de precios para su organización, complete los procedimientos en el tema [Creación de campos y entidades](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Agregar un recurso que se puede reservar a formularios y vistas
Para que los campos sean visibles en la interfaz de usuario en la solución de dimensión de precios, deberá recorrer todos los formularios y las vistas de las entidades clave de Project Service y agregar estos campos a los formularios y las vistas de dichas entidades.
La tabla siguiente ofrece una lista completa de los formularios y las vistas estándar por entidad que deberán actualizarse. Si hay formularios o vistas adicionales en sus personalizaciones acerca de estas entidades, agregue también los campos nuevos.
Abra el Explorador de soluciones de la solución de dimensión de precios y después haga clic en **Publicar todas las personalizaciones**.


|   Entidad        | Formularios   |Vistas        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurar un recurso que se puede reservar como dimensión de precios

1. En la interfaz web, vaya a **Project Service** > **Configuración** > **Parámetros**. En la página **Parámetro**, en la pestaña **Dimensiones de precios basadas en el importe**, observe que la cuadrícula de la pestaña muestra los registros en la entidad de dimensiones de precios. 
2. Agregue el **Recurso que se puede reservar** a la lista de dimensiones de precios como **msdyn_bookableresource**. 
3. Indique el contexto en el que el recurso que se puede reservar se usa como dimensión de precios y establezca los valores **Aplicable a costes** y valores **Aplicable a ventas**.
4. En el campo **Tipo de dimensión**, seleccione **Basado en el importe**. 
5. Seleccione el coste y la prioridad de ventas para el recurso que se puede reservar. Normalmente, cuando se incluye como dimensión de precios, un recurso que se puede reservar tiene la máxima prioridad. De este modo, si establece este valor en **1** (o **0**, en función de cómo se cuenta la prioridad), se asegurará de obtener este comportamiento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nombres de campo de dimensión de precios

Cuando el nombre del campo de una dimensión de precios de la tabla **Precio de rol** es distinto del nombre de campo de cualquiera de las demás entidades en las que debe funcionar el establecimiento del precio predeterminado, el registro de la dimensión de cálculo de precios debe estar al tanto de los distintos nombres.    
Para los recursos que se pueden reservar, la entidad **Miembros del equipo del proyecto** tiene un nombre de campo un poco diferente (**msdyn_bookableresourceid**) del de la entidad **Precio de rol** (**msdyn_bookableresource**). El registro de la dimensión de precios para **msydn_bookableresource** debe estar al tanto de ello. 
1. Para ello, haga doble clic en la fila de la cuadrícula **Dimensiones de precios** para abrir la página de la dimensión de **msdyn_bookableresource**.
2. En la página de la dimensión, en la pestaña **Relacionado**, haga clic en **Nombres de campos de la dimensión de precios**.

 ![Pestaña de nombres del campo de la dimensión de precios.](media/PD-fieldname.png)

4. En la vista asociada que se abre, haga clic en **Agregar nuevo nombre del campo de la dimensión de precios**.

 ![Agregar nuevos nombres del campo de la dimensión de precios.](media/Add-NewPD-fieldname.png)


Esto abre la página **Nuevo nombre de campo de la dimensión de precios** para **msdyn_bookableresource**. 

5. Agregue **msdyn_projectteam** al campo **Nombre lógico de la entidad** y **msdyn_bookableresourceid** al campo **Nombre de campo**. Guarde el registro.

 ![Formulario de nuevo nombre del campo de la dimensión de precios.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]