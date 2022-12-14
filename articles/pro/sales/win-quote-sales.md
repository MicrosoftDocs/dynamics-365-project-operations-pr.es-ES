---
title: Cerrar ofertas de proyecto
description: Este artículo proporciona información sobre el cierre de una cotización en Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826197"
---
# <a name="close-project-quotes"></a>Cerrar ofertas de proyecto

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las ofertas de proyectos se pueden cerrar como Ganadas o Perdidas. Un borrador de oferta se puede cerrar porque en Microsoft Dynamics 365 Project Operations no se admiten las operaciones Activar y Revisar en las ofertas.

## <a name="close-a-quote-as-won"></a>Cierre de oferta como Ganada

Al cerrar una oferta de proyecto como Lograda, el estado se establece en Cerrada y la razón para el estado será Lograda. Cerrar las ofertas hace la oferta del proyecto de solo lectura y crea un borrador del contrato del proyecto que contiene la información de la oferta. Puesto que una oferta cerrada no se puede volver a abrir, los cambios se confirmarán con un cuadro de diálogo de confirmación.

Si la oferta se adjunta a una oportunidad, cualquier otra oferta de proyecto de la oportunidad se cierra automáticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financiero de cerrar una oferta como Ganada

Si hay datos reales de tiempo en un proyecto mientras aún está adjunto a un borrador de oferta, solo se registra el coste del tiempo o gasto. Una vez que una oferta se cierra como Ganada, la aplicación refactorizará los costes al revertir los costes reales más antiguos y volver a crear nuevos costes reales. La aplicación procesará estos costes reales según el método de facturación de la línea de contrato del proyecto asociado. Si los datos reales de costes hacen referencia a una línea de contrato de tiempo y material, se crean los datos reales de ventas no facturados correspondientes para cuando se cierre la cotización y se cree el contrato de proyecto. Si el coste real hace referencia a una línea de contrato de precio fijo, la aplicación dejará de volver a procesar los costes reales que se basan en las reglas de facturación divididas para los clientes del contrato de proyecto.

## <a name="closing-a-quote-as-lost"></a>Cerrar una oferta como perdida

Al cerrar una oferta de proyecto como Perdida, el estado se establece en Cerrada y la razón para el estado será Perdida. Cerrar la oferta hace que la oferta del proyecto sea de solo lectura. Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.

Si la oferta de proyecto que se cierra como Perdida hace referencia a un proyecto en cualquiera de sus líneas, ese proyecto también se marcará como Cerrado. Se cancelan todas las reservas de recursos a partir de ese día.

> [!NOTE]
> En Project Operations, cerrar una oferta como Ganada o Perdida no afectará el estado de la Oportunidad, que permanecerá abierta hasta que se cierre manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
