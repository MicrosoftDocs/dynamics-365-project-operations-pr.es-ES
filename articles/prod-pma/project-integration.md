---
title: Integración Microsoft Project Client
description: La planificación y el mantenimiento del programa de un proyecto pueden ser complejos, por lo que los jefes de proyectos deben usar herramientas que les ayuden a administrar esta tarea. La integración con Microsoft Project Client brinda soporte para abrir y administrar una estructura de desglose del trabajo del proyecto.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289345"
---
# <a name="microsoft-project-client-integration"></a>Integración Microsoft Project Client

[!include [banner](../includes/banner.md)]

La planificación y el mantenimiento del programa de un proyecto pueden ser complejos, por lo que los jefes de proyectos deben usar herramientas que les ayuden a administrar esta tarea. La integración con Microsoft Project Client brinda soporte para abrir y administrar una estructura de desglose del trabajo del proyecto. El director del proyecto puede volver a publicar cualquier cambio en la estructura de descomposición del trabajo de Dynamics 365 Finance.

> [!NOTE]
> Si está utilizando la actualización de julio (versión 10.0.4), debe instalar KB 4054797 y 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurar el complemento de Microsoft Project Client
Para habilitar la integración con Microsoft Project Client, es encesario instalar un complemento de Microsoft Dynamics 365 en la aplicación cliente del usuario de Microsoft Project. Esto se hace abriendo el **Espacio de trabajo de gestión de proyectos**.

• Haga clic en **Configurar el complemento de cliente del proyecto** en la sección **Vínculos** > **Configuración** del espacio de trabajo.

• Haga clic en **Abrir** y luego en **Ejecutar** cuando se le solicite.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Abrir y editar una estructura de descomposición del trabajo en Microsoft Project Client
Si un proyecto en Dynamics 365 Finance ya tiene una estructura de desglose de trabajo creada, la estructura de descomposición del trabajo se puede abrir en la aplicación Microsoft Project Client si la estructura de descomposición del trabajo está en un estado de borrador. Para abrir desde la página **Proyecto**, haga clic en el vínculo **Abrir en Microsoft Project** desde la pestaña **Plan**. Esta página también se puede abrir desde la aplicación Microsoft Project Client haciendo clic en **Abrir** en la pestaña **Microsoft Dynamics 365**. Seleccione **Entidad jurídica** y **Proyecto** desde la lista.

> [!NOTE]
> Si está usando Internet Explorer como su explorador, deberá hacer clic en **Guardar** para abrir manualmente desde la ubicación en la que se descargó el archivo. O haga clic en **Guardar y abrir** para abrir el archivo en Microsoft Project Client. No cambie el nombre del archivo al guardar.

Antes de realizar modificaciones en el archivo con Microsoft Project Client, debe verificarlo. Haga clic **Comprobar** en la pestaña **Microsoft Dynamics 365**. Esto evitará que otros usuarios editen la estructura de descomposición del trabajo desde Finance al mismo tiempo. Para publicar la estructura de descomposición del trabajo después de completar cualquier edición, haga clic en **Registrarse** en la pestaña **Microsoft Dynamics 365**.

Si ya se ha agregado un equipo de proyecto al proyecto en Finance, la lista de recursos se completará con los miembros del equipo. Si aún no se ha agregado un equipo de proyecto al proyecto, puede seleccionar recursos y crear el equipo dentro de Microsoft Project Client haciendo clic en el botón **Recursos** en la pestaña **Microsoft Dynamics 365**. 

Los siguientes datos se sincronizarán con Finance como parte del proceso de registro:

• Nombre de la tarea

• Fecha de inicio

• Fecha de finalización

• Predecesoras

• Nombre de recurso

• Categoría

• Categoría de recurso

• Horas laborables

• Notas

• Prioridad

> [!NOTE]
> Si agrega otras columnas a su archivo de Microsoft Project Client, no se guardarán en el archivo y no se mostrarán cuando el archivo se abra nuevamente.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Crear la estructura de descomposición del trabajo para un proyecto existente utilizando Microsoft Project Client
Para crear una estructura de descomposición del trabajo nueva para un proyecto existente utilizando Microsoft Project Client, siga estos pasos:


1.  Abra Microsoft Project Client.

2.  En la pestaña **Microsoft Dynamics 365**, haga clic en **Abrir**.

3.  Seleccione la **Entidad jurídica** para el proyecto.

4.  Seleccione el **Proyecto**.

5.  Haga clic en **Comprobar** en la pestaña **Microsoft Dynamics 365**.

6.  Cuando esté listo para publicar en Finance, haga clic en **Registrarse** en la pestaña **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Sustituir la estructura de descomposición del trabajo existente para un proyecto existente utilizando Microsoft Project Client
Para crear una nueva estructura de descomposición del trabajo con Microsoft Project Client y reemplazar una estructura de descomposición del trabajo existente para un proyecto existente, siga estos pasos:

1.  Abra Microsoft Project Client.

2.  Cree el programa en Microsoft Project Client.

3.  En la pestaña **Microsoft Dynamics 365**, haga clic en **Guardar cambios** > **Reemplazar proyecto existente**.

4.  Seleccione la **Entidad jurídica** para el proyecto.

5.  Seleccione el **Proyecto**.

6.  Haga clic en **Aceptar**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Cree un nuevo proyecto desde Microsoft Project Client


1.  Abra Microsoft Project Client.

2.  Cree el programa en Microsoft Project Client.

3.  En la pestaña **Microsoft Dynamics 365**, haga clic en **Guardar cambios** > **Guardar en nuevo proyecto**.

4.  Seleccione la **Entidad jurídica** para el proyecto.

5.  Especifique **Id. del proyecto**, si necesario.

6.  Especifique el **Nombre del proyecto**.

7.  Seleccione **Tipo de proyecto**, **Grupo de proyecto** e **Id. del contrato del proyecto**. Alternativamente, puede crear un nuevo contrato de proyecto haciendo clic en **Nuevo**.

8.  Selecciona el **Calendario** que se va a utilizar para dotar de recursos.

11. Haga clic en **Aceptar**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]