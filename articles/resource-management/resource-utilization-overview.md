---
title: Información general de utilización de recursos
description: En este tema se proporciona información acerca de la vista de uso de recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401397"
---
# <a name="resource-utilization-overview"></a>Información general de utilización de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los recursos pueden tener un uso facturable objetivo. Este uso objetivo se define como un atributo en el rol predeterminado de un recurso o se establece en el registro del recurso individual que se puede reservar. Los cálculos de uso se basan en las horas reales informadas por los recursos mediante entradas de tiempo aprobadas.

Se utilizan las siguientes fórmulas para calcular el uso:

  - Uso facturable = Horas reales imputables ÷ Capacidad de recursos
  - Uso no facturable = Tiempo real con Id. de tipo de facturación = No imputable, Complementario o No disponible ÷ Capacidad de recursos
  - Interno = Tiempo real sin contrato de venta ÷ Capacidad de recursos
  - Capacidad de recursos = Horas de trabajo de recursos - Fuera de la oficina - Días no laborables

Puede encontrar la vista **Uso de recursos** en el panel **Recursos**.

Cada celda de la cuadrícula representa el porcentaje de uso facturable del recurso en un período, como un día, una semana o un mes. Se usan las siguientes fórmulas para colorear las celdas:

  - **Verde**: uso facturable >= uso de destino del recurso.
  - **Amarillo**: uso de destino – 20 <= uso facturable < uso de destino.
  - **Rojo**: uso facturable < uso de destino – 20.

Puesto que la vista **Uso de recursos** se basa en el tablero de programación, puede usar las capacidades de filtrado del tablero de programación para filtrar sus resultados.

La cuadrícula requiere que establezca un uso objetivo en el rol o en el recurso individual. Para realizar esta configuración, vaya a **Recursos** > **Roles de recursos**.

Además, se debe asignar un rol predeterminado a cada recurso que se puede reservar. Vaya a **Recursos** > **Recursos**. En la pestaña **Project Service**, verifique que se haya definido un rol de recurso y que el campo **Es predeterminado** esté establecido en **Sí**. Puede agregar roles adicionales en los que **Es predeterminado** = **No**. El rol en el que **Es predeterminado** = **Sí** se usa para evaluar el uso del recurso en relación el objetivo para ese rol.

En la pestaña **Project Service** también puede establecer un uso objetivo individual para el recurso. El cálculo de uso utiliza después ese uso objetivo para evaluar el objetivo del recurso en lugar del objetivo del rol predeterminado del recurso.

El uso solo se muestra para un recurso solo si ese recurso ha aprobado el tiempo imputable durante el período que se muestra en la cuadrícula.
