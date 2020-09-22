---
title: Implementar campos personalizados para la aplicación móvil Microsoft Dynamics 365 Project Timesheet en iOS y Android
description: Este tema proporciona patrones comunes para usar extensiones para implementar campos personalizados.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755966"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="54a41-103">Implementar campos personalizados para la aplicación móvil Microsoft Dynamics 365 Project Timesheet en iOS y Android</span><span class="sxs-lookup"><span data-stu-id="54a41-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54a41-104">Este tema proporciona patrones comunes para usar extensiones para implementar campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="54a41-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="54a41-105">Se cubren los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="54a41-105">The following topics are covered:</span></span>

- <span data-ttu-id="54a41-106">Los diversos tipos de datos que admite el marco de campo personalizado</span><span class="sxs-lookup"><span data-stu-id="54a41-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="54a41-107">Cómo mostrar campos de solo lectura o editables en las entradas de la hoja de horas y guardar los valores proporcionados por el usuario en la base de datos</span><span class="sxs-lookup"><span data-stu-id="54a41-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="54a41-108">Cómo mostrar campos de solo lectura en el encabezado de la hoja de horas</span><span class="sxs-lookup"><span data-stu-id="54a41-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="54a41-109">Cómo integrar otra lógica empresarial personalizada para ingresar valores predeterminados en los campos y realizar una validación adicional</span><span class="sxs-lookup"><span data-stu-id="54a41-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="54a41-110">Audiencia</span><span class="sxs-lookup"><span data-stu-id="54a41-110">Audience</span></span>

<span data-ttu-id="54a41-111">Este tema está dirigido a desarrolladores que integran sus campos personalizados en la aplicación móvil Microsoft Dynamics 365 Project Timesheet que está disponible para Apple iOS y Google Android.</span><span class="sxs-lookup"><span data-stu-id="54a41-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="54a41-112">Se asume que los lectores están familiarizados con el desarrollo de X++ y la funcionalidad de la hoja de horas del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54a41-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="54a41-113">Contrato de datos: clase TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="54a41-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="54a41-114">La clase **TSTimesheetCustomField** es la clase de contrato de datos X++ que representa información sobre un campo personalizado para la funcionalidad de la hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="54a41-115">Se pasan listas de los objetos de campo personalizados tanto al contrato de datos TSTimesheetDetails como al contrato de datos TSTimesheetEntry para mostrar campos personalizados en la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="54a41-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="54a41-116">**TSTimesheetDetails**: el contrato de encabezado de la hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="54a41-117">**TSTimesheetEntry**: el contrato de transacción de la hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="54a41-118">Los grupos de estos objetos que tienen la misma información de proyecto y el valor **timesheetLineRecId** constituyen una línea.</span><span class="sxs-lookup"><span data-stu-id="54a41-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="54a41-119">fieldBaseType (tipos)</span><span class="sxs-lookup"><span data-stu-id="54a41-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="54a41-120">La propiedad **FieldBaseType** en el objeto **TsTimesheetCustom** determina el tipo de campo que aparece en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="54a41-121">Los siguientes valores **Tipos** que son compatibles.</span><span class="sxs-lookup"><span data-stu-id="54a41-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="54a41-122">Valor Tipos</span><span class="sxs-lookup"><span data-stu-id="54a41-122">Types value</span></span> | <span data-ttu-id="54a41-123">Escribir</span><span class="sxs-lookup"><span data-stu-id="54a41-123">Type</span></span>              | <span data-ttu-id="54a41-124">Notas</span><span class="sxs-lookup"><span data-stu-id="54a41-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="54a41-125">0</span><span class="sxs-lookup"><span data-stu-id="54a41-125">0</span></span>           | <span data-ttu-id="54a41-126">Cadena (y enumeración)</span><span class="sxs-lookup"><span data-stu-id="54a41-126">String (and Enum)</span></span> | <span data-ttu-id="54a41-127">El campo aparece como un campo de texto.</span><span class="sxs-lookup"><span data-stu-id="54a41-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="54a41-128">1</span><span class="sxs-lookup"><span data-stu-id="54a41-128">1</span></span>           | <span data-ttu-id="54a41-129">Integer</span><span class="sxs-lookup"><span data-stu-id="54a41-129">Integer</span></span>           | <span data-ttu-id="54a41-130">El valor se muestra como un número sin decimales.</span><span class="sxs-lookup"><span data-stu-id="54a41-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="54a41-131">2</span><span class="sxs-lookup"><span data-stu-id="54a41-131">2</span></span>           | <span data-ttu-id="54a41-132">Real</span><span class="sxs-lookup"><span data-stu-id="54a41-132">Real</span></span>              | <span data-ttu-id="54a41-133">El valor se muestra como un número con decimales.</span><span class="sxs-lookup"><span data-stu-id="54a41-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="54a41-134">Para mostrar el valor real como moneda en la aplicación, use la propiedad **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="54a41-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="54a41-135">Puede usar la propiedad **numberOfDecimals** para establecer el número de posiciones decimales que se muestran.</span><span class="sxs-lookup"><span data-stu-id="54a41-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="54a41-136">3</span><span class="sxs-lookup"><span data-stu-id="54a41-136">3</span></span>           | <span data-ttu-id="54a41-137">Date</span><span class="sxs-lookup"><span data-stu-id="54a41-137">Date</span></span>              | <span data-ttu-id="54a41-138">Los formatos de fecha los determina la configuración **Formato de fecha, hora y número** del usuario que se especifica en **Preferencia de idioma y país o región** en **Opciones de usuario**.</span><span class="sxs-lookup"><span data-stu-id="54a41-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="54a41-139">4</span><span class="sxs-lookup"><span data-stu-id="54a41-139">4</span></span>           | <span data-ttu-id="54a41-140">Booleana</span><span class="sxs-lookup"><span data-stu-id="54a41-140">Boolean</span></span>           | |
| <span data-ttu-id="54a41-141">15</span><span class="sxs-lookup"><span data-stu-id="54a41-141">15</span></span>          | <span data-ttu-id="54a41-142">GUID</span><span class="sxs-lookup"><span data-stu-id="54a41-142">GUID</span></span>              | |
| <span data-ttu-id="54a41-143">16</span><span class="sxs-lookup"><span data-stu-id="54a41-143">16</span></span>          | <span data-ttu-id="54a41-144">Int64</span><span class="sxs-lookup"><span data-stu-id="54a41-144">Int64</span></span>             | |

