---
title: Información general del asistente de programación
description: Este tema proporciona información sobre cómo trabajar con el asistente de programación para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908618"
---
# <a name="schedule-assistant-overview"></a>Información general del asistente de programación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

El asistente de programación se utiliza para reservar recursos según los requisitos definidos por el gerente de proyecto. El asistente de programación se basa en los parámetros proporcionados en el requisito de recursos para encontrar el recurso. El asistente de programación recomienda recursos que coinciden con los requisitos relevantes, como ventanas de tiempo o habilidades necesarias.

Una vez identificados los recursos adecuados, el administrador de recursos o proyecto puede reservar el recurso para el trabajo.

## <a name="prerequisites"></a>Requisitos previos

El asistente de programación es parte de la solución Universal Resource Scheduling. Esta solución se incluye e instala con Dynamics 365 Project Operations, Dynamics 365 Field Service y Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Asociar requisitos y recursos

Un requisito de recursos generado se basa en detalles como:

-   Características
-   Roles
-   Unidades de negocio
-   Preferencias de recursos
-   Contornos de esfuerzo
-   Zona horaria

El asistente de programación utiliza estos detalles para filtrar recursos.

## <a name="launch-the-schedule-assistant"></a>Iniciar el asistente de programación

Hay dos formas de iniciar el asistente de programación. Si está utilizando el modo híbrido, en la cuadrícula de miembros del equipo puede seleccionar cualquier miembro del equipo con un requisito de recursos sin rellenar y luego seleccionar **Reservar**. Si está utilizando el modo central, el administrador de recursos busca y selecciona el recurso.

## <a name="schedule-assistant-filters"></a>Filtros del asistente de programación

Una vez que se ejecuta el asistente de programación, los detalles del requisito de recursos se muestran como valores filtrados en el panel izquierdo. El administrador de recursos o el administrador de proyectos puede ajustar los resultados ajustando los filtros para satisfacer las necesidades de programación.

El panel de filtro muestra opciones relacionadas con el trabajo, que incluyen:

-   Inicio y finalización del trabajo
-   Características
-   Roles
-   Unidades organizativas
-   Empresa de recursos
-   Tipos de recursos
-   Recursos preferidos
