---
title: Configurar la contabilidad para proyectos internos
description: Este tema proporciona información sobre cómo configurar prácticas de contabilidad para proyectos internos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857999"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar la contabilidad para proyectos internos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los proyectos internos permiten a las empresas realizar un seguimiento de los costos relacionados con las actividades que no se facturan a un cliente. Ejemplos de proyectos internos incluyen:

- Desarrollar un producto, como una aplicación móvil, y seguir el coste asociado con el desarrollo.
- Gestionar el tiempo y los gastos de preventa. Este proyecto interno de preventa se puede convertir más tarde en un proyecto facturable si se gana la oferta.

Cualquier proyecto no asociado con un contrato en Dynamics 365 Project Operations se procesa como interno. Los perfiles de costes e ingresos del proyecto no se usan para determinar las reglas contables del proyecto. El coste interno del proyecto siempre se registra utilizando principios de pérdidas y ganancias. Las cuentas contables para contabilizaciones se definen en la página **Configuración de libro contable**.

- Las transacciones de tiempo se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Asignación de nómina**.
- Las transacciones de gastos se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Cuenta de contrapartida para gastos**.
- Las transacciones de elementos se registran cargando en la cuenta **Coste** y abonando en la cuenta **Coste - Elemento**.

Una vez que las transacciones se registran en el proyecto, si el proyecto está asociado a un contrato de proyecto, el sistema revierte todas las transacciones acumuladas y crea nuevas transacciones facturables. Las transacciones facturables siguen las reglas de contabilidad definidas en el respectivo perfil de costos e ingresos del Proyecto.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
