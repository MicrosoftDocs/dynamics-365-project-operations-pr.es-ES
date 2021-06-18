---
title: Previsiones y presupuestos de proyectos
description: Microsoft Dynamics 365 Finance proporciona previsiones de proyectos y presupuestos de proyectos para gestionar y controlar sus proyectos.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1c1cde984334af8cc30e7899e3cf0b38467666f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999647"
---
# <a name="project-forecasts-and-budgets"></a>Previsiones y presupuestos de proyectos

[!include [banner](../includes/banner.md)]

Hay dos formas para gestionar y controlar proyectos: previsiones de proyectos y presupuestos de proyectos. 

Utilice la previsión de proyectos si su organización tiene una perspectiva operativa y se centra en los ingresos y costes que se derivan de transacciones específicas. Utilice el presupuesto de proyectos si su organización se centra más en cantidades financieras. 

Tanto los pronósticos como los presupuestos del proyecto utilizan modelos de pronóstico para mantener los importes de transacción proyectados. 

Cada método tiene sus ventajas. Debe considerar los siguientes puntos antes de seleccionar un método para su organización.

|   Método de asignación       |           Previsión de proyectos            |        Presupuesto de proyectos                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Asignación de períodos**     | No puede asignar transacciones explícitamente sobre un período fiscal. En cambio, la previsión y el control del pronóstico se basan en la vida del proyecto. Debido a que los pronósticos se basan en una fecha específica, debe inferir el período a partir de la fecha. | No puede asignar transacciones a todo el proyecto o un período fiscal. Si asigna durante un período, puede transferir los importes no utilizados al próximo período fiscal. |
| **Ver transacciones**  | Puede ver las transacciones en los formularios de previsión, donde ve las previsiones para toda la empresa y para todos los proyectos, independientemente de la jerarquía. Para concentrarse en un proyecto en particular, debe filtrar los datos.                                       | Puede ver las transacciones presupuestadas para una sola jerarquía de proyecto. Por lo tanto, puede ver los detalles de la transacción de un proyecto principal o sus subproyectos.                 |
| **Variables de transacción** | Cuando especifica transacciones de previsión, puede usar todos los atributos que existen para una transacción real. Esto permite mayor detalle en la previsión. Por ejemplo, puede especificar detalles para cantidades, trabajadores, artículos o propiedades de línea.         | Cuando especifica los detalles del presupuesto, puede usar solo cantidades, categorías y actividades.                    |
| **Seguridad**              | La previsión se basa en transacciones que especifica en los formularios de previsión y no implica ningún mecanismo de control de proceso. Cualquier trabajador que tenga permisos para un formulario de previsión puede revisar la información sin aprobación.                                        | El presupuesto utiliza el sistema de flujo de trabajo, que permite la gestión de cambios y le permite mantener un historial de las revisiones.         |
| **Tipos de entrada**           | Las entradas de transacciones de previsión se basan en el número de unidades y en los precios unitarios de coste y venta.  | Los detalles del presupuesto se basan en importes, que se dividen entre costes e ingresos.                                          |
| **Modelos de previsión**       | Dado que cada previsión debe estar asociada a un modelo, puede crear varios modelos de previsión y también configurar submodelos.           | La creación de presupuestos para proyectos limita los modelos de previsión que se utilizan para los presupuestos. Menos modelos de previsión pueden ayudar a aumentar la coherencia en las previsiones.                           |
| **Costes excesivos**         | Solo puede permitir o no permitir la entrada de transacciones que provocarán un coste excesivo.   | La creación de presupuestos para proyectos proporciona opciones de control adicionales para los usuarios. Puede permitir advertencias y saturaciones.                    |
| **Control**               | El control de previsiones se realiza utilizando la reducción de previsiones. Los importes reales se restan de los saldos de transacciones previstos sin ninguna traza de auditoría. Esto puede hacer que sea más difícil trazar dónde ocurrieron las transacciones reales.                   | En el control del presupuesto de proyectos, los importes reales se restan de los importes del presupuesto restante. Esto permite una traza de auditoría más clara.                                   |

## <a name="project-forecasts"></a>Previsiones de proyectos
Cuando utiliza la previsión de proyectos, puede especificar transacciones de previsión en formularios de previsión para cada tipo de transacción. Cada atributo disponible para una transacción real se puede usar para una transacción de previsiones por ejemplo, rentabilidad de línea, atributos de línea, trabajadores o descripciones. También puede prever cuánto tiempo después de incurrir en un coste facturará a un cliente. 

Las transacciones de previsión de proyectos se basan en unidades y cantidades. 

