---
title: Emparejar un recibo y un gasto mediante OCR
description: En este tema se proporciona información sobre el procesamiento de reconocimiento óptico de caracteres (OCR) para recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085113"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="a48d1-103">Emparejar un recibo y un gasto mediante OCR</span><span class="sxs-lookup"><span data-stu-id="a48d1-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="a48d1-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no mantenidos, implementación lite: del acuerdo a la factura proforma_</span><span class="sxs-lookup"><span data-stu-id="a48d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a48d1-105">La entrada de gastos se ha mejorado mediante la introducción del procesamiento de reconocimiento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="a48d1-106">Esta funcionalidad está diseñada para mejorar la experiencia del usuario al crear informes de gastos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="a48d1-107">Características clave</span><span class="sxs-lookup"><span data-stu-id="a48d1-107">Key features</span></span>

- <span data-ttu-id="a48d1-108">El sistema extrae el nombre del comerciante, la fecha y el importe total de los recibos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="a48d1-109">El sistema intentará hacer coincidir los recibos sin adjuntar con las transacciones de gastos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="a48d1-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="a48d1-110">Puede crear transacciones de gastos introducidas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="a48d1-111">Adjuntar recibos a un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="a48d1-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="a48d1-112">Para adjuntar automáticamente recibos que incluyen transacciones con tarjeta de crédito cuando se crea un informe de gastos, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="a48d1-113">Abra el área de trabajo **Administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="a48d1-114">En la pestaña **Recibos** , verifique que existan recibos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="a48d1-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="a48d1-115">También puede cargar recibos en la pestaña **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="a48d1-116">En la pestaña **Gastos** , verifique que existan gastos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="a48d1-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="a48d1-117">Normalmente, el administrador de gastos importa estos gastos del proveedor de la tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="a48d1-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="a48d1-118">Seleccione **Nuevo informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-118">Select **New expense report**.</span></span> <span data-ttu-id="a48d1-119">Tenga en cuenta que ahora también puede incluir gastos y recibos cuando cree un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="a48d1-120">Si agrega tanto gastos como recibos, se activa la coincidencia automática de los recibos con los gastos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="a48d1-121">Cerrar o hacer coincidir recibos a un informe de gastos</span><span class="sxs-lookup"><span data-stu-id="a48d1-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="a48d1-122">Para crear un gasto o hacer coincidir un gasto de un recibo, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="a48d1-123">En un informe de gastos, en la pestaña **Recibos** , adjunte un recibo seleccionando **Agregar recibos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="a48d1-124">Debajo de la imagen cargada del recibo, observe las opciones **Crear** y **Coincidir**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="a48d1-125">Seleccione **Crear** para crear una transacción de gastos introducida manualmente y completar los valores que se extraen del recibo.</span><span class="sxs-lookup"><span data-stu-id="a48d1-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="a48d1-126">Si selecciona **Coincidir** , el sistema intenta hacer coincidir un gasto existente con el recibo.</span><span class="sxs-lookup"><span data-stu-id="a48d1-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="a48d1-127">Instalación</span><span class="sxs-lookup"><span data-stu-id="a48d1-127">Installation</span></span>

<span data-ttu-id="a48d1-128">Para utilizar estas funciones avanzadas de gastos, instale el complemento Servicio de administración de gastos para Microsoft Dynamics 365 Finance y active las características en su instancia.</span><span class="sxs-lookup"><span data-stu-id="a48d1-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="a48d1-129">Puede obtener acceso al complemento desde su proyecto en Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a48d1-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="a48d1-130">Inicie sesión en LCS y abra el ambiente deseado.</span><span class="sxs-lookup"><span data-stu-id="a48d1-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="a48d1-131">Vaya a **Detalles completos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="a48d1-132">Seleccione **Mantener** o desplácese hacia abajo hasta la ficha desplegable **Complementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="a48d1-133">Seleccione **Instalar un nuevo complemento**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="a48d1-134">Seleccione **Servicio de administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="a48d1-135">Siga la guía de instalación y acepte los términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="a48d1-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="a48d1-136">Seleccionar **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-136">Select **Install**.</span></span>

<span data-ttu-id="a48d1-137">En el área de trabajo **Administración de características** , active las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="a48d1-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="a48d1-138">Informes de gastos reinventados</span><span class="sxs-lookup"><span data-stu-id="a48d1-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="a48d1-139">Coincidencia automática y creación de gastos a partir de un recibo</span><span class="sxs-lookup"><span data-stu-id="a48d1-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="a48d1-140">Cuando activa estas características, se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a48d1-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="a48d1-141">El área de trabajo **Administración de gastos** existente se reemplaza por el nuevo área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a48d1-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a48d1-142">Se agrega un nuevo elemento de menú para la visibilidad del campo de gastos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a48d1-143">Aún puede abrir la página **Informes de gastos** antigua dirigiéndose a **Administración de gastos > Mis gastos > Informes de gastos**.</span><span class="sxs-lookup"><span data-stu-id="a48d1-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="a48d1-144">Los flujos de trabajo y las aprobaciones aún le llevan a la página de informes de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="a48d1-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="a48d1-145">Los recibos se procesarán a través de Microsoft Azure Cognitive Services y los metadatos se extraerán y agregarán.</span><span class="sxs-lookup"><span data-stu-id="a48d1-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="a48d1-146">Se agrega una opción que le permite crear un informe de gastos que incluye recibos no adjuntos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="a48d1-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="a48d1-147">Una opción que se agrega a los informes de gastos le permite crear una línea de gastos a partir de un recibo, o intenta hacer coincidir un recibo existente con una línea de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="a48d1-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a48d1-148">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="a48d1-148">Frequently asked questions</span></span>

<span data-ttu-id="a48d1-149">**¿Microsoft usa mis datos para sus modelos?**</span><span class="sxs-lookup"><span data-stu-id="a48d1-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="a48d1-150">No, Microsoft ha creado un modelo de aprendizaje automático general para su servicio de procesamiento de recibos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="a48d1-151">Este modelo no se basa en los recibos que carga.</span><span class="sxs-lookup"><span data-stu-id="a48d1-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="a48d1-152">**¿Dónde está disponible y se procesa esta característica?**</span><span class="sxs-lookup"><span data-stu-id="a48d1-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="a48d1-153">Actualmente, es compatible con Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="a48d1-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="a48d1-154">**¿A dónde van mis recibos?**</span><span class="sxs-lookup"><span data-stu-id="a48d1-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="a48d1-155">Finance se pondrá en contacto con Cognitive Services para extraer los datos de campo.</span><span class="sxs-lookup"><span data-stu-id="a48d1-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="a48d1-156">Cognitive Services conservará una copia de su recibo durante un máximo de 24 horas mientras se procesa.</span><span class="sxs-lookup"><span data-stu-id="a48d1-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="a48d1-157">Una vez completado el procesamiento, Cognitive Services eliminará el recibo.</span><span class="sxs-lookup"><span data-stu-id="a48d1-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="a48d1-158">Los recibos seguirán almacenándose en Finance.</span><span class="sxs-lookup"><span data-stu-id="a48d1-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="a48d1-159">Para obtener más información, consulte [Habilitar el reconocimiento de recibos con la nueva capacidad de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="a48d1-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
