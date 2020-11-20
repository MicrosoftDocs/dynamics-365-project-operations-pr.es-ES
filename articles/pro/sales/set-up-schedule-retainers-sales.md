---
title: Configurar una programación de pagos a cuenta (lite)
description: Este tema proporciona información sobre cómo configurar un cronograma de retención en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181293"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Configurar una programación de pagos a cuenta (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

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