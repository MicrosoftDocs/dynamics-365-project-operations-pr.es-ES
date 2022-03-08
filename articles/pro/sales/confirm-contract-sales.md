---
title: Conformar un contrato de proyecto
description: Este tema proporciona información sobre confirmar un contrato en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085268"
---
# <a name="confirm-a-project-contract"></a>Conformar un contrato de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Un contrato de proyecto en Dynamics 365 Project Operations puede estar activo con una razón de **Confirmado**, o cerrado con razón de **Perdido**. Cuando confirma un contrato de proyecto, el estado se actualiza desde **Borrador** a **Activo** y la razón para el estado es **Confirmado**. Un contrato activo o cerrado no se puede editar ni volver a abrir. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impacto financiero de confirmar un contrato de proyecto

Una vez que un contrato de proyecto se confirma, la aplicación recalcula los costos al revertir los costos reales más antiguos y a crear nuevos costos reales. Los nuevos costes reales se procesarán según el método de facturación de la línea de contrato del proyecto asociado. Si los datos reales de costes hacen referencia a una línea de contrato de tiempo y material, la aplicación vuelve a crear automáticamente los datos reales de ventas no facturados correspondientes. Si los costos reales hacen referencia a una línea de contrato de precio fijo, la aplicación deja de procesar los costos reales.

Los límites que no deben excederse, la configuración de la valoración y el precio y el coste de los datos reales se evalúan y luego se actualizan como parte del proceso de confirmaciones.

## <a name="close-a-project-contract-as-lost"></a>Cerrar un contrato de proyecto como perdido

Cuando cierra un contrato de proyecto como perdido, el estado del contrato se actualiza a **Cerrado** y la razón para el estado es **Perdido**. El contrato del proyecto pasa a ser de solo lectura. Se proporciona un cuadro de diálogo de confirmación antes de que se completen los cambios porque no puede volver a abrir un contrato de proyecto cerrado.

Si el contrato del proyecto que se cierra como perdido hace referencia a un proyecto en sus líneas, ese proyecto también se marca como cerrado. Se cancelan todas las reservas de recursos a partir de ese día. Los datos reales de ventas no facturados en el contrato del proyecto que aún no estén en una factura se revertirán.

> [!NOTE]
> En Dynamics 365 Project Operations, cerrar un contrato de proyecto como perdido no afectará el estado de la oportunidad asociada. La oportunidad permanecerá abierta y deberá cerrarse manualmente.
