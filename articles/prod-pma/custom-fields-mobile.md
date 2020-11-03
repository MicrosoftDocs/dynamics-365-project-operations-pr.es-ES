---
title: Implementar campos personalizados para la aplicación móvil Microsoft Dynamics 365 Project Timesheet en iOS y Android
description: Este tema proporciona patrones comunes para usar extensiones para implementar campos personalizados.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085202"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementar campos personalizados para la aplicación móvil Microsoft Dynamics 365 Project Timesheet en iOS y Android

[!include [banner](../includes/banner.md)]

Este tema proporciona patrones comunes para usar extensiones para implementar campos personalizados. Se cubren los siguientes temas:

- Los diversos tipos de datos que admite el marco de campo personalizado
- Cómo mostrar campos de solo lectura o editables en las entradas de la hoja de horas y guardar los valores proporcionados por el usuario en la base de datos
- Cómo mostrar campos de solo lectura en el encabezado de la hoja de horas
- Cómo integrar otra lógica empresarial personalizada para ingresar valores predeterminados en los campos y realizar una validación adicional

## <a name="audience"></a>Audiencia

Este tema está dirigido a desarrolladores que integran sus campos personalizados en la aplicación móvil Microsoft Dynamics 365 Project Timesheet que está disponible para Apple iOS y Google Android. Se asume que los lectores están familiarizados con el desarrollo de X++ y la funcionalidad de la hoja de horas del proyecto.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contrato de datos: clase TSTimesheetCustomField X++

La clase **TSTimesheetCustomField** es la clase de contrato de datos X++ que representa información sobre un campo personalizado para la funcionalidad de la hoja de horas. Se pasan listas de los objetos de campo personalizados tanto al contrato de datos TSTimesheetDetails como al contrato de datos TSTimesheetEntry para mostrar campos personalizados en la aplicación móvil.

- **TSTimesheetDetails** : el contrato de encabezado de la hoja de horas.
- **TSTimesheetEntry** : el contrato de transacción de la hoja de horas. Los grupos de estos objetos que tienen la misma información de proyecto y el valor **timesheetLineRecId** constituyen una línea.

### <a name="fieldbasetype-types"></a>fieldBaseType (tipos)

La propiedad **FieldBaseType** en el objeto **TsTimesheetCustom** determina el tipo de campo que aparece en la aplicación. Los siguientes valores **Tipos** que son compatibles.

| Valor Tipos | Escribir              | Notas |
|-------------|-------------------|-------|
| 0           | Cadena (y enumeración) | El campo aparece como un campo de texto. |
| 1           | Integer           | El valor se muestra como un número sin decimales. |
| 2           | Real              | El valor se muestra como un número con decimales.<p>Para mostrar el valor real como moneda en la aplicación, use la propiedad **fieldExtenededType**. Puede usar la propiedad **numberOfDecimals** para establecer el número de posiciones decimales que se muestran.</p> |
| 3           | Date              | Los formatos de fecha los determina la configuración **Formato de fecha, hora y número** del usuario que se especifica en **Preferencia de idioma y país o región** en **Opciones de usuario**. |
| 4           | Booleana           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Si la propiedad **stringOptions** no se proporciona en el objeto **TSTimesheetCustomField** , se proporciona al usuario un campo de texto libre.

    La propiedad **stringLength** se puede usar para establecer la longitud máxima de cadena que los usuarios pueden especificar.

- Si la propiedad **stringOptions** se proporciona en el objeto **TSTimesheetCustomField** , esos elementos de la lista son los únicos valores que los usuarios pueden seleccionar mediante los botones de opción (botones de opción).

    En este caso, el campo de cadena puede actuar como un valor de enumeración con el propósito de que el usuario pueda indicar datos. Para guardar el valor en la base de datos como una enumeración, asigne manualmente el valor de la cadena de nuevo al valor de la enumeración antes de guardar en la base de datos mediante la cadena de comando (consulte "Usar cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas la aplicación desde la aplicación de nuevo a la base de datos" más adelante en este tema para ver un ejemplo).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Puede utilizar esta propiedad para dar formato a valores reales como divisa. Este enfoque es aplicable solo cuando el valor **fieldBaseType** es **Real**.

- **TSCustomFieldExtendedType:None** : no se aplica ningún formato.
- **TSCustomFieldExtendedType::Currency** : da formato al valor como divisa.

    Cuando el formato de divisa está activo, el campo **stringValue** se puede usar para pasar el código de moneda que debe mostrarse en la aplicación. El valor es un valor de solo lectura.

    El campo **realValue** contiene el importe de dinero que se debe guardar en la base de datos.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Puede usar esta propiedad para especificar dónde debe aparecer el campo personalizado en la aplicación.

