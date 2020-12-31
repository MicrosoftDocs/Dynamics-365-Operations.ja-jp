---
title: 消費償却
description: この記事は、消費方法の減価償却の概要を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445065"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="66737-103">消費償却</span><span class="sxs-lookup"><span data-stu-id="66737-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66737-104">この記事は、消費方法の減価償却の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="66737-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="66737-105">固定資産減価償却プロファイルを設定し、**減価償却プロファイル** ページの **方法** フィールドにある **消費** を選択した場合、固定資産は使用の度合いに基づいて減価償却プロファイルに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="66737-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="66737-106">**減価償却プロファイル** ページでパーセンテージと間隔を設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="66737-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="66737-107">[消費] 方法を使用する減価償却プロファイルを作成後、さまざまな方法でその方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="66737-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="66737-108">消費償却の設定および使用</span><span class="sxs-lookup"><span data-stu-id="66737-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="66737-109">**減価償却プロファイル** ページで、減価償却プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="66737-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="66737-110">消費の計算では、減価償却プロファイルは ID と名前を必要とし、**消費** を **方法** フィールドで選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66737-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="66737-111">**消費係数** ページで、消費係数を設定します。</span><span class="sxs-lookup"><span data-stu-id="66737-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="66737-112">各消費係数は、ID と名前、および数量またはパーセントのいずれかで指定した消費係数を必要とします。</span><span class="sxs-lookup"><span data-stu-id="66737-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="66737-113">**消費単位** ページで、消費単位を設定します。</span><span class="sxs-lookup"><span data-stu-id="66737-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="66737-114">各消費単位には、ID と名前が必要です。</span><span class="sxs-lookup"><span data-stu-id="66737-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="66737-115">減価償却単位が、**消費償却** ページでの消費償却の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="66737-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="66737-116">単位の例として、キロメートル (km)、キログラム (kg)、時間があります。</span><span class="sxs-lookup"><span data-stu-id="66737-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="66737-117">**固定資産** ページで、個々の固定資産を設定します。</span><span class="sxs-lookup"><span data-stu-id="66737-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="66737-118">各固定資産について、減価償却プロファイルを持つ価値モデルおよび減価償却簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="66737-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="66737-119">[消費] 方法に基づいた減価償却プロファイルを使用する固定資産がある場合、消費償却の価値モデルまたは減価償却簿を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66737-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="66737-120">この設定は、**価値モデル** ページの **減価償却** タブ、または **減価償却プロファイル** ページの **全般** クイック タブで行います。</span><span class="sxs-lookup"><span data-stu-id="66737-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="66737-121">多数の固定資産に対して、同一の価値モデルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="66737-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="66737-122">減価償却プロファイルは、各固定資産に対して選択する価値モデルや減価償却簿の一部です。</span><span class="sxs-lookup"><span data-stu-id="66737-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="66737-123">減価償却プロファイルの追加や変更を、**固定資産** ページで直接行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="66737-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="66737-124">減価償却プロファイルの変更は、**減価償却簿** ページでのみ行うことができます。</span><span class="sxs-lookup"><span data-stu-id="66737-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="66737-125">**価値モデル** ページまたは **減価償却簿** ページで、**消費償却** フィールド グループの次のフィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="66737-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="66737-126">消費量係数</span><span class="sxs-lookup"><span data-stu-id="66737-126">Consumption factor</span></span>
    -   <span data-ttu-id="66737-127">単位</span><span class="sxs-lookup"><span data-stu-id="66737-127">Unit</span></span>
    -   <span data-ttu-id="66737-128">個別償却</span><span class="sxs-lookup"><span data-stu-id="66737-128">Unit depreciation</span></span>
    -   <span data-ttu-id="66737-129">消費予測</span><span class="sxs-lookup"><span data-stu-id="66737-129">Estimated consumption</span></span>

    <span data-ttu-id="66737-130">**転記された消費** フィールドには、固定資産と価値モデルの組合せについて、または固定資産減価償却簿について転記済の消費償却が個別に表示されます。</span><span class="sxs-lookup"><span data-stu-id="66737-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="66737-131">このフィールドの値を手動で更新できません。</span><span class="sxs-lookup"><span data-stu-id="66737-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="66737-132">例</span><span class="sxs-lookup"><span data-stu-id="66737-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="66737-133">例 1</span><span class="sxs-lookup"><span data-stu-id="66737-133">Example 1</span></span>

<span data-ttu-id="66737-134">次の消費係数が 1 月 31 日に対して設定されています。</span><span class="sxs-lookup"><span data-stu-id="66737-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="66737-135">数量は 1,000 です。</span><span class="sxs-lookup"><span data-stu-id="66737-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="66737-136">固定資産に対して指定されている償却単価は 1.5 です。</span><span class="sxs-lookup"><span data-stu-id="66737-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="66737-137">1 月 31 日の償却提案は次のとおりです。数量 × 個別償却 1,000 × 1.5 = 1,500。固定資産に指定される係数が比率係数の場合、固定資産の価値モデルについて **消費予測** フィールドで予測されている数量に、選択した終了日に対して設定されている比率が掛け合わされます。</span><span class="sxs-lookup"><span data-stu-id="66737-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="66737-138">その結果の数量がその期間の減価償却数量として提示されます。</span><span class="sxs-lookup"><span data-stu-id="66737-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="66737-139">例 2</span><span class="sxs-lookup"><span data-stu-id="66737-139">Example 2</span></span>

<span data-ttu-id="66737-140">次の消費償却係数が 1 月 31 日に対して設定されています。</span><span class="sxs-lookup"><span data-stu-id="66737-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="66737-141">比率は 10% です。</span><span class="sxs-lookup"><span data-stu-id="66737-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="66737-142">固定資産に対して指定されている償却単価は 1.5 です。</span><span class="sxs-lookup"><span data-stu-id="66737-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="66737-143">固定資産の見積数量は 2,000 です。</span><span class="sxs-lookup"><span data-stu-id="66737-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="66737-144">1 月 31 日の償却提案は次のとおりです。見積数量 × 比率 × 個別償却 2,000 × 0.10 × 1.5 = 300</span><span class="sxs-lookup"><span data-stu-id="66737-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



