---
title: Líneas de oportunidad basadas en proyectos (lite)
description: En este tema se proporciona información sobre lineas de oportunidad basadas en proyectos. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 90b1b078d51c2842f6406c4455188a4433820a77
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994427"
---
# <a name="project-based-opportunity-lines---lite"></a>Líneas de oportunidad basadas en proyectos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las líneas de oportunidad basadas en proyectos solo están disponibles en oportunidades basadas en proyectos. Los registros de oportunidad basada en proyectos tienen el valor del campo **Tipo** establecido en **Basado en trabajo**.

Las líneas de oportunidad basadas en proyectos son los elementos de línea que se entregarán al cliente mediante un proyecto. Sin embargo, un proyecto no puede vincularse a una línea de oportunidades basada en proyectos. Los proyectos se pueden vincular a artículos de línea desde la fase **Oferta** en adelante, porque normalmente la oportunidad ocurre en una fase temprana del ciclo de vida de una oferta. La determinación de cuántos proyectos se utilizarán para entregar el trabajo al cliente es una decisión que se toma más adelante en la fase de ventas. Puede usar la fase de oportunidad para identificar los componentes de entrega discretos para el cliente. Las decisiones relacionadas con el número real de proyectos utilizados para entregar estos componentes se pueden postergar hasta que se conozca más información sobre el trabajo en sí.

A continuación, se muestran los campos de una línea de oportunidades basada en proyectos:

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Tipo de producto | Pestaña General (oculta) | Puede seleccionar una de las siguientes opciones:</br>- Servicio basado en proyectos (disponible solo cuando Dynamics 365 Project Operations está instalado)</br>- Producto (disponible solo cuando están instalados Project Operations y Dynamics 365 Sales) | El valor de este campo se establece en **Servicio basado en proyectos** cuando crea una línea de oportunidad basada en el proyecto a partir de la cuadrícula de líneas basadas en el proyecto en la oportunidad. <br> Si cambia o anula este valor, la funcionalidad del proyecto no se habilitará en sus líneas de pedido basadas en proyectos. |
| Oportunidad | Pestaña General | Este campo es de solo lectura y hace referencia al registro de oportunidad principal al que pertenece este artículo de línea. | No hay impacto posterior a partir de este campo. |
| Nombre | Pestaña General | Este es un campo de texto editable que se puede usar para dar una identidad corta del artículo de línea. | Este valor se transfiere a la línea de oferta cuando crea una oferta a partir de esta oportunidad. |
| Presupuesto del cliente | Pestaña General | Este campo de moneda editable se puede utilizar para realizar un seguimiento de la cantidad que el cliente está dispuesto a gastar en esta línea de pedido. | Este valor se transfiere al campo correspondiente de la oferta cuando crea una oferta a partir de esta oportunidad. |
| Método de facturación | Pestaña General | Este campo editable tiene los siguientes valores:</br>- Tiempo y material</br>- Precio fijo | Este valor se transfiere al campo correspondiente de la oferta cuando crea una oferta a partir de esta oportunidad. Una vez creada la línea de oferta, el campo se bloquea y no se puede cambiar. Asigne este valor de campo con la mayor precisión posible. Si necesita cambiar el valor de este campo en la línea de oferta, elimine y vuelva a crear la línea de oferta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]