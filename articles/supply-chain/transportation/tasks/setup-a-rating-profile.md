---
title: 評価プロファイル
description: このトピックでは、評価プロファイルのデータ設定方法について説明します。
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828445"
---
# <a name="rating-profiles"></a><span data-ttu-id="c4fe5-103">評価プロファイル</span><span class="sxs-lookup"><span data-stu-id="c4fe5-103">Rating profiles</span></span>

<span data-ttu-id="c4fe5-104">評価プロファイルは、物流契約に似ています (ただし、法的契約ではありません)。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="c4fe5-105">これを使用して、積荷の輸送税率を特定します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="c4fe5-106">各評価プロファイルは出荷配送業者によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="c4fe5-107">プロファイルでは、出荷配送業者をレート マスターに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="c4fe5-108">レート マスターは、レート基準の割り当てとレート基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="c4fe5-109">レート基準は、配送業者のレートを決定します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="c4fe5-110">すべての既存の評価プロファイルの概要が表示される一般的なページを使用して、評価のプロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="c4fe5-111">または、出荷配送業者から評価プロファイルを直接設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="c4fe5-112">どちらの場合も、評価プロファイルに対して設定した情報は同じです。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="c4fe5-113">[評価プロファイル] ページでの評価プロファイルの作成または編集</span><span class="sxs-lookup"><span data-stu-id="c4fe5-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="c4fe5-114">**評価プロファイル** ページでは、使用可能なすべての評価プロファイルを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="c4fe5-115">既存のプロファイルを編集したり、新しいプロファイルを作成したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="c4fe5-116">**輸送管理 \> 設定 \> 評価 \> 評価プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="c4fe5-117">アクション ペインで **新規** を選択して新しい評価プロファイルをグリッド追加するか、**編集** を選択して既存のプロファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="c4fe5-118">新規または既存の評価プロファイルの行で、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="c4fe5-119">**評価プロファイル** - 評価プロファイルの一意識別子 (ID) を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="c4fe5-120">**名前** - 評価プロファイルに、内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="c4fe5-121">**出荷配送業者** - 出荷配送業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="c4fe5-122">設定している評価プロファイルは、選択した配送業者の **出荷配送業者** ページにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="c4fe5-123">**サイト** および **倉庫** - サイトと倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="c4fe5-124">**レート エンジン** - 評価プロファイルのレート エンジンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="c4fe5-125">**レート マスター** - 評価プロファイルのレート マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="c4fe5-126">レート マスターを使用して、レート基準タイプおよびレート基準を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="c4fe5-127">詳細については、[レート マスターの設定](set-up-rate-masters.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="c4fe5-128">**輸送時間エンジン** - 評価プロファイルの輸送時間エンジンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="c4fe5-129">**配送業者の燃料インデックス** - 評価プロファイルに配送業者の燃料インデックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="c4fe5-130">**有効開始日時** と **有効終了日時** - 評価プロファイルを有効にする期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="c4fe5-131">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="c4fe5-132">[出荷配送業者] ページでの評価プロファイルの直接作成</span><span class="sxs-lookup"><span data-stu-id="c4fe5-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="c4fe5-133">**輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="c4fe5-134">リストで出荷配送業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="c4fe5-135">**評価プロファイル** クイックタブで、**新規** を選択して、評価プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="c4fe5-136">新しい評価プロファイルのフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="c4fe5-137">これらのフィールドは、このトピックの前のセクションで説明したように、**評価プロファイル** ページのフィールドに対応しています。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="c4fe5-138">**出荷配送業者** ページで作成したプロファイルは、**評価プロファイル** ページにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4fe5-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]