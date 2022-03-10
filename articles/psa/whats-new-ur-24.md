---
title: Novedades o cambios en la versión de actualización 24, V3, de Project Service Automation
description: En este tema se muestran las características y correcciones que están disponibles en la versión de actualización 24, V3, de Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998077"
---
# <a name="project-service-automation-update-release-24-v3"></a>Versión de actualización de Project Service Automation 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nos complace anunciar la última actualización de la aplicación Project Service Automation para Dynamics 365. Esta versión incluye algunas mejoras importantes en la calidad, el rendimiento y la facilidad de uso. Esta versión es compatible con Dynamics 365 9.x. Para actualizar a esta versión, visite la página de soluciones en línea del Centro de administración para Dynamics 365 para instalar la actualización. Para obtener más información, consulta [Instalar, actualizar o quitar una solución preferida](/power-platform/admin/install-remove-preferred-solution).

En este tema se muestran las características y correcciones que son nuevas o que han cambiado para Project Service Automation V3, versión de actualización 24. Esta versión tiene un número de compilación de V 3.10.42.43 y está disponible con carácter general a través de una actualización automática en octubre de 2020.

## <a name="update-release-24"></a>Versión de actualización 24

### <a name="bug-fixes"></a>Correcciones de errores

**Sales**

Se han solucionado los siguientes problemas:

- Problema al establecer la lista de precios predeterminada de productos.
- El rendimiento de Ganar una oferta es lento debido a la lista de precios incorporada y la copia de registros de precios de rol.
- **Contrato de proyecto/Centro de ventas** > **Elemento de línea de productos/Cantidad de línea de pedido** se redondea automáticamente al número entero más cercano.
- Eleve a privilegios del sistema al leer listas de precios.
- Copie los campos de la dirección del cliente **address1_freighttermscode** y **address1_shippingmethodcode** en Oferta/Pedido. 


**Tiempo y gasto**

Se han solucionado los siguientes problemas:

- La **Cuadrícula de entrada de tiempo** no es compatible con el comportamiento de fecha **Solo fecha**.
- La **Entrada de tiempo** no se actualiza automáticamente. Se requiere una actualización manual.
- No se pueden importar las entradas de tiempo de una asignación cuando haya una pausa (0 horas) en las asignaciones de un recurso.
- Al crear una entrada de tiempo, establezca el inicio lo mismo que **msdyn_date**.
- Vuelva a habilitar la edición masiva para la entrada de tiempo.

**Administración de recursos**

Se han solucionado los siguientes problemas:

- Intentar actualizar el estado de una reserva entre días sin un requisito lanzará una excepción de referencia nula.
- Error al cargar la **Vista de conciliación**.


**Administración del proyecto**

Se han solucionado los siguientes problemas:

- En la **Programación del proyecto**, al cambiar de **Manual** a **Automático**, el autoguardado no se completa.
- Los costes de gastos no deben calcularse en función de la variación en la **Cuadrícula de seguimiento de proyectos**.
- Un comportamiento incoherente para la columna **Etiqueta de estimaciones** durante la carga en comparación con cambiar el tipo **Fases temporales**.
- El coste real de un proyecto puede que no refleje los totales de **Datos reales**.
- **Fecha de finalización estimada** en la pestaña **Resumen** no coincide con la **Programación de WBS**.
- **Actualizar horas reales** en una sangría anulada no funciona correctamente.
- Un jefe de proyecto fuera de la raíz **BU** no puede crear un proyecto.
- Los cambios en la tarea o categoría de **Estimaciones de gastos** no se conservan.
- **Copia de contrato** copia las programaciones de facturación y el estado de ejecución.
- El botón **Actualizar datos reales** calcula incorrectamente las tareas de resumen.
- Complemento de Microsoft Project: corrige el error de referencia nula si algún miembro del equipo tiene una unidad de recursos vacía.



[!INCLUDE[footer-include](../includes/footer-banner.md)]