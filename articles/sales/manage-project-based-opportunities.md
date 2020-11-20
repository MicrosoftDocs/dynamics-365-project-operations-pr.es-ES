---
title: Administrar oportunidades basadas en proyectos
description: Este tema proporciona información sobre cómo trabajar con oportunidades relacionadas con proyectos.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5a8bfea5540432a62d7075443cf237571bfa4de
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118494"
---
# <a name="manage-project-based-opportunities"></a>Administrar oportunidades basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las empresas basadas en proyectos suelen tener sus operaciones de entrega repartidas en varios países y geografías. El costo de ejecución y entrega del proyecto puede variar según la geografía o división que gestiona la entrega. A su vez, esto puede afectar los márgenes del trato. La prestación de servicios basados en proyectos generalmente implica una gran cantidad de tiempo de recursos humanos, gastos considerables de viaje, costos de materiales y otros gastos.

Las oportunidades basadas en proyectos en Dynamics 365 Project Operations están diseñadas con extensiones a Dynamics 365 Sales. El tema proporciona detalles sobre los diferentes campos y la lógica empresarial incluidos en la funcionalidad adicional que requieren las empresas basadas en proyectos para gestionar oportunidades basadas en proyectos.

## <a name="view-all-project-based-opportunities"></a>Ver todas las oportunidades basadas en proyectos

Se puede ver una lista de todas las oportunidades basadas en proyectos en la página de lista **Oportunidad**. 

1. Vaya a **Ventas** > **Oportunidades**.
2. Use **Ver conmutador** para seleccionar otras vistas filtradas de las oportunidades. Puede crear sus propias vistas con criterios de filtro personalizados para configurar estas vistas y opciones de navegación.

Las oportunidades de proyecto se pueden crear o eliminar de esta página de lista o de la página de detalles.

## <a name="business-process-flow-for-project-based-deals"></a>Flujo de proceso de negocio para ofertas basadas en proyectos

Los siguientes flujos de procesos de negocio son compatibles con ofertas basadas en Project Operations:

- Proceso de negocio de cliente potencial a oportunidad
- Proceso de venta de la oportunidad

### <a name="lead-to-opportunity-business-process"></a>Proceso de negocio de cliente potencial a oportunidad 
El proceso de negocio de cliente potencial a oportunidad comprende las etapas siguientes:

| Fase | Entidad mapeada | Funcionalidad |
| --- | --- | --- |
| Calificar | Cliente potencial | Calificar el cliente potencial para crear una cuenta, un contacto y una oportunidad. |
| Desarrollar | Oportunidad | Desarrolle la oportunidad de agregar más información sobre el trabajo involucrado, las partes interesadas clave y la competencia. |
| Proponer | Oportunidad | Desarrolle la propuesta y obtenga la aprobación del equipo de revisión interno. |
| Cerrada | Oportunidad | Gane la oportunidad de cerrar la oferta. |

### <a name="opportunity-sales-process"></a>Proceso de venta de la oportunidad
El proceso de ventas de Oportunidades en Project Operations es una extensión del flujo de negocios del proceso de ventas de Oportunidades en la aplicación Sales. Este proceso comercial está diseñado de manera inmediata para respaldar las siguientes etapas en una oportunidad basada en proyectos.

| Fase | Entidad mapeada | Funcionalidad |
| --- | --- | --- |
| Calificar | Oportunidad | Calificar el cliente potencial para crear una cuenta, un contacto y una oportunidad. |
| Proponer | Oferta | Desarrolle la propuesta usando cotizaciones de proyecto y obtenga la aprobación del equipo de revisión interno. |
| Contrato | Contrato de proyecto | Gana la cotización para crear el contrato y comenzar la ejecución y entrega del proyecto. |
| Cerrada | Contrato de proyecto | Termina el trabajo con éxito y cierra el contrato del proyecto. |

> [!NOTE]
> Si su acuerdo basado en proyecto comenzó con un cliente potencial, el proceso de negocio de cliente potencial a la oportunidad tiene prioridad.
>
> Si su acuerdo basado en proyecto comenzó con una Oportunidad, el proceso de venta de Oportunidad la oportunidad tiene prioridad.

Puede editar el producto flujo de proceso de negocio o crear sus propios flujos de procesos comerciales para realizar un seguimiento de su proceso de ventas según sea necesario. Para obtener más información acerca de los flujos de proceso de negocio, consulte [Información general sobre flujos de proceso de negocio](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).