---
title: Corregir la contabilidad en propuestas de factura de proyecto en borrador
description: Este tema explica cómo ajustar la información relacionada con la contabilidad en un borrador de propuesta de factura.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251279"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="a1517-103">Corregir la contabilidad en propuestas de factura de proyecto en borrador</span><span class="sxs-lookup"><span data-stu-id="a1517-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="a1517-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="a1517-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a1517-105">El administradior del proyecto mantiene los *Detalles de operaciones* para las facturas del mismo en una factura proforma.</span><span class="sxs-lookup"><span data-stu-id="a1517-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="a1517-106">Estos detalles incluyen la decisión sobre las horas, gastos, materiales o hitos que se deben facturar, las tarifas y la aplicación de los importes de anticipos y avances.</span><span class="sxs-lookup"><span data-stu-id="a1517-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="a1517-107">Después de confirmar la factura proforma original, puede ajustar los detalles de operaciones creando y confirmando una [factura proforma correctiva](../proforma-invoicing/corrective-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="a1517-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="a1517-108">Los *Detalles de contabilidad* para las facturas del proyecto se mantienen en un documento de factura de cara al cliente.</span><span class="sxs-lookup"><span data-stu-id="a1517-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="a1517-109">Estos detalles incluyen el cálculo del impuesto sobre las ventas y las dimensiones financieras que se aplican a la factura.</span><span class="sxs-lookup"><span data-stu-id="a1517-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="a1517-110">Este tema proporciona detalles sobre cómo se pueden ajustar estos detalles de contabilidad en un borrador de propuesta de factura de proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="a1517-111">Ajustar el impuesto de ventas</span><span class="sxs-lookup"><span data-stu-id="a1517-111">Adjust sales tax</span></span>

<span data-ttu-id="a1517-112">Los grupos de impuestos sobre las ventas de facturación predeterminados y los grupos de impuestos sobre las ventas de artículos se pueden ajustar directamente en el documento de propuesta de factura.</span><span class="sxs-lookup"><span data-stu-id="a1517-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="a1517-113">Para ajustar estos grupos, seleccione **Editar** y luego, en cada línea de propuesta de factura de proyecto, introduzca un nuevo valor en los campos **Grupo de impuestosç** o **Grupos de impuestos de artículos**.</span><span class="sxs-lookup"><span data-stu-id="a1517-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="a1517-114">Ajustar dimensiones financieras</span><span class="sxs-lookup"><span data-stu-id="a1517-114">Adjust financial dimensions</span></span>

<span data-ttu-id="a1517-115">Las dimensiones financieras no se pueden editar directamente en una línea de propuesta de factura de proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="a1517-116">En su lugar, siga estos pasos para ajustar las dimensiones financieras en una propuesta de factura de proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="a1517-117">En la propuesta de factura del proyecto, seleccione **Eliminar todo** para eliminar las líneas de propuesta de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a1517-118">El botón **Eliminar todo** está disponible solo después de que el administrador del sistema habilite la característica **Eliminar las líneas de propuesta de factura cuando utilice Project Operations para escenarios basados en recursos/sin existencias** en el área de trabajo **Administración de características**.</span><span class="sxs-lookup"><span data-stu-id="a1517-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="a1517-119">Ajustar dimensiones financieras:</span><span class="sxs-lookup"><span data-stu-id="a1517-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="a1517-120">**Transacciones a cuenta (hitos de facturación):** vaya a **Todos los proyectos** \> **Administrar** \> **Transacciones a cuenta** y seleccione el hito que necesite ajuste.</span><span class="sxs-lookup"><span data-stu-id="a1517-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="a1517-121">Después, en la pestaña **Dimensiones financieras**, actualice los valores según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a1517-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="a1517-122">**Transacciones de tiempo, gastos y materiales:** en la página **Transacciones de proyecto registradas**, seleccione **Ajustar la contabilidad** para actualizar las dimensiones financieras.</span><span class="sxs-lookup"><span data-stu-id="a1517-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="a1517-123">Una vez que haya terminado de ajustar los valores de la dimensión financiera, vaya a **Administración de proyectos y contabilidad** \> **Periódico** \> **Integración de Project Operations** y seleccione **Importar desde tabla de almacenamiento provisional** para ejecutar el proceso periódico.</span><span class="sxs-lookup"><span data-stu-id="a1517-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="a1517-124">Ese proceso utiliza los valores de dimensión financiera actualizados para volver a crear las líneas de propuesta de factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="a1517-125">Los valores actualizados se utilizan en el libro mayor auxiliar y en el libro mayor general del proyecto cuando se registra la factura del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a1517-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>