---
title: Crear y confirmar diarios de movimientos
description: Este tema proporciona información sobre cómo crear y confirmar diarios de movimientos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584249"
---
# <a name="create-and-confirm-entry-journals"></a>Crear y confirmar diarios de movimientos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Utilice diarios de entrada para registrar datos reales directamente en Microsoft Dynamics 365 Project Operations. Cuando usa diarios de entrada, no tiene que introducir registros de uso de tiempo, gastos y materiales en Project Operations.

Un diario de un solo movimiento permite crear varias líneas de diario. Cuando se confirma el diario, una línea de Diario de movimiento registra el dato real para los siguientes detalles:

- El coste o los ingresos, según el tipo de transacción que se seleccionó.
- La clase de transacción seleccionada. Las clases disponibles son **Tiempo**, **Gastos**, **Material**, **Anticipo**, **Hito** e **Impuesto**.
- El proyecto y/o una tarea que se selecciona en la línea del diario.

Siga estos pasos para crear un diario de entradas en Project Operations.

1. Vaya a **Ventas** \> **ransacciones** \> **Diarios**.
2. En la página de lista **Diarios de movimientos**, en el Panel de acciones, seleccione **Nuevo** para crear un diario.
3. En la página **Nuevo diario**, en el campo **Descripción**, introduzca una descripción del diario.
4. Asegúrese de que el campo **Tipo de diario** se establece en **Movimiento** y luego seleccione **Guardar**. Después de guardar el nuevo Diario de movimientos, debe aparecer una pestaña **Líneas de diario** en la página del diario.
5. En la pestaña **Líneas de diario**, en la barra de herramientas de encima de la cuadrícula, seleccione **Nuevo** para crear una línea de diario de movimientos.
6. En el cuadro de diálogo **Creación rápida** para crear una línea de diario de movimientos, configure los campos como se describe en la siguiente tabla.

    | Campo | Description | Impacto funcional |
    | --- | --- | --- |
    | Clase de transacción | La línea de diario se puede clasificar en una de las seis clases de transacciones: **Tiempo**, **Gastos**, **Material**, **Anticipo**, **Hito** o **Impuesto**. | La clase de transacción **Impuesto** ha quedado en desudo en Project Operations. <br> Si crea una clase de transacción **Impuesto**, no se procesará mediante facturación o en cálculos de costes o ingresos. **Hito** es una clase de transacción solo para ingresos. <br>La clase de transacción **Anticipo** representa un anticipo que se recibió de un cliente. Siempre debe crearse como un par de líneas de diario de ventas facturadas y ventas no facturadas. |
    | Tipo de transacción | Los tipos de transacción **Coste**, **Ventas entre empresas** y **Coste unitario de recursos** deben usarse para registrar el coste.<br> Los tipos de transacciones **Ventas no facturadas** y **Ventas facturadas** deben utilizarse para registrar ingresos. | La clase de transacción **Anticipo** solo funciona con los tipos de transacciones **Ventas no facturadas** y **Ventas facturadas**.<br> La clase de transacción **Hito** solo funciona con el tipo de transacción **Ventas facturadas**. <br>Los tipos de transacciones **Ventas entre empresas** y **Coste unitario de recursos** son aplicables sólo a las clases de transacción **Tiempo** y estos solo están disponibles en los diarios de entrada en el escenario de implementación resumida y no cuando se implementa Project Operations en los escenarios de recursos/no en existencias. |
    | Seleccionar producto | Cuando se selecciona la clase de transacción **Material**, este campo le permite especificar si la transacción de material para la que está creando la línea de diario es un producto existente o un producto fuera de catálogo. | Si selecciona **Producto fuera de catálogo**, puede introducir un nombre para el producto. |
    | Producto | Una referencia al producto del catálogo. | |
    | Description | Una descripción de la línea del diario para facilitar su identificación. | Para las líneas del diario de ventas no facturadas, el valor se utilizará como descripción cuando se creen los detalles de la línea de la factura. |
    | Descripción externa | Una descripción de la línea del diario que se puede usar para compartir con partes interesadas externas. | Para las líneas del diario de ventas no facturadas, el valor se utilizará como descripción externa cuando se creen los detalles de la línea de la factura. También puede aparecer en la factura que se envía al cliente. |
    | Tipo de facturación | Un valor que indica si la línea del diario se contará como un componente cobrable, complementario o no cobrable en el proyecto. | En un flujo típico, el tipo de facturación se deriva de los términos acordados que se establecen en el contrato. Sin embargo, cuando registra una línea de diario, puede introducir un valor en este campo. |
    | Fecha del documento | Utilice una fecha en la que se produjo la transacción. | |
    | Fecha de inicio | Utilice la fecha en la que se produjo la transacción. | Este campo se utiliza para la comparación con la fecha de creación de la factura para las transacciones del tipo **Ventas no facturadas**. Esta comparación le ayudará a decidir si la transacción es de fecha futura o pasada. Solo las transacciones con fecha pasada se agregarán a la factura. |
    | Fecha de finalización | Utilice la fecha en la que se produjo la transacción. | |
    | Fecha contable | Utilice la fecha en la que se registrará el impacto contable. | |
    | Cliente de línea de contrato | De forma predeterminada, si la línea de contrato tiene solo un cliente, este campo se establece en el cliente en la línea de contrato cuando se guarda la línea de diario. Si la línea de contrato tiene varios clientes, seleccione el cliente correcto en la línea de contrato. | Si el sistema no puede determinar el cliente de la línea de contrato en la línea del diario, y si está en blanco en el dato real del tipo **Ventas no facturadas** que se crea a partir de la línea del diario, no se facturará el dato real. |
    | Project | Seleccione el proyecto donde registrar el dato real. | Según el proyecto, la clase de transacción y la tarea seleccionados, el sistema intentará determinar el contrato, la línea de contrato y el cliente de la línea de contrato. |
    | Task | Seleccione la tarea donde registrar el dato real. | Si asoció tareas con líneas de contrato durante la configuración del contrato, el sistema utilizará la tarea seleccionada, junto con un proyecto y una clase de transacción, para determinar el contrato, la línea de contrato y el cliente de la línea de contrato. |
    | Categoría de transacción | Seleccione la categoría de transacción donde registrar el dato real. | Para los gastos, la categoría de transacción seleccionada determina el precio predeterminado que se introducirá en la línea del diario cuando se guarde. |
    | Role | Este campo es relevante para las líneas del diario de Tiempo. Seleccione el rol del recurso que dedicó tiempo al proyecto y/o la tarea. | Para las líneas de diario de Tiempo, si usa la configuración original para la entrada de costes de recursos predeterminados y tasas de facturación, el rol seleccionado se usa junto con la unidad de recursos para determinar el precio predeterminado que se introducirá en la línea de diario cuando se guarde. Si usa una configuración personalizada para la entrada de precios predeterminados, debe revisar esa configuración para determinar si el campo **Rol** se utiliza para introducir valores de precio predeterminados. |
    | Subcontrato | Si la línea del diario representa capacidad subcontratada o gastos o materiales subcontratados, seleccione el subcontrato correspondiente. | Cuando se registran las líneas del diario Costes, el subcontrato seleccionado determinará la lista de precios que se utiliza para introducir el coste unitario predeterminado. |
    | Línea de subcontrato | Si la línea del diario representa capacidad subcontratada, o gastos o materiales subcontratados, seleccione la línea del subcontrato correspondiente. | Cuando se registran las líneas del diario Costes, la línea de subcontrato seleccionada garantizará que los cálculos de capacidad disponibles en la línea de subcontrato se calculen correctamente. |
    | Método de importe | De forma predeterminada, este campo se establece en **Multiplicar la cantidad por el precio**. Cuando se utiliza este método, la cantidad se calculará como *Cantidad* × *Precio*. El otro método soportado es **Precio fijo**. Cuando se usa este método, el precio se establecerá en el importe y la cantidad no se usará en el cálculo. | |
    | Programación de unidades y Unidad | Juntos, la programación unitaria y la unidad identifican la unidad de la cantidad. | La combinación de la unidad y la categoría de transacción se utiliza para introducir precios predeterminados para gastos. En la configuración predeterminada de Project Operations, la combinación de la unidad, el rol y la unidad de recursos se usa para introducir precios predeterminados para el tiempo. Si tiene una configuración personalizada para la entradaa de precios por defecto, se utilizará junto con la unidad. La combinación del producto y la unidad se utiliza para introducir precios predeterminados para materiales. |
    | Cantidad | Especifique la cantidad. | |
    | Precio | Si el precio se deja en blanco cuando se crea la línea del diario, los valores relevantes se usarán para introducir los precios predeterminados, según la clase de transacción. Si se introduce un precio cuando se crea la línea de diario, se utilizará ese precio. | |
    | Impuestos | Introduzca cualquier importe de impuestos. | Según el importe del impuesto que se introduzca, el importe extendido se calculará como *Importe* + *Impuesto*. |

