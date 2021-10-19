---
title: Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente
description: Este tema explica cómo registrar facturas de proveedor pendientes.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547310"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Adquirir materiales no mantenidos en existencias utilizando una factura de proveedor pendiente

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando una empresa adquiere materiales no mantenidos en existencias para un proyecto, los costes se pueden registrar inmediatamente en el proyecto. 

Por ejemplo, Contoso Robotics US está realizando un proyecto de renovación de equipos y necesita licencias de software. Estas licencias se obtienen de un proveedor externo.  Utilizando Dynamics 365 Finance, el empleado de Proveedores registra un documento de factura de proveedor pendiente y atribuye los costes de la licencia directamente al proyecto de renovación del equipo. 

> [!IMPORTANT]
> Antes de utilizar la funcionalidad descrita en este tema, revise y aplique las configuraciones necesarias. Para más información, vea [Habilitar materiales no mantenidos en existencias y facturas de proveedor pendiente](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrar una factura de proveedor pendiente relacionada con el proyecto 

Las facturas de proveedor pendientes se pueden registrar en la página **Facturas de proveedor pendientes** (**Proveedores** > **Facturas** > **Facturas de proveedor pendientes**). Complete los siguientes pasos para registrar una factura de proveedor pendiente relacionada con el proyecto:

1. Vaya a **Proveedores** > **Facturas** y seleccione **Nueva**. 
2. En el campo **Cuenta de facturación**, seleccione un proveedor y en el campo **Número**, ingrese la identificación de la factura del proveedor.
3. Agregue una línea a la factura del proveedor y en el campo **Número de artículo**, seleccione el artículo no mantenido en existencias comprado al proveedor. 

    > [!NOTE]
    > Las líneas de factura de proveedor que se basan en una categoría de adquisición no se pueden registrar en el proyecto. 
    
5. Agregue la cantidad comprada. El sistema completará el precio unitario según la configuración del precio del artículo no mantenido en existencias. 
6. Verifique el importe total y otros detalles requeridos en la línea.
7. En los detalles de la línea, en la pestaña **Proyecto**, seleccione el ID del proyecto en el que se registrará este elemento.
8. Opcionalmente, seleccione el número de actividad y actualice la categoría del proyecto y la propiedad de la línea.
9. Registre la factura del proveedor pendiente. Cuando se contabiliza la factura, el sistema registra:
    
    - El importe del saldo del proveedor.
    - El importe del impuesto sobre ventas.
    - El coste del proyecto se registra en la cuenta de integración de adquisiciones.
    - La transacción de costo real del proyecto en Dataverse.  La transacción se sigue procesando utilizando el diario [Integración de Project Operations](../project-accounting/project-operations-integration-journal.md). El registro de este diario mueve el importe de la cuenta de integración de compras a la cuenta de coste del proyecto. 
    - Compras que se facturan al cliente del proyecto mediante el método de facturación de tiempo y materiales. Además, se crean transacciones de ventas no facturadas para las compras en Dataverse. La lista de precios del producto en Dataverse se utiliza para los precios de venta y los importes de la transacción de venta no facturada.
