---
title: 日本のキャッシュ生成単位の固定資産減損会計
description: このトピックでは、日本の減損会計の概念モデルの概要を説明します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAllocationGoodwillSharedAsset_JP, AssetCashGeneratingUnit_JP, AssetCashGeneratingUnitGroup_JP, AssetImpairmentRecognitionMethod1_JP, AssetImpairmentRecognitionMethod2_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 25691
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2dd3f6014c1733ab29bdb2f4b253399db638078
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175795"
---
# <a name="fixed-asset-impairment-accounting-on-cash-generating-units-for-japan"></a><span data-ttu-id="7fe34-103">日本のキャッシュ生成単位の固定資産減損会計</span><span class="sxs-lookup"><span data-stu-id="7fe34-103">Fixed asset impairment accounting on cash-generating units for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fe34-104">このトピックでは、固定資産の減損の機能について説明します。主な目的は、減損会計の概念モデルの概要を示すことです。</span><span class="sxs-lookup"><span data-stu-id="7fe34-104">This topic introduces the features for fixed asset impairment, and the primary objective is to give you an overview of the conceptual model for impairment accounting.</span></span> 

<span data-ttu-id="7fe34-105">固定資産は、管理不良、新規競合、および技術革新などの要因によって、その価値の減損 (減少) の影響を受けやすい場合があります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-105">Fixed assets might be susceptible to impairment (decline) of their value because of factors such as poor management, new competition, and technological innovations.</span></span> <span data-ttu-id="7fe34-106">減損損失は損益勘定で表示されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-106">Impairment losses are stated in a profit and loss account.</span></span> <span data-ttu-id="7fe34-107">減損価値は、固定資産または利益生成単位の値を回収可能金額と比較して測定されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-107">The impairment value is measured by comparing the value of the fixed asset or income generating unit with its recoverable amount.</span></span> <span data-ttu-id="7fe34-108">回収可能金額は、固定資産またはその工程から生成される収益の売上から取得できる最大値です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-108">The recoverable amount is the highest value that can be obtained from selling the fixed asset or income that is generated from operation of the fixed asset.</span></span> <span data-ttu-id="7fe34-109">日本では、固定資産の減損は、日本の一般会計原則 (GAAP) の</span><span class="sxs-lookup"><span data-stu-id="7fe34-109">In Japan, impairment of fixed assets is done in accordance with No.</span></span> <span data-ttu-id="7fe34-110">第 6 項目に従って行い、2 つのステップがある方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="7fe34-110">6 of Japanese generally accepted accounting principles (GAAP), where a two-step method is used.</span></span> <span data-ttu-id="7fe34-111">最初のステップは、減損損失の認識テストで、2 つ目のステップは減損損失の測定です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-111">The first step is a recognition test of impairment loss, and the second step is measurement of the impairment loss.</span></span> <span data-ttu-id="7fe34-112">減損後、回収可能金額は、将来の減価償却計算のための固定資産の新しい正味簿価額となります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-112">After impairment, the recoverable amount will be the new net book value of the fixed asset for future depreciation calculation.</span></span> <span data-ttu-id="7fe34-113">減損の作業プロセスには次の主要タスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-113">The impairment work process includes the following major tasks.</span></span>

## <a name="cgu-groups"></a><span data-ttu-id="7fe34-114">CGU グループ</span><span class="sxs-lookup"><span data-stu-id="7fe34-114">CGU groups</span></span>
<span data-ttu-id="7fe34-115">基本ページは、**CGU グループ**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **CGU グループ**)。</span><span class="sxs-lookup"><span data-stu-id="7fe34-115">The primary page is **CGU groups** (**Fixed assets** &gt; **Setup** &gt; **Impairment** &gt; **CGU groups**).</span></span> <span data-ttu-id="7fe34-116">CGU グループは、減損プロセスの組み合わせ全体です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-116">CGU groups are the entire combination of the impairment process.</span></span> <span data-ttu-id="7fe34-117">特定の CGU グループでは、1 つのキャッシュ生成単位のみに 1 つの特定の固定資産を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-117">In a given CGU group, a user can assign one particular fixed asset to only one cash generating unit.</span></span> <span data-ttu-id="7fe34-118">この制限は、ユーザーが別の CGU グループを作成し、そのグループでキャッシュ生成単位を作成するときに適用されません。</span><span class="sxs-lookup"><span data-stu-id="7fe34-118">This restriction doesn't apply when the user creates a different CGU group and then creates cash generating units under that group.</span></span> <span data-ttu-id="7fe34-119">複数の CGU グループの作成は、固定資産の最も適したグループを検索するためのシミュレーションに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-119">Creating multiple CGU groups is useful for simulations to find the most appropriate grouping of fixed assets.</span></span>

