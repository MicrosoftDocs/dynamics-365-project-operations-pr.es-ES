---
title: Extensión de entradas de tiempo
description: Este tema proporciona información sobre cómo los desarrolladores pueden extender el control de entrada de tiempo.
author: stsporen
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 02ed62c9ea27429b4b1d95d67d1607a090ab1dd2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996002"
---
# <a name="extending-time-entries"></a>Extensión de entradas de tiempo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations incluye un control personalizado de entrada de tiempo extensible. Este control incluye las siguientes características:

- Introduzca el tiempo horizontalmente durante una semana
- Totales por día, fila o semana
- Copiar filas o semanas
- Entrada de tiempo mediante HH: mm o HH.hh (se convierte automáticamente a HH.hh)
- Importar desde asignaciones, reservas o citas

Es posible extender las entradas de tiempo en dos áreas:
- [Agregar entradas de tiempo personalizadas para su propio uso](#add)
- [Personalizar el control semanal de entrada de tiempo](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Agregar entradas de tiempo personalizadas para su propio uso

Las entradas de tiempo son una entidad de núcleo utilizada en múltiples escenarios. En la Oleada 1 de abril de 2020 se presentó la solución principal de TESA. TESA proporciona una entidad **Configuración** y un nuevo rol de seguridad **Usuario de entrada de tiempo**. Los nuevos campos, **msdyn_start** y **msdyn_end**, que tienen una relación directa con **msdyn_duration**, también se incluyeron. La nueva entidad, el rol de seguridad, y los campos permiten un enfoque más unificado del tiempo en varios productos.


### <a name="time-source-entity"></a>Entidad de origen de tiempo
| Campo | Descripción | 
|-------|------------|
| Nombre  | El nombre de la entrada de origen de tiempo utilizado como valor de selección durante la creación de las entradas de tiempo. |
| Origen de tiempo predeterminado [Origen de tiempo: isdefault] | De forma predeterminada, solo se puede marcar en el predeterminado. Esta capacidad permite que las entradas se establezcan de forma predeterminada en un origen de tiempo si no se especifica uno. |
|Tipo de origen de tiempo [Origen de tiempo: sourcetype] | El tipo de origen es una opción (Tipo de origen de entrada de tiempo) que permite la asociación del origen de tiempo a una aplicación. Microsoft reserva valores superiores a 190 000 000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entradas de tiempo y la entidad de origen de tiempo
Cada entrada de tiempo está asociada a un registro de origen de tiempo. Este registro determina cómo y qué aplicaciones deben procesar la entrada de tiempo.

Las entradas de tiempo son siempre un bloque de tiempo contiguo con el inicio, el final y la duración vinculados.

La lógica actualizará automáticamente el registro de entrada de tiempo en las siguientes situaciones:

- Si se proporcionan dos de los tres campos siguientes, el tercero se calcula automáticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Los campos,**msdyn_start** y **msdyn_end**, son dependientes de la zona horaria.
- Entradas de tiempo creadas con solo **msdyn_date** y **msdyn_duration** especificado comenzará a la medianoche. Los campos **msdyn_start** y **msdyn_end** se actualizarán en consecuencia.

#### <a name="time-entry-types"></a>Tipos de entradas de tiempo

Los registros de entrada de tiempo tienen un tipo asociado que define el comportamiento en el flujo de envío para la aplicación asociada.

|Etiqueta | valor|
|-----|-----|
|En descanso   |192,355,000|
|Viaje | 192,355,001|
|Horas extra   | 192,354,320|
|Trabajo   | 192,350,000|
|Ausencia    | 192,350,001|
|Vacaciones   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizar el control semanal de entrada de tiempo
Los desarrolladores pueden agregar campos y búsquedas adicionales a otras entidades e implementar reglas de negocio personalizadas para apoyar sus escenarios comerciales.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Adición de campos personalizados con búsquedas a otras entidades
Existen tres pasos principales para agregar un campo personalizado a la cuadrícula de entrada de tiempo semanal.

1. Agregue el campo personalizado al cuadro de diálogo de creación rápida.
2. Configure la cuadrícula para mostrar el campo personalizado.
3. Agregue el campo personalizado al flujo de tareas de edición de filas o al flujo de tareas de edición de celdas.

Asegúrese de que el nuevo campo tenga las validaciones requeridas en el flujo de tareas de edición de fila o celda. Como parte de este paso, debe bloquear el campo, en función del estado de entrada de tiempo.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adición del campo personalizado al cuadro de diálogo de creación rápida
Agregue el campo personalizado al cuadro de diálogo **Creación rápida de entrada de tiempo**. Entonces, cuando se agregan las entradas de tiempo se puede introducir un valor seleccionando **Nuevo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configuración de la cuadrícula para mostrar el campo personalizado
Existen dos formas de agregar un campo personalizado a la cuadrícula de entrada de tiempo semanal:

  - Personalizar una vista y agregar un campo personalizado
  - Crear una nueva entrada de tiempo personalizada predeterminada 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Personalizar una vista y agregar un campo personalizado

Personalice **Mis entradas de tiempo semanales** y agregue el campo personalizado. Puede elegir la posición y el tamaño del campo personalizado en la cuadrícula editando las propiedades en la vista.

#### <a name="create-a-new-default-custom-time-entry"></a>Crear una nueva entrada de tiempo personalizada predeterminada

Esta vista debe contener los campos **Descripción** y **Comentarios externos**, además de las columnas que desea tener en la cuadrícula. 

1. Elija la posición, el tamaño y el criterio de ordenación predeterminado de la cuadrícula editando esas propiedades en la vista. 
2. Configure el control personalizado para esta vista, para que sea un control **Cuadrícula de entrada de tiempo**. 
3. Agregue este control a la vista y selecciónelo para la web, el teléfono y la tableta. 
4. Configure los parámetros para la cuadrícula de entrada de tiempo semanal. 
5. Establezca el campo **Fecha de inicio** en **msdyn_date**, el campo **Duración** en **msdyn_duration** y el campo **Estado** en **msdyn_entrystatus**. 
6. Para la vista predeterminada, el campo **Lista de estado de solo lectura** está configurado en **192350002,192350003,192350004**. El campo **Flujo de tareas de edición de filas** está configurado en **msdyn_timeentryrowedit**. El campo **Flujo de tareas de edición de celda** está configurado en **msdyn_timeentryedit**. 
7. Puede personalizar estos campos para agregar o eliminar el estado de solo lectura, o para usar una experiencia basada en tareas (TBX) diferente para la edición de filas o celdas. Estos campos ahora están vinculados a un valor estático.


> [!NOTE] 
> Ambas opciones eliminarán algunos filtros listos para usar en las entidades **Proyecto** y **Tarea de proyecto**, por lo que todas las vistas de búsqueda para las entidades serán visibles. Con los filtros listos para usar, solo se verán las vistas de búsqueda relevantes.

Debe determinar el flujo de tareas apropiado para el campo personalizado. Si agregó el campo a la cuadrícula, debe ir en el flujo de tareas de edición de fila que se utiliza para los campos que se aplican a toda la fila de entradas de tiempo. Si el campo personalizado tiene un valor único todos los días, como un campo personalizado para **Hora de finalización**, debe ir en el flujo de tareas de edición de celda.

Para agregar el campo personalizado a un flujo de tareas, arrastre un elemento **Campo** a la posición adecuada en la página y, a continuación, establezca las propiedades del campo. Establezca la propiedad **Origen** en **Entrada de tiempo** y la propiedad **Campo de datos** en el campo personalizado. La propiedad **Campo** especifica el nombre para mostrar en la página TBX. Seleccione **Aplicar** para guardar sus cambios en el campo y luego seleccione **Actualizar** para guardar sus cambios en la página.

Para utilizar una nueva página TBX personalizada, cree un nuevo proceso. Establezca la categoría en **Flujo de proceso de negocio**, la entidad en **Entrada de tiempo** y el tipo de proceso de negocio en **Ejecutar proceso como un flujo de tareas**. En **Propiedades**, la propiedad **Nombre de página** debe establecerse en el nombre para mostrar de la página. Agregue todos los campos relevantes a la página TBX. Guarde y publique el proceso. Actualice la propiedad de control personalizado para el flujo de tareas relevante al valor de **Nombre** en el proceso.

### <a name="add-new-option-set-values"></a>Adición de nuevos valores de conjunto de opciones
Para agregar valores de conjunto de opciones a un campo listo para usar, abra la página de edición para el campo y, a continuación, en **Tipo**, seleccione **Editar** junto al conjunto de opciones. Agregar una nueva opción que tenga una etiqueta y un color personalizados. Si desea agregar un nuevo estado de entrada de tiempo, el campo listo para usar se denomina **Estado de entrada**, no **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designación de un nuevo estado de entrada de tiempo como solo lectura
Para designar un nuevo estado de entrada de tiempo como de solo lectura, agregue el nuevo valor de entrada de tiempo a la propiedad **Lista de estados de solo lectura**. La parte editable de la cuadrícula de entrada de tiempo se bloqueará para las filas que tienen el nuevo estado.
A continuación, agregue reglas comerciales para bloquear todos los campos en las páginas TBX **Editar fila de entrada de tiempo** y **Editar entrada de tiempo**. Puede acceder a las reglas comerciales para estas páginas abriendo el editor de flujo de proceso de negocio para la página y, a continuación, seleccionando **Reglas de negocio**. Puede agregar el nuevo estado a la condición en las reglas de negocio existentes, o puede agregar una nueva regla comercial para el nuevo estado.

### <a name="add-custom-validation-rules"></a>Adición de reglas de validación personalizadas
Hay dos tipos de reglas de validación que puede agregar para la experiencia de la cuadrícula de entrada de tiempo semanal:

- Reglas comerciales del lado del cliente que funcionan en cuadros de diálogo de creación rápida y en páginas TBX.
- Validaciones de complementos del lado del servidor que se aplican a todas las actualizaciones de entrada de tiempo.

#### <a name="business-rules"></a>Reglas de negocio
Use reglas de negocio para bloquear y desbloquear campos, introducir valores predeterminados en los campos y definir validaciones que requieran información solo del registro de entrada de tiempo actual. Puede acceder a las reglas comerciales para una página TBX abriendo el editor de flujo de proceso de negocio para la página y, a continuación, seleccionando **Reglas de negocio**. Luego puede editar las reglas de negocio existentes o agregar una nueva. Para validaciones aún más personalizadas, puede usar una regla de negocio para ejecutar JavaScript.

#### <a name="plug-in-validations"></a>Validaciones de complementos
Usar validaciones de complementos para cualquier validación que requiera más contexto del que está disponible en un registro de entrada de tiempo único, o para cualquier validación que desee ejecutar en actualizaciones en línea en la cuadrícula. Para completar la validación, cree un complemento personalizado en la entidad **Entrada de tiempo**.

### <a name="copying-time-entries"></a>Copiar entradas de tiempo
Use la vista **Copiar columnas de entrada de tiempo** para definir la lista de campos a copiar durante la entrada de tiempo. **Fecha** y **Duración** son campos obligatorios y no deben eliminarse de la vista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]