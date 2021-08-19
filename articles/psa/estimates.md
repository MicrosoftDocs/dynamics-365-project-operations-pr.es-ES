---
title: Estimaciones
description: En este tema se proporciona información sobre las estimaciones de Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ebb59d2b38bf99aed15206646e77c74003aba2a92a6d8d262e6e7b2017285ed3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992407"
---
# <a name="estimates"></a>Estimaciones

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En una oferta basada en proyecto, puede usar la entidad de detalles de línea de oferta para estimar el trabajo que se necesita para entregar un proyecto. A continuación, podrá compartir dicha estimación con el cliente.

Las líneas de oferta basadas en proyecto no tienen ningún detalle de línea de oferta. Como alternativa, pueden tener numerosos detalles de línea de oferta. Los detalles de línea de oferta se usan para estimar el tiempo, los gastos o las cuotas. PSA no permite las estimaciones de materiales en los detalles de línea de oferta. Estas se denominan clases de transacción. Los importes de Impuestos estimados también se pueden introducir en una clase de transacción.

Además de clases de transacciones, los detalles de línea de oferta tienen un tipo de transacción. PSA admite dos tipos de transacciones para los detalles de línea de oferta: **Coste** y **Contrato de proyecto**.

## <a name="estimate-by-using-a-contract"></a>Estimación mediante un contrato

Si utilizó una oferta de PSA cuando creó un contrato basado en proyecto, la estimación que hizo para cada línea de oferta de la oferta se copiará al contrato de proyecto. La estructura de un contrato de proyecto es como la estructura de la oferta del proyecto que tiene líneas, detalles de línea y programaciones de factura.

Las estimaciones se pueden realizar directamente en un contrato de proyecto como en una oferta de proyecto. Para una oferta del proyecto, la estimación se realiza mediante líneas de contrato y detalles de línea de contrato. Los detalles de líneas de contrato también se pueden generar a partir de un plan de proyecto que se haya creado utilizando el enfoque de estimación ascendente.

Los detalles de línea de contrato se pueden utilizar para estimar el tiempo, los gastos o las tarifas. Los importes de impuestos estimados también se pueden introducir en un detalle de línea de contrato.

PSA no permite las estimaciones de materiales en los detalles de línea de contrato.

Los procesos que se admiten en un contrato de proyecto son la confirmación y la creación de factura. La creación de factura crea un borrador de una factura basada en proyecto que incluye todos los datos reales de ventas sin facturar hasta la fecha actual.

La confirmación hace que el contrato sea de solo lectura y cambia su estado de **Borrador** a **Confirmado**. Tras realizar esta acción, no se puede deshacer. Como esta acción es permanente, se recomienda, como práctica recomendada, conservar el contrato con el estado **Borrador**.

Las únicas diferencias entre los contratos borrador y confirmados son los estados y el hecho de que los contratos borrador se pueden editar, mientras que los contratos confirmados no. La creación de facturas y el seguimiento de datos reales se puede realizar tanto en contratos borrador como en contratos confirmados.

PSA no permite cambiar los pedidos de contratos o proyectos.

## <a name="estimating-projects"></a>Estimación de proyectos

Puede estimar el tiempo y los gastos en los proyectos. PSA no permite realizar estimaciones de materiales o cuotas en los proyectos.

Las estimaciones de tiempo se generan cuando se crea una tarea y se identifican los atributos de un recurso genérico necesario para realizar la tarea. Las estimaciones de tiempo se generan a partir de tareas programadas. Las estimaciones de tiempo no se crean si crea miembros de equipo genéricos fuera del contexto de la programación.

Las estimaciones de gastos se introducen en la cuadrícula de la página **Estimaciones**.

## <a name="understanding-estimation"></a>Concepto de estimación

Use la siguiente tabla como guía para comprender la lógica de negocios de la fase de estimación.

