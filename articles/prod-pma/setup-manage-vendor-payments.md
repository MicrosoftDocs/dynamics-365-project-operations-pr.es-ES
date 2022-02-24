---
title: Configurar y utilizar pagos de proveedores de pago cuando se pagan
description: Este tema explica cómo crear condiciones de pago cuando se paga (PWP) para que pueda liberar pagos parciales a proveedores, según los pagos de los clientes.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085127"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configurar y utilizar pagos de proveedores de pago cuando se pagan

[!include [banner](../includes/banner.md)]

Cuando aprueba a un proveedor para trabajar como subcontratista, es posible que desee retener el pago al proveedor hasta que su cliente le pague por el proyecto. Para respaldar este escenario, puede configurar términos de pago cuando se paga (PWP) cuando configura la orden de compra (PO) con el proveedor.

Por ejemplo, cuando un cliente paga un monto en una factura de proyecto, puede liberar parte o todo el monto de la factura del proveedor. Simplemente configure los términos de PWP que especifiquen que se le pagará al proveedor después de que usted reciba un porcentaje del pago relacionado del cliente. Si recibe un pago parcial de un cliente, puede liberar manualmente algunas de las facturas de proveedor relacionadas para el pago.

El siguiente ejemplo describe el proceso cuando se utilizan términos de PWP.

## <a name="example"></a>Ejemplo

Su organización acepta proporcionar a un cliente 100 ordenadores que tengan software instalado, por un precio de 150,00 dólares estadounidenses (USD) por ordenador. Luego, contrata a un proveedor para que le proporcione los ordenadores que tienen el software instalado. Según el acuerdo, el cliente debe aprobar la calidad de las computadoras antes de pagar a su organización. La política de su organización es retener el pago a los proveedores hasta que el cliente le haya pagado. Por lo tanto, configura el proyecto para que tenga un porcentaje de PWP del 100 por ciento.

El proveedor le envía los 100 ordenadores que tienen software instalado, junto con una factura por 10 000,00 USD. Debido a que los términos de PWP están configurados para su proyecto, no le paga al proveedor al recibir las computadoras. En su lugar, envía los ordenadores al cliente, junto con una factura por 15 000,00. El cliente inspecciona los ordenadores y aprueba el monto total de la factura del proyecto.

Después de recibir el pago completo del cliente, le paga al proveedor 10 000,00, el monto total de la factura del proveedor.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurar términos de PWP para un proyecto

Cuando configura los términos de PWP para un proyecto, debe especificar, como un porcentaje, la cantidad mínima que un cliente debe pagarle por el proyecto antes de pagarle al proveedor. La cantidad de umbral se calcula automáticamente en las facturas de los clientes para el proyecto. Siga estos pasos para configurar el porcentaje de umbral para los términos de PWP.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos**.
2. Busque y abra el proyecto para el que desea configurar los términos de PWP.
3. En la ficha desplegable **Acuerdos de proveedor**, seleccione **Agregar línea**.
3. En el campo **Código de cuenta**, seleccione una de las siguientes opciones:

    - **Tabla**: los términos de PWP se aplican a un solo proveedor.
    - **Grupo**: los términos de PWP se aplican a todos los proveedores de un grupo de proveedores.
    - **Todos**: los términos de PWP se aplican a todos los proveedores.

4. Si seleccionó **Tabla** o **Grupo** en el paso anterior, en el campo **Proveedor / Grupo de proveedores**, seleccione el proveedor o grupo de proveedores al que se aplican los términos de PWP. Si ha seleccionado **Todos** en el paso anterior, el campo **Proveedor / Grupo de proveedores** no se puede editar.
5. Si los términos de retención de proveedores están configurados para el proveedor en el proyecto, en el campo **Términos de retención de proveedores**, seleccione el identificador de la regla para los términos de retención.
6. En el campo **Porcentaje de umbral de PWP**, introduzca el porcentaje de umbral para el proyecto. El porcentaje que introduce para el proyecto define la cantidad mínima que el cliente debe pagarle antes de que usted le pague al proveedor.

## <a name="create-a-po-that-has-pwp-terms"></a>Crea una orden de compra que tenga términos de PWP

Cuando registra una factura de un proveedor, si el proveedor está sujeto a los términos de PWP, esos términos se muestran en las líneas de orden de compra. Para crear una orden de compra que tiene términos PWP, siga estos pasos.

1. Vaya a **Adquisiciones y abastecimiento** \> **Pedidos de compra** \> **Todos los pedidos de compra**.
2. En el panel de acción seleccione **Nuevo**. Después en el cuadro de diálogo **Crear pedido de compra** introduzca la información obligatoria y seleccione **ACEPTAR**.

    Alternativamente, abra un pedido de compra existente en la página de lista **Todos los pedidos de compra**.

4. En la página **Pedido de compra**, en la ficha desplegable **Líneas de pedido de compra**, revise los detalles de la línea de pedido de compra del proveedor. La opción **Pagar cuando cobre** se selecciona automáticamente y el valor del campo **Porcentaje de umbral de PWP** se copia automáticamente del campo **Porcentaje de umbral de PWP** en la página **Proyectos**.
6. Si no desea aplicar los términos de PWP al proveedor para una línea de pedido de compra, borre la opción **Pago al cobro**. En este caso, el campo **Porcentaje de umbral de PWP** de la línea de orden de compra se restablecerá a 0 (cero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualizar el pago de un cliente y pagar al proveedor

Cuando un proveedor completa su trabajo en un proyecto y le envía una factura, debe revisar el estado del proyecto y las facturas del cliente para determinar si se han cumplido los términos de PWP para el proyecto. Si se cumplieron los términos de PWP para el proveedor, puede determinar qué líneas de la factura del proveedor pagar, según los pagos del cliente por el proyecto. Si decide pagarle al proveedor aunque no se cumplieron los términos de PWP, puede anular los términos de PWP en la página **Factura del proveedor con pago al cobro**.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Consultas e informes** \> **Consultas de retención** \> **Factura del proveedor con pago cuando se paga**.
2. En la página **Facturas de proveedores con pago al cobro**, en el campo de búsqueda, introduzca los valores para encontrar la factura del proveedor que desea revisar y luego seleccione **Buscar**.
3. En la ficha desplegable **Líneas de factura de proveedor**, seleccione las líneas que desea cambiar.
4. Si las condiciones de **Pago al cobro** se cumplen para la línea de factura, seleccione **Liberar el pago del proveedor**. La opción **Pago al cobro** se borra y el valor del campo **Listo para el pago** se cambia a **Sí**.
