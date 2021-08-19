---
title: Eliminar una estimación de proyecto
description: Este tema proporciona información sobre cómo eliminar una estimación de proyecto una vez que se ha completado.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a7c9f5a03e3b5e9ad43e23c6174a820088025dc8419ae4f80d247d69e80c8038
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994117"
---
# <a name="eliminate-a-project-estimate"></a>Eliminar una estimación de proyecto

[!include [banner](../includes/banner.md)]

Las estimaciones del proyecto proporcionan la vista financiera del trabajo estimado y programado para un proyecto. Para trabajar con estimaciones para un proyecto, debe adjuntar el proyecto a un proyecto de estimación. Un proyecto de estimación siempre se basa en un proyecto existente, sin embargo, varios proyectos pueden referirse a un solo proyecto de estimación. Solo se pueden adjuntar proyectos de inversión y de precio fijo a los proyectos de estimación, y esos proyectos deben pertenecer al mismo grupo de proyectos que el proyecto de estimación.

Para eliminar un proyecto de presupuesto, debe estar completo. Los siguientes pasos explican cómo eliminar una estimación.

1. Vaya a **Gestión de proyectos y contabilidad** > **Todos los proyectos** y abra el proyecto. 
2. En la pestaña **Gestionar**, seleccione **Estimaciones**, y en la página **Estimación** seleccione **Eliminar**.
3. En la página **Eliminar estimación** en la pestaña **General**, configure las siguientes opciones:

   - **Código de período**: seleccione el código de período para elegir los proyectos de estimación adecuados. 
   - **Fecha estimada**: seleccione la fecha estimada adecuada para la eliminación.
   - **Eliminar con advertencias WIP**: habilite esta opción para proporcionar una notificación cuando se elimine una estimación asociada con un trabajo en curso (WIP). Cuando esta opción no está habilitada, la eliminación no puede continuar si existen transacciones no estimadas. 
   > [!NOTE]
   > Esta opción está disponible solo cuando la eliminación se aplica a un proyecto de estimación. No está disponible si utiliza contabilizaciones periódicas. Esta configuración funciona con la configuración de la pestaña **Estimación** en la página **Parámetros del proyecto**, en el grupo de campo **Permitir la eliminación cuando existan transacciones no estimadas**.
   - **Establecer escenario para Terminado**: habilite esta opción para establecer la etapa del proyecto de estimación en **Terminado** después de ejecutar la eliminación.
   - **Imprimir lista de estimación**: seleccione la información que se incluirá cuando se imprima la lista de estimación.
   - **Mostrar Infolog**: habilite esta opción para mostrar el Infolog.
   - **Fecha de publicación**: elija la fecha de registro del libro mayor del presupuesto.

4.  Seleccione **Aceptar**.
5. Una vez completado el proceso de eliminación, el proyecto de estimación eliminado se muestra con un valor negativo. 

Si no tenía la intención de eliminar una estimación, puede seleccionar la estimación eliminada y seleccionar **Eliminación inversa**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]