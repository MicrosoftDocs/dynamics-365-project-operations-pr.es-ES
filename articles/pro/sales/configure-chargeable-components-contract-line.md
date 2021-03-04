---
title: Configurar componentes facturables de una línea de contrato basada en proyectos (lite)
description: Este tema proporciona información sobre cómo agregar componentes facturables a las líneas de contrato en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513900"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Configurar componentes facturables de una línea de contrato basada en proyectos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Una línea de contrato basada en proyectos tiene *incluido* componentes y componentes *facturables*.

Los componentes incluidos son componentes que están sujetos a:

  - Método de facturación y divisiones de clientes
  - Límites a no exceder 
  - Configuración de frecuencia de facturación definida en la línea de contrato basada en proyecto

Un subconjunto de los componentes incluidos se puede marcar como facturable usando el campo **Tipo de facturación**. El campo **Tipo de facturación** es un conjunto de opciones que permite los siguientes valores en el contexto de una línea de contrato:

  - Imputable
  - No facturable

Los componentes facturables se pueden definir en tareas, roles y categorías de transacciones.

La facturabilidad se define en las tareas de una línea de contrato de proyecto y se aplica a todas las clases de transacciones incluidas en la línea. Si el campo **Incluir tareas** en una línea de contrato está en blanco o configurado en **Proyecto entero**, la pestaña **Tareas imputables** no estará disponible.

La imputabilidad definida en roles para una línea de contrato de proyecto solo se aplica a la clase de transacción **Hora**. Si el campo **Incluir tiempo** en una línea de contrato está configurado en **No**, la pestaña **Roles facturables** no estará disponible.

La imputabilidad definida en categorías de transacción para una línea de contrato de proyecto solo se aplica a la clase de transacción **Gastos**. Si el campo **Incluir gastos** en una línea de contrato está configurado en **No**, la pestaña **Categorías facturables** no estará disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizar una tarea del proyecto como facturable o no facturable

Una tarea de proyecto puede ser facturable o no facturable en una línea de contrato específica, lo que hace posible la siguiente configuración:

Si una línea de contrato basada en proyecto incluye **Tiempo** y una determinada tarea, **T1** está asociado como facturable. Si hay una segunda línea de contrato que incluye **Gastos**, puede asociar la tarea T1 en la línea de contrato como no imputable. El resultado es que todo el tiempo registrado en la tarea es imputable y todos los gastos no son imputables.

El tipo de facturación de una tarea se puede configurar en la pestaña **Tareas con cargo** de la línea de contrato actualizando el campo **Tipo de facturación** en la subcuadrícula de tareas de la línea de contrato. Alternativamente, puede actualizar el campo **Tipo de facturación** en la subcuadrícula de la tarea Configuración de facturación de un proyecto que muestra las líneas de contrato asociadas a una tarea.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizar un rol como facturable o no facturable

Un rol puede ser facturable o no facturable en una línea de contrato específica.

El tipo de facturación de un rol se puede configurar en la pestaña **Roles imputables** de una línea de contrato. Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Funciones imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizar una categoría de transacción como facturable o no facturable

Una categoría de transacción puede ser facturable o no facturable en una línea de contrato específica.

El tipo de facturación de una transacción se puede configurar en la pestaña **Categorías imputables** de una línea de contrato basada en un proyecto. Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver imputabilidad

Una estimación o real creada para el tiempo solo se considerará imputable si **Tiempo** está incluido en la línea del contrato, y si **Tarea** y **Rol** están configurados como facturables en la línea de contrato.

Una estimación o real creada para los gastos solo se considerará imputable si **Gastos** está incluido en la línea del contrato, y si las categorías **Tarea** y **Transacción** están configuradas como facturables en la línea de contrato.


| Incluye tiempo | Incluye gasto | Incluye tareas | Rol           | Categoría       | Tarea                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Sí           | Sí              | Proyecto entero | Imputable     | Imputable     | Facturación a tiempo real: **Facturable** </br> Tipo de facturación en Gastos actuales: **Facturable**           |
| Sí           | Sí              | Tareas seleccionadas | Imputable     | Imputable     | Facturación a tiempo real: **Facturable** </br> Tipo de facturación en Gastos actuales: **Facturable**           |
| Sí           | Sí              | Tareas seleccionadas | No facturable | Imputable     | Facturación a tiempo real: **No facturable** </br> Tipo de facturación en Gastos actuales: **Facturable**       |
| Sí           | Sí              | Tareas seleccionadas | Imputable     | Imputable     | Facturación a tiempo real: **No facturable** </br> Tipo de facturación en Gastos actuales: **No facturable** |
| Sí           | Sí              | Tareas seleccionadas | No facturable | Imputable     | Facturación a tiempo real: **No facturable** </br> Tipo de facturación en Gastos actuales: **No facturable** |
| Sí           | Sí              | Tareas seleccionadas | No facturable | No facturable | Facturación a tiempo real: **No facturable** </br> Tipo de facturación en Gastos actuales: **No facturable** |
| No            | Sí              | Proyecto entero | No puede estar establecido   | Imputable     | Facturación a tiempo real: **No disponible**</br>Tipo de facturación en Gastos actuales: **Facturable**          |
| No            | Sí              | Proyecto entero | No puede estar establecido   | No facturable | Facturación a tiempo real: **No disponible**</br> Tipo de facturación en Gastos actuales: **No facturable**     |
| Sí           | No               | Proyecto entero | Imputable     | No puede estar establecido   | Facturación a tiempo real: **Facturable** </br> Tipo de facturación en Gastos actuales: **No disponible**        |
| Sí           | No               | Proyecto entero | No facturable | No puede estar establecido   | Facturación a tiempo real: **No facturable** </br>Tipo de facturación en Gastos actuales: **No disponible**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]