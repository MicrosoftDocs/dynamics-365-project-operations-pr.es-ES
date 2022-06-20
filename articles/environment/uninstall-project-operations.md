---
title: Desinstalar Dynamics 365 Project Operations
description: En este artículo se proporciona información sobre cómo desinstalar Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911985"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Desinstalar Dynamics 365 Project Operations 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Para desinstalar Dynamics 365 Project Operations, debe tener asignado el rol de Administrador.

1. Vaya a **Configuración** > **Soluciones**.

    ![Página Configuración.](./media/uninstall-proj-ops-solutions.png)
  
2. Elimine las soluciones en el orden exacto en que se enumeran en la siguiente tabla. 

    | Paso | Nombre de la solución                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Si no lo encuentra, omita esta solución.                                                            |
    | 2 | ProjectOperations_Anchor                           | Si no lo encuentra, omita esta solución.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Si no lo encuentra, omita esta solución.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Si no lo encuentra, omita esta solución.                                                            |
    | 5 | ProjectService                                     | No hay notas adicionales.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | No hay notas adicionales.                                                                         |
    | 7 | ProjectServiceCore                                 | No hay notas adicionales.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Si no lo encuentra, omita esta solución.                                                            |
    | 9 | FieldServiceCommon                                 | Obligatorio para doble escritura con Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Obligatorio para doble escritura con Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Necesario para Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Necesario para Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Necesario para Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Necesario para Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Necesario para Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Necesario para Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Necesario para Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Si no lo encuentra, omita esta solución.                                                            |
    | 19 | Dynamics365Notes                                   | Si no lo encuentra, omita esta solución.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Si no lo encuentra, omita esta solución.                                                            |
    | 21 | DualWriteCore                                      | Si no lo encuentra, omita esta solución.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Si no lo encuentra, omita esta solución.                                                            |
    | 23 | Dynamics365AssetManagement                         | Si no lo encuentra, omita esta solución.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Si no lo encuentra, omita esta solución.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Si no lo encuentra, omita esta solución.                                                            |
    | 26 | HCMCommon                                          | Si no lo encuentra, omita esta solución.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Si no lo encuentra, omita esta solución.                                                            |
    | 28 | Parte                                              | Si no lo encuentra, omita esta solución.                                                            |
    | 29 | Dynamics365Company                                 | Si no lo encuentra, omita esta solución.                                                            |
    | 30 | CurrencyExchangeRates                              | Si no lo encuentra, omita esta solución.                                                            |
    | 31 | AssetCommon                                        | Si no lo encuentra, omita esta solución.                                                            |