- **TSCustomFieldSection ::Header** : el campo aparecerá en la sección **Ver más detalles** en la aplicación. Estos campos son siempre de solo lectura.
- **TSCustomFieldSection::Line** : el campo aparecerá después de todos los campos de línea predefinidos en las entradas de la hoja de horas. Estos campos pueden ser editables o de solo lectura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Esta propiedad identifica el campo cuando los valores que proporciona la aplicación se guardan de nuevo en la base de datos.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Esta propiedad identifica el campo cuando los valores que proporciona la aplicación se guardan de nuevo en la base de datos.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Establezca esta propiedad en **Sí** para especificar que el campo en la sección de entrada de la hoja de horas debe ser editable por los usuarios. Establezca la propiedad en **No** para que el campo sea de solo lectura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Establezca esta propiedad en **Sí** para especificar que el campo en la sección de entrada de la hoja de horas debe ser obligatorio.

### <a name="label-str"></a>label (str)

Esta propiedad especifica la etiqueta que se muestra junto al campo en la aplicación.

### <a name="stringoptions-list-of-strings"></a>stringOptions (lista de cadenas)

Esta propiedad es aplicable solo cuando **fieldBaseType** se establece en **Cadena**. Si **stringOptions** está configurado, los valores de cadena que están disponibles para su selección mediante botones de opción se especifican mediante las cadenas de la lista. Si no se proporcionan cadenas, se permite la entrada de texto libre en el campo de la cadena (consulte la sección "Usar cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas desde la aplicación en la base de datos" más adelante en este tema para ver un ejemplo).

### <a name="stringlength-int"></a>stringLength (int)

Esta propiedad especifica la longitud máxima para un campo de cadena. Es aplicable solo cuando **fieldBaseType** se establece en **Cadena**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Esta propiedad especifica el número de posiciones decimales que se muestran para un campo real. Es aplicable solo cuando **fieldBaseType** se establece en **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Esta propiedad controla el orden en el que se muestran los campos personalizados en la aplicación cuando se especifica más de un campo personalizado. Los campos que tienen números más bajos se muestran primero.

### <a name="booleanvalue-boolean"></a>booleanValue (booleano)

Para los campos de tipo **Booleano** , esta propiedad pasa el valor booleano del campo entre el servidor y la aplicación.

### <a name="guidvalue-guid"></a>guidValue (guid)

Para los campos de tipo **GUID** , esta propiedad pasa el identificador único global (GUID) entre el servidor y la aplicación.

### <a name="int64value-int64"></a>int64Value (int64)

Para los campos de tipo **Int64** , esta propiedad pasa el valor Int64 del campo entre el servidor y la aplicación.

### <a name="intvalue-int"></a>intValue (int)

Para los campos de tipo **Int** , esta propiedad pasa el valor int del campo entre el servidor y la aplicación.

### <a name="realvalue-real"></a>realValue (real)

Para los campos de tipo **Real** , esta propiedad pasa el valor real del campo entre el servidor y la aplicación.

### <a name="stringvalue-str"></a>stringValue (str)

Para los campos de tipo **Cadena** , esta propiedad pasa el valor de la cadena del campo entre el servidor y la aplicación. También se utiliza para campos del tipo **Real** que tienen el formato de divisa. Para esos campos, la propiedad se usa para pasar el código de divisa a la aplicación.

### <a name="datevalue-date"></a>dateValue (date)

Para los campos de tipo **Fecha** , esta propiedad pasa el valor de la fecha del campo entre el servidor y la aplicación.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostrar y guardar un campo personalizado en la sección de entrada de la hoja de horas

A continuación se muestra una captura de pantalla de la aplicación móvil de la creación de una entrada de hoja de horas. Muestra los campos listos para usar y un campo personalizado en la sección "Entrada de tiempo" denominada "Cadena de prueba" con un valor de enumeración de "Segunda opción" ya establecido.

![Campo personalizado de cadena de prueba en la aplicación](media/timesheet-entry.jpg)



A continuación se muestra una captura de pantalla de la aplicación móvil del usuario que selecciona una de las opciones de enumeración disponibles para el campo personalizado "Cadena de prueba".  Las dos opciones son "Primera opción" y "Segunda opción" que se muestran como botones de opción. La segunda opción está actualmente seleccionada.

