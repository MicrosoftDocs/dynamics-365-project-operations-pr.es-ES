---
title: Configurar directivas de gasto
description: Puede configurar directivas de gastos que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje en Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005767"
---
# <a name="set-up-expense-policies"></a>Configurar directivas de gasto

Puede definir directivas que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.         
La implementación de directivas de gastos puede serle útil para gestionar de forma efectiva los gastos.         

Por ejemplo, puede establecer una directiva para los gastos de hotel en la ciudad de Nueva York, que establece que el gasto por noche no puede exceder los 250 USD.       
Si un trabajador presenta un informe de gastos o una solicitud de viaje donde la tarifa por habitación excede esta cantidad, el sistema notificará al        
trabajador que se ha excedido el importe de la directiva de gastos. Puede configurar el mensaje que recibirá el trabajador cuando        
defina la directiva.      
        
Puede definir tres tipos de directivas:         
        
- Advertencia: permite al trabajador enviar un informe de gastos o una solicitud de viaje, pero el gasto se marcará para todos los aprobadores y        
  para informes posteriores.        

- Error: requiere que el trabajador revise el gasto para cumplir con la directiva antes de enviar el informe de gastos o la solicitud de viaje.       
 
 - Justificación: requiere que el trabajador o un gerente introduzca una justificación por exceder el importe de la directiva antes de enviar el informe de gastos o la solicitud de viaje.        

## <a name="policy-tips"></a>Consejos para crear directivas
A continuación, se incluyen algunas sugerencias que pueden ayudarle a crear nuevas directivas para la administración de gastos. 
* Las directivas tienen fecha de vigencia, lo que significa que una directiva no surtirá efecto si se crea con una fecha posterior a la fecha en que se produjo el gasto. Por ejemplo, si está creando una nueva política hoy para imponer un gasto máximo de comida de $50, los gastos existentes ingresados a partir de ayer no se compararán con esta política.
* Al crear una directiva para una categoría de gastos que se puede desglosar, considere la posibilidad de agregar una condición para el tipo de línea de gastos. Algunas políticas, como exigir un recibo, pueden no tener sentido para las líneas detalladas y solo deben aplicarse a la línea del encabezado o a una línea no detallada. 
* Las directivas de administración de gastos se evalúan respecto a la entidad de origen de forma predeterminada. En los escenarios de empresas vinculadas, puede configurar la directiva para que se evalúe según a la entidad de destino (entidad prestataria) en su lugar. Para ejecutar las directivas en la entidad de destino, active la característica "Evaluar la directiva con respecto a la entidad jurídica prestataria" en el área de trabajo **Administración de característica**.

## <a name="when-to-evaluate-policies"></a>Cuándo evaluar las directivas

En los parámetros de administración de gastos, hay una opción para evaluar las directivas de administración de gastos cuando se guarda una línea o cuando se envía un informe de gastos. Si opta por evaluar cuándo se guarda una línea esto aseguro que los usuarios tendrán una visibilidad más temprana de lo que deben hacer para completar su informe de gastos de una vez. De lo contrario, puede retrasar la evaluación de la directiva y tiene una validación al final, durante el envío al flujo de trabajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]