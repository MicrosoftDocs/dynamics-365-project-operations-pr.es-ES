---
title: Correcciones masivas de datos reales creados por entradas de gastos y tiempo aprobadas
description: En este tema se explica de qué manera un administrador puede hacer correcciones únicas o masivas a entradas de tiempo o gastos previamente aprobadas si la facturación no está completa.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085324"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Correcciones masivas de datos reales creados por entradas de gastos y tiempo aprobadas

Ocasionalmente, se puede introducir incorrectamente una entrada de tiempo o gasto. Por ejemplo, un consultor puede seleccionar la fecha incorrecta al crear una entrada de tiempo o puede transponer los números al introducir un gasto. Si un consultor no puede realizar las actualizaciones de las entradas enviadas, un administrador puede corregir directamente la entrada de un proyecto.

Para completar los procedimientos en este tema, necesitará permisos de Administrador.

## <a name="correct-approved-time-entries"></a>Corregir entradas de tiempo aprobadas     

Complete los siguientes pasos para corregir entradas de tiempo únicas o múltiples para un proyecto.

1. En el área **Ventas** , seleccione **Transacciones** y luego seleccione **Tiempo aprobado**. 

2. En la lista **Tiempo aprobado** , encuentra y seleccione una o más entradas de tiempo aprobadas para corregir. Puede usar el filtro para encontrar entradas relacionadas. Por ejemplo, puede filtrar por un id. de proyecto y seleccionar todas las entradas de tiempo aprobadas con ese id. de proyecto.

3. Seleccione **Corregir entradas**. Se crea automáticamente un nuevo diario de corrección, con el tipo asignado **Corrección de tiempo**. Las entradas que seleccionó se agregan al diario. 

4. En la página **Nuevo diario** , introduzca una **Descripción** para su diario de corrección y luego seleccione la pestaña **Correcciones de entradas de tiempo**.  
5. En la sección **Nuevos valores de entradas de tiempo** , actualice los campos con la información correcta según sea necesario. Por ejemplo, puede cambiar el proyecto asignado o el recurso que se puede reservar.

6. Seleccione **Vista previa**. En el cuadro de diálogo, seleccione **Aceptar**. En la pestaña **Líneas de diario** , puede ver una lista de los datos reales originales que están relacionados con las entradas de tiempo seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado. Si es necesario realizar correcciones adicionales, repita los pasos 5 y 6. 

> [!NOTE]
> Todos los datos reales corregidos tendrán los mismos valores que seleccionó en la sección **Nuevos valores de entradas de tiempo**.

7. Si las correcciones aparecen como se espera, seleccione **Confirmar**. En el cuadro de diálogo, seleccione **Aceptar**.

8. Vuelva al área **Ventas** , seleccione **Proyectos** y luego abra el proyecto para el que acaba de actualizar las entradas de tiempo. 

9. En la página **Proyectos** , en la pestaña **Datos reales** , vea los cambios que ha realizado. 

> [!NOTE]
> Si la pestaña **Datos reales** no está visible, seleccione **Relacionado** > **Datos reales**.  

10. En la lista **Vista asociada real** , puede ver que las entradas de tiempo originales que se han revertido todavía se muestran, al igual que las entradas de tiempo corregidas correspondientes. 

Por ejemplo, en el siguiente gráfico, hay dos elementos de línea con una cantidad de 8,00 que tienen débitos en la columna Cantidad. Además, hay dos elementos de línea con una cantidad de -8,00 que muestran los importes abonados en la columna Importe. Estas correcciones lleva la cantidad a cero.

![Lista de vista asociada de datos reales](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Corregir entradas de gasto aprobadas

Complete los siguientes pasos para corregir una o más entradas de gastos. 

1. En el área **Ventas** , en el panel de navegación izquierdo, debajo de **Transacciones** , seleccione **Gastos aprobados**.

2. En la lista **Gastos aprobados** , seleccione el proyecto que desea corregir y luego seleccione **Corregir entradas**. Se creará automáticamente un nuevo diario de corrección, con el tipo asignado de **Corrección de gastos**. 

3. En la página **Nuevo diario** , introduzca una **Descripción** para la corrección y, en la pestaña **Corrección de gastos** , en la sección **Nuevos valores para los gastos** , seleccione los campos de datos que desea corregir para las líneas de gastos seleccionadas. Por ejemplo, puede asignar el gasto a otro **Proyecto** o corregir la **Categoría de gastos** , la **Fecha del gasto** o el **Recurso que se puede reservar**.

4. Seleccione **Vista previa**. En el cuadro de diálogo, seleccione **Aceptar**. 

5. Compruebe las correcciones en la pestaña **Líneas de diario**. Puede ver una lista de los datos reales originales que están relacionados con las entradas de gasto seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado.

6. Si los valores corregidos aparecen como se espera, seleccione **Confirmar**. En el cuadro de diálogo, seleccione **Aceptar**. Si los valores no se muestran según lo previsto, seleccione **Cancelar** para volver a la lista **Gastos aprobados**. Repita los pasos del 2 al 5. 

> [!NOTE]
> Los datos reales corregidos tendrán los mismos valores que seleccionó en la sección **Nuevos valores para los gastos**.

7. Después de confirmar el diario de corrección, vuelva al proyecto o proyectos que ha actualizado, para ver sus cambios.  

8. En la página del proyecto, en la pestaña **Datos reales** , revise la **Vista asociada de datos reales**. Se enumeran las entradas originales y las entradas corregidas. En el siguiente gráfico se muestran los importes de entrada de gastos originales y los importes de entrada de gastos corregidos correspondientes. 

![Datos reales de gastos](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)