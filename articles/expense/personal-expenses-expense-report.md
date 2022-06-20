---
title: Trabajar con gastos personales en un informe de gastos
description: Este artículo proporciona información sobre cómo trabajar con los gastos personales incurridos por los empleados mientras viajan por motivos de negocios.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 1cda5151a32482f92c69402bcc0056d7b6572db8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922289"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Trabajar con gastos personales en un informe de gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

En un viaje de negocios, un empleado pueden cargar gastos personales en la tarjeta de crédito corporativa. Si no se ha definido un proceso para gestionar los gastos personales, el proceso de aprobación de informes de gastos podría verse interrumpido cuando el empleado envía el informe detallado de gastos.

Están disponibles dos métodos para trabajar con los gastos personales de un empleado:

  - **Pagados por empleado**: su organización no paga los gastos personales que aparecen en la factura de la tarjeta de crédito corporativa. En lugar de ello, el empleado paga directamente los gastos al proveedor de la tarjeta de crédito. 
  - **Pagados por la empresa**: la organización paga la factura completa de la tarjeta de crédito corporativa y luego carga los gastos personales en la cuenta del empleado.

Puede seleccionar el método que utiliza su organización en la página **Parámetros de gestión de gastos**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido

La característica **Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido** solo se aplica a los informes de gastos aprobados mediante un flujo de trabajo de nivel de línea. Los informes se aprueban yendo a **Procesar informes de gastos** > **Informes de gastos asignados a mí** > **Abrir informe de gastos**. 

Para habilitar esta característica, vaya a **Espacios de trabajo** > **Gestión de funciones**, seleccione **Habilitar la función de gasto dividido cuando el campo de importe personal tenga un valor definido** y luego seleccione **Habilitar ahora**. 

Si la característica está habilitada, las líneas de gastos que utilizan esta funcionalidad generan dos líneas cuando se envía el informe. Se generan dos líneas para que el aprobador pueda aprobar cada línea por separado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
