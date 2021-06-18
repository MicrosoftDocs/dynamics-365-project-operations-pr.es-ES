---
title: Administrar propuestas de factura de proyecto
description: Este tema proporciona los detalles del procesamiento de facturas para los clientes con Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7e6d060c1cca08f86e2d04ca96c9315a17316d11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001492"
---
# <a name="manage-project-invoice-proposals"></a>Administrar propuestas de factura de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las propuestas de factura de proyecto se pueden procesar en el departamento de facturación cuando se cumplen las dos condiciones siguientes:

  - El jefe del proyecto confirma la factura proforma en Microsoft Dataverse.
  - Todas las transacciones de ventas de tiempo y material no facturadas que se incluyan en la factura proforma se registrarán mediante el diario **Integración de Project Operations** de Dynamics 365.

Use los pasos siguientes para completar una propuesta de factura de proyecto en Dynamics 365 Finance.

1. Revise la información de facturación para las transacciones de tiempo y material y registre el diario de **Integración de Project Operations**.
2. Revise la información de facturación para conocer los hitos de facturación de precio fijo.
3. Revise y formatee una propuesta de factura de proyecto.
4. Registre e imprima las facturas de proyecto.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Administrar la información de facturación en el diario de integración de Project Operations

Los datos reales de proyecto creados en Dataverse los revisa y registra el contable del proyecto en Finance. Para obtener más información sobre cómo trabajar con el diario de integración, consulte [Diario de integración en Project Operations](../project-accounting/project-operations-integration-journal.md).

Los datos reales de coste y los de ventas no facturadas se agregan al diario de integración como líneas independientes:

  - Para el precio de coste unitario y el importe del coste en los datos reales de coste se usan los valores predeterminados de la transacción de coste real del proyecto en Dataverse.
  - Para el precio de venta unitario y el importe de venta de la transacción de ventas no facturadas se usan los valores predeterminados de la transacción de ventas no facturada real del proyecto en Dataverse.

### <a name="billing-sales-tax"></a>Impuestos sobre las ventas de facturación

El cálculo del impuesto sobre las ventas para la facturación se determina mediante la combinación de campos **Grupo de impuestos sobre las ventas de facturación** y **Grupo de impuestos sobre las ventas de artículos de facturación** en un registro de ventas no facturadas en la línea del diario de **Integración de Project Operations**. El sistema establece estos valores de campo de forma predeterminada en función de la configuración de la pestaña **Datos financieros** en la página **Parámetros de gestión de proyectos y contabilidad**.

- **Método de grupo de impuestos** determina la lógica de incumplimiento del grupo de impuestos de facturación:
  
  - **Proyecto**: siempre usará de forma predeterminada el grupo de impuestos de facturación del proyecto. Para revisar o cambiar el grupo de impuestos de facturación predeterminado en un proyecto, seleccione **Mostrar contabilidad predeterminada** en la página **Todos los proyectos**.
  - **Contrato de proyecto**: siempre usará de forma predeterminada el grupo de impuestos de facturación del contrato de proyecto. Para revisar o cambiar el grupo de impuestos predeterminado en un contrato de proyecto, seleccione **Mostrar contabilidad predeterminada** en la página **Contratos de proyecto**.
  - **Cliente**: siempre usará de forma predeterminada el grupo de impuestos de facturación del cliente.
  - **Buscar**: buscará en todas las entidades anteriores y seleccionará el primer valor disponible. La búsqueda comienza con la entidad **Proyecto**, sigue con la entidad **Contrato de proyecto** y finaliza con la entidad **Cliente**.

- **Método de grupo de impuestos de artículos** determina la lógica de incumplimiento del grupo de impuestos de artículos de facturación:
  
  - Para los tipos de transacciones de tiempo, gastos y tarifas, el grupo de impuestos de artículos de facturación siempre usará de forma predeterminada la entidad **Categoría de proyecto**.
  - Para los tipos de transacciones de material, el grupo de impuestos de artículos de facturación usará de forma predetermina la configuración de **Método de grupo de impuestos de artículos** en **Parámetros de gestión de proyectos y contabilidad**. El número de artículo usa de forma predeterminada el grupo de impuestos de artículo de la entidad **Producto emitido**. La categoría usa de forma predeterminada el grupo de impuestos de artículo de la entidad **Categoría de proyecto**.

### <a name="financial-dimensions"></a>Dimensiones financieras

