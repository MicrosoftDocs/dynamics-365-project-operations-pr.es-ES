---
title: 'Novedades de febrero de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de febrero de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cb6ab1337652d18a30fba56560ffe50f78dd4eb4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589033"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de febrero de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en el entorno de Dataverse 4.7.0.95
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.16 

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| **Facturación y precios** | 2053736 | Ahora se puede acceder a los detalles de la línea de factura a través de **Factura** > **Información relacionada**. |
| **Facturación y precios** | 2122613 | Se han quitado las acciones **Activar** y **Desactivar** de las entidades de asociación de **Lista de precios**. |
| **Facturación y precios** | 2128606 | Se ha solucionado el problema de **NullReferenceException** en el complemento **GetEstimatesForProject**. |
| **Implementación y configuración** | 2139346 | Se ha solucionado el problema de importación de la solución **Dynamics365ProjectOperationsDualWrite** no administrada. |
| **Implementación y configuración** | 2140569 | La solución del proyecto no se debe instalar en los entornos de Dataverse Teams. |
| **Implementación y configuración** | 2086991 | Se ha restringido la localización personalizada de recursos web. |
| **Administración de oportunidades** | 2136794 | Se muestra el mensaje de error correcto cuando se produce un error del proceso **Confirmar factura** o el proceso **Marcar factura como pagada**. |
| **Administración de oportunidades** | 2139330 | Cambiar el jefe de proyecto en un proyecto no debe restablecer el valor predeterminado de la empresa propietaria. |
| **Administración de oportunidades** | 2146376 | Se crea un importe de impuestos corregido en los datos reales no imputables a partir de la confirmación de la factura. |
| **Planificación y seguimiento de proyectos** | 2099879 | La implementación del entorno de Dataverse debe crear una categoría de transacción predeterminada con un identificador estático y no generar aleatoriamente un identificador por entorno. |
| **Planificación y seguimiento de proyectos** | 2128577 | Se han corregido los privilegios de usuario de Project Service para actualizar la categoría de transacciones en una asignación de recursos. |
| **Planificación y seguimiento de proyectos** | 2164035 | Se han corregido los problemas de la función **Copiar proyecto**. |
| **Entrada de tiempo** | 2129161 | Se han aplicado restricciones más estrictas para garantizar que los usuarios no puedan cambiar ni actualizar una entrada de tiempo que se ha enviado o aprobado. |
| **Entrada de tiempo** | 2103572 | La aprobación de tiempo para entradas de tiempo no relacionadas con proyectos no debe buscar el rol de aprobador de proyectos. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance 

Para obtener más información sobre la gestión y contabilidad de proyectos en Dynamics 365 Finance, consulte [Novedades de enero de 2021: Project Operations para escenarios basados en recursos/sin existencias](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Actualizaciones regulatorias

Para obtener información sobre actualizaciones normativas para aplicaciones de finanzas y operaciones, consulte [Actualizaciones normativas](/dynamics365/finance/localizations/regulatory-updates). Otra forma de conocer las actualizaciones regulatorias es iniciar sesión en Lifecycle Services (LCS) y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de temas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]