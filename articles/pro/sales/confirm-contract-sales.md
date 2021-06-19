---
title: Conformar un contrato de proyecto
description: Este tema proporciona información sobre confirmar un contrato en Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003697"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="ad07e-103">Conformar un contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="ad07e-103">Confirm a project contract</span></span>

<span data-ttu-id="ad07e-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="ad07e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ad07e-105">Un contrato de proyecto en Dynamics 365 Project Operations puede estar activo con una razón de **Confirmado**, o cerrado con un motivo de **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="ad07e-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="ad07e-106">Cuando confirma un contrato de proyecto, el estado se actualiza desde **Borrador** a **Activo** y la razón para el estado es **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="ad07e-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="ad07e-107">Un contrato activo o cerrado no se puede editar ni volver a abrir.</span><span class="sxs-lookup"><span data-stu-id="ad07e-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="ad07e-108">Repercusión financiera de confirmar un contrato de proyecto</span><span class="sxs-lookup"><span data-stu-id="ad07e-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="ad07e-109">Una vez que el contrato de proyecto esté confirmado, la aplicación volverá a calcular los costes; para ello, revertirá los datos reales de coste más antiguos y creará nuevos datos reales de coste.</span><span class="sxs-lookup"><span data-stu-id="ad07e-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="ad07e-110">A continuación, estos datos reales de costes nuevos se procesarán de acuerdo con el método de facturación de la línea de contrato de proyecto asociada.</span><span class="sxs-lookup"><span data-stu-id="ad07e-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="ad07e-111">Si los datos reales de costes hacen referencia a una línea de contrato de tiempo y material, la aplicación vuelve a crear automáticamente los datos reales de ventas no facturados correspondientes.</span><span class="sxs-lookup"><span data-stu-id="ad07e-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="ad07e-112">Si los costos reales hacen referencia a una línea de contrato de precio fijo, la aplicación deja de procesar los costos reales.</span><span class="sxs-lookup"><span data-stu-id="ad07e-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="ad07e-113">Los límites que no deben excederse, la configuración de la valoración y el precio y el coste de los datos reales se evalúan y luego se actualizan como parte del proceso de confirmaciones.</span><span class="sxs-lookup"><span data-stu-id="ad07e-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="ad07e-114">Cerrar un contrato de proyecto como perdido</span><span class="sxs-lookup"><span data-stu-id="ad07e-114">Close a project contract as lost</span></span>

<span data-ttu-id="ad07e-115">Cuando cierra un contrato de proyecto como perdido, el estado del contrato se actualiza a **Cerrado** y la razón para el estado es **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="ad07e-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="ad07e-116">El contrato del proyecto pasa a ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ad07e-116">The project contract becomes read-only.</span></span> <span data-ttu-id="ad07e-117">Se proporciona un cuadro de diálogo de confirmación antes de que se completen los cambios porque no puede volver a abrir un contrato de proyecto cerrado.</span><span class="sxs-lookup"><span data-stu-id="ad07e-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="ad07e-118">Si el contrato del proyecto que se cierra como perdido hace referencia a un proyecto en sus líneas, ese proyecto también se marca como cerrado.</span><span class="sxs-lookup"><span data-stu-id="ad07e-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="ad07e-119">Se cancelan todas las reservas de recursos a partir de ese día.</span><span class="sxs-lookup"><span data-stu-id="ad07e-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="ad07e-120">Los datos reales de ventas no facturados en el contrato del proyecto que aún no estén en una factura se revertirán.</span><span class="sxs-lookup"><span data-stu-id="ad07e-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="ad07e-121">En Dynamics 365 Project Operations, cerrar un contrato de proyecto como perdido no afectará el estado de la oportunidad asociada.</span><span class="sxs-lookup"><span data-stu-id="ad07e-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="ad07e-122">La oportunidad permanecerá abierta y deberá cerrarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="ad07e-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]