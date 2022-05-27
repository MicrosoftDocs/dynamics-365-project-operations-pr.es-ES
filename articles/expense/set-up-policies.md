---
title: Definir directivas de gastos
description: Puede definir directivas de gastos que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ae6de664fc18a00fd6d3d6c8177daa95da5754d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576935"
---
# <a name="define-expense-policies"></a>Definir directivas de gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede definir directivas que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.         
La implementación de directivas de gastos puede serle útil para gestionar de forma efectiva los gastos.         

Por ejemplo, puede establecer una directiva de gastos para estancias en hoteles de Nueva York, en la que se establezca que el gasto por noche no puede superar los 250 USD.       
Si un trabajador presenta un informe de gastos o una solicitud de viaje donde la tarifa por habitación excede esta cantidad, el sistema notificará al         
trabajador que se ha excedido el importe de la directiva de gastos. Puede configurar el mensaje que recibirá el trabajador cuando        
defina la directiva.      
        
Puede definir tres tipos de directivas:         
        
- **Advertencia**: Permite al trabajador enviar un informe de gastos o una solicitud de viaje, pero el gasto se marcará para todos los aprobadores y         
  para informes posteriores.        

- **Error**: Requiere que el trabajador revise el gasto para cumplir con la directiva antes de enviar el informe de gastos o la solicitud de viaje.        
 
 - **Justificación**: Requiere que el trabajador o un gerente introduzca una justificación por exceder el importe de la directiva antes de enviar el informe de gastos o la solicitud de viaje.        

## <a name="policy-tips"></a>Consejos para crear directivas
A continuación, se incluyen algunas sugerencias que pueden serle útiles para crear nuevas directivas para la gestión de gastos: 

- Las directivas tienen una fecha de vigencia, lo que significa que una directiva no se aplicará si se crea con una fecha posterior a la fecha en que se produjo el gasto. Por ejemplo, supongamos que crea hoy una directiva nueva para imponer un gasto máximo de comida de 50 $. Todos los gastos que se introdujeron ayer no se regirán por esta directiva.
- Al crear una directiva para una categoría de gastos que se pueda detallar, sopese agregar una condición para el tipo de línea de gasto. Es posible que algunas directivas, como exigir un recibo, no tengan sentido para las líneas detalladas. En este caso, la directiva solo se aplicará a la línea de encabezado o en una línea no detallada. 
- De forma predeterminada, las directivas de gestión de gastos se evalúan conforme a la entidad de origen. En los escenarios de empresas vinculadas, puede configurar la directiva para que se evalúe según a la entidad de destino (entidad prestataria) en su lugar. Para ejecutar las directivas en la entidad de destino, active la característica **Evaluar la directiva con respecto a la entidad jurídica prestataria** en el área de trabajo **Administración de característica**.

## <a name="when-to-evaluate-policies"></a>Cuándo evaluar las directivas

En los parámetros de administración de gastos, puede seleccionar la opción de evaluar las directivas de administración de gastos cuando se guarda una línea o cuando se envía un informe de gastos. Si opta por evaluar cuándo se guarda una línea, los usuarios tendrán una visibilidad más temprana de lo que deben hacer para completar su informe de gastos de una vez. De lo contrario, puede retrasar la evaluación de la directiva y ahorrar tiempo validando al final, durante el envío al flujo de trabajo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]