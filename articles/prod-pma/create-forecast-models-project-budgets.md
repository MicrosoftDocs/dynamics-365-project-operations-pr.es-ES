---
title: Crear modelos de pronóstico para presupuestos de proyectos
description: Este tema describe cómo crear un modelo de previsión para los presupuestos restantes.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006321"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="6e23d-103">Crear modelos de pronóstico para presupuestos de proyectos</span><span class="sxs-lookup"><span data-stu-id="6e23d-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e23d-104">Este tema describe cómo crear un modelo de previsión para los presupuestos restantes.</span><span class="sxs-lookup"><span data-stu-id="6e23d-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="6e23d-105">Un proyecto que está sujeto a control presupuestario utiliza dos tipos de presupuestos: original y restante.</span><span class="sxs-lookup"><span data-stu-id="6e23d-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="6e23d-106">Cuando crea un presupuesto de proyecto, debe especificar los modelos de previsión presupuestaria original y restante que se crearon en la página **Modelos de pronóstico**.</span><span class="sxs-lookup"><span data-stu-id="6e23d-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="6e23d-107">Los presupuestos del proyecto basados en los modelos especificados se crean cuando compromete el presupuesto del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e23d-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="6e23d-108">Un modelo de previsión que se utiliza para el control presupuestario no puede tener un submodelo ni utilizarse como submodelo.</span><span class="sxs-lookup"><span data-stu-id="6e23d-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="6e23d-109">Seleccione **Gestión de proyectos y contabilidad** > **Configuración** > **Pronósticos**  > **Modelos de pronóstico**.</span><span class="sxs-lookup"><span data-stu-id="6e23d-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="6e23d-110">Seleccione **Nuevo** para crear un nuevo modelo de pronóstico y luego ingrese un número de identificación de modelo y un nombre para el nuevo modelo.</span><span class="sxs-lookup"><span data-stu-id="6e23d-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="6e23d-111">Establezca la opción **Detenido** a **Sí** para evitar cambios en las líneas de pronóstico del modelo de pronóstico.</span><span class="sxs-lookup"><span data-stu-id="6e23d-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="6e23d-112">Si las líneas de pronóstico con las que está asociado el modelo deben generar pronósticos de flujo de efectivo en el libro mayor, establezca **Incluir en las previsiones de flujo de caja** a **Sí.**</span><span class="sxs-lookup"><span data-stu-id="6e23d-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="6e23d-113">Para usar la fecha del proyecto como la fecha de la factura, establezca **Fecha de la factura prevista** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="6e23d-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="6e23d-114">En el campo **Tipo de presupuesto**, seleccione uno de los siguientes tipos de modelo:</span><span class="sxs-lookup"><span data-stu-id="6e23d-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="6e23d-115">**Presupuesto original**: utilice los importes del presupuesto original que se comprometen cuando se crea y aprueba el presupuesto inicial.</span><span class="sxs-lookup"><span data-stu-id="6e23d-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="6e23d-116">**Presupuesto restante**: utilice los importes restantes del presupuesto durante la vida del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e23d-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="6e23d-117">Los saldos en este modelo de pronóstico se reducen por transacciones reales y aumentan o disminuyen por revisiones presupuestarias.</span><span class="sxs-lookup"><span data-stu-id="6e23d-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="6e23d-118">**Transferir**: use los importes del presupuesto transferidos para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="6e23d-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="6e23d-119">Transferir es un proceso opcional que se puede ejecutar para transferir los importes presupuestarios no utilizados de un año fiscal a otro.</span><span class="sxs-lookup"><span data-stu-id="6e23d-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="6e23d-120">Establezca las siguientes opciones según sea necesario:</span><span class="sxs-lookup"><span data-stu-id="6e23d-120">Set the following options as required:</span></span>

   - <span data-ttu-id="6e23d-121">Habilite **Fecha de la factura prevista** para usar la fecha del proyecto como fecha de la factura.</span><span class="sxs-lookup"><span data-stu-id="6e23d-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="6e23d-122">Habilite **Previsión con WIP** para pronosticar según el trabajo en curso (WIP) y, a continuación, seleccione el tipo de WIP.</span><span class="sxs-lookup"><span data-stu-id="6e23d-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="6e23d-123">Puede mantener el **Tipo de presupuesto** predeterminado como **Ninguno** o introducir un nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="6e23d-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="6e23d-124">El tipo de presupuesto no se puede cambiar después de cambiar un registro.</span><span class="sxs-lookup"><span data-stu-id="6e23d-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="6e23d-125">Si cambia el tipo de presupuesto predeterminado, todas las demás opciones no estarán disponibles para las actualizaciones y no podrá reutilizar este modelo de previsión.</span><span class="sxs-lookup"><span data-stu-id="6e23d-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]