- <span data-ttu-id="54a41-145">Si la propiedad **stringOptions** no se proporciona en el objeto **TSTimesheetCustomField**, se proporciona al usuario un campo de texto libre.</span><span class="sxs-lookup"><span data-stu-id="54a41-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="54a41-146">La propiedad **stringLength** se puede usar para establecer la longitud máxima de cadena que los usuarios pueden especificar.</span><span class="sxs-lookup"><span data-stu-id="54a41-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="54a41-147">Si la propiedad **stringOptions** se proporciona en el objeto **TSTimesheetCustomField**, esos elementos de la lista son los únicos valores que los usuarios pueden seleccionar mediante los botones de opción (botones de opción).</span><span class="sxs-lookup"><span data-stu-id="54a41-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="54a41-148">En este caso, el campo de cadena puede actuar como un valor de enumeración con el propósito de que el usuario pueda indicar datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="54a41-149">Para guardar el valor en la base de datos como una enumeración, asigne manualmente el valor de la cadena de nuevo al valor de la enumeración antes de guardar en la base de datos mediante la cadena de comando (consulte "Usar cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas la aplicación desde la aplicación de nuevo a la base de datos" más adelante en este tema para ver un ejemplo).</span><span class="sxs-lookup"><span data-stu-id="54a41-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="54a41-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="54a41-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="54a41-151">Puede utilizar esta propiedad para dar formato a valores reales como divisa.</span><span class="sxs-lookup"><span data-stu-id="54a41-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="54a41-152">Este enfoque es aplicable solo cuando el valor **fieldBaseType** es **Real**.</span><span class="sxs-lookup"><span data-stu-id="54a41-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="54a41-153">**TSCustomFieldExtendedType:None**: no se aplica ningún formato.</span><span class="sxs-lookup"><span data-stu-id="54a41-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="54a41-154">**TSCustomFieldExtendedType::Currency**: da formato al valor como divisa.</span><span class="sxs-lookup"><span data-stu-id="54a41-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="54a41-155">Cuando el formato de divisa está activo, el campo **stringValue** se puede usar para pasar el código de moneda que debe mostrarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="54a41-156">El valor es un valor de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a41-156">The value is a read-only value.</span></span>

    <span data-ttu-id="54a41-157">El campo **realValue** contiene el importe de dinero que se debe guardar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="54a41-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="54a41-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="54a41-159">Puede usar esta propiedad para especificar dónde debe aparecer el campo personalizado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="54a41-160">**TSCustomFieldSection ::Header**: el campo aparecerá en la sección **Ver más detalles** en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="54a41-161">Estos campos son siempre de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a41-161">These fields are always read-only.</span></span>
