---
title: Informes de gastos rediseñados
description: Este tema proporciona información sobre la experiencia rediseñada y reinventada para la entrada del informe de gastos.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: cad971f3b45faf13dab4cd71ff7439c44b2e7b61
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685675"
---
# <a name="redesigned-expense-reports"></a>Informes de gastos rediseñados

La entrada del informe de gastos se ha rediseñado para simplificar el proceso de completar informes de gastos y reducir el tiempo necesario. Estos son los componentes principales de la nueva experiencia de gastos:

- Un nuevo área de trabajo de gestión de gastos que le permite acceder a los gastos de su delegado.
- Una nueva experiencia de coincidencia de recibos para mostrar mejor los recibos a nivel de encabezado y simplificar el proceso de adjuntar recibos a las líneas de gastos.
- Una nueva cuadrícula de solo lectura le permite ver muchas más líneas de gastos y columnas de datos adicionales. Ahora puede ver todas las líneas desglosadas y divididas, junto con sus gastos principales.
- Un panel simplificado para editar gastos.
- Mensajes de error, advertencia y directivas rediseñados para ayudar a garantizar que tiene el contexto y la comprensión correctos del problema y cómo resolverlo. Microsoft ha eliminado muchos mensajes que aparecieron antes de que los usuarios tuvieran la oportunidad de completar sus tareas y abordar los problemas, como el mensaje de desglose incompleto.
- Una nueva página para especificar qué campos son obligatorios para su organización, qué campos son opcionales y qué campos no deben capturarse. Esta página le ayudará a reducir el número de campos que los usuarios deben establecer.
- Una nueva apariencia para los informes de gastos, de modo que los informes ya no parezcan diseñados para contables.

Para activar la nueva experiencia, use el espacio de trabajo **Gestión de funciones** para activar la característica **Informes de gastos reimaginados**. Cuando activa esta característica, se producen las siguientes acciones:

- El área de trabajo de gastos existente se reemplaza por el nuevo área de trabajo.
- Se agrega un nuevo elemento de menú para la visibilidad del campo de gastos.
- No se eliminan los elementos de menú existentes para los informes de gastos (la página existente) ni los campos del informe de gastos.
- Los flujos de trabajo y las aprobaciones aún le llevan a la página de informes de gastos existente.

## <a name="new-features"></a>Nuevas características

| Nueva característica | Descripción |
|---|----|
| Visibilidad del campo de gastos | Una nueva página de configuración le permite especificar qué campos deben deshabilitarse para una organización, qué campos deben ser obligatorios y qué campos se recomiendan. |
| Campos obligatorios | La nueva configuración simple le permite hacer que algunos campos sean obligatorios sin tener que usar el marco de directivas. |
| Campos opcionales | Se agrega una segunda página para campos opcionales. De esta manera, los empleados no sentirán que deben configurar los campos, pero los campos seguirán siendo fácilmente accesibles. |
| Agregar recibos sin adjuntar | La capacidad de agregar recibos sin adjuntar al informe de gastos es más visible desde el área de trabajo y en el informe de gastos. |
| Mensajería mejorada | Hay una mejor visibilidad de las líneas de gastos que tienen advertencias o errores. |
| Reducción de mensajes en la barra de mensajes| Se ha reducido el número de mensajes de Infolog y se ha hecho un esfuerzo para evitar que aparezcan mensajes duplicados en muchos casos. |
| Acciones comunes agrupadas | La interfaz se limpió con la adición de un nuevo botón de acciones para la mayoría de las acciones comunes a nivel de línea y la adición de un botón de puntos suspensivos (...) para el encabezado y otras acciones menos frecuentes. |
| Nuevo área de trabajo para aumentar la visibilidad | Un nuevo área de trabajo unifica funciones y vínculos que permiten a los usuarios moverse a diferentes áreas. |
| Agregar los gastos y recibos existentes durante la creación de gastos | Cuando crea informes de gastos, puede agregar todos los gastos y recibos, o los seleccionados. |
| Calculadora de tipos de cambio | Se agrega una calculadora de tipo de cambio que permite calcular el tipo de cambio para transacciones de desembolso directo en múltiples monedas. |
| Guardar y agregar nuevas líneas de gastos | Los botones **Guardar** y **Nuevo** están disponibles cuando se ingresan nuevos gastos, para ayudar a introducir rápidamente líneas de gastos. |
| Mejor visibilidad en líneas divididas y detalladas | Las líneas detalladas y divididas se agregan directamente a la lista de gastos para aumentar la visibilidad y ayudarle a determinar si hay errores de directiva o de otra clase. |
| Mostrar recibos durante el desglose | Los recibos pueden mostrarse durante el desglose. |

La versión inicial se centra en escenarios de entrada de gastos. Cualquier escenario de revisión o aprobación de informe de gastos seguirá utilizando la página de entrada de gastos existente.

Las siguientes funciones están presentes en la página existente, pero aún no están presentes en la nueva página. Estas características se volverán a introducir en las próximas versiones:

- Aprobaciones
- Aprobaciones de proveedores y capacidad de editar la contabilidad
- Múltiples puntos de entrada
- Integración de solicitudes de viaje
- Entidad de datos para la visibilidad del campo de gastos
- Entrada para gastos de dietas
- Flujo de trabajo a nivel de línea
- Soporte de aprobador interino
- Desglose avanzado


[!INCLUDE[footer-include](../includes/footer-banner.md)]