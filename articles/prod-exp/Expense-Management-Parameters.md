---
title: Parámetros de administración de gastos
description: Los siguientes parámetros controlan el comportamiento en la gestión de gastos.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 454d3f6feb46b28762a6a1249df2336f1aa5e91a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960403"
---
# <a name="expense-management-parameters"></a>Parámetros de administración de gastos


Los siguientes parámetros controlan el comportamiento general en la gestión de gastos.

### <a name="general"></a>General

| **Campo**                                                | **Descripción**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Tasa estándar de kilometraje**                             | Introduzca la tasa de reembolso por gastos de kilometraje. La tarifa se multiplicará por el kilometraje que se ingresa para el gasto, para calcular el importe a reembolsar por el gasto de viaje.                       |
|**Gastos personales pagados por**                             | Seleccione quién es responsable de pagar los importes de las transacciones con tarjeta de crédito que se clasifican como personales.                                                                                                     |
|**Mostrar el informe de gastos completo en desglose**               | Seleccione esta opción para mostrar todos los gastos de un informe de gastos cuando se visualizan los detalles del documento original para un comprobante específico que se generó cuando se registró el informe de gastos.              |
|**La preautorización de viaje es obligatoria**                 | Seleccione esta opción para solicitar que se envíe y apruebe una solicitud de viaje antes de que un empleado pueda enviar un informe de gastos.                                                                    |
|**Permitir la edición de distribuciones antes de registrar**            | Seleccione si las distribuciones de un informe de gastos se pueden editar antes de publicarse.                                                                                                                 |
|**Evaluar las políticas de gestión de gastos**                     | Seleccione cuándo se evalúan los gastos para determinar si se ha infringido una directiva de gastos. Los gastos se pueden evaluar para detectar infracciones cuando se ingresa y guarda la entrada de gastos, o cuando el gasto se envía para aprobación. Las reglas de directiva para los recibos necesarios se evaluarán cuando se guarde la línea de gastos.                   |
|**Permitir líneas de gastos de empresas vinculadas**                         | Seleccione permite la entrada de los gastos de otras entidades legales dentro de un informe de gastos.                                                                                                          |
|**Permitir editar el tipo de cambio para gastos de tarjetas de crédito** | Seleccione esta opción para permitir al usuario editar el tipo de cambio para los gastos de tarjetas de crédito importadas.                                                                        |
|**Campos de jerarquía de varios niveles para mostrar**                  | Seleccione los campos de aprobador que se muestran cuando el tipo de asignación de flujo de trabajo del informe de gastos se establece para ser una jerarquía y la selección de jerarquía está configurada para utilizar la jerarquía de aprobación de gastos de varios niveles. Cuando se utiliza la jerarquía de aprobación de varios niveles para un flujo de trabajo, los campos seleccionados se mostrarán y podrán editar en el informe de gastos. |
|**Ingrese el número de tarjeta de crédito del empleado (actualización de julio de 2017)**     | Seleccione si se puede ingresar y guardar un número de 15 o 16 caracteres en el campo **Id. de tarjeta** en la página **Tarjetas de crédito** de un empleado.                                                                          |

### <a name="financial"></a>Actividades financieras

| **Campo**                                                            | **Descripción**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nombre del diario del libro mayor**                                         | Seleccione el nombre del diario contable en el que se registran los informes de gastos aprobados.            |
|**Habilitar la recuperación de impuestos de los gastos**                                  | Seleccione esta opción para habilitar la recuperación de impuestos sobre gastos para gastos aptos para ello. Esta opción no se puede habilitar si están habilitadas las reglas de impuestos sobre las ventas y sobre el uso de EE. UU.      |
|**Registrar inmediatamente los anticipos en efectivo**                                     | Seleccione esta opción para registrar un anticipo en efectivo aprobado cuando se complete el proceso de pago y transferencia. Si esta opción no está seleccionada, el proceso de Pago y transferencia generará un diario general no contabilizado. |
|**Fecha contable correcta durante el registro**                             | Seleccione esta opción para actualizar la fecha contable cuando se registran los gastos, si el período actual está en espera o cerrado. La fecha contable se establecerá en el próximo período abierto.   |
|**Permitir la agrupación de transacciones según la cuenta de compensación especificada en el método de pago**      | Seleccione esta opción para resumir las transacciones de gastos para un informe de gastos, según la cuenta de compensación que se especifica en el método de pago para los gastos.   
|**Impuesto incluido**                                                   | Seleccione esta opción para incluir el impuesto sobre las ventas en el importe del gasto de forma predeterminada.             |
|**Liberar gravámenes al cerrar solicitudes de viaje**            | Seleccione esta opción para liberar los fondos gravados cuando se cierre una solicitud de viaje aprobada.                                                                                   |
|**Permitir que la solicitud de viaje se envíe con un presupuesto excedido para el registro presupuestario y el presupuesto del proyecto** | Seleccione esta opción para permitir que los empleados envíen solicitudes de viaje para su aprobación que excedan el presupuesto permitido que se establece en el registro de presupuestos o el presupuesto permitido para un proyecto.            |
|**Permitir el envío de informe de gastos con un presupuesto excedido para el registro presupuestario y el presupuesto del proyecto**    | Seleccione esta opción para permitir que los empleados envíen informes de gastos para su aprobación, que excedan el presupuesto permitido que se establece en el registro de presupuestos o el presupuesto permitido para un proyecto.                |
|**Permitir la aprobación de informes de gastos con un presupuesto excedido solo para registro presupuestario**                | Seleccione esta opción para permitir que los aprobadores aprueben informes de gastos que excedan el presupuesto permitido que se establece en el registro presupuestario.                                                                       |

