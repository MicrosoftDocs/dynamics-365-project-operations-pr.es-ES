---
title: Novedades o cambios en la versión de actualización 22, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 22, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280599"
---
# <a name="project-service-automation-update-release-22-v3"></a>Versión de actualización de Project Service Automation 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 22. Esta versión tiene un número de compilación V 3.10.33.48 y generalmente está disponible a través de una actualización automática en junio de 2020.

## <a name="update-release-22"></a>Versión de actualización 22

### <a name="bug-fixes"></a>Correcciones de errores



**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- Las **entradas de tiempo** no se agregan automáticamente en la programación de entradas de tiempo después de la importación.
- El selector de fechas de cuadrícula **Entrada de tiempo** no reconoce la configuración regional de un usuario.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- En modo manual, los cambios en los contornos de **Asignación de recursos** no se reconocen al generar **Requerimientos de recursos**.
- Las **solicitudes de recursos** no admiten estados de solicitud personalizados.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Al hacer doble clic en EstimateGridControl no se analizan correctamente los números con formato neerlandés.
- Las horas asignadas no se actualizan correctamente cuando se cambian las asignaciones mediante el complemento de cliente de escritorio de Microsoft Project.
- Las cuadrículas de Seguimiento del proyecto y Estimaciones muestran un código de divisa de ventas incorrecto cuando la divisa del contrato es diferente a la divisa del cliente y la organización está configurada para mostrar códigos de divisa en lugar de símbolos de divisa.
- La fecha de finalización de un miembro del equipo agregará un día si el horario de trabajo es de 24 horas al día.
- En la programación del proyecto, al agregar una categoría de transacción a una tarea no se activa el guardado automático.
- Se muestra el siguiente error al agregar un miembro del equipo a la plantilla de proyecto: "Los requisitos de recursos no se pueden asociar con las plantillas de proyecto". 
- El script de regla de cinta "msdyn.Approval.CanApproveOrReject" muestra un error de tiempo de espera.

**Sales**

Se han solucionado los siguientes problemas:

- El mensaje de error de validación no se muestra cuando se selecciona una lista de precios de coste en la búsqueda de lista de precios en el formulario/entidad "Nueva lista de precios del proyecto de cotización".
- Al cerrar la cotización como ganada no se navega hasta el contrato creado si un BPF adjunto a la cotización se encuentra en la etapa final.
- Al revertir las **Ventas no facturadas**, se vinculan al coste original cuando se recupera una entrada de tiempo.
- Después de seleccionar el botón **Confirmar**, el estado de la factura no cambia a **Confirmado** a menos que se actualice la factura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]