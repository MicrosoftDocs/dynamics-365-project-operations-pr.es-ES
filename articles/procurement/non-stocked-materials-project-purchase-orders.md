---
title: Comprar materiales no mantenidos en existencias para un proyecto usando pedidos de compra de proyecto
description: Este tema explica cómo puede comprar materiales no mantenidos en existencias para un proyecto usando pedidos de compra de proyecto.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563043"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Comprar materiales no mantenidos en existencias para un proyecto usando pedidos de compra de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

El departamento de adquisiciones de su organización podría utilizar [pedidos de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) para rastrear pedidos de bienes y servicios. Los pedidos de compra de materiales que no están en stock se pueden atribuir a un proyecto. La facturación de estos pedidos de compra registra el costo del proyecto.

## <a name="prerequisites"></a>Requisitos previos
Complete los siguientes pasos para habilitar la funcionalidad de pedidos de compra del proyecto.

1. En Dynamics 365 Finance, vaya al espacio de trabajo **Administración de funciones**.
2. En la lista de funciones, busque y seleccione la función **Habilitar pedidos de compra del proyecto en Project Operations para escenarios basados en recursos/sin existencias**.
3. Seleccione **Habilitar**.
4. Configure los materiales de los que no hay existencias y las facturas de proveedor pendientes como se describe en [Configurar materiales de los que no hay existencias y facturas de proveedores pendientes](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Cree un pedido de compra de proyecto a partir de la lista de pedidos de compra del proyecto

1. En Finance, vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos** y seleccione y un proyecto.
2. En el panel de acciones, en la pestaña **Administrar**, en el grupo **Nuevo**, seleccione **Tarea de artículo** > **Pedido de compra**.
3. En la página **Crear pedido de compra**, seleccione el proveedor con el que desea realizar el pedido de compra, ingrese otra información según corresponda y luego seleccione **Aceptar**.
4. En la página **Pedido de compra**, en la cuadrícula **Líneas de pedido de compra**, seleccione **Agregar línea**.
5. Ingrese un número de producto, cantidad, unidad, precio unitario y otra información según corresponda.

    > [!NOTE]
    > Solo los artículos y servicios no mantenidos en existencias se pueden usar con los pedidos de compra del proyecto. No se admiten artículos mantenidos en existencias y categorías de compras.

6. Continúe agregando artículos según sea necesario y confirme el pedido de compra.

    Los recibos de bienes y servicios se pueden registrar creando y contabilizando un recibo de producto.

    > [!NOTE]
    > Los recibos de productos no se registran en los datos reales del proyecto en Microsoft Dataverse y no afectan a la subcontabilidad del proyecto.

    Después de que un proveedor envía la factura de los artículos y servicios en el pedido de compra, el departamento de compras puede generar una factura para el pedido de compra en **Factura** > **Generar** > **Factura** en el Panel de acciones. Para obtener más información sobre las facturas de proveedores pendientes, consulte [Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente](pending-vendor-invoices.md).
