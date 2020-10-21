---
title: Informes de gastos y múltiples aprobadores
description: En este tema se proporciona información sobre los informes de gastos que requieren la aprobación de más de una persona.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897112"
---
# <a name="expense-reports-and-multiple-approvers"></a>Informes de gastos y múltiples aprobadores

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado. Cuando configura el proceso de flujo de trabajo para la aprobación del informe de gastos, puede agregar elementos del flujo de trabajo que incluyen tareas o pasos para uno o más aprobadores de informes de gastos. Por ejemplo, es posible que requiera que todos los informes de gastos sean aprobados por dos personas distintas, el gerente del empleado que envió el informe y el coordinador de proveedores.

Si decide requerir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo de cualquiera de las siguientes formas:

- Agregue un elemento de aprobación que tenga un paso. Por ejemplo, es posible que el paso requiera que se asigne un informe de gastos a un grupo de usuarios y que sea aprobado por el 50 por ciento de los miembros del grupo de usuarios.
- Agregue un elemento de aprobación que tenga varios pasos. Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:

    1. El gerente del empleado que envió el informe de gastos lo aprueba.
    2. El empleado del departamento de proveedores verifica los recibos y los elementos del informe de gastos.
    3. El propietario del presupuesto aprueba el informe de gastos.

- Agregue varios elementos de aprobación, cada uno de los cuales tiene un paso. Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:

    1. El gerente del empleado aprueba el informe de gastos.
    2. El propietario del presupuesto aprueba el informe de gastos.
