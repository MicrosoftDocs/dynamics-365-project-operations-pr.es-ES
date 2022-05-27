---
title: Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias
description: Este tema proporciona información sobre cómo suscribir e implementar Project Operations para escenarios basados en recursos/no en existencias.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575831"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_



Este tema explica cómo suscribirse a la oferta de prueba e implementar el entorno de Project Operations para escenarios basados en recursos/no mantenidos en existencias.

## <a name="prerequisites"></a>Requisitos previos
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure. Puede crear un inquilino durante el primer caje de oferta. 
- La implementación de un entorno de Finance requiere una suscripción de Azure válida que se facturará por entorno. Puede utilizar la suscripción existente de su organización o utilizar una [Prueba de Azure](https://azure.microsoft.com/free/) para empezar. El entorno CDS se proporcionará de forma gratuita durante un período limitado de 30 días.

> [!IMPORTANT]
> Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.
> 
> Las pruebas son de un solo uso en el inquilino. Solo puede ejecutar una prueba una vez. Le recomendamos que cree un nuevo inquilino para la prueba.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Prueba preliminar 

Antes de comenzar, asegúrese de haber iniciado sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea la vista previa de Project Operations.

1. Cajee el primer código de oferta de **Dynamics 365 Project Operations** aquí [Prueba de Projectos Operations](https://aka.ms/try-po).
2. Confirme su pedido.

  Verá que la oferta de confirmación se canjeó correctamente.

### <a name="dynamics-365-finance-preview-trial"></a>Prueba preliminar de Dynamics 365 Finance

Vaya a [Prueba preliminar de Dynamics 365 for Finance](https://aka.ms/trypoche) y repita los pasos de la sección anterior con la oferta: Registrarse para el entorno alojado en la nube.  

## <a name="assign-licenses"></a>Asignación de licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.

1. Vaya a [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.

2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.

3. Verifique que la licencia de **Dynamics 365 Project Operations** ha sido seleccionada y seleccione **Guardar cambios**.

> [!NOTE]
> No es necesario asignar la oferta de prueba de Finance a un usuario.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un nuevo proyecto en LCS

Cree un nuevo proyecto LCS como se describe en el tema [Iniciar un nuevo proyecto en LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Agregar una suscripción de Azure a un proyecto LCS

Para completar esta tarea, siga los pasos del tema [Agregar una suscripción de Azure a proyecto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar el entorno de demostración de Finance con Project Operations para escenarios de recursos/no en existencias

Siga las instrucciones del tema [Aprovisionar un nuevo entorno](resource-provision-new-environment.md) para completar la implementación. Utilizar el tipo de implementación de [entorno de demostración](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para la versión preliminar. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar la configuración de CDS y los datos de configuración

Instale los datos de instalación y configuración de CDS como se describe en el tema [Configurar y aplicar datos de configuración en Common Data Service](resource-apply-pro-setup-config-data.md).
Complete este paso solo después de que se implemente el entorno de demostración de Finance y los datos de demostración estén listos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
