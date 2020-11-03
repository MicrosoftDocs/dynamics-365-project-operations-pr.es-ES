---
title: Correcciones masivas de datos reales creados por entradas de gastos y tiempo aprobadas
description: En este tema se explica de qué manera un administrador puede hacer correcciones únicas o masivas a entradas de tiempo o gastos previamente aprobadas si la facturación no está completa.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085324"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="f63a0-103">Correcciones masivas de datos reales creados por entradas de gastos y tiempo aprobadas</span><span class="sxs-lookup"><span data-stu-id="f63a0-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="f63a0-104">Ocasionalmente, se puede introducir incorrectamente una entrada de tiempo o gasto.</span><span class="sxs-lookup"><span data-stu-id="f63a0-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="f63a0-105">Por ejemplo, un consultor puede seleccionar la fecha incorrecta al crear una entrada de tiempo o puede transponer los números al introducir un gasto.</span><span class="sxs-lookup"><span data-stu-id="f63a0-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="f63a0-106">Si un consultor no puede realizar las actualizaciones de las entradas enviadas, un administrador puede corregir directamente la entrada de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="f63a0-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="f63a0-107">Para completar los procedimientos en este tema, necesitará permisos de Administrador.</span><span class="sxs-lookup"><span data-stu-id="f63a0-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="f63a0-108">Corregir entradas de tiempo aprobadas</span><span class="sxs-lookup"><span data-stu-id="f63a0-108">Correct approved time entries</span></span>     

<span data-ttu-id="f63a0-109">Complete los siguientes pasos para corregir entradas de tiempo únicas o múltiples para un proyecto.</span><span class="sxs-lookup"><span data-stu-id="f63a0-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="f63a0-110">En el área **Ventas** , seleccione **Transacciones** y luego seleccione **Tiempo aprobado**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="f63a0-111">En la lista **Tiempo aprobado** , encuentra y seleccione una o más entradas de tiempo aprobadas para corregir.</span><span class="sxs-lookup"><span data-stu-id="f63a0-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="f63a0-112">Puede usar el filtro para encontrar entradas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f63a0-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="f63a0-113">Por ejemplo, puede filtrar por un id. de proyecto y seleccionar todas las entradas de tiempo aprobadas con ese id. de proyecto.</span><span class="sxs-lookup"><span data-stu-id="f63a0-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="f63a0-114">Seleccione **Corregir entradas**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-114">Select **Correct entries**.</span></span> <span data-ttu-id="f63a0-115">Se crea automáticamente un nuevo diario de corrección, con el tipo asignado **Corrección de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="f63a0-116">Las entradas que seleccionó se agregan al diario.</span><span class="sxs-lookup"><span data-stu-id="f63a0-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="f63a0-117">En la página **Nuevo diario** , introduzca una **Descripción** para su diario de corrección y luego seleccione la pestaña **Correcciones de entradas de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="f63a0-118">En la sección **Nuevos valores de entradas de tiempo** , actualice los campos con la información correcta según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f63a0-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="f63a0-119">Por ejemplo, puede cambiar el proyecto asignado o el recurso que se puede reservar.</span><span class="sxs-lookup"><span data-stu-id="f63a0-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="f63a0-120">Seleccione **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-120">Select **Preview**.</span></span> <span data-ttu-id="f63a0-121">En el cuadro de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="f63a0-122">En la pestaña **Líneas de diario** , puede ver una lista de los datos reales originales que están relacionados con las entradas de tiempo seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado.</span><span class="sxs-lookup"><span data-stu-id="f63a0-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="f63a0-123">Si es necesario realizar correcciones adicionales, repita los pasos 5 y 6.</span><span class="sxs-lookup"><span data-stu-id="f63a0-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="f63a0-124">Todos los datos reales corregidos tendrán los mismos valores que seleccionó en la sección **Nuevos valores de entradas de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="f63a0-125">Si las correcciones aparecen como se espera, seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="f63a0-126">En el cuadro de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="f63a0-127">Vuelva al área **Ventas** , seleccione **Proyectos** y luego abra el proyecto para el que acaba de actualizar las entradas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f63a0-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="f63a0-128">En la página **Proyectos** , en la pestaña **Datos reales** , vea los cambios que ha realizado.</span><span class="sxs-lookup"><span data-stu-id="f63a0-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="f63a0-129">Si la pestaña **Datos reales** no está visible, seleccione **Relacionado** > **Datos reales**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="f63a0-130">En la lista **Vista asociada real** , puede ver que las entradas de tiempo originales que se han revertido todavía se muestran, al igual que las entradas de tiempo corregidas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f63a0-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="f63a0-131">Por ejemplo, en el siguiente gráfico, hay dos elementos de línea con una cantidad de 8,00 que tienen débitos en la columna Cantidad.</span><span class="sxs-lookup"><span data-stu-id="f63a0-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="f63a0-132">Además, hay dos elementos de línea con una cantidad de -8,00 que muestran los importes abonados en la columna Importe.</span><span class="sxs-lookup"><span data-stu-id="f63a0-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="f63a0-133">Estas correcciones lleva la cantidad a cero.</span><span class="sxs-lookup"><span data-stu-id="f63a0-133">These corrections bring the quantity to zero.</span></span>

