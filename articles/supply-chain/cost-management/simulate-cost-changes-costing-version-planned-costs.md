---
title: 予定原価に対する原価バージョンを使用した原価変更のシミュレーション
description: この記事では、製造品目の算出原価に対する原価変更の影響を、予定原価の個別の原価バージョンを使用してシミュレーションする方法を説明します。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 78183
ms.assetid: 1e41953f-cdb9-4598-b776-46e49383a773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ef3cdb2ede2c30609db4addfc10b819629cdc64
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568754"
---
# <a name="simulate-cost-changes-by-using-a-costing-version-for-planned-costs"></a><span data-ttu-id="0757b-103">予定原価に対する原価バージョンを使用した原価変更のシミュレーション</span><span class="sxs-lookup"><span data-stu-id="0757b-103">Simulate cost changes by using a costing version for planned costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0757b-104">この記事では、製造品目の算出原価に対する原価変更の影響を、予定原価の個別の原価バージョンを使用してシミュレーションする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="0757b-104">This article explains how you can simulate the effects of cost changes on a manufactured item’s calculated costs by using a separate costing version for planned costs.</span></span>

<span data-ttu-id="0757b-105">製造品目の算出原価に対する原価変更の影響は、予定原価の個別の原価バージョンを使用してシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="0757b-105">You can simulate the effects of cost changes on the calculated costs of a manufactured item by using a separate costing version for planned costs.</span></span> <span data-ttu-id="0757b-106">増額の原価変更を反映する保留中原価レコードの入力、および製造品目に対する原価影響の計算において、個別の原価バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="0757b-106">Use this separate costing version to enter pending cost records that reflect incremental cost changes, and to calculate the cost impact on manufactured items.</span></span> <span data-ttu-id="0757b-107">部品表 (BOM) の計算では、有効原価の予備原則が使用されるため、入力が必要なのは増額の原価変更のみとなります。</span><span class="sxs-lookup"><span data-stu-id="0757b-107">Because the Active costs fallback principle will be used in the bill of materials (BOM) calculations, only the incremental cost changes must be entered.</span></span>

## <a name="guidelines-for-defining-the-simulation-costing-version"></a><span data-ttu-id="0757b-108">シミュレーション原価バージョンの定義に関するガイドライン</span><span class="sxs-lookup"><span data-stu-id="0757b-108">Guidelines for defining the simulation costing version</span></span>
<span data-ttu-id="0757b-109">シミュレーション原価バージョンの定義には、次のガイドラインを使用してください。</span><span class="sxs-lookup"><span data-stu-id="0757b-109">Use the following guidelines when you define the costing version for simulations:</span></span>

