---
title: 'Novedades de marzo de 2022: implementación ligera de Project Operations'
description: Este tema proporciona información sobre las actualizaciones de calidad disponibles en la versión de marzo de 2022 de la implementación simplificada de Project Operations.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583771"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novedades de marzo de 2022: implementación ligera de Project Operations

_Se aplica a: Implementación ligera: del acuerdo a la facturación proforma_

Este tema se aplica a los siguientes componentes y versiones de Microsoft Dynamics 365 Project Operations:

- Project Operations en una versión del entorno de Dataverse 4.30.0.99

## <a name="features-included-in-this-release"></a>Características incluidas en esta versión

- Subcontratación: creación de facturas de proveedores y coincidencia de experiencias

## <a name="quality-updates"></a>Actualizaciones de calidad

| Área de características | Número de referencia | Actualización de calidad |
| --- | --- | --- |
| Tiempo y gastos | 2388011 | Mostrar comentarios de rechazo a los remitentes de entradas de tiempo durante la aprobación masiva. |
| Planificación y seguimiento del proyecto | 2495294 | Los detalles del proyecto no deben ser editables en la página **Detalles de la tarea**. |
| Facturación y precios | 2499605 | Los hitos de contrato que se crean a partir de hitos de cotización se marcan incorrectamente como de solo lectura. |
| Planificación y seguimiento del proyecto | 2506050 | El conjunto de operaciones permanece pendiente durante una hora si no hay ningún cambio que guardar. A continuación, el conjunto se marca falsamente como **Fallido**, mientras que debe completarse inmediatamente. |
| Facturación y precios | 2507401 | Las unidades de contratación predeterminadas se ingresan incorrectamente en los proyectos debido a un almacenamiento en caché incorrecto. |
| Facturación y precios | 2541660 | **Validación de creación de pedidos de venta** en doble escritura debe ser solo para pedidos basados en proyectos. |
| Facturación y precios | 2552745 | Los impuestos no se dividen entre los clientes que han configurado reglas de facturación dividida. |
| Facturación y precios | 2558859 | Mensajes de error mejorados cuando se configuran las dimensiones de precios. |
| Facturación y precios | 2558933 | **Importar desde estimaciones del proyecto** falla cuando **msdyn\_project** se agrega como una dimensión de precios. |
| Facturación y precios | 2559101 | La eliminación de parámetros del proyecto no está bloqueada y causa problemas. |
| Administración de oportunidades | 2570390 | El complemento de doble escritura obliga a que el tipo de cuenta en cotizaciones, pedidos y oportunidades sea **Cliente**, incluso cuando ese tipo de cuenta no sea correcto. |
| Facturación y precios | 2586097 | Los datos reales de costos facturados divididos no se revierten cuando se elimina un proyecto de una línea de contrato de proyecto. |
| Facturación y precios | 2589619 | El impuesto sobre el material fuera de catálogo se propaga a los datos reales de ventas no facturados y a la factura. |
| Administración de oportunidades | 2594015 | Un presupuesto no se puede cerrar como ganado para clientes que tienen términos de pago **Net60**. |
| Planificación y seguimiento del proyecto | 2595841 | En Project for the Web, los usuarios reciben un mensaje de error acerca de un **msdyn\_actualstart** que falta cuando crean una nueva solicitud de recursos. |
| Tiempo y gasto | 2602511 | El campo **Rechazado por** para las entradas de tiempo muestra **Sistema** en lugar de un usuario designado como rechazador. |
| Tiempo y gasto | 2602528 | Un aprobador de proyectos puede aprobar el tiempo en proyectos en los que no figura como aprobador. |
| Facturación y precios | 2608550 | Una factura de corrección se puede confirmar incluso si no hay cambios en el original. |

## <a name="removed-and-deprecated-features"></a>Características quitadas y en desuso

El tema [Funciones quitadas o en desuso en Project Operations](../../whats-new/removed-depreciated-features-project.md) describe funciones que se eliminaron o dejaron en desuso para Dynamics 365 Project Operations.

- Una característica quitada ya no está disponible en el producto.
- Una función en desuso no está en desarrollo activo y se podría quitar en una actualización futura.

Antes de eliminar una característica del producto, aparecerá un aviso de desuso en el tema [Características quitadas o en desuso en Project Operations](../../whats-new/removed-depreciated-features-project.md), 12 meses antes de su eliminación.
