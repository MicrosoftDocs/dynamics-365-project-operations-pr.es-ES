---
title: Integración de factura de proyecto
description: Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955839"
---
# <a name="project-invoice-integration"></a><span data-ttu-id="d3545-103">Integración de factura de proyecto</span><span class="sxs-lookup"><span data-stu-id="d3545-103">Project invoice integration</span></span>

<span data-ttu-id="d3545-104">Este tema proporciona información sobre la integración de doble escritura de Project Operations para facturación de clientes.</span><span class="sxs-lookup"><span data-stu-id="d3545-104">This topic provides information about Project Operations dual-write integration for customer invoicing.</span></span>

<span data-ttu-id="d3545-105">En Project Operations, el jefe de proyecto administra el trabajo pendiente de facturación del proyecto y crea una factura proforma para el cliente en Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3545-105">In Project Operations, the Project manager manages the project billing backlog and creates a proforma invoice for the customer in Microsoft Dataverse.</span></span> <span data-ttu-id="d3545-106">De acuerdo con esta factura proforma, el empleado de Proveedores o el contable del proyecto crea una factura de cara al cliente.</span><span class="sxs-lookup"><span data-stu-id="d3545-106">Based on this proforma invoice, the Accounts receivable clerk or Project accountant creates a customer-facing invoice.</span></span> <span data-ttu-id="d3545-107">La integración de doble escritura garantiza que los detalles de la factura proforma se sincronizan con aplicaciones de Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3545-107">Dual-write integration ensures that the proforma invoice details are synchronized to Finance and Operations apps.</span></span> <span data-ttu-id="d3545-108">Una vez que se registra la factura de cara al cliente, el sistema actualiza los datos reales del proyecto relevantes en Dataverse con el detalle de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d3545-108">After the customer-facing invoice is posted, the system updates the relevant project actuals in Dataverse with the accounting detail.</span></span> <span data-ttu-id="d3545-109">El siguiente gráfico proporciona una descripción conceptual de alto nivel de esta integración.</span><span class="sxs-lookup"><span data-stu-id="d3545-109">The following graphic provides a high-level conceptual overview of this integration.</span></span>

   ![Integración de factura de proyecto](./media/DW5Invoicing.png)

<span data-ttu-id="d3545-111">Cuando el jefe del proyecto confirma la factura proforma en Dataverse, la información de encabezado de la factura proforma se sincroniza con aplicaciones de Finance and Operations que utilizan la asignación de tabla de doble escritura, **Propuesta de factura de proyecto V2 (facturas)**.</span><span class="sxs-lookup"><span data-stu-id="d3545-111">After the Project manager confirms the proforma invoice in Dataverse, the proforma invoice header information synchronizes to Finance and Operations apps using the dual-write table map, **Project invoice proposal V2 (invoices)**.</span></span> <span data-ttu-id="d3545-112">Esta es una integración unidireccional de Dataverse con aplicaciones de Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3545-112">This is a one-way integration from Dataverse to Finance and Operations apps.</span></span> <span data-ttu-id="d3545-113">No es posible crear o eliminar propuestas de factura de proyecto directamente en las aplicaciones de Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3545-113">Creating or deleting Project invoice proposals directly in Finance and Operations apps isn't supported.</span></span>

<span data-ttu-id="d3545-114">La confirmación de factura en Dataverse también desencadena la lógica de negocios para crear registros relacionados con facturación en la entidad **Datos reales**.</span><span class="sxs-lookup"><span data-stu-id="d3545-114">Invoice confirmation in Dataverse also triggers the business logic to create billing-related records in the **Actuals** entity.</span></span> <span data-ttu-id="d3545-115">Estos registros se sincronizan con aplicaciones de Finance and Operations que utilizan la asignación de tabla de doble escritura **Datos reales de integración de Project Operations (msdyn\_actuals).**</span><span class="sxs-lookup"><span data-stu-id="d3545-115">These records are synchronized to Finance and Operations using the dual-write table map, **Project Operations integration actuals (msdyn\_actuals).**</span></span> <span data-ttu-id="d3545-116">Para obtener más información, consulte [Estimaciones y datos reales del proyecto](resource-dual-write-estimates-actuals.md).</span><span class="sxs-lookup"><span data-stu-id="d3545-116">For more information, see [Project estimates and actuals](resource-dual-write-estimates-actuals.md).</span></span> 

<span data-ttu-id="d3545-117">Las líneas de propuestas de factura de proyecto se crean por el proceso periódico, **Importar desde tabla de almacenamiento provisional**.</span><span class="sxs-lookup"><span data-stu-id="d3545-117">Project invoice proposal lines are created by the periodic process, **Import form staging**.</span></span> <span data-ttu-id="d3545-118">Este proceso se basa en los detalles reales de las ventas facturadas en la tabla **Preparación de datos reales**.</span><span class="sxs-lookup"><span data-stu-id="d3545-118">This process is based on the billed sales actuals details in the **Actuals staging** table.</span></span> <span data-ttu-id="d3545-119">Para más información, vea [Administrar propuestas de facturas de proyectos](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span><span class="sxs-lookup"><span data-stu-id="d3545-119">For more information, see [Manage project invoice proposals](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals).</span></span> 