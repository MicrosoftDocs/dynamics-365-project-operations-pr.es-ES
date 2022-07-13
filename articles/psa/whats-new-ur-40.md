---
title: Novedades o cambios en la versión de actualización 40, V3, de Project Service Automation
description: Este artículo enumera las funciones y correcciones que están disponibles en la actualización de la versión 40, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912813"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novedades o cambios en la versión de actualización 40, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este artículo se enumeran las funciones y correcciones que son nuevas o modificadas para Project Service Automation Update Release 40, V3. Esta versión tiene el número de compilación V3.10.61.61 y está disponible de forma generalizada mediante una actualización automática desde febrero de 2022.

## <a name="update-release-40"></a>Versión de actualización 40

### <a name="features"></a>Características
La fase 1 de la actualización de Project Service Automation a Project Operations Lite se lanzará en febrero de 2022 para todos los clientes. Para comprobar la idoneidad, consulte [Actualizar de Project Service Automation a Project Operations](upgrade-project-operations-non-stocked.md). Si la aplicación no aparece en su instancia del Centro de administración de Power Platform comuníquese con soporte y solicite que el paquete piloto se habilite para sus entornos. Su solicitud debe incluir una lista de id. de entornos en los que se debe habilitar el paquete piloto.

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**
- Falta una entrada de nota cuando se rechaza o cancela una entrada de tiempo. 

**Ventas**

- Cuando actualiza las estimaciones de costos o ventas mediante complementos listos para usar, se le permite incorrectamente enviar cargas JSON que no son válidas fuera de la interfaz de usuario.
- Cuando actualiza líneas de oferta utilizando la vista rápida, puede activar ofertas.