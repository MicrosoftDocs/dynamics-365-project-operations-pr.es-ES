---
title: Configurar tarifas de costos laborales
description: Este tema proporciona información sobre cómo configurar tarifas para el costo de la mano de obra Operaciones del proyecto
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 605bf2a578528117a6ef70614a8e5ff5a3fc300c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274794"
---
# <a name="set-up-labor-cost-rates"></a>Configurar tarifas de costos laborales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Cada lista de precios tiene un conjunto de tarifas laborales (precios de función) que se alinean con el contenido y la fecha de vigencia de la lista de precios.

1. Cree una lista de precios y en la pestaña **Precio del rol**, en la subcuadrícula, seleccione **Nuevo rol**.
2. En la página **Creación rápida**, seleccione el rol y la unidad organizativa.
3. Especifique cualquier otra información obligatoria del campo.

La siguiente tabla incluye algunos de los campos que son importantes al crear tarifas de mano de obra en una lista de precios de costo.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| Rol | Pestaña **General** y páginas **Creación rápida** | Seleccione el rol a la que se aplica la tasa de coste. | El rol en la estimación entrante o real se comparará con esta línea para predeterminar el coste del rol. |
| Empresa de dotación de recursos | Pestaña **General** y páginas **Creación rápida** | Seleccione la entidad jurídica a la que está asignado el rol. Por ejemplo, un desarrollador de Fabrikam India o un desarrollador de Fabrikam USA. | La compañía de recursos en la estimación entrante o real se comparará con esta línea para predeterminar la tarifa de coste del rol. |
| Unidad de dotación de recursos | Pestaña **General** y páginas **Creación rápida** | Seleccione la unidad organizativa o división de la empresa desde donde se utilizará este rol. Por ejemplo, un desarrollador de la división de robótica de Fabrikam India o un desarrollador de la división de software de Fabrikam USA. | La unidad de recursos en la estimación entrante o real se comparará con esta línea para predeterminar el de coste del rol. |
| Precio | Pestaña **General** y páginas **Creación rápida** | Configure la tarifa de coste para el rol, empresa de recursos y combinación de unidad de recursos. Por ejemplo, un desarrollador de Fabrikam India cuesta 1000 INR o un desarrollador de Fabrikam USA cuesta 150 USD. | El precio es la tarifa de coste que se establece por defecto en el costo unitario del estimado entrante o línea actual de la clase de transacción **Hora**. |
| Divisa | Pestaña **General** y páginas **Creación rápida** | De forma predeterminada, el valor de la moneda proviene de la moneda en el encabezado de la lista de precios de costo, pero puede anularse. Por ejemplo, un desarrollador de Fabrikam India cuesta 1000 INR. Un desarrollador de Fabrikam USA cuesta 150 USD. | Esta moneda predetermina el costo unitario del entrante de la línea de coste actual para la clase de transacción **Hora**. En una estimación de proyecto, el valor de la moneda se convierte a la moneda del proyecto y se muestra en la vista por fases de la estimación. |
| Programación de unidad | Pestaña **General** y páginas **Creación rápida** | La programación unitaria tiene como valor predeterminado el Tiempo y no se puede cambiar en la entidad Precio de rol porque se utilizan tarifas rápidas por unidades de tiempo. | Esto no afecta a la funcionalidad. |
| Unidad | Pestaña **General** y páginas **Creación rápida** | De forma predeterminada, el valor sale del campo **Unidad de tiempo** en el encabezado de la lista de precios de coste. El valor se puede sobrescribir. Por ejemplo, un desarrollador de Fabrikam India cuesta 1000 INR por **Día de India**. Un desarrollador de Fabrikam USA cuesta 150 USD por **Día de EE.UU.**. | El sistema utiliza el sistema de unidades y conversión en unidades base para calcular un coste unitario para calcular el precio predeterminado por unidad en una estimación entrante o línea real. Por ejemplo, una estimación es de 10 **Días de la India** de trabajo para un desarrollador de la India, y la unidad, **Día de la india** se define como 10 horas. Al calcular el costo de esa línea de estimación, la aplicación calcula el costo unitario en la estimación como: 1000 INR / 10 horas = 100 INR por hora que se convierte en USD y se muestra como el costo unitario en la página **Estimaciones del proyecto**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Precios de transferencia y costos de recursos fuera de su división o entidad legal

