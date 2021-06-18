---
title: Registrar uso de materiales en proyectos y tareas de proyectos
description: Este tema proporciona información sobre cómo registrar el uso de material en proyectos y tareas de proyectos.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001582"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registrar uso de materiales en proyectos y tareas de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

A medida que un equipo de proyecto trabaja en las tareas de un proyecto, consume o usa materiales. Un registro de uso de material proporciona una forma de registrar este uso para que pueda ser aprobado por el director del proyecto y eventualmente facturarse al cliente. 

Para registrar el uso del catálogo o materiales fuera de catálogo y enviarlos al aprobador, siga estos pasos: 

1. En el panel de navegación, seleccione **Uso de materiales** y luego seleccione **Nuevo**.
2. En la página **Nuevo uso de material**, escriba la información de uso de material requerida, y luego seleccione **Guardar**.

La siguiente tabla proporciona información sobre los campos en la página **Registro de uso de materiales**. 

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Descripción | Descripción del uso específico del material. | No hay impacto posterior para este campo. |
| Fecha | La fecha en la que se espera que se utilice el material. | No hay impacto posterior para este campo. |
| Project | Una lista de proyectos que están activos. | La selección de un proyecto para un registro de uso de materiales afecta al campo **Tarea** para que muestre solo las tareas que están en el proyecto. |
| Tarea | Una lista de tareas para el proyecto, incluidas las tareas de resumen y de nodo hoja. | La selección de una tarea para un registro de uso de material afecta al coste real del material y las ventas reales de material para una tarea. Si este campo se deja vacío, se realiza un seguimiento de las ventas y costes de uso de material correspondiente y se resume solo a nivel de proyecto. |
| Seleccionar producto | Especifique si este uso de materiales es para un producto **Existente** (catálogo) o un producto **Fuera de catálogo**. | Este campo determina el tipo de producto. |
| Producto | El identificador del producto del catálogo de productos. Cuando selecciona un identificador de producto, el campo **Seleccionar producto** se actualiza automáticamente a **Producto existente**. El identificador se utiliza para recuperar los precios de coste y venta de la lista de precios. | No hay impacto posterior para este campo. |
| Descripción de producto fuera de catálogo | Un campo de texto para escribir el nombre del producto. Este campo está disponible cuando selecciona un producto **Fuera de catálogo** en el campo **Seleccionar producto**.| No hay impacto posterior para este campo. |
| Recurso que se puede reservar| Recurso que utilizó este material en el proyecto. El valor predeterminado para este campo es el recurso reservable del usuario que inició sesión, pero se puede cambiar para registrar el uso en nombre de otros miembros del equipo del proyecto. | No hay impacto posterior para este campo. |
| Unidad de venta | El valor predeterminado en este campo proviene del grupo de unidades que está configurado como valor predeterminado en el producto de catálogo. Puede actualizar este campo para seleccionar otro grupo de unidades. | No hay impacto posterior para este campo. |
| Unidad | El valor predeterminado de este campo es la unidad predeterminada del producto seleccionado. Puede actualizar este campo para seleccionar otra unidad. | Cambiar la unidad da como resultado un precio y un coste unitarios predeterminados diferentes. |
| Cantidad | La cantidad de producto que se ha utilizado en el proyecto o la tarea del proyecto. | No hay impacto posterior para este campo. |
| Coste unitario | El coste unitario del producto seleccionado y la combinación de unidades según lo establecido en la lista de precios de coste aplicable. | El coste unitario siempre se muestra en la divisa de coste del proyecto. Si no hay un coste unitario para la combinación del producto y la unidad en la lista de precios, el coste unitario se establecerá por defecto en 0,00. |
| Coste total | El importe del coste que se calcula como cantidad \* coste unitario.| El importe de coste siempre se muestra en la divisa de coste del proyecto. |


## <a name="submit-material-usage-for-review-and-approval"></a>Enviar el uso del material para su revisión y aprobación 
Una vez que haya capturado todo el uso de material y esté listo para que se apruebe, debe enviar la información de uso para su revisión.

1. Vaya a **Registro de uso de material** y seleccione una o más entradas. O seleccione todos los registros de uso de material usando la casilla de verificación en el encabezado.
2. Seleccione **Enviar**. El sistema procesa las entradas seleccionadas y luego crea solicitudes de aprobación de uso de material.

## <a name="recall-a-material-usage-log"></a>Recuperar un registro de uso de material

Cuando sea necesario, puede recuperar un uso de material enviado. El tiempo necesario para recuperar una entrada de uso de material depende de la etapa de aprobación.  Si el aprobador aún no ha aprobado la entrada, la recuperación puede ocurrir de inmediato. Sin embargo, si la entrada ya se ha aprobado, se le pide al aprobador que apruebe la recuperación y revierta las transacciones.

1. Vaya a **Uso de material** y, en la lista de registros de uso de material, seleccione el uso de material que desea recordar.
2. Seleccione **Recuperar**. Si la entrada de uso de material aún no ha sido aprobada, el sistema la recupera inmediatamente. Si la entrada de material ya ha sido aprobada, se crea una solicitud de recuperación para notificar al aprobador que desea recuperar el uso del material. El aprobador luego confirmará que se puede realizar la reversión y se devolverá la entrada.

## <a name="delete-a-material-usage-log"></a>Eliminar un registro de uso de material

Puede eliminar los registros de uso de material que no se hayan enviado. Para eliminar un registro de uso de material que ya ha sido enviado, primero debe recuperarlo.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
