---
title: Novedades o cambios en la versión 3 de Project Service Automation
description: Este tema proporciona información sobre las novedades y los cambios en Project Service Automation versión 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150689"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novedades o cambios en la versión 3 de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema proporciona información sobre los cambios en la interfaz de usuario (IU), la funcionalidad y la terminología en Project Service Automation entre la versión 2 o la versión 1 y la versión 3.

## <a name="project-scheduling"></a>Programación de proyectos
El programa del proyecto, que se conocía como Estructura de descomposición del trabajo (WBS) en versiones anteriores, ha cambiado de nombre a Programación y se accede a él clic en la pestaña. **Programación**. 

![Programación del proyecto](media/psa-schedule-01.png)

El programa ahora tiene una nueva superficie de interacción que es tanto moderna como accesible. Sin embargo, el motor de programación de Project Service Automation subyacente no ha cambiado. Los botones de control en la cinta de la cuadrícula de programación le permiten interactuar con la programación de forma similar a la versión anterior de Project Service Automation. Entre los cambios adicionales en la programación se encuentran los siguientes:

- **Diagrama de Gantt**: el diagrama de Gantt ya no está presente. Volverá a aparecer una nueva visualización de Gannt en una actualización futura.
- **Encabezados de columna**: puede ocultar los encabezados de columna en la cuadrícula haciendo clic en el indicador hacia abajo junto al título de la columna. 
- **Columnas**: puede mostrar columnas ocultas haciendo clic en **Agregar columna**. 
- **Categoría de transacción**: se ha agregado una **Categoría de transacción** a la cuadrícula de programación y se muestra de forma predeterminada. 
 
## <a name="project-templates"></a>Plantillas de proyecto
Se han realizado los siguientes cambios en la funcionalidad de la plantilla del proyecto.

### <a name="create-a-project-template"></a>Crear una plantilla de proyecto 
Puede crear una plantilla de proyecto en la versión 3 de forma similar a las versiones anteriores de Project Service Automation. La plantilla puede contener solo una programación y esta puede incluir asignaciones, pero no son obligatorias. Si la programación tiene asignaciones, solo pueden ser para recursos genéricos. Puede generar requisitos de recursos para recursos genéricos, pero no se pueden reservar con recursos reales en la plantilla. No puede reservar un recurso real para un equipo en una plantilla. 

### <a name="create-a-template-from-an-existing-template"></a>Creación de una plantilla a partir de una plantilla existente
Cuando crea una nueva plantilla de proyecto a partir de una plantilla existente en la versión 3 de Project Service Automation, sucede lo siguiente: 

- La programación del proyecto de origen se copia en la plantilla. 
- Se copian los recursos genéricos en el equipo y cualquier asignación de recursos genéricos. Los requisitos para los recursos genéricos no se copian. 

### <a name="create-a-template-from-an-existing-project"></a>Creación de una plantilla a partir de un proyecto existente
Cuando crea una nueva plantilla de proyecto a partir de un proyecto existente, sucede lo siguiente: 

- La programación del proyecto de origen se copia en la plantilla. 
- Se copian los recursos genéricos en el equipo y se conserva cualquier asignación de recursos genéricos. Los requisitos para los recursos genéricos no se copian.    
- Los recursos con nombre, asignados o no asignados, se eliminan del equipo y se reemplazan por recursos genéricos.
- Si está presente, se elimina la información del cliente. 
- Si está presente, se eliminan las referencias a ofertas y contratos. 

### <a name="create-a-project-from-a-template"></a>Crear un proyecto a partir de una plantilla
Al crear un nuevo proyecto desde una plantilla, en la versión 3 de Project Service Automation, sucede lo siguiente:

- La programación, el equipo y las asignaciones se copian en el nuevo proyecto.   
- La fecha de inicio es la fecha de copia o la fecha seleccionada por el usuario.   
- Para cualquier miembro del equipo genérico con requisitos de recursos en la plantilla, los requisitos no se copian ni se generan automáticamente. Tendrá que generarlos. 

