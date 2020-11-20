---
title: Copiar ofertas basadas en proyectos
description: En este tema se proporciona información sobre cómo copiar ofertas basadas en proyectos en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4e70ed1451c1076f72ef5d7200b918c626ab23c
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181833"
---
# <a name="copy-project-based-quotes"></a>Copiar ofertas basadas en proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Puede crear fácilmente una nueva oferta de proyecto copiando una existente. 

- Para copiar una oferta de proyecto, enla página de lista **Ofertas de proyecto** o la página de detalles **Oferta del proyecto**, seleccione la oferta del proyecto que desea copiar y luego seleccione **Copiar**.

Esto abrirá una página de diálogo donde puede introducir los parámetros de la copia. En la tabla siguiente se enumeran loscampos incluidos en la página de diálogo: Dependiendo de los valores que seleccione, el proceso de copia puede cambiar.

| **Campo** | **Descripción** | **Impacto posterior** |
| --- | --- | --- |
| Tema | Introduzca el tema relevante, o el nombre, de la oferta objetivo. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en el tema de la oferta de origen con **-copia** al final. | |
| Cliente potencial | Referencia al registro de cuenta o empresa del cliente. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la cuenta de la oferta de origen. | Este campo es el cliente principal de la oferta. |
| Unidad de contratación | La unidad organizativa responsable de la entrega de los proyectos asociados a esta oferta.
Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la unidad de contratación de la oferta de origen. | La unidad de contratación es la división de la empresa que ejecutará los proyectos una vez cerrada la oferta. Cada unidad contratante tiene una divisa. La divisa se utiliza para informar de los costes estimados y reales incurridos durante la ejecución del proyecto. |
| Divisa | Esta es la divisa en la que se realiza la transacción de la oferta. Cuando se abre el cuadro de diálogo, el sistema lo establecerá en la divisa de la oferta de origen. Esto se puede modificar y, si se cambia, el campo **Copiar precios** siempre se establece en **No**. Esto se debe a que las listas de precios de la oferta original ya no son relevantes. | La moneda se utiliza para predeterminar una lista de precios, para generar un presupuesto financiero en la oferta y, finalmente, para facturar al cliente cuando se gana la oferta. |
| Fecha de entrega solicitada | Esta es la fecha de entrega solicitada por el cliente. | Se utiliza como fecha de finalización al crear fechas de facturación con una frecuencia específica. |
| Copiar precios | Un valor Sí/No indica si el precio de la oferta debe copiarse de la oferta de origen. | Si se selecciona **Sí**, la lista de precios del proyecto y las referencias de la lista de precios del producto se copian de la oferta de origen a la oferta de destino. Si se selecciona **No**, las listas de precios se vuelven a predeterminar en función de las últimas listas de precios que se configuraron en la cuenta o los parámetros del proyecto. |

Cuando selecciona **Aceptar** en la página de diálogo, el sistema crea una copia de la oferta del proyecto basada en los parámetros seleccionados en el diálogo. Se abre la nueva oferta del proyecto. 

> [!NOTE]
> La siguiente información no se copia del presupuesto de origen al de destino:
>
> - Programar facturas
> - Clientes de oferta y línea de oferta
> - Referencia del proyecto en el proyecto, líneas de oferta basadas, información del presupuesto del cliente
>
>Debido a que esta información es muy específica para cada oferta, estos campos y registros no se copian. Se copian las líneas de oferta para proyectos y productos, las estimaciones sobre los detalles de la línea de oferta y los valores que no deben excederse a nivel de oferta. Los valores predeterminados de precio y tasa de coste dependen de la opción **Copiar precios** seleccionada en la página de diálogo **Copiar parámetros**.
