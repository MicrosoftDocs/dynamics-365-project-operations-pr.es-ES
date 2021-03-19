---
title: Administrar una factura proforma
description: En este tema se proporciona información acerca de cómo gestionar las facturas proforma.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29e301062f8f3ba955a95953bc2e891f3acaf765
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287709"
---
# <a name="manage-a-proforma-invoice"></a>Administrar una factura proforma

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

En Dynamics 365 Project Operations, las facturas proforma se crean como una extensión de las facturas de Dynamics 365 Sales. Sin embargo, existen muchas diferencias en el proceso de facturación entre Sales y Project Operations cuando se trata de facturación. Por ejemplo, no es posible crear una nueva factura desde la página **Lista de facturas** en Project Operations, pero es posible hacerlo en Sales. Estas diferencias y extensiones están implementadas para respaldar los procesos de facturación para proyectos que son diferentes de una factura típica para un pedido de cliente.

> [!IMPORTANT]
> Debido a las diferencias, no use las facturas en Sales y Project Operations de manera intercambiable.

## <a name="invoice-header"></a>Encabezado de la factura

La siguiente información está disponible en un encabezado de factura proforma en Project Operations.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Id. de factura** | Pestaña **Resumen** | El identificador que se genera automáticamente cuando se crea una factura proforma. Un campo de solo lectura que no puede editarse. | Este campo se utiliza como referencia para cada factura proforma. |
| **Nombre** | Pestaña **Resumen** | Se establece el nombre del contrato de proyecto de forma predeterminada. Este campo puede ser editado por el usuario. | &nbsp;  |
| **Divisa** | Pestaña **Resumen** | Se establece la divisa del contrato de proyecto de forma predeterminada. Un campo de solo lectura que no puede editarse. |&nbsp; |
| **Lista de precios** | Pestaña **Resumen** | Se establece la lista de precios del contrato de proyecto de forma predeterminada. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Oportunidad** | Pestaña **Resumen** | La referencia a la oportunidad vinculada. Un campo de solo lectura que no puede editarse. | &nbsp;  |
| **Contrato** | Pestaña **Resumen** | La referencia al contrato de proyecto enlazado. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Cliente** | Pestaña **Resumen** | La referencia al contrato de proyecto enlazado. Un campo de solo lectura que no puede editarse. |&nbsp;  |
| **Descripción** | Pestaña **Resumen** | El campo de texto que describe la factura. Este campo puede ser editado por el usuario. | &nbsp; |
| **Cobrar a** y campos relacionados | Pestaña **Resumen** | Los valores predeterminados se establecen desde el cliente del contrato del proyecto. Este campo puede ser editado por el usuario.  | &nbsp; |
| **Estado** | Pestaña **Resumen** | Establece las siguientes opciones: **Activo**, **Cerrado**, **Pagado** y **Cancelado** y el usuario puede editarlo. | Los estados no admitidos para Project Operations incluyen **Cerrado** y **Cancelado**. </br> El estado se establece en **Activo** cuando se crea la factura. </br>El estado debe establecerse en **Pagado** solo después de que se confirme la factura. |
| **Estado de la factura de proyecto** | Pestaña **Resumen** | Establece las siguientes opciones: **Borrador**, **En revisión** y **Confirmado**, y el usuario puede editarlas. | En los estados **Borrador** y **En revisión**, la factura se puede editar. La factura no se puede editar una vez confirmada. |
| **Importe detallado** | Pestaña **Resumen** | La suma de los importes de todas las líneas de factura después de anticipos y deducciones. Un campo de solo lectura que no puede editarse. | Este campo se utiliza para calcular la cantidad final. |
| **Descuento (%)** | Pestaña **Resumen** | Este campo se puede editar para ingresar un porcentaje de descuento. Este campo no es compatible con la funcionalidad de Project Operations. | Este campo no se admite. |
| **Importe de descuento** | Pestaña **Resumen** | Este campo se puede editar para ingresar el importe de descuento. Este campo no es compatible con la funcionalidad de Project Operations. | Este campo no se admite. |
| **Importe sin flete** | Pestaña **Resumen** | El monto total de la factura después de aplicar los descuentos. Un campo de solo lectura que no puede editarse. | Este campo se utiliza para calcular la cantidad final. |
| **Importe de flete** | Pestaña **Resumen** | Este campo se puede editar para ingresar el importe de flete. Este campo no es compatible con la funcionalidad de Project Operations. | Este campo no se admite. |
| **Impuesto total** | Pestaña **Resumen** | El impuesto total de todas las líneas de factura en la factura. Un campo de solo lectura que no puede editarse. | Ninguno. |
| **Importe total** | Pestaña **Resumen** | La suma del importe después de descuentos e impuestos. | La suma es la cantidad que el cliente debe pagar. |

