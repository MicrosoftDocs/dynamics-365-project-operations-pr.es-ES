---
title: 'Novedades de enero de 2021: implementación ligera de Project Operations'
description: Este artículo proporciona información sobre las actualizaciones de calidad disponibles en la versión de enero de 2021 de la implementación de Project Operations Lite.
author: sigitac
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 47932fb89cdd9481988d00f2f3be094b68110cbc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934295"
---
# <a name="whats-new-january-2021---project-operations-lite-deployment"></a>Novedades de enero de 2021: implementación ligera de Project Operations


_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este artículo se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.6.0.154.
  
## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| **Implementación y configuración** | 2106818 | Se ha corregido el cambio de nombre del recurso web que causaba problemas relacionados con la personalización de una página. |
| **Facturación y precios** | 2091908 | Se ha corregido la visibilidad de las opciones **Bloquear precios** y **Usar precios actuales** en la página **Factura** cuando se instala Project Operations junto con Dynamics 365 Field Service. |
| **Facturación y precios** | 2103058 | Se ha renovado la opción **Totales del proyecto** de forma que pueda procesar valores nulos para el coste real en una tarea. |
| **Facturación y precios** | 2116100 | Se han mejorado los mensajes de error de la funcionalidad **Corregir entradas en datos reales**. |
| **Facturación y precios** | 2116129 | Se ha mejorado la visibilidad de las estimaciones de gastos en la pestaña **Estimaciones** de la página **Proyectos**. |
| **Facturación y precios** | 2119112 | Agregación fija de ventas reales y coste real cuando se utilizan diferentes tipos de cambio. |
| **Facturación y precios** | 2134705 | Se ha corregido el error "No se puede leer la propiedad **getResourceString** de algo indefinido" cuando se abre la página **Factura** con Field Service instalado. |
| **Administración de oportunidades** | 2022195 | La cuadrícula de facturación basada en tareas de la página **Proyecto** incluye un icono que indica que hay un contrato o una línea de contrato u oferta vinculada a esa tarea. |
| **Administración de oportunidades** | 2029135 | Se ha corregido el error del proceso empresarial que se produce cuando un usuario intenta abrir una línea de factura en una factura confirmada que tiene un pago a cuenta facturado. |
| **Administración de oportunidades** | 2040713 | Se ha corregido el error de script que se produce al crear una factura a partir de un contrato con Field Service instalado. |
| **Planificación y seguimiento de proyectos** | 2090202 | Se han marcado las reglas de negocio que ya no se utilizan como **En desuso**. |
| **Tiempo y gasto** | 2091249 | Se han establecido controles más estrictos para que los usuarios no puedan cambiar la tarea en una entrada de tiempo enviada o aprobada. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]