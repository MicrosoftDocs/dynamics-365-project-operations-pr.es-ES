---
title: Configurar la contabilidad para proyectos facturables
description: Este tema proporciona información sobre las opciones de contabilidad para proyectos facturables.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 32031742b1a9580b9ebdbaf6952a998733be5e8f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896166"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurar la contabilidad para proyectos facturables

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Dynamics 365 Project Operations admite diversas opciones de contabilidad para proyectos facturables que incluyen transacciones de tiempo y material y precio fijo.

- **Transacciones de tiempo y material**: estas transacciones se facturan a medida que avanza el trabajo en función del consumo de horas, gastos, elementos o tarifas del proyecto. Estos costes de transacción se pueden confrontar con los ingresos de cada transacción y el proyecto se factura a medida que avanza el trabajo. Los ingresos del proyecto también se pueden acumular en el momento en que se produce la transacción. Durante la facturación, se reconocen los ingresos y, si corresponde, se revierten los ingresos acumulados.
- **Transacciones de precio fijo**: estas transacciones se facturan de acuerdo con un programa de facturación que se basa en un contrato de proyecto. Los ingresos por transacciones de precio fijo pueden reconocerse en la facturación o calcularse y contabilizarse periódicamente, de acuerdo con los métodos **Contrato completado** o **Porcentaje completado**.

Un proyecto se considera facturable cuando está asociado con una o más líneas de contrato. Una línea de contrato de proyecto define por sí misma qué método de facturación y tipos de transacciones están permitidos.

Como ejemplo, Fabrikam Robotics ha ganado un contrato de proyecto con Adatum Corporation para la optimización de equipos. Adatum pagará una cantidad fija de $10.000 USD para cubrir los gastos incurridos en el proyecto. Este es un método de facturación de precio fijo. El tiempo del proyecto y las tarifas se facturarán por uso. Este es un método de facturación por tiempo y material. Todo el trabajo se seguirá bajo un solo proyecto llamado Optimización de equipos Adatum.

Un miembro del equipo del proyecto presenta ocho horas de trabajo en el proyecto Optimización de equipos Adatum. Cuando el administrador del proyecto aprueba este tiempo, el sistema utiliza el método de facturación de tiempo y material para crear transacciones reales, una factura y una cuenta. Esta transacción no se incluirá en el cálculo de la estimación de ingresos de precio fijo.

Otro miembro del equipo del proyecto presenta un gasto de viaje de $2.000,00 USD contra el proyecto Optimización de equipos Adatum. Cuando el administrador del proyecto aprueba este envío, el sistema utiliza el método de facturación de precio fijo para crear transacciones reales y una cuenta para este gasto de proyecto. No se facturará al cliente en función de esta transacción. En su lugar, se facturará utilizando hitos de facturación configurados por separado. Esta transacción de gastos, junto con las estimaciones de gastos, se incluirán en el cálculo de la estimación de ingresos de precio fijo.

Los principios contables para las transacciones del proyecto se definen en los perfiles de costes e ingresos del proyecto. Para cada transacción del proyecto, el sistema determina el perfil de costes e ingresos del proyecto adecuado mediante el uso de las reglas del perfil de costes e ingresos del proyecto que se han configurado.

## <a name="define-project-cost-and-revenue-profiles"></a>Definir los perfiles de costes e ingresos del proyecto 

Los perfiles de costes e ingresos del proyecto determinan las reglas contables de las transacciones del proyecto. Estos perfiles se configuran en Gestión de proyectos y contabilidad. 

Complete los siguientes pasos para crear un nuevo perfil de costes e ingresos del proyecto. 

