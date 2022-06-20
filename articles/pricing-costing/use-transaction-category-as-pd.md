---
title: Usar la categoría de transacción como dimensión de precios
description: En este artículo se proporciona información sobre cómo usar el campo Categoría de transacción como dimensión de precios.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911725"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Usar la categoría de transacción como dimensión de precios


_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_


En este artículo se explica cómo usar el campo **Categoría de transacción** como dimensión de precios. 

## <a name="prerequisites"></a>Requisitos previos
Antes de completar los procedimientos de este artículo, debe tener una nueva solución de dimensión de precios para su organización. Si aún no ha creado una, consulte [Crear entidades y campos personalizados como dimensiones de precios](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Agregar el campo Categoría de transacción a formularios y vistas
Para que el campo **Categoría de transacción** sea visible en la solución de dimensión de precios, debe agregar el campo a todos los formularios y vistas como una entidad.

En la siguiente tabla se enumeran todos los formularios y vistas listos para usar, por entidad. También deberá agregar el nuevo campo a cualquier formulario o vista adicional en sus entidades personalizadas.

|  Entity        | Formularios     |Vistas        |
| ------------------------------|---------------------------------|----------------------------------|
|  Precio de rol| Información |- Precios de categorías de recursos activos<br> - Vista asociada de precios de categorías de recursos |
|  Incremento del precio de rol| Información|- Activo - Incremento del precio de rol<br>- Incremento del precio de rol - Vista asociada |
|  Detalle de línea de oferta|- Información del proyecto<br>- Creación rápida de proyecto| - Detalle de línea de oferta activo<br>- Detalles de líneas de oferta combinadas<br>- Vista asociada de detalles de líneas de oferta |
|  Detalle de línea de contrato de proyecto|- Información del proyecto<br>- Creación rápida de proyecto|- Detalles de línea de contrato combinados<br>- Detalles de línea de contrato activos<br>- Vista asociada de detalles de línea de contrato |
|  Tarea de proyecto|- Información<br>- Nuevo formulario| &nbsp; |
|  Miembro del equipo del proyecto|- Información<br>- Nuevo formulario|- Miembros del equipo del proyecto activos<br>- Miembros del equipo del proyecto<br>- Miembros del equipo del proyecto asociados |
|  Entrada de tiempo|- Información<br>- Crear entrada de tiempo|- Mis entradas de tiempo por fecha<br>- Mis entradas de tiempo para esta semana<br>- Entradas de tiempo pendientes de aprobación|
|  Línea de diario|- Información<br>- Creación rápida|- Líneas de diario activas<br>- Vista asociada de líneas de diario|
|  Detalle de línea de factura|- Información<br>- Creación rápida|- Detalles de líneas de factura activos<br>- Transacciones de facturas imputables<br>- Transacciones de facturas gratuitas<br>- Vista asociada de detalle de línea de factura <br>- Transacciones de facturas no imputables|
|  Real|- Información<br>- Datos reales activos| Vista asociada de datos reales |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurar el campo Categoría de transacción como una dimensión de precios

1. Vaya a **Configuración** > **Parámetros**. 
2. En la página **Parámetros**, en la pestaña **Dimensiones de precios basadas en el importe**, compruebe que la cuadrícula muestra los registros en la entidad **Dimensiones de precios**.
3. Agregue **Categoría de transacciones** a esta lista y establezca los campos **Aplicable a costes** y **Aplicable a ventas** en **Sí**.
4. En el campo **Tipo de dimensión**, seleccione **Basado en el importe** y, a continuación, seleccione la prioridad para **Categoría de transacción** relacionada con el coste y las ventas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]