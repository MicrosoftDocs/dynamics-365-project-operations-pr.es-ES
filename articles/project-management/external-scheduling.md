---
title: Programación externa
description: En este artículo se proporciona información sobre la programación externa.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736973"
---
# <a name="external-scheduling"></a>Programación externa

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

El modo de programación externa le permite crear, actualizar y eliminar de forma nativa entidades relacionadas con estructuras de descomposición del trabajo (WBS), pero sin los límites actuales que impone Microsoft Project for the Web. También proporciona una validación limitada. Este modo debe ser utilizado únicamente por los siguientes clientes:

- Clientes que tienen las herramientas necesarias para definir una WBS fuera de la lógica de programación proporcionada por Project Operations
- Clientes que tienen que administrar la jerarquía de horarios, las dependencias o la duración de las tareas

> [!IMPORTANT]
> Es posible que los datos que no se ingresan correctamente en las entidades relacionadas con la WBS no se representen en la cuadrícula de reconciliación de recursos, la cuadrícula de estimaciones, la cuadrícula de seguimiento o la cuadrícula de asignación de recursos.

## <a name="configuration"></a>Configuration

Esta característica está habilitada de manera predeterminada. Sin embargo, en la página principal lista para usar para proyectos, el campo relacionado no está visible de forma predeterminada. Para habilitar el campo, en Maker Portal, abra la página principal de la entidad del proyecto, seleccione el campo **Motor de programación** y luego cambie el campo a **Visible por defecto**. Si no usa la página principal del proyecto lista para usar, edite su página existente y agréguele el campo **Motor de programación**.

## <a name="settings"></a>Configuración

Para usar el modo de programación externa, primero debe crear un nuevo proyecto y seleccionar el motor de programación **Programado externamente** en la lista desplegable de la página principal del proyecto. Después de configurar este modo para un proyecto, no se puede cambiar.

## <a name="viewing-the-wbs"></a>Visualización de la EDT

Si un proyecto está programado externamente, el acceso a Project for the Web está restringido para ese proyecto. Para ver la EDT, debe ir a la cuadrícula de seguimiento, donde se muestra la EDT completa.

## <a name="creating-and-editing-the-wbs"></a>Crear y editar el WBS

Si la programación externa está habilitada para un proyecto, debe definir los datos para todas las entidades relacionadas con la EDT, incluidas las tareas, los miembros del equipo, las asignaciones de recursos y las dependencias.

La ilustración siguiente muestra el modelo de datos para planificación del proyecto.

![Modelo de datos de planificación de proyectos.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitaciones funcionales

Las siguientes operaciones no están permitidas en proyectos programados externamente.

### <a name="project-planning"></a>Planificación del proyecto

- **Copiar proyecto** – Esta operación no se admite en proyectos programados externamente.
- **Mover proyecto** – Los cambios en la fecha de inicio de un proyecto no moverán el inicio de tareas o asignaciones de recursos en la EDT.
- **Actualización del administrador de proyectos** – Los cambios en el administrador del proyecto en la página principal del proyecto no crearán automáticamente un nuevo miembro del equipo del proyecto hasta que el proyecto se haya convertido.
- **Actualización de la plantilla de horas de trabajo del proyecto** – Los cambios en la plantilla de horas de trabajo del proyecto no volverán a calcular la programación del proyecto.
- **Contornos de asignación de recursos** – La creación de asignaciones de recursos no actualizará automáticamente el campo **mdyn\_PlannedWork**. Este campo se utiliza para almacenar contornos para el esfuerzo de asignación de recursos. Si muestra el esfuerzo por fases en la cuadrícula de asignación de recursos o la cuadrícula de reconciliación de recursos, debe definir contornos de asignación de recursos válidos. Estos contornos deben tener el formato correcto para que activen el cálculo de contornos de costos y contornos de precios de venta. Le recomendamos que cree un proyecto de prueba programado por Project for the Web y luego revise los datos asociados para confirmar los requisitos y el formato.

### <a name="resource-management"></a>Administración de recursos

- **Cumplimiento de recursos genéricos** – El cumplimiento de recursos genéricos no es compatible con proyectos programados externamente. Los intentos de cumplir con los requisitos abiertos activos crearán nuevos miembros del equipo del proyecto, pero no eliminarán el miembro del equipo genérico ni reemplazarán al miembro del equipo genérico en las asignaciones de recursos existentes.
- **Eliminar miembro del equipo** – La eliminación de un miembro del equipo no eliminará automáticamente las asignaciones de recursos.

### <a name="quoting-and-contracting"></a>Cotización y contratación

- **Importación de detalles de Línea de cotización y Línea de contrato** – Cuando se importan detalles de línea de cotización o contrato de un proyecto, la aplicación se ha probado para admitir un máximo de solo 500 tareas en WBA, según un límite de 20 asignaciones por tarea.

### <a name="actuals-and-invoicing"></a>Datos reales y facturación

- Aunque no hay cambios en las validaciones existentes entre la EDT y las transacciones financieras, es importante que se ajuste al modelo de datos listo para usar, para asegurarse de que todas las transacciones posteriores se ejecuten como se esperaba.
