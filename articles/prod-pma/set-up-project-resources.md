---
title: Configurar los recursos del proyecto
description: En este tema se proporciona información sobre configurar o solicitar recursos de proyecto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9af71fe0638a5601ded3f0e80301ae5dfa198c1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682612"
---
# <a name="set-up-project-resources"></a>Configurar los recursos del proyecto

[!include [banner](../includes/banner.md)]

Debe configurar un calendario y asociarlo con un empleado o un trabajador. El calendario se utiliza para programar el proyecto y el tiempo de trabajo de los recursos que están reservados para el proyecto. Durante la configuración del calendario, los administradores de proyectos pueden nivelar los recursos como parte de la optimización de los recursos. Según la programación del calendario, se pueden imponer restricciones a los recursos. Puede configurar un calendario en la página **Calendarios**.

Cuando configura un trabajador como recurso del proyecto, puede seleccionar entre los trabajadores que trabajan en la empresa para la que está configurando los recursos. Alternativamente, puede seleccionar trabajadores de otras empresas de su organización. Estos trabajadores se conocen como recursos de empresas vinculadas.

Los siguientes procedimientos explican cómo configurar un trabajador como recurso de proyecto en su empresa y cómo configurar un recurso de proyecto de empresas vinculadas.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un trabajador como recurso de proyecto

1. En la página **Trabajadores**, en lista **Trabajadores**, seleccione el trabajador que está agregando como recurso del proyecto y abra el registro del trabajador.
2. En el panel de acciones, seleccione **Proyecto** &gt; **Configurar** &gt; **Configuración del proyecto**.
3. Seleccione un calendario y cierre la página.

También puede especificar proyectos predeterminados para un recurso como un tipo de asignación previa. Las asignaciones previas se pueden usar cuando el administrador de recursos o el administrador de proyectos sepan con anticipación en qué proyectos trabajará el recurso. Las asignaciones previas también pueden basarse en la solicitud de un cliente o patrocinador del proyecto. Para asignar previamente un proyecto, en la página **Asignar proyectos**, en la pestaña **Proyectos**, en la lista **Proyectos restantes**, seleccione el proyecto apropiado.

## <a name="set-up-an-intercompany-resource"></a>Configurar un recurso de empresas vinculadas

Cuando configura un trabajador como recurso de empresas vinculadas, debe completar la configuración tanto en la empresa prestamista como en la empresa prestataria.

### <a name="in-the-lending-company"></a>En la empresa prestamista

1. En Finance, verifique que la empresa prestamista esté seleccionada y luego complete el procedimiento de la sección anterior, "Configurar un trabajador como recurso de proyecto".
2. En la página **Contabilidad de empresas vinculadas**, seleccione **+Nuevo**.
3. En el campo **Id. de entidad legal**, seleccione la empresa prestamista. Rellene los campos restantes como corresponda y seleccione **Guardar**.
4. En la página **Transferir precios**, seleccione **Nuevo**.
5. En el campo **Entidad legal prestataria**, seleccione la empresa apropiada.
6. Para prestar a la empresa prestataria solo el recurso que creó al principio de esta sección, en el campo **Recurso**, seleccione el nombre del recurso que creó. Para que todos los recursos de la empresa prestamista estén disponibles para la empresa prestataria, deje el campo **Recurso** en blanco.
7. En la página **Parámetros de gestión de proyectos y contabilidad**, en la pestaña **Empresas vinculadas**, establezca la opción **Habilitar la programación de recursos y las hojas de horas de empresas vinculadas** en **Sí**.

### <a name="in-the-borrowing-company"></a>En la empresa prestataria

- En la página **Lista de recursos**, en el filtro de búsqueda, especifique el nombre del recurso que creó para la empresa prestamista, para verificar que el nombre esté incluido en la lista de recursos para la empresa prestataria.

## <a name="request-project-resources"></a>Solicitar recursos del proyecto
La funcionalidad para la programación de recursos del proyecto solo permite a los administradores de recursos distribuir los recursos del personal en compromisos o proyectos. Para habilitar esta funcionalidad, complete las siguientes tareas o verifique que se hayan completado:

- Configurar las secuencias numéricas.
- Configurar los flujos de trabajo de gestión de proyectos y contabilidad.
- Habilite los flujos de trabajo de solicitud de recursos.

Una vez completadas las tareas anteriores, puede completar las siguientes tareas según sea necesario:

- Cree una solicitud de recurso a partir de un recurso con personal reservado temporalmente.
- Supervise solicitudes de recursos.
- Ejecute solicitudes de recursos.
- Solicite un recurso con personal de una WBS.
- Reserve recursos para un proyecto sin tener una solicitud de recursos con personal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]