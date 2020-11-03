---
title: Cerrar una oferta
description: En este tema se proporciona información el cierre de ofertas en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085046"
---
# <a name="close-a-quote"></a>Cerrar una oferta

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las ofertas de proyectos se pueden cerrar como Ganadas o Perdidas. Debido a que las funciones Activar y Revisar no se admiten en ofertas de Microsoft Dynamics 365 Project Operations, puede cerrar un borrador de oferta.

## <a name="close-a-quote-as-won"></a>Cierre de oferta como Ganada

Cerrar una oferta de proyecto como Ganada establecerá el estado de la oferta en **Cerrado** y razón para el estado en **Ganada**. Cerrar las ofertas las hace de solo lectura y crea un borrador del contrato del proyecto con toda la información de la oferta. Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.

El contrato de proyecto creado a partir de una oferta de proyecto también está disponible en el módulo contable Gestión de proyectos de Project Operations. Si un contrato de proyecto no se asigna a un proyecto en ninguna de sus líneas, este contrato de proyecto se pone a disposición como un contrato de proyecto inactivo y se activa tan pronto como se asigna un proyecto a al menos una de sus líneas de contrato.

Si la oferta se adjunta a una oportunidad, cualquier otra oferta de proyecto de la oportunidad se cierra automáticamente como Perdida.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financiero de cerrar una oferta como Ganada

Si ha habido datos reales del tiempo registrado en un proyecto mientras aún está adjunto a un presupuesto preliminar, solo se registra el coste del tiempo o el gasto. Una vez que una oferta se cierra como Ganada, la aplicación refactorizará los costes al revertir los costes reales más antiguos y volver a crear nuevos costes reales. La aplicación procesará estos costes reales según el método de facturación de la línea de contrato del proyecto asociado. Si los costes reales hacen referencia a una línea de contrato de tiempo y material, el sistema creará automáticamente los correspondientes datos reales de ventas no facturadas para cuando se cierre la oferta y se cree el contrato del proyecto. Si los costes reales hacen referencia a una línea de contrato de precio fijo, la aplicación dejará de volver a procesar los costes reales en función de las reglas de facturación dividida para los clientes del contrato del proyecto.

Todos los datos reales reprocesados están disponibles en el módulo de contabilidad y gestión de proyectos para que el contable del proyecto los revise, actualice y registre en el libro mayor. 

## <a name="close-a-quote-as-lost"></a>Cerrar una oferta como Perdida

Cerrar una oferta de proyecto como Perdida establecerá el estado en **Cerrado** y la razón para el estado en **Perdida**. Cerrar la oferta hace que sea de solo lectura. Debido a que una oferta cerrada no se puede volver a abrir, antes de cerrar una oferta, un cuadro de diálogo de confirmación confirmará sus cambios.

Si la oferta del proyecto que se cierra como Perdido tiene un proyecto referenciado en cualquiera de sus líneas, ese proyecto también se marca como Cerrado y se cancelan las reservas de recursos desde ese día en adelante.

> [!NOTE]
> En Project Operations, cerrar una oferta como Ganada o Perdida no afectará el estado de la Oportunidad, que permanecerá abierta hasta que se cierre manualmente.