## <a name="cash-generating-unit-cgu"></a><span data-ttu-id="7fe34-120">キャッシュ生成単位 (CGU)</span><span class="sxs-lookup"><span data-stu-id="7fe34-120">Cash-generating unit (CGU)</span></span>
<span data-ttu-id="7fe34-121">基本ページは、**キャッシュ生成グループ**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **キャッシュ生成グループ**)。</span><span class="sxs-lookup"><span data-stu-id="7fe34-121">The primary page is **Cash generating groups** (**Fixed assets** &gt; **Setup** &gt; **Impairment** &gt; **Cash generating groups**).</span></span> <span data-ttu-id="7fe34-122">ユーザーは CGU グループでキャッシュ生成単位を作成し、個別の固定資産をキャッシュ生成単位に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-122">A user can create cash-generating units under a CGU group and then assign individual fixed assets to each cash-generating unit.</span></span> <span data-ttu-id="7fe34-123">ユーザーは、これらの資産が共有資産または営業権である場合、CGU グループに直接固定資産を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-123">The user can also directly assign the fixed assets to the CGU group if those assets are shared assets or goodwill.</span></span> <span data-ttu-id="7fe34-124">共有資産と無形固定資産の減損は、日本の GAAP のメソッド I に従って、CGU グループ単位でテストおよび測定されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-124">Impairment on shared assets and goodwill will be tested and measured on the CGU group unit, in compliance with Method I under Japanese GAAP.</span></span> <span data-ttu-id="7fe34-125">ユーザーは、メソッド II も適用できます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-125">A user can also apply Method II.</span></span> <span data-ttu-id="7fe34-126">この場合、ユーザーは各キャッシュ生成単位に、共有資産および営業権の正味簿価額を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-126">In this case, the user will have to allocate the net book value of the shared assets and goodwill to each cash generating unit.</span></span>

### <a name="optional-allocating-the-net-book-value-of-shared-assets-and-goodwill"></a><span data-ttu-id="7fe34-127">オプション: 共有資産と営業権の正味簿価額の配賦</span><span class="sxs-lookup"><span data-stu-id="7fe34-127">Optional: Allocating the net book value of shared assets and goodwill</span></span>

<span data-ttu-id="7fe34-128">基本ページは、**営業権と共有資産の正味簿価額の配賦**です (**固定資産** &gt; **設定** &gt; **減損** &gt; **営業権と共有資産の正味簿価額の配賦**)。</span><span class="sxs-lookup"><span data-stu-id="7fe34-128">The primary page is **Allocation of net book value of goodwill and shared asset** (**Fixed assets** &gt; **Setup** &gt; **Impairment** &gt; **Allocation of net book value of goodwill and shared asset**).</span></span> <span data-ttu-id="7fe34-129">ユーザーが CGU グループにメソッド II を適用する場合、共有資産と営業権の正味簿価額を各キャッシュ生成単位に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-129">If a user chooses to apply Method II in a CGU group, the net book value of shared assets and goodwill must be allocated to each cash generating unit.</span></span>

