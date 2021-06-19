---
title: Trabajar con gastos personales en un informe de gastos
description: Este tema proporciona información sobre cómo trabajar con los gastos personales de los empleados en sus viajes de negocios.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025705"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="3075a-103">Trabajar con gastos personales en un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="3075a-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="3075a-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="3075a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3075a-105">En un viaje de negocios, un empleado pueden cargar gastos personales en la tarjeta de crédito corporativa.</span><span class="sxs-lookup"><span data-stu-id="3075a-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="3075a-106">Si no se ha definido un proceso para gestionar los gastos personales, el proceso de aprobación de informes de gastos podría verse interrumpido cuando el empleado envía el informe detallado de gastos.</span><span class="sxs-lookup"><span data-stu-id="3075a-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="3075a-107">Están disponibles dos métodos para trabajar con los gastos personales de un empleado:</span><span class="sxs-lookup"><span data-stu-id="3075a-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="3075a-108">**Pagados por empleado**: su organización no paga los gastos personales que aparecen en la factura de la tarjeta de crédito corporativa.</span><span class="sxs-lookup"><span data-stu-id="3075a-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="3075a-109">En lugar de ello, el empleado paga directamente los gastos al proveedor de la tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="3075a-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="3075a-110">**Pagados por la empresa**: la organización paga la factura completa de la tarjeta de crédito corporativa y luego carga los gastos personales en la cuenta del empleado.</span><span class="sxs-lookup"><span data-stu-id="3075a-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="3075a-111">Puede seleccionar el método que utiliza su organización en la página **Parámetros de gestión de gastos**.</span><span class="sxs-lookup"><span data-stu-id="3075a-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="3075a-112">Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido</span><span class="sxs-lookup"><span data-stu-id="3075a-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="3075a-113">La característica **Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido** solo se aplica a los informes de gastos aprobados mediante un flujo de trabajo de nivel de línea.</span><span class="sxs-lookup"><span data-stu-id="3075a-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="3075a-114">Los informes se aprueban yendo a **Procesar informes de gastos** > **Informes de gastos asignados a mí** > **Abrir informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="3075a-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="3075a-115">Para habilitar esta característica, vaya a **Espacios de trabajo** > **Gestión de funciones**, seleccione **Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido** y luego seleccione **Habilitar ahora**.</span><span class="sxs-lookup"><span data-stu-id="3075a-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="3075a-116">Si la característica está habilitada, las líneas de gastos que utilizan esta funcionalidad generan dos líneas cuando se envía el informe.</span><span class="sxs-lookup"><span data-stu-id="3075a-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="3075a-117">Se generan dos líneas para que el aprobador pueda aprobar cada línea por separado.</span><span class="sxs-lookup"><span data-stu-id="3075a-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
