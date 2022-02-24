---
title: Área de trabajo móvil de gestión de gastos
description: En este tema se proporciona información sobre el área de trabajo móvil Administración de gastos. Este área de trabajo permite a los usuarios capturar y cargar un recibo para luego adjuntarlo a un informe de gastos. Los usuarios también pueden crear rápidamente una línea de gastos mediante un recibo adjunto y crear y administrar sus informes de gastos.
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7eccf5cd234df6ca4fc4c83b581f6c4c22b3396f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993662"
---
# <a name="expense-management-mobile-workspace"></a>Área de trabajo móvil de gestión de gastos

En este tema se proporciona información sobre el área de trabajo móvil **Administración de gastos**. Este área de trabajo permite a los usuarios capturar y cargar un recibo para luego adjuntarlo a un informe de gastos. Los usuarios también pueden crear rápidamente una línea de gastos mediante un recibo adjunto y crear y administrar sus informes de gastos. Además, los aprobadores pueden utilizar el área de trabajo móvil **Administración de gastos** para ver los informes de gastos que se les asignan y aprobar o rechazar esos informes de gastos.


Este espacio de trabajo móvil está diseñado para utilizarse con la aplicación móvil de operaciones unificadas de Dynamics 365.


## <a name="overview"></a>Introducción

Muchas organizaciones requieren que se adjunte una copia de un recibo a un informe de gastos relacionado con viajes o con el negocio que un empleado envía para su reembolso. El área de trabajo móvil **Administración de gastos** permite a los usuarios crear rápidamente nuevas líneas de gastos en el dispositivo móvil de su elección usando una foto adjunta de un recibo. Como alternativa, los usuarios pueden capturar una foto de un recibo y luego adjuntarla más adelante a un informe de gastos. Los empleados también pueden crear y administrar sus informes de gastos y luego enviarlos para su aprobación y reembolso mediante su dispositivo móvil.


Concretamente, el área de trabajo **Administración de gastos** permite a los usuarios realizar estas tareas:

- Tome una foto de un recibo y cárguela en Dynamics 365 Finance. A continuación, puede adjuntar esa foto a un informe de gastos más adelante.
- Cargue un archivo como recibo capturado. A continuación, puede adjuntar ese archivo a un informe de gastos más adelante.
- Cree una nueva línea de gastos utilizando un recibo adjunto. Después, puede agregar el elemento de línea a un informe de gastos más adelante y enviarlo para su aprobación y reembolso.

También puede usar estas características:

- Cree un nuevo informe de gastos.
- Adjunte transacciones con tarjetas de crédito y otros gastos creados previamente a un informe de gastos.
- Cree nuevos gastos para un informe de gastos.
- Adjunte un recibo a cualquier gasto de un informe de gastos, ya sea tomando una foto del recibo o cargando un archivo como recibo capturado.
- Dependiendo de la directiva de gastos de la empresa, agregue la lista de invitados a un gasto.
- Dependiendo de la directiva de gastos de la empresa, desglose los gastos.
- Envíe un informe de gastos para su aprobación y reembolso.
- Apruebe o rechace los informes de gastos para los que es un aprobador asignado.

