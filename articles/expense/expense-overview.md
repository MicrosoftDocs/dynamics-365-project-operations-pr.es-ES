---
title: Información general de gastos
description: Este tema proporciona información sobre la funcionalidad Gastos en Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967387"
---
# <a name="expense-home-page"></a><span data-ttu-id="61e83-103">Página principal de gasto</span><span class="sxs-lookup"><span data-stu-id="61e83-103">Expense home page</span></span>

<span data-ttu-id="61e83-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="61e83-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="61e83-105">Dynamics 365 Project Operations admite la capacidad de procesar gastos.</span><span class="sxs-lookup"><span data-stu-id="61e83-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="61e83-106">El procesamiento de gastos se produce con o sin proyectos mediante el uso de un flujo de trabajo personalizable de directivas, categorías de transacciones y aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="61e83-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="61e83-107">En Project Operations, hay dos modelos de implementación admitidos para Gastos:</span><span class="sxs-lookup"><span data-stu-id="61e83-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="61e83-108">**Completo**: la implementación completa está disponible para **Operaciones de proyecto para escenarios basados en recursos/no en existencias** u **Operaciones de proyecto para escenarios basados en pedidos de producción**.</span><span class="sxs-lookup"><span data-stu-id="61e83-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="61e83-109">**Básico**: la implementación básica está disponible para **Operaciones de proyecto para escenarios basados en recursos/no en existencias** e **Implementación simplificada: facturación de ofertas a proforma**.</span><span class="sxs-lookup"><span data-stu-id="61e83-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="61e83-110">Completo</span><span class="sxs-lookup"><span data-stu-id="61e83-110">Full</span></span> 
<span data-ttu-id="61e83-111">La implementación de gastos completos proporciona una aplicación de directivas completa que incluye la capacidad de crear directivas, como:</span><span class="sxs-lookup"><span data-stu-id="61e83-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="61e83-112">Límites de Categoría de gastos</span><span class="sxs-lookup"><span data-stu-id="61e83-112">Expense category limits</span></span>
  - <span data-ttu-id="61e83-113">Viaje</span><span class="sxs-lookup"><span data-stu-id="61e83-113">Travel</span></span>
  - <span data-ttu-id="61e83-114">Dietas</span><span class="sxs-lookup"><span data-stu-id="61e83-114">Per diem</span></span>
  - <span data-ttu-id="61e83-115">Importaciones de tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="61e83-115">Credit card imports</span></span>
  - <span data-ttu-id="61e83-116">Reconocimiento óptico de caracteres de recibos</span><span class="sxs-lookup"><span data-stu-id="61e83-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="61e83-117">Básica</span><span class="sxs-lookup"><span data-stu-id="61e83-117">Basic</span></span> 
<span data-ttu-id="61e83-118">El escenario de implementación de gastos básicos solo le permite registrar los gastos básicos frente a un proyecto.</span><span class="sxs-lookup"><span data-stu-id="61e83-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="61e83-119">Para más información, consulte [Entrada de gastos (simplificada)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="61e83-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="61e83-120">Determinar la implementación de gastos</span><span class="sxs-lookup"><span data-stu-id="61e83-120">Determine your Expense deployment</span></span>
<span data-ttu-id="61e83-121">Para determinar si está ejecutando la implementación de la administración de gastos básicos, verifique que la dirección URL termine por **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="61e83-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
