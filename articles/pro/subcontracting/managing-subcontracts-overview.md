---
title: Administración de subcontratos en Project Operations
description: Este tema proporciona una descripción general del proceso completo de gestión de subcontratos, normalmente para organizaciones basadas en proyectos.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323617"
---
# <a name="subcontract-management-in-project-operations"></a>Administración de subcontratos en Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema proporciona una descripción general del proceso completo de gestión de subcontratos, para organizaciones basadas en proyectos. La subcontratación de servicios generalmente sigue el flujo de proceso de negocio que se muestra en el siguiente diagrama.

![Flujo del proceso de subcontratación](../media/SubcontractingProcessFlow.png)

La lista siguiente describe paso a paso el proceso de subcontratación.

1. El administrador del proyecto crea un subcontrato con un proveedor. De forma predeterminada, las listas de precios que se adjuntan al registro de proveedor se usan para el subcontrato. La cuenta de proveedor tiene un tipo de relación de **Proveedor** o **Distribuidor**.
2. El administrador del proyecto puede desglosar todas las compras como elementos de línea en el subcontrato. Las líneas del subcontrato pueden ser por tiempo, gastos o productos. La clase de transacción de la línea de subcontrato determina para qué es la línea.
3. El administrador de cuentas del proveedor y el administrador del proyecto pueden iterar sobre el subcontrato. Los precios se pueden ajustar en las listas de precios de compra que estén asociadas al subcontrato.
4. En este punto o más adelante en el proceso, si la línea de subcontrato es por tiempo, el administrador de cuentas del proveedor asocia los contactos del proveedor con cada línea de subcontrato. Esta asociación proporciona información al administrador del proyecto que está trabajando en el subcontrato. Cuando un contacto de proveedor está asociado con una línea de subcontrato, el sistema crea automáticamente un recurso reservable desde el contacto, si aún no existe un recurso reservable.
5. El método de facturación en cada línea de subcontrato puede ser **Precio fijo** o **Tiempo y material**. Para las líneas de subcontratos de precio fijo, se configura un programa de facturación basado en hitos.
6.  Una vez que se configura el subcontrato y se completa la negociación, se confirma. Los subcontratos confirmados no se pueden editar, pero si se producen cambios, un subcontrato se puede 'reabrir para modificaciones', lo que establece el estado de **Confirmado** de regreso a **Borrador** y se puede reabrir la negociación. 
7.  Al crear un miembro del equipo genérico en un proyecto, el miembro del equipo se puede asociar a una línea de subcontrato. Esto indica la necesidad de dotar de personal al miembro del equipo genérico con capacidad de subcontratista.
8.  Los miembros del equipo designados pueden crearse directamente en un proyecto o crearse reservándolos utilizando las experiencias de programación de recursos. Si un miembro del equipo del proyecto designado es un trabajador por contrato, es posible asociarlo a una línea de subcontrato. Esto reducirá la capacidad disponible en una línea de subcontrato.
9.  Los recursos de los subcontratistas pueden registrar el tiempo, los gastos y el uso de materiales en proyectos y tareas del proyecto, y luego enviarlos para su aprobación. Esto es similar para los empleados. Al registrar el tiempo, un trabajador contratado puede seleccionar un subcontrato específico y una línea de subcontrato.
10. Tras la aprobación, el tiempo aprobado por los subcontratos registrará los costes reales del proyecto en función del precio de compra del trabajador contratado o del papel que desempeñó en el proyecto.
11. Las facturas de proveedor y los artículos de línea de factura de proveedor se pueden registrar en el sistema para el trabajo realizado por los recursos del proveedor o los productos entregados por el proveedor. Las líneas de la factura del proveedor deben ser específicas para un proyecto y para una clase de transacción de tiempo, gasto, producto/material, hito o tarifa. Opcionalmente, las líneas de factura de proveedor pueden hacer referencia a una línea de subcontrato.
12. El sistema asociará automáticamente todos los costes reales que coincidan con la línea de subcontrato y el proyecto con la factura del proveedor. Esto facilitará un proceso de verificación y coincidencia de 3 vías.
13. El administrador del proyecto puede entonces revisar los datos reales del proyecto que coinciden automáticamente, eliminar o agregar otros datos reales de los costes del proyecto y completar el proceso de verificación.
14. Completar el proceso de verificación en todas las líneas marcará la factura del proveedor como **Lista para el pago**. En esta fase, la factura del proveedor y las líneas se pueden transferir a un sistema de contabilidad o de proveedores para procesar el pago al proveedor. Los costes del proyecto previamente registrados se revertirán y los costes reales de la línea de factura del proveedor se registrarán en el proyecto.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Líneas de subcontrato basadas en cantidad y líneas de subcontrato basadas en trabajo

Una línea de subcontrato puede basarse en cantidades o en trabajo. 

Cuando una línea de subcontrato es **basada en cantidad**, la cantidad que se compra en la línea de subcontrato por tiempo, gasto o material se puede utilizar en cualquier proyecto.

Cuando una línea de subcontrato es **basada en trabajo**, la línea de subcontrato se asigna a un cuerpo de trabajo representado por un nodo en el plan del proyecto. El valor de la línea de subcontrato es la suma de todos los componentes que se requieren para entregar ese cuerpo de trabajo. Estos se modelan como detalles de la línea de subcontrato y pueden ser una colección de tiempo, gastos o materiales. Para una línea de subcontratación basada en trabajo, la línea de subcontrato también se dedica a un solo proyecto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