-   <span data-ttu-id="0757b-110">**予定原価**の原価タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="0757b-110">Assign a costing type of **Planned costs**.</span></span>
-   <span data-ttu-id="0757b-111">原価バージョンにはわかりやすい識別子を割り当てます (**シミュレーション**など)。</span><span class="sxs-lookup"><span data-stu-id="0757b-111">Assign a meaningful identifier for the costing version, such as **Simulation**.</span></span>
-   <span data-ttu-id="0757b-112">内容には必ず原価レコードが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="0757b-112">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="0757b-113">原価レコードを入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="0757b-113">Allow the entry of cost records.</span></span> <span data-ttu-id="0757b-114">保留中の原価の入力をブロックしないでください。</span><span class="sxs-lookup"><span data-stu-id="0757b-114">Don't block the entry of pending costs.</span></span>
-   <span data-ttu-id="0757b-115">すべてのサイトの原価レコードの入力を許可します。</span><span class="sxs-lookup"><span data-stu-id="0757b-115">Allow the entry of cost records for all sites.</span></span> <span data-ttu-id="0757b-116">サイトを指定すると、原価レコードの入力範囲はそのサイトに限定されます。</span><span class="sxs-lookup"><span data-stu-id="0757b-116">If you specify a site, you will limit the entry of cost records to that site.</span></span>
-   <span data-ttu-id="0757b-117">保留中の原価を有効にできないようにします。</span><span class="sxs-lookup"><span data-stu-id="0757b-117">Prevent the activation of pending costs.</span></span> <span data-ttu-id="0757b-118">シミュレーション原価バージョン内の原価レコードには、保留中原価のみを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757b-118">Only pending costs must be entered for cost records in the simulation costing version.</span></span>
-   <span data-ttu-id="0757b-119">開始日は入力しないでください。</span><span class="sxs-lookup"><span data-stu-id="0757b-119">Don't enter a "from" date.</span></span> <span data-ttu-id="0757b-120">計算日は、シミュレーション原価バージョンを使用する BOM 計算ごとに入力します。</span><span class="sxs-lookup"><span data-stu-id="0757b-120">A calculation date will be entered for each BOM calculation that uses the simulation costing version.</span></span>
-   <span data-ttu-id="0757b-121">**現在有効**の予備原則を指定します。</span><span class="sxs-lookup"><span data-stu-id="0757b-121">Specify a fallback principle of **Current active**.</span></span> <span data-ttu-id="0757b-122">予備原則を使用すると、シミュレーションのために増額原価変更を入力でき、他のすべての原価レコードに対するソースとしては現在有効原価を使用します。</span><span class="sxs-lookup"><span data-stu-id="0757b-122">The fallback principle enables incremental cost changes to be entered for simulation purposes but uses the current active costs as the source for all other cost records.</span></span> <span data-ttu-id="0757b-123">ここでは、他のすべての原価レコードに対し、すべての現在有効原価が存在すると想定します。</span><span class="sxs-lookup"><span data-stu-id="0757b-123">We assume that all current active costs exist for all other cost records.</span></span>
-   <span data-ttu-id="0757b-124">**バージョンの原価価格**の原価価格モデルを指定しますが、計算を制限しないでください。</span><span class="sxs-lookup"><span data-stu-id="0757b-124">Specify a cost price model of **Version cost price**, but don't restrict calculations.</span></span> <span data-ttu-id="0757b-125">たとえば、シミュレーションは、**BOM 計算グループ**の原価価格モデルを使用して、購入品目に対する原価貢献度データのソースを示す場合もあります。</span><span class="sxs-lookup"><span data-stu-id="0757b-125">For example, the simulations can also use the **BOM calculation group** cost price model to indicate the source of cost contribution data for purchased items.</span></span>
-   <span data-ttu-id="0757b-126">**複数レベル**の展開モードを指定しますが、計算を制限しないでください。</span><span class="sxs-lookup"><span data-stu-id="0757b-126">Specify an explosion mode of **Multilevel**, but don't restrict calculations.</span></span> <span data-ttu-id="0757b-127">シミュレーションで他の展開モードが使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0757b-127">The simulations can use other explosion modes.</span></span>

## <a name="costing-versions"></a><span data-ttu-id="0757b-128">原価バージョン</span><span class="sxs-lookup"><span data-stu-id="0757b-128">Costing versions</span></span>
<span data-ttu-id="0757b-129">次のシナリオでは、シミュレーション原価バージョンを使用した原価変更の影響のシミュレーションを示します。</span><span class="sxs-lookup"><span data-stu-id="0757b-129">The following scenarios illustrate how the simulation costing version is used to simulate the impact of cost changes.</span></span> <span data-ttu-id="0757b-130">シミュレーション原価変更を入力する前に、シミュレーション原価バージョン内の保留中原価レコードを削除して、何もない状態から開始してください。</span><span class="sxs-lookup"><span data-stu-id="0757b-130">Before you enter a simulated cost change, delete the pending cost records in the simulation costing version, so that you have a clean starting point.</span></span> <span data-ttu-id="0757b-131">品目の価格および原価カテゴリの価格に関係のある保留中原価レコードを表示および削除するには、**品目の価格**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="0757b-131">Use the **Item price** page to view and delete the pending cost records that are related to item prices and cost category prices.</span></span>

