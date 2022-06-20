---
title: Novedades o cambios en la versión de actualización 41, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 41, V3 de Microsoft Dynamics 365 Project Service Automation.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930569"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novedades o cambios en la versión de actualización 41, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 41, V3. Esta versión tiene un número de compilación de V3.10.62.162 y está disponible con carácter general a través de una actualización automática en marzo de 2022.

## <a name="update-release-41"></a>Versión de actualización 41

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Administración del proyecto**
- Cuando intenta crear un proyecto a partir de una plantilla que se basa en un proyecto creado desde el complemento de escritorio, aparece el siguiente error: "Validación del campo de trabajo planificado de la asignación de recursos: la fecha de finalización de cada intervalo de tiempo de asignación de recursos no debe ser anterior a su fecha de inicio".

**Tiempo y gasto**
- Cuando intenta eliminar una entrada de tiempo, aparece el siguiente mensaje de error: "Se produjo un error inesperado del código ISV".

**Ventas**
- Cuando crea una factura para un hito de precio fijo, los campos **Descripción** y **Descripción externa** no están rellenos. 
