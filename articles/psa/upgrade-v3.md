---
title: 'Consideraciones sobre actualizaciones: Microsoft Dynamics 365 Project Service Automation versión 2.x o 1.x a versión 3'
description: En este tema se proporciona información sobre las consideraciones que debe tomar cuando actualiza de la versión 2.xo 1.x a la versión 3 de Project Service Automation.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ae6aa3ef6a14a6f85dce3eaa5af01e0adce9ba
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014915"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Consideraciones de actualización: De la versión 2.x o 1.x a la versión 3.x

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation y Field Service
Tanto Dynamics 365 Project Service Automation como Dynamics 365 Field Service usan la solución Universal Resourcing Scheduling (URS) para la programación de recursos. Si tiene Project Service Automation y Field Service en su instancia, actualice ambas soluciones a la versión más reciente. En el caso de Project Service Automation, es la versión 3.x. Para Field Service, es la versión 8.x. La actualización de Project Service Automation o Field Service instalará la versión más reciente de URS. Si no se actualizan las soluciones de Project Service Automation y Field Service de la misma instancia a la versión más reciente, pueden producirse comportamientos incoherentes.

## <a name="resource-assignments"></a>Asignaciones de recursos
En las versiones 2 y 1 de Project Service Automation, las asignaciones de tareas se almacenaron como tareas secundarias (también llamadas tareas de línea) en la entidad **Entidad de tarea** e indirectamente relacionadas con la entidad **Asignación de recursos**. La tarea de línea era visible en la ventana emergente de asignación en la estructura de descomposición del trabajo (WBS).

![Tareas de línea en la WBS en Project Service Automation versión 2 y versión 1](media/upgrade-line-task-01.png)

En la versión 3 de Project Service Automation, ha cambiado el esquema subyacente de asignación de recursos reservables a tareas. . La tarea de línea ha quedado en desuso y existe una relación directa 1:1 entre la tarea en la entidad **Tarea** y el miembro del equipo en la entidad **Asignación de recursos**. Las tareas que se asignan a un miembro del equipo del proyecto ahora se almacenan directamente en la entidad Asignación de recursos.  

Estos cambios afectan la actualización de cualquier proyecto existente que tenga asignaciones de recursos para recursos que se pueden reservar con nombre y recursos genéricos en un equipo de proyecto. Este tema proporciona las consideraciones que deberá tener en cuenta para sus proyectos cuando actualice a la versión 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tareas asignadas a recursos con nombre
Mediante la entidad de tarea subyacente, las tareas en la versión 2 y la versión 1 permitían a los miembros del equipo representar un rol distinta del definido de forma predeterminada. Por ejemplo, Eva Martínez, que de forma predeterminada tiene asignada el rol de Administrador de programas, podría asignarse a una tarea con el rol de Desarrollador. En la versión 3, el rol de un miembro del equipo con nombre es siempre el predeterminado, por lo que cualquier tarea a la que se le asigne Eva Martínez utilizará su rol predeterminado de Administrador de programas.

Si ha asignado un recurso a una tarea fuera de su rol predeterminado en la versión 2 y la versión 1, cuando actualice, el recurso con nombre tendrá asignado el rol predeterminado para todas las asignaciones de tareas, independientemente de la asignación de roles en la versión 2. Esta asignación generará diferencias en las estimaciones calculadas de la versión 2 o la versión 1 a la versión 3, ya que las estimaciones se calculan en función del rol del recurso y no de la asignación de tareas de línea. Por ejemplo, en la versión 2, se han asignado dos tareas a Carmen Linares. El rol en la tarea de línea para la tarea 1 es Desarrollador y, para la tarea 2, Administrador de programas. Carmen Linares tiene el rol predeterminado de Administrador del programa.

![Varios roles asignados a un recurso](media/upgrade-multiple-roles-02.png)

Debido a que los roles de Desarrollador y Administrador del programa son diferentes, las estimaciones de costes y ventas son las siguientes:

![Estimaciones de costes para roles de recursos](media/upggrade-cost-estimates-03.png)

![Estimaciones de ventas para roles de recursos](media/upgrade-sales-estimates-04.png)

Cuando actualiza a la versión 3, las tareas de línea se reemplazan por asignaciones de recursos en la tarea del miembro del equipo de recursos que se puede reservar. La asignación utilizará el rol predeterminado del recurso que se puede reservar. En el siguiente gráfico, Carmen Linares, que tiene un rol de Administrador del programa, es el recurso.

![Asignaciones de recursos](media/resource-assignment-v2-05.png)

Debido a que las estimaciones se basan en el rol predeterminado del recurso, las estimaciones de ventas y costes pueden cambiar. En el siguiente gráfico ya no verá el rol **Desarrollador**, ya que ahora el rol se toma del rol predeterminado del recurso que se puede reservar.

![Estimaciones de costes para roles predeterminados.](media/resource-assignment-cost-estimate-06.png)
![Estimación de ventas para roles predeterminados](media/resource-assignment-sales-estimate-07.png)

