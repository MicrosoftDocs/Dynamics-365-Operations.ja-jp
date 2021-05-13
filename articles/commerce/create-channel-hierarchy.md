---
title: チャネル ナビゲーション階層の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce にチャネル ナビゲーション階層を作成する方法について説明します。
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951911"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="feb4c-103">チャネル ナビゲーション階層の作成</span><span class="sxs-lookup"><span data-stu-id="feb4c-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="feb4c-104">このトピックでは、Microsoft Dynamics 365 Commerce にチャネル ナビゲーション階層を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="feb4c-105">概要</span><span class="sxs-lookup"><span data-stu-id="feb4c-105">Overview</span></span>

<span data-ttu-id="feb4c-106">チャネル ナビゲーション階層は、製品をグループ化してカテゴリに整理し、製品をオンラインまたは販売時点管理 (POS) で閲覧できるようにします。</span><span class="sxs-lookup"><span data-stu-id="feb4c-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="feb4c-107">チャネル ナビゲーション階層の作成</span><span class="sxs-lookup"><span data-stu-id="feb4c-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="feb4c-108">チャネルのナビゲーション階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feb4c-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="feb4c-109">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> チャネル ナビゲーション カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="feb4c-110">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="feb4c-111">**名前** ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="feb4c-112">**説明** ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="feb4c-113">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-113">Select **Create**.</span></span>
1. <span data-ttu-id="feb4c-114">アクション ウィンドウで、**新しいカテゴリ ノード** を選択してルート ノードを作成します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="feb4c-115">**名前** ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="feb4c-116">**説明** ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="feb4c-117">**フレンドリ名** ボックスに、フレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="feb4c-118">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="feb4c-119">次の図は、ルート ノードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="feb4c-119">The following image shows a example root node.</span></span>

![サンプル ルート ノード](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="feb4c-121">ナビゲーション カテゴリ ノードの作成</span><span class="sxs-lookup"><span data-stu-id="feb4c-121">Create navigation category nodes</span></span>

<span data-ttu-id="feb4c-122">チャネルの製品カテゴリを表すその他のナビゲーション カテゴリ ノードを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feb4c-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="feb4c-123">ナビゲーション ウィンドウで、カテゴリを追加する親ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="feb4c-124">アクション ウィンドウで、**新しいカテゴリ ノード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="feb4c-125">**名前** ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="feb4c-126">**説明** ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="feb4c-127">**フレンドリ名** ボックスに、フレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="feb4c-128">**表示の順序** ボックスに、表示順序を入力します (オプション)。</span><span class="sxs-lookup"><span data-stu-id="feb4c-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="feb4c-129">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="feb4c-130">次の図は、チャネル ナビゲーション階層の完成例を示しています。</span><span class="sxs-lookup"><span data-stu-id="feb4c-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![サンプル チャネル階層](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="feb4c-132">製品をカテゴリ ノードに追加する</span><span class="sxs-lookup"><span data-stu-id="feb4c-132">Add products to category nodes</span></span>

<span data-ttu-id="feb4c-133">カテゴリ ノードに製品を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feb4c-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="feb4c-134">カテゴリ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-134">Select a category node.</span></span>
1. <span data-ttu-id="feb4c-135"> **製品** で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="feb4c-136">製品番号または製品名を使用して追加する新しい製品を検索し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="feb4c-137">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="feb4c-138">選択されたチャネルで製品を表示するためには、チャネル ナビゲーション階層内ノードへの製品の追加だけでなく、その製品をチャネルに類別する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="feb4c-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="feb4c-139">品揃えの詳細については、[品揃え管理](assortments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="feb4c-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="feb4c-140">次の図は、製品が追加されたノードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="feb4c-140">The following image shows an example node with products added.</span></span>

![カテゴリ ノードに追加された製品](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="feb4c-142">製品属性グループをカテゴリ ノードに追加</span><span class="sxs-lookup"><span data-stu-id="feb4c-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="feb4c-143">属性グループは、チャネル ナビゲーション階層内ノードに追加する前に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="feb4c-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="feb4c-144">カテゴリ ノードへ製品属性グループを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feb4c-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="feb4c-145">カテゴリ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-145">Select a category node.</span></span>
1. <span data-ttu-id="feb4c-146">**製品属性グループ** で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="feb4c-147">追加する属性グループを検索し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="feb4c-148">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feb4c-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="feb4c-149">次の図は、製品属性グループが追加されたサンプル ノードを示しています。</span><span class="sxs-lookup"><span data-stu-id="feb4c-149">The following image shows a sample node with product attribute groups added.</span></span>

![ノードで製品属性グループの表示](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="feb4c-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="feb4c-151">Additional resources</span></span>

[<span data-ttu-id="feb4c-152">品揃えの設定</span><span class="sxs-lookup"><span data-stu-id="feb4c-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="feb4c-153">属性および属性グループの管理</span><span class="sxs-lookup"><span data-stu-id="feb4c-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
