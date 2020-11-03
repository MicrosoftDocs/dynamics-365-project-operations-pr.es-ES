---
title: Copiar oportunidades basadas en proyectos
description: En este tema se proporciona información sobre copiar oportunidades basadas en proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085087"
---
# <a name="copy-project-based-opportunities"></a>Copiar oportunidades basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Las oportunidades de proyectos se pueden copiar fácilmente para crear nuevas oportunidades de proyectos. 

1. Vaya a la página de lista **Oportunidades de proyecto** y seleccione una oportunidad de la lista. O abra la página de detalles de una oportunidad específica. 
2. Desde cualquier página, seleccione **Copiar**. Se abrirá una página de diálogo que contiene la siguiente información de campo. Dependiendo de los valores que seleccionados en este diálogo, el proceso de copia puede cambiar.

    | **Campo** | **Relevancia, propósito y orientación** | **Impacto posterior** |
    | --- | --- | --- |
    | Tema | Especifique el tema relevante de la oportunidad de destino. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en el tema de la oportunidad de origen con **-copia** al final. | No hay impacto posterior para este campo. |
    | Cuenta | Referencia al registro de cuenta o empresa del cliente. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la cuenta de la oportunidad de origen. | Este campo es el cliente principal de la oportunidad. |
    | Unidad de contratación | La unidad organizativa responsable de la entrega de los proyectos asociados a esta oferta. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la unidad de contratación de la oportunidad de origen. | La unidad de contratación es la división de la empresa que ejecuta los proyectos una vez cerrada la oferta. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar los costes estimados y reales incurridos durante el proyecto. |
    | Divisa | La divisa en la que se realiza la transacción de la oferta. Cuando se abre la página de diálogo, el sistema lo establecerá en la moneda de la oportunidad de origen. | La moneda se utiliza para predeterminar una lista de precios y generar estimaciones financieras en la cotización. Finalmente, la moneda se utiliza para facturar al cliente cuando se gana la oferta. |
    | Copiar precios | Un valor Sí / No que indica si el precio de la oportunidad debe copiarse de la oportunidad de origen. | Si se selecciona **Sí** , las listas de precios se copian desde el origen a la oportunidad de destino. Si se selecciona **No** , las listas de precios se vuelven a predeterminar en función de las últimas listas de precios que se configuraron. |

3. Seleccione **Aceptar**. El sistema crea una copia de la oportunidad de proyecto en función de los parámetros seleccionados y se abre la nueva oportunidad de proyecto.
