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
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132399"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurar la contabilidad para proyectos internos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Los proyectos internos permiten a las empresas realizar un seguimiento de los costos relacionados con las actividades que no se facturan a un cliente. Ejemplos de proyectos internos incluyen:

- Desarrollar un producto, como una aplicación móvil, y seguir el coste asociado con el desarrollo.
- Gestionar el tiempo y los gastos de preventa. Este proyecto interno de preventa se puede convertir más tarde en un proyecto facturable si se gana la oferta.

Cualquier proyecto no asociado con un contrato en Dynamics 365 Project Operations se trata como interno. Los perfiles de costes e ingresos del proyecto no se usan para determinar las reglas contables del proyecto. El coste interno del proyecto siempre se registra utilizando principios de pérdidas y ganancias. Las cuentas contables para contabilizaciones se definen en la página **Configuración de libro contable**.

- Las transacciones de tiempo se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Asignación de nómina**.
- Las transacciones de gastos se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Cuenta de contrapartida para gastos**.

Una vez que las transacciones se registran en el proyecto, si el proyecto está asociado con un contrato de proyecto, el sistema revierte todas las transacciones acumuladas y crea nuevas transacciones facturables. Las transacciones facturables siguen las reglas de contabilidad definidas en el respectivo perfil de costos e ingresos del Proyecto.


