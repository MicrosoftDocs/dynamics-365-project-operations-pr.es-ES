---
title: Recuperación de IVA
description: Este tema explica cómo recuperar reembolsos en transacciones con impuesto al valor añadido (IVA).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49397592ea002b9da872ac1aa455719b6ca2292e
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960223"
---
# <a name="vat-recovery"></a>Recuperación de IVA 

Para recibir reembolsos en transacciones elegibles de impuesto al valor añadido (IVA), una empresa u organización debe identificar, recopilar, verificar y enviar información precisa. Este proceso incluye múltiples tareas y, dependiendo del tamaño de su empresa, puede incluir varios empleados o roles.

Para recuperar el IVA usando Administración de gastos, se deben completar los siguientes requisitos previos:

- Se deben crear códigos de impuestos para países/regiones que se asignan a categorías de gastos.
- Se debe crear un grupo de impuestos para cada código de impuestos.
- Se debe crear un código de impuestos sobre las ventas de elemento para cada grupo de impuestos sobre las ventas.

Una vez que se completan los requisitos previos, los empleados siguen los siguientes pasos para solicitar reembolsos por transacciones de IVA.

1. En un informe de gastos, introduzca información fiscal sobre transacciones con tarjeta de crédito para identificar reembolsos de IVA elegibles.
2. Verifique que toda la información fiscal esté completa y luego registre el informe de gastos.
3. Gastos de proceso que son elegibles para la recuperación del IVA internacional.
4. Envíe los datos de recuperación del IVA al proveedor externo para presentar declaraciones de recuperación internacionales.
5. Gastos de proceso para la recuperación del IVA nacional.

Las siguientes secciones proporcionan ejemplos que muestran cómo los empleados de Contoso completan cada paso.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>En un informe de gastos, introduzca información fiscal sobre transacciones con tarjeta de crédito para identificar reembolsos de IVA elegibles

Nancy, una representante de ventas de Contoso que reside en los Estados Unidos, regresó recientemente de un viaje de ventas al Reino Unido. Durante el viaje, incurrió en algunos gastos de tarjetas de crédito personales para las comidas. Nancy ahora debe crear un informe de gastos para conciliar sus gastos.

Cuando Nancy ingresa información en su informe de gastos, selecciona **Reino Unido** en el campo **País/región** de la página **Editar informe de gastos**. A continuación, se filtra la lista de grupos de impuestos sobre las ventas para que solo muestre los grupos que se aplican al Reino Unido. Nancy selecciona el grupo de impuestos sobre las ventas **Reino Unido 001** y luego selecciona el grupo de impuestos sobre las ventas de artículos **Comidas**. A continuación, ella agrega una nueva transacción de su alojamiento. Debido a que solo hay un grupo de impuestos sobre las ventas y un grupo de impuestos sobre las ventas de elementos para alojamiento en el Reino Unido, esta información se completa automáticamente en el informe de gastos de Nancy.

Según la directiva de Contoso, todos los gastos deben tener un recibo correspondiente. Por lo tanto, cuando Nancy guarda su informe de gastos, recibe un mensaje que indica que debe adjuntar un recibo por cada transacción que anotó en su informe de gastos. Nancy verifica que haya adjuntado una imagen digital de cada recibo de transacción a su informe de gastos y luego envía su informe para su aprobación. Luego envía los recibos en papel al equipo de procesamiento administrativo. Este equipo enviará los datos de recuperación del IVA al proveedor externo que presente las declaraciones internacionales de recuperación del IVA para Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Verifique que toda la información fiscal esté completa y luego registre el informe de gastos

April, la coordinadora de proveedores de Contoso puede debe introducir cualquier información fiscal que falte de un informe de gastos antes de poder publicar el informe. Ella abre la página **Detalles del informe de gastos** y ve el informe de gastos aprobado de Nancy. April luego abre el informe de gastos para ver los detalles de las transacciones. Ella ve que Nancy no introdujo a un grupo de impuestos sobre las ventas de artículos para una de las transacciones. Debido a que no se proporciona esta información, April no puede registrar el informe de gastos. Por lo tanto, April mira en la página **Configuraciones de impuestos** en Gestión de gastos y busca el grupo de impuestos sobre las ventas de artículos adecuado para el país/región y el tipo de transacción. April ahora puede contabilizar el informe de gastos en el libro mayor.

Cuando April registra el informe de gastos, se crea un elemento de trabajo recuperable de IVA. Este elemento de trabajo se asigna a un miembro del equipo de procesamiento de administración. April recibe un mensaje que confirma que la contabilización se realizó correctamente. Este mensaje también enumera el número de transacciones de IVA que se identificaron para su recuperación.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Gastos de proceso que son elegibles para la recuperación del IVA internacional

Arnie, miembro del equipo de administración de Contoso, es responsable de confirmar que toda la información requerida para la recuperación del IVA esté incluida en los informes de gastos. Abre la página **Recuperación de impuestos sobre gastos** y selecciona el informe de gastos que presentó Nancy. Arnie verifica que todos los recibos requeridos estén adjuntos y que se ingresaron el grupo de impuestos sobre las ventas y los códigos de impuestos sobre las ventas del artículo correctos.

Cuando Arnie recibe los recibos en papel de Nancy, verifica los recibos en papel contra los recibos digitales y luego cambia el estado del informe de gastos a **Listo para recuperación**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Envíe los datos de recuperación del IVA al proveedor externo para presentar declaraciones de recuperación internacionales

Cuando Arnie está listo para enviar los datos del informe de gastos al proveedor externo que presentará las declaraciones de recuperación del IVA, abre la página **Recuperación de impuestos sobre gastos**. Filtra la página para que muestre solo los informes de gastos que están marcados como **Listo para recuperación**. Arnie luego selecciona **Archivo** &gt; **Exportar a Excel**. La información de IVA de los informes de gastos se exporta a una hoja de cálculo de Microsoft Excel. Arnie envía esta hoja de trabajo al proveedor externo e incluye un mensaje que indica que los recibos en papel se enviaron por mensajería.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Gastos de proceso para la recuperación del IVA nacional

Arnie debe verificar que las transacciones del informe de gastos sean elegibles para la recuperación del IVA y que los recibos digitales estén adjuntos a los informes. Para comenzar a procesar los gastos elegibles para la recuperación nacional, Arnie abre la página **Recuperación de impuestos sobre gastos** y selecciona el informe de gastos que requiere verificación. Verifica que los recibos estén a nombre de la empresa y no del empleado. Para la recuperación del IVA, los recibos deben estar a nombre de la empresa. Arnie confirma que se aplicaron el grupo de impuestos sobre las ventas y los códigos de impuestos sobre las ventas de artículos correctos.

Cuando Arnie recibe los recibos en papel, cambia el estado del informe de gastos a **Listo para recuperación**. Luego puede presentar la declaración ante la autoridad fiscal correspondiente. En este caso, la autoridad fiscal apropiada de los Estados Unidos es el Servicio de Impuestos Internos (IRS).
