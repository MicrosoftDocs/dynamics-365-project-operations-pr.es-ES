---
title: Información general de aprobaciones
description: Este tema proporciona información sobre cómo trabajar con aprobaciones en Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14c6914cf9b5fb52e7554e51604e79f0920064df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123849"
---
# <a name="approvals-overview"></a>Información general de aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los envíos de tiempo y gastos se mueven a través de un flujo de trabajo de aprobación. Una vez aprobadas las entradas, las transacciones se registran en datos reales o el tiempo se registra en la programación.

## <a name="approvals-workflow"></a>Flujo de trabajo de aprobación
Cuando crea y envía una entrada de tiempo o gastos, se crea una entrada de aprobación. El aprobador del proyecto o su gerente revisa y aprueba su entrada. Si la entrada está relacionada con un proyecto, cuando se apruebe, se crearán los datos reales. Esto permite realizar un seguimiento del coste y la facturación. 

## <a name="approve-an-entry"></a>Aprobar una entrada
El formulario **Aprobaciones** le permite cambiar entre diferentes vistas para que pueda ver los diferentes tipos de aprobaciones.
  
1. Vaya al formulario **Aprobaciones** y seleccione **Gastos**, **Hora** o **Recordatorios**.
2. Revise cada aprobación y seleccione las que desea aprobar.
3. Seleccione **Aprobar** para aprobar las entradas seleccionadas.
El sistema procesará estas entradas y creará datos reales o una reserva.

## <a name="reject-an-entry"></a>Rechazar una entrada
Como aprobador del proyecto, es posible que deba enviar una entrada a un usuario para que la corrija.
  
1. Vaya al formulario **Aprobaciones** y seleccione la entrada a rechazar. 
2. Seleccione **Rechazar**.
3. Opcional: agregue un comentario en el cuadro de diálogo **Comentarios de rechazo** para informar al usuario de por qué se rechaza la entrada.
4. Seleccione **Aceptar**. La entrada se devolverá al usuario.
  
## <a name="recall-entries"></a>Recuperar entradas
En algún punto, es posible que deba recuperar una entrada enviada. Si la entrada no se ha aprobado, se devolverá de inmediato. Sin embargo, una entrada aprobada puede tener un impacto material. Se requiere que el aprobador del proyecto apruebe la recuperación para revertir la transacción en datos reales.

## <a name="specify-project-approvers"></a>Especificar aprobadores de proyecto
Cada proyecto tiene varios miembros del equipo del proyecto. Puede especificar qué miembros del equipo son también aprobadores de proyectos.

1. Vaya al formulario **Proyectos** y abra el proyecto en la lista.
2. En la pestaña **Equipo**, seleccione el miembro del equipo que será aprobador del proyecto y luego seleccione **Editar**.
3. Establezca el campo **Aprobador de proyecto** en **Sí**.
4. Seleccione **Guardar**.
5. Para agregar más aprobadores de proyectos, repita los pasos 2 a 4.

## <a name="configure-the-users-manager"></a>Configurar el administrador de usuarios

1. Vaya a **Configuración** > **Seguridad** > **Usuarios**.
2. Seleccione el usuario al que le está asignando un administrador y en el área **Información de la organización**, seleccione el administrador de la lista. 
3. Seleccione **Guardar**.


