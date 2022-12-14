---
title: Ajustes de proyecto
description: En este artículo se proporciona información sobre los ajustes de proyectos.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788309"
---
# <a name="project-adjustments"></a>Ajustes de proyecto

_**Se aplica a:** Project Operations para escenarios basados en existencias/producción_

## <a name="adjustments-overview"></a>Información general de los ajustes

Puede configurar Microsoft Dynamics 365 Project Operations para que los usuarios puedan realizar cambios en las transacciones publicadas. Puede ajustar las transacciones del proyecto individualmente, o puede seleccionar varias transacciones en una lista de todas las transacciones del proyecto. Los ajustes del proyecto se utilizan, por ejemplo, para actualizar en masa el estado facturable, volver a calcular el costo después de un cambio de configuración o actualizar las fuentes de financiación.

Los usuarios pueden acceder a la funcionalidad de ajuste del proyecto de varias maneras:

- Mediante el uso de la página **Ajustar transacciones** a la que se puede acceder desde **Gestión de proyectos y contabilidad** \> **Configuración**.
- Mediante el botón **Ajuste** en la página **Transacciones de proyecto registradas** a la que se puede acceder desde **Gestión de proyectos y contabilidad** \> **Transacciones**.
- Mediante el uso del botón **Ajuste** en la página **Transacciones de proyecto registradas** en el contexto de un proyecto. Se puede acceder a esta página desde **Gestión de proyectos y contabilidad** \> **Todos los proyectos**.

Para permitir ajustes, debe habilitar uno o más estados de transacción desde **Gestión de proyectos y contabilidad** \> **Gestión de proyectos y parámetros contables** en la página **Pestaña General** en la sección **Permitir ajuste del estado de la transacción**. Los ejemplos de estados de transacción incluyen transacciones registradas, transacciones facturadas o transacciones eliminadas. Cualquier estado de transacción que se establezca en **No** tendrá transacciones en ese estado que no aparecerán dentro del proceso de ajuste como seleccionables para el ajuste.

Una opción de configuración denominada **Crear siempre transacción de ajuste** está disponible actualmente en Gestión de proyectos y parámetros contables. Puede deshabilitar esta opción para actualizar la transacción original en lugar de crear nuevas transacciones durante el ajuste en un subconjunto de escenarios. Se ha anunciado que este parámetro quedará obsoleto el 1 de marzo de 2023. Después del 1 de marzo de 2023, el sistema siempre se comportará como si la opción estuviera habilitada.

## <a name="adjustments-process-flow"></a>Flujo de proceso de ajustes

Los siguientes pasos muestran el flujo típico para el procesamiento de ajustes.

1. bra la página **Ajustes del proyecto** .
2. Seleccione **Seleccionar** para buscar transacciones que cumplan con los criterios esperados para el ajuste.
3. En la lista de transacciones, seleccione todas las transacciones o un subconjunto de las transacciones para el ajuste.
4. Seleccione **Ajustar** y modifique los atributos en la línea. Como alternativa, si los valores se especificaron manualmente durante el registro de la transacción, puede optar por ingresar los valores predeterminados del sistema.
5. Se devuelve la lista de transacciones y aparece una marca de verificación en la columna **Ajuste pendiente** para indicar dónde se realizaron los cambios. Los ajustes que tienen cambios pendientes se muestran en la mitad inferior de la página. Allí, puede realizar cambios detallados adicionales además de los que se muestran en la página anterior.
6. Seleccione **Registrar** para registrar las transacciones de ajuste.

Según la configuración, normalmente se crean nuevas transacciones para el ajuste.

- El campo **Estado de ajuste** de la transacciónoriginal se actualiza a **Ajustado**.
- Se crea una transacción de reversión para revertir la transacción original y el campo **Estado** se establece en **Ajustado**.
- Se crea una nueva transacción que tiene los cambios que se realizaron durante el proceso de ajuste.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Selección de varias transacciones de proyecto registradas a la vez para ajustes y notas de crédito