## <a name="confirm-an-entry-journal"></a>Confirmar un diario de movimientos

Después de haber introducido todas las líneas de diario en un diario de movimientos, puede confirmar el diario. Este proceso registrará cada línea de diario como valores reales en los proyectos correspondientes.

Una vez que se confirma un diario, ya no puede editarlo,y tampoco ninguna de sus líneas.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Datos reales creados por la confirmación del diario de movimientos

Hay algunas diferencias clave entre los datos reales que se crean mediante la confirmación del diario de movimientos y los datos reales que se crean durante la aprobación de los registros de uso de Tiempo, Gastos y Material y la confirmación de la factura en Project Operations:

- Los diarios de movimientos no usan conexiones de transacciones para vincular el coste real con el dato real de ventas no facturadas. Los datos reales que se crean cuando se aprueban los registros de uso de Tiempo, Gastos y Material siempre usan conexiones de transacción para vincular los datos reales de ventas no facturadas y de costes.
- Los diarios de movimientos no usan orígenes de transacciones para vincular el coste real y los datos reales de ventas no facturadas con ningún registro de origen. Los datos reales que se crean cuando se aprueban los registros de uso de Tiempo, Gastos y Material siempre usan orígenes de transacción para vincular los datos reales de ventas no facturadas y de costes con el movimiento de tiempo de origen.
- Cuando se facturan los datos reales de ventas no facturadas que se crean mediante la confirmación del diario de entrada, los datos reales de ventas facturadas que se crean durante la confirmación de la factura se vinculan a los datos reales de ventas no facturadas, de manera similar a los datos reales de ventas no facturadas que se crean cuando se aprueban los registros de Tiempo, Gastos y Material.
- Las líneas de diario de movimientos que se crean para el tiempo en que se introducen mediante recursos entre organizaciones hacen que se creen automáticamente los tipos **Coste unitario de recursos** y **Ventas entre empresas** que se crearán automáticamente. Estos datos reales se deben crear manualmente. Este comportamiento difiere del comportamiento de las entradas de tiempo que registran los recursos entre organizaciones. En ese caso, cuando se aprueba el tiempo, la aplicación crea automáticamente datos reales del tipo **Coste** en el proyecto, y datos reales de los tipos **Coste unitario de recursos** y **Ventas entre empresas** en la división propietaria del empleado. A continuación, utiliza conexiones de transacción para vincular entre sí esos datos reales y los orígenes de transacción para vincularlos con la entrada de tiempo de origen.
- Cuando se confirman los diarios de movimientos, se crean datos reales. Sin embargo, los diarios de corrección no se pueden usar para corregir esos datos reales. Este comportamiento difiere del comportamiento de los datos reales que se crean cuando se aprueban los registros de uso de Tiempo, Gastos y Material. En ese caso, la aplicación le permite usar diarios de corrección para corregir los datos reales y corregir cualquier error, siempre que esos datos reales aún no se hayan facturado. Si ya se han facturado, aún puede corregir un dato real si procesa un crédito completo de ese dato real para el cliente.

> [!NOTE]
> Los diarios de movimientos no imponen reglas predeterminadas estrictas. Por lo tanto, use estos diarios de movimientos lo menos posible y tenga cuidado y precaución para asegurarse de no crear datos financieros corruptos en su sistema. Siempre que pueda, use registros de uso de Tiempo, Gastos y Material, la configuración de hitos y anticipos en contratos de proyectos y el proceso de confirmación de facturas de proyectos en lugar de diarios de movimientos para crear datos reales.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
