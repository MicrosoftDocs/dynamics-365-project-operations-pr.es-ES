---
title: Crear facturas de proveedores y clientes de empresas vinculadas
description: En este tema se ofrece información acerca de cómo crear facturas de proveedor y cliente de empresas vinculadas.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 92d08537fe0c2a1deba486974db53e7ebe1ff2d8
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948416"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Crear facturas de proveedores y clientes de empresas vinculadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Un contable de proyecto de una entidad jurídica prestamista crea una factura de cliente de empresas vinculadas para los costes del proyecto que se transfieren a la entidad prestataria. Una vez aprobada y registrada la factura del cliente de empresas vinculadas, la entidad jurídica prestamista envía la factura de empresas vinculadas a la entidad jurídica prestataria.

El contable de proyecto de la entidad jurídica prestamista puede configurar un proceso por lotes para generar facturas entre empresas vinculadas de forma periódica. El contable de proyecto especifica los criterios, como proyectos específicos, para crear facturas de empresas vinculadas en un lote.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Crear manualmente una factura de cliente de empresas vinculadas para transacciones de proyecto 

Use este procedimiento para crear manualmente una factura de cliente de empresas vinculadas para transacciones de proyecto. Busque las horas registradas por los trabajadores en proyectos de las entidades jurídicas prestatarias y los gastos en los que incurrió su entidad jurídica en nombre de las entidades jurídicas prestatarias. Puede buscar por nombre de entidad jurídica, número de contrato de proyecto, número de proyecto, rango de fechas o cualquier combinación de estas opciones. En los resultados de la búsqueda, seleccione las transacciones para agregar a una factura de empresas vinculadas. 

Los siguientes pasos deben realizarse en la entidad legal prestamista. 

1. En Dynamics 365 Finance, vaya a **Gestión de proyectos y contabilidad** > **Facturas de proyecto** > **Facturas de clientes de empresas vinculadas**. En la página de lista **Facturas de clientes de empresas vinculadas**, en el Panel de acciones, seleccione **Nuevo**.
2. En la página **Crear factura de empresas vinculadas**, en el campo **Entidad jurídica**, seleccione una entidad jurídica prestataria.
3. Opcional: Introduzca un contrato de proyecto y un número de proyecto específicos.
4. Restrinja la búsqueda seleccionando un rango de fechas. Introduzca las fechas específicas en los campos **Fecha de inicio** y **Fecha de finalización**. Solo las transacciones de empresas vinculadas que se registran dentro de este rango de fechas se muestran en los resultados de la búsqueda.
5. Establezca el **Parámetro de línea de diario avanzado de proyecto** en **Sí** y seleccione **Buscar**.
6. En los resultados de la búsqueda, seleccione las transacciones que se incluirán en la propuesta de factura de empresas vinculadas y, a continuación, seleccione **Aceptar**.
7. En la página **Factura de cliente de empresas vinculadas**, se muestran las transacciones de proyectos de empresas vinculadas que haya seleccionado de los resultados de búsqueda. Para modificar las transacciones antes de enviar la factura a la entidad jurídica prestataria, haga lo siguiente:
  
    1. En la página **Factura de cliente de empresas vinculadas**, abra los detalles de la factura y luego seleccione **Agregar línea**.
    2. Para quitar una línea, selecciónela y, a continuación, haga clic en **Quitar**.
    3. Vea comentarios, motivos, dimensiones financieras y otra información sobre una línea seleccionada en los detalles de la línea de factura.
    
8. Para registrar la factura de cliente de empresas vinculadas, en el Panel de acciones, seleccione **Registrar**.

> [!NOTE]
> Si su organización requiere que las facturas de empresas vinculadas se revisen antes de registrarse, un administrador del sistema podría configurar un flujo de trabajo para las facturas de empresas vinculadas. Si un flujo de trabajo no está configurado para facturas de empresas vinculadas, puede registrar la factura de empresas vinculadas.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Crear un trabajo por lotes para facturas de empresas vinculadas

Puede crear varias facturas de empresas vinculadas al mismo tiempo para todas las entidades jurídicas prestatarias. Con la funcionalidad de búsqueda, puede, por ejemplo, buscar todas las transacciones registradas por trabajadores con préstamo y relacionadas con proyectos gestionados por otras entidades jurídicas. Luego, para cada entidad jurídica prestataria, puede crear una factura de empresas vinculadas para las transacciones proporcionadas en los resultados de la búsqueda.

1. Vaya a **Gestión de proyectos y contabilidad** > **Periódico** > **Facturas de proyecto** > **Crear facturas de clientes de empresas vinculadas**.
2. En la página **Crear facturas de clientes de empresas vinculadas**, en el campo **Empresa**, seleccione una entidad jurídica para facturar. Si no selecciona una empresa, todas las transacciones que cumplen con los criterios de búsqueda se muestran para todas las entidades jurídicas prestatarias.
3. En **Crear una factura por**, seleccione si desea crear una factura para transacciones de empresas vinculadas en función de un proyecto o de una entidad jurídica prestataria.
4. Opcional: Para seleccionar un proyecto específico y un contrato de proyecto para el que crear facturas de empresas vinculadas, haga clic en **Seleccionar**. En la página **Consulta**, en el campo **Criterios**, seleccione el contrato del proyecto, el número de proyecto o ambos, y luego seleccione **Aceptar**.
5. En la pestaña **Lote**, configure un proceso por lotes para crear facturas de empresas vinculadas de forma periódica. Para más información, consulte [Enviar un trabajo de procesamiento por lotes desde un formulario](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Para registrar las facturas de empresas vinculadas, en el Panel de acciones, seleccione **Registrar**.

> [!NOTE]
> Si su organización requiere que las facturas de empresas vinculadas se revisen antes de registrarse, un administrador del sistema podría configurar un flujo de trabajo para las facturas de empresas vinculadas. Si un flujo de trabajo no está configurado para facturas de empresas vinculadas, puede registrar las facturas de empresas vinculadas.

## <a name="post-the-intercompany-vendor-invoice"></a>Registrar la factura de proveedor de empresas vinculadas

Un contable de proyecto en la entidad jurídica prestamista puede revisar facturas de proveedores pendientes de empresas vinculadas cuando se registra la factura de cliente de empresas vinculadas. En Finance, en la entidad jurídica prestataria, vaya a **Proveedores** > **Facturas** > **Factura de proveedor pendiente**. El número de factura pendiente coincidirá con el número de factura de cliente de empresas vinculadas. Compruebe que la factura sea correcta y luego registre la factura. El registro de la factura de proveedor de empresas vinculadas crea un libro auxiliar del proyecto y una transacción de contabilidad general que refleja los costes de transacción en la entidad jurídica prestataria.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
