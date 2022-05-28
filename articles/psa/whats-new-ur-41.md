---
title: Novedades o cambios en la versión de actualización 41, V3, de Project Service Automation
description: Este tema enumera las características y correcciones que están disponibles en Microsoft Dynamics 365 Project Service Automation, versión de actualización 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580983"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novedades o cambios en la versión de actualización 41, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 41, V3. Esta versión tiene un número de compilación de V3.10.62.162 y está disponible con carácter general a través de una actualización automática en marzo de 2022.

## <a name="update-release-41"></a>Versión de actualización 41

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Administración del proyecto**
- Cuando intenta crear un proyecto a partir de una plantilla que se basa en un proyecto creado desde el complemento de escritorio, aparece el siguiente error: "Validación del campo de trabajo planificado de la asignación de recursos: la fecha de finalización de cada intervalo de tiempo de asignación de recursos no debe ser anterior a su fecha de inicio".

**Tiempo y gasto**
- Cuando intenta eliminar una entrada de tiempo, aparece el siguiente mensaje de error: "Se produjo un error inesperado del código ISV".

**Ventas**
- Cuando crea una factura para un hito de precio fijo, los campos **Descripción** y **Descripción externa** no están rellenos. 
