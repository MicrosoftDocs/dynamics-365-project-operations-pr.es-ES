---
title: Extensión de entradas de tiempo
description: Este tema proporciona información sobre cómo los desarrolladores pueden extender el control de entrada de tiempo.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583007"
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
Cada entrada de tiempo está asociada a un registro de origen de tiempo. Este registro determina qué aplicaciones deben procesar la entrada de tiempo y cómo.

Las entradas de tiempo son siempre un bloque de tiempo contiguo con el inicio, el final y la duración vinculados.

La lógica actualizará automáticamente el registro de entrada de tiempo en las siguientes situaciones:

- Si se proporcionan dos de los tres campos siguientes, el tercero se calcula automáticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Los campos **msdyn_start** y **msdyn_end** son conscientes de la zona horaria.
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

1. Agregue el campo personalizado al cuadro de diálogo **Creación rápida**.
2. Configure la cuadrícula para mostrar el campo personalizado.
3. Agregue el campo personalizado a la página **Edición de fila** o **Edición de entrada de tiempo**, según corresponda.

Asegúrese de que el nuevo campo tenga las validaciones requeridas en la página **Edición de fila** o **Edición de entrada de tiempo**. Como parte de esta tarea, debe bloquear el campo, en función del estado de la entrada de tiempo.

Cuando agrega un campo personalizado a la cuadrícula **Entrada de tiempo** y luego crea entradas de tiempo directamente en la cuadrícula, el campo personalizado para esas entradas se establece automáticamente para que coincida con la fila. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Agregar el campo personalizado al cuadro de diálogo Creación rápida
Debe agregar el campo personalizado al cuadro de diálogo **Creación rápida: crear entrada de tiempo**. Los usuarios pueden introducir un valor cuando agregan entradas de tiempo seleccionando **Nuevo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configuración de la cuadrícula para mostrar el campo personalizado
Existen dos formas de agregar un campo personalizado a la cuadrícula **Entrada de tiempo semanal**.

- Personalice la vista **Mis entradas de tiempo semanales** y agregue a ella el campo personalizado. Puede especificar la posición y el tamaño del campo personalizado en la cuadrícula, editando las propiedades en la vista.
- Cree una nueva vista de entrada de tiempo personalizada y establecerla como la vista predeterminada. Esta vista debe contener los campos **Descripción** y **Comentarios externos**, además de las columnas que desea que incluya la cuadrícula. Puede especificar la posición, el tamaño y el criterio de ordenación predeterminado de la cuadrícula editando las propiedades en la vista. A continuación, configure el control personalizado para esta vista para que sea un control **Cuadrícula de entrada de tiempo**. Agregue el control a la vista y selecciónelo para **Web**, **Teléfono** y **Tableta**. A continuación, configure los parámetros para la cuadrícula **Entrada de tiempo semanal**. Establezca el campo **Fecha de inicio** en **msdyn\_date**, el campo **Duración** en **msdyn\_duration** y el campo **Estado** en **msdyn\_entrystatus**. El campo **Lista de estado de solo lectura** se establece en **192350002 (Aprobado)**, **192350003 (Enviado)** o **192350004 (Coincidencia solicitada)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Agregar el campo personalizado a la página de edición apropiada
Las páginas que se utilizan para editar una entrada de tiempo o una fila de entradas de tiempo se pueden encontrar en **Formularios**. El botón **Editar entrada** de la cuadrícula abre la página **Editar entrada**, y el botón **Editar fila** abre la página **Edición de fila**. Puede editar estas páginas para que incluyan campos personalizados.

Ambas opciones eliminarán algunos filtros listos para usar en las entidades **Proyecto** y **Tarea de proyecto**, por lo que todas las vistas de búsqueda para las entidades son visibles. Con los filtros listos para usar, solo se verán las vistas de búsqueda relevantes.

