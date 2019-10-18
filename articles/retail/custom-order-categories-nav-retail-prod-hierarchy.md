---
title: 販売促進エンティティの並べ替え順序の変更
description: このトピックでは、Dynamics 365 Retail で、販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c159ff869d6c504fdebbef1fa68115a410c81d85
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019419"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="3cf13-103">販売促進エンティティの並べ替え順序の変更</span><span class="sxs-lookup"><span data-stu-id="3cf13-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3cf13-104">小売業者は、製品の検出を、すべての小売チャンネルでの顧客とのやり取りにおける主要なツールと考えています。</span><span class="sxs-lookup"><span data-stu-id="3cf13-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="3cf13-105">さまざまな機能により、顧客が製品を簡単に検索できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3cf13-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="3cf13-106">たとえば、カテゴリ、検索、およびフィルターを参照できます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="3cf13-107">このトピックでは、 販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="3cf13-108">また、並べ替え順序を変更する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="3cf13-109">概要</span><span class="sxs-lookup"><span data-stu-id="3cf13-109">Overview</span></span>

<span data-ttu-id="3cf13-110">販売促進に関連したさまざまなエンティティを並べ替えるためのサポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="3cf13-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="3cf13-111">このサポートにより、以前には実装パートナーからの拡張を必要としていた既存の顧客シナリオとの整合性が向上しました。</span><span class="sxs-lookup"><span data-stu-id="3cf13-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="3cf13-112">バージョン 10.0.5 よりも前の Retail のバージョンでは、ナビゲーション階層でのカテゴリの並べ替え順序はアルファベット順になっていました。</span><span class="sxs-lookup"><span data-stu-id="3cf13-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="3cf13-113">新しいカスタム並べ替え順序機能を使用すると、販売促進マネージャーは、すべてのエンド ユーザー クライアントでの販売促進に関連したさまざまなエンティティの並べ替え順序をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="3cf13-114">これらのクライアントには、本社 (HQ) およびコール センターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="3cf13-115">小売製品階層でのカテゴリに対する表示順序のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3cf13-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="3cf13-116">この手順を完了する前に、デモ データが環境にインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cf13-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="3cf13-117">**小売 \> 製品とカテゴリ \> 小売製品階層**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="3cf13-118">**カテゴリ階層の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cf13-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="3cf13-119">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cf13-119">Click **Edit**.</span></span>
4. <span data-ttu-id="3cf13-120">ツリーで、**ALL \> Action Sports** を展開します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="3cf13-121">ツリーで、**ALL \> Team Sports** を展開します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="3cf13-122">**表示順序**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="3cf13-123">(数値は負の場合があります。)</span><span class="sxs-lookup"><span data-stu-id="3cf13-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="3cf13-124">順序を変更する追加のカテゴリに対して、手順 4 ～ 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="3cf13-125">チャネル ナビゲーション階層の表示順序は、小売製品階層およびカテゴリ別のリリース済製品に対して HQ で反映されます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![負の値でカスタム並べ替えされた小売製品階層](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![小売製品階層に基づいてカスタム並べ替えされた、カテゴリ別のリリース済製品](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="3cf13-128">チャネル ナビゲーション階層でのカテゴリに対する表示順序のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3cf13-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="3cf13-129">この手順を完了する前に、デモ データが環境にインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cf13-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="3cf13-130">**小売 \> 製品とカテゴリ \> チャネル ナビゲーション カテゴリ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="3cf13-131">一覧で、**ファッション ナビゲーション**階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="3cf13-132">**カテゴリ階層の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cf13-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="3cf13-133">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3cf13-133">Click **Edit**.</span></span>
5. <span data-ttu-id="3cf13-134">ツリーで、**ファッション \> ウィメンズウェア \> ウィメンズ シューズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="3cf13-135">**表示順序**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="3cf13-136">ツリーで、**ファッション \> ウィメンズウェア \> トップス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="3cf13-137">同様に、サブカテゴリの並べ替え順序を定義できます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="3cf13-138">ツリーで、**ファッション \> メンズウェア \> カジュアル シャツ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="3cf13-139">**表示順序**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="3cf13-140">ツリーで、**ファッション \> メンズウェア \> コート & ジャケット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="3cf13-141">**表示順序**フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="3cf13-142">順序を変更する任意の追加のカテゴリに対して繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3cf13-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="3cf13-143">チャネル ナビゲーション階層の表示順序は HQ、カタログ、および小売チャネルで反映されます。</span><span class="sxs-lookup"><span data-stu-id="3cf13-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![カスタム並べ替えされたチャネル ナビゲーション階層](./media/ChannelNavCustomSorted.png)

![チャネル ナビゲーション階層に基づいてカスタム並べ替えされた、カタログ ナビゲーション階層](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![カスタム並べ替えされたカテゴリを含む POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="3cf13-147">既定では、カスタム並べ替え順序機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="3cf13-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="3cf13-148">この機能およびその他の機能を有効にする方法については、[機能管理](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cf13-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
