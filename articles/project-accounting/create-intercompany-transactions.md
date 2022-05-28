---
title: Crear transacciones de empresas vinculadas
description: Este tema proporciona información sobre cómo crear transacciones de empresas vinculadas.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 88e5658c9087fdb19adce1c23bc5cad0ad0fa434
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600011"
---
# <a name="create-intercompany-transactions"></a>Crear transacciones de empresas vinculadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Las transacciones de empresas vinculadas son transacciones de tiempo y gastos de un contrato de proyecto que pertenecen a una empresa o unidad organizativa, mientras que los recursos del contrato del proyecto forman parte de una empresa o unidad organizativa diferentes.

Cuando se aprueba una transacción de empresas vinculadas, se crean las siguientes transacciones reales.

| **Tipo de transacción** | **Lista de precios aplicada** | **Divisa de la transacción** |
| --- | --- | --- |
| Coste | Lista de precios de costo unitario de contratación | Moneda en la línea de precio |
| Ventas sin facturar. Estos se crean solo para los datos reales que están asociados con una línea de contrato con el tipo de facturación, el tiempo y el material. | Lista de precios de ventas de proyecto de contrato | Divisa de contrato |
| Coste de unidad de dotación de recursos | Lista de precios de coste unitario de dotación de recursos | Moneda en la línea de precio |
| Ventas entre unidades organizativas | Lista de precios de costo unitario de contratación | Moneda en la línea de precio |

El coste, el coste unitario de recursos, y los precios y la moneda de las transacciones de ventas entre unidades organizativas están determinadas por la **unidad organizativa**. Es importante recordar esto al decidir cómo estructurar empresas y unidades organizativas en su implementación.

Al crear registros de oportunidades, ofertas, contratos de proyectos y proyectos, el sistema comprueba que la moneda de la unidad contratante coincida con la moneda contable de la empresa contratante. Cuando no son los mismos, no se pueden crear estos registros. Para definir la moneda de la unidad organizativa en Dynamics 365 Project Operations, vaya a **Dataverse** > **Configuraciones** > **Unidades organizativas**. La divisa contable de una empresa se define en Dynamics 365 Finance yendo a **Contabilidad general** > **Configuración de contabilidad general** > **Contabilidad general**. La moneda está sincronizada con su entorno de Dataverse utilizando el mapa de escritura dual de libros mayores.

El sistema crea costes unitarios de recursos y datos reales de ventas entre unidades organizativas en las siguientes situaciones:

  - Cuando la unidad de recursos difiere de la unidad de contratación
  - Cuando la empresa de recursos difiere de la empresa de contratación

Sin embargo, solo las transacciones que tengan una empresa de recursos distinta a la de la empresa contratante se transferirán al entorno de Dynamics 365 Finance para una contabilidad adicional.

La contabilidad de datos reales de proyecto se registra en el diario de integración de Project Operations en Finance. El sistema crea las siguientes líneas de diario.

| **Tipo de transacción** | **Entidad jurídica** | **Crea la transacción del proyecto al realizar el registro** | **Valor predeterminado de dimensiones financieras desde** | **Grupo de impuestos de ventas de facturación y grupo de impuestos de ventas de artículos de facturación predeterminados** |
| --- | --- | --- | --- | --- |
| Coste | No se agrega al diario de integración | N/D | N/D | N/D |
| Ventas sin facturar | El diario de integración de la entidad jurídica prestataria | Sí | Project | **Grupo de impuestos sobre las ventas de facturación**: basado en el **cliente del contrato** <br/> **Grupo de impuestos sobre las ventas de artículos de facturación**: de la categoría de proyecto de entidad jurídica actual en la línea del diario |
| Coste de unidad de dotación de recursos | Diario de integración de la entidad jurídica prestataria | No | Cliente de empresas vinculadas | **Grupo de impuestos sobre las ventas de facturación**: basado en el **cliente de empresas vinculadas** <br/> **Grupo de impuestos sobre las ventas de artículos de facturación**: de la categoría de proyecto de entidad jurídica actual en la línea del diario |
| Ventas entre organizaciones | Diario de integración de la entidad jurídica prestataria | No | Cliente de empresas vinculadas | **Grupo de impuestos sobre las ventas de facturación**: basado en el **cliente de empresas vinculadas** <br/> **Grupo de impuestos sobre las ventas de artículos de facturación**: de la categoría de proyecto de entidad jurídica actual en la línea del diario |

### <a name="example-intercompany-transactions"></a>Ejemplo: Transacciones de empresas vinculadas

