---
title: Configurar la facturación con empresas vinculadas
description: En este tema se proporciona información y ejemplos sobre la configuración de la facturación con empresas vinculadas para proyectos.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595562"
---
# <a name="configure-intercompany-invoicing"></a>Configurar la facturación con empresas vinculadas

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Complete los siguientes pasos para configurar la facturación de empresas vinculadas para proyectos en Dynamics 365 Project Operations. Las transacciones de empresas vinculadas son transacciones de tiempo y gastos de un contrato de proyecto que pertenecen a una empresa o unidad organizativa, mientras que los recursos del contrato del proyecto forman parte de una empresa o unidad organizativa diferentes.

## <a name="example-configure-intercompany-invoicing"></a>Ejemplo: Configurar la facturación con empresas vinculadas

En el siguiente ejemplo, Contoso Robotics USA (USPM) es la entidad jurídica prestataria y Contoso Robotics UK (GBPM) es la entidad jurídica prestamista. 

1. **Configurar la contabilidad de empresas vinculadas entre entidades jurídicas**. Cada par de entidades legales prestatarias y prestamistas debe configurarse en la página Contabilidad general [Contabilidad de empresas vinculadas](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. En Dynamics 365 Finance, vaya a **Contabilidad general** > **Configuración del registro** > **Contabilidad de empresas vinculadas**. Cree un registro con la siguiente información:

        - **Empresa de origen** = **GBPM**
        - **Empresa de destino** = **USPM**

2. **Configurar la relación comercial entre personas jurídicas**. El registro de cliente que representa a la entidad jurídica prestataria debe crearse en la entidad jurídica prestamista. El registro de proveedor que representa a la entidad jurídica prestamista debe crearse en la entidad jurídica prestataria.

     1. En Finance, seleccione la entidad jurídica **GBPM**.
     2. Vaya a **Clientes** > **Cliente** > **Todos los clientes**. Cree un nuevo registro para la entidad jurídica, **USPM**.
     3. Expanda **Nombre**, filtre los registros por **Tipo** y seleccione **Entidades jurídicas**. 
     4. Busque y seleccione el registro de cliente para **Contoso Robotics USA (USPM)**.
     5. Seleccione **Usar coincidencia**. 
     6. Seleccione el grupo de clientes y luego guarde el registro.
     7. Seleccione la entidad jurídica **USPM**.
     8. Vaya a **Proveedores** > **Proveedores** > **Todos los proveedores**. Cree un nuevo registro para la entidad jurídica, **GBPM**.
     9. Expanda **Nombre**, filtre los registros por **Tipo** y seleccione **Entidades jurídicas**. 
     10. Busque y seleccione el registro de cliente para **Contoso Robotics UK (GBPM)**.
     11. Seleccione **Usar coincidencia**, seleccione el grupo de proveedores y luego guarde el registro.
     12. En el registro de proveedor, seleccione **General** > **Configuración** > **Empresas vinculadas**.
     13. En la pestaña **Relación comercial**, establezca **Activo** en **Sí**.
     14. Seleccione la empresa proveedora **GBPM** y en **Mi registro de cuenta**, seleccione el registro de cliente que creó anteriormente en el procedimiento.

3. **Configurar la configuración de empresas vinculadas en los parámetros de Gestión de proyectos y contabilidad**. 

    1. Seleccione la entidad jurídica **USPM** y vaya a **Gestión y contabilidad de proyectos** > **Configuración** > **Parámetros de gestión de proyectos y contabilidad**.
    2. En la pestaña **Empresas vinculadas**, seleccione la categoría de compras para que coincida con las facturas de proveedor que se generan automáticamente.
    3. En **Categoría predeterminada**, seleccione **Recursos de empresas vinculadas**.
    4. Seleccione la entidad jurídica **GBPM** y vaya a **Gestión y contabilidad de proyectos** > **Configuración** > **Parámetros de gestión de proyectos y contabilidad**.
    5. En la pestaña **Empresas vinculadas**, seleccione una categoría de proyecto predeterminada para cada tipo de transacción. Las categorías de proyecto se utilizan para la configuración de impuestos cuando la categoría facturada en las transacciones entre empresas vinculadas existe solo en la entidad jurídica prestataria. Puede optar por acumular ingresos por transacciones entre empresas vinculadas. La acumulación se produce cuando las transacciones se registran a través del diario de integración de Project Operations en la entidad jurídica prestamista. El diario se invierte cuando se registra la factura de empresas vinculadas.
    6. En el grupo **Al prestar recursos**, seleccione **...** > **Nuevo**. 
    7. En la cuadrícula, seleccione la siguiente información:

          - **Entidad jurídica prestataria** = **GBPM**
          - **Ingresos acumulados** = **Sí**
          - **Categoría de parte de horas predeterminada** = **Predeterminado: hora**
          - **Categoría de gastos predeterminada** = **Predeterminado: gasto**

4. **Establecer cuentas de costes e ingresos de empresas vinculadas en la configuración de registro contable**. Se realiza un abono en la cuenta de ingresos de empresas vinculadas cuando la factura de cliente de empresas vinculadas se registra en la entidad jurídica prestamista. Se efectúa un cargo en la cuenta de costes de empresas vinculadas cuando la factura de proveedor pendiente coincidente se registra en la entidad jurídica prestataria. Estas cuentas se configuran en las entidades jurídicas correspondientes. 
      
     1. En Finance, seleccione la entidad jurídica prestataria **USPM**. 
     2. Vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Registro** > **Configuración de registro de libro mayor**. 
     3. En la pestaña **Cuentas de costes**, en **Tipo de cuenta contable**, seleccione **Coste de empresas vinculadas**. Cree un nuevo registro con la información siguiente:
      
        - **Entidad jurídica prestamista** = **GBPM**
        - **Cuenta principal** = Seleccionar la cuenta principal para el coste de empresas vinculadas
        
     4. Seleccione la entidad jurídica prestamista, **GBPM**. 
     5. Vaya a **Gestión de proyectos y contabilidad** > **Configuración** > **Registro** > **Configuración de registro de libro mayor**. 
     6. En la pestaña **Cuentas de ingresos**, en **Tipo de cuenta contable**, seleccione **Ingresos de empresas vinculadas**. Cree un nuevo registro con la información siguiente:

        - **Entidad jurídica prestataria** = **USPM**
        - **Cuenta principal** = Seleccionar la cuenta principal para los ingresos de empresas vinculadas 

5. **Configurar precios de transferencia para mano de obra**. Los precios de transferencia de empresas vinculadas se configuran en Project Operations en Dataverse. Configure las [tarifas de costes de mano de obra](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) y las [tarifas de facturas de mano de obra](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) para facturación de empresas vinculadas. Los precios de transferencia no son compatibles con las transacciones de gastos de empresas vinculadas. El precio de venta unitario entre organizaciones siempre se establecerá en el mismo valor que el precio de coste unitario de recursos.

      El coste de recursos para desarrolladores en Contoso Robotics UK es de 88 GBP por hora. Contoso Robotics UK facturará a Contoso Robotics USA 120 USD por cada hora que este recurso haya trabajado en proyectos estadounidenses. Contoso Robotics USA facturará al cliente Adventure Works 200 USD por el trabajo realizado por el recurso para desarrolladores de Contoso Robotics UK.

      1. En Project Operations en Dataverse, vaya a **Venta** > **Listas de precios**. Cree una nueva lista de precios de coste llamada **Tarifas de coste de Contoso Robotics UK**. 
      2. En la lista de precios de coste, cree un registro con la siguiente información:
         - **Rol** = **Desarrollador**
         - **Coste** = **88 GBP**
      3. Vaya a **Configuración** > **Unidades organizativas** y adjunte esta lista de precios de coste a la unidad organizativa **Contoso Robotics UK**.
      4. Vaya a **Ventas** > **Listas de precios**. Cree una lista de precios de coste llamada **Tarifas de coste de Contoso Robotics USA**. 
      5. En la lista de precios de coste, cree un registro con la siguiente información:
          - **Rol** = **Desarrollador**
          - **Empresa de dotación de recursos** = **Contoso Robotics UK**
          - **Coste** = **120 USD**
      6. Vaya a **Configuración** > **Unidades organizativas** y adjunte la lista de precios de coste **Tarifas de coste de Contoso Robotics USA** a la unidad organizativa **Contoso Robotics USA**.
      7. Vaya a **Ventas** > **Listas de precios**. Cree una lista de precios de venta llamada **Tarifas de facturación de Adventure Works**. 
      8. En la lista de precios de venta, cree un registro con la siguiente información:
          - **Rol** = **Desarrollador**
          - **Empresa de dotación de recursos** = **Contoso Robotics UK**
          - **Tasa de facturación** = **200 USD**
      9. Vaya a **Ventas** > **Contratos de proyectos** y adjunte la lista de precios de **Tarifas de facturación de Adventure Works** en la lista de precios a la lista de precios del proyecto Adventure Works del contrato del proyecto.
