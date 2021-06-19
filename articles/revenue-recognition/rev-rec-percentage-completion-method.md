---
title: Proyectos de estimación de ingresos a precio fijo
description: En este tema se proporciona información sobre los ingresos a precio fijo en proyectos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013822"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Proyectos de estimación de ingresos a precio fijo 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando crea una línea de contrato de proyecto con los siguientes atributos en Dynamics 365 Project Operations en Microsoft Dataverse, el sistema crea automáticamente un proyecto de estimación de ingresos a precio fijo. La información de este proyecto se basa en lo siguiente:

  - Un método de facturación de precio fijo.
  - Un proyecto asociado.
  - Al menos un hito definido en la pestaña **Programación de facturas** de la página **Línea de contrato de proyecto**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisar proyectos de estimaciones de ingresos a precio fijo
Para revisar proyectos de estimaciones de ingresos a precio fijo, complete los siguientes pasos:

1. En el entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Proyectos de estimación de ingresos a precio fijo**.
2. Seleccione el proyecto que desea ver y haga doble clic en el **Id. de proyecto de estimación** para abrir el registro y revisar sus detalles.
3. Expanda la pestaña **Proyecto**. Verá un proyecto en la cuadrícula **Proyectos seleccionados**. El sistema lo usa como proyecto predeterminado porque es el proyecto asociado a la línea de contrato del proyecto. 
4. Para cambiar la asociación, seleccione proyectos adicionales y agréguelos a la cuadrícula **Proyectos seleccionados**. Si se seleccionan varios proyectos en esta cuadrícula, el porcentaje de finalización del proyecto y las estimaciones de ingresos se calculan juntos para todos los proyectos seleccionados.

  El coste del proyecto, el perfil de ingresos, la plantilla de costes y el código de período se pueden configurar manualmente. Si no se configuran manualmente, los valores predeterminados durante el primer cálculo estimado para el proyecto utilizando las reglas configuradas para los perfiles de costes e ingresos del proyecto.



[!INCLUDE[footer-include](../includes/footer-banner.md)]