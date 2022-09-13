---
title: Copiar contratos basados en proyectos
description: Este artículo proporciona información sobre la copia de contratos de proyectos en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410340"
---
# <a name="copy-project-based-contracts"></a>Copiar contratos basados en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Puede crear fácilmente nuevos contratos de proyecto copiando los contratos existentes de una de estas dos formas:

- En la página de lista **Contratos de proyecto**, seleccione un contrato de proyecto y después seleccione **Copiar**.
- En la página de detalles **Contrato de proyecto**, seleccione **Copiar**.

En ambos casos, aparece un cuadro de diálogo en el que puede establecer los parámetros del contrato copiado. El cuadro de diálogo incluye los siguientes campos. Dependiendo de los valores que seleccione, el proceso de copia puede cambiar.

| Campo | Description | Impacto posterior |
| --- | --- | --- |
| Tema | Especifique el tema del contrato de destino. Cuando se abre el cuadro de diálogo, el sistema establece este campo al nombre del contrato de origen, pero con copia al final. | No hay impacto posterior para este campo. |
| Customer | Una referencia al registro de cuenta o empresa del cliente. Cuando se abre el cuadro de diálogo, el sistema establece este campo a la cuenta del contrato de origen. | Este campo es el cliente principal del contrato. |
| Empresa propietaria | La empresa responsable de la entrega de los proyectos asociados a esta oferta. Cuando se abre el cuadro de diálogo, el sistema establece este campo a la empresa propietaria del contrato de origen. | La empresa propietaria es la entidad jurídica que ejecutará el proyecto una vez cerrada la oferta. La divisa de la empresa propietaria debe coincidir con la divisa de la unidad contratante del proyecto. |
| Unidad de contratación | La unidad organizativa responsable de la entrega de los proyectos asociados a esta oferta. Cuando se abre el cuadro de diálogo, el sistema establece este campo a la unidad contratante del contrato de origen. | La unidad de contratación es la división de la empresa que ejecutará los proyectos una vez cerrada la oferta. Cada unidad contratante tiene una divisa. Esta divisa se utiliza para informar de los costes estimados y reales incurridos durante el proyecto. |
| Moneda | La divisa en la que se realiza la transacción de la oferta. Cuando se abre el cuadro de diálogo, el sistema establece el campo en la moneda del contrato de origen. La moneda no se puede cambiar. Si lo es, el campo **Copiar precios** siempre se establece en **No** porque las listas de precios en el contrato de origen ya no son relevantes. | Esta divisa se usa para las listas de precios predeterminadas, para generar estimaciones financieras en el contrato y para facturar al cliente cuando se gana la oferta. |
| Fecha de entrega solicitada | La fecha de entrega solicitada por el cliente. | Esta fecha se usa como la fecha de finalización al crear fechas de facturación con una frecuencia específica. |
| Copiar precios | Un valor que indica si el precio de la cotización del contrato debe copiarse del contrato de origen. | Si el campo se establece a **Sí**, las referencias al proyecto y la lista de precios de productos se copian del contrato de origen al de destino. Si está establecido en **No**, se usan las listas de precios predeterminadas en función de las últimas listas de precios en los parámetros de la cuenta o proyecto. |

Cuando selecciona **Aceptar** en el cuadro de diálogo, el sistema crea una copia del contrato basada en los valores de parámetros que ha establecido. Entonces, se abre el nuevo contrato.

La siguiente información **no** se copia del contrato de origen al contrato de destino, porque es específica de cada contrato:

- Programar facturas
- Clientes de contrato y línea de contrato
- Referencia del proyecto en las líneas de contrato basadas en proyectos
- Información del presupuesto del cliente

Se copian las líneas de contrato para proyectos y productos, las estimaciones sobre los detalles de la línea de contrato y los valores que no deben excederse a nivel de contrato. La entrada de tasas de precios y costes predeterminadas depende de la selección en el campo **Copiar precios** en el cuadro de diálogo **Copiar parámetros**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
