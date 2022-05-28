---
title: Configurar los componentes facturables de una línea de cotización
description: Este tema proporciona información sobre cómo configurar componentes facturables y no facturables en una línea de presupuesto basada en proyectos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3c9bd23f4e78e3ea5ae8f74ff1a4829a11f91929
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598417"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurar los componentes facturables de una línea de oferta 

_**Se aplica a:** Implementación lite: acuerdo para factura proforma, Project Operations para escenarios basados en recursos/no mantenidos_

Una línea de contrato basada en proyectos tiene el concepto de componentes *incluidos* y componentes *facturables*.

Los componentes incluidos están sujetos a:

  - Método de facturación y divisiones de clientes
  - Límites a no exceder 
  - Configuración de frecuencia de facturación definida en la línea de oferta basada en proyecto

Un subconjunto de los componentes incluidos se puede marcar como facturable usando el campo **Tipo de facturación**. El campo **Tipo de facturación** es un conjunto de opciones que permite los siguientes valores en el contexto de una línea de oferta:

  - Imputable
  - No facturable

Los componentes facturables se pueden definir en tareas, roles y categorías de transacciones.

La facturabilidad se define en las tareas de una línea de oferta de proyecto y se aplica a todas las clases de transacciones incluidas en esa línea. Si el campo **Incluir tareas** en una línea de contrato está en blanco o configurado en **Proyecto entero**, la pestaña **Tareas facturables** no estará disponible.

La imputabilidad está definida en roles para una línea de oferta y solo se aplica a la clase de transacción **Hora**. Si el campo **Incluir tiempo** en una línea de oferta de proyecto está configurado en **No**, la pestaña **Roles facturables** no estará disponible.

La imputabilidad se define en categorías de transacción para una línea de oferta y solo se aplica a la clase de transacción **Gastos**. Si el campo **Incluir gastos** en una línea de oferta de proyecto está configurado en **No**, la pestaña **Categorías facturables** no estará disponible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualizar una tarea del proyecto para ser facturable o no facturable

Una tarea de proyecto puede ser facturable o no facturable en el contexto de una línea de cotización basada en proyecto, lo que posibilita la siguiente configuración.

Si una línea de cotización basada en un proyecto incluye **Hora** y la tarea **T1**, la tarea se asocia a la línea de cotización como facturable. Si hay una segunda línea de oferta que incluye **Gastos**, puede asociar la tarea **T1** en la línea de oferta como no facturable. El resultado es que todo el tiempo registrado en la tarea es imputable y todos los gastos registrados en la tarea no son facturables.

El tipo de facturación de una tarea se puede configurar en la pestaña **Tareas con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Tareas de la línea de oferta**. Alternativamente, puede actualizar el tipo de facturación en el campo **Tipo de facturación** de la subcuadrícula en la configuración de facturación de tareas de un proyecto que muestra las líneas de oferta asociadas a una tarea.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizar un rol para ser facturable o no facturable

Un rol puede ser facturable o no facturable en el contexto de una línea de cotización específica basada en un proyecto.

El tipo de facturación de un rol se puede configurar en la pestaña **Roles con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Roles con cargo**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizar una categoría de transacción para ser facturable o no facturable

Una categoría de transacción puede ser facturable o no facturable en una línea de oferta específica.

El tipo de facturación de una transacción se puede configurar en la pestaña **Categorías con cargo** de la línea de oferta basada en proyecto actualizando el campo **Tipo de facturación** en la subcuadrícula **Categorías con cargo**.

### <a name="resolve-chargeability"></a>Resolver imputabilidad
Un cálculo o dato real creado para el tiempo solo se considerará imputable si:

   - El **Tiempo** se incluye en la línea de cotización.
   - El **Rol** está configurado como imputable en la línea de cotización.
   - Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización. 

Si estas tres cosas son ciertas, la **Tarea** también se configura como imputable. 

Un cálculo o dato real creado para el gasto solo se considera imputable si: 

   - El **Gasto** se incluye en la línea de cotización.
   - La **Categoría de transacción** está configurada como imputable en la línea de cotización.
   - Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización.

Si estas tres cosas son ciertas, la **Tarea** también se configura como imputable. 

Un cálculo o dato real creado para el material solo se considerará imputable si:

   - Los **materiales** se incluyen en la línea de cotización.
   - Las **Tareas incluidas** se establecen en **Tareas seleccionadas** en la línea de cotización.

Si estas dos tres cosas son ciertas, la **Tarea** también deben configurarse como imputables. 


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
No se puede configurar </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: Facturable </p>
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
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturación a tiempo real: Facturable </p>
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
No se puede configurar </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No se puede configurar </p>
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
No se puede configurar </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No se puede configurar </p>
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
No se puede configurar </p>
            </td>
            <td width="65" valign="top">
                <p>
No se puede configurar </p>
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
No se puede configurar </p>
            </td>
            <td width="65" valign="top">
                <p>
No se puede configurar </p>
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
No se puede configurar </p>
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
No se puede configurar </p>
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
