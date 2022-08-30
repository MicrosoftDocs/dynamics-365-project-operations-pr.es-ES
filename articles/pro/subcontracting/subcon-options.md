---
title: Opciones de subcontratación para miembros del equipo del proyecto
description: Este artículo explica las opciones de subcontratación para los miembros del equipo del proyecto en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261628"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opciones de subcontratación para miembros del equipo del proyecto

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

En Microsoft Dynamics 365 Project Operations, puede evaluar las opciones de subcontratación disponibles para uno o más miembros del equipo del proyecto. Las siguientes opciones de subcontratación están disponibles para usted:

- Cree un nuevo subcontrato y / o cree nuevas líneas en un subcontrato existente para los miembros del equipo del proyecto seleccionados. 
- Reserve un subcontrato y una línea de subcontratación existentes. 

Puede elegir entre las opciones de subcontratación disponibles para los miembros genéricos del equipo del proyecto o elegir entre los miembros del equipo del proyecto que han sido dotados de un recurso con nombre que es un trabajador contratado. 

No hay opciones de subcontratación disponibles para lo siguiente:

- Miembros del equipo del proyecto que han sido dotados de un empleado. 
- Miembros del equipo que ya están asociados a un subcontrato y línea de subcontratación. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontratación de un miembro del equipo del proyecto sin dotación de personal

Para revisar y elegir entre las opciones de subcontratación disponibles para un miembro del equipo del proyecto genérico o sin personal, siga estos pasos:

1. Seleccione uno o más registros de miembros del equipo del proyecto donde el recurso es un recurso genérico.
2. Asegúrese de que ninguno de los registros de los miembros del equipo del proyecto seleccionados ya esté subcontratado. 
3. Seleccione **Opciones de subcontratación** en la subcuadrícula de miembros del equipo del proyecto. Se abrirá el cuadro de diálogo **Opciones de subcontratación**. 
4. Si solo seleccionó un registro de miembro del equipo del proyecto en el paso 1, estarán disponibles las siguientes opciones:
    - Crear nuevas líneas de subcontratación. 
    - Reservar contra un subcontrato existente Si seleccionó varios registros de miembros del equipo del proyecto en el paso 1, la única opción disponible es crear una nueva línea de subcontrato.
5. La opción de reservar contra una línea de subcontrato existente le permite seleccionar un subcontrato y una línea de subcontrato que desea reservar. Al seleccionar una línea de subcontrato para reservar capacidad, debe asegurarse de que la línea de subcontrato seleccionada sea por tiempo y que el rol requerido en el miembro del equipo del proyecto coincida con el rol que se compró en la línea de subcontrato.
6. Cuando seleccione crear nuevas líneas de subcontrato para los miembros del equipo del proyecto, el sistema le permitirá seleccionar el subcontrato para el que desea crear estas líneas. El subcontrato que seleccione para crear nuevas líneas debe estar en estado **Borrador**. Con esta opción para crear nuevas líneas de subcontrato para los miembros del equipo del proyecto seleccionados, el sistema creará una línea de subcontrato por tiempo para cada miembro del equipo del proyecto. El rol, las horas y las fechas se copiarán del miembro del equipo del proyecto a cada línea de subcontrato que se cree. 
7. Cuando un miembro del equipo genérico está asociado con un subcontrato y una línea de subcontrato, el campo **Tipo de trabajador** de la fila de miembros del equipo genérico se actualizará a **Trabajador contratado** y el valor **Validez del subcontrato** se establecerá en **Válido**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontratación de un miembro del equipo del proyecto con dotación de personal

Al igual que los miembros del equipo genéricos o sin personal, también puede ver las opciones de subcontratación para un miembro del equipo del proyecto con personal siempre que el miembro del equipo con personal sea un trabajador contratado. Para revisar y elegir entre las opciones de subcontratación disponibles para un miembro del equipo del proyecto con personal o con nombre, siga estos pasos:

1. Seleccione uno o más registros de miembros del equipo del proyecto donde el recurso es un trabajador con contrato con nombre.
2. Asegúrese de que ninguno de los registros de los miembros del equipo del proyecto seleccionados ya esté subcontratado. 
3. Seleccione **Opciones de subcontratación** en la subcuadrícula de miembros del equipo del proyecto. Se abrirá el cuadro de diálogo **Opciones de subcontratación**. 
4. Si solo seleccionó un registro de miembro del equipo del proyecto en el paso 1, estarán disponibles las siguientes opciones:
      - Crear nuevas líneas de subcontratación.
      - Reservar un subcontrato existente.
  Si seleccionó varios registros de miembros del equipo del proyecto en el paso 1, la única opción disponible es crear una nueva línea de subcontrato.
5. La opción de reservar contra una línea de subcontrato existente le permite seleccionar un subcontrato y una línea de subcontrato que desea reservar. Al seleccionar una línea de subcontrato para reservar capacidad, debe asegurarse de lo siguiente:
      - La línea de subcontrato seleccionada es por tiempo. 
      - El rol requerido en el miembro del equipo del proyecto coincide con el rol que se adquirió en la línea de subcontrato. 
      - El proveedor al que está asociado el trabajador contratado es el mismo que el proveedor del subcontrato.
6. Cuando seleccione crear nuevas líneas de subcontrato para los miembros del equipo del proyecto, el sistema le permitirá seleccionar el subcontrato para el que desea crear estas líneas. Con esta opción, debería asegurarse de que el proveedor al que pertenece el trabajador contratado es el mismo que el proveedor del subcontrato. 
7. El subcontrato que seleccione para crear nuevas líneas debe estar en estado **Borrador**. Con esta opción para crear nuevas líneas de subcontrato para los miembros del equipo del proyecto seleccionados, el sistema creará una línea de subcontrato por tiempo para cada miembro del equipo del proyecto. El rol, las horas y las fechas se copiarán del miembro del equipo del proyecto a cada línea de subcontrato que se cree.  
8. Cuando un miembro del equipo con nombre está asociado con un subcontrato y una línea de subcontrato, el campo **Tipo de trabajador** de la fila de miembros del equipo con nombre se actualizará a **Trabajador contratado** y el valor **Validez del subcontrato** se establecerá en **Válido**.

## <a name="re-costing-subcontractor-assignments"></a>Volver a calcular los costos de las asignaciones de subcontratistas

Cuando un miembro del equipo del proyecto (genérico o nombrado) está vinculado a líneas de subcontrato utilizando el cuadro de diálogo **Opciones de subcontratación**, las asignaciones a las tareas que tiene el miembro del equipo se volverán a calcular según la lista de precios de compra adjunta al subcontrato. Sobre la pestaña **Estimaciones** de la página **Detalles del proyecto**, seleccione **Actualizar precios** para ver precios y/o costos actualizados como resultado de la decisión de subcontratar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
