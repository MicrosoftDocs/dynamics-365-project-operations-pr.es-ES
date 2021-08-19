---
title: Configurar la integración de Project Operations por entidad jurídica
description: Este tema proporciona información sobre cómo configurar la integración entidad jurídica en Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999427"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar la integración de Project Operations por entidad jurídica 

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema lo guía a través de los pasos necesarios para configurar Dynamics 365 Project Operations por entidad legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Habilitar características clave en Dynamics 365 Finance

Complete los siguientes pasos para habilitar las funciones necesarias.

1. En Dynamics 365 Finance, vaya al espacio de trabajo **Administración de funciones**.
2. En **Lista de características**, busque y habilite las siguientes funciones:
  
    - **Habilitar varias líneas de contrato para un proyecto**
    - **Habilitar Project Operations en Dynamics 365 Customer Engagement**

> [!NOTE]
> Si no ve **Características clave** en la lista, verifique que su versión de Finance cumpla con el requisito de versión mínima (versión de la aplicación 10.0.13 con todas las actualizaciones de calidad aplicadas o superior). Seleccione **Buscar actualizaciones** para actualizar la lista de funciones.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir el escenario de implementación de Project Operations para una entidad jurídica

Puede habilitar Project Operations en Dynamics 365 Customer Engagement a nivel de entidad legal. Puede tener una entidad legal usando Project Operations en Dynamics 365 Customer Engagement para escenarios basados en recursos / no almacenados. En el mismo entorno, puede tener otra entidad jurídica que utilice Project Operations para escenarios de pedidos de existencias / producción.

1. En Dynamics 365 Finance, vaya a **Gestión y contabilidad de proyectos** > **Configuración** > **Parámetros de gestión de proyectos y contabilidad**.
2. En la lista de entidades legales disponibles, seleccione las entidades donde se encuentran múltiples líneas de contrato y las funciones de Project Operations en Dynamics 365 Customer Engagement estarán habilitadas. Deje sin seleccionar las entidades legales que utilizarán Project Operations para escenarios de órdenes de producción / almacenadas.

> [!NOTE]
> Se puede seleccionar una entidad legal solo si no tiene ningún proyecto existente.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar Parámetros de gestión de proyectos y contabilidad

Cada entidad legal que usa Project Operations en Dynamics 365 Customer Engagement necesita un conjunto de parámetros predeterminados. Estos parámetros se configuran en la pestaña **Project Operations** en la página **Parámetros contables y de gestión de proyectos**. Los parámetros son los siguientes:

  - **Valores predeterminados del tipo de facturación**: Project Operations utiliza un conjunto fijo de valores predeterminados de tipo de facturación que deben asignarse a las propiedades de línea Finance. Cree un registro para cada tipo de facturación: **No especificado**, **Facturable**, **No facturable**, **Complementario** y **No disponible**.
  - **Valores predeterminados de categoría de proyecto**: seleccione las categorías de proyecto predeterminadas que se utilizarán para cada tipo de transacción. Estos valores predeterminados se utilizarán en el **Diario de integración de Project Operations** y en estimaciones donde no se especifica ninguna categoría de transacción para el proyecto real.
  - **Pronósticos**: seleccione el modelo de pronóstico que se utilizará para las estimaciones de tiempo y gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]