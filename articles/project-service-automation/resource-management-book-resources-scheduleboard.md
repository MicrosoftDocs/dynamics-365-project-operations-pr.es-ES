---
title: Uso del panel de programación para reservar recursos de proyecto
description: En este tema se proporciona información sobre cómo reservar recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 169f7b98-119b-4aa2-b121-c73c0396fcde
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b377e0c80b2c4eb5028f131620213ea534a1a4dc
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756059"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a>Uso del panel de programación para reservar recursos de proyecto

Además de reservar recursos en un proyecto desde dentro de un proyecto, puede reservar recursos de tentativa de reservas o reservas en firme desde el panel de programación.

Para poder reservar desde el panel de programación, debe crear o generar requisitos de recursos. Siga estos pasos para crear requisitos de recursos desde el panel de programación.

1. Si el panel **Requisitos de reserva** de la parte inferior de la página está contraído, seleccione el control de expansión para ampliarlo.
2. En el panel **Requisitos de reserva**, en la pestaña **Proyecto**, seleccione el requisito para reservar.

    ![Requisito seleccionado en la pestaña Proyecto](media/Resource-Management-image73.png)

3. Seleccione **Buscar disponibilidad** para filtrar los recursos que se pueden reservar y ver los recursos disponibles. 
4. Seleccione uno o más recursos del panel de programación. 
5. En el panel **Crear reserva de recursos** a la derecha de la página, introduzca la información de la reserva y, a continuación, seleccione **Reservar y salir**.

    ![Panel Crear reserva de recursos para el recurso que se puede reservar seleccionado](media/Resource-Management-image74.png)

6. Mientras el requisito esté seleccionado en el panel **Crear reserva de recursos**, seleccione una o más celdas de un recurso para crear la reserva.

    ![Varias celdas seleccionadas para un recurso](media/Resource-Management-image75.png)

7. Seleccione **Reservar**.

El requisito se cumple mediante el recurso seleccionado. En el panel **Requisitos de reserva**, observe que se haya actualizado el requisito y que el recurso se muestre como reservado en el proyecto.

![Recurso reservado en el proyecto](media/Resource-Management-image76.png)