En las empresas basadas en proyectos, es común utilizar empleados de diferentes entidades legales o divisiones en los proyectos. Un proyecto puede ser ejecutado por una entidad legal, pero los empleados o consultores que trabajan en el proyecto pueden provenir de la misma entidad legal o de una diferente, o puede haber una combinación de ambas. En Dynamics 365 Project Operations, la entidad jurídica propietaria de la entrega del proyecto es la **Empresa propietaria** y la división propietaria de la entrega es la **Unidad de contratación**. Otras entidades legales que aportan recursos son las **Empresas de recursos** y las divisiones que proporcionan recursos son las **Unidades de recursos**. En la mayoría de los países, las empresas están obligadas a garantizar que la entidad jurídica o división que proporciona los recursos cobre a la empresa propietaria y a la unidad contratante por el uso de los recursos.

Por ejemplo, la corporación Fabrikam debe asegurarse de que Fabrikam India-Robotics haya negociado una hoja de tarifas de costos con Fabrikam US-Robotics o Fabrikam UK-Robotics.

Un desarrollador de Fabrikam India-Robotic cobra 100 $ cuando se presta a Fabrikam US-Robotics y 150 $ cuando se presta a Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Configurar costes para recursos externos

1. Cree una lista de precios de costo llamada, *Tarifas de costes de Fabrikam US-Robotics* y establezca un rango de fecha de vigencia.
2. En la lista de precios de costes, configure las tarifas utilizando la información de la siguiente tabla. 

| Rol | Empresa de dotación de recursos | Unidad de dotación de recursos | Índice de coste |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India-Robotics | 100 USD |
| Developer | Fabrikam Filipinas | Fabrikam Filipinas-Robotics | 90 $ |
| Developer | Fabrikam US | Fabrikam US-Robotics | 150 $ |

3. Adjunte esta lista de precios de costes a la unidad organizativa Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurar precios de transferencia para un recurso en la moneda apropiada 

En Operaciones de proyecto, los precios de los recursos se pueden configurar en cualquier moneda. La moneda predeterminada es la que está en el encabezado de la lista de precios, pero se puede cambiar.

Usando el ejemplo para configurar el precio de transferencia, la información podría cambiarse a:

La corporación Fabrikam debe asegurarse de que Fabrikam India-Robotics haya negociado una tarifa de costes con Fabrikam US-Robotics o Fabrikam UK-Robotics.

Un desarrollador de Fabrikam India-Robotics cuesta 5000 INR cuando se presta a Fabrikam US-Robotics y 5500 INR cuando se presta a Fabrikam UK-Robotics.

En la lista de precios de costes de Fabrikam US-Robotics, las tarifas de costes se pueden expresar como:

| Rol | Empresa de dotación de recursos | Coste |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 INR |
| Developer | Fabrikam US | 115 USD |

En la lista de precios de costes de Fabrikam UK-Robotics, las tarifas de costes se pueden expresar como:

| Rol | Empresa de recursos | Coste |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

La lista de precios de coste puede proporcionar tarifas de mano de obra en varias monedas. Al generar una estimación de costos en el proyecto, las operaciones del proyecto convertirán estas tasas de costos a la moneda del proyecto y se las mostrarán al usuario. Cuando se aprueba una entrada de tiempo y se crea un costo real, el costo real se calcula en la moneda de esa línea de precio de función coincidente en la lista de precios de costo. Los costes reales por tiempo en un solo proyecto se pueden registrar en múltiples monedas. Sin embargo, al acumular o resumir los costes laborales reales a nivel de proyecto, las operaciones del proyecto convertirán todos los montos de costos laborales a la moneda del proyecto, que el usuario puede ver.


[!INCLUDE[footer-include](../includes/footer-banner.md)]