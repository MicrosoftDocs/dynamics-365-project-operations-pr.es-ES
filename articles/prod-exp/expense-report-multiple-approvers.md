---
title: Múltiples aprobadores en un informe de gastos
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de varias personas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960628"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Múltiples aprobadores en un informe de gastos

Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado por un empleado. Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos. Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados primero por el gerente del empleado que envió el informe y después el coordinador de proveedores.

Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:

- Agregue un elemento de aprobación que tenga un paso. Por ejemplo, es posible que el paso requiera que se asigne un informe de gastos a un grupo de usuarios y que sea aprobado por el 50 por ciento de los miembros del grupo de usuarios.
- Agregue un elemento de aprobación que tenga varios pasos. Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:

    1. El gerente del empleado que envió el informe de gastos lo aprueba.
    2. El empleado del departamento de proveedores verifica los recibos y los elementos del informe de gastos.
    3. El propietario del presupuesto aprueba el informe de gastos.

- Agregue varios elementos de aprobación, cada uno de los cuales tiene un paso. Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:

    1. El gerente del empleado aprueba el informe de gastos.
    2. El propietario del presupuesto aprueba el informe de gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]