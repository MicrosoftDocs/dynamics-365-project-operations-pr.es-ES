---
title: Registrarse para una suscripción de versión preliminar (lite)
description: 'Este tema proporciona información sobre cómo suscribirse y realizar la implementación simplificada de Project Operations: de oferta a facturación proforma.'
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5ba43ba9f917da068415fb62067ab73433b701139ee07014b6bd8c02612008ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991552"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrarse para una suscripción de versión preliminar (lite) 

Este tema explica cómo suscribirse a la oferta de prueba e implementar la implementación simplificada de Dynamics 365 Project Operations: del acuerdo a la facturación proforma.

> [!NOTE]
> Este proceso cambiará en las próximas versiones de Project Operations.

## <a name="prerequisites"></a>Requisitos previos
- El usuario que implementa la vista previa debe tener derechos de administrador global de inquilinos de Azure. Puede crear un inquilino durante el primer caje de oferta.

> [!IMPORTANT]
> Solo una persona, el inquilino administrador, necesita realizar esta tarea en una organización. Si no es el suscriptor de esta versión, espere hasta que su organización se haya registrado y haya recibido sus credenciales de usuario.
> 
> Las pruebas son de un solo uso en el inquilino. Solo puede ejecutar una prueba una vez. Le recomendamos que cree un nuevo inquilino para la prueba.

### <a name="dynamics-365-project-operations-trial"></a>Prueba de Dynamics 365 Project Operations 

Antes de comenzar, asegúrese de haber iniciado sesión en un navegador con la cuenta de trabajo del usuario en el inquilino donde desea la vista previa de Project Operations.

1. Vaya a [Prueba de Project Operations](https://aka.ms/try-po) para canjear el primer código de oferta, **Dynamics 365 Project Operations**.
2. Confirme su pedido.

  Verá que la oferta de confirmación se canjeó correctamente.

## <a name="assign-licenses"></a>Asignación de licencias

> [!IMPORTANT]
> Necesitará acceso administrativo al Portal de Microsoft 365 de la organización para completar los siguientes pasos.


1. Vaya al [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.
2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.
3. Verifique que la licencia de **Dynamics 365 Project Operations** está seleccionada. 
4. Seleccione **Guardar cambios**.

## <a name="create-a-new-dataverse-environment"></a>Crear un nuevo entorno de Dataverse

1. Aprovisione un nuevo entorno de implementación de Dataverse de Project Operations siguiendo las instrucciones del tema [Modelo de implementación Dataverse](lite-deployment.md). Cuando seleccione el tipo de entorno, asegúrese de utilizar **Prueba (basada en suscripción)**.

  ![Nuevo entorno.](./media/19CreateEnvironment.png)

2. Seleccione la opción **Habilitar aplicaciones de Dynamics 365** y deje **Implementar automáticamente estas aplicaciones** en blanco.  
3. Seleccione **Guardar** para crear el entorno.

  ![Agregar base de datos.](./media/20CreateEnvironment1.png)

4. Una vez creado el entorno, instale la solución **Microsoft Dynamics 365 Project Operations**. 

![Instalación de la solución.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instalar una configuración CDS y datos de demostración de configuración

Instale la configuración CDS y configure los datos de demostración siguiendo las instrucciones del tema [Aplicar datos de configuración y configuración de demostración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
