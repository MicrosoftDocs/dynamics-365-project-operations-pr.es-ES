---
title: Flujo de trabajo de gestión de gastos
description: Este tema explica cómo puede usar el sistema de flujo de trabajo en Microsoft Dynamics 365 Finance para configurar un proceso de revisión para los informes de gastos en la Gestión de gastos.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960583"
---
# <a name="expense-management-workflow"></a>Flujo de trabajo de gestión de gastos

Puede usar el sistema de flujo de trabajo en para configurar un proceso de revisión para los informes de gastos en la Gestión de gastos. Puede configurar un flujo de trabajo que utilice los siguientes criterios para determinar quién aprueba los informes de gastos:

- La jerarquía de informes de los empleados y los límites de aprobación predefinidos
- Aprobación de varios niveles que admite aprobadores interinos y un aprobador final
- Dimensiones financieras y responsabilidad del proyecto
- Asignación a usuarios o grupos de usuarios específicos

Se pueden crear aprobaciones de flujo de trabajo para informes de gastos, solicitudes de viaje, adelantos en efectivo y recuperación del impuesto al valor agregado (IVA).

**Ejemplo**

El siguiente proceso es un ejemplo del flujo de trabajo de gestión de gastos para un informe de gastos.

1. Un empleado crea y guarda un informe de gastos.
2. El empleado envía el informe de gastos para su aprobación. El aprobador se identifica según las reglas que se definieron cuando se configuró el flujo de trabajo.
3. El aprobador recibe una notificación de que un informe de gastos está listo para su aprobación. El aprobador revisa el informe de gastos y verifica que se cumplan las siguientes condiciones:

    - Los gastos no violan ninguna política de gastos. Si un gasto viola una directiva, el aprobador verifica que el informe de gastos incluya una justificación comercial válida.
    - Los recibos electrónicos se adjuntan al informe de gastos.

4. El aprobador aprueba el informe de gastos.
5. El informe de gastos se asigna al coordinador de proveedores para su contabilización.
6. Se produce uno de los siguientes pasos, dependiendo de si la publicación automática está configurada:

    - Si se configura la contabilización automática, el informe de gastos se procesa para el pago y se actualiza el estado del informe de gastos.
    - Si la contabilización automática no está configurada, el coordinador de proveedores verifica que se hayan enviado todos los recibos originales y que los recibos estén alineados con los gastos del informe de gastos. Todos los códigos de impuestos que se introducen en el informe de gastos también deben verificarse como correctos.

Una vez verificados estos requisitos, se contabiliza el informe de gastos.

Una vez que se contabiliza el informe de gastos, se autoriza el pago del informe de gastos y se reembolsa al empleado.
