---
title: Conceptos de estimación financiera
description: Este tema proporciona información sobre la estimación financiera de proyectos en Project Operations.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a251be995abddba04cee689714d0a8f4e9d9e7d7
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701757"
---
# <a name="financial-estimation-concepts"></a>Conceptos de estimación financiera

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En Dynamics 365 Project Operations, puede estimar financieramente sus proyectos en dos etapas: 
1. Durante la etapa de preventa antes de que se cierre el trato. 
2. Durante la etapa de ejecución posterior a la creación del contrato del proyecto. 

Puede crear una estimación financiera para el trabajo basado en proyectos utilizando cualquiera de las siguientes 3 páginas:
- La página **Línea de cotización**, utilizando los detalles de la línea de cotización.  
- La página **Línea de contrato del proyecto**, utilizando los detalles de la línea de contrato. 
- La página **Proyecto**, usando las páginas de las pestañas **Tareas** o **Estimaciones de gastos**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Utilizar una cotización de proyecto para crear una estimación
En una oferta basada en proyecto, puede usar la entidad **Detalle de línea de oferta** para estimar el trabajo que se necesita para entregar un proyecto. A continuación, podrá compartir dicha estimación con el cliente.

Las líneas de oferta basadas en proyecto pueden tener de cero a muchos detalles de línea de oferta. Los detalles de línea de oferta se usan para estimar el tiempo, los gastos o las cuotas. Microsoft Dynamics 365 Project Operations no permite las estimaciones de materiales en los detalles de línea de oferta. Estas se denominan clases de transacción. Los importes de Impuestos estimados también se pueden introducir en una clase de transacción.

Además de clases de transacciones, los detalles de línea de oferta tienen un tipo de transacción. Se admite dos tipos de transacciones para los detalles de línea de oferta: **Coste** y **Contrato de proyecto**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Utilizar un contrato de proyecto para crear una estimación

Si utilizó una oferta cuando creó un contrato basado en proyecto, la estimación que hizo para cada línea de oferta de la oferta se copiará al contrato de proyecto. La estructura de un contrato de proyecto es como la estructura de la oferta del proyecto que tiene líneas, detalles de línea y programaciones de factura.

Las estimaciones se pueden realizar directamente en un contrato de proyecto como en una oferta de proyecto. Para una oferta del proyecto, la estimación se realiza mediante líneas de contrato y detalles de línea de contrato. Los detalles de línea de contrato también se pueden generar a partir de un plan de proyecto que se creó utilizando el enfoque de estimación de abajo a arriba.

Los detalles de línea de contrato se pueden usar para estimar el tiempo, los gastos o las cuotas. Los importes de impuestos estimados también se pueden introducir en un detalle de línea de contrato.

No se permite estimaciones de materiales en los detalles de línea de contrato.

## <a name="use-a-project-to-create-an-estimate"></a>Utilizar un proyecto para crear una estimación 

Puede estimar el tiempo y los gastos en los proyectos. Project Operations no admite estimaciones de materiales o tarifas de proyectos.

Las estimaciones de tiempo se generan cuando se crea una tarea y se identifican los atributos de un recurso genérico necesario para realizar la tarea. Las estimaciones de tiempo se generan a partir de tareas de programación. Las estimaciones de tiempo no se generan si crea los miembros del equipo genéricos fuera del contexto de la programación.

Las estimaciones de gastos se introducen en la cuadrícula de la página **Estimaciones de gastos**.

La creación de una estimación para un proyecto se considera una mejor práctica porque puede generar estimaciones detalladas de abajo a arriba para la mano de obra o el tiempo y los gastos en cada tarea en el plan del proyecto. Luego, puede utilizar esta estimación detallada para crear estimaciones para cada línea de cotización y crear una cotización más creíble para el cliente. Cuando importa o crea una estimación detallada en la línea de cotización utilizando el plan del proyecto, Project Operations importa los valores de ventas y los valores de coste de estas estimaciones. Después de la importación, puede ver la rentabilidad, los márgenes y las métricas de viabilidad en la cotización del proyecto.

## <a name="understanding-estimates"></a>Concepto de estimación

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

Si ha agregado un campo personalizado al detalle de la línea de oferta y desea que el sistema introduzca el valor del campo como valor predeterminado en la línea de coste relacionada que genera, use las herramientas de complementos de registro **PreOperationContractLineDetailUpdate** y **PreOperationQuoteLineDetailUpdate**. Estos complementos se deben registrar tras cambiar el detalle de la línea de oferta o el detalle de la línea de contrato. Siga los pasos que se indican a continuación para completar el proceso.

1. Abra PluginRegistrationTool y conéctese a su instancia en línea.
2. Seleccione **Buscar** y busque el complemento que desea actualizar.
3. Seleccione el complemento y después haga clic en **Seleccionar** en la página principal.
4. Seleccione el paso del complemento que desea actualizar, haga clic con el botón secundario y después seleccione **Actualizar**.
5. En el cuadro de diálogo **Actualizar paso existente**, en el campo **Atributos de filtro**, seleccione el botón de puntos suspensivos (**...**):
6. En el cuadro de diálogo **Seleccionar atributos**, active las casillas de verificación de los atributos personalizados.
7. Seleccione **Aceptar** para cerrar el cuadro de diálogo y después seleccione **Actualizar paso**.
8. Repita los pasos del 1 al 7 para el segundo complemento.
9. Cierre **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
