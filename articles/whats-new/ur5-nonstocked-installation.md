---
title: Actualizar Project Operations en el entorno de Finance
description: Este tema proporciona información sobre cómo actualizar Project Operations en el entorno de Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011077"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Actualizar Project Operations en el entorno de Finance

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Este tema proporciona información sobre cómo actualizar Dynamics 365 Project Operations en el entorno de Dynamics 365 Finance. Hay tres procedimientos necesarios para actualizar las operaciones de Project Operations a la actualización 5 (UR5):

- [Importar el paquete al proyecto de versión preliminar](#import)
- [Aplicar la actualización](#apply)
- [Actualizar el entorno de Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importar el paquete en el proyecto de LCS

1. Inicie sesión en [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como propietario del proyecto o administrador del entorno.
2. Seleccione su proyecto de LCS en la lista de proyectos.
3. En la página **Proyecto**, en el grupo **Entornos**, abra el entorno que desea actualizar.
4. Compruebe que el entorno se ejecuta correctamente. Si no se ha inicia el entorno, inícielo.
5. En la sección **Nueva versión**, en **Actualizaciones disponibles**, seleccione **Ver actualización** para 10.0.15.

![Botón Ver actualización](media/view-update.png)

6. En la página **Actualizaciones binarias**, seleccione **Guardar paquete**.
7. En la página **Revisar y guardar actualizaciones**, seleccione **Guardar paquete**.
8. En el panel **Guardar paquete en la biblioteca de activos** que se abre, especifique el nombre del paquete y seleccione **Guardar paquete**.
9. Cuando LCS haya terminado de guardar el paquete, se habilita el botón **Listo**. Seleccione **Listo**. LCS comprobará el paquete. La comprobación puede tardar desde unos minutos hasta una hora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplicar la actualización del paquete

1. En LCS, en la página **Detalles del entorno**, seleccione **Mantener** > **Aplicar actualizaciones**.
2. En la lista, seleccione el paquete que guardó anteriormente y, a continuación, seleccione **Aplicar**.
3. Seleccione **Sí** para confirmar que desea quitar implementar el paquete.

![Cuadro de diálogo Confirmar implementación del paquete](media/confirm-package-deployment.png)

4. Seleccione **Sí** para confirmar que desea actualizar la aplicación.

![Cuadro de diálogo Confirmar actualización de la aplicación](media/confirm-application-update.png)

Se iniciará la implementación y la actualización de la aplicación. 

En la página **Detalles del entorno**, en la esquina superior derecha, se actualizará el estado del entorno a **Servicio**. La actualización se habrá completado en aproximadamente dos horas. La información de versión de la aplicación se actualizará a **Microsoft Dynamics 365 for Finance and Operations 10.0.15** y el estado del entorno se actualizará a **Implementado**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Actualizar el entorno de Dataverse

1. Inicie sesión en el [Centro de administración de Power Platform](https://admin.powerplatform.com/).
2. En la lista, busque y abra el entorno que utilizó para instalar Project Operations.
3. En la página **Entornos**, seleccione **Recurso** > **Aplicaciones de Dynamics 365**.
4. En la lista, localice **Microsoft Dynamics 365 Project Operations** y, en la columna **Estado**, seleccione **Actualización disponible**.
5. Active la casilla **Acepto los términos de servicio** y seleccione **Actualizar**. Se instalará la versión más reciente de la solución.

Cuando se haya completado la instalación tendrá instalada la versión 4.5.0.134.

## <a name="configure-new-features"></a>Configurar nuevas características

### <a name="enable-dual-write-mapping"></a>Habilitar la asignación de doble escritura

Una vez completada la actualización de los entornos de Finance y Dataverse, puede habilitar las asignaciones de doble escritura necesarias. Lleve a cabo los procedimientos siguientes para habilitar las asignaciones de doble escritura:

- [Actualizar la configuración de seguridad en el entorno de Customer Engagement](#security)
- [Actualizar entidades de datos](#refresh)
- [Actualizar y ejecutar las asignaciones de doble escritura](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Actualizar la configuración de seguridad en el entorno de Dataverse

Las siguientes actualizaciones de los privilegios de seguridad para las entidades son necesarios para realizar la actualización a UR5.

1. En el entorno de Dataverse, vaya a **Configuración** y, en el grupo **Sistema**, seleccione **Seguridad**.

![Configuración del entorno de Dataverse](media/Picture21.png)

2. Seleccione **Roles de seguridad**.
3. En la lista de roles, seleccione **usuario de aplicación de doble escritura** y, a continuación, seleccione la pestaña **Entidades personalizadas**. 
4. Compruebe que el rol tenga los permisos **Leer** y **Anexar a** para:

      - **Tipo de cambio de la divisa**
      - **Plan de cuentas** 
      - **Calendario fiscal** 
      - **Ledger**

5. Después de actualizar el rol de seguridad, vaya a **Configuración** > **Seguridad** > **Equipos**. Compruebe que se haya aplicado al equipo el rol **usuario de la aplicación de doble escritura**. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Actualizar entidades de datos de la actualización

1. En el entorno de Finance, abra el área de trabajo **Gestión de datos** y, a continuación, abra la página **Parámetros del marco**.
2. En la pestaña **Configuración de entidad**, seleccione **Actualizar la lista de entidades**.
3. Seleccione **Cerrar** para confirmar la actualización de la entidad.

 > [!NOTE]
 > Este proceso tardará aproximadamente 20 minutos. Recibirá una notificación cuando se haya completado la actualización.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Asignaciones de doble escritura

1. En el área de trabajo **Administración de datos**, seleccione **Doble escritura**.
2. Seleccione **Aplicar soluciones**, seleccione ambas soluciones en la lista y, a continuación, seleccione **Aplicar**.
3. En la página **Doble escritura**, seleccione las siguientes asignaciones de tablas y, a continuación, seleccione **Detener**.

    - **Datos reales de integración de Project Operations (msdyn_actuals)**
    - **Categorías de gastos de proyecto de integración de Project Operations (msdyn_expensecategories)**
    - **Entidad de exportación de gastos de proyecto de datos reales de integración de Project Operations (msdyn_expenses)**

4. En la página **Versión de asignación de tabla**, aplique una nueva versión de la asignación a cada una de las tres entidades.
5. En la página **Doble escritura**, seleccione ejecutar para reiniciar las asignaciones.
6. En la lista de mapas, seleccione la asignación **Contabilidad (msdyn_ledgers)** con todos los requisitos previos y active la casilla **Sincronización inicial**. 
7. En el campo **Maestro para la sincronización inicial**, seleccione **Aplicaciones de Finance and Operations** y, a continuación, seleccione **Ejecutar**.
 
 ![Sincronización de asignaciones de contabilidad](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]