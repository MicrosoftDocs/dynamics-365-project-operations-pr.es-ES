---
title: Migrar hitos de facturación totalmente facturados en la transición
description: Este artículo explica cómo migrar hitos de facturación de precio fijo que se han facturado al cliente para contratos de proyectos abiertos antes de la fecha de lanzamiento.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912261"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar hitos de facturación totalmente facturados en la transición

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

## <a name="scenario"></a>Escenario

Contoso va a actuar con Microsoft Dynamics 365 Project Operations para escenarios de recursos/sin existencias. Como parte de las actividades de transición, el equipo de implementación debe migrar los contratos de proyectos abiertos del sistema anterior. Algunos de los contratos de proyecto incluyen líneas de contrato que utilizan el método de facturación de precio fijo y ya se han facturado parcialmente al cliente final. El equipo de implementación debe migrar estos hitos de facturación como **Factura de cliente registrada**, porque deben incluirse en el valor total del contrato a efectos del reconocimiento de ingresos. Sin embargo, los saldos de clientes en Clientes y Contabilidad general no deben verse afectados.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Requisitos previos

- Debe estar instalado Dynamics 365 Finance 10.0.24 o posterior.
- El entorno donde se completarán los pasos de migración debe estar en modo de mantenimiento. No se deben realizar otras actividades mientras se migran los hitos.
- Los pasos de migración se deben seguir exactamente como se describe aquí y solo se pueden usar para la actividad de transición. Microsoft no admite ningún otro uso de esta capacidad.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Crear una versión de transición del mapa de escritura dual de hitos de línea de contrato de integración de Project Operations 

1. Asegúrese de que la asignación de destino para la entidad **Hitos de línea de contrato de integración de Project Operations** está actualizada. 

    1. En Finanzas, vaya a **Gestión de datos** \> **Entidades de datos** y seleccione la entidad **Hitos de línea de contrato de integración de Project Operations**. 
    2. Seleccione **Modificar asignación de destino**. 
    3. En la página **Asignar almacenamiento provisional al objetivo**, seleccione **Generar asignación** y luego confirme que desea generar la asignación.

2. Deténgase y actualice el mapa de doble escritura **Hitos de línea de contrato de integración de Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Vaya a **Gestión de datos** \> **Doble escritura**, seleccione el mapa y abra sus detalles. 
    2. Seleccione **Detenerse** y espere hasta que el sistema detenga la asignación. 
    3. Seleccione **Actualizar tablas**.

3. Agregue una asignación para el estado de la transacción.

    1. Seleccione **Agregar asignación**.
    2. En la nueva línea, en la columna **Aplicaciones de finanzas y operaciones**, seleccione el campo **TRANSSTATUS\[TRANSSTATUS\]**.
    3. En la columna de **Microsoft Dataverse**, seleccione **msdyn\_invoicestatus \[Estado de la factura\]**.
    4. En la columna **Tipo de asignación**, seleccione la flecha derecha (**\>**).
    5. En el cuadro de diálogo que aparece, en el campo **Dirección de sincronización**, seleccione **Dataverse a las aplicaciones de finanzas y operaciones**.
    6. Seleccione **Agregar transformación**.
    7. En el campo **Tipo de transformación**, seleccione **ValueMap**.
    8. Seleccione **Agregar asignación de valor**.
    9. En el campo izquierdo, introduzca **4**. En el campo derecho, introduzca **192350001**. 
    10. Seleccione **Guardar** y cierre el cuadro de diálogo.

4. Seleccione **Guardar como** para guardar la versión del mapa de doble escritura. 
5. En el panel **Agregar tabla**, en el campo **Editor**, seleccione **Editor predeterminado**.
6. En el campo **Versión**, introduzca la versión.
7. En el campo **Descripción**, ingrese una nota sobre esta versión de transición de la asignación. 
8. Seleccione **Guardar**.
9. Inicie la asignación.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar hitos facturados al entorno de Dataverse

1. En el entorno de Project Operations Dataverse, cree hitos que tengan un estado de factura de **Listo para facturar**. En este punto, no migre ningún hito que no haya sido facturado.

    > [!NOTE]
    > Antes de migrar los hitos de facturación, asegúrese de que las dimensiones financieras relacionadas con la línea de contrato del proyecto estén configuradas como se esperaba. Las dimensiones financieras no se pueden editar una vez completada la migración.

2. Después de migrar todos los hitos, detenga las siguientes asignaciones de doble escritura:

    - Los hitos de la línea de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)
    - Datos reales de integración de Project Operations (msdyn\_actuals)
    - Propuesta de factura de proyecto V2 (facturas)

    Para detener las asignaciones, siga estos pasos:

    1. En Finance, vaya a **Gestión de datos** \> **Doble escritura**, seleccione el mapa y abra sus detalles.
    2. Seleccione **Detenerse** y espere hasta que el sistema detenga la asignación.

3. En el entorno de Project Operations Dataverse, cree y confirme facturas proforma para los hitos de facturación. 

    1. En el mapa del sitio, vaya a los contratos del proyecto, seleccione los contratos y luego seleccione **Crear facturas**.
    2. Una vez creadas las facturas, ábralas desde el menú **Facturas** del mapa del sitio y luego seleccione **Confirmar**.

    Este paso crea los registros requeridos en el entorno de Dataverse. Sin embargo, no afecta las finanzas y las cuentas por cobrar, porque se detuvieron las asignaciones de doble escritura enumeradas anteriormente.

4. Después de confirmar todas las facturas proforma, devuelva todas las asignaciones de doble escritura a su estado inicial.

    1. Actualice la versión del mapa de doble escritura de **Hitos de línea de contrato de integración de Project Operations** (**msdyn\_contractlinescheduleofvalues**) de vuelta al original. 
    2. Seleccione el mapa de doble escritura en la lista de asignaciones, seleccione **Versión de asignación de tablas** y, a continuación, seleccione la versión original de la asignación de tabla.
    3. Seleccione **Guardar**.
    4. Reinicie las siguientes asignaciones de doble escritura:

        - Los hitos de la línea de contrato de integración de Project Operations (msdyn\_contractlinescheduleofvalues)
        - Datos reales de integración de Project Operations (msdyn\_actuals)
        - Propuesta de factura de proyecto V2 (facturas)

Los hitos ahora se han migrado y el sistema está listo para los siguientes pasos en la actividad de transición.
