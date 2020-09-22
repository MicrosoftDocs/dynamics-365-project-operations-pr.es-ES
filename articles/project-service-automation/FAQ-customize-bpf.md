---
title: ¿Cómo personalizo el flujo de proceso de negocio de las fases del proyecto?
description: Información general sobre cómo personalizar el flujo de proceso de negocio de fases del proyecto?
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755961"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>¿Cómo personalizo el flujo de proceso de negocio de las fases del proyecto?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Existe una limitación conocida en versiones anteriores de la aplicación Project Service que los nombres de las fases en el flujo de proceso de negocio de las fases de proyecto deben coincidir exactamente con los nombres esperados en inglés (**Quote**, **Plan**, **Close**). En caso contrario, la lógica de negocios, que se basan en nombres de fases en inglés, no funciona correctamente. Por eso no se ven acciones familiares como **Cambiar proceso** o **Editar proceso** disponibles en el formulario de proyecto, y no se fomenta la personalización del flujo de proceso de negocio. 

Esta limitación se ha abordado en la versión 2.4.5.48 y posteriores. Este artículo ofrece las soluciones alternativas sugeridas si necesita personalizar el flujo de proceso de negocio predeterminado para versiones anteriores.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>La lógica de negocios requiere un coincidencia exacta con nombres de fases en inglés

El flujo de proceso de negocio de las fases del proyecto incluye lógica de negocios que controla los comportamientos siguientes en la aplicación:
- Cuando el proyecto se asocia a una oferta, el código establece el flujo de proceso de negocio en la fase **Quote**.
- Cuando el proyecto se asocia a un contrato, el código establece el flujo de proceso de negocio en la fase **Plan**.
- Cuando el flujo de proceso de negocio avanza a la fase **Close** , se desactiva el registro de proyecto. Cuando se desactiva el proyecto, el formulario y la estructura de descomposición del trabajo (WBS) del proyecto se establecen en de solo lectura, se liberan las reservas de recurso con nombre y se desactivan las listas de precios asociadas.

Esta lógica de negocios se basa en los nombres ingleses para las fases del proyecto. Esta dependencia de los nombres de fases ingleses es la razón principal por la que la personalización del flujo de proceso de negocio de las fases de proyecto no se recomienda, además de la razón por la que no ve acciones de flujo de proceso de negocio comunes como **Cambiar proceso** o **Editar proceso** en la entidad del proyecto.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>¿Qué sucede si no coinciden los nombres de fases con los nombres ingleses?

En la aplicación Project Service versión 1.x en la plataforma 8.2, cuando no coinciden exactamente los nombres de fases en el flujo de proceso de negocio con los nombres de fases en inglés, se omite la lógica de negocios que establece la fase adecuada para ofertas o contratos, o que cierra el proyecto. No se muestra ningún mensajes de error. Por lo tanto parece que puede personalizar el flujo de proceso de negocio de las fases del proyecto. Sin embargo, no verá ninguno de los procesos automáticos trabajando para citas, contratos, y cierre de proyecto.

En la aplicación Project Service versión 2.4.4.30 o anterior en la plataforma 9.0, se produjo un cambio arquitectónico relevante para los flujos de proceso de negocio, que requerían una reescritura de la lógica de negocios de flujo de proceso de negocio. Por ello, si no coinciden los nombres de fases de procesos con los nombres ingleses esperados, aparece un mensaje de error. 

Por tanto, si desea personalizar el flujo de proceso de negocio de las fases de proyecto para la entidad de proyecto, solo puede agregar nuevas fases al flujo de proceso de negocio predeterminado para la entidad de proyecto, manteniendo las fases **Quote**, **Plan** y **Close** como se encuentran. Esta restricción garantiza que no recibe errores de la lógica de negocios que espera los nombres de fases ingleses en el flujo de proceso de negocio.

En la versión 2.4.5.48 o versiones posteriores, la lógica de negocios descrita en este artículo se ha quitado del flujo de proceso de negocio predeterminado para la entidad de proyecto. La actualización a esa versión o posterior le permitirá personalizar o reemplazar el flujo de proceso de negocio predeterminado con uno propio. 

