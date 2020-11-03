---
title: 'Ofertas: conceptos clave'
description: En este tema se proporciona información sobre las ofertas de proyecto y las ofertas de ventas disponibles en Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42ea1eb71b3285159b3fdf79ba34a562f948fd6e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085314"
---
# <a name="quotes---key-concepts"></a>Ofertas: conceptos clave

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En Dynamics 365 Project Operations, hay dos tipos de ofertas, proyectos y ventas. A continuación se indican las diferencias entre estos dos tipos de ofertas:

- **Cuadrículas para elementos de línea** : En una oferta de ventas, solo hay una cuadrícula para los elementos de línea. En una oferta de proyecto, hay dos cuadrículas para elementos de línea. Una cuadrícula es para líneas de proyecto y la otra es para líneas de producto.
- **Activación y revisiones** : Las ofertas de ventas respaldan la activación y las revisiones. Estos procesos no son compatibles con una oferta de proyecto.
- **Pedidos adjuntos** : Puede adjuntar varios pedidos a una oferta de ventas. Solo se puede adjuntar un contrato de proyecto a una oferta de proyecto.
- **Ganar una oferta** : Cuando gana una oferta de venta, la oportunidad relacionada puede permanecer abierta. Tras ganar una oferta de proyecto, la oportunidad relacionada se cierra.
- **Campos y conceptos** : Una oferta de ventas no incluye algunos campos y conceptos que se incluyen en una oferta de proyecto. Entre los campos se incluyen **Unidad de contratación** , **Administrador de cuentas** y **Nombre de contacto de facturación**.  
- **Tipo** : Las ofertas de ventas y de proyecto también se identifican mediante el campo basado en un conjunto de opciones, **Tipo**. Para una oferta de ventas, este campo tiene el valor **Basado en artículo**. Para una oferta de proyecto, tiene el valor **Basado en trabajo**.

Este tema se centra en los detalles de las ofertas de proyecto.

Una oferta del proyecto en Project Operations puede tener varios elementos de línea o varias líneas de oferta. De hecho, una oferta de proyecto tiene dos cuadrículas para elementos de línea. Una cuadrícula es para las líneas basadas en proyecto que permiten las estimaciones detalladas. La otra cuadrícula es para las líneas basadas en productos que utilizan un precio unitario sencillo y un enfoque basado en la cantidad.

- **Basado en proyecto** : El valor ofertado se determina tras estimar la cantidad de trabajo requerida. Puede estimar el trabajo en un nivel alto, directamente como detalles de línea debajo de cada línea de oferta, o según estimaciones realizadas desde cero utilizando un proyecto y un plan de proyecto. Las líneas de oferta basadas en proyectos solo se encuentran en ofertas basadas en proyectos creadas con Project Operations. Este tipo de línea de oferta es un formulario personalizado de las líneas de oferta fuera de catálogo que están disponibles en Microsoft Dynamics 365 Sales.

- **Basado en producto** : el valor ofertado se determina en función de la cantidad de unidades vendidas y del precio de venta unitario. El producto de una basada en producto puede provenir de un catálogo de productos de ventas, o bien puede ser un producto que usted defina. Este tipo de línea de oferta también está disponible en ofertas basadas en proyecto que se crean con Project Operations.

El importe de una oferta es el total de las líneas basadas en producto y las líneas basadas en proyecto.

> [!NOTE]
> Las ofertas y las líneas de oferta no son necesarias en Project Operations. Puede iniciar el proceso de proyecto con un contrato de proyecto (proyecto vendido). Sin embargo, siempre necesitará una oportunidad, independientemente de si comienza con una oferta o con un contrato de proyecto.

## <a name="project-based-quote-lines"></a>Líneas de ofertas basadas en proyectos

En Project Operations, una línea de oferta basada en proyecto dispone de los métodos de facturación siguientes:

- Tiempo y material
- Precio fijo

### <a name="time-and-material"></a>Tiempo y material

