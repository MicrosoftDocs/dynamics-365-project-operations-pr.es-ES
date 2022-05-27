---
title: Novedades o cambios del primer lanzamiento de 2020 de la versión 3.x de Project Service Automation
description: Este tema proporciona información sobre las novedades y los cambios en el primer lanzamiento de Project Service Automation versión 3, 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
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
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577901"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novedades o cambios del primer lanzamiento de 2020 de la versión 3 de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

El tema resalta las consideraciones de actualización clave al pasar a la última versión del primer lanzamiento de Project Service Automation (PSA) versión 3.x, 2020.

## <a name="time-entry"></a>Entrada de tiempo
La experiencia de entrada de tiempo se ha ampliado para ofrecer capacidades para ampliar la entrada de tiempo en más escenarios de clientes. Esto incluye la capacidad de agregar tipos de entrada, que ahora impulsan un comportamiento específico basado en el nombre del esquema de campo **Configuración de entrada de tiempo**, que se muestra como **Origen de la hora**. Se ha agregado una nueva solución, llamada Tiempo, Gasto, Estado y Aprobaciones (TESA) para admitir esta funcionalidad.

### <a name="upgrade-consideration"></a>Consideración sobre actualizaciones
Para admitir esta funcionalidad, se han actualizado los roles dentro de PSA para incluir nuevos privilegios. Estos privilegios conceden acceso de lectura a la nueva entidad, **Configuración de entrada de tiempo**.

A los usuarios que requieren la capacidad de registrar el tiempo se les debe conceder el rol de usuario **Usuario de entrada de tiempo** además de los roles existentes. Este rol incluye la nueva funcionalidad y garantiza que la entrada de tiempo continuará funcionando.

Además, si tiene algún módulo de aplicación personalizado que incluya todos los formularios para la entidad de entrada de tiempo, deberá eliminar el **Formulario de creación rápida de entrada de tiempo TESA** del módulo.

### <a name="currently-extended-time-entry-changes"></a>Cambios de entrada de tiempo actualmente ampliados
Para minimizar el impacto en los usuarios actuales de la entrada de tiempo, este cambio de rol es el único requisito central necesario para continuar utilizando la entrada de tiempo. Si ha creado vistas personalizadas o experiencias de entrada de tiempo independientes, debe establecer los campos **Configuración de entrada de tiempo** al valor de PSA correcto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
