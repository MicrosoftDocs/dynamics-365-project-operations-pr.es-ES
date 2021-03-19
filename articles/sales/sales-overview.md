---
title: Información general del proceso de venta
description: En este tema se proporciona información sobre procesos de ventas básicos.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277404"
---
# <a name="sales-process-overview"></a>Información general del proceso de venta

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los procesos de ventas que se usan en una organización basada en proyecto difieren de los procesos de ventas que se usan en una organización basada en producto. Esta se debe a que los ciclos de ventas de las organizaciones basadas en proyecto son más largos y requieren técnicas de estimación personalizadas para analizar y crear ofertas para cada operación. Dynamics 365 Project Operations utiliza algunas de las siguientes funciones que se utilizan en un proceso de ventas:

- Se utiliza un registro de cliente potencial para realizar un seguimiento del proceso de ventas.
- El seguimiento de los clientes potenciales en calificación se realiza como oportunidades.
- Todos los artefactos relacionados para una oportunidad están accesibles. Estos artefactos incluyen el equipo de ventas, las partes interesadas, la probabilidad, la clasificación, las fases de ventas y los procesos de negocio.
- Se crean varias ofertas para una oportunidad.
- Se otorga a una cita el estado **Cerrada como ganada** para crear un pedido de ventas. En Project Operations, el pedido de ventas se personaliza y se denomina contrato de proyecto.

## <a name="estimate-a-sale"></a>Estimar una venta
El valor de una venta se puede estimar en función de los proyectos que se han entregado anteriormente y de la complejidad de los proyectos. Puede utilizarse un proceso de estimación más sencillo para proyectos que implican extensiones a proyectos anteriores, o bien proyectos en los que el proveedor posee una amplia experiencia y se utilizan plantillas de trabajo conocidas. Los proyectos más complejos suelen tener un proceso de compra más largo. Por lo tanto, existen más fases en el proceso de estimación de ventas. Al principio del proceso, el equipo de ventas utiliza los aportes de los administradores de cuentas y expertos en el tema (SME) para crear una estimación general para cada componente de trabajo distinto que se oferta. Estos componentes de trabajo se representan mediante líneas de oferta. 

Puede crear una estimación general de la oferta. Finalmente, esta estimación general se reemplazará por una estimación más detallada basada en un plan de proyecto creado mediante plantillas de proyecto estandarizadas. Estas plantillas le ayudan a crear una programación y a determinar los valores monetarios de la oferta y sus componentes (líneas de oferta). 

Puede crear varias ofertas para un proyecto y agruparlas en un único registro de oportunidad. Finalmente, una de las ofertas se marcará como **Cerrada como ganada** y se creará un contrato de proyecto o una declaración de trabajo (SOW). El contrato de proyecto contiene el valor contratado de cada componente (línea de contrato) que el cliente acepta para su entrega. Las SOW se suelen crear como documentos de Microsoft Word. Todas las facturas que se envían al cliente durante la entrega del proyecto hacen referencia al contrato del proyecto o la SOW.

También puede crear ofertas alternativas bajo un registro de oportunidad, o bien configurar el sistema para crear un contrato de proyecto cuando se gana una oferta. En este caso, puede adjuntar al registro de contrato del proyecto un documento de Word que represente la SOW.

## <a name="configure-the-sales-process"></a>Configurar el proceso de ventas
Puede usar los flujos de proceso de negocio para configurar el proceso de ventas. Estos flujos proporcionan una interfaz visual guiada para hacer avanzar los tratos por las etapas del proceso de ventas.

Por ejemplo, su compañía podría tener las seis fases que se indican a continuación en el proceso de ventas:

1. Calificar
2. Estimación
3. Revisión interna
4. Contrato
5. Entregar
6. Cerrada
 
Su organización puede usar distintas entidades para representar la misma operación a medida que evoluciona. Al principio del proceso de ventas, una operación se representa con la entidad Oportunidad. A medida que pasa el tiempo y afloran más detalles, puede utilizar estimaciones generales para crear una o varias ofertas. Si las partes interesadas del cliente e internas revisan una de dichas ofertas, la operación pasa a representarse con la entidad Oferta. Cuando el cliente acepta la oferta, la operación pasa a representarse con un contrato de proyecto o una SOW. Para facilitar este comportamiento, los BPF se estructuran de manera a que cada fase del proceso esté vinculada a una tabla de base de datos distinta.

La fase **Calificar** del proceso de ventas se puede respaldar con la entidad Oportunidad. Las fases **Estimar** y **Revisión interna** se pueden respaldar con la entidad Oferta. Las fases **Contrato**, **Entrega** y **Cerrar** Se pueden respaldar con la entidad Contrato de proyecto.

A medida que las operaciones pasen por las distintas fases, se le pedirá que cree el registro de entidad correspondiente como ayuda y guía durante el proceso. Las fases pueden ser condicionales. Por ejemplo, si necesita una revisión interna de una oferta solo si la oferta usa una lista de precios personalizada, puede configurar la condición en la fase adecuada del proceso de negocio. La fase **Revisión interna** solo se muestra para las ofertas que utilizan una lista de precios personalizada. Para el resto de operaciones y ofertas, la fase **Estimación** va seguida de la fase **Contrato**.

> [!NOTE]
> Project Operations tiene páginas específicas para registros de entidad de Oportunidad, Oferta, Pedido y Factura. Debe crear estos registros utilizando las páginas de información del proyecto para estas entidades. De lo contrario, no podrá abrir los registros desde la página **Información del proyecto**. Si desea abrir un registro desde la página **Información del proyecto**, debe eliminar el registro y volver a crearlo utilizando la página **Información del proyecto** donde la lógica de negocios para cada uno de estos tipos de entidad garantiza que el campo **Tipo** del registro se establece correctamente, y todos los conceptos obligatorios se inicializan correctamente.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Realizar un seguimiento de revisiones de ofertas y planes de proyecto en el ciclo de ventas
En Project Operations, no es posible realizar seguimientos de las revisiones de ofertas. En su lugar, debe marcar la oferta existente como **Cerrada como perdida** y crear una nueva oferta. Puede copiar una oferta o clonar una oferta basada en proyecto.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Realizar un seguimiento de comentarios y aprobaciones de ofertas y contratos de proyecto
Puede administrar la revisión y la aprobación de ofertas y contratos de proyecto mediante el muro de registros y las publicaciones. Su organización puede crear flujos de trabajo personalizados y complementos para asignar, redirigir, remitir a instancias superiores y administrar notificaciones de revisiones y la aprobación de elementos de trabajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]