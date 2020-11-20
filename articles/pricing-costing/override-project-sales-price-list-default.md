---
title: Reemplazar listas de precios de venta de proyecto
description: Este tema proporciona información sobre cómo crear listas de precios de venta personalizadas.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130869"
---
# <a name="override-project-sales-price-lists"></a>Reemplazar listas de precios de venta de proyecto

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

## <a name="customer-specific-project-price-lists"></a>Listas de precios de proyecto específicas del cliente

Los acuerdos de precios específicos del cliente se pueden configurar como listas de precios de proyectos en un registro de cuenta en Dynamics 365 Project Operations.

Para configurar una lista de precios de proyecto específica del cliente, en el área **Ventas**, navegue hasta el registro de la cuenta.

1. Abra la página de lista **Cuentas**.
2. Busque y haga doble clic en un registro de cliente para abrir la página de detalles **Cuenta**.
3. En la pestaña **Listas de precios de proyectos**, seleccione **+ Nueva de lista de precios de proyecto^^.
4. Sobre la página **Lista de precios del nuevo proyecto**, seleccione una lista de precios en el menú desplegable. Solo las listas de precios que tienen el contexto establecido en **Ventas** y cuya moneda coincide con la moneda de la cuenta.
5. Dé un nombre a la asociación y luego y seleccione **Guardar**. Se crea una lista de precios de proyecto específica del cliente. Esta lista de precios se utilizará para predeterminar los precios del proyecto en las cotizaciones del proyecto o los contratos creados para este cliente cuando la fecha de creación de la cotización o el contrato del proyecto se encuentre dentro de la fecha de vigencia de la lista de precios.

## <a name="custom-pricing-on-project-quotes"></a>Precios personalizados en cotizaciones de proyectos

En las cotizaciones de proyectos, puede tener precios de proyectos que comiencen con una lista de precios estándar predeterminada que se establece por defecto del cliente o de los parámetros del proyecto.

Cuando necesite precios personalizados para trabajos relacionados con el proyecto en una cotización en particular, puede obtenerlos de la entidad asociada de listas de precios del proyecto.

Complete los siguientes pasos para configurar precios de proyecto específicos de cotización.

1. Abra la oferta del proyecto y seleccione la pestaña **Listas de precios de proyectos**.
2. En la subcuadrícula, seleccione **Crear precios personalizados**.

Todas las listas de precios del proyecto que se adjuntan a la cotización se copian en nuevas listas de precios. Los nombres de las nuevas listas de precios reflejan el nombre de la cotización con un sello de fecha y hora para cuando se crearon estas listas de precios.

Puede utilizar cada una de esas listas de precios y actualizar los precios de mano de obra (precio de función) y de gastos (precio de categoría). Estos precios se aplicarán únicamente a esta oferta de proyecto.

## <a name="price-lists-on-a-project-contract"></a>Listas de precios de un contrato de proyecto

En un contrato de proyecto, el precio del proyecto siempre se establece de forma predeterminada como una lista de precios personalizada con el nombre del contrato y el sello de fecha y hora creado adjunto al nombre. Esto es cierto si el contrato se creó cuando se ganó la cotización o si el contrato se creó desde cero. Si es necesario, puede eliminar esta asociación a la lista de precios personalizada y asociar una lista de precios estándar al contrato del proyecto.

Cuando asocia una lista de precios estándar a las listas de precios del proyecto en la cotización o el contrato, cualquier cambio realizado en los precios en la lista de precios afectará a todas las cotizaciones y contratos que utilizan la lista de precios.