### <a name="per-diem"></a>Dietas

| **Campo**                             | **Descripción**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Horas mínimas por dietas**           | Introduzca el número mínimo predeterminado de horas que un empleado debe trabajar en un día para poder optar a recibir dietas para gastos relacionados con viajes.  Este valor se utiliza solo como valor predeterminado para el campo Horas mínimas para los niveles de tarifas de dietas.                                                                                      |
|**Porcentaje de comida**                          | Introduzca el porcentaje predeterminado de dietas para comidas que se utiliza en el primer y último día del gasto relacionado con el viaje cuando el campo **Calcular reducción de comida mediante** se establece en **Tipo de comida por día** o **Número de comidas por día**. La jornada laboral del primer y último día puede ser más corta que una jornada laboral estándar. Por lo tanto, la cantidad de dietas de esos días puede diferir de la cantidad estándar. Si el porcentaje se establece en 0, las deducciones del primer y último día serán de 0,00. |
|**Porcentaje del hotel**                        | Introduzca el porcentaje predeterminado de dietas para hoteles que se usan en el primer y último día del gasto relacionado con el viaje. La jornada laboral del primer y último día puede ser más corta que una jornada laboral estándar. Por lo tanto, la cantidad de dietas de esos días puede diferir de la cantidad estándar. Si el porcentaje se establece en 0, las deducciones del primer y último día serán de 0,00.                                              |
|**Otro porcentaje**                        | Introduzca el porcentaje predeterminado de dietas para gastos diversos que se usan en el primer y último día del gasto relacionado con el viaje. La jornada laboral del primer y último día puede ser más corta que una jornada laboral estándar. Por lo tanto, la cantidad de dietas de esos días puede diferir de la cantidad estándar. Si el porcentaje se establece en 0, las deducciones del primer y último día serán de 0,00.                                                                                                     |
|**Reducción de porcentaje para desayuno** | Ingrese la cantidad en que se reducen las dietas para el desayuno. Por ejemplo, si un empleado recibe un desayuno gratuito, es posible que desee reducir la cantidad de dietas en un 10 por ciento.                               |
|**Reducción de porcentaje para comida**    | Ingrese la cantidad en que se reducen las dietas para la comida. Por ejemplo, si un empleado recibe una comida gratuita, es posible que desee reducir la cantidad de dietas en un 15 por ciento.                                       |
|**Reducción de porcentaje para cena**   | Ingrese la cantidad en que se reducen las dietas para la cena. Por ejemplo, si un empleado recibe una cena gratuita, es posible que desee reducir la cantidad de dietas en un 25 por ciento.                                     |
|**Calcular la reducción de comida mediante**         | Seleccione cómo debe calcular el sistema la reducción de dietas de comida, seleccionando si la reducción se basa en el tipo de comida por viaje o por día, o si la reducción se basa en la cantidad de comidas permitidas por día.|
|**Redondeo de dietas**                  | Seleccione el tipo de redondeo que se utiliza para los gastos de dietas. Si selecciona el redondeo normal, cualquier gasto de dieta que tenga un monto de 0,50 se redondea a 1,00 y cualquier gasto de dieta que tenga un importe inferior a 0,50 se redondea a 0,00.                                                                                              |
|**Cálculo de dietas en base a**         | Seleccione si la cantidad de dietas se basa en días naturales o períodos de 24 horas.       |

### <a name="fax-cover-pages"></a>Portadas de fax

| **Campo**                      | **Descripción**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instrucciones**                   | Introduzca las instrucciones que los empleados deben seguir cuando crean una portada para un fax que se utiliza para enviar recibos relacionados con un informe de gastos. Pulse el botón **Traducciones** para introducir texto específico del idioma que se mostrará, según el idioma del usuario. |
|**Id. de usuario (información de código de barras)** | Seleccione esta opción para almacenar el identificador único de un empleado en el código de barras que se utiliza en la portada del fax.                 |
|**Código de barras**                      | Seleccione el código de barras que se utiliza en la portada del fax. Los códigos de barras 39 y 128 son compatibles con la gestión de gastos.               |

### <a name="anti-corruption"></a>Anticorrupcion

|                 <strong>Campo</strong>                 |                                                                                                                                                                                            <strong>Descripción</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Mostrar declaración anticorrupción</strong>  | Seleccione esta opción para mostrar el texto anticorrupción cuando se crea un informe de gastos. Luego, se pueden habilitar categorías de gastos específicas que requerirán que se seleccione la declaración anticorrupción en el informe de gastos. Por ejemplo, una categoría de obsequio relacionada con un gasto de funcionario público puede requerir que el empleado confirme que el gasto cumple con la política de la empresa relacionada con funcionarios gubernamentales. |
| <strong>Mensaje anticorrupción para el remitente</strong> |                                                                                             Ingrese el texto que se le mostrará al empleado cuando cree un nuevo informe de gastos. Pulse el botón <strong>Traducciones</strong> para introducir texto específico del idioma que se mostrará, según el idioma del usuario.                                                                                             |
| <strong>Mensaje anticorrupción para el aprobador</strong>  |                                                                                             Ingrese el texto que se le mostrará al aprobador cuando cree un nuevo informe de gastos. Pulse el botón <strong>Traducciones</strong> para introducir texto específico del idioma que se mostrará, según el idioma del usuario.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]