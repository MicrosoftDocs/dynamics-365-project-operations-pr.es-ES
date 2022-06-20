---
title: Adquirir materiales no mantenidos en existencias o categorías de adquisición usando facturas de proveedor pendientes
description: Este artículo explica cómo registrar facturas de proveedores pendientes.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922013"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Adquirir materiales no mantenidos en existencias o categorías de adquisición usando facturas de proveedor pendientes

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

A medida que una empresa adquiere materiales no en existencias o categorías de adquisición para un proyecto, los costes se pueden registrar inmediatamente contra el proyecto. 

Por ejemplo, Contoso Robotics US está realizando un proyecto de renovación de equipos y necesita licencias de software. Estas licencias se obtienen de un proveedor externo.  Con Dynamics 365 Finance, el empleado Proveedores registra un documento de factura de proveedor pendiente y atribuye los costos de la licencia directamente al proyecto de renovación del equipo. 

> [!IMPORTANT]
> Antes de usar la funcionalidad descrita en este artículo, revise y aplique las configuraciones requeridas. Para más información, consulte [Habilitar materiales no almacenados y facturas de proveedores pendientes](configure-materials-nonstocked.md) y [Usar categorías de adquisición con pedidos de compra de proyectos y facturas de proveedores pendientes](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrar una factura de proveedor pendiente relacionada con el proyecto 

Las facturas de proveedor pendientes se pueden registrar en la página **Facturas de proveedor pendientes** (**Proveedores** > **Facturas** > **Facturas de proveedor pendientes**). Complete los siguientes pasos para registrar una factura de proveedor pendiente relacionada con el proyecto:

1. Vaya a **Proveedores** > **Facturas** y seleccione **Nueva**. 
1. En el campo **Cuenta de factura** seleccione un proveedor y, a continuación, en el campo **Número**, introduzca la identificación de la factura del proveedor.
1. Agregue una línea a la factura del proveedor y luego, en el campo **Número de artículo**, seleccione el artículo no almacenado que se compró al proveedor. Alternativamente, en el campo **Categoría de adquisiciones**, seleccione la categoría de adquisiciones que se compró al proveedor.   
1. Agregue la cantidad que se compró. El sistema rellena el precio unitario, según la configuración del precio del artículo no en existencias. 
1. Verifique el importe total y otros detalles requeridos en la línea.
1. En los detalles de la línea, en la pestaña **Proyecto**, seleccione el id. del proyecto en el que se registrará este elemento.
1. Opcional: seleccione el número de actividad y actualice la categoría del proyecto y la propiedad de la línea.
1. Registre la factura del proveedor pendiente. Cuando se contabiliza la factura, el sistema registra la siguiente información:
    
    - El importe del saldo del proveedor.
    - El importe del impuesto sobre ventas.
    - El coste del proyecto se registra en la cuenta de integración de adquisiciones.
    - La transacción de costo real del proyecto en Dataverse.  La transacción se sigue procesando utilizando el diario [Integración de Project Operations](../project-accounting/project-operations-integration-journal.md). El registro de este diario mueve el importe de la cuenta de integración de compras a la cuenta de coste del proyecto. 
    - Compras que se facturan al cliente del proyecto mediante el método de facturación de tiempo y materiales. Además, se crean transacciones de ventas no facturadas para las compras en Dataverse. La lista de precios del producto en Dataverse se utiliza para los precios de venta y los importes de la transacción de venta no facturada.
