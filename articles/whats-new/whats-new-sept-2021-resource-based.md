---
title: 'Novedades de septiembre de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de septiembre de 2021 de la implementación de Project Operations para escenarios basados en recursos/no mantenidos en existencias.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582915"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novedades de septiembre de 2021: Project Operations para escenarios basados en recursos/no mantenidos en existencias

*Se aplica a: Project Operations para escenarios basados en recursos/no mantenidos en existencias*

Este tema se aplica a los siguientes componentes y versiones de Dynamics 365 Project Operations:

   - Project Operations en la versión del entorno 4.14.0.99 de Microsoft Dataverse.
   - Gestión de proyectos y contabilidad en un entorno de Dynamics 365 Finance, versión 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizaciones de asignaciones de doble escritura de Project Operations

No hay actualizaciones para las asignaciones de escritura dual de Project Operations en esta versión. Para obtener una lista actual y las versiones de las asignaciones de escritura dual de Project Operations, consulte [Versiones de asignación de doble escritura de Project Operations](../environment/resource-dual-write-maps.md).

Ejecute siempre la última versión de la asignación en su entorno y habilite todas las asignaciones de tabla relacionadas a medida que actualiza la solución Project Operations Dataverse y la versión de la solución de Finance. Es posible que algunas funciones y capacidades no funcionen correctamente si la última versión de la asignación no está activada. Puede ver la versión activa de la asignación en la página **Escritura dual** en la columna **Versión**. Para activar una nueva versión de la asignación, seleccione **Versiones de asignación de tabla**, seleccione la última versión y luego guarde la versión seleccionada. Si ha personalizado un mapa de asignación lista para usar, vuelva a aplicar los cambios. Para obtener más información, consulte [Administración del ciclo de vida de las aplicaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si tiene algún problema al iniciar la asignación, siga las instrucciones de la sección [Problema de columnas de tabla que faltan en las asignaciones](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guía de resolución de problemas de doble escritura.

## <a name="quality-updates"></a>Actualizaciones de calidad

### <a name="project-operations-on-dataverse"></a>Project Operations en Dataverse

| **Área de características** | **Número de referencia** | **Actualización de calidad** |
| --- | --- | --- |
| Tiempo y gastos | 1811407 | Se ajustó el rol de seguridad Aprobador de proyecto para aprobaciones de entrada de gastos. |
| Tiempo y gastos | 1811438 | Se ajustó el rol de seguridad Aprobador de proyecto para cancelación de aprobación de entrada de tiempo. |
| Tiempo y gastos | 2370126 | Se actualizaron los iconos **Tarea de proyecto** y **Rol** en la entidad **Entrada de tiempo**. |
| Tiempo y gastos | 2379879 | Se corregió la función **Copiar semana** en la entrada de tiempo cuando se usa Dynamics 365 para teléfonos. |
| Facturación y precios | 2371906 | El importe total de la factura proforma no debe ser ajustable en Project Operations para implementaciones basadas en recursos. |
| Facturación y precios | 2385802 | Se corrigió el error que ocurre con las horas reales negativas cuando se actualizan los totales del proyecto. |
| Facturación y precios | 2389675 | Se mejoró el comportamiento de confirmación de la factura proforma. La entidad de trabajos de larga duración debe tener en cuenta la actividad requerida para escribir los resultados de confirmación para contabilidad. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administración y contabilidad de proyectos de Dynamics 365 Finance

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Viajes y gastos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Los importes de las transacciones de impuestos sobre ventas y con proveedores que se registran a partir de un gasto que se creó a partir de una transacción con tarjeta de crédito son incorrectos. |
| Viajes y gastos | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Se crean líneas de liquidación incorrectas cuando se genera el diario de pagos. |
| Viajes y gastos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Los importes de las transacciones de impuestos sobre ventas que se registran a partir de un gasto que se creó a partir de una transacción con tarjeta de crédito son incorrectos. |
| Viajes y gastos | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Eliminar una línea de gastos puede llevar mucho tiempo. |
| Contabilidad de proyecto | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Después de aplicar KB 4619395, no se admite cambiar la secuencia numérica a **Continua** y cuando registra una estimación, se produce el siguiente error: "El sistema no admite la configuración 'continua' de la secuencia numérica Proj_X". |
| Contabilidad de proyecto | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | El registro de una factura de proveedor puede fallar con el siguiente mensaje de error: "Las transacciones en el asiento no se equilibran el 17/05/2021. (divisa de contabilidad: 0,00, divisa de informe: 0,01)." |
