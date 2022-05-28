---
title: Introducción al reconocimiento de ingresos
description: En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 51c553ecf45452615cbcadce6386f32be427acaa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601453"
---
# <a name="revenue-recognition-overview"></a>Introducción al reconocimiento de ingresos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

En Dynamics 365 Project Operations, los principios de reconocimiento de ingresos varían según el método de facturación seleccionado para un proyecto o parte del proyecto. En este tema se proporciona información acerca de reconocimiento de ingresos en Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transacciones contabilizadas usando el método de facturación de tiempo y material

- El reconocimiento de costes e ingresos están conectados. El coste de transacción y las ventas no facturadas se registran utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md).
- El perfil de costes e ingresos del proyecto determina si las transacciones de ventas no facturadas se registran en la contabilidad general. Si se ha seleccionado **Ingresos acumulados**, el sistema utiliza las cuentas de **Trabajo en proceso - Valor de ventas** y **Ingresos acumulados - Valor de ventas** durante el registro. A continuación, se muestra ejemplo de este método.  

  | Tipo de transacción | Debe/Haber | Importe |
  | --- | --- | --- |
  | Trabajo en proceso - Valor de ventas | Debe | 100 |
  | Trabajo en proceso - Valor de ventas | Haber | 100 |

- Los ingresos se reconocen durante la facturación. El sistema utiliza la cuenta de **Ingresos facturados** durante el registro. A continuación, se muestra ejemplo de este método.  

  | Tipo de transacción | Debe/Haber | Importe |
  | --- | --- | --- |
  | Saldo del cliente | Débito | 120 |
  | Impuestos repercutidos | Crédito | 20 |
  | Ingresos facturados | Crédito | 100 |

- Si se acumularon ingresos cuando se registraron las ventas sin facturar, el sistema revertirá los ingresos acumulados al momento de la facturación.

  | Tipo de transacción | Debe/Haber | Importe |
  | --- | --- | --- |
  | Trabajo en proceso - Valor de ventas | Crédito | 100 |
  | Trabajo en proceso - Valor de ventas | Débito | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transacciones contabilizadas usando el método de facturación de precio fijo

- El reconocimiento de costes e ingresos son independientes. El coste de transacción se registra utilizando el [Diario de integración de Project Operations](../project-accounting/project-operations-integration-journal.md). No se crean transacciones de ventas sin facturar.
- Los ingresos se pueden reconocer durante la facturación si el perfil de costes e ingresos del proyecto tiene el **Principio utilizado para los cálculos de finalización de proyectos** establecido en **Sin trabajo en curso**. Utilice este método solo para proyectos sencillos a corto plazo.
- Los ingresos se pueden reconocer utilizando estimaciones de ingresos a precio fijo, con el método **Contrato completado** o **Reconocimiento de ingresos de porcentaje de finalización**.

## <a name="additional-resources"></a>Recursos adicionales
[Artículo Configurar la contabilidad para proyectos facturables](../project-accounting/configure-accounting-billable-projects.md)

[Proyectos de estimación de ingresos a precio fijo](rev-rec-percentage-completion-method.md)

[Administrar estimaciones de ingresos](rev-rec-completed-contract-method.md)

[Coste para completar métodos](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]