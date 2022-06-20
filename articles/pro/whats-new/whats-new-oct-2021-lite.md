---
title: 'Novedades de octubre de 2021: implementación de Project Operations Lite'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de octubre de 2021 de la implementación de Project Operations Lite.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921967"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novedades de octubre de 2021: implementación de Project Operations Lite

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Microsoft Dataverse versión 4.25.0.91


## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

[Administración de subcontratos](../subcontracting/managing-subcontracts-overview.md): Esta función brinda la capacidad de crear un subcontrato con el proveedor, detallar todas las compras como elementos de línea en el subcontrato, ajustar los precios y asociar los contactos.


## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2209402 | Se corrigieron las validaciones que impedían que se facturaran los importes de anticipo cuando se confirma un contrato de proyecto. |
| Administración de oportunidades | 2227414 | Los campos **Producto**, **Fuera de catálogo** y **Es un producto reemplazado** se copian en los detalles de la línea de oferta y los detalles de la línea de contrato. |
| Facturación y precios | 2338357 | La moneda en el registro de uso de materiales debe tomar de manera predeterminada la moneda del proyecto cuando se selecciona el proyecto. |
| Tiempo y gastos | 2414777 | Debe ser posible cancelar una aprobación cuando la entrada de gasto o tiempo tiene más de una aprobación de proyecto asociada. |
