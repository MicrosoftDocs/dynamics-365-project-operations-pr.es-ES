---
title: Procesamiento de recibos de gastos
description: En este tema se proporciona información sobre el procesamiento de reconocimiento óptico de caracteres (OCR) para recibos. Esta característica está diseñada para mejorar la experiencia del usuario cuando se crean informes de gastos en Microsoft Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 067432106742447d2b8fa215ec05bf05f4b41e70
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684341"
---
# <a name="expense-receipt-processing"></a>Procesamiento de recibos de gastos

La entrada de gastos se ha mejorado mediante la introducción del procesamiento de reconocimiento óptico de caracteres (OCR) para recibos. Esta funcionalidad está diseñada para mejorar la experiencia del usuario al crear informes de gastos se crean.

## <a name="key-features"></a>Características clave

- El nombre del comerciante, la fecha y el importe total se extrae de los recibos.
- La función intentará hacer coincidir los recibos sin adjuntar con las transacciones de gastos sin adjuntar.
- Los usuarios pueden crear transacciones de gastos introducidas manualmente a partir de recibos.

## <a name="usage-examples"></a>Ejemplos de uso

Para adjuntar automáticamente recibos que incluyen transacciones con tarjeta de crédito cuando se crea un informe de gastos, haga lo siguiente:

  1. Abra el área de trabajo **Administración de gastos**.
  2. En la pestaña **Recibos**, verifique que existan recibos sin adjuntar. También puede cargar recibos en la pestaña **Recibos**.
  3. En la pestaña **Gastos**, verifique que existan gastos sin adjuntar. Normalmente, el administrador de gastos importa estos gastos del proveedor de la tarjeta de crédito.
  4. Seleccione **Nuevo informe de gastos**. Tenga en cuenta que ahora también puede incluir gastos y recibos cuando cree un informe de gastos. Si agrega tanto gastos como recibos, se activa la coincidencia automática de los recibos con los gastos.

Para crear un gasto o hacer coincidir un gasto de un recibo, haga lo siguiente:

  1. En un informe de gastos, en la pestaña **Recibos**, adjunte un recibo seleccionando **Agregar recibos**.
  2. Debajo de la imagen cargada del recibo, observe las opciones **Crear** y **Coincidir**.

      - Seleccione **Crear** para crear una transacción de gastos introducida manualmente y completar los valores que se extraen del recibo.
      - Si selecciona **Coincidir**, el sistema intenta hacer coincidir un gasto existente con el recibo.

## <a name="installation"></a>Instalación

Esta característica funciona en combinación con la función **Informes de gastos reinventados** para ayudar a simplificar la experiencia de gastos. Esta función solo está disponible para entornos Tier 2+, que son Sandbox y Production.

Para usar estas capacidades avanzadas de gastos, instale el complemento del Servicio de administración de gastos para Microsoft Dynamics 365 Finance y active las características en su instancia. Puede obtener acceso al complemento desde su proyecto en Microsoft Dynamics Lifecycle Services (LCS).

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

Para obtener más información sobre la función reinventada de informes de gastos, consulte [Informes de gastos reinventados](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

**¿Microsoft usa mis datos para sus modelos?**

No, Microsoft ha creado un modelo de aprendizaje automático general para su servicio de procesamiento de recibos. Este modelo no se basa en los recibos que carga.

**¿Dónde está disponible y se procesa esta característica?**

Actualmente, es compatible con Estados Unidos.

**¿A dónde van mis recibos?**

Finance se pondrá en contacto con Cognitive Services para extraer los datos de campo. Cognitive Services conservará una copia de su recibo durante un máximo de 24 horas mientras se procesa. Una vez completado el procesamiento, Cognitive Services eliminará el recibo. Los recibos seguirán almacenándose en Finance.

Para obtener más información, consulte [Habilitar el reconocimiento de recibos con la nueva capacidad de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]