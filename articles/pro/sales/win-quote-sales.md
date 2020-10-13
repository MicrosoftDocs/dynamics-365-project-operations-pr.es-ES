---
title: Cerrar ofertas
description: En este tema se proporciona información el cierre de una oferta en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896212"
---
# <a name="close-quotes"></a>Cerrar ofertas 

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las ofertas de proyectos se pueden cerrar como Ganadas o Perdidas. Las operaciones Activar y Revisar en ofertas no se admiten en Microsoft Dynamics 365 Project Operations, por lo que pueden cerrarse las ofertas en borrador.

## <a name="close-a-quote-as-won"></a>Cierre de oferta como Ganada

Cerrar una oferta de proyecto como Ganada cerrará la oferta con el estado puesto en Cerrada y la razón para el estado en Ganada. Cerrar las ofertas hace la oferta del proyecto de solo lectura y crea un borrador del contrato del proyecto que contiene la información de la oferta. Debido a que una oferta cerrada no se puede volver a abrir, existe un diálogo de confirmación antes de que se realicen los cambios, ya que una oferta cerrada no se puede volver a abrir y los cambios son irreversibles.

Si la oferta se adjunta a una oportunidad, cualquier otra oferta de proyecto de la oportunidad se cierra automáticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financiero de cerrar una oferta como Ganada

Si ha habido datos reales del tiempo registrado en un proyecto mientras aún está adjunto a un presupuesto preliminar, solo se registra el coste del tiempo o el gasto. Una vez que una oferta se cierra como Ganada, la aplicación refactorizará los costes al revertir los costes reales más antiguos y volver a crear nuevos costes reales. La aplicación procesará estos costes reales según el método de facturación de la línea de contrato del proyecto asociado. Si los costes reales hacen referencia a una línea de contrato de tiempo y material, el sistema creará automáticamente los correspondientes datos reales de ventas no facturadas para cuando se cierre la oferta y se cree el contrato del proyecto. Si los costes reales hacen referencia a una línea de contrato de precio fijo, la aplicación dejará de volver a procesar los costes reales en función de las reglas de facturación dividida para los clientes del contrato del proyecto.

## <a name="closing-a-quote-as-lost"></a>Cerrar una oferta como perdida:

Cerrar una oferta de proyecto como Perdida establecerá el estado de la oferta en Cerrado y la razón para el estado en Perdida. Cerrar la oferta hace que la oferta del proyecto sea de solo lectura. Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.

Si la oferta del proyecto que se cierra como Perdido tiene un proyecto referenciado en cualquiera de sus líneas, ese proyecto también se marca como Cerrado y se cancelan las reservas de recursos desde ese día en adelante.

> [!NOTE]
> En Project Operations, cerrar una oferta como Ganada o Perdida no afectará el estado de la Oportunidad, que permanecerá abierta hasta que se cierre manualmente.