Las dimensiones financieras de los registros de ventas no facturados en el diario de **Integración de Project Operations** usa de forma predeterminada la entidad **Proyecto**. Las dimensiones financieras se pueden revisar y ajustar seleccionando **Distribuir importes**. Si tiene que cambiar las dimensiones financieras del registro de ventas no facturado después de que se haya contabilizado el diario de integración pero antes de que se confirme la factura proforma, vaya a **Todos los proyectos** > **Administrar** > **Transacciones registradas**, seleccione la transacción y después seleccione **Proceso** > **Ajustar la contabilidad**.

### <a name="exchange-rates"></a>Tipos de cambio

La divisa de transacción no facturada en Dataverse se utiliza como divisa de transacción en Finance y se convierte a la divisa de contabilidad de la empresa con los tipos de cambio definidos en Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Administrar los atributos financieros de los hitos de facturación 

Las líneas de contrato de proyecto que utilizan el método de facturación de precio fijo se facturan a través de [Hitos de precio fijo](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). El contable del proyecto puede revisar los hitos de facturación en Finance yendo a **Gestión de proyectos y contabilidad** > **Todos los proyectos** > **Administrar** > **Transacciones en cuenta**.

### <a name="billing-sales-tax"></a>Impuestos sobre las ventas de facturación

En **Grupo de impuestos** y **Grupo de impuestos de artículos** se usan de forma predeterminada los valores de la configuración al crear un nuevo hito de facturación en Dataverse. El sistema usa de forma predeterminada los valores de estos campos según la configuración de la pestaña **Datos financieros** de la página **Parámetros de gestión de proyectos y contabilidad**.

- **Método de grupo de impuestos** determina la lógica de valores predeterminados de **Grupo de impuestos de facturación**:

    - **Proyecto** siempre usará de forma predeterminada el grupo de impuestos de facturación del proyecto. Para revisar o cambiar el grupo de impuestos predeterminado en un proyecto, seleccione **Mostrar contabilidad predeterminada** en la página **Todos los proyectos**.
    - **Contrato de proyecto** siempre usará de forma predeterminada el grupo de impuestos de facturación del contrato de proyecto. Para revisar o cambiar el grupo de impuestos predeterminado en un contrato de proyecto, seleccione **Mostrar contabilidad predeterminada** en la página **Contratos de proyecto**.
    - **Cliente** siempre usará de forma predeterminada el grupo de impuestos de facturación del cliente.
    - **Buscar** buscará en todas las entidades de esta lista y seleccionará el primer valor disponible. La búsqueda comienza con la entidad **Proyecto**, sigue con la entidad **Contrato de proyecto** y finaliza con la entidad **Cliente**.

- **Grupo de impuestos sobre las ventas de artículos de hito de precio fijo** se utiliza como valor predeterminado en el campo **Grupo de impuestos sobre las ventas de artículos** para el hito de facturación. El contador puede revisar y modificar este valor en la página **Transacciones a cuenta**. El sistema utiliza el valor de la transacción a cuenta al crear una línea de propuesta de factura de proyecto.
 

### <a name="financial-dimensions"></a>Dimensiones financieras

Las dimensiones financieras predeterminadas para el hito de facturación de precio fijo se establecen en las líneas de contrato del proyecto. Vaya a **Contratos de proyecto** > **Mostrar contabilidad predeterminada** y, en la pestaña **Líneas de contrato**, seleccione **línea de contrato de precio**. A continuación, establezca los valores de dimensiones financieras que desee utilizar como predeterminados.

El contable del proyecto podrá editar la información sobre las dimensiones financieras y de impuestos sobre las ventas en los hitos de la factura hasta que se cree la propuesta de factura del proyecto.


## <a name="create-project-invoice-proposals"></a>Crear propuestas de factura de proyecto

Las propuestas de factura de proyecto se pueden revisar en el módulo **Gestión de proyectos y contabilidad**. Vaya a **Facturas de proyecto** > **Propuestas de factura de proyecto**.

El encabezado de la propuesta de factura del proyecto se crea en Finance cuando se confirma la factura proforma en Dataverse. Para facilitar la conciliación, el sistema establece como número de propuesta de factura de proyecto en Finance el mismo número que se usa como id. de factura proforma en Dataverse. Como las facturas proforma no se confirman necesariamente en el mismo orden en que se crean, la secuencia de números de propuesta de factura de proyecto en Finance debe permitir cambios en los números más bajos y en los más altos. Configure las secuencias numéricas mediante los pasos siguientes:

