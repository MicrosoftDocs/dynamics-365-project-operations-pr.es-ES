---
title: Usar un recurso reservable como dimensión de precios
description: En este tema se proporciona información sobre cómo usar un recurso que se puede reservar como dimensión de precios.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d46d4659a5f60226f80b29f3dd8607249cb91ac2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011212"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Usar un recurso reservable como dimensión de precios

 _**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_ 

En este tema se proporciona información sobre cómo usar un recurso que se puede reservar como dimensión de precios. Si su estrategia de precios está configurada de manera que cada recurso reservable debe tener un precio o tasa de coste específicos, utilice un recurso reservable como dimensión de precios.

## <a name="prerequisites"></a>Requisitos previos
Antes de completar los procedimientos de este tema, debe tener una nueva solución de dimensión de precios para su organización. Si aún no ha creado uno, consulte [Crear entidades y campos personalizados](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Agregar el campo Recurso que se puede reservar a formularios y vistas
Para que el campo **Recurso que se puede reservar** sea visible en la solución de dimensión de precios, debe agregar el campo a todos los formularios y vistas como una entidad.

En la siguiente tabla se enumeran todos los formularios y vistas listos para usar, por entidad. También deberá agregar el nuevo campo a cualquier formulario o vista adicional en sus entidades personalizadas.

|   Entity        | Formularios   |Vistas        |
| ------------------------------|---------------------------------|----------------------------------|
|  Precio de rol| Información | - Precios de categorías de recursos activos<br> - Vista asociada de precios de categorías de recursos |
|  Incremento del precio de rol| Información| - Activo - Incremento del precio de rol<br>- Incremento del precio de rol - Vista asociada |
|  Detalle de línea de oferta| - Información del proyecto<br>- Creación rápida de proyecto| - Detalle de línea de oferta activo<br>- Detalles de líneas de oferta combinadas<br>- Vista asociada de detalles de líneas de oferta |
|  Detalle de línea de contrato del proyecto| - Información del proyecto<br>- Creación rápida de proyecto| - Detalles de línea de contrato combinados<br>- Detalles de línea de contrato activos<br>- Vista asociada de detalles de línea de contrato |
|  Tarea de proyecto| - Información<br>- Nuevo formulario| &nbsp; |
|  Miembro del equipo del proyecto| - Información<br>- Nuevo formulario| - Miembros del equipo del proyecto activos<br>- Miembros del equipo del proyecto<br>- Miembros del equipo del proyecto asociados |
|  Entrada de tiempo| - Información<br>- Crear entrada de tiempo| - Mis entradas de tiempo por fecha<br>- Mis entradas de tiempo para esta semana<br>- Entradas de tiempo pendientes de aprobación|
|  Línea de diario| - Información<br>- Creación rápida| - Líneas de diario activas<br>- Vista asociada de líneas de diario |
|  Detalle de línea de factura| - Información<br>- Creación rápida| - Detalles de líneas de factura activos<br>- Transacciones de facturas imputables<br>- Transacciones de facturas gratuitas<br>- Vista asociada de detalle de línea de factura <br>- Transacciones de facturas no imputables|
|  Real| - Información<br>- Datos reales activos| Vista asociada de datos reales |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurar un recurso que se puede reservar como dimensión de precios
Para configurar un recurso que se puede reservar como dimensión de precios, siga estos pasos:

1. Vaya a **Configuración** > **Parámetros**. 
2. En la página **Parámetro**, en la pestaña **Dimensiones de precios basadas en el importe**, compruebe que la cuadrícula muestra los registros en la entidad **Dimensiones de precios**. 
2. Agregue el **Recurso que se puede reservar** a la lista de dimensiones de precios como **msdyn_bookableresource**. 
3. En **Aplicable a costes** y **Aplicable a ventas**, seleccione un valor.
4. En **Tipo de dimensión**, seleccione **Basado en el importe**. 
5. Seleccione el coste y la prioridad de ventas para el recurso que se puede reservar. Normalmente, un recurso que se puede reservar tiene la máxima prioridad cuando se incluye como una dimensión de precios. Establezca la prioridad en **1** (o **0** en función de cómo cuente la prioridad) para garantizar este comportamiento.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar nombres de campo de dimensión de precios

Cuando el nombre del campo de una dimensión de precios de la tabla **Precio de rol** es distinto del nombre de campo de cualquiera de las demás entidades en las que se usa el precio predeterminado, el registro de la dimensión de precios debe estar al tanto de los distintos nombres.  

Para un recurso que se puede reservar, la entidad **Miembros del equipo del proyecto** tiene un nombre de campo un poco diferente del de la entidad **Precio de rol**: 

 - Entidad **Miembros del equipo del proyecto** = **msdyn_bookableresourceid**
 - Entidad **Precio de rol** =**msdyn_bookableresource**

El registro de la dimensión de precios para **msydn_bookableresource** debe estar al tanto de esta diferencia.

1. Haga doble clic en la fila de la cuadrícula **Dimensiones de precios** para abrir la página de la dimensión de **msdyn_bookableresource**.
2. En la página de la dimensión, en la pestaña **Relacionado**, seleccione **Nombres de campos de la dimensión de precios**.

  ![Pestaña de nombres de campo de la dimensión de precios](media/PD-fieldname.png)

3. En la vista asociada que se abre, seleccione **Agregar nuevo nombre del campo de la dimensión de precios**.

  ![Agregar nuevos nombres de campo de la dimensión de precios](media/Add-NewPD-fieldname.png)

  Esto abre la página **Nuevo nombre de campo de la dimensión de precios** para **msdyn_bookableresource**. 

4. En la página **Nuevo nombre de campo de dimensión de precios**, agregue **msdyn_projectteam** a **Nombre lógico de la entidad**.
5. Agregue **msdyn_bookableresourceid** a **Nombre del campo**.

 ![Formulario de nuevo nombre de campo de la dimensión de precios](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]