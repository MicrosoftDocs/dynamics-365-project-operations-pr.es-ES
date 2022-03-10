---
title: Implementar manualmente la aplicación Project Operations Dataverse con soporte de escritura dual
description: Este tema explica cómo implementar manualmente la aplicación Project Operations Dataverse para que admita escritura dual.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986467"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Implementar manualmente la aplicación Project Operations Dataverse con soporte de escritura dual

_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_

Este tema explica cómo implementar manualmente la aplicación Microsoft Dynamics 365 Project Operations en Microsoft Dataverse para que admita escritura dual. Project Operations detecta la configuración del entorno y agrega soporte adicional para escritura dual si se cumplen los requisitos previos.

Durante la implementación mediante Microsoft Dynamics Lifecycle Services (LCS), si ha seguido las instrucciones de este tema, puede omitir la implementación de la integración de Microsoft Power Platform (anteriormente conocida como el entorno Common Data Service).

El proceso de implementación de Project Operations en Dataverse para que admita escritura dual tiene cuatro pasos principales:

1. [Crear un nuevo entorno en Dataverse que admita escritura dual](#create).
2. [Agregar requisitos previos de escritura dual al entorno](#prerequisites).
3. [Agregar la aplicación Project Operations Dataverse](#dataverse).
4. [Vincular sus entornos](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Crear un nuevo entorno en Dataverse que admita escritura dual

Para completar este proceso, debe iniciar sesión como administrador.

1. Abra el [Centro de administración de Power Platform](https://admin.powerplatform.com) e inicie sesión como administrador.
2. Cree un nuevo entorno y póngale un nombre.
3. Seleccione el tipo de entorno. Si se registró para la oferta de prueba, seleccione **Prueba (basada en suscripción)**.
4. Confirme la región de implementación.
5. Habilite la opción **Desea crear una base de datos para este entorno**. 
6. Confirme el idioma y luego confirme que la moneda coincide con la moneda de sus aplicaciones de Finance and Operations.
7. Habilite la opción **Aplicaciones de Dynamics 365** y confirme que el campo **Implementar automáticamente estas aplicaciones** está configurado en **Ninguno**.
8. Agregue un grupo de seguridad si es necesario.
9. Seleccione **Guardar** para crear el entorno.
10. Espere hasta que se complete la implementación y el entorno alcance el estado **Listo**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Agregar requisitos previos de escritura dual al entorno

El soporte de escritura dual incluye campos adicionales que se agregan a entidades clave, como la entidad **Empresa**. Si va a agregar soporte de escritura dual a un entorno existente, es posible que deba actualizar los datos para habilitar el soporte. Para obtener información sobre cómo impulsar los datos, consulte [Impulsar datos de la empresa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Para obtener más información sobre escritura dual, consulte [Requisitos del sistema de escritura dual](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Complete este procedimiento para agregar los requisitos previos de escritura dual a su entorno.

1. Abra el entorno que acaba de crear y luego vaya a **Recurso** \> **Aplicaciones de Dynamics 365**.
2. Seleccione **Solución básica de doble escritura** en la lista de aplicaciones e instálela.
3. Espere hasta que se complete la instalación. Después, seleccione **Solución de orquestación de aplicaciones de doble escritura** en la lista de aplicaciones e instálela.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Agregar la aplicación Project Operations Dataverse

Puede completar este procedimiento solo si completó los procedimientos anteriores antes de instalar Project Operations. Durante la instalación, el sistema analiza la configuración del entorno y agrega soporte para escritura dual si es necesario.

1. Abra el entorno que ha creado antes y luego vaya a **Recurso** \> **Aplicaciones de Dynamics 365**.
2. Seleccione **Microsoft Dynamics 365 Project Operations** en la lista de aplicaciones e instálelo.

## <a name="link-your-environments"></a><a name="link"></a>Vincular sus entornos

Después que el entorno de Dataverse esté implementado, puede configurar el vínculo en sus aplicaciones de Finance and Operations. Siga los pasos en [Usar el asistente de escritura dual para vincular sus entornos](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
