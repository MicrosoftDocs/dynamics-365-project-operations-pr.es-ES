---
title: Configurar retención de proveedores
description: En este artículo se explica cómo configurar la retención de proveedores.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f30e8829d8d5d99c81fce730cb93cd7ce31913fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929787"
---
# <a name="set-up-vendor-retention"></a>Configurar retención de proveedores

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

En este artículo se ofrece información acerca de cómo configurar la retención de proveedores.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurar una cuenta de retención de proveedores en contabilidad general

1. En Dynamics 365 Finance, vaya a **Contabilidad general** > **Configuración de registro** > **Cuentas para transacciones automáticas**.
2. Agregue una nueva línea.
3. En el campo **Tipo de registro**, seleccione **Retención de proveedores**.
4. Seleccione la cuenta principal para el registro de retención de proveedores.

## <a name="create-vendor-retention-terms"></a>Condiciones de retención de retención de proveedores

Utilice la página **Condiciones de retención de proveedores** para configurar y mantener las condicones de retención para pagos a proveedores. Especifique el porcentaje del pago al proveedor a retener y el porcentaje de los importes retenidos anteriormente a liberar. Los importes se retienen automáticamente en las facturas del proveedor hasta que el contrato alcanza el estado especificado de finalización. Una vez configuradas las condiciones de retención para un proveedor, puede aplicarlas a cualquier proyecto en el que trabaje el proveedor.

1. En Finance, vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Retencion** > **Términos de retención de pago a proveedores**.
2. Seleccione **Nuevo** para agregar un nuevo plazo de retención de proveedores. El valor del campo **Id. de regla** de la nueva condición se especifica automáticamente. 
3. En el campo **Descripción**, escriba un nombre descriptivo para la nueva condición.
4. En la pestaña **Condiciones**, seleccione **Agregar línea** para ingresar una condición de retención de proveedores.
5. En el campo **Porcentaje de unidades entregado**, introduzca un porcentaje de completado de la regla. Los importes se retienen automáticamente en las facturas al proveedor hasta que la etapa de proyecto de finalización sea igual al porcentaje que especifica. Por ejemplo, si introduce 50,00, las cantidades se retienen hasta que el proyecto se completa en un 50 por ciento.
6. En el campo **Porcentaje a retener**, introduzca el porcentaje del importe de una factura de proveedor a retener. Por ejemplo, si especifica 10,00 en este campo, el 10 por ciento del importe de facturas a proveedores se retiene hasta que el proyecto alcance el porcentaje de finalización que usted seleccione en el campo **Porcentaje de unidades entregado**.
7. En el campo **Porcentaje a liberar**, seleccione el porcentaje de los importes retenidos anteriormente para liberar en el nivel seleccionado de finalización del proyecto.

> [!NOTE]
> Si tiene más de un hito para distintos niveles de finalización del proyecto, especifique una línea de termino de retención independiente al proveedor para cada regla de retención. Cada línea puede especificar otro porcentaje a retener y otro porcentaje a liberar para cada nivel designado de finalización del proyecto.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configuración de un contrato de proveedor para el proyecto

Configure los términos de retención de proveedores que se aplican al proyecto. Los términos de retención de proveedores también se muestran en las órdenes de compra que crea para el proveedor.

1. En Finance, vaya a **Gestión de proyectos y contabilidad** > **Proyectos** > **Todos los proyectos**. 
2. Seleccione un proyecto y, en el Panel de acciones, seleccione **Grupo de proyecto** > **Contratos de proveedor**.
3. En lapágina **Contratos de proveedor**, agregue una nueva línea.
4. En el campo **Código de cuenta**, seleccione una de las siguientes opciones:
   - **Tabla**: los términos de retención de proveedor se aplican a un solo proveedor.
   - **Grupo**: los términos de retención de proveedor se aplican a todos los proveedores de un grupo de proveedores.
   - **Todos**: los términos de retención de proveedor se aplican a todos los proveedores.
5. En el campo **Proveedor/campo de grupo de proveedores**, seleccione el proveedor o el grupo de proveedores al que se aplican los términos de retención de proveedores. Si seleccionó **Todos** en el paso anterior, este campo no está disponible.
6. En el campo **Términos de retención de proveedores**, seleccione el ID de la regla para que los términos de retención se apliquen a este proveedor.

