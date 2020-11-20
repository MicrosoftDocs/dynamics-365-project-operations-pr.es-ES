---
title: Administrar clientes potenciales
description: En este tema se proporciona información sobre la administración de clientes potenciales basados en proyecto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4c99485a1d0c54ae848e5fbed4c4590e96cba9fd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181788"
---
# <a name="manage-leads"></a>Administrar clientes potenciales

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los clientes potenciales basados en proyectos se pueden gestionar y calificar en Project Operations. El proceso de gestión de clientes potenciales incluye la creación de clientes potenciales basados en el trabajo y la calificación de esos clientes potenciales. 

## <a name="project-sales-leads"></a>Clientes potenciales de proyecto

En la sección **Ventas**, en el panel de navegación izquierdo, abra la página de lista **Clientes potenciales** para ver una lista de todos los registros de clientes potenciales del sistema. La lista de clientes potenciales que se muestra están basados en el trabajo y otros tipos de clientes potenciales que se pueden crear si también tiene Dynamics 365 Sales o aplicaciones de Dynamics 365 Field Service.

Puede crear un vista filtrada para ver solo clientes potenciales basados en proyectos creando un filtro en el valor **Tipo**. Por ejemplo, puede seleccionar mostrar solo los clientes potenciales basados en el trabajo.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Cree un nuevo cliente potencial para una oferta basada en proyecto

Cuando se califica un cliente potencial basado en un proyecto, se crean una oportunidad y una cuenta. Una oportunidad basada en proyecto es el punto de partida para las actividades de búsqueda de ventas en la fase de oportunidad. Las oportunidades basadas en proyectos tienen capacidades únicas que se requieren para vender el trabajo del proyecto. Entre estas capacidades se incluyen:

- Métodos de facturación de tiempo y material y precio fijo
- Listas de precios de múltiples fechas efectivas para recursos humanos, gastos y material incurrido en proyectos

Para que un cliente potencial calificado cree automáticamente una oportunidad, establezca el atributo **Tipo** en **Basado en trabajo** al crear el cliente potencial. Si elige un tipo diferente, el cliente potencial no creará una oportunidad basada en el proyecto cuando esté calificado. Si no se crea la oportunidad basada en el proyecto, las capacidades específicas del proyecto no estarán disponibles en los procesos de ventas posteriores.

La siguiente tabla incluye información de campos importante para un cliente potencial y las implicaciones posteriores de esos campos.
 
| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Tema | Pestaña General | Este campo de texto debe contener una breve descripción de la oferta. | El tema del cliente potencial se establecerá de forma predeterminada como tema de la oportunidad y el nombre de la oferta y el contrato del proyecto. |
| Escribir | Pestaña General | El campo de conjunto de opciones incluye las siguientes opciones:</br>- Basado en el trabajo (disponible solo cuando está instalado Project Operations)</br>- Basado en artículo (disponible solo cuando están instalados Project Operations y Ventas)</br>- Servicio basado en mantenimiento (disponible cuando se instala Field Service) | Cuando el valor de este campo se establece en **Basado en el trabajo** en el cliente potencial, el cliente potencial está calificado para crear una Oportunidad basada en proyectos. Es necesaria una oportunidad basada en proyecto para habilitar todas las extensiones y funcionalidades específicas del proyecto en el proceso de ventas posterior de esta oferta. |
| Nombre | Pestaña General | Nombre de pila del contacto del posible interesado | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El nombre de pila del contacto es el valor establecido aquí. |
| Apellido | Pestaña General | Nombre de pila del contacto del posible interesado | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El apellido del contacto es el valor establecido aquí. |
| Empresa | Pestaña General | Nombre de la empresa del cliente potencial | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El nombre de la cuenta que creó el valor establecido aquí. |
| Divisa | Pestaña Detalles | Moneda del cliente potencial | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. La moneda de la cuenta creada es el valor establecido aquí. |

## <a name="qualify-a-new-project-based-lead"></a>Calificar un nuevo cliente potencial basado en proyectos

Los clientes potenciales con el valor **Tipo** establecido en **Basado en el trabajo** se denominan clientes potenciales basados en proyectos. Cuando se califica un cliente potencial basado en un proyecto, se crea lo siguiente:

- Una cuenta que usa el campo **Empresa** del cliente potencial.
- Un registro de contacto asociado a la cuenta basado en los valores de los campos **Nombre de pila** y **Apellido** del cliente potencial.
- Una oportunidad basada en proyectos que tiene el campo **Tipo** establecido en **Basado en trabajo**.

Para obtener información más detallada sobre los clientes potenciales calificados, consulte [Calificar o convertir clientes potenciales](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Calificación de cliente potencial e información de la entidad legal 

Cuando ejecuta operaciones de proyecto usando el modo de implementación, operaciones de proyecto para escenarios basados en recursos/no en existencias, cada cliente y oportunidad requerirán tener el conjunto de campos **Empresa propietaria**. La empresa propietaria es una entidad legal de su organización que es propietaria de la entrega del proyecto. Cada cliente, o cuenta con tipo de relación de cliente, debe tener el valor de campo **Empresa propietaria** establecido al valor de la entidad jurídica que contrata y negocia con este cliente. Un cliente solo puede estar en una entidad jurídica.

Cuando un cliente potencial está calificado, los registros de clientes y oportunidades creados tendrán el campo **Empresa propietaria** establecido en la empresa del registro de recursos reservables del usuario actual.

Si el registro de recursos reservables del usuario actual está vacío, entonces el valor del campo **Empresa propietaria** del registro de usuario se usa para predeterminar el cliente y los registros de oportunidad.

## <a name="business-process-flow-for-project-based-deals"></a>Flujo de proceso de negocio para ofertas basadas en proyectos

Los siguientes flujos de procesos de negocio son compatibles con ofertas basadas en Project Operations:

- Proceso de negocio de cliente potencial a oportunidad
- Proceso de venta de la oportunidad

El proceso de negocio de cliente potencial a oportunidad comprende las etapas siguientes:

| Nombre de la fase | Entidad mapeada | Funcionalidad |
| --- | --- | --- |
| Calificar | Cliente potencial | Calificar el cliente potencial para crear una cuenta, un contacto y una oportunidad. |
| Desarrollar | Oportunidad | Desarrolle la oportunidad de agregar más información sobre el trabajo involucrado, las partes interesadas clave y la competencia. |
| Proponer | Oportunidad | Desarrolle la propuesta y obtenga la aprobación del equipo de revisión interno. |
| Cerrada | Oportunidad | Gane la oportunidad de cerrar la oferta. |
