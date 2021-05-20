---
title: Importar y mantener transacciones con tarjetas de crédito
description: En este tema se explica cómo importar y mantener transacciones con tarjeta de crédito relacionadas con gastos. Estas transacciones se pueden configurar para que se importen automáticamente en una programación periódica, o se pueden importar manualmente según sea necesario.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951095"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="d1bc4-104">Importar y mantener transacciones con tarjetas de crédito</span><span class="sxs-lookup"><span data-stu-id="d1bc4-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="d1bc4-105">Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="d1bc4-106">O bien, las transacciones se pueden importar manualmente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="d1bc4-107">Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="d1bc4-108">Para obtener más información sobre entidades de datos, consulte [Entidades de datos](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="d1bc4-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="d1bc4-109">Importar transacciones con tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="d1bc4-109">Import credit card transactions</span></span>

1. <span data-ttu-id="d1bc4-110">En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="d1bc4-111">Si abre la administración de datos por primera vez, el sistema deberá actualizar la lista de entidades de datos para que pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="d1bc4-112">En el campo **Nombre**, introduzca una descripción única del trabajo de importación.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="d1bc4-113">En el campo **Formato de datos de origen**, seleccione el formato del archivo que contiene las transacciones con tarjeta de crédito que quiere importar.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="d1bc4-114">Seleccione **Cargar** y luego busque y seleccione el archivo que desee importar.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="d1bc4-115">Una vez cargado el archivo, valide la asignación del archivo de transacciones con tarjeta de crédito y las columnas de la entidad de datos de transacciones con tarjeta de crédito seleccionando el vínculo **Ver mapa** en el mosaico.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="d1bc4-116">Si hay errores de asignación o si debe cambiar la asignación, introduzca los cambios de asignación desde la pestaña **Visualización de asignación** o la pestaña **Detalles de la asignación**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="d1bc4-117">Para automatizar las transacciones con tarjeta de crédito, seleccione **Crear trabajo de datos periódico**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="d1bc4-118">Luego ya podrá establecer la periodicidad que define la frecuencia con la que se deben importar las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="d1bc4-119">Cuando haya terminado, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="d1bc4-120">Para importar ahora el archivo seleccionado, seleccione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="d1bc4-121">Si se producen errores durante la importación, puede ver el registro de ejecución o los datos de almacenamiento provisional para ver los errores que debe corregir para ayudar a garantizar una importación correcta.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="d1bc4-122">Si debe importar más de un formato de archivo, debe crear trabajos de importación independientes para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="d1bc4-123">Reasignar las transacciones con tarjeta de crédito para empleados cancelados</span><span class="sxs-lookup"><span data-stu-id="d1bc4-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="d1bc4-124">Una vez que se cancela un registro de empleado, la cuenta de Active Directory Domain Services (AD DS) del empleado se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="d1bc4-125">Sin embargo, es posible que haya transacciones con tarjeta de crédito activas que aún deben contabilizarse como gastos y reembolsarse.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="d1bc4-126">Desde la página **Transacciones con tarjeta de crédito**, puede reasignar al empleado para cualquier transacción con tarjeta de crédito en la que se haya cancelado al empleado.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="d1bc4-127">Seleccione una o varias transacciones con tarjeta de crédito y luego seleccione **Reasignar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="d1bc4-128">A continuación, puede seleccionar otro empleado para asignarle las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="d1bc4-129">Una vez reasignadas las transacciones con tarjeta de crédito, pueden seleccionarse para un informe de gastos y pagarse mediante el proceso habitual para el reembolso del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="d1bc4-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]