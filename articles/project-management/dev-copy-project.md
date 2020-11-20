---
title: Desarrollar plantillas de proyectos con Copiar proyecto
description: Este tema proporciona información sobre cómo crear plantillas de proyecto mediante la acción personalizada Copiar proyecto.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131634"
---
# <a name="develop-project-templates-with-copy-project"></a>Desarrollar plantillas de proyectos con Copiar proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations admite la capacidad de copiar un proyecto y revertir cualquier asignación a los recursos genéricos que representan el rol. Los clientes pueden utilizar esta funcionalidad para crear plantillas de proyectos básicas.

Cuando selecciona **Copiar proyecto**, se actualiza el estado del proyecto de destino. Use **Razón para el estado** para determinar cuándo se completa la acción de copia. Seleccionar **Copiar proyecto** también actualiza la fecha de inicio del proyecto a la fecha de inicio actual si no se detecta una fecha objetivo en la entidad del proyecto objetivo.

## <a name="copy-project-custom-action"></a>Acción personalizada Copiar proyecto 

### <a name="name"></a>Nombre 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parámetros de entrada
Hay tres parámetros de entrada:

| Parámetro          | Escribir   | Valores                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referencia de entidad | Proyecto de origen |
| Destino             | Referencia de entidad | Proyecto de destino |


- **{"clearTeamsAndAssignments":true}**: el comportamiento predeterminado de Project for the Web y eliminará todas las asignaciones y miembros del equipo.
- **{"removeNamedResources":true}** El comportamiento predeterminado de Project Operations y revertirá las asignaciones a recursos genéricos.

Para obtener más información sobre las acciones predeterminadas, consulte [Usar acciones de la API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especifique los campos para copiar 
Cuando se llama a la acción, **Copiar proyecto** mirará la vista del proyecto **Copiar columnas de proyecto** para determinar qué campos copiar cuando se copia el proyecto.
