---
title: Gastos de empresas vinculadas
description: Este tema proporciona información sobre cómo se usan los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960853"
---
# <a name="intercompany-expenses"></a>Gastos de empresas vinculadas

Un trabajador contratado por una entidad jurídica de una organización puede trabajar para otra entidad jurídica de la misma organización. Puede utilizar los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo. La entidad jurídica que emplea al trabajador se denomina entidad jurídica prestamista. La entidad jurídica por la que el trabajador incurre en gastos se denomina entidad jurídica prestataria. 

Para que un trabajador pueda crear y enviar gastos de empresas vinculadas, hay que habilitar las líneas de gastos de empresas vinculadas. En la entidad jurídica prestamista, en la página **Parámetros de gestión de gastos**, seleccione **Permitir líneas de gastos de empresas vinculadas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impuestos para gastos de empresas vinculadas

[!include [banner](../includes/banner.md)]

Para poder utilizar grupos de impuestos asociados con la entidad jurídica prestamista (origen) en lugar de la entidad jurídica prestataria (destino) en un informe de gastos, hay que habilitar la funcionalidad en la configuración de impuestos sobre las ventas de la contabilidad general. Si el parámetro **Entidad jurídica para registrar impuestos de empresas vinculadas** está establecido en **Origen** y el campo **Aplicar reglas de tributación de impuestos** está establecido en **No**, se utilizará la combinación de impuestos para la entidad jurídica prestamista. Cuando el mismo parámetro se establece en **Destino**, se utilizará la combinación de impuestos para la entidad jurídica prestataria. Para las entidades legales en los Estados Unidos, cuando el parámetro se establece en **Origen**, el campo **Impuesto sobre las ventas por cobrar** también debe configurarse en la nueva página **Grupos de contabilización del libro mayor**. El motor de contabilidad utilizará la información de este campo para la entrada contable relacionada con los impuestos.   
El comportamiento es consistente para las líneas de gastos contabilizadas con o sin un proyecto.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]