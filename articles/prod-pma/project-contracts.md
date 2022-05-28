---
title: Contratos de proyecto
description: Este tema proporciona ejemplos de los contratos de proyecto que puede crear para varios tipos de proyectos y fuentes de financiación, y cómo puede administrar contratos y facturar a los clientes del proyecto.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cfc5183ce28574d865389eba72cafd3528741cc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683513"
---
# <a name="project-contracts"></a>Contratos de proyecto

[!include [banner](../includes/banner.md)]

Este artículo proporciona ejemplos de los contratos de proyecto que puede crear para varios tipos de proyectos y fuentes de financiación, y cómo puede administrar contratos y facturar a los clientes del proyecto.

El tipo de proyecto que crea para un contrato de proyecto determina el método que se utiliza para facturar a los clientes del proyecto. Puede modificar un contrato de proyecto y el proyecto relacionado, pero no puede cambiar el tipo de proyecto. 

Al usar un contrato de proyecto, puede facturar uno o varios proyectos al mismo tiempo. El contrato del proyecto también ayuda a garantizar un procedimiento de facturación consistente para cada subproyecto en una estructura de proyecto. 

Cada proyecto que se facturará debe estar asociado con un contrato de proyecto. La configuración para un contrato de proyecto se aplica a todos los proyectos y subproyectos asociados con ese contrato de proyecto. 

Un contrato de proyecto puede especificar una o más fuentes de financiación. Por lo tanto, puede dividir la facturación entre varias entidades financieras, establecer límites de financiación para que no se facture a las fuentes de financiación más de un importe específico y configurar reglas de financiación para cobrar gastos.

## <a name="funding-for-project-contracts"></a>Financiación para contratos de proyectos
Algunos contratos de proyectos especifican que varias de sus partes comparten la responsabilidad de financiar los costes del proyecto. Estos son algunos ejemplos:

-   Un cliente grande que tiene varias divisiones solicita que la financiación de un proyecto se divida por división.
-   Su empresa comparte los costos de un gran proyecto con una organización externa.
-   Un proyecto de carretera está cofinanciado por dos municipios.
-   El proyecto de un puente se financia parcialmente con una subvención pública y la intervención de una empresa privada.

En Dynamics 365 Finance, puede dividir la facturación para una sola transacción o un proyecto completo entre varios clientes, subvenciones u organizaciones. 

En proyectos que tengan múltiples responsables de financiación, todas las partes que contribuyan a la financiación de un proyecto de financiación avanzada se denominan fuentes de financiación. Tras definir como fuente de financiación a un cliente, una organización o una subvención, se puede asignar a una o varias reglas de financiación. Las reglas de financiación contienen los criterios que determinan cómo se asignan los cobros a las diversas fuentes de financiación de un proyecto. 

Debido a que los artículos almacenados, como los que aparecen en las solicitudes de compra y las órdenes de compra, no se pueden dividir, el importe del coste no se puede dividir entre varias fuentes de financiación en el momento de la distribución. Por lo tanto, el valor de la fuente de financiación sigue siendo 0 (cero) hasta que se registre la emisión de inventario. Cuando se registra la emisión de inventario, el importe del coste se distribuye de acuerdo con las reglas de distribución de cuentas para el proyecto.

A continuación, se muestran algunos pasos que puede seguir para facilitar la división de la facturación entre varias fuentes de financiación:

-   Especifique que todas las transacciones que se especifican para un proyecto utilizan la misma moneda de venta que el contrato del proyecto.
-   Establezca límites de financiación, de modo que no se facture a una fuente de financiación más de un importe específico para un proyecto.
-   Configure las reglas de financiación y los límites de financiación para cada trabajador, artículo, categoría, grupo de categoría y tipo de transacción (o para todos los tipos de transacciones).
-   Seleccione fechas de inicio y finalización opcionales para definir el período en el que cada regla de financiación es válida.
-   Especifique el porcentaje del que es responsable cada fuente de financiación.
-   Especifique qué fuente de financiamiento es responsable de redondear las diferencias causadas por los cálculos de asignación de fondos.
-   Configure reglas que determinen cómo se facturan los costes del proyecto a los clientes externos y cómo se cobran a las organizaciones internas.
-   Registre las transacciones en una cuenta de fondos retenidos hasta que pueda obtener fondos adicionales, o hasta que decida asumir los costes internamente.

