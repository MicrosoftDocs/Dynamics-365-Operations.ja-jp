---
title: 資産の重要度タイプ
description: このトピックでは、資産管理の資産の重要度タイプについて説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7d6e3dea1b3c1ef47490df678f639c036cdd5c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889820"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="0fda6-103">資産の重要度タイプ</span><span class="sxs-lookup"><span data-stu-id="0fda6-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0fda6-104">このトピックでは、資産管理の資産の重要度タイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="0fda6-105">資産の重要度は資産に関連し、ワーク オーダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="0fda6-106">ワーク オーダーでは変更できません。</span><span class="sxs-lookup"><span data-stu-id="0fda6-106">It can't be changed on a work order.</span></span> <span data-ttu-id="0fda6-107">資産の重要度は、ワーク オーダー スケジューリング中にワーク オーダーの重要度を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="0fda6-108">つまり、資産のどのメンテナンス ジョブが会社の生産スケジュールと生産性にどの程度影響するかを計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="0fda6-109">ワーク オーダー スケジューリングの評価スコアの計算に関連する設定の詳細については、[資産管理パラメーター](../setup-for-objects/enterprise-asset-management-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0fda6-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="0fda6-110">重要度を設定するには、まず資産設定で使用する重要度タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="0fda6-111">それから、資産の重要度の設定をします。</span><span class="sxs-lookup"><span data-stu-id="0fda6-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="0fda6-112">重要度タイプの設定</span><span class="sxs-lookup"><span data-stu-id="0fda6-112">Set up criticality types</span></span>

1. <span data-ttu-id="0fda6-113">**資産管理** \> **設定** \> **資産** \> **重要度タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="0fda6-114">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="0fda6-115">**重要度**フィールドに、重要度を示す数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="0fda6-116">**名前**フィールドに、重要度タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="0fda6-117">**係数**フィールドに係数を入力します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="0fda6-118">この係数は、ワーク オーダー スケジューリングの計算中に使用され、重要度レコードが使用されるべきかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="0fda6-119">(最も高い係数を持つレコードは常に使用されます。) この設定は、次の図に示すように、同じ重要度値を持つ重要度明細行が作成されている場合に関係します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![重大度タイプ ページ](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="0fda6-121">資産の重要度の設定</span><span class="sxs-lookup"><span data-stu-id="0fda6-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="0fda6-122">**資産管理** \> **設定** \> **資産の重要度**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="0fda6-123">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="0fda6-124">資産の重要度の特定のレベルの詳細に応じて、**機能場所**、**資産タイプ**、**メーカー**、**モデル**、**資産**、**ジョブ タイプ カテゴリ**、**ジョブ タイプ**、**ジョブ タイプ バリアント**および**ジョブ要件**フィールドで関連する選択を行います。</span><span class="sxs-lookup"><span data-stu-id="0fda6-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fda6-125">資産の重要度が選択されると、資産管理はすべての資産重要度レコードを調べて、一致の可能性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="0fda6-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="0fda6-126">常に最も限定的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="0fda6-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="0fda6-127">つまり、資産管理は、まず**ジョブ要件**をチェックします。</span><span class="sxs-lookup"><span data-stu-id="0fda6-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="0fda6-128">一致するものが見つからない場合は、**ジョブ タイプ バリアント**がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="0fda6-129">一致するものが見つからない場合は、**ジョブ タイプ**などがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="0fda6-130">ページのレイアウトで分かるように、この動作は、最も限定的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="0fda6-131">一致するものが見つからない場合は、選択がない「既定」のレコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="0fda6-132">**重要度**フィールドで、前の手順で作成した重要度値の一つを選択します。</span><span class="sxs-lookup"><span data-stu-id="0fda6-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="0fda6-133">重要度の設定に関する注記</span><span class="sxs-lookup"><span data-stu-id="0fda6-133">Notes about criticality setup</span></span>

- <span data-ttu-id="0fda6-134">ワーク オーダーで既に使用した後に、この設定で資産の重要度を変更した場合、ワーク オーダーにある重要度は適宜更新されません。</span><span class="sxs-lookup"><span data-stu-id="0fda6-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="0fda6-135">ワーク オーダーにある重要度は、ワーク オーダーにワーク オーダー明細行が追加または削除されるたびに再計算されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="0fda6-136">ワーク オーダーに複数のワーク オーダー ジョブが含まれている場合、**重要度タイプ** ページの**係数**フィールドに従って、ワーク オーダーでは常に最高の重要度が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fda6-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="0fda6-137">一般に、資産の重要度は一定期間で変化する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0fda6-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="0fda6-138">重要度は、新しい機器の購入、改修などによって影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0fda6-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="0fda6-139">資産の重要度を定期的に再評価し (たとえば、1 年または 1 年おきに 1 回)、重要度の定義が現在の生産の設定と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0fda6-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
