---
title: Rendimiento de la API de programación de proyectos
description: Este artículo proporciona información sobre los puntos de referencia de rendimiento de las API de programación del proyecto e identifica las mejores prácticas para un uso óptimo.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911203"
---
# <a name="project-schedule-api-performance"></a>Rendimiento de la API de programación de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias, implementación simplificada: de la oferta a la facturación proforma, Project for the Web_

Este artículo proporciona información sobre los puntos de referencia de rendimiento de las interfaces de programación de aplicaciones (API) de programación del proyecto e identifica las mejores prácticas para optimizar el uso.

## <a name="project-scheduling-service"></a>Servicio de programación de proyectos
El servicio de programación de proyectos es un servicio de múltiples inquilinos que se ejecuta en Microsoft Azure. Está diseñado para mejorar la interacción al proporcionar una experiencia rápida y fluida cuando los usuarios trabajan en proyectos. Esta mejora se logra aceptando solicitudes de cambio, procesándolas y luego devolviendo el resultado de inmediato. El servicio persiste asincrónicamente para Dataverse y no impide que los usuarios realicen otras operaciones.

Las API de programación de proyectos se basan en el servicio de programación de proyectos para ejecutar solicitudes que se describen con más detalle en secciones posteriores de este artículo.

Las API de programación del proyecto están diseñadas para trabajar con las siguientes entidades de estructura de desglose del trabajo (WBS):

  - Project
  - Tarea de proyecto
  - Dependencia de tareas de proyecto
  - Miembro del equipo del proyecto
  - Asignación de recursos
  
Se admiten tanto los campos predefinidos como los campos personalizados. A menos que se indique lo contrario, se admiten todas las operaciones comunes, como crear, actualizar y eliminar. Para más información, vea [Utilizar las API de programación del proyecto para realizar operaciones y programar entidades](schedule-api-preview.md).

Como parte de las API de programación del proyecto, se ha agregado un patrón de unidad de trabajo. Este patrón se conoce como OperationSet y se puede utilizar cuando se deben procesar varias solicitudes en una sola transacción.

La siguiente ilustración muestra el flujo que experimentará un socio cuando se utilice esta función.

![Dataverse y flujo de servicio de programación de proyectos.](./media/dataverse-project-scheduling-service-flow.png)

**Paso 1**: Un cliente realiza una llamada API a un protocolo de datos abiertos (OData) punto de conexión en Dataverse para crear un OperationSet.

**Paso 2**: Una vez creado el nuevo OperationSet, se devuelve un valor **OperationSetId**.

**Paso 3**: El cliente utiliza el valor **OperationSetId** para realizar otra solicitud de API de programación del proyecto. El resultado es una solicitud de creación, actualización o eliminación en una entidad de programación. Cuando se realiza esta solicitud, se realiza la validación de metadatos. Si la validación falla, la solicitud finaliza y se devuelve un error.

**Pasos 4a-4c**: Estos pasos representan la fase ACEPTAR. El cliente llama a la API **ExecuteOperationSetV1**, que envía todos los cambios al servicio de programación de proyectos en un solo lote. El servicio de programación de proyectos ejecuta sus propias validaciones en las solicitudes en el lote. Cualquier falla de validación deshace el lote y devuelve una excepción a la persona que llama. Si el servicio de programación de proyectos acepta con éxito el lote, el estado del conjunto de operaciones se actualiza para reflejar el hecho de que el servicio de programación de proyectos está procesando el conjunto de operaciones.

**Paso 5**: Este paso representa es la fase PERSIST. El servicio de programación de proyectos escribe de forma asincrónica el lote en Dataverse en una transacción. Si la operación de escritura es exitosa, OperationSet se marca como **Terminado**. Cualquier error revierte la transacción y el lote, y OperationSet se marca como **Fallido**.

