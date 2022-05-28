---
title: Novedades o cambios en la versión de actualización 15, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 15 de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585169"
---
# <a name="project-service-automation-update-release-15-v3"></a>Versión de actualización de Project Service Automation 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA). Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 15. Esta versión tiene un número de compilación de V3.10.5.28 y está disponible con carácter general a través de una actualización automática en enero de 2020.

## <a name="update-release-15"></a>Versión de actualización 15 

### <a name="enhancements"></a>Mejoras

- Administración del proyecto

### <a name="bug-fixes"></a>Solución de errores

- Tiempo y gasto

  - Corregido: Agregar el manejo de errores en carga en la vista de conciliación.
  - Corregido: Centro de recursos de proyecto: Cambiar de nombre **Importe** para reducir la ambigüedad.
  - Corregido: Ajustar la vista **Copiar columnas de entrada de tiempo** para incluir el tipo.
  - Corregido: la edición de la duración de la entrada de tiempo en la vista de cuadrícula utilizando números decimales genera un error desconocido para algunos números.

- Administración del proyecto

  - Corregido: El menú desplegable para **Usar en la vista de seguimiento** ahora se amplía según el ancho de las opciones.
  - Corregido: Al administrar proyectos en la zona horaria +13, los cálculos de tareas pueden mostrar resultados imprecisos.
  - Corregido: **Hora de finalización del miembro del equipo** se ha corregido al usar un calendario de 24 horas.
  - Corregido: Se ha reactivado el **BPF** en el formulario principal de **msdyn_project**.
  - Corregido: El cálculo de asignaciones ya no ignora un día.
  - Corregido: Se ha agregado un nuevo banner de notificación al formulario del proyecto cuando la zona horaria difiere entre el usuario y el proyecto.

- Sales

  - Corregido: La búsqueda de categoría de estimación de gastos se puede usar para filtrar duplicados.
  - Corregido: El código en **PluginDomain.ExecuteIn TryCatchBlock (..)** ya no oculta el origen de la excepción.
  - Corregido: Ya no aparece un mensaje de error en **Búsqueda de proyectos** en el formulario **Línea de oferta** cuando hay más de 1000 proyectos.
  - Corregido: La cuadrícula **Estimaciones** para estimaciones de mano de obra y estimaciones de gastos ahora muestra el símbolo de moneda correcto.
  - Corregido: Después de que una organización actualice PSA de la versión de actualización 14 a la versión de actualización 15, la pestaña **Programación** ya no aparece en blanco en el formulario **Proyecto**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
