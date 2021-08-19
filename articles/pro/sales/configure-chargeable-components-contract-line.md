---
title: Configurar componentes facturables de una línea de contrato basada en proyectos
description: Este tema proporciona información sobre cómo agregar componentes facturables a las líneas de contrato en Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003477"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar componentes facturables de una línea de contrato basada en proyectos

_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_

Una línea de contrato basada en proyectos tiene *incluido* componentes y componentes *facturables*.

Los componentes incluidos son componentes que están sujetos a:

  - Método de facturación y divisiones de clientes
  - Límites a no exceder 
  - Configuración de frecuencia de facturación definida en la línea de contrato basada en proyecto

Un subconjunto de los componentes incluidos se puede marcar como facturable usando el campo **Tipo de facturación**. El campo **Tipo de facturación** es un conjunto de opciones que permite los siguientes valores en el contexto de una línea de contrato:

  - Imputable
  - No facturable

Los componentes facturables se pueden definir en tareas, roles y categorías de transacciones.

La facturabilidad se define en las tareas de una línea de contrato de proyecto y se aplica a todas las clases de transacciones incluidas en la línea. Si el campo **Incluir tareas** en una línea de contrato está en blanco o configurado en **Proyecto entero**, la pestaña **Tareas imputables** no estará disponible.

La imputabilidad definida en roles para una línea de contrato de proyecto solo se aplica a la clase de transacción **Hora**. Si el campo **Incluir tiempo** en una línea de contrato está configurado en **No**, la pestaña **Roles facturables** no estará disponible.

La imputabilidad definida en categorías de transacción para una línea de contrato de proyecto solo se aplica a la clase de transacción **Gastos**. Si el campo **Incluir gastos** en una línea de contrato está configurado en **No**, la pestaña **Categorías facturables** no estará disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizar una tarea del proyecto como facturable o no facturable

Una tarea de proyecto puede ser facturable o no facturable en una línea de contrato específica, lo que hace posible la siguiente configuración:

Si una línea de contrato basada en proyecto incluye **Tiempo** y una determinada tarea, **T1** está asociado como facturable. Si hay una segunda línea de contrato que incluye **Gastos**, puede asociar la tarea T1 en la línea de contrato como no imputable. El resultado es que todo el tiempo registrado en la tarea es imputable y todos los gastos no son imputables.

El tipo de facturación de una tarea se puede configurar en la pestaña **Tareas con cargo** de la línea de contrato actualizando el campo **Tipo de facturación** en la subcuadrícula de tareas de la línea de contrato. Alternativamente, puede actualizar el campo **Tipo de facturación** en la subcuadrícula de la tarea Configuración de facturación de un proyecto que muestra las líneas de contrato asociadas a una tarea.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizar un rol como facturable o no facturable

Un rol puede ser facturable o no facturable en una línea de contrato específica.

El tipo de facturación de un rol se puede configurar en la pestaña **Roles imputables** de una línea de contrato. Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Funciones imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizar una categoría de transacción como facturable o no facturable

Una categoría de transacción puede ser facturable o no facturable en una línea de contrato específica.

El tipo de facturación de una transacción se puede configurar en la pestaña **Categorías imputables** de una línea de contrato basada en un proyecto. Para hacer esto, actualice el campo **Tipo de facturación** en la subcuadrícula **Categorías imputables**.

### <a name="resolve-chargeability"></a>Resolver imputabilidad

Un cálculo o dato real creado para el tiempo solo se considera imputable si:

   - El **Tiempo** se incluye en la línea de contrato.
   - El **Rol** está configurado como imputable en la línea de contrato.
   - Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de contrato.
 
 Si estas tres cosas son ciertas, la tarea se configura como imputable. 

Un cálculo o dato real creado para el gasto solo se considera imputable si:

   - El **Gasto** se incluye en la línea de contrato.
   - La **Categoría de transacción** está configurada como imputable en la línea de contrato.
   - Las **Tareas incluidas** se establecen en **Tarea seleccionada** en la línea de contrato.
  
 Si estas tres cosas son ciertas, la **Tarea** se configura como imputable. 

Un cálculo o dato real creado para el material solo se considera imputable si:

   - Los **Materiales** se incluye en la línea de contrato.
   - Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de contrato.

Si estas dos cosas son ciertas, la **Tarea** se configura como imputable. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Incluye tiempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Incluye gasto</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Incluye materiales</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tareas incluidas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoría</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tarea</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impacto de imputabilidad</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>Imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos actuales: Facturable </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: <strong>No imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: <strong>No imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Solo tareas seleccionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No disponible</strong>
                </p>
                <p>
Tipo de facturación en gastos actuales: Facturable </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No disponible</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: Facturable </p>
                <p>
Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No disponible</strong>
                </p>
                <p>
Tipo de facturación en material real: Imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: Facturable </p>
                <p>
Tipo de facturación en gastos actuales: Facturable </p>
                <p>
Tipo de facturación en material real: <strong>No disponible</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Proyecto entero </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No puede estar establecido </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en gastos reales: <strong>No imputable</strong>
                </p>
                <p>
Tipo de facturación en material real: <strong>No disponible</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
