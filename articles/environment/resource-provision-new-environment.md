---
title: Aprovisionar un entorno nuevo
description: Este tema proporciona información sobre cómo aprovisionar un nuevo entorno de Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643013"
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

1. Abra un nuevo despliegue de Dynamics 365 Finance de [entorno de demostración](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorno de espacio aislado/producción](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

![Configuración de implementación](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Seleccione **Aceptar** para reconocer los términos de servicio y luego seleccione **Listo** para volver a la configuración de implementación.

![Consentimiento de implementación](./media/2DeploymentConsent.png)

7. Complete los campos obligatorios restantes en el asistente y confirme la implementación. El tiempo de aprovisionamiento del entorno varía según el tipo de entorno. El aprovisionamiento puede tardar hasta seis horas.

  Una vez que la implementación se completa correctamente, el entorno se mostrará como **Implementado**.

8. Para confirmar que el entorno se ha implementado correctamente, seleccione **Iniciar sesión** e inicie sesión en el entorno para confirmar.

![Detalles del entorno de](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Aplicar datos de demostración de Project Operations Finance (paso opcional)

Aplique los datos de demostración de Project Operations Finance al entorno alojado en la nube de la versión de servicio 10.0.13, como se describe en [este artículo](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplique actualizaciones al entorno de Finance

Project Operations requiere un entorno de Finance con versión de la aplicación **10.0.13 (10.0.569.20009)** o superior.

Es posible que deba aplicar actualizaciones de calidad a su entorno de Finance para recibir esta versión.

1. En LCS, en la página **Detalles del entorno**, en la sección **Actualizaciones disponibles**, seleccione **Ver actualización**.

![Ver actualizaciones](./media/5ViewUpdates.png)

2. En la página **Actualizaciones binarias**, seleccione **Guardar paquete.**

![Guardar paquete](./media/6SavePackage.png)

3. Haga clic en **Seleccionar todo** y luego en **Guardar paquete**.

![Revisar y guardar actualizaciones](./media/7ReviewAndSaveUpdates.png)

4. Introduzca un nombre y una descripción del paquete y luego seleccione **Guardar**. Dependiendo de la conexión a Internet, este proceso puede llevar algún tiempo.

![Cargar paquete a la biblioteca de activos](./media/8UploadPackageToAssetsLibrary.png)

5. Una vez guardado el paquete, seleccione **Hecho** y guarde este paquete en la biblioteca de activos de su proyecto LCS.

Guardar y validar el paquete puede tardar unos 15 minutos.

6. Para aplicar la actualización, vaya a la página **Detalles del entorno** en LCS y seleccione **Mantener** > **Aplicar actualizaciones**.

![Mantener entornos](./media/9MaintainEnvironment.png)

7. En la lista de actualizaciones, seleccione el paquete que creó y seleccione **Aplicar**.

![Aplicar actualizaciones](./media/10ApplyUpdates.png)

El mantenimiento del entorno llevará algún tiempo. Una vez que se haya completado, el entorno volverá a un estado implementado.

![Entorno implementado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establecer una conexión de escritura dual 

1. En su proyecto LCS, vaya a la página **Detalles del entorno**.
2. En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones**.
3. Una vez completado el vínculo, seleccione **Vincular a CDS para aplicaciones** otra vez. Se le redirigirá a Escritura dual en Finance.

![Vincular con CDS](./media/12LinktoCDS.png)

4. Seleccione **Aplicar solución** para acceder a las entidades que se asignarán en la integración.

![Aplicar soluciones](./media/13ApplySolutions.png)

5. Seleccione ambas soluciones, **Asignación de tablas de doble escritura de Dynamics 365 Finance and Operations** y **Asignación de tablas de doble escritura de Dynamics 365 Project Operations** y luego seleccione **Aplicar**.

![Confirmar soluciones](./media/14ConfirmSolutions.png)

Una vez aplicadas las soluciones, las entidades de escritura dual se aplican al entorno.

![Aplicación de soluciones](./media/15ApplyingSolutions.png)

Una vez aplicadas las entidades, todas las asignaciones disponibles se enumeran en el entorno.

![Mapas de doble escritura](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualizar las entidades de datos después de la actualización

1. En Finance, vaya al área de trabajo **Administración de datos**.

![Espacio de trabajo de administración de datos](./media/16DataManagement.png)

2. Seleccione el icono **Parámetros del marco**.

![Parámetros del marco](./media/17FrameworkParameters.png)

3. En la página **Configuración de entidad**, seleccione **Refrescar lista de entidades**.

![Actualizar lista de entidades](./media/18RefreshEntityList.png)

La actualización tomará aproximadamente 20 minutos. Recibirá una alerta cuando termine.

![Confirmación de actualización](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Ejecutar asignaciones de escritura doble de Project Operations

1. En su proyecto LCS, vaya a la página **Detalles del entorno**.
2. En **Información de entorno de Common Data Service**, seleccione **Vincular a CDS para aplicaciones.** Después de seleccionar el vínculo, se le redirigirá a la lista de entidades de las asignaciones.
3. Comience las asignaciones como se describe en la siguiente tabla. Asegúrese de seguir la secuencia indicada.

| **Asignación de entidad** | **Actualizar entidad** | **Sincronización inicial** | **Maestro para sincronización inicial** | **Ejecutar requisitos previos** | **Sincronización inicial de requisitos previos** |
| --- | --- | --- | --- | --- | --- |
| **Roles de recursos del proyecto para todas las empresas (categorías de recursos reservables)** | No | Sí | Common Data Service | No | N/D |
| **Entidades legales (empresas\_cdm)** | No | Sí | Aplicaciones de Finance and Operations | No | N/D |
| **Libro mayor (msdyn_ledgers)** | No | Sí | Aplicaciones de Finance and Operations | Sí | Si, aplicaciones de Finance and Operations |
| **Datos reales de integración de Project Operations (datos reales de\_msdyn)** | No | No | N/D | Sí | No |
| **Líneas de contrato de proyecto (detalles de pedidos de ventas)** | No | No | N/D | No | No |
| **Entidad de integración para las relaciones de transacciones del proyecto (conexiones de transacción\_msdyn)** | No | No | N/D | No | N/D |
| **Hitos de la línea de contrato de integración de Project Operations (programación de valores de líneas de contrato\_msdyn)** | No | No | N/D | No | N/D |
| **Entidad de integración de operaciones de proyecto para estimaciones de gastos (líneas de estimaciones\_msdyn)** | No | No | N/D | No | N/D |
| **Entidad de exportación de categorías gastos de proyecto de integración de Project Operations (msdyn\_expensecategories)** | No | No | N/D | No | N/D |
| **Entidad de exportación de gastos de proyecto de integración de Project Operations (gastos\_msdyn)** | Sí | No | N/D | No | N/D |
| **Entidad de integración de operaciones de proyecto para estimaciones de tiempo (asignaciones de recursos\_msdyn)** | Sí | No | N/D | No | N/D |


4. Para actualizar la entidad, seleccione el nombre del mapa y luego seleccione **Actualizar entidades**. 


![Actualizar Mapa](./media/20RefreshMapping.png)

5. Tras completar la actualización, ejecute el mapa. Antes de habilitar el siguiente mapa, verifique que el mapa de la tabla esté en un estado de **Ejecución**. La ejecución de mapas con una mayor cantidad de requisitos previos puede llevar algún tiempo.

Para ejecutar un mapa con requisitos previos, habilite la alternancia **Mostrar mapas de entidades relacionadas**. Si la tabla indica que **Sincronización inicial de requisitos previos** tiene el valor **No**, verifique que el indicador **Sincronización inicial** esté en **Desactivado** en todos los mapas de requisitos previos antes de ejecutarlo.

![Ejecutar mapa](./media/21RunMap.png)

6. Valide que todos los mapas relacionados con el proyecto estén en estado de ejecución.

![Todos los mapas en ejecución](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicar datos de configuración en CDS para Project Operations (opcional)

Si ha aplicado datos de demostración al entorno financiero, consulte [Configurar y aplicar datos de configuración en Common Data Service para Project Operations](resource-apply-pro-setup-config-data.md) para aplicar datos de demostración al entorno CDS.


Su entorno de Project Operations ya está aprovisionado y configurado. 
