---
title: Crear y confirmar diarios de corrección
description: Este artículo proporciona información sobre cómo crear y confirmar un diario de corrección.
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
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928085"
---
# <a name="create-and-confirm-correction-journals"></a>Crear y confirmar diarios de corrección

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Ocasionalmente, una entrada de tiempo o gasto puede ingresarse incorrectamente. Por ejemplo, un consultor puede seleccionar una fecha incorrecta cuando crea una entrada de tiempo, o puede seleccionar un proyecto incorrecto cuando ingresa un gasto. Si un consultor no puede actualizar las entradas enviadas, un administrador de back-end puede corregir directamente los datos reales de un proyecto.

## <a name="correct-approved-time-entries"></a>Corregir entradas de tiempo aprobadas     

Complete los siguientes pasos para corregir entradas de tiempo únicas o múltiples para un proyecto.

1. En el área **Ventas**, seleccione **Transacciones** y luego seleccione **Tiempo aprobado**. 

2. En la lista **Tiempo aprobado**, encuentra y seleccione una o más entradas de tiempo aprobadas para corregir. Puede usar el filtro para encontrar entradas relacionadas. Por ejemplo, puede filtrar por un id. de proyecto y seleccionar todas las entradas de tiempo aprobadas con ese id. de proyecto.

3. Seleccione **Corregir entradas**. Se crea automáticamente un nuevo diario de corrección, con el tipo asignado **Corrección de tiempo**. Las entradas que seleccionó se agregan al diario. 

4. En la página **Nuevo diario**, introduzca una **Descripción** para su diario de corrección y luego seleccione la pestaña **Correcciones de entradas de tiempo**.  

5. En la sección **Nuevos valores de entradas de tiempo**, actualice los campos con la información correcta según sea necesario. Por ejemplo, puede cambiar el proyecto asignado o el recurso que se puede reservar.

6. Seleccione **Vista previa**. En el cuadro de diálogo, seleccione **Aceptar**. En la pestaña **Líneas de diario**, puede ver una lista de los datos reales originales que están relacionados con las entradas de tiempo seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado. Si es necesario realizar correcciones adicionales, repita los pasos 5 y 6. 

    > [!NOTE]
    > Todos los datos reales corregidos tendrán los mismos valores que seleccionó en la sección **Nuevos valores de entradas de tiempo**.

7. Si las correcciones aparecen como se espera, seleccione **Confirmar**. En el cuadro de diálogo, seleccione **Aceptar**.

8. Vuelva al área **Ventas**, seleccione **Proyectos** y luego abra el proyecto para el que acaba de actualizar las entradas de tiempo. 

9. En la página **Proyectos**, en la pestaña **Datos reales**, vea los cambios que ha realizado. 

    > [!NOTE]
    > Si la pestaña **Datos reales** no está visible, seleccione **Relacionado** > **Datos reales**.  

10. En la lista **Vista asociada real**, puede ver que las entradas de tiempo originales que se han revertido todavía se muestran, al igual que las entradas de tiempo corregidas correspondientes. 

 
## <a name="correct-approved-expense-entries"></a>Corregir entradas de gasto aprobadas

Complete los siguientes pasos para corregir una o más entradas de gastos. 

1. En el área **Ventas**, en el panel de navegación izquierdo, debajo de **Transacciones**, seleccione **Gastos aprobados**.

2. En la lista **Gastos aprobados**, seleccione el proyecto que desea corregir y luego seleccione **Corregir entradas**. Se creará automáticamente un nuevo diario de corrección, con el tipo asignado de **Corrección de gastos**. 

3. En la página **Nuevo diario**, introduzca una **Descripción** para la corrección y, en la pestaña **Corrección de gastos**, en la sección **Nuevos valores para los gastos**, seleccione los campos de datos que desea corregir para las líneas de gastos seleccionadas. Por ejemplo, puede asignar el gasto a otro **Proyecto** o corregir la **Categoría de gastos**, la **Fecha del gasto** o el **Recurso que se puede reservar**.

4. Seleccione **Vista previa**. En el cuadro de diálogo, seleccione **Aceptar**. 

5. Compruebe las correcciones en la pestaña **Líneas de diario**. Puede ver una lista de los datos reales originales que están relacionados con las entradas de gasto seleccionadas que se han revertido y las líneas correspondientes corregidas que se han creado.

6. Si los valores corregidos aparecen como se espera, seleccione **Confirmar**. En el cuadro de diálogo, seleccione **Aceptar**. Si los valores no se muestran según lo previsto, seleccione **Cancelar** para volver a la lista **Gastos aprobados**. Repita los pasos del 2 al 5. 

7. Después de confirmar el diario de corrección, regrese al proyecto o a los proyectos que actualizó para ver sus cambios.

8. En la página del proyecto, en la pestaña **Datos reales**, revise la pestaña **Vista asociada real**. Se enumeran las entradas originales y las entradas corregidas.


## <a name="correct-approved-material-usage-logs"></a>Corrija los registros de uso de materiales aprobados

Complete los siguientes pasos para corregir una o más entradas de registros de uso de material.

1. En el área **Ventas**, en el panel de navegación izquierdo, en **Transacciones**, seleccione **Datos reales**.

2. En la lista **Datos reales**, use filtros de columna para seleccionar la clase de transacción **Material**, de modo que solo se muestren los datos reales de los materiales. Utilice otros filtros de columna para limitar aún más los datos reales que se muestran. Una vez que pueda encontrar el conjunto deseado de datos reales, seleccione los datos reales y, a continuación, seleccione **Entradas correctas**. Se crea automáticamente un nuevo diario de corrección y se asigna el tipo **Corrección de materiales**.

3. En la página **Nuevo diario**, en el campo **Descripción**, introduzca una descripción de la corrección. Entonces, en la pestaña **Corrección de materiales**, en la sección **Nuevos valores para materiales**, seleccione los campos de datos a corregir para las líneas de material seleccionadas. Por ejemplo, puede asignar el material a otro proyecto o corregir el producto, la fecha del material o el subcontrato.

4. Seleccione **Vista previa**. Luego, en el cuadro de diálogo, seleccione **Aceptar**.

5. En la pestaña **Líneas de diario**, verifique las correcciones. Puede ver una lista de los datos reales originales relacionados con las entradas de material seleccionadas que se han anulado y las líneas correspondientes corregidas que se han creado.

6. Si los valores corregidos aparecen como se espera, seleccione **Confirmar**. Luego, en el cuadro de diálogo, seleccione **Aceptar**. Si los valores no son los esperados, seleccione **Cancelar** para volver a la lista **Datos reales**. A continuación, repita los pasos 2 a 5.

7. Después de confirmar el diario de corrección, regrese al proyecto o a los proyectos que actualizó para ver sus cambios.

8. En la página del proyecto, en la pestaña **Datos reales**, revise la pestaña **Vista asociada real**. Se enumeran las entradas originales y las entradas corregidas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
