---
title: Novedades o cambios en la versión de actualización 34, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 34, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588711"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novedades o cambios en la versión de actualización 34, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 34. Esta versión tiene un número de compilación de V3.10.55.38 y generalmente está disponible a través de una actualización automática en julio de 2021.

## <a name="update-release-34"></a>Versión de actualización 34

### <a name="bug-fixes"></a>Correcciones de errores
Se han solucionado los siguientes problemas.

**General**

- Las actualizaciones impulsadas por el editor no activan el nuevo flujo de trabajo de aprobación moderno.
- Faltan los atributos **Estado del objetivo** y **Tipo de acción** en la página principal de **Conjunto de aprobación**.

**Tiempo y gasto**

- No se puede aprobar una solicitud de coincidencia mediante el flujo de aprobación moderno.
- Copiar entradas de una semana de tiempo no funciona cuando se copian entradas que no están relacionadas con el usuario que inició sesión.

**Planificación del proyecto**

- Los contornos de asignación de recursos se dañan al importar desde el complemento de escritorio de Microsoft Project.

**Administración de recursos**

- Cuando publica un proyecto desde el complemento de cliente de escritorio de Microsoft Project, se cambia la fecha de finalización de los requisitos existentes.
- La precisión decimal supera los dos lugares decimales en el cuadro de diálogo de confirmación de reservas extendidas.

**Ventas**

- Cuando agrega una línea basada en productos con un producto existente a un contrato de proyecto, se muestra la excepción **clave no encontrada en el diccionario**.
- Los clientes potenciales no se pueden calificar cuando un tipo de orden se asigna de un cliente potencial a una oportunidad.