## <a name="copy-a-project"></a>Copia de un proyecto
Al copiar un proyecto, en la versión 3 de Project Service Automation, sucede lo siguiente: 

- La fecha de inicio estimada se copia, pero se puede cambiar.  
- La programación y las tareas del proyecto se copian. 
- Los recursos genéricos y sus asignaciones se copian. Los requisitos de recursos para los recursos genéricos no se copian. Tendrá que volver a generarlos. 
- Los recursos reales y sus asignaciones no se copian. En su lugar, se reemplazan por recursos genéricos. 
- Los datos reales no se copian al nuevo proyecto. 

## <a name="move-a-scheduled-project"></a>Movimiento de un proyecto programado
Cuando mueve la programación del proyecto existente, sucede lo siguiente: 

- Las fechas de las tareas se mueven automáticamente para que se correspondan con el período de movimiento. 
- Los recursos genéricos asignados permanecen asignados.   
- Si se generan antes de mover el proyecto, los requisitos para el recurso genérico siguen siendo los mismos y no se vuelven a generar automáticamente. Deberá generarlos nuevamente para reflejar las nuevas asignaciones debido al movimiento de la tarea. 
- Las asignaciones de recursos reales cambian para que se correspondan con el movimiento de la fecha de la tarea. Las reservas en recursos reales no cambian. Tendrá que modificar las reservas mediante la vista de conciliación. 
- Los recursos del equipo con reservas, pero sin asignaciones, no cambian. 
- Los datos reales no se mueven. 

## <a name="estimates"></a>Estimaciones
Las estimaciones se han dividido en dos pestañas:, **Asignación de recursos** y **Estimaciones**. La pestaña **Asignación de recursos** contiene las estimaciones de esfuerzo y muestra las asignaciones de recursos para las tareas en una vista en fases temporales. Puede editar las estimaciones en función de lo que ha generado el motor de programación.

![Pestaña Asignaciones de recursos con las estimaciones de esfuerzo y las asignaciones de recursos para tareas](media/resource-assignments-tab-02.png)

La pestaña **Estimaciones** muestra los importes de costes y ventas para las asignaciones de recursos. Los importes son de solo lectura. Los costes y los precios de ventas ahora se basan en las asignaciones de miembros del equipo en la programación. Esto significa que si tiene una tarea sin ninguna asignación, la tarea se mostrará debajo del cubo no asignado. Esto también significa que sin **rol**, que es una dimensión de precios predeterminada, no habrá costes o ventas estimados si tiene un cliente o contrato/oferta asociados con el proyecto. 

![Pestaña Estimaciones con los importes de costes y ventas](media/estimates-tab-03.png)
  
La categoría también se admite en tareas en la vista de programación. La agrupación por categoría en la vista de estimaciones por fases proporcionará una mejor experiencia, especialmente cuando también tiene estimaciones de gastos en su proyecto. Las estimaciones de gastos se introducen con una cuadrícula en una pestaña separada. 

Las estimaciones de gastos se pueden introducir en la cuadrícula en la pestaña **Estimaciones de gastos**. 

