---
title: Copiar contratos de proyecto (lite)
description: Este tema proporciona información sobre la copia de contratos de proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4137fc400c7fdd8fecd9d8349bf7f57f3470b51f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181428"
---
# <a name="copy-project-contracts---lite"></a>Copiar contratos de proyecto (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Puede crear fácilmente nuevos contratos de proyecto haciendo copias de los contratos existentes de una de estas dos formas: 

  - En la página de lista **Contratos de proyecto**, seleccione un contrato de proyecto y después seleccione **Copiar**.
  - En la página de detalles **Contrato de proyecto**, seleccione **Copiar**.

Se abrirá una página de diálogo donde puede seleccionar los parámetros del contrato copiado. Los siguientes campos se incluyen en el diálogo. Dependiendo de los valores que seleccione en este diálogo, el proceso de copia puede cambiar.

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Tema | Especifique el tema del contrato de destino. Cuando se abre la página de diálogo, el sistema establecerá este campo al nombre del contrato de origen con **copia** al final. | No hay impacto posterior para este campo. |
| Cliente | Referencia al registro de cuenta o empresa del cliente. Cuando se abre el cuadro de diálogo, el sistema establecerá este campo a la cuenta del contrato de origen. | Este campo es el cliente principal del contrato. |
| Unidad de contratación | La unidad organizativa responsable de la entrega de los proyectos asociados a esta oferta. Cuando se abre la página de diálogo, el sistema lo establecerá en la unidad de contratación del contrato de origen. | La unidad de contratación es la división de la empresa que ejecutará los proyectos una vez cerrada la oferta. Cada unidad contratante tiene una divisa. Esta divisa se utiliza para informar de los costes estimados y reales incurridos durante el proyecto. |
| Divisa | La divisa en la que se realiza la transacción de la oferta. Cuando se abre la página de diálogo, el sistema establecerá el campo en la moneda del contrato de origen. La moneda no se puede cambiar. Si lo es, el campo **Copiar precios** siempre se establece en **No** porque las listas de precios en el contrato de origen ya no son relevantes. | La moneda se usa para las listas de precios predeterminadas, estimaciones financieras de construcción en el contrato y para facturar al cliente cuando se gana la oferta. |
| Fecha de entrega solicitada | La fecha de entrega solicitada por el cliente. | Esta fecha se usa como la fecha de finalización al crear fechas de facturación con una frecuencia específica. |
| Copiar precios | Indica si el precio de la cotización del contrato debe copiarse del contrato de origen. | Si el campo se establece a **Sí**, las referencias al proyecto y la lista de precios de productos se copian del contrato origen al de destino. Si se selecciona **No**, las listas de precios vuelven al predeterminado basado en las últimas listas de precios en los parámetros de la cuenta o proyecto. |

Cuando selecciona **Aceptar** en la página de diálogo, el sistema crea una copia del contrato basada en los parámetros seleccionados en el diálogo. Se abrirá el nuevo contrato.

La siguiente información no se copia del **Origen** al **Contrato de destino**:

  - Programar facturas
  - Clientes de contrato y línea de contrato
  - Referencia del proyecto en las líneas de contrato basadas en proyectos
  - Información del presupuesto del cliente

Debido a que esta información es muy específica para cada contrato, estos campos y registros no se copian. Se copian las líneas de contrato para proyectos y productos, las estimaciones sobre los detalles de la línea de contrato y los valores que no deben excederse a nivel de contrato. Los valores predeterminados de precio y tasa de coste dependen de la selección en el campo **Copiar precios** en la página de diálogo **Copiar parámetros**.
