---
title: Novedades o cambios en la versión de actualización 13, V3, de Project Service Automation
description: En este artículo se proporciona información sobre las novedades y los cambios en Project Service Automation, Update Release 13, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930707"
---
# <a name="project-service-automation-update-release-13-v3"></a>Versión de actualización de Project Service Automation 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA). Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation V3, Update Release 13. Esta versión tiene un número de compilación de V3.10.3.18 y está disponible en la siguiente programación:

- **Disponibilidad general (actualización automática):** noviembre de 2019
- **Actualización automática:** diciembre de 2019


## <a name="update-release-13"></a>Versión de actualización 13 

### <a name="bug-fixes"></a>Solución de errores

- Tiempo y gasto

     - Corregido: La funcionalidad de búsqueda en la página **Aprobación de gastos** no funciona al buscar por propósito de gasto.

- Administración de recursos

     - Corregido: Los números en la conciliación se han actualizado para justificarse a la derecha.
     - Corregido: Los recursos con nombre no se pueden asignar a tareas a través de la pestaña **Programación**.

- Administración del proyecto

     - Corregido: La excepción de referencia nula al asignar un miembro de equipo cuando falta información de configuración en el **TransactionType** para **Unidad** y **DefaultGroup**.

- Sales

     - Corregido: Los registros de tipo de transacción duplicados devuelven un error cuando se crean registros de precios de roles.
     - Corregido: botones adicionales para **Nueva oportunidad**, **Cita**, **Fila para ordenar** y **Añadir producto** son visibles en los comandos de Oportunidades, Presupuestos, Pedidos de productos y la subcuadrícula Líneas basadas en proyectos.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
