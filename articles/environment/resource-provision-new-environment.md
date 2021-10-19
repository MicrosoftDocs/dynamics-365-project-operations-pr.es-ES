---
title: Aprovisionar un entorno nuevo
description: Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7f63b144b6fe3eb848d0c303b64237516a97cb56
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501437"
---
# <a name="provision-a-new-environment"></a>Aprovisionar un entorno nuevo

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Dynamics 365 Project Operations para escenarios basados en recursos/no mantenidos en existencias.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Habilitear el aprovisionamiento automatizado de Project Operations en un proyecto LCS

Utilice los siguientes pasos para habilitar el flujo de aprovisionamiento automatizado de Project Operations para su proyecto LCS.

1. Vaya a [LCS](https://lcs.dynamics.com/v2) y seleccione el icono **Gestión de funciones de vista previa**.
2. En la lista **Característica de vista previa**, seleccione **Característica de Project Operations** y después seleccione **Función de vista previa habilitada** para habilitar Project Operations.

   > [!NOTE]
   > Este paso se realiza solo una vez por proyecto LCS.

## <a name="provision-a-project-operations-environment"></a>Aprovisionar un entorno de Project Operations

1. Abra un nuevo despliegue de Dynamics 365 Finance de [entorno de demostración](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorno de espacio aislado/producción](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Siga el asistente de **Aprovisionamiento de entornos**. 

   > [!IMPORTANT]
   > Asegúrese de que la versión de la aplicación seleccionada sea 10.0.13 o superior.

3. Para aprovisionar Project Operations, en **Configuración avanzada**, seleccione **Common Data Service**. 
4. Habilite la **Opción Common Data Service** seleccionando **Sí** y luego introduzca información en los campos obligatorios:

  - Nombre
  - Región
  - Lenguaje
  - Divisa
 
5. En el campo **Plantilla de Common Data Service**, seleccione **Project Operations** 
6. Seleccione el tipo de entorno de su implementación. Una prueba basada en suscripción le permitirá implementar un entorno CDS durante 30 días. 

     ![Configuración de implementación.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Seleccione **Aceptar** para reconocer los términos de servicio y luego seleccione **Listo** para volver a la configuración de implementación.
    >
    >![Consentimiento de implementación.](./media/2DeploymentConsent.png)

7. Opcional: Aplicar datos de demostración al entorno. Vaya a **Configuración avanzada**, seleccione **Personalizar configuración de base de datos SQL**, y establezca **Especificar un conjunto de datos para base de datos de aplicación** en **Demostración**.
8. Complete los campos obligatorios restantes en el asistente y confirme la implementación. El tiempo de aprovisionamiento del entorno varía según el tipo de entorno. El aprovisionamiento puede tardar hasta seis horas.

   Una vez que la implementación se completa correctamente, el entorno se mostrará como **Implementado**.

9. Para confirmar que el entorno se ha implementado correctamente, seleccione **Iniciar sesión** e inicie sesión en el entorno.

    ![Detalles del entorno.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplique actualizaciones al entorno de Finance

Project Operations requiere un entorno de Finance con versión de la aplicación **10.0.13 (10.0.569.20009)** o superior.

Es posible que deba aplicar actualizaciones de calidad a su entorno de Finance para recibir esta versión.

1. En LCS, en la página **Detalles del entorno**, en la sección **Actualizaciones disponibles**, seleccione **Ver actualización**.

    ![Ver actualizaciones.](./media/5ViewUpdates.png)

2. En la página **Actualizaciones binarias**, seleccione **Guardar paquete.**

    ![Guardar paquete.](./media/6SavePackage.png)

3. Haga clic en **Seleccionar todo** y luego en **Guardar paquete**.

    ![Revisar y guardar actualizaciones.](./media/7ReviewAndSaveUpdates.png)

4. Introduzca un nombre y una descripción del paquete y luego seleccione **Guardar**. Dependiendo de la conexión a Internet, este proceso puede llevar algún tiempo.

    ![Cargar paquete a la biblioteca de activos.](./media/8UploadPackageToAssetsLibrary.png)

5. Una vez guardado el paquete, seleccione **Hecho** y guarde este paquete en la biblioteca de activos de su proyecto LCS.

   Guardar y validar el paquete puede tardar unos 15 minutos.

6. Para aplicar la actualización, vaya a la página **Detalles del entorno** en LCS y seleccione **Mantener** > **Aplicar actualizaciones**.

    ![Mantener entornos.](./media/9MaintainEnvironment.png)

7. En la lista de actualizaciones, seleccione el paquete que creó y seleccione **Aplicar**.

    ![Aplicar actualizaciones.](./media/10ApplyUpdates.png)

   El mantenimiento del entorno llevará algún tiempo. Una vez que se haya completado, el entorno volverá a un estado implementado.

    ![Entorno implementado.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establecer una conexión de escritura dual 

1. En su proyecto LCS, vaya a la página **Detalles del entorno**.
2. En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones**.
3. Una vez completado el vínculo, seleccione **Vincular a CDS para aplicaciones** otra vez. Se le redirigirá a Escritura dual en Finance.

    ![Vincular con CDS.](./media/12LinktoCDS.png)

4. Seleccione **Aplicar solución** para acceder a las entidades que se asignarán en la integración.

    ![Aplicar soluciones.](./media/13ApplySolutions.png)

5. Seleccione ambas soluciones, **Asignación de tablas de doble escritura de Dynamics 365 Finance and Operations** y **Asignación de tablas de doble escritura de Dynamics 365 Project Operations** y luego seleccione **Aplicar**.

    ![Confirmar soluciones.](./media/14ConfirmSolutions.png)

    Una vez aplicadas las soluciones, las entidades de escritura dual se aplican al entorno.

    ![Aplicación de soluciones.](./media/15ApplyingSolutions.png)

    Una vez aplicadas las entidades, todas las asignaciones disponibles se enumeran en el entorno.

    ![Mapas de doble escritura.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualizar las entidades de datos después de la actualización

1. En Finance, vaya al área de trabajo **Administración de datos**.

    ![Área de trabajo de administración de datos.](./media/16DataManagement.png)

2. Seleccione el icono **Parámetros del marco**.

    ![Parámetros del marco.](./media/17FrameworkParameters.png)

3. En la página **Configuración de entidad**, seleccione **Refrescar lista de entidades**.

    ![Actualizar lista de entidades.](./media/18RefreshEntityList.png)

La actualización tomará aproximadamente 20 minutos. Recibirá una alerta cuando termine.

  ![Confirmación de actualización.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Actualizar la configuración de seguridad de Project Operations en Dataverse

1. Vaya a Project Operations en el entorno de Dataverse. 
2. Vaya a **Configuración** > **Seguridad** > **Roles de seguridad**. 
3. En la página **Roles de seguridad**, en la lista de roles, seleccione **usuario de aplicación de doble escritura** y, a continuación, seleccione la pestaña **Entidades personalizadas**.  
4. Verifique que el rol tenga permisos de **Leer** y **Anexar a** para las siguientes entidades:
      
      - **Tipo de cambio de la divisa**
      - **Plan de cuentas**
      - **Calendario fiscal**
      - **Ledger**
      - **Empresa**
      - **Tipo de cambio de la divisa**
      - **Gasto**

5. Una vez que se haya actualizado el rol de seguridad, vaya a **Configuración** > **Seguridad** > **Equipos** y seleccione el equipo predeterminado en la vista de equipo **Propietario de empresa local**.
6. Seleccione **Administrar roles** y compruebe que se haya aplicado el privilegio de seguridad **usuario de aplicación de doble escritura** a este equipo.

## <a name="run-project-operations-dual-write-maps"></a>Ejecutar asignaciones de escritura doble de Project Operations

1. En su proyecto LCS, vaya a la página **Detalles del entorno**.
2. En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones.** Después de seleccionar el vínculo, se le redirigirá a la lista de entidades de las asignaciones.
3. Inicie los mapas. Para más información, vea [Versiones de asignación de doble escritura de Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Valide que todos los mapas relacionados con el proyecto estén en estado de ejecución.

    ![Todos los mapas en ejecución.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicar datos de configuración en CDS para Project Operations (opcional)

Si ha aplicado datos de demostración al entorno financiero, consulte [Configurar y aplicar datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración al entorno CDS.


Su entorno de Project Operations ya está aprovisionado y configurado. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
