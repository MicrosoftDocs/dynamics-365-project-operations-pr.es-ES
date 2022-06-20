---
title: 'Novedades de marzo de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de marzo de 2021 de la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932961"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de marzo de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en el entorno de Dataverse versión 4.8.0.91 
- Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.16 

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse


| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2133873 | Se corrigió la visualización del símbolo de moneda de **Precio de venta unitario** en la cuadrícula **Estimaciones de gastos**. |
| Facturación y precios | 2174616 | Cuando se gana una cotización, se hace referencia a la lista de precios personalizada del contrato en los detalles de la línea del contrato que se copian de la cotización. |
| Administración de oportunidades | 2167475 | Importe de impuesto fijo en la factura de corrección que originó una entrada real no facturada. |
| Administración de oportunidades | 2176285 | El monto del impuesto no debe copiarse de los detalles del contrato de venta / línea de cotización a los detalles del contrato de costo / línea de cotización. |
| Administración de oportunidades | 2188079 | No se debe crear una regla de facturación dividida para contratos que no se basan en el trabajo. |
| Planificación y seguimiento | 2125274 | **Proyecto de mapa de escritura dual** atributo para **Asignación de fecha de inicio del proyecto** actualizado desde **msdyn\_taskearlieststart** a **msdyn\_actualstart**. |
| Planificación y seguimiento | 2138853 | Se actualizó la función de copia del proyecto para garantizar que las líneas de estimación de gastos que las tareas de referencia se copien en el proyecto de destino. |
| Planificación y seguimiento | 2154306 | Se corrigieron problemas con la eliminación de estimaciones de gastos en Project Operations para escenarios basados en recursos. |
| Planificación y seguimiento | 2173259 | Se actualizó la función de copia del proyecto para garantizar que no se muestre el mensaje de error **Copiando WBS** en ciertos escenarios. |
| Tiempo y gasto | 2148910 | Problema de pantalla solucionado con la página **Editar entrada** en la cuadrícula **Entrada de tiempo**. |
| Tiempo y gasto | 2159798 | Controles más estrictos para garantizar que las entradas de gastos aprobadas no se puedan editar. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

Para más información, consulte [Novedades de enero de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Actualizaciones regulatorias

Para obtener información sobre actualizaciones normativas para aplicaciones de finanzas y operaciones, consulte [Actualizaciones normativas](/dynamics365/finance/localizations/regulatory-updates). Otra forma de conocer las actualizaciones regulatorias es iniciar sesión en LCS y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de temas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]