1. Vaya a **Gestión de proyectos y contabilidad** > **Preparar** > **Contabilidad** > **Perfiles de costes e ingresos del proyecto**. 
2. Seleccione **Nuevo** para crear un nuevo perfil de costes e ingresos del proyecto.
3. En el campo **Nombre**, introduzca el nombre y una breve descripción del perfil.
4. En el campo **Método de facturación**, seleccione **Tiempo y material** o **Precio fijo**.
5. Expanda la ficha desplegable **Libro mayor**. Los campos de esta pestaña definen los principios contables que se utilizan cuando las transacciones del proyecto se registran en el diario de integración de Operaciones del proyecto y luego se facturan mediante la propuesta de factura del proyecto.
6. Seleccione la información adecuada en los siguientes campos de la ficha desplegable **Libro mayor**:

    - **Costes de registro, hora**:

       - *Sin libro mayor*: el coste de las transacciones de tiempo no se contabilizará en el Libro mayor cuando se registre el diario de integración de Operaciones del proyecto. Sin embargo, el contable puede registrar costes utilizando la función Registrar costes en un momento posterior.
       - **Saldo**: el coste de las transacciones de tiempo se cargará al tipo de cuenta del Libro mayor, *WIP: valor de costo* y se abonará a la *Cuenta de asignación de nómina* en la configuración de registro del Libro mayor. El contable utilizará la función Registrar costes para mover este coste de una cuenta de saldo a una cuenta de pérdidas y ganancias de forma periódica.
       - **Pérdidas y ganancias**: al registrar el diario de integración de Operaciones del proyecto, el coste de la transacción de tiempo se cargará al tipo de cuenta del Libro mayor *Coste*, y se abonará a la *Cuenta de asignación de nómina* definida en la pestaña **Coste** de la página **Configuración de registro contable** (**Gestión de proyectos y contabilidad** \> **Configuración** \> **Registro** \> **Configuración de registro contable**). Esta es la configuración más común para transacciones de tiempo y material.
        - *Nunca al Libro mayor*: el coste de las transacciones de tiempo nunca se contabilizará en el Libro mayor.

    - **Registro de costes, gasto**:

         - **Saldo**: al registrar el diario de integración de Operaciones del proyecto, el coste de la transacción de gastos se cargará en el tipo de cuenta del Libro mayor *WIP: valor de coste* como se define en la pestaña **Coste** de la página **Configuración de registro contable** y se abona en la cuenta de compensación en la línea del diario. Las cuentas de compensación predeterminadas para gastos se definen en **Gestión de proyectos y contabilidad** > **Configuración** \> **Registro** \> **Cuenta de compensación predeterminada para gastos**. El contable utilizará la función **Registrar costes** para mover este coste desde la cuenta de saldo a la cuenta de pérdidas y ganancias de forma periódica.
        - **Pérdidas y ganancias**: al registrar el diario de integración de Operaciones del proyecto, el coste de la transacción de gastos se cargará en el tipo de cuenta del Libro mayor *WIP: valor de coste* como se define en la pestaña **Coste** de la página **Configuración de registro contable** y se abona en la cuenta de compensación en la línea del diario. Las cuentas de compensación predeterminadas para gastos se definen en **Gestión de proyectos y contabilidad** \> **Configuración** \> **Registro** \> **Cuenta de compensación predeterminada para gastos**.
       
    - **Facturación en cuenta**:

        - **Saldo**: al publicar la propuesta de factura del proyecto, se abonará una transacción en cuenta (hito de facturación) en el tipo de cuenta de Libro mayor *WIP facturado, en cuenta* como se define en la pestaña **Ingresos** de la página **Configuración de registro contable** y se carga en la cuenta de saldo del cliente.
         - **Pérdidas y ganancias**: al publicar la propuesta de factura del proyecto, se abonará una transacción en cuenta (hito de facturación) en el tipo de cuenta de Libro mayor *Ingreso facturado, en cuenta* como se define en la pestaña **Ingresos** de la página **Configuración de registro contable** y se carga en la cuenta de saldo del cliente. Las cuentas de saldo de clientes se definen en **Clientes** \> **Configuración** \> **Perfiles de registro de clientes**.

   Cuando define los perfiles de contabilización para los métodos de facturación de tiempo y material, tiene la opción de acumular ingresos por tipo de transacción (hora, gasto y tarifa). Si la opción **Acumular ingresos** está configurada en **Sí**, las transacciones de ventas no facturadas del diario de Integración de Operaciones del Proyecto se registrarán en el libro mayor. El valor de las ventas se carga a **WIP: cuenta de valor de ventas** y se abona a la cuenta **Ingresos acumulados: valor de ventas** que se configuró en la página **Configuración de registro contable**, en la pestaña **Ingresos**. 
  
  > [!NOTE]
  > La opción **Acumular ingresos** está disponible solo cuando el tipo de transacción respectivo **Coste** se contabiliza en la cuenta de pérdidas y ganancias.
    
7. Expanda la ficha desplegable **Estimación**. Los campos de esta pestaña definen la configuración de cálculo para estimaciones de ingresos de precio fijo. Los campos de esta pestaña solo se aplican a los perfiles de costes e ingresos del proyecto con un método de facturación de **Precio fijo**.
8. Seleccione la información adecuada en los siguientes campos de la ficha desplegable **Estimación**:

    - **Principio utilizado para los cálculos de finalización de proyectos**:

        - **Contrato completado**: La confrontación de costes y el reconocimiento de ingresos no ocurren hasta el final del proyecto. Los costes se reflejan como WIP en el saldo hasta que se complete el proyecto.
        - **Porcentaje completado**: los ingresos acumulados se calculan y se registran en el libro mayor cada período en función del porcentaje de finalización del proyecto. Hay varios métodos disponibles para calcular el porcentaje de finalización. Estos métodos pueden ser automáticos, según la configuración, o manuales.
        - **Sin WIP**: esta configuración se utiliza para proyectos de precio fijo con un período de tiempo corto y donde la factura y los costes ocurren en el mismo período. En este caso, el valor de campo **Facturación en cuenta** de la ficha desplegable **Libro mayor** se establece automáticamente en **Pérdidas y ganancias** para asegurar que los ingresos se reconozcan en la facturación. El proceso de estimación de ingresos no se utilizará para este perfil de costes e ingresos del proyecto.

    - **Principio de coincidencia**: este campo determina cómo se contabilizará el valor de ventas calculado (ingresos acumulados) en el libro mayor.

        - Utilizando el principio **Valor de ventas**, el sistema calculará el valor de las ventas haciendo coincidir los costes y los ingresos y luego los contabilizará como una sola cantidad.
        - Utilizando el principio **Producción y beneficio**, el sistema dividirá el valor de las ventas en costes incurridos y ganancias calculadas. Estos se registran por separado.

    - **Plantillas de costes**: permite que las transacciones del proyecto se agrupen según el tipo de transacción y la categoría del proyecto y define las reglas de cálculo del porcentaje de finalización para estos grupos.
    - **Códigos de período**: define la frecuencia con la que se calculan las estimaciones de ingresos para un perfil de ingresos y costes de proyecto determinado.
    - **Categorías para estimación**: se utiliza para la contabilización del valor de las ventas (ingresos acumulados) en las transacciones del proyecto. Primero, configure la categoría de proyecto dedicada para un tipo de transacción **Tarifa** y luego establecer el indicador **Estimar** para esta categoría de proyecto. A continuación, según el principio de coincidencia seleccionado, elija esta categoría de proyecto en el valor **Ventas** o el campo **Beneficio** del perfil de costes e ingresos del proyecto.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Configuraciones de muestra para perfiles de costes e ingresos del proyecto

