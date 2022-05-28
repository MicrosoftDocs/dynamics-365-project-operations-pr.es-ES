---
title: Novedades o cambios en la versión de actualización 31, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 31, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 70a8bd381c27c9a3dd3b33c582e5616fad280e95
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586779"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novedades o cambios en la versión de actualización 31, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 31. Esta versión tiene un número de compilación V3.10.52.77 y generalmente está disponible a través de una actualización automática de mayo de 2021.

## <a name="update-release-31"></a>Versión de actualización 31

### <a name="bug-fixes"></a>Correcciones de errores

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Los botones de comando de control de entrada de tiempo en la página **Recurso que se puede reservar** eran confusos.
- Se generó una excepción de referencia nula en **Project.SetTrackingFields** al aprobar una entrada de tiempo.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- **Crear miembro del equipo** no muestra correctamente la configuración de metadatos de configuración de reserva para **Estado confirmado de la reserva predeterminada**.
- Al actualizar de PSA 1.X a 3.X, el proceso de actualización falla en **UpgradeResourceRequirements**.


**Ventas**

Se han solucionado los siguientes problemas:

- Los ingresos reales convierten los importes a la moneda del proyecto en la cuadrícula de seguimiento.
- La moneda predeterminada no está clara al crear líneas de diario, líneas de ofertas y líneas de contrato en escenarios donde la moneda base de una organización difiere de la moneda del proyecto.
- La consulta **Validación del diario pendiente de corrección** no se filtra por proyecto.
- Las ventas restantes se calculan incorrectamente en un proyecto.
- Las ofertas basadas en un contacto fallan cuando se crean sin una lista de precios.
- No se muestra ningún indicador giratorio de procesamiento cuando selecciona **Confirmar factura**.
- No se muestra ningún indicador giratorio de procesamiento cuando selecciona **Crear factura**.
- Cerrar una oferta como perdida no cancela las reservas.







