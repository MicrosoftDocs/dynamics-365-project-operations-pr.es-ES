---
title: Espacio de trabajo móvil de entrada de tiempo del proyecto
description: En este tema se proporciona información sobre el espacio de trabajo móvil Entrada de tiempo del proyecto. Este espacio de trabajo permite a los usuarios especificar y ahorrar tiempo en un proyecto mediante el uso de su dispositivo móvil.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756018"
---
# <a name="project-time-entry-mobile-workspace"></a>Espacio de trabajo móvil de entrada de tiempo del proyecto

[!include [banner](../includes/banner.md)]

En este tema se proporciona información sobre el espacio de trabajo móvil **Entrada de tiempo del proyecto**. Este espacio de trabajo permite a los usuarios especificar y ahorrar tiempo en un proyecto mediante el uso de su dispositivo móvil.

Este espacio de trabajo móvil está diseñado para utilizarse con la aplicación móvil de operaciones unificadas de Dynamics 365. 

## <a name="overview"></a>Información general
Como parte de su trabajo diario, los recursos del proyecto a menudo se encuentran en el sitio o están en movimiento. El espacio de trabajo **Entrada de tiempo del proyecto** permite a los usuarios especificar su tiempo facturable o no facturable respecto a un proyecto en el dispositivo móvil de su elección. Por lo tanto, los recursos del proyecto pueden registrar entradas de tiempo en cualquier momento y lugar. También pueden ver las entradas de tiempo que ya se han registrado. 

Específicamente, en el espacio de trabajo móvil **Entrada de tiempo del proyecto**, los usuarios pueden realizar estas tareas:

-   Para cualquier fecha seleccionada, especifique la cantidad de horas que dedicó a una tarea específica.
-   Busque por nombre de proyecto o cliente para encontrar el proyecto para el cual especificar el tiempo.
-   Especifique la categoría y la actividad para el tiempo que invirtió.
-   Registre el tiempo como facturable o no facturable para el proyecto.
-   Opcionalmente, especifique cualquier comentario externo o interno.

## <a name="prerequisites"></a>Requisitos previos
Los requisitos previos varían según la versión de Microsoft Dynamics 365 que se haya implementado en la organización.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisitos previos si usa Dynamics 365 Finance
Si se ha implementado Finance para la organización, el administrador del sistema debe publicar el espacio de trabajo para dispositivos móviles **Entrada de tiempo del proyecto**. Para obtener instrucciones, consulte [Publicar espacios de trabajo para dispositivos móviles](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Requisitos previos si usa la versión 1611 con Platform update 3 o posterior
Si se implementó la versión 1611 con Platform update 3 o posterior para su organización, el administrador del sistema debe completar los siguientes requisitos previos. 

<table>
<thead>
<tr class="header">
<th>Requisito previo</th>
<th>Rol</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementar KB 4018050.</td>
<td>Administrador del sistema</td>
<td>KB 4018050 es una actualización de X++ o revisión de metadatos que contiene el espacio de trabajo para dispositivos móviles <strong>Entrada de tiempo del proyecto</strong>. Para implementar KB 4018050, su administrador del sistema debe seguir estos pasos.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Descargue la revisión de metadatos de Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instale la revisión de metadatos</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Cree un paquete que se pueda implementar</a> que contiene los modelos <strong>ApplicationSuite</strong> y <strong>ProjectMobile</strong> y luego cargue el paquete que se puede implementar en LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Aplique el paquete que se puede implementar</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publique el espacio de trabajo para dispositivos móviles <strong>Entrada de tiempo del proyecto</strong>.</td>
<td>Administrador del sistema</td>
<td>Consulte <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicar espacios de trabajo para dispositivos móviles</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Descargar e instalar la aplicación móvil

Descargar e instalar la aplicación móvil Finance and Operations:

-   [Para teléfonos Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar sesión en la aplicación móvil
1.  Inicie la aplicación en el dispositivo móvil.
2.  Introduzca la URL de Dynamics 365.
3.  La primera vez que inicie sesión, se le solicitará su nombre de usuario y contraseña. Especifique sus credenciales.
4.  Después de iniciar sesión, se muestran los espacios de trabajo disponibles para su empresa. Tenga en cuenta que si el administrador del sistema publica un nuevo espacio de trabajo más tarde, deberá actualizar la lista de espacios de trabajo para dispositivos móviles.

[![Deslizar para actualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Especificar el tiempo utilizando el espacio de trabajo para dispositivos móviles Entrada de tiempo del proyecto
1.  En su dispositivo móvil, seleccione el espacio de trabajo **Entrada de tiempo del proyecto**.
2.  Seleccione **Entrada de tiempo**. Se muestran las fechas del calendario de la semana actual.
3.  Para una fecha seleccionada, seleccione **Acciones** &gt; **Nueva entrada**.
4.  Escriba el número de horas que desea registrar.
5.  Seleccione el proyecto para la entrada de horas. Una lista muestra los proyectos que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, consulte [Plataforma para dispositivos móviles](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Si su proyecto no está en la lista, seleccione **Buscar**. Busque por nombre o cambie para buscar por nombre de proyecto o cliente.
7.  Seleccione una categoría. Una lista muestra las categorías que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, consulte [Plataforma para dispositivos móviles](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Si su categoría no está en la lista, seleccione **Buscar**. Busque por categoría o cambie para buscar por nombre de categoría.
9.  Seleccione una actividad. Una lista muestra las actividades que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, consulte [Plataforma para dispositivos móviles](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Si su actividad no está en la lista, seleccione **Buscar**. Busque por número de actividad o cambie para buscar por propósito.

11. Seleccione la propiedad de línea.
12. Opcionalmente: especifique cualquier comentario externo e interno.
13. Seleccione **Listo**.