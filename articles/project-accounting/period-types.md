---
title: Tipos de período
description: En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531563"
---
# <a name="period-types"></a><span data-ttu-id="15ae1-103">Tipos de período</span><span class="sxs-lookup"><span data-stu-id="15ae1-103">Period types</span></span>

<span data-ttu-id="15ae1-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="15ae1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="15ae1-105">Un tipo de período define la frecuencia con la que se estiman los ingresos de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="15ae1-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="15ae1-106">En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos.</span><span class="sxs-lookup"><span data-stu-id="15ae1-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="15ae1-107">Crear y trabajar con tipos de períodos</span><span class="sxs-lookup"><span data-stu-id="15ae1-107">Create and work with period types</span></span>
<span data-ttu-id="15ae1-108">Para crear y trabajar con tipos de período, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="15ae1-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="15ae1-109">En su entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Estimaciones** > **Tipos de período**.</span><span class="sxs-lookup"><span data-stu-id="15ae1-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="15ae1-110">Seleccione **Nuevo** para crear un nuevo tipo de período.</span><span class="sxs-lookup"><span data-stu-id="15ae1-110">Select **New** to create new period type.</span></span> <span data-ttu-id="15ae1-111">Escriba un nombre y una descripción.</span><span class="sxs-lookup"><span data-stu-id="15ae1-111">Enter a name and description.</span></span>
3. <span data-ttu-id="15ae1-112">En el campo **Frecuencia**, seleccione un valor:</span><span class="sxs-lookup"><span data-stu-id="15ae1-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="15ae1-113">Si selecciona **Semana**,**Quincenal**, **Semimensual**, **Mes**, **Día**, **Trimestre** o **Año**, el calendario se utilizará para generar los períodos.</span><span class="sxs-lookup"><span data-stu-id="15ae1-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="15ae1-114">Si selecciona **Período contable**, los períodos contables de la configuración de Contabilidad general se utilizarán para generar períodos.</span><span class="sxs-lookup"><span data-stu-id="15ae1-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="15ae1-115">Si selecciona **Sin límite**, puede especificar períodos personalizados.</span><span class="sxs-lookup"><span data-stu-id="15ae1-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="15ae1-116">Seleccione el registro de tipo de período y, a continuación, **Generar períodos** para crear períodos para el tipo de período.</span><span class="sxs-lookup"><span data-stu-id="15ae1-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="15ae1-117">Según la frecuencia del período que haya seleccionado, es posible que tenga la opción de especificar una fecha de inicio o el número de períodos para generar.</span><span class="sxs-lookup"><span data-stu-id="15ae1-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="15ae1-118">Seleccione **Períodos** para revisar periodos generados.</span><span class="sxs-lookup"><span data-stu-id="15ae1-118">Select **Periods** to review generated periods.</span></span>

