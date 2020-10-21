---
title: Definir calendarios de recursos
description: Este tema proporciona información sobre cómo definir los calendarios de horas de trabajo para los recursos en Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961952"
---
# <a name="define-resource-calendars"></a>Definir calendarios de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Cada recurso reservable que trabaja en un proyecto debe tener un calendario de horas de trabajo para definir su disponibilidad. Las horas laborales de los recursos se pueden definir de dos maneras: 

   - Definir reglas de calendario individuales para un recurso
   - Aplicar una plantilla de calendario existente para el recurso

## <a name="define-a-resources-working-hours"></a>Definir las horas laborables de un recurso

1. En el menú **Recursos**, seleccione **Recursos**.
2. En la vista de cuadrícula, seleccione el **Recurso reservable**.
3. En la página **Detalles del recurso**, seleccione la pestaña **Horas Laborables**. De forma predeterminada, el calendario de recursos reservables tiene como valor predeterminado las horas de trabajo de la plantilla de horas de trabajo predeterminada que se define para la organización.
4. Para actualizar el horario laboral, haga clic con el botón derecho en la fecha de inicio de la regla de calendario propuesta a definir. Utilice el menú de reglas de calendario para definir una regla de calendario para un día específico, el resto de la serie o el calendario completo.
5. Una vez seleccionada la opción, puede definir:

    - El día de la semana en el que se aplicará el horario laboral.
    - Las horas laborables de cada día.
    - La zona horaria de la regla de calendario.
    - Si corresponde, también se puede especificar el tiempo no laborable para la regla.

## <a name="applying-a-calendar-template-to-a-resource"></a>Aplicción de un calendario a un recurso

1. En el menú **Recursos**, seleccione **Recursos**.
2. En la vista de cuadrícula, seleccione hasta 25 **Recursos reservables** para actualizar.
3. Seleccione **Establecer calendario** y un cuadro de diálogo le mostrará una lista de plantillas de horas de trabajo disponibles.
4. Seleccione la plantilla que desee utilizar y seleccione **Aplicar**.
