---
title: Novedades o cambios en la versión de actualización 21, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 21, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002348"
---
# <a name="project-service-automation-update-release-21-v3"></a>Versión de actualización de Project Service Automation 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 21. Esta versión tiene un número de compilación V 3.10.32.50 y generalmente está disponible a través de una actualización automática en junio de 2020.

## <a name="update-release-21"></a>Versión de actualización 21

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Al hospedar el **Control de cuadrícula de entrada de tiempo** en Paneles, la cuadrícula no utiliza todo el ancho del contenedor de la cuadrícula del panel.
- Para zonas horarias específicas, el control de cuadrícula **Entrada de tiempo** no muestra registros.
- Las entradas de tiempo posteriores a las 9:00 p. m. aparecen en el día incorrecto.
- Los usuarios no pueden enviar gastos si la categoría de gastos **Se requiere recibo de gastos** no tiene ningún valor.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- Las reservas inactivas se muestran en la vista **Conciliación**.
- Falta la validación del cumplimiento de recursos genéricos para garantizar que exista un estado de reserva válido.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Las cuadrículas del formulario **Proyecto** (**Asignación de recursos**, **Tarea**, la vista **Conciliación**, **Estimaciones de gastos**) permanecen editables incluso cuando un proyecto no está activo.
- Los clientes duplicados no se pueden fusionar con los clientes que están vinculados a contratos de proyecto confirmados.
- Cuando se agrega un recurso que no tiene un calendario válido, el sistema no devuelve un mensaje de error descriptivo.
- El botón **Agregar tarea** en la cuadrícula de tareas está habilitado cuando el proyecto está vinculado al **complemento de Microsoft Project**.
- El esfuerzo crece de manera incontrolable cuando se asigna una tarea con una categoría a un recurso con un rol para el que hay un precio de coste definido.

**Sales**

Se han realizado las siguientes mejoras:

- **Frecuencia de la factura** e **Inicio de facturación** se han trasladado a la pestaña **Programación de facturas**.

Se han solucionado los siguientes problemas:

- **Precio de venta total** es cero (0) para **Categoría** aunque el **Rol** tenga un precio de venta total que no sea cero.
- Los clientes no pueden cambiar el valor del campo **Estado de la factura** a **Listo para facturación** cuando otro proceso personalizado está actualizando un campo adicional.
- El botón **Actualizar líneas de factura** puede crear varias líneas duplicadas si se selecciona repetidamente.
- El botón **Actualizar precios** no funciona en la subcuadrícula **Precios de roles** en el formulario **Vista rápida**.
- La lógica **Resolución de lista de precios de venta** maneja incorrectamente las zonas horarias, lo que resulta en una selección incorrecta de listas de precios.
- El **Coste real total** de un proyecto puede quedar fuera por un importe fraccionario después de que se aprueba una sola entrada de tiempo.
- La lógica de **Resolución de precios** no proporciona un mensaje de error descriptivo si el **Precio de rol recuperado** no tiene valores en los campos **Unidad principal** y **Precio en unidad principal**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]