## <a name="prerequisites"></a>Requisitos previos
Los requisitos previos varían según la versión que se haya implementado en la organización.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisitos previos si usa Dynamics 365 Finance 
Si se ha implementado Finance para la organización, el administrador del sistema debe publicar el área de trabajo móvil **Administración de gastos**. Para obtener instrucciones, consulte [Publicar espacios de trabajo para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Requisitos previos si usa la versión 1611 con Platform update 3 o posterior
Si se implementó la versión 1611 con Platform update 3 o posterior para su organización, el administrador del sistema debe completar los siguientes requisitos previos. 

<table>
<thead>
<tr class="header">
<th>Requisito previo</th>
<th>Rol</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementar KB 4019015.</td>
<td>Administrador del sistema</td>
<td>KB 4019015 es una actualización de X++ o revisión de metadatos que contiene el área de trabajo móvil <strong>Administración de gastos</strong>. Para implementar KB 4019015, su administrador del sistema debe seguir estos pasos.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">Descargue la revisión de metadatos de Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">Instale la revisión de metadatos</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Cree un paquete que se pueda implementar</a> que contiene los modelos <strong>ApplicationSuite</strong> y <strong>ExpenseMobile</strong> y luego cargue el paquete que se puede implementar en LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Aplique el paquete que se puede implementar</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publique el área de trabajo <strong>Administración de gastos</strong>.</td>
<td>Administrador del sistema</td>
<td>Consulte <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar espacios de trabajo para dispositivos móviles</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Descargar e instalar la aplicación móvil Dynamics 365 for Operations
Descargar e instalar la aplicación móvil Dynamics 365 Unified Ops:

- [Para teléfonos Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Para iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar sesión en la aplicación móvil
1. Inicie la aplicación en el dispositivo móvil.
2. Introduzca la URL de Dynamics 365.
4. La primera vez que inicie sesión, se le solicitará su nombre de usuario y contraseña. Especifique sus credenciales.
5. Después de iniciar sesión, se muestran los espacios de trabajo disponibles para su empresa. Tenga en cuenta que si el administrador del sistema publica un nuevo espacio de trabajo más tarde, deberá actualizar la lista de espacios de trabajo para dispositivos móviles.


[![Deslizar para actualizar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturar un recibo mediante el área de trabajo móvil Administración de gastos

1. En el dispositivo móvil, abra el área de trabajo **Administración de activos**.
2. Seleccione **Capturar recibo**.
3. Seleccione **Tomar foto** o **Elegir imagen**.
4. Siga uno de estos pasos:

    - Si seleccionó **Tomar foto**, siga estos pasos:

        1. Será dirigido a la cámara de su dispositivo móvil para que pueda tomar una foto del recibo. Cuando haya terminado de tomar una foto, seleccione **Aceptar** para aceptar la foto.
        2. Opcional: introduzca un nombre para la foto e introduzca las notas.

    - Si seleccionó **Elegir imagen**, siga estos pasos:

        1. Seleccione una imagen en la lista.
        2. Opcional: introduzca un nombre para la imagen e introduzca las notas.

5. Seleccione **Listo**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduzca rápidamente los gastos mediante el área de trabajo móvil Administración de gastos
1. En el dispositivo móvil, abra el área de trabajo **Administración de activos**.
2. Seleccione **Entrada rápida de gastos**.
3. Seleccione la categoría del gasto. Verá una lista de categorías de gastos que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su categoría no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por categoría de gastos o cambie para buscar por tipo de gasto.
4. Introduzca la fecha de transacción del gasto.
5. Opcional: introduzca el comerciante para el gasto.
6. Introduzca el importe del gasto.
7. Seleccione la divisa del gasto. Verá una lista de códigos de divisa que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 400 divisas, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su divisa no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por divisa o cambie para buscar por nombre.
8. Seleccione **Tomar foto** o **Elegir imagen**.
9. Siga uno de estos pasos:

    - Si seleccionó **Tomar foto**, será dirigido a la cámara de su dispositivo móvil para que pueda tomar una foto del recibo. Cuando haya terminado de tomar una foto, seleccione **Aceptar** para aceptar la foto.
    - Si seleccionó **Elegir imagen**, seleccione una imagen de la lista.

10. Seleccione **Listo**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Aprobar un informe de gastos mediante el área de trabajo móvil Administración de gastos (si utiliza la actualización de julio de 2017)
1. En el dispositivo móvil, abra el área de trabajo **Administración de activos**.
2. **Aprobaciones de gastos** muestra el número de informes de gastos que se le asignan para su aprobación. El número se actualiza aproximadamente cada 30 minutos. Seleccione **Aprobaciones de gastos**.

    Se muestra la lista de informes de gastos que se le asignan para su aprobación.
    
3. Seleccione un informe de gastos para ver sus detalles.
4. Seleccione un gasto para ver sus detalles. La información que se muestra para un gasto incluye detalles del recibo, el invitado y el desglose.
5. De nuevo en la página **Informe de gastos**, seleccione esta opción para aprobar o rechazar el informe de gastos.
6. Introduzca cualquier comentario para la acción de aprobación.
7. Seleccione **Listo**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Cree un nuevo informe de gastos y envíelo para su aprobación mediante el área de trabajo móvil Administración de gastos (si utiliza la actualización de julio de 2017)
1. En el dispositivo móvil, abra el área de trabajo **Administración de activos**.
2. Seleccione **Entrada de gastos**.
3. Seleccione **Nuevo informe** o seleccione un informe de gastos existente en la lista.
4. Para nuevos informes de gastos, introduzca el objetivo y cualquier información adicional que esté disponible. Esta información varía en función de la forma en que la administración de gastos esté configurada para su empresa.
5. Seleccione **Listo**.
6. Para agregar gastos existentes, como transacciones con tarjeta de crédito, al informe de gastos, seleccione **Adjuntar**.
7. Seleccione uno o varios gastos de la lista.
8. Seleccione **Listo**.
9. Para agregar un nuevo gasto al informe de gastos, seleccione **Nuevo gasto**.
10. Seleccione la categoría del gasto. Verá una lista de categorías de gastos que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su categoría no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por categoría de gastos o cambie para buscar por tipo de gasto.
11. Opcional: introduzca el comerciante para el gasto.
12. Introduzca la fecha de transacción del gasto.
13. Introduzca el importe del gasto.
14. Seleccione la divisa del gasto. Verá una lista de códigos de divisa que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 400 divisas, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su divisa no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por divisa o cambie para buscar por nombre.
15. Seleccione **Listo**.
16. Para agregar más detalles al gasto, seleccione **Agregar más detalles**. Los campos que están disponibles dependen de la configuración de la administración de gastos de su empresa.
17. Si la directiva de la empresa requiere un recibo del gasto, seleccione **Recibos** y siga estos pasos:

    1. Seleccione **Capturar recibo** o **Adjuntar recibo**.
    2. Siga uno de estos pasos:

        - Si seleccionó **Capturar recibo**, siga estos pasos:

            1. Seleccione **Tomar foto** o **Elegir imagen**.
            2. Siga uno de estos pasos:

                - Si seleccionó **Tomar foto**, siga estos pasos:

                    1. Será dirigido a la cámara de su dispositivo móvil para que pueda tomar una foto del recibo. Cuando haya terminado de tomar una foto, seleccione **Aceptar** para aceptar la foto.
                    2. Opcional: introduzca un nombre para la foto e introduzca las notas.

                - Si seleccionó **Elegir imagen**, siga estos pasos:

                    1. Seleccione una imagen en la lista.
                    2. Opcional: introduzca un nombre para la imagen e introduzca las notas.

            3.  Seleccione **Listo**.

        - Si seleccionó **Adjuntar recibo**, siga estos pasos:

            1.  Seleccione una o varias imágenes de la lista.
            2.  Seleccione **Listo**.

    3. Seleccione el botón **Atrás** para volver a los detalles de gastos.

18. Si la directiva de la empresa requiere invitados para el gasto, seleccione **Invitados** y siga estos pasos:

    1. Seleccione **Invitado**, **Invitados anteriores** o **Compañeros**.
    2. Siga uno de estos pasos:

        - Si seleccionó **Invitado**, siga estos pasos:

            1. Especifique el nombre del invitado.
            2. Opcional: introduzca la organización o el país del invitado.
            3. Opcional: introduzca el título del invitado.
            4. Seleccione **Listo**.

        - Si seleccionó **Invitados anteriores**, siga estos pasos:

            1. Seleccione uno o varios invitados anteriores de la lista. Verá una lista de invitados anteriores que ha agregado a informes de gastos anteriores que se cargan en su aplicación para uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su invitado anterior no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por nombre o cambie para buscar por organización, país o título.
            2. Seleccione **Listo**.

        - Si seleccionó **Compañeros**, siga estos pasos:

            1. Seleccione uno o varios compañeros de la lista. Verá una lista de compañeros que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su compañero no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por nombre o cambie para buscar por empresa o título.
            2. Seleccione **Listo**.

    3. Seleccione el botón **Atrás** para volver a los detalles de gastos.

19. Si la directiva de la empresa requiere que el gasto se detalle, seleccione **Desglosar** y siga estos pasos:

    1. Seleccione la primera fecha para desglosar.
    2. Seleccione **Agregar desglose**.
    3. Seleccione la subcategoría para el desglose del gasto. Verá una lista de subcategorías de gastos que se cargan en su aplicación para su uso sin conexión. De forma predeterminada, se cargan 50 elementos, pero un desarrollador puede cambiar este número. Para obtener más información, los desarrollados deben consultar [Plataforma para dispositivos móviles](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Si su subcategoría no está en la lista, seleccione **Buscar** para hacer una búsqueda en línea. Busque por nombre de subcategoría de gastos.
    4. Introduzca el importe de la transacción para el desglose.
    5. Edite la fecha de la transacción si es necesario.
    6. Seleccione **Listo**.
    7. Repita los pasos anteriores hasta que haya terminado de agregar todos los desgloses para la fecha seleccionada.
    8. Para días adicionales, puede seleccionar **Copiar al día siguiente** para copiar los desgloses al día siguiente. Como alternativa, puede seleccionar la fecha para desglosar y luego agregar desgloses como lo hizo para la primera fecha.
    9. Una vez que haya terminado de desglosar el gasto, seleccione el botón **Atrás** para volver a los detalles del gasto.

20. Seleccione el botón **Atrás** para volver a la página **Informe de gastos**.
21. Repita los pasos anteriores hasta que haya terminado de agregar todos los gastos.
22. Seleccione **Enviar**.
23. Introduzca cualquier comentario para el aprobador.
24. Seleccione **Listo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]