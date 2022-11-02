---
title: Seguridad y aprobaciones
description: Este artículo proporciona información sobre la configuración de seguridad para el trabajo con aprobaciones en Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709419"
---
# <a name="security-and-approvals"></a>Seguridad y aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Microsoft Dynamics 365 Project Operations utiliza dos roles de seguridad para permitir la aprobación de entradas de tiempo, gastos y materiales:

- Aprobador de proyecto
- Administrador aprobador de proyecto

## <a name="project-approver"></a>Aprobador de proyecto

Debes tener el rol de seguridad **Aprobador del proyecto** para aprobar las entradas de tiempo, gastos y materiales del proyecto. También debe tener acceso a las entidades relacionadas pertinentes, como **Proyecto**. Ese acceso puede ser asignado por alguien que tenga el rol **Gerente de proyecto**. Además, debe ser miembro del equipo del proyecto y estar marcado como aprobador.

Para aprobar entradas que no sean de proyectos, debe ser el administrador del remitente.

## <a name="project-approver-admin"></a>Administrador aprobador de proyecto

> [!NOTE]
> La característica [Conjuntos de aprobación](approval-sets.md) debe estar habilitada antes de poder usar la función de administrador aprobador de proyectos.

El rol de seguridad **Administrador aprobador de proyectos** permite a los usuarios eludir políticas y permite la aprobación de entradas en todos los proyectos. La asignación de este rol omitirá la lógica de validación que requiere ser miembro del equipo y estar marcado como aprobador. Debe tener acceso a las tablas relacionadas pertinentes, como **Proyecto**, a través de los roles de seguridad que se le han asignado.

El contexto de usuario del SISTEMA omite las validaciones de la misma manera que el administrador aprobador del proyecto rol de seguridad.
