---
title: Cambios de características para Project Service Automation en Project Operations
description: Este artículo proporciona una descripción general de los cambios de características para Microsoft Dynamics 365 Project Service Automation en Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621272"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Cambios de características para Project Service Automation en Project Operations

Después de que un proyecto se haya actualizado con éxito desde Microsoft Dynamics 365 Project Service Automation 3.X a Dynamics 365 Project Operations Lite, no es posible editar las tareas del proyecto en la estructura de desglose del trabajo (WBS) de la cuadrícula de tareas. Los clientes podrán revisar las EDT en la cuadrícula de seguimiento donde se agregaron nuevos campos para proporcionar todos los detalles relacionados con la tarea. Para los proyectos en los que se requieren ediciones en la EDT, puede convertir de forma selectiva los proyectos elegibles a la nueva experiencia de programación de Project for the web.

## <a name="project-conversion-process"></a>Proceso de conversión de proyectos

Para convertir un proyecto, siga estos pasos.

1. Abra la página principal del proyecto y seleccione **Convertir** en el Panel de acciones.
1. En el cuadro de mensaje de confirmación que aparece, seleccione **ACEPTAR** para confirmar la conversión de proyectos. Se producen las siguientes acciones:

    1. Una barra de mensajes que aparece en la página principal del proyecto dice: "El cronograma del proyecto se está convirtiendo. No puede realizar cambios en el proyecto hasta que se complete la conversión".
    1. Será redirigido a la lista de proyectos.

    Una vez completada la conversión del proyecto, se producen las siguientes acciones:

    1. El jefe de proyecto asignado recibe una notificación en el lado derecho de la aplicación.
    1. Se elimina la barra de mensajes que indica que la conversión está en curso.
    1. La pestaña **Calendario** muestra la nueva experiencia de programación con Project for the Web. Cualquier usuario que tenga las licencias y los roles de seguridad apropiados puede editar la EDT.
    1. El campo **Motor de programación** se actualiza a **Project for the web**.
    1. El botón **Convertir** se elimina del Panel de acciones.

> [!IMPORTANT]
> No se permite la conversión masiva de proyectos. Se limitará cualquier intento de actualizar un gran volumen de proyectos al mismo tiempo. Esta limitación ayuda a garantizar un alto rendimiento para todos los clientes.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tareas manuales frente a tareas automáticas

Cuando se actualiza un entorno de Project Service Automation a Project Operations, todas las tareas de la EDT se consideran programadas automáticamente. El concepto de tareas programadas manualmente no está disponible en Project for the web. Sin embargo, puede definir el comportamiento de programación preferido para sus proyectos utilizando la configuración del [modo de programación](/project-management/scheduling-modes.md) al crear nuevos proyectos.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operaciones restringidas para proyectos de preconversión

Esta sección describe las diferencias funcionales que puede esperar cuando los proyectos no se han convertido.

### <a name="copy-project"></a>Copiar proyecto

La operación **Copiar** solo se admite en proyectos convertidos. Los proyectos actualizados no se pueden copiar antes de la conversión.

### <a name="move-project"></a>Mover proyecto

Un cambio en la fecha de inicio de un proyecto no moverá proporcionalmente el inicio de las tareas a menos que el proyecto se haya convertido.

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>¿Cuáles son las diferencias entre los proyectos convertidos y los nuevos proyectos que se crean después de que se haya completado la actualización?

Para los proyectos que se convierten después de que se haya actualizado el entorno, se establecerá una bandera que le indicará al cronograma que respete solo el calendario del proyecto. Este comportamiento coincide con el comportamiento en Project Service Automation. Sin embargo, la marca no se establecerá para los nuevos proyectos que se creen después de la actualización. Por lo tanto, el cronograma respetará las horas de trabajo de los recursos cuando estén asignados a una tarea.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>¿Qué debo hacer si mi proyecto no se convierte?

Si su proyecto no se convierte, el primer paso es revisar los registros de errores para identificar cualquier problema común relacionado con su WBS. Si los registros no indican un error específico sobre el que pueda tomar medidas, comuníquese con Atención al cliente para que su caso pueda ser revisado más a fondo.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>¿Cómo se manejan los cierres de empresas en Project for the web?

Project for the web no respeta los cierres comerciales que la empresa define a nivel de organización. Sin embargo, respetará otros tipos de días libres que se definan en una determinada plantilla de horas de trabajo.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>¿Cuáles son las limitaciones de Project for the web?

Vea [Crear una estructura de descomposición del trabajo: limitaciones de proyecto](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>¿Puedo esperar cambios en mis estimaciones de costos y ventas?

En casos excepcionales en los que se recalculan los contornos de asignación de recursos, o en los que se encuentran en un límite de fecha diferente al del proyecto de origen, es posible que observe diferencias en las estimaciones de ventas y costos. Como parte del proceso de actualización, se espera que los clientes prueben una muestra representativa de proyectos, para que puedan comprender cualquier cambio potencial en el cronograma.
