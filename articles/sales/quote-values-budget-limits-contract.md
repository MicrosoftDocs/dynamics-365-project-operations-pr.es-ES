---
title: Configuración de oferta de proyecto
description: Este tema proporciona información sobre la información y la configuración que se aplican a las ofertas de proyectos e impactan en ellas.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9181fc1f6a4820662cb145abab55072e9743bbaa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011347"
---
# <a name="header-details-for-project-based-quotes"></a>Detalles del encabezado para ofertas basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Este artículo explica la información que se aplica a una oferta de proyecto. Esto incluye la configuración que afecta a todas las líneas de oferta e información sobre la oferta que se resume en todas las líneas de pedido para impulsar los KPI de la oferta del proyecto.

La siguiente tabla enumera los campos de información de resumen en una oferta de proyecto que son exclusivos de Dynamics 365 Project Operations o tiene algunos cambios importantes en el comportamiento de los presupuesots de Dynamics 365 Sales.

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Tipo | Pestaña Resumen (oculta) | El campo de conjunto de opciones tiene las siguientes opciones:</br>- Basado en el trabajo (disponible solo cuando está instalado Project Operations)</br>- Basado en artículo (disponible solo cuando están instalados Project Operations y Ventas)</br>- Servicio basado en mantenimiento (disponible cuando Dynamics 365 Field Service está instalado) | Cuando utiliza la aplicación Project Operations, el valor de este campo se establece automáticamente en **Basado en el trabajo**. Esto clasifica la oferta como oferta basada en proyecto. Una oferta debe basarse en proyecto para permitir todas las extensiones y funciones específicas del proyecto. |
| Empresa propietaria | Resumen | La entidad legal que contabilizará los costes e ingresos que se acumulen de este proyecto o proyectos asociados con esta oferta. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. | La empresa propietaria se equipara al concepto de entidad jurídica en el módulo **Gestión de proyectos y contabilidad** de Project Operations. Todos los costes e ingresos acumulados de este proyecto se contabilizarán en el libro mayor de la empresa propietaria. |
| Cliente potencial | Pestaña Resumen | Referencia al registro de cuenta o empresa del cliente. Un cliente válido a referenciar en la oferta del proyecto debe configurarse como cliente en la empresa propietaria de la oferta. La empresa propietaria muestra la lista de entidades jurídicas, y estas están configuradas en el módulo **Gestión de proyectos y contabilidad** de Project Operations. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. | La moneda de la oferta del proyecto se establece de forma predeterminada según la moneda del cliente. Esto, sin embargo, se puede cambiar antes de guardar la oferta. |
| Administrador de cuentas | Pestaña Resumen | El nombre del administrador de la cuenta de esta oferta. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. | El administrador de cuentas es responsable de gestionar la relación con el cliente hasta la finalización de este proyecto. Según el registro de recursos reservables vinculado al administrador de la cuenta, la unidad de contratación está predeterminada en la oferta de proyecto.|
| Unidad de contratación | Pestaña Resumen | La unidad organizativa responsable de la entrega del proyecto o los proyectos asociados a esta oferta. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. | La unidad de contratación es la división de la empresa que ejecutará los proyectos una vez cerrada la oferta. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar de los costes estimados y reales incurridos durante la ejecución del proyecto. |
| Lista de precios de productos | Pestaña Resumen | Esta es la lista de precios que se utiliza para los precios predeterminados en las líneas de oferta basadas en productos. La lista de opciones para este campo muestra una lista de listas de precios donde la moneda de la lista de precios coincide con la moneda de la oferta. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. Este campo de la oportunidad está predeterminado en el registro de la cuenta, pero se puede cambiar. | Cuando se gana una oferta, el valor del campo se copia en el contrato del proyecto que se crea. |
| Divisa | Pestaña Resumen | Esto indica la moneda que se utilizará para informar del valor de esta oferta. Esta es también la moneda en la que se facturará al cliente si se gana la oferta. Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. Este campo de la oportunidad está predeterminado en el registro de la cuenta, pero puede cambiarlo el usuario.  | Una vez que se guarda una oferta, este campo ya no se puede editar. Se usa para establecer el valor predetermiando de las listas de precios de productos y proyectos en la oferta. La moneda de la oferta se utiliza para coincidir con la moneda de la lista de precios. |
| Límite a no exceder | Pestaña Resumen | Esto indica el máximo negociado sobre el valor final que el cliente acepta para esta oferta. | Este límite se evalúa durante la ejecución y se aplica a todas las líneas de pedido y proyectos asociados con esta oferta. |
| Fecha de entrega solicitada | Pestaña Resumen | Cuando una oferta se crea a partir de una oportunidad, este campo se copia del campo correspondiente de la oportunidad. | Esta fecha se utiliza como fecha de finalización para generar programaciones de facturas. |

A continuación se muestran las pestañas y los KPI disponibles en una oferta de proyecto que son exclusivos de Project Operations o tienen algunos cambios importantes en el comportamiento de las ofertas de ventas:

| **Campo** | **Ubicación** | **Descripción** |
| --- | --- | --- |
| Análisis de rentabilidad | Pestaña de la oferta | La pestaña muestra las siguientes métricas:</br>- Coste imputable total</br></br>- Coste no imputable total</br>- Ingresos totales</br>- Ingresos totales (base)</br>- Margen bruto</br>- Margen bruto ajustado|
| Comparación con las expectativas del cliente | Pestaña de la oferta | Esta pestaña muestra las siguientes métricas:</br>- Finalización estimada</br>- Finalización solicitada</br>- Presupuesto del cliente</br>- Valor de oferta |
| Análisis de ofertas | Pestaña de la oferta | Esta pestaña resume los siguientes KPI principales de una oferta de proyecto</br>- Comparación con las expectativas del cliente en cuanto a presupuesto y programación</br>- Margen bruto</br>- Margen bruto ajustado |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
