---
title: Fases del proyecto
description: En este tema se proporciona información sobre las fases del proyecto que están disponibles en Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996947"
---
# <a name="project-stages"></a>Fases del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las fases de un proyecto se diseñan para reflejar el estado del proyecto a medida que avanza. Las personalizaciones se pueden utilizar para actualizar automáticamente las etapas con los flujos de procesos comerciales, Power Automate o extensiones de complementos.

Se definen las siguientes fases en el flujo de proceso de negocio predeterminado:

- Nueva
- Oferta
- Plan
- Entregar
- Completa
- Cerrada 

## <a name="new"></a>Nueva

Cuando cree un proyecto, la fase del proyecto se establece como **Nueva**. Si el proyecto se creó a partir de una plantilla, podría tener datos de programación, estimación y equipo. De lo contrario, es un perfil del proyecto y se deben introducir los componentes restantes.

## <a name="quote"></a>Oferta

Cuando asocia un proyecto a una oferta o lo crea desde una oferta, la fase del proyecto se establece en **Oferta** y las fechas de inicio y finalización estimadas se actualizan. Cuando el proyecto se encuentra en la fase **Oferta**, la pestaña **Ventas** en la página **Entidad del proyecto** muestra detalles de la oferta.

## <a name="plan"></a>Planear

Cuando gana una oferta asociada a un proyecto, y el proyecto se mueve a la fase **Contrato**, la fase del proyecto se actualiza a **Planificar**. Cuando el proyecto se encuentra en la fase **Planificar**, la página **Entidad del proyecto** muestra detalles del contrato.

## <a name="deliver"></a>Entregar

Cuando se completa el plan del proyecto y está listo para comenzar el proyecto, el jefe de proyecto debe actualizar la fase del proyecto a **Entregar** para mostrar que el proyecto ha comenzado.

## <a name="complete"></a>Completo 

Cuando se completa el trabajo para el proyecto, el administrador del proyecto puede actualizar la fase a **Completo**. Al actualizar la fase del proyecto a **Completo**, el administrador del proyecto indica que el trabajo se ha completado al cien por cien, pero que el proyecto se mantiene abierto para que se puedan registrar las entradas de tiempo o gastos pendientes.

## <a name="close"></a>Cerrar

Cuando se registran todas las transacciones para el proyecto, el administrador del proyecto puede actualizar la fase a **Cerrar**. A partir de ese momento, no se podrán registrar transacciones y el proyecto quedará configurado como de solo lectura.



[!INCLUDE[footer-include](../includes/footer-banner.md)]