---
title: 'Novedades del acceso anticipado del segundo lanzamiento de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las características disponibles en la versión de acceso anticipado del segundo lanzamiento de 2021 de implementación simplificada de Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323932"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novedades del acceso anticipado del segundo lanzamiento de 2021: implementación simplificada de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.23.0.4

La versión solo se aplica cuando un entorno [ha optado por el acceso anticipado](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

[Gestión de subcontratos](../subcontracting/subcontracting_EA_scope.md): esta función proporciona una mejor visibilidad y control sobre todos los aspectos del trabajo en un proyecto. La vista previa de la gestión de subcontratos incluye las siguientes capacidades:

  - Un administrador de proyecto puede crear un subcontrato con un proveedor. De forma predeterminada, las listas de precios que se adjuntan al registro de proveedor se usan para el subcontrato. La cuenta de proveedor tiene un tipo de relación de **Proveedor** o **Distribuidor**.
  - Un administrador de proyecto puede desglosar todas las compras como elementos de línea en el subcontrato. Las líneas del subcontrato pueden ser por tiempo, gastos o productos. La clase de transacción de la línea de subcontrato determina para qué es la línea.
  - El administrador de cuentas del proveedor y el administrador del proyecto pueden iterar sobre el subcontrato. Los precios se pueden ajustar en las listas de precios de compra que estén asociadas al subcontrato.
  - Durante el proceso, si la línea de subcontrato es por tiempo, el administrador de cuentas del proveedor puede asociar los contactos del proveedor con cada línea de subcontrato. Esta asociación proporciona información al administrador del proyecto que está trabajando en el subcontrato. Cuando un contacto de proveedor está asociado con una línea de subcontrato, el sistema crea automáticamente un recurso reservable desde el contacto, si aún no existe un recurso reservable.
  - El método de facturación de cada línea de subcontrato puede ser de precio fijo o por tiempo y material. Para las líneas de subcontratos de precio fijo, se configura un programa de facturación basado en hitos.
