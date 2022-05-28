---
title: Registro de tiempo, gastos y uso de material para componentes subcontratados
description: Este tema explica cómo Microsoft realiza un seguimiento del tiempo, los gastos y el uso de materiales registrados en proyectos de componentes subcontratados por Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599245"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registro de tiempo, gastos y uso de material en proyectos para componentes subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema explica cómo Microsoft realiza un seguimiento del tiempo, los gastos y el uso de materiales registrados en proyectos de componentes subcontratados por Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Cálculo del costo del tiempo de los subcontratistas en los proyectos
En Project Operations, los trabajadores contratados pueden registrar el tiempo en los proyectos de manera similar a los empleados. Al ingresar tiempo en proyectos y / o tareas de proyectos, un trabajador por contrato puede seleccionar un subcontrato específico y una línea de subcontrato.

Cuando se aprueba el tiempo enviado por los trabajadores contratados, el costo del proyecto se registra utilizando la tasa de costo unitario que se configura para ese recurso de trabajador contratado en la sección **Precios de roles** de la lista de precios de compra en el subcontrato.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Cálculo del costo de los gastos subcontratados en los proyectos
Al ingresar los gastos incurridos en proyectos, puede seleccionar un subcontrato y una línea de subcontrato en la entrada de gastos. 

Cuando esta entrada de gasto se envía y aprueba, el coste del gasto se registra en el proyecto según el costo unitario que se configura para esa categoría de transacción en la sección **Precios de categorías** de la lista de precios de compra en el subcontrato.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Cálculo del costo de los materiales subcontratados en los proyectos
Al ingresar el uso de materiales en proyectos, puede seleccionar un subcontrato y una línea de subcontrato en el registro de uso de material. Cuando el registro de uso de material se envía y aprueba, el coste del material se registra en el proyecto según el costo unitario que se configura para ese producto en la sección **Elementos de lista de precios** de la lista de precios del subcontrato.

El uso de material también se puede registrar para productos de escritura en proyectos. Este tipo de uso de material también se puede vincular a un subcontrato y una línea de subcontrato. Al registrar el uso de material para productos inscritos, debe ingresar el costo unitario del producto inscrito. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
