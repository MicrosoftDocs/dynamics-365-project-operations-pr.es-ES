---
title: Gastos de empresas vinculadas
description: Este tema proporciona información sobre cómo se usan los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684255"
---
# <a name="intercompany-expenses"></a>Gastos de empresas vinculadas

Un trabajador contratado por una entidad jurídica de una organización puede trabajar para otra entidad jurídica de la misma organización. Puede utilizar los gastos de empresas vinculadas para asignar los gastos del trabajador a la entidad jurídica para la que se realizó el trabajo. La entidad jurídica que emplea al trabajador se denomina entidad jurídica prestamista. La entidad jurídica por la que el trabajador incurre en gastos se denomina entidad jurídica prestataria. 

Para que un trabajador pueda crear y enviar gastos de empresas vinculadas, hay que habilitar las líneas de gastos de empresas vinculadas. En la entidad jurídica prestamista, en la página **Parámetros de gestión de gastos**, seleccione **Permitir líneas de gastos de empresas vinculadas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Contabilización de impuestos para gastos de empresas vinculadas

[!include [banner](../includes/banner.md)]

Para poder utilizar grupos de impuestos asociados con la entidad jurídica prestamista (origen) en lugar de la entidad jurídica prestataria (destino) en un informe de gastos, hay que habilitar la funcionalidad en la configuración de impuestos sobre las ventas de la contabilidad general. Si el parámetro **Entidad jurídica para registrar impuestos de empresas vinculadas** está establecido en **Origen** y el campo **Aplicar reglas de tributación de impuestos** está establecido en **No**, se utilizará la combinación de impuestos para la entidad jurídica prestamista. Cuando el mismo parámetro se establece en **Destino**, se utilizará la combinación de impuestos para la entidad jurídica prestataria. Para las entidades legales en los Estados Unidos, cuando el parámetro se establece en **Origen**, el campo **Impuesto sobre las ventas por cobrar** también debe configurarse en la nueva página **Grupos de contabilización del libro mayor**. El motor de contabilidad utilizará la información de este campo para la entrada contable relacionada con los impuestos.   
El comportamiento es consistente para las líneas de gastos contabilizadas con o sin un proyecto.  

## <a name="new-expense-expression-builder"></a>Nuevo generador de expresiones de gastos

El nuevo generador de expresiones de gastos resuelve problemas con escenarios de gastos de empresas vinculadas que utilizan proyectos. Esta función garantiza que cuando crea un gasto entre empresas vinculadas, la política de gastos se valida correctamente con el proyecto seleccionado en la línea de gastos y que el informe de gastos se puede enviar correctamente.

Para que la característica generador de expresiones de gastos funcione, debe estar activada. Además, se debe configurar la directiva de gastos que tiene un ID de proyecto.

Si ya ha configurado directivas que validan el ID de proyecto en la línea de gastos, debe retirarlas. Después podrá activar la característica y volver a configurar las directivas.

Para activar esta característica, siga los pasos indicados a continuación.

1. Vaya a **Áreas de trabajo** \> **Administración de características**.
2. En la lista, seleccione **Nuevo generador de expresiones de gastos para resolver problemas con escenarios de gastos de empresas vinculadas que utilizan proyectos**. Luego seleccione **Activar ahora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
