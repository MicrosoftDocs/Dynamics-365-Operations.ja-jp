---
title: "固定資産の資産償却責務の設定"
description: "日本では、資産除去債務 (ARO) は法的な除去責務のある固定資産に対して認識されます。 この記事は、ARO の負債がどのように認識、償却、および未払となるか、および固定資産と ARO の負債が除去される方法について説明します。"
author: yijialuan
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetRetirementObligation_JP, AssetRetirementObligationDocument_JP, AssetRetirementObligationExplorer_JP, AssetRetirementObligationLine_JP, AssetTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10174
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f944258e7efdd5c9eba7daf9a80c67058a6cc055
ms.openlocfilehash: df59b74c8bfe57bff52cf885dc1b2ebd7181e53b
ms.contentlocale: ja-jp
ms.lasthandoff: 10/25/2017

---

# <a name="set-up-asset-retirement-obligation"></a><span data-ttu-id="7480d-104">資産償却責務の設定</span><span class="sxs-lookup"><span data-stu-id="7480d-104">Set up asset retirement obligation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7480d-105">日本では、資産除去債務 (ARO) は法的な除去責務のある固定資産に対して認識されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-105">In Japan, asset retirement obligation (ARO) is recognized for fixed assets that have legal obligations at their retirement.</span></span> <span data-ttu-id="7480d-106">この記事は、ARO の負債がどのように認識、償却、および未払となるか、および固定資産と ARO の負債が除去される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7480d-106">This article explains how the ARO liability is recognized, amortized, and accrued, and how the fixed asset and ARO liability are retired.</span></span>

<span data-ttu-id="7480d-107">資産償却責務 (ARO) は、資産償却の原価を耐用年数で配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-107">Asset retirement obligation (ARO) is used to distribute the retirement cost of an asset to its service life.</span></span> <span data-ttu-id="7480d-108">ARO は、固定資産の取得または構築する際に最初に負債として認識されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-108">ARO is initially recognized as a liability when you acquire or construct a fixed asset.</span></span> <span data-ttu-id="7480d-109">ARO 負債は、耐用年数の初めに見積もられた資産に対する償却原価の現在の値を表します。</span><span class="sxs-lookup"><span data-stu-id="7480d-109">The ARO liability is equal to the present value of the estimated retirement cost for the asset at the beginning of its service life.</span></span> <span data-ttu-id="7480d-110">ARO 負債を固定資産の取得原価に追加すると、ARO の負債原価は固定資産の耐用年数で償却されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-110">When the ARO liability is added to the acquisition cost of the fixed asset, the ARO liability cost is amortized throughout the service life of the fixed asset.</span></span> <span data-ttu-id="7480d-111">ARO 負債の利息費用は、最終的な ARO 負債が当初の見積除去原価に到達するように、特定の割引率での未払費用になります。</span><span class="sxs-lookup"><span data-stu-id="7480d-111">Interest expense on the ARO liability is accrued at the discount rate, so that the final ARO liability reaches the initially estimated retirement cost.</span></span> <span data-ttu-id="7480d-112">固定資産が除去されると、ARO 負債の勘定に支払額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-112">When the fixed asset is retired, the payable due is accounted for in the ARO liability account.</span></span> <span data-ttu-id="7480d-113">元の見積からの違いがない限り、これ以外の経費は転記されません。</span><span class="sxs-lookup"><span data-stu-id="7480d-113">No more expenses are accounted unless there is a difference from the original estimate.</span></span> <span data-ttu-id="7480d-114">次の表に、ライフ サイクルの実例を示します。</span><span class="sxs-lookup"><span data-stu-id="7480d-114">The following table shows a real-world example of the life cycle.</span></span>

