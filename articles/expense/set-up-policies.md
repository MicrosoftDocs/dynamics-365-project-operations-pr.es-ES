---
title: Definir directivas de gastos
description: Puede definir directivas de gastos que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128439"
---
# <a name="define-expense-policies"></a>Definir directivas de gastos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede definir directivas que sus trabajadores deben seguir al introducir y enviar informes de gastos y solicitudes de viaje.         
La implementación de directivas de gastos puede ayudarle a administrar los gastos de manera eficaz.         

Por ejemplo, puede establecer una directiva para los gastos de hotel en la ciudad de Nueva York, que establece que el gasto por noche no puede exceder los 250 USD.       
Si un trabajador presenta un informe de gastos o una solicitud de viaje donde la tarifa por habitación excede esta cantidad, el sistema notificará al         
trabajador que se ha excedido el importe de la directiva de gastos. Puede configurar el mensaje que recibirá el trabajador cuando        
defina la directiva.      
        
Puede definir tres tipos de directivas:         
        
- **Advertencia**: Permite al trabajador enviar un informe de gastos o una solicitud de viaje, pero el gasto se marcará para todos los aprobadores y         
  para informes posteriores.        

- **Error**: Requiere que el trabajador revise el gasto para cumplir con la directiva antes de enviar el informe de gastos o la solicitud de viaje.        
 
 - **Justificación**: Requiere que el trabajador o un gerente introduzca una justificación por exceder el importe de la directiva antes de enviar el informe de gastos o la solicitud de viaje.        

## <a name="policy-tips"></a>Sugerencias de directiva
A continuación, se incluyen algunas sugerencias que pueden ayudarle a crear nuevas directivas para la administración de gastos: 

- Las directivas tienen fecha de vigencia, lo que significa que una directiva no surtirá efecto si se crea con una fecha posterior a la fecha en que se produjo el gasto. Por ejemplo, hoy crea una nueva directiva para establecer un gasto máximo de comida de 50 USD. Cualquier gasto existente introducido a partir de ayer no se comprobará con esta directiva.
- Al crear una directiva para una categoría de gastos que se puede desglosar, considere la posibilidad de agregar una condición para el tipo de línea de gastos. Puede que algunas directivas, como exigir un recibo, no tengan sentido para las líneas desglosadas. En esta situación, la directiva solo se aplica a la línea de encabezado o a una línea no desglosada. 
- Las directivas de administración de gastos se evalúan respecto a la entidad de origen de forma predeterminada. Para los escenarios de empresas vinculadas, en su lugar puede establecer que la directiva se evalúe con respecto a la entidad de destino (entidad prestataria). Para ejecutar las directivas en la entidad de destino, active la característica **Evaluar la directiva con respecto a la entidad jurídica prestataria** en el área de trabajo **Administración de característica**.

## <a name="when-to-evaluate-policies"></a>Cuándo evaluar las directivas

En los parámetros de administración de gastos, puede seleccionar la opción de evaluar las directivas de administración de gastos cuando se guarda una línea o cuando se envía un informe de gastos. Si opta por evaluar cuándo se guarda una línea, los usuarios tendrán una visibilidad más temprana de lo que deben hacer para completar su informe de gastos de una vez. De lo contrario, puede retrasar la evaluación de la directiva y ahorrar tiempo validando al final, durante el envío al flujo de trabajo.
