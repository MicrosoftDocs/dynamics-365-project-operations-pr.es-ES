---
title: 'Novedades de noviembre de 2022: implementación de Project Operations Lite'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2022 de la implementación simplificada de Microsoft Dynamics 365 Project Operations.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831111"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Novedades de noviembre de 2022: implementación de Project Operations Lite

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.58.0.119


## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2781818 | Error de clave no encontrada al establecer el precio predeterminado para el registro de uso de material. |
| Facturación y precios | 2922373 | No se puede vincular la línea de presupuesto al proyecto que se ha cerrado como presupuesto perdido. |
| Facturación y precios | 2943206 | El campo **Línea de contrato** en la entidad del proyecto debe ser opcional. |
| Facturación y precios | 2953182 | Mejorar el mensaje de error para las facturas de corrección.|
| Facturación y precios | 2959500 | No se puede vincular la línea de presupuesto a una tarea de proyecto que ya está asociada con un presupuesto perdido.|
| Facturación y precios | 2959560 | Se recibió el mensaje "Este cliente ya está en el contrato del proyecto" al cerrar la cotización como ganada en ciertos lugares. |
| Facturación y precios | 3031727 | Las asignaciones de recursos fallan con el error Falta el campo obligatorio 'msdyn_Company'. |
| Facturación y precios | 3036905 | La empresa propietaria nunca se inicializa en ProjectTeamMember. |
| Administración de oportunidades | 2763519 | Error de referencia nula en EnsureProjectContractAllowsUpdates. |
| Administración de oportunidades | 2783798 | Al importar estimaciones de proyectos en la línea de cotización, faltan descripciones de tareas para estimaciones de gastos y materiales.|
| Administración de oportunidades | 2988635 | Mejore la descripción del mensaje de error al eliminar el cliente en la cotización. |
| Administración de oportunidades | 3001191 | No se puede crear una cotización de Oportunidad donde el método de facturación se especifica como nulo. |
| Actualizado | 3012324 | La conversión del proyecto falló en un proyecto con caracteres de control como Tabulador en su nombre. || Planificación y seguimiento de proyectos | 2790384 | El tiempo de espera de OperationSet pendiente es demasiado corto. |
| Planificación y seguimiento de proyectos | 3044275 | Falta la localización para: missingProjectSchedulerErrorMessage. |
| Planificación y seguimiento de proyectos | 3044277 | La cuadrícula de Project Recon no se carga cuando el programador no está configurado.|
| Administración de recursos | 2943153 | Actualice la pestaña Seguimiento para mostrar dos lugares decimales para la Duración.|
| Subcontratación | 2932774 | Línea de factura del proveedor Solo lectura arrojando error incorrectamente. |
| Subcontratación | 2939556 | El estado del encabezado de la factura del proveedor no debe configurarse como Borrador para eliminar en línea si no está activo. |
| Tiempo y gasto | 2939998 | Adopción de la nueva versión de TESA en ProjOps. |
