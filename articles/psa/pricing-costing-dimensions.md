---
title: Página principal de dimensiones de precios y costes
description: En este tema se proporciona una descripción general de las dimensiones de precios.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151319"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Página principal de dimensiones de precios y costes

[!include [banner](../includes/psa-now-project-operations.md)]

Las dimensiones utilizadas para establecer el precio y el coste de la mano de obra en organizaciones basadas en proyectos dependen de los siguientes atributos:

- Personas que realizan un trabajo similar a su experiencia, rol o geografía
- Trabajo a realizar similar a su complejidad o hora del día

Dada la naturaleza típica de estos atributos del trabajo y las personas necesarias para realizar el trabajo, existen dos tipos de valores de dimensión de precios disponibles en Project Service Automation: 

- **Conjuntos de opciones**: atributos que son enumeraciones fijas para un conjunto de valores.
- **Valores basados en entidades**: atributos que pueden tener un conjunto variado de valores que son finitos pero que pueden cambiar con el tiempo.

## <a name="pricing-dimensions"></a>Dimensiones de precios

PSA se envía con un conjunto predeterminado de dimensiones de precios. Puede verlos yendo a **Project Service** > **Parámetros**. En el registro de parámetros, en la pestaña **Dimensión de precios basados en importes**, verifique que el rol **msdyn_resourcecategory** y la unidad organizativa de recursos **msdyn_organizationalunit** tenga los campos **Aplicable a ventas** y **Aplicable a costes** establecido en **Sí**. Esto le permitirá configurar el precio y el coste de cada combinación de roles y unidades organizativas.

![Captura de pantalla de los parámetros Project Service con la opción "Aplicable a ventas" resaltada](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Si ha estado utilizando campos listos para usar de rol y unidad organizativa como dimensiones de precios antes de la versión 3 de PSA, no habrá ningún cambio observable. Puede continuar utilizando Project Service como de costumbre. 

Si necesita fijar el precio o el coste de sus recursos mediante atributos adicionales, puede crear campos, entidades y dimensiones personalizados. Para obtener más información, consulte los siguientes temas. Sin embargo, tenga en cuenta que debe completar los procedimientos en el orden que se detalla a continuación:

- [Creación de campos y entidades](create-custom-fields-entities.md)
- [Adición de campos personalizados a la configuración de precios y entidades transaccionales](field-references.md)
- [Configurar campos personalizados como dimensiones de precios ](set-up-pricing-dimensions.md)
- [Actualización de atributos de complemento para incluir nuevas dimensiones de precios](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Precios del tiempo de recursos humanos
La forma en que una organización establece el precio para el tiempo de los recursos humanos es a menudo una consideración estratégica importante que afecta directamente la rentabilidad de la organización. Trabaje con los equipos de finanzas y los directores de práctica cuando su organización esté lista para identificar cómo quiere establecer las tarifas y los costes del tiempo de recursos humanos.

Otras consideraciones para los precios incluyen si se deben reutilizar campos o entidades que actualmente no son dimensiones de precios, pero que se aplican como una dimensión de precios para su organización. Los campos como **Categoría de transacción** (**msdyn_transactioncategory**) y **Recurso que se puede reservar** (**bookableresource**) son ejemplos de dimensiones candidatas. 

Considere si su dimensión de precios debe ser una tabla o un conjunto de opciones. Si prevé cambios en los valores de una dimensión que supere 10 o 12 y necesita atributos adicionales en estos valores, cree una entidad en lugar de un conjunto de opciones. Mantener un conjunto de opciones, como agregar o eliminar valores, requiere un administrador o desarrollador, mientras que la mayoría de los usuarios profesionales pueden agregar nuevas filas a una tabla.

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
