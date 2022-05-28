---
title: Error de coincidencia de divisas
description: Este tema proporciona información de solución de problemas sobre un error de discordancia de moneda que se produce al guardar tipos de registros específicos.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589769"
---
# <a name="currency-mismatch-error"></a>Error de coincidencia de divisas 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Cuando se guarda un proyecto, contrato, oferta o recurso reservable, puede que se reciba un error similar al siguiente: **La divisa de la empresa propietaria no coincide con la divisa de la unidad de contratación. Elija una empresa o unidad de contratación distinta para continuar.** Esto se debe a que existe un desajuste de moneda entre la moneda de la unidad de contratación para el registro y la moneda de la empresa propietaria.


## <a name="resolution"></a>Resolución

Para solucionar este problema, siga estos pasos:
- Verifique la moneda de la unidad contratante para este registro. Puede ver la moneda abriendo el registro de la unidad organizativa y verificando el valor en la pestaña **General** del campo **Divisa**.
- Verifique la moneda de la empresa propietaria. Puede ver la moneda yendo a **Relacionado** > **Libros de contabilidad** en el registro de la empresa. Haga doble clic en el registro del libro mayor asociado con la empresa y verifique el valor en la pestaña **General** en el campo **Moneda contable**.

Si la moneda establecida en la unidad de contratación y el registro del libro mayor no coinciden, ajuste la configuración o seleccione valores diferentes cuando guarde el registro. El sistema requiere que estos registros coincidan para garantizar los flujos correctos de facturación entre empresas. Para obtener más información sobre las configuraciones de empresas vinculadas, consulte [Crear transacciones entre empresas vinculadas](../../project-accounting/create-intercompany-transactions.md).

Si el registro de la empresa no tiene un registro de contabilidad asociado, esto indica que falta una configuración al configurar el entorno. El administrador del sistema debe corregir la configuración. El sistema Administrador debe ir a **Configuraciones de escritura dual** y parar y reiniciar **Mapa de escritura doble de libros mayores** con la sincronización inicial de este mapa y sus requisitos previos. Para más información, vea [Versiones de mapas de doble escritura de Project Operations](../../environment/resource-dual-write-maps.md).
