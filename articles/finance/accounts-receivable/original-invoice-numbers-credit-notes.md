---
title: 貸方票での元の請求書への参照
description: このトピックでは、元の請求書番号を関連する貸方表に設定・印刷する方法について説明します。
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5100005"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="fd58b-103">貸方票での元の請求書への参照</span><span class="sxs-lookup"><span data-stu-id="fd58b-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fd58b-104">一部の国や地域では、貸方書の印刷に元の請求書への参照を含めるという法的要件があります。</span><span class="sxs-lookup"><span data-stu-id="fd58b-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="fd58b-105">このトピックでは、元の請求書番号を関連する貸方表に設定・印刷する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd58b-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="fd58b-106">Prerequisites</span></span>

- <span data-ttu-id="fd58b-107">**機能管理** ワークスペースで、**販売およびプロジェクト請求レポートの請求の貸方転記レイアウト** 機能を有効 にします。</span><span class="sxs-lookup"><span data-stu-id="fd58b-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="fd58b-108">詳細については [機能管理の概要](../../fin-and-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd58b-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="fd58b-109">必要なドキュメントの印刷可能な形式については、印刷管理で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd58b-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="fd58b-110">このトピックで説明する機能は、以下のドキュメントに適用されます:</span><span class="sxs-lookup"><span data-stu-id="fd58b-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="fd58b-111">**売掛金勘定**</span><span class="sxs-lookup"><span data-stu-id="fd58b-111">**Accounts receivable**</span></span>

- <span data-ttu-id="fd58b-112">自由書式の訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-112">Free text credit note</span></span>
- <span data-ttu-id="fd58b-113">顧客訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-113">Customer credit note</span></span>

<span data-ttu-id="fd58b-114">**プロジェクト管理および会計**</span><span class="sxs-lookup"><span data-stu-id="fd58b-114">**Project management and accounting**</span></span>

- <span data-ttu-id="fd58b-115">プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="fd58b-116">売掛金のパラメーターを設定する</span><span class="sxs-lookup"><span data-stu-id="fd58b-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="fd58b-117">これらの手順に従って、元の請求書への参照が関連する訂正票に印刷されるかどうかを制御するパラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="fd58b-118">**売掛金勘定** \> **設定** \> **売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="fd58b-119">**更新** タブの **請求書** クイックタブで、**クレジット請求書のレイアウトを販売請求書とプロジェクト請求書レポートに適用する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![売掛金のパラメーターを構成する](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="fd58b-121">元の請求書への参照を定義する</span><span class="sxs-lookup"><span data-stu-id="fd58b-121">Define references to original invoices</span></span>

<span data-ttu-id="fd58b-122">以下の手順を使用して、文書の種類に基づいて元の請求書への参照を定義します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="fd58b-123">自由書式の訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-123">Free text credit note</span></span>

1. <span data-ttu-id="fd58b-124">**売掛金勘定** \> **請求書** \> **すべての自由書式の請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="fd58b-125">新しい貸方書を作成するか、既存の貸方書を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="fd58b-126">請求書を開きます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-126">Open the invoice.</span></span>
4. <span data-ttu-id="fd58b-127">アクション ペインの、**請求書** タブで、**機能** グループから **貸方請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="fd58b-128">元の請求書への参照を入力し、修正の理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![自由形式請求書の参照の定義](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="fd58b-130">顧客訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-130">Customer credit note</span></span>

1. <span data-ttu-id="fd58b-131">**売掛金勘定** \> **注文** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="fd58b-132">訂正する必要のある請求書付き販売注文を選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="fd58b-133">[アクション ウィンドウ] の **販売** タブで、 **訂正票** グループで、**訂正票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="fd58b-134">修正の理由を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-134">Enter the reason for the correction.</span></span> <span data-ttu-id="fd58b-135">請求書の原本への参照が自動的に確立されます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-135">The reference to the original invoice is automatically established.</span></span>

![販売注文の参照を定義する](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="fd58b-137">プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="fd58b-137">Project credit note</span></span>

1. <span data-ttu-id="fd58b-138">**プロジェクト管理および会計** \> **プロジェクト請求書** \> **プロジェクト請求書** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="fd58b-139">訂正する必要のあるプロジェクト請求書を選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="fd58b-140">アクション ペインの、**プロジェクト請求書** タブで、**機能** グループから **訂正票を選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="fd58b-141">**貸方請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="fd58b-142">修正の理由を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd58b-142">Enter the reason for the correction.</span></span> <span data-ttu-id="fd58b-143">請求書の原本への参照が自動的に確立されます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-143">The reference to the original invoice is automatically established.</span></span>

![プロジェクト請求書の参照の定義](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="fd58b-145">訂正票の印刷</span><span class="sxs-lookup"><span data-stu-id="fd58b-145">Printing credit notes</span></span>

<span data-ttu-id="fd58b-146">自由形式、顧客、プロジェクトの貸方伝票を印刷する場合は、元の請求書への参照、修正理由が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd58b-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![印刷された訂正票](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="fd58b-148">請求書の原本への参照が印刷されることを前提として、文書の印刷可能な形式が正しく設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fd58b-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>