Para determinar qué grupo de impuestos asociar con una transacción, se busca en el proyecto una asignación de grupo de impuestos. Si no se ha realizado ninguna asignación de grupo de impuestos en el nivel de proyecto, se busca el contrato del proyecto.

### <a name="example-multiple-funding-sources-simple"></a>Ejemplo: múltiples fuentes de financiación (simple)

La siguiente tabla proporciona escenarios para administrar la asignación de fondos entre múltiples fuentes de financiación. Estos escenarios se basan en los supuestos siguientes:

-   La configuración de prioridades se tiene en cuenta en la asignación de fondos antes de que se apliquen otros criterios de reglas de financiación.
-   No se ha especificado ningún intervalo de fechas para definir el período d, cuando la regla de financiación es válida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Escenario</strong></td>
<td><strong>Fuente de financiación</strong></td>
<td><strong>Porcentaje de asignación</strong></td>
<td><strong>Prioridad de asignación</strong></td>
</tr>
<tr class="even">
<td>Desea asignar costes a una fuente de financiamiento hasta que se agoten sus fondos, asignar costos a una segunda fuente de financiación hasta que se agoten sus fondos y, finalmente, asignar los costes restantes a una tercera fuente de financiación.</td>
<td><ul>
<li>Fuente de financiación 1</li>
<li>Fuente de financiación 2</li>
<li>Fuente de financiación 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Desea asignar el 75 por ciento de los costes a una fuente de financiación y el 25 por ciento a una segunda fuente de financiación. Cuando se agote cualquiera de esas fuentes de financiación, querrá pagar los costes restantes de una tercera fuente de financiación.</td>
<td><ul>
<li>Fuente de financiación 1</li>
<li>Fuente de financiación 2</li>
<li>Fuente de financiación 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Desea asignar el 75 por ciento de los costes a una fuente de financiación y el 25 por ciento a una segunda fuente de financiación. Cuando se agote cualquiera de esas fuentes de financiación, querrá dividir los costes restantes entre una tercera fuente de financiación y una cuarta.</td>
<td><ul>
<li>Fuente de financiación 1</li>
<li>Fuente de financiación 2</li>
<li>Fuente de financiación 3</li>
<li>Fuente de financiación 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Desea asignar el primer 25 por ciento de los costes a una fuente de financiación y el resto a una segunda fuente de financiación.</td>
<td><ul>
<li>Fuente de financiación 1</li>
<li>Fuente de financiación 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Ejemplo: Múltiples fuentes de financiación (complejo)

Tiene tres fuentes de financiación que quiere utilizar en el siguiente orden:

1.  Usar la fuente de financiación 2 y la fuente de financiación 3 por igual hasta que se agote la fuente de financiación 2.
2.  Seguir usando la fuente de financiación 3 hasta que se agote.
3.  Usar la fuente de financiación 1 cuando se agote la fuente de financiación 3.

Para cumplir este objetivo, en primer lugar debe hacer lo siguiente:

-   Configure límites de financiación para la fuente de financiación 2 y la fuente de financiación 3, para sus respectivos importes.
-   Cree las siguientes reglas de financiación:
    -   Regla 1 (Prioridad 1): asignar el 50 por ciento de las transacciones a la fuente de financiación 2 y el 50 por ciento a la fuente de financiación 3.
    -   Regla 2 (Prioridad 2): asignar el 100 por cien de las transacciones a la fuente de financiación 3.
    -   Regla 3 (Prioridad 3): asignar el 100 por cien de las transacciones a la fuente de financiación 1.

Esta configuración funciona porque las transacciones se comparan con reglas y límites para determinar si alguna de ellas se aplica a la transacción. Si no se aplican reglas o límites específicos a la transacción, se aplica la regla Todas las transacciones. La regla Todas las transacciones coincide con todas las transacciones. 