El método de facturación Tiempo y material se basa en el consumo. Cuando seleccione este método de facturación, se facturará al cliente a medida que el proyecto vaya incurriendo en costes. Las facturas se crean con una frecuencia periódica basada en la fecha. Durante el proceso de ventas, el valor ofertado de un componente de tiempo y material solo ofrece al cliente una estimación del coste final. El proveedor no se compromete a completar el proyecto según el valor ofertado exacto. Los componentes de tiempo y material aumentan el riesgo del cliente. Por ello, es posible que los clientes deseen negociar cláusulas no superables adicionales para minimizar el riesgo. Project Operations no permite establecer cláusulas no superables.

### <a name="fixed-price"></a>Precio fijo

En el método de facturación de precio fijo, el proveedor se compromete a entregar el proyecto al cliente a un coste fijo. De este modo, se factura al cliente el valor ofertado de la línea de oferta de precio fijo independientemente de los costes en los que incurra el proveedor para proporcionar dicha línea de oferta. El valor de la línea de oferta de precio fijo se factura de una de las maneras siguientes: 

- Como importe de suma total al principio o al final del proyecto, o bien cuando se alcanza un hito de proyecto. 
- Con una frecuencia basada en fechas de plazos iguales del valor fijo de la línea de oferta. Estos plazos se conocen como hitos periódicos.
- En plazos que tienen un valor monetario que se alinea con el progreso del trabajo o con hitos específicos logrados en el proyecto. En este caso, el valor de cada plazo puede variar; sin embargo, todos deben sumar el valor fijo de la línea de oferta.

Project Operations admite los tres tipos de programaciones de facturación para las líneas de oferta de precio fijo.

## <a name="transaction-classification"></a>Clasificación de transacciones

Las organizaciones de servicios profesionales suelen ofertar y facturar a sus clientes según una clasificación de costes. Los costes se representan con las clasificaciones de transacciones siguientes:

- **Tiempo** : esta clasificación representa el coste de la mano de obra o el tiempo que los recursos humanos dedicaron a un proyecto.
- **Gasto** : esta clasificación representa el resto de gastos de un proyecto. Puesto que los gastos se pueden clasificar de manera general, la mayoría de las organizaciones crean subcategorías, como, por ejemplo, viajes, alquiler de vehículos, habitaciones de hotel o material de oficina.
- **Tarifa** : esta clasificación representa gastos generales variados, sanciones u otros elementos que se cobran al cliente. 
- **Impuesto** : esta clasificación representa los importes de los impuestos que los usuarios agregan mientras especifican gastos.
- **Transacción material** : esta clasificación representa datos reales de líneas de producto de una factura de proyecto confirmada.
- **Hito** : esta clasificación se utiliza en la lógica de facturación de precio fijo.

Puede asociar una o varias de estas clasificaciones de transacciones a cada línea de oferta. Tras ganar una oferta, la asignación entre las clasificaciones de transacciones y la línea de oferta se transfiere a la línea de contrato.
  
Por ejemplo, una oferta puede contener las siguientes dos líneas de oferta: 

- Trabajo de consultoría que usa un método de facturación de tiempo y material en el que se aplican clasificaciones de transacciones de cuota y tiempo. Por ejemplo, todas las transacciones de cuota y tiempo del proyecto de ejemplo **Implementación de Dynamics AX** se facturan al cliente en función del tiempo y los materiales utilizados. 
- Gastos de desplazamiento relacionados que utilizan un método de facturación de precio fijo. Por ejemplo, todos los gastos de desplazamientos del proyecto **Implementación de Dynamics AX** se facturan a un valor monetario fijo.

> [!NOTE]
> La combinación de las clasificaciones de transacciones y del proyecto de **Tiempo** , **Gasto** y **Tarifa** asociados a una línea de oferta o a la línea de contrato debe ser única. Si se asocia la misma combinación de clases de transacciones y proyecto a más de una línea de contrato o línea de oferta, Project Operations no funcionará correctamente.

