---
title: Información general de gastos
description: Este tema proporciona información sobre la funcionalidad Gastos en Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967387"
---
# <a name="expense-home-page"></a>Página principal de gasto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


Dynamics 365 Project Operations admite la capacidad de procesar gastos. El procesamiento de gastos se produce con o sin proyectos mediante el uso de un flujo de trabajo personalizable de directivas, categorías de transacciones y aprobaciones.

En Project Operations, hay dos modelos de implementación admitidos para Gastos: 

- **Completo**: la implementación completa está disponible para **Operaciones de proyecto para escenarios basados en recursos/no en existencias** u **Operaciones de proyecto para escenarios basados en pedidos de producción**.
- **Básico**: la implementación básica está disponible para **Operaciones de proyecto para escenarios basados en recursos/no en existencias** e **Implementación simplificada: facturación de ofertas a proforma**.

## <a name="full"></a>Completo 
La implementación de gastos completos proporciona una aplicación de directivas completa que incluye la capacidad de crear directivas, como:

  - Límites de Categoría de gastos
  - Viaje
  - Dietas
  - Importaciones de tarjeta de crédito
  - Reconocimiento óptico de caracteres de recibos

## <a name="basic"></a>Básica 
El escenario de implementación de gastos básicos solo le permite registrar los gastos básicos frente a un proyecto. 

Para más información, consulte [Entrada de gastos (simplificada)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Determinar la implementación de gastos
Para determinar si está ejecutando la implementación de la administración de gastos básicos, verifique que la dirección URL termine por **.crm.dynamics.com**. 
