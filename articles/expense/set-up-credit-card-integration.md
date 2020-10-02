---
title: Configurar la integración de tarjetas de crédito
description: En este tema se explica cómo importar y mantener transacciones con tarjeta de crédito relacionadas con gastos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896842"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="3aa55-103">Configurar la integración de tarjetas de crédito</span><span class="sxs-lookup"><span data-stu-id="3aa55-103">Set up credit card integration</span></span>

<span data-ttu-id="3aa55-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="3aa55-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3aa55-105">Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico.</span><span class="sxs-lookup"><span data-stu-id="3aa55-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3aa55-106">Como alternativa, las transacciones se pueden importar manualmente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3aa55-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3aa55-107">Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="3aa55-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3aa55-108">Importar transacciones con tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="3aa55-108">Import credit card transactions</span></span>

1. <span data-ttu-id="3aa55-109">En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3aa55-110">Si abre la administración de datos por primera vez, el sistema debe actualizar la lista de entidades de datos antes de que pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="3aa55-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3aa55-111">En el campo **Nombre**, escriba una descripción única del trabajo de importación.</span><span class="sxs-lookup"><span data-stu-id="3aa55-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="3aa55-112">En el campo **Formato de datos de origen**, seleccione el formato del archivo que contiene las transacciones con tarjeta de crédito para importar.</span><span class="sxs-lookup"><span data-stu-id="3aa55-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3aa55-113">Seleccione **Cargar** y luego busque y seleccione el archivo para importar.</span><span class="sxs-lookup"><span data-stu-id="3aa55-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3aa55-114">Una vez cargado el archivo, valide la asignación del archivo de transacciones con tarjeta de crédito y las columnas de la entidad de datos de transacciones con tarjeta de crédito seleccionando el vínculo **Ver mapa** en el mosaico.</span><span class="sxs-lookup"><span data-stu-id="3aa55-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3aa55-115">Si hay errores de asignación, o si debe cambiar la asignación, realice los cambios de asignación desde la pestaña **Visualización de asignaciones** o la pestaña **Detalles de la asignación**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3aa55-116">Para automatizar las transacciones con tarjeta de crédito, seleccione **Crear trabajo de datos periódico**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3aa55-117">A continuación, puede establecer la periodicidad que define la frecuencia con la que se deben importar las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="3aa55-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3aa55-118">Cuando haya terminado, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3aa55-119">Para importar ahora el archivo seleccionado, seleccione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3aa55-120">Si se producen errores durante la importación, puede ver el registro de ejecución o los datos de almacenamiento provisional para ver los errores que debe corregir para ayudar a garantizar una importación correcta.</span><span class="sxs-lookup"><span data-stu-id="3aa55-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3aa55-121">Si debe importar más de un formato de archivo, debe crear trabajos de importación independientes para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="3aa55-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3aa55-122">Reasignar las transacciones con tarjeta de crédito para empleados cancelados</span><span class="sxs-lookup"><span data-stu-id="3aa55-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3aa55-123">Una vez que se cancela un registro de empleado, la cuenta de Active Directory Domain Services (AD DS) del empleado se deshabilita.</span><span class="sxs-lookup"><span data-stu-id="3aa55-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3aa55-124">Sin embargo, es posible que haya transacciones con tarjeta de crédito activas que aún deben contabilizarse como gastos y reembolsarse.</span><span class="sxs-lookup"><span data-stu-id="3aa55-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3aa55-125">Desde la página **Transacciones con tarjeta de crédito**, puede reasignar al empleado para cualquier transacción con tarjeta de crédito en la que se haya cancelado al empleado.</span><span class="sxs-lookup"><span data-stu-id="3aa55-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3aa55-126">Seleccione una o varias transacciones con tarjeta de crédito y luego seleccione **Reasignar transacciones**.</span><span class="sxs-lookup"><span data-stu-id="3aa55-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3aa55-127">A continuación, puede seleccionar otro empleado para asignarle las transacciones con tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="3aa55-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3aa55-128">Una vez reasignadas las transacciones con tarjeta de crédito, pueden seleccionarse para un informe de gastos y pagarse mediante el proceso habitual para el reembolso del informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="3aa55-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
