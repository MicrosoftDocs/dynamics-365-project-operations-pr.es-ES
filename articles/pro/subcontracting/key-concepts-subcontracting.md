---
title: Conceptos clave en la subcontratación
description: Este tema explica algunos conceptos clave que se aplican a la subcontratación en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578178"
---
# <a name="key-concepts-in-subcontracting"></a>Conceptos clave en la subcontratación

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

El tema explica algunos conceptos clave que debe conocer antes de comenzar a utilizar la funcionalidad de subcontratación en Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unidad de contratación en el subcontrato

La unidad de contratación representa la división o práctica que posee la entrega final del proyecto. La unidad de contratación es también la división que entra en la relación contractual con el proveedor.

## <a name="purchase-currency"></a>Moneda de compra

En Project Operations, la moneda de compra es la moneda en la que se crea el subcontrato. También es la moneda en la que se registran los costes de los subcontratistas en un proyecto. La moneda de compra puede diferir de la moneda del proyecto y, a su vez, la moneda del proyecto puede diferir de la moneda de venta.

## <a name="billing-methods-on-subcontract-lines"></a>Métodos de facturación en líneas de subcontrato

Para los proyectos, existen modelos de contratación habituales de los proyectos y modelos basados en el consumo. Project Operations admite estos métodos de facturación en los contextos de ventas y compras. Para una compra, los métodos de facturación funcionan de la siguiente manera:

- **Tiempo y material** - Cuando una línea de subcontrato utiliza el método de facturación **Tiempo y material**, el coste del tiempo se registra en el proyecto a medida que los subcontratistas trabajan en ese proyecto y registran el tiempo. Estas transacciones de costes de los subcontratistas luego se comparan con los artículos de línea en las facturas de los proveedores. En este modelo, los administradores de proyecto que utilizan Project Operations pueden comparar y verificar las líneas de la factura del proveedor con el tiempo del subcontratista que se registra y se aprueba. Una vez completada la verificación, los costes reales anteriores que se registraron después de la aprobación se revierten y los nuevos costes reales que se basan en la factura del proveedor se crean en el proyecto.
- **Precio fijo** – En este modelo de contratación de tarifa fija, las facturas de los proveedores se basan en hitos fijos. Sin embargo, los recursos de los subcontratistas también pueden informar del tiempo. Luego, el administrador del proyecto revisa y aprueba el tiempo. Cuando está aprobado, Project Operations crea datos reales de costes temporales en el proyecto. Después de que el proveedor envíe una factura por un hito, el administrador del proyecto puede comparar los costes reales registrados previamente con el hito. Cuando se completa la verificación, los costes reales se invierten y se registra el coste basado en hitos.

## <a name="project-price-lists-on-subcontracts"></a>Listas de precios del proyecto en subcontratos

Las listas de precios del proyecto son listas de precios que se utilizan para configurar los precios de compra, para el tiempo, los gastos y otros componentes relacionados con el proyecto. Puede haber varias listas de precios, cada una de las cuales puede tener su propio subcontrato con fecha de vigencia en Project Operations. Project Operations no admite la superposición de fechas de vigencia en las listas de precios del proyecto para un subcontrato.

## <a name="transaction-classes-on-subcontracts"></a>Clases de transacciones en subcontratos

Project Operations admite cuatro tipos de clases de transacciones:

- Tiempo
- Gasto
- Material
- Precio

Los costes de compra se pueden estimar e incurrir solo en las clases de transacciones **Tiempo**, **Gasto** y **Material** . **Tarifa** es una clase de transacción que solo genera ingresos y no está disponible en el contenido de compras.

## <a name="purchase-pricing-dimensions"></a>Dimensiones de precios de compra

Las dimensiones de precios le permiten decidir qué atributos se utilizan para la configuración de precios de compra y el cumplimiento de las transacciones a tiempo. En relación con las compras, Project Operations solo admite conjuntos de dimensiones fijas para la configuración y el cumplimiento del precio de compra. Para la configuración del precio de compra y el cumplimiento de las líneas de subcontrato y las transacciones de tiempo de subcontrato, los atributos son **Papel** y **Recurso que se puede reservar**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
