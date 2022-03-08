---
title: Tipos de fases del proyecto
description: En este tema se proporciona información sobre las fases del proyecto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996907"
---
# <a name="project-stage-types"></a>Tipos de fases del proyecto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Las fases de un proyecto se diseñan para reflejar el estado del proyecto a medida que avanza. Las personalizaciones se pueden utilizar para actualizar automáticamente las etapas con los flujos de procesos comerciales, Power Automate o extensiones de complementos.

Se definen las siguientes fases en el BPF predeterminado:

- Nueva
- Oferta
- Planear
- Entregar
- Completo
- Cerrar 

## <a name="new"></a>Nuevo

Cuando cree un proyecto, la fase del proyecto se establece como **Nueva**. Si el proyecto se creó a partir de una plantilla, podría tener datos de programación, estimación y equipo. De lo contrario, es solo un perfil del proyecto y se deben introducir los componentes restantes.

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