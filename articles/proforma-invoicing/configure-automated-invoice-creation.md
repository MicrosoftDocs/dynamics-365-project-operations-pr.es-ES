---
title: Configurar la creación automática de facturas
description: En este tema se proporciona información sobre cómo configurar el sistema para generar facturas automáticamente.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085041"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar la creación automática de facturas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Complete los siguientes pasos para configurar una ejecución automática de facturas en Dynamics 365 Project Operations.

1. Vaya a **Configuración** > **Trabajos por lotes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**. El nombre del trabajo por lotes debe incluir las palabras "creación de facturas".
3. En el campo **Tipo de trabajo** , seleccione **Ninguno**. De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registros** , se mostrarán tres flujos de trabajo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y después seleccione **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. El flujo de trabajo **Reposo** va seguido de un flujo de trabajo **Proceso**.

  > [!NOTE]
  > También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar** , el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea realmente las facturas. Pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas. Para determinar las líneas de contrato para las que se deben crear facturas, el trabajo busca fechas de ejecución de facturas para las líneas de contrato. Si hay líneas de contrato que pertenecen a un contrato que tiene la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para crear facturas, el trabajo omite la creación de factura.

Cuando finaliza la ejecución de **ProcessRunner** , se llama al flujo de trabajo **ProcessRunCaller** , que proporciona la hora de finalización y después se cierra. A continuación, **ProcessRunCaller** pone en marcha un temporizador que se ejecuta durante 24 horas desde la hora de finalización especificada. Cuando se agota el tiempo del temporizador, el flujo de trabajo **ProcessRunCaller** se cierra.

El trabajo del proceso por lotes para la creación de facturas es un trabajo recurrente. Si este proceso por lotes se ejecuta muchas veces, se crean varias instancias del trabajo y se generan errores. Por lo tanto, debe iniciar el proceso por lotes solo una vez y debe reiniciarlo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha. Lo mismo se aplica a una línea de contrato basada en proyectos.     
