---
title: Tipos de período
description: En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 83cf88bafbc7fc97fba664e278b232c24db53391
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580477"
---
# <a name="period-types"></a>Tipos de período

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Un tipo de período define la frecuencia con la que se estiman los ingresos de un proyecto. En este tema se proporciona información acerca de cómo configurar tipos de período para estimación de ingresos. 

## <a name="create-and-work-with-period-types"></a>Crear y trabajar con tipos de períodos
Para crear y trabajar con tipos de período, complete los siguientes pasos:

1. En su entorno de Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad.** > **Configuración** > **Estimaciones** > **Tipos de periodo**.
2. Seleccione **Nuevo** para crear un nuevo tipo de período. Escriba un nombre y una descripción.
3. En el campo **Frecuencia**, seleccione un valor:

    - Si selecciona **Semana**,**Quincenal**, **Semimensual**, **Mes**, **Día**, **Trimestre** o **Año**, el calendario se utilizará para generar los períodos. 
    - Si selecciona **Período contable**, los períodos contables de la configuración de Contabilidad general se utilizarán para generar períodos.
    - Si selecciona **Sin límite**, puede especificar períodos personalizados.
4. Seleccione el registro de tipo de período y, a continuación, **Generar períodos** para crear períodos para el tipo de período. Según la frecuencia del período que haya seleccionado, es posible que tenga la opción de especificar una fecha de inicio o el número de períodos para generar.
5. Seleccione **Períodos** para revisar periodos generados.



[!INCLUDE[footer-include](../includes/footer-banner.md)]