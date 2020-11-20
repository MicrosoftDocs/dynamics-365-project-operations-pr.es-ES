---
title: Configurar la integración de Project Operations por entidad jurídica
description: Este tema proporciona información sobre cómo configurar la integración entidad jurídica en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122904"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="147d4-103">Configurar la integración de Project Operations por entidad jurídica</span><span class="sxs-lookup"><span data-stu-id="147d4-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="147d4-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="147d4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="147d4-105">Este tema le guía a través de los pasos necesarios para configurar Dynamics 365 Project Operations por entidad legal.</span><span class="sxs-lookup"><span data-stu-id="147d4-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="147d4-106">Habilitar características clave en Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="147d4-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="147d4-107">Complete los siguientes pasos para habilitar las funciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="147d4-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="147d4-108">En Dynamics 365 Finance, vaya al espacio de trabajo **Administración de funciones**.</span><span class="sxs-lookup"><span data-stu-id="147d4-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="147d4-109">En **Lista de características**, busque y habilite las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="147d4-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="147d4-110">**Habilitar varias líneas de contrato para un proyecto**</span><span class="sxs-lookup"><span data-stu-id="147d4-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="147d4-111">**Habilitar Project Operations en Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="147d4-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="147d4-112">Si no ve **Características clave** en la lista, verifique que su versión de Finance cumpla con el requisito de versión mínima (versión de la aplicación 10.0.13 con todas las actualizaciones de calidad aplicadas o superior).</span><span class="sxs-lookup"><span data-stu-id="147d4-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="147d4-113">Seleccione **Buscar actualizaciones** para actualizar la lista de funciones.</span><span class="sxs-lookup"><span data-stu-id="147d4-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="147d4-114">Definir el escenario de implementación de Project Operations para una entidad jurídica</span><span class="sxs-lookup"><span data-stu-id="147d4-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="147d4-115">Puede habilitar Project Operations en Dynamics 365 Customer Engagement a nivel de entidad legal.</span><span class="sxs-lookup"><span data-stu-id="147d4-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="147d4-116">Puede tener una entidad legal usando Project Operations en Dynamics 365 Customer Engagement para escenarios basados en recursos / no almacenados.</span><span class="sxs-lookup"><span data-stu-id="147d4-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="147d4-117">En el mismo entorno, puede tener otra entidad jurídica que utilice Project Operations para escenarios de pedidos de existencias / producción.</span><span class="sxs-lookup"><span data-stu-id="147d4-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="147d4-118">En Dynamics 365 Finance, vaya a **Gestión y contabilidad de proyectos** > **Configuración** > **Parámetros de gestión de proyectos y contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="147d4-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="147d4-119">En la lista de entidades legales disponibles, seleccione las entidades donde se encuentran múltiples líneas de contrato y las funciones de Project Operations en Dynamics 365 Customer Engagement estarán habilitadas.</span><span class="sxs-lookup"><span data-stu-id="147d4-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="147d4-120">Deje sin seleccionar las entidades legales que utilizarán Project Operations para escenarios de órdenes de producción / almacenadas.</span><span class="sxs-lookup"><span data-stu-id="147d4-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="147d4-121">Se puede seleccionar una entidad legal solo si no tiene ningún proyecto existente.</span><span class="sxs-lookup"><span data-stu-id="147d4-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="147d4-122">Configurar Parámetros de gestión de proyectos y contabilidad</span><span class="sxs-lookup"><span data-stu-id="147d4-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="147d4-123">Cada entidad legal que usa Project Operations en Dynamics 365 Customer Engagement necesita un conjunto de parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="147d4-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="147d4-124">Estos parámetros se configuran en la pestaña **Project Operations** en la página **Parámetros contables y de gestión de proyectos**.</span><span class="sxs-lookup"><span data-stu-id="147d4-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="147d4-125">Los parámetros son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="147d4-125">The parameters are:</span></span>

  - <span data-ttu-id="147d4-126">**Valores predeterminados del tipo de facturación**: Project Operations utiliza un conjunto fijo de valores predeterminados de tipo de facturación que deben asignarse a las propiedades de línea Finance.</span><span class="sxs-lookup"><span data-stu-id="147d4-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="147d4-127">Cree un registro para cada tipo de facturación: **No especificado**, **Facturable**, **No facturable**, **Complementario** y **No disponible**.</span><span class="sxs-lookup"><span data-stu-id="147d4-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="147d4-128">**Valores predeterminados de categoría de proyecto**: seleccione las categorías de proyecto predeterminadas que se utilizarán para cada tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="147d4-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="147d4-129">Estos valores predeterminados se utilizarán en el **Diario de integración de Project Operations** y en estimaciones donde no se especifica ninguna categoría de transacción para el proyecto real.</span><span class="sxs-lookup"><span data-stu-id="147d4-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="147d4-130">**Pronósticos**: seleccione el modelo de pronóstico que se utilizará para las estimaciones de tiempo y gastos.</span><span class="sxs-lookup"><span data-stu-id="147d4-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
