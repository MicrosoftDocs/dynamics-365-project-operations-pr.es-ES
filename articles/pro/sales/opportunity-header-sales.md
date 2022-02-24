---
title: Configuración de oportunidades (lite)
description: Este tema proporciona información sobre acuerdos basados en proyectos y líneas de oportunidades basadas en proyectos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6631e136572b958ca616d708a5e3c3c2d9f2675c
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663840"
---
# <a name="header-details-for-project-opportunities"></a>Detalles del encabezado para oportunidades de proyectos

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

El encabezado de oportunidad captura la información general sobre una oferta basada en un proyecto que se aplica a todas las líneas de la oportunidad basada en un proyecto.

Las oportunidades basadas en proyectos en Dynamics 365 Project Operations son extensiones de oportunidades en Dynamics 365 Sales. Estas extensiones proporcionan funcionalidad adicional que es específica y necesaria para oportunidades basadas en proyectos. Estas extensiones pueden incluir nuevos campos y acciones de cinta disponibles en oportunidades basadas en proyectos. Es posible que algunos campos, funcionalidades y lógica predeterminada que están disponibles en Ventas no estén disponibles en Project Operations.

La siguiente tabla incluye los campos de una oportunidad basada en proyectos que son exclusivos de Project Operations o tienen algunos cambios importantes en el comportamiento según las oportunidades de Ventas.

| **Campo** | **Ubicación** | **Descripción** | **Impacto posterior** |
| --- | --- | --- | --- |
| Tipo | Pestaña General (oculta) | El campo de conjunto de opciones incluye las siguientes opciones:</br>- Basado en el trabajo (disponible solo con Project Operations)</br>- Basado en artículo (disponible solo cuando están instalados Project Operations y Ventas)</br>- Servicio basado en mantenimiento (disponible cuando se instala Field Service) | Cuando utiliza Project Operations, este valor de campo se establece automáticamente en **Basado en el trabajo** que clasifica la oportunidad como basada en proyecto. Una oportunidad debe estar basada en proyecto para habilitar todas las extensiones y funcionalidades específicas del proyecto en el proceso de ventas posterior de esta oferta. |
| CONTACTO | Pestaña General | Referencia al contacto principal del cliente para esta oferta. | |
| Cuenta | Pestaña General | Referencia al registro de cuenta o empresa del cliente. | |
| Administrador de cuentas | Pestaña General | El nombre del administrador de cuentas de esta oportunidad basada en proyecto. | El administrador de cuentas es responsable de gestionar la relación con el cliente hasta la finalización de este proyecto. Según el registro de recursos contables vinculado al administrador de la cuenta, la unidad de contratación está predeterminada. |
| Unidad de contratación | Pestaña General | La unidad organizativa responsable de la entrega del proyecto o los proyectos asociados a esta oferta. | La unidad de contratación es la división de la empresa que completará el proyecto o los proyectos una vez cerrada la oferta. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar los costes estimados y reales incurridos durante el proyecto. |

Para todos los demás campos y secciones de la pestaña **Resumen** de la oportunidad, consulte [Crear o editar oportunidades (Ventas y Centro de ventas)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
