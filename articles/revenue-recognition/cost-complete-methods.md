---
title: Coste para completar métodos
description: Este artículo proporciona información sobre los métodos utilizados para calcular el costo para completar un proyecto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920311"
---
# <a name="cost-to-complete-methods"></a>Coste para completar métodos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este artículo proporciona información sobre los métodos utilizados para calcular el costo para completar un proyecto. Hay varios métodos que puede utilizar para calcular el coste de completar un proyecto. 

Cuando crea una estimación para un proyecto, en la página **Crear estimación**, en el campo **Coste para completar método**, puede seleccionar uno de los siguientes métodos de coste para completar.

| Coste para completar método    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coste total: real            | Introduzca los costes de estimaciones manualmente en los campos **Coste total** o **Cantidad total** mediante el botón **Coste estimado** de la **Página de estimación**. El sistema resta los costes reales de los totales que ha introducido. El total es el coste de completar el proyecto. Este método no utiliza las estimaciones de gastos y las asignaciones de recursos introducidas en Project Operations integradas en Microsoft Dataverse. El coste total o la cantidad total se pueden actualizar manualmente según sea necesario.  |
| Previsión total: real        | Las asignaciones de recursos y las estimaciones de gastos se utilizan para determinar el importe total de la previsión del proyecto. Los costes reales se comparan con esta previsión para calcular el coste de completar.                                                                                                                                                                                                                                                                          |
| Como la estimación anterior         | Aquí se utilizan los mismos métodos de estimación que se usaron en el período anterior. Este método requiere un modelo de previsión si el período anterior requirió un modelo de previsión.                                                                                                                                                                                                                                                                                                                           |
| Establecer en cero el costo para completar | Usado normalmente antes de que se elimine el proyecto de estimación, este método concilia las estimaciones totales con las transacciones reales registradas y borra la columna **Coste para completar**. Cuando se completa, el resultado es siempre del 100 por cien. Para cada línea de coste que cree, la casilla **Previsión** está desactivada y la estimación total se copia de la estimación de costes anterior. El consumo real para el período estimado se deduce del coste para completar el proyecto.              |
| De la plantilla de costes           | El método de coste para completar que se configura en la plantilla de costes que está asociada al proyecto de estimación seleccionado.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]