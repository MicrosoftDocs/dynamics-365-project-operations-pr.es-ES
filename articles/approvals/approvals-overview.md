---
title: Información general de aprobaciones
description: Este tema proporciona información sobre cómo trabajar con aprobaciones en Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996722"
---
# <a name="approvals-overview"></a><span data-ttu-id="1d5fb-103">Información general de aprobaciones</span><span class="sxs-lookup"><span data-stu-id="1d5fb-103">Approvals overview</span></span>

<span data-ttu-id="1d5fb-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="1d5fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d5fb-105">Los envíos de tiempo, gastos y uso de materiales se desplazan en un flujo de trabajo de aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="1d5fb-106">Una vez aprobadas las entradas, las transacciones se registran en datos reales o el tiempo se registra en la programación.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="1d5fb-107">Flujo de trabajo de aprobación</span><span class="sxs-lookup"><span data-stu-id="1d5fb-107">Approvals workflow</span></span>
<span data-ttu-id="1d5fb-108">Cuando crea y envía una entrada de tiempo, gasto o uso de material, se crea un registro de aprobación.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="1d5fb-109">El aprobador o administrador del proyecto revisa y aprueba la entrada.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="1d5fb-110">Si la entrada está relacionada con un proyecto, los datos reales se crearán cuando se apruebe.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="1d5fb-111">Esto permite realizar un seguimiento del coste y la facturación.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="1d5fb-112">Aprobar una entrada</span><span class="sxs-lookup"><span data-stu-id="1d5fb-112">Approve an entry</span></span>
<span data-ttu-id="1d5fb-113">La página **Aprobaciones** le permite cambiar entre diferentes vistas para que pueda ver los diferentes tipos de aprobaciones.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="1d5fb-114">Vaya a la página **Aprobaciones** y seleccione **Gastos**, **Hora**, **Uso de material**, o **Retiradas**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="1d5fb-115">Revise cada aprobación y seleccione las que desea aprobar.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="1d5fb-116">Seleccione **Aprobar** para aprobar las entradas seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="1d5fb-117">El sistema procesa estas entradas y crea datos reales.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="1d5fb-118">Rechazar una entrada</span><span class="sxs-lookup"><span data-stu-id="1d5fb-118">Reject an entry</span></span>
<span data-ttu-id="1d5fb-119">Como aprobador del proyecto, es posible que deba enviar una entrada a un usuario para que la corrija.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="1d5fb-120">Vaya a la página **Aprobaciones** y seleccione la entrada que desee rechazar.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="1d5fb-121">Seleccione **Rechazar**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-121">Select **Reject**.</span></span>
3. <span data-ttu-id="1d5fb-122">Opcionalmente, puede agregar un comentario en el cuadro de diálogo **Comentarios de rechazo** para informar al usuario de por qué se rechaza la entrada.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="1d5fb-123">Seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-123">Select **OK**.</span></span> <span data-ttu-id="1d5fb-124">La entrada se devolverá al usuario.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="1d5fb-125">Cancelar aprobación</span><span class="sxs-lookup"><span data-stu-id="1d5fb-125">Cancel approval</span></span>
<span data-ttu-id="1d5fb-126">En algunos casos, es posible que deba cancelar una entrada aprobada previamente.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="1d5fb-127">Cancelar una entrada previamente aprobada tendrá un impacto financiero.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="1d5fb-128">Aprobación solicitudes de retirada</span><span class="sxs-lookup"><span data-stu-id="1d5fb-128">Approving recall requests</span></span>
<span data-ttu-id="1d5fb-129">En algunos casos, es posible que un consultor necesite recuperar una entrada aprobada previamente.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="1d5fb-130">Cancelar una entrada previamente aprobada tendrá un impacto financiero.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="1d5fb-131">Se requiere que el aprobador del proyecto apruebe la retirada para revertir la transacción en Datos reales.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="1d5fb-132">Especificar aprobadores de proyecto</span><span class="sxs-lookup"><span data-stu-id="1d5fb-132">Specify Project approvers</span></span>
<span data-ttu-id="1d5fb-133">Cada proyecto tiene varios miembros del equipo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-133">Each project has a number of project team members.</span></span> <span data-ttu-id="1d5fb-134">Puede especificar qué miembros del equipo son también aprobadores de proyectos.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="1d5fb-135">Vaya a la página **Proyectos** y abra el proyecto en la lista.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="1d5fb-136">En la pestaña **Equipo**, seleccione el miembro del equipo que será aprobador del proyecto y luego seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="1d5fb-137">Establezca el campo **Aprobador de proyecto** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="1d5fb-138">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-138">Select **Save**.</span></span>
5. <span data-ttu-id="1d5fb-139">Para agregar más aprobadores de proyectos, repita los pasos 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="1d5fb-140">Configurar el administrador de usuarios</span><span class="sxs-lookup"><span data-stu-id="1d5fb-140">Configure the user's manager</span></span>

1. <span data-ttu-id="1d5fb-141">Vaya a **Configuración** > **Seguridad** > **Usuarios**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="1d5fb-142">Seleccione el usuario al que le está asignando un administrador y en el área **Información de la organización**, seleccione el administrador de la lista.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="1d5fb-143">Seleccione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1d5fb-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
