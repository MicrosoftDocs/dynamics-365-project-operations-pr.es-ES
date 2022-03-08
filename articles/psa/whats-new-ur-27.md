---
title: Novedades o cambios en la versión de actualización 27, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 27, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ee7bbe888a982e3554ba524c67442437c9be9183a5ee0940ccc3261b4a4992e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985072"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novedades o cambios en la versión de actualización 27, V3, de Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 27. Esta versión tiene un número de compilación de V3.10.45.98 y está disponible con carácter general a través de una actualización automática en enero de 2021.

## <a name="update-release-27"></a>Versión de actualización 27

### <a name="bug-fixes"></a>Correcciones de errores

**Generales**

Se han solucionado los siguientes problemas:

- Los registros generados por complementos en Project Service Automation no se han configurado para su eliminación automática.
- Se produce un error en la actualización automática porque la solución Project Service Automation contiene elementos de título y NavBarArea nulos heredados.

**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- La cuadrícula **Entrada de tiempo** muestra datos incorrectos para el comportamiento de fecha **Independiente de la zona horaria**.
- La cuadrícula **Entrada de tiempo** crea horas incorrectas para el comportamiento de fecha **Independiente de la zona horaria**.
- La búsqueda de tareas no se limita al proyecto seleccionado en la página **Editar entrada de tiempo**.
- La aprobación de tiempo para entradas de tiempo que no sean del proyecto está bloqueada porque el sistema busca un aprobador de proyectos.
- Las entradas correctas en Datos reales muestran un mensaje de error incorrecto.
- Cuando una tarea contiene un valor nulo para el coste real y se actualizan los totales del proyecto, se produce el siguiente error: "La clave especificada no está presente en el diccionario".
- En casos específicos, los filtros **Agrupar por** de la pestaña **Estimación del proyecto** no muestra estimaciones de gastos.
- El intervalo **Horario de verano** no es correcto para las entradas de tiempo.

**Administración del proyecto**

Se han solucionado los siguientes problemas:

- Mejoras del almacenamiento en caché que aumentan el rendimiento relacionado con la carga de la página **Proyecto**.
- Regla de negocio obsoleta que impide que se completen las tareas del proyecto.
- Los perfiles del complemento de Microsoft Project no respetan el calendario del complemento, lo que genera requisitos de recursos incorrectos.
- La creación de proyectos a partir de plantillas establece fechas de asignación incorrectamente e impide generar requisitos de recursos.
- El usuario no puede acceder a las opciones **Categoría**, **Descripción** y **Estado** a través del teclado.
- Los valores de ventas reales del proyecto no incluyen los valores de ventas de tarifas y materiales.
- La agregación de ventas reales y coste real se realiza incorrectamente con diferentes tipos de cambio.
- La descripción de la **Plantilla de horas laborables predeterminada** es engañosa.
- Al degradar una tarea no se quita la **Categoría** en la interfaz de usuario hasta que se actualice.
- Falta una validación para garantizar que no se permita mover un proyecto más allá de su fecha de finalización.

**Sales**

Se han solucionado los siguientes problemas:

- Se genera una excepción de referencia nula en una línea de oferta de proyecto porque **Importar desde la estimación del proyecto** está visible cuando no se ha seleccionado un proyecto.
- Se produce el error "Referencia de objeto no establecida en una instancia de un objeto" al cerrar una oferta como **Lograda**.
- El estado de ajuste no se establece durante una reversión real al desvincular un proyecto de una línea de contrato.
- Cuando Dynamics 365 Field Service y Project Service Automation están instalados, las opciones **Bloquear precios** y **Usar precios actuales** no se muestran al mismo tiempo en la página **Factura**.
- Para el idioma japonés, hay una traducción incoherente con otras páginas basadas en el calendario.
- Se han quitado las acciones **Activar** y **Desactivar** de las entidades **Asociación de lista de precios** en Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]