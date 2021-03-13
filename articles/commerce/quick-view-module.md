---
title: クイック ビュー モジュール
description: このトピックでは、クイック ビュー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097055"
---
# <a name="quick-view-module"></a><span data-ttu-id="826a1-103">クイック ビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="826a1-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="826a1-104">このトピックでは、クイック ビュー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="826a1-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="826a1-105">クイック ビュー モジュールを使用すると、商品詳細ページ (PDP) に移動することなく、リストページで商品を閲覧した際に商品情報を素早く表示し、リストページから1つ以上の商品をカートに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="826a1-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="826a1-106">クイックビューモジュールは、ユーザーが「カートに追加」を決断するために必要な製品情報の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="826a1-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="826a1-107">また、PDP へのリンクも提供されており、ユーザーは追加の製品詳細や購入オプションを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="826a1-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="826a1-108">クイック ビュー モジュールは、[製品コレクション](product-collection-module-overview.md)と[検索結果モジュール](search-result-module.md)によってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="826a1-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="826a1-109">クイック ビュー モジュールは、Commerce バージョン 10.0.17 リリース時点で使用できます。</span><span class="sxs-lookup"><span data-stu-id="826a1-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="826a1-110">次の図は、商品一覧ページのクイック ビュー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="826a1-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![商品一覧ページにおけるクイック ビュー モジュールの例](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="826a1-112">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="826a1-112">Module properties</span></span>

<span data-ttu-id="826a1-113">クイック ビュー モジュールは、購入ボックス モジュールと同じ機能の一部をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="826a1-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="826a1-114">したがって、クイック ビュー モジュールのプロパティは、購入ボックス モジュールのプロパティと同じように表示されます。</span><span class="sxs-lookup"><span data-stu-id="826a1-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="826a1-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="826a1-115">Property</span></span> | <span data-ttu-id="826a1-116">値</span><span class="sxs-lookup"><span data-stu-id="826a1-116">Values</span></span> | <span data-ttu-id="826a1-117">説明</span><span class="sxs-lookup"><span data-stu-id="826a1-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="826a1-118">ヘッダー タグ</span><span class="sxs-lookup"><span data-stu-id="826a1-118">Heading tag</span></span> | <span data-ttu-id="826a1-119">**H1**、**H2**、**H3**、**H4**、**H5**、**H6**</span><span class="sxs-lookup"><span data-stu-id="826a1-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="826a1-120">このプロパティは、製品タイトルの見出しタグを定義します。</span><span class="sxs-lookup"><span data-stu-id="826a1-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="826a1-121">クイック ビュー モジュールがページの一番上にある場合は、アクセシビリティ標準を満たすため、このプロパティを **H1** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="826a1-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="826a1-122">カスタム価格の許可</span><span class="sxs-lookup"><span data-stu-id="826a1-122">Allow custom price</span></span> | <span data-ttu-id="826a1-123">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="826a1-123">**True** or **False**</span></span> | <span data-ttu-id="826a1-124">このプロパティが **True** に設定されている 場合、ユーザーはカスタム価格を入力できます。</span><span class="sxs-lookup"><span data-stu-id="826a1-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="826a1-125">最小価格</span><span class="sxs-lookup"><span data-stu-id="826a1-125">Minimum price</span></span> | <span data-ttu-id="826a1-126">整数</span><span class="sxs-lookup"><span data-stu-id="826a1-126">Integer</span></span> | <span data-ttu-id="826a1-127">このプロパティは、**カスタム価格を許容する** プロパティが **True** に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="826a1-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="826a1-128">これは、ユーザーが入力できる最小価格を定義します (価格変更など$1)。</span><span class="sxs-lookup"><span data-stu-id="826a1-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="826a1-129">最大価格</span><span class="sxs-lookup"><span data-stu-id="826a1-129">Maximum price</span></span> | <span data-ttu-id="826a1-130">整数</span><span class="sxs-lookup"><span data-stu-id="826a1-130">Integer</span></span> | <span data-ttu-id="826a1-131">このプロパティは、**カスタム価格を許容する** プロパティが **True** に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="826a1-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="826a1-132">これは、ユーザーが入力できる最大価格を定義します (価格変更など$1,000)。</span><span class="sxs-lookup"><span data-stu-id="826a1-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="826a1-133">Commerce のサイト ビルダーの設定</span><span class="sxs-lookup"><span data-stu-id="826a1-133">Commerce site builder settings</span></span>

<span data-ttu-id="826a1-134">購入ボックス モジュールと同様に、クイック ビュー モジュールは **サイト設定 \> 拡張機能 \> 買い物カゴに製品を追加する** での設定を反映します。</span><span class="sxs-lookup"><span data-stu-id="826a1-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="826a1-135">ただし、**カートに移動** ページの設定は、クイック ビュー モジュールの目的と整合しないため無視されます。この目的とは、ユーザーがリスト ページ上で複数の商品を閲覧し、リストページから離れることなくカートに追加できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="826a1-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="826a1-136">製品コレクション モジュールにクイック ビュー モジュールを追加する</span><span class="sxs-lookup"><span data-stu-id="826a1-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="826a1-137">商品コレクションや検索結果モジュールにクイック ビュー モジュールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="826a1-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="826a1-138">Commerce サイト ビルダーの商品コレクション モジュールにクイック ビュー モジュールを追加するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="826a1-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="826a1-139">**ページ** に移動し、Fabrikamサイトのホーム ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="826a1-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="826a1-140">ホームページの任意の **製品コレクション**  モジュールに移動し、省略記号 **...** を選択して、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="826a1-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="826a1-141">**モジュールの追加** ダイアログ ボックスで、**クイック ビュー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="826a1-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="826a1-142">**クイック ビュー** モジュールのプロパティ ウィンドウで、**見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="826a1-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="826a1-143">**見出し** ダイアログ ボックスで、**ヘッダーレベル** フィールドを **H2** に設定し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="826a1-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="826a1-144">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="826a1-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="826a1-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="826a1-145">Additional resources</span></span>

[<span data-ttu-id="826a1-146">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="826a1-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="826a1-147">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="826a1-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="826a1-148">製品収集モジュール</span><span class="sxs-lookup"><span data-stu-id="826a1-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="826a1-149">検索結果モジュール</span><span class="sxs-lookup"><span data-stu-id="826a1-149">Search results module</span></span>](search-result-module.md)
