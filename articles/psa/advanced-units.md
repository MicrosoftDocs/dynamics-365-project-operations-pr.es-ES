---
title: Unidades y grupos de unidades
description: En este tema se proporciona información sobre las unidades y las unidades de venta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145604"
---
# <a name="unit-groups-and-units"></a>Unidades y grupos de unidades

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Las unidades y las unidades de venta son entidades básicas en Microsoft Dynamics 365. Una unidad es una unidad de medida sencilla y las unidades múltiples se pueden agrupar en unidades de venta. A veces se hace referencia a las unidades de venta como programas de unidad en la interfaz de usuario de Dynamics 365. 

A continuación se muestran algunos ejemplos de unidades y unidades de venta:
 
- **Unidad de venta**: Distancia 
    - **Unidades**: Milla, Kilómetro, etc.
- **Unidad de venta**: Tiempo
    - **Unidades**: Hora, Día, Semana, etc. 

Cuando se configuran varias unidades en una unidad de venta, también hay que configurar un factor de conversión entre ellas designando la primera unidad que se configura como unidad principal o predeterminada para la unidad de venta. 

Por ejemplo, en una unidad de venta **Tiempo** , si configura **Hora** como la primera unidad, el sistema designará la unidad **Hora** como predeterminada. Si la siguiente unidad que se configura es **Día**, debe configurar un factor de conversión de **Día** a **Hora**. Si se agrega a continuación la unidad **Semana** como tercera unidad, debe configurar un factor de conversión para **Semana** con respecto a las unidades **Día** u **Hora**. 

La imagen siguiente muestra un ejemplo de configuración para la unidad **Día**, donde el campo **Cantidad** muestra el número de horas que hay en un día, y para la unidad **Semana**, donde el campo **Cantidad** muestra el número de días que hay en una semana.

> ![Unidad de venta: página de información](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Uso de unidades y unidades de venta

Dynamics 365 Project Service Automation utiliza unidades y unidades de venta para procesar las estimaciones y las entradas de gastos y tiempo. 

Para los gastos, cada categoría de gastos tiene una unidad y una unidad de venta predeterminadas. Estos valores se especifican como valores predeterminados en las entradas de lista de precios para las categorías de gastos. 

Por ejemplo, supongamos que tiene una categoría de gastos con el nombre **Kilometraje**. Esta tiene una unidad de venta con el nombre **Distancia** y una unidad predeterminada con el nombre **Milla**. Si configura la unidad de venta **Distancia** para que tenga dos unidades (**Milla** y **Kilómetro**), podrá establecer dos precios para la categoría **Kilometraje** en una lista de precios: precio por milla y precio por kilómetro.

| Categoría de gastos  | Unidad de venta  | Unidad      | Método de cálculo de precios  | Precio unitario  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometraje           | Distancia      | Milla      | Precio unitario    | 10 USD            |
| Kilometraje           | Distancia      | Kilómetro | Precio unitario    |  6 USD            |

Al especificar un gasto en un proyecto, el sistema determina el precio al combinar la categoría y la unidad del gasto. 

| Descripción del gasto        | Categoría de gastos  | Unidad  | Cantidad  | Precio unitario   |
|----------------------------|---------------------|-------|-----------|----------------|
| Recorrido hasta la ubicación del cliente | Kilometraje             | Milla  | 10        | 10 USD         |

Para el tiempo, cada encabezado de la lista de precios tiene el campo **Unidad de tiempo predeterminada**. El valor se establece cuando se crea el encabezado de la lista de precios. A continuación, esta unidad se usa para establecer todos los precios basados en roles en dicha lista de precios.

Las líneas de estimación del campo **Tiempo en oferta** se pueden expresar en cualquier unidad de tiempo. Sin embargo, las líneas de estimación de entradas de tiempo y proyectos solo pueden utilizar la unidad de tiempo **Hora**. Si la unidad de la entrada de tiempo o estimación no coincide con la unidad de la línea de la lista de precios para dicho rol, el sistema convertirá el precio a las unidades definidas en la estimación del proyecto o la transacción real del proyecto.

El siguiente ejemplo se muestra cómo usa PSA la unidad de venta, las unidades y los factores de conversión.
- Unidades de medida

   - **Unidad de venta**: Tiempo 
   - **Unidades**: Hora 
    
    - **Día**: factor de conversión de 8 horas       
    - **Semana**: factor de conversión de 40 horas  
        
- Configuración de la lista de precios en el proyecto A:

    - **Nombre**: Precios de venta del Reino Unido de 2016 
    - **Unidad de tiempo predeterminada**: Día 
    - **Divisa**: GBP

| Rol      | Unidad de venta | Unidad | Unidad organizativa | Precio   |
|-----------|------------|------|---------------------|---------|
| Desarrollador | Time       | Day  | Contoso Reino Unido          | 800 GBP |

### <a name="time-entry"></a>Entrada de tiempo

La siguiente tabla muestra la transacción resultante de ventas que crea PSA para un proyecto de tres horas.


| Proyecto   | Tarea    | Rol      | Cantidad | Unidad  | Precio unitario | Importe de ventas sin facturar |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Proyecto A | Diseño  | Desarrollador | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Preguntas frecuentas acerca de la unidad de tiempo

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>¿Realiza PSA la conversión a diferentes unidades en el caso de los gastos?
Núm. La conversión de unidades solo se utiliza con el tiempo. Para los gastos, si el sistema no puede encontrar un precio para la combinación de la categoría de gastos y la unidad, el precio que se establece en 0,00 de forma predeterminada.

### <a name="why-does-psa-convert-time-units"></a>¿Por qué convierte PSA las unidades de tiempo?
En algunos países o regiones, hay requisitos legales que exigen que los índices de facturación estén configurados en días. La negociación de precios y descuentos durante el ciclo de oferta se realiza utilizando los índices de día de cada rol facturable. La estimación de programación y la entrada de tiempo se hace en horas. PSA convierte las unidades de tiempo para dar soporte a esta diferencia en las unidades de tiempo.

### <a name="can-time-units-be-changed-on-project-estimates"></a>¿Se pueden cambiar las unidades de tiempo en las estimaciones de proyecto?
Núm. Actualmente, la estimación de programación solo se puede hacer en horas y no se puede cambiar.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>¿Es posible editar, eliminar y agregar las unidades y las unidades de venta?
Sí. A excepción de la unidad de venta **Tiempo** y la unidad **Hora**, todas las unidades se pueden eliminar o editar y también es posible agregar nuevas unidades. En PSA, la unidad de venta **Tiempo** y la unidad **Hora** no pueden eliminarse. Sin embargo, se pueden actualizar con un texto traducido para el campo **Nombre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]