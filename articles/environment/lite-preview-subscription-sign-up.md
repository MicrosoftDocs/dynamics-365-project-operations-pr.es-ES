---
title: Suscribirse para una suscripción de vista previa
description: 'Este tema proporciona información sobre cómo suscribirse y realizar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949089"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Regístrese para obtener una suscripción de vista previa para implementación simplificada: de oferta a facturación proforma

Este tema explica cómo suscribirse a la oferta de partners de vista previa e implementar de forma simplificada Dynamics 365 Project Operations: de oferta a facturación proforma.

> [!NOTE]
> Este proceso cambiará en las próximas versiones de Project Operations.

## <a name="prerequisites"></a>Requisitos previos

- Recibirá un correo electrónico invitándole a participar en la vista previa. Puede solicitar una vista previa en el [Sitio web de Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.
- El usuario que implemente la vista previa necesitará un número de teléfono y una tarjeta de crédito válida. Durante la suscripción, no habrá cargos a la tarjeta durante seis meses. Después de seis meses, debe cancelar la suscripción. 
- Revise todos los términos y condiciones.

## <a name="subscribe"></a>Suscribirse

Cuando recibe una aprobación de [solicitud de vista previa](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), recibirá dos ofertas de Microsoft por correo electrónico. Estas ofertas le permiten implementar la Vista previa de Project Operations:

- Prueba de vista previa de preliminar de Dynamics 365 Customer Service: código de un solo uso
- Dynamics 365 Project Operations: versión de vista previa

### <a name="dynamics-365-customer-service-paid-offer"></a>Oferta de pago de Dynamics 365 Customer Service

1. Con una ventana de explorador InPrivate/Incognito, canjee el primer código de oferta de Dynamics 365 Customer Service. Para registrarse en Customer Service, necesitará:

- Un número de teléfono
- Una tarjeta de crédito. Al suscribirse, no habrá cargos a la tarjeta durante seis meses. Después de seis meses, debe cancelar la suscripción.
- Revise todos los términos y condiciones.

2. Facilite su información de contacto.

![Información de contacto](./media/1ContactInformation.png)

3. Proporcione los detalles del nuevo inquilino.

![Crear Id. de usuario](./media/2CreateUserID.png)

4. Verifique su identidad, guarde su nueva Id. de usuario y luego seleccione **Configurar**.

![Guardar información](./media/3SaveInfo.png)

5. Complete el registro de la tarjeta de crédito y revise todos los términos y condiciones. 

![Completar tarjeta de crédito](./media/4CompleteCreditCard.png)

![Pago final con tarjeta de crédito](./media/5CreditCardCheckout.png)

![Guardar pedido](./media/6SaveOrder.png)

![Confirmación de tarjeta de crédito](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Cancelar la oferta empresarial de Dynamics 365 Customer Service

La oferta empresarial de Dynamics 365 Customer Service se proporciona de forma gratuita durante seis meses. La oferta se renovará a la tarifa completa al final del período de seis meses. Para cancelar antes de la fecha de renovación, complete las siguientes instrucciones. 

> [!NOTE]
> Después de completar estos pasos, ya no podrá utilizar el entorno de versión preliminar pública de Project Operations.

1. Vaya al [Portal de administración](https://admin.microsoft.com/) y, en **Facturación**, seleccione **Sus productos**.

![Portal de administración, página Sus productos](./media/8AdminPortal.png)

2. Seleccione la **Oferta empresarial de Dynamics 365 Customer Service**.

![Cancelar suscripción](./media/9CancelSubscription.png)

3. Seleccione **Configuración** > **Acciones** > **Cancelar suscripción**.
4. En el formulario **Cancelación de suscripción**, introduzca la información en los campos requeridos.
5. Seleccione **Cancelar** > **Suscripción.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: prueba de Vista previa

1. Canjee la segunda oferta, Prueba de Dynamics 365 Project Operations, con la URL proporcionada en su correo electrónico de bienvenida.

![Canjear oferta 2](./media/10RedeemOffer2.png)

2. Verifique que haya iniciado sesión como el usuario que pertenece a la misma organización a la que se suscribió utilizando el primer código de oferta y luego proceda a canjear la oferta. 
3. Seleccione **Si, agregar a mi cuenta**.

![Agregar a cuenta](./media/11AddToAccount.png)

![Pantalla Probar ahora](./media/12TryNow.png)

![Detalles de pedido](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Asignación de licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Office 365 de la organización para completar los siguientes pasos.

1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.

![Página principal del Centro de administración](./media/14AdminPortal.png)

2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.

![Asignar licencias](./media/15AssignLicenses.png)

3. Verifique que se haya seleccionado la licencia de **Customer Service Enterprise** y **Operaciones de proyecto** y seleccione **Guardar cambios**.

## <a name="create-a-new-cds-environment"></a>Crear un nuevo entorno CDS

Aprovisione un nuevo entorno de implementación de CDS de Project Operations siguiendo las instrucciones del tema [Modelo de implementación CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar una configuración CDS y datos de demostración de configuración

Instale la configuración CDS y configure los datos de demostración siguiendo las instrucciones del tema [Aplicar datos de configuración y configuración de demostración](lite-apply-demo-setup-config-data.md).
