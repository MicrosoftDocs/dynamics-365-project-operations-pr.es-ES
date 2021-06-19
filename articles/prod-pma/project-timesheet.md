---
title: Aplicación móvil Project Timesheet
description: Este tema proporciona información sobre la aplicación para dispositivos móviles Microsoft Dynamics 365 Project Timesheet. La aplicación móvil Project Timesheet permite a los usuarios enviar y aprobar hojas de horas para proyectos en su dispositivo móvil.
author: abruer
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 517c6f2b749fa3ed44b198b799489e7e29e34d7f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009907"
---
# <a name="project-timesheet-mobile-application"></a>Aplicación móvil Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Información general

La aplicación móvil Microsoft Dynamics 365 Project Timesheet permite a los usuarios enviar y aprobar hojas de horas para proyectos en su dispositivo móvil (iPhone o Android). Esta aplicación móvil muestra la funcionalidad de la hoja de horas que reside en el área de contabilidad y gestión de proyectos de Dynamics 365 Finance, mejorando la productividad y la eficiencia de los usuarios, además de permitir la entrada y aprobación oportunas de las hojas de horas del proyecto.

## <a name="download-and-install-the-mobile-app"></a>Descargar e instalar la aplicación móvil

Descargue e instale la aplicación Microsoft Dynamics 365 Project Timesheet para Android o iPhone de la tienda móvil para su dispositivo.

## <a name="enable-the-app"></a>Habilitar la aplicación 

En Finance, la aplicación móvil Project Timesheet debe estar habilitada. Para habilitar la funcionalidad, vaya a **Parámetros de gestión de proyectos y contabilidad \> Hoja de horas** y seleccione el parámetro **Habilitar Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Iniciar sesión en la aplicación

1.  Inicie la aplicación en el dispositivo móvil.

2.  Escriba su URL de Finance.

3.  La primera vez que inicie sesión, se le solicitará su nombre de usuario y contraseña. Especifique sus credenciales.

4.  Se iniciará sesión en su empresa predeterminada.

## <a name="submit-a-project-timesheet"></a>Enviar una hoja de horas del proyecto

Puede crear y enviar una hoja de horas del proyecto en la aplicación. Puede basar una nueva hoja de horas en la información de una hoja de horas anterior, líneas guardadas o asignaciones de proyectos. Si se le ha designado como delegado, también puede especificar una hoja de horas para otro trabajador. Para crear una hoja de horas como delegado, seleccione el botón **Menú** y luego seleccione un nombre de recurso.

La página de la hoja de horas creará una nueva hoja de horas para el período de la hoja de horas, según la fecha actual. Aparecerá la semana de trabajo. Si el período de la hoja de horas cubre varias semanas, puede seleccionar otra semana laboral en las pestañas de semana laboral.
Si existe una hoja de horas para la fecha actual, se mostrará. Si necesita crear una nueva hoja de horas en un período de hoja de horas diferente, seleccione el botón **Menú** y luego seleccione **Nueva hoja de horas**.

Puede especificar la información del proyecto haciendo clic en la acción **Agregar tiempo** o la acción **Copiar tiempo desde**. La acción **Copiar tiempo desde** copiará la información de la línea del proyecto, pero no las horas. El menú **Copiar tiempo desde** incluye las siguientes opciones:

- **Copiar desde la hoja de horas existente**: copia las líneas de la hoja de horas de una hoja de horas existente.

- **Copiar desde favorito**: cree nuevas líneas de la hoja de horas utilizando la configuración de la hoja de horas que seleccionó como favorito.

- **Copiar desde la asignación**: crear nuevas líneas de horas trabajadas a partir de proyectos asignados.

La información del proyecto que se muestra depende de los parámetros móviles que definió en la página **Parámetros de gestión de proyectos y contabilidad**.

En el campo **Entidad jurídica**, seleccione la entidad jurídica para la que realizó el trabajo del proyecto. El campo **Entidad jurídica** está disponible solo si se ha habilitado la compatibilidad con la hoja de horas de empresas vinculadas para su entidad jurídica.

Seleccione el cliente asociado con el proyecto para la hoja de horas. Para el lanzamiento inicial en Android, no se admiten entradas por parte del cliente, ya que primero debe seleccionar el proyecto. Si seleccionó el proyecto primero, el campo **Cliente** se completa automáticamente.

En el campo **Proyecto**, seleccione el proyecto para el que está especificando tiempo. El campo **Cliente** se rellena automáticamente.

Las búsquedas de clientes y proyectos permiten realizar búsquedas tanto en clientes como en proyectos.

Seleccione información en los campos **Categoría**, **Actividad**, **Propiedad de línea**, **Grupo de impuestos** y **Grupo de impuestos de artículos** según sea necesario. Estos campos se pueden anular.

El campo **Propiedad de línea** se establecerá en un valor predeterminado, según los parámetros de contabilidad y gestión del proyecto. Cuando los parámetros de proyecto/categoría y categoría/recurso están habilitados, el valor **Propiedad de línea** se establecerá en el valor predeterminado que haya definido para esta validación. Cuando los parámetros de proyecto/categoría y categoría/recurso no están habilitados, el valor **Propiedad de línea** se establecerá en un valor predeterminado de acuerdo con el campo **Habilitar la propiedad de línea predeterminada** en la página **Parámetros contables y de gestión de proyectos**. El valor **Propiedad de línea** se puede anular.

Seleccione un día para agregar tiempo. Especifique la cantidad de horas que trabajó cada día.

Para agregar comentarios sobre las horas que está especificando, haga clic en **Añadir comentarios** y luego ingrese comentarios para una audiencia interna, una audiencia de cliente o ambas.
Los jefes de proyecto pueden ver los comentarios internos. Los comentarios de los clientes se incluyen en las facturas.

Para guardar la línea como favorita, seleccione la casilla de verificación y luego haga clic en **Guardar como favorito**.

La dimensión financiera y el soporte para archivos adjuntos no se proporcionan en la aplicación móvil.

Continúe agregando líneas de proyecto según sea necesario para completar su hoja de horas.

Haga clic en **Enviar** para enviar la hoja de horas al flujo de trabajo de aprobación.

## <a name="review-timesheets"></a>Revisar las hojas de horas

En el menú se encuentra disponible una lista de las hojas de horas que deben revisarse. Esta opción solo está disponible si ha sido designado como aprobador de flujo de trabajo. Se admiten tanto la aprobación de encabezado como de línea. La aprobación de nivel de línea ofrece la posibilidad de marcar una o más líneas para su aprobación. Después de revisar la información de la hoja de horas, haga clic en **Aprobar**, **Delegar** o **Regresar** para continuar con el flujo de trabajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]