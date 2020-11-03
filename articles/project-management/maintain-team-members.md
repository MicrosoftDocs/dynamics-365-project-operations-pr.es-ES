---
title: Mantener miembros del equipo
description: En este tema se proporciona información sobre cómo reservar recursos con nombre para equipos de proyectos y asignarlos a tareas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085014"
---
# <a name="maintain-team-members"></a>Mantener miembros del equipo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede agregar un recurso con nombre a su equipo de proyecto reservándolo directamente para el equipo.

1. En Dynamics 365 Project Operations, vaya a **Proyectos** y seleccione el proyecto abierto para el que desea reservar.
2. En la página **Proyecto** , en la pestaña **Equipo** , seleccione **Nuevo**. 
3. En el cuadro de diálogo **Creación rápida: Miembro del equipo del proyecto** , seleccione el recurso reservable. El campo **Rol** se completará con el rol predeterminado del recurso si tiene alguno asignado. Puede cambiar el rol. 
4. Seleccione las fechas de inicio y finalización en que será necesario el recurso y seleccione el método de asignación de capacidad del recurso. 
5. En el campo **Aprobador de proyecto** , seleccione **Sí** en caso de que desee que el miembro del equipo sea aprobador de proyecto. El miembro del equipo puede aprobar las entradas de gastos y de tiempo enviadas para este proyecto. 
6. Seleccione **Guardar**.

Ahora puede asignar el recurso reservado a las tareas del proyecto. En la página **Proyecto** , en la pestaña **Programación** , asigne tareas al nuevo recurso. El selector de recursos que se inicia desde el campo **Recursos** de la cuadrícula de tareas mostrará los miembros de equipo que se pueden seleccionar.


En Operaciones de proyectos, las reservas de recursos y las asignaciones de tareas no están estrechamente relacionadas. Al usar el selector de recursos en la programación, puede asignar tareas a los miembros del equipo por más horas de las que cubren sus reservas en el proyecto.

Las diferencias entre las reservas y las asignaciones de los miembros del equipo se muestran en las pestañas **Equipo** y **Recursos**. También puede conciliar las diferencias entre las reservas y las asignaciones de recursos a un nivel más detallado.

Use el selector de recursos de la pestaña **Programación** para buscar y seleccionar recursos reservables que ya no formen parte del equipo del proyecto. Estos recursos se muestran en el selector de recursos como **Otros recursos**.

Al realizar una selección, el recurso se agrega al equipo del proyecto y se asigna a la tarea, pero no se genera ninguna reserva.

Puede usar la capacidad de ampliación de reserva de la pestaña **Reconciliación** o el **Tablero de programación** para reservar la capacidad del recurso para el proyecto.

Tras reservar un miembro de equipo en su proyecto, podrá usar **Mantener reservas** o **Panel de programación** directamente para administrar las reservas.
