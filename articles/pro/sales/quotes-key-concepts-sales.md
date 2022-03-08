---
title: 'Ofertas: conceptos clave (lite)'
description: En este tema se proporciona información sobre el uso de ofertas de proyectos en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009462"
---
# <a name="concepts-unique-to-project-quotes"></a>Conceptos únicos para ofertas de proyectos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_


Los siguientes son conceptos clave que debe conocer antes de comenzar a usar los contratos de proyecto en Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unidad de contratación

La unidad contratante representa la división o práctica propietaria de la entrega del proyecto. Puede configurar costes de recursos para cada unidad de contratación. Cuando especifique el coste del recurso para un recurso de la unidad de contratación, también podrá configurar diferentes tarifas de coste para los recursos que esta unidad de contratación toma prestados, u otra división o prácticas dentro de la empresa. Estos se conocen como precios de transferencia, préstamos de recursos o precios de cambio. Cuando configura el coste de pedir prestados recursos de otras divisiones, también puede optar por configurar esas tarifas de coste en la moneda de la división que presta.

## <a name="cost-currency"></a>Divisa de coste

La divisa de coste en Project Operations es la divisa en la que se informan los costes. Esta moneda se deriva de la moneda adjunta al campo **Unidad de contratación** de la oferta, el contrato y el proyecto. Los costes se pueden registrar en cualquier moneda contra un proyecto. Sin embargo, existe una conversión de moneda de la moneda en que se registraron los costes a la moneda de coste del proyecto.

Debido a que las tasas de cambio en la plataforma CDS no pueden tener vigencia en una fecha determinada, los totales en pantalla del coste pueden cambiar con el tiempo si actualiza las tasas de cambio de moneda. Sin embargo, los costes registrados en la base de datos permanecen sin cambios porque los importes se almacenan en la moneda en la que se incurrieron.

## <a name="sales-currency"></a>Divisa de ventas

La moneda de ventas en Project Operations es la moneda en la que se registran y muestran los importes de ventas estimados y reales. También es la moneda en la que se factura al cliente la transacción. En una oferta de proyecto, la moneda de venta se establece por defecto en el registro de cuenta o cliente y se puede cambiar cuando se crea la oferta. Una vez guardada la oferta, no se puede cambiar la moneda de ventas. Las listas de precios de productos y proyectos están predeterminadas en función de la moneda de venta de la oferta.

A diferencia de los costes, los valores de ventas solo se pueden registrar en la moneda de Ventas.

## <a name="billing-method"></a>Método de facturación

Los proyectos suelen tener modelos de contratación de tarifa fija y basados en el consumo. Esto se representa en Project Operations como **Método de facturación** y tiene dos valores, tiempo y material y precio fijo.

- **Tiempo y material:** este es un modelo de contrato basado en el consumo donde cada coste incurrido está respaldado por los ingresos correspondientes. A medida que estime o incurra en más costos, las ventas estimadas y reales correspondientes también aumentarán. Puede especificar límites que no deben excederse en las líneas de oferta que tienen este método de facturación. Esto limitará por arriba los ingresos reales. Los ingresos estimados no se ven afectados por los límites que no se deben exceder.
- **Precio fijo:** este es un modelo de contrato de tarifa fija que indica que los valores de venta serán independientes de los costes incurridos. El valor de venta es fijo y no cambia a medida que estima o incurre en más costes.

## <a name="project-price-lists"></a>Listas de precios de proyectos

Las listas de precios del proyecto son listas de precios que se utilizan para los precios predeterminados, no las tarifas de coste, para el tiempo, los gastos y otros componentes relacionados con el proyecto. Puede haber varias listas de precios, y cada lista puede tener su propia fecha de vigencia para cada presupuesto de proyecto. La superposición de fechas de vigencia de las listas de precios de proyecto no se admite en Project Operations.

## <a name="product-price-lists"></a>Listas de precios de productos

Las listas de precios de productos son listas de precios que se utilizan para los precios predeterminados, no las tarifas de coste, para las líneas basadas en productos de una oferta. Solo hay una lista de precios de productos por oferta.

## <a name="transaction-classes"></a>Clases de transacciones

Project Operations admite cuatro tipos de clases de transacciones:

- Tiempo
- Gasto
- Material
- Tarifa

Los valores de costes y ventas se pueden estimar e incurrir en Tiempo, Gastos y clases de Transacciones de material. La tarifa es una clase de transacciones de solo ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabajo y entidades de facturación

Las entidades que representan el trabajo son Proyectos y Tareas. Las entidades que representan la facturación son las líneas de Oferta y las líneas de Contrato. Puede vincular diferentes entidades de trabajo a opciones de facturación asociándolas con líneas de Oferta o Contrato.

## <a name="multi-customer-deals"></a>Ofertas para varios clientes

Los acuerdos con varios clientes se producen cuando hay más de un cliente para facturar. Entre los ejemplos comunes de esto se encuentran:

- **Empresas OEM y sus socios:** los socios y revendedores venden un producto con servicios de valor agregado. Este suele ser un escenario en el que durante una oferta particular con un cliente, el OEM ofrece financiar una parte del proyecto. 

- **Proyectos del sector público:** varios departamentos de una administración pública local acuerdan financiar un proyecto y se facturan de acuerdo con una división previamente acordada. Por ejemplo, un distrito escolar y la ciudad o el departamento de administración pública local acuerdan financiar la construcción de una piscina.

## <a name="invoice-schedules"></a>Programar facturas

Los programas de facturación son específicos para cada línea de oferta y también son opcionales. Los programas de facturación se crean en función de determinadas fechas de inicio y finalización y la frecuencia de facturación. Los programas de facturación se utilizan en la etapa de contrato cuando se configura el proceso de creación automática de facturas. En la etapa de oferta, las programaciones son opcionales. Cuando se crean programas de facturas en la fase **Oferta**, se copian en el contrato del proyecto que se crea cuando se gana una oferta del proyecto.

## <a name="changes-from-dynamics-365-sales-quote"></a>Cambios desde una oferta de Dynamics 365 Sales:

Las ofertas de Project Operations se basan en las ofertas de Dynamics 365 Sales. Sin embargo, existen algunas diferencias importantes en la funcionalidad que debe conocer:

- Las acciones **Revisar** y **Activar** no son compatibles.
- Las ofertas de Project Operations tienen dos tipos diferentes de líneas. Una es para líneas de proyecto y la otra es para productos.
- Las ofertas de Project Operations tienen su propio formulario y elementos de interfaz de usuario, reglas de negocio, lógica de negocio en complementos y scripts del lado del cliente que las hacen únicos en las ofertas de Ventas.

Por estas razones, no se recomienda utilizar una oferta de Ventas y una oferta de Project Operations indistintamente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
