---
title: Facturación de empresas vinculadas
description: Este artículo proporciona información y ejemplos sobre la facturación de empresas vinculadas para proyectos.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085174"
---
# <a name="intercompany-invoicing"></a>Facturación de empresas vinculadas

[!include [banner](../includes/banner.md)]

Este artículo proporciona información y ejemplos sobre la facturación de empresas vinculadas para proyectos.

Su organización puede tener varias divisiones, subsidiarias y otras entidades jurídicas que se transfieren productos y servicios entre sí para proyectos. La entidad jurídica que proporciona el servicio o producto se denomina *entidad jurídica prestamista* , y la entidad legal que recibe el servicio o producto se llama *entidad jurídica prestataria*. 

La siguiente ilustración muestra un escenario típico donde dos entidades jurídicas, SI FR (la entidad jurídica prestataria) y SI USA (la entidad jurídica prestamista) comparten recursos para entregar un proyecto al cliente A. Para este escenario, SI FR está contratada para entregar el trabajo al cliente A. 

[![Ejemplo de facturación de empresas vinculadas](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

El objetivo es hacer que el control de costos, el reconocimiento de ingresos, los impuestos y el precio de transferencia para las transacciones de proyectos en empresas vinculadas sean más flexibles y eficaces. Además, se proporcionan las siguientes capacidades:

-   Crear facturas de cliente para un proyecto en una entidad jurídica prestataria mediante el uso de hojas de horas, gastos y facturas de proveedores de empresas vinculadas en una entidad jurídica prestamista.
-   Compatibilidad con cálculos de impuestos y costes indirectos.
-   Diferir el reconocimiento de ingresos en una entidad jurídica prestamista y cuando una entidad legal prestataria debería reconocer el coste.
-   Acumular ingresos de trabajo en proceso (WIP) en la entidad jurídica prestamista.
-   Establecer precios de transferencia que puedan basarse en varios modelos de precios. Estos son algunos ejemplos:
    -   **Cantidad** : la cantidad que ingresa en el campo **Precios** es el cose real por cantidad o unidad.
    -   **Importe de los cargos** : el precio o coste por transacción más el importe de los cargos que se especifica en el campo **Precios**.
    -   **Porcentaje de cargos** : el precio de transferencia es el precio o coste por transacción multiplicado por el porcentaje de cargos que se especifican en el campo **Precios**.
    -   **Porcentaje del precio de venta** : el porcentaje del precio de venta que se transfiere a la entidad jurídica prestamista.
    -   **Importe por debajo del precio de venta** : el importe que la entidad jurídica prestataria retiene de los precios de venta antes de transferirlo a la entidad jurídica prestamista.
    -   **Proporción de contribución** : el número que especifica en el campo **Precios** es la proporción de contribución, que se expresa como un porcentaje del precio de venta.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Ejemplo 1: configurar parámetros para la facturación de empresas vinculadas
En este ejemplo, USSI es una entidad jurídica prestamista, y sus empleados están notificando tiempo a atribuir a la entidad jurídica prestataria, FRSI, que es propietaria del contrato con el cliente final. Las horas y los gastos que informan los empleados de USSI se pueden incluir en la factura del proyecto que genera FRSI. Además, existe un tercer origen de transacciones que pueden originarse en la entidad jurídica prestamista (USSI en este ejemplo) cuando brinda servicios de proveedores compartidos a subsidiarias (como FRSI) y luego transfiere esos costes a proyectos dentro de esas subsidiarias. Todos los documentos correspondientes a facturas y los cálculos de impuestos los tramita Finance. 

Para este ejemplo, FRSI debe ser un cliente en la entidad jurídica USSI y USSI debe ser un proveedor en la entidad jurídica FRSI. A continuación, puede configurar una relación de empresas vinculadas entre las dos entidades jurídicas. El siguiente procedimiento muestra cómo configurar los parámetros para que ambas entidades jurídicas puedan participar en la facturación entre empresas.

1. Configure FRSI como un cliente en la entidad jurídica USSI y configure USSI como proveedor de la entidad jurídica FRSI. Hay tres puntos de entrada para los pasos necesarios para esta tarea.

   | Paso |                                                       Punto de entrada                                                        |                                                                                                                                                                                               Descripción                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  E   | En USSI, haga clic en <strong>Clientes</strong> &gt; <strong>Clientes</strong> &gt; <strong>Todos los clientes</strong>. |                                                                                                                                                                  Cree un nuevo registro de cliente para FRSI y seleccione el grupo de clientes.                                                                                                                                                                  |
   |  B   |    En FRSI, haga clic en <strong>Proveedores</strong> &gt; <strong>Proveedores</strong> &gt; <strong>Todos los proveedores</strong>.     |                                                                                                                                                                    Cree un nuevo registro de proveedor para USSI y seleccione el grupo de proveedores.                                                                                                                                                                    |
   |  C   |                                  En FRSI, abra el registro del proveedor que acaba de crear.                                  | En el Panel de acciones, en la pestaña <strong>General</strong>, en el grupo <strong>Configurar</strong>, haga clic en <strong>Empresas vinculadas</strong>. En la página <strong>Empresas vinculadas</strong>, en la pestaña <strong>Relación comercial</strong>, establezca el control deslizante <strong>Activo</strong> en <strong>Sí</strong>. En el campo <strong>Empresa del cliente</strong>, seleccione el registro de cliente que creó en el paso A. |


2. Haga clic en **Gestión de proyectos y contabilidad** &gt; **Configuración** &gt; **Parámetros de gestión de proyectos y contabilidad** y luego haga clic en la pestaña **Empresas vinculadas**. La forma de configurar los parámetros depende de si usted es la entidad jurídica prestataria o la entidad jurídica prestamista.
   -   Si usted es la entidad jurídica prestataria, seleccione la categoría de compras que debe usarse para hacer corresponder las facturas del proveedor, que se generan automáticamente.
   -   Si es la entidad jurídica prestamista, para cada entidad prestataria, seleccione una categoría de proyecto predeterminada para cada tipo de transacción. Las categorías de proyecto se utilizan para la configuración de impuestos cuando la categoría facturada en las transacciones entre empresas vinculadas existe solo en la entidad jurídica prestataria. Puede optar por acumular ingresos por transacciones entre empresas vinculadas. Esta acumulación se realiza cuando se registran las transacciones y luego se revierte cuando se registra la factura de empresas vinculadas.

3. Haga clic en **Gestión de proyectos y contabilidad** &gt; **Configuración** &gt; **Precios** &gt; **Precio de transferencia**.
4. Seleccione una divisa, tipo de transacción y modelo de precio de transferencia. La divisa que se utiliza en la factura es la divisa configurada en el registro de cliente para la entidad jurídica prestataria en la entidad jurídica prestamista. La divisa se utiliza para hacer coincidir las entradas en la tabla de precios de transferencias.
5. Haga clic en **Contabilidad general** &gt; **Configuración del registro** &gt; **Contabilidad entre empresas** y establezca una relación para USSI y FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Ejemplo 2: Crear y publicar una hoja de horas de empresas vinculadas
USSI, la entidad legal prestamista, debe crear y publicar la hoja de horas para un proyecto de FRSI, la entidad legal prestataria. Hay dos puntos de entrada para los pasos necesarios para esta tarea.

| Paso | Punto de entrada                                                                       | Descripción                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| E    | **Gestión de proyectos y contabilidad** &gt; **Proyectos** &gt; **Todas las hojas de horas** | Cree una nueva hoja de horas. En la línea de la hoja de horas, en el campo **Entidad jurídica** , seleccione **FRSI**. En el campo **Id. de proyecto** , seleccione el proyecto en FRSI. Especifique las horas para cada día de la semana. |
| B    | Página **Hoja de horas**                                                                | Después de que se ejecute el flujo de trabajo, publique la hoja de horas y anote el número de comprobante.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Ejemplo 3: Crear y publicar una factura de proveedor de empresas vinculadas
USSI, la entidad legal prestamista, debe crear y publicar la factura de proveedor de empresas vinculadas un proyecto de FRSI, la entidad legal prestataria. Esta factura de proveedor representa la mano de obra subcontratada y los gastos realizados por los proveedores pagados por USSI. Hay dos puntos de entrada para los pasos necesarios para esta tarea.

| Paso | Punto de entrada                                                                                      | Descripción                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| E    | **Proveedores** &gt; **Facturas** &gt; **Facturas de proveedor abiertas** &gt; **Nueva factura de proveedor** | Cree una nueva factura de proveedor y especifique los servicios que se produjeron en nombre del proyecto de FRSI.                                                                                                                                                                                  |
| B    | La página **Factura de proveedor**                                                                      | Especifique las líneas que representen los servicios subcontratados en nombre de FRSI. En la ficha desplegable **Detalles de la línea** , en la pestaña **Proyecto** para la línea de factura, en el campo **Empresa de proyecto** , especifique **FRSI**. Especifique el proyecto y la información correspondiente. Posteriormente, registre la factura del proveedor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Ejemplo 4: Crear y publicar la factura de empresas vinculadas
USSI, la entidad legal prestamista, debe crear y registrar la factura entre empresas vinculadas. Hay dos puntos de entrada para los pasos necesarios para esta tarea.

| Paso | Punto de entrada                                                                                             | Descripción                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| E    | **Gestión de proyectos y contabilidad** &gt; **Facturas del proyecto** &gt; **Factura de cliente de empresas vinculadas**  | Haga clic en **Nuevo** para abrir la página **Crear factura de empresas vinculadas**.                                                                                  |
| B    | **Gestión de proyectos y contabilidad** &gt; **Facturas del proyecto** &gt; **Factura de cliente de empresas vinculadas** | En la página **Crear factura de empresas vinculadas** , especifique la entidad legal y la transacción que debe incluirse, y luego haga clic en **Buscar**. |
| C    | **Gestión de proyectos y contabilidad** &gt; **Facturas del proyecto** &gt; **Factura de cliente de empresas vinculadas** | Seleccione las transacciones a facturar o haga clic en **Seleccionar todo** para facturar todas las transacciones de la lista y luego haga clic en **Okay**.                  |
| E    | La página **Factura de empresas vinculadas**                                                                       | Se muestra la propuesta de factura de cliente de empresas vinculadas.                                                                                             |
| E    | La página **Factura de empresas vinculadas**                                                                       | Haga clic en **Registrar**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Ejemplo 5: Registrar la factura del proveedor y facturar al cliente
Cuando la entidad jurídica prestamista, USSI, registra la factura del cliente de empresas vinculadas, se crea la factura correspondiente de proveedor pendiente en la entidad jurídica prestataria, FRSI. Después de que se registre esta factura de proveedor, FRSI también factura al cliente del proyecto por las horas que especificó USSI. Hay tres puntos de entrada para los pasos necesarios para esta tarea.

| Paso | Punto de entrada                                                                                        | Descripción                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| E    | **Proveedores** &gt; **Facturas** &gt; **Facturas de proveedor abiertas**                            | Revise la factura para verificar que se incluyan los valores de la hoja de horas y luego registre la factura del proveedor.                  |
| B    | **Gestión de proyectos y contabilidad** &gt; **Facturas del proyecto** &gt; **Propuestas de facturas del proyecto** | Cree una nueva factura de proyecto para el proyecto y verifique que aparezcan las transacciones de horas que se registraron.            |
| C    | La página **Factura de proyecto**                                                                       | Seleccione la factura del proyecto y luego haga clic en **Ver detalles** para revisar el coste y el importe de las ventas. Posteriormente, registre la factura. |


Para más información, vea [Configurar la facturación de proyectos de empresas vinculadas](tasks/configure-intercompany-project-invoicing.md).


