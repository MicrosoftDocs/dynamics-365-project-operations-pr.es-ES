---
title: Información general de gastos
description: Este tema proporciona información sobre la funcionalidad Gastos en Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764930"
---
# <a name="expense-home-page"></a><span data-ttu-id="94a7b-103">Página principal de gasto</span><span class="sxs-lookup"><span data-stu-id="94a7b-103">Expense home page</span></span>

<span data-ttu-id="94a7b-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="94a7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="94a7b-105">Dynamics 365 Project Operations admite la capacidad de procesar los gastos.</span><span class="sxs-lookup"><span data-stu-id="94a7b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="94a7b-106">El procesamiento de gastos se produce con o sin proyectos mediante el uso de un flujo de trabajo personalizable de directivas, categorías de transacciones y aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="94a7b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="94a7b-107">En Project Operations, hay dos modelos de implementación admitidos para Gastos:</span><span class="sxs-lookup"><span data-stu-id="94a7b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="94a7b-108">**Completa**: la implementación completa está disponible para **Project Operations para basados en recursos/no mantenidos en existencias** o **Project Operations para escenarios basados en pedidos de producción**.</span><span class="sxs-lookup"><span data-stu-id="94a7b-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="94a7b-109">**Básico**: la implementación básica está disponible para **Operaciones de proyecto para escenarios basados en recursos/no en existencias** e **Implementación simplificada: facturación de ofertas a proforma**.</span><span class="sxs-lookup"><span data-stu-id="94a7b-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="94a7b-110">Completo</span><span class="sxs-lookup"><span data-stu-id="94a7b-110">Full</span></span> 
<span data-ttu-id="94a7b-111">La implementación de gasto completo proporciona una aplicación de directivas completa que incluye la capacidad de crear directivas, como:</span><span class="sxs-lookup"><span data-stu-id="94a7b-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="94a7b-112">Límites de categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="94a7b-112">Expense category limits</span></span>
  - <span data-ttu-id="94a7b-113">Viajes</span><span class="sxs-lookup"><span data-stu-id="94a7b-113">Travel</span></span>
  - <span data-ttu-id="94a7b-114">Dietas</span><span class="sxs-lookup"><span data-stu-id="94a7b-114">Per diem</span></span>
  - <span data-ttu-id="94a7b-115">Importaciones de tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="94a7b-115">Credit card imports</span></span>
  - <span data-ttu-id="94a7b-116">Reconocimiento óptico de caracteres de recibos</span><span class="sxs-lookup"><span data-stu-id="94a7b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="94a7b-117">Básica</span><span class="sxs-lookup"><span data-stu-id="94a7b-117">Basic</span></span> 
<span data-ttu-id="94a7b-118">El escenario de implementación de gastos básicos solo le permite registrar los gastos básicos frente a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="94a7b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="94a7b-119">Para más información, consulte [Entrada de gastos (simplificada)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="94a7b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="94a7b-120">Determinar la implementación de gastos</span><span class="sxs-lookup"><span data-stu-id="94a7b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="94a7b-121">Para determinar si está ejecutando la implementación de la administración de gastos básicos, verifique que la dirección URL termine por **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="94a7b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
