---
title: Campos e información de proyecto de contrato
description: Este tema proporciona información sobre los campos que afectan las líneas de contrato y la información sobre el contrato que se resume en todas las líneas de pedido.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088116"
---
# <a name="project-contract-fields-and-information"></a>Campos e información de proyecto de contrato 

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Este tema proporciona información sobre los campos que se aplican a todo el contrato del proyecto, incluida la configuración que afecta a todas las líneas del contrato. También se incluye información sobre el contrato que se resume en todos los elementos de línea para impulsar los KPI del contrato del proyecto.

La siguiente tabla enumera los campos de información en un proyecto de contrato que son exclusivos de Dynamics 365 Project Operations o tienen algunos cambios importantes en el comportamiento de los pedidos de ventas de Dynamics 365 Sales.

| Campo | Ubicación | Relevancia, propósito y orientación | Impacto posterior |
| --- | --- | --- | --- |
| Escribir | Pestaña **Resumen** (oculta) | Este es un campo de conjunto de opciones con las siguientes opciones:</br>- **Basado en el trabajo** (disponible solo cuando está instalado Project Operations)</br>- **Basado en artículo** (disponible solo cuando están instalados Project Operations and Sales)</br>- **Servicio basado en mantenimiento** (disponible cuando Dynamics 365 Field Service está instalado) | En Project Operations, el valor de este campo predeterminado es **Basado en el trabajo** y clasifica el contrato como un contrato basado en proyectos. Un contrato debe basarse en proyecto para permitir todas las extensiones y funciones específicas del proyecto. |
| Cliente potencial | Pestaña **Resumen** | La referencia al registro de cuenta o empresa del cliente. Cuando un contrato se crea a partir de una oferta, este campo se copia del campo correspondiente del registro de la oferta. | La moneda del contrato de proyecto se establece de forma predeterminada según la moneda del cliente. Esto se puede cambiar antes de guardar el contrato. |
| Administrador de cuentas | Pestaña **Resumen** | El nombre del Administrador de la cuenta de esta oferta. Cuando un contrato se crea a partir de una oferta, este campo se copia del campo correspondiente del registro de la oferta. | El Administrador de cuentas es responsable de gestionar la relación con el cliente hasta la finalización del proyecto. Según el registro de recursos reservables vinculado al Administrador de la cuenta, la unidad de contratación está predeterminada en el contrato de proyecto. |
| Unidad de contratación | Pestaña **Resumen** | La unidad organizativa responsable de la entrega de los proyectos asociados a este contrato. Cuando un contrato se crea a partir de una oferta, este campo se copia del campo correspondiente del registro de la oferta. | La unidad de contratación es la división de la empresa que ejecutará los proyecto. Cada unidad de contratación tiene una moneda, y esta moneda se utiliza para informar los costes estimados y reales incurridos durante el proyecto. |
| Lista de precios de productos | Pestaña **Resumen** | Esta lista de precios que se utiliza para los precios predeterminados en las líneas de contrato basadas en productos. La lista de opcione desplegables para este campo muestra una lista de listas de precios donde la moneda de la lista de precios coincide con la moneda del contrato. Cuando un contrato se crea a partir de una oferta, este campo se copia del campo correspondiente del registro de la oferta. En el contrato de proyecto este campo está predeterminado en el registro de la cuenta, pero se puede cambiar. | No hay ninguna relevancia descendente para este campo. |
| Divisa | Pestaña **Resumen** | La moneda utilizada para informar el valor de esta oferta y la moneda en la que se facturará al cliente. Cuando un contrato se crea a partir de una oferta, este campo se copia del campo correspondiente del registro de la oferta. En el contrato de proyecto este campo está predeterminado en el registro de la cuenta, pero se puede cambiar. | Una vez que se guarda un contrato, este campo ya no se puede editar. Este campo se usa para establecer el valor predeterminado de las listas de precios de productos y proyectos en el contrato. La moneda del contrato se utiliza para coincidir con la moneda de la lista de precios. |
| Límite a no exceder | Pestaña **Resumen** | Este campo indica el máximo negociado sobre el valor final que el cliente ha aceptado para esta oferta. | El límite se evalúa durante la ejecución y se aplica a todas las líneas de pedido y proyectos asociados con esta oferta. |
| Fecha de entrega solicitada | Pestaña **Resumen** | Cuando un contrato se crea a partir de una oferta de proyecto, este campo se copia del campo correspondiente del registro de la oferta de proyecto. | Esta fecha se utiliza como fecha de finalización para generar programaciones de facturas. |