Molly Clark, desarrolladora empleada en GBPM, registra 10 horas de trabajo en un proyecto de USPM Adventure Works, aprobado por el jefe de proyecto. El coste del desarrollador en GBPM es de 88 GBP por hora. GBPM facturará a USPM 120 USD por hora de desarrollador. USPM facturará al cliente Adventure Works, 200 USD por el trabajo realizado por el recurso de GBPM. Para obtener más información, consulte [Configurar la facturación con empresas vinculadas](configure-intercompany-invoicing.md).

1. En Project Operations, vaya a **Recursos** y seleccione **Molly Clark** en la lista. En la pestaña **Programación**, en el campo **Emprea**, seleccione **GBPM**.
2. Vaya a **Ventas** > **Clientes** y seleccione **Nuevo** para crear un nuevo registro de cliente para Adventure Works.
    1. Establezca la empresa en **USPM**.
    2. Establezca **Tipo de relación** en **Cliente**.
    3. Seleccione **Grupo de clientes 10 - Nacional**.
    4. Establezca la divisa en **USD**.
    5. Guarde el registro.
3. Vaya a **Ventas** > **Contratos de proyecto** y cree un nuevo contrato de proyecto para Adventure Works.
    1. Establezca la empresa propietaria en **USPM** y la unidad contratante en **Contoso Robotics US**.
    2. Seleccione Adventure Works como cliente.
    3. Seleccione una lista de precios de productos y guarde el registro.
    4. En la pestaña **Líneas de contrato**, cree una nueva línea de contrato. Establezca cualquier nombre y seleccione **Tiempo y materiales** como método de facturación.
    5. Cree un nuevo proyecto y asócielo a esta línea de contrato.
4. Inicie sesión como el recurso, **Molly Clark**. Vaya a **Proyectos** > **Entradas de tiempo** y cree una entrada de tiempo para el proyecto de Adventure Works.
5. Inicie sesión como jefe de proyecto. Vaya a **Proyectos** > **Aprobaciones** y apruebe la transacción de entrada de tiempo registrada por María Carrero.
6. Navegue hasta el proyecto de Adventure Works y seleccione **Relacionado** > **Datos reales**. Se crean las siguientes transacciones de datos reales.

| **Tipo de transacción** | **Precio** | **Divisa de la transacción** | **Importe** |
| --- | --- | --- | --- |
| Coste | 120 | USD | 1200 |
| Ventas sin facturar | 200 | USD | 2000 |
| Coste de unidad de dotación de recursos | 88 | GBP | 880 |
| Ventas entre unidades organizativas | 120 | USD | 1200 |

7. Inicie sesión como contable de USPM. Abra la instancia de Finance de Project Operations y seleccione la empresa **USPM**. 
8. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Project Operations en Customer Engagement** > **Importar desde la puesta en escena** y seleccione para ejecutar el proceso periódico. Este proceso periódico llenará el diario de integración de Project Operations.
9. Vaya a **Gestión de proyectos y contabilidad** > **Diarios** > **Diario de integración de Project Operations** y revise las líneas de diario. El sistema crea la siguiente línea.

    | **Tipo de transacción** | **Precio** | **Divisa de la transacción** | **Importe** |
    | --- | --- | --- | --- |
    | Ventas sin facturar | 200 | USD | 2000 |

    Si el sistema está configurado para acumular ingresos para este proyecto, se registra lo siguiente:

    - Débito: Proyecto - Valor de ventas de trabajo en proceso 200 USD
    - Crédito: Proyecto - Ingresos acumulados 200 USD

    Esta venta sin facturar ya está lista para su facturación. La factura del cliente Adventure Works se puede registrar financieramente cuando sea necesario.

10. Inicie sesión como contable de **GBPM**. Abra la instancia de Finance de Project Operations y abra la empresa, **GBPM**. 
11. Vaya a **Administración y contabilidad de proyectos** > **Periódicos** > **Integración de Project Operations** > **Importar desde tabla de almacenamiento provisional** y ejecute el proceso periódico para completar el diario de Integración de Project Operations.
12. Vaya a **Gestión de proyectos y contabilidad** > **Diarios** > **Diario de integración de Project Operations** y revise las líneas. El sistema crea las siguientes líneas.

    | **Tipo de transacción** | **Precio** | **Divisa de la transacción** | **Importe** |
    | --- | --- | --- | --- |
    | Coste de unidad de dotación de recursos | 88 | GBP | 880 |
    | Ventas entre unidades organizativas | 120 | USD | 1200 |

    El registro de estos registros genera las siguientes transacciones de asientos:

    - Débito: coste del proyecto 88 GBP
    - Crédito: asignación de nómina 88 GBP

    Si el sistema está configurado para acumular ingresos de empresas vinculadas, se registra lo siguiente:

    - Débito: Proyecto - Valor de ventas de trabajo en proceso 120 USD
    - Crédito: Proyecto - Ingresos acumulados 120 USD

    El sistema ahora está listo para crear una factura de cliente de empresas vinculadas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
