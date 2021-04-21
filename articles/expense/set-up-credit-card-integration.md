---
title: Configurar la integración de tarjetas de crédito
description: Este tema explica cómo trabajar con transacciones de tarjetas de crédito relacionadas con gastos.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866704"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="113fb-103">Configurar la integración de tarjetas de crédito</span><span class="sxs-lookup"><span data-stu-id="113fb-103">Set up credit card integration</span></span>

<span data-ttu-id="113fb-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="113fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="113fb-105">Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico.</span><span class="sxs-lookup"><span data-stu-id="113fb-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="113fb-106">Como alternativa, las transacciones se pueden importar manualmente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="113fb-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="113fb-107">Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="113fb-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="113fb-108">Importar transacciones con tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="113fb-108">Import credit card transactions</span></span>

<span data-ttu-id="113fb-109">Para importar transacciones con tarjeta de crédito, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="113fb-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="113fb-110">En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="113fb-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="113fb-111">Si abre la administración de datos por primera vez, el sistema debe actualizar la lista de entidades de datos antes de que pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="113fb-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="113fb-112">En el campo **Nombre**, indique una descripción única para el trabajo de importación.</span><span class="sxs-lookup"><span data-stu-id="113fb-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="113fb-113">En el campo **Formato de datos de origen**, seleccione el formato del archivo que contiene las transacciones con tarjeta de crédito para importar.</span><span class="sxs-lookup"><span data-stu-id="113fb-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="113fb-114">Seleccione **Cargar** y luego busque y seleccione el archivo para importar.</span><span class="sxs-lookup"><span data-stu-id="113fb-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="113fb-115">Una vez cargado el archivo, valide la asignación del archivo de transacciones con tarjeta de crédito y las columnas de la entidad de datos de transacciones con tarjeta de crédito seleccionando el vínculo **Ver mapa** en el mosaico.</span><span class="sxs-lookup"><span data-stu-id="113fb-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="113fb-116">Si hay errores de asignación, o si debe cambiar la asignación, realice los cambios de asignación desde la pestaña **Visualización de asignaciones** o la pestaña **Detalles de la asignación**.</span><span class="sxs-lookup"><span data-stu-id="113fb-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="113fb-117">Para automatizar las transacciones con tarjeta de crédito, seleccione **Crear trabajo de datos periódico**.</span><span class="sxs-lookup"><span data-stu-id="113fb-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="113fb-118">A continuación, puede establecer la periodicidad que define la frecuencia con la que se deben importar las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="113fb-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="113fb-119">Cuando haya terminado, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="113fb-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="113fb-120">Para importar ahora el archivo seleccionado, seleccione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="113fb-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="113fb-121">Si se producen errores durante la importación, puede ver el registro de ejecución o los datos de ensayo para ver los errores que debe corregir para ayudar a garantizar una importación correcta.</span><span class="sxs-lookup"><span data-stu-id="113fb-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="113fb-122">Si necesita importar más de un formato de archivo, debe crear trabajos de importación separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="113fb-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="113fb-123">Reasignar las transacciones con tarjeta de crédito para empleados cancelados</span><span class="sxs-lookup"><span data-stu-id="113fb-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="113fb-124">Una vez que se cancela un registro de empleado, la cuenta de Active Directory Domain Services (AD DS) del empleado se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="113fb-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="113fb-125">Sin embargo, es posible que haya transacciones con tarjeta de crédito activas que aún deben contabilizarse como gastos y reembolsarse.</span><span class="sxs-lookup"><span data-stu-id="113fb-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="113fb-126">En la página **Transacciones con tarjeta de crédito**, puede reasignar al empleado para cualquier transacción con tarjeta de crédito en la que el empleado asociado haya sido rescindido.</span><span class="sxs-lookup"><span data-stu-id="113fb-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="113fb-127">Seleccione una o varias transacciones con tarjeta de crédito y luego seleccione **Reasignar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="113fb-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="113fb-128">A continuación, puede seleccionar otro empleado para asignarle las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="113fb-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="113fb-129">Una vez reasignadas las transacciones con tarjeta de crédito, pueden seleccionarse para un informe de gastos y pagarse mediante el proceso habitual para el reembolso del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="113fb-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="113fb-130">Eliminar transacciones con tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="113fb-130">Delete credit card transactions</span></span> 

<span data-ttu-id="113fb-131">A veces, después de que se importan las transacciones con tarjeta de crédito, es posible que sea necesario eliminar ciertas transacciones.</span><span class="sxs-lookup"><span data-stu-id="113fb-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="113fb-132">Esto podría deberse a que las transacciones están duplicadas o a que los datos pueden no ser precisos.</span><span class="sxs-lookup"><span data-stu-id="113fb-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="113fb-133">Los administradores pueden usar la característica **"Eliminar transacciones con tarjeta de crédito"** para seleccionar y eliminar transacciones con tarjeta de crédito que **no estén asociada** a un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="113fb-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="113fb-134">Vaya a **Tareas periódicas** > **Eliminar transacciones con tarjeta de crédito**.</span><span class="sxs-lookup"><span data-stu-id="113fb-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="113fb-135">Seleccione **Filtro** y proporcione información para identificar los registros que se incluirán.</span><span class="sxs-lookup"><span data-stu-id="113fb-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="113fb-136">Seleccione **Aceptar** para eliminar los registros.</span><span class="sxs-lookup"><span data-stu-id="113fb-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
