---
title: Novedades o cambios en la versión de actualización 20, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones disponibles en la Versión de actualización de Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126774"
---
# <a name="project-service-automation-update-release-20-v3"></a>Versión de actualización de Project Service Automation 20, V3

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 20. Esta versión tiene un número de compilación V 3.10.31.37 y generalmente está disponible a través de una actualización automática en junio de 2020.

## <a name="update-release-20"></a>Versión de actualización 20

### <a name="bug-fixes"></a>Correcciones de errores

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- La importación de miembros del equipo del proyecto con un método de asignación que requiere horas da como resultado un mensaje de error poco claro cuando las horas especificadas son cero.
- Los usuarios reciben un error incorrecto cuando se ha ingresado el número máximo de caracteres en el campo **Descripción** para una tarea de proyecto.
- La página **Descargar complemento Microsoft Dynamics 365 Project Service Automation** redirige a la página de descarga en inglés cuando la configuración de idioma del usuario está establecida en japonés.
- Cuando se produce un error del servidor, la etiqueta de sincronización de la pestaña **Calendario** del formulario **Proyectos** a veces permanece.
- Las actualizaciones de tareas redundantes se envían al servidor cuando se modifica una tarea.

**Sales**

Se han solucionado los siguientes problemas:

- En el formulario **Contrato**, haciendo doble clic en **Crear factura**, se crean dos facturas para un único registro de datos reales.
- En Internet Explorer 11, los usuarios no pueden crear entradas de gastos.
- La reversión de costos y la reversión de ventas reales no facturadas no están vinculadas.
- El botón **Actualizar datos reales** del formulario **Proyecto** no actualiza **Horas reales de la tarea**.
- El complemento **PreValidateProjectTeamMemberCreate** puede crear recursos duplicables genéricos que se pueden reservar cuando el atributo **msdyn_isgenericresourceprojectscoped** se establece en **Falso**.
- **Recalcular** borra los costos imputables de los detalles de la línea de presupuesto basada en el producto y los detalles de la línea del contrato.
- En escenarios específicos, el complemento **PostEstimateLineUpdate** muestra un error de excepción de referencia nula.
- La duración de la fase de tiempo en **Cuadro de análisis de rentabilidad** no coincide con la duración de los costos en el detalle de la línea de presupuesto de precio fijo del presupuesto.
- Los valores de unidad y grupo de unidades no se predeterminan correctamente para categorías de gastos en los formularios **Detalles de línea de contrato** y **Detalles de línea de presupuesto**.
- La lista **Precio de coste de unidad de organización** permite superposiciones en la vigencia de la fecha.
- Los usuarios no pueden cambiar **OrgUnit** cuando el tipo de pedido no está basado en el trabajo porque dará lugar a un error de excepción de referencia nula.
- Al intentar navegar desde el formulario **Detalles de línea de presupuesto**, de vuelta a la pestaña **Presupuesto**, el formulario se actualiza y muestra la pestaña **Resumen**.