Si se encuentra una regla que coincide con una transacción, el porcentaje que se ha asignado en esa regla se aplica primero, pero solo después de que las coincidencias se verifiquen con arreglo a los límites que se hayan establecido. Si se ha alcanzado un límite y se agotan los fondos de una fuente de financiación, se ignora la regla de financiación asociada con el límite de financiación y el programa verifica la siguiente regla que se aplica. 

En algunos casos, solo se puede asignar una parte de una transacción según una regla. Esto puede suceder porque se alcanza un límite cuando se asigna la transacción. En este caso, solo se asigna una cierta cantidad de acuerdo con esa regla, como el 50 por ciento, a cada fuente de financiación. Este es el caso de la regla 1, que se describe anteriormente en esta sección. El resto se asigna de acuerdo con la siguiente regla de la secuencia. 

En la siguiente tabla se examina este escenario en mayor detalle.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Foco</strong></td>
<td><strong>Detalles</strong></td>
</tr>
<tr class="even">
<td>Reglas de financiación</td>
<td><ul>
<li>Regla 1 (Prioridad 1): Todas las transacciones. Asignar la fuente de financiación 2 al 50 % y la fuente de financiación 3 al 50 %.</li>
<li>Regla 2 (Prioridad 2): Todas las transacciones. Asignar la fuente de financiación 3 al 100 %.</li>
<li>Regla 3 (Prioridad 2): Todas las transacciones. Asignar la fuente de financiación 1 al 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Límite de financiación</td>
<td><ul>
<li>Límite de la fuente de financiación 1 = 10 000,00</li>
<li>Límite de la fuente de financiación 2 = 500,00</li>
<li>Límite de la fuente de financiación 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transacción 1</td>
<td><strong>Importe de la transacción</strong>: 100 <strong>Financiación</strong>: la transacción se paga de acuerdo con la regla 1 únicamente, porque la transacción se paga en su totalidad después de que se aplica la regla 1. La transacción se financia a partes iguales entre la fuente de financiación 2 y la fuente de financiación 3.
<ul>
<li>Fuente de financiación 2: 50,00</li>
<li>Fuente de financiación 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transacción 2</td>
<td><strong>Importe de la transacción</strong>: 5000 <strong>Financiación</strong>: la transacción se paga de acuerdo con la totalidad de las tres reglas. <strong>Regla 1</strong>
<ul>
<li>Fuente de financiación 2: 450,00</li>
<li>Fuente de financiación 3: 450,00</li>
</ul>
<strong>Regla 2</strong>
<ul>
<li>Fuente de financiación 3: 250,00 (= 750,00 - 50,00 - 450,00)</li>
</ul>
<strong>Regla 3</strong>
<ul>
<li>Fuente de financiación 1: 3850,00 (= 5000,00 - 450,00 - 450,00 - 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Fondos totales que se distribuyen para cada fuente de financiación</td>
<td><ul>
<li>Fuente de financiación 1: 3850</li>
<li>Fuente de financiación 2: 500</li>
<li>Fuente de financiación 3: 750</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Reglas de facturación
Cuando negocia un contrato de proyecto con un cliente, define cómo y cuándo puede facturar al cliente por el trabajo en un proyecto. Después de configurar el contrato de proyecto y el proyecto, puede configurar las reglas de facturación para el proyecto. Las reglas de facturación se basan en los términos del proyecto que se especifican en el contrato del proyecto. Las reglas de facturación que puede crear dependen de los términos del contrato del proyecto y del tipo de proyecto (de tiempo y material o de precio fijo) que asocie con la regla de facturación. Puede crear más de una regla de facturación para un contrato de proyecto. También puede asignar una regla de facturación a varios proyectos que estén asociados al mismo contrato de proyecto y tengan términos de facturación similares. 

Puede configurar los siguientes tipos de reglas de facturación:

-   **Unidad de entrega**: facturar a un cliente cuando complete una unidad de entrega. Las unidades de entrega se definen en el contrato.
-   **Progreso**: facturar a un cliente cuando se complete un porcentaje específico del proyecto. Puede configurar una regla de facturación para calcular automáticamente el porcentaje de trabajo completado, o puede calcular manualmente el porcentaje de trabajo completado y la cantidad que se ha de facturar al cliente.
-   **Hito**: facturar a un cliente por el importe total de un hito del proyecto cuando se alcance el hito.
-   **Tarifa**: facturar a un cliente por sus servicios más una tarifa de administración, que generalmente es un porcentaje del coste de los servicios.
-   **Tiempo y material**: facturar a un cliente por el valor del tiempo y los materiales que se utilizan en un proyecto.

Para todos los tipos de reglas de facturación, puede especificar un porcentaje de retención que se deduce de las facturas de los clientes hasta que un proyecto alcanza una fase acordada. El porcentaje de retención de pago se especifica en el contrato del proyecto. El importe se calcula y se resta del valor total de las líneas en una factura de cliente. 

Para las reglas de facturación **Tiempo y material** y **Progreso**, puede asignar categorías imputables. Las categorías imputables indican las transacciones que deben incluirse en las facturas de los clientes. 

Cuando esté listo para facturar al cliente, el importe a facturar por el proyecto se calcula según las reglas de facturación y se genera una propuesta de factura del proyecto. 

Las siguientes secciones proporcionan ejemplos que muestran cómo configurar y administrar reglas de facturación para un proyecto.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Ejemplo: Crear una regla de facturación basada en la cantidad de unidades entregadas

Su organización formaliza un acuerdo para proporcionar un total de cinco sesiones de formación a los empleados de un cliente a un coste de 10 000 por sesión de formación. Factura al cliente después de cada sesión de formación. 

Cuando configura las reglas de facturación para el contrato, usa los siguientes valores:

-   La unidad de entrega es una sesión de formación.
-   El precio unitario es de 10 000 por sesión de formación.
-   El número total de unidades es de cinco sesiones de formación.

Cuando haya completado una sesión de formación, puede crear una factura por 10 000, por la primera unidad que se entregó, y enviar la factura al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Ejemplo: Crear una regla de facturación basada en un porcentaje específico de finalización del proyecto (cálculo manual)

Su organización, una empresa de consultoría de software, formaliza un acuerdo con un cliente para desarrollar parte de un producto que el cliente está desarrollando. Su organización acepta entregar el código de software a lo largo de un periodo de seis meses. El cliente acepta pagar a su organización un total de 100 000 por el trabajo. Crea una regla de facturación para facturar al cliente en función del porcentaje de trabajo que se completa en el proyecto, como se especifica en el contrato.

-   Al final del primer mes, se reúne con el cliente para determinar el porcentaje de trabajo completado. Después de que usted y el cliente revisen el proyecto, decide que el proyecto está completado en un 15 por ciento.
-   Crea una factura para 15 000 (15 por ciento de 100 000) y se la envía al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Ejemplo: Crear una regla de facturación basada en un porcentaje específico de finalización del proyecto (cálculo automático)

Su organización, una empresa de desarrollo de software, acepta desarrollar un paquete de gestión de nóminas para un cliente por 30 000. El cliente acepta pagar a su organización en función del porcentaje de trabajo terminado. Calcula que los costes del proyecto son 20 000. El contrato del proyecto especifica las categorías de trabajo que utiliza en el proceso de facturación. Configura reglas de facturación que calculan automáticamente los importes de la factura para el porcentaje de trabajo completado para cada categoría. Establece un presupuesto para cada categoría:

-   **Desarrollo**: coste de 15 000 e ingresos de 20 000
-   **Instalación**: coste de 5000 e ingresos de 10 000

Cuando crea una factura de cliente por primera vez, el importe de la factura se calcula automáticamente en función de la siguiente información:

-   Después de un mes, el trabajador del proyecto envía una hoja de horas para el proyecto. El coste de las horas del trabajador es de 5000 para el desarrollo y 1000 para la instalación. El trabajo de desarrollo está completado en un 33 % (coste real de 5000/coste presupuestado de 15 000) y el trabajo de instalación está completado en un 20 % (coste real de 1000/coste presupuestado de 5000).
-   El importe de la factura de 8667 se calcula automáticamente (33 por ciento de 20 000 + 20 por ciento de 10 000).
-   Crea una factura por 8667 y se la envía al cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Ejemplo: Crear una regla de facturación basada en hitos acordados

Su organización, una empresa de consultoría de gestión, acepta realizar una investigación de mercado para un producto de consumo que el cliente planea vender. El cliente acepta utilizar sus servicios por un período de tres meses, a partir de marzo, y acepta pagar a su organización 50 000. El proyecto tiene tres hitos:

-   Hito 1: Recopilar datos del consumidor (31 de marzo)
-   Hito 2: Analizar datos de consumidores (30 de abril)
-   Hito 3: Presentar una propuesta de viabilidad del producto (31 de mayo)

El cliente acepta pagar a su organización 10 000 por el primer hito, 20 000 por el segundo y 20 000 por el tercer hito. 

Cuando configura el contrato del proyecto, acepta facturar al cliente según el hito que se haya completado. La configuración de la regla de facturación incluye los siguientes pasos:

-   Definir la categoría del hito.
-   Defina el importe a facturar al cliente cuando se complete cada hito.

Cuando se completa el primer hito el 31 de marzo, marca el hito como completado y luego crea una factura por 10 000 y se la envía al cliente. No puede crear una factura para un hito hasta que haya marcado el hito como completado.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Ejemplo: Crear una regla de facturación basada en los servicios más una tarifa de gestión

Su organización, una empresa de consultoría de gestión, acepta realizar una investigación de mercado para evaluar la viabilidad de un producto que el cliente, una empresa minorista, está desarrollando. Los términos del acuerdo especifican que proporcionará los servicios de sus tres principales consultores de gestión, quienes realizarán la investigación en función del tiempo y los materiales. El cliente acepta pagar 100 por hora, más una tarifa de gestión del 10 por ciento por las horas de consultoría que se cargan al proyecto. 

Cuando configure el contrato del proyecto, cree una regla de facturación para agregar una tarifa de gestión del 10 por ciento a las horas de consultoría que se cargan al proyecto. 

Cuando crea una factura para el cliente, al cliente se le factura una tarifa de gestión del 10 por ciento más el coste de las horas de consultoría. Por ejemplo, si los tres consultores trabajaron un total de 200 horas en el proyecto, se crea una factura por 22 000 según el siguiente cálculo:

-   200 horas a 100 por hora = 20 000
-   Comisión de gestión del 10 por ciento = 2000
-   Importe total de la factura = 22 000

Si las tarifas están sujetas a impuestos para un cliente y selecciona un grupo de impuestos en el contrato del proyecto, el grupo de impuestos se especifica automáticamente en una regla de facturación para las tarifas.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Ejemplo: Crear una regla de facturación para el valor del tiempo y los materiales

Su organización, una empresa de consultoría de software, acepta proporcionar cinco consultores técnicos para trabajar en un proyecto de desarrollo de software para un cliente durante los próximos seis meses. El cliente se compromete a pagar 150 por cada hora de consultoría, más el coste de los suministros de oficina. Su organización envía una factura al cliente al final de cada mes. 

Cuando configura el contrato del proyecto, acepta facturar al cliente cada mes por el tiempo y los materiales del proyecto. Crea una regla de facturación que incluye la siguiente información:

-   La duración del contrato es de seis meses.
-   El tiempo de consulta se calcula a razón de 150 por hora.
-   Los suministros de oficina se facturan al coste y el coste total del proyecto no debe exceder los 10 000.
-   Crea una factura de cliente al final de cada mes natural durante el proyecto.

Durante el primer mes, los consultores del proyecto registran un total de 800 horas. El coste de los suministros de oficina que se cargan al proyecto es de 2000. Por lo tanto, al final del mes, crea una factura por 122 000, que se calcula como 800 horas a 150 por hora, más 2000 para suministros de oficina.





[!INCLUDE[footer-include](../includes/footer-banner.md)]