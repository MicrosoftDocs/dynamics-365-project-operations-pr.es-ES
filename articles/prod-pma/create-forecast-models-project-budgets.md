---
title: Crear modelos de pronóstico para presupuestos de proyectos
description: Este tema describe cómo crear un modelo de previsión para los presupuestos restantes.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085284"
---
# <a name="create-forecast-models-for-project-budgets"></a>Crear modelos de pronóstico para presupuestos de proyectos 

[!include [banner](../includes/banner.md)]

Este tema describe cómo crear un modelo de previsión para los presupuestos restantes. Un proyecto que está sujeto a control presupuestario utiliza dos tipos de presupuestos: original y restante. Cuando crea un presupuesto de proyecto, debe especificar los modelos de previsión presupuestaria original y restante que se crearon en la página **Modelos de pronóstico**. Los presupuestos del proyecto basados en los modelos especificados se crean cuando compromete el presupuesto del proyecto.

> [!NOTE]
> Un modelo de previsión que se utiliza para el control presupuestario no puede tener un submodelo ni utilizarse como submodelo.

1. Seleccione **Gestión de proyectos y contabilidad** > **Configuración** > **Pronósticos**  > **Modelos de pronóstico**.
2. Seleccione **Nuevo** para crear un nuevo modelo de pronóstico y luego ingrese un número de identificación de modelo y un nombre para el nuevo modelo. 
3. Establezca la opción **Detenido** a **Sí** para evitar cambios en las líneas de pronóstico del modelo de pronóstico. 
4. Si las líneas de pronóstico con las que está asociado el modelo deben generar pronósticos de flujo de efectivo en el libro mayor, establezca **Incluir en las previsiones de flujo de caja** a **Sí.** 
5. Para usar la fecha del proyecto como la fecha de la factura, establezca **Fecha de la factura prevista** a **Sí**. 
6. En el campo **Tipo de presupuesto** , seleccione uno de los siguientes tipos de modelo:

   - **Presupuesto original** : utilice los importes del presupuesto original que se comprometen cuando se crea y aprueba el presupuesto inicial.
   - **Presupuesto restante** : utilice los importes restantes del presupuesto durante la vida del proyecto. Los saldos en este modelo de pronóstico se reducen por transacciones reales y aumentan o disminuyen por revisiones presupuestarias.
   - **Transferir** : use los importes del presupuesto transferidos para el proyecto. Transferir es un proceso opcional que se puede ejecutar para transferir los importes presupuestarios no utilizados de un año fiscal a otro.

7. Establezca las siguientes opciones según sea necesario:

   - Habilite **Fecha de la factura prevista** para usar la fecha del proyecto como fecha de la factura.
   - Habilite **Previsión con WIP** para pronosticar según el trabajo en curso (WIP) y, a continuación, seleccione el tipo de WIP. 
   - Puede mantener el **Tipo de presupuesto** predeterminado como **Ninguno** o introducir un nuevo tipo. El tipo de presupuesto no se puede cambiar después de cambiar un registro.     
    > [!NOTE]
    > Si cambia el tipo de presupuesto predeterminado, todas las demás opciones no estarán disponibles para las actualizaciones y no podrá reutilizar este modelo de previsión. 
   


 

