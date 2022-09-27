---
title: Pagos de proveedores de pago cuando se pagan
description: Este tema explica cómo usar el escenario de pago cuando se paga (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525346"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagos de proveedores de pago cuando se pagan

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema explica cómo usar el escenario de pago cuando se paga (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Crear una orden de compra que tenga términos de PWP

Cuando registra una factura de un proveedor, si el proveedor está sujeto a los términos de PWP, esos términos se muestran en las líneas de orden de compra (PO). Para crear una orden de compra que tiene términos PWP, siga estos pasos.

1. Siga uno o varios de estos pasos en Microsoft Dynamics 365 Finance:

    - Vaya a **Adquisiciones y abastecimiento** \> **Pedidos de compra** \> **Todos los pedidos de compra**. En el panel de acción seleccione **Nuevo**. En el cuadro de diálogo **Crear orden de compra**, seleccione el proveedor para el que se configuraron los términos de PWP en el proyecto, ingrese otra información requerida y luego seleccione **ACEPTAR**.
    - Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos**. En el panel de acciones, en la pestaña **Administrar**, seleccione **Tarea de artículos**. Seleccione el pedido de compra. Seleccione el proveedor para el que se configuran los términos de PWP en el proyecto y, a continuación, seleccione **ACEPTAR**.

2. Sobre la página **Orden de compra**, en la ficha rápida, **Líneas de orden de compra**, seleccione **Añadir línea** para crear una línea de orden de compra.
3. Seleccione el número de artículo o la categoría de adquisición e ingrese los demás detalles requeridos. Revise los detalles de la línea de orden de compra para el proveedor.

    La opción **Pagar cuando cobre** se selecciona automáticamente y el valor del campo **Porcentaje de umbral de PWP** se copia automáticamente del campo **Porcentaje de umbral de PWP** en la página **Proyectos**.

4. Si no desea aplicar los términos de PWP al proveedor para una línea de pedido de compra, borre la opción **Pago al cobro**. En este caso, el campo **Porcentaje de umbral de PWP** de la línea de orden de compra se restablecerá a **0** (cero).
5. En la página **Orden de compra**, en el panel de acciones, en la pestaña **Compra**, seleccione **Confirmar** para confirmar la orden de compra.
6. En el panel de acciones, en la pestaña **Factura**, seleccione **Factura** para generar la factura del pedido de compra.

## <a name="create-a-project-invoice-proposal"></a>Crear una propuesta de factura de proyecto

Las propuestas de factura de proyecto se utilizan para crear facturas de proyecto para el cliente. En el escenario de PWP, los pagos de los proveedores dependen de los pagos de los clientes según la configuración de PWP. Sin embargo, existen opciones que le permiten liberar los pagos sin los pagos de los clientes según lo requiera. Para crear una factura de proyecto para el cliente, siga estos pasos.

1. En las aplicaciones de participación del cliente, vaya a **Proyecto** \> **Proyectos** y seleccione el proyecto.
2. En la pestaña **Datos reales**, seleccione la línea real generada por la orden de compra que tiene el tipo de transacción **Ventas no facturadas**. Luego seleccione **Listo para la factura**.
3. Vaya a **Ventas** \> **Ventas** \> **Contrato de proyecto** y seleccione el contrato del proyecto.
4. En el panel de acciones, seleccione **Factura** para generar la factura de cliente.
5. En Finance, vaya a **Administración y contabilidad de proyectos** \> **Periódicos** \> **Importar desde tabla de almacenamiento provisional** y seleccione **Aceptar** para generar el diario de integración de Project Operations.
6. Vaya a **Gestión de proyectos y contabilidad** \> **Facturas de proyecto** \> **Propuesta de factura de proyecto** y seleccione **Correo** para registrar la propuesta de factura que se generó para el proyecto.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizar el pago de un cliente y pagar al proveedor

Cuando un proveedor completa su trabajo en un proyecto y le envía una factura, debe revisar el estado del proyecto y las facturas del cliente para determinar si se han cumplido los términos de PWP para el proyecto. Si se cumplieron los términos de PWP para el proveedor, puede determinar qué líneas de la factura del proveedor pagar, según los pagos del cliente por el proyecto. Si decide pagarle al proveedor aunque no se cumplieron los términos de PWP, puede anular los términos de PWP en la página **Factura del proveedor con pago al cobro**.

1. En Finance, vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos** y seleccione el proyecto.
2. En el panel de acciones, seleccione **Control** y luego seleccione **Facturas de proveedores** para mostrar todas las facturas de proveedor que se han generado para el proyecto.
3. En la página **Facturas de proveedores con pago al cobro**, en el campo de búsqueda, introduzca los valores para encontrar la factura del proveedor que desea revisar y luego seleccione **Buscar**.
4. Seleccione la opción **Pagar cuando se paga** para ver solo las facturas de PWP.
5. En la ficha desplegable **Líneas de factura de proveedor**, seleccione las líneas que liberar para el pago.
6. Seleccione **Liberar pago de proveedor**. La opción **Pago al cobro** se borra y el valor del campo **Listo para el pago** se cambia a **Sí**.
