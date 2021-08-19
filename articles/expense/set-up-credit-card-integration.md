---
title: Configurar la integración de tarjetas de crédito
description: Este tema explica cómo trabajar con transacciones de tarjetas de crédito relacionadas con gastos.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996232"
---
# <a name="set-up-credit-card-integration"></a>Configurar la integración de tarjetas de crédito

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico. Como alternativa, las transacciones se pueden importar manualmente según sea necesario. Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.

## <a name="import-credit-card-transactions"></a>Importar transacciones con tarjeta de crédito

Para importar transacciones con tarjeta de crédito, siga estos pasos:

1. En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**. Si abre la administración de datos por primera vez, el sistema debe actualizar la lista de entidades de datos antes de que pueda continuar.
2. En el campo **Nombre**, indique una descripción única para el trabajo de importación.
3. En el campo **Formato de datos de origen**, seleccione el formato del archivo que contiene las transacciones con tarjeta de crédito para importar.
4. Seleccione **Cargar** y luego busque y seleccione el archivo que desee importar.
5. Una vez cargado el archivo, valide la asignación del archivo de transacciones con tarjeta de crédito y las columnas de la entidad de datos de transacciones con tarjeta de crédito seleccionando el vínculo **Ver mapa** en el mosaico. Si hay errores de asignación o si debe cambiar la asignación, introduzca los cambios de asignación desde la pestaña **Visualización de asignación** o la pestaña **Detalles de la asignación**.
6. Para automatizar las transacciones con tarjeta de crédito, seleccione **Crear trabajo de datos periódico**. Luego ya podrá establecer la periodicidad que define la frecuencia con la que se deben importar las transacciones con tarjeta de crédito. Cuando haya terminado, seleccione **Aceptar**.
7. Para importar ahora el archivo seleccionado, seleccione **Importar**.
8. Si se producen errores durante la importación, puede ver el registro de ejecución o los datos de ensayo para ver los errores que debe corregir para ayudar a garantizar una importación correcta.

> [!NOTE]
> Si necesita importar más de un formato de archivo, debe crear trabajos de importación separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reasignar las transacciones con tarjeta de crédito para empleados cancelados

Una vez que se cancela un registro de empleado, la cuenta de Active Directory Domain Services (AD DS) del empleado se deshabilita. Sin embargo, es posible que haya transacciones con tarjeta de crédito activas que aún deben contabilizarse como gastos y reembolsarse. En la página **Transacciones con tarjeta de crédito**, puede reasignar al empleado para cualquier transacción con tarjeta de crédito en la que el empleado asociado haya sido rescindido.

Seleccione una o varias transacciones con tarjeta de crédito y luego seleccione **Reasignar transacciones**. A continuación, puede seleccionar otro empleado para asignarle las transacciones con tarjeta de crédito. Una vez reasignadas las transacciones con tarjeta de crédito, pueden seleccionarse para un informe de gastos y pagarse mediante el proceso habitual para el reembolso del informe de gastos.

## <a name="delete-credit-card-transactions"></a>Eliminar transacciones con tarjeta de crédito 

A veces, después de que se importan las transacciones con tarjeta de crédito, es posible que sea necesario eliminar ciertas transacciones. Esto podría deberse a que las transacciones están duplicadas o a que los datos pueden no ser precisos. Los administradores pueden usar la característica **"Eliminar transacciones con tarjeta de crédito"** para seleccionar y eliminar transacciones con tarjeta de crédito que **no estén asociada** a un informe de gastos. 

1. Vaya a **Tareas periódicas** > **Eliminar transacciones con tarjeta de crédito**.
2. Seleccione **Filtro** y proporcione información para identificar los registros que se incluirán.
3. Seleccione **Aceptar** para eliminar los registros. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