-   <span data-ttu-id="0757b-132">購入品目の原価変更をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0757b-132">Simulate the cost change for a purchased item.</span></span> <span data-ttu-id="0757b-133">たとえば、原価変更は、重要な購入材料の原価に予想される上昇または下落を反映する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0757b-133">For example, the cost change might reflect an expected increase or decrease in the cost of critical purchased materials.</span></span> <span data-ttu-id="0757b-134">購入品目に対して異なる原価を定義するには、**品目価格**ページを使用して、シミュレーション原価バージョン内の保留中原価レコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="0757b-134">To define the different cost for a purchased item, use the **Item price** page to enter a pending cost record in the simulation costing version.</span></span>
-   <span data-ttu-id="0757b-135">原価カテゴリの原価変更をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0757b-135">Simulate the cost change for a cost category.</span></span> <span data-ttu-id="0757b-136">たとえば、原価変更は、労務費率や、運営リソースの時間レートに予想される上昇または下落を反映する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0757b-136">For example, the cost change might reflect an expected increase or decrease in labor rates, or in the hourly rates for operations resources.</span></span> <span data-ttu-id="0757b-137">原価カテゴリに対して異なる原価を定義するには、**原価カテゴリ価格**ページを使用して、シミュレーション原価バージョン内の保留中原価レコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="0757b-137">To define the different cost for a cost category, use the **Cost category price** page to enter a pending cost record in the simulation costing version.</span></span>
-   <span data-ttu-id="0757b-138">間接原価計算式における原価変更をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="0757b-138">Simulate the cost change in an indirect cost calculation formula.</span></span> <span data-ttu-id="0757b-139">たとえば、原価変更は、製造諸経費に予想される上昇または下落を反映する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0757b-139">For example, the cost change might reflect an expected increase or decrease in manufacturing overhead.</span></span> <span data-ttu-id="0757b-140">間接原価計算式での変更を定義するには、**原価計算表設定**ページを使用して、シミュレーション原価バージョン内の保留中原価レコードを入力し、変更を検証して保存します。</span><span class="sxs-lookup"><span data-stu-id="0757b-140">To define the change in an indirect cost calculation formula, use the **Costing sheet setup** page to enter a pending cost record in the simulation of costing version, and to validate and save the change.</span></span>

<span data-ttu-id="0757b-141">シミュレーション原価変更を入力した後、原価変更の影響を受ける製造品目の原価を計算します。</span><span class="sxs-lookup"><span data-stu-id="0757b-141">After you enter the simulated cost changes, calculate the costs for manufactured items that are affected by the cost changes.</span></span> <span data-ttu-id="0757b-142">シミュレーション原価バージョンの**計算**ページを使用して、原価変更の影響を受ける製造品目を選択して指定します。</span><span class="sxs-lookup"><span data-stu-id="0757b-142">Use the **Calculation** page for the simulation costing version, and identify the selected manufactured items that will be affected by the cost changes.</span></span> <span data-ttu-id="0757b-143">特定の品目を選択しない限り、BOM 計算はすべての製造品目に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0757b-143">The BOM calculations apply to all manufactured items unless you select specific items.</span></span> <span data-ttu-id="0757b-144">代わりに、使用場所更新の BOM 計算オプションを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0757b-144">Alternatively, you can use the BOM calculation option for where-used updates.</span></span> <span data-ttu-id="0757b-145">シミュレーション原価バージョン内の品目原価レコードを調べて、シミュレーション原価変更による選択した製造品目の原価への影響を分析します。</span><span class="sxs-lookup"><span data-stu-id="0757b-145">View the item cost records in the simulation costing version to analyze how the simulated cost changes affected the costs of the selected manufactured items.</span></span> <span data-ttu-id="0757b-146">**品目価格**ページおよび**品目原価の計算**ページを使用して、原価を表示または分析します。</span><span class="sxs-lookup"><span data-stu-id="0757b-146">Use the **Item price** page and the **Calculate item cost** page to view and analyze the costs.</span></span>



