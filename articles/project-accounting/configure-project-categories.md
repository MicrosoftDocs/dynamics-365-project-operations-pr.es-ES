---
title: Configurar categorías de proyectos
description: En este tema se proporciona información sobre la configuración de categorías de proyecto.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997132"
---
# <a name="configure-project-categories"></a>Configurar categorías de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations ofrece capacidades sólidas para categorizar ingresos y gastos en proyectos. Las categorías brindan la capacidad de informar y analizar las transacciones del proyecto y de impulsar el registro en la contabilidad general.

El siguiente diagrama ilustra la correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos. 

Las categorías de transacciones son la agrupación básica para las transacciones de proyectos. Dentro de dicha agrupación hay un conjunto de categorías compartidas que se pueden compartir entre aplicaciones y módulos. Si profundizamos aún más en los detalles, las categorías de proyectos son el nivel de categorías más preciso. Las categorías de proyectos son específicas de la entidad jurídica, el módulo y la aplicación.

![Correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos.](media/project-categories.png)

## <a name="transaction-categories"></a>Categorías de transacciones

Las categorías de transacciones representan la agrupación básica para las transacciones de proyecto y no son específicas de la empresa ni del tipo de transacción. Por ejemplo, Contoso Robotics usa las categorías Diseño, Viajes, Instalación y Transacción de servicio para agrupar transacciones del proyecto.

Las categorías de transacciones se definen en el módulo Operaciones de proyecto. 
1. Vaya a **Configuración** \> **Categorías de transacciones** para abrir el formulario. 
2. Cree una nueva categoría de transacción seleccionando **Nueva** o seleccionando **Importar desde Excel**.

## <a name="shared-categories"></a>Categorías compartidas

Dynamics 365 utiliza el concepto de categorías compartidas para categorizar los gastos en diferentes aplicaciones, como Dynamics 365 Finance, Dynamics 365 Supply Chain y Dynamics 365 Project Operations. Para cada categoría de transacción creada, Project Operations crea automáticamente cuatro categorías compartidas relacionadas: Horas, Gastos, Tarifas y Artículo. Puede revisar y ajustar las categorías compartidas yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías compartidas**.

## <a name="project-categories"></a>Categorías de proyecto

Las categorías de proyectos representan el nivel más granular de configuración de categorías y deben configurarse por separado, y para cada empresa, por medio de un contable de proyectos.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías de proyectos**.
2. Seleccione **Nuevo**.
3. Seleccione el **Id. de categoria** de la categoría compartida que creó en la sección anterior. Project Operations permite usar solo las categorías compartidas que están asociadas a las categorías de transacciones.
4. Seleccione un grupo de categorías.

## <a name="category-groups"></a>Grupos de categorías

Los grupos de categorías se utilizan para compartir propiedades, principalmente registrar perfiles, entre categorías de proyectos relacionados. Debe haber al menos un grupo de categorías por cada tipo de transacción y a cada categoría de proyecto se le asigna un grupo.

Las especificaciones de contabilización de las operaciones de proyecto se definen mediante las reglas del perfil de costes e ingresos del proyecto, las categorías de proyectos y los grupos de categorías. Puede configurar grupos de categorías yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Grupos de categorías**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]