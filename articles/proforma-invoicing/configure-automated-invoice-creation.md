---
title: Configurar la creación automática de facturas
description: En este tema se proporciona información sobre cómo configurar el sistema para generar facturas automáticamente.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43b75ea823a62acaab708a1ef2fa2467904fdd00
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583422"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar la creación automática de facturas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_


Complete los siguientes pasos para configurar una ejecución automática de facturas en Dynamics 365 Project Operations.

1. Vaya a **Configuración** > **Trabajos por lotes**.
2. Cree un trabajo por lotes y asígnele el nombre **Creación de facturas de Project Operations**. El nombre del trabajo por lotes debe incluir las palabras "creación de facturas".
3. En el campo **Tipo de trabajo**, seleccione **Ninguno**. De forma predeterminada, las opciones **Frecuencia diaria** y **Está activo** están configuradas con el valor **Sí**.
4. Seleccione **Ejecutar flujo de trabajo**. En el cuadro de diálogo **Buscar registro**, aparecerán tres flujos de trabajo:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccione **ProcessRunCaller** y luego elija **Agregar**.
6. En el siguiente cuadro de diálogo, seleccione **Aceptar**. Al flujo de trabajo **Suspensión** le sigue el flujo de trabajo **Proceso**.

  > [!NOTE]
  > También puede seleccionar **ProcessRunner** en el paso 5. A continuación, cuando se selecciona **Aceptar**, el flujo de trabajo **Proceso** va seguido del flujo de trabajo **Reposo**.

Los flujos de trabajo **ProcessRunCaller** y **ProcessRunner** crean facturas. **ProcessRunCaller** llama a **ProcessRunner**. **ProcessRunner** es el flujo de trabajo que crea realmente las facturas. Pasa por todas las líneas de contrato para las que se deben crear facturas y crea las facturas para dichas líneas. Para determinar para qué líneas de contrato deben crearse facturas, el trabajo examina las fechas de ejecución de facturas de las líneas de contrato. Si detecta líneas de contrato que pertenecen a un mismo contrato con la misma fecha de ejecución de factura, las transacciones se combinarán en una factura con dos líneas de factura. Si no hay transacciones para las que crear facturas, el trabajo omitirá la creación de facturas.

Cuando **ProcessRunner** termina de ejecutarse, llama a **ProcessRunCaller**, proporciona la hora de finalización y se cierra. **ProcessRunCaller**, a su vez, inicia un temporizador que se ejecuta durante 24 horas a partir de la hora de finalización especificada. Cuando el temporizador marque el final, **ProcessRunCaller** se cerrará.

El trabajo de proceso por lotes de creación de facturas es periódico. Si este proceso por lotes se ejecuta muchas veces, se crean numerosas instancias del trabajo y se producen errores. Por lo tanto, debe iniciar el proceso por lotes solo una vez y debe reiniciarlo solo si se detiene su ejecución.

> [!NOTE]
> La facturación por lotes solo se ejecuta para las líneas de contrato del proyecto que se configuran mediante programas de facturación. Una línea de contrato con un método de facturación de precio fijo debe tener hitos configurados. Una línea de contrato de proyecto con un método de facturación de tiempo y material necesitará una programación de facturación basada en fecha. Lo mismo se aplica a una línea de contrato basada en proyectos.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]