---
title: Configurar la contabilidad para proyectos internos
description: Este artículo proporciona un enlace a información sobre cómo configurar prácticas contables para proeyctos internos en Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919483"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar la contabilidad para proyectos internos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los proyectos internos permiten a las empresas realizar un seguimiento de los costos relacionados con las actividades que no se facturan a un cliente. Entre los ejemplos de proyectos internos se incluyen:

- Desarrollo de un producto, como una aplicación móvil y seguimiento del coste asociado con el desarrollo.
- Gestión del tiempo y los gastos de preventa. Este proyecto interno de preventa se puede convertir más tarde en un proyecto facturable si se gana la oferta.

Cualquier proyecto no asociado con un contrato en Dynamics 365 Project Operations se procesa como interno. Los perfiles de costes e ingresos del proyecto no se usan para determinar las reglas contables del proyecto. El coste interno del proyecto siempre se registra con principios de pérdidas y ganancias. Las cuentas contables para los registros se definen en la página **Configuración de registro**.

- Las transacciones de tiempo se registran cargando en la cuenta de **Coste** y abonando en la cuenta **Asignación de nóminas**.
- Las transacciones de gastos se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Cuenta de contrapartida para gastos**.
- Las transacciones de elementos se registran cargando en la cuenta **Coste** y abonando en la cuenta **Coste - Elemento**.

Una vez que las transacciones se registran en el proyecto, si el proyecto está asociado a un contrato de proyecto, el sistema revierte todas las transacciones acumuladas y crea nuevas transacciones facturables. Las transacciones facturables siguen las reglas de contabilidad que se definen en el perfil Costes e ingresos del proyecto respectivo.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
