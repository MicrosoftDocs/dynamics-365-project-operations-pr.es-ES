---
title: Crear estimaciones sobre una línea de oferta
description: Este artículo proporciona información sobre cómo crear una estimación en una línea de oferta para un proyecto.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9f606ff2c33c46063f7025e8bc58e704d472061b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912583"
---
# <a name="create-estimates-on-a-quote-line"></a>Crear estimaciones sobre una línea de oferta

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En una oferta basada en proyecto, puede usar la entidad de detalles de línea de oferta para estimar el trabajo que se necesita para entregar un proyecto. A continuación, podrá compartir dicha estimación con el cliente.

Las líneas de oferta basadas en proyecto no tienen ningún detalle de línea de oferta. Como alternativa, pueden tener numerosos detalles de línea de oferta. Los detalles de línea de oferta se usan para estimar el tiempo, los gastos o las cuotas. Dynamics 365 Project Operations no permite las estimaciones de materiales en los detalles de línea de oferta. Estas se denominan clases de transacción. Los importes de Impuestos estimados también se pueden introducir en una clase de transacción.

Además de clases de transacciones, los detalles de línea de oferta tienen un tipo de transacción. Hay dos tipos de transacciones para los detalles de línea de oferta: **Coste** y **Contrato de proyecto**.

## <a name="estimate-by-using-a-contract"></a>Estimación mediante un contrato

Si utilizó una oferta de Project Operations cuando creó un contrato basado en proyecto, la estimación que hizo para cada línea de oferta de la oferta se copiará al contrato de proyecto. La estructura de un contrato de proyecto es como la estructura de la oferta del proyecto que tiene líneas, detalles de línea y programaciones de factura.

Las estimaciones se pueden realizar directamente en un contrato de proyecto como en una oferta de proyecto. Para una oferta del proyecto, la estimación se realiza mediante líneas de contrato y detalles de línea de contrato. Los detalles de líneas de contrato también se pueden generar a partir de un plan de proyecto que se haya creado utilizando el enfoque de estimación ascendente.

Los detalles de línea de contrato se pueden utilizar para estimar el tiempo, los gastos o las tarifas. Los importes de impuestos estimados también se pueden introducir en un detalle de línea de contrato.

No se permiten estimaciones de material en los detalles de línea de contrato.

Los procesos que se admiten en un contrato de proyecto son la confirmación y la creación de factura. La creación de factura crea un borrador de una factura basada en proyecto que incluye todos los datos reales de ventas sin facturar hasta la fecha actual.

La confirmación hace que el contrato sea de solo lectura y cambia su estado de **Borrador** a **Confirmado**. Tras realizar esta acción, no se puede deshacer. Como esta acción es permanente, se recomienda, como práctica recomendada, conservar el contrato con el estado **Borrador**.

Las únicas diferencias entre los contratos borrador y confirmados son los estados y el hecho de que los contratos borrador se pueden editar, mientras que los contratos confirmados no. La creación de facturas y el seguimiento de datos reales se puede realizar tanto en contratos borrador como en contratos confirmados.

No se permite cambiar pedidos en contratos o proyectos.

## <a name="estimating-projects"></a>Estimación de proyectos

Puede estimar el tiempo y los gastos de los proyectos, pero no materiales ni cuotas.

Las estimaciones de tiempo se generan cuando se crea una tarea y se identifican los atributos de un recurso genérico necesario para realizar la tarea. Las estimaciones de tiempo se generan a partir de tareas programadas. Las estimaciones de tiempo no se crean si crea miembros de equipo genéricos fuera del contexto de la programación.

Las estimaciones de gastos se introducen en la cuadrícula de la página **Estimaciones**.

## <a name="understand-estimation"></a>Información de una estimación

Use la siguiente tabla como guía para comprender la lógica de negocios de la fase de estimación.

| Escenario                                                                                                                                                                                                                                                                                                                                          | Registro de entidad                                                                                                                                                                                                       | Tipo de transacción | Clase de transacción | Información adicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Cuando se necesita estimar el valor de ventas del tiempo en una oferta                                                                                                                                                                                                                                                                                    | Se crea el registro de detalle de línea de oferta (QLD).                                                                                                                                                                               | Contrato de proyecto | Time        | El campo de origen de transacciones de la fila de QLD de ventas hace referencia al QLD de costes. |
|                                                                                                                                                                                                                                                                                     | El sistema crea un segundo registro de QLD para almacenar los valores de coste correspondientes. El sistema copia todos los campos no relacionados con el dinero del QLD de ventas al QLD de costes.                                                                                                                                                                               | Costo | Time        | El campo de origen de transacciones de la fila de detalle de la línea de oferta (QLD) de ventas hace referencia al QLD de costes. |
| Cuando se necesita estimar el valor de ventas del tiempo en un contrato                                                                                                                                                                                                                                                                                 | Se crea el registro de detalle de línea de contrato (CLD).                                                                                                                                                                    | Contrato de proyecto | Time        | El campo de origen de transacciones de la fila de CLD de ventas hace referencia al CLD de costes.      |
|                                                                                                                                                                                                                                                                                  | El sistema crea un segundo registro de CLD para almacenar los valores de coste correspondientes. El sistema copia todos los campos no relacionados con el dinero del CLD de ventas al CLD de costes.                                                                                                                                                                    | Costo | Time        | El campo de origen de transacciones de la fila de CLD de ventas hace referencia al CLD de costes.      |
| Cuando el usuario describe un recurso en una tarea de proyecto                                                                                                                                                                                                                                                                                            | Se crea el registro de la línea de estimación para mostrar el valor de ventas de la tarea cuando se crea una tarea con todas las dimensiones de precio necesarias. El rol y las unidades organizativas son las dimensiones de precio | Contrato de proyecto | Tiempo        |                                                                                   |
|     | Se crea el registro de la línea de estimación para mostrar el valor de coste de la tarea cuando se crea una tarea con todas las dimensiones de precio necesarias. El sistema copia todos los campos no relacionados con el dinero de la línea de estimación de ventas a la línea de estimación de costes. El rol y la unidad organizativa son las dimensiones de precios para las cuotas de coste y facturación.                                                                                                                                                                                                                | Coste             | Tiempo           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar las entidades de detalle de la línea de oferta y detalle de la línea de contrato

Si ha agregado un campo personalizado al detalle de la línea de oferta y desea que el sistema introduzca el valor del campo como valor predeterminado en la línea de coste relacionada que genera, use las herramientas de complementos de registro PreOperationContractLineDetailUpdate y PreOperationQuoteLineDetailUpdate. Estos complementos se deben registrar tras cambiar el detalle de la línea de oferta o el detalle de la línea de contrato. Siga los pasos que se indican a continuación para completar el proceso.

1. Abra PluginRegistrationTool y conéctese a su instancia en línea.
2. Seleccione **Buscar** y busque el complemento que desea actualizar.
3. Seleccione el complemento y después seleccione la opción **Seleccionar** en la página principal.
4. Seleccione el paso del complemento que desea actualizar, haga clic con el botón secundario y después seleccione **Actualizar**.
5. En el cuadro de diálogo **Actualizar paso existente**, en el campo **Atributos de filtro**, seleccione el botón de puntos suspensivos (**...**):
6. En el cuadro de diálogo **Seleccionar atributos**, active las casillas de verificación de los atributos personalizados.
7. Seleccione **Aceptar** para cerrar el cuadro de diálogo y después seleccione **Actualizar paso**.
8. Repita los pasos del 1 al 7 para el segundo complemento.
9. Cierre PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]