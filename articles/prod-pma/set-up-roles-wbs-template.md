---
title: Configurar roles en plantillas de estructura de descomposición del trabajo
description: Este tema proporciona información sobre cómo configurar información de roles en las plantillas de estructura de descomposición del trabajo.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997622"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurar roles en plantillas de estructura de descomposición del trabajo

[!include [banner](../includes/banner.md)]

Los jefes de proyecto pueden configurar plantillas de estructura de descomposición del trabajo (WBS) que pueden aplicar cuando crean una WBS para nuevos proyectos. Los jefes de proyecto pueden agregar roles cuando crean una plantilla. Utilice el siguiente procedimiento para asignar un rol a una plantilla WBS.

1. Seleccione **Gestión de proyectos y contabilidad** > **Configuración** > **Proyectos** > **Plantillas de estructura de descomposición del trabajo**.
2. Seleccione **Detalles** para una plantilla WBS seleccionada.
3. Seleccione una tarea en la lista y luego, en el campo **Rol**, seleccione un rol para asignar a la tarea.

## <a name="work-with-a-wbs"></a>Trabajar con una WBS

Puede crear una nueva WBS o puede copiar una WBS de una plantilla de WBS existente. Un jefe de proyecto puede administrar fácilmente los recursos asignando roles a nuevas tareas en la WBS. Los roles se pueden reemplazar después de adquirir un recurso o después de identificar un recurso confirmado para trabajar en la tarea. Esta flexibilidad permite a los jefes de proyecto realizar las siguientes tareas:

- Identificar la cantidad de recursos que se requieren para los paquetes de trabajo de WBS.
- Calcular los costes del proyecto.
- Determinar un presupuesto preliminar.
- Estimar la duración de la actividad, según los roles y los recursos.
- Desarrollar algunos planes de gestión de proyectos, basados en la información disponible del proyecto.

Se han agregado opciones adicionales en la WBS para utilizar mejor la funcionalidad de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Asignaciones de recursos</td>
<td>Consulte los recursos asignados, las fechas, la cantidad de horas y el tipo de reserva para las tareas en la WBS.</td>
</tr>
<tr class="even">
<td>Equipo de generación automática</td>
<td>Agregue automáticamente recursos planificados utilizando roles asociados con una tarea. Finance sugiere automáticamente los recursos planificados mediante el uso de análisis de decisiones de criterios múltiples que se basan en roles. Una vez que se hayan establecido los roles y el esfuerzo (horas) para las tareas en una WBS, y después de que se haya liberado la estructura, seleccione <strong>Equipo de generación automática</strong>. La cantidad requerida de recursos planificados se agrega a la WBS y la pestaña <strong>Programación de proyectos y equipos</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista desplegable)</td>
<td>En la página <strong>Lanzar asignación de recursos</strong>, puede seleccionar recursos para la reserva manual o automática, según la duración especificada. Puede ajustar la configuración de la vista para ver y establecer la duración de las actividades de los recursos. Puede seleccionar y asignar recursos a nivel de paquete de trabajo mediante las siguientes opciones:
<ul>
<li><strong>Aceptar</strong> : confirmar cambios en el recurso asignado a una tarea.</li>
<li><strong>Cancelar</strong> : cancelar cambios en el recurso asignado a una tarea.</li>
<li><strong>Asignar automáticamente</strong>: un recurso de personal disponible que tiene un rol coincidente se selecciona y asigna automáticamente a la tarea seleccionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.
2. Seleccione **Plan** > **Actividades** > **Estructura de descomposición del trabajo**.
3. Seleccione **Nuevo** para agregar las siguientes actividades de nivel uno a la WBS:

    - Iniciación
    - Planificación
    - Ejecutando
    - Supervisión y control
    - Cerrada

4. Configure las fechas y el esfuerzo (horas), como se muestra en la siguiente ilustración.

    [![Configuración de las fechas y el esfuerzo](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccione la línea de tarea **Iniciando** y, luego, en el campo **Rol**, seleccione **Jefe de proyectos sénior**.
6. Seleccione **Publish**.
7. En la misma línea, en el campo **Recurso**, seleccione **Daniel Goldschmidt** y luego seleccione **Aceptar**.
8. Seleccione la línea de tarea **Planificación** y luego, en el campo **Rol**, seleccione **Analista de negocios**.
9. Seleccione **Publicar** y luego seleccione **Equipo de generación automática**.
10. En el cuadro mensaje que aparece, seleccione **Sí**.
11. En el campo **Recurso**, verifique que el valor sea **Analista de negocios 1**.
12. Para el recurso **Analista de negocios 1**, abra la búsqueda y seleccione **Lanzar asignaciones de recursos**. Luego seleccione un trabajador para la tarea.
13. Seleccione **Asignación automática** &gt; **Capacidad completa**.

    > [!NOTE] 
    > No recibe una advertencia de que el recurso especificado ahora es 2, porque la cantidad de recursos sigue siendo 1.

14. En la página **Estructura de descomposición del trabajo**, valide la asignación de recursos en la WBS y luego seleccione **Guardar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]