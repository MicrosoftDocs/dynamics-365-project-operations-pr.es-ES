---
title: Sincronizar el estado del proyecto para evitar la entrada contra proyectos cerrados
description: Este artículo explica cómo sincronizar el estado del proyecto para evitar la entrada en proyectos inactivos o cerrados.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348037"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronizar el estado del proyecto para evitar la entrada contra proyectos cerrados

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

## <a name="scenario"></a>Escenario

Contoso va a actuar con Microsoft Dynamics 365 Project Operations para escenarios de recursos/sin existencias. Como parte de las actividades comerciales normales, los proyectos pueden completarse o suspenderse. Puede desactivar el proyecto para asegurarse de que no se generen gastos ni facturas.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Requisitos previos

-   Debe tener instaldo Microsoft Dynamics 365 Finance 10.0.29 o posterior.
-   Debe instalar o configurar un mapa de escritura dual 1.0.0.3 para Projects V2 (msdyn\_projects) manualmente como se describe a continuación.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Crear una versión actualizada del mapa de escritura dual Projects V2 de la integración de Project Operations

Para actualizar el mapa de escritura dual Projects V2 de Project Operations:

1. Vaya al área de trabajo **Administración de datos** y seleccione **Doble escritura**.
2. Seleccione el icono **Doble escritura**.
3. En la columna **Asignación de tabla**, busque y seleccione **Project V2 (msdyn\_projects)** y luego seleccione Detener.
4. Seleccione el nombre del mapa para abrirlo y luego seleccione **[None]**.
5. En el cuadro de diálogo Seleccionar columna, seleccione **statecode \[Project Status\]** y luego seleccione Aceptar. Puedee escribir **state** en el valor del filtro para reducir la lista.
6.  Seleccione **Agregar o editar transformación** en la columna **tipo de mapa** para editar la transformación.
7.  En **Tipo de transformación**, seleccione **ValueMap**.
8.  Seleccione **Agregar asignación de valores** y luego agregue las siguientes **Claves** y **Valores**:

   Llave       | valor 
   ----------|-------
   InProcess | 0     
   completada | 1     

![Captura de pantalla que muestra la asignación de escritura dual](media/projectstage-dw-mapping.png)

9. Seleccione **Guardar**.
10. En la parte superior de la página **Escritura dual > Projects V2 (msdyn_projects)**, seleccione **Guardar como**.
11. En **Agregar tabla**, en el campo **Editor**, seleccione **Editor predeterminado de CDS**.
12. En el campo **Versión**, seleccione 1.0.0.3.
13. Escriba una **Descripción** y luego seleccione **Guardar**.
14. En la parte superior de la página **Escritura dual > Projects V2 (msdyn_projects)**, seleccione **Ejecutar** para iniciar la asignación, y luego seleccione **Sí** si se le pide que confirme antes de ejecutar. 

### <a name="close-a-newly-completed-project"></a>Cerrar un proyecto recién completado

Dynamics 365 Finance utiliza el campo **fase del proyecto** para diferenciar entre proyectos **en curso** o **acabados**. Los proyectos **Acabados** no pueden generar gastos ni facturarse a los clientes.

1. Abra un proyecto para desactivar.
2. En la cinta, seleccione **Desactivar**.

> [!NOTE]
> Puede desactivar o cerrar un proyecto, ya que ambos se comportarán de la misma manera en el contexto de Finance.

3. En Finance, abra la página **Lista Todos los proyectos**.
4. Confirme que el proyecto desactivado no aparece en la lista.
5. En el filtro **mostrar proyectos** encima de la lista, cambie el valor de **Activo** a **Todos**.
6. Ahora verá el proyecto desactivado.

Si intenta registrar el tiempo o los gastos de este proyecto en Finance, no debería ver el proyecto para su selección. Si introduce manualmente el número de proyecto en un gasto, verá un mensaje como "La etapa del proyecto finalizada no permite registrar el proyecto". La facturación y otras funciones de facturación deben desactivarse, ya que estarán en el contexto de un proyecto cerrado.

