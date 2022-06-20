---
title: Adición de campos personalizados a la configuración de precios y entidades transaccionales
description: En este artículo se proporciona información sobre cómo agregar campos personalizados a la configuración de precios y las entidades transaccionales.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: b666d1767306b9833fba36c6ed2c59a633c5fdf0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920495"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Adición de campos personalizados a la configuración de precios y entidades transaccionales 

[!include [banner](../includes/psa-now-project-operations.md)]

En este artículo se supone que ha completado los procedimientos que se describen en el artículo [Crear campos y entidades personalizados](create-custom-fields-entities.md). Si no ha completado esos procedimientos, vuelva y complételos y, a continuación, regrese a este artículo. 

En este artículo, los procedimientos mostrarán cómo agregar las referencias de campos personalizadas necesarias a las entidades y los elementos de la interfaz de usuario como los formularios y las vistas.

## <a name="add-custom-pricing-dimension-fields"></a>Agregar campos de dimensiones de precios personalizadas 
Tras crear los campos y las entidades personalizadas, el siguiente paso es que la configuración de precios y las entidades transaccionales conozcan las entidades personalizadas o los conjuntos de opciones con la creación de campos de referencia. En función de si su lista de dimensiones de precios incluye dimensiones de conjuntos de opciones, dimensiones de entidad o ambas cosas, siga solo los pasos que se describen en **Dimensiones de precio personalizadas basadas en conjuntos de opciones**, en **Dimensiones de precio personalizadas basadas en entidades** o en ambas secciones, respectivamente.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensiones de precios personalizadas basadas en conjuntos de opciones
Cuando una dimensión de precio personalizada se basa en conjuntos de opciones, agréguela como campo a las entidades clave de Project Service. En el procedimiento siguiente, **Ubicación de trabajo del recurso** y **Horas de trabajo del recurso** se utilizan como dimensiones de precios basadas en conjuntos de opciones. Estas se deben agregar primero como campos a las entidades de precio **Precio de rol** e **Incremento del precio de rol**.

1. En Project Service Automation (PSA), haga clic en **Configuración** > **Soluciones** y después haga doble clic en **Dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Precio de rol**.
3. Expanda la entidad **Precio de rol** y seleccione **Campos**.
4. Haga clic en **Nuevo** para crear un nuevo campo llamado **Ubicación de trabajo del recurso** y seleccione **Conjunto de opciones** como tipo de campo. 
5. Seleccione **Utilizar un conjunto de opciones existente**, seleccione el conjunto de opciones **Ubicación de trabajo del recurso** y después haga clic en **Guardar**.
6. Repita los pasos del 1 al 5 para agregar este campo a la entidad **Incremento del precio de rol**. 
7. Repita los pasos del 1 al 5 para el conjunto de opciones **Horas de trabajo del recurso**.

> [!IMPORTANT]
> Cuando se agrega un campo a más de una entidad, use el mismo nombre de campo en todas las entidades. 

> ![Agregar la ubicación de trabajo del recurso al precio de rol.](media/RWL-Field.png)

En las fases de ventas y estimación de un proyecto, las estimaciones del esfuerzo de trabajo necesario para completar el trabajo **Local** e **In situ**, en **Horas ordinarias** y **Horas extra** se usan para estimar el valor de la oferta o el proyecto. Los campos **Ubicación de trabajo del recurso** y **Horas de trabajo del recurso** se agregarán a las entidades de estimación **Detalle de línea de oferta**, **Detalle de línea de contrato**, **Tarea de proyecto**, **Miembro del equipo del proyecto** y **Línea de estimación**.

1. En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Detalle de línea de oferta**.
3. Expanda la entidad **Detalle de línea de oferta** y seleccione **Campos**.
4. Haga clic en **Nuevo** para crear un nuevo campo llamado **Ubicación de trabajo del recurso** y seleccione el tipo de campo **Conjunto de opciones**. 
5. Seleccione **Utilizar un conjunto de opciones existente** y **Ubicación de trabajo del recurso** y después haga clic en **Guardar**.
6. Repita los pasos del 1 al 5 para agregar este campo a las entidades **Detalle de línea de contrato de proyecto**, **Tarea de proyecto**, **Miembro del equipo del proyecto** y **Línea de estimación**.
7. Repita los pasos del 1 al 6 para el conjunto de opciones **Horas de trabajo del recurso**. 

