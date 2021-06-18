---
title: Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente
description: Este tema explica cómo registrar facturas de proveedor pendientes.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993835"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="32b96-103">Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente</span><span class="sxs-lookup"><span data-stu-id="32b96-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="32b96-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="32b96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="32b96-105">Cuando una empresa adquiere materiales no mantenidos en existencias para un proyecto, los costes se pueden registrar inmediatamente en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="32b96-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="32b96-106">Por ejemplo, Contoso Robotics US está realizando un proyecto de renovación de equipos y necesita licencias de software.</span><span class="sxs-lookup"><span data-stu-id="32b96-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="32b96-107">Estas licencias se obtienen de un proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="32b96-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="32b96-108">Utilizando Dynamics 365 Finance, el empleado de Proveedores registra un documento de factura de proveedor pendiente y atribuye los costes de la licencia directamente al proyecto de renovación del equipo.</span><span class="sxs-lookup"><span data-stu-id="32b96-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="32b96-109">Antes de utilizar la funcionalidad descrita en este tema, revise y aplique las configuraciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="32b96-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="32b96-110">Para más información, vea [Habilitar materiales no mantenidos en existencias y facturas de proveedor pendiente](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="32b96-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="32b96-111">Registrar una factura de proveedor pendiente relacionada con el proyecto</span><span class="sxs-lookup"><span data-stu-id="32b96-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="32b96-112">Las facturas de proveedor pendientes se pueden registrar en la página **Facturas de proveedor pendientes** (**Proveedores** > **Facturas** > **Facturas de proveedor pendientes**).</span><span class="sxs-lookup"><span data-stu-id="32b96-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="32b96-113">Complete los siguientes pasos para registrar una factura de proveedor pendiente relacionada con el proyecto:</span><span class="sxs-lookup"><span data-stu-id="32b96-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="32b96-114">Vaya a **Proveedores** > **Facturas** y seleccione **Nueva**.</span><span class="sxs-lookup"><span data-stu-id="32b96-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="32b96-115">En el campo **Cuenta de facturación**, seleccione un proveedor y en el campo **Número**, ingrese la identificación de la factura del proveedor.</span><span class="sxs-lookup"><span data-stu-id="32b96-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="32b96-116">Agregue una línea a la factura del proveedor y en el campo **Número de artículo**, seleccione el artículo no mantenido en existencias comprado al proveedor.</span><span class="sxs-lookup"><span data-stu-id="32b96-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="32b96-117">Las líneas de factura de proveedor que se basan en una categoría de adquisición no se pueden registrar en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="32b96-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="32b96-118">Agregue la cantidad comprada.</span><span class="sxs-lookup"><span data-stu-id="32b96-118">Add the quantity purchased.</span></span> <span data-ttu-id="32b96-119">El sistema completará el precio unitario según la configuración del precio del artículo no mantenido en existencias.</span><span class="sxs-lookup"><span data-stu-id="32b96-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="32b96-120">Verifique el importe total y otros detalles requeridos en la línea.</span><span class="sxs-lookup"><span data-stu-id="32b96-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="32b96-121">En los detalles de la línea, en la pestaña **Proyecto**, seleccione el ID del proyecto en el que se registrará este elemento.</span><span class="sxs-lookup"><span data-stu-id="32b96-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="32b96-122">Opcionalmente, seleccione el número de actividad y actualice la categoría del proyecto y la propiedad de la línea.</span><span class="sxs-lookup"><span data-stu-id="32b96-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="32b96-123">Registre la factura del proveedor pendiente.</span><span class="sxs-lookup"><span data-stu-id="32b96-123">Post pending vendor invoice.</span></span> <span data-ttu-id="32b96-124">Cuando se contabiliza la factura, el sistema registra:</span><span class="sxs-lookup"><span data-stu-id="32b96-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="32b96-125">El importe del saldo del proveedor.</span><span class="sxs-lookup"><span data-stu-id="32b96-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="32b96-126">El importe del impuesto sobre ventas.</span><span class="sxs-lookup"><span data-stu-id="32b96-126">The sales tax amount.</span></span>
    - <span data-ttu-id="32b96-127">El coste del proyecto se registra en la cuenta de integración de adquisiciones.</span><span class="sxs-lookup"><span data-stu-id="32b96-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="32b96-128">La transacción real del proyecto en Dataverse.</span><span class="sxs-lookup"><span data-stu-id="32b96-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="32b96-129">La transacción se sigue procesando utilizando el diario [Integración de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="32b96-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="32b96-130">El registro de este diario mueve el importe de la cuenta de integración de compras a la cuenta de coste del proyecto.</span><span class="sxs-lookup"><span data-stu-id="32b96-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
