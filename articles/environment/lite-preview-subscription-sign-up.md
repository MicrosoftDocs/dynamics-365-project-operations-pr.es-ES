---
title: Registrarse para una suscripción de versión preliminar (lite)
description: 'Este artículo proporciona información sobre cómo suscribirse e implementar Project Operations de forma simplificada: del acuerdo a la facturación proforma.'
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410097"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrarse para una suscripción de versión preliminar (lite) 

Este artículo explica cómo suscribirse a la oferta de prueba e implementar Dynamics 365 Project Operations de forma simplificada: del acuerdo a la facturación proforma.

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


1. Vaya a [Centro de administración de Microsoft 365](https://portal.office.com/) para asignar las licencias a sus usuarios.
2. En la página **Usuarios activos**, seleccione los usuarios a los que desea asignar una licencia.
3. Verifique que la licencia de **Dynamics 365 Project Operations** está seleccionada. 
4. Seleccione **Guardar cambios**.

## <a name="create-a-new-dataverse-environment"></a>Crear un nuevo entorno de Dataverse

1. Aprovisionar un nuevo entorno de implementación de Project Operations Dataverse siguiendo las instrucciones del artículo [Modelo de despliegue de Dataverse](lite-deployment.md). Cuando seleccione el tipo de entorno, asegúrese de utilizar **Prueba (basada en suscripción)**.

  ![Nuevo entorno.](./media/19CreateEnvironment.png)

2. Seleccione la opción **Habilitar aplicaciones de Dynamics 365** y deje **Implementar automáticamente estas aplicaciones** en blanco.  
3. Seleccione **Guardar** para crear el entorno.

  ![Agregar base de datos.](./media/20CreateEnvironment1.png)

4. Una vez creado el entorno, instale la solución **Microsoft Dynamics 365 Project Operations**. 

![Instalación de la solución.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Configurar datos de demostración

Configure los datos de demostración siguiendo las instrucciones del artículo [Aplicar configuración de demostración y datos de configuración](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
