---
title: ヘッダー モジュール
description: このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686625"
---
# <a name="header-module"></a><span data-ttu-id="b7146-103">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7146-104">このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7146-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b7146-105">概要</span><span class="sxs-lookup"><span data-stu-id="b7146-105">Overview</span></span>

<span data-ttu-id="b7146-106">Dynamics 365 Commerce では、ページヘッダーは、ヘッダー、ナビゲーション メニュー、検索、プロモーション バナー、Cookie の同意モジュールなど、複数のモジュールで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b7146-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="b7146-107">ヘッダー モジュールには、サイトのロゴ、ナビゲーション階層へのリンク、サイト上の他のページへのリンク、カート記号、欲しい物記号、サインイン オプション、検索バーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7146-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="b7146-108">ヘッダー モジュールは、サイトが表示されているデバイス (デスクトップ デバイスまたはモバイル デバイス) に対して自動的に最適化されます。</span><span class="sxs-lookup"><span data-stu-id="b7146-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="b7146-109">たとえば、モバイル デバイスでは、ナビゲーションバーを**メニュー** ボタンで折りたたむことができます (このボタンは、*ハンバーガー メニュー*と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="b7146-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="b7146-110">以下の図は、ホーム ページにおけるヘッダー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b7146-110">The following image shows an example of a header module on a home page.</span></span>

![ヘッダー モジュールの例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="b7146-112">ヘッダー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7146-112">Properties of a header module</span></span>

<span data-ttu-id="b7146-113">ヘッダー モジュールは、**ロゴの画像**、**ロゴのリンク**、および**個人用アカウント リンク**のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b7146-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="b7146-114">**ロゴのイメージ**と**ロゴのリンク**のプロパティは、ページでロゴを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7146-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="b7146-115">詳細については、[タブの追加](add-logo.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7146-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="b7146-116">**個人用アカウント リンク**プロパティを使用すると、サイト所有者がヘッダーでのクイック リンクを表示するためのアカウント ページを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b7146-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="b7146-117">ヘッダー モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-117">Modules that are available in a header module</span></span>

<span data-ttu-id="b7146-118">ヘッダー モジュールで使用できるモジュールは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="b7146-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="b7146-119">**ナビゲーション メニュー** – ナビゲーション メニューは、チャネル ナビゲーション階層やその他の静的ナビゲーション リンクを表します。</span><span class="sxs-lookup"><span data-stu-id="b7146-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="b7146-120">チャネル ナビゲーション階層は、Dynamics 365 Commerce でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b7146-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b7146-121">ナビゲーション メニューには、Retail Server ナビゲーション メニュー項目と静的メニュー項目をソースとして指定するために使用される**ナビゲーション ソース** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b7146-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="b7146-122">静的メニュー項目がソースとして指定されている場合は、サイトの他のページへの相対リンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="b7146-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="b7146-123">コンフィギュレーションされた品目は、ヘッダー ナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7146-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="b7146-124">**検索** – 検索モジュールを使用すると、ユーザーは検索用語を入力して製品を検索できます。</span><span class="sxs-lookup"><span data-stu-id="b7146-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="b7146-125">既定の検索ページの URL および検索クエリ パラメーターは、**サイトの設定 \> 拡張子**で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7146-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="b7146-126">検索モジュールには、検索ボタンまたはラベルを必要に応じて非表示にできるプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="b7146-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="b7146-127">また、検索モジュールは、製品、キーワード、カテゴリ検索の結果など、自動提案オプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b7146-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="b7146-128">**買い物カゴ アイコン** - 買い物カゴ アイコン モジュールは、買い物カゴ内の品目数を随時示す買い物カゴ アイコンを表します。</span><span class="sxs-lookup"><span data-stu-id="b7146-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="b7146-129">詳細については、[買い物カゴ アイコン モジュール](cart-icon-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7146-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="b7146-130">ページのヘッダー モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="b7146-130">Create a header module for a page</span></span>

<span data-ttu-id="b7146-131">ヘッダー モジュールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b7146-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="b7146-132">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="b7146-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b7146-133">**新規ページ フラグメント** ダイアログ ボックスで、**コンテナー** モジュールを選択し、ページ フラグメントの名前を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-134">既定の **既定のコンテナー**スロットを選択し、右側のプロパティ ウィンドウで **幅**プロパティを**全画面表示**に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="b7146-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="b7146-135">**既定のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-136">**モジュールの追加**  ダイアログ ボックスで、**プロモーション バナー** と **クッキーの同意**モジュールを選択し、続いて **OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-137">**既定のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-138">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-139">既定の **コンテナー**スロットを選択し、右側のプロパティ ウィンドウで **幅**プロパティを**全画面表示**に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="b7146-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="b7146-140">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-141">**モジュールの追加** ダイアログ ボックスで、**ヘッダー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-142">ヘッダー モジュールの**ナビゲーション メニュー** スロットにて、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-143">**モジュールの追加** ダイアログ ボックスで、**ナビゲーション メニュー** を選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-144">ナビゲーション メニュー モジュールのプロパティ ウィンドウで、必要に応じてプロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="b7146-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="b7146-145">ヘッダー モジュールの**検索** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-146">**モジュールの追加** ダイアログ ボックスで、**検索** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-147">検索モジュールのプロパティ ウィンドウで、必要に応じてプロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="b7146-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="b7146-148">ヘッダー モジュールの**買い物カゴ アイコン** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7146-149">**モジュールの追加** ダイアログ ボックスで、**買い物カゴ アイコン** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7146-150">買い物カゴ モジュールのプロパティ ウィンドウで、必要に応じてプロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="b7146-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="b7146-151">ユーザーがマウス オーバーした際に買い物カゴの概要 (ミニカートとも呼ばれます) を表示する場合は、**ミニカートを表示する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7146-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="b7146-152">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="b7146-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b7146-153">すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b7146-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b7146-154">**既定ページ** モジュールの **ヘッダー** スロットに、作成したフッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="b7146-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b7146-155">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="b7146-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7146-156">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b7146-156">Additional resources</span></span>

[<span data-ttu-id="b7146-157">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="b7146-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b7146-158">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b7146-159">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b7146-160">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b7146-161">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b7146-162">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b7146-163">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b7146-164">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b7146-165">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="b7146-165">Footer module</span></span>](author-footer-module.md)
