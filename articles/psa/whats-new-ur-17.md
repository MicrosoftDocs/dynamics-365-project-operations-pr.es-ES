---
title: Novedades o cambios en la versión de actualización 17, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 17, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949250"
---
# <a name="project-service-automation-update-release-17-v3"></a>Versión de actualización de Project Service Automation 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.  Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 17. Esta versión tiene un número de compilación de V3.10.6.34 y está disponible con carácter general a través de una actualización automática en marzo de 2020.


## <a name="update-release-17"></a>Versión de actualización 17

### <a name="bug-fixes"></a>Solución de errores

**Generales**

- Corregido: Actualizar Project Service Automation para que se apliquen las licencias de Team Member (el Centro de recursos de proyecto incluirá metadatos del plan de Team Member Service 3.x)
 
**Tiempo y gasto**

- Corregido: No es posible cambiar una estimación de gastos a partir de un precio distinto de cero a cero (0). Se omite el cambio.

**Administración del proyecto**

- Corregido: Se ha agregado una comprobación para valores nulos en el nombre de puesto de un miembro del equipo.
- Corregido: El campo **msdyn_userresourceid** de la entidad **msdyn_resourceassignment** ha quedado en desuso.
- Corregido: Actualizar de 2.x a 3.x ahora maneja los contornos de esfuerzo vacíos en las asignaciones de tareas.

**Sales**

- Corregido: **Invoice.PreValidateInvoiceUpdate** ahora controla el escenario de la reasignación de propietarios de registros de manera adecuada.
- Corregido: Cuando la clase de transacción es **Hora**, **UnitGroup** es no editable para todas las entidades, incluyendo, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** y **ContractLineDetails**. Sin embargo, **Unidad** es no editable solo para **JournalLine** y **FacturaLíneaDetalles**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]