## <a name="performance-methodology"></a>Metodología de desempeño
El tiempo de ejecución se define como el tiempo desde la llamada hasta la API **ExecuteOperationSetV1** hasta que el servicio de programación de proyectos haya terminado de escribir en Dataverse. Todas las operaciones se ejecutan un total de 2200 veces y se informan las mediciones del tiempo de ejecución P99. Se miden las operaciones de registro único y a granel.

Para una operación de registro único, OperationSet contiene una solicitud. Para operaciones masivas, contiene 20, 50 o 100 solicitudes. Cada tamaño a granel se informa por separado.

Estas operaciones se ejecutan en una implementación UR 15 Project Operations Lite en Norteamérica.

## <a name="results"></a>Resultados
### <a name="create-operations"></a>Crear operaciones
#### <a name="single-record-create-operations"></a>Operaciones de creación de registro único
La siguiente tabla muestra los tiempos de ejecución para la creación de un solo registro. Las horas son en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;&nbsp;de&nbsp;registro</th>
    <th class="tg-0lax" colspan="2">Tiempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarea</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Asignación</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Miembro del equipo</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operaciones de creación en masa
La siguiente tabla muestra los tiempos de ejecución para la creación de muchos registros. Específicamente, Microsoft midió los tiempos de ejecución para la creación de 20, 50 y 100 registros en un solo OperationSet. Las horas son en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo&nbsp;&nbsp;de&nbsp;registro</th>
    <th class="tg-0lax" colspan="6">Tiempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registros</th>
    <th class="tg-0lax" colspan="2">50 registros</th>
    <th class="tg-0lax" colspan="2">100 registros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarea</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Asignación</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operaciones de creación masiva en las entidades **Proyecto** y **Miembro del equipo** no se incluyen en esta tabla, porque el tiempo de ejecución de esas operaciones se asemeja al tiempo de ejecución cuando la API para crear un solo registro se llama varias veces. Estas API se ejecutan inmediatamente en Dataverse.

La siguiente ilustración muestra un gráfico de los tiempos de ejecución para las entidades **Tarea**, **Asignación** y **Dependencia** cuando se crean 20, 50 y 100 registros y se utilizan todos los campos admitidos.

