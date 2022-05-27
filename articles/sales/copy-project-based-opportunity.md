---
title: Copiar oportunidades basadas en proyectos
description: En este tema se proporciona información sobre copiar oportunidades basadas en proyectos en Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ca48125d90ee50c5621780be19bd4ceb2130d2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577809"
---
# <a name="copy-project-based-opportunities"></a>Copiar oportunidades basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Las oportunidades de proyectos se pueden copiar fácilmente para crear nuevas oportunidades de proyectos. 

1. Vaya a la página de lista **Oportunidades de proyecto** y seleccione una oportunidad de la lista. O abra la página de detalles de una oportunidad específica. 
2. Desde cualquier página, seleccione **Copiar**. Se abrirá una página de diálogo que contiene la siguiente información de campo. Dependiendo de los valores que seleccionados en este diálogo, el proceso de copia puede cambiar.

    | **Campo** | **Descripción** | **Impacto posterior** |
    | --- | --- | --- |
    | Tema | Especifique el tema relevante de la oportunidad de destino. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en el tema de la oportunidad de origen con **-copia** al final. | No hay impacto posterior para este campo. |
    | Cuenta | Referencia al registro de cuenta o empresa del cliente. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la cuenta de la oportunidad de origen. | Este campo es el cliente principal de la oportunidad. |
    | Unidad de contratación | La unidad organizativa responsable de la entrega de los proyectos asociados a esta oferta. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la unidad de contratación de la oportunidad de origen. | La unidad de contratación es la división de la empresa que ejecuta los proyectos una vez cerrada la oferta. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar los costes estimados y reales incurridos durante el proyecto. |
    | Divisa | La divisa en la que se realiza la transacción de la oferta. Cuando se abre la página de diálogo, el sistema lo establecerá en la moneda de la oportunidad de origen. | La moneda se utiliza para predeterminar una lista de precios y generar estimaciones financieras en la cotización. Finalmente, la moneda se utiliza para facturar al cliente cuando se gana la oferta. |
    | Copiar precios | Un valor Sí / No que indica si el precio de la oportunidad debe copiarse de la oportunidad de origen. | Si se selecciona **Sí**, las listas de precios se copian desde el origen a la oportunidad de destino. Si se selecciona **No**, las listas de precios se vuelven a predeterminar en función de las últimas listas de precios que se configuraron. |

3. Seleccione **Aceptar**. El sistema crea una copia de la oportunidad de proyecto en función de los parámetros seleccionados y se abre la nueva oportunidad de proyecto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]