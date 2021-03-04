---
title: Proyectos de estimación de ingresos a precio fijo
description: En este tema se proporciona información sobre los ingresos a precio fijo en proyectos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531564"
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