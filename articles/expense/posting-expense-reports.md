---
title: Registrar informes de gastos
description: Este tema explica cómo registrar informes de gastos.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
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
ms.openlocfilehash: ec897373cd74f7d7f63cd9ca4c46f4245336eb7f
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907429"
---
# <a name="post-expense-reports"></a>Registrar informes de gastos

Una vez que se ha aprobado y transferido un informe de gastos al diario general, se puede registrar. Cuando publica un informe de gastos, se identifican los gastos que son idóneos para la recuperación del impuesto sobre el valor añadido (IVA). La tarea de verificar y recuperar los pagos del IVA se asigna al empleado que es responsable de verificar el informe de gastos.

Si los gastos de un informe de gastos se cargan a una empresa que no sea la empresa que emplea al empleado, debe verificar tanto la empresa a la que se le deben esos gastos como la empresa que los adeuda. Por ejemplo, el empleado que presentó un informe de gastos trabaja para la empresa DAT pero le cobró un gasto a la empresa DIR. En este caso, DAT es la empresa a la que se debe el gasto y DIR es la empresa que debe el gasto. Después de verificar estas líneas de diario, puede registrar las líneas de gastos en el libro mayor.

Para registrar un informe de gastos, en la página **Informes de gastos aprobados**, seleccione el informe de gastos y, a continuación, en el Panel de acciones, seleccione **Registrar**.

También puede registrar todos los informes de gastos de la lista al mismo tiempo. Seleccione todos los informes de gastos y luego seleccione **Registrar**.