Debe asociar cada pronóstico del proyecto a un modelo de previsión. Cuando introduce una transacción de previsión, se sugiere automáticamente un modelo de previsión. El modelo de previsión actúa como un contenedor para las transacciones de previsión. 

Puede designar modelos de previsión como submodelos de un modelo. Esto le permite realizar previsiones por región, período de tiempo o departamento. Puede copiar las transacciones de previsión en un modelo para crear un nuevo modelo y también puede transferir las transacciones al libro de contabilidad. Debido a que existe una relación uno a uno entre un pronóstico y un modelo, cada modelo de pronóstico constituye un presupuesto separado para un proyecto. 

Los modelos de previsión pueden utilizar la reducción de previsión como mecanismo de control para proyectos. En la reducción prevista, las transacciones reales reducen los saldos de las transacciones previstas. Sin embargo, debido a que la reducción de la previsión se aplica al proyecto más alto de la jerarquía, proporciona una vista limitada de los cambios en la previsión. Por ejemplo, si un trabajador está asociado con un subproyecto, las transacciones reales del trabajador se registran en el proyecto principal. Esto puede dificultar el seguimiento de los cambios, porque no puede determinar fácilmente qué transacción en qué subproyecto provocó una reducción del importe previsto. Por lo tanto, es una buena idea crear una copia de un modelo de previsión para utilizar la reducción de previsión. Luego, puede usar los informes para ver cuál era la previsión original. 

Puede revisar, copiar, eliminar o transferir las previsiones del proyecto a un presupuesto del libro de contabilidad. Sin embargo, no hay control de proceso. Cualquier trabajador que tenga permisos para un formulario de previsión puede hacer revisiones sin revisión.

-   **Revisar**: puede revisar una transacción prevista en los mismos formularos en los que se realizaron las entradas originales.
-   **Copiar o borrar**: cuando copia transacciones de previsión, copia las líneas de transacción de un modelo de previsión a otro modelo de previsión. Cuando elimina una previsión, elimina las transacciones de previsión de un modelo de previsión. Para limitar las transacciones de previsión que se copian o eliminan, se seleccionan tipos de transacciones y fechas específicas. Esto permite copiar o eliminar solo partes específicas de una previsión.
-   **Transferir**: cuando transfiere una previsión de proyecto a un presupuesto de contabilidad general, transfiere las transacciones de previsión de un modelo de previsión a un presupuesto de contabilidad general. Puede sobrescribir cualquier transacción transferida previamente en el presupuesto de contabilidad general al que transfiere la previsión del proyecto.

## <a name="project-budgets"></a>Presupuestos de proyecto
La creación de presupuestos de proyectos es un método más sencillo que la previsión, aunque se integra con los modelos de previsión. Utiliza un formulario de entrada única para los detalles y las revisiones del presupuesto original, y permite proyecciones que se basan únicamente en la cantidad, categoría o actividad. 

En la gestión presupuestaria de proyectos, todos los presupuestos originales y las revisiones deben enviarse a un flujo de trabajo de proyecto para su aprobación. Los flujos de trabajo le brindan un mayor control sobre el proceso y crean un registro del historial de cambios. 

La creación de presupuestos de proyecto se parece a la creación de presupuestos del libro de contabilidad, pero es más rápida y fácil de configurar. Muchas de las opciones de la creación de presupuestos del libro de contabilidad, como las secuencias numéricas o la moneda, no tienen que configurarse por separado para los proyectos.

Los presupuestos del proyecto se asocian automáticamente con dos modelos de previsión, uno para el presupuesto original y otro para el presupuesto restante. Por lo tanto, los informes que se basan en modelos de previsión pueden utilizar datos presupuestarios. Cuando se confirma un presupuesto de proyecto, el sistema crea transacciones de previsión basadas en los modelos asociados, que se utilizan para fines de informes y control.

## <a name="forecast-models"></a>Modelos de previsión
Los modelos de previsión tienen una jerarquía de una sola capa. Esto significa que la previsión de un proyecto debe estar asociada con un modelo de previsión.

Si utiliza la previsión de proyectos, puede identificar los modelos como submodelos. A continuación, puede crear previsiones por departamento, período de tiempo o región. Por ejemplo, puede crear un modelo de previsión para un año y luego crear submodelos para las previsiones regionales Noreste, Sudeste, Noroeste y Suroeste que envían los jefes regionales. Al seleccionar diferentes opciones en los informes disponibles, puede ver la información por pronóstico total o por submodelo.





[!INCLUDE[footer-include](../includes/footer-banner.md)]