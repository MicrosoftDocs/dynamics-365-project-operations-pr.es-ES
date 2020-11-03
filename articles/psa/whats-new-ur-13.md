---
title: Novedades o cambios en la versión de actualización 13, V3, de Project Service Automation
description: Este tema proporciona información sobre las novedades de la versión de actualización 13 de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085108"
---
# <a name="project-service-automation-update-release-13-v3"></a>Versión de actualización de Project Service Automation 13, V3
Nos complace anunciar la última actualización para la aplicación Dynamics 365 Project Service Automation (PSA). Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite el Centro de administración para Dynamics 365 en línea y vaya a la página de soluciones para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 13. Esta versión tiene un número de compilación de V3.10.3.18 y está disponible en la siguiente programación:

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
     - Corregido: Los botones adicionales para **Nueva oportunidad** , **Oferta** , **Línea de pedido** y **Agregar producto** son visibles en comandos para Oportunidades, Ofertas, Pedidos de productos y la subcuadrícula de líneas basadas en proyectos.


