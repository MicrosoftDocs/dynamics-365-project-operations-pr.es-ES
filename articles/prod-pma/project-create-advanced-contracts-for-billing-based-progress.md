---
title: Crear contratos avanzados para la facturación según el progreso
description: Este tema explica cómo crear contratos de proyecto para que pueda generar facturas para los clientes, basadas en un porcentaje del trabajo completado.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289525"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Crear contratos avanzados para la facturación según el progreso
[!include [banner](../includes/banner.md)]

Este tema explica cómo crear contratos de proyecto para que pueda crear facturas para los clientes, basadas en un porcentaje del trabajo completado. Los importes de las facturas se calculan automáticamente para las categorías presupuestarias de trabajo que configura para un proyecto. El tiempo de facturación se establece cuando negocia el contrato del proyecto con el cliente.

Utilice los procedimientos de este tema para configurar un contrato, un proyecto asociado y las reglas de facturación que calculan los importes de las facturas para las categorías presupuestarias de trabajo que configuró para el proyecto.

Una vez que haya creado el contrato y el proyecto, puede configurar los detalles del proyecto. Por ejemplo, puede definir actividades y asignar trabajadores al proyecto.

## <a name="example"></a>Ejemplo

Su organización es una empresa de desarrollo de software. Acepta desarrollar un paquete de contabilidad de nómina para un cliente por una tarifa total de 20 000 dólares estadounidenses (USD). Su organización acepta facturar al cliente a medida que complete porcentajes específicos del proyecto. Configura las siguientes categorías de proyectos para el trabajo, de modo que pueda utilizarlas en el proceso de facturación:

- Consultoría
- Diseño
- Instalación

También configura reglas de facturación que calculan automáticamente los importes de la factura para el porcentaje de trabajo del proyecto completado en cada categoría.

El director de presupuesto crea un presupuesto para las categorías de proyectos. La cantidad de trabajo completado se calcula automáticamente como un porcentaje del trabajo real en comparación con las cantidades presupuestadas.

## <a name="prerequisites"></a>Requisitos previos

Antes de crear un proyecto que usa reglas de facturación, debe configurar las secuencias de números para las reglas de facturación y un diario de tarifas que se usa para registrar el progreso de la facturación.

1. Vaya a **Gestión y contabilidad de proyectos** \> **Configuración** \> **Parámetros de gestión de proyectos y contabilidad**.
2. Sobre la página **Parámetros contables y de gestión de proyectos**, en la pestaña **Secuencias numéricas** , configure la secuencia numérica que desea utilizar cuando se crean las reglas de facturación.
3. Vaya a **Gestión de proyectos y contabilidad** \> **Diarios** \> **Precio**.
4. En la página **Diario de tarifas**, seleccione **Nuevo** e ingrese el nombre del diario.

## <a name="create-a-contract-for-progress-billings"></a>Crear un contrato para facturación progresiva

Utilice este procedimiento para crear un contrato de proyecto para un proyecto de precio fijo. Usted crea una factura de proyecto cuando el trabajo que se completa en el proyecto alcanza un porcentaje específico.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Contratos de proyecto**.
2. En la página **Contratos de proyecto**, seleccione **Nuevo**.
3. En el cuadro de diálogo **Nuevo contrato de proyecto**, establezca los siguientes campos:

    - **Nombre**
    - **Tipo de financiación**
    - **Fuente de financiación**
    - **Moneda de venta**: de forma predeterminada, esta moneda se usa para las facturas de clientes que están asociadas con el contrato del proyecto. Sin embargo, puede cambiar la moneda de venta en una factura de cliente específica.

4. Seleccione **Aceptar**. La información se copia en el encabezado de la página **Contratos de proyecto**.
5. En la página **Contratos de proyecto**, complete el resto de la información requerida para el proyecto.

## <a name="create-a-project-for-progress-billings"></a>Crear un proyecto para facturación progresiva

Siga estos pasos para crear un proyecto y cualquier subproyecto que esté asociado con un contrato de proyecto.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos**.
2. En la página de **Todos los proyectos**, seleccione **Nuevo**.
3. En el cuadro de diálogo **Nuevo proyecto**, en el campo **Tipo de proyecto**, seleccione **Tiempo y material**.
4. Seleccione un grupo de proyecto. Un grupo de proyectos define la información de publicación de los proyectos asignados al grupo.
5. Seleccione **Crear proyecto**.
6. Una vez creado el proyecto, configure la etapa del proyecto en **En proceso**.

## <a name="create-a-budget-for-a-project"></a>Creación de un presupuesto para un proyecto

Las categorías de presupuesto calculan automáticamente los importes de la factura para el porcentaje de trabajo completado para cada categoría. Siga estos pasos para crear categorías presupuestarias para los costos estimados.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Todos los proyectos**.
2. En la página **Todos los proyectos**, seleccione y abra el proyecto que desee.
3. En la página **Proyectos**, en el panel de acciones, en la pestaña **Plan**, en el grupo **Presupuesto**, haga clic en **Presupuesto del proyecto**.
4. En la página **Presupuesto del proyecto**, introduzca un costo estimado para cada categoría en el proyecto.

## <a name="create-billing-rules-for-progress-billings"></a>Crear reglas de facturación para facturación progresiva

1. Vaya a **Gestión de proyectos y contabilidad** \> **Proyectos** \> **Contratos de proyecto**.
2. En la página de lista **Contratos de proyecto**, seleccione y abra un contrato de proyecto.
3. En la página del contrato del proyecto, en la ficha desplegable **Reglas de facturación**, seleccione **Agregar**.
4. En la página **Regla de facturación**, en el campo **Tipo de línea** , seleccione **Progreso**.
5. En la ficha desplegable **Detalles de la línea de la regla de facturación**, en el campo **Valor del contrato**, introduzca el valor total del contrato.
6. En el campo **Categoría**, seleccione la categoría para publicar la transacción de tarifa.
7. En el campo **Proyecto**, seleccione el proyecto que utiliza esta regla de facturación.
8. Opcional: asigne la regla de facturación a proyectos adicionales. En la ficha desplegable **Proyecto**, en la sección **Proyectos disponibles**, seleccione un proyecto y luego seleccione el botón de flecha derecha para agregar el proyecto a la sección **Proyectos seleccionados**.
9. Opcional: calcule el porcentaje que el cliente retiene de los pagos de una factura. En la ficha desplegable **Condiciones de retención de pagos**, seleccione la fuente de financiación y, a continuación, en el campo **Porcentaje de retención**, introduzca el porcentaje de retención.
10. Repita estos pasos para crear reglas de facturación adicionales para el contrato del proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]