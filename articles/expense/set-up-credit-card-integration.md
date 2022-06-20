---
title: Configurar la integración de tarjetas de crédito
description: En este artículo se explica cómo trabajar con transacciones de tarjeta de crédito relacionadas con los gastos.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924516"
---
# <a name="set-up-credit-card-integration"></a>Configurar la integración de tarjetas de crédito

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Las transacciones con tarjeta de crédito relacionadas con gastos se pueden configurar para que se importen automáticamente en un programa periódico. Como alternativa, las transacciones se pueden importar manualmente según sea necesario. Las transacciones con tarjeta de crédito se importan a través de la entidad de datos de transacciones con tarjeta de crédito.

## <a name="import-credit-card-transactions"></a>Importar transacciones con tarjeta de crédito

Para importar transacciones con tarjeta de crédito, siga estos pasos:

1. En la página **Transacciones con tarjeta de crédito**, seleccione **Importar transacciones**. Si abre la administración de datos por primera vez, el sistema deberá actualizar la lista de entidades de datos para que pueda continuar.
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

A veces, después de que se importan las transacciones con tarjeta de crédito, es posible que sea necesario eliminar ciertas transacciones. Esto podría deberse a que las transacciones están duplicadas o porque los datos no son precisos. Los administradores pueden usar la característica **"Eliminar transacciones con tarjeta de crédito"** para seleccionar y eliminar transacciones con tarjeta de crédito que **no estén asociada** a un informe de gastos. 

1. Vaya a **Tareas periódicas** > **Eliminar transacciones con tarjeta de crédito**.
2. Seleccione **Filtro** y proporcione información para identificar los registros que se incluirán.
3. Seleccione **Aceptar** para eliminar los registros. 

## <a name="storing-credit-card-numbers"></a>Almacenar números de tarjetas de crédito

Hay tres opciones disponibles para almacenar números de tarjetas de crédito. Los números de tarjetas de crédito se almacenan en la página **Parámetros de gestión de gastos**.

- **Evitar la entrada del número de tarjeta** - Los números de tarjetas de crédito no se almacenan.
- **Números de tarjetas hash (almacenar los últimos cuatro dígitos)** - Los últimos cuatro dígitos de los números de las tarjetas de crédito se almacenan en formato cifrado.
- **Almacenar números de tarjetas** - Los números de tarjetas de crédito se almacenan en un formato no cifrado. Esta opción no cumple con el Estándar de seguridad de datos (DSS) de la industria de tarjetas de pago (PCI). Por lo tanto, para que su organización cumpla con las regulaciones PCI DSS, los administradores de la organización deben optar por no almacenar los números de las tarjetas de crédito o por almacenar los números de las tarjetas hash.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
