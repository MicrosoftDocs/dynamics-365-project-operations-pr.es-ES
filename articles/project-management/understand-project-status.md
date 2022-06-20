---
title: Conocer el estado del proyecto
description: Este artículo proporciona información acerca del estado asignado a proyectos en Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923623"
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