![Pestaña Estimaciones de gastos con la cuadrícula de estimaciones de gastos](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Administración de recursos
En la versión 3 de Project Service Automation, con la nueva interfaz unificada del cliente y los cambios en la relación entre las reservas y las asignaciones, la dotación de personal de un proyecto con recursos genéricos o reales ha cambiado drásticamente desde la versión 2 y la versión 1. Sin embargo, los conceptos de recursos reservables, tanto **real** como **genérico**, siguen siendo los mismos, al igual que los miembros del equipo, los requisitos, las asignaciones y las reservas.   

![Uso de selector de recursos](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Asignación de un recurso que se puede reservar real 
En Project Service Automation versión 3, las reservas y las asignaciones de tareas no están tan estrechamente entrelazadas como en versiones anteriores de Project Service Automation. Puede usar la cuadrícula del equipo para reservar un miembro **real** del equipo, similar a en el mercado.

Mediante el selector de recursos en la programación, puede seleccionar el miembro del equipo creado en la vista de equipo y, a continuación, asignarlo a las tareas. Puede continuar asignándoles tareas, incluso más allá de sus reservas. Use la pestaña **Conciliación** para conciliar a los miembros del equipo que tienen diferencias en las reservas y asignaciones.

El selector de recursos mostrará a los miembros del equipo para el proyecto. También puede usar el selector de recursos para buscar y ver otros recursos que se pueden reservar que no forman parte del equipo del proyecto. Puede asignarlos a una tarea y pasarán a formar parte del equipo del proyecto. Deberá reservarlos mediante la pestaña **Tablero de programación** o **Conciliación**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Asignación de un recurso que se puede reservar genérico en una tarea y un equipo de proyecto y posterior cumplimiento con un recurso real a través del tablero de programación 
En la versión 3 de Project Service Automation, la funcionalidad de generación de equipo no se usa para recursos genéricos. En su lugar, puede crear y asignar directamente un recurso genérico a partir de la programación escribiendo el nombre del puesto del recurso genérico en la celda de recursos de la programación. También puede seleccionar el icono de recurso en la celda y, a continuación, mediante el selector de recursos, escribir el nombre del recurso genérico que desee crear. Con ese procedimiento, se abrirá un panel de creación rápida que le permitirá establecer el rol y la unidad organizativa del miembro del equipo de recurso genérico. Después de crear el recurso, se asigna a la tarea y puede continuar asignando ese recurso genérico a otras tareas en la programación.    
 
Cuando haya asignado el recurso a todas las tareas apropiadas, podrá generar un requisito de recurso y luego cumplirlo reservando directamente con **Tablero de programación** o enviando una solicitud de recurso. También puede agregar recursos genéricos directamente a la cuadrícula de miembros del equipo. 

Los recursos genéricos se agregan al equipo del proyecto sin requisitos de recursos y con las fechas de inicio/finalización del proyecto hasta que se generen los requisitos de recursos. Para generar un requisito, seleccione el recurso genérico y haga clic en **Generar**. Ahora se mostrará el enlace del requisito y las horas necesarias se completarán con las horas asignadas. Puede hacer clic en el enlace para abrir y actualizar el requisito.
  
Cuando la reserva esté completa y un recurso con nombre la cumpla totalmente, el recurso genérico se reemplazará por el recurso con nombre y la asignación de la programación se actualizará con el recurso con nombre. 

Los recursos propuestos para los requisitos se almacenan ahora en una pestaña en lugar de en una sección separada.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Múltiples recursos con nombre que cumplen un recurso genérico
Cuando se cumple un requisito con múltiples recursos, el recurso genérico permanece en el equipo y se asigna a la tarea. Los miembros del equipo con nombre reservados no se asignan como parte de la posición. El jefe de proyecto puede asignar el trabajo según sea necesario a los recursos reales.  La vista **Conciliación** proporciona un desglose de las reservas de distintos recursos en varias asignaciones de tarea. Esto no se realiza automáticamente porque en escenarios más complicados, como uno en el que tiene una agrupación de tareas que componen el requisito, debe asumirse la intención con la que jefe de proyecto desea realizar la asignación. Debido a que el sistema no puede entender la intención, las suposiciones probablemente serán diferentes de lo previsto y se producirá un resultado incorrecto o impredecible. El resultado predecible es que el recurso genérico permanece asignado hasta que el jefe de proyecto asigne recursos de manera intencionada con la vista **Conciliación**.

### <a name="reconciliation"></a>Conciliación
La pestaña **Conciliación** muestra las reservas y todas las asignaciones para cada miembro del equipo del proyecto. La vista muestra horas en celdas que pueden representar puntos de tiempo de meses a días. Esta vista permite a los jefes de proyecto conciliar las reservas de los miembros del equipo y sus asignaciones para su equipo de proyecto. Esto resulta útil porque las reservas y las asignaciones de tareas no están estrechamente vinculadas, lo que permite una mayor flexibilidad al planificar un proyecto. 

![Pestaña Conciliación con reservas y asignaciones para los miembros del equipo del proyecto](media/resource-reconciliation-tab-06.png)

Para cada recurso, la vista selecciona la diferencia entre las reservas de un miembro del equipo y un informe de sus asignaciones de tareas y muestra las siguientes dos diferencias que pueden producirse con las reservas y asignaciones en un proyecto: 

- **Escasez de reservas**: la escasez de reservas se produce cuando un recurso tiene más asignaciones que reservas. Puesto que esta capacidad no se ha reservado, un jefe de proyecto puede efectuar la corrección extendiendo las reservas del recurso para cubrir el déficit. 
- **Reservas en exceso**: las reservas en exceso se producen cuando se ha reservado un recurso para el proyecto, pero no se ha asignado a tareas.  Esto podría ser aceptable si, por ejemplo, el recurso se ha reservado antes de que se produzca la a asignación de tareas. Sin embargo, en otros casos, es posible que no se planee asignar el recurso, y el jefe de proyecto debería considerar cancelar las reservas del recurso para permitir que la capacidad se use para otro proyecto. 

Cuando tenga asignaciones de tareas para un recurso sin reservas (escasez de reservas), puede seleccionar la escasez de reservas agregadas y hacer clic en **Ampliar reserva**. Desde ahí, puede ver la reserva que se necesita para solucionar la escasez de recursos y su disponibilidad. 
 
## <a name="time-and-expense"></a>Tiempo y gasto
En esta sección se proporciona información sobre los cambios de tiempo, gastos y aprobación en la versión 3 de Project Service Automation. Como parte de la solución Dynamics 365 Project Service Automation, se ha actualizado la característica **Entrada de tiempo** para aprovechar el marco de trabajo de interfaz unificada. Esto permite la entrega de una interfaz de usuario uniforme y coherente que sigue un diseño con capacidad de respuesta para una visualización óptima en cualquier tamaño de pantalla o dispositivo. 

### <a name="landing-page"></a>Página de aterrizaje
La experiencia de entrada de tiempo personalizada no extensible ha quedado en desuso en la versión 3. En su lugar, ahora hay una experiencia de cuadrícula nativa extensible y accesible. Puede obtener acceso a la funcionalidad de entrada de tiempo mediante el mapa del sitio de la izquierda. Con ese cambio, ya no podrá introducir el tiempo de una semana a la vez. En su lugar, deberá crear una entrada de tiempo para cada día en la cuadrícula. Después de que se hayan creado algunas entradas de tiempo, los usuarios pueden crear entradas de tiempo de forma masiva con la función **Copiar** que se explica más adelante en este tema. 

![Página de aterrizaje de entrada de tiempo](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Creación de nuevas entradas de tiempo 
Haga clic en **Nuevo** en la cinta para abrir una página de creación rápida para la entrada de tiempo donde introducir la duración en minutos, horas o días. Para hacer esto, simplemente comience a escribir h, m o d junto con la cantidad.  

![Creación rápida de entrada de tiempo](media/quick-create-time-entry-08.png)

Los campos de búsqueda están respaldados por vistas del sistema. Por ejemplo, después de introducir la información del proyecto, el campo **Tarea de proyecto** se establece de forma predeterminada en la vista **Mis tareas de proyecto abiertas**. Para crear entradas de tiempo para tareas que no están asignadas al usuario, haga clic en **Cambiar vista** en la búsqueda y seleccione **Todas las tareas de proyecto activas**. Una vez que se haya creado la entrada de tiempo y se muestre en la cuadrícula, podrá editar cualquier valor de línea directamente en la cuadrícula.  

### <a name="bulk-createcopy"></a>Creación/copia de forma masiva 
Después de que se hayan creado algunas entradas de tiempo, puede usar la funcionalidad de copia para crear entradas de tiempo adicionales de forma masiva. Haga clic en **Copiar** para abrir el cuadro de diálogo **Copiar**. En **Desde el período: fecha de inicio**, establezca el rango de fechas desde el que se deben copiar los períodos. En **Hasta el período: fecha de inicio**, especifique la fecha para la que se deben crear entradas de tiempo. Haga clic en **Copiar** para copiar las entradas de tiempo al día correspondiente de la semana indicado en **Hasta el período**. Por ejemplo, la entrada de tiempo del lunes de la semana pasada se copiará en el lunes de la semana indicada en **Hasta el período**. 

![Copia de entradas de tiempo de forma masiva](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importar datos 
Las asignaciones y el intercambio siguen el mismo patrón de interfaz de usuario, que permite al usuario especificar el rango de fechas desde el momento en que deben importarse las reservas. Luego, debe elegir explícitamente las reservas que deben copiarse en las entradas de tiempo **Borrador**. En la versión 3, ya no puede ver el patrón de las entradas de tiempo **Sugerido** en la cuadrícula y el calendario.  

### <a name="change-in-calendar-control"></a>Cambio en control del calendario
En la versión 3, nos hemos alejado del control de calendario personalizado y ahora estamos usando el calendario de UC para mostrar las entradas de tiempo para la semana. Con este calendario, puede ver el día, la semana y el mes. 

> [!NOTE]
> Una limitación del calendario es que este control no admite acciones en elementos de calendario individuales. Por ejemplo, no podrá seleccionar uno o más elementos del calendario y enviar o eliminar esos elementos. Al hacer clic en un elemento del calendario, se abrirá la página de la entidad **Entrada de tiempo** para acciones adicionales. 

### <a name="extensibility"></a>Extensibilidad
**Captura de datos en campos personalizados solo en entidades de entrada tiempo y gastos**: la entrada de tiempo utiliza una cuadrícula editable, una cuadrícula de solo lectura y controles de calendario desde la plataforma. Todos estos controles son nativos y, por lo tanto, admitirán personalizaciones. En la versión 3 de Project Service Automation, puede agregar campos personalizados adicionales, configurar campos de búsqueda y realizar una copia de seguridad con vistas personalizadas. También puede establecer una lógica empresarial personalizada basada en valores seleccionados en campos personalizados.  

**Captura de datos en campos personalizados en la entrada de tiempo y gastos y propagación a través de entidades que admiten el flujo de envío y aprobación**: el procesamiento típico de las entradas de tiempo se muestra en el siguiente diagrama.

![Flujo de entrada de procesamiento de tiempo](media/process-time-entries-10.png)

Si los requisitos comerciales estipulan que las entidades de tiempo y gasto deben capturar dimensiones de precios personalizadas y propagar los valores establecidos por un recurso de tiempo y entrada en la dimensión de precios personalizada a través de todas las entidades en el gráfico anterior, consulte [Configuración de campos personalizados como dimensiones de precios](set-up-pricing-dimensions.md).

Para admitir los requisitos comerciales en los que las entidades de tiempo y gastos deben capturar dimensiones personalizadas que no sean de precios y propagar los valores, puede usar la configuración de dimensiones de precios y expresar las dimensiones personalizadas como dimensiones de precios sin coste ni tasa de facturación. Otro escenario sería agregar un campo personalizado a cada una de las entidades con el mismo nombre de campo en todas las entidades. Se pueden crear complementos personalizados para relacionar registros en las entidades que participan en el flujo de envío/aprobación con el origen de la transacción y las entidades de conexión de la transacción.  

### <a name="delegate-time-and-expense-entry"></a>Delegación de entrada de tiempo y gastos
La plataforma Common Data Service no admite que un usuario se haga pasar por otro, lo que significa que en la versión 3 de Project Service Automation no se admite la entrada delegada de tiempo y gastos. Sin embargo, los socios y los clientes han aprovechado una solución alternativa para habilitar el soporte para experiencias de entrada de tiempo delegado en la versión 3. Esto es solo una solución alternativa y no completa, por lo que es importante comprender las limitaciones. Además, solo debe usar este enfoque si las limitaciones son aceptables . 

> [!IMPORTANT]
> El socio/cliente debe considerar esta información solo como guía sugerida para la implementación personalizada. El equipo del producto no ofrecerá soporte formal para esta funcionalidad a través de ninguno de nuestros canales de soporte.

### <a name="customization-details"></a>Detalles de personalización 
La personalización le permite agregar **Recurso que se puede reservar** a las experiencias de creación y edición, lo que permitirá que un usuario actúe como delegado al cambiar el campo **Reserva de recursos** a otro usuario para el que se deben registrar las entradas de tiempo y gastos. Los siguientes pasos tratan sobre la delegación de entrada de tiempo. Se aplica la misma información a la delegación de entrada de gastos. 
 
1.  Asegúrese de que el usuario delegado tenga acceso de seguridad global en proyectos y tareas de proyecto. 
1.  Puesto que **Recurso que se puede reservar**, que es un campo de la entidad **Entrada de tiempo**, no se expone en la página **Creación rápida**, tendrá que agregarlo.

    O bien.

    Cree una vista personalizada, que incluye la columna **Recurso que se puede reservar**, para ver solo las entradas de tiempo creadas para el recurso. Publique las personalizaciones en el diseñador del módulo de la aplicación para que esta vista aparezca en **Selector de vistas** en la página **Entradas de tiempo**. Existen dos complementos que gestionan la configuración del administrador para las entradas de tiempo que no son del proyecto:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Cree un nuevo complemento para sobrescribir el campo **Administrador** en el administrador del usuario asignado en el campo **Recurso que se puede reservar**. Use la misma **fase de ejecución** que el complemento fuera de banda (OOB) (prevalidación) y use un **orden de ejecución** superior a los complementos OOB (mayor que 1). Esto garantizará que el complemento personalizado se ejecute después de los complementos OOB.  
 
### <a name="end-user-experience"></a>Experiencia de usuario final
1.  Cuando cree una entrada de tiempo en la página de creación rápida, introduzca los detalles de Proyecto y Tarea del proyecto y, a continuación, elija el usuario en el campo **Recurso que se puede reservar** para el que se deben registrar las entradas de tiempo. 
2.  De forma predeterminada, este campo está predeterminado para el usuario conectado. Sin embargo, puesto que el usuario anuló este campo, ahora se crea una entrada de tiempo para el **recurso que se puede reservar** elegido.
3.  Cuando envíe las entradas de tiempo que creó para estos registros, las entradas se pondrán en cola para el aprobador en el proyecto como se esperaba. 
4.  Cuando recupere las entradas de tiempo creadas para el otro usuario, las entradas de tiempo volverán a un estado de **Borrador** con el campo **Recurso que se puede reservar** establecido para el otro usuario. 
5.  Opcionalmente, puede cambiar a la vista personalizada para filtrar las entradas de tiempo creadas para el otro usuario. 
 
### <a name="limitations"></a>Limitaciones
La funcionalidad **Copiar** e **Importar** solo funciona en el contexto del usuario que ha iniciado sesión. Esto significa que no es posible copiar o importar entradas de tiempo creadas para el usuario que ha iniciado sesión como recurso que se puede reservar.

Las entradas de tiempo que no son para un proyecto se enrutarán para su aprobación al administrador del recurso que se puede reservar solo si se completa el paso 4 en la sección **Detalles de la personalización** completa anterior. De lo contrario, las entradas de tiempo que no sean del proyecto para el otro usuario se enrutarán incorrectamente al administrador del usuario conectado. 

### <a name="other-changes"></a>Otros cambios 
Se ha eliminado la funcionalidad **Reservas y tareas**. 

## <a name="multidimensional-pricing"></a>Precios multidimensionales
Para maximizar la flexibilidad y cumplir con los diferentes requisitos comerciales, la versión 3 de Project Service Automation admite la aplicación discreta de conjuntos de dimensiones de precios a tasas de coste y facturación. Los valores de dimensión se pueden establecer como predeterminados y, a continuación, propagarse a través del proceso de cálculo de costes y precios desde la creación de perfiles de recursos hasta la entrada de tiempo a los datos reales del proyecto. La configuración y modificación o extensión específica del cliente aprovecha la infraestructura de personalización estándar.

Project Service Automation se envía con un conjunto predeterminado de dimensiones de precios y roles y unidades de recursos, y permite la configuración de precios y costes para cada combinación de roles y unidades organizativas.

Para los clientes de Project Service Automation que desean continuar utilizando estos campos listos para usar como dimensiones de precios en la versión 3, no habrá ningún cambio observable. Puede continuar utilizando Project Service Automation como de costumbre. Sin embargo, si necesita fijar el precio o el coste de sus recursos utilizando otros atributos adicionales, la versión 3 le permite agregar sus propias dimensiones de precios personalizados a Project Service Automation. La extensión de las dimensiones de precios personalizados es una experiencia de configuración complicada. 

## <a name="quotes-and-contracts"></a>Ofertas y contratos
En la versión 3 de Project Service Automation, los aspectos de configuración y administración de ofertas y contratos han cambiado. Las siguientes secciones proporcionan información más detallada.

### <a name="set-up-chargeability-options"></a>Configuración de opciones de imputabilidad
En las versiones 1 y 2, la configuración de imputabilidad para roles y categorías para ofertas y contratos específicos se realizó mediante la vista **Imputabilidad** que estaba en la navegación superior de una línea de oferta o una línea de contrato. Aquí también se podían configurar los precios para esos roles y categorías de gastos.

A partir de la versión 3, la configuración de las opciones de imputabilidad por rol y categoría de gastos se realizará a nivel de línea de oferta o contrato. La configuración de precios es independiente de la configuración de imputabilidad. Podrá encontrar **Roles imputables** y **Categorías de gastos imputables** como pestañas en las páginas **Línea de oferta** y  **Línea de contrato** sin tener que utilizar la barra de navegación superior.

![Roles imputables](media/chargeable-12.png)
 
La configuración de Roles imputables y Categorías imputables también aprovecha el control de cuadrícula editable listo para usar. Para cada función y categoría, las opciones soportadas para el tipo de facturación durante la fase de oferta y contrato no han cambiado desde las versiones anteriores como **Imputable** y **No imputable**. **Gratis** no es un tipo admitido durante la fase de oferta o contrato. **Gratis** solo se admite durante la aprobación de tiempo o gastos.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Creación y edición de precios personalizados para una oferta de Project Service Automation y un contrato de proyecto
En las versiones 1 y 2, el uso de la lista de precios personalizada para ofertas y contratos específicos se realizó mediante **Editar precios** en la vista **Imputabilidad**. La vista **Imputabilidad** se encuentra en la navegación superior de una línea de oferta o una línea de contrato. Aquí también era donde podía configurar opciones de imputabilidad para roles o categorías de gastos.

A partir de la versión 3, la creación y el uso de una lista de precios de proyecto personalizada en una oferta y un contrato de proyecto de Project Service Automation se ha separado de la configuración de imputabilidad. La oferta y los contratos de proyecto de Project Service Automation tienen una pestaña nueva denominada **Listas de precios de proyecto**. Esta pestaña muestra una vista asociada de todas las listas de precios del proyecto que se adjuntan a la oferta o al contrato del proyecto de Project Service Automation. Para crear una lista de precios personalizada a partir de una lista de precios existente que ya asociada a la oferta o contrato del proyecto, haga clic en **Crear precios personalizados**. Esto creará una copia de todas las listas de precios asociadas y las adjuntará a la oferta o al contrato. Ahora puede abrir la lista de precios y editar el precio de la categoría de gastos o roles para que esos cambios de precios solo se apliquen a esta oferta o contrato. 
  
El siguiente gráfico es de antes de que se hayan creado listas de precios personalizadas.

![Antes de listas de precios personalizadas](media/before-custom-price-lists-13.png)

El siguiente gráfico es de después de que se hayan creado listas de precios personalizadas.

![Después de listas de precios personalizadas](media/after-custom-price-lists-14.png)

> [!NOTE]
> Puede producirse un pequeño retraso entre cuando hace clic en **Crear precios personalizados** y cuando se crea la lista de precios personalizada. Recomendamos actualizar la cuadrícula en lugar de hacer clic varias veces. Se ha creado una lista de precios personalizada si el nombre de la lista de precios asociada tiene el nombre de oferta o el nombre del contrato del proyecto adjunto.
