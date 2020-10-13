---
title: Configurar categorías de proyectos
description: En este tema se proporciona información sobre la configuración de categorías de proyecto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895987"
---
# <a name="configure-project-categories"></a>Configurar categorías de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Project Operations ofrece capacidades sólidas para categorizar ingresos y gastos en proyectos. Las categorías brindan la capacidad de informar y analizar las transacciones del proyecto e impulsar la contabilización en el libro mayor.

El siguiente diagrama ilustra la correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos. 

Las categorías de transacciones son la agrupación básica para las transacciones de proyectos. Dentro de esa agrupación, hay un conjunto de categorías compartidas que se pueden compartir entre aplicaciones y módulos. Entrando aún más en los detalles, las categorías de proyectos son el nivel más granular de las categorías. Las categorías de proyectos son específicas de la entidad jurídica, el módulo y la aplicación.

![Correlación entre categorías de transacciones, categorías compartidas y categorías de proyectos](media/project-categories.png)

## <a name="transaction-categories"></a>Categorías de transacciones

Las categorías de transacciones representan la agrupación básica para las transacciones de proyecto y no son específicas de la empresa ni del tipo de transacción. Por ejemplo, Contoso Robotics usa las categorías Diseño, Viaje, Instalación y Transacción de servicio para agrupar transacciones de proyecto.

Las categorías de transacciones se definen en el módulo Operaciones de proyecto. 
1. Vaya a **Configuración** \> **Categorías de transacciones** para abrir el formulario. 
2. Cree una nueva categoría de transacción seleccionando **Nueva** o seleccionando **Importar desde Excel**.

## <a name="shared-categories"></a>Categorías compartidas

Dynamics 365 utiliza el concepto de categorías compartidas para categorizar los gastos en diferentes aplicaciones, como Dynamics 365 Finance, Dynamics 365 Supply Chain y Dynamics 365 Project Operations. Para cada categoría de transacción creada, Project Operations crea automáticamente cuatro categorías compartidas relacionadas: Horas, Gastos, Tarifas y Artículo. Puede revisar y ajustar las categorías compartidas yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías compartidas**.

## <a name="project-categories"></a>Categorías de proyecto

Las categorías de proyectos representan el nivel más granular de configuración de categorías y deben configurarse por separado, y para cada empresa, por medio de un contable de proyectos.

1. Vaya a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Categorías de proyectos**.
2. Seleccione **Nuevo**.
3. Seleccione el **Id. de categoria** de la categoría compartida que creó en la sección anterior. Las operaciones de proyecto permiten usar solo las categorías compartidas que están asociadas con las categorías de transacciones.
4. Seleccione un grupo de categorías.

## <a name="category-groups"></a>Grupos de categorías

Los grupos de categorías se utilizan para compartir propiedades, principalmente perfiles de registro, entre categorías de proyectos relacionadas. Debe haber al menos un grupo de categorías para cada tipo de transacción y a cada categoría de proyecto se le asigna un grupo.

Las especificaciones de contabilización de las operaciones de proyecto se definen mediante las reglas del perfil de costes e ingresos del proyecto, las categorías de proyectos y los grupos de categorías. Puede configurar grupos de categorías yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Categorías** \> **Grupos de categorías**.
