---
title: Conceptos únicos para ofertas basadas en proyectos
description: Este artículo proporciona información sobre la copia de ofertas de proyectos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824373"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceptos únicos para ofertas basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Antes de comenzar a utilizar presupuestos de proyectos en Microsoft Dynamics 365 Project Operations, debe conocer los siguientes conceptos clave.

## <a name="owning-company"></a>Empresa propietaria

La empresa propietaria representa a la entidad jurídica propietaria de la entrega del proyecto. El cliente en la cotización debe ser un cliente válido en esa entidad legal en aplicaciones de finanzas y operaciones. La moneda de la empresa propietaria y la moneda de la unidad de contratación seleccionada en una cotización basada en proyectos deben coincidir.

## <a name="contracting-unit"></a>Unidad de contratación

Una unidad contratante representa la división o práctica propietaria de la entrega del proyecto. Puede configurar los costes de recursos de cada unidad de contratación. Cuando especifique los costes del recurso para un recurso de una unidad de contratación, también puede configurar diferentes tarifas de coste para los recursos que la unidad de contratación toma prestados, o para otras divisiones o prácticas dentro de la empresa. Estas tasas de costes se conocen como precios de transferencia, préstamos de recursos o precios de cambio. Cuando configura el coste de pedir prestados recursos de otras divisiones, puede configurar las tarifas de coste en la moneda de la división que presta.

## <a name="cost-currency"></a>Divisa de coste

La divisa de coste en Project Operations es la divisa en la que se informan los costes. Esta moneda se deriva de la moneda adjunta al campo **Unidad de contratación** de la oferta, el contrato y el proyecto. Los costes de un proyecto se pueden registrar en cualquier divisa. Sin embargo, existe una conversión de moneda de la moneda en que se registraron los costes a la moneda de coste del proyecto.

Debido a que las tasas de cambio en la plataforma Dataverse no pueden tener vigencia en una fecha determinada, los totales en pantalla del coste podría cambiar con el tiempo si actualiza las tasas de cambio de moneda. Sin embargo, los costes registrados en la base de datos permanecen sin cambios porque los importes se almacenan en la moneda en la que se incurrieron.

## <a name="sales-currency"></a>Divisa de ventas

La moneda de ventas en Project Operations es la moneda en la que se registran y muestran los importes de ventas estimados y reales. También es la moneda en la que se factura al cliente la transacción. Para una oferta de proyecto, se establece una moneda de venta por defecto en el registro de cuenta o cliente y se puede cambiar cuando se crea la oferta. En cambio,  no se puede cambiar la moneda de ventas una vez guardada la oferta. Las listas de precios de productos y proyectos predeterminadas se basan en la moneda de venta de la oferta.

A diferencia de los costes, los valores de ventas **solo** se pueden registrar en la moneda de ventas.

## <a name="billing-method"></a>Método de facturación

Los proyectos suelen tener modelos de contratación de tarifa fija y basados en el consumo. En Project Operations, el modelo de contratación de un proyecto está representado por el método de facturación. El método de facturación tiene dos valores: tiempo y material y precio fijo.

- **Tiempo y material:** un modelo de contrato basado en el consumo donde cada coste incurrido está respaldado por los ingresos correspondientes. A medida que estime o incurra en más costos, las ventas estimadas y reales correspondientes también aumentan. Puede especificar límites que no deben excederse en las líneas de oferta que tienen este método de facturación. De esta forma, puede limitar los ingresos reales. Los ingresos estimados no se ven afectados por los límites que no se deben exceder.
- **Precio fijo**: un modelo de contrato de tarifa fija donde los valores de venta son independientes de los costes incurridos. El valor de venta es fijo y no cambia a medida que estima o incurre en más costes.

## <a name="project-price-lists"></a>Listas de precios de proyectos

