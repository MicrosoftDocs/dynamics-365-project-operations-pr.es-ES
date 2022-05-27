---
title: Copiar un proyecto
description: En este tema se proporciona información sobre la copia de proyectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574451"
---
# <a name="copy-a-project"></a>Copiar un proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Con Dynamics 365 Project Operations, puede crear rápidamente nuevos proyectos seleccionando **Copiar proyecto** en el formulario **Proyectos**. Para copiar un proyecto, abra el proyecto que desea copiar y luego seleccione **Copiar proyecto**. La acción copiará lo siguiente:

- Propiedades del proyecto 
- Estructura de descomposición del trabajo
- Miembros del equipo del proyecto
- Estimaciones de proyecto
- Estimaciones de gastos del proyecto
- Estimaciones de materiales del proyecto
- Listas de comprobación del proyecto
- Recipientes de proyecto

## <a name="project-properties"></a>Propiedades del proyecto

Cuando se copia el proyecto, se copian los valores de los siguientes campos.

| Campo | Materiales sin existencias de Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Customer | :heavy_check_mark: | :heavy_check_mark: | |
| Plantilla de calendario | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Moneda | :heavy_check_mark: | :heavy_check_mark: | |
| Unidad de contratación | :heavy_check_mark: | :heavy_check_mark: | |
| Empresa propietaria | :heavy_check_mark: | | |
| Jefe de proyecto | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Estado general del proyecto | :heavy_check_mark: | :heavy_check_mark: | |
| Comments | :heavy_check_mark: | :heavy_check_mark: | |
| Estimaciones | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Fecha de inicio estimada</p><p><strong>Nota:</strong> este campo especifica la fecha en que se crea el proyecto a partir de la copia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Fecha de finalización estimada</p><p><strong>Nota:</strong> la fecha de este campo se ajusta en función de la fecha de inicio del nuevo proyecto que se realizó a partir de la copia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Esfuerzo (horas) | :heavy_check_mark: | :heavy_check_mark: | |
| Coste estimado de mano de obra | :heavy_check_mark: | :heavy_check_mark: | |
| Coste estimado de gastos | :heavy_check_mark: | :heavy_check_mark: | |
| Coste estimado de materiales | | :heavy_check_mark: | |

> [!NOTE]
> Copiar proyecto es una operación de larga duración. También se copian los registros del proyecto, sus atributos relevantes y muchas entidades relacionadas. Debido a la naturaleza de larga duración de la operación, una vez iniciada la copia, la página del proyecto de destino se bloquea para su edición hasta que se completa la operación de copia.

## <a name="work-breakdown-structure"></a>Estructura de descomposición del trabajo

Cuando se copia el proyecto, se copia toda la estructura de descomposición del trabajo cargada por los recursos. Los recursos con nombre se sustituyen por recursos genéricos. Si los recursos con nombre no tienen las mismas horas de trabajo que el recurso genérico, la programación se volverá a calcular y la duración de las tareas podría cambiar.

## <a name="project-team-members"></a>Miembros del equipo del proyecto

Cuando un equipo de proyecto se copia desde el proyecto de origen, se copian los recursos genéricos. Las asignaciones de recursos genéricos también se mantienen como si estuvieran en el proyecto de origen. Los recursos con nombre se convertirán en miembros del equipo genéricos.

> [!NOTE]
> Los miembros del equipo y las tareas no se copian en Project for the Web.

## <a name="estimates"></a>Estimaciones

Cuando se copia el proyecto, las líneas de estimación de recursos, gastos y materiales se copian del proyecto de origen. 

Para obtener información sobre cómo acceder mediante programación a Copiar proyecto, consulte [Desarrollar plantillas de proyectos con Copy Project](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ofertas y contratos

Las ofertas y los contratos no están vinculados al proyecto de destino.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
