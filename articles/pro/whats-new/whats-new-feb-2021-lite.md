---
title: 'Novedades de febrero de 2021: implementación ligera de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de febrero de 2021 de la implementación ligera de Project Operations.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 139494962562aaaf005e116f02bcd41db58eea27
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574681"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Novedades de febrero de 2021: implementación ligera de Project Operations

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.7.0.95

## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| **Facturación y precios** | 2053736 | Ahora se puede acceder a los detalles de la línea de factura a través de **Factura** > **Información relacionada**. |
| **Facturación y precios** | 2122613 | Se han quitado las acciones **Activar** y **Desactivar** de las entidades de asociación de **Lista de precios**. |
| **Facturación y precios** | 2128606 | Se ha solucionado el problema de **NullReferenceException** en el complemento **GetEstimatesForProject**. |
| **Implementación y configuración** | 2140569 | La solución del proyecto no se debe instalar en los entornos de Dataverse Teams. |
| **Implementación y configuración** | 2086991 | Se ha restringido la localización personalizada de recursos web. |
| **Administración de oportunidades** | 2136794 | Mostrar el mensaje de error correcto cuando se produce un error del proceso **Confirmar factura** o **Marcar factura como pagada**, |
| **Administración de oportunidades** | 2146376 | Se crea un importe de impuestos corregido en los datos reales no imputables a partir de la confirmación de la factura. |
| **Planificación y seguimiento de proyectos** | 2099879 | La implementación del entorno de Dataverse debe crear una categoría de transacción predeterminada con un identificador estático y no generar aleatoriamente un identificador por entorno. |
| **Planificación y seguimiento de proyectos** | 2128577 | Se han corregido los privilegios de usuario de Project Service para actualizar la categoría de transacciones en una asignación de recursos. |
| **Planificación y seguimiento de proyectos** | 2164035 | Se han corregido los problemas de la función **Copiar proyecto**. |
| **Entrada de tiempo** | 2129161 | Se han aplicado restricciones más estrictas para garantizar que los usuarios no puedan cambiar ni actualizar una entrada de tiempo que se ha enviado o aprobado. |
| **Entrada de tiempo** | 2103572 | La aprobación de tiempo para entradas de tiempo no relacionadas con proyectos no debe buscar el rol de aprobador de proyectos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]