| <span data-ttu-id="7480d-115">品目</span><span class="sxs-lookup"><span data-stu-id="7480d-115">Item</span></span>        | <span data-ttu-id="7480d-116">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="7480d-116">Content</span></span>                                                                                                                                                                                   |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7480d-117">前提</span><span class="sxs-lookup"><span data-stu-id="7480d-117">Assumptions</span></span> | <span data-ttu-id="7480d-118">取得原価: **10,000** (残存価額 0) 耐用期間: **5** 減価償却方法: **定額** 見積除去原価: **1,000** 割引率: **3%**</span><span class="sxs-lookup"><span data-stu-id="7480d-118">Acquisition cost: **10,000** (0 residual value) Useful life: **5** Depreciation method: **Straight line** Estimated cost of retirement: **1,000** Discount rate: **3%**</span></span>                  |
| <span data-ttu-id="7480d-119">ステップ１</span><span class="sxs-lookup"><span data-stu-id="7480d-119">Step 1</span></span>      | <span data-ttu-id="7480d-120">借方: 設備 **10,863** 貸方: 他の支払 **10,000** 貸方: ARO の負債 **863**</span><span class="sxs-lookup"><span data-stu-id="7480d-120">Debit: Equipment **10,863** Credit: Other payable **10,000** Credit: ARO liability **863**</span></span>                                                                                                |
| <span data-ttu-id="7480d-121">ステップ２\*</span><span class="sxs-lookup"><span data-stu-id="7480d-121">Step 2\*</span></span>    | <span data-ttu-id="7480d-122">借方: 減価償却費用 **2,173** 貸方: 減価償却累計額 (FA) **2,000** 貸方: 減価償却累計額 (ARO) **173**</span><span class="sxs-lookup"><span data-stu-id="7480d-122">Debit: Depreciation expenses **2,173** Credit: Accumulated depreciation (FA) **2,000** Credit: Accumulated depreciation (ARO) **173**</span></span>                                                     |
| <span data-ttu-id="7480d-123">ステップ 3\*</span><span class="sxs-lookup"><span data-stu-id="7480d-123">Step 3\*</span></span>    | <span data-ttu-id="7480d-124">借方: 支払利息 **27** 貸方: ARO の負債 **27**</span><span class="sxs-lookup"><span data-stu-id="7480d-124">Debit: Interest expenses **27** Credit: ARO liability **27**</span></span>                                                                                                                              |
| <span data-ttu-id="7480d-125">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="7480d-125">Step 4</span></span>      | <span data-ttu-id="7480d-126">借方: 減価償却累計額 (FA) **10,000** 借方: 減価償却累計額 (ARO) **863** 貸方: 設備 **10,863** 借方: ARO 負債 **1,000** 貸方: 他の支払 **1,000**</span><span class="sxs-lookup"><span data-stu-id="7480d-126">Debit: Accumulated depreciation (FA) **10,000** Debit: Accumulated depreciation (ARO) **863** Credit: Equipment **10,863** Debit: ARO liability **1,000** Credit: Other payable **1,000**</span></span> |

> [!NOTE]
><span data-ttu-id="7480d-127">\** 手順 2 と 3 が、固定資産の耐用年数全体に複数回繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="7480d-127">\* Steps 2 and 3 are repeated multiple times throughout the service life of the fixed asset.</span></span>

![ARO トランザクションの T 字勘定での表示](./media/aro-t-account.png) 

## <a name="setup-information"></a><span data-ttu-id="7480d-129">設定情報</span><span class="sxs-lookup"><span data-stu-id="7480d-129">Setup information</span></span>
<span data-ttu-id="7480d-130">ARO を使用するには、次の設定手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7480d-130">To use ARO, you must complete the following setup tasks:</span></span>

