---
title: Dietas
description: Este artículo proporciona información acerca de las reglas de dietas que se utilizan en Gestión de gastos.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930201"
---
# <a name="per-diems"></a>Dietas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Una dieta es un subsidio que se paga a un trabajador que viaja por trabajo. En la gestión de gastos, puede crear reglas de dietas para diversas situaciones de viaje. Las tarifas de dietas pueden basarse en la época del año, el lugar de viaje o ambos. Cuando crea una regla de dietas, puede especificar que se retendrá un porcentaje de la tarifa de dieta si un trabajador recibe comidas o servicios gratuitos. También puede establecer un número mínimo y máximo de horas que la tarifa de dieta puede aplicar al viaje de un trabajador.

## <a name="configuration"></a>Configuración 

1. Para agregar ubicaciones de dietas, vaya a **Configurar** > **Cálculos y códigos** > **Ubicaciones de dietas**.
2. Para cada una de las ubicaciones agregadas anteriormente, seleccione una tarifa de dieta y una moneda que sea válida entre una fecha de inicio y finalización específicas para el hotel, las comidas y otros gastos. Las tasas de dietas y las monedas se configuran en **Configurar** > **Cálculos y códigos** > **Dietas**.
3. En la página **Ubicaciones de dietas**, configure niveles de tarifas de dietas. Los niveles de tarifas de dietas le permiten definir la división porcentual de una asignación diaria para hotel, comidas y otros gastos. 
4. Para especificar la reducción del porcentaje de comida para el desayuno, el almuerzo o la cena, actualice los campos de la página **Parámetros de gestión de gastos** en la pestaña **Dietas**. 
    
## <a name="submit-expenses-using-per-diem"></a>Enviar los gastos utilizando dietas
Para enviar gastos utilizando dietas, use la categoría de gastos **Dietas** al crear un informe de gastos. Introduzca **Dietas desde la fecha**, **Dietas hasta la fecha**, y la **Ubicación de dietas**. La cantidad se calculará en función de las tarifas de dietas para la ubicación seleccionada y la reducción de comidas se calculará en función de los niveles de tarifas de dietas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]