Los siguientes KPI están disponibles en la pestaña **Rendimiento del contrato** de un contrato de proyecto.

| Campo | Ubicación | Relevancia, propósito y orientación |
| --- | --- | --- |
| Valor del contrato | Contrato general | El valor total del contrato del proyecto. |
| Importe facturado | Contrato general | La suma de los importes de todas las facturas de este contrato. |
| Coste incurrido | Contrato general | La suma de todos los costos reales registrados en todos los proyectos asignados al contrato. |
| Margen bruto | Contrato general | Monto facturado: coste incurrido hasta la fecha / monto facturado |
| Margen previsto | Contrato general | (Valor del contrato - Costos estimados) / Valor del contrato Costos estimados = La suma de todos los costos estimados en todos los proyectos asignados al contrato.|
| Valor del contrato | Líneas basadas en proyectos | El valor de la línea de contrato. |
| Importe facturado | Líneas basadas en proyectos | Para la línea de contrato de precio fijo: la suma de los importes de todos los datos reales de los hitos de ventas facturados contra esta línea de contrato en varias facturas creadas para este contrato. Para la línea de contrato de tiempo y materiales : la suma de los importes de todos los datos reales de las ventas facturadas facturables contra esta línea de contrato en varias facturas creadas para este contrato. |
| Coste incurrido | Líneas basadas en proyectos | La suma de todos los costos reales registrados en todos los proyectos asignados a la línea de contrato. |
| Margen bruto | Líneas basadas en proyectos | (Monto facturado - Coste incurrido hasta la fecha) / Monto facturado |
| Margen previsto | Líneas basadas en proyectos | (Importe de la línea del contrato en la moneda base - Costes estimados para la línea del contrato en la divisa base) / Importe de la línea del contrato en la divisa base |
| Coste incurrido | Detalle de una línea basada en proyectos | Tiempo: la suma de la cantidad de datos reales de costos de tiempo registrados para este rol en el proyecto asignado a la línea de contrato. Gastos: la suma de la cantidad de datos reales de costos de gastos registrados para esta categoría en el proyecto asignado a la línea de contrato. |
| Cantidad registrada | Detalle de una línea basada en proyectos | Tiempo: la cantidad de datos reales de costos de tiempo total para un rol en el proyecto que está asignado a esta línea de contrato. Gastos: todas las cantidades para esta categoría de gastos en los datos reales de costes de gastos en el proyecto están asignadas a esta línea de contrato. |
| Importe facturado | Detalle de una línea basada en proyectos | Para una línea de contrato de precio fijo, este campo se deja en blanco en el nivel de detalle y solo se muestra en el nivel de línea de contrato. Para una línea de contrato de tiempo y materiales, los cálculos se completan en el nivel de detalles. Los detalles muestran la suma del monto en todas las líneas de ingresos facturadas contra esta línea de contrato que son imputables. |
| Cantidad facturada | Detalle de una línea basada en proyectos | Para una línea de contrato de precio fijo, este campo se deja en blanco en el nivel de detalle y solo se muestra en el nivel de línea de contrato. Para una línea de contrato de tiempo y materiales, los cálculos se completan en el nivel de detalles para tiempo y gastos. Tiempo: la suma de las horas de todas las líneas de ingresos facturadas para este rol contra esta línea de contrato que son imputables. Gastos: todas las cantidades para esta categoría de gastos en los datos reales de costes de gastos en el proyecto están asignadas a esta línea de contrato. |
| Valor del contrato | Líneas basadas en productos | El valor de la línea de contrato de esta línea de contrato basada en productos. |
| Importe facturado | Líneas basadas en productos | La suma de los importes de todas las líneas de factura contra esta línea de contrato basada en productos en varias facturas que se crean para este contrato. |
| Coste incurrido | Líneas basadas en productos | La suma de todos los costos reales registrados para la línea de contrato basada en productos. |
| Margen bruto | Líneas basadas en proyectos | Monto facturado: coste incurrido hasta la fecha / monto facturado |
| Margen previsto | Líneas basadas en productos | (Valor de la línea del contrato - Costes estimados de la línea del contrato) / Valor de la línea del contrato |
