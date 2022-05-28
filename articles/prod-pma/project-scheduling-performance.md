---
title: Rendimiento de la programación de recursos del proyecto
description: Este tema proporciona información sobre cómo mejorar el rendimiento de la programación de recursos para una gran cantidad de proyectos.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 726788e9ecb7fc70648d06d0a5036becd7a45d2a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682897"
---
# <a name="project-resource-scheduling-performance"></a>Rendimiento de la programación de recursos del proyecto

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Los problemas de rendimiento relacionados con la programación de recursos pueden ocurrir cuando el número de proyectos llega a miles. Para mejorar el rendimiento de la programación de recursos, hay una función disponible que permite a los usuarios reducir el tiempo que lleva iniciar el formulario de disponibilidad de recursos. Específicamente, esto elimina el proceso de sincronización de acumulación de capacidad de recursos y utiliza la tabla **ResProjectResource** para acelerar la búsqueda de recursos. Tenga en cuenta que la tabla **ResRollup** ya no se utilizará.

> [!IMPORTANT]
> Si existe una dependencia del proceso de sincronización de acumulación de capacidad de recursos o de la tabla **ResProjectResource**, no utilice esta función.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Habilite la mejora del rendimiento de la programación de recursos
Para habilitar la mejora del rendimiento de la programación de recursos, complete los siguientes pasos.

1. Vaya a **Gestión de funciones** > **Todos** y en la lista de funciones, ubique **Habilitar la función de mejora del rendimiento de la programación de recursos del proyecto**.
2. Seleccione **Habilitar ahora**.

> [!NOTE]
> Si no puede encontrar la función en la lista, seleccione **Buscar actualizaciones** para actualizar la lista.

3. Actualice su navegador y luego vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Recursos del proyecto** > **Sincronizar la capacidad de los calendarios de recursos en todas las empresas**.
4. Establezca **Eliminar registros de capacidad existentes** a **Sí** para eliminar los datos anteriores. Si desea generar datos incrementales, configúrelo en **No**.
5. En el campo **Código de período**, seleccione el período en el que se deben generar los datos. Si selecciona un código de período, no es necesario definir una fecha de inicio y finalización.
6. Si deja el campo **Código de período** en blanco, seleccione fechas de inicio y finalización específicas para generar datos.
7. Seleccione **Aceptar**.

 > [!NOTE]
 > Esto distribuirá datos generales a la tabla **ResCalendarCapacity** en todas las empresas de su entorno, por lo que el trabajo por lotes solo debe ejecutarse en una entidad legal. Los datos de este trabajo por lotes son necesarios para calcular la capacidad de recursos a través del calendario asociado.

8. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Recursos del proyecto** > **Completar los recursos del proyecto en todas las empresas** y luego seleccione **Aceptar**. Este es el script de actualización de datos para datos generales en las tablas **ResProjectResource**, **ResCalendarDateTimeRange** y **ResEffectiveDateTimeRange**. Los valores para el campo **PSAPRojSchedRole.RootActivity** también se actualizan. Si no se ejecuta, recibirá una advertencia cuando intente ejecutar operaciones de programación de recursos.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Desactive la mejora del rendimiento de la programación de recursos

1. Vaya a **Gestión de funciones** > **Todos** y busque **Habilitar la función de mejora del rendimiento de la programación de recursos del proyecto**.
2. Seleccione la función y luego seleccione el botón **Deshabilitar**.
3. Actualice el explorador.
4. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Sincronización de capacidad** > **Sincronizar acumulaciones de capacidad de recurso**.
5. En la página **Sincronización de acumulación de capacidad**, establezca **Eliminar registros de capacidad existentes** a **Sí** para eliminar los datos anteriores. Si desea generar datos incrementales, configúrelo en **No**.
6. En el campo **Código de período**, seleccione el período en el que se deben generar los datos. Si selecciona un código de período, no es necesario definir una fecha de inicio y finalización.
7. Si deja el campo **Código de período** en blanco, seleccione fechas de inicio y finalización específicas para generar datos.
8. Seleccione **Aceptar**.

> [!NOTE]
> Esto distribuirá datos generales a la tabla **ResRollup** en todas las empresas de su entorno, por lo que el trabajo por lotes solo debe ejecutarse en una entidad legal. Este trabajo por lotes es necesario para todas las vistas **Disponibilidad de recursos**. Si este trabajo por lotes no se ejecuta, los datos de **ResRollup** se generarán sobre la marcha, lo que puede llevar tiempo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]