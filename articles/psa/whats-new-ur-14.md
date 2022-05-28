---
title: Novedades o cambios en la versión de actualización 14, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 14 de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8504ac5a0ce7254baee9139e4407e712c758540d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594324"
---
# <a name="project-service-automation-update-release-14-v3"></a>Versión de actualización de Project Service Automation 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA). Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 14. Esta versión tiene un número de compilación de V3.10.4.21 y está disponible en la siguiente programación:

- **Disponibilidad general (actualización automática):** enero de 2020
- **Actualización automática:** febrero de 2020

## <a name="update-release-14"></a>Versión de actualización 14

### <a name="enhancements"></a>Mejoras

- Sales

     - Los valores de campo personalizados de **Detalles de línea de oferta** se copian en **Detalles de línea de contrato de proyecto** cuando una oferta se actualiza a **cerrada como lograda**.
     - Los proyectos confirmados pueden ser **cerrados como perdidos**.

- Administración de recursos

     - Al ampliar las reservas, los usuarios recibirán un cuadro de diálogo de confirmación para resumir los resultados de la reserva y proporcionar un vínculo para Mantener reservas.


### <a name="bug-fixes"></a>Solución de errores

- Tiempo y gasto

     - Corregido: Se mejoró la experiencia del usuario cuando el usuario no ha seleccionado ninguna entrada para corregirla.

- Administración de recursos

     - Corregido: La reserva de un recurso varias veces desborda el nombre del recurso que se puede reservar.

- Sales

     - Corregido: El precio de venta total no se calcula hasta que el usuario también introduce un precio de coste para las estimaciones de gastos en un proyecto.
     - Corregido: Se produce un error al cerrar una oferta como **Lograda** si el contrato del proyecto asociado no está en un estado **Borrador**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
