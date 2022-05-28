---
title: 'Novedades de mayo de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de mayo de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 854a8c2290281b4d11a045321a334d8866806041
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583789"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novedades de mayo de 2021: implementación simplificada de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

   - Project Operations en el entorno de Dataverse versión 4.10.0.186.

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- [Modos de programación](../../project-management/scheduling-modes.md): los directores de proyecto ahora pueden definir si un proyecto debe administrarse utilizando un modo de programación de duración fija, trabajo fijo o unidades fijas.

## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2224568 | Lógica agregada para habilitar personalizaciones que implican invocar el complemento de confirmación de factura. |
| Facturación y precios | 2101098 | Se mejoró la lógica de los campos predeterminados para la factura proforma. Estos campos incluyen, **Dirección de la facturación**, **Nombre de facturación**, y **Condiciones de pago**. Los campos ahora predeterminados del registro de cliente del contrato de proyecto correspondiente. |
| Facturación y precios | 2021413 | Se actualizaron los campos **Coste real** y **Ventas** en la entidad **Tarea** para incluir los valores de ventas de los gastos facturados y no facturados en las tareas. |
| Facturación y precios | 2182110 | Al copiar un contrato de proyecto, el identificador de la línea del contrato se vuelve a generar en el contrato del proyecto de destino para garantizar que sea único. |
| Administración de oportunidades | 2186741 | Validaciones agregadas para garantizar que el campo **Origen** y Tipo de transacción no se puede actualizar en los detalles de la línea de cotización existente. |
| Administración de oportunidades | 2191353 | No se debe permitir crear hitos en una línea de contrato de tiempo y material. |
| Administración de oportunidades | 2216956 | Se resolvieron los problemas con **Actualizar precios**. |
| Planificación y seguimiento | 2182979 | Se mejoró la función de copia del proyecto para garantizar que las líneas de estimación de gastos se copien desde el proyecto original. |
| Planificación y seguimiento | 2184144 | Se mejoró la función de copia del proyecto para garantizar el nombre de posición del recurso se copie desde el proyecto original. |
| Planificación y seguimiento | 2184799 | Control más estricto al copiar un proyecto para garantizar que la fecha de inicio estimada no se puede cambiar mientras se realiza la copia. |
| Planificación y seguimiento | 2185134 | Durante la copia del proyecto, la fecha de inicio estimada del proyecto de destino se establece en la fecha de hoy. |
| Planificación y seguimiento | 2196373 | Al copiar un proyecto, asegúrese de que los registros del director de proyectos y los miembros del equipo no estén duplicados en el equipo del proyecto. |
| Planificación y seguimiento | 2211833 | Las asignaciones de recursos se copian desde la tarea del proyecto de origen al proyecto de destino. |
| Planificación y seguimiento | 2186541 | Problemas resueltos en la cuadrícula **Estimaciones** al agrupar por **recurso**. |
| Planificación y seguimiento | 2166906 | La categoría de transacción de una tarea se debe copiar en la entidad **Asignación de recursos**. |
| Administración de recursos | 2125362 | Se solucionaron problemas con la creación de un miembro del equipo genérico utilizando un método de asignación basado en horas. |
| Tiempo y gasto | 2113603 | Se solucionó el problema relacionado con la personalización con la eliminación de atributos de la página **Entrada de tiempo**. El sistema verifica si el atributo existe en la página antes de acceder a él mediante un script. |
| Tiempo y gasto | 2204377 | Las hojas de horas copiadas deben mostrarse automáticamente cuando seleccione **Copiar semana**. |
| Tiempo y gasto | 2209059 | El campo **Estado** se puede editar para las entradas de tiempo de Dynamics 365 Field Service. |
