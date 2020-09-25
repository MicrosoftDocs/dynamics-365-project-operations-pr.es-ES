---
title: Actualización de la página principal
description: En este tema se muestra dónde encontrar la información importante sobre las características nuevas y modificadas en Dynamics 365 Project Service Automation y el proceso para actualizar a la versión más reciente.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756041"
---
# <a name="upgrade-home-page"></a>Actualización de la página principal

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Actualización desde la versión 2.x o 1.x de PSA a la versión 3.x

### <a name="new-instances"></a>Instancias nuevas

A partir del 17 de mayo de 2019, cuando se selecciona Project Service Automation durante el aprovisionamiento de una nueva instancia, se instala la versión 3.x de manera predeterminada.

### <a name="existing-instances"></a>Instancias existentes

Anteriormente, los clientes que tuvieran una instancia de la versión 2.x de PSA y necesitaran actualizar a la versión 3.x, que es la versión de PSA basada en la interfaz de cliente unificada (UCI), debían ponerse en contacto con el Soporte técnico de Microsoft y proporcionar los detalles de su instancia, para que ese departamento pudiera habilitar la instancia para la actualización a la versión 3.x. A partir del 1 de marzo de 2020, los clientes que tengan una instancia de PSA versión 2.x y necesiten actualizar a la versión 3.x, podrán actualizar sus instancias directamente desde el portal de administración sin tener que ponerse en contacto con el Soporte técnico de Microsoft.  

> [!NOTE]
> La versión 3.x de PSA incluye cambios significativos. Se ha creado en el marco de la interfaz unificada para ayudar a proporcionar una experiencia de usuario mejorada. La aplicación rediseñada ofrece una interfaz de usuario (IU) coherente y uniforme, y sigue principios de diseño receptivos para una visualización óptima en cualquier tamaño de pantalla o dispositivo. Se han producido otros cambios en toda la aplicación. Algunas de las áreas que se han modificado incluyen precios, reservas y asignación de recursos, tiempo, gastos y aprobaciones.

Antes de comenzar el proceso de actualización, le recomendamos que complete las siguientes tareas:

- Verifique que tanto Dynamics 365 Field Service como Project Service Automation estén instalados en la instancia identificada. Si ambas soluciones están instaladas, debe planear actualizar ambas antes de reanudar el uso regular de la instancia.
- Revise atentamente los siguientes temas. El conocimiento y la comprensión de los cambios entre versiones le ayudarán con el proceso de actualización. Estos temas proporcionan información sobre los principales cambios en PSA, junto con consideraciones y recomendaciones para planificar su actualización a la versión 3.x.

    - [Novedades o cambios en la versión 3 de Project Service Automation](whats-new-changed-v3.md)
    - [Consideraciones de actualización: De la versión 2.x o 1.x a la versión 3 de Project Service Automation](upgrade-v3.md)

- Actualice su instancia de espacio aislado para evaluar los cambios en su implementación antes de actualizar su instancia de producción.

Una vez que haya revisado los temas mencionados anteriormente y esté listo para actualizar a la versión 3.x de PSA o a la versión basada en UCI, envíe una solicitud a Soporte técnico de Microsoft para que la actualización esté disponible desde el Centro de administración. En su solicitud, proporcione los detalles de su instancia.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versiones anteriores de PSA (versión 2.x de PSA) en una instancia recién creada

A partir del 17 de mayo de 2019, todas las nuevas instancias tendrán UCI como cliente predeterminado. Para la alineación con este cambio, se aprovisionarán la versión 3.x de PSA y la versión 8.x de Field Service de forma predeterminada, ya que estas versiones están diseñadas para funcionar con el cliente UCI.

A partir del 1 de marzo de 2020, los clientes de Dynamics PSA ya no podrán crear nuevos entornos con versiones anteriores de PSA, por ejemplo, PSA versión 2.x o inferior. Cualquier entorno nuevo será para obtener solo la versión 3.x de PSA.

> [!NOTE]
> Para obtener la mejor experiencia cuando utilice versiones anteriores de las aplicaciones PSA y Field Service, vaya a la página **Configuración del sistema** y para el campo, **Usar solo la nueva interfaz unificada (recomendado)**, seleccione **No**, ya que estas versiones no están diseñadas para su carga correcta en UCI. Después de desactivar UCI, podrá abrir y ejecutar esas versiones de Field Service y PSA mediante el cliente web antiguo. Para obtener instrucciones sobre cómo desactivar el cliente UCI, consulte [Habilitación solo de la interfaz unificada](../admin/enable-unified-interface-only.md).