- <span data-ttu-id="54a41-162">**TSCustomFieldSection::Line**: el campo aparecerá después de todos los campos de línea predefinidos en las entradas de la hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="54a41-163">Estos campos pueden ser editables o de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a41-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="54a41-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="54a41-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="54a41-165">Esta propiedad identifica el campo cuando los valores que proporciona la aplicación se guardan de nuevo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="54a41-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="54a41-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="54a41-167">Esta propiedad identifica el campo cuando los valores que proporciona la aplicación se guardan de nuevo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="54a41-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="54a41-168">isEditable (NoYes)</span></span>

<span data-ttu-id="54a41-169">Establezca esta propiedad en **Sí** para especificar que el campo en la sección de entrada de la hoja de horas debe ser editable por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="54a41-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="54a41-170">Establezca la propiedad en **No** para que el campo sea de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54a41-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="54a41-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="54a41-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="54a41-172">Establezca esta propiedad en **Sí** para especificar que el campo en la sección de entrada de la hoja de horas debe ser obligatorio.</span><span class="sxs-lookup"><span data-stu-id="54a41-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="54a41-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="54a41-173">label (str)</span></span>

<span data-ttu-id="54a41-174">Esta propiedad especifica la etiqueta que se muestra junto al campo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="54a41-175">stringOptions (lista de cadenas)</span><span class="sxs-lookup"><span data-stu-id="54a41-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="54a41-176">Esta propiedad es aplicable solo cuando **fieldBaseType** se establece en **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="54a41-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="54a41-177">Si **stringOptions** está configurado, los valores de cadena que están disponibles para su selección mediante botones de opción se especifican mediante las cadenas de la lista.</span><span class="sxs-lookup"><span data-stu-id="54a41-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="54a41-178">Si no se proporcionan cadenas, se permite la entrada de texto libre en el campo de la cadena (consulte la sección "Usar cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas desde la aplicación en la base de datos" más adelante en este tema para ver un ejemplo).</span><span class="sxs-lookup"><span data-stu-id="54a41-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="54a41-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="54a41-179">stringLength (int)</span></span>

<span data-ttu-id="54a41-180">Esta propiedad especifica la longitud máxima para un campo de cadena.</span><span class="sxs-lookup"><span data-stu-id="54a41-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="54a41-181">Es aplicable solo cuando **fieldBaseType** se establece en **Cadena**.</span><span class="sxs-lookup"><span data-stu-id="54a41-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="54a41-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="54a41-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="54a41-183">Esta propiedad especifica el número de posiciones decimales que se muestran para un campo real.</span><span class="sxs-lookup"><span data-stu-id="54a41-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="54a41-184">Es aplicable solo cuando **fieldBaseType** se establece en **Real**.</span><span class="sxs-lookup"><span data-stu-id="54a41-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="54a41-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="54a41-185">orderSequence (int)</span></span>

