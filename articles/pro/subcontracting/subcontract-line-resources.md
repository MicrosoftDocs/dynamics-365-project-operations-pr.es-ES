---
title: Recursos de línea de subcontrato
description: Este tema explica cómo especificar los recursos dedicados que proporciona el proveedor para una línea de subcontrato específica por tiempo.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96bce2d6797c124331ce0174b16804ff8dfec993
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576107"
---
# <a name="subcontract-line-resources"></a>Recursos de línea de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplica a:** implementación simplificada: de oferta a facturación proforma_

En Dynamics 365 Project Operations, un proveedor puede especificar los recursos que se utilizarán para suministrar la capacidad de recursos que se está comprando en la línea de subcontrato por tiempo.

## <a name="create-subcontract-line-resources"></a>Crear recursos de línea de subcontrato

Para crear recursos de línea de subcontrato, siga estos pasos.

1. En el panel de navegación, seleccione **Subcontratos** y abra el subcontrato con el que quiere trabajar.
2. Abra la línea de subcontrato para el tiempo en el que desea especificar los recursos del proveedor.
3. En la pestaña **Recursos de la línea de subcontrato**, en la subcuadrícula, seleccione **Nuevo recurso de línea de subcontrato**.
4. En la página **Nuevo recurso de línea de subcontratación**, ingrese la información requerida y luego seleccione **Guardar y cerrar**.

La siguiente tabla explica los campos del recurso de línea de subcontrato.

| Campo | Descripción | Impacto funcional |
| ----- | ----------- | ----------------- |
| Recurso que se puede reservar | Seleccione un recurso que se pueda reservar del tipo **Trabajador contratado** que desee utilizar como recurso en la línea de subcontratación.| Si no ha creado un recurso que se pueda reservar para el trabajador contratado, deje este campo vacío. Se creará un recurso que se puede reservar cuando guarde el registro.  |
| CONTACTO | Puede crear su recurso de línea de subcontratación a partir de un contacto existente. Utilice la búsqueda para ver la lista de contactos activos en el sistema. Seleccione un contacto para el proveedor de este subcontrato. Si el contacto que seleccionó no es un contacto válido para el proveedor en el subcontrato, el registro de recursos de línea de subcontratación no se guardará.| Si no hay un recurso que se pueda reservar para el contacto seleccionado, el sistema crea un recurso reservable para el contacto seleccionado antes de crear el recurso de línea de subcontrato. |
| Usuario | Puede crear un recurso de línea de subcontratación seleccionando un usuario activo. Utilice la búsqueda para ver la lista de usuarios activos del sistema.| Si no hay un recurso que se pueda reservar para el usuario seleccionado, el sistema crea un recurso reservable para el contacto seleccionado antes de crear el recurso de línea de subcontrato. |
| Fecha de inicio | La fecha en que comenzará la asignación del trabajador subcontratado.| Si este recurso se reserva para un período anterior a este rango de fechas, se producirá una advertencia. |
| Fecha de finalización | La fecha en que termina la asignación del trabajador subcontratado.| Si este recurso se reserva para un período posterior a este rango de fechas, se producirá una advertencia. |
| Esfuerzo | El número total de horas de esfuerzo que el trabajador contratado dedicará a esta línea de subcontratación.| Si este recurso se reserva más allá del esfuerzo asignado en este subcontrato, se producirá una advertencia. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
