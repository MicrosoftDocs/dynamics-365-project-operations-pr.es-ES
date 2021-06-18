---
title: 'Novedades de abril de 2021: implementación simplificada de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de abril de 2021 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 868d6daf8ac3ad9ef4245cef3c74a735137d3903
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994112"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novedades de abril de 2021: implementación simplificada de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

  - Project Operations en el entorno de Dataverse versión 4.9.0.221 

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Materiales no almacenados para proyectos. Entre las funcionalidades clave, se incluyen:
  - Estimación y precio de materiales no almacenados durante el ciclo de ventas de un proyecto. Para obtener más información, vea [Configurar tarifas de costes y ventas para productos de catálogo (lite)](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Seguimiento del uso de materiales no almacenados durante la entrega del proyecto. Para obtener más información, vea [Registrar uso de materiales en proyectos y tareas de proyectos](../../material/material-usage-log.md).
  - La facturación utilizó los costes de materiales no almacenados. Para obtener más información, vea [Administrar el trabajo pendiente de facturación (lite)](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Las nuevas API en Dynamics 365 Dataverse permiten crear, actualizar y eliminar operaciones con **Entidades de programación**. Para obtener más información, vea [Utilizar las API de programación para realizar operaciones con entidades de programación](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualizaciones de calidad

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2224568 | Lógica agregada para habilitar personalizaciones que implican invocar el complemento de confirmación de factura. |
| Facturación y precios | 2101098 | Se mejoró la lógica de los campos predeterminados para la factura proforma: **Dirección de facturación**, **Facturar a un nombre**, y **Condiciones de pago** ahora resultan de forma predeterminada del registro de cliente del contrato del proyecto correspondiente. |
| Facturación y precios | 2021413 | Se actualizaron los campos **Coste real** y **Ventas** en la entidad **Tarea** para incluir los valores de ventas de los gastos facturados y no facturados en las tareas. |
| Facturación y precios | 2182110 | Al copiar un contrato de proyecto, el identificador de la línea del contrato se vuelve a generar en el contrato del proyecto de destino para garantizar que sea único. |
| Administración de oportunidades | 2186741 | Validaciones agregadas para garantizar que el campo **Origen** y **Tipo de transacción** no se puede actualizar en los detalles de la línea de cotización existente. |
| Administración de oportunidades | 2191353 | Los hitos no deben crearse en una línea de contrato de tiempo y material. |
| Administración de oportunidades | 2216956 | Se resolvieron los problemas con **Actualizar precios**. |
| Planificación y seguimiento | 2182979 | Se mejoró la función de copia del proyecto para garantizar que las líneas de estimación de gastos se copien desde el proyecto original. |
| Planificación y seguimiento | 2184144 | Se mejoró la función de copia del proyecto para garantizar el nombre de posición del recurso se copie desde el proyecto original. |
| Planificación y seguimiento | 2184799 | Copia del proyecto: control más estricto para garantizar que la fecha de inicio estimada no se puede cambiar mientras se realiza la copia. |
| Planificación y seguimiento | 2185134 | Copia del proyecto: la fecha de inicio estimada del proyecto de destino se establece en la fecha de hoy. |
| Planificación y seguimiento | 2196373 | Copia del proyecto: asegúrese de que los registros del director de proyectos y los miembros del equipo no estén duplicados en el equipo del proyecto. |
| Planificación y seguimiento | 2211833 | Copia del proyecto: las asignaciones de recursos se copian desde la tarea del proyecto de origen al proyecto de destino. |
| Planificación y seguimiento | 2186541 | Problemas resueltos en la cuadrícula **Estimaciones** al agrupar por recurso. |
| Planificación y seguimiento | 2166906 | La categoría de transacción de una tarea se debe copiar en la entidad **Asignación de recursos**. |
| Administración de recursos | 2125362 | Se solucionaron problemas con la creación de un miembro del equipo genérico utilizando un método de asignación basado en horas. |
| Tiempo y gasto | 2113603 | Se solucionó el problema relacionado con la personalización con la eliminación de atributos de la página **Entrada de tiempo**. El sistema ahora verifica si el atributo existe en la página antes de acceder a ellos mediante un script. |
| Tiempo y gasto | 2204377 | Las hojas de horas copiadas deben mostrarse automáticamente cuando seleccione **Copiar semana** durante la entrada de tiempo. |
| Tiempo y gasto | 2209059 | El campo **Estado** se puede editar para las entradas de tiempo de Dynamics 365 Field Service. |