## <a name="billing-types"></a>Tipo de facturación

El campo **Tipo de facturación** define el concepto de imputabilidad. Se trata de un conjunto de opciones que puede tener los valores siguientes:

- **Imputable** : el coste acumulado por este rol o esta categoría es un coste directo que determina la ejecución del proyecto y el cliente debe pagar por este trabajo. El pago se puede administrar como acuerdo de tiempo y materiales o de precio fijo. Sin embargo, al empleado que invierta este tiempo recibirá se le abonará el uso facturable de este tiempo.
- **No imputable** : el coste acumulado por este rol o esta categoría se considera un coste directo que determina la ejecución del proyecto a pesar de que el cliente no reconozca este hecho y no vaya a pagar por este trabajo. Al empleado que invierta este tiempo no se le abonará ningún uso facturable por este tiempo.
- **Gratis** : el coste acumulado por este rol o esta categoría se considera un coste directo que determina la ejecución del proyecto y el cliente así lo reconoce. Al empleado que invierta este tiempo se le abonará el uso facturable por este tiempo. Sin embargo, este coste no se cobrará al cliente.
- **No disponible** : esta opción se utiliza para los costes en los que se incurre en proyectos internos que no requieren seguimiento.

## <a name="invoice-schedule"></a>Programación de facturas

Una programación de facturas es una serie de fechas en las que se emiten facturas de un proyecto. Puede crear opcionalmente una programación de facturas en una línea de oferta. Cada línea de oferta puede tener su propia programación de facturas. Para crear una programación de facturas, debe proporcionar los valores de atributo siguientes:

- Una fecha de inicio de la facturación 
- Una fecha de entrega que representa la fecha de finalización de facturación del proyecto
- Una frecuencia de factura

Estos tres valores de atributos se utilizan para generar un conjunto provisional de fechas que se puede utilizar como base para establecer la facturación.

## <a name="invoice-frequency"></a>Frecuencia de factura

La frecuencia de facturación es una entidad que almacena los valores de atributos que ayudan a expresar la frecuencia con la que se crean las facturas. Los siguientes atributos expresan o definen la entidad Frecuencia de factura:

- **Período** : los períodos pueden ser mensuales, quincenales y semanales. 
- **Ejecuciones por período** : para los períodos semanales y quincenales, puede definir solo una ejecución por período. Para los períodos mensuales, puede definir entre una y cuatro ejecuciones por período. 
- **Días de ejecución** : días en que se debe ejecutar la facturación. Puede configurar este atributo de dos maneras:
  - **Días de la semana** : por ejemplo, puede especificar que la facturación se ejecute todos los lunes o cada segundo lunes. Es posible que los clientes que necesitan establecer la ejecución de la facturación en un día laboral prefieran este tipo de configuración. 
  - **Días naturales** : por ejemplo, puede especificar que la facturación se ejecute los días siete y veintiuno de cada mes. Algunas organizaciones pueden preferir esta tipo de configuración porque ayuda a garantizar que la facturación se ejecute según una programación fija todos los meses.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Programación de facturas para una línea de oferta de precio fijo

Para una línea de oferta de precio fijo, puede utilizar la cuadrícula **Programación de facturas** para crear los hitos de facturación que igualan el valor de línea de oferta.

- Para crear hitos de facturación divididos por igual, seleccione una frecuencia de facturación, escriba la fecha de inicio de facturación en la línea de oferta y seleccione **Fecha de finalización solicitada** para la oferta en la sección **Resumen** del encabezado de la oferta. A continuación seleccione **Generar hitos periódicos** para crear hitos divididos por igual según la frecuencia de factura seleccionada. 
- Para crear un hito de facturación de suma total, cree un hito y después introduzca el valor de línea de oferta como importe de hito.
- Para crear hitos de facturación basados en tareas específicas en el plan de proyecto, cree un hito y asígnelo al elemento de programación del proyecto en la interfaz de usuario del hito de facturación.
