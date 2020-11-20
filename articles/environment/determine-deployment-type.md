---
title: Determinar el tipo de implementación
description: Este tema proporciona información para ayudarle a determinar el tipo de implementación correcto de las operaciones de proyecto para su empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401239"
---
# <a name="determine-your-deployment-type"></a>Determinar el tipo de implementación

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

> [!IMPORTANT]
> Después de comprar la licencia, comience aquí para determinar el mejor modelo de implementación de Dynamics 365 Project Operations usando el [Flujo de instalación guiado](https://aka.ms/provisionprojectoperations).
> Una vez que haya finalizado el flujo de instalación guiada, se le dirigirá al portal de administración correcto para completar su instalación. Consulte los detalles de implementación para completar la instalación.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clientes existentes de Dynamics que utilizan Dynamics 365 Project Service Automation
Project Operations incluye las capacidades que se incluyen con Project Service Automation. Se lanzará una ruta de actualización para estos clientes en la primera ola de versiones de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clientes existentes de Dynamics 365 Finance que usan gestión de proyectos y contabilidad 

Los clientes existentes de Finance que utilizan la funcionalidad de contabilidad y gestión de proyectos pueden seguir utilizándola tal cual. Consulte [Project Operations para escenarios de pedidos en existencias/producción](#pma).


## <a name="deployment-types"></a>Tipo de implementación
Project Operations admite múltiples opciones de implementación para satisfacer sus necesidades. Ya sea un cliente nuevo o existente de Dynamics 365, Project Operations puede satisfacer sus necesidades.

Nuestro [Cuestionario de implementación](https://aka.ms/provisionprojectoperations) le ayudará a determinar la implementación correcta. Los resultados le guiarán hacia uno de los siguientes tipos de implementación:

- [Implementación lite: del acuerdo a la facturación proforma](#lite)
- [Project Operations para escenarios de recursos/no mantenidos en existencias](#integrated)
- [Project Operations para escenarios mantenidos en existencias/orden de producción](#pma)

Project Operations admite escenarios de pedidos de existencias/producción y escenarios de no existencias/basados en recursos en el mismo entorno a través de configuraciones a nivel de entidad legal. Por ejemplo, Contoso puede usar las capacidades de pedidos de stock / producción en sus instalaciones de fabricación de EE. UU. (Entidad legal = Contoso Manufacturing United States). Contoso puede usar las capacidades no almacenadas / basadas en recursos en su instalación de servicio Contoso Robotics Arms en el Reino Unido (entidad legal = Contoso Robotics Reino Unido).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implementación lite: del acuerdo a la facturación proforma

La implementación simplificada incluye las siguientes capacidades:

- Proceso de ventas para proyectos que amplía las experiencias de la aplicación Dynamics 365 Sales
- Planificación de proyectos con Microsoft Project para la Web
- Precios multidimensionales
- Administración de recursos unificada
- Seguimiento en el tiempo
- Gasto básico
- Facturación proforma y de cara al cliente 

#### <a name="deployment-steps"></a>Pasos de implementación
Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).

Para esta implementación, consulte [Registrarse para suscripciones de vista previa](lite-preview-subscription-sign-up.md) y [Aprovisionar un nuevo entorno](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations para escenarios de recursos/no mantenidos en existencias
Project Operations para escenarios de recursos/no en existencias incluye las siguientes capacidades:
 
- Proceso de ventas para proyectos que amplía la aplicación Dynamics 365 Sales
- Planificación de proyectos con Microsoft Project para la Web
- Precios multidimensionales
- Administración de recursos unificada
- Seguimiento en el tiempo
- Gasto básico
- Gasto completo
- OCR de recibos
- Facturación proforma y de cara al cliente 
- Reconocimiento de ingresos para proyectos

#### <a name="deployment-steps"></a>Pasos de implementación
Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).

Para esta implementación, consulte [Registrarse para suscripciones de vista previa](resource-sign-up-preview-subscription.md) y [Aprovisionar un nuevo entorno](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations para escenarios mantenidos en existencias/orden de producción

- Planificación del proyecto usando WBS
- Administración de recursos
- Seguimiento en el tiempo
- Gasto completo
- OCR de recibos
- Facturación completa
- Reconocimiento de ingresos
- Órdenes de producción
- Soporte de materiales

#### <a name="deployment-steps"></a>Pasos de implementación
Determine el mejor modelo de implementación de Project Operations utilizando el [Cuestionario de implementación](https://aka.ms/provisionprojectoperations).

Para esta implementación, consulte [Registrarse para suscripciones de vista previa](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) y [Aprovisionar un nuevo entorno](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

