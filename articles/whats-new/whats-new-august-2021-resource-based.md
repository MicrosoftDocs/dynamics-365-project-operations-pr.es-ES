---
title: 'Novedades de agosto de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de agosto de 2021 de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323482"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de agosto de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

   - Project Operations en la versión del entorno 4.13.0.152 de Microsoft Dataverse.
   - Gestión de proyectos y contabilidad en el entorno de la versión 10.0.20 de Dynamics 365 Finance.

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

En esta versión se incluyen las siguientes características:

- **Conjuntos de aprobación**: los conjuntos de aprobación agrupan las solicitudes de aprobación de uso de materiales, gastos o tiempo en subconjuntos más pequeños de operaciones. Esta agrupación permite que las aprobaciones se procesen en un orden específico por proyecto y permite reintentar y secuenciar. La agrupación de las solicitudes de aprobación mejora la confiabilidad y la trazabilidad del proceso de aprobación para grandes volúmenes de aprobaciones. Para obtener más información, consulte [Conjuntos de aprobaciones](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de doble escritura de Project Operations en esta versión. 

Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si la última versión de la asignación no está activada. Puede ver la versión activa de la asignación en la página **Escritura dual** en la columna **Versión**. Active una nueva versión de la asignación seleccionando **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) en la guía de resolución de problemas de escritura dual.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Facturación y precios | 2295625 | El nombre del hito se debe copiar de la programación de la factura al detalle de la línea de la factura. |
| Facturación y precios | 2316323 | El descuento no debe ser editable en una factura proforma en Project Operations para escenarios basados en recursos. |
| Administración de oportunidades | 2338619 | Las reglas comerciales de **Oportunidad** y **Oferta** deben invocarse solo en las páginas. |
| Administración de recursos | 2316523 | El uso de **Enviar petición** desde un requisito de recursos que tiene un rol adjunto no debería mostrar un error. |
| Administración de recursos | 2326885 | La creación de un requisito de recursos a través de un proyecto no debería mostrar un error. |
| Tiempo y gastos | 2335584 | Flujos de tareas en desuso en la entrada de tiempo. |
| Tiempo y gastos | 2336884 | El botón de entrada de tiempo **Copiar semana** debe funcionar para algo más que solo el usuario actual. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestión de proyectos y contabilidad en Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Viajes y gastos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Los importes incorrectos de transacciones de proveedores y transacciones de impuestos sobre las ventas se contabilizan cuando se crea un gasto a partir de una transacción de tarjeta de crédito. |
| Viajes y gastos | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | La liquidación incorrecta son las líneas creadas cuando se genera el diario de pagos. |
| Viajes y gastos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Los importes incorrectos de transacciones de impuestos sobre las ventas se contabilizan cuando se crea un gasto a partir de una transacción de tarjeta de crédito. |
| Viajes y gastos | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Eliminar una línea de gastos puede llevar mucho tiempo. |
| Contabilidad de proyecto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | El sistema no admite la configuración de secuenciación continua de números al registrar una estimación después de aplicar KB 4619395. |
| Contabilidad de proyecto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | El registro de la factura del proveedor puede fallar con el mensaje de error "Las transacciones del asiento no cuadran conforme a 17/05/2021. (divisa de contabilidad: 0,00, divisa de informe: 0,01)" |
