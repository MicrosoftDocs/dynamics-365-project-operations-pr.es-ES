---
title: Configurar componentes facturables de una línea de contrato basada en proyectos
description: Este tema proporciona información sobre cómo componentes incluidos, facturables y no facturables en líneas de contrato.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085085"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar componentes facturables de una línea de contrato basada en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Una línea de contrato basada en proyectos tiene el concepto de componentes incluidos y componentes facturables y no facturables.

Los componentes incluidos están sujetos al método de facturación, las divisiones de clientes, los límites de no exceder y la configuración de frecuencia de facturación definida en la línea de contrato basada en el proyecto.

Un subconjunto de los componentes incluidos se puede marcar como facturable actualizando el campo **Tipo de facturación**.

Los componentes facturables se pueden definir en roles y categorías de transacciones.

La imputabilidad definida en roles para una línea de contrato de proyecto solo se aplica a la clase de transacción **Hora**. Si **Incluir tiempo** en una línea de contrato de proyecto está configurado en **No** , la pestaña **Roles facturables** no estará disponible.

La imputabilidad definida en categorías de transacción para una línea de contrato de proyecto solo se aplica a la clase de transacción **Gastos**. Si **Incluir gastos** en una línea de contrato de proyecto está configurado en **No** , la pestaña **Categorías facturables** no estará disponible.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para ser facturable o no facturable

Un rol puede ser facturable o no facturable en una línea de contrato específica.

En la pestaña **Roles facturables** de una línea de contrato basada en proyectos, en la subcuadrícula **Categorías facturables** , en el campo **Tipo de facturación** , actualice el tipo de facturación para un rol.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar una categoría de transacción para ser facturable o no facturable

Una categoría de transacción puede ser facturable o no facturable en una línea de contrato basada en proyectos específica.

En la pestaña **Categorías facturables** de una línea de contrato basada en proyectos, en la subcuadrícula **Categorías facturables** , en el campo **Tipo de facturación** , actualice el tipo de facturación para una transacción.

### <a name="resolve-chargeability"></a>Resolver imputabilidad

Una estimación o real creada para el tiempo solo se considerará imputable si tiempo está incluido en la línea del contrato, y si el rol está configurado como facturable en la línea de contrato.

Una estimación o real creada para los gastos solo se considerará imputable si gastos está incluido en la línea del contrato y si las categoría transacción está configurada como facturable en la línea de contrato.

| Incluye tiempo | Incluye gasto | Rol | Categoría | Tarea |
| --- | --- | --- | --- | --- |
| Sí | Sí | Imputable | Imputable | Facturación a tiempo real: Facturable </br>Tipo de facturación en gastos actuales: Facturable |
| Sí | Sí | No facturable | Imputable | Facturación a tiempo real: No facturable </br>Tipo de facturación en gastos actuales: Facturable |
| Sí | Sí | No facturable | No facturable | Facturación a tiempo real: No facturable </br>Tipo de facturación en gastos actuales: No facturable |
| No | Sí | No puede estar establecido | Imputable | Facturación a tiempo real: No disponible </br>Tipo de facturación en gastos actuales: Facturable |
| No | Sí | No puede estar establecido | No facturable | Facturación a tiempo real: No disponible </br>Tipo de facturación en gastos actuales: No facturable |
| Sí | No | Imputable | No puede estar establecido | Facturación a tiempo real: Facturable </br>Tipo de facturación un gasto actual: No disponible |
| Sí | No | No facturable | No puede estar establecido | Facturación a tiempo real: No facturable </br> Tipo de facturación un gasto actual: No disponible |
