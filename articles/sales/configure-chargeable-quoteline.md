---
title: Configurar los componentes facturables de una línea de oferta basada en proyecto
description: Este tema proporciona información sobre los componentes incluidos, cargables y no cargables en las líneas de oferta basadas en proyecto.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004017"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurar los componentes facturables de una línea de oferta basada en proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Una línea de oferta basada en proyecto puede tener componentes incluidos y componentes imputables.

Los componentes incluidos están sujetos al método de facturación, divisiones de clientes, los límites que no se deben superar y configuraciones de frecuencia de facturación definidas en la línea de oferta basada en proyecto.
Un subconjunto de los componentes incluidos se puede marcar como imputable usando **Tipo de facturación**. Puede seleccionar una de las siguientes opciones en el campo **Tipo de facturación** en el contexto de una línea de oferta:

   - Imputable
   - No facturable

Los componentes facturables se pueden definir en roles y categorías de transacciones.

La imputabilidad que se define en los roles para una línea de oferta de proyecto solo se aplica a la clase de transacción **Tiempo**. Si una línea de oferta de proyecto tiene **Incluir tiempo** = **No**, la pestaña **Roles imputables** no está disponible.

La imputabilidad que se define en las categorías de transacciones para una línea de oferta de proyecto solo se aplica a la clase de transacción **Gasto**. Si una línea de oferta de proyecto tiene **Incluir gastos** = **No**, la pestaña **Categorías de gastos imputables** no está disponible.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para ser facturable o no facturable
Un rol puede ser imputable o no en una línea de oferta basada en proyecto. El tipo de facturación en un rol se puede configurar en la pestaña **Roles imputables** de una línea de oferta basada en proyecto. Para ello, actualice **Tipo de facturación** en la subcuadrícula **Roles imputables**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar una categoría de transacción para ser facturable o no facturable
Un categoría de transacción puede ser imputable o no en una línea de oferta basada en proyecto. El tipo de facturación en una transacción se puede configurar en la pestaña **Categorías de gastos imputables** de una línea de oferta basada en proyecto. Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Categorías imputables**. 

## <a name="resolve-chargeability"></a>Resolver imputabilidad

Una estimación o un valor real creado para tiempo solo se considerará imputable si el tiempo se incluye en la línea de oferta y si el rol está configurado como imputable.
Una estimación o un valor real creado para un gasto solo se considerará imputable si el gasto se incluye en la línea de oferta y si la categoría de transacción está configurada como imputable en la línea de oferta. En la siguiente tabla se muestra cómo la imputabilidad se establece por defecto en cada valor real. Los valores predeterminados se basan en los componentes incluidos y el tipo de facturación que se configura en la línea de oferta.

| Incluye tiempo | Incluye gasto | Rol | Categoría | Tarea |
| --- | --- | --- | --- | --- |
| Sí | Sí | Imputable | Imputable | Facturación a tiempo real: Facturable </br>Tipo de facturación en gastos actuales: Facturable |
| Sí | Sí | No facturable | Imputable | Facturación a tiempo real: No facturable </br>Tipo de facturación en gastos actuales: Facturable |
| Sí | Sí | No facturable | No facturable | Facturación a tiempo real: No facturable </br>Tipo de facturación en gastos actuales: No facturable |
| No | Sí | No puede estar establecido | Imputable | Facturación a tiempo real: No disponible </br>Tipo de facturación en gastos actuales: Facturable |
| No | Sí | No puede estar establecido | No facturable | Facturación a tiempo real: No disponible </br>Tipo de facturación en gastos actuales: No facturable |
| Sí | No | Imputable | No puede estar establecido | Facturación a tiempo real: Facturable </br>Tipo de facturación un gasto actual: No disponible |
| Sí | No | No facturable | No puede estar establecido | Facturación a tiempo real: No facturable </br> Tipo de facturación un gasto actual: No disponible |


[!INCLUDE[footer-include](../includes/footer-banner.md)]