---
title: Administrar listas de precios de proyectos en ofertas de proyectos (lite)
description: En este tema se proporciona información sobre el trabajo con listas de precios de proyectos en ofertas. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176002"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Administrar listas de precios de proyectos en ofertas de proyectos (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

Las ofertas de proyectos están diseñadas para admitir listas de precios de venta vigentes en varias fechas. Con Dynamics 365 Project Operations, se añade una nueva entidad asociada llamada **Listas de precios de proyectos**. Esta entidad tiene una relación de 1 a muchos con la oferta de un proyecto.

Las listas de precios de proyectos se utilizan para fijar el precio de las transacciones de tiempo y gastos en un proyecto. Cuando una oferta tiene una o más listas de precios de proyectos, estas listas de precios se utilizan para valorar las estimaciones de tiempo y gastos y los datos reales de los proyectos asociados a la oferta a través de la línea de oferta.

Cuando no haya listas de precios de proyectos en una oferta de proyecto, recibirá un mensaje de advertencia. El mensaje indica que, debido a que no hay listas de precios del proyecto, no se fijarán los precios de su trabajo y gastos estimados y reales del proyecto. En cambio, tendrán un precio cero (0) para los valores de venta.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Asociar o desvincular una lista de precios de proyecto en una oferta de proyecto

Para crear o seleccionar una lista de precios específica para estimar el trabajo y los gastos basados en el proyecto, complete los siguientes pasos.

1. En la oferta, seleccione la pestaña **Precio del proyecto** y, en la subcuadrícula, seleccione **+ Agregar nueva lista de precios del proyecto**.
2. En la página Creación rápida, seleccione una lista de precios. La lista desplegable muestra todas las listas de precios que tienen el contexto establecido en **Ventas** y la moneda coincide con la moneda de la oferta.
4. Introduzca una descripción para la asociación de lista de precios del proyecto y seleccione **Guardar y cerrar**.

Se crea una asociación de lista de precios del proyecto.

Puede repetir este proceso si necesita asociar más de una lista de precios del proyecto a la oferta del proyecto. Solo cree varias listas de precios de proyectos si tiene diferentes fechas de vigencia en cada una de las listas de precios de proyectos asociados.

> [!NOTE]
> Project Operations no admite la superposición de fechas de vigencia de las listas de precios del proyecto. Si hay varias listas de precios de proyectos para una transacción con una fecha determinada, el precio de esa transacción se establecerá de forma predeterminada en cero (0).
Para eliminar una asociación de lista de precios del proyecto, seleccione la lista de precios del proyecto y luego seleccione **Eliminar lista de precios del proyecto de oferta**. La lista de precios se elimina de las listas de precios del proyecto de la oferta, pero la propia lista de precios no se elimina. Solo se elimina la asociación a la oferta.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurar listas de precios de proyectos predeterminadas en una oferta

Las listas de precios del proyecto se pueden configurar de forma predeterminada en una oferta del proyecto. Esta configuración garantiza que todas las ofertas de su organización siempre comiencen con una lista de precios estándar para ese período de precios.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurar valores predeterminados de organización para listas de precios de proyectos

1. Vaya a **Configuración** > **General** > **Parámetros**.
2. En la página de lista **Parámetros activos**,localice el registro y haga doble clic para abrirlo. 
3. En la página **Parámetros**, seleccione la pestaña **Lista de precios**. Puede ver como se muestra la lista de listas de precios predeterminadas. Esta es una lista de costes estándar y listas de precios de venta. Tener una lista de precios de venta asociada aquí para cada divisa en la que venda, garantizará que esta lista de precios de venta esté predeterminada en cualquier oferta que cree para los clientes que realizan transacciones en esta divisa.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurar listas de precios de proyectos específicas para clientes

También se pueden configurar listas de precios de proyectos específicos para el cliente cuando haya negociado un contrato de precios marco con sus clientes.

Para configurar una lista de precios de proyecto específica para el cliente, complete los siguientes pasos.

1. En la zona **Ventas**, seleccione **Cliente**.
2. En la lista de sus cuentas activas, seleccione y abra el registro de cliente para el que tiene una lista de precios especial.
3. En la pestaña **Listas de precios de proyectos**, puede crear una nueva asociación de lista de precios para tener la lista de precios del proyecto que es específica para este cliente.

## <a name="create-custom-pricing-on-a-project-quote"></a>Crear precios personalizados en una oferta de proyecto

Una vez que tenga listas de precios de proyectos predeterminadas de la organización y específicas del cliente, sus ofertas de proyectos se crearán automáticamente con estas asociaciones de listas de precios de proyectos. Sin embargo, en ciertos casos, es posible que deba crear precios personalizados para una oferta de proyecto específica. 

1. En **Oferta del proyecto**, en la pestaña **Lista de precios del proyecto**, verifique en la subcuadrícula que no se haya seleccionado ningún registro de lista de precios específico.
2. Seleccione **Crear precios personalizados**. Esto hará copias de todas las listas de precios estándar actualmente asociadas a la oferta y asociará estas copias a la oferta. Se eliminarán las asociaciones existentes con las listas de precios estándar. El comercial puede entonces comenzar a editar los precios de estas copias. Estos precios modificados se aplicarán únicamente a la oferta de este proyecto.
