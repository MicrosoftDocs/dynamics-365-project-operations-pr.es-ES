---
title: Página principal de dimensiones de precios y costes
description: En este tema se proporciona una descripción general de las dimensiones de precios.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755987"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Página principal de dimensiones de precios y costes

Las dimensiones que se utilizan en los recursos humanos para establecer los precios y los costes se dividen en dos categorías:

- Personas
- Trabajo previsto

Debido a esto, hay dos tipos de valores de dimensión de precios disponibles en Project Service Automation (PSA): 

- **Conjuntos de opciones**: dimensiones que son enumeraciones fijas para un conjunto de valores.
- **Valores basados en entidad**: dimensiones que son enumeraciones fijas para un conjunto de valores.

## <a name="pricing-dimensions"></a>Dimensiones de precios

PSA se envía con un conjunto predeterminado de dimensiones de precios. Puede verlos yendo a **Project Service** > **Parámetros**. En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**. Esto le permitirá configurar el precio y el coste de cada combinación de roles y unidades organizativas.

![Captura de pantalla de los parámetros Project Service con la opción "Aplicable a ventas" resaltada](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Si ha estado utilizando campos listos para usar de rol y unidad organizativa como dimensiones de precios antes de la versión 3 de PSA, no habrá ningún cambio observable. Puede continuar utilizando Project Service como de costumbre. 

Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados. Para obtener más información, consulte los siguientes temas. Sin embargo, tenga en cuenta que debe completar los procedimientos en el orden que se detalla a continuación:

- [Creación de campos y entidades](create-custom-fields-entities.md)
- [Adición de campos personalizados a la configuración de precios y entidades transaccionales](field-references.md)
- [Configuración de campos personalizados como dimensiones de precios](set-up-pricing-dimensions.md)
- [Actualización de atributos de complemento para incluir nuevas dimensiones de precios](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Precios del tiempo de recursos humanos
La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización. Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.

Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización. Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas. 

También debe considerar si su dimensión de precios debe ser una tabla o un conjunto de opciones. Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, puede crear una entidad en lugar de un conjunto de opciones. Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios pueden agregar nuevas filas a una tabla.

El siguiente ejemplo muestra las tasas de facturación que se configuran en función del rol y la unidad organizativa de recursos a la que pertenece el recurso. Las tasas de costes generalmente se basan en la banda salarial del empleado y la unidad organizativa a la que pertenecen. En este ejemplo, las tablas de tasa de facturación y tasa de coste tendrán el siguiente aspecto.

**Tasas de facturación de ejemplo**

| Rol        | Unidad organizativa    |Unidad      |Precio      |Divisa  |
| ------------|-------------|----------|----------:|----------|
| Desarrollador   | Contoso US  |Hour | 200|USD     |
| Desarrollador   | Contoso India |Hour|   112|USD     |


**Tasas de costes de ejemplo**

| Banda salarial     | Unidad organizativa    |Unidad      |Precio      |Divisa  |
| ----------------|-------------|----------|----------:|----------|
| Mi empresa_Banda1 | Contoso US  |Hour | 145|USD     |
| Mi empresa_Banda2 | Contoso India |Hour|   67|USD     |
