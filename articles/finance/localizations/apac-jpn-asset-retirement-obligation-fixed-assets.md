---
title: 日本の固定資産の資産償却責務を設定します。
description: この記事は、ARO の負債がどのように認識、償却、および未払となるか、および固定資産と ARO の負債が日本で除去される方法について説明します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetRetirementObligation_JP, AssetRetirementObligationDocument_JP, AssetRetirementObligationExplorer_JP, AssetRetirementObligationLine_JP, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10174
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce6fb1625acf39e6b1dee843be4083b913abf966
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552359"
---
# <a name="set-up-asset-retirement-obligation-for-fixed-assets-for-japan"></a><span data-ttu-id="acde6-103">日本の固定資産の資産償却責務を設定します。</span><span class="sxs-lookup"><span data-stu-id="acde6-103">Set up asset retirement obligation for fixed assets for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acde6-104">日本では、資産除去債務 (ARO) は法的な除去責務のある固定資産に対して認識されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-104">In Japan, asset retirement obligation (ARO) is recognized for fixed assets that have legal obligations at their retirement.</span></span> <span data-ttu-id="acde6-105">この記事は、ARO の負債がどのように認識、償却、および未払となるか、および固定資産と ARO の負債が除去される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="acde6-105">This article explains how the ARO liability is recognized, amortized, and accrued, and how the fixed asset and ARO liability are retired.</span></span>

<span data-ttu-id="acde6-106">資産償却責務 (ARO) は、資産償却の原価を耐用年数で配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-106">Asset retirement obligation (ARO) is used to distribute the retirement cost of an asset to its service life.</span></span> <span data-ttu-id="acde6-107">ARO は、固定資産の取得または構築する際に最初に負債として認識されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-107">ARO is initially recognized as a liability when you acquire or construct a fixed asset.</span></span> <span data-ttu-id="acde6-108">ARO 負債は、耐用年数の初めに見積もられた資産に対する償却原価の現在の値を表します。</span><span class="sxs-lookup"><span data-stu-id="acde6-108">The ARO liability is equal to the present value of the estimated retirement cost for the asset at the beginning of its service life.</span></span> <span data-ttu-id="acde6-109">ARO 負債を固定資産の取得原価に追加すると、ARO の負債原価は固定資産の耐用年数で償却されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-109">When the ARO liability is added to the acquisition cost of the fixed asset, the ARO liability cost is amortized throughout the service life of the fixed asset.</span></span> <span data-ttu-id="acde6-110">ARO 負債の利息費用は、最終的な ARO 負債が当初の見積除去原価に到達するように、特定の割引率での未払費用になります。</span><span class="sxs-lookup"><span data-stu-id="acde6-110">Interest expense on the ARO liability is accrued at the discount rate, so that the final ARO liability reaches the initially estimated retirement cost.</span></span> <span data-ttu-id="acde6-111">固定資産が除去されると、ARO 負債の勘定に支払額が転記されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-111">When the fixed asset is retired, the payable due is accounted for in the ARO liability account.</span></span> <span data-ttu-id="acde6-112">元の見積からの違いがない限り、これ以外の経費は転記されません。</span><span class="sxs-lookup"><span data-stu-id="acde6-112">No more expenses are accounted unless there is a difference from the original estimate.</span></span> <span data-ttu-id="acde6-113">次の表に、ライフ サイクルの実例を示します。</span><span class="sxs-lookup"><span data-stu-id="acde6-113">The following table shows a real-world example of the life cycle.</span></span>

