---
title: Crear un proyecto
description: En este tema se proporciona información sobre cómo crear un proyecto nuevo.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270744"
---
# <a name="create-a-new-project"></a>Crear un proyecto

[!include [banner](../includes/banner.md)]

Para crear un nuevo proyecto, siga los pasos que se indican a continuación.

1. En la página **Gestión de proyectos**, seleccione **Nuevo proyecto**, e indique los valores siguientes:

    - **Tipo de proyecto**: Tiempo y material
    - **Nombre del proyecto**: Fase 2 de la actualización XYZ
    - **Grupo de proyecto**: TM\_WIP
    - **Id. de contrato de proyecto**: 00000002

2. Seleccione **Crear proyecto**.

## <a name="assign-a-resource-to-a-project"></a>Asignar un recurso a un proyecto

1. En la página **Trabajadores**, en la lista **Trabajadores**, seleccione el registro del trabajador para el que definió las competencias anteriormente y abra el registro del trabajador.
2. En el panel de acciones, en la pestaña **Proyecto**, en el grupo **Configurar**, seleccione **Asignar proyectos**.
3. En la página **Asignaciones de proyectos de validación de recursos**, en la pestaña **Proyectos**, en el campo **Agregar el proyecto a los proyectos seleccionados**, filtrar en el proyecto **Fase 2 de la actualización XYZ**.
4. En el panel **Proyectos restantes**, seleccione un proyecto y luego seleccione el botón de flecha para agregarlo al panel **Proyectos seleccionados**.

También puede asignar categorías para un recurso según lo requiera. El tipo de categoría es **Coste** o **Ingresos**. El tipo de categoría lo determina su organización. Si no se asignan categorías para un recurso, Finance busca la categoría predeterminada en precios por hora para costes e ingresos.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurar las características de los roles y los recursos del proyecto

Un jefe de proyecto puede utilizar la funcionalidad de dotación de recursos de proyecto para crear los roles necesarios para el proyecto. Los roles se pueden usar si los recursos confirmados aún se desconocen cuando se reservan los recursos. Los roles se pueden reservar temporalmente como recursos planificados, para que pueda continuar con las etapas de planificación del proyecto.

[![Ejemplo de un rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenario**: Contoso fue contratado para completar un proyecto de tiempo y material que tiene un estado de proyecto aprobado. El jefe de proyecto junior aún está completando el alcance del proyecto. El administrador de recursos actualmente está identificando recursos específicos que se reservarán para trabajar en el nuevo proyecto. Debido a la naturaleza crítica del proyecto, el patrocinador del proyecto solicitó jefe de proyecto senior como uno de los roles. El administrador de recursos debe adquirir el nuevo recurso y definir el rol en el sistema en caso de que el jefe de proyectos junior requiera la información de recursos durante la planificación del proyecto.

Los siguientes pasos muestran cómo el administrador de recursos puede configurar el rol de jefe de proyectos senior y asociar características de recursos con él. Posteriormente, el rol se puede utilizar para buscar recursos disponibles que coincidan con las competencias de recursos requeridas.

1. En la página **Configurar roles**, seleccione **Nuevo**, e indique los valores siguientes:

    - **Id. del rol**: jefe de proyectos sénior
    - **Descripción**: jefe de proyectos sénior

2. Seleccione **Crear**.
3. Selecciona el rol **Jefe de proyectos sénior** y luego seleccione **Configurar características**.
4. En el campo **Tipo de característica**, seleccione **Aptitud**.
5. En el campo **Características disponibles**, indique la aptitud que desea buscar.
6. En el campo **Tipo de característica**, seleccione **Certificado**.
7. En el campo **Características disponibles**, indique el tipo de certificado que desea buscar.

## <a name="assign-a-project-resource-to-a-project"></a>Asignar un recurso de proyecto a un proyecto

1. En la página **Todos los proyectos**, seleccione el proyecto **Fase 2 de la actualización XYZ**.
2. En la pestaña **Equipo de proyecto y programación**, seleccione **Agregar**.
3. En el campo **Rol** campo, seleccione **Miembro del equipo**.
4. Seleccione **Reservar en el calendario**.
5. En la página **Disponibilidad de recursos**, seleccione **Ver configuraciones**.
6. En la página **Ajustar la configuración de la vista**, escriba los siguientes valores:

    - **Formato para la vista de rango de fechas**: Día
    - **Mostrar descripciones de disponibilidad**: Sí
    - **Mostrar capacidad restante**: Sí

7. En la lista de recursos, seleccione un recurso.
8. Seleccione **Reserva manual** y **Capacidad completa**.

## <a name="assign-a-resource-to-a-default-role"></a>Asignar un recurso a un rol predeterminado

Para ayudar a los administradores de proyectos o recursos pueden explorar en profundidad más sobre los recursos que se pueden reservar para un proyecto. Puede asociar un rol predeterminado con un recurso existente o un recurso recién adquirido. Por ejemplo, cuando contrataron a Daniel, tenía la experiencia y las aptitudes para ocupar el puesto de analista comercial. El administrador de recursos asignó este rol como el rol predeterminado de Daniel. Por lo tanto, el administrador de recursos agregó a Daniel a un grupo de analistas comerciales que están disponibles para trabajar en proyectos.

Durante la reserva de recursos, los jefes de proyecto pueden filtrar los recursos de roles que están disponibles para trabajar en proyectos. Pueden utilizar esta información como un criterio cuando realizan análisis de decisiones de criterios múltiples durante la ejecución de los recursos. También pueden agregar otras características de recursos al filtro para buscar recursos que tengan aptitudes, educación y experiencia específicas para un proyecto determinado.

**Escenario**: se ha iniciado un proyecto aprobado y se reservó el rol de jefe de proyecto sénior como recurso planificado durante la etapa de planificación del proyecto. El administrador de recursos ahora ha adquirido un recurso para ejecutar el rol de jefe de proyectos senior.

1. En la página **Lista de recursos**, seleccione **Daniel Goldschmidt**.
2. En la página **Rol del recurso**, seleccione **Nuevo**, e indique los valores siguientes:

    - **Vigencia a partir de**: indique la fecha actual.
    - **Vencimiento**: especificar **Nunca**.
    - **Rol**: especifique **Jefe de proyectos sénior**.

3. Seleccione **Guardar** y cierre la página.
4. En la pestaña **Competencias**, agregue la aptitud **ProjectMgmt** y el certificado **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]