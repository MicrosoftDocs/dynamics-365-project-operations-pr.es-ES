---
title: Precios del proyecto
description: En este tema se proporciona información sobre cómo funcionan los precios en Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: 176b84671ca0b5b998c44be4f306d1f8f5200c72
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148934"
---
# <a name="project-pricing"></a>Precios del proyecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation amplía la entidad Lista de precios en Dynamics 365 Sales. 

## <a name="key-entities"></a>Entidades clave

Las listas de precios incluyen la información que proporcionan cuatro entidades distintas:

- **Lista de precios**: esta entidad almacena información sobre el contexto, la divisa, la validez de fecha y la unidad de tiempo para el cálculo de precios del tiempo. El contexto indica si es una lista de precios expresa índices de costes o índices de ventas. 
- **Divisa**: esta entidad almacena la divisa de los precios de la lista de precios. 
- **Fecha**: esta entidad se usa cuando el sistema intenta especificar un precio predeterminado en una transacción. Para el cálculo de precios en PSA, se selecciona la lista de precios cuya validez de fecha incluye la fecha en que se produjo la transacción. Si el cálculo de precios de PSA encuentra más de una lista de precios válida para la fecha de transacción adjunta a la unidad organizativa, el contrato o la oferta relacionada, no se establecerá ningún precio como predeterminado. 
- **Tiempo**: esta entidad almacena la unidad de tiempo en la que se expresan los precios, como, la tarifa por horas o días. 

La entidad Lista de precios dispone de tres tablas para almacenar precios:

  - **Precio de rol**: esta tabla almacena una tarifa para una combinación de valores del rol y unidad organizativa y se usa para configurar precios basados en roles para recursos humanos.
  - **Precio de categoría de transacciones**: esta tabla almacena precios por categoría de transacciones y se usa para configurar precios de categoría de gastos.
  - **Elementos de lista de precios**: esta tabla almacena los precios de los productos del catálogo.

> ![Configuración de precios mediante una lista de precios](media/basic-guide-12.png)
 
La lista de precios es una lista de tarifas. Las listas de tarifas son una combinación de la entidad Lista de precios y las filas relacionadas de las tablas Precio de rol, Precio de categoría de transacciones y Elementos de lista de precios.

## <a name="resource-roles"></a>Roles de recursos

El término *rol de recurso* hace referencia al conjunto de conocimientos, competencias y certificaciones que una persona necesitará para poder realizar un conjunto específico de tareas en un proyecto.

El tiempo de recursos humanos se suele ofertar en función del rol que desempeña un recurso en un proyecto específico. Para el tiempo de recursos humanos, PSA admite el cálculo de costes y la facturación basados en el rol de recurso. El precio del tiempo se puede establecer en cualquier unidad de la unidad de venta **Tiempo**.

La unidad de venta **Tiempo** se crea al instalar PSA. Tiene la unidad predeterminada **Hora**. No puede eliminar, cambiar el nombre ni editar los atributos de la unidad de venta **Tiempo** o de la unidad **Hora**. No obstante, puede agregar otras unidades a la unidad de venta **Tiempo**. Si intenta eliminar la unidad de venta **Tiempo** o la unidad **Hora**, es posible que se produzcan errores en la lógica de negocios de PSA.

