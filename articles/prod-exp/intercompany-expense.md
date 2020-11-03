---
title: Gastos de empresas vinculadas
description: Un trabajador contratado por una entidad legal en una organización puede realizar trabajo para otra entidad legal en la misma organización. En esta situación, puede utilizar la función de gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085299"
---
# <a name="intercompany-expenses"></a>Gastos de empresas vinculadas

[!include [banner](../includes/banner.md)]

Un trabajador contratado por una entidad legal en una organización puede realizar trabajo para otra entidad legal en la misma organización. En esta situación, puede utilizar la función de gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo. La entidad jurídica que emplea al trabajador se denomina entidad jurídica prestamista. La entidad jurídica por la que el trabajador incurre en gastos se denomina entidad jurídica prestataria. 

Antes de que un trabajador pueda crear y enviar gastos por el trabajo que se realiza para una entidad legal diferente, en la entidad legal prestadora, en la página **Parámetros de gestión de gastos** , seleccione la opción **Permitir líneas de gastos de empresas vinculadas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impuestos para gastos de empresas vinculadas

[!include [banner](../includes/banner.md)]

Si desea utilizar grupos de impuestos que están asociados con la entidad jurídica prestamista (fuente) en lugar de la entidad jurídica prestataria (destino) en su informe de gastos, deberá configurar esto en la configuración del impuesto sobre las ventas del Libro mayor. Cuando el parámetro del libro mayor, **Entidad jurídica para la contabilización de impuestos entre empresas** se establece en **Origen** y **Aplicar reglas de impuestos sobre las ventas** se establece en **No** , se utilizará la combinación de impuestos para la entidad jurídica prestadora. Cuando el mismo parámetro se establece en **Destino** , se utilizará la combinación de impuestos para la entidad jurídica prestataria. Para las entidades legales en los Estados Unidos, cuando el parámetro se establece en **Origen** , el campo **Impuesto sobre las ventas por cobrar** también debe configurarse en la nueva página **Grupos de contabilización del libro mayor**. El motor de contabilidad utilizará la información de este campo para la entrada contable relacionada con los impuestos.   
El comportamiento es consistente para las líneas de gastos contabilizadas con o sin un proyecto.  
