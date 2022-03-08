---
title: Importar y mantener transacciones con tarjetas de crédito
description: En este tema se explica cómo importar y mantener transacciones con tarjeta de crédito relacionadas con gastos. Estas transacciones se pueden configurar para que se importen automáticamente en una programación periódica, o se pueden importar manualmente según sea necesario.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c3a53d2ae4eae411364aaf68ac806b55335c75d4870a24715954ccae327f4358
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995872"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importar y mantener transacciones con tarjetas de crédito

Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico. O bien, las transacciones se pueden importar manualmente según sea necesario. Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.

Para obtener más información sobre entidades de datos, consulte [Entidades de datos](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importar transacciones con tarjeta de crédito

1. En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**. Si abre la administración de datos por primera vez, el sistema deberá actualizar la lista de entidades de datos para que pueda continuar.
2. En el campo **Nombre**, introduzca una descripción única del trabajo de importación.
3. En el campo **Formato de datos de origen**, seleccione el formato del archivo que contiene las transacciones con tarjeta de crédito que quiere importar.
4. Seleccione **Cargar** y luego busque y seleccione el archivo que desee importar.
5. Una vez cargado el archivo, valide la asignación del archivo de transacciones con tarjeta de crédito y las columnas de la entidad de datos de transacciones con tarjeta de crédito seleccionando el vínculo **Ver mapa** en el mosaico. Si hay errores de asignación o si debe cambiar la asignación, introduzca los cambios de asignación desde la pestaña **Visualización de asignación** o la pestaña **Detalles de la asignación**.
6. Para automatizar las transacciones con tarjeta de crédito, seleccione **Crear trabajo de datos periódico**. Luego ya podrá establecer la periodicidad que define la frecuencia con la que se deben importar las transacciones con tarjeta de crédito. Cuando haya terminado, seleccione **Aceptar**.
7. Para importar ahora el archivo seleccionado, seleccione **Importar**.
8. Si se producen errores durante la importación, puede ver el registro de ejecución o los datos de almacenamiento provisional para ver los errores que debe corregir para ayudar a garantizar una importación correcta.

> [!NOTE]
> Si debe importar más de un formato de archivo, debe crear trabajos de importación independientes para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reasignar las transacciones con tarjeta de crédito para empleados cancelados

Una vez que se cancela un registro de empleado, la cuenta de Active Directory Domain Services (AD DS) del empleado se deshabilita. Sin embargo, es posible que haya transacciones con tarjeta de crédito activas que aún deben contabilizarse como gastos y reembolsarse. Desde la página **Transacciones con tarjeta de crédito**, puede reasignar al empleado para cualquier transacción con tarjeta de crédito en la que se haya cancelado al empleado.

Seleccione una o varias transacciones con tarjeta de crédito y luego seleccione **Reasignar transacciones**. A continuación, puede seleccionar otro empleado para asignarle las transacciones con tarjeta de crédito. Una vez reasignadas las transacciones con tarjeta de crédito, pueden seleccionarse para un informe de gastos y pagarse mediante el proceso habitual para el reembolso del informe de gastos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]