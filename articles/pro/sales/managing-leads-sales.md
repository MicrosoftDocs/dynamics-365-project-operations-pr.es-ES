---
title: Administrar clientes potenciales (lite)
description: En este tema se proporciona información sobre la administración de clientes potenciales basados en proyecto (pro).
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67480459478ffb8a157a2943af919dc63721b779
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994742"
---
# <a name="manage-leads---lite"></a>Administrar clientes potenciales (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Los clientes potenciales basados en proyectos se pueden gestionar y calificar en Project Operations. El proceso de gestión de clientes potenciales incluye la creación de clientes potenciales basados en el trabajo y la calificación de esos clientes potenciales. 

## <a name="list-of-project-sales-leads"></a>Lista de clientes potenciales de proyecto

En la sección **Ventas**, en el panel de navegación izquierdo, abra la página de lista **Clientes potenciales** para ver una lista de todos los registros de clientes potenciales del sistema. Los clientes potenciales de la lista están basados en trabajo y otros tipos de clientes potenciales que se pueden crear si también tiene las aplicaciones de Dynamics 365 Sales o Dynamics 365 Field Service.

Puede crear una vista filtrada para ver solo los clientes potenciales basados en proyectos creando un filtro en el valor **Tipo**. Por ejemplo, puede seleccionar mostrar solo los clientes potenciales basados en el trabajo.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Creación de un nuevo cliente potencial para una oferta basada en proyecto

Cuando se califica un cliente potencial basado en un proyecto, se crean una oportunidad y una cuenta. Una oportunidad basada en proyectos es el punto de partida para las actividades de búsqueda de ventas en la fase Oportunidad. Las oportunidades basadas en proyectos tienen capacidades únicas que se requieren para vender el trabajo del proyecto. Entre estas capacidades se incluyen:

- Métodos de facturación de tiempo y material y precio fijo
- Listas de precios vigentes en múltiples fechas para recursos humanos, gastos y material incurrido en proyectos.

Para que un cliente potencial calificado cree automáticamente una oportunidad, establezca el atributo **Tipo** en **Basado en trabajo** al crear el cliente potencial. Si elige un tipo diferente, el cliente potencial no creará una oportunidad basada en el proyecto cuando esté calificado. Si no se crea la oportunidad basada en el proyecto, las capacidades específicas del proyecto no estarán disponibles en los procesos de ventas posteriores.

La siguiente tabla incluye información de campos importante para un cliente potencial y las implicaciones posteriores de esos campos.

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Tema | Pestaña General | Este campo de texto debe contener una breve descripción de la oferta. | El tema del cliente potencial se establecerá de forma predeterminada como tema de la oportunidad, y el nombre de la oferta y el contrato del proyecto. |
| Escribir | Pestaña General | El campo de conjunto de opciones incluye las siguientes opciones:</br>- Basado en el trabajo (disponible solo cuando está instalado Project Operations)</br>- Basado en artículo (disponible solo cuando están instalados Project Operations y Ventas)</br>- Servicio basado en mantenimiento (disponible cuando se instala Field Service) | Cuando el valor de este campo se establece en **Basado en el trabajo** en el cliente potencial, el cliente potencial está calificado para crear una Oportunidad basada en proyectos. Es necesaria una oportunidad basada en proyecto para habilitar todas las extensiones y funcionalidades específicas del proyecto en el proceso de ventas posterior de esta oferta. |
| Nombre | Pestaña General | Nombre de pila del contacto del posible interesado | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El nombre de pila del contacto es el valor establecido aquí. |
| Apellido | Pestaña General | Nombre de pila del contacto del posible interesado | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El apellido del contacto es el valor establecido aquí. |
| Empresa | Pestaña General | Nombre de la empresa del cliente potencial | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. El nombre de la cuenta creada es el valor establecido aquí. |
| Divisa | Pestaña Detalles | Moneda del cliente potencial | Cuando se califica el cliente potencial, se crean una cuenta, un contacto y una oportunidad. La moneda de la cuenta creada es el valor establecido aquí. |

## <a name="qualify-a-new-project-based-lead"></a>Calificar un nuevo cliente potencial basado en proyectos

Los clientes potenciales con el valor **Tipo** establecido en **Basado en el trabajo** se denominan clientes potenciales basados en proyectos. Cuando se califica un cliente potencial basado en un proyecto, se crea lo siguiente:

- Una cuenta que usa el campo **Empresa** del cliente potencial.
- Un registro de contacto asociado a la cuenta basado en los valores de los campos **Nombre de pila** y **Apellido** del cliente potencial.
- Una oportunidad basada en proyectos que tiene el campo **Tipo** establecido en **Basado en trabajo**.

Para obtener información más detallada sobre los clientes potenciales calificados, consulte [Calificar o convertir clientes potenciales](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Flujo de proceso de negocio para ofertas basadas en proyectos

Los siguientes flujos de procesos de negocio son compatibles con ofertas basadas en Project Operations:

- Proceso de negocio de cliente potencial a oportunidad
- Proceso de venta de la oportunidad

El proceso de negocio de cliente potencial a oportunidad comprende las etapas siguientes:

| Nombre de la fase | Entidad mapeada | Funcionalidad |
| --- | --- | --- |
| Calificar | Cliente potencial | Calificar el cliente potencial para crear una cuenta, un contacto y una oportunidad. |
| Desarrollar | Oportunidad | Desarrolle la oportunidad para agregar más información sobre el trabajo involucrado, las partes interesadas clave y la competencia. |
| Proponer | Oportunidad | Desarrolle la propuesta y obtenga la aprobación del equipo de revisión interno. |
| Cerrada | Oportunidad | Gane la oportunidad de cerrar la oferta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]