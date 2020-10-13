---
title: Información general de aprobaciones
description: Este tema proporciona información sobre cómo trabajar con aprobaciones en Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961187"
---
# <a name="approvals-overview"></a><span data-ttu-id="44bca-103">Información general de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="44bca-103">Approvals overview</span></span>

<span data-ttu-id="44bca-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="44bca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44bca-105">Los envíos de tiempo y gastos se mueven a través de un flujo de trabajo de aprobación.</span><span class="sxs-lookup"><span data-stu-id="44bca-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="44bca-106">Una vez aprobadas las entradas, las transacciones se registran en datos reales o el tiempo se registra en la programación.</span><span class="sxs-lookup"><span data-stu-id="44bca-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="44bca-107">Flujo de trabajo de aprobación</span><span class="sxs-lookup"><span data-stu-id="44bca-107">Approvals workflow</span></span>
<span data-ttu-id="44bca-108">Cuando crea y envía una entrada de tiempo o gastos, se crea una entrada de aprobación.</span><span class="sxs-lookup"><span data-stu-id="44bca-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="44bca-109">El aprobador del proyecto o su gerente revisa y aprueba su entrada.</span><span class="sxs-lookup"><span data-stu-id="44bca-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="44bca-110">Si la entrada está relacionada con un proyecto, cuando se apruebe, se crearán los datos reales.</span><span class="sxs-lookup"><span data-stu-id="44bca-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="44bca-111">Esto permite realizar un seguimiento del coste y la facturación.</span><span class="sxs-lookup"><span data-stu-id="44bca-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="44bca-112">Aprobar una entrada</span><span class="sxs-lookup"><span data-stu-id="44bca-112">Approve an entry</span></span>
<span data-ttu-id="44bca-113">El formulario **Aprobaciones** le permite cambiar entre diferentes vistas para que pueda ver los diferentes tipos de aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="44bca-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="44bca-114">Vaya al formulario **Aprobaciones** y seleccione **Gastos**, **Hora** o **Recordatorios**.</span><span class="sxs-lookup"><span data-stu-id="44bca-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="44bca-115">Revise cada aprobación y seleccione las que desea aprobar.</span><span class="sxs-lookup"><span data-stu-id="44bca-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="44bca-116">Seleccione **Aprobar** para aprobar las entradas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="44bca-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="44bca-117">El sistema procesará estas entradas y creará datos reales o una reserva.</span><span class="sxs-lookup"><span data-stu-id="44bca-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="44bca-118">Rechazar una entrada</span><span class="sxs-lookup"><span data-stu-id="44bca-118">Reject an entry</span></span>
<span data-ttu-id="44bca-119">Como aprobador del proyecto, es posible que deba enviar una entrada a un usuario para que la corrija.</span><span class="sxs-lookup"><span data-stu-id="44bca-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="44bca-120">Vaya al formulario **Aprobaciones** y seleccione la entrada a rechazar.</span><span class="sxs-lookup"><span data-stu-id="44bca-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="44bca-121">Seleccione **Rechazar**.</span><span class="sxs-lookup"><span data-stu-id="44bca-121">Select **Reject**.</span></span>
3. <span data-ttu-id="44bca-122">Opcional: agregue un comentario en el cuadro de diálogo **Comentarios de rechazo** para informar al usuario de por qué se rechaza la entrada.</span><span class="sxs-lookup"><span data-stu-id="44bca-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="44bca-123">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="44bca-123">Select **OK**.</span></span> <span data-ttu-id="44bca-124">La entrada se devolverá al usuario.</span><span class="sxs-lookup"><span data-stu-id="44bca-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="44bca-125">Recuperar entradas</span><span class="sxs-lookup"><span data-stu-id="44bca-125">Recall entries</span></span>
<span data-ttu-id="44bca-126">En algún punto, es posible que deba recuperar una entrada enviada.</span><span class="sxs-lookup"><span data-stu-id="44bca-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="44bca-127">Si la entrada no se ha aprobado, se devolverá de inmediato.</span><span class="sxs-lookup"><span data-stu-id="44bca-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="44bca-128">Sin embargo, una entrada aprobada puede tener un impacto material.</span><span class="sxs-lookup"><span data-stu-id="44bca-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="44bca-129">Se requiere que el aprobador del proyecto apruebe la recuperación para revertir la transacción en datos reales.</span><span class="sxs-lookup"><span data-stu-id="44bca-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="44bca-130">Especificar aprobadores de proyecto</span><span class="sxs-lookup"><span data-stu-id="44bca-130">Specify Project approvers</span></span>
<span data-ttu-id="44bca-131">Cada proyecto tiene varios miembros del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="44bca-131">Each project has a number of project team members.</span></span> <span data-ttu-id="44bca-132">Puede especificar qué miembros del equipo son también aprobadores de proyectos.</span><span class="sxs-lookup"><span data-stu-id="44bca-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="44bca-133">Vaya al formulario **Proyectos** y abra el proyecto en la lista.</span><span class="sxs-lookup"><span data-stu-id="44bca-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="44bca-134">En la pestaña **Equipo**, seleccione el miembro del equipo que será aprobador del proyecto y luego seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="44bca-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="44bca-135">Establezca el campo **Aprobador de proyecto** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="44bca-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="44bca-136">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="44bca-136">Select **Save**.</span></span>
5. <span data-ttu-id="44bca-137">Para agregar más aprobadores de proyectos, repita los pasos 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="44bca-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="44bca-138">Configurar el administrador de usuarios</span><span class="sxs-lookup"><span data-stu-id="44bca-138">Configure the user's manager</span></span>

1. <span data-ttu-id="44bca-139">Vaya a **Configuración** > **Seguridad** > **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="44bca-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="44bca-140">Seleccione el usuario al que le está asignando un administrador y en el área **Información de la organización**, seleccione el administrador de la lista.</span><span class="sxs-lookup"><span data-stu-id="44bca-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="44bca-141">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="44bca-141">Select **Save**.</span></span>


