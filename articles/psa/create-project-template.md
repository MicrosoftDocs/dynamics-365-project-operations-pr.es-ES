---
title: Crear una plantilla de proyecto
description: Cómo crear una plantilla de proyecto en Project Service
author: ruhercul
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
ms.openlocfilehash: 1423dfedccfdc471662581707b4441c9ed477f7c0811ccf3905af8c59f774f77
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990877"
---
# <a name="create-a-project-template-project-service"></a>Crear una plantilla de proyecto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Las plantillas de proyecto ahorran tiempo si su empresa presenta ofertas regularmente para tipos similares de proyectos. Ofrecen un conjunto de roles estándar y de horas estimadas para un tipo de proyecto. Los administradores de cuentas y los jefes de proyecto pueden crear los proyectos basados en una plantilla de proyectos, o pueden copiar la plantilla y crear la suya propia.  
  
## <a name="components-of-project-template"></a>Componentes de la plantilla de proyecto
 Una plantilla de proyecto consta de tres componentes:  
  
- **Estructura de descomposición del trabajo**: Una estructura de descomposición del trabajo en una plantilla de proyecto tiene el mismo conjunto de elementos que en el proyecto. Puede crear una jerarquía de tareas, asociar roles a tarea, definir atributos de programación, establecer dependencias y ver todos los datos del diagrama de Gantt. La estructura de descomposición del trabajo en plantillas de proyecto también es compatible con los modos de tarea para cada tarea. No hay diferencia entre una plantilla de proyecto y un proyecto al crear un programa de trabajo.  
  
- **Estimaciones de proyecto**: Las estimaciones de proyecto en plantillas funcionan igual que en proyectos, excepto las listas de precios para establecer valores predeterminados de coste y precios de ventas siempre son las listas de precios de coste y precios de ventas predeterminadas definidas en parámetros de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. El resto de la funcionalidad es igual que en un proyecto.  
  
- **Formación del equipo de proyecto**: Cuando se forma un equipo de proyecto para una plantilla de proyectos, no puede reservar un recurso con nombre en una plantilla. Puede usar **Generar equipo de proyecto** en la estructura de descomposición del trabajo para generar un conjunto de recursos genéricos. También puede especificar conocimientos y habilidades necesarios para recursos genéricos. No puede sustituir un recurso genérico con un recurso reservable en plantillas de proyecto.  
  
## <a name="create-a-project-from-a-template"></a>Crear un proyecto a partir de una plantilla  
 Puede crear un proyecto a partir de una plantilla de las siguientes formas:  
  
-   Cuando cree un proyecto de la oferta, puede seleccionar una plantilla de proyecto en el formulario de creación rápida de proyecto.  
  
-   Cuando cree un proyecto haciendo clic en **Nuevo proyecto**, el formulario de proyecto se muestra antes de guardar el registro. Desde ahí, puede hacer clic en el campo **Elegir una plantilla** para elegir de la lista de plantillas de proyecto predefinidas en su organización.  
  
-   Haga clic en **Crear un proyecto a partir de una plantilla** en la página **Plantilla del proyecto** para crear un proyecto desde la plantilla.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copiar componentes de una plantilla a un proyecto  
 Al copiar los componentes de una plantilla en un proyecto, hay algunas cosas que debería saber.  
  
 **Copiar una estructura de descomposición del trabajo**: Al copiar la estructura de descomposición del trabajo de una plantilla de proyecto, si el proyecto tiene otro calendario del proyecto que la plantilla, las horas laborables del calendario del proyecto se aplicarán a la programación de tareas. Esto ajusta la programación al calendario del proyecto de apoyo. De forma similar, la primera tarea en la estructura de descomposición del trabajo toma la fecha de inicio del proyecto, por lo que el resto de la programación de la jerarquía de tareas se actualiza en función de la duración y las dependencias especificadas en la estructura de descomposición del trabajo de la plantilla.  
  
 **Copiar estimaciones del proyecto**: Al copiar a través de las líneas de estimación de proyectos, se actualizarán las listas de precios basándose en la unidad propietaria del proyecto para la lista de precios de coste y el cliente para la lista de precios de ventas. El coste unitario y los precios de venta se determinan a partir de estas listas de precios en los proyectos asociados a una entidad de ventas.  
  
 **Copiar un equipo del proyecto**: Al copiar el equipo del proyecto desde la plantilla hasta un proyecto, los recursos genéricos se copian, junto con las cualificaciones y las habilidades definidas en la plantilla. Las asignaciones de recursos genéricos también se mantienen como en la plantilla del proyecto.  
  
### <a name="see-also"></a>Vea también  
 [Guía del jefe de proyecto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]