| <span data-ttu-id="acde6-114">品目</span><span class="sxs-lookup"><span data-stu-id="acde6-114">Item</span></span>        | <span data-ttu-id="acde6-115">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="acde6-115">Content</span></span>                                                                                                                                                                                   |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acde6-116">前提</span><span class="sxs-lookup"><span data-stu-id="acde6-116">Assumptions</span></span> | <span data-ttu-id="acde6-117">取得原価: **10,000** (残存価額 0) 耐用期間: **5** 減価償却方法: **定額** 見積除去原価: **1,000** 割引率: **3%**</span><span class="sxs-lookup"><span data-stu-id="acde6-117">Acquisition cost: **10,000** (0 residual value) Useful life: **5** Depreciation method: **Straight line** Estimated cost of retirement: **1,000** Discount rate: **3%**</span></span>                  |
| <span data-ttu-id="acde6-118">ステップ１</span><span class="sxs-lookup"><span data-stu-id="acde6-118">Step 1</span></span>      | <span data-ttu-id="acde6-119">借方: 設備 **10,863** 貸方: 他の支払 **10,000** 貸方: ARO の負債 **863**</span><span class="sxs-lookup"><span data-stu-id="acde6-119">Debit: Equipment **10,863** Credit: Other payable **10,000** Credit: ARO liability **863**</span></span>                                                                                                |
| <span data-ttu-id="acde6-120">ステップ２\*</span><span class="sxs-lookup"><span data-stu-id="acde6-120">Step 2\*</span></span>    | <span data-ttu-id="acde6-121">借方: 減価償却費用 **2,173** 貸方: 減価償却累計額 (FA) **2,000** 貸方: 減価償却累計額 (ARO) **173**</span><span class="sxs-lookup"><span data-stu-id="acde6-121">Debit: Depreciation expenses **2,173** Credit: Accumulated depreciation (FA) **2,000** Credit: Accumulated depreciation (ARO) **173**</span></span>                                                     |
| <span data-ttu-id="acde6-122">ステップ 3\*</span><span class="sxs-lookup"><span data-stu-id="acde6-122">Step 3\*</span></span>    | <span data-ttu-id="acde6-123">借方: 支払利息 **27** 貸方: ARO の負債 **27**</span><span class="sxs-lookup"><span data-stu-id="acde6-123">Debit: Interest expenses **27** Credit: ARO liability **27**</span></span>                                                                                                                              |
| <span data-ttu-id="acde6-124">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="acde6-124">Step 4</span></span>      | <span data-ttu-id="acde6-125">借方: 減価償却累計額 (FA) **10,000** 借方: 減価償却累計額 (ARO) **863** 貸方: 設備 **10,863** 借方: ARO 負債 **1,000** 貸方: 他の支払 **1,000**</span><span class="sxs-lookup"><span data-stu-id="acde6-125">Debit: Accumulated depreciation (FA) **10,000** Debit: Accumulated depreciation (ARO) **863** Credit: Equipment **10,863** Debit: ARO liability **1,000** Credit: Other payable **1,000**</span></span> |

> [!NOTE]
><span data-ttu-id="acde6-126">\*\* 手順 2 と 3 が、固定資産の耐用年数全体に複数回繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="acde6-126">\* Steps 2 and 3 are repeated multiple times throughout the service life of the fixed asset.</span></span>

![ARO トランザクションの T 字勘定での表示](./media/aro-t-account.png) 

## <a name="setup-information"></a><span data-ttu-id="acde6-128">設定情報</span><span class="sxs-lookup"><span data-stu-id="acde6-128">Setup information</span></span>
<span data-ttu-id="acde6-129">ARO を使用するには、次の設定手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acde6-129">To use ARO, you must complete the following setup tasks:</span></span>

