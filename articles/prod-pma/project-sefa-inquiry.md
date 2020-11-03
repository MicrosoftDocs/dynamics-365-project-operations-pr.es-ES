---
title: Consulta sobre el programa de gastos de las adjudicaciones federales
description: Este tema proporciona información sobre la consulta sobre el Programa de gastos de las adjudicaciones federales.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085132"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Consulta sobre el programa de gastos de las adjudicaciones federales

[!include [banner](../includes/banner.md)]

Según la Circular A-133 de la Oficina de Gestión y Presupuestos, las agencias que reciben fondos federales están sujetas a requisitos de auditoría, que también se conocen como auditorías únicas. El proceso de auditoría se utiliza para informar sobre los ingresos y gastos de las subvenciones federales de forma periódica. Parte del informe de auditoría único incluye el Programa de gastos de las adjudicaciones federales (SEFA).

La consulta del Programa de gastos de las subvenciones federales incluye el título y número del Catálogo de asistencia doméstica federal (CFDA), el número de la subvención, el año de la subvención, el nombre de la agencia federal que proporciona los fondos y el nombre de la entidad de paso. La consulta es por un período específico. Normalmente, ese período es el mismo que el período del estado financiero, que es un año fiscal.

La consulta incluye subvenciones que tienen fechas de proyección en el rango de fechas seleccionado. La columna **Agencia concesionaria** de la consulta muestra el cliente de la concesión o, para una concesión de transferencia, la agencia concesionaria. Para una concesión de transferencia, la columna **Agencia concesionaria** muestra el cliente de la concesión. Si la concesión no es una concesión de transferencia, la columna **Agencia concesionaria** está en blanco.

## <a name="set-up-the-cfda-clusters"></a>Configuración de los grupos CFDA

Debe configurar los grupos de CFDA que se pueden asociar con los números de CFDA en la consulta de Lista de gastos de adjudicaciones federales.

1. Vaya a **Gestión de proyectos y contabilidad \> Configuración \> Concesiones \> Catálogo de grupos de Asistencia Doméstica Federal**.
2. Para crear un clúster CFDA seleccione **Nuevo**.
3. Especifique el nombre del clúster.
4. Seleccione **Guardar** para guardar los cambios.

## <a name="set-up-cfda-numbers"></a>Configurar números CFDA

Debe configurar los números de CFDA que se pueden agregar a las concesiones y se incluyen en la consulta de Lista de gastos de adjudicaciones federales.

1. Vaya a **Gestión de proyectos y contabilidad \> Configuración \> Concesiones \> Catálogo de números de Asistencia Doméstica Federal**.
2. Seleccione **Nuevo** para crear un número CFDA.
3. En la columna **Número** , especifique el número CFDA.
4. Presione la tecla **Tabulador**.
5. En la columna **Descripción** , introduzca el título CFDA.
6. Presione la tecla **Tabulador**.
7. Opcional: en el campo **Clúster de programas** , agregue el clúster CFDA apropiado.
8. Seleccione **Guardar** para guardar los cambios.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurar subvenciones para informar para la consulta del Programa de gastos de las subvenciones federales

1. Vaya a **Gestión de proyectos y contabilidad \> Concesiones \> Concesiones** y seleccione una concesión existente.
2. En la ficha desplegable **Configuración** , en el campo **Catálogo de Asistencia Doméstica Federal** , asigne el número CFDA. El número de CFDA en la concesión determina el clúster de CFDA para informar.
3. En la ficha desplegable **Información del contacto** , introduzca la información del otorgante siguiendo estos pasos:

    1. En el campo **Cliente de concesión** , introduzca el cliente responsable de la subvención. Para una subvención existente, es posible que esta información ya esté ingresada.
    2. Indique si el cliente de la concesión es el financiador. Si el cliente de la concesión es el financiador, deje la casilla de verificación **Pasar por** desactivada. Si otro cliente es el financiador y el cliente de la concesión es responsable de gastar y seguir el dinero, seleccione la casilla de verificación **Pasar por**.

4. Si seleccionó la casilla de verificación **Pasar por** en el paso anterior, en el campo **Agencia otorgante** introduzca el cliente que proporcionó la concesión. La agencia otorgante y el cliente de la concesión no pueden ser el mismo cliente.

A continuación, se muestra un ejemplo de una concesión de transferencia:

El gobierno federal financió un proyecto de infraestructura para un estado. El gobierno federal entregó el dinero al estado para que lo gastara. En este caso, el gobierno federal es la agencia otorgante y el estado es el cliente de la concesión.

> [!NOTE] 
> Cuando active la función por primera vez, los números CFDA iniciales se ingresarán utilizando los números existentes en las subvenciones.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excluir las subvenciones de los informes SEFA según el tipo de subvención

1. Vaya a **Gestión de proyectos y contabilidad \> Configurar \> Concesiones \> Tipos de concesiones**.
2. En la ficha desplegable **Información predeterminada** , seleccione la casilla de verificación **Excluir de la Lista de gastos de las adjudicaciones federales**.
3. Seleccione **Guardar** para guardar los cambios.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Ejecute la consulta del programa de gastos de las adjudicaciones federales

1. Vaya a **Gestión de proyectos y contabilidad \> Consultas e informes \> Solicitud de concesión \> Lista de gastos de las adjudicaciones federales**.
2. En la sección **Parámetros** siga estos pasos:

    1. En campo **Intervalo de fechas** , seleccione el código para el intervalo de fechas. Alternativamente, en los campos **Desde fecha** y **Hasta fecha** , defina el intervalo de fechas.
    2. Opcional: para incluir solo las transacciones facturadas como ingresos en la consulta, establezca la opción **Incluir solo los ingresos facturados** a **Sí**.

## <a name="columns"></a>Columnas

La consulta de Lista de gastos de adjudicaciones federales incluye las siguientes columnas:

- Catálogo de nombre del grupo de Asistencia Doméstica Federal
- Agencia otorgante
- Agencia de paso
- Nombre de la concesión
- ID de concesión
- Identificador de aplicación de concesión
- Catálogo de Asistencia Doméstica Federal
- Recibos
- Gastos
