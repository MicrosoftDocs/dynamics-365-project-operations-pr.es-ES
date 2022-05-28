---
title: 'Novedades de noviembre de 2020: implementación Lite de Project Operations: del acuerdo a la facturación proforma'
description: 'Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de noviembre de 2020 de la implementación Lite de Project Operations: del acuerdo a la facturación proforma.'
author: sigitac
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3a7d63e746edf73873840aee2f095192364cb286
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584663"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novedades de noviembre de 2020: implementación Lite de Project Operations: del acuerdo a la facturación proforma

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

La siguiente tabla enumera las actualizaciones de Project Operations en la versión del entorno CDS 4.4.0.70.

| Área de características                 | Número de referencia | Actualización de calidad                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Administración de oportunidades       | 2036993          | La línea de estimación y las líneas de contrato de asignación de recursos se actualizan en las cotizaciones ganadoras cuando el tipo de línea de cotización es **Todas las tareas**.                                                 |
|   Administración de oportunidades       | 2071514          | No se puede crear una factura para un hito de precio fijo en un contrato que tiene habilitada la facturación basada en tareas.                                                                          |
| Facturación y precios          | 2070392          | Las líneas de contrato del proyecto en la factura aumentan cada vez que se selecciona **Actualizar transacciones de facturas**.                                                                       |
| Planificación del proyecto             | 2043336          | No se puede eliminar el registro de un miembro del equipo del proyecto.                                                                                                                                    |
| Planificación del proyecto             | 2046013          | Comportamiento incoherente para las columnas de etiquetas Estimates durante la carga frente al cambio de tipo de fase de tiempo.                                                                                   |
| Planificación del proyecto             | 2046647          | Las horas de inicio y finalización tienen una diferencia de una hora cuando los requisitos de recursos se generan a partir de los miembros del equipo del proyecto.                                                                      |
| Planificación del proyecto             | 2053879          | (Según el próximo lanzamiento de CDS) PublishUnassignedAssignments interrumpe un intento de guardar una tarea cuando aparece el error "El valor pasado para ConditionOperator.In está vacío". |
| Planificación del proyecto             | 2055501          | Al dejar **Fecha de inicio del proyecto** vacío, se produce un error en la programación.                                                                                                      |
| Planificación del proyecto             | 2066817          | No se puede crear un recurso genérico con el selector de personas en la pestaña **Tareas**.                                                                                               |
| Planificación del proyecto             | 2067034          | El botón **Ver detalles** no está disponible en la página **Detalles de la tarea**.                                                                                                         |
| Administración de recursos          | 2046667          | Los miembros genéricos del equipo no se eliminan incluso después de que se hayan completado todos los recursos.                                                                                                     |
| Entrada de tiempo y gasto rápido | 2047499          | El botón **Nuevo** en la página de Entrada de tiempo abre la página **Nueva firma de correo electrónico**.                                                                                               |
| Entrada de tiempo y gasto rápido | 2059859          | Se abre una ventana emergente inesperada al crear una entrada de gastos.                                                                                                                         |
| Otros                        | 2044181          | [Desinstalación de pedido de compra]: al intentar desinstalar **msdyn_ProjectServiceCore_Patch** y las soluciones centrales del servicio msdyn Project, aparece el error "El registro no está disponible".        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]