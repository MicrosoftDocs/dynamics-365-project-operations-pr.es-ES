---
title: Configurar opciones de parámetros adicionales
description: Cómo configurar las opciones de parámetros adicionales en Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001132"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Configurar opciones de parámetros adicionales (Project Service Automation)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Una vez que ha configurado los elementos de los temas anteriores, debe configurar parámetros de proyecto adicionales para usar con sus proyectos. La primera vez que instaló [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], creó una configuración de parámetros para crear primero todos los registros necesarios para que funcione [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Ahora es el momento de volver y configurar campos adicionales para estas configuraciones de parámetros.  
  
 Deberá haber configurado los siguientes valores:  
  
-   Unidad organizativa  
  
-   Frecuencia de factura  
  
-   Plantilla de horas laborables  
  
-   Lista de precios  
 
En este paso, también indicará el tipo de asignación de recursos que desee:  
  
- **Central**. Sólo los administradores de recursos pueden asignar recursos a proyectos.  
  
- **Híbrido**. Los administradores de recursos, jefes de proyecto, y los directores de cuentas pueden asignar recursos a proyectos.  
  
 
Para establecer parámetros de proyecto:  
  
1. Vaya a **Project Service > Parámetros**.  
  
2. Haga clic en las opciones de parámetros que desea configurar (los que creó la primera vez que instaló el [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), o haga clic en **Nuevo** para crear uno nuevo.  
  
3. En el área **General**, defina todas las opciones para los parámetros del proyecto.  
  
4. En el área **Lista de precios**, haga clic en **+** para agregar una lista de precios, seleccione una lista de precios en la lista desplegable **Lista de precios de parámetros de proyecto** y después haga clic en **Guardar**.  
  
5. Haga clic en el botón **Guardar** en la esquina inferior derecha de la pantalla.  

> [!NOTE]
> El registro de parámetros del proyecto debe mantenerse para que Project Service funcione correctamente. No se debe eliminar este registro.

### <a name="see-also"></a>Vea también  
 [Configuración de recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]