## <a name="project-based-invoice-lines"></a>Líneas de factura basadas en proyectos

En Project Operations, siempre hay una línea de factura para cada línea de contrato de proyecto. La línea de factura se crea incluso si no hay datos reales. La siguiente información está disponible en una línea de factura proforma.

| Campo | Ubicación | Descripción | Impacto posterior |
| --- | --- | --- | --- |
| **Id. de factura** | Pestaña **General** | La referencia al ID de factura. Un campo de solo lectura que no puede editarse. | El enlace de ID de factura se puede utilizar para volver al encabezado de la factura. |
| **Nombre** | Pestaña **General** | El nombre de la línea de la factura establecida de forma predeterminada a partir del nombre de la línea del contrato. Este campo puede ser editado por el usuario. | &nbsp; |
| **Project** | Pestaña **General** | El proyecto en la línea de contrato del proyecto relacionado. Un campo de solo lectura que no puede editarse. | El enlace del proyecto se puede utilizar para navegar al proyecto. |
| **Método de facturación** | Pestaña **General** | El método de facturación en la línea de contrato del proyecto relacionado. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Importe de línea de contrato** | Pestaña **General** | El importe del contrato en la línea de contrato de proyecto relacionada. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Facturado hasta la fecha** | Pestaña **General** | La suma de los importes de todos los detalles de la línea de factura de esta factura. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Importe** | Pestaña **General** | La suma de los importes de todos los detalles de la línea de factura que se cobran de esta factura. Un campo de solo lectura que no puede editarse. | Este campo se utiliza para calcular la cantidad final en el encabezado de factura. |
| **Impuesto** | Pestaña **General** | La suma de los importes de impuestos de todos los detalles de la línea de factura de esta línea de factura. Un campo de solo lectura que no puede editarse. | Este campo se utiliza para calcular la cantidad de impuestos final en el encabezado de factura. |
| **Importe ampliado** | Pestaña **General** | La suma de los importes totales (**Impuestos + Importes**) de todos los detalles de la línea de factura que se cobran de esta línea de factura. Un campo de solo lectura que no puede editarse. | Este campo se utiliza para calcular la cantidad final en el encabezado de factura. |

## <a name="invoice-line-details"></a>Detalles de línea de factura

Cada línea de factura en una factura de proyecto incluye detalles de la línea de factura. Estos detalles de línea están relacionados con los datos reales de ventas no facturadas y los hitos que se relacionan con la línea de contrato a la que hace referencia la línea de factura. Todas estas transacciones están marcadas **Listo para facturar**.

Para la línea **Factura de tiempo y material**, los detalles de la línea de factura se agrupan en **Cobrable**, **No imputable** y **Complementario** en la página **Línea de factura**. Los detalles de **Línea de factura con cargo** se suman al total de la línea de factura. **Complementario** y **Datos reales no imputables** no se suman al total de la línea de la factura.

Para la línea **Factura de precio fijo**, los detalles de la línea de factura se crean a partir de hitos que están marcados como **Listo para facturar** en la línea de contrato relacionada. Una vez que se crea el detalle de la línea de factura a partir de un hito, el estado de facturación en el hito se actualiza a **Factura de cliente creada**.

### <a name="edit-invoice-line-details"></a>Editar detalles de línea de factura

