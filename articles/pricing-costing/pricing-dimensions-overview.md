---
title: Información general de dimensiones de precios
description: En este tema se proporciona información sobre las dimensiones de Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005002"
---
# <a name="pricing-dimensions-overview"></a>Información general de dimensiones de precios

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las dimensiones que se utilizan en los recursos humanos para establecer los precios y los costes se dividen en dos categorías:

- Personas
- Trabajo previsto

Debido a esto, hay dos tipos de valores de dimensión de precios disponibles:

- **Conjuntos de opciones**: dimensiones que son enumeraciones fijas para un conjunto de valores.
- **Valores basados en entidad**: dimensiones que son enumeraciones fijas para un conjunto de valores.

## <a name="pricing-dimensions"></a>Dimensiones de precios

Dynamics 365 Project Operations se envía con un conjunto predeterminado de dimensiones de precios. Puede ver estas dimensiones de precios yendo a **Project Operations** > **Parámetros**. En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**. Con estos cambios habilitados, puede configurar el precio y el coste de cada combinación de roles y unidades organizativas.

![Captura de pantalla de los parámetros Project Service con la opción "Aplicable a ventas" resaltada](media/PS-OOB-parameters.png)

Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados. Para obtener más información, vea los siguientes temas: 
  
  > [!NOTE]
  > Los procedimientos deben completarse en el orden en que se enumeran.

1. [Crear una solución para dimensiones de precios personalizadas](../sales/create-solution-custompd.md)
2. [Crear campos y entidades personalizados](create-custom-fields-entities-pricing-dimensions.md)
3. [Agregar de campos personalizados a la configuración de precios y entidades transaccionales ](add-custom-fields-price-setup-transactional-entities.md)
4. [Configurar campos personalizados como dimensiones de precios ](set-up-custom-fields-pricing-dimensions.md)
5. [Actualización de atributos de complemento para incluir nuevas dimensiones de precios](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Precios del tiempo de recursos humanos
La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización. Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.

Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización. Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas. 

Considere si su dimensión de precios debe ser una tabla o un conjunto de opciones. Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, puede crear una entidad en lugar de un conjunto de opciones. Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios pueden agregar nuevas filas a una tabla.

El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso. Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen. En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.

**Tasas de facturación de ejemplo**

| Rol        | Unidad organizativa    |Unidad      |Precio      |Moneda  |
| ------------|-------------|----------|----------:|----------|
| Desarrollador   | Contoso EE. UU.  |Hora | 200|USD     |
| Desarrollador   | Contoso India |Hora|   112|USD     |


**Tasas de costes de ejemplo**

| Banda salarial     | Unidad organizativa    |Unidad      |Precio      |Moneda  |
| ----------------|-------------|----------|----------:|----------|
| Mi empresa_Banda1 | Contoso EE. UU.  |Hora | 145|USD     |
| Mi empresa_Banda2 | Contoso India |Hora|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]