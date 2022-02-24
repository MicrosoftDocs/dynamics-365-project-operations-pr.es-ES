---
title: 'Novedades de noviembre de 2020: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2020 de Project Operations para escenarios basados en recursos / no almacenados.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367287"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de noviembre de 2020: Project Operations para escenarios basados en recursos/no mantenidos en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

- Project Operations en el entorno CDS versión 4.4.0.70
- Gestión de proyectos y contabilidad en el entorno de Dynamics 365 Finance versión 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Actualizaciones en Project Operations para escenarios basados en recursos/no mantenidos en existencias

### <a name="project-operations-on-cds"></a>Project Operations en CDS

| Área de características                 | Número de referencia | Actualización de calidad                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Administración de oportunidades       | 2036993          | La línea de estimación y las líneas de contrato de asignación de recursos se actualizan en las cotizaciones ganadoras cuando el tipo de línea de cotización es **Todas las tareas**.                                                 |
| Facturación y precios          | 2070392          | Las líneas de contrato del proyecto en la factura aumentan cada vez que se selecciona **Actualizar transacciones de facturas**.                                                                         |
| Planificación del proyecto             | 2043336          | No se puede eliminar el registro de un miembro del equipo del proyecto.                                                                                                                                  |
| Planificación del proyecto             | 2046013          | Comportamiento incoherente para las columnas de etiquetas Estimates durante la carga frente al cambio de tipo de fase de tiempo.                                                                                   |
| Planificación del proyecto             | 2046647          | Las horas de inicio y finalización tienen una diferencia de una hora cuando los requisitos de recursos se generan a partir de los miembros del equipo del proyecto.                                                                      |
| Planificación del proyecto             | 2053879          | (Según el próximo lanzamiento de CDS) PublishUnassignedAssignments interrumpe un intento de guardar una tarea cuando aparece el error "El valor pasado para ConditionOperator.In está vacío".                       |
| Planificación del proyecto             | 2055501          | Al dejar **Fecha de inicio del proyecto** vacío, se produce un error en la programación.                                                                                                      |
| Planificación del proyecto             | 2066817          | No se puede crear un recurso genérico con el selector de personas en la pestaña **Tareas**.                                                                                                   |
| Planificación del proyecto             | 2067034          | El botón **Ver detalles** no está disponible en la página **Detalles de la tarea**.                                                                                                       |
| Administración de recursos          | 2046667          | Los miembros genéricos del equipo no se eliminan incluso después de que se hayan completado todos los recursos.                                                                                                    |
| Entrada de tiempo y gasto rápido | 2047499          | El botón **Nuevo** en la página de Entrada de tiempo abre la página **Nueva firma de correo electrónico**.                                                                                               |
| Entrada de tiempo y gasto rápido | 2059859          | Se abre una ventana emergente inesperada al crear una entrada de gastos.                                                                                                                         |
| Otros                        | 2044181          | (Desinstalación de la orden de compra) Al intentar desinstalar msdyn_ProjectServiceCore_Patch y las soluciones centrales de Project Service msdyn, aparece el error "El registro no está disponible".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| Área de características        | Número de referencia | Actualización de calidad                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconocimiento de ingresos | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | El porcentaje de avance estimado del proyecto es incorrecto cuando el contrato utiliza una moneda extranjera y el porcentaje de avance del trabajo para el método completo.                     |
| Reconocimiento de ingresos | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | No se pueden publicar estimaciones con el método de finalización **Costo real**.                                                                                                    |
| Reconocimiento de ingresos | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | La eliminación falla debido a un error de desequilibrio del comprobante cuando la moneda de la empresa y la moneda de la transacción son diferentes.                                              |
| Gestión de gastos  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Para los usuarios que no son administradores, los valores de búsqueda para las columnas de la línea de gastos como **Id. de proyecto** y **Categoría de gastos** no se muestran correctamente en el marco del conector de datos. |
| Gestión de gastos  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | La propiedad de línea predeterminada no se muestra para las categorías de gastos.                                                                                                         |
| Gestión de gastos  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | La integración de gastos debe incluir la propiedad de línea del informe de gastos.                                                                                             |
| Facturación           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | No se pueden publicar propuestas de facturas de proyectos debido a un mensaje de error que dice que la combinación de FD no se validó.                                                    |
| Facturación           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | No se pueden ver las transacciones de la página de detalles de la **factura**.                                                                                                              |
| Facturación           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Las líneas de propuesta de factura se pueden eliminar.                                                                                                                                  |
| Contabilidad de proyecto  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Los elementos del menú **Pronóstico** no son visibles en la página de lista **Proyectos**.                                                                                                   |
| Contabilidad de proyecto  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | No se puede abrir **Declaración de proyecto**   > **Transacciones y previsión**.                                                                                                       |
| Contabilidad de proyecto  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajustar la contabilidad** no está habilitado para transacciones de proyectos facturados.                                                                                                  |
| Contabilidad de proyecto  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Los detalles contables no se incluyen en la tabla **ProyCDSActualsImport** cuando el diario **Integración** se publica.                                                  |
| Contabilidad de proyecto  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | La entrada de previsión del proyecto se duplica cuando elimina y luego vuelve a leer una asignación de recursos.                                                                            |
| Contabilidad de proyecto  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Seleccionar un enlace de ID de proyecto no abre la URL del enlace profundo de CDS.                                                                                                         |
| Contabilidad de proyecto  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | No se puede actualizar la fecha de inicio de una tarea en CDS.                                                                                                                           |
| Contabilidad de proyecto  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Habilitar la función, múltiples líneas de contrato no es posible sin la integración de CDS.                                                                                   |

### <a name="regulatory-updates"></a>Actualizaciones regulatorias
Para obtener información sobre actualizaciones normativas para aplicaciones de Finance and Operations, vea [Actualizaciones regulatorias](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). También puede iniciar sesión en LCS y ver las actualizaciones normativas planificadas mediante la herramienta de búsqueda de problemas. La búsqueda de problemas le permite buscar por país, tipo de función y lanzamiento.
