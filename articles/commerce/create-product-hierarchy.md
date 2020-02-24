---
title: 新しい製品階層の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce で新しい製品階層を作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001901"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="339d9-103">新しい製品階層の作成</span><span class="sxs-lookup"><span data-stu-id="339d9-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="339d9-104">このトピックでは、Microsoft Dynamics 365 Commerce で新しい製品階層を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="339d9-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="339d9-105">概要</span><span class="sxs-lookup"><span data-stu-id="339d9-105">Overview</span></span>

<span data-ttu-id="339d9-106">Dynamics 365 Commerce は複数の小売チャンネルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="339d9-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="339d9-107">これらの小売チャンネルには、オンライン ストア、コール センター、および小売用店舗 (従来型の店舗とも呼ばれる) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="339d9-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="339d9-108">各小売店舗チャネルは、独自の支払方法、価格グループ、POS レジスタ、収入/経費勘定、およびスタッフを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="339d9-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="339d9-109">小売店舗チャネルを作成する前に、これらのすべての要素を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="339d9-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="339d9-110">Commerce の製品階層は、組織の全体的な製品階層を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="339d9-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="339d9-111">販売促進、価格決定とプロモーション、および品揃え計画に Commerce 製品階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="339d9-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="339d9-112">組織ごとに、1 つの Commerce 製品階層だけを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="339d9-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="339d9-113">製品階層の作成およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="339d9-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="339d9-114">Commerce 製品階層を作成してコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="339d9-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="339d9-115">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> Commerce 製品階層**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="339d9-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="339d9-116">階層がまだ存在しない場合、**アクション ウィンドウ**で**新規**を選択して階層のルートを作成します。</span><span class="sxs-lookup"><span data-stu-id="339d9-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="339d9-117">**一般**の下で:</span><span class="sxs-lookup"><span data-stu-id="339d9-117">Under **General**:</span></span>
    1. <span data-ttu-id="339d9-118">**名前**ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="339d9-119">**説明**ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="339d9-120">**フレンドリ名**ボックスに、フレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="339d9-121">**有効**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="339d9-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="339d9-122">階層ノードの追加</span><span class="sxs-lookup"><span data-stu-id="339d9-122">Add hierarchy nodes</span></span>

<span data-ttu-id="339d9-123">階層ノードを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="339d9-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="339d9-124">アクション ウィンドウで、**カテゴリ階層の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="339d9-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="339d9-125">新しいノードを追加する親ノードを選択し、**新しいカテゴリ ノード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="339d9-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="339d9-126">**一般**セクションで、**名前**、**説明**、**フレンドリ名**、および**キーワード**を指定します。</span><span class="sxs-lookup"><span data-stu-id="339d9-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="339d9-127">**一般**の下で:</span><span class="sxs-lookup"><span data-stu-id="339d9-127">Under **General**:</span></span>
    1. <span data-ttu-id="339d9-128">**名前**ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="339d9-129">**説明**ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="339d9-130">**フレンドリ名**ボックスに、フレンドリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="339d9-131">**キーワード** ボックスで、関連するキーワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="339d9-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="339d9-132">**表示順序**ボックスで、表示順序の番号を入力します (オプション)。</span><span class="sxs-lookup"><span data-stu-id="339d9-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="339d9-133">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="339d9-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="339d9-134">上記の手順を繰り返して、ノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="339d9-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="339d9-135">次の図は、新しい製品階層ノードの作成を示しています。</span><span class="sxs-lookup"><span data-stu-id="339d9-135">The following image shows the creation of a new product hierarchy node.</span></span>

![製品階層の作成](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="339d9-137">その他の設定</span><span class="sxs-lookup"><span data-stu-id="339d9-137">Other settings</span></span>

<span data-ttu-id="339d9-138">必要に応じて、各グループにカテゴリ属性グループを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="339d9-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="339d9-139">追加リソース</span><span class="sxs-lookup"><span data-stu-id="339d9-139">Additional resources</span></span>

[<span data-ttu-id="339d9-140">小売階層</span><span class="sxs-lookup"><span data-stu-id="339d9-140">Retail hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="339d9-141">製品カテゴリおよび製品の管理</span><span class="sxs-lookup"><span data-stu-id="339d9-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="339d9-142">マーチャンダイジング エンティティの並べ替え順序の変更</span><span class="sxs-lookup"><span data-stu-id="339d9-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
