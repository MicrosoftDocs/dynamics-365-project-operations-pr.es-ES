---
title: Crear una factura proforma manual (lite)
description: Este tema proporciona información sobre crear una factura proforma manual en Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176407"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Crear una factura proforma manual (lite)

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

En Dynamics 365 Project Operations, las facturas proforma se pueden crear manualmente según sea necesario. Puede crear manualmente una factura proforma desde la página de lista **Contratos de proyectos** o de la página de detalles **Contrato de proyecto**.

##  <a name="project-contracts-list-page"></a>Página de lista de contrato de proyecto

Desde la página de lista **Contratos de proyectos**, seleccione uno o más contratos de proyecto y cree facturas para todos los registros seleccionados.

El sistema verifica cuál de los contratos de proyecto seleccionados tiene atrasos **Listo para facturar** con fecha anterior a la fecha de hoy. A partir de esos contratos, el sistema crea borradores de facturas proforma. Si un contrato de proyecto tiene varios clientes, puede haber una factura creada por cliente y varias facturas por contrato de proyecto.

Todas las facturas del proyecto creadas están disponibles en la página **Factura** en la sección **Facturación** de la zona **Ventas**.

## <a name="project-contract-details-page"></a>Página de detalles de contrato de proyecto

También se puede crear una factura proforma a partir de la página de detalles **Contrato de proyecto**, que crea la factura para ese contrato de proyecto específico. El sistema verifica que el contrato de proyecto tiene un atraso **Listo para facturar** con fecha anterior a la fecha de hoy. A partir de estos contratos, el sistema crea borradores de facturas proforma en función del número de clientes en cada línea de contrato.

Cuando se crea una sola factura proforma, se abre la página **Factura**. Si hay varias facturas creadas para ese contrato de proyecto, entonces se abre la página de lista **Facturas** para mostrar todas las facturas creadas.