1. En Finance, vaya a **Administración de la organización** > **Secuencias numéricas** > **Secuencias numéricas**.
2. En el filtro **Área**, seleccione **Proyectos**.
3. En el filtro **Referencia**, seleccione **Propuesta de factura**.
4. Use el campo **Empresa** para filtrar cada entidad jurídica con la integración de Project Operations Dataverse habilitada.
5. Abra **Detalles de la secuencia numérica** y, en la pestaña **General**, establezca:

    - **Permitir cambios de usuario: a un número menor** = **Sí**
    - **Permitir cambios de usuario: a un número mayor** = **Sí**

El sistema agrega líneas de propuesta de factura de proyecto mediante el proceso periódico **Importar desde tabla de almacenamiento provisional** (**Gestión de proyectos y contabilidad** > **Periódico** > **Integración de Project Operations** > **Importar desde la tabla de almacenamiento provisional**). Este proceso se puede ejecutar manualmente o con una programación periódica. El sistema no agregará líneas al documento de propuesta de factura hasta que todas las líneas estén listas para facturarse. Las transacciones de tiempo y material solo estarán listas para facturarse cuando se contabilicen mediante el diario de **Integración de Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formato e impresión de propuestas de factura

El contable del proyecto puede personalizar la impresión de una factura de proyecto a través de la página **Formato de propuesta de factura** y la funcionalidad de administración de la impresión.

### <a name="format-invoice-proposals"></a>Aplicar formato a propuestas de factura

La página **Aplicar formato a propuestas de factura** permite que las transacciones de agrupación personalizadas se muestren en la factura del proyecto del cliente.

1. En la página **Propuesta de factura de proyecto**, seleccione **Impresión** > **Formato de propuesta de factura**.
2. Seleccione **Nuevo** para crear una nueva agrupación para la impresión de la factura del proyecto.
3. En el campo **Detalles/resumen**, seleccione las opciones de esta agrupación:

    - Seleccione **Detalle** para imprimir los detalles de la transacción de la factura del cliente.
    - Seleccione **Resumen** para imprimir el resumen de transacción de la factura del cliente.

> [!NOTE]
> La selección del campo **Detalle/resumen** en la página **Formato de propuesta de factura** anula la opción seleccionada en el campo **Formato de la factura** en la página **Propuestas de factura** para imprimir una factura detallada o una factura resumida.

- Seleccione las líneas de transacción que desea incluir en esta sección en la pestaña **Transacciones disponibles** y seleccione **Incluir transacciones** para moverlos a la pestaña **Transacciones seleccionadas**.
- Seleccione **Subir** y **Bajar** para cambiar el orden de las secciones.
- Seleccione **Vista previa de impresión** para obtener una vista previa de la factura formateada.

### <a name="print-management"></a>Administración de impresión

La administración de impresión utiliza diferentes archivos de informe para imprimir, especificar destinos y personalizar el texto del pie de página para la factura. La administración de impresión puede configurarse a nivel de módulo, pero se puede anular esta configuración para un cliente, contrato o propuesta de factura específicos. Para acceder a esta función en la página **Propuesta de factura de proyecto**, seleccione **Imprimir** > **Administración de impresión**.

La configuración de la administración de impresión se muestra como una vista de árbol, donde cada nivel de nodo muestra los documentos disponibles para ajustar. Puede asignar impresiones personalizadas a nivel de módulo, cliente, contrato o documento de propuesta de factura. Para modificar la impresión del documento original, expanda el nodo en cuestión y seleccione **Elemento original**. En el campo **Formato de informe**, seleccione el formato de informe que se utilizará para la impresión. Puede utilizar formatos de informe personalizados mediante el [Marco de administración de documentos empresariales](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Registrar propuestas de factura

Una vez que haya revisado y editado la factura, y las líneas de propuesta de factura sean satisfactorias, compruebe los totales de la factura y el impuesto sobre las ventas. En el grupo **Detalles**, seleccione **Totales** y, a continuación, seleccione **Enviar** para registrar la factura.

Para ver la factura antes de registrarla, desactive la casilla **Registro**. Se imprimirá **Proforma** en la factura para indicar que se trata de una factura de ejemplo. Para imprimir la factura, active la casilla **Imprimir factura**.

Además de la página **Propuesta de factura**, las propuestas de factura también se pueden publicar ejecutando el trabajo periódico **Registrar propuestas de factura**. Para encontrar este trabajo, vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Facturas de proyecto** > **Registrar propuestas de factura**.

Esta página muestra todas las propuestas de facturas que están listas para su registro. Puede seleccionar **Lote** para programar el registro de propuestas de facturas. Establezca el parámetro **Procesamiento por lotes** en **Sí** y seleccione **Periodicidad** para establecer la periodicidad del procesamiento por lotes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
