---
title: Transferir los presupuestos del proyecto al final de año fiscal
description: Este artículo proporciona información sobre cómo transferir los montos restantes del presupuesto a años futuros y cómo crear los detalles del registro presupuestario.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289750"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferir los presupuestos del proyecto al final de año fiscal

[!include [banner](../includes/banner.md)]

Cuando trabaje en un proyecto de varios años, es posible que tenga un presupuesto restante al final del año fiscal. Puede transferir los importes presupuestarios restantes a un año futuro y crear detalles de registro presupuestario para los importes en las cuentas del libro mayor asociadas. Antes de transferir los importes restantes, revise y analice los importes presupuestarios restantes.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Revisar y analizar los montos restantes del presupuesto

Complete los siguientes pasos para revisar los montos del presupuesto de fin de año para los proyectos, pero no traslade los montos.

1. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Presupuestos** > **Transferir presupuestos**. 
2. En la página **Proceso de arrastre del presupuesto del proyecto**, en la pestaña **Opciones de fin de año**, verifique que **Trasladar los importes restantes del presupuesto del proyecto** no está habilitado.
3. En la pestaña **Parámetros**, en el campo **Año presupuestario del proyecto**, seleccione el año fiscal para el que desea ver el monto del presupuesto restante. 
4. En el campo **Año fiscal de apertura**, seleccione el año fiscal para el que desea ver el monto del presupuesto restante. 
5. En el campo **Del modelo de pronóstico** campo, seleccione **Presupuesto restante**. 
6. Para incluir proyectos que cumplan con los criterios seleccionados y no tengan presupuesto restante, seleccione **Mostrar cero restante**.  
7. En la pestaña **Seleccionar presupuestos**, seleccione **Recuperar todos los presupuestos** para cargar todos los presupuestos que coincidan con los criterios seleccionados y luego seleccione **Proceso**. 
8. Para diseñar una consulta de base de datos que cargue un conjunto específico de presupuestos en el panel, seleccione **Recuperar presupuestos seleccionados**.

Para obtener más información sobre una línea específica en el panel, seleccione la línea y luego seleccione **Ver detalles del presupuesto** o **Ver cuentas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Trasladar los importes restantes del presupuesto 

Cuando procesa los importes restantes del presupuesto, puede crear transacciones en el libro mayor para los importes que está arrastrando. Para crear transacciones del libro mayor, complete los pasos en la sección, [Trasladar los importes del presupuesto y crear transacciones del libro mayor](#carry-forward). 

> [!NOTE]
> Los importes del presupuesto que se trasladan se transfieren al modelo de previsión que se selecciona en la página **Modelos de pronóstico** como modelo de pronóstico de arrastre.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Trasladar los importes del presupuesto y crear transacciones del libro mayor

1.  Seleccione **Gestión de proyectos y contabilidad** > **Periódico** > **Presupuestos** > **Transferir presupuestos**. 
2. En la página **Proceso de arrastre del presupuesto del proyecto**, seleccione **Fin de año** y luego habilite **Trasladar los importes restantes del presupuesto del proyecto** y **Crear asientos de registro presupuestario en el libro mayor**. 
3. En la pestaña **Parámetros**, en grupo de campo **Parámetros del proyecto**, seleccione lo siguiente:

   - **Año fiscal del proyecto**: seleccione el comienzo del año fiscal para el que desea ver las cantidades del presupuesto restante. 
   - **Ganancias y pérdidas**: cree transacciones de pérdidas y ganancias en el libro mayor. 
   -  **WIP**: cree transacciones de trabajo en curso (WIP) en el libro mayor.
   -  **Nómina**: cree transacciones de asignación de nómina en el libro mayor. 

5. En el grupo de campo **Libro de contabilidad general**, proporcione la siguiente información: 

   - En el campo **Año fiscal de apertura**, seleccione el año fisca al que desea trasferir las cantidades de presupuesto restantes para los proyectos. El valor predeterminado es un año después del valor en el campo **Año presupuestario del proyecto**.
   -  En el campo **Período de prórroga**, seleccione el período para el que desea crear los detalles del registro presupuestario en el libro mayor. Este suele ser el primer punto de la apertura año fiscal.

6. En el grupo de campo **Copiar de/a**, proporcione la siguiente información:

   - En el campo **Del modelo de pronóstico**, seleccione el modelo de previsión presupuestaria del proyecto asociado con los importes presupuestarios restantes que desea transferir para los proyectos. 
   - En el campo **Al modelo de presupuesto del libro de contabilidad**, seleccione el modelo de presupuesto del libro de contabilidad asociado con las cantidades de presupuesto que quiera transferir al libro de contabilidad general. 
   -  Seleccione **Transferir moneda de venta** para utilizar la moneda de venta del proyecto para las transacciones del libro mayor que se crean cuando transfiere los importes presupuestarios para los proyectos. Cuando no se selecciona la opción, las transacciones utilizan la moneda contable. 
   -  Seleccione **Mostrar cero restante** para incluir proyectos que no tienen montos presupuestarios restantes, pero que cumplen con los demás criterios que seleccione en los proyectos que se muestran en el panel inferior.

7. En la pestaña **Seleccionar presupuestos**, seleccione **Recuperar todos los presupuestos** para cargar todos los presupuestos que coincidan con los criterios que ha seleccionado. Si prefiere diseñar una consulta de base de datos que cargue un conjunto específico de presupuestos de proyecto en el panel, seleccione **Recuperar presupuestos seleccionados**.
8. Para cada proyecto que desee procesar, seleccione la opción al principio de la línea del proyecto.

    > [!TIP]
    > Para seleccionar todos o la mayoría de los proyectos, seleccione la marca de verificación en la esquina superior izquierda. Para excluir el procesamiento de cualquier proyecto, desactive la marca de verificación de ese proyecto.

9. Para transferir los importes presupuestarios restantes para los proyectos seleccionados al año fiscal seleccionado y crear detalles de registro presupuestario en el libro mayor, seleccione **Proceso**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Trasladar los importes del presupuesto sin crear transacciones del libro mayor

1. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Presupuestos** > **Transferir presupuestos**.
2. En la página **Proceso de arrastre del presupuesto del proyecto**, en el campo **Opciones de fin de año**, seleccione **Trasladar los importes restantes del presupuesto del proyecto**.
3. En el grupo **Parámetros**, en el campo **Año presupuestario del proyecto**, seleccione el año fiscal para el que desea ver las cantidades del presupuesto restante.
4. En el grupo **Copiar de/a**, proporcione la siguiente información:

   - En el campo **Del modelo de pronóstico**, seleccione el modelo de previsión presupuestaria del proyecto asociado con los importes presupuestarios restantes que desea transferir para los proyectos. 
   - Seleccione **Mostrar cero restante** para incluir proyectos que no tengan cantidades de presupuesto restante pero cumplan los otros criterios que ha seleccionado.
   - En el grupo **Seleccionar presupuestos**, seleccione **Recuperar todos los presupuestos** para cargar todos los presupuestos que coincidan con los criterios que ha seleccionado. Para diseñar una consulta de base de datos que cargue un conjunto específico de presupuestos de proyecto en el panel, seleccione **Recuperar presupuestos seleccionados**.

5. Para cada proyecto que desee procesar, seleccione la opción al principio de la línea del proyecto. 
6. Seleccione **Proceso** para transferir los importes restantes del presupuesto de los proyectos seleccionados al año fiscal seleccionado.



[!INCLUDE[footer-include](../includes/footer-banner.md)]