Una nueva característica que se introdujo en la versión 10.0.30 permite la selección de múltiples transacciones para el ajuste a la vez desde la página **Transacciones de proyecto registradas**.

Antes de poder usar esta característica, debe estar habilitada en su sistema. Los administradores pueden usar el espacio de trabajo **Administración de características** para comprobar el estado de la característica y activarla si es necesario. En el espacio de trabajo **Gestión de características**, busque y seleccione **Transacciones de proyecto publicadas de selección múltiple para ajustes y notas de crédito** y luego seleccione **Habilitar ahora**.

Esta característica permite la siguiente funcionalidad clave:

- Se puede acceder desde la página de transacción publicada dentro de un proyecto usando el botón **Ajuste** existente.
- Habilita un control de selección de filas múltiples en la página **Transacciones de proyecto registradas**. Puede aplicar filtros a la página de lista y seleccionar sus registros antes de comenzar los ajustes.
- Deshabilita el botón **Ajuste** si no se puede ajustar una sola transacción, o si selecciona una combinación de notas de crédito y diarios juntos en lugar de individualmente.
- Debido a la adición del control de selección de varias filas, el vínculo **Costo comprometido** en la cinta ya no está deshabilitado si se seleccionan varias filas.
- Agrega el siguiente mensaje de advertencia: "Ha seleccionado más de (número seleccionado) registros para ajuste. Continuar con esta acción puede llevar algún tiempo. ¿Seguro que desea eliminar continuar con esta acción?

Esta característica también elimina el paso 2 del flujo de proceso que se describió anteriormente en este artículo. Por lo tanto, todas las transacciones que se seleccionaron antes de que se abriera la página **Ajustar transacciones** se incluirán en la lista de transacciones para ajuste. No tienes que usar el botón **Seleccionar** para buscarlos.

> [!NOTE] 
> Incluso si esta función está deshabilitada, aún puede seleccionar varios registros para el ajuste. Sin embargo, solo un registro *permanecerá seleccionado* y el cuadro de diálogo **Seleccionar transacciones** aparecerá inmediatamente después de seleccionar Ajustes abiertos.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Estados de transacción de ajuste que se pueden habilitar o deshabilitar para ajustes

Los siguientes estados se pueden habilitar o deshabilitar en la pestaña **General** de la página **Parámetros de gestión y contabilidad de proyectos**:

- Registrada
- Propuesta de factura
- Facturado
- Estimado
- Eliminado
- Saldo inicial (hora)

## <a name="adjustment-parameters"></a>Parámetros de ajuste

Estos parámetros se enumeran en la página **Parámetros de administración y contabilidad de proyectos** en la pestaña **General** en el grupo **Ajuste** y modificará el comportamiento de cómo se procesan los ajustes. 

| Nombre de parámetro | Description |
|----------------|-------------
| Crear siempre una transacción de ajuste | Si este parámetro está habilitado, el proceso de ajuste siempre creará una nueva transacción de reversión y una nueva transacción ajustada cuando haya un impacto financiero o de informes. Si el parámetro está deshabilitado, el proceso de ajuste actualizará la transacción original en lugar de crear una reversión y una nueva transacción para un escenario como una actualización del texto de la transacción. |
| Actualizar campo automáticamente | Si este parámetro está habilitado, el sistema volverá a calcular el precio de costo y el precio de venta. |
| Usar fecha de ajuste como nuevo proyecto | Este parámetro se usa para mover transacciones a un futuro período fiscal antes de que el sistema admitiera esta función. No recomendamos que lo use, porque cambia la fecha comercial de la transacción y quedará obsoleto en una versión futura. |
| Permitir actividades cerradas | Por lo general, no se pueden crear transacciones para actividades cerradas. Si este parámetro está habilitado, ese comportamiento se anula. Por lo tanto, se pueden crear ajustes para actividades cerradas. |
