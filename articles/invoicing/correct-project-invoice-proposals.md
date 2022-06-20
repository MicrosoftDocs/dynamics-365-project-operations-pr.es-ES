---
title: Corregir la contabilidad en propuestas de factura de proyecto en borrador
description: Este artículo explica cómo ajustar la información relacionada con la contabilidad en un borrador de propuesta de factura.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921231"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corregir la contabilidad en propuestas de factura de proyecto en borrador

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

El administradior del proyecto mantiene los *Detalles de operaciones* para las facturas del mismo en una factura proforma. Estos detalles incluyen la decisión sobre las horas, gastos, materiales o hitos que se deben facturar, las tarifas y la aplicación de los importes de anticipos y avances. Después de confirmar la factura proforma original, puede ajustar los detalles de operaciones creando y confirmando una [factura proforma correctiva](../proforma-invoicing/corrective-invoices.md).

Los *Detalles de contabilidad* para las facturas del proyecto se mantienen en un documento de factura de cara al cliente. Estos detalles incluyen el cálculo del impuesto sobre las ventas y las dimensiones financieras que se aplican a la factura. Este artículo proporciona detalles sobre cómo se pueden ajustar estos detalles contables en un borrador de propuesta de factura de proyecto.

## <a name="adjust-sales-tax"></a>Ajustar el impuesto de ventas

Los grupos de impuestos sobre las ventas de facturación predeterminados y los grupos de impuestos sobre las ventas de artículos se pueden ajustar directamente en el documento de propuesta de factura. Para ajustar estos grupos, seleccione **Editar** y luego, en cada línea de propuesta de factura de proyecto, introduzca un nuevo valor en los campos **Grupo de impuestosç** o **Grupos de impuestos de artículos**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensiones financieras

### <a name="header-dimensions"></a>Dimensiones del encabezado

De forma predeterminada, las dimensiones financieras de la factura se derivan de los registros de transacciones de proyectos no facturados que se están facturando. Sin embargo, la configuración del sistema le permite usar dimensiones financieras en el encabezado de las propuestas de facturas de proyectos para registrar saldos de clientes. Para habilitar esta función, seleccione **Permitir actualizaciones de las dimensiones del proyecto para clientes** en la pestaña **Finanzas** de la página **Parámetros contables y de gestión de proyectos**.

Las dimensiones financieras en los encabezados de las facturas se pueden editar antes de que se registre una factura. En la página **Propuesta de factura de proyecto**, cambie a la vista **Encabezamiento** y luego edite los valores en la pestaña **Dimensiones financieras**.

La vista **Encabezamiento** está disponible solo después de que el administrador del sistema habilite la característica **Utilizar la propuesta de factura del proyecto y los formularios de diario de facturas con la vista Encabezado y Líneas**, en el espacio de trabajo **Gestión de características**. Esta característica requiere la actualización de Finanzas 10.0.25 o posterior.

### <a name="line-dimensions"></a>Dimensiones de línea

Las dimensiones financieras no se pueden editar directamente en una línea de propuesta de factura de proyecto. En su lugar, siga estos pasos para ajustar las dimensiones financieras en una propuesta de factura de proyecto.

1. En la propuesta de factura del proyecto, seleccione **Eliminar todo** para eliminar las líneas de propuesta de factura del proyecto.

    El botón **Eliminar todo** está disponible solo después de que el administrador del sistema habilite la característica **Eliminar las líneas de propuesta de factura cuando utilice Project Operations para escenarios basados en recursos/sin existencias** en el área de trabajo **Administración de características**.

2. Ajustar dimensiones financieras:

    - **Transacciones a cuenta (hitos de facturación):** vaya a **Todos los proyectos** \> **Administrar** \> **Transacciones a cuenta** y seleccione el hito que necesite ajuste. Después, en la pestaña **Dimensiones financieras**, actualice los valores según sea necesario.
    - **Transacciones de tiempo, gastos y materiales:** en la página **Transacciones de proyecto registradas**, seleccione **Ajustar la contabilidad** para actualizar las dimensiones financieras.

3. Una vez que haya terminado de ajustar los valores de la dimensión financiera, vaya a **Administración de proyectos y contabilidad** \> **Periódico** \> **Integración de Project Operations** y seleccione **Importar desde tabla de almacenamiento provisional** para ejecutar el proceso periódico. Ese proceso utiliza los valores de dimensión financiera actualizados para volver a crear las líneas de propuesta de factura del proyecto. Los valores actualizados se utilizan en el libro mayor auxiliar y en el libro mayor general del proyecto cuando se registra la factura del proyecto.
