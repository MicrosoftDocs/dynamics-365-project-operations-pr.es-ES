---
title: Usar categorías de compras con pedidos de compra de proyectos y facturas de proveedores pendientes
description: Este tema describe cómo configurar categorías de compras que se pueden usar con pedidos de compra de proyectos y facturas de proveedores pendientes.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613296"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Usar categorías de compras con pedidos de compra de proyectos y facturas de proveedores pendientes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los encargados de compras pueden crear y mantener los catálogos de los artículos y servicios que se pueden usar en pedidos de compra de proyectos y facturas de proveedores pendientes. [Catálogos de compras](/dynamics365/supply-chain/procurement/procurement-catalogs) le brinda una manera fácil de categorizar las compras sin tener que configurar y usar un catálogo de productos publicado. Cada categoría de compras se puede asignar a una categoría de proyecto para transacciones de tiempo, gastos o artículos. Después de registrar una factura de proveedor pendiente que utiliza una categoría de adquisición, el sistema creará datos reales del proyecto de tiempo, gasto o material, transacciones del proyecto y asientos del submayor.

## <a name="minimum-version-requirements"></a>Requisitos de versión mínima

Se requieren las siguientes versiones para usar categorías de compras con órdenes de compra de proyectos para escenarios de Microsoft Dynamics 365 Project Operations sin existencias/basados en recursos:

- Versión de la solución 4.41.0.45 de Project Operations Dataverse
- Entorno de Finanzas y operaciones, versión 10.0.26 o posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Ejecute asignaciones de doble escritura para soporte de la categoría de adquisiciones

Asegúrese de que la asignación para la **Entidad de exportación de línea de factura de proveedor de proyecto de integración de Project Operations msdyn\_projectvendorinvoicelines** usa la versión 1.0.0.4 o posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Habilite la clave de la característica para las categorías de compras

Siga estos pasos para habilitar la funcionalidad para usar categorías de compras con órdenes de compra de proyectos.

1. En Dynamics 365 Finance, abra el espacio de trabajo **Gestión de características**.
1. En la lista de características, busque la característica **Usar categorías de adquisición en Project Operations para escenarios basados en recursos/sin existencias** y luego seleccione **Habilitar**.

> [!IMPORTANT]
> Como requisito previo, también debe habilitar la característica **Habilitar facturas de proveedores pendientes en Project Operations para escenarios basados en recursos/no en existencias**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Asignar categorías de proyectos en la jerarquía de categorías de compras

Siga estos pasos para asignar categorías de proyectos a categorías de adquisiciones en la jerarquía **Categoría de adquisiciones**:

1. Vaya a **Adquisición y abastecimiento \> Categorías de compras**.
1. Seleccione **Editar jerarquía de categoría**.
1. Seleccione el nodo de jerarquía de categorías deseado y, a continuación, en la pestaña **Asignar categorías de proyectos**, asocie el nodo con la categoría de proyecto de la categoría **Tiempo**, Gasto**, o **Proyecto de artículo** (es decir, la categoría **Hora predeterminada** o **Gasto predeterminado**).
1. Seleccione **Guardar**.
1. Cierre la página.

> [!NOTE]
> La asignación de una categoría de compras a una categoría de proyecto es opcional. Si una categoría de compras no está asignada, el sistema utilizará el valor que se establece en el campo **Articulo** de la sección **Valores predeterminados de categoría de proyecto**, en la pestaña **Project Operations en Dynamics 365 Customer Engagement** de la página **Administración de proyectos y parámetros contables**.
