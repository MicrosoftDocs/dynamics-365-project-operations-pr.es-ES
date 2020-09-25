---
title: Novedades en la versión de actualización 16, de Project Service Automation V3
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 16, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756002"
---
# <a name="project-service-automation-v3-update-release-16"></a>Versión de actualización 16 Project Service Automation V3
Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso.

Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea, página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar una solución preferida](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page). En este tema se muestran las características y correcciones que son nuevas o que han cambiado para PSA V3, versión de actualización 16. Esta versión tiene un número de compilación de V3.10.6.34 y está disponible con carácter general a través de una actualización automática en enero de 2020

## <a name="update-release-16"></a>Versión de actualización 16

### <a name="bug-fixes"></a>Correcciones de errores

-   Tiempo y gasto

    -   Corregido: Los usuarios que intenten enviar entradas de tiempo y gastos eliminados para aprobaciones ahora recibirán los mensajes de error pertinentes.

-   Administración del proyecto

    -   Corregido: Las unidades de dotación de recursos definidas para los miembros del equipo en las plantillas se respetan y las plantillas se aplican a un nuevo proyecto.

    -   Corregido: Se ha mejorado el manejo de la reasignación de la propiedad de los registros.

    -   Corregido: No se permitirá copiar los proyectos que se encuentren en proceso de copia hasta que se completen todas las operaciones de copia.

-   Administración de recursos

    -   Corrección: Ampliar reservas ahora maneja las duraciones cortas correctamente y ya no crea cero horas para reservas ampliadas.

    -   Corregido: La vista de reconciliación ahora se representa cuando la zona horaria del proyecto es +5:30 GMT y la zona horaria del usuario es diferente.

-   Sales

    -   Solucionado: Cuando se elimina un proyecto asignado a una línea de contrato y se asigna un proyecto nuevo, los registros reales del nuevo proyecto no se reevalúan en función delas reglas de facturación y precios definidas en la línea de contrato. Esto se ha corregido en esta versión. Los precios y los registros reales del proyecto recién asignado se revertirán y volverán a crear correctamente según las reglas de precios y facturación de la línea de contrato. Los registros reales del proyecto no mapeado también se reevaluarán y se volverán a crear como consecuencia.

    -   Corregido: Se ha agregado validación adicional al campo **Importe** de una línea de estimación campo para garantizar que los valores nulos no sean persistentes.

    -   Corregido: Cuando los datos reales se han actualizado en un proyecto, se ha agregado un botón de actualización al formulario principal del proyecto para permitir a los usuarios vuelvan a sincronizar los datos reales.

    -   Corregido: cuando los usuarios actualizan de 2.X a 3.X, se permitirán proyectos con un valor NULO para el nombre del proyecto.