> ![Configuración de precios por rol](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Categorías de transacción y categorías de gastos

Los viajes y los demás gastos en los que incurren los consultores de proyectos suelen facturarse al cliente. PSA permite calcular el precio de las categorías de gastos mediante listas de precios. Los vuelos, las habitaciones de hotel y el alquiler de vehículos son ejemplos de categorías de gastos. Cada línea de la lista de precios de gastos especifica el cálculo de precios de una categoría de gastos específica. Para el cálculo de precios de categorías de gastos, PSA admite los tres métodos de cálculo de precios siguientes:

- **De coste**: el coste del gasto se factura al cliente y no se aplica ningún incremento.
- **Porcentaje de incremento**: el porcentaje sobre el coste real se factura al cliente. 
- **Precio por unidad**: se establece un precio de facturación para cada unidad de la categoría de gastos. El importe que se factura al cliente se calcula en función del número de unidades de gasto de las que informa el consultor. El kilometraje usa el método de cálculo de precios Precio unitario. Por ejemplo, la categoría de gasto de kilometraje se puede configurar para a 30 dólares estadounidenses (USD) por día o a 2 USD por milla. Cuando un consultor informa de kilometraje en un proyecto, el importe para facturar se calcula en función del número de millas de las que informa el consultor.

> ![Configuración del cálculo de precios para las categorías de gastos](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Cálculo de precios de ventas de proyecto y reemplazos

Para los contratos y las ofertas de proyecto, la lista de precios de proyectos cuenta con un patrón de reemplazo de precios distinto que el de la lista de precios de productos. En una línea de oferta basada en un catálogo de productos, puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta, porque cada línea de la oferta apunta exactamente a un elemento del catálogo. Sin embargo, en una línea de oferta basada en un proyecto, no puede reemplazar el precio de los roles y las categorías directamente en la línea de oferta. Para admitir los dos patrones de reemplazo distintos, PSA ha introducido una nueva asociación de lista de precios: la lista de precios de proyecto.

> [!NOTE]
> Se recomienda disponer de una lista de precios independiente para sus recursos de proyecto y sus elementos del catálogo debido a las diferencias de comportamiento entre las dos al reemplazar el cálculo de precios.

Cada una de las siguientes entidades puede tener una o varias listas de precios de ventas asociadas para el cálculo de precios de proyecto:

- Cliente (cuenta) 
- Oportunidad 
- Oferta 
- Contrato de proyecto

La asociación de estas entidades a una lista de precios se indica con las listas de precios de proyecto. Puede asociar una o más listas de precios a las entidades de ventas Cliente, Oportunidad, Oferta y Contrato de proyecto.

La lista de precios de proyecto predeterminada no se introduce automáticamente en los registros de cliente. Sin embargo, puede adjuntar manualmente una lista de precios de proyecto al registro de cliente. No obstante, deberá adjuntar manualmente una lista de precios de proyecto solo cuando tenga un acuerdo de precios personalizado con el cliente. 

Cuando una lista de precios de proyecto se adjunta una entidad de ventas, PSA valida la información siguiente:

- Si la lista de precios tiene un contexto de **Ventas**. 
- Si la divisa de la lista de precios coincide con la divisa del cliente. 

En un contrato de proyecto, PSA usa el orden de precedencia siguiente para establecer automáticamente las listas de precios de proyecto relacionadas:

1. Oferta
2. Oportunidad
3. Cliente 
4. Configuración global de PSA

Cuando una lista de precios de proyecto se especifica de forma predeterminada, PSA valida que la divisa coincida con la divisa del cliente y que las listas de precios predeterminadas que se han especificado tengan un contexto de **Ventas**.

Puede asociar varias listas de precios de proyecto a las entidades Cliente, Oportunidad, Oferta y Contrato de proyecto. Esta funcionalidad admite precios predeterminados con fecha específica para contratos de proyectos de larga duración en los que es posible que necesite más de una lista de precios para las actualizaciones de precios que se producen debido a la inflación. Sin embargo, si las listas de precios que asocie con las entidades Cliente, Oportunidad, Oferta o Contrato de proyecto tienen validez de fecha que se solapan, es posible que los precios predeterminados sean incorrectos. Por lo tanto, debe asegurarse de que no se asocian a dichas entidades listas de precios de proyecto que tienen fechas de validez que se solapan.

### <a name="deal-specific-price-overrides"></a>Reemplazos de precios específicos de operaciones

En PSA, puede crear reemplazos específicos de operaciones para determinados precios de las listas de precios de proyecto que se especifican de manera predeterminada en una oferta o contrato de proyecto.

De forma predeterminada, un contrato de proyecto obtiene siempre una copia de la lista de precios de ventas principal en lugar de un vínculo directo a la lista. Este comportamiento ayuda garantizar que los acuerdos de precios que se hagan con un cliente para una declaración de trabajo (SOW) no cambien si se modifica la lista de precios principal.

Sin embargo, en una oferta, puede usar una lista de precios principal. Como alternativa, puede copiar una lista de precios principal y editarla para crear una lista de precios personalizada aplicable solo a esa oferta. Para crear una nueva lista de precios específica para una oferta, en la página **Oferta**, seleccione **Crear precios personalizados**. Solo podrá obtener acceso a la lista de precios de proyecto específica de operaciones desde la oferta. 

Al crear una lista de precios de proyecto personalizada, solo se copian los componentes del proyecto de la lista de precios. Es decir, se crea una nueva lista de precios como copia de la lista de precios de proyecto existente adjunta a la oferta. Dicha nueva lista de precios solo incluye precios de rol relacionados y precios de categoría de transacciones.

> ![Visualización y configuración de precios personalizados para un contrato de proyecto](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Seguimiento de costes

PSA realiza un seguimiento de los costes por el uso de tiempo de recursos humanos en proyectos. También realiza un seguimiento de los costes de otros gastos en los que se incurre durante el proyecto, como, por ejemplo, los gastos de viaje.

Al igual que los índices de facturación, los índices de costes de recursos humanos también se configuran con listas de precios. A continuación se describen las principales diferencias de comportamiento de las listas de precios de costes y las listas de precios de ventas:

- El índice de costes de un recurso no se puede reemplazar en un proyecto, un contrato o una oferta específicos. Sin embargo, los índices de facturación se pueden reemplazar por operación si los cambios son específicos a la naturaleza de la operación. 

- A continuación se describe el orden que se usa para resolver una lista de precios de coste:

    1. Lista de precios de coste adjunta a la unidad organizativa.
    2. Lista de precios de coste adjunta a los parámetros de servicio del proyecto. Puesto que las listas de precios de coste en diferentes divisas se pueden adjuntar a los parámetros de servicio del proyecto, PSA busca coincidencias de divisa entre la divisa de la unidad organizativa de contratación del proyecto, el contrato o la oferta, y la divisa de la lista de precios de coste.
    3. Para los gastos, los métodos de cálculo de precios De coste e Incremento por encima del coste no se aplican a las listas de precios de coste. Aunque se utilicen estos métodos de cálculo de precios en las líneas de la lista de precios de coste para configurar los costes de categorías de transacciones, el sistema los omite y no se especifica ningún precio de coste predeterminado.