Las listas de precios del proyecto son listas de precios que se utilizan para introducir los precios predeterminados, no las tarifas de coste, para el tiempo, los gastos y otros componentes relacionados con el proyecto. Puede haber varias listas de precios, y cada lista puede tener su propia fecha de vigencia para cada presupuesto de proyecto. En Project Operations no se admite la superposición de validez de fechas en las listas de precios de proyecto.

## <a name="product-price-lists"></a>Listas de precios de productos

Las listas de precios de productos son listas de precios que se utilizan para introducir los precios predeterminados, no las tarifas de coste, para las líneas basadas en productos de una oferta. Solo hay una lista de precios de productos por oferta.

## <a name="transaction-classes"></a>Clases de transacciones

Project Operations admite cuatro tipos de clases de transacciones:

- Tiempo
- Gasto
- Material
- Tarifa

Los valores de costes y ventas se pueden estimar e incurrir en las clases de transacciones **Tiempo**, **Gastos** y **Material** . **Tarifa** es una clase de transacción solo para ingresos.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabajo y entidades de facturación

Los proyectos y tareas son entidades que representan el trabajo. Las líneas de Oferta y las líneas de Contrato son entidades que representan la facturación. Puede vincular diferentes entidades de trabajo a opciones de facturación asociándolas con líneas de Oferta o Contrato.

## <a name="multi-customer-deals"></a>Ofertas para varios clientes

Los acuerdos con varios clientes se producen cuando hay más de un cliente por factura. A continuación se incluyen algunos ejemplos típicos:

- **Empresas de fabricantes de equipos originales (OEM) y sus socios:** los socios y revendedores venden un producto que incluyen servicios de valor agregado. Durante una oferta particular con un cliente, el OEM normalmente ofrece financiar una parte del proyecto.
- **Proyectos del sector público:** varios departamentos de una administración pública local acuerdan financiar un proyecto y se facturan de acuerdo con una división previamente acordada. Por ejemplo, un distrito escolar y la ciudad o el departamento de administración pública local acuerdan financiar la construcción de una piscina.

## <a name="invoice-schedules"></a>Programar facturas

Los programas de facturación son específicos para cada línea de oferta y son opcionales. Los programas de facturas se crean en función de determinadas fechas de inicio y finalización, así como la frecuencia de facturación. Se usan durante la etapa de contrato cuando se configura el proceso de creación automática de facturas. Durante la etapa de oferta, las programaciones de factura son opcionales. Si se crean en la fase oferta, se copian en el contrato del proyecto que se crea cuando se gana una oferta del proyecto.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferencias con las ofertas de Dynamics 365 Sales

Las ofertas de Project Operations se basan en las ofertas de Dynamics 365 Sales. Sin embargo, existen algunas diferencias importantes en la funcionalidad que debe conocer:

- Las ofertas de Project Operations tienen dos tipos diferentes de líneas, una para proyectos y otra para productos.
- Las ofertas de Project Operations tienen su propia página y elementos de interfaz de usuario (IU), reglas de negocio, lógica de negocio en complementos y scripts del lado del cliente que las hacen diferentes de las ofertas de Ventas.
- En Sales, ouede adjuntar varios pedidos a una oferta de ventas. En Project Operations, solo puede adjuntar un contrato de proyecto a una oferta de proyecto.
- Cuando gana una oferta de venta, la oportunidad relacionada puede permanecer abierta. Tras ganar una oferta de proyecto, la oportunidad relacionada se cierra.
- Las ofertas de ventas no incluyen algunos campos y conceptos que se incluyen en una oferta de proyecto. Entre los campos se incluyen **Unidad de contratación**, **Administrador de cuentas** y **Nombre de contacto de facturación**.
- Las ofertas de ventas y de proyecto también se identifican mediante el campo **Tipo** basado en un conjunto de opciones. Para una oferta de ventas, el valor de este campo es **Basado en artículo**. Para una oferta de proyecto, el valor es **Basado en trabajo**.

Debido a estas diferencias, no recomendamos que use ofertas de Sales y Project Operations de manera intercambiable.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
