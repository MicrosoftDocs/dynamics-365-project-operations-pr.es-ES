---
title: Corregir la contabilidad en propuestas de factura de proyecto en borrador
description: Este tema explica cómo ajustar la información relacionada con la contabilidad en un borrador de propuesta de factura.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251279"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corregir la contabilidad en propuestas de factura de proyecto en borrador

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

El administradior del proyecto mantiene los *Detalles de operaciones* para las facturas del mismo en una factura proforma. Estos detalles incluyen la decisión sobre las horas, gastos, materiales o hitos que se deben facturar, las tarifas y la aplicación de los importes de anticipos y avances. Después de confirmar la factura proforma original, puede ajustar los detalles de operaciones creando y confirmando una [factura proforma correctiva](../proforma-invoicing/corrective-invoices.md).

Los *Detalles de contabilidad* para las facturas del proyecto se mantienen en un documento de factura de cara al cliente. Estos detalles incluyen el cálculo del impuesto sobre las ventas y las dimensiones financieras que se aplican a la factura. Este tema proporciona detalles sobre cómo se pueden ajustar estos detalles de contabilidad en un borrador de propuesta de factura de proyecto.

## <a name="adjust-sales-tax"></a>Ajustar el impuesto de ventas

Los grupos de impuestos sobre las ventas de facturación predeterminados y los grupos de impuestos sobre las ventas de artículos se pueden ajustar directamente en el documento de propuesta de factura. Para ajustar estos grupos, seleccione **Editar** y luego, en cada línea de propuesta de factura de proyecto, introduzca un nuevo valor en los campos **Grupo de impuestosç** o **Grupos de impuestos de artículos**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensiones financieras

Las dimensiones financieras no se pueden editar directamente en una línea de propuesta de factura de proyecto. En su lugar, siga estos pasos para ajustar las dimensiones financieras en una propuesta de factura de proyecto.

1. En la propuesta de factura del proyecto, seleccione **Eliminar todo** para eliminar las líneas de propuesta de factura del proyecto.

    > [!NOTE]
    > El botón **Eliminar todo** está disponible solo después de que el administrador del sistema habilite la característica **Eliminar las líneas de propuesta de factura cuando utilice Project Operations para escenarios basados en recursos/sin existencias** en el área de trabajo **Administración de características**.

2. Ajustar dimensiones financieras:

    - **Transacciones a cuenta (hitos de facturación):** vaya a **Todos los proyectos** \> **Administrar** \> **Transacciones a cuenta** y seleccione el hito que necesite ajuste. Después, en la pestaña **Dimensiones financieras**, actualice los valores según sea necesario.
    - **Transacciones de tiempo, gastos y materiales:** en la página **Transacciones de proyecto registradas**, seleccione **Ajustar la contabilidad** para actualizar las dimensiones financieras.

3. Una vez que haya terminado de ajustar los valores de la dimensión financiera, vaya a **Administración de proyectos y contabilidad** \> **Periódico** \> **Integración de Project Operations** y seleccione **Importar desde tabla de almacenamiento provisional** para ejecutar el proceso periódico. Ese proceso utiliza los valores de dimensión financiera actualizados para volver a crear las líneas de propuesta de factura del proyecto. Los valores actualizados se utilizan en el libro mayor auxiliar y en el libro mayor general del proyecto cuando se registra la factura del proyecto.
