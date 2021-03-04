---
title: Programar recursos para un proyecto
description: Cómo programar recursos para un proyecto en Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150464"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Programar recursos para un proyecto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Puede comprobar la disponibilidad de recursos para obtener una visión general de lo reservados que están sus recursos o bien puede filtrar la vista por conocimientos, equipo, ubicación y otras opciones.  
  
El tablero de programación muestra una lista de recursos y su disponibilidad. Seleccione un modo de vista para mostrar disponibilidad por **Horas**, **Día**, **Semana** o **Mes**.  
  
Antes de usar al tablero de programación, es importante configurarlo. Para obtener más información, consulte [Configurar la tabla de programación (Field Service o Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Si usa una versión anterior, para disponibilidad de recursos, consulte [Ver disponibilidad de recursos](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Para usar la funcionalidad de reserva del tablero de programación, geocodificación y servicios de ubicación, debe activar los mapas.  
> 
> 1. En el menú principal, seleccione **Programación de recursos** > **Administración**.  
> 2. Haga clic en **Parámetros de programación**.  
> 3. Abra el registro y desplácese hacia abajo hasta la sección **Resource Scheduling Optimization**.  
> 4. En el campo **Conectar con Mapas**, elija **Sí**.  
> 5. Acepte la términos y guarde el registro.  
> 6. En el menú principal, seleccione **Project Service** > **Tabla de programación**. A partir de aquí, hay varias formas diferentes de programar manualmente un requisito de reserva. Elija el método que funcione para usted.
  
## <a name="find-available-resources"></a>Buscar recursos disponibles

1.  De la lista **Requisitos de reserva**, haga clic con el botón secundario en una reserva no programada y seleccione una de las acciones siguientes:  
  
- Elija **Buscar disponibilidad - Recurso actual** para buscar un recurso disponible en la lista de recursos del tablero de programación.  
- Elija **Buscar disponibilidad - Todos los recursos** para buscar un recurso disponible en los recursos del sistema  
   > [!NOTE]
   >  Al hacerlo, los filtros mostrarán las opciones del requisito de reserva seleccionado.  
  
2. Cuando vea un intervalo disponible, haga clic con el botón secundario en el intervalo de tiempo en el tablero de programación y elija **Reservar aquí**. O bien, arrastre y coloque el requisito de reserva al intervalo de tiempo disponible.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Reserve un recurso mediante la vista diaria y busque quién tiene pocas reservas
  
1.  En el tablero de programación, seleccione **Modo de vista** y **Días**.  
  
    Esto muestra una vista de cuadrícula del número de horas que está reservado un recurso por día y qué días está libre.  
  
2.  Haga clic en el nombre del recurso que desea para reservar y seleccione **Reservar**.  
  
3.  En el cuadro de diálogo **Reserva de recursos (crear)**, elija el proyecto para el que desea reservar el recurso junto con el método de reserva y las horas de inicio y finalización.  
  
4.  Cuando esté listo, seleccione **Reservar**.  
  
## <a name="view-to-the-schedule-board"></a>Ver el tablero de programación
  
1.  Seleccione un requisito de reserva no programado desde la lista de la parte inferior.  
  
2.  Arrastre el requisito de reserva a un intervalo de tiempo/recurso disponible en el tablero de programación.  
  
3.  Cuando haya terminado, seleccione **Reservar**.  
  
### <a name="additional-resources"></a>Recursos adicionales  
 [Guía del administrador de recursos](../psa/resource-manager-guide.md)
