---
title: Novedades o cambios en la versión de actualización 36, V3, de Project Service Automation
description: Este tema enumera las características y correcciones que están disponibles en Microsoft Dynamics 365 Project Service Automation, versión de actualización 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606824"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novedades o cambios en la versión de actualización 36, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Microsoft Dynamics 365 Project Service Automation. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 e instale la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation, versión de actualización 36, V3. Esta versión tiene un número de compilación de V3.10.57.152 y está disponible con carácter general a través de una actualización automática en octubre de 2021.

## <a name="update-release-36"></a>Versión de actualización 36

### <a name="bug-fixes"></a>Corrección de errores

Se han solucionado los siguientes problemas.

**General**
- El nombre del campo **Plantilla predeterminada de horas de trabajo** se traduce incorrectamente en la página **Parámetros del proyecto**.
- Los complementos asíncronicos no gestionan correctamente las excepciones relacionadas con **SharedVariableService**.

**Tiempo y gasto**
- Cuando faltan líneas del diario o el usuario no tiene los privilegios correctos para leer las líneas del diario, se produce un error incorrecto cuando se cancelan las aprobaciones del proyecto.
- Los usuarios no pueden cancelar una aprobación cuando una entrada de gasto o tiempo tiene más de una aprobación de proyecto asociada.
- **Ausencia** y **Vacaciones** están traducidos incorrectamente para el idioma chino en una búsqueda en la página de creación rápida **Entrada de tiempo**.

**Administración de recursos**
- El usuario no puede buscar recursos en el **Asistente de programación** cuando el modo de vista se establece en **Día**, **Semana** o **Mes**.
- Se permite incorrectamente que recursos genéricos tengan nombres de posición vacíos. 
- Cerrar un contrato como perdido no cancela futuras reservas.

**Ventas**
- Cuando un entorno tiene un gran volumen de productos, el rendimiento se degrada en la cuadrícula **Estimación de materiales**.
- Al crear un proyecto a partir de una plantilla, la moneda del proyecto no es de manera predeterminada la unidad de contratación del Jefe de proyecto correspondiente.
- Los importes reales no siempre coinciden con lo que se refleja en el proyecto debido, o los importes se vuelven negativos en escenarios de recuperación específicos.
- Se produce un error cuando asocia un proyecto creado a partir de una plantilla de proyecto a una línea de contratación.
- Los usuarios pueden eliminar una línea de contratación con los hitos, **Listo para facturar** y **Factura creada**. Esto no debería permitirse.
- Cuando se importan estimaciones desde un proyecto, la imputabilidad de detalle de línea de oferta se establece incorrectamente cuando la facturación basada en tareas está habilitada para la línea de oferta.
- Cuando agrega un hito de facturación de precio fijo, el hito no se refleja en la subcuadrícula de hitos hasta que se actualiza la página.
- Se genera una excepción de referencia nula cuando crea un contrato de proyecto con un nombre de oferta que es nulo.
- Las tareas del modo manual en las que la divisa del proyecto es diferente de la divisa del recurso dan como resultado estimaciones de precios incorrectas.
- Los usuarios no pueden recuperar una transacción que haya sido corregida con éxito mediante una factura correctiva.
- Las categorías de transacciones desactivadas aparecen en la cuadrícula **Estimaciones de gastos**.



