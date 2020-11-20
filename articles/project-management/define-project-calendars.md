---
title: Definir calendarios de proyectos
description: En este tema se proporciona información sobre el uso de un calendario de proyecto para realizar un seguimiento de la programación del proyecto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131679"
---
# <a name="define-project-calendars"></a>Definir calendarios de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Para crear una programación de proyecto, cree una plantilla de calendario de proyecto que defina la cantidad de horas de trabajo por día y los cierres de negocios. Para crear una plantilla de calendario de proyecto, asocie una plantilla de trabajo con el campo **Plantilla de calendario** para el proyecto. Siga estos pasos para crear una plantilla de trabajo.

1. En el panel de navegación izquierdo, seleccione **Recursos**. 
2. En la página de la lista **Recursos**, abra un registro de usuario y, a continuación, seleccione **Mostrar horas laborables**.

  > [!NOTE]
  > Asegúrese de permitir ventanas emergentes en la página del explorador. Esto le permitirá ver las horas de trabajo establecidas para el recurso.
  
3. En la pestaña **Vista mensual** , seleccione **Configurar**. Aparecerá una lista con tres opciones: 

  - Nueva programación semanal
  - Programación de trabajo para un día
  - Indisponibilidad

4. Seleccione **Nueva programación semanal** y, a continuación, establezca las opciones para esta programación del recurso. Puede establecer una programación semanal recurrente, parámetros de horas diarias, cierres comerciales, etc.
5. Establezca el rango de fechas, seleccione **Guardar** y, a continuación, seleccione **Cerrar**. 
6. Vuelva a la página de lista **Recursos** y seleccione el recurso para el que estableció las horas de trabajo. 
7. Seleccione **Establecer calendario como** para establecer la plantilla de trabajo. 
8. En el cuadro de diálogo **Plantilla de trabajo**, introduzca un nombre para la plantilla de trabajo y, a continuación, seleccione **Aplicar**. 

Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.