---
title: Novedades o cambios en la versión de actualización 47, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 47, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477243"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novedades o cambios en la versión de actualización 47, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 45, V3. Esta versión tiene un número de compilación de V3.10.78.8 y generalmente está disponible a través de una actualización automática en julio de 2022.

## <a name="update-release-47"></a>Versión de actualización 47

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Administración de recursos**
- Se actualizó una validación para garantizar que los usuarios no puedan desencadenar una excepción de referencia nula al intentar crear un miembro del equipo del proyecto sin un **Recurso reservable**.
