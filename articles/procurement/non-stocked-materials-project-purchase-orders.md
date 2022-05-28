---
title: Comprar materiales no mantenidos en existencias para un proyecto usando pedidos de compra de proyecto
description: Este tema explica cómo puede comprar materiales no mantenidos en existencias para un proyecto usando pedidos de compra de proyecto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612724"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Categorías de adquisición de pedidos o materiales no mantenidos en existencias para un proyecto usando pedidos de compra del proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

El departamento de adquisiciones de su organización podría utilizar [pedidos de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) para rastrear pedidos de bienes y servicios. Los pedidos de compra de categorías de adquisición de pedidos o materiales no mantenidos en existencias se pueden atribuir a un proyecto. La facturación de estos pedidos de compra registra el costo del proyecto.

## <a name="prerequisites"></a>Requisitos previos
Complete los siguientes pasos para habilitar la funcionalidad de pedidos de compra del proyecto.

1. En Dynamics 365 Finance, vaya al espacio de trabajo **Gestión de características**.
2. En la lista de funciones, busque y seleccione la función **Habilitar pedidos de compra del proyecto en Project Operations para escenarios basados en recursos/sin existencias**.
3. Seleccione **Habilitar**.
4. Configure los materiales de los que no hay existencias y las facturas de proveedor pendientes como se describe en [Configurar materiales de los que no hay existencias y facturas de proveedores pendientes](configure-materials-nonstocked.md).
5. Configure las categorías de adquisición según se describe en [Usar las categorías de adquisición con pedidos de compra de proyectos y facturas de proveedores pendientes](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Cree un pedido de compra de proyecto a partir de la lista de pedidos de compra del proyecto

1. En Finance, vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos** y seleccione y un proyecto.
2. En el panel de acciones, en la pestaña **Administrar**, en el grupo **Nuevo**, seleccione **Tarea de artículo** > **Pedido de compra**.
3. En la página **Crear pedido de compra**, seleccione el proveedor con el que desea realizar el pedido de compra, ingrese otra información según corresponda y luego seleccione **Aceptar**.
4. En la página **Pedido de compra**, en la cuadrícula **Líneas de pedido de compra**, seleccione **Agregar línea**.
5. Introduzca un número de artículo o categoría de adquisición, cantidad, unidad, precio unitario y otra información según corresponda.

    > [!NOTE]
    > Solo las categorías de adquisición, los artículos no mantenidos en existencias y los servicios se pueden usar con los pedidos de compra del proyecto. Los artículos almacenados no se admiten.

6. Continúe agregando artículos o categorías de adquisición según sea necesario y confirme el pedido de compra.

    Los recibos de bienes y servicios se pueden registrar creando y contabilizando un recibo de producto.

    > [!NOTE]
    > Los recibos de productos no se registran en los datos reales del proyecto en Microsoft Dataverse y no afectan a la subcontabilidad del proyecto.

    Después de que un proveedor envía la factura de los artículos y servicios en el pedido de compra, el departamento de compras puede generar una factura para el pedido de compra en **Factura** > **Generar** > **Factura** en el Panel de acciones. Para obtener más información sobre las facturas de proveedores pendientes, consulte [Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente](pending-vendor-invoices.md).
