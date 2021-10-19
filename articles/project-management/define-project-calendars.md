---
title: Definir calendarios de proyectos
description: Este tema proporciona información sobre cómo aplicar una plantilla de calendario a un proyecto para realizar un seguimiento de la programación del proyecto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487661"
---
# <a name="define-project-calendars"></a>Definir calendarios de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Para crear y administrar un proyecto, debe aplicar una plantilla de calendario al proyecto. La plantilla de calendario define los siguientes atributos del proyecto:

- Horas laborables, incluida la hora de inicio y finalización
- Días laborables
- Excepciones de calendario, como días no laborables

La plantilla de calendario que se aplica a un proyecto es una copia de la plantilla de calendario definida en la configuración de su organización.

> [!NOTE]
> Si cambia la plantilla del calendario, esos cambios no se propagan a las horas laborables del proyecto. Para cambiar las horas laborables del proyecto se debe aplicar una nueva plantilla.

Para crear una plantilla de calendario para su organización, existen dos requisitos clave:

- Defina las horas laborables deseadas de la plantilla utilizando un recurso que se puede reservar nuevo o existente.
- Cree una nueva plantilla de calendario y asóciela con el recurso que se puede reservar.

**Defina las horas laborables de la plantilla**

1. Vaya a **Recursos** \> **Recursos**.
2. Cree un nuevo recurso al que hacer referencia en la plantilla de calendario o seleccione un recurso existente.
3. Seleccione la pestaña **Horas laborables** del recurso y complete las instrucciones de [Establecer horas laborables para un recurso](/dynamics365/field-service/set-work-hours-resource) para configurar las reglas del calendario.

**Cree una nueva plantilla de calendario**

1. Vaya a **Configuración** \> **Plantilla de calendario**.
2. Seleccione **Nuevo** e ingrese un nombre, una descripción y un recurso de plantilla.

> [!NOTE]
> Cuando se hace referencia a un recurso en una plantilla de calendario, se asocia una copia del calendario del recurso con la plantilla de calendario. Si cambian las horas laborables de la plantilla copiada, esos cambios no se propagarán a la plantilla del calendario.

Ahora puede asociar la plantilla de trabajo con una plantilla de calendario de proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

