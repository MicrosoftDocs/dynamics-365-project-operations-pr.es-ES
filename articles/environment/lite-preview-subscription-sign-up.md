---
title: Registrarse para una suscripción de versión preliminar (lite)
description: 'Este tema proporciona información sobre cómo suscribirse y realizar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997442"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrarse para una suscripción de versión preliminar (lite) 

Este tema explica cómo suscribirse a la oferta de socio de vista previa e implementar Dynamics 365 Project Operations ligero: trato de facturación proforma.

> [!NOTE]
> Este proceso cambiará en las próximas versiones de Project Operations.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico invitándole a participar en la vista previa. Puede solicitar una vista previa en el [Sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.
- Revise todos los términos y condiciones.

## <a name="subscribe"></a>Suscribirse

Cuando recibe una aprobación de [solicitud de vista previa](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dos ofertas de Microsoft por correo electrónico. Estas ofertas le permiten implementar la Vista previa de Project Operations:

- Dynamics 365 Project Operations (CRM): Prueba de versión preliminar
- Office 365 Project Operations: prueba de Vista previa

> [!IMPORTANT]
> Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM): Prueba de versión preliminar 

Antes de comenzar, asegúrese de haber iniciado sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea la vista previa de Project Operations.

1. Canjee el primer código de oferta, **Dynamics 365 Project Operations (CRM): Prueba de versión preliminar** pegándolo en la dirección URL del navegador.

![Canjear oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme su pedido.
![Confirmar el pedido](./media/17ConfirmOrderNew.png)

Verá que la oferta de confirmación se canjeó correctamente.

![Confirmación](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations: prueba de Vista previa

Repita los mismos pasos que con el primer código de oferta. Asegúrese de agregar el segundo código de oferta con la misma cuenta de usuario que se utilizó con el primer código de oferta.

## <a name="assign-licenses"></a>Asignación de licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.


1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.

![Página principal del Centro de administración](./media/14AdminPortal.png)

2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.

![Asignar licencias](./media/15AssignLicenses.png)

3. Verifique que las licencias de **Dynamics 365 Project Operations (CRM) Vista previa** y **Office 365 Project Operations: vista previa** están seleccionadas. 
4. Seleccione **Guardar cambios**.

## <a name="create-a-new-cds-environment"></a>Crear un nuevo entorno CDS

1. Aprovisione un nuevo entorno de implementación de CDS de Project Operations siguiendo las instrucciones del tema [Modelo de implementación CDS](lite-deployment.md). Cuando seleccione el tipo de entorno, asegúrese de utilizar **Prueba (basada en suscripción)**.
![Nuevo entorno](./media/19CreateEnvironment.png)

2. Seleccione la opción **Habilitar aplicaciones de Dynamics 365** y deje **Implementar automáticamente estas aplicaciones** en blanco.  
3. Seleccione **Guardar** para crear el entorno.

![Agregar base de datos](./media/20CreateEnvironment1.png)

4. Una vez creado el entorno, instale la solución **Microsoft Dynamics 365 Project Operations**. 

![Instalación de la solución](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar una configuración CDS y datos de demostración de configuración

Instale la configuración CDS y configure los datos de demostración siguiendo las instrucciones del tema [Aplicar datos de configuración y configuración de demostración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]