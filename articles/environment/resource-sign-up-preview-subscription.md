---
title: Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias
description: Este tema proporciona información sobre cómo suscribir e implementar Project Operations para escenarios basados en recursos/no en existencias.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949092"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Regístrese para obtener suscripciones de vista previa de Project Operations para escenarios de recursos/no en existencias

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema explica cómo suscribirse a la oferta de vista previa/partner y cómo implementar el entorno de Project Operations para escenarios basados en recursos/no en existencias.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico invitándole a participar en la vista previa. Puede solicitar una vista previa en el [Sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.
- La implementación de un entorno de Finance requiere una suscripción de Azure válida que se facturará por entorno. Puede utilizar la suscripción existente de su organización o utilizar una [Prueba de Azure](https://azure.microsoft.com/en-us/free/) para empezar. El entorno CDS se proporcionará de forma gratuita durante un período limitado de 30 días.

## <a name="subscribe"></a>Suscribirse

Cuando se apruebe su [solicitud de vista previa](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dos ofertas de Microsoft por correo electrónico. Estas ofertas le permiten implementar la Vista previa de Project Operations:

- Dynamics 365 Project Operations: prueba de Vista previa
- Prueba de Vista previa de Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: prueba de Vista previa

1. Canjee la primera oferta, **Prueba de Dynamics 365 Project Operations**, con la URL proporcionada en su correo electrónico de bienvenida.

![Primera oferta](./media/1FirstOffer.png)

2. Verifique que haya iniciado sesión como el usuario que pertenece a la organización que se suscribirá al servicio.
3. Proceda a canjear la oferta. 
4. Seleccione **Si, agregar a mi cuenta**.

![Canjear oferta](./media/2RedeemFirstOffer.png)

![Confirmar oferta](./media/3ConfirmFirstOffer.png)

![Oferta canjeada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Prueba de versión preliminar de Dynamics 365 Finance

Repita los mismos pasos con la segunda oferta del correo electrónico de bienvenida.

## <a name="assign-licenses"></a>Asignar licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Office 365 de la organización para completar los siguientes pasos.

1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar licencias a sus usuarios.

![Portal de administración de Office](./media/5OfficeAdminPortal.png)

2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.

![Asignar licencias](./media/6AssignLicenses.png)

3. Verifique que se haya seleccionado la licencia de Project Operations y seleccione **Guardar cambios**. 

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