![Lista de vista asociada de datos reales](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="f63a0-135">Corregir entradas de gasto aprobadas</span><span class="sxs-lookup"><span data-stu-id="f63a0-135">Correct approved expense entries</span></span>

<span data-ttu-id="f63a0-136">Complete los siguientes pasos para corregir una o más entradas de gastos.</span><span class="sxs-lookup"><span data-stu-id="f63a0-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="f63a0-137">En el área **Ventas** , en el panel de navegación izquierdo, debajo de **Transacciones** , seleccione **Gastos aprobados**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="f63a0-138">En la lista **Gastos aprobados** , seleccione el proyecto que desea corregir y luego seleccione **Corregir entradas**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="f63a0-139">Se creará automáticamente un nuevo diario de corrección, con el tipo asignado de **Corrección de gastos**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="f63a0-140">En la página **Nuevo diario** , introduzca una **Descripción** para la corrección y, en la pestaña **Corrección de gastos** , en la sección **Nuevos valores para los gastos** , seleccione los campos de datos que desea corregir para las líneas de gastos seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="f63a0-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="f63a0-141">Por ejemplo, puede asignar el gasto a otro **Proyecto** o corregir la **Categoría de gastos** , la **Fecha del gasto** o el **Recurso que se puede reservar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="f63a0-142">Seleccione **Vista previa**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-142">Select **Preview**.</span></span> <span data-ttu-id="f63a0-143">En el cuadro de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="f63a0-144">Compruebe las correcciones en la pestaña **Líneas de diario**. Puede ver una lista de los datos reales originales que están relacionados con las entradas de gasto seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado.</span><span class="sxs-lookup"><span data-stu-id="f63a0-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="f63a0-145">Si los valores corregidos aparecen como se espera, seleccione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="f63a0-146">En el cuadro de diálogo, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="f63a0-147">Si los valores no se muestran según lo previsto, seleccione **Cancelar** para volver a la lista **Gastos aprobados**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="f63a0-148">Repita los pasos del 2 al 5.</span><span class="sxs-lookup"><span data-stu-id="f63a0-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="f63a0-149">Los datos reales corregidos tendrán los mismos valores que seleccionó en la sección **Nuevos valores para los gastos**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="f63a0-150">Después de confirmar el diario de corrección, vuelva al proyecto o proyectos que ha actualizado, para ver sus cambios.</span><span class="sxs-lookup"><span data-stu-id="f63a0-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="f63a0-151">En la página del proyecto, en la pestaña **Datos reales** , revise la **Vista asociada de datos reales**.</span><span class="sxs-lookup"><span data-stu-id="f63a0-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="f63a0-152">Se enumeran las entradas originales y las entradas corregidas.</span><span class="sxs-lookup"><span data-stu-id="f63a0-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="f63a0-153">En el siguiente gráfico se muestran los importes de entrada de gastos originales y los importes de entrada de gastos corregidos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f63a0-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Datos reales de gastos](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
