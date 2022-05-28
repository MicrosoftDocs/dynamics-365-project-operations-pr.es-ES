---
title: Configurar costos estándar para mano de obra y gastos
description: Este tema explica cómo configurar los costos estándar de mano de obra y gastos para un proyecto.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd74da69986a73e933f8cfedce40158555c2ac60
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685353"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar costos estándar para mano de obra y gastos

[!include [banner](../../includes/banner.md)]

Este tema explica cómo configurar los costos estándar de mano de obra y gastos para un proyecto. Esta tarea utiliza el conjunto de datos de USSI.

1. En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de coste (hora)**.
2. Seleccione **Nuevo**.
3. En el campo **Fecha de vigencia**, especifique una fecha.
4. En el campo **Precio de coste**, introduzca un número. Puede configurar un precio de coste estándar para la categoría de proyecto, o puede configurar un precio de coste por número de trabajador, número de proyecto, categoría, fecha o cualquier combinación de estos. El precio de coste que se aplica es el precio de coste con el mayor nivel de detalle.  
5. Seleccione **Guardar**.
6. En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de venta (hora)**.
7. Seleccione **Nuevo**.
8. En el campo **Fecha de vigencia**, especifique una fecha.
9. En el campo **Válido para**, seleccione una opción.
10. En el campo **Precio**, especifique un número. Puede configurar un precio de venta estándar para transacciones por hora o para una categoría de proyecto. También puede configurar los precios de venta por número de trabajador, número de proyecto, categoría, fecha de transacción o cualquier combinación de estos. El precio de venta real, que se aplica cuando un trabajador especifica una transacción en el diario de horas, es el precio de venta con el mayor nivel de detalle. Por ejemplo, si se configura tanto un precio de venta general como un precio de venta específico del trabajador, se utiliza el precio de venta específico del trabajador.  
11. Seleccione **Guardar**.
12. Cierre la página.
13. En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de coste (gasto)**.
14. Seleccione **Nuevo**.
15. En el campo **Fecha de vigencia**, especifique una fecha.
16. En el campo **Precio de coste**, introduzca un número. Se pueden completar varios campos, pero este es el mínimo necesario para guardar el registro.  
17. Seleccione **Guardar**.
18. En el panel de navegación, vaya a **Módulos > Gestión de proyectos y contabilidad > Configuración > Precios > Precio de venta (gasto)**.
19. Seleccione **Nuevo**.
20. En el campo **Fecha de vigencia**, especifique una fecha.
21. En el campo **Válido para**, seleccione una opción.
22. En el campo **Precio**, especifique un número. El precio de venta real, que se aplica cuando un trabajador especifica una transacción en el diario de gastos, es el precio de venta con el mayor nivel de detalle. Por ejemplo, si se configura tanto un precio de venta general como un precio de venta específico del trabajador, se utiliza el precio de venta específico del trabajador.  
23. Seleccione **Guardar**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]