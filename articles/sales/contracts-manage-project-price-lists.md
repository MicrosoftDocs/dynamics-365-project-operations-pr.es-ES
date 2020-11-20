---
title: Administrar listas de precios de proyectos en contratos de proyectos
description: Este tema proporciona información sobre cómo administrar listas de precios de proyectos en contratos de proyectos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133450"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Administrar listas de precios de proyectos en contratos de proyectos

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los contratos de proyecto en Dynamics 365 Project Operations están diseñados para admitir varias listas de precios de venta de fecha efectiva en un contrato. En Project Operations, hay una nueva entidad asociada llamada **Listas de precios de proyectos**. Esta entidad tiene una relación de uno a varios con un contrato de proyecto.

Las listas de precios de proyectos se utilizan para fijar el precio de las transacciones de tiempo y gastos en un proyecto. Cuando un contrato tiene una o más listas de precios de proyectos, estas listas de precios se utilizan para calcular el precio de las estimaciones de tiempo y gastos y los datos reales de los proyectos que están asociados al contrato a través de la línea de contrato.

Cuando no hay listas de precios del proyecto en un contrato de proyecto, verá un mensaje de advertencia que indica que no hay listas de precios del proyecto y que sus estimaciones, el trabajo real del proyecto y los gastos no tendrán precio. No habrá precio para los valores de venta.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Asociar o desasociar una lista de precios de proyecto en un contrato de proyecto

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Cree o asocie una lista de precios específica para estimar el trabajo y los gastos basados en el proyecto

1. En el contrato del proyecto, seleccione la pestaña **Listas de precios de proyectos**.
2. En la subcuadrícula, seleccione **+ Agregar nueva lista de precios del proyecto**.
3. En el control deslizante **Creación rápida**, seleccione una lista de precios. 

  La lista desplegable muestra todas las listas de precios que tienen el contexto establecido en **Ventas**, donde la moneda de la lista de precios coincide con la moneda del contrato.
  
4. Ingrese una descripción para la asociación de lista de precios del proyecto, seleccione **Salvar** y luego cierre el control deslizante **Creación rápida**.

   Se crea una asociación de lista de precios del proyecto.
   
5. Repita los pasos 1 a 4 para asociar más de una lista de precios del proyecto al contrato del proyecto. Solo cree varias listas de precios de proyectos si tiene una fecha de vigencia diferente en cada una de las listas de precios de proyectos asociados.

> [!NOTE]
> Project Operations no admite la superposición de la fecha de vigencia de las listas de precios del proyecto. Si hay varias listas de precios de proyectos para una transacción con una fecha determinada, el precio de esa transacción se establecerá por defecto en cero.

### <a name="remove-a-project-price-list-association"></a>Quitar una asociación de lista de precios de proyecto

- Seleccione la lista de precios del proyecto y luego seleccione **Eliminar lista de precios del proyecto del contrato** en la subcuadrícula. 

  La lista de precios se elimina de las listas de precios del proyecto en el contrato. La lista de precios en sí no se eliminará. Solo se eliminará la asociación al contrato.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurar el incumplimiento automático de las listas de precios del proyecto en un contrato

Se puede configurar una lista de precios del proyecto como lista predeterminada en un contrato de proyecto. Esta configuración puede ayudar a garantizar que todos los contratos de su organización siempre comiencen con una lista de precios estándar para ese período de precios.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurar el valor predeterminado organizativo para listas de precios de proyectos

1. Vaya a **Configuración** > **General** y después seleccione **Parámetros**.
2. En la página de lista **Parámetros activos**, seleccione y haga doble clic en el registro para abrirlo. Al hacer doble clic, asegúrese de no hacer clic en un valor de campo que sea un hipervínculo. 
3. Sobre la página **Parámetros activos**, seleccione la pestaña **Lista de precios**. Una subcuadrícula muestra una lista de listas de precios predeterminadas. Esta es una lista de costos estándar y listas de precios de venta. Tener una lista de precios de **Ventas** asociada aquí para cada moneda en la que vende garantiza que la lista de precios de venta sea la predeterminada en cualquier contrato que cree para los clientes que realizan transacciones en esta moneda.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurar una lista de precios de proyecto específica para el cliente

También puede configurar listas de precios de proyectos específicos para el cliente cuando haya negociado un acuerdo de precios marco con sus clientes.

1. Vaya a **Ventas** > **Clientes**.
2. De la lista de cuentas activas, seleccione el cliente para el que tiene una lista de precios especial.
3. Seleccione el registro del cliente para abrirlo y luego seleccione la pestaña **Listas de precios de proyectos**. Una subcuadrícula muestra una lista de listas de precios de proyectos específicas para este cliente. 
4. Cree una nueva asociación de lista de precios aquí para tener una lista de precios del proyecto específica para este cliente.

## <a name="custom-pricing-on-a-project-contract"></a>Precios personalizados en un contrato de proyecto

Una vez que tenga listas de precios de proyectos predeterminadas organizativas y específicas del cliente, sus contratos de proyecto se crearán automáticamente con estas asociaciones de listas de precios de proyectos. Sin embargo, las listas de precios del proyecto en un contrato de proyecto siempre se copian con la fecha y el nombre del contrato adjuntos. Los gerentes de cuentas y proyectos pueden comenzar a editar los precios de estas copias. Estos precios modificados se aplicarán únicamente a este contrato de proyecto.