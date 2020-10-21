---
title: Información general sobre los modos de administración de recursos
description: Este tema proporciona información sobre la funcionalidad de gestión de recursos en las Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930112"
---
# <a name="resource-management-modes-overview"></a>Información general sobre los modos de administración de recursos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Dynamics 365 Project Operations admite dos modos para poder ejecutar el flujo de reserva general. El modo de gestión se define como un parámetro del proyecto y se puede modificar si sus necesidades comerciales cambian.    

## <a name="central-mode"></a>Modo central
Para las organizaciones que centralizan la asignación de recursos a los proyectos, el modo Central proporciona una forma de garantizar que los gerentes de proyecto puedan definir los requisitos de recursos a nivel de proyecto. El cumplimiento de los requisitos de recursos se delega a un administrador de recursos. Los administradores de proyecto pueden aceptar o rechazar los recursos propuestos por el administrador de recursos.

![Modo Central](./media/resource-management-central.png)

Para administrar recursos con el modo Central, consulte:

- [Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos con nombre desde los requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Enviar una solicitud de recursos](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Ejecutar solicitudes de recursos](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Aceptar o rechazar un recurso de proyecto propuesto de una solicitud de recurso](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Modo Híbrido
Para las organizaciones que requieren flexibilidad en la asignación de recursos, el modo híbrido permite tanto a los administradores de proyectos como a los administradores de recursos la capacidad de reservar recursos.

![Modo Híbrido](./media/resource-management-hybrid.png)

Además del proceso del modo Central admitido, consulte los siguientes temas para administrar todos los demás flujos de reserva admitidos en modo Híbrido:

Asignar un recurso directamente a un proyecto:
- [Reservar recursos con nombre que se pueden reservar para un equipo de proyecto y asignar tareas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reservar recursos a partir de requisitos de recursos:
- [Asignar recursos genéricos que se pueden reservar a una tarea y generar requisitos de recurso](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reservar recursos con nombre desde los requisitos de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
