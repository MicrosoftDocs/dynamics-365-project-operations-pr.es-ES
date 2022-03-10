---
title: Modelo de seguridad
description: Este tema proporciona información sobre el modelo de seguridad en Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2f283771921504dc29ddcc26ca659d4e151598840339bd8c1a857e8bf5dde9ed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991507"
---
# <a name="security-model"></a>Modelo de seguridad

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations contiene un modelo de seguridad único que permite un modelo de seguridad empresarial basado en roles que colabora con Grupos de Microsoft Office. 


## <a name="security-roles"></a>Roles de seguridad
Las capacidades de front-end de Project Operations incluyen los siguientes roles:

| Rol                          | Descripción                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Administrador de prácticas              | Admite informes entre proyectos.                                                                                                            | Unidad de negocio              |
| Aprobador de proyecto              | Aprueba tiempo y gastos frente a los proyectos.                                                                                                                              | Unidad de negocio |
| Administrador de facturación de proyectos | Crea la propuesta de factura.                                                                                                                                                 | Unidad de negocio |
| Director del proyecto               | Crea el plan del proyecto y solicita recursos.                                                                                                                              | Unidad de negocio |
| Recurso de proyecto              | Miembros del equipo reservables e informar el tiempo.                                                                                                          | Unidad de negocio|
| Administrador de recursos              | Todas las funciones de gestión de recursos, como el cumplimiento de solicitudes y reservas de recursos, se separan para admitir una configuración híbrida de administrador de proyectos + administrador de recursos y un rol de administrador de recursos único y centralizado. | Unidad de negocio |


Microsoft Project para la Web incluye los siguientes roles:

| Rol           | Descripción                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Usuario del proyecto   | Usuario colaborativo del proyecto que puede crear sus propios proyectos y ver cualquier proyecto compartido con ellos. | Usuario   |
| Sistema de proyectos | Rol utilizado para el contexto de la aplicación. Los clientes no deben utilizar este rol del sistema.                                    | Organización |

## <a name="security-enforcement"></a>Refuerzo de seguridad
Las acciones que se realizan a nivel de proyecto se realizan en el contexto del usuario que ha iniciado sesión. Esto significa que para crear, abrir o eliminar un proyecto, el usuario debe tener acceso disponible en CDS. El acceso en CDS puede otorgarse a través de cualquiera de los posibles mecanismos incluidos en la plataforma. Por ejemplo, un usuario con un ámbito mayor puede acceder al proyecto o si se ha realizado una acción explícita para compartir el proyecto que le otorga acceso al usuario.

Es importante tener esto en cuenta al crear proyectos en Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Colaboración de grupo moderna con Project Operations
Project for the Web y Project Operations admiten la colaboración de grupos modernos. Los usuarios agregados al proyecto a través de un grupo pueden editar el plan del proyecto.

Project for the Web agrega usuarios al grupo automáticamente después de la asignación.

Los grupos permiten trabajar en colaboración en los permisos del proyecto y los artefactos de colaboración de apoyo. El siguiente diagrama muestra los eventos y cambios de estado que ocurren durante el proceso de asignación de grupo.

Project Operations no crea un grupo a través de una acción implícita y solo lo hace a través de la acción explícita de pulsar en grupos.

La búsqueda de miembros del grupo en el diálogo **Administración de grupos** se limita a aquellos que están configurados como parte del grupo de seguridad del entorno. Para obtener más información, consulte [Controlar el acceso de usuario a entornos: grupos de seguridad y licencias](/power-platform/admin/control-user-access).

![Modo de grupo.](./media/groupsmode.png)

1. El proyecto lo crea y posee el usuario que lo crea.
2. El propietario del proyecto se actualiza en el equipo.
3. El equipo propietario se asigna al grupo de Office especificado o creado.
4. El propietario original del proyecto se agrega al grupo de Office.

## <a name="deployment-recommendation"></a>Recomendación de implementación
A medida que evolucione el modelo de colaboración del grupo de Office, se agregarán funciones para proporcionar un control más detallado a lo largo del tiempo. Se anima a los clientes que implementan operaciones de Project Operations a día de hoy que se centren en el modelo de seguridad de Microsoft Dynamics 365.

Para obtener más información, consulte [Seguridad en Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations y seguridad de Microsoft Dynamics 365 Finance
Project Operations incluye los roles siguientes:

- Director del proyecto
- Contable de proyecto

Para obtener más información sobre la seguridad en Finance, consulte [Seguridad basada en roles](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]