-   <span data-ttu-id="acde6-130">既定の帳簿、理由コード、および番号順序などの、基本的な固定資産パラメーターを**固定資産パラメーター** ページで設定します</span><span class="sxs-lookup"><span data-stu-id="acde6-130">Set up basic fixed asset parameters, such as a default Book, reason codes, and number sequences on the **Fixed assets parameters** page</span></span>
-   <span data-ttu-id="acde6-131">固定資産グループを**固定資産グループ**ページで定義します</span><span class="sxs-lookup"><span data-stu-id="acde6-131">Define a fixed asset group on the **Fixed asset groups** page</span></span>
-   <span data-ttu-id="acde6-132">減価償却の会計カレンダーを設定します</span><span class="sxs-lookup"><span data-stu-id="acde6-132">Set up a fiscal calendar for depreciation</span></span>
-   <span data-ttu-id="acde6-133">現在の市場の割引率を使用する割引率スケジュールを設定して、ARO 金額を計算します</span><span class="sxs-lookup"><span data-stu-id="acde6-133">Set up a discount rate schedule that uses current market discount rates to calculate ARO amounts</span></span>
-   <span data-ttu-id="acde6-134">資産に使用する ARO タイプと、ARO 金額の変更を転記する頻度を指定します</span><span class="sxs-lookup"><span data-stu-id="acde6-134">Specify the type of ARO to use for an asset, and specify how often changes to the ARO amounts are posted</span></span>
-   <span data-ttu-id="acde6-135">ARO の見積償却原価計画を設定し、資産の耐用年数の会計期間ごとに ARO 金額をシミュレーションします</span><span class="sxs-lookup"><span data-stu-id="acde6-135">Set up an estimated retirement cost plan for ARO, and simulate ARO amounts for each fiscal period of the asset’s service life</span></span>
-   <span data-ttu-id="acde6-136">**資本化資産償却責務**と**資産償却債務 - 増加** **経費**のドキュメント タイプで使用する転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="acde6-136">Set up a posting profile for the **Capitalized asset retirement obligation** and **Asset retirement obligation - accretion** **expense** document types</span></span>
-   <span data-ttu-id="acde6-137">**処分する ARO** のトランザクション タイプである固定資産を転記する際に、トランザクション金額の取得元の勘定を設定します</span><span class="sxs-lookup"><span data-stu-id="acde6-137">Set up accounts that the transaction amounts are retrieved from when you post a fixed asset that has a transaction type of **ARO for disposal**</span></span>

## <a name="set-up-asset-retirement-obligation-documents-and-enter-aro-amount-on-a-fixed-asset"></a><span data-ttu-id="acde6-138">資産除去責務ドキュメントの設定と固定資産の ARO 金額の入力</span><span class="sxs-lookup"><span data-stu-id="acde6-138">Set up asset retirement obligation documents and enter ARO amount on a fixed asset</span></span>
<span data-ttu-id="acde6-139">[資産除去責務ドキュメントの設定](./tasks/set-up-asset-retirement-obligation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="acde6-139">See [Set up asset retirement obligation documents](./tasks/set-up-asset-retirement-obligation.md).</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="acde6-140">システム管理者向け技術情報</span><span class="sxs-lookup"><span data-stu-id="acde6-140">Technical information for system administrators</span></span>
<span data-ttu-id="acde6-141">このタスクを完了するために使用するページに対するアクセス権限がない場合は、システム管理者に連絡し、次の表に示される情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="acde6-141">If you don't have access to the pages that are used to complete this task, contact your system administrator and provide the information that is shown in the following table.</span></span>


|         <span data-ttu-id="acde6-142">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="acde6-142">Category</span></span>          |                                                                                                <span data-ttu-id="acde6-143">前提条件</span><span class="sxs-lookup"><span data-stu-id="acde6-143">Prerequisite</span></span>                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    <span data-ttu-id="acde6-144">コンフィギュレーション キー</span><span class="sxs-lookup"><span data-stu-id="acde6-144">Configuration keys</span></span>     | <span data-ttu-id="acde6-145">アプリケーション オブジェクト ツリー (AOT) の<strong>データ ディクショナリ</strong> &gt; <strong>コンフィギュレーション キー</strong> ノードで、固定<strong>資産</strong>のコンフィギュレーション キーが使用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="acde6-145">Ensure that the Fixed <strong>Assets</strong> configuration key is available under the <strong>Data Dictionary</strong> &gt; <strong>Configuration Keys</strong> node in the Application Object Tree (AOT).</span></span> |
| <span data-ttu-id="acde6-146">セキュリティ ロールおよび職務</span><span class="sxs-lookup"><span data-stu-id="acde6-146">Security roles and duties</span></span> |                                                  <span data-ttu-id="acde6-147">このタスクを実行するには、<strong>固定資産の管理</strong>のセキュリティ ロールのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="acde6-147">To perform this task, you must be a member of the <strong>-Maintain fixed assets-</strong> security role.</span></span>                                                  |
