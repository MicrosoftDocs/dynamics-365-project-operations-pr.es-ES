---
title: Dotar de personal a un proyecto con trabajadores contratados y capacidad subcontratada
description: Este tema explica cómo se pueden cubrir los requisitos del proyecto utilizando trabajadores contratados o capacidad subcontratada en Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902938"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotar de personal a un proyecto con trabajadores contratados y capacidad subcontratada

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Los miembros genéricos del equipo del proyecto pueden contar con empleados o trabajadores subcontratados. Al dotar de personal a un proyecto con trabajadores contratados, puede limitar sus opciones de dotación de personal a trabajadores contratados específicos que están asignados a una línea de subcontratos. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Busque requisitos de recursos de personal con trabajadores contratados que pertenezcan a una línea de subcontrato específica

Para buscar requisitos de recursos de personal con trabajadores contratados que pertenezcan a una línea de subcontrato específica, siga estos pasos:

1. Cree un miembro del equipo del proyecto genérico que haga referencia a un subcontrato y línea de subcontratación.
2. Genere un requisito de recursos para este miembro del equipo de proyecto genérico utilizando el botón **Generar requisito** en la subcuadrícula de miembros del equipo del proyecto.
3. Seleccione la fila de miembros del equipo y luego seleccione el botón **Reservar** en la subcuadrícula. 
4. Esto abre el tablero de programación con el contexto de requisitos. Junto con otros atributos como fechas, roles y campos de unidad organizativa, los filtros del tablero de programación también se completan automáticamente con los campos de línea de proveedor, subcontrato y subcontrato del requisito de recursos.
5. El sistema busca recursos que cumplan con los criterios de filtrado y los enumera. 
6. Seleccione uno de los recursos filtrados y reserve el recurso para el requisito. 
7. Se crea un miembro del equipo del proyecto y se actualiza con las referencias a un subcontrato y línea de subcontratación. Vaya a **Estimaciones del proyecto** y seleccione **Actualizar precios** para ver el costo actualizado de la asignación de recursos. 

> [!NOTE]
> Es posible que no siempre sea posible actualizar al miembro del equipo del proyecto con un subcontrato y una referencia de línea de subcontrato durante la reserva si el recurso se asigna a varias líneas de subcontrato. Si el sistema no puede actualizar al miembro del equipo del proyecto con una línea de subcontrato y subcontrato, abra el registro del miembro del equipo del proyecto y actualice manualmente estos campos para que la estimación del costo financiero refleje con precisión el costo del subcontratista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Búsqueda y requisitos de recursos de personal con cualquier trabajador por contrato

Para buscar y dotar de personal requisitos de recursos con cualquier trabajador por contrato, siga estos pasos:

1. Cree un miembro del equipo del proyecto genérico.
2. Genere un requisito de recursos para este miembro del equipo de proyecto genérico utilizando el botón **Generar requisito** en la subcuadrícula de miembros del equipo del proyecto.
3. Seleccione la fila de miembros del equipo y luego seleccione el botón **Reservar** en la subcuadrícula. 
4. Esto abre el tablero de programación con el contexto de requisitos. Junto con otros atributos como fechas, roles y campos de unidad organizativa, los filtros del tablero de programación también se completan automáticamente con los campos de línea de proveedor, subcontrato y subcontrato del requisito de recursos. Debido a que el requisito no tenía ningún valor de línea de subcontrato o subcontrato completado, estos atributos estarán vacíos en el panel de filtro.
5. El sistema busca recursos que cumplan con los criterios de filtrado y los enumera.
6. Actualice el campo **Tipo de trabajador** en el panel de filtro a **Trabajador contratado** para limitar la búsqueda a trabajadores contratados. Actualice **Vendedor** en el panel de filtro para seleccionar un proveedor para limitar la búsqueda y mostrar solo los trabajadores contratados que pertenecen a una empresa proveedora específica.
7. Seleccione un trabajador contratado de la lista y reserve el recurso para el requisito.
8. Se crea un miembro del equipo del proyecto. Sin embargo, el miembro del equipo del proyecto no se actualiza con ningún subcontrato o línea de subcontrato y, por lo tanto, la asignación de recursos no se calculará utilizando el precio del subcontrato. Actualice manualmente al miembro del equipo del proyecto con una línea de subcontrato y vaya a **Estimaciones del proyecto** y seleccione **Actualizar precios** para ver el costo actualizado de la asignación de recursos.

> [!NOTE]
> Los miembros del equipo del proyecto que tienen **Tipo de trabajador** como **Trabajador contratado** pero no tienen una referencia de subcontrato están marcados como **Inválido** en la cuadrícula **Miembros del equipo del proyecto**. Si hay miembros del equipo del pryecto con este estado, abra el registro del miembro del equipo del proyecto y actualice los campos de subcontrato y línea de subcontraración para que la estimación del costo financiero refleje con precisión el costo del subcontratista en la pestaña **Estimaciones**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
