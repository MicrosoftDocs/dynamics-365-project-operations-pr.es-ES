---
title: 'Novedades de octubre de 2022: implementación de Project Operations Lite'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de octubre de 2022 de la implementación simplificada de Microsoft Dynamics 365 Project Operations.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806659"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novedades de octubre de 2022: implementación de Project Operations Lite

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.57.0.176

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

| Área de características | Nombre de característica | Más información |
| --- | --- | --- |
| Planificación y seguimiento de proyectos | **Programación externa de Project Operations**<br>El modo de programación externa permite a los clientes crear, actualizar y eliminar de forma nativa entidades relacionadas con estructuras de descomposición del trabajo (WBS) usando API de Dataverse nativas sin los límites actuales que impone Microsoft Project for the Web. | [Programación externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementación y configuración | <p>**Permitir que los clientes elijan el tipo de implementación**<br>Las actualizaciones impulsadas por productos (PDU) de Project Operations se utilizan para instalar automáticamente la solución de escritura dual de Project Operations cuando las soluciones centrales y de orquestación de escritura dual están instaladas en el entorno.</p><p>Esta función introduce un nuevo parámetro **Comportamiento de actualización de la solución** en los parámetros del proyecto. Cuando este parámetro se establece en **Solo Lite**, las PUD ya no instalarán automáticamente la solución de escritura dual de Project Operations aun cuando las soluciones centrales y de orquestación de escritura dual están instaladas en el entorno. Este comportamiento beneficiará a los clientes que planean usar soluciones de escritura dual para integrar pedidos de ventas en aplicaciones de finanzas y operaciones, pero desean usar Project Operations en modo Lite (es decir, sin integración en aplicaciones de finanzas y operaciones).</p> | |

## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2316317 | El sistema permite crear facturas que no tengan transacciones imputables. |
| Facturación y precios | 2737300 | Valide la disponibilidad del campo Cliente antes de acceder al formulario. |
| Facturación y precios | 2744948 | Agregue una verificación nula para el método de facturación. |
| Facturación y precios | 2763515 | Manejador de error de referencia nula cuando falta el contrato de venta de la factura. |
| Facturación y precios | 2844301 | La creación de facturas por lotes falla debido a un error. |
| Facturación y precios | 2845869 | Almacenamiento incorrecto del servicio de organización. |
| Facturación y precios | 2853729 | Los detalles de la función y el precio se actualizan cuando se modifica el tipo de facturación. |
| Facturación y precios | 2940350 | Cuando se determina el precio de los datos reales, solo se deben ingresar automáticamente las listas de precios activas. |
| Implementación y configuración | 3001206 | La entidad msdyn\_replaylogheader impide las actualizaciones de las organizaciones de clientes. |
| Administración de oportunidades | 2755582 | Control de excepciones de referencia nula en el asistente de regla de facturación dividida. |
| Administración de oportunidades | 2761477 | Cuando se utiliza la facturación dividida, la eliminación de un hito (encabezado) deja hitos huérfanos. |
| Administración de oportunidades | 2767595 | Cuando se abre un registro de uso de material en el formulario principal, el recurso que se puede reservar para el registro cambia al usuario que ha iniciado sesión actualmente. |
| Planificación y seguimiento de proyectos | 2790384 | El tiempo de espera de OperationSet pendiente es demasiado corto. |
| Administración de recursos | 2751560 | Unidades organizativas preferidas incoherentes en los requisitos de recursos. |
| Subcontratación | 2907231 | La etapa de proceso de las facturas de proveedores no puede avanzar. |
| Tiempo y gasto | 2867363 | Los registros no quedan fuera de la vista Ausencias/Vacaciones para aprobación cuando están en cola para aprobación. |
| Tiempo y gasto | 2894405 | TESA: El directorio POC no utilizado está causando problemas de cumplimiento. |
