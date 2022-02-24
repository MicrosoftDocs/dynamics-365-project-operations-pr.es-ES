---
title: Aplicar datos de demostración a un entorno de Finance hospedado en la nube
description: Este tema explica cómo aplicar datos de demostración de Project Operations a un entorno alojado en la nube de Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365259"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicar datos de demostración a un entorno de Finance hospedado en la nube

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

> [!IMPORTANT]
> Este tema solo se aplica a Microsoft Dynamics 365 Finance, versión 10.0.13, y solo se puede ejecutar en un entorno alojado en la nube. Complete los pasos de este tema **ANTES** de aplicar actualizaciones de calidad al entorno.

1. En su proyecto LCS, abra la página **Detalles del entorno**. Tenga en cuenta que incluye los detalles necesarios para conectarse al entorno mediante el Protocolo de escritorio remoto (RDP).

![Detalles del entorno de](./media/1EnvironmentDetails.png)

El primer conjunto de credenciales resaltadas son las credenciales de la cuenta local y contienen un hipervínculo a la conexión de escritorio remoto. Las credenciales incluyen el nombre de usuario y la contraseña del administrador del entorno. El segundo conjunto de credenciales se utiliza para iniciar sesión en SQL Server en este entorno.

2. Conéctese remotamente con el entorno mediante el hipervínculo de **Cuentas locales** y use las **Credenciales de cuenta local** para autenticar.
3. Vaya a **Servicios de Información de Internet** > **Grupos de aplicaciones** > **AOSService** y detenga el servicio. Está deteniendo el servicio en este punto para poder continuar reemplazando la base de datos SQL.

![Detener AOS](./media/2StopAOS.png)

4. Vaya a **Servicios** y detenga los siguientes dos elementos:

- Microsoft Dynamics 365 Unified Operations: Servicio de gestión de lotes
- Microsoft Dynamics 365 Unified Operations: marco de importación y exportación de datos

![Detener servicios](./media/3StopServices.png)

5. Abrir Microsoft SQL Server Management Studio. Inicie sesión con las credenciales del servidor SQL y use el usuario axdbadmin y la contraseña de la página **Detalles de entornos** LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. En el Explorador de objetos, **Bases de datos** y localice **AXDB**. Reemplazará la base de datos con una nueva base de datos que se encuentra en el [Centro de descargas](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copie el archivo zip en la VM a la que está conectado de forma remota y extraiga el contenido del zip.
8. En SQL Server Management Studio, haga clic con el botón derecho en **AxDB** y luego seleccione **Tareas** > **Restaurar** > **Base de datos**.

![Restaurar base de datos](./media/5RestoreDatabase.png)

9. Seleccione **Dispositivo de origen** y navegue hasta el archivo extraído del zip que copió.

![Dispositivos de origen](./media/6SourceDevice.png)

10. Seleccione **Opciones** y luego seleccione **Sobrescribir la base de datos existente** y **Cerrar las conexiones existentes a la base de datos de destino**. 
11. Seleccione **Aceptar**.

![Restaurar configuracion](./media/7RestoreSetting.png)

Recibirá la confirmación de que la restauración de AXDB se realizó correctamente. Después de recibir esta confirmación, puede cerrar SQL Services Management Studio.

12. Vuelva a **Servicios de Información de Internet** > **Grupos de aplicaciones** > **AOSService** e inicie AOSService.
13. Vaya a **Servicios** e inicie los dos servicios que detuvo antes.

14. Busque la herramienta AdminUserProvisioning en esta VM. Busque en K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Ejecute el archivo .ext con su dirección de usuario en el campo **Dirección de correo electrónico**. 
16. Seleccione **Enviar**.

![Aprovisionamiento de usuarios administradores](./media/8AdminUserProvisioning.png)

Esto puede tardar un par de minutos en completarse. Debería recibir un mensaje de confirmación de que el usuario administrador se actualizó correctamente.

17. Por último, ejecute el símbolo del sistema como administrador y realice iisreset

![Restablecimiento de IIS](./media/9IISReset.png)

18. Cierre la sesión de escritorio remoto y use la página **Detalles del entorno** LCS para iniciar sesión en el entorno y confirmar que funciona como se esperaba.

![Finance and Operations](./media/10FinanceAndOperations.png)
