---
title: Configure el tablero de programación para mostrar los trabajadores contratados y la capacidad subcontratada
description: Este artículo describe cómo configurar Schedule Board en Microsoft Dynamics 365 Project Operations para mostrar la capacidad de recursos subcontratados al dotar de personal a los requisitos de recursos del proyecto.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919851"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configure el tablero de programación para mostrar los trabajadores contratados y la capacidad subcontratada 

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Tablero de programación en Microsoft Dynamics 365 Project Operations se puede utilizar para buscar recursos de dos formas:

- Búsqueda de recursos generales sin el contexto de ningún requisito de recursos específico basado en proyectos.
- Búsqueda de recursos específicos de requisitos donde el requisito del proyecto proporcionará el contexto para los recursos sugeridos.

Para notificar al tablero de programación sobre la capacidad de recursos subcontratados y los trabajadores contratados, debe realizar actualizaciones en la configuración del Tablero de programación. Estas actualizaciones incluyen: 
- Actualice la configuración del tablero de programación para la búsqueda general de recursos.
- Actualice la configuración del tablero de programación para la búsqueda de recursos basada en requisitos.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualice la configuración del tablero de programación para la búsqueda general de recursos
### <a name="update-filters-for-general-resource-search"></a>Actualizar filtros para la búsqueda de recursos generales
Cuando busca un recurso, los filtros disponibles en el tablero de programación deben actualizarse para que también pueda buscar recursos externos especificando cualquiera o todos los siguientes:
  - Tipo de trabajador, si los recursos mostrados deben ser trabajadores por contrato o empleados.
  - Empresa proveedora a la que debe pertenecer un recurso.
  - Recursos que pertenecen a un subcontrato o línea de subcontrato específico.
    
### <a name="update-retrieve-resource-query"></a>Actualizar consulta de recuperación de recursos
La consulta utilizada para la búsqueda también debe actualizarse para utilizar estos atributos de filtro adicionales. Utilice los siguientes pasos para actualizar la configuración del tablero de programación para la búsqueda general de recursos:  
1. Abra **Configuración del tablero de programación** para un tablero de programación específico.
2. Abra la pestaña **Configuración general** y desplácese hasta **Otros ajustes**.
3. En la lista de configuraciones de esta sección, actualice **Diseño de filtro** a **Diseño de filtro predeterminado para Project Operations Lite**.
4. Actualice **Consulta de recuperación de recursos** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite**.

![Actualice la configuración del tablero de programación para la búsqueda general de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualice la configuración del tablero de programación para la búsqueda de recursos basada en requisitos
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualizar filtros para la búsqueda de recursos basada en requisitos 
Cuando busca un recurso, los filtros disponibles en el tablero de programación deben actualizarse para que también pueda buscar recursos externos especificando cualquiera o todos los siguientes:
 - Tipo de trabajador, si los recursos mostrados deben ser trabajadores por contrato o empleados.
 - Empresa proveedora a la que debe pertenecer un recurso.
 - Recursos que pertenecen a un subcontrato o línea de subcontrato específico.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualizar la consulta de recuperación de recursos para la búsqueda de recursos específicos de requisitos 
La consulta utilizada para la búsqueda también debe actualizarse para utilizar estos atributos de filtro adicionales. Utilice los siguientes pasos para actualizar la configuración del tablero de programación para la búsqueda de recursos basada en requisitos:

1. Abra **Configuración del tablero de programación** para un tablero de programación específico y luego seleccione **Abrir configuración predeterminada** para abrir la configuración para la búsqueda específica de requisitos.
2. Abra la pestaña **Configuración general** y desplácese hasta **Otros ajustes**.
3. En la lista de configuraciones de esta sección, actualice **Diseño de filtro** a **Diseño de filtro predeterminado para Project Operations Lite**.
4. Actualice **Consulta de recuperación de recursos** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite**.
5. Abra la pestaña **Tipos de horarios** y vaya a **Proyecto**.
6. En la configuración de **Proyecto**, actualice **Asistente de programación Recuperar consulta de recursos** a **Consulta de recursos de recuperación predeterminada para Project Operations Lite** y actualice **Consulta de recuperación de restricciones del asistente de programación** a **Consulta de restricciones de recuperación predeterminada para Project Operations Lite**.

![Actualice la configuración del tablero de programación para la búsqueda de recursos basada en requisitos](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
