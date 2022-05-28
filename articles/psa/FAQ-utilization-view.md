---
title: Ver el uso imputable de los recursos
description: En este tema se proporciona información acerca de la vista de uso de recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 0f6240a3337eb78496570ddfabc85d431e61d640
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595657"
---
# <a name="view-chargeable-utilization-for-resources"></a>Ver el uso imputable de los recursos

[!include [banner](../includes/psa-now-project-operations.md)]
 
La vista **Uso** de la página **Uso de recursos** de Project Service muestra el uso imputable de cada recurso que se puede reservar. Puesto que la vista se basa en el tablero de programación, encontrará muchas funciones iguales.

> ![Captura de Vista de uso.](media/FAQ-utilization-1.png)
 

El cálculo de uso imputable funciona de la siguiente manera:

   Uso imputable = (Horas reales imputables)/(Capacidad del recurso).

Las celdas representan el uso imputable calculado para el período seleccionado (días, semanas, o meses).

Los colores de cada celda muestran el uso imputable para un recurso comparado con su uso imputable de destino. 

El uso objetivo se puede establecer en cualquier rol predeterminado del recurso o en el propio recurso individual. El cálculo considera el individual para el destino primero y después al rol predeterminado del recurso.

## <a name="set-target-on-a-resource"></a>Definir el objetivo en un recurso

1. Vaya a **Recursos** \> **Recursos**. 
2. Seleccione un recurso para abrir el registro. 
3. En la pestaña **Project Service**, puede establecer el uso objetivo de un recurso.

> ![Captura de pantalla de uso de la pestaña Project Service para establecer uso de destino.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Definir un uso objetivo en un rol

1. Vaya a **Recursos** \> **Roles de recursos**. 
2. Seleccione un rol y abra el registro. 
3. Establezca el uso de destino para el rol.

> ![Captura de pantalla de uso de Roles de recursos para establecer el uso de destino.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcular el uso imputable para un recurso

Para calcular el uso imputable para un recurso, necesitará completar algunos requisitos previos. 

### <a name="set-default-role-for-individual-resource"></a>Establecer el rol predeterminado para un recurso individual

Primero, el uso objetivo se puede establecer en el recurso individual o en roles de recursos. Si va a usar roles de recursos para destinos, cada recurso individual debe tener un rol predeterminado. 

1. Para establecerlo, vaya a **Recursos** \> **Recursos**. 
2. Seleccione un recurso, abra el registro y después seleccione la pestaña **Project Service**. 
3. En la cuadrícula **Rol de recurso**, asegúrese de que haya un rol para el recurso y de que la opción **Es predeterminado** está establecida en **Sí**.
 
### <a name="change-billing-type-for-resource-role"></a>Cambiar el tipo de facturación para el rol de recurso

Los roles de recursos se deben establecer para tener un tipo de facturación **Imputable**. 

1. Vaya a **Recursos** \> **Roles de recursos**. 
2. Abra el registro que desea actualizar y después establezca el valor predeterminado del tipo de facturación como **Imputable**.

### <a name="set-working-hours-for-resource-role"></a>Establecer las horas laborables de un rol de recursos
 
El recurso debe tener horas laborables para el cálculo de capacidad. 

1. Vaya a **Recursos** \> **Recursos**. 
2. Seleccione un recurso para abrir el registro y después seleccione **Mostrar horas laborables**. 
3. Puede actualizar de forma masiva la lista de recursos aplicando una **Plantilla de horas laborables** desde la vista **Lista de recursos**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Solución de problemas de horas reales imputables

Las horas reales imputables se obtienen de la entidad **Datos reales**. Los datos reales con tipo de facturación **Imputable** se incluyen en el cálculo y por este motivo usted debe tener proyectos donde los datos reales sean imputables.

Si no ve uso imputable, estas son algunas cosas que puede comprobar:

- El recurso tiene horas laborables definidas para capacidad.
- El recurso tiene un destino de uso definido de forma individual o tiene un rol predeterminado asignado. El rol tiene un destino de uso definido para él.
- Los datos reales tienen un tipo de facturación **Imputable** para el período para el que está esperando un cálculo de uso. Consulte lo siguiente si ve datos reales con tipos de facturación distintos de imputables:

  - El rol usado en los datos reales tiene un tipo predeterminado de facturación distinto de imputable.
  - El rol en la línea de contrato de proyecto que apoya el proyecto se ha establecido en no imputable.
  - El proyecto no tiene una línea de contrato asociada.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