> ![Agregar la ubicación de trabajo del recurso a la línea de estimación.](media/RWL-Default-Value.png)


Para la entrega y la facturación, el precio del trabajo completado se debe valorar de manera exacta para seleccionar si se realizó de forma **Local** o **In situ** y si se completó durante **Horas normales** u **Horas extras** en los datos reales del proyecto. Los campos **Ubicación de trabajo del recurso** y **Horas de trabajo del recurso** se deben agregar a las entidades **Entrada de tiempo**, **Real**, **Detalle de línea de factura** y **Línea de diario**.

1. En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**.
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Entrada de tiempo**.
3. Expanda la entidad **Detalle de línea de oferta** y después seleccione **Campos**.
4. Haga clic en **Nuevo** para crear un nuevo campo llamado **Ubicación de trabajo del recurso** y seleccione **Conjunto de opciones** como tipo de campo. 
5. Seleccione **Utilizar un conjunto de opciones existente**, seleccione el conjunto de opciones **Ubicación de trabajo del recurso** y después haga clic en **Guardar**.
6. Repita los pasos del 1 al 5 para agregar este campo a las entidades **Real**, **Detalle de línea de factura** y **Línea de diario**.
7. Repita los pasos del 1 al 6 para el conjunto de opciones **Horas de trabajo del recurso**. 

> ![Agregar la ubicación de trabajo del recurso a la entrada de tiempo.](media/RWL-time-entry.png)

Esto completa los cambios de esquema necesarios para las dimensiones personalizadas basadas en conjuntos de opciones.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensiones de precios personalizadas basadas en entidades

Cuando la dimensión de precios personalizada es una entidad, deberá agregar relaciones de 1:N entre la entidad de la dimensión y las entidades clave de Project Service. Utilizando el ejemplo de título estándar anterior, es razonable esperar que se asigne a cada empleado un título estándar. Como resultado, necesitará una relación de 1:N entre el título estándar y el recurso que se puede reservar, o bien una relación de N:1 si se crearon desde un recurso que se puede reservar a un título estándar.

1. En PSA, haga clic en **Configuración** > **Soluciones** y luego haga doble clic en **dimensiones de precios de \<your organization name>**. 
2. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Título estándar**.
3. Expanda la entidad **Título estándar** y seleccione **Relaciones de 1:N**.
4. Haga clic en **Nuevo** para crear una nueva relación de 1:N con el nombre **Título estándar a recurso que se puede reservar**. Especifique la información necesaria y después haga clic en **Guardar**.

> ![Agregar el título estándar como un campo de referencia a un recurso que se puede reservar.](media/ST-BR.png)

El título estándar también deberá agregarse a las entidades de precios de Project Service, **Precio de Rol** e **Incremento del precio de rol**. Esto también se puede realizar utilizando relaciones de 1:N entre las entidades **Título estándar** y **Rol de precio** y las entidades **Título estándar** e **Incremento del precio de rol**.

1. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Título estándar**.
2. Expanda la entidad **Título estándar** y seleccione **Relaciones de 1:N**.
3. Haga clic en **Nuevo** para crear una nueva relación de 1:N con el nombre **Título estándar a precio de rol**. Especifique la información necesaria y después haga clic en **Guardar**.
4. Repita los pasos del 1 al 4 para crear relaciones de 1:N entre las entidades **Título estándar** e **Incremento del precio de rol**.

En las fases de ventas y estimación del proyecto, para establecer el precio de la oferta o el proyecto, las estimaciones de esfuerzo de trabajo son necesarios para cada título estándar. Esto significa que se necesitan las relaciones de 1:N del título estándar a cada una de las entidades de Project Service que se indican a continuación: 

