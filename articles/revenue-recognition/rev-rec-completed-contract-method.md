---
title: Administrar estimaciones de ingresos
description: En este tema se proporciona información acerca de cómo trabajar con estimaciones de ingresos para proyectos.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531561"
---
# <a name="manage-revenue-estimates"></a>Administrar estimaciones de ingresos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Puede crear, calcular, registrar, revertir o eliminar estimaciones de ingresos. Puede hacerlo manualmente o mediante un proceso periódico. En este tema se proporciona información acerca de cómo trabajar con estimaciones de ingresos para proyectos.

### <a name="manage-revenue-estimates-manually"></a>Administrar estimaciones de ingresos manualmente

En el proyecto de estimación de ingresos a precio fijo o la página **Consulta de estimación** (**Gestión de proyectos y contabilidad** > **Informes y consultas** > **Estimaciones de consultas e informes**), seleccione **Estimaciones**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Administrar estimaciones de ingresos mediante un proceso periódico

Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones** y seleccione el proceso correspondiente.

## <a name="create-a-revenue-estimate"></a>Crear una estimación de ingresos

Para crear una estimación de ingresos, complete los siguientes pasos. 

1. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones**.
2. Seleccione **Nuevo**. En la página **Creación de estimaciones**, seleccione los siguientes parámetros:

   - **Código de período**: este código determina la frecuencia con la que se registran las estimaciones.
   - **Fecha estimada**: la fecha en que se procesa la estimación.
   - **Continuo**: seleccione esta casilla para crear estimaciones solo si se registraron estimaciones en el período anterior o si la estimación es la primera estimación que se ha creado. Si no se selecciona, se crean estimaciones incluso si las estimaciones no se registraron en el período anterior.
   - **Coste para completar el método**: defina cómo estimar el trabajo restante del proyecto. Para más información, consulte [Coste para completar métodos](cost-complete-methods.md).
   - **Método de finalización**: seleccione un método de finalización entre las siguientes opciones:
     - **Automático**: el porcentaje de finalización se calcula automáticamente y se basa en las líneas de coste incluidas en el cálculo. La plantilla de coste define las líneas de costes que se incluyen.
     - **Manual**: el porcentaje de finalización es igual al porcentaje de finalización de la última estimación. Una vez creado la estimación, puede cambiar el **Cálculo manual** en la página **Estimaciones**.
     - **De la plantilla de coste**: una combinación de los métodos automático y manual. Esta opción se establece automática o manualmente, según el valor predeterminado de la plantilla de coste.
   - **Modelo de previsión**: seleccione un modelo de previsión para la estimación.
   - **Imprimir lista de estimaciones**: cree y muestre una lista de estimaciones. La lista contiene el estado de la función actual. Puede imprimir cualquier advertencia sobre la estimación en el informe. Las siguientes condiciones hacen que aparezcan advertencias en la lista de estimaciones:
     - Un porcentaje de finalización de más del 100 por ciento.
     - Un porcentaje de finalización menor del cero por ciento.
     - Un importe negativo en la columna **Para completar**.
     - Una estimación sin importe de contrato correspondiente.
     - Una estimación sin estimación de coste adjunta.
   - **Mostrar registro de información**: seleccione esta opción para recibir un mensaje que contiene información acerca de los proyectos de estimaciones que se procesaron cuando se ejecutó el trabajo.


## <a name="post-wip-or-accruals"></a>Registrar trabajos en curso o acumulaciones

Después de evaluar las estimaciones, se mantienen, disminuyen o aumentan. A continuación, puede registrar el trabajo en curso cuando trabaje con el principio de evaluación **Contrato completado**, o registre las acumulaciones cuando trabaje con el principio de evaluación **Porcentaje completado**.
  
El estado del período de estimación cambia de **Creado** a **Registrado**.

## <a name="reverse-wip-or-accruals"></a>Trabajo en curso inverso o acumulaciones

Utilice la opción de inversión para acreditar trabajo en curso o acumulaciones ya registradas, y luego cree estimaciones para el período.

> [!NOTE]
> Para revertir un período que se encuentra entre otros, invierta los períodos estimados necesarios y luego vuelva a registrarlos. Como todos los períodos posteriores dependen de las estimaciones del período anterior, no omita ningún período.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminar el proyecto de estimación y finalizar el proyecto

El paso final en el proceso de estimación es eliminar el proyecto de estimación y finalizar el proyecto de precio fijo cuando el porcentaje de finalización alcanza el 100 por ciento.

Lo siguiente se produce al ejecutar la eliminación:

- Para un proyecto de precio fijo con un contrato completado, los valores de trabajo en curso se borran de las cuentas de saldo y se registran en las cuentas de pérdidas y ganancias.
- Para un proyecto de precio fijo con un porcentaje completado, las acumulaciones se eliminan de las cuentas de pérdidas y ganancias.

La estimación cambia el estado a **Eliminado**.

> [!NOTE]
> En casos especiales, el porcentaje puede extenderse más allá del 100 por cien. Cuando esto suceda, reduzca el porcentaje de finalización con **Establecer coste para completar en método cero** para llegar al 100 por cien.

## <a name="reverse-elimination"></a>Invertir eliminación

1. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Estimaciones** > **Invertir eliminación**. 
2. En el panel de acciones, en la pestaña **Proceso**, en el grupo **Mantener**, seleccione **Estimación**. 
3. Seleccione **Invertir eliminación**.

Utilice esta página para invertir todas las eliminaciones con una fecha estimada especificada y con un estado estimado de **Eliminado**. El estado de la transacción cambia después de seleccionar los campos correspondientes.

Esto también cambia automáticamente el estado del proyecto a **En curso** si la fase del proyecto está establecida como finalizada. El estado de estimación del período del proyecto vuelve a cambiar a **Registrado**.