<span data-ttu-id="54a41-186">Esta propiedad controla el orden en el que se muestran los campos personalizados en la aplicación cuando se especifica más de un campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="54a41-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="54a41-187">Los campos que tienen números más bajos se muestran primero.</span><span class="sxs-lookup"><span data-stu-id="54a41-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="54a41-188">booleanValue (booleano)</span><span class="sxs-lookup"><span data-stu-id="54a41-188">booleanValue (boolean)</span></span>

<span data-ttu-id="54a41-189">Para los campos de tipo **Booleano**, esta propiedad pasa el valor booleano del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="54a41-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="54a41-190">guidValue (guid)</span></span>

<span data-ttu-id="54a41-191">Para los campos de tipo **GUID**, esta propiedad pasa el identificador único global (GUID) entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="54a41-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="54a41-192">int64Value (int64)</span></span>

<span data-ttu-id="54a41-193">Para los campos de tipo **Int64**, esta propiedad pasa el valor Int64 del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="54a41-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="54a41-194">intValue (int)</span></span>

<span data-ttu-id="54a41-195">Para los campos de tipo **Int**, esta propiedad pasa el valor int del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="54a41-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="54a41-196">realValue (real)</span></span>

<span data-ttu-id="54a41-197">Para los campos de tipo **Real**, esta propiedad pasa el valor real del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="54a41-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="54a41-198">stringValue (str)</span></span>

<span data-ttu-id="54a41-199">Para los campos de tipo **Cadena**, esta propiedad pasa el valor de la cadena del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="54a41-200">También se utiliza para campos del tipo **Real** que tienen el formato de divisa.</span><span class="sxs-lookup"><span data-stu-id="54a41-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="54a41-201">Para esos campos, la propiedad se usa para pasar el código de divisa a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="54a41-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="54a41-202">dateValue (date)</span></span>

<span data-ttu-id="54a41-203">Para los campos de tipo **Fecha**, esta propiedad pasa el valor de la fecha del campo entre el servidor y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="54a41-204">Mostrar y guardar un campo personalizado en la sección de entrada de la hoja de horas</span><span class="sxs-lookup"><span data-stu-id="54a41-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="54a41-205">A continuación se muestra una captura de pantalla de la aplicación móvil de la creación de una entrada de hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="54a41-206">Muestra los campos listos para usar y un campo personalizado en la sección "Entrada de tiempo" denominada "Cadena de prueba" con un valor de enumeración de "Segunda opción" ya establecido.</span><span class="sxs-lookup"><span data-stu-id="54a41-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Campo personalizado de cadena de prueba en la aplicación](media/timesheet-entry.jpg)



<span data-ttu-id="54a41-208">A continuación se muestra una captura de pantalla de la aplicación móvil del usuario que selecciona una de las opciones de enumeración disponibles para el campo personalizado "Cadena de prueba".</span><span class="sxs-lookup"><span data-stu-id="54a41-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="54a41-209">Las dos opciones son "Primera opción" y "Segunda opción" que se muestran como botones de opción.</span><span class="sxs-lookup"><span data-stu-id="54a41-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="54a41-210">La segunda opción está actualmente seleccionada.</span><span class="sxs-lookup"><span data-stu-id="54a41-210">The second option is currently selected.</span></span>