-   <span data-ttu-id="7480d-131">既定の帳簿、理由コード、および番号順序などの、基本的な固定資産パラメーターを**固定資産パラメーター** ページで設定します</span><span class="sxs-lookup"><span data-stu-id="7480d-131">Set up basic fixed asset parameters, such as a default Book, reason codes, and number sequences on the **Fixed assets parameters** page</span></span>
-   <span data-ttu-id="7480d-132">固定資産グループを**固定資産グループ**ページで定義します</span><span class="sxs-lookup"><span data-stu-id="7480d-132">Define a fixed asset group on the **Fixed asset groups** page</span></span>
-   <span data-ttu-id="7480d-133">減価償却の会計カレンダーを設定します</span><span class="sxs-lookup"><span data-stu-id="7480d-133">Set up a fiscal calendar for depreciation</span></span>
-   <span data-ttu-id="7480d-134">現在の市場の割引率を使用する割引率スケジュールを設定して、ARO 金額を計算します</span><span class="sxs-lookup"><span data-stu-id="7480d-134">Set up a discount rate schedule that uses current market discount rates to calculate ARO amounts</span></span>
-   <span data-ttu-id="7480d-135">資産に使用する ARO タイプと、ARO 金額の変更を転記する頻度を指定します</span><span class="sxs-lookup"><span data-stu-id="7480d-135">Specify the type of ARO to use for an asset, and specify how often changes to the ARO amounts are posted</span></span>
-   <span data-ttu-id="7480d-136">ARO の見積償却原価計画を設定し、資産の耐用年数の会計期間ごとに ARO 金額をシミュレーションします</span><span class="sxs-lookup"><span data-stu-id="7480d-136">Set up an estimated retirement cost plan for ARO, and simulate ARO amounts for each fiscal period of the asset’s service life</span></span>
-   <span data-ttu-id="7480d-137">**資本化資産償却責務**と**資産償却債務 - 増加****経費**のドキュメント タイプで使用する転記プロファイルを設定します</span><span class="sxs-lookup"><span data-stu-id="7480d-137">Set up a posting profile for the **Capitalized asset retirement obligation** and **Asset retirement obligation - accretion** **expense** document types</span></span>
-   <span data-ttu-id="7480d-138">**処分する ARO** のトランザクション タイプである固定資産を転記する際に、トランザクション金額の取得元の勘定を設定します</span><span class="sxs-lookup"><span data-stu-id="7480d-138">Set up accounts that the transaction amounts are retrieved from when you post a fixed asset that has a transaction type of **ARO for disposal**</span></span>

## <a name="set-up-asset-retirement-obligation-documents-and-enter-aro-amount-on-a-fixed-asset"></a><span data-ttu-id="7480d-139">資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力</span><span class="sxs-lookup"><span data-stu-id="7480d-139">Set up asset retirement obligation documents and enter ARO amount on a fixed asset</span></span>
<span data-ttu-id="7480d-140">[資産除去責務ドキュメントの設定](./tasks/set-up-asset-retirement-obligation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7480d-140">See [Set up asset retirement obligation documents](./tasks/set-up-asset-retirement-obligation.md).</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="7480d-141">システム管理者向け技術情報</span><span class="sxs-lookup"><span data-stu-id="7480d-141">Technical information for system administrators</span></span>
<span data-ttu-id="7480d-142">このタスクを完了するために使用するページに対するアクセス権限がない場合は、システム管理者に連絡し、次の表に示される情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7480d-142">If you don't have access to the pages that are used to complete this task, contact your system administrator and provide the information that is shown in the following table.</span></span>

| <span data-ttu-id="7480d-143">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="7480d-143">Category</span></span>                  | <span data-ttu-id="7480d-144">前提条件</span><span class="sxs-lookup"><span data-stu-id="7480d-144">Prerequisite</span></span>                                                                                                                                                         |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7480d-145">コンフィギュレーション キー</span><span class="sxs-lookup"><span data-stu-id="7480d-145">Configuration keys</span></span>        | <span data-ttu-id="7480d-146">アプリケーション オブジェクト ツリー (AOT) の**データ ディクショナリ** &gt; **コンフィギュレーション キー** ノードで、固定**資産**のコンフィギュレーション キーが使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7480d-146">Ensure that the Fixed **Assets** configuration key is available under the **Data Dictionary** &gt; **Configuration Keys** node in the Application Object Tree (AOT).</span></span> |
| <span data-ttu-id="7480d-147">セキュリティ ロールおよび職務</span><span class="sxs-lookup"><span data-stu-id="7480d-147">Security roles and duties</span></span> | <span data-ttu-id="7480d-148">このタスクを実行するには、**固定資産の管理**のセキュリティ ロールのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="7480d-148">To perform this task, you must be a member of the **-Maintain fixed assets-** security role.</span></span>|






