---
title: 'Contratos de proyectos: conceptos clave'
description: Este artículo proporciona información sobre los conceptos clave de los contratos de proyecto en Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 016a5d1defacdc6ba5828ca26395c9123e9323d0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926245"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Conceptos únicos para contratos basados en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_



Este artículo proporciona los conceptos clave que debe conocer antes de empezar a usar contratos de proyecto en Dynamics 365 Project Operations:

## <a name="owning-company"></a>Empresa propietaria

La empresa propietaria es la entidad jurídica del módulo **Administración de proyectos y contabilidad** para Project Operations de Dynamics 365 Finance. La empresa propietaria representa la entidad legal que contabilizará el costo y los ingresos que se derivan de un trato.

## <a name="contracting-unit"></a>Unidad de contratación

La unidad contratante representa la división o práctica propietaria de la entrega del proyecto. Puede configurar los costes de recursos de cada unidad de contratación. Cuando especifica el coste de un recurso, también puede configurar diferentes tarifas de costes para los recursos. Esta unidad contratante toma prestados estos recursos de otras divisiones o prácticas dentro de la empresa. Las tasas de coste para los recursos se conocen como precios de transferencia, préstamos de recursos o precios de cambio. Cuando configura las tasas de coste para pedir prestados recursos de otras divisiones, usa la moneda de la división que presta.

## <a name="cost-currency"></a>Moneda de coste

La moneda de coste es la divisa en la que se informan los costes en pantalla. Esta moneda se deriva de la moneda adjunta al campo **Unidad de contratación** del contrato y el proyecto. Los costes se pueden registrar en cualquier divisa para un proyecto. Sin embargo, existe una conversión de moneda de la moneda en que se registraron los costes a la moneda de coste del proyecto cuando aparecen en la pantalla.

Debido a que las tasas de cambio en la plataforma Common Data Service (CDS) no pueden tener vigencia en una fecha determinada, los totales en pantalla del coste pueden cambiar con el tiempo si actualiza las tasas de cambio de moneda. Sin embargo, los costes registrados en la base de datos permanecen sin cambios porque los importes se almacenan en la moneda en la que se incurrieron.

## <a name="sales-currency"></a>Divisa de venta

La moneda de ventas en Project Operations es la moneda en la que se registran y muestran los importes de ventas estimados y reales. La divisa de ventas es también la divisa en la que se factura la transacción al cliente. En un contrato de proyecto, la moneda de venta se establece por defecto en el registro de cuenta o cliente y se puede cambiar cuando se crea la cotización. Cuando se crea un contrato al cerrar una cotización como ganado, la divisa del contrato se establece por defecto con respecto a la divisa de la cotización.

Cuando crea un contrato de proyecto desde cero, el campo **Moneda de venta** no se puede editar. Las listas de precios de productos y proyectos están predeterminadas según esta moneda en el contrato.

A diferencia de los costes, los valores de ventas solo se pueden registrar en la moneda de ventas.

## <a name="billing-method"></a>Método de facturación

Estos son normalmente dos tipos de modelos de contrato para proyectos, precio fijo y basado en el consumo. Estos modelos se representan en Project Operations como métodos de facturación con dos valores posibles:

- Tiempo y material: un modelo de contrato basado en el consumo donde cada coste incurrido está respaldado por los ingresos correspondientes. A medida que estime o incurra en más costos, las ventas estimadas y reales correspondientes también aumentan. Especifique los límites que no deben excederse en las líneas de contrato que tienen este método de facturación que limita los ingresos reales. Los ingresos estimados no se ven afectados por los límites que no se deben exceder.
- Precio fijo: un modelo de contrato de tarifa fija que indica que los valores de venta serán independientes de los costes incurridos. El valor de venta es fijo y no cambia a medida que estima o incurre en más costes.

## <a name="project-price-lists"></a>Listas de precios de proyectos

Las listas de precios del proyecto se utilizan para los precios predeterminados, no las tarifas de coste, para el tiempo, los gastos y otros componentes relacionados con el proyecto. Puede haber varias listas de precios. Cada lista de precios tiene su propia fecha de vigencia para cada contrato de proyecto. La superposición de fechas de vigencia de las listas de precios de proyecto no se admite en Project Operations.

Cuando se crea un contrato de proyecto al ganar una cotización de proyecto, las listas de precios del proyecto se copian con el nombre del contrato y la fecha incluidos. Copiar esta información constituye un precio personalizado para los componentes del proyecto en este contrato de proyecto.

## <a name="transaction-classes"></a>Clases de transacciones

Project Operations admite cuatro tipos de clases de transacciones:

- Tiempo
- Gasto
- Material
- Tarifa

Los valores de costes y ventas se pueden estimar e incurrir en Tiempo, Gastos y clases de Transacciones de material. La tarifa es una clase de transacción de solo ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabajo y entidades de facturación

Las entidades que representan el trabajo son proyectos y tareas. Las entidades que representan aspectos de facturación son líneas de contrato. Puede vincular diferentes entidades de trabajo a opciones de facturación al asociarlas a las líneas del contrato.

## <a name="multi-customer-deals"></a>Ofertas para varios clientes

Los acuerdos con varios clientes deben tener más de un cliente para facturar un acuerdo. Entre los ejemplos comunes de esto se encuentran:

- Empresas OEM y sus socios: los socios y revendedores venden un producto con algunos servicios de valor agregado, que generalmente involucran un trato particular con un cliente. El OEM ofrece financiar una parte del proyecto. 

- Proyectos del sector público: varios departamentos de una administración pública local acuerdan financiar un proyecto y se facturan de acuerdo con una división previamente acordada. Por ejemplo, un distrito escolar y administración pública local acuerdan financiar la construcción de una piscina.

## <a name="invoice-schedules"></a>Programar facturas

Los programas de facturación son específicos para cada línea de contrato y son necesarios para que funcione la facturación automática. Los programas de facturas se crean en función de determinadas fechas de inicio y finalización, así como la frecuencia de facturación. Las programaciones se utilizan en la etapa de contrato cuando se configura el proceso de creación automática de facturas. Cuando un contrato de proyecto se crea a partir de una oferta, la factura está programada para copiarse al contrato de proyecto desde la oferta.

## <a name="changes-from-dynamics-365-sales-orders"></a>Cambios desde una oferta de Dynamics 365 Sales Orders

Los contractos en Project Operations se basan en los pedidos de Dynamics 365 Sales. Sin embargo, existen diferencias y desviaciones importantes en la funcionalidad. Los contratos tienen su propio formulario y elementos de interfaz de usuario, reglas de negocio, lógica de negocio en complementos y scripts del lado del cliente que las hacen únicos desde Orders. Por estas razones, no debe usar un contrato de Sales y un contrato de Project Operations de manera intercambiable.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
