---
title: Múltiples aprobadores en un informe de gastos
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de varias personas.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 383ce9eda6d0604ce0dd090e27a5c6fd569bd9e5
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685307"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Múltiples aprobadores en un informe de gastos

Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado por un empleado. Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos. Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados primero por el gerente del empleado que envió el informe y después el coordinador de proveedores.

Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:

- Agregar un elemento de aprobación que tenga un paso. Por ejemplo, el paso puede requerir que se asigne un informe de gastos a un grupo de usuarios y que se exija la aprobación del 50 por ciento de los miembros del grupo de usuarios.
- Agregar un elemento de aprobación con varios pasos. Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:

    1. El gerente del empleado que envió el informe de gastos lo aprueba.
    2. El empleado de Proveedores verifica los recibos y los elementos del informe de gastos.
    3. El propietario del presupuesto aprueba el informe de gastos.

- Agregar varios elementos de aprobación que tengan, cada uno de ellos, un paso. Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:

    1. El gerente del empleado aprueba el informe de gastos.
    2. El propietario del presupuesto aprueba el informe de gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]