![Botones de opción para el campo personalizado Cadena de prueba](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Extienda la tabla TSTimesheetLine para que tenga un campo personalizado

En escenarios típicos, es probable que los datos de un campo personalizado en la sección de entrada de la hoja de horas se guarden en la tabla TSTimesheetLine. Sin embargo, se pueden usar otras tablas si los datos se pueden recuperar basándose en un registro TSTimesheetTrans que se proporciona, o si no tiene un contexto de registro específico (por ejemplo, si el campo está configurado como de solo lectura en los parámetros del proyecto).

Tenga en cuenta que los campos personalizados no tienen que tener ningún registro de base de datos de respaldo. Se pueden generar dinámicamente basándose en la lógica X++. Este enfoque puede ser útil en escenarios de solo lectura (consulte la sección "Usar cadena de comando en la clase TSTimesheetDetails, método buildCustomFieldListForHeader para completar los detalles de la hoja de horas" para ver un ejemplo de valores de campo personalizados generados dinámicamente).

A continuación se muestra una captura de pantalla de Visual Studio del árbol de objetos de la aplicación. Muestra una extensión de la tabla TSTimesheetLine con el campo TestLineString agregado como un campo personalizado.

![Cadena de líneas](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Usar la cadena de comando en el método buildCustomFieldList de la clase TSTimesheetSettings para mostrar un campo en la sección de entrada de la hoja de horas

Este código controla la configuración de visualización para el campo en la aplicación. Por ejemplo, controla el tipo de campo, la etiqueta, si el campo es obligatorio y en qué sección aparece el campo.

El siguiente ejemplo muestra un campo de cadena en entradas de tiempo. Este campo tiene dos opciones, **Primera opción** y **Segunda opción** , que están disponibles mediante botones de opción. El campo de la aplicación está asociado con el campo **TestLineString** que se agrega a la tabla TSTimesheetLine.

Tenga en cuenta el uso del método **TSTimesheetCustomField::newFromMetatdata()** para simplificar la inicialización de las propiedades del campo personalizado: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** y **numberOfDecimals**. También puede configurar estos parámetros manualmente, como prefiera.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Usar la cadena de comando en el método buildCustomFieldListForEntry de la clase TSTimesheetEntry para especificar valores en una entrada de hoja de horas.

El método **buildCustomFieldListForEntry** se utiliza para especificar valores en las líneas de la hoja de horas guardada en la aplicación móvil. Toma un registro TSTimesheetTrans como parámetro. Los campos de ese registro se pueden usar para completar el valor del campo personalizado en la aplicación.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Use la cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas de la aplicación en la base de datos

Para guardar un campo personalizado en la base de datos con un uso típico, debe ampliar varios métodos:

- El método **parte de horasLineNeedsUpdating** se utiliza para determinar si el usuario ha cambiado el registro de líneas en la aplicación y debe guardarse en la base de datos. Si el rendimiento no es un problema, este método se puede simplificar para que siempre devuelva **True**.
- Los métodos **populateTimesheetLineFromEntryDuringCreate** y **populateTimesheetLineFromEntryDuringUpdate** se pueden ampliar para que especifiquen valores en el registro de base de datos TSTimesheetLine del registro de contrato de datos TSTimesheetEntry que se proporciona. En el ejemplo que sigue, observe cómo la asignación entre el campo de la base de datos y el campo de entrada se realiza manualmente a través del código X++.
- El método **populateTimesheetWeekFromEntry** se puede extender si el campo personalizado que se asigna al objeto **TSTimesheetEntry** se debe volver a escribir en la tabla de base de datos TSTimesheetLineweek.

> [!NOTE]
> El siguiente ejemplo guarda el valor **firstOption** o **secondOption** que el usuario selecciona en la base de datos como valor de cadena sin formato. Si el campo de la base de datos es un campo del tipo **Enum** , esos valores se pueden asignar manualmente a un valor de enumeración y luego se pueden guardar en un campo de enumeración en la tabla de la base de datos.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostrar un campo personalizado en la sección del encabezado

A continuación se muestra una captura de pantalla de la aplicación móvil de un usuario que ve una hoja de horas. Se ha seleccionado el botón "Más información" en la esquina superior derecha para mostrar la opción "Ver más detalles".  

![Comando Ver más detalles](media/show-more.png)

A continuación se muestra una captura de pantalla de la aplicación móvil que muestra la sección "Más" de una hoja de horas. Se ha agregado un campo personalizado llamado "Índice de uso de esta hoja de horas (campo personalizado calculado)" a la sección de encabezado de la hoja de horas. Se establece un valor de solo lectura de "0,667" en el campo personalizado.

![Sección Más](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Extienda la tabla TSTimesheetTable para que tenga un campo personalizado

En escenarios típicos, es probable que los datos de un campo personalizado en la sección del encabezado se extraigan de la tabla TSTimesheetHeader. Sin embargo, se pueden usar otras tablas si los datos se pueden recuperar basándose en un registro TSTimesheetTable que se proporciona, o si no tiene un contexto de registro específico (por ejemplo, si el campo está configurado como de solo lectura en los parámetros del proyecto).

Tenga en cuenta que los campos personalizados no tienen que tener ningún registro de base de datos de respaldo. Se pueden generar dinámicamente basándose en la lógica X++. El ejemplo que sigue muestra este enfoque.

Los campos de la sección del encabezado siempre son de solo lectura en la aplicación.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Usar la cadena de comando en el método buildCustomFieldList de la clase TSTimesheetSettings para mostrar un campo en la sección del encabezado

Este código controla la configuración de visualización para el campo en la aplicación. Por ejemplo, controla el tipo de campo, la etiqueta, si el campo es obligatorio y en qué sección aparece el campo.

El siguiente ejemplo muestra un valor calculado en la sección de encabezado de la aplicación.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Usar la cadena de comando en el método buildCustomFieldListForHeader de la clase TSTimesheetDetails para completar los detalles en la hoja de horas

El método **buildCustomFieldListForHeader** se utiliza para completar los detalles en el encabezado de la hoja de horas en la aplicación móvil. Toma un registro TSTimesheetTable como parámetro. Los campos de ese registro se pueden usar para completar el valor del campo personalizado en la aplicación. El siguiente ejemplo no lee ningún valor de la base de datos. En su lugar, utiliza la lógica X++ para generar un valor calculado que luego se muestra en la aplicación.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Otras oportunidades de capacidad de configuración y extensión

### <a name="adding-additional-validation-for-the-app"></a>Agregar validación adicional para la aplicación

La lógica existente para la funcionalidad de la hoja de horas en la base de datos seguirá funcionando como se esperaba. Para interrumpir la finalización de las operaciones de guardar o enviar y mostrar un mensaje de error específico, puede agregar **generar error ("mensaje al usuario")** al código a través de una extensión de cadena de mando. Aquí hay tres ejemplos de métodos extensibles útiles:

- Si **validateWrite** en la tabla TSTimesheetLine devuelve **False** durante una operación de guardado para una línea de la hoja de horas, se muestra un mensaje de error en la aplicación móvil.
- Si **validateSubmit** en la tabla TSTimesheetTable devuelve **False** durante un envío de la hoja de horas en la aplicación, se muestra un mensaje de error al usuario.
- La lógica que rellena campos (por ejemplo, **Propiedad de línea** ) durante el método **insert** en la tabla TSTimesheetLine aún se ejecutará.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ocultar y marcar campos listos para usar como de solo lectura a través de la configuración

Desde los parámetros del proyecto, puede hacer que los campos predefinidos sean de solo lectura u que estén ocultos en la aplicación móvil. Configure las opciones en la sección **Hojas de horas móviles** en la pestaña **Hoja de horas** de la página **Parámetros de gestión de proyectos y contabilidad**.

![Parámetros de proyecto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Cambiar las actividades que están disponibles para su selección mediante extensiones

Las actividades que están disponibles para la selección de un proyecto se completan a través de los métodos **getActivitiesForProject()** y **getActivityQuery()** en la clase **TsTimesheetProjectService**. Puede utilizar la cadena de comando para cambiar este comportamiento para que coincida con su escenario empresarial para las actividades que están disponibles para la selección de un proyecto específico.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Especificar una categoría de proyecto predeterminada en las entradas de la hoja de horas

La entrada de una categoría de proyecto predeterminada en las entradas de la hoja de horas se produce en tres niveles. Puede utilizar la cadena de mando para extender el comportamiento en cualquiera o en todos estos niveles para lograr el comportamiento deseado. Se utiliza la siguiente jerarquía:

1. La aplicación intenta poner la categoría predeterminada desde recurso del proyecto. Esta categoría predeterminada se establece en los métodos **getCurrentUserResource** y **getDelegatedResourcesForCurrentUser** en la clase **TSTimesheetSettingsService**.
2. Si la categoría predeterminada no se proporciona en el nivel de recursos del proyecto, la aplicación intenta extraerla de la actividad del proyecto. Esta categoría predeterminada se establece en el método **getActivitiesForProject** en la clase **TSTimesheetProjectService**.
3. Si la categoría predeterminada no se proporciona en el nivel de actividad del proyecto, la categoría predeterminada se toma de los parámetros del proyecto. Esta categoría predeterminada se establece en el método **getProjectDetailsbyRule** en la clase **TSTimesheetProjectService**.
