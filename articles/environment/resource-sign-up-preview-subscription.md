---
title: Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias
description: Este tema proporciona información sobre cómo suscribir e implementar Project Operations para escenarios basados en recursos/no en existencias.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085034"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema explica cómo suscribirse a la oferta de vista previa/partner y cómo implementar el entorno de Project Operations para escenarios basados en recursos/no en existencias.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico invitándole a participar en la vista previa. Puede solicitar una vista previa en el [Sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.
- La implementación de un entorno de Finance requiere una suscripción de Azure válida que se facturará por entorno. Puede utilizar la suscripción existente de su organización o utilizar una [Prueba de Azure](https://azure.microsoft.com/en-us/free/) para empezar. El entorno CDS se proporcionará de forma gratuita durante un período limitado de 30 días.

## <a name="subscribe"></a>Suscribirse

Cuando se apruebe su [solicitud de vista previa](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá tres ofertas de Microsoft por correo electrónico. Estas ofertas le permiten implementar la Vista previa de Project Operations:

- Dynamics 365 Project Operations (CRM): prueba de Vista previa
- Office 365 Project Operations: prueba de Vista previa
- Dynamics 365 Finance - Prueba de versión preliminar

> [!IMPORTANT]
> Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM): prueba de Vista previa 

Antes de comenzar, asegúrese de haber iniciado sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea la vista previa de Project Operations.

1. Canjee el primer código de oferta, **Dynamics 365 Project Operations (CRM): versión preliminar de prueba** pegándolo en la URL del navegador.

![Canjear oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme su pedido.

![Confirmar el pedido](./media/17ConfirmOrderNew.png)

Verá que la oferta de confirmación se canjeó correctamente.

![Confirmación](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations: prueba de Vista previa

Repita los mismos pasos que con el primer código de oferta. Asegúrese de agregar el segundo código de oferta con la misma cuenta de usuario que se utilizó con el primer código de oferta.

### <a name="dynamics-365-finance-preview-trial"></a>Prueba de versión preliminar de Dynamics 365 Finance

Repita los mismos pasos con la última oferta del correo electrónico de bienvenida.

## <a name="assign-licenses"></a>Asignación de licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.

1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.

![Página principal del Centro de administración](./media/14AdminPortal.png)

2. En la página **Usuarios activos** , seleccione los usuarios a los que desea asignar una licencia.

![Asignar licencias](./media/15AssignLicenses.png)

3. Verifique que las licencias **Vista previa de Dynamics 365 Project Operations (CRM)** y **Office 365 Project Operations: vista previa** se han seleccionado y seleccione **Guardar cambios**.

> [!NOTE]
> No es necesario asignar la oferta de prueba de Finance a un usuario.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un nuevo proyecto en LCS

Cree un nuevo proyecto LCS como se describe en el tema [Iniciar un nuevo proyecto en LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Agregar una suscripción de Azure a un proyecto LCS

Para completar esta tarea, siga los pasos del tema [Agregar una suscripción de Azure a proyecto LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar el entorno de demostración de Finance con Project Operations para escenarios de recursos/no en existencias

Siga las instrucciones del tema [Aprovisionar un nuevo entorno](resource-provision-new-environment.md) para completar la implementación. Utilizar el tipo de implementación de [entorno de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para la versión preliminar. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalar la configuración de CDS y los datos de configuración

Instale los datos de instalación y configuración de CDS como se describe en el tema [Configurar y aplicar datos de configuración en Common Data Service](resource-apply-pro-setup-config-data.md).
Complete este paso solo después de que se implemente el entorno de demostración de Finanzas y los datos de demostración en FO estén listos.