## <a name="impairment-recognition-test"></a><span data-ttu-id="7fe34-130">減損認識テスト</span><span class="sxs-lookup"><span data-stu-id="7fe34-130">Impairment recognition test</span></span>
<span data-ttu-id="7fe34-131">基本ページは、**固定資産** &gt; **調整**です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-131">The primary page is **Fixed assets** &gt; **Adjustment**.</span></span> <span data-ttu-id="7fe34-132">メソッド I またはメソッド II が適用されるかによってサブメニューが異なります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-132">The sub-menus different, depending on whether Method I or Method II is applied.</span></span> <span data-ttu-id="7fe34-133">減損の最初の手順は、認識テストです。</span><span class="sxs-lookup"><span data-stu-id="7fe34-133">The first step of impairment is the recognition test.</span></span> <span data-ttu-id="7fe34-134">割引のない将来のキャッシュ フローが、帳簿価額 (または正味簿価額) を比較する基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-134">Future cash flow that isn't discounted is used as a standard that the carrying amount (or net book value) is compared against.</span></span> <span data-ttu-id="7fe34-135">この将来のキャッシュ フローが資産の正味簿価額を満たしていない場合、減損の測定では仕訳帳金額が認識されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-135">If this future cash flow isn't enough to cover the net book value of the asset, the impairment measurement must recognize the journal amount.</span></span>

## <a name="measurement-of-the-impairment-amount"></a><span data-ttu-id="7fe34-136">減損金額の測定</span><span class="sxs-lookup"><span data-stu-id="7fe34-136">Measurement of the impairment amount</span></span>
<span data-ttu-id="7fe34-137">2 つ目のステップは減損金額の測定です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-137">The second step is measurement of the impairment amount.</span></span> <span data-ttu-id="7fe34-138">回収可能金額は、減損金額を計算するために固定資産の正味簿価額から差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-138">The recoverable amount is subtracted from the net book value of the fixed asset to calculate the impairment amount.</span></span> <span data-ttu-id="7fe34-139">回収可能金額は、使用中の値または資産の市場価値のいずれかより高いほうになります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-139">The recoverable amount is either the value in use or the market value of the asset, whichever is higher.</span></span> <span data-ttu-id="7fe34-140">2 つのステップは、同じページで行います。</span><span class="sxs-lookup"><span data-stu-id="7fe34-140">The two steps are done on the same page.</span></span>

## <a name="posting-the-impairment"></a><span data-ttu-id="7fe34-141">減損の転記</span><span class="sxs-lookup"><span data-stu-id="7fe34-141">Posting the impairment</span></span>
<span data-ttu-id="7fe34-142">減損金額の認識テストおよび測定の後、ユーザーは各固定資産に対する減損金額を転記できます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-142">After the recognition test and measurement of the impairment amount, the user can post the impairment amount to each fixed asset.</span></span> <span data-ttu-id="7fe34-143">転記後に、償却提案では減損金額が考慮され、正しい減価償却金額が提案されます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-143">After posting, the depreciation proposal will consider the impairment amount and propose the correct depreciation amount.</span></span>

## <a name="reports-and-other-required-operations"></a><span data-ttu-id="7fe34-144">レポートおよびその他の必要な工程</span><span class="sxs-lookup"><span data-stu-id="7fe34-144">Reports and other required operations</span></span>
<span data-ttu-id="7fe34-145">ユーザーは**減損レポートおよびトランザクション**照会ページを使用して、減損トランザクションに関する詳細情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="7fe34-145">The user can use the **Impairment reports and transactions** inquiry pages to retrieve detailed information about the impairment transactions.</span></span> <span data-ttu-id="7fe34-146">会社の税務申告の調整など特定の工程が、減損の転記後に必要です。</span><span class="sxs-lookup"><span data-stu-id="7fe34-146">Specific operations are required after an impairment is posted, such as adjustment on the corporate tax declaration.</span></span> <span data-ttu-id="7fe34-147">ユーザーは、これらの工程を手動で計算して転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fe34-147">The user will have to manually calculate and post these operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fe34-148">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7fe34-148">Additional resources</span></span>
- [<span data-ttu-id="7fe34-149">固定資産の減損会計</span><span class="sxs-lookup"><span data-stu-id="7fe34-149">Impairment accounting for fixed assets</span></span>](apac-jpn-impairment-accounting-fixed-assets.md)
- [<span data-ttu-id="7fe34-150">資産グループの減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="7fe34-150">Propose and post the impairment amount on a cash generating unit</span></span>](./tasks/propose-post-impairment-amount-cash-generating-unit.md)
