---
title: Conocer el estado del proyecto
description: Este tema proporciona información sobre el estado asignado a proyectos en Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965697"
---
# <a name="understand-project-status"></a>Conocer el estado del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


La sección **Estado** de la página **Entidad del proyecto** proporciona un resumen del estado de un proyecto según el coste y el esfuerzo.


## <a name="status-summary-fields"></a>Campos de resumen de estado

- El campo **Estado general del proyecto** es un campo editable que muestra el estado general del proyecto. Este campo utiliza códigos de colores, como verde, amarillo y rojo, para indicar un riesgo creciente. 
- El campo **Comentarios** permite al administrador de proyecto introducir comentarios específicos sobre el estado. 
- El campo **Estado actualizado en fecha de** no se puede editar. El valor de este campo es una marca de tiempo que indica cuándo se actualizó por última vez el estado.
- Los campos **Rendimiento de programación** y **Rendimiento de coste** se establecen desde la cuadrícula de seguimiento. Cuando la programación y la variación de costes para el nodo raíz en la vista **Seguimiento del esfuerzo** son positivas, estos campos se actualizan a **Adelantado**. Cuando la programación y la variación de coste para el nodo raíz son negativas, estos campos se establecen en **Retrasado**.
