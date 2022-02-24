---
title: Capturar un recibo usando OCR
description: En este tema se proporciona información sobre el procesamiento de reconocimiento óptico de caracteres (OCR) para recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499872"
---
# <a name="capture-a-receipt-using-ocr"></a>Capturar un recibo usando OCR

_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_

La entrada de gastos se ha mejorado mediante la introducción del procesamiento de reconocimiento óptico de caracteres (OCR) para recibos. Esta funcionalidad está diseñada para mejorar la experiencia del usuario al crear informes de gastos.

## <a name="key-features"></a>Características clave

- El sistema extrae el nombre del comerciante, la fecha y el importe total de los recibos.
- El sistema intentará hacer coincidir los recibos sin adjuntar con las transacciones de gastos sin adjuntar.
- Puede crear transacciones de gastos introducidas manualmente a partir de recibos.

## <a name="attach-receipts-to-an-expense-report"></a>Adjuntar recibos a un informe de gastos

Para adjuntar automáticamente recibos que incluyen transacciones con tarjeta de crédito cuando se crea un informe de gastos, complete los siguientes pasos.

  1. Abra el área de trabajo **Administración de gastos**.
  2. En la pestaña **Recibos**, verifique que existan recibos sin adjuntar. También puede cargar recibos en la pestaña **Recibos**.
  3. En la pestaña **Gastos**, verifique que existan gastos sin adjuntar. Normalmente, el administrador de gastos importa estos gastos del proveedor de la tarjeta de crédito.
  4. Seleccione **Nuevo informe de gastos**. Tenga en cuenta que ahora también puede incluir gastos y recibos cuando cree un informe de gastos. Si agrega tanto gastos como recibos, se activa la coincidencia automática de los recibos con los gastos.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Cerrar o hacer coincidir recibos a un informe de gastos
Para crear un gasto o hacer coincidir un gasto de un recibo, complete los siguientes pasos.

  1. En un informe de gastos, en la pestaña **Recibos**, adjunte un recibo seleccionando **Agregar recibos**.
  2. Debajo de la imagen cargada del recibo, observe las opciones **Crear** y **Coincidir**.

      - Seleccione **Crear** para crear una transacción de gastos introducida manualmente y completar los valores que se extraen del recibo.
      - Si selecciona **Coincidir**, el sistema intenta hacer coincidir un gasto existente con el recibo.

## <a name="installation"></a>Instalación

Para utilizar estas funciones avanzadas de gastos, instale el complemento Servicio de administración de gastos para Microsoft Dynamics 365 Finance y active las características en su instancia. Puede obtener acceso al complemento desde su proyecto en Microsoft Dynamics Lifecycle Services (LCS).

1. Inicie sesión en LCS y abra el ambiente deseado.
2. Vaya a **Detalles completos**.
3. Seleccione **Mantener** o desplácese hacia abajo hasta la ficha desplegable **Complementos de ambiente**.
4. Seleccione **Instalar un nuevo complemento**.
5. Seleccione **Servicio de administración de gastos**.
6. Siga la guía de instalación y acepte los términos y condiciones.
7. Seleccionar **Instalar**.

En el área de trabajo **Administración de características**, active las siguientes características:

- Informes de gastos reinventados
- Coincidencia automática y creación de gastos a partir de un recibo

Cuando activa estas características, se producen las siguientes acciones:

- El área de trabajo **Administración de gastos** existente se reemplaza por el nuevo área de trabajo.
- Se agrega un nuevo elemento de menú para la visibilidad del campo de gastos.
- Aún puede abrir la página **Informes de gastos** antigua dirigiéndose a **Administración de gastos > Mis gastos > Informes de gastos**.
- Los flujos de trabajo y las aprobaciones aún le llevan a la página de informes de gastos existente.
- Los recibos se procesarán a través de Microsoft Azure Cognitive Services y los metadatos se extraerán y agregarán.
- Se agrega una opción que le permite crear un informe de gastos que incluye recibos no adjuntos coincidentes.
- Una opción que se agrega a los informes de gastos le permite crear una línea de gastos a partir de un recibo, o intenta hacer coincidir un recibo existente con una línea de gastos existente.

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Microsoft usa mis datos para sus modelos?**

No, Microsoft ha creado un modelo de aprendizaje automático general para su servicio de procesamiento de recibos. Este modelo no se basa en los recibos que carga.

**¿Dónde está disponible y se procesa esta característica?**

Actualmente, es compatible con Estados Unidos.

**¿A dónde van mis recibos?**

Finance se pondrá en contacto con Cognitive Services para extraer los datos de campo. Cognitive Services conservará una copia de su recibo durante un máximo de 24 horas mientras se procesa. Una vez completado el procesamiento, Cognitive Services eliminará el recibo. Los recibos seguirán almacenándose en Finance.

Para obtener más información, consulte [Habilitar el reconocimiento de recibos con la nueva capacidad de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
