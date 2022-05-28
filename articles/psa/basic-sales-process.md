---
title: Procesos de venta
description: En este tema se proporciona información sobre los procesos de ventas básicos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bec8718e287500a7cbc778dc32758e793be8dc3b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580339"
---
# <a name="sales-processes"></a>Procesos de venta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Los procesos de ventas que se usan en una organización basada en proyecto difieren de los procesos de ventas que se usan en una organización basada en producto. Esta diferencia se produce porque los ciclos de ventas de las organizaciones basadas en proyecto son más largos y requieren técnicas de estimación personalizadas para analizar y crear ofertas para cada operación. Dynamics 365 Project Service Automation usa parte de la misma funcionalidad que se usa en el proceso de ventas de Dynamics 365 Sales. A continuación, encontrará algunos ejemplos:

- Se utiliza la entidad Cliente potencial para realizar un seguimiento del proceso de ventas.
- El seguimiento de los clientes potenciales en calificación se realiza como oportunidades. El proceso de ventas también puede empezar con una oportunidad.
- Se accede a todos los artefactos relacionados con las oportunidades. Entre estos artefactos se incluyen el equipo de ventas, las partes interesadas, la probabilidad, la valoración, las fases de ventas y los procesos de negocio.
- Se crean varias ofertas para una oportunidad.
- Una cita se marca como **Cerrada como ganada** para crear un pedido pedido de ventas. En PSA, el pedido de ventas se personaliza y se denomina contrato de proyecto.

La ilustración siguiente muestra un proceso de ventas típico en una organización basada en proyecto.

