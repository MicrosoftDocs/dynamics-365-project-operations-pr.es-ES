---
title: Informes de gastos y múltiples aprobadores
description: En este artículo se proporciona información sobre los informes de gastos que requieren la aprobación de más de una persona.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f42535e4826d1f618bd542eec3b26a6fde1a97
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914479"
---
# <a name="expense-reports-and-multiple-approvers"></a>Informes de gastos y múltiples aprobadores

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Según las directivas de aprobación de gastos de su organización, es posible que más de una persona tenga que aprobar un informe de gastos enviado. Cuando configure el proceso de flujo de trabajo para aprobar un informe de gastos, puede agregar elementos del flujo de trabajo que incluyan tareas o pasos para uno o varios aprobadores de informes de gastos. Por ejemplo, puede exigir que todos los informes de gastos sean aprobados por dos personas independientes, el jefe del empleado que envió el informe y el coordinador de proveedores.

Si decide exigir varios aprobadores de informes de gastos, puede agregar los elementos del flujo de trabajo según una de las formas que indicamos a continuación:

- Agregar un elemento de aprobación que tenga un paso. Por ejemplo, el paso puede requerir que se asigne un informe de gastos a un grupo de usuarios y que se exija la aprobación del 50 por ciento de los miembros del grupo de usuarios.
- Agregar un elemento de aprobación con varios pasos. Por ejemplo, el elemento de aprobación puede tener los siguientes pasos:

    1. El gerente del empleado que envió el informe de gastos lo aprueba.
    2. El empleado de Proveedores verifica los recibos y los elementos del informe de gastos.
    3. El propietario del presupuesto aprueba el informe de gastos.

- Agregar varios elementos de aprobación que tengan, cada uno de ellos, un paso. Por ejemplo, puede agregar un elemento de aprobación independiente para cada uno de los siguientes pasos:

    1. El gerente del empleado aprueba el informe de gastos.
    2. El propietario del presupuesto aprueba el informe de gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]