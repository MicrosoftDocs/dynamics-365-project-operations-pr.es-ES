---
title: Novedades o cambios en la versión de actualización 26, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 26, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948845"
---
# <a name="project-service-automation-update-release-26-v3"></a>Versión de actualización de Project Service Automation 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 26, V3. Esta versión tiene un número de compilación de V3.10.44.59 y es de lanzamiento público mediante una actualización automática desde diciembre de 2020.

## <a name="update-release-26"></a>Versión de actualización 26

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Los usuarios pueden cambiar la tarea en una entrada de tiempo que haya sido aprobada o enviada.
- Error "Referencia de objeto no establecida" al guardar la entrada de tiempo.
- La importación de entradas de tiempo desde asignaciones de recursos crea entradas de tiempo con valores de DateTime incorrectos.
- Cuando se instalan Project Service Automation y la aplicación Field Service, el botón **Nuevo** se muestra dos veces en la barra de comandos para las entradas de tiempo en la aplicación Field Service.
- Las actualizaciones de celdas de **Permitir unidad** y **Unidad de venta** ahora trabajan de la cuadrícula **Estimaciones de gastos**.
- El formulario **Actualizar edición de entrada de tiempo** incluye **Escala de tiempo**.
- La aprobación de tiempo para entradas de tiempo que no sean del proyecto bloquea el sistema al buscar un rol de aprobador de proyectos.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- Validación agregada en el complemento **PostProjectCreate** para comprobar si hay un requisito principal antes de crear uno.
- El formulario de creación rápida **Miembro del equipo del proyecto** genera una excepción de referencia nula si los campos se eliminan del formulario.
- Se producirá un error en la generación de requisitos durante 12 horas durante 1 año.
- Se ha mejorado la excepción de referencia nula del mensaje de error durante la creación de requisitos de recursos.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Validación mejorada para abordar la excepción de referencia nula generada en el complemento **PreProjectUpdate**.
- Los proyectos publicados por el complemento de escritorio de Microsoft Project eliminan las asignaciones no asignadas.
- Se agregó una nueva validación cuando la referencia del proyecto de una tarea no es válida debido a una excepción de referencia nula en el complemento **PreValidateProjectTaskUpdate**.
- La cuadrícula Miembro del equipo no muestra asignaciones distintas en el registro de miembros del equipo.
- Se agregaron nuevos mensajes de validación y error debido a una excepción de referencia nula en el complemento **PreProjectTaskDelete**.

**Sales**

Se han solucionado los siguientes problemas:

- Al seleccionar una línea basada en proyecto en la oferta o el contrato, el botón **Sugerencia** solo debe estar visible al seleccionar una línea basada en producto asociada a un producto existente.
- Dividir el privilegio **Create_Product** desde el privilegio **Create_ProjectContract**.
- La eliminación de una línea de factura provoca una error de referencia nula en **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]