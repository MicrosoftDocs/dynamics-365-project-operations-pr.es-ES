---
title: Cambios en la entidad, el control y la interfaz de usuario (Project Service Automation 3.x)
description: En este tema se describen los cambios de soluciones para Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148754"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Cambios en la entidad, el control y la interfaz de usuario (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Con la versión de Microsoft Dynamics Project Service Automation (PSA) 3.x se han realizado muchos cambios en las entidades, los controles, las vistas y la interfaz de usuario. Este tema proporciona información sobre estos cambios importantes.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relaciones primarias y secundarias para las entidades de documentos de ventas, líneas de documentos de ventas y detalles de líneas de documentos de ventas
En las versiones de Dynamics 365 Project Service Automation (PSA) anteriores a la versión 3.0, algunas de las relaciones entre las entidades de documentos de ventas, líneas de documentos de ventas y detalles de líneas de documentos de ventas se implementaban mediante campos de cadena que conservaban una representación de cadena del GUID de la entidad relacionada. Esto se debía a las limitaciones de la plataforma que requerían bastante código personalizado en los lados del cliente y del servidor de la solución para que dichas relaciones funcionaran de manera similar a las relaciones de entidad de Dynamics CRM típicas y para que los campos de cadena actuaran como campos de búsqueda.

PSA 3.0 se ha actualizado para utilizar las nuevas relaciones de entidades entre las entidades de documentos de ventas y líneas de documentos de ventas.

Puesto que los campos de búsqueda se pueden utilizar ahora para indicar referencias a las entidades, los campos que conservaban el valor de cadena del GUID de la entidad relacionada en las versiones anteriores ya no son necesarios y, por lo tanto, están en desuso. El código personalizado de los lados del servidor y el cliente que gestionaba las relaciones definidas por los campos de cadena anteriores también están en desuso.

### <a name="entity-schema-changes"></a>Cambios de esquema de entidad
En la siguiente tabla se proporciona una lista individual de los campos de cadena en desuso y de los nuevos campos de búsqueda para las entidades. 

 Entidad |   Campo en desuso (cadena) | Campo nuevo (búsqueda)
--- | --- | ---
invoicedetail (Línea de factura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Real) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Programación de facturas de línea de contrato de proyecto) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Hito de línea de contrato de proyecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Hecho) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Detalle de línea de factura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Línea de diario) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Categoría de recursos de línea de contrato de proyecto) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Detalle de línea de contrato de proyecto) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Categoría de transacciones de línea de contrato de proyecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Clasificación de transacciones de línea de contrato de proyecto) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Programación de facturas de línea de oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Categoría de recursos de línea de oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Hito de línea de oferta) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Detalle de línea de oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Categoría de transacciones de línea de oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Clasificación de transacciones de línea de oferta) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Línea de pedido) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Controles y vistas personalizados en desuso
A continuación se describen los controles y las vistas personalizados en desuso junto con sus artefactos relacionados.

- Vista de imputabilidad.
- Controles de cuadrícula personalizados para mostrar los detalles de línea de oferta en la página **Información del proyecto** para la línea de oferta.
- Controles de cuadrícula personalizados para mostrar los detalles de línea de contrato del proyecto en la página **Información del proyecto** para la línea de pedido de ventas.

> [!NOTE]
> Para obtener la lista completa de recursos en desuso, consulte [Recursos web en desuso en Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Módulo de la aplicación de la interfaz del cliente unificada
Con la introducción de módulos de la aplicación de la interfaz del cliente unificada (UCI), se han quitado las entradas del mapa del sitio de PSA del sistema.  
La funcionalidad relacionada al cambio de formularios para Oportunidad, Oferta, Pedido y Factura está en desuso, ya que ha dejado de ser necesaria debido a que el módulo de la aplicación de UCI solo incluye versiones de PSA del formulario.  

A continuación se describen los recursos web que están en desuso:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Para obtener la lista completa de recursos en desuso, consulte [Recursos web en desuso en Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


