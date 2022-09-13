---
title: Activar y revisar una oferta de proyecto
description: Este artículo proporciona información sobre cómo activar y revisar ofertas en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410349"
---
# <a name="activate-and-revise-a-project-quote"></a>Activar y revisar una oferta de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las capacidades de activación y revisión le ayudan a realizar un seguimiento de las versiones de las ofertas basadas en proyectos durante las fases de estimación y negociación. Cuando se activa un borrador de una oferta, pasa a ser de solo lectura.

Las capacidades de activación y revisión le permiten realizar las siguientes tareas:

- Ganar o perder ofertas solo después de la activación.
- Revisar una oferta para realizar cambios en la existente o crear una nueva versión.

> [!NOTE]
> Una vez habilitada la característica de activación y revisión de ofertas, no se puede deshabilitar.

Para activar la capacidad de activar y revisar ofertas basadas en proyectos, siga estos pasos.

1. Vaya a **Configuración** \> **Parámetros**.
1. Abra el registro **Parámetros**.
1. En el panel de acciones, en la pestaña **Control de características**, seleccione **Habilitar activación y revisión de ofertas**.
1. En el cuadro de diálogo de confirmación, seleccione **Aceptar**.
1. Después de unos momentos, actualice su navegador. Las capacidades de activación y revisión ahora deberían estar disponibles. Sabrá que estas capacidades han sido habilitadas si el botón **Habilitar activación y revisión de ofertas** ya no aparece en el panel de acciones.

## <a name="activating-a-quote"></a>Activar una oferta

Una vez habilitada la característica de activación y revisión de ofertas, los botones **Cerrar oferta como ganada** y **Cerrar oferta como perdida** del panel de acciones no están disponibles para los borradores de ofertas de proyectos. Están disponibles solo después de activar una oferta.

La activación representa la etapa en el proceso de oferta en la que desea evitar más cambios en la misma. En esta etapa, la oferta se envía para revisión interna o al cliente.

Los botones **Cerrar oferta como ganada** y **Cerrar oferta como perdida** del panel de acciones están disponibles para ofertas activadas. En función del resultado de la revisión interna o del cliente, puede usar uno de estos botones para cerrar una oferta activada. Puede realizar negociaciones y cambios en las ofertas activadas si selecciona **Revisar oferta**.

## <a name="revising-a-quote"></a>Revisar una oferta

Si debe realizar cambios en una oferta activada, seleccione **Revisar oferta**. La oferta está cerrada y se utiliza el código de motivo **revisado**. Luego se crea una nueva oferta que tiene el misma id. y un número de revisión incrementado. Todos los detalles de la oferta original se copian a la nueva oferta. La nueva oferta está en estado de borrador y se puede editar según sea necesario.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