Debe determinar la página apropiada para el campo personalizado. Lo más probable es que, si agregó el campo a la cuadrícula, debe ir en la página **Edición de fila** que se utiliza para los campos que se aplican a toda la fila de entradas de tiempo. Si el campo personalizado tiene un valor único en la fila todos los días (por ejemplo, si es un campo personalizado para el tiempo de finalización), debería ir en la página **Edición de entrada de tiempo**.

Para agregar el campo personalizado a una página, arrastre un elemento **Campo** a la posición adecuada en la página y, a continuación, configure sus propiedades.

### <a name="add-new-option-set-values"></a>Adición de nuevos valores de conjunto de opciones
Para agregar valores de conjunto de opciones a un campo listo para usar, siga estos pasos.

1. Abra la página de edición para el campo y, a continuación, en **Tipo**, seleccione **Editar** junto al conjunto de opciones.
2. Agregar una nueva opción que tenga una etiqueta y un color personalizados. Si desea agregar un nuevo estado de entrada de tiempo, el campo listo para usar se denomina **Estado de entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designación de un nuevo estado de entrada de tiempo como solo lectura
Para designar un nuevo estado de entrada de tiempo como de solo lectura, agregue el nuevo valor de entrada de tiempo a la propiedad **Lista de estados de solo lectura**. Asegúrese de agregar el número, no la etiqueta. La parte editable de la cuadrícula de entrada de tiempo se bloqueará ahora para las filas que tienen el nuevo estado. Para configurar la propiedad **Lista de estado de solo lectura** de forma diferente para diferentes vistas de **Entrada de tiempo** agregue la cuadrícula **Entrada de tiempo** en la sección de una vista **Controles personalizados** y configure los parámetros según corresponda.

A continuación, agregue reglas de negocio para bloquear todos los campos en las páginas **Editar fila** y **Editar entrada de tiempo**. Para acceder a las reglas de negocio para estas páginas, abra el editor de formularios para cada página y, a continuación, seleccione **Reglas de negocio**. Puede agregar el nuevo estado a la condición en las reglas de negocio existentes, o puede agregar una nueva regla comercial para el nuevo estado.

### <a name="add-custom-validation-rules"></a>Adición de reglas de validación personalizadas
Puede agregar dos tipos de reglas de validación para la experiencia de cuadrícula **Entrada de tiempo semanal**:

- Reglas de negocio del lado del cliente que funcionan en las páginas
- Validaciones de complementos del lado del servidor que se aplican a todas las actualizaciones de entradas de tiempo

#### <a name="client-side-business-rules"></a>Reglas de negocio del lado del cliente
Use reglas de negocio para bloquear y desbloquear campos, introducir valores predeterminados en los campos y definir validaciones que requieran información solo del registro de entrada de tiempo actual. Para acceder a las reglas de negocio para una página, abra el editor de formulario y, a continuación, seleccione **Reglas de negocio**. Luego puede editar las reglas de negocio existentes o agregar una nueva.

#### <a name="server-side-plug-in-validations"></a>Validaciones de complementos del lado del servidor
Debe usar validaciones de complementos para cualquier validación que requiera más contexto del que está disponible en un registro de entrada de tiempo único. También debe usarlos para cualquier validación que desee ejecutar en actualizaciones en línea en la cuadrícula. Para completar las validaciones, cree un complemento personalizado en la entidad **Entrada de tiempo**.

### <a name="limits"></a>Límites
Actualmente, la cuadrícula **Entrada de tiempo** tiene un límite de tamaño de 500 filas. Si hay más de 500 filas, las filas sobrantes no se mostrarán. No hay forma de aumentar este límite de tamaño.

### <a name="copying-time-entries"></a>Copiar entradas de tiempo
Use la vista **Copiar columnas de entrada de tiempo** para definir la lista de campos a copiar durante la entrada de tiempo. **Fecha** y **Duración** son campos obligatorios y no deben eliminarse de la vista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
