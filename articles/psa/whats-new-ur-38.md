---
title: Novedades o cambios en la versión de actualización 38, V3, de Project Service Automation
description: Este tema enumera las características y correcciones que están disponibles en Microsoft Dynamics 365 Project Service Automation, versión de actualización 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901497"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novedades o cambios en la versión de actualización 38, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 38, V3. Esta versión tiene un número de compilación de V3.10.59.117 y es de lanzamiento público mediante una actualización automática desde diciembre de 2021.

## <a name="update-release-38"></a>Versión de actualización 38

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**Tiempo y gasto**

- Se produce una excepción cuando la longitud de los registros del conjunto de aprobaciones supera los 100.000 registros.
- Los usuarios no pueden acceder a la cuadrícula **Entrada de tiempo** de la pagina principal **Entrada de tiempo**.
- El cuadro de diálogo **Importación de entrada de tiempo** no muestra ningún texto cuando no se pueden importar elementos.
- Los usuarios pueden crear conjuntos de aprobación donde el campo **Estado objetivo** está configurado en **Desconocido**.

**Administración del proyecto**

- Los contornos no se muestran correctamente en las asignaciones de recursos para UTC (+09: 30) y UTC (+10: 00) cuando comienza el horario de verano.
- El campo **Columna adicional** para estructuras de desglose de trabajo está oculto en algunos lugares.
- El selector de fecha para el control de calendario en la cuadrícula **Tarea de proyecto** no está correctamente localizado para chino.

**Ventas**

- Los valores **Ejecución del contrato** y **Costo real del proyecto** no coinciden cuando los recursos que se pueden reservar que tienen diferentes unidades de contratación y monedas envían entradas de tiempo.
- Un flujo de trabajo personalizado para confirmar automáticamente las facturas falla cuando las facturas se importan como solución administrada. Se muestra el siguiente mensaje: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Mensaje: estado de factura no válido".
- Cuándo se selecciona **Raíz** como la opción de resumen, y el proyecto tiene estimaciones de una combinación de clases de transacciones (por ejemplo, una combinación de estimaciones de tiempo, gastos y materiales), el sistema resume las clases de transacciones como una sola línea de tarifa.
- En escenarios donde se agrega una línea de gastos antes de que una línea de contrato se asocie con un proyecto, el precio correcto no se ingresa como un valor predeterminado en el campo **Actualizar precio**.
- No se permiten cantidades negativas de ventas en las entidades **Proyecto** y **Tarea**.