Tiempo y materiales: no WIP

![Perfil de costes e ingresos, tiempo y materiales: sin WIP](media/time-material-no-wip.png)

Tiempo y materiales: WIP (ingresos)

![Perfil de costes e ingresos, tiempo y materiales: WIP](media/time-material-with-wip.png)

Precio fijo: sin WIP

![Perfil de costes e ingresos, precio fijo: sin WIP](media/fixed-price-no-wip.png)

Precio fijo: contrato completado

![Perfil de costes e ingresos, precio fijo: contrato completado](media/fixed-price-completed-contract.png)

Precio fijo: porcentaje completado

![Perfil de costes e ingresos, precio fijo: porcentaje completado](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Ejemplos de eventos contables de perfiles de costes e ingresos del proyecto de muestra.

| Evento contable                  | Tiempo y material: sin WIP                       | Tiempo y material: WIP                                                                                           | Precio fijo: sin WIP                                            | Precio fijo: contrato completado                                                                            | Precio fijo: porcentaje completado                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Registro de transacciones de tiempo    | Cargo: costo <br>Crédito: asignación de nómina          | Cargo: coste <br>Crédito: asignación de nómina <br>Débito: valor de ventas WIP <br>Crédito: valor de ventas de ingresos acumulados                | Cargo: costo <br>Crédito: asignación de nómina                         | Cargo: costo <br>Crédito: asignación de nómina                                                                    | Cargo: costo <br>Crédito: asignación de nómina                       |
| Registro de transacciones de gastos | Cargo: costo <br>Crédito: cuenta de compensación por gastos | Cargo: costo <br>Crédito: cuenta de compensación por gastos <br>Cargo: valor de ventas WIP <br>Crédito: valor de ventas de ingresos acumulados      | Cargo: coste <br>Crédito: cuenta de compensación por gastos                 | Cargo: costo<br> Crédito: cuenta de compensación por gastos                                                            | Cargo: costo <br>Crédito: cuenta de compensación por gastos               |
| Cliente de facturación                | Débito: saldo del cliente <br>Crédito: ingresos facturados | Cargo: saldo del cliente <br>Crédito: ingresos facturados <br>Crédito, cargo de valor de ventas WIP, valor de ventas de ingresos acumulados | Cargo: saldo del cliente <br>Crédito, ingresos facturados, en cuenta | Débito: saldo del cliente <br>Crédito, WIP, facturado en cuenta                                                  | Cargo: saldo del cliente <br>Crédito, WIP, facturado en cuenta    |
| Estimación de registro de ingresos             | No aplicable                                   | No aplicable                                                                                                    | No aplicable                                                  | Cargo: valor de coste WIP <br>Crédito: coste                                                                         | Cargo, WIP, valor de ventas <br>Crédito: valor de ventas de ingresos acumulados |
| Eliminar                         | No aplicable                                   | No aplicable                                                                                                    | No aplicable                                                  | Cargo: valor de coste WIP <br>Cargo: costo <br>Crédito, ingresos acumulados, valor de ventas <br>Cargo, WIP, facturado en cuenta | Cargo, WIP, facturado en cuenta <br>Cargo: valor de ventas WIP     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurar las reglas de perfiles de costes e ingresos del proyecto

Las reglas del perfil de costes e ingresos del proyecto determinan el perfil de costes e ingresos del proyecto que se debe utilizar al procesar cualquier transacción facturable del proyecto. Defina las reglas yendo a **Gestión de proyectos y contabilidad** \> **Configuración** \> **Registro** \> **Reglas de perfil de costes e ingresos del proyecto**.

Las reglas se pueden definir por contrato de proyecto, grupo de proyecto o para un proyecto específico. El sistema siempre elegirá primero la regla de granularidad más alta.
