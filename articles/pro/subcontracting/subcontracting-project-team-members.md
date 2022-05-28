---
title: Miembros del equipo del proyecto de subcontratación
description: Este tema explica cómo subcontratar miembros del equipo del proyecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587883"
---
# <a name="subcontracting-project-team-members"></a>Miembros del equipo del proyecto de subcontratación

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

En Microsoft Dynamics 365 Project Operations, puede optar por subcontratar a miembros del equipo del proyecto sin personal o con personal.

- Los miembros del equipo del proyecto sin personal tienen asignado un recurso genérico.
- Los miembros del equipo dotados de personal tienen asignado un recurso con nombre.

Cuando vincula a un miembro del equipo del proyecto a una línea de subcontrato, cualquier asignación a tareas que tenga el miembro del equipo se calculará según la lista de precios de compra adjunta al subcontrato.  Sobre la pestaña **Estimaciones** de la página **Detalles del proyecto**, seleccione **Actualizar precios** para ver precios y/o costos actualizados como resultado de la decisión de subcontratar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación de un miembro del equipo del proyecto sin dotación de personal
La página **Detalles del miembro del equipo** tiene campos de línea de subcontrato y subcontrato que permiten al gerente de proyecto expresar cómo le gustaría obtener la capacidad requerida de un subcontrato. Para subcontratar a un miembro del equipo del proyecto como recurso genérico, siga estos pasos:

1.  Elija un subcontrato en la página **Detalle del miembro del equipo**.

2.  Solo puede seleccionar subcontratos con estado **Borrador** o **Confirmado**. Los subcontratos **Cerrado** o **Cancelado** no se pueden seleccionar. 

3.  El campo **Línea de subcontrato** se vuelve visible después de seleccionar un subcontrato.

4.  En el campo **Línea de subcontrato** solo puede seleccionar líneas de subcontrato que sean por tiempo. No puede seleccionar líneas de subcontrato para gastos o material.

5.  El rol para el registro de miembros del equipo del proyecto debe coincidir con el rol en la línea de subcontrato. Esto asegura que el tiempo para el rol que se estima en el proyecto sea el mismo que se compra en la línea de subcontrato. 

Cuando un miembro del equipo genérico está asociado con un subcontrato y una línea de subcontrato, el campo **Tipo de trabajador** de la fila de miembros del equipo genérico se actualizará a **Trabajador contratado** y **Validez del subcontrato** se establecerá en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación de un miembro del equipo del proyecto con dotación de personal
Al igual que los miembros del equipo genéricos o sin personal, la capacidad de los miembros del equipo con personal requerida en un proyecto también se puede vincular a un subcontrato. Para subcontratar a un miembro del equipo del proyecto con nombre, siga estos pasos:

1.  Asegúrese de que el recurso nombrado esté configurado como un tipo de recurso reservable de trabajador contratado. Además, asegúrese de que el campo **Vendedor** del recurso que se puede reservar coincide con el proveedor del subcontrato que está seleccionando. 

2.  Solo puede seleccionar subcontratos en estado **Borrador** o **Confirmado**. Los subcontratos **Cerrado** o **Cancelado** no se pueden seleccionar. 

3.  El campo **Línea de subcontrato** se vuelve visible después de seleccionar un subcontrato.

4.  En el campo **Línea de subcontrato** solo puede seleccionar líneas de subcontrato que sean por tiempo. No puede seleccionar líneas de subcontrato para gastos o material.

5.  El rol para el registro de miembros del equipo del proyecto debe coincidir con el rol en la línea de subcontrato. Esto asegura que el tiempo para el rol que se estima en el proyecto sea el mismo que se compra en la línea de subcontrato. 

Miembros del equipo del proyecto con nombre que se configuran como un tipo de trabajador por contrato **Recurso reservable** se mostrará con un estado de validez de subcontrato de **No es válido** si no están vinculados a un subcontrato. Cuando un miembro del equipo del proyecto con nombre está asociado con un subcontrato y una línea de subcontrato, el campo **Tipo de trabajador** de la fila de miembros del equipo se actualizará a **Trabajador contratado** y **Validez del subcontrato** se establecerá en **Válido**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