> ![Proceso de ventas en una organización basada en proyecto.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimación de una venta
El valor de una venta se puede estimar en función de los proyectos que se han entregado anteriormente y de la complejidad de los proyectos. Puede utilizarse un proceso de estimación más sencillo para proyectos que implican extensiones a proyectos anteriores, o bien proyectos en los que el proveedor posee una amplia experiencia y se utilizan plantillas de trabajo conocidas. Los proyectos más complejos suelen tener un proceso de compra más largo. Por lo tanto, existen más fases en el proceso de estimación de ventas. Al principio del proceso, el equipo de ventas utiliza los aportes de los administradores de cuentas y expertos en el tema (SME) para comenzar a crear una estimación general para cada componente de trabajo distinto que se oferta. Estos componentes de trabajo se representan mediante líneas de oferta. 

Puede crear una estimación general de la oferta. Finalmente, esta estimación general se reemplazará por una estimación más detallada basada en un plan de proyecto creado mediante plantillas de proyecto estandarizadas. Estas plantillas le ayudan a crear una programación y a determinar los valores monetarios de la oferta y sus componentes (líneas de oferta). 

Puede crear varias ofertas para un proyecto y agruparlas en un único tipo de entidad de oportunidad. Finalmente, una de estas ofertas se marcará como **Cerrada como ganada** y se creará un contrato de proyecto o una declaración de trabajo (SOW). El contrato de proyecto contiene el valor contratado de cada componente (línea de contrato) que el cliente acepta para su entrega. Las SOW se suelen crear como documentos de Microsoft Word. Todas las facturas que se envían al cliente durante la entrega del proyecto hacen referencia al contrato del proyecto o la SOW.

También puede crear ofertas alternativas bajo un tipo de entidad de oportunidad, o bien configurar el sistema para crear un contrato de proyecto cuando se gana una oferta. En este caso, puede adjuntar al registro de contrato del proyecto un documento de Word que represente la SOW.

![Cierre de una oferta para crear un contrato de proyecto.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configuración del proceso de ventas
Puede usar los flujos de proceso de negocio (BPF) en Microsoft Dynamics 365 para configurar el proceso de ventas. Los BPF ofrecen al personal de ventas una interfaz visual guiada que se puede utilizar para mover operaciones por las distintas fases típicas de su compañía.

Por ejemplo, su compañía podría tener las seis fases que se indican a continuación en el proceso de ventas:

1. Calificar
2. Estimación
3. Revisión interna
4. Contrato
5. Entregar
6. Cerrar

Estas seis fases se representan con cheurones (\>) que se pueden seleccionar para expandirlas en cada tipo de entidad de oportunidad que se cree.

![Configuración del proceso de negocio en Dynamics 365.](media/basic-guide-3.png)
 
Su organización puede usar distintas entidades para representar la misma operación a medida que evoluciona. Al principio del proceso de ventas, una operación se representa con la entidad Oportunidad. A medida que pasa el tiempo y afloran más detalles, puede utilizar estimaciones generales para crear una o varias ofertas. Si las partes interesadas del cliente e internas revisan una de dichas ofertas, la operación pasa a representarse con la entidad Oferta. Cuando el cliente acepta la oferta, la operación pasa a representarse con un contrato de proyecto o una SOW. Para facilitar este comportamiento, los BPF se estructuran de manera a que cada fase del proceso esté vinculada a una tabla de base de datos distinta.

La fase **Calificar** del proceso de ventas se puede respaldar con la entidad Oportunidad. Las fases **Estimar** y **Revisión interna** se pueden respaldar con la entidad Oferta. Las fases **Contrato**, **Entrega** y **Cerrar** Se pueden respaldar con la entidad Contrato de proyecto.

A medida que las operaciones pasen por las distintas fases, se le pedirá que cree el registro de entidad correspondiente como ayuda y guía durante el proceso. Las fases pueden ser condicionales. Por ejemplo, si necesita una revisión interna de una oferta solo si la oferta usa una lista de precios personalizada, puede configurar la condición en la fase adecuada del proceso de negocio. La fase **Revisión interna** solo se muestra para las ofertas que utilizan una lista de precios personalizada. Para el resto de operaciones y ofertas, la fase **Estimación** va seguida de la fase **Contrato**.

> [!NOTE]
> PSA cuenta con páginas específicas para las entidades Oportunidad, Oferta, Pedido y Factura. Debe crear oportunidades, ofertas, pedidos y facturas de servicios de proyecto mediante las páginas de información de proyecto de dichas entidades. Si usa otra página para crear un registro, no podrá abrir el registro desde la página **Información de proyecto**. Si desea abrir un registro desde la página **Información de proyecto**, debe eliminar el registro y volver a crearlo mediante la página **Información de proyecto**. En la página **Información de proyecto**, la lógica de negocios de cada uno de estos tipos de entidad garantiza que el campo **Tipo** del registro esté configurado correctamente y que todos los conceptos obligatorios se inicialicen correctamente.

> ![Información del proyecto para un nuevo pedido.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferencias entre Project Service Automation y Ventas
Aunque el proceso de ventas de PSA usa las capacidades básicas del proceso de ventas de Ventas, este tiene algunas diferencias clave que se deben a las variaciones en las prácticas de negocio de las organizaciones basadas en proyecto. A continuación, encontrará algunos ejemplos:

- **Ofertas de proyecto**: en Project Service Automation, una oferta se cierra después de crear un contrato de proyecto a partir de una oferta. En Ventas, se puede mantener una oferta abierta después de ganarla. La razón de esta diferencia es que la coincidencia entre una oferta y un contrato de proyecto es mejor para las organizaciones basadas en proyecto. 
- **Activación y revisiones**: en PSA, la activación y las revisiones no son compatibles con las ofertas de proyecto. En Ventas, una oferta se puede bloquear para evitar ediciones adicionales.
- **Cierre de una oferta como perdida o ganada**: en PSA, cuando una oferta de proyecto se cierra como ganada o perdida, la oportunidad permanece abierta. Todas las demás ofertas de la oportunidad se cierran como perdidas. En Ventas, cuando una oferta se cierra como ganada o perdida, se solicita al usuario que realice una acción en la oportunidad. Dependiendo de la entrada del usuario, la oportunidad subyacente se puede cerrar o dejar abierta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Seguimiento de revisiones de ofertas y planes de proyecto en el ciclo de ventas
En PSA, no es posible realizar seguimientos de las revisiones de ofertas. En su lugar, debe marcar la oferta existente como **Cerrada como perdida** y crear una nueva oferta. Puede copiar una oferta o clonar una oferta basada en proyecto con PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Seguimiento de comentarios y aprobaciones de ofertas y contratos de proyecto
Puede administrar la revisión y la aprobación de ofertas y contratos de proyecto mediante el muro de registros y las publicaciones. Su organización puede crear flujos de trabajo personalizados y complementos para asignar, redirigir, remitir a instancias superiores y administrar notificaciones de los elementos de trabajo de revisión y aprobación.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
