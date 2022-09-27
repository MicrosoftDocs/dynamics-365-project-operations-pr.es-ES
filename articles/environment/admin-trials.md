---
title: Registrarse para pruebas de Project Operations
description: Este artículo ofrece información sobre el procedimiento de implementar una prueba de Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 60790d83d5fcc8c75fef8eac2877d1ca14a761f2
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528041"
---
# <a name="sign-up-for-project-operations-trials"></a>Registrarse para pruebas de Project Operations 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos en existencias, implementación Lite - trato a facturación proforma y Project Operations para escenarios basados en existencias/producción_ 



Este artículo explica cómo suscribirse a la oferta de versión preliminar para socios e implementar un entorno de Dynamics 365 Project Operations.

Con la nueva versión de prueba de Project Operations, puede implementar automáticamente cualquiera de los tres escenarios de implementación admitidos, completando un cuestionario que recomienda el mejor enfoque de implementación. En este artículo se proporciona información sobre cómo:

- Canjear su oferta de prueba.
- Iniciar el aprovisionamiento.
- Configurar la escritura dual.
- Más información sobre Project Operations. 

La siguiente tabla describe los detalles de la nueva oferta de prueba.

| **Artículo de oferta**               | **Detalles**                                  |
|------------------------------|----------------------------------------------|
| Tipo de oferta                   | Este tipo de oferta es de cliente potencial de administrador, por lo que se requiere un administrador de inquilinos para canjear. |
| Uso de la oferta                    | Una vez por inquilino                          |
| Duración de la oferta               | 30 días naturales                             |
| Canjes por inquilino       | 1                                            |
| Extensión                    | 1 extensión, 30 días naturales               |
| Número de entornos de prueba | 3                                            |


## <a name="admin-trial-details"></a>Detalles de la prueba de administrador
La siguiente tabla enumera los detalles de la prueba y cómo se aplican a cada tipo de implementación.

| **Artículo**                      | **Simplificada**                                     | **Materiales no mantenidos en existencias** | **Materiales mantenidos en existencias** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Datos de configuración proporcionados           | Sí                                          | Sí                       | Sí (USSI)            |
| Datos transaccionales            | No                                           | No                        | No                    |
| Tiempo de aprovisionamiento en minutos  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Requisitos previos
Para comenzar una implementación de Dynamics 365 Project Operations, los requisitos previos siguientes son necesarios.

- Registrarse para la [Prueba de versión preliminar de Dynamics 365 Project Operations](https://www.aka.ms/try-po).
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure.

> [!IMPORTANT]
> Solo una persona en una organización, el inquilino Administrador, necesita realizar esta tarea. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.

### <a name="dynamics-365-project-operations---preview-trial"></a>Prueba de versión preliminar de Dynamics 365 Project Operations 

Antes de comenzar, inicie sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea obtener la versión preliminar de Project Operations.

1. Canjee el primer código de oferta, **Prueba de versión preliminar de Dynamics 365 Project Operations** pegándolo en la dirección URL del navegador.

    ![Canjear oferta](./media/16RedeemFirstOfferNew.png)

2. Confirme su pedido.

    ![Confirmar el pedido](./media/17ConfirmOrderNew.png)

  Verá que la oferta de confirmación se canjeó correctamente.

   ![Confirmación](./media/18OrderConfirmationNew.png)

  Se le redirigirá al [Centro de administración de Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Cuestionario y aprovisionamiento

1.  Vaya al [Centro de administración de Power Platform](https://admin.powerplatform.com/projectoperationstrial) y rellene el cuestionario.  
2.  Revise el tipo de implementación recomendado y seleccione **Comenzar la configuración** para iniciar el aprovisionamiento.
3.  Revise los términos y condiciones y, a continuación, seleccione **Iniciar**.

   Una vez que se inicia el aprovisionamiento, se le redirige a la lista de entornos en el centro de administración de Power Platform. Mientras el aprovisionamiento está en progreso, el estado de su entorno es **PreparingInstance**.
 
  Cuando se completa el aprovisionamiento, el estado de su entorno es **Listo**. El aprovisionamiento del entorno incluye la implementación de datos de demostración.
 
4.  Seleccione las correspondientes URL de Microsoft Dataverse y las URL de aplicaciones de finanzas y operaciones para validar la implementación.

## <a name="configuring-dual-write"></a>Configuración de la escritura dual
- Para configurar roles de seguridad para escritura dual, consulte [Actualice la configuración de seguridad en Project Operations en Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Para acceder a la configuración de doble escritura, navegue a la instancia de finanzas y operaciones, luego navegue a **Gestión de datos** > **Doble escritura**.
- Para configurar mapas de escritura dual, consulte [Ejecutar mapas de escritura dual de Project Operations](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Asignación de licencias

Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.

1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.

   ![Página principal del Centro de administración](./media/14AdminPortal.png)

2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.

   ![Asignar licencias](./media/15AssignLicenses.png)

3. Verifique que la licencia de **Versión preliminar de Dynamics 365 Project Operations** se ha seleccionado y seleccione **Guardar cambios**.

## <a name="additional-resources"></a>Recursos adicionales

Los siguientes recursos brindan una guía útil al comenzar su viaje con Project Operations:

- [Serie de videos: descripción general de Project Operations, características detalladas y hoja de ruta](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/training/modules/examine-dynamics-365-project-operations/)
- [Determinar el tipo de implementación](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Preguntas frecuentes

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>¿Qué sucede si necesito ALM o ELM para mi entorno de aplicaciones de finanzas y operaciones?

- Para los partners que requieren capacidades de gestión del ciclo de vida del entorno completo, consulte la [Solicitud de licencia de espacio aislado para partners](https://experience.dynamics.com/requestlicense) para revisar la nueva oferta de socios. 
- Para los socios que buscan más información sobre los derechos de uso interno, consulte [Beneficio de software y nube de derechos de uso interno (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>¿Puedo extender mi prueba más allá de 30 días?
Para extender su prueba, complete los siguientes pasos.

1. En el **Centro de administración de Microsoft 365**, vaya a **Facturación** > **Sus productos**.
2. Seleccione **Prueba de versión preliminar de Dynamics 365 Project Operations**.
3. En **Fecha de expiración**, seleccione **Ampliar fecha**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>¿Puedo actualizar de la implementación simplificada a la implementación de escenario basada en recursos/sin mantenimiento de existencias?
Actualmente, no hay soporte para actualizar un entorno de una implementación simplificada a una implementación sin mantenimiento en existencias.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>¿Puedo acceder a Lifecycle Services (LCS) para mis entornos de Finance?  
N.º Para estas pruebas, la implementación se maneja a través del Centro de administración de Power Platform. El acceso al entorno de Finance está restringido.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>¿Puedo instalar mi versión de prueba en un entorno existente?
Si tiene un entorno existente, se le permitirá instalar la implementación simplificada en un entorno de ventas existente de Dataverse desde el Centro de administración de Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
