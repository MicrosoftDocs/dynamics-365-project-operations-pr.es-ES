---
title: Encabezado de oportunidad
description: Este tema proporciona informacióngeneral sobre ofertas basadas en proyectos y las líneas de oportunidades basadas en proyectos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085076"
---
# <a name="opportunity-header"></a>Encabezado de oportunidad

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

El encabezado de oportunidad captura la información general sobre una oferta basada en un proyecto que se aplica a todas las líneas de la oportunidad basada en un proyecto.

Las oportunidades basadas en proyectos en Dynamics 365 Project Operations son extensiones de oportunidades en Dynamics 365 Sales. Estas extensiones proporcionan funcionalidad adicional que es específica y necesaria para oportunidades basadas en proyectos. Estas extensiones pueden incluir nuevos campos y acciones de cinta disponibles en oportunidades basadas en proyectos. Es posible que algunos campos, funcionalidades y lógica predeterminada que están disponibles en Ventas no estén disponibles en Project Operations.

La siguiente tabla incluye los campos de una oportunidad basada en proyectos que son exclusivos de Project Operations o tienen algunos cambios importantes en el comportamiento según las oportunidades de Ventas.

| **Campo** | **Ubicación** | **Relevancia, propósito y orientación** | **Impacto posterior** |
| --- | --- | --- | --- |
| Escribir | Pestaña General (oculta) | El campo de conjunto de opciones incluye las siguientes opciones:</br>- Basado en el trabajo (disponible solo con Project Operations)</br>- Basado en artículo (disponible solo cuando están instalados Project Operations y Ventas)</br>- Servicio basado en mantenimiento (disponible cuando se instala Field Service) | Cuando utiliza Project Operations, este valor de campo se establece automáticamente en **Basado en el trabajo** que clasifica la oportunidad como basada en proyecto. Una oportunidad debe estar basada en proyecto para habilitar todas las extensiones y funcionalidades específicas del proyecto en el proceso de ventas posterior de esta oferta. |
| CONTACTO | Pestaña General | Referencia al contacto principal del cliente para esta oferta. | |
| Cuenta | Pestaña General | Referencia al registro de cuenta o empresa del cliente. | |
| Administrador de cuentas | Pestaña General | El nombre del administrador de cuentas de esta oportunidad basada en proyecto. | El administrador de cuentas es responsable de gestionar la relación con el cliente hasta la finalización de este proyecto. Según el registro de recursos contables vinculado al administrador de la cuenta, la unidad de contratación está predeterminada. |
| Unidad de contratación | Pestaña General | La unidad organizativa responsable de la entrega del proyecto o los proyectos asociados a esta oferta. | La unidad de contratación es la división de la empresa que completará el proyecto o los proyectos una vez cerrada la oferta. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar los costes estimados y reales incurridos durante el proyecto. |

Para todos los demás campos y secciones de la pestaña **Resumen** de la oportunidad, consulte [Crear o editar oportunidades (Ventas y Centro de ventas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
