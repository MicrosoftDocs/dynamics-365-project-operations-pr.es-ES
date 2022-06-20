---
title: Información general de aprobaciones
description: Este artículo proporciona información sobre el trabajo con aprobaciones en Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: d5b5c93dc948992505054ef7b17579aafcdf8f8d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924727"
---
# <a name="approvals-overview"></a>Información general de aprobaciones

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

Los envíos de tiempo, gastos y uso de materiales se desplazan en un flujo de trabajo de aprobaciones. Una vez aprobadas las entradas, las transacciones se registran en datos reales o el tiempo se registra en la programación.

## <a name="approvals-workflow"></a>Flujo de trabajo de aprobación
Cuando crea y envía una entrada de tiempo, gasto o uso de material, se crea un registro de aprobación. El aprobador o administrador del proyecto revisa y aprueba la entrada. Si la entrada está relacionada con un proyecto, los datos reales se crearán cuando se apruebe. Esto permite realizar un seguimiento del coste y la facturación.

## <a name="approve-an-entry"></a>Aprobar una entrada
La página **Aprobaciones** le permite cambiar entre diferentes vistas para que pueda ver los diferentes tipos de aprobaciones.
  
1. Vaya a la página **Aprobaciones** y seleccione **Gastos**, **Hora**, **Uso de material**, o **Retiradas**.
2. Revise cada aprobación y seleccione las que desea aprobar.
3. Seleccione **Aprobar** para aprobar las entradas seleccionadas.
El sistema procesa estas entradas y crea datos reales.

## <a name="reject-an-entry"></a>Rechazar una entrada
Como aprobador del proyecto, es posible que deba enviar una entrada a un usuario para que la corrija.
  
1. Vaya a la página **Aprobaciones** y seleccione la entrada que desee rechazar. 
2. Seleccione **Rechazar**.
3. Opcionalmente, puede agregar un comentario en el cuadro de diálogo **Comentarios de rechazo** para informar al usuario de por qué se rechaza la entrada.
4. Seleccione **Aceptar**. La entrada se devolverá al usuario.
  
## <a name="cancel-approval"></a>Cancelar aprobación
En algunos casos, es posible que deba cancelar una entrada aprobada previamente. Cancelar una entrada previamente aprobada tendrá un impacto financiero. 

## <a name="approving-recall-requests"></a>Aprobación solicitudes de retirada
En algunos casos, es posible que un consultor necesite recuperar una entrada aprobada previamente. Cancelar una entrada previamente aprobada tendrá un impacto financiero. Se requiere que el aprobador del proyecto apruebe la retirada para revertir la transacción en Datos reales.

## <a name="specify-project-approvers"></a>Especificar aprobadores de proyecto
Cada proyecto tiene varios miembros del equipo del proyecto. Puede especificar qué miembros del equipo son también aprobadores de proyectos.

1. Vaya a la página **Proyectos** y abra el proyecto en la lista.
2. En la pestaña **Equipo**, seleccione el miembro del equipo que será aprobador del proyecto y luego seleccione **Editar**.
3. Establezca el campo **Aprobador de proyecto** en **Sí**.
4. Seleccione **Guardar**.
5. Para agregar más aprobadores de proyectos, repita los pasos 2 a 4.

## <a name="configure-the-users-manager"></a>Configurar el administrador de usuarios

1. Vaya a **Configuración** > **Seguridad** > **Usuarios**.
2. Seleccione el usuario al que le está asignando un administrador y en el área **Información de la organización**, seleccione el administrador de la lista. 
3. Seleccione **Guardar**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
