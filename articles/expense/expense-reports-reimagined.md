---
title: Informes de gastos rediseñados (contiene vídeo)
description: Este artículo explica la experiencia rediseñada y reinventada para la entrada de informes de gastos.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c74b4b70722af72bc66dba0662813c29d3d1df04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930293"
---
# <a name="expense-reports-reimagined"></a>Informes de gastos reinventados

La entrada del informe de gastos se ha rediseñado para simplificar el proceso y reducir el tiempo necesario para completar un informe. Estos son los componentes principales de la nueva experiencia de gastos:

- Un nuevo área de trabajo de gestión de gastos que le permite acceder a los gastos de su delegado.
- Una nueva experiencia de coincidencia de recibos para mostrar mejor los recibos a nivel de encabezado y simplificar el proceso de adjuntar recibos a las líneas de gastos.
- Una nueva cuadrícula de solo lectura que le permite ver muchas más líneas de gastos y otras columnas de datos. Ahora puede ver todas las líneas desglosadas y divididas, junto con sus gastos principales.
- Un panel simplificado para editar gastos.
- Mensajes de error, advertencia y directivas rediseñados para proporcionar el contexto y la comprensión correctos del problema y cómo resolverlo. Hemos eliminado varios de los mensajes que aparecían antes de que los usuarios pudieran completar sus tareas y solucionar los problemas.
- Una nueva página para especificar los campos obligatorios, los campos opcionales y los campos que no deben incluirse. Esta página ayuda a reducir el número de campos que se deben configurar.
- Una nueva apariencia para los informes de gastos, de modo que los informes ya no parezcan diseñados para contables.

Para activar la nueva experiencia, use el área de trabajo **Administración de características** para activar la característica **Área de trabajo de informes de gastos reinventados**. Cuando activa esta característica, se producen las siguientes acciones:

- El área de trabajo de gastos existente se reemplaza por el nuevo área de trabajo.
- Se agrega un nuevo elemento de menú para la visibilidad del campo de gastos.
- No se eliminan los elementos de menú existentes para los informes de gastos (la página existente) ni los campos del informe de gastos.
- Los flujos de trabajo y las aprobaciones aún le llevan a la página de informes de gastos existente.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Nuevas características

| Nueva característica | Descripción |
|---|----|
| Visibilidad del campo de gastos | Una nueva página de configuración le permite especificar qué campos deben deshabilitarse para una organización. También puede especificar qué campos deben ser obligatorios y qué campos se recomiendan. |
| Campos obligatorios | La nueva configuración simple le permite hacer que algunos campos sean obligatorios sin tener que usar el marco de directivas. |
| Campos opcionales | Se agrega una segunda página para campos opcionales. De esta manera, los empleados no sentirán que deben configurar los campos, pero los campos seguirán siendo fácilmente accesibles. |
| Agregar recibos sin adjuntar | La capacidad de agregar recibos sin adjuntar al informe de gastos es más visible desde el área de trabajo y en el informe de gastos. |
| Mensajería mejorada | Hay una mejor visibilidad de las líneas de gastos que tienen advertencias o errores. |
| Reducción de mensajes en la barra de mensajes| Se ha reducido el número de mensajes de Infolog y se ha hecho un esfuerzo para evitar que aparezcan mensajes duplicados en muchos casos. |
| Acciones comunes agrupadas | La interfaz se limpió con la adición de un nuevo botón de acciones para la mayoría de las acciones comunes a nivel de línea y la adición de un botón de puntos suspensivos (...) para el encabezado y otras acciones menos frecuentes. |
| Nuevo área de trabajo para aumentar la visibilidad | Un nuevo área de trabajo unifica funciones y vínculos que permiten a los usuarios moverse a diferentes áreas. |
| Agregar los gastos y recibos existentes durante la creación de gastos | Cuando crea informes de gastos, puede agregar todos los gastos o seleccionar gastos no adjuntos. Los gastos no adjuntos son los gastos que se importaron de la fuente de la tarjeta de crédito corporativa o los gastos que el usuario creó manualmente pero que no se adjuntaron a un informe de gastos.|
| Calculadora de tipos de cambio | Se agrega una calculadora de tipo de cambio que permite calcular el tipo de cambio para transacciones de desembolso directo en múltiples monedas. |
| Guardar y agregar nuevas líneas de gastos | Los botones **Guardar** y **Nuevo** están disponibles cuando se ingresan nuevos gastos, para ayudar a introducir rápidamente líneas de gastos. |
| Mejor visibilidad en líneas divididas y detalladas | Las líneas detalladas y divididas se agregan directamente a la lista de gastos para aumentar la visibilidad y ayudarle a determinar fácilmente si hay algún error. |
| Ver detalles de subcategorías en líneas detalladas | Las líneas desglosadas de un gasto primario muestran las etiquetas de subcategoría en el informe de gastos. El desglose le permite revisar los detalles granulares de un vistazo.|
|Detallar los gastos recurrentes rápidamente | El espacio de trabajo de gastos reinventado brinda la capacidad de detallar los gastos recurrentes rápidamente agregando la subcategoría, la fecha de inicio y la cantidad. La cantidad se refiere al número de veces que se repite la carga a lo largo de un período continuo. |
| Mostrar recibos durante el desglose | Los recibos pueden mostrarse durante el desglose. |
| Selección de anticipo de efectivo | Seleccione uno o más adelantos en efectivo para realizar una sola transacción de gastos. |
| Saldo de anticipo de efectivo | Revise el saldo de anticipos en efectivo en tiempo real cuando cree una entrada de gastos contra anticipos en efectivo aprobados y pagados. |

La versión inicial se centra en escenarios de entrada de gastos. Cualquier escenario de revisión o aprobación de informe de gastos seguirá utilizando la página de entrada de gastos existente.


Las siguientes características no son compatibles con el área de trabajo de informes de gastos reinventados, pero están previstas para versiones futuras: 

- Integración de solicitudes de viaje
- Entrada de gastos por día
- Soporte de aprobador interino
- Capacidad para ver el historial del flujo de trabajo


[!INCLUDE[footer-include](../includes/footer-banner.md)]