![Cree un gráfico de tiempo de ejecución récord.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operaciones de actualización
#### <a name="single-record-update-operations"></a>Operaciones de actualización de registro único
La siguiente tabla muestra los tiempos de ejecución para las actualizaciones de un solo registro. Las horas son en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;&nbsp;de&nbsp;registro</th>
    <th class="tg-0lax" colspan="2">Tiempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obligatorios </th>
    <th class="tg-0lax">Todos los campos compatibles</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tarea</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Miembro del equipo</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Actualizar operaciones en las entidades **Asignaciones de recursos** y **Dependencia de la tarea del proyecto** no son compatibles.

#### <a name="bulk-update-operations"></a>Operaciones de actualización en masa
La siguiente tabla muestra los tiempos de ejecución para las actualizaciones de muchos registros. Específicamente, Microsoft midió los tiempos de ejecución para las actualizaciones de 20, 50 y 100 registros en un solo OperationSet. Las horas son en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipo&nbsp;&nbsp;de&nbsp;registro</th>
    <th class="tg-0lax" colspan="6">Tiempo</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registros</th>
    <th class="tg-0lax" colspan="2">50 registros</th>
    <th class="tg-0lax" colspan="2">100 registros</th>
  </tr>
  <tr>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
    <th class="tg-0lax">Campos obligatorios</th>
    <th class="tg-0lax">Todos los campos compatibles</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarea</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Miembro del equipo</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Actualizar operaciones en las entidades **Asignaciones de recursos** y **Dependencia de la tarea del proyecto** no son compatibles.

La siguiente ilustración muestra un gráfico de los tiempos de ejecución para las entidades Tarea y Miembro de equpo cuando se crean 20, 50 y 100 registros y se utilizan todos los campos admitidos.

![Actualice un gráfico de tiempo de ejecución récord.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operaciones de eliminación
#### <a name="single-record-delete-operations"></a>Operaciones de eliminación de registro único
La siguiente tabla muestra los tiempos de ejecución para la eliminación de un solo registro. Las horas son en segundos.

| Tipo de registro | Tiempo  |
|-------------|-------|
| Tarea        | 20.12 |
| Asignación  | 10.86 |
| Miembro del equipo | 12.52 |
| Dependencia  | 20.89 |

> [!NOTE]
> No se permiten las operaciones de eliminación en la entidad **Proyecto**.

#### <a name="bulk-delete-operations"></a>Operaciones de eliminación en masa
La siguiente tabla muestra los tiempos de ejecución para la eliminación de muchos registros. Específicamente, Microsoft midió los tiempos de ejecución para la eliminación de 20, 50 y 100 registros en un solo OperationSet. Las horas son en segundos.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipo&nbsp;&nbsp;de&nbsp;registro</th>
    <th class="tg-0lax" colspan="3">Tiempo</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 registros</th>
    <th class="tg-0lax">50 registros</th>
    <th class="tg-0lax">100 registros</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tarea</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Asignación</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Miembro del equipo</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependencia</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> No se permiten las operaciones de eliminación en la entidad **Proyecto**.

La siguiente ilustración muestra un gráfico de los tiempos de ejecución para las entidades **Tarea**, **Asignación**, **Miembro de equipo** y **Dependencia** cuando se eliminan 20, 50 y 100 registros.

![Elimine un gráfico de tiempo de ejecución récord.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observaciones
Para cada operación de registro, la API **ExecuteOperationSet** tarda unos 800 milisegundos en enviar una solicitud al servicio de programación de proyectos. El servicio de programación de proyectos tarda unos cinco segundos en procesar la carga útil y llamar Dataverse. El resto del tiempo de ejecución se dedica a ejecutar la lógica empresarial y a escribir datos en la base de datos en Dataverse.

Cuando se crean, actualizan o eliminan 100 registros, la API **ExecuteOperationSet** tarda unos tres segundos en enviar la solicitud al servicio de programación de proyectos. El servicio de programación de proyectos tarda unos cinco segundos en procesar las solicitudes y llamar a Dataverse. Las operaciones a granel deben pagar un **Impuesto al servicio de programación de proyectos** una vez, para todos los registros del OperationSet. Por lo tanto, las operaciones masivas tienen un tiempo de ejecución promedio significativamente menor que las operaciones de registro único.

## <a name="scenarios"></a>Escenarios
La siguiente tabla muestra los tiempos de ejecución cuando las API de programación del proyecto se utilizan para lograr escenarios específicos. Las horas son en segundos.

| Escenario                                                                   | Tiempo  |
|----------------------------------------------------------------------------|-------|
| Crea un proyecto que tenga 40 tareas.                                      | 36.01 |
| Crea un proyecto que tenga 40 tareas y 20 dependencias.                  | 38.11 |
| Crea un proyecto que tenga 40 tareas y 30 asignaciones.                   | 60.17 |
| Crea un proyecto que tenga 40 tareas, 20 dependencias y 30 asignaciones. | 60.27 |

## <a name="best-practices"></a>Prácticas recomendadas
Según los resultados del escenario anterior, las API funcionan mejor en las siguientes condiciones:

  - Agrupe tantas operaciones como sea posible. El tiempo de ejecución promedio para operaciones masivas es mejor que el tiempo de ejecución promedio para operaciones de registro único. Cuanto menor sea el número de OperationSets en uso, más rápido será el tiempo medio de ejecución.
  - Establezca solo los atributos mínimos que se requieren para lograr su escenario. Sea selectivo con los tipos de campos no obligatorios incluidos en una solicitud OperationSet. Los campos que contienen claves externas o campos acumulados afectarán negativamente al rendimiento.