- **Detalle de línea de oferta**
- **Detalle de línea de contrato de proyecto**
- **Tarea de proyecto**
- **Miembro del equipo del proyecto**
- **Línea de estimación**

5. Repita los pasos del 1 al 5 para crear relaciones de 1:N de **Título estándar** a **Detalle de línea de oferta**, **Detalle de línea de contrato de proyecto**, **Tarea de proyecto**, **Miembro del equipo del proyecto** y **Línea de estimación**.

> ![Agregar el título estándar como un campo de referencia a la línea de estimación.](media/ST-Estimate-Line.png)

En las fases de entrega y facturación, el precio del trabajo completado por cada título estándar se debe valorar con exactitud en los datos reales de proyecto. Esto significa que debe haber relaciones de 1:N desde las entidades **Título estándar** hasta **Entrada de tiempo**, **Real**, **Detalle de línea de factura** y **Línea de diario**.

6. Repita los pasos del 1 al 6 para crear relaciones de 1:N desde las entidades **Título estándar** hasta las entidades **Entrada de tiempo**, **Real**, **Detalle de línea de factura** y **Línea de diario**.

> ![Agregar el título estándar como un campo de referencia a la entrada de tiempo.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurar el establecimiento del valor Dimensión como predeterminado utilizando las características de asignación de la plataforma
Para la entrada de tiempo, resultaría muy útil que el sistema proporcionara de manera predeterminada el título estándar en la entrada de tiempo desde el recurso que se puede facturar que está registrando la entrada de tiempo. Use los siguientes pasos para agregar asignaciones de campos a la relación de 1:N desde **Recurso que se puede reservar** hasta **Entrada de tiempo**.

1. En el Explorador de soluciones, en el panel de navegación izquierdo, seleccione **Entidades > Título estándar**.
2. Expanda la entidad **Título estándar** y seleccione **Relaciones de 1:N**.
3. Haga doble clic en **Recurso que se puede reservar a entrada de tiempo**. En la página **Relación**, haga clic en **Utilizar asignaciones de campos**. 
4. Haga clic en **Nuevo** para crear una nueva asignación de campos entre el campo **Título estándar** de la entidad **Recurso que se puede reservar** hasta el campo de referencia **Título estándar** de la unidad **Entrada de tiempo**. 

> ![Configurar las asignaciones de campos para permitir establecer como predeterminado el título estándar desde Recurso que se puede reservar hasta Entrada de tiempo.](media/ST-Mapping2.png)


Esto completa los cambios de esquema necesarios para las dimensiones personalizadas basadas en entidades.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Agregar campos personalizados a formularios, vistas y reglas de negocio

Tras realizar todos los cambios de esquema necesarios, el siguiente paso es hacer que los campos estén visibles en la interfaz de usuario. Para ello, agregue los campos a los formularios y las vistas.

1. Abra el formulario o la vista. En el panel de navegación derecho, seleccione el campo y arrástrelo al lienzo de formulario. 
2. Si va a editar una vista, utilice el panel de navegación derecho, haga clic en **Agregar campos** y, en el cuadro de diálogo **Listado de campos**, seleccione los campos que necesite y haga clic en **Aceptar**.

La tabla siguiente proporciona una lista completa de los formularios y las vistas estándar por entidad que deberán actualizarse con los nuevos campos. Si tiene formularios o vistas adicionales en sus personalizaciones acerca de estas entidades, agregue también los campos nuevos.

| Entidad de Project Service        | Formularios que necesitan el nuevo campo   |Vistas que necesitan el nuevo campo      |
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

Es posible que también tenga que agregar los campos personalizados a las reglas de negocio en función de lo que definió. Un ejemplo estándar es para la regla de negocio **Capacidad de edición de entradas de tiempo según estado**. Esta regla define los campos que se deben bloquear cuando la Entrada de tiempo tiene un estado no editable como, por ejemplo, **Aprobado**. Agregue los campos a esta regla de negocio para que los campos se bloqueen y no se puedan editar cuando la Entrada de tiempo tenga un estado distinto de **Borrador** o **Devuelto**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