## <a name="workarounds-for-earlier-versions"></a>Soluciones alternativas para versiones anteriores

Si la actualización no es una opción, puede personalizar el flujo de proceso de negocio de las fases de proyecto para la entidad de proyecto de una de estas dos formas:

1. Agregue fases adicionales a la configuración predeterminada, manteniendo los nombres de fases ingleses para **Quote**, **Plan** y **Close**.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de cómo agregar fases a la configuración predeterminada](media/FAQ-Customize-BPF-1.png)
 
2. Cree su propio flujo de proceso de negocio y conviértalo en el flujo de proceso de negocio principal para la entidad de proyecto, lo que le permite tener los nombres de etapa que desee. Sin embargo, si desea usar las mismas fases estándar de proyecto **Quote**, **Plan** y **Close**, necesita realizar algunas personalizaciones que se toman de sus nombres de fases personalizados. La lógica más compleja está en el cierre del proyecto, que usted puede desencadenar desactivando el registro del proyecto.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de personalización de BFP](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Consideraciones adicionales para la aplicación Project Service versión 2.4.4.30 o anterior en la plataforma 9.0

En Project Service 2.4.4.30 o anterior en la plataforma 9.0, con un flujo de proceso de negocio personalizado, el campo **Nombre de fase** en la entidad de proyecto usada en las vistas de gráfico y lista de proyecto **Proyecto por fase** no se actualizará porque está emparejado con el flujo de proceso de negocio predeterminado de las fases del proyecto. Puede resolver este problema con los pasos siguientes:

- Agregue un campo personalizado para capturar la fase actual del flujo de proceso de negocio que se actualiza cuando el usuario avanza a través del flujo de proceso de negocio personalizado.

- Modifique el gráfico **Proyecto por fase** para trabajar con el campo personalizado en lugar de la configuración predeterminada.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Pasos para crear su propio flujo de proceso de negocio para la entidad de proyecto

Siga estas instrucciones para crear su propio flujo de proceso de negocio para la entidad de proyecto:

1. Vaya a **Configuración** > **Centro de procesos**. No copie el flujo de proceso de negocio de las fases de proyecto porque también se copiará la lógica de negocio de Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de personalización de BFP](media/FAQ-Customize-BPF-3.png)

2. Use el diseñador del proceso para crear los nombres de fases que desee. Si desea la misma funcionalidad que las fases predeterminadas para **Quote**, **Plan** y **Close**, tendrá que crearla basada en los nombres de fase del flujo de proceso de negocio personalizado.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla del diseñador del proceso usado para personalizar BPF](media/FAQ-Customize-BPF-4.png) 

3. En el diseñador del proceso, haga clic en **Ordenar flujo de proceso** para convertir el flujo de proceso de negocio personalizado en el flujo de proceso de negocio principal para la entidad de proyecto moviéndolo por el flujo de proceso de negocio de las fases del proyecto hasta la parte superior de la lista.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla del uso de Ordenar flujo de proceso](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Los pasos siguientes se aplican a la aplicación Project Service 2.4.4.30 o anterior de la plataforma 9.0

4. Agregue un nuevo campo personalizado a la entidad de proyecto para capturar las fases personalizadas en el flujo de proceso de negocio personalizado. Deberá agregar lógica de negocios (complemento/flujo de trabajo) para actualizar este campo cuando la fase del flujo de proceso de negocio personalizado se actualice.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de personalizar la entidad de proyecto](media/FAQ-Customize-BPF-6-720.png)

5. Modificar el gráfico **Proyecto por fase** para usar su nuevo campo personalizado para fases.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de usar el gráfico Proyecto por fase](media/FAQ-Customize-BPF-7-720.png)

6. Modifique cualquier vista de la entidad de proyecto para incluir su nuevo campo personalizado para fases.

   > [!div class="mx-imgBorder"] 
   > ![Captura de pantalla de cómo modificar vistas en la entidad de proyecto](media/FAQ-Customize-BPF-8-720.png)