| Escenario                                                                                                                                                                                                                                                                                                                                          | Registro de entidad                                                                                                                                                                                                       | Tipo de transacción | Clase de transacción | Información adicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Cuando se necesita estimar el valor de ventas del tiempo en una oferta                                                                                                                                                                                                                                                                                    | Se crea el registro de detalle de línea de oferta (QLD).                                                                                                                                                                               | Contrato de proyecto | Time        | El campo de origen de transacciones de la fila de QLD de ventas hace referencia al QLD de costes. |
|                                                                                                                                                                                                                                                                                     | El sistema crea un segundo registro de QLD para almacenar los valores de coste correspondientes. El sistema copia todos los campos no relacionados con el dinero del QLD de ventas al QLD de costes.                                                                                                                                                                               | Costo | Time        | El campo de origen de transacciones de la fila de detalle de la línea de oferta (QLD) de ventas hace referencia al QLD de costes. |
| Cuando se necesita estimar el valor de ventas del tiempo en un contrato                                                                                                                                                                                                                                                                                 | Se crea el registro de detalle de línea de contrato (CLD).                                                                                                                                                                    | Contrato de proyecto | Time        | El campo de origen de transacciones de la fila de CLD de ventas hace referencia al CLD de costes.      |
|                                                                                                                                                                                                                                                                                  | El sistema crea un segundo registro de CLD para almacenar los valores de coste correspondientes. El sistema copia todos los campos no relacionados con el dinero del CLD de ventas al CLD de costes.                                                                                                                                                                    | Costo | Time        | El campo de origen de transacciones de la fila de CLD de ventas hace referencia al CLD de costes.      |
| Cuando el usuario describe un recurso en una tarea de proyecto                                                                                                                                                                                                                                                                                            | Se crea el registro de la línea de estimación para mostrar el valor de ventas de la tarea cuando se crea una tarea con todas las dimensiones de precio necesarias. El rol y las unidades organizativas son las dimensiones de precio de OOB de Project Service. | Contrato de proyecto | Time        |                                                                                   |
|     | Se crea el registro de la línea de estimación para mostrar el valor de coste de la tarea cuando se crea una tarea con todas las dimensiones de precio necesarias. El sistema copia todos los campos no relacionados con el dinero de la línea de estimación de ventas a la línea de estimación de costes. El rol y la unidad organizativa son las dimensiones de precios de OOB de PSA para las cuotas de coste y facturación.                                                                                                                                                                                                                | Costo             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalización de las entidades de detalle de la línea de oferta y detalle de la línea de contrato

Si ha agregado un campo personalizado al detalle de la línea de oferta y desea que el sistema introduzca el valor del campo como valor predeterminado en la línea de coste relacionada que genera, use las herramientas de complementos de registro PreOperationContractLineDetailUpdate y PreOperationQuoteLineDetailUpdate. Estos complementos se deben registrar tras cambiar el detalle de la línea de oferta o el detalle de la línea de contrato. Siga los pasos que se indican a continuación para completar el proceso.

1. Abra PluginRegistrationTool y conéctese a su instancia en línea.
2. Seleccione **Buscar** y busque el complemento que desea actualizar.

    ![Cuadro de diálogo de árbol de búsqueda.](media/basic-guide-19.png)

3. Seleccione el complemento y después seleccione la opción **Seleccionar** en la página principal.
4. Seleccione el paso del complemento que desea actualizar, haga clic con el botón secundario y después seleccione **Actualizar**.

    ![Selección de un paso en el complemento.](media/basic-guide-20.png)

5. En el cuadro de diálogo **Actualizar paso existente**, en el campo **Atributos de filtro**, seleccione el botón de puntos suspensivos (**...**):
 
    ![Cuadro de diálogo de actualización del paso existente.](media/basic-guide-21.png)

6. En el cuadro de diálogo **Seleccionar atributos**, active las casillas de verificación de los atributos personalizados.

    ![Cuadro de diálogo Seleccionar atributos.](media/basic-guide-22.png)

7. Seleccione **Aceptar** para cerrar el cuadro de diálogo y después seleccione **Actualizar paso**.
 
    ![Botón Actualizar paso.](media/basic-guide-23.png)

8. Repita los pasos del 1 al 7 para el segundo complemento.
9. Cierre PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]