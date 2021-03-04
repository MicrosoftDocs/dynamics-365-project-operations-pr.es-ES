---
title: Crear un equipo de proyecto
description: En este tema se proporciona información sobre cómo crear y gestionar equipos de proyecto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085313"
---
# <a name="create-a-project-team"></a>Crear un equipo de proyecto

[!include [banner](../includes/banner.md)]

Para utilizar los roles que se configuraron previamente en un proyecto, un jefe de proyecto debe asociar los roles con el proyecto. Se pueden asignar varios roles a un proyecto. Para evitar confusiones, estos roles se etiquetan automáticamente durante la reserva. Por ejemplo, si el jefe de proyecto requiere tres ingenieros de software, se generan automáticamente tres roles de ingeniero de software que tengan **ingeniero de software 1** , **ingeniero de software 2** e **ingeniero de software 3** como sus etiquetas. Si las características del rol se establecieron previamente para el rol, se aplican como filtro durante las búsquedas de un recurso. Se pueden agregar características adicionales según sea necesario para refinar aún más la búsqueda.

La configuración de visualización también se puede personalizar para ofrecer una mejor visión de la disponibilidad de recursos. Hay opciones para mostrar la disponibilidad horaria, diaria, semanal, mensual, trimestral y anual. También hay una opción para mostrar la capacidad disponible y restante en los recursos. Esta opción es útil para la administración del tiempo, cuando tiene previsto tener tiempo disponible para actividades o disponibilidad de recursos.

El jefe de proyecto puede seleccionar un rol en la página y luego, si hay un recurso disponible que se ajuste al requisito, seleccionar reservar un recurso para llenar el rol. Tenga en cuenta que no es necesario reservar los recursos en este punto de la etapa de planificación. Cuando crea una WBS, puede reemplazar roles con recursos de personal para el proyecto. Si los roles se reemplazan con recursos de personal en la WBS, la configuración de recursos actualiza automáticamente la lista y la programación del equipo del proyecto.

[![Listado del equipo del proyecto que incluye tanto roles como recursos reales](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

El jefe de proyecto tiene varias opciones para reservar un recurso para un proyecto, como **Capacidad restante** , **Capacidad completa** , **Porcentaje de capacidad** y **Especificar horas**. Estas opciones de reserva se pueden cancelar en cualquier momento si cambian las asignaciones de recursos. Se admiten dos tipos de reserva:

- **Reserva manual** : la reserva de recursos fue aprobada y confirmada para trabajar en la interacción por la duración especificada.
- **Reserva automática** : las reservas de recursos se configuró provisionalmente para trabajar en la interacción por la duración especificada.

El proceso siguiente explica cómo crear un equipo de proyecto.

## <a name="create-a-project-team"></a>Crear un equipo de proyecto

1. En la página de lista **Todos los proyectos** , seleccione un proyecto y luego seleccione **Editar**.
2. En la pestaña **Equipo de proyecto y programación** , en el campo **Programar fecha de finalización** , especifique la fecha de inicio del programa más un mes. Por ejemplo, si la fecha de inicio del programa es el 24 de junio de 2017 (24/06/2017), especifique **24/07/2017**.
3. Seleccione **Agregar**.
4. En el panel **Agregar roles al proyecto** , en el campo **Rol** , seleccione **Jefe de proyectos sénior**.
5. Seleccione **Competencias requeridas**.
6. En la página **Elegir características** , las características que estableció previamente para el rol de jefe de proyecto sénior están seleccionadas de manera predeterminada. Seleccione **Aceptar**.
7. En la página **Agregar roles al proyecto** , en el campo **Cantidad de recursos** , especifique **1**.
8. En el campo **Recurso** , la búsqueda muestra todos los recursos que tienen las competencias requeridas. Seleccione **Daniel Goldschmidt** y, a continuación seleccione **Crear**.
9. En la página **Proyecto** , seleccione **Agregar**.
10. En el panel **Agregar roles al proyecto** , en el campo **Rol** , seleccione **Miembro del equipo**. En el campo **Número de recursos** , indique **5**.
11. Seleccione **Crear**.
12. En la página **Proyectos** , seleccione **Ejecutar recurso**.

## <a name="monitor-project-teams"></a>Supervisar equipos de proyectos
1. En la página **Todos los proyectos** , seleccione vínculo **Id. de proyecto** para el proyecto **Fase 2 de la actualización XYZ**.
2. En la ficha desplegable **Equipo de proyecto y programación** , verifique que los recursos del proyecto que se enumeran sean correctos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]