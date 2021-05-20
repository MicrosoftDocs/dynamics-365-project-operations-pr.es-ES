---
title: Información general sobre la gestión de proyectos y contabilidad
description: La funcionalidad de gestión de proyectos y contabilidad se puede utilizar en múltiples sectores para proporcionar un servicio, producir un producto o lograr un resultado.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f6ceabe1809cc94357a31f1d57c445593f0f788
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950510"
---
# <a name="project-management-and-accounting-overview"></a>Información general sobre la gestión de proyectos y contabilidad

[!include [banner](../includes/banner.md)]

La funcionalidad de gestión de proyectos y contabilidad se puede utilizar en múltiples sectores para proporcionar un servicio, producir un producto o lograr un resultado.  

Un proyecto es un grupo de actividades que está diseñado para proporcionar un servicio, producir un producto o lograr un resultado. Los proyectos consumen recursos y generan resultados financieros en forma de ingresos o activos.

## <a name="projects-across-industries"></a>Proyectos en todos los sectores
La administración de proyectos y la funcionalidad de contabilidad se pueden usar en múltiples industrias, como se muestra en la siguiente ilustración.

[![Proyectos en todos los sectores](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

En un centro de llamadas, se puede usar un vale para describir el conjunto de acciones necesarias para resolver una llamada. Las empresas de consultoría, como las organizaciones de consultoría técnica o administrativa o las agencias de publicidad, se refieren a sus actividades como proyectos. En marketing, una campaña representa un conjunto de trabajos que debe entregarse. En la fabricación basada en proyectos, un pedido de producción se refiere a diversos trabajos que se deben hacer para producir algunos productos terminados. Cualquiera sea el nombre que se use para ellos, estos proyectos involucran recursos, programaciones y costes, y la gestión de proyectos y la funcionalidad de contabilidad pueden ayudar con la planificación, ejecución y análisis de estos proyectos.

## <a name="project-phases"></a>Fases del proyecto
Aunque el siguiente flujo de proceso está dirigido a proyectos externos o proyectos que se completan para uno o más clientes, la funcionalidad también se aplica a proyectos internos de solo coste. 

![3 fases de un proyecto](./media/3-stages-of-a-project.png) 

Como se muestra en la ilustración anterior, la gestión de proyectos y la contabilidad se pueden dividir en tres fases:

1.  Iniciar
2.  Ejecutar
3.  Analizar

## <a name="initiate-the-project"></a>Iniciar el proyecto
Durante el inicio del proyecto, ocurren varios procesos clave. Puede utilizar una cotización de proyecto para comunicar al cliente la mano de obra, los gastos y los materiales estimados. Puede registrar los términos de facturación, los límites y los acuerdos en un contrato de proyecto. Puede utilizar una estructura de descomposición del trabajo (WBS) para planificar y estimar el trabajo. Puede configurar previsiones y presupuestos para guiar la ejecución del proyecto. La siguiente ilustración muestra la estructura de un proyecto.[![estructura del proyecto](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Crear presupuestos de proyecto

En la fase inicial de ventas de un proyecto, una cotización de proyecto le permite ofrecer a un cliente una oferta sin compromiso. Un presupuesto puede incluir elementos como los artículos y servicios que se presupuestan, información de contacto básica, acuerdos comerciales especiales y descuentos, y posibles impuestos y recargos.

También puede emitir una carta de garantía para una transacción de presupuesto de proyecto entre su organización y el cliente. Una vez creado el presupuesto del proyecto, puede crear la solicitud de carta de garantía para el cliente y enviarla al banco. Una vez que el banco haya aprobado la solicitud, se emite la carta de garantía al cliente. 

Para obtener más información, consulte [Presupuestos de proyectos](project-quotations.md).

### <a name="create-project-contracts"></a>Crear contratos de proyecto

Cuando firma un contrato con un cliente u otra fuente de financiación para completar un proyecto, primero debe crear un contrato de proyecto. Luego, al crear el proyecto, debe asignarlo al contrato correspondiente. El tipo de proyecto que crea para un contrato de proyecto determina el método que se utiliza para facturar a los clientes del proyecto. Puede modificar un contrato de proyecto y el proyecto relacionado, pero no puede cambiar el tipo de proyecto. Para obtener más información acerca de los tipos de proyecto, consulte sección "Crear proyectos".

Para obtener más información sobre los contratos de proyectos, consulte [Contratos de proyecto](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Crear estructuras de descomposición del trabajo

El grado de detalle en una WBS depende del nivel de precisión que se requiera en las estimaciones y el nivel de seguimiento que se requiera frente a esas estimaciones. Los proyectos que tienen una tolerancia muy baja a los retrasos en el programa o el coste generalmente requieren una WBS más detallada y también requieren un seguimiento diligente del progreso del trabajo y el coste con respecto a la WBS. 

Para más información, consulte [Información general sobre las estructuras de descomposición del trabajo](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Crear previsiones y presupuestos de proyectos

Puede utilizar la previsión si su organización tiene una perspectiva operativa y se centra en los ingresos y costes que se derivan de transacciones específicas. Sin embargo, si su organización se centra más en cantidades financieras, puede utilizar los presupuestos. Cada método tiene sus ventajas. Para más información, consulte [Previsiones y presupuestos de proyectos](project-forecasts-budgets.md).

### <a name="create-projects"></a>Crear proyectos

Puede crear seis tipos de proyectos en Finance. Cada tipo de proyecto se configura de manera diferente para el reconocimiento de costes e ingresos. El tipo de proyecto que seleccione depende del propósito del proyecto. La siguiente tabla describe el uso típico de cada tipo de proyecto.
                                                                                                            
<table>
  <tr>
    <td>Tipo de proyecto</th>
    <td>Descripción</th>
  </tr>
  <tr>
    <td>Tiempo y material</td>
    <td>En Proyectos de tiempo y materiales, se factura al cliente por todos los costes en los que se incurre en un proyecto. Estos costes incluyen costes por horas, gastos, artículos y tarifas.</td>
  </tr>
  <tr>
    <td>Precio fijo</td>
    <td>En los proyectos de precio fijo, las facturas consisten en transacciones a cuenta. Un proyecto de precio fijo se factura de acuerdo con una programación de facturación basada en el contrato del proyecto. Los ingresos de un proyecto de precio fijo se pueden calcular y contabilizar en todo el proyecto mediante el método de porcentaje completado. Alternativamente, los ingresos se pueden calcular y contabilizar cuando se completa el proyecto, utilizando el método de contrato completado. Las empresas a menudo pueden beneficiarse del valor del trabajo en proceso (WIP) para calcular el grado de finalización de un proyecto o grupo de proyectos.</td>
  </tr>
  <tr>
    <td>Inversión</td>
    <td>Los proyectos de inversión son proyectos que no producen ganancias inmediatas. Por lo general, se utilizan para proyectos internos a largo plazo en los que los costes deben capitalizarse. Solo se pueden registrar los costes de artículos, horas y gastos para un proyecto de inversión. Los costes de un proyecto de inversión se rastrean y controlan mediante la funcionalidad de estimación. Los proyectos de inversión se pueden configurar con una capitalización máxima opcional. A medida que avanza un proyecto de inversión, registra sus costes en cuentas de trabajo en curso, donde los costes se mantienen hasta que se completa el proyecto. Cuando se elimina el proyecto, transfiere el valor WIP a un activo fijo, una cuenta contable o un nuevo proyecto. <br></br> <strong>NOTA:</strong> las transacciones en proyectos de inversión no se muestran en la página <strong>Gastos de envío<strong>, <strong>Acumular ingresos</strong> o <strong>Crear propuestas de factura</strong>.</td>
  </tr>
  <tr>
    <td>Proyecto de coste</td>
    <td>Al igual que los proyectos de inversión, los proyectos de coste se utilizan normalmente para realizar un seguimiento de los proyectos internos y solo se pueden registrar las horas, los gastos y los artículos. Sin embargo, los proyectos de coste suelen tener una duración más corta que los proyectos de inversión. Además, a diferencia de los proyectos de inversión, los proyectos de coste no se pueden capitalizar en las cuentas de balance de situación. En cambio, las transacciones de proyectos se registran solo en cuentas de pérdidas y ganancias. <br></br> <strong>NOTA:</strong> las transacciones en proyectos de costes no se reflejan en la página <strong>Gastos de envío</strong>, <strong>Acumular ingresos</strong> o <strong>Crear propuestas de factura</strong>. Dado que los proyectos de coste generalmente se usan para rastrear proyectos internos, generalmente no tienen que estar asociados con una cuenta de cliente. Sin embargo, si su configuración requiere que se creen requisitos de artículo para sus pedidos de compra, debe asociar el proyecto de coste con un cliente. Esta asociación es necesaria, porque los requisitos de artículo se gestionan como líneas de un pedido de ventas y el sistema requiere que se especifique un cliente. Sin embargo, esta configuración no hará que los requisitos del artículo se creen automáticamente a partir de un pedido de compra. Para proyectos de costes, el parámetro <strong>Crear requisito de artículo</strong> se ignora. Si necesita un requisito de artículo en un proyecto de coste, puede crearlo manualmente, siempre que haya un cliente asociado al proyecto.</td>
  </tr>
  <tr>
    <td>Interno</td>
    <td>Los proyectos internos se utilizan para realizar un seguimiento de los costes de un proyecto interno de su organización. Los proyectos internos pueden proporcionar una herramienta de planificación para gestionar el consumo de recursos. <br></br><strong>NOTA:<strong> las transacciones en proyectos internos no se reflejan en la página <strong>Acumular ingresos</strong> o <strong>Crear propuestas de factura</strong>.</td>
  </tr>
  <tr>
    <td>Tiempo</td>
    <td>Los proyectos de tiempo se utilizan para realizar un seguimiento del tiempo asociado con actividades que no se pueden cobrar o no son productivas, como un proyecto de seguimiento del tiempo de las bajas laborales. Las transacciones en los proyectos de tiempo no se registran en el libro de contabilidad. Se incluyen en los informes de utilización de los trabajadores. En los proyectos de tiempo solo se pueden registrar transacciones de horas. Utiliza un diario de horas o una hoja de horas para registrar estas horas en el proyecto. Una vez registradas las horas, aparecen como transacciones de proyecto, pero no tienen transacciones de comprobantes correspondientes. <br></br><strong>NOTA:</strong> las transacciones en proyectos de tiempo no se reflejan en la página <strong>Gastos de envío</strong>, <strong>Acumular ingresos</strong> o <strong>Crear propuestas de factura</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Asignar trabajadores, categorías y recursos

Puede programar los recursos de los trabajadores en función de los requisitos y la programación de un proyecto o de las habilidades y la disponibilidad de los trabajadores. Al utilizar las capacidades de programación de recursos, puede desplegar los trabajadores de su organización de manera eficiente y efectiva. Puede encontrar rápidamente a los trabajadores más cualificados que están disponibles para trabajar en su proyecto. También puede ver fácilmente cómo esos trabajadores podrían usarse de manera más efectiva durante el transcurso del proyecto. 

Estas son algunas de las formas en que puede usar la funcionalidad de programación de recursos:

-   Utilice información sobre los atributos de un trabajador, como educación, habilidades, certificaciones y experiencia en proyectos, para que el trabajador se corresponda con los requisitos de un proyecto.
-   Utilice información sobre el calendario y la disponibilidad de un trabajador para hacer coincidir el horario del trabajador con el calendario del proyecto.
-   Revise la capacidad de cada trabajador y determine cómo se está usando esa capacidad. Por ejemplo, si un trabajador está siendo infrautilizado, el trabajador puede asignarse a un proyecto que se ajuste a su disponibilidad y atributos.
-   Revise la disponibilidad de un trabajador para asegurarse de que no haya conflictos de calendario con las asignaciones del trabajador.
-   Revise la información sobre la utilización de los trabajadores en una vista de resumen (por ejemplo, por departamento o por trabajador) o una vista detallada (por ejemplo, por trabajadores en un departamento o por detalle semanal para cada trabajador).
-   Modifique las asignaciones de recursos para varias unidades de tiempo, como día, semana o mes, para optimizar la forma en que se utilizan los trabajadores.

## <a name="execute-the-project"></a>Ejecutar el proyecto
Durante la ejecución del proyecto, los miembros del equipo o los gerentes registran el trabajo y los gastos incurridos mediante el uso de hojas de horas, informes de gastos y otros documentos comerciales. Los jefes de proyectos tienen herramientas que les permiten supervisar el consumo de los importes presupuestados para el proyecto. Los directores de proyecto también pueden solicitar, recoger o adquirir materiales para proyectos mediante pedidos de compra y otros documentos comerciales. Las facturas se preparan y aprueban, de modo que se pueda facturar a los clientes por el trabajo en curso. Finalmente, los ingresos se reconocen durante este proceso para que afecten a las finanzas de la organización.

### <a name="manage-work-breakdown-structures"></a>Gestionar estructuras de descomposición del trabajo

Una WBS es una descripción del trabajo que se completará para un proyecto. Una WBS es una jerarquía de tareas. Representa no solo el trabajo de cada tarea, sino también el tamaño, el coste y la duración de la tarea. 

Para más información, consulte [Información general sobre las estructuras de descomposición del trabajo](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Gestionar previsiones y presupuestos de proyectos

Hay dos formas para gestionar y controlar proyectos: previsiones de proyectos y presupuestos de proyectos. Puede utilizar la previsión si su organización tiene una perspectiva operativa y se centra en los ingresos y costes que se derivan de transacciones específicas. Sin embargo, si su organización se centra más en cantidades financieras, puede utilizar los presupuestos.

Para más información, consulte [Previsiones y presupuestos de proyectos](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Crear pedidos de producción

Una orden de producción relacionada con el proyecto se puede vincular a un pedido de venta o un requisito de artículo mediante el método de artículo terminado o el método de artículo consumido. Además, si la orden de producción se creó manualmente, no hay vínculo entre la orden de producción y el pedido de venta o el requisito de artículo (no hay vínculo a una orden o pedido). Sin embargo, si el pedido de producción se creó automáticamente para cumplir con un pedido de venta o un requisito de artículo, existe un vínculo entre el pedido de producción y el pedido de venta o requisito de artículo (vínculo al pedido). 

Según las combinaciones de estos factores, utilice uno de los siguientes métodos:

- **Artículo terminado/vínculo al pedido**: se vincula el proyecto a un pedido de venta o un requisito de artículo. Cuando usa este método, los costes reales del proyecto se registran cuando se factura el pedido de ventas o cuando se actualiza el albarán para el requisito de artículo. El coste se registra como un artículo terminado.
- **Artículo terminado/sin vincular a orden**: los costes reales no se pueden registrar hasta que el ciclo de producción de un artículo tenga un estado de **Finalizado**. El coste del artículo terminado se registra como una sola transacción.
- **Artículo consumido/vincular a orden**: vincule el proyecto a un requisito de artículo. Al usar este método, puede ver los costes reales del proyecto cuando la producción tiene un estado de **Iniciado** o se notifica como terminado. Los costes se registran como múltiples transacciones de artículos del proyecto para materias primas y horas consumidas para la producción. Cuando se actualiza el albarán para el requisito de artículo, no se registran los costes del proyecto. También puede definir el nivel en la jerarquía de la lista de materiales (L. MAT) en la que se realiza el seguimiento de los proyectos en la producción.
- *<strong><em>Artículo consumido/sin vínculo al pedido</em></strong>*: se vincula el proyecto a un requisito de artículo. Al utilizar este método, puede ver los costes reales del proyecto cuando la producción tiene un estado de <strong>Empezado</strong> o se informa como finalizado. Los costes se registran como múltiples transacciones de artículos del proyecto para materias primas y horas consumidas para la producción. También puede definir el nivel en la jerarquía de la L. MAT. en el que se realiza el seguimiento de los proyectos en la producción.

### <a name="procure-products-and-services"></a>Adquirir productos y servicios

La compra y venta de artículos son actividades frecuentes en muchas empresas centradas en proyectos.

#### <a name="purchase-orders-for-projects"></a>Pedidos de compra para proyectos

El propósito del pedido de compra determina cuándo se utiliza el pedido de compra y, por lo tanto, cuándo se cargan los artículos en un proyecto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Finalidad</th>
<th>Uso de artículos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cree un pedido de compra directamente.</td>
<td>Compre artículos a un proveedor externo para su utilización en un proyecto. Puede crear el pedido de compra de las siguientes formas:
<ul>
<li>Desde el propio proyecto. En este caso, el proyecto ya está definido para el pedido de compra.</li>
<li>Dirigiéndose hasta el pedido de compra del proyecto. Debe seleccionar tanto el proveedor como el proyecto para el que se va a crear el pedido de compra.</li>
</ul></td>
<td>Los artículos se consumen cuando se actualiza la factura del proveedor.</td>
</tr>
<tr class="even">
<td>Cree un pedido de compra desde un pedido de ventas.</td>
<td>Compre artículos cuando cree un pedido de venta a partir de un proyecto.</td>
<td>Los artículos se consumen cuando el pedido de venta se factura al cliente.</td>
</tr>
<tr class="odd">
<td>Cree un pedido de compra a partir de un requisito de artículo.</td>
<td>Compre artículos cuando cree un requisito de artículo a partir de un proyecto.</td>
<td>Los artículos se consumen cuando se actualiza el albarán de requisitos del artículo.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Pedidos de venta para proyectos

En Gestión de proyectos y contabilidad, puede registrar el consumo de artículos de varias formas. Puede vender artículos o comprar artículos de un proyecto o reservar artículos para un proyecto. 

Puede solicitar artículos del inventario de la empresa para su consumo en un proyecto. Alternativamente, puede comprar artículos de un proveedor externo. Los artículos se pueden consumir en todo tipo de proyectos, excepto en los proyectos de tiempo. 

La forma en que pide los artículos depende de dónde los solicite:

-   Para pedir artículos del inventario de la empresa, debe ingresar el pedido como requisito de artículo. Si usa la página **Requisitos del artículo**, puede configurar el requisito para recibir artículos como entregas parciales. Por lo tanto, puede posponer el consumo de una cantidad de artículos hasta que los artículos sean necesarios.
-   Para pedir artículos de un proveedor externo, debe crear el pedido como un pedido de compra en la página **Pedido de compra**.

> [!NOTE] 
> El albarán de un pedido de cliente relacionado con un proyecto no se puede cancelar si los artículos ya se han marcado para su embalaje. 

En la siguiente tabla se indican los métodos para pedir artículos y se describe cómo se consumen los artículos.

| Método            | Finalidad                                                                                                                                                        | Uso de transacciones de artículos                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Pedido de venta       | Especifique una transacción directamente en un proyecto de tiempo y material.                                                                                                   | Las transacciones de artículos se utilizan cuando se registra la factura del cliente.                                                                               |
| Diario de inventario | Introduzca y mantenga rápidamente registros de artículos. Si, por ejemplo, desea introducir un requisito de artículo basado en una lista impresa, se puede aplicar el diario de inventario. | Las transacciones de artículos se consumen cuando se registra el diario.                                                                                        |
| Requisito de artículo  | Introduzca los artículos que no se consumirán de inmediato. Este método le permite realizar un seguimiento del número de artículos que se han consumido en un registro de requisitos de un solo artículo.    | Las transacciones de artículos se consumen cuando se actualiza el albarán. En otras palabras, el requisito de artículo se crea cuando se registra el albarán. |
| Pedidos de compra   | Especifique transacciones en una de las tres ubicaciones, según el método de compra.                                                                              | Las transacciones de artículos se usan cuando se actualiza el albarán o cuando se factura al cliente o proveedor.                                      |

### <a name="process-project-invoices"></a>Procesar facturas de proyectos

El tipo de proyecto determina qué procedimiento de facturación se debe aplicar. Solo se pueden facturar los dos tipos de proyectos externos (tiempo y materiale y precio fijo). Los proyectos de tiempo y material y los proyectos de precio fijo siempre se adjuntan a un contrato de proyecto. 

Antes de crear una factura de cliente para un proyecto, puede crear una factura preliminar o una propuesta de factura. En una propuesta de factura, puede seleccionar transacciones de proyecto para incluirlas en una factura de proyecto. Luego, puede revisar los detalles de la factura antes de registrar la factura del proyecto y enviarla al cliente u otra fuente de financiación. 


Para obtener más información sobre cómo procesar facturas de proyecto, consulte [Facturación de proyectos](/dynamics365/finance/accounts-payable/project-invoicing).


### <a name="calculate-the-cost-to-complete-a-project"></a>Calcular el coste para completar un proyecto

Cuando crea un presupuesto, puede elegir el método que se utiliza para calcular el coste para completar el proyecto. Seleccione un método en el campo **Coste para completar el método** en la página **Crear presupuesto**. El método que elija se aplica por separado a cada línea de coste en la estimación de costes. Mientras que una línea tenga estado de **Creado**, puede cambiar el método que se le aplica en la página **Coste estimado**. 

La siguiente tabla describe los métodos para calcular el coste de completar un proyecto.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Coste total: real</td>
<td>Los costes estimados deben especificarse manualmente. Después de que la columna <strong>Coste total</strong> o <strong>Cantidad total</strong> en la página <strong>Coste estimado</strong> se completa, los costes reales se restan de los totales especificados por el usuario. El resultado es el coste de completar el proyecto. Por lo general, el progreso de los costes no se rastrea según, por ejemplo, el número de estancias de hotel y comidas que se registran en cada período. En su lugar, el seguimiento generalmente se basa en una comparación con la cantidad total de horas estimadas. Este enfoque no requiere un modelo de previsión y el coste total o la cantidad total se pueden cambiar manualmente. Cuando se especifica un valor en la columna <strong>Coste total</strong> o <strong>Cantidad total</strong>, Finance compara este valor con las transacciones reales que se registran en el período y luego disminuye el valor en la columna <strong>Cantidad a completar</strong> o <strong>Coste a completar</strong>.</td>
</tr>
<tr class="even">
<td>Presupuesto total: real</td>
<td>Los costes reales se comparan con el modelo de previsión que selecciona para determinar el coste. Este método utiliza un modelo de presupuesto total que incluye las transacciones previstas. Para obtener una vista más precisa del proyecto, puede ajustar el modelo presupuestario cuando el proyecto está en curso. Si debe ajustar la previsión, siga este proceso general:
<ol>
<li>Copie las transacciones de previsión en otro modelo de previsión.</li>
<li>Compare las transacciones previstas con las transacciones reales.</li>
<li>Mantenga, disminuya o aumente las estimaciones para el próximo período.</li>
</ol>
Finance no reduce automáticamente las estimaciones previstas. Por lo tanto, es una buena idea mantener un modelo de previsión original en el proyecto de precio fijo, para establecer una línea de base para comparar cuando se complete el proyecto. 
<br></br> <strong>NOTA:</strong> Cuando seleccione este método, utilice al menos dos modelos de previsión. Un modelo debe contener la previsión original. Para el otro modelo, debe copiar las transacciones de previsión de otro modelo. Este método es válido solo para proyectos de inversión y de precios fijos.</td>
</tr>
<tr class="odd">
<td>Presupuesto restante</td>
<td>Este método utiliza un modelo de presupuesto restante para calcular el coste de completar el proyecto. Cuando utiliza este método, los costes reales y los importes previstos en el modelo de presupuesto restante se suman. El resultado es un coste total. Antes de utilizar este método, se debe configurar un modelo de presupuesto restante para deducir transacciones según las transacciones reales que se registran en el sistema. En la página <strong>Modelos de pronóstico</strong>, asegúrese de que los campos estén marcados en el grupo <strong>Reducción automática de la previsión</strong>. Normalmente, un presupuesto restante se copia de un presupuesto original. A medida que se especifican transacciones, se reducen las transacciones del presupuesto restante. A medida que avanza el proyecto, si determina que el presupuesto restante debe ajustarse, cargue las transacciones de previsión al presupuesto restante. <br></br> <strong>NOTA:</strong> Este método solo se puede aplicar si se adjunta un modelo de previsión a la estimación.</td>
</tr>
<tr class="even">
<td>Como la estimación anterior</td>
<td>Se aplica el mismo método de estimación que se utilizó en el período anterior. Este método requiere un modelo de previsión si el período anterior requirió un modelo de previsión.</td>
</tr>
<tr class="odd">
<td>Establecer en cero el costo para completar</td>
<td>Normalmente, este método se utiliza antes de eliminar el proyecto de estimación. Este método hace corresponder las estimaciones totales con las transacciones reales que se registraron y borra los valores de la columna <strong>Coste para completar</strong>. El porcentaje de finalización resultante es siempre del 100 por ciento. El campo <strong>Previsión</strong> no está seleccionado para cada línea de coste que crea y la estimación total se copia de la estimación de coste anterior. El consumo real para el período estimado se deduce del coste para completar el proyecto. Este método no requiere un modelo de previsión.</td>
</tr>
<tr class="even">
<td>De la plantilla de costes</td>
<td>Se aplica el método de coste para completar que está configurado en la plantilla de coste que está asociada con el proyecto de estimación seleccionado.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analizar el proyecto
En su nivel más básico, un proyecto se utiliza para agrupar transacciones que registran costes y luego contabilizar estos costes en la contabilidad general. 

Por lo general, estas transacciones son el resultado de documentos empresariales, como partes de horas, informes de gastos, facturas de proveedores o transacciones de inventario. El ciclo de vida de un proyecto suele empezar con estimaciones, previsiones y presupuestos que ayudan a planificar y anticipar el trabajo y el impacto financiero del proyecto. A medida que analiza un proyecto, puede evaluar no solo las transacciones que se produjeron durante el proyecto, sino también la precisión de sus estimaciones y previsiones, los índices de utilización de los miembros del equipo del proyecto y el éxito general del proyecto.

### <a name="analyze-cash-flow"></a>Analizar el flujo de efectivo

Utilice la supervisión del flujo de efectivo para revisar tanto los flujos de efectivo previstos como los flujos de efectivo reales para un proyecto. Puede revisar los flujos de efectivo mientras un proyecto está en curso, o ver los flujos de efectivo de un proyecto completado. 

Al supervisar los flujos de efectivo, puede evaluar un solo proyecto, usar los informes para ver varios proyectos y transferir los flujos de efectivo del proyecto a los pronósticos de flujo de efectivo a la contabilidad general.

#### <a name="cash-inflow-forecasting"></a>Previsiones de entrada de efectivo

Según su configuración, puede pronosticar las entradas de efectivo para un proyecto seleccionado. Por ejemplo, si la fecha del proyecto es el 5 de marzo de 2012 y factura el 31 de marzo de 2012, así es como puede prever la fecha de vencimiento y la fecha de pago de las ventas esperada:

-   **Fecha del proyecto**: 5 de marzo de 2012.
-   **Fecha de la factura**: 31 de marzo de 2012. Esta fecha se determina en función de la frecuencia de facturación. Para este ejemplo, establece la frecuencia de facturación para el mes actual. Por lo tanto, todas las transacciones que se contabilizan en el mes de marzo se facturan el último día del mes.
-   **Fecha de vencimiento**: 14 de abril de 2012. Esta fecha se determina en función de las condiciones de pago que se establecieron para el proyecto. Para este ejemplo, seleccionó condiciones de pago de 14 días. Por lo tanto, se agregan 14 días a la fecha de la factura para llegar a una fecha de vencimiento del 14 de abril de 2012.
-   **Fecha prevista de pago de las ventas**: 27 de abril de 2012. Esta fecha se calcula sumando el número de días en el campo **Días de reserva general** en la página **Parámetros de gestión de proyectos y contabilidad** al número de días en el campo **Días de reserva individual** en la página **Contratos del proyecto** y, luego, sumando el total al número de días en el campo **Fecha de vencimiento**. Para este ejemplo, especificó **3** en el campo **Días de reserva general** y **10** en el campo **Días de reserva individual**. Por lo tanto, se agregan 13 días a la fecha de vencimiento de la factura para llegar a una fecha de pago de las ventas esperada del 27 de abril de 2012.

Los días de reserva general pueden reemplazar los días de reserva individual o agregarse a los días de reserva individual:

-   Para utilizar los días de reserva generales para sustituir los días de reserva individual, especifique el número promedio de días entre la fecha de vencimiento y la fecha de pago real para los clientes.
-   Para agregar los días de reserva general a los días de reserva individual en el campo **Días de reserva general**, especifique su estimación para el número de días entre el día en que el cliente envía el pago y el día en que su organización recibe el pago.

Configure días de reserva individual en el contrato del proyecto. Los días se calculan según la fecha de vencimiento de la factura de venta y la experiencia de su organización con el patrón de pago de un cliente.

#### <a name="actual-cash-inflow"></a>Entrada de efectivo real

La entrada de efectivo real se asemeja a la previsión, pero puede comenzar sus cálculos desde la fecha de la primera factura. A continuación, tiene un ejemplo:

-   **Fecha de la factura**: 2 de marzo de 2012.
-   **Fecha de vencimiento**: 16 de marzo de 2012. Las condiciones de pago se establecen en 14 días.
-   **Fecha prevista de pago de las ventas**: 29 de marzo de 2012. El cálculo incluye tres días de reserva general y 10 días de reserva individual.

#### <a name="cost-forecasting"></a>Previsión de costes

Según los días definidos, la fecha de pago del coste puede diferir de la fecha del proyecto. En este caso, la fecha de pago del coste se calcula sumando el número de días desde la fecha del proyecto al número de días en las condiciones de pago. 

Por ejemplo, la fecha del proyecto de la transacción es el 5 de marzo de 2012 y se establecen las siguientes condiciones de pago:

-   **Horas:** mes actual (**M**)
-   **Gastos**: 14 días (**D14**)
-   **Artículos**: 30 días (**D30**)

Según esta configuración, aquí está la fecha de pago del coste para cada tipo de transacción:

-   **Horas**: 31 de marzo de 2012, que es el último día del mes seleccionado.
-   **Gastos**: 19 de marzo de 2012, que es 14 días después de la fecha de la transacción.
-   **Artículos**: 4 de abril de 2012, que es 30 días después de la fecha de la transacción.

> [!NOTE] 
> La fecha de vencimiento del pedido de compra se basa en la transacción del proveedor cuando se crea el pedido de compra del proyecto. La fecha de vencimiento no está determinada por ninguna configuración predeterminada. 

La fecha de pago del coste no se calcula en días de reserva. Después de que se completa un proyecto, cuando se completan todos los costes y la facturación, tanto el coste como las ventas se registran en las cuentas de pérdidas y ganancias. 

Cuando se completen todas las facturas de ventas y proveedores, puede ver la relación entre los campos en la página **Flujo de efectivo** y los campos en la página **Declaraciones del proyecto**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Página de flujo de efectivo
        - Entradas de efectivo 
        - Salidas de efectivo
        - Flujos de efectivo netos
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Página de declaraciones del proyecto
        - Ingresos
        - Coste total
        - Margen bruto
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Revisar costos

Puede supervisar los costos en los que incurre su organización durante un proyecto en la página **Control de costes**. Al comparar los costes presupuestados originales para el proyecto con los costes reales actuales y los gastos confirmados, puede determinar si el proyecto va según lo programado, o por encima o debajo del presupuesto. 

> [!NOTE] 
> Cuando usa la página **Control de costes** para ver el estado actual de los costes del proyecto, utilice los modelos de pronóstico que se seleccionaron para el presupuesto original y restante. Si selecciona otros modelos de previsión al calcular los costes, los resultados del cálculo no serán precisos.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Ver los importes presupuestados restantes

Si **Presupuesto restante** se selecciona como el método de control de costes en la página **Parámetros de gestión de proyectos y contabilidad**, la página **Control de costes** calcula los costes que no se han publicado como reales o no se han marcado como confirmados. Específicamente, los importes de la pestaña **General** en el panel inferior de la página **Control de costes** se calculan de las siguientes formas:

-   **Coste real**: el importe total que se ha gastado en el proyecto para la línea de coste seleccionada. El importe del coste real se calcula en la página **Actualizaciones de contabilidad**.
-   **Gasto comprometido**: el importe adicional de gastos que la entidad jurídica se ha comprometido a pagar. Los importes de gastos comprometidos específicos se calculan en la página **Gastos comprometidos**.
-   **Presupuesto restante**: la cantidad del importe presupuestado original que todavía está disponible para la línea de coste seleccionada. El importe del presupuesto restante se calcula en la página **Vista previa de contabilidad general**.
-   **Coste total**: la suma del coste real, el coste confirmado y los importes presupuestarios restantes.

En la página **Control de costes**, en la pestaña **Desviación**, puede ver una comparación del coste total esperado con el presupuesto original. Esta comparación muestra las diferencias entre estos importes. Por tanto, puede ver dónde no coinciden los datos. Los importes de las desviaciones se calculan de las siguientes formas:

-   **Presupuesto original**: el importe que se presupuestó originalmente para la línea de coste seleccionada. El importe del presupuesto original se calcula en la página **Vista previa de contabilidad general**.
-   **Coste total**: la suma del coste real, el gasto comprometido y el presupuesto restante, según se notifica en la pestaña **General**.
-   **Desviación**: La diferencia entre el coste total y el presupuesto original.
-   **Desviación según cantidad**: la diferencia total entre la previsión original y la previsión total. Esta diferencia se puede expresar matemáticamente como (Cantidad prevista total) × (Precio medio original - Precio medio total). Este cálculo solo se aplica a las horas del proyecto.
-   **Desviación según precio**: la diferencia total entre la previsión original y la previsión total. Esta diferencia se puede expresar matemáticamente como (Precio previsto original) × (Cantidad prevista original: cantidad prevista total). Este cálculo se aplica solo a las horas del proyecto.

#### <a name="viewing-the-total-budgeted-amounts"></a>Ver los importes presupuestados totales

Si **Presupuesto total** se selecciona como el método de control de costes en la página **Parámetros de gestión de proyectos y contabilidad**, la página **Control de costes** calcula los costes reales y los costes totales del proyecto para ayudarlo a detectar cualquier diferencia entre los dos. En concreto, en la página **Control de costes**, los importes de las columnas del panel inferior de la pestaña **General** se calculan de las siguientes formas:

-   **Coste presupuestado total**: el importe presupuestado total para la línea de coste seleccionada.
-   **Coste real**: el importe total de los costes en los que se ha incurrido en el proyecto hasta la fecha para las líneas de costes seleccionadas.
-   **Gasto comprometido**: el importe total que se ha comprometido para la línea de coste seleccionada.
-   **Desviación**: la diferencia entre la suma de los costes reales y los gastos comprometidos, y el coste total. La desviación muestra si se deben especificar costes adicionales para el presupuesto total.

En la página **Control de costes**, en la pestaña **Desviación**, puede ver la diferencia entre el presupuesto total y el presupuesto original en los siguientes campos:

-   **Presupuesto original**: el importe que se presupuestó originalmente para la línea de coste. El presupuesto original se calcula en la página **Vista previa de contabilidad general**.
-   **Coste presupuestado total**: el coste total que se presupuestó originalmente para la línea de coste. El coste presupuestado total se calcula en la página **Vista previa de contabilidad general**.
-   **Desviación**: la desviación de la línea de coste. Este importe se calcula restando el coste total del presupuesto original.
-   **Desviación según cantidad**: la diferencia total entre el presupuesto original y el presupuesto total. Este importe se calcula restando el total de horas presupuestadas de las horas presupuestadas originales y luego multiplicando la diferencia por el precio de coste presupuestado original. Esta diferencia se puede expresar matemáticamente como (Precio de coste presupuestado original) × (Horas presupuestadas originales - Horas presupuestadas totales). Este cálculo solo se aplica a las horas del proyecto.
-   **Desviación según precio**: este importe se calcula restando el total de horas presupuestadas de las horas presupuestadas originales y luego multiplicando la diferencia por el número total de horas consumidas. Esta diferencia se puede expresar matemáticamente como (Horas consumidas totales) × (Horas presupuestadas originales: horas presupuestadas totales). Este cálculo se aplica solo a las horas del proyecto.

### <a name="analyze-utilization"></a>Analizar la utilización

El índice de utilización es el porcentaje de tiempo que un trabajador realiza un trabajo facturable o productivo en un período de trabajo específico. Las horas facturables son las horas del trabajador que se pueden cobrar a un cliente específico. 

El índice de utilización de un trabajador se calcula dividiendo la cantidad de horas facturables por la cantidad de horas de trabajo en un período específico. Por ejemplo, si un trabajador tiene 30 horas facturables en un período, y el número de horas laborables en el mismo período es 40, la tasa de uso del trabajador es del 75 por ciento. 

Al calcular la tasa de uso de un trabajador, puede calcular la tasa facturable o la tasa de eficiencia:

-   **Tarifa facturable**: la diferencia entre las horas facturables y las horas no facturables u horas normales.
-   **Tarifa de eficacia**: la diferencia entre las horas productivas y las horas no productivas u horas normales. Las horas productivas son las horas que el trabajador dedica a contribuir a un proyecto específico. Las horas productivas generalmente se facturan a los clientes, excepto en el caso de proyectos internos. Las horas no productivas nunca se facturan a un cliente.

El índice de utilización se calcula en la página **Utilización de horas**. Los cálculos se basan en las preferencias predeterminadas. Estas preferencias también especifican cómo se calculan las horas asignando **Utilización** o **Carga** a cada tipo de proyecto. Esto se aplica a los cálculos de tasas facturables y a los cálculos de tarifas de eficacia.

-   **Utilización**: las horas que se notifican para el tipo de proyecto seleccionado siempre se consideran para la utilización facturable o de eficacia.
-   **Carga**: las horas que se notifican para el tipo de proyecto seleccionado siempre se consideran para la utilización no facturable o que no es de eficacia.
-   **Según propiedad de línea**: las propiedades de línea de una transacción de hora concreta determinan si las horas se consideran para uso facturable o de eficacia.
-   **No incluido**: las horas no se tienen en cuenta en el cálculo de la utilización facturable o de eficiencia.

En la página **Utilización de horas**, además del porcentaje de índice de utilización general para un trabajador o un proyecto, puede ver la cantidad de horas que se utilizaron para los cálculos del índice de utilización para cada uno de los siguientes tipos de horas:

-   **Horas no incluidas**: estas horas no están incluidas en la tasa de utilización de horas.
-   **Horas incluidas**: estas horas se calculan sumando las horas de utilización y las horas de carga. Estas horas están incluidas en la tasa de utilización.
-   **Horas de carga**: si está calculando una tarifa facturable, estas horas son las mismas que las no imputables. Si está calculando una tasa de eficacia, estas horas son las mismas que las horas no productivas.
-   **Horas de utilización**: si está calculando una tarifa facturable, estas horas son las mismas que las imputables. Si está calculando una tasa de eficacia, estas horas son las mismas que las horas productivas.

Al calcular la tasa de utilización de un trabajador, puede usar las horas normales o las horas incluidas. Si usa las horas incluidas, debe asegurarse de que los trabajadores registren todo su tiempo de trabajo para los períodos de la hoja de horas, porque el cálculo se expresa como un porcentaje de las horas introducidas. Cuando calcula el índice de utilización de horas para un proyecto, contrato de proyecto, registro de cliente o categoría, debe usar las horas incluidas para su cálculo.

### <a name="review-project-statements"></a>Revisar instrucciones del proyecto

Puede crear una instrucción de proyecto para ver una instantánea rápida del progreso de un proyecto. Cuando ejecuta una instrucción de proyecto, puede especificar los criterios que se utilizan para calcular la instrucción haciendo selecciones en la pestaña **General** en la página **Instrucciones de proyecto**. Puede seleccionar incluir o excluir la siguiente información:

-   Tipos de proyecto
-   Tipos de transacciones
-   Fecha del proyecto/fecha contable
-   Datos

Una vez calculado el informe, puede ver la siguiente información en las distintas pestañas de la página **Informes de proyecto**:

-   **General**: información general sobre la estructura básica de pérdidas y ganancias del proyecto.
-   **Ganancias y perdidas**: información sobre ingresos acumulados.
-   **WIP**: información sobre saldos de cuentas WIP.
-   **Consumo**: información sobre el consumo de horas, artículos, gastos y transacciones de nómina.
-   **Factura**: información sobre facturas y facturación a cuenta.
-   **Tasa horaria**: las tasas horarias que se registran en las cuentas de ingresos y costes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]