---
title: 'Novedades de junio de 2022: implementación simplificada de Project Operations'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de junio de 2022 de la implementación simplificada de Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031214"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novedades de junio de 2022: implementación simplificada de Project Operations

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en la versión del entorno de Dataverse 4.43.0.77 o 4.43.0.119

## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Subcontratación | 2708885 | Se corrigió el mensaje de error que aparece cuando un usuario crea un registro de encabezado de reserva de recursos reservables donde no se completa ningún recurso reservable. |
| Planificación y seguimiento del proyecto | 2629441 | Se corrigió la lógica de activación del flujo de trabajo para ayudar a evitar un bucle infinito cuando se actualizan las tareas del proyecto. |
| Tiempo y gastos | 2641209 | Las importaciones de entradas de tiempo de asignaciones/reservas deben conservar una referencia de recurso reservable. |
| Planificación y seguimiento del proyecto | 2651148 | El encabezado del documento del proyecto debe estar protegido.|
| Planificación y seguimiento del proyecto | 2653145 | Se agregaron validaciones para garantizar que no se pueda crear un registro de proyecto que tenga caracteres no válidos en su nombre. |
| Tiempo y gastos | 2654710 | Corregido el filtrado en la página **Aprobaciones**. |
| Facturación y precios | 2667805 | Se agregaron validaciones para ayudar a evitar que se creen datos reales de ventas facturados si no existen respaldos de datos reales de ventas no facturados. |
| Facturación y precios | 2668378 | Se agregaron validaciones para ayudar a evitar que se agregue una dimensión de precios personalizada a menos que se complete un nombre lógico y un nombre de campo. |
| Tiempo y gastos | 2700428 | Se mejoró la lógica de aprobaciones para garantizar que se puedan procesar otros conjuntos de aprobación para el proyecto incluso si uno de los conjuntos de aprobación está atascado en los trabajos del sistema. |
