---
title: Actualizar de Project Service Automation a Project Operations
description: Este tema proporciona información general sobre el proceso para actualizar de Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952849"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualizar de Project Service Automation a Project Operations

Nos complace anunciar la primera de las tres fases para actualizar desde Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations. Este tema proporciona una descripción general para los clientes que se están embarcando en este emocionante viaje. Los temas futuros incluirán consideraciones de los desarrolladores y detalles sobre las mejoras de funciones. No solo brindarán orientación para ayudarlo a prepararse para su actualización a Project Operations, sino que también le explicarán lo que puede esperar después de la actualización.

El programa de actualización se dividirá en tres fases.

| Entrega de actualización | Fase 1 (enero de 2022) | Fase 2 (oleada de abril de 2022) | Fase 3 (oleada de abril de 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Sin dependencia de la estructura de desglose del trabajo (WBS) para proyectos | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La EDT dentro de los límites actualmente admitidos de Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| La EDT fuera de los límites admitidos actualmente de Project Operations, incluida la compatibilidad con Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Actualización de características del proceso 

Como parte del proceso de actualización, hemos agregado registros de actualización al mapa del sitio, para que los administradores puedan diagnosticar fallas más fácilmente. Además de la nueva interfaz, se agregarán nuevas reglas de validación para garantizar la integridad de los datos después de una actualización. Las siguientes validaciones se agregarán al proceso de actualización.

| Validaciones | Fase 1 (enero de 2022) | Fase 2 (oleada de abril de 2022) | Fase 3 (oleada de abril de 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| La WBS se validará frente a violaciones comunes de la integridad de los datos (por ejemplo, asignaciones de recursos que están asociadas con la misma tarea principal pero tienen diferentes proyectos principales). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS se validará contra los [límites conocidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS se validará contra los límites conocidos de Project Desktop Client. | | :heavy_check_mark: | :heavy_check_mark: |
| Los recursos que se pueden reservar y los calendarios de proyectos se evaluarán en función de las excepciones comunes de reglas de calendario incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

En la fase 2, los clientes que se actualicen a Project Operations verán sus proyectos existentes actualizados a una experiencia de solo lectura para la planificación de proyectos. En esta experiencia de solo lectura, la WBS completa será visible en la cuadrícula de seguimiento. Para editar la EDT, los jefes de proyecto pueden seleccionar **Convertir** en la página principal de **Proyectos**. Luego, un proceso en segundo plano actualizará el proyecto para que sea compatible con la nueva experiencia de programación de proyectos de Project for the Web. Esta fase es apropiada para clientes que tienen proyectos que encajan dentro de los [límites conocidos de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

En la fase 3, se agregará soporte para Project Desktop Client, en beneficio de los clientes que deseen continuar editando sus proyectos desde esa aplicación. Sin embargo, si los proyectos existentes se convierten a la nueva experiencia de Project for the Web, el acceso al complemento se deshabilitará para cada proyecto convertido.

## <a name="prerequisites"></a>Requisitos previos

Para ser elegible para la actualización de la fase 1, un cliente debe cumplir con los siguientes criterios:

- El entorno de destino no debe contener ningún registro en la entidad **msdyn_projecttask**.
- Las licencias de Project Operations válidas deben asignarse a todos los usuarios activos del cliente. 
- El cliente debe validar el proceso de actualización en al menos un entorno que no sea de producción que tenga un conjunto de datos representativo que esté alineado con los datos de producción.
- El entorno de destino debe actualizarse a Project Service Automation Update Release 38 o posterior.

Los requisitos previos para la fase 2 y la fase 3 se actualizarán a medida que se acerquen las fechas de disponibilidad general.

## <a name="licensing"></a>Licencias

Si tiene licencias activas para Project Service Automation, puede instalar y usar Project Operations, que incluye todas las capacidades de Project Service Automation y más. De esta manera, puede probar las capacidades de Project Operations mientras continúa utilizando Project Service Automation en producción. Una vez que expiren sus licencias de Project Service Automation, deberá realizar la transición a Project Operations. Cuando planifique esta transición, debe tener en cuenta el hecho de que la licencia de Project Operations no incluye una licencia de Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Prueba y refactorización de personalizaciones

Como punto de partida, importe todas las personalizaciones en un entorno limpio de Project Operations (lite) para confirmar que la importación se realiza correctamente y que las operaciones comerciales se comportan como se esperaba.

Aquí hay algunas cosas a tener en cuenta:

- La importación puede fallar debido a que faltan dependencias. En otras palabras, las personalizaciones hacen referencia a campos u otros componentes que se han eliminado en Project Operations. En este caso, elimine estas dependencias del entorno de desarrollo.
- Si sus soluciones administradas y no administradas incluyen componentes que no están personalizados, elimínelos de la solución. Por ejemplo, cuando personaliza la entidad **Proyecto**, agregue solo el encabezado de la entidad a su solución. No agregue todos los campos. Si ha agregado previamente todos los subcomponentes, es posible que deba crear manualmente una nueva solución y agregarle componentes relevantes.
- Es posible que los formularios y las vistas no parezcan tan inesperados. En algunas circunstancias, si ha personalizado cualquiera de los formularios o vistas listos para usar, las personalizaciones pueden evitar que entren en vigencia las nuevas actualizaciones en Project Operations. Para identificar estos problemas, le recomendamos que haga una revisión en paralelo de una instalación limpia de Project Operations y una instalación de Project Operations que incluya sus personalizaciones. Compare los formularios más utilizados en su empresa para confirmar que su versión del formulario todavía tiene sentido y que no le falta nada en la versión limpia del formulario. Realice el mismo tipo de revisión en paralelo para las vistas que haya personalizado.
- La lógica empresarial puede fallar en tiempo de ejecución. Debido a que las referencias a campos en sus complementos no se validan en el momento de la importación, la lógica empresarial puede fallar debido a referencias a campos que ya no existen y es posible que reciba un mensaje de error similar al siguiente ejemplo: "'Proyecto' la entidad no contiene el atributo con Name = 'msdyn_plannedhours' y NameMapping = 'Logical'. " En este caso, modifique sus personalizaciones para que utilicen los nuevos campos. Si usa clases de proxy generadas automáticamente y referencias de tipo fuerte en la lógica de su complemento, considere la posibilidad de volver a generar esos proxies a partir de una instalación limpia. De esta manera, puede identificar fácilmente todos los lugares donde sus complementos dependen de campos obsoletos.

Después de actualizar sus personalizaciones para importar Project Operations de manera limpia, continúe con los siguientes pasos.

## <a name="end-to-end-testing-in-lower-environments"></a>Pruebas de un extremo a otro en entornos inferiores

### <a name="run-the-upgrade-in-production"></a>Ejecute la actualización en producción

1. En el centro de administración de Power Platform, busque y seleccione su entorno. Luego, en las aplicaciones, busque y seleccione **Dynamics 365 Project Operations**.
2. Seleccione **Instalar** para iniciar la actualización. El centro de administración de Power Platform presentará esta instalación como una nueva instalación. Sin embargo, se detectará la presencia de una versión anterior de Project Service Automation y se actualizará la instalación existente.

    Una vez completada la actualización, el entorno debería mostrar que Project Operations está instalado y que Project Service Automation no está instalado.

    > [!NOTE]
    > Según la cantidad de datos del entorno, la actualización puede tardar varias horas. El equipo central que administra la actualización debe planificar en consecuencia y ejecutar la actualización fuera del horario comercial. En algunos casos, si el volumen de datos es grande, la actualización debe ejecutarse durante el fin de semana. La decisión sobre la programación debe basarse en los resultados de las pruebas en entornos inferiores.

3. Actualice las soluciones personalizadas según corresponda. En este punto, implemente cualquier cambio que haya realizado en sus personalizaciones en la sección [Prueba y refactorización de personalizaciones](#testing-and-refactoring-customizations) de este tema.
4. Vaya a **Ajustes** \> **Soluciones** y seleccione para desinstalar la solución **Componentes obsoletos de Project Operations**.

    Esta solución es una solución temporal que contiene el modelo de datos existente y los componentes que están presentes durante la actualización. Al eliminar esta solución, elimina todos los campos y componentes que ya no se utilizan. De esta manera, ayuda a simplificar la interfaz y facilita la integración y la extensión.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Cambios importantes entre Project Service Automation y Project Operations

Esta sección proporciona un resumen de los principales cambios que puede esperar entre Project Service Automation y Project Operations.

### <a name="project-planning"></a>Planificación del proyecto

Las capacidades de planificación de proyectos en Project Operations ya no dependen de una combinación de lógica del lado del cliente y lógica del lado del servidor. En su lugar, Project Operations usa Project for the Web como su motor de programación principal. Este cambio en las capacidades de programación habilita varias características nuevas, como vistas de tablero y Gantt, planificación basada en recursos, [elementos de la lista de verificación de tareas](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) y modos de programación de proyectos. Las nuevas capacidades de programación también son compatibles con un amplio conjunto de nuevas [interfaces de programación de aplicaciones (API)](../project-management/schedule-api-preview.md). Estas API están destinadas a ayudar a garantizar que ninguna operación programática para crear, actualizar o eliminar una entidad en la WBS corrompa los campos calculados en la programación.

## <a name="billing-and-pricing"></a>Facturación y precios

Como parte de las inversiones continuas en Project Operations, hay varias capacidades nuevas disponibles en Facturación y precios. Estos son algunos ejemplos:

- [Registrar el uso de materiales en proyectos y tareas de proyectos](../material/material-usage-log.md)
- [Administración de subcontrataciones](../pro/subcontracting/managing-subcontracts-overview.md)
- [Contratos basados en pagos a cuenta y anticipos](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Contrato sin exceder los estados y las validaciones](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturación basada en tareas

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>¿Qué tipos de implementación se admiten actualmente para la actualización?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementación de Project Operations Lite                        | Addmitido               |
| Gestión de proyectos y contabilidad de Dynamics 365 Finance | Implementación de Project Operations Lite                        | No se admite actualmente |
| Administración de proyectos y contabilidad en Finance              | Project Operations para escenarios de recursos/no mantenidos en existencias     | No se admite actualmente |
| Administración de proyectos y contabilidad en Finance              | Project Operations para escenarios mantenidos en existencias/orden de producción | No se admite actualmente |
| Project Service Automation 3.x                         | Project Operations para escenarios de recursos/no mantenidos en existencias     | No se admite actualmente |
| Project for the Web (entorno dedicado)            | Implementación de Project Operations Lite                        | No se admite actualmente |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>¿Cómo puedo instalar Project Operations antes de que las herramientas de actualización estén disponibles?

Hay dos opciones para instalar Project Operations antes de que las herramientas de actualización estén disponibles:

- Aprovisionar un nuevo entorno.
- Implemente Project Operations por separado en cualquier organización de ventas donde no esté presente Project Service Automation.

> [!NOTE]
> Si Project Service Automation está instalado en una organización, pero no se usó, se puede desinstalar. Después de eliminar por completo Project Service Automation, Project Operations se puede instalar en la misma organización.
