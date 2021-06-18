---
title: Crear una plantilla de horas de trabajo
description: Este tema explica cómo crear una plantilla de horas laborables en Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997217"
---
# <a name="create-a-work-hours-template-project-service"></a>Crear una plantilla de horas laborables (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Seleccione la pestaña **Horas laborables** del recurso y complete las instrucciones de [Establecer horas laborables para un recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar las reglas del calendario.

**Cree una nueva plantilla de calendario**

1. Vaya a **Configuración** \> **Plantilla de calendario**.
2. Seleccione **Nuevo** e ingrese un nombre, una descripción y un recurso de plantilla.


> [!NOTE]
> Cuando se hace referencia a un recurso en una plantilla de calendario, se asocia una copia del calendario del recurso con la plantilla de calendario. Si cambian las horas laborables de la plantilla copiada, esos cambios no se propagarán a la plantilla del calendario.


### <a name="see-also"></a>Vea también  
 [Configuración de recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
