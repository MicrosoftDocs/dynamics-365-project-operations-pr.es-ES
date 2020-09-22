---
title: Creación de entrada de tiempo
description: En este tema se proporciona información sobre cómo crear entradas de tiempo.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756048"
---
# <a name="create-time-entries"></a>Creación de entrada de tiempo

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En versiones anteriores de Dynamics 365 Project Service Automation, las entradas de tiempo se introducían semanalmente. En la versión 3 de Project Service Automation, las entradas de tiempo se introducen diariamente. Sin embargo, después de que se hayan creado algunas entradas de tiempo, puede crearlas o copiarlas de forma masiva.

## <a name="create-a-time-entry"></a>Creación de una entrada de tiempo

Siga estos pasos para crear una entrada de tiempo.

1. En la página **Entradas de tiempo**, seleccione **Nuevo**.
2. En el cuadro de diálogo **Creación rápida: entrada de tiempo**, escriba la duración de la entrada de tiempo en minutos, horas o días. La duración se debe especificar en el siguiente formato: *x* minutos, *x* horas o *x* días. Las horas y los días también se pueden introducir como valores decimales, como *x,x* horas o *x,x* días.
3. Seleccione el tipo de entrada de tiempo y el proyecto para el que está introduciendo la entrada de tiempo.
4. En el campo **Tarea de proyecto**, busque la tarea para esta entrada de tiempo.

    > [!NOTE]
    > Si está creando una entrada de tiempo para una tarea no asignada a un usuario en el campo **Tarea de proyecto**, seleccione el botón **Buscar**, seleccione **Cambiar vista** y, a continuación, seleccione **Todas las tareas de proyecto activas** para ver todas las tareas.

5. Introduzca una descripción, si se requiere una descripción, y, a continuación, seleccione **Guardar y cerrar**.

Después de crear y guardar la entrada de tiempo, puede editarla en la cuadrícula de entrada de tiempo. La cuadrícula de entrada de tiempo admite dos formatos:

- Puede introducir entradas de tiempo en formato **hh:mm**. Este formato se convierte a horas y fracciones.
- Puede introducir horas y fracciones directamente.

Tenga en cuenta que las fracciones de una hora no son minutos. Por lo tanto, 1,5 horas representan 1 hora y 30 minutos. La misma regla se aplica a las fracciones de un día. Un día son 24 horas, y 0,5 días representan 12 horas.

## <a name="bulk-create-time-entries"></a>Creación de entrada de tiempo de forma masiva

Después de que se hayan creado algunas entradas de tiempo, puede copiarlas para crear entradas de tiempo adicionales de forma masiva.

1. En la página **Entradas de tiempo**, seleccione **Copiar semana**.
2. En el grupo de campos **Desde el período**, en los campos **Fecha de inicio** y **Fecha de finalización**, defina el rango de fechas desde el que copiar las entradas de tiempo.
3. En el grupo de campos **Hasta el período**, en el campo **Fecha de inicio**, especifique la fecha para la que crear entradas de tiempo.
4. Seleccione **Copiar** para crear una copia de las entradas de tiempo que corresponden al día de la semana que se especifica en el grupo de campos **Hasta el período**. Por ejemplo, la entrada de tiempo para el lunes de la semana pasada se copia al lunes de la semana que se especifica en el grupo de campos **Hasta el período**.

## <a name="import-data-for-time-entries"></a>Importación de datos para entradas de tiempo

Puede importar datos de reservas y asignaciones de proyectos. Cuando importe datos, puede especificar el rango de fechas de las reservas para importar y, a continuación, seleccionar explícitamente las reservas que se deben crear como entradas de hora de **Borrador**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Capacidades de agrupación, ordenación, búsqueda y filtrado

Puede agrupar y filtrar las entradas de tiempo por las dimensiones que se especifican en las columnas. En el campo **Agrupar por**, seleccione la dimensión que se usará para filtrar las entradas de tiempo. También puede ordenar los registros de entrada de tiempo en orden ascendente o descendente mediante la flecha de ordenación en los encabezados de columna. Además, puede mostrar u ocultar entradas seleccionando el botón **Filtrar** en los encabezados de las columnas y, a continuación, en el cuadro **Buscar** introduciendo el texto que se debe usar para buscar entradas de tiempo por nombre de proyecto, tarea de proyecto, entrada de tiempo o recurso.