![Botones de opción para el campo personalizado Cadena de prueba](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="54a41-212">Extienda la tabla TSTimesheetLine para que tenga un campo personalizado</span><span class="sxs-lookup"><span data-stu-id="54a41-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="54a41-213">En escenarios típicos, es probable que los datos de un campo personalizado en la sección de entrada de la hoja de horas se guarden en la tabla TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="54a41-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="54a41-214">Sin embargo, se pueden usar otras tablas si los datos se pueden recuperar basándose en un registro TSTimesheetTrans que se proporciona, o si no tiene un contexto de registro específico (por ejemplo, si el campo está configurado como de solo lectura en los parámetros del proyecto).</span><span class="sxs-lookup"><span data-stu-id="54a41-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="54a41-215">Tenga en cuenta que los campos personalizados no tienen que tener ningún registro de base de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="54a41-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="54a41-216">Se pueden generar dinámicamente basándose en la lógica X++.</span><span class="sxs-lookup"><span data-stu-id="54a41-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="54a41-217">Este enfoque puede ser útil en escenarios de solo lectura (consulte la sección "Usar cadena de comando en la clase TSTimesheetDetails, método buildCustomFieldListForHeader para completar los detalles de la hoja de horas" para ver un ejemplo de valores de campo personalizados generados dinámicamente).</span><span class="sxs-lookup"><span data-stu-id="54a41-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="54a41-218">A continuación se muestra una captura de pantalla de Visual Studio del árbol de objetos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="54a41-219">Muestra una extensión de la tabla TSTimesheetLine con el campo TestLineString agregado como un campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="54a41-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Cadena de líneas](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="54a41-221">Usar la cadena de comando en el método buildCustomFieldList de la clase TSTimesheetSettings para mostrar un campo en la sección de entrada de la hoja de horas</span><span class="sxs-lookup"><span data-stu-id="54a41-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="54a41-222">Este código controla la configuración de visualización para el campo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="54a41-223">Por ejemplo, controla el tipo de campo, la etiqueta, si el campo es obligatorio y en qué sección aparece el campo.</span><span class="sxs-lookup"><span data-stu-id="54a41-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="54a41-224">El siguiente ejemplo muestra un campo de cadena en entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="54a41-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="54a41-225">Este campo tiene dos opciones, **Primera opción** y **Segunda opción**, que están disponibles mediante botones de opción.</span><span class="sxs-lookup"><span data-stu-id="54a41-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="54a41-226">El campo de la aplicación está asociado con el campo **TestLineString** que se agrega a la tabla TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="54a41-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="54a41-227">Tenga en cuenta el uso del método **TSTimesheetCustomField::newFromMetatdata()** para simplificar la inicialización de las propiedades del campo personalizado: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** y **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="54a41-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="54a41-228">También puede configurar estos parámetros manualmente, como prefiera.</span><span class="sxs-lookup"><span data-stu-id="54a41-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="54a41-229">Usar la cadena de comando en el método buildCustomFieldListForEntry de la clase TSTimesheetEntry para especificar valores en una entrada de hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="54a41-230">El método **buildCustomFieldListForEntry** se utiliza para especificar valores en las líneas de la hoja de horas guardada en la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="54a41-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="54a41-231">Toma un registro TSTimesheetTrans como parámetro.</span><span class="sxs-lookup"><span data-stu-id="54a41-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="54a41-232">Los campos de ese registro se pueden usar para completar el valor del campo personalizado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="54a41-233">Use la cadena de comando en la clase TSTimesheetEntryService para guardar una entrada de la hoja de horas de la aplicación en la base de datos</span><span class="sxs-lookup"><span data-stu-id="54a41-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="54a41-234">Para guardar un campo personalizado en la base de datos con un uso típico, debe ampliar varios métodos:</span><span class="sxs-lookup"><span data-stu-id="54a41-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="54a41-235">El método **parte de horasLineNeedsUpdating** se utiliza para determinar si el usuario ha cambiado el registro de líneas en la aplicación y debe guardarse en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="54a41-236">Si el rendimiento no es un problema, este método se puede simplificar para que siempre devuelva **True**.</span><span class="sxs-lookup"><span data-stu-id="54a41-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="54a41-237">Los métodos **populateTimesheetLineFromEntryDuringCreate** y **populateTimesheetLineFromEntryDuringUpdate** se pueden ampliar para que especifiquen valores en el registro de base de datos TSTimesheetLine del registro de contrato de datos TSTimesheetEntry que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="54a41-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="54a41-238">En el ejemplo que sigue, observe cómo la asignación entre el campo de la base de datos y el campo de entrada se realiza manualmente a través del código X++.</span><span class="sxs-lookup"><span data-stu-id="54a41-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="54a41-239">El método **populateTimesheetWeekFromEntry** se puede extender si el campo personalizado que se asigna al objeto **TSTimesheetEntry** se debe volver a escribir en la tabla de base de datos TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="54a41-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="54a41-240">El siguiente ejemplo guarda el valor **firstOption** o **secondOption** que el usuario selecciona en la base de datos como valor de cadena sin formato.</span><span class="sxs-lookup"><span data-stu-id="54a41-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="54a41-241">Si el campo de la base de datos es un campo del tipo **Enum**, esos valores se pueden asignar manualmente a un valor de enumeración y luego se pueden guardar en un campo de enumeración en la tabla de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="54a41-242">Mostrar un campo personalizado en la sección del encabezado</span><span class="sxs-lookup"><span data-stu-id="54a41-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="54a41-243">A continuación se muestra una captura de pantalla de la aplicación móvil de un usuario que ve una hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="54a41-244">Se ha seleccionado el botón "Más información" en la esquina superior derecha para mostrar la opción "Ver más detalles".</span><span class="sxs-lookup"><span data-stu-id="54a41-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Comando Ver más detalles](media/show-more.png)

<span data-ttu-id="54a41-246">A continuación se muestra una captura de pantalla de la aplicación móvil que muestra la sección "Más" de una hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="54a41-247">Se ha agregado un campo personalizado llamado "Índice de uso de esta hoja de horas (campo personalizado calculado)" a la sección de encabezado de la hoja de horas.</span><span class="sxs-lookup"><span data-stu-id="54a41-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="54a41-248">Se establece un valor de solo lectura de "0,667" en el campo personalizado.</span><span class="sxs-lookup"><span data-stu-id="54a41-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Sección Más](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="54a41-250">Extienda la tabla TSTimesheetTable para que tenga un campo personalizado</span><span class="sxs-lookup"><span data-stu-id="54a41-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="54a41-251">En escenarios típicos, es probable que los datos de un campo personalizado en la sección del encabezado se extraigan de la tabla TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="54a41-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="54a41-252">Sin embargo, se pueden usar otras tablas si los datos se pueden recuperar basándose en un registro TSTimesheetTable que se proporciona, o si no tiene un contexto de registro específico (por ejemplo, si el campo está configurado como de solo lectura en los parámetros del proyecto).</span><span class="sxs-lookup"><span data-stu-id="54a41-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="54a41-253">Tenga en cuenta que los campos personalizados no tienen que tener ningún registro de base de datos de respaldo.</span><span class="sxs-lookup"><span data-stu-id="54a41-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="54a41-254">Se pueden generar dinámicamente basándose en la lógica X++.</span><span class="sxs-lookup"><span data-stu-id="54a41-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="54a41-255">El ejemplo que sigue muestra este enfoque.</span><span class="sxs-lookup"><span data-stu-id="54a41-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="54a41-256">Los campos de la sección del encabezado siempre son de solo lectura en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="54a41-257">Usar la cadena de comando en el método buildCustomFieldList de la clase TSTimesheetSettings para mostrar un campo en la sección del encabezado</span><span class="sxs-lookup"><span data-stu-id="54a41-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="54a41-258">Este código controla la configuración de visualización para el campo en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="54a41-259">Por ejemplo, controla el tipo de campo, la etiqueta, si el campo es obligatorio y en qué sección aparece el campo.</span><span class="sxs-lookup"><span data-stu-id="54a41-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="54a41-260">El siguiente ejemplo muestra un valor calculado en la sección de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="54a41-261">Usar la cadena de comando en el método buildCustomFieldListForHeader de la clase TSTimesheetDetails para completar los detalles en la hoja de horas</span><span class="sxs-lookup"><span data-stu-id="54a41-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="54a41-262">El método **buildCustomFieldListForHeader** se utiliza para completar los detalles en el encabezado de la hoja de horas en la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="54a41-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="54a41-263">Toma un registro TSTimesheetTable como parámetro.</span><span class="sxs-lookup"><span data-stu-id="54a41-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="54a41-264">Los campos de ese registro se pueden usar para completar el valor del campo personalizado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="54a41-265">El siguiente ejemplo no lee ningún valor de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="54a41-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="54a41-266">En su lugar, utiliza la lógica X++ para generar un valor calculado que luego se muestra en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54a41-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="54a41-267">Otras oportunidades de capacidad de configuración y extensión</span><span class="sxs-lookup"><span data-stu-id="54a41-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="54a41-268">Agregar validación adicional para la aplicación</span><span class="sxs-lookup"><span data-stu-id="54a41-268">Adding additional validation for the app</span></span>

<span data-ttu-id="54a41-269">La lógica existente para la funcionalidad de la hoja de horas en la base de datos seguirá funcionando como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="54a41-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="54a41-270">Para interrumpir la finalización de las operaciones de guardar o enviar y mostrar un mensaje de error específico, puede agregar **generar error ("mensaje al usuario")** al código a través de una extensión de cadena de mando.</span><span class="sxs-lookup"><span data-stu-id="54a41-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="54a41-271">Aquí hay tres ejemplos de métodos extensibles útiles:</span><span class="sxs-lookup"><span data-stu-id="54a41-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="54a41-272">Si **validateWrite** en la tabla TSTimesheetLine devuelve **False** durante una operación de guardado para una línea de la hoja de horas, se muestra un mensaje de error en la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="54a41-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="54a41-273">Si **validateSubmit** en la tabla TSTimesheetTable devuelve **False** durante un envío de la hoja de horas en la aplicación, se muestra un mensaje de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="54a41-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="54a41-274">La lógica que rellena campos (por ejemplo, **Propiedad de línea**) durante el método **insert** en la tabla TSTimesheetLine aún se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="54a41-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="54a41-275">Ocultar y marcar campos listos para usar como de solo lectura a través de la configuración</span><span class="sxs-lookup"><span data-stu-id="54a41-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="54a41-276">Desde los parámetros del proyecto, puede hacer que los campos predefinidos sean de solo lectura u que estén ocultos en la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="54a41-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="54a41-277">Configure las opciones en la sección **Hojas de horas móviles** en la pestaña **Hoja de horas** de la página **Parámetros de gestión de proyectos y contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="54a41-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Parámetros de proyecto](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="54a41-279">Cambiar las actividades que están disponibles para su selección mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="54a41-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="54a41-280">Las actividades que están disponibles para la selección de un proyecto se completan a través de los métodos **getActivitiesForProject()** y **getActivityQuery()** en la clase **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="54a41-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="54a41-281">Puede utilizar la cadena de comando para cambiar este comportamiento para que coincida con su escenario empresarial para las actividades que están disponibles para la selección de un proyecto específico.</span><span class="sxs-lookup"><span data-stu-id="54a41-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="54a41-282">Especificar una categoría de proyecto predeterminada en las entradas de la hoja de horas</span><span class="sxs-lookup"><span data-stu-id="54a41-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="54a41-283">La entrada de una categoría de proyecto predeterminada en las entradas de la hoja de horas se produce en tres niveles.</span><span class="sxs-lookup"><span data-stu-id="54a41-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="54a41-284">Puede utilizar la cadena de mando para extender el comportamiento en cualquiera o en todos estos niveles para lograr el comportamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="54a41-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="54a41-285">Se utiliza la siguiente jerarquía:</span><span class="sxs-lookup"><span data-stu-id="54a41-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="54a41-286">La aplicación intenta poner la categoría predeterminada desde recurso del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54a41-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="54a41-287">Esta categoría predeterminada se establece en los métodos **getCurrentUserResource** y **getDelegatedResourcesForCurrentUser** en la clase **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="54a41-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="54a41-288">Si la categoría predeterminada no se proporciona en el nivel de recursos del proyecto, la aplicación intenta extraerla de la actividad del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54a41-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="54a41-289">Esta categoría predeterminada se establece en el método **getActivitiesForProject** en la clase **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="54a41-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="54a41-290">Si la categoría predeterminada no se proporciona en el nivel de actividad del proyecto, la categoría predeterminada se toma de los parámetros del proyecto.</span><span class="sxs-lookup"><span data-stu-id="54a41-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="54a41-291">Esta categoría predeterminada se establece en el método **getProjectDetailsbyRule** en la clase **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="54a41-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
