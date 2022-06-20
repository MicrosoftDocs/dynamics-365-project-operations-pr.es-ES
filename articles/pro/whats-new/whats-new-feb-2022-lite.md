---
title: 'Novedades de febrero de 2022: implementación ligera de Project Operations'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de febrero de 2022 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922841"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Novedades de febrero de 2022: implementación ligera de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.28.0.120

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

A partir de esta versión, puede agregar hasta 300 miembros del equipo a un solo proyecto. Anteriormente, el límite en el número de miembros del equipo era de 150. Para obtener más información, consulte [Límites de proyecto](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2497369 | La corrección material debe seguir el valor de la fecha de los parámetros **Corrección**. |
| Facturación y precios | 2498697 | Se mejoró la configuración de seguridad para **Recuperación de entrada de tiempo**. |
| Facturación y precios | 2517455 | No se debe permitir que la acción **Transacciones de línea de factura actualizadas** se desencadene varias veces simultáneamente para la misma factura. |
| Facturación y precios | 2517465 | La acción **Desactivar detalles de línea de factura** está bloqueada porque no es compatible. |
| Facturación y precios | 2556660 | Se corrigieron las comprobaciones de vigencia de fechas que se realizan en la lista de precios que se adjunta a un registro de parámetros del proyecto. |
| Administración de oportunidades | 2369202 | Se corrigió la lógica comercial que verifica que las listas de precios que tienen fechas de vigencia superpuestas se pueden adjuntar al mismo contrato de proyecto. |
| Administración de oportunidades | 2385965 | Se corrigió el comportamiento en la pestaña **Clientes** de la página **Contrato de proyecto** cuando seleccione **Guardar y cerrar**. |
