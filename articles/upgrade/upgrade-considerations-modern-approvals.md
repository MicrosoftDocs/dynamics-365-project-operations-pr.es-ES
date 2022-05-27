---
title: Consideraciones de actualización para Aprobaciones modernas
description: El tema cubre los puntos que los administradores deben considerar cuando habilitan la funcionalidad de Aprobaciones modernas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578407"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Consideraciones de actualización para Aprobaciones modernas 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Como parte del primer lanzamiento de versiones de abril de 2022, la funcionalidad de Aprobaciones modernas se habilitará de forma predeterminada. Esta funcionalidad mejora la confiabilidad de la lógica de aprobación y garantiza que pueda determinar el motivo si la lógica de aprobación falla.

Como parte de este cambio, se actualizan los cambios de estado para las aprobaciones de proyectos. El estado ahora va directamente de **Enviado** a **Aprobado**. **Pendiente** ya no es un estado de las aprobaciones. Para determinar si una aprobación está pendiente, verifique que la aprobación sea parte de un conjunto de aprobaciones y luego revise el estado del conjunto de aprobaciones adjunto.

## <a name="before-you-upgrade"></a>Antes de actualizar

Antes de actualizar a Aprobaciones modernas, asegúrese de que no tiene aprobaciones pendientes. Las Aprobaciones modernas no utilizan el estado **Pendiente**. Por lo tanto, cualquier aprobación que siga marcada como **Pendiente** después de la actualización no se procesará.

## <a name="after-you-upgrade"></a>Después de actualizar

Después de actualizar a Aprobaciones modernas, un administrador debe validar que el flujo en la nube que procesa las aprobaciones se haya habilitado.

1. Inicie sesión en [flow.microsoft.com](https://flow.microsoft.com)
2. En la parte superior derecha de la página, cambie su entorno al entorno que ha actualizado.
3. Seleccione **Soluciones** para enumerar las soluciones instaladas en el entorno.
4. En la lista de soluciones, seleccione **Project Operations** o **Project Service**.
5. Cambie el filtro de **Todos** a **Flujos de nube**.
6. Verifique que la opción **Project Service: programación recurrente de conjuntos de aprobación de proyectos** esté establecida en **Activado**. Si no es así, seleccione el flujo y luego seleccione **Activar**.
7. Verifique que el procesamiento esté ocurriendo cada cinco minutos revisando la lista **Trabajos del sistema** lista en el área de **Configuración**.

## <a name="short-term-rollback"></a>Reversión a corto plazo

Si no puede aceptar los cambios, o si encuentra un problema grave con esta característica, puede revertir temporalmente al flujo de aprobación original realizando los siguientes pasos:
1. Inicie sesión en su entorno y verifique que no haya aprobaciones pendientes.
2. Vaya a **Configuración** > **Parámetros de proyecto**.
3. Seleccione **Control de características** y luego seleccione **Aprobaciones modernas** para desactivar la característica.

## <a name="removing-the-feature-flag"></a>Eliminación de la marca de característica

En la segunda actualización de octubre de 2022, se eliminará la capacidad de desactivar esta característica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
