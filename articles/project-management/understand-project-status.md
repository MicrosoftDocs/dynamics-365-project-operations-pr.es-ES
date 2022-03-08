---
title: Conocer el estado del proyecto
description: Este tema proporciona información sobre el estado asignado a los proyectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 47d71b945a2d5e7aa41d2ac3731ac4a5d3051ce279229794e31c9673f688130e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997042"
---
# <a name="understand-project-status"></a>Conocer el estado del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


La sección **Estado** de la página **Entidad del proyecto** proporciona un resumen del estado de un proyecto según el coste y el esfuerzo.


## <a name="status-summary-fields"></a>Campos de resumen de estado

- El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto. Este campo utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente. 
- El campo **Comentarios** permite al jefe de proyecto introducir comentarios específicos sobre el estado. 
- El campo **Estado actualizado en fecha de** no se puede editar. El valor de este campo es una marca de tiempo que indica cuándo se actualizó por última vez el estado.
- Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la cuadrícula de seguimiento. Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, estos campos se actualizan a **Adelantado**. Cuando la programación y la variación de coste para el nodo raíz son negativas, estos campos se establecen en **Retrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]