Una vez completada la actualización, puede editar el rol de un miembro del equipo para que sea distinto del predeterminado asignado. Sin embargo, si cambia el rol de un miembro del equipo, se cambiará en todas sus tareas asignadas, ya que en la versión 3 ya no se pueden asignar varios roles a miembros de equipo.

![Actualización de un rol de recurso](media/resource-role-assignment-08.png)

Esto también se cumple con las tareas de línea que se asignaron a recursos con nombre cuando cambia la unidad organizativa del recurso de la predeterminada a otra unidad organizativa. Una vez completada la actualización de la versión 3, la asignación utilizará la unidad organizativa predeterminada del recurso en lugar de la establecida en la tarea de línea.

### <a name="tasks-assigned-to-generic-resources"></a>Tareas asignadas a recursos genéricos
En la versión 2 y la versión 1, puede establecer el rol y la unidad organizativa en una tarea y luego usar la característica **Generar equipo** para generar recursos genéricos basados en los atributos establecidos en la tarea. En la versión 3, cree los miembros genéricos del equipo con rol y unidad organizativa y, a continuación, asigne los miembros del equipo a las tareas.

En la versión 2 y 1, los proyectos con recursos genéricos pueden estar en dos estados, o una combinación de ambos a nivel de tarea. Por ejemplo, puede tener los siguientes escenarios. Por ejemplo, pueden darse los siguientes escenarios:

- Tareas con roles y unidades organizativas establecidas, pero sin que se genere ninguna asignación de recursos afiliados.
- Tareas con asignaciones de recursos de miembros de equipo genéricos que se asignaron creando recursos genéricos mediante la característica **Generar equipo**.

Antes de comenzar con la actualización, le recomendamos que vuelva a generar el equipo para cada proyecto que tenga tareas asignadas a recursos genéricos o que no haya ejecutado aún el proceso de generación de equipo en ellos.

Para las tareas asignadas a los miembros genéricos del equipo que se generaron con **Generar equipo**, la actualización dejará el recurso genérico en el equipo y la asignación a ese miembro genérico del equipo. Le recomendamos que genere los requisitos de recursos para el miembro del equipo genérico después de la actualización, pero antes de reservar o enviar una solicitud de recursos. Esto conservará cualquier asignación de unidad organizativa en los miembros genéricos del equipo que sea diferente de la unidad organizativa contratante del proyecto.

Por ejemplo, en el proyecto Project Z, la unidad organizativa contratante es Contoso Estados Unidos. En el plan del proyecto, a las tareas de prueba dentro de la fase de Implementación se les ha asignado el rol de Consultor técnico y la unidad organizativa asignada es Contoso India.

![Asignación de la organización de la fase de implementación](media/org-unit-assignment-09.png)

Después de la fase de implementación, la tarea de prueba de integración se asigna al rol de Consultor técnico, pero la organización se establece en Contoso Estados Unidos.  

![Asignación de organización de tarea de prueba de integración](media/org-unit-generate-team-10.png)

Cuando genere un equipo para el proyecto, se crearán dos miembros genéricos del equipo debido a las diferentes unidades organizativas en las tareas. El consultor técnico 1 tendrá asignadas las tareas de Contoso India y el consultor técnico 2 tendrá las tareas de Contoso Estados Unidos.  

![Miembros del equipo genéricos generados](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> En la versión 2 y 1 de Project Service Automation, el miembro del equipo no posee la unidad organizativa, que se mantiene en la tarea de línea.

![Tareas de línea de versión 2 y 1 en Project Service Automation](media/line-tasks-12.png)

Puede ver la unidad organizativa en la vista de estimaciones. 

![Estimaciones de unidad organizativa](media/org-unit-estimates-view-13.png)
 
Cuando se completa la actualización, la unidad de organización en la tarea de línea que corresponde al miembro del equipo genérico se agrega al miembro del equipo genérico y se elimina la tarea de línea. Por eso, recomendamos que antes de actualizar, genere o vuelva a generar el equipo en cada proyecto que contenga recursos genéricos.

Para las tareas que se asignan a un rol con una unidad organizativa distinta de la unidad organizativa del proyecto contratante, y sin un equipo, generado la actualización creará un miembro genérico del equipo para el rol, pero utilizará la unidad contratante del proyecto para la unidad organizativa del miembro del equipo. Volviendo al ejemplo con el Proyecto Z, esto significa que la unidad organizativa contratante Contoso Estados Unidos, y las tareas de prueba del plan del proyecto dentro de la fase de implementación tienen asignado el rol de Consultor técnico con la unidad organizativa asignada a Contoso India. La tarea de prueba de integración que se completa después de la fase de implementación se ha asignado al rol de Consultor técnico. La unidad organizativa es Contoso Estados Unidos y no se ha generado un equipo. La actualización creará un miembro genérico del equipo, un consultor técnico que tendrá las horas asignadas de las tres tareas y una unidad organizativa de Contoso Estados Unidos, la unidad organizativa contratante del proyecto.   
 
El cambio del valor predeterminado de las diferentes unidades organizativas de recursos en los miembros del equipo no generados es la razón por la que recomendamos que genere o vuelva a generar el equipo en cada proyecto que contenga recursos genéricos antes de la actualización de manera que las asignaciones de unidades organizativas no se pierdan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]