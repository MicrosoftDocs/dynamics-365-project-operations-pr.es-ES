---
title: Procesamiento de recibos de gastos
description: En este tema se proporciona información sobre el procesamiento de reconocimiento óptico de caracteres (OCR) para recibos. Esta funcionalidad está diseñada para mejorar la experiencia del usuario al crear informes de gastos se crean en Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993527"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="cc5b1-104">Procesamiento de recibos de gastos</span><span class="sxs-lookup"><span data-stu-id="cc5b1-104">Expense receipt processing</span></span>

<span data-ttu-id="cc5b1-105">La entrada de gastos se ha mejorado mediante la introducción del procesamiento de reconocimiento óptico de caracteres (OCR) para recibos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="cc5b1-106">Esta funcionalidad está diseñada para mejorar la experiencia del usuario al crear informes de gastos se crean.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="cc5b1-107">Características clave</span><span class="sxs-lookup"><span data-stu-id="cc5b1-107">Key features</span></span>

- <span data-ttu-id="cc5b1-108">El nombre del comerciante, la fecha y el importe total se extrae de los recibos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="cc5b1-109">La función intentará hacer coincidir los recibos sin adjuntar con las transacciones de gastos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="cc5b1-110">Los usuarios pueden crear transacciones de gastos introducidas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="cc5b1-111">Ejemplos de uso</span><span class="sxs-lookup"><span data-stu-id="cc5b1-111">Usage examples</span></span>

<span data-ttu-id="cc5b1-112">Para adjuntar automáticamente recibos que incluyen transacciones con tarjeta de crédito cuando se crea un informe de gastos, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc5b1-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="cc5b1-113">Abra el área de trabajo **Administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="cc5b1-114">En la pestaña **Recibos**, verifique que existan recibos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="cc5b1-115">También puede cargar recibos en la pestaña **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="cc5b1-116">En la pestaña **Gastos**, verifique que existan gastos sin adjuntar.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="cc5b1-117">Normalmente, el administrador de gastos importa estos gastos del proveedor de la tarjeta de crédito.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="cc5b1-118">Seleccione **Nuevo informe de gastos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-118">Select **New expense report**.</span></span> <span data-ttu-id="cc5b1-119">Tenga en cuenta que ahora también puede incluir gastos y recibos cuando cree un informe de gastos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="cc5b1-120">Si agrega tanto gastos como recibos, se activa la coincidencia automática de los recibos con los gastos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="cc5b1-121">Para crear un gasto o hacer coincidir un gasto de un recibo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc5b1-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="cc5b1-122">En un informe de gastos, en la pestaña **Recibos**, adjunte un recibo seleccionando **Agregar recibos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="cc5b1-123">Debajo de la imagen cargada del recibo, observe las opciones **Crear** y **Coincidir**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="cc5b1-124">Seleccione **Crear** para crear una transacción de gastos introducida manualmente y completar los valores que se extraen del recibo.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="cc5b1-125">Si selecciona **Coincidir**, el sistema intenta hacer coincidir un gasto existente con el recibo.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="cc5b1-126">Instalación</span><span class="sxs-lookup"><span data-stu-id="cc5b1-126">Installation</span></span>

<span data-ttu-id="cc5b1-127">Esta característica funciona en combinación con la función **Informes de gastos reinventados** para ayudar a simplificar la experiencia de gastos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="cc5b1-128">Esta función solo está disponible para entornos Tier 2+, que son Sandbox y Production.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="cc5b1-129">Para utilizar estas funciones avanzadas de gastos, instale el complemento Servicio de administración de gastos para Microsoft Dynamics 365 Finance y active las características en su instancia.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="cc5b1-130">Puede obtener acceso al complemento desde su proyecto en Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cc5b1-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="cc5b1-131">Inicie sesión en LCS y abra el ambiente deseado.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="cc5b1-132">Vaya a **Detalles completos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="cc5b1-133">Seleccione **Mantener** o desplácese hacia abajo hasta la ficha desplegable **Complementos de ambiente**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="cc5b1-134">Seleccione **Instalar un nuevo complemento**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="cc5b1-135">Seleccione **Servicio de administración de gastos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="cc5b1-136">Siga la guía de instalación y acepte los términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="cc5b1-137">Seleccionar **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-137">Select **Install**.</span></span>

<span data-ttu-id="cc5b1-138">En el área de trabajo **Administración de características**, active las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="cc5b1-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="cc5b1-139">Informes de gastos reinventados</span><span class="sxs-lookup"><span data-stu-id="cc5b1-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="cc5b1-140">Coincidencia automática y creación de gastos a partir de un recibo</span><span class="sxs-lookup"><span data-stu-id="cc5b1-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="cc5b1-141">Cuando activa estas características, se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="cc5b1-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="cc5b1-142">El área de trabajo **Administración de gastos** existente se reemplaza por el nuevo área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="cc5b1-143">Se agrega un nuevo elemento de menú para la visibilidad del campo de gastos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="cc5b1-144">Aún puede abrir la página **Informes de gastos** antigua dirigiéndose a **Administración de gastos > Mis gastos > Informes de gastos**.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="cc5b1-145">Los flujos de trabajo y las aprobaciones aún le llevan a la página de informes de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="cc5b1-146">Los recibos se procesarán a través de Microsoft Azure Cognitive Services y los metadatos se extraerán y agregarán.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="cc5b1-147">Se agrega una opción que le permite crear un informe de gastos que incluye recibos no adjuntos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="cc5b1-148">Una opción que se agrega a los informes de gastos le permite crear una línea de gastos a partir de un recibo, o intenta hacer coincidir un recibo existente con una línea de gastos existente.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="cc5b1-149">Para obtener más información sobre la función reinventada de informes de gastos, consulte [Informes de gastos reinventados](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="cc5b1-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="cc5b1-150">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="cc5b1-150">Frequently asked questions</span></span>

<span data-ttu-id="cc5b1-151">**¿Microsoft usa mis datos para sus modelos?**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="cc5b1-152">No, Microsoft ha creado un modelo de aprendizaje automático general para su servicio de procesamiento de recibos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="cc5b1-153">Este modelo no se basa en los recibos que carga.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="cc5b1-154">**¿Dónde está disponible y se procesa esta característica?**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="cc5b1-155">Actualmente, es compatible con Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="cc5b1-156">**¿A dónde van mis recibos?**</span><span class="sxs-lookup"><span data-stu-id="cc5b1-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="cc5b1-157">Finance se pondrá en contacto con Cognitive Services para extraer los datos de campo.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="cc5b1-158">Cognitive Services conservará una copia de su recibo durante un máximo de 24 horas mientras se procesa.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="cc5b1-159">Una vez completado el procesamiento, Cognitive Services eliminará el recibo.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="cc5b1-160">Los recibos seguirán almacenándose en Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5b1-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="cc5b1-161">Para obtener más información, consulte [Habilitar el reconocimiento de recibos con la nueva capacidad de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="cc5b1-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]