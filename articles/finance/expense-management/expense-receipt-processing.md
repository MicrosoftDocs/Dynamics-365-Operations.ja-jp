---
title: 経費の領収書
description: このトピックでは、領収書の光学式文字認識 (OCR) 処理に関する情報を提供します。 この機能は、Microsoft Dynamics 365 Finance で経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
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
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378234"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="78453-104">経費の領収書</span><span class="sxs-lookup"><span data-stu-id="78453-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78453-105">領収書の光学式文字認識 (OCR) 処理の導入により、経費入力が強化されました。</span><span class="sxs-lookup"><span data-stu-id="78453-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="78453-106">この機能は、経費精算書を作成する際のユーザー エクスペリエンスの向上を目的に設計されています。</span><span class="sxs-lookup"><span data-stu-id="78453-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="78453-107">主な機能</span><span class="sxs-lookup"><span data-stu-id="78453-107">Key features</span></span>

- <span data-ttu-id="78453-108">領収書から販売者名、日付、合計金額を抽出する。</span><span class="sxs-lookup"><span data-stu-id="78453-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="78453-109">この機能は、未添付の領収書を未添付の経費トランザクションと照合します。</span><span class="sxs-lookup"><span data-stu-id="78453-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="78453-110">ユーザーは、領収書から手動で入力された経費トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="78453-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="78453-111">使用例</span><span class="sxs-lookup"><span data-stu-id="78453-111">Usage examples</span></span>

<span data-ttu-id="78453-112">経費精算書の作成時に、クレジット カード トランザクションを含む領収書を自動的に添付する場合は、以下の手順に従ってください:</span><span class="sxs-lookup"><span data-stu-id="78453-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="78453-113">**経費管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="78453-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="78453-114">**領収書**タブで、未添付の領収書が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="78453-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="78453-115">**領収書**タブで領収書をアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="78453-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="78453-116">**経費**タブで、未添付の経費が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="78453-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="78453-117">通常、経費管理者は、これらの経費をクレジット カード プロバイダーからインポートします。</span><span class="sxs-lookup"><span data-stu-id="78453-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="78453-118">**新しい経費精算書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="78453-118">Select **New expense report**.</span></span> <span data-ttu-id="78453-119">経費精算書を作成するときに、経費、および領収書を含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="78453-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="78453-120">経費と領収書の両方を追加すると、経費に対する領収書の自動照合がトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="78453-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="78453-121">経費を作成する、または領収書から経費を照合するには、以下の手順に従ってください:</span><span class="sxs-lookup"><span data-stu-id="78453-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="78453-122">経費精算書の**領収書**タブで、**領収書の追加**を選択して領収書を添付します。</span><span class="sxs-lookup"><span data-stu-id="78453-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="78453-123">アップロードされた領収書の画像の下に**作成**および**照合**オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="78453-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="78453-124">**作成**を選択して、手動で入力された経費トランザクションを作成し、領収書から抽出された値を入力します。</span><span class="sxs-lookup"><span data-stu-id="78453-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="78453-125">**照合**を選択した場合、システムは既存の経費と領収書を照合しようとします。</span><span class="sxs-lookup"><span data-stu-id="78453-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="78453-126">インストール</span><span class="sxs-lookup"><span data-stu-id="78453-126">Installation</span></span>

<span data-ttu-id="78453-127">この機能は、**経費精算書の再設計**機能と組み合わせて機能し、経費のエクスペリエンスを簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="78453-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="78453-128">この機能は、サンドボックス環境と実か同環境の Tier 2 + 環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="78453-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="78453-129">これらの高度な経費機能を使用するには、Microsoft Dynamics 365 Finance の経費管理サービス アドインをインストールし、インスタンスの機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="78453-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="78453-130">Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからアドインにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78453-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="78453-131">LCS にサインインし、目的の環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="78453-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="78453-132">**完全な詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="78453-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="78453-133">**メンテナンス**を選択するか、**環境アドイン** クイック タブまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="78453-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="78453-134">**新しいアドインのインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="78453-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="78453-135">**経費管理サービス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="78453-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="78453-136">インストール ガイドに従って、契約条件に同意します。</span><span class="sxs-lookup"><span data-stu-id="78453-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="78453-137">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="78453-137">Select **Install**.</span></span>

<span data-ttu-id="78453-138">**機能の管理**ワークスペースで、次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="78453-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="78453-139">経費レポートの再設計</span><span class="sxs-lookup"><span data-stu-id="78453-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="78453-140">レシートからの自動照合および経費の作成</span><span class="sxs-lookup"><span data-stu-id="78453-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="78453-141">これらの機能をオンにすると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="78453-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="78453-142">既存の**経費管理**ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="78453-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="78453-143">経費フィールド表示の新しいメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="78453-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="78453-144">以前の**経費精算書**ページは、**経費管理 > 自分の経費 > 経費精算書**に移動して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="78453-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="78453-145">ワークフローと承認を行っても、既存の経費精算書ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="78453-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="78453-146">領収書は、Microsoft Azure Cognitive Services によって処理され、メタデータが抽出されて追加されます。</span><span class="sxs-lookup"><span data-stu-id="78453-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="78453-147">一致する未添付の領収書を含む経費精算書を作成できるオプションが追加されました。</span><span class="sxs-lookup"><span data-stu-id="78453-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="78453-148">経費精算書に追加されたオプションを使用すると、領収書から経費明細行を作成したり、既存の領収書を既存の経費明細行と一致させたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="78453-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="78453-149">再設計された経費精算書の詳細については、[経費精算書の再設計](ExpenseWorkspaceNew.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78453-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="78453-150">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="78453-150">Frequently asked questions</span></span>

<span data-ttu-id="78453-151">**Microsoft は、モデルにデータを使用しますか ?**</span><span class="sxs-lookup"><span data-stu-id="78453-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="78453-152">いいえ、Microsoft は、領収書処理サービス用の一般的な機械学習モデルを構築しています。</span><span class="sxs-lookup"><span data-stu-id="78453-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="78453-153">このモデルは、アップロードした領収書に基づいていません。</span><span class="sxs-lookup"><span data-stu-id="78453-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="78453-154">**この機能はどこで使用および処理されますか ?**</span><span class="sxs-lookup"><span data-stu-id="78453-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="78453-155">現在、米国がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="78453-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="78453-156">**領収書はどこに移動しますか ?**</span><span class="sxs-lookup"><span data-stu-id="78453-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="78453-157">財務では、Cognitive Services に連絡してフィールド データを抽出します。</span><span class="sxs-lookup"><span data-stu-id="78453-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="78453-158">Cognitive Services は、処理が行われている間、最大 24 時間領収書のコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="78453-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="78453-159">処理が完了すると、Cognitive Services で領収書が削除されます。</span><span class="sxs-lookup"><span data-stu-id="78453-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="78453-160">領収書は財務に保管されたままになります。</span><span class="sxs-lookup"><span data-stu-id="78453-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="78453-161">詳細については、[Form Recognizer の新機能を使用して領収書を理解する](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78453-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
