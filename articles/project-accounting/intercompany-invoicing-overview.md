---
title: Información general de facturación con empresas vinculadas
description: En este tema se proporciona información y ejemplos sobre la facturación con empresas vinculadas para proyectos.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c343c5bf525574e496036793cd4e131394e8b1b471153147a66cfebe1acf3fce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005412"
---
# <a name="intercompany-invoicing-overview"></a>Información general de facturación con empresas vinculadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Su organización puede tener varias divisiones, subsidiarias y otras entidades jurídicas que se transfieren productos y servicios entre sí para proyectos. La entidad jurídica que proporciona el servicio o producto se denomina *entidad jurídica prestamista*. La entidad jurídica que recibe el servicio o producto se denomina *entidad jurídica prestataria*.

La siguiente ilustración muestra un escenario típico donde dos entidades jurídicas, Contoso Robotics USA (la entidad jurídica prestataria) y Contoso Robotics UK (la entidad jurídica prestamista) comparten recursos para entregar un proyecto al cliente, Adventure Works. Para este escenario, Contoso Robotics USA está contratado para entregar el trabajo a Adventure Works.

![Facturación entre empresas vinculadas.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations utiliza el siguiente flujo para procesar transacciones entre empresas vinculadas:

1. Los recursos de la entidad jurídica prestamista registran las transacciones de tiempo o gasto de empresas vinculadas reservando el tiempo y el gasto para proyectos en la entidad jurídica prestataria.
2. Los costes de tiempo y gasto se registran en la empresa prestamista utilizando la lista de precios de coste unitario de la empresa prestataria.
3. Las transacciones de venta sin facturar de empresas vinculadas se registran en la empresa prestamista utilizando la lista de precios de coste unitario de la empresa prestataria.
4. Los ingresos sin facturar se registran en la empresa prestataria utilizando la lista de precios de venta del contrato del proyecto. Se puede facturar al cliente cuando se registran los ingresos no facturados. El cliente no tiene que esperar hasta que se complete el procesamiento de facturas de empresas vinculadas.
5. Las facturas de clientes de empresas vinculadas se crean periódicamente en la empresa prestamista. Las facturas se crean manualmente o mediante un proceso automatizado periódico. Se puede crear una sola factura para cada entidad legal prestataria o se pueden crear facturas independientes por proyecto.
6. Cuando la factura del cliente de empresas vinculadas se registra en la entidad jurídica prestamista, se crea la factura de proveedor pendiente correspondiente en la entidad jurídica prestataria. Los costes de la factura de proveedor pendiente se registrarán en el libro auxiliar del proyecto cuando se registre la factura.

El siguiente diagrama muestra la facturación de empresas vinculadas en relación con los eventos contables y los registros previstos en la contabilidad general.

![Flujo de empresas vinculadas.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Recursos adicionales

- [Configurar la facturación con empresas vinculadas](configure-intercompany-invoicing.md)
- [Registrar transacciones de empresas vinculadas](create-intercompany-transactions.md)
- [Crear facturas de proveedores y clientes de empresas vinculadas](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]