Los siguientes campos están disponibles en el detalle de la línea de factura que está respaldado por un real de ventas no facturadas.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| **Línea de factura** | Una referencia al **ID de línea de factura**. Campo de solo lectura, bloqueado para la edición. | Este enlace se puede utilizar para volver al encabezado de la factura. |
| **Descripción** | Una descripción del detalle de línea de factura. Establecido por defecto en el campo **Comentarios internos** de **Entrada de tiempo**, y en el campo **Descripción** en **Entrada de gastos**. El campo puede ser editado por el usuario.| &nbsp; |
| **Descripción externa** | Una descripción del detalle de línea de factura. Establecido por defecto en el campo **Comentarios externos** de **Entrada de tiempo**, y en el campo **Descripción** en **Entrada de gastos**. El campo puede ser editado por el usuario. | Esta descripción se puede utilizar para determinar qué debe estar en la factura impresa que se enviará al cliente. En Project Operations, una factura proforma no tiene todas las funciones necesarias para configurar los ajustes de impresión de una factura. |
| **Fecha de inicio** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Este campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Project** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Se establece por defecto en el proyecto en la línea de contrato relacionada. |
| **Tarea** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. Una lista desplegable muestra todas las tareas asociadas a la línea de contrato del proyecto relacionado.  |
| **Categoría de transacción** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Rol** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Recurso que se puede reservar** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Empresa de dotación de recursos** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Unidad de dotación de recursos** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Cantidad** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. |
| **Programación de unidad** | Para el detalle de la línea de la factura por tiempo, esto siempre se establece en tiempo y no se puede editar. Para los gastos, esto se establece de forma predeterminada a partir del gasto de origen real. Un campo de solo lectura que no puede editarse. | Establecido de forma predeterminada en **Hora** en un nuevo detalle de línea de factura que no esté respaldado por un valor real. |
| **Unidad** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real |
| **Precio** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | El campo se puede editar en un nuevo detalle de línea de factura que no esté respaldado por una fuente real. Si no se ingresa ningún valor, se establece por defecto después de **Salvar**. |
| **Divisa** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Se establece de forma predeterminada desde el encabezado de la factura al crear un nuevo detalle de factura sin respaldo real.  Un campo de solo lectura que no puede editarse. |
| **Importe** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Calculado como **Cantidad\* Precio** al crear un nuevo detalle de factura sin un respaldo real. Se calcula después de **Salvar**. Un campo de solo lectura que no puede editarse. |
| **Impuesto** | Establecido por defecto a partir de la fuente actual. El campo puede ser editado por el usuario | El usuario puede editar el campo al crear un nuevo detalle de línea de factura sin un respaldo real. |
| **Importe ampliado** | Un campo calculado, calculado como **Importe + Impuestos**. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Tipo de facturación** | Establecido por defecto a partir de la fuente actual. El campo puede ser editado por el usuario. | Al seleccionar **Cobrable**, se suma la línea al total de la línea de la factura. **Complementario** y **No imputable** lo excluirán del total de la línea de factura. |
| **Tipo de transacción** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Establecido de forma predeterminada en **Ventas facturadas** y bloqueado al crear un nuevo **Detalle de la línea de la factura** sin respaldo real.  |
| **Clase de transacción** | Establecido por defecto a partir de la fuente actual. Un campo de solo lectura que no puede editarse. | Establecido de forma predeterminada en función de si el usuario elige crear un detalle de línea de factura de **Hora**, **Gastos** o **Cuota** al mismo tiempo que crea un nuevo **Detalle de la línea de la factura** sin un respaldo real. Bloqueado para edición. |

Los siguientes campos están disponibles en un detalle de la línea de factura que está respaldado por un hito:

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| **Línea de factura** | Referencia al **ID de línea de factura**. Un campo de solo lectura que no puede editarse. | El enlace se puede utilizar para volver al encabezado de la factura. |
| **Descripción** | Descripción del detalle de línea de factura. Establecido de forma predeterminada a partir de la descripción del hito de origen. | &nbsp; |
|**Descripción externa** | Descripción del detalle de la línea de factura que se establece de forma predeterminada a partir de la descripción del hito de origen. | Este campo se puede utilizar para determinar qué debe estar en la factura impresa que se enviará al cliente. Una factura proforma en Project Operations no tiene todas las funciones necesarias para configurar los ajustes de impresión de una factura. |
| **Fecha de inicio** | Establecido por defecto desde la fecha del **Hito** en el hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Project** | Establecido por defecto a partir del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Tarea** | Establecido por defecto a partir del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Categoría de transacción** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Rol** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Recurso que se puede reservar** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Unidad de dotación de recursos** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Programación de unidad** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Unidad** | Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Precio** | Establecido de forma predeterminada a partir del importe del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Divisa** | Establecido por defecto a partir del hito de origen. Un campo de solo lectura que no puede editarse. |&nbsp; |
| **Importe** | Establecido de forma predeterminada a partir del importe del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Impuesto** | Establecido de forma predeterminada a partir del importe de impuestos del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Importe ampliado** | Establecido de forma predeterminada a partir del importe extendido del hito de origen. El campo puede ser editado por el usuario | &nbsp; |
| **Tipo de facturación** | Siempre configurado de forma predeterminada en **Cobrable**. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Tipo de transacción** | Establecido por defecto a partir del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |
| **Clase de transacción** | Establecido por defecto a partir del hito de origen. Un campo de solo lectura que no puede editarse. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Actualizar transacciones de factura

Si tiene datos reales que llegaron después de que se creó la factura, puede incluir estos datos reales en la factura.

1. En **Vista del registro de facturación**, marcar los datos como **Listo para facturar**.   
2. Abra el borrador de la factura proforma y, en la cinta **Comportamiento**, haga clic en **Actualizar transacciones de línea de factura**.

  Esto crea detalles de línea de factura para cualquier importe real que tenga fecha pasada y esté marcado como **Listo para facturar**; pero no está incluido en la factura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]