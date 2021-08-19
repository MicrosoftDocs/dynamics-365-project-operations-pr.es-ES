---
title: Configurar una programación de anticipos
description: Este tema proporciona información sobre cómo configurar un cronograma de retención en Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994387"
---
# <a name="set-up-a-retainer-schedule"></a>Configurar una programación de anticipos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los horarios de los retenedores se configuran en la página **Contrato de proyecto** en Dynamics 365 Project Operations.

1. Sobre la página **Contrato de proyecto**, en la pestaña **Anticipos y retenciones**, seleccione **Configurar horario de retención**.
2. En la página de diálogo que se abre, se muestran los campos enumerados en la siguiente tabla. La tabla da una idea de cómo los valores ingresados impactan o influyen en el programa de retención que se creará.

| Campo | Descripción | Impacto posterior |
| --- | --- | --- |
| Cliente de contrato de proyecto | El cliente del contrato al que se le facturará este anticipo o pago a cuenta. | Si tiene varios clientes en el contrato y necesita facturar a cada uno de ellos por un anticipo o monto de anticipo específico, cree manualmente una factura para cada cliente. |
| Iniciar programación de anticipos | Escriba la fecha de inicio de la programación del anticipo. | Esta fecha puede no ser la fecha en la que se crea el primer anticipo o anticipo. La fecha en la que se crea el primer anticipo o anticipo también está influenciada por la frecuencia de facturación. |
| Final de programación de anticipos | Escriba la fecha de finalización de la programación del anticipo. | Esta fecha puede no ser la fecha en la que se crea el último anticipo o pago a cuenta. La fecha en la que se crea el último anticipo o pago a cuenta también está influenciada por la frecuencia de facturación. |
| Número de anticipos a crear | Cuando ingresa el número de retenedores para crear, el sistema usa la fecha de inicio y la frecuencia para crear el número en este campo. | Cuando este campo se actualiza manualmente, el sistema ignora el valor en el campo **Fin del programa de retención** y, en su lugar, crea el número específico de anticipos o avances. |
| Frecuencia de facturación | Con qué frecuencia la aplicación creará retenciones y avances. | Este valor influye directamente en el número de anticipos y anticipos y las fechas de creación. |
| Importe total | El monto total es el monto que se divide en el anticipo individual o los pagos por adelantado que se crearán. | No hay impacto posterior para este campo. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]