---
title: Confirmar, actualizar y enviar una cotización de proyecto
description: Este tema proporciona información sobre cómo enviar un presupuesto al cliente para su confirmación, modificarlo en función de los comentarios y luego reenviar el presupuesto.
author: ruhercul
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f9d76c65cb6732a96cd0bd6c4c36a2a73a65a2b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085286"
---
# <a name="confirm-update-and-send-a-project-quotation"></a>Confirmar, actualizar y enviar una cotización de proyecto

[!include [banner](../includes/banner.md)]

Después de crear y enviar una cotización de proyecto a un cliente, debe obtener la confirmación del cliente antes de actualizar el estado de la cotización a **Enviado**. Cualquier modificación solicitada por el cliente se puede actualizar en el presupuesto. Después de actualizar el estado de la cotización a **Enviado** , no puede modificarlo. El siguiente procedimiento describe las opciones para enviar una cotización para su confirmación, realizar actualizaciones basadas en los comentarios y luego enviar la cotización.

## <a name="send-a-project-quotation-confirmation"></a>Enviar una confirmación de cotización de proyecto  

Puede enviar una cotización de proyecto existente para su confirmación por correo electrónico o como copia impresa. 

1. Vaya a **Gestión de proyectos y contabilidad** > **Cotizaciones** > **Cotización de proyecto.** 
2. En la página **Cotización de proyecto** , seleccione la cotización que desea enviar para confirmación. 
3. En la pestaña **Seguimiento** , en el grupo **Generar** , seleccione **Confirmar**. 
4. En la página **Confirmar cotización** , configure los parámetros necesarios. Por ejemplo, para imprimir la confirmación, en las opciones de **Imprimir** , active **Confirmación de impresión** y luego seleccione **Aceptar**.
5. En la página **Enviar cotización** , seleccione **Opciones** , y en la página **Configuración de destino de impresión** , seleccione si desea que la cotización se envíe a **Pantalla** , **Correo electrónico** , **Archivo** , **Archivo de impresión** o **Impresora** y, a continuación, realice los ajustes que desee en el área **Especificación** para enrutar la cotización.
6. En la página **Configuración de destino de impresión** , seleccione **Aceptar**.  

## <a name="update-a-project-quotation"></a>Actualizar una cotización de proyecto

Para modificar una cotización de proyecto existente, el estado de la cotización debe ser **Creado**. Complete los siguientes pasos para actualizar una cotización existente. 

1. Vaya a **Gestión de proyectos y contabilidad** > **Cotizaciones** > **Cotizaciones de proyecto**.
2. En la página **Cotizaciones de proyectos** , seleccione la cotización que desea actualizar y en el Panel de acciones, seleccione **Editar**.
3. Actualice la información de campo necesaria y, en el Panel de acciones, seleccione **Guardar**.  

## <a name="send-a-project-quotation-to-a-customer"></a>Enviar una cotización de proyecto a un cliente 

1. Vaya a **Gestión de proyectos y contabilidad** > **Cotizaciones** > **Cotizaciones de proyecto** y seleccione la cotización del proyecto que desea enviar.
2. En la página **Cotizaciones de proyecto** , en la pestaña **Cotización** , en el grupo **Proceso** , seleccione **Enviar cotización**. El estado de la cotización se actualiza a **Enviado**.

> [!NOTE]
> No puede modificar la cotización de un proyecto después de que el estado cambie a **Enviado**.