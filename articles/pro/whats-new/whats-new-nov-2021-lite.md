---
title: 'Novedades de noviembre de 2021: implementación de Project Operations Lite'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2021 de la implementación de Project Operations Lite.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0fd910fb1b1e4e4576afa386a600e56e6f2dd504
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942952"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novedades de noviembre de 2021: implementación de Project Operations Lite

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en la versión del entorno de Dataverse 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- Las interfaces de programación de aplicaciones (API) de programación de proyectos ahora admiten la capacidad de crear y eliminar depósitos de proyectos

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-in-dataverse"></a>Project Operations en Dataverse

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Facturación y precios | 2358236 | La corrección de facturas debe permitir correcciones que tengan líneas de precio cero. |
| Administración de recursos | 2410072 | Permite la configuración de un recurso que está asignado a la tarea como un administrador de proyecto. |
| Facturación y precios | 2430234 | Solucione un problema de cálculo de rendimiento de costos. |
| Tiempo y gasto | 2436978 | Permita que se ingrese el tiempo en formato hh:mm. |
| Facturación y precios | 2448623 | Permitir que las listas de precios se actualicen después de que estén asociadas a una unidad organizativa. |
| Tiempo y gasto | 2460396 | Permita que se elimine una entrada de tiempo borrando la celda. |
| Facturación y precios | 2467386 | Permita que se elimine un proyecto que tiene una tarea, incluso cuando la tarea esté asociada con una cotización ganada. |
| Tiempo y gasto | 2461744 | La vista **Mi aprobación fallida** solo contiene aprobaciones de proyectos con un estado de **Enviado**. |
| Tiempo y gasto | 2464082 | Elimine el enlace de aprobaciones de proyectos al conjunto de aprobaciones cuando se coincida con un estado de destino. |
| Tiempo y gasto | 2468108 | El trabajo de programación no debe establecer un estado **Procesando** del conjunto de aprobaciones. |
| Tiempo y gasto | 2471503 | Elimine los conjuntos de aprobación que tengan siete días de antigüedad. |
| Facturación y precios | 2480687 | La referencia de la línea de cotización no debe eliminarse cuando se crea un hito de la línea de cotización. |
