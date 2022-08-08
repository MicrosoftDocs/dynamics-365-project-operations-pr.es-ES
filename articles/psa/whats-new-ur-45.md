---
title: Novedades o cambios en la versión de actualización 45, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 45, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169166"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novedades o cambios en la versión de actualización 45, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 45, V3. Esta versión tiene un número de compilación de V3.10.76.168 y generalmente está disponible a través de una actualización automática en julio de 2022.

## <a name="update-release-45"></a>Versión de actualización 45

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Ventas**

- Los usuarios no pueden crear facturas correctamente después de intentar crear una factura sin ventas no facturadas, si también están viendo la misma instancia de la página y no la actualizan.

**Tiempo y gasto**

- Cuando la opción Aprobaciones modernas está habilitada y se aprueba una aprobación de proyecto recuperada, la fase de registro se actualiza incorrectamente a **Solicitud de recuperación aprobada**.
- Cuando la opción Aprobaciones modernas está habilitada y Flujos de nube está inactiva, el proceso de aprobación no se realiza correctamente y no se notifica a los usuarios que envían o aprueban.
