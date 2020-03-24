---
title: 経費の領収書
description: このトピックでは、領収書の光学式文字認識 (OCR) 処理に関する情報を提供します。 この機能は、Microsoft Dynamics 365 Finance で経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2e819521828b054f70476b1eb061ee08c486d09f
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113689"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="4065e-104">パブリックプレビュー: 経費レシートの処理</span><span class="sxs-lookup"><span data-stu-id="4065e-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="4065e-105">領収書の光学式文字認識 (OCR) 処理の導入により、経費入力が強化されました。</span><span class="sxs-lookup"><span data-stu-id="4065e-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="4065e-106">この機能は、経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。</span><span class="sxs-lookup"><span data-stu-id="4065e-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="4065e-107">主な機能</span><span class="sxs-lookup"><span data-stu-id="4065e-107">Key features</span></span>

- <span data-ttu-id="4065e-108">領収書から販売者名、日付、合計金額を抽出する。</span><span class="sxs-lookup"><span data-stu-id="4065e-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="4065e-109">この機能は、未添付の領収書を未添付の経費トランザクションと照合します。</span><span class="sxs-lookup"><span data-stu-id="4065e-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="4065e-110">ユーザーは、領収書から手動で入力された経費トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4065e-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="4065e-111">使用例</span><span class="sxs-lookup"><span data-stu-id="4065e-111">Usage examples</span></span>

- <span data-ttu-id="4065e-112">**経費精算書の作成時に、クレジット カード トランザクションを含む領収書を自動的に添付します。**</span><span class="sxs-lookup"><span data-stu-id="4065e-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="4065e-113">**経費管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="4065e-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="4065e-114">**領収書**タブで、未添付の領収書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4065e-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="4065e-115">**領収書**タブで領収書をアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4065e-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="4065e-116">**経費**タブで、未添付の経費が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4065e-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="4065e-117">通常、経費管理者は、これらの経費をクレジット カード プロバイダーからインポートします。</span><span class="sxs-lookup"><span data-stu-id="4065e-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="4065e-118">**新しい経費精算書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4065e-118">Select **New expense report**.</span></span> <span data-ttu-id="4065e-119">経費精算書を作成するときに、経費、および領収書を含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4065e-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="4065e-120">経費と領収書の両方を追加すると、経費に対する領収書の自動照合がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="4065e-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="4065e-121">**経費を作成するか、領収書から経費を照合します。**</span><span class="sxs-lookup"><span data-stu-id="4065e-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="4065e-122">経費精算書の**領収書**タブで、**領収書の追加**を選択して領収書を添付します。</span><span class="sxs-lookup"><span data-stu-id="4065e-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="4065e-123">アップロードされた領収書の画像の下に**作成**および**照合**オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4065e-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="4065e-124">**作成**を選択して、手動で入力された経費トランザクションを作成し、領収書から抽出された値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4065e-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="4065e-125">**照合**を選択した場合、システムは既存の経費と領収書を照合しようとします。</span><span class="sxs-lookup"><span data-stu-id="4065e-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="4065e-126">インストール</span><span class="sxs-lookup"><span data-stu-id="4065e-126">Installation</span></span>

<span data-ttu-id="4065e-127">この機能は、**経費精算書の再設計**機能と組み合わせて機能し、経費のエクスペリエンスを簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="4065e-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="4065e-128">これらの高度な経費機能を使用するには、Microsoft Dynamics 365 Finance の経費管理サービス アドインをインストールし、インスタンスの機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4065e-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="4065e-129">Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからアドインにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4065e-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="4065e-130">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="4065e-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="4065e-131">**完全な詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="4065e-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="4065e-132">**メンテナンス**を選択するか、**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="4065e-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="4065e-133">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4065e-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="4065e-134">**経費管理サービス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4065e-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="4065e-135">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="4065e-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="4065e-136">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4065e-136">Select **Install**.</span></span>

<span data-ttu-id="4065e-137">**機能の管理**ワークスペースで、次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4065e-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="4065e-138">経費レポートの再設計</span><span class="sxs-lookup"><span data-stu-id="4065e-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="4065e-139">レシートからの自動照合および経費の作成</span><span class="sxs-lookup"><span data-stu-id="4065e-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="4065e-140">これらの機能をオンにすると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4065e-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="4065e-141">既存の**経費管理**ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="4065e-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="4065e-142">経費フィールド表示の新しいメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="4065e-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="4065e-143">以前の**経費精算書**ページは、**経費管理 > 自分の経費 > 経費精算書**に移動して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4065e-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="4065e-144">ワークフローと承認を行っても、既存の経費精算書ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="4065e-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="4065e-145">領収書は、Microsoft Azure Cognitive Services によって処理され、メタデータが抽出されて追加されます。</span><span class="sxs-lookup"><span data-stu-id="4065e-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="4065e-146">一致する未添付の領収書を含む経費精算書を作成できるオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4065e-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="4065e-147">経費精算書に追加されたオプションを使用すると、領収書から経費明細行を作成したり、既存の領収書を既存の経費明細行と一致させたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="4065e-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="4065e-148">再設計された経費精算書の詳細については、[経費精算書の再設計](ExpenseWorkspaceNew.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4065e-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="4065e-149">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4065e-149">Frequently asked questions</span></span>

<span data-ttu-id="4065e-150">**Microsoft は、モデルにデータを使用しますか ?**</span><span class="sxs-lookup"><span data-stu-id="4065e-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="4065e-151">いいえ、Microsoft は、領収書処理サービス用の一般的な機械学習モデルを構築しています。</span><span class="sxs-lookup"><span data-stu-id="4065e-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="4065e-152">このモデルは、アップロードした領収書に基づいていません。</span><span class="sxs-lookup"><span data-stu-id="4065e-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="4065e-153">**この機能はどこで使用および処理されますか ?**</span><span class="sxs-lookup"><span data-stu-id="4065e-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="4065e-154">現在、米国がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4065e-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="4065e-155">**領収書はどこに移動しますか ?**</span><span class="sxs-lookup"><span data-stu-id="4065e-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="4065e-156">財務では、Cognitive Services に連絡してフィールド データを抽出します。</span><span class="sxs-lookup"><span data-stu-id="4065e-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="4065e-157">Cognitive Services は、処理が行われている間、最大 24 時間領収書のコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="4065e-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="4065e-158">処理が完了すると、Cognitive Services で領収書が削除されます。</span><span class="sxs-lookup"><span data-stu-id="4065e-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="4065e-159">領収書は財務に保管されたままになります。</span><span class="sxs-lookup"><span data-stu-id="4065e-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="4065e-160">詳細については、[Form Recognizer の新機能を使用して領収書を理解する](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4065e-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
