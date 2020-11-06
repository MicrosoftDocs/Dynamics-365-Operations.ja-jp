---
title: ヘッダー モジュール
description: このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055453"
---
# <a name="header-module"></a><span data-ttu-id="116a0-103">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="116a0-104">このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="116a0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="116a0-105">概要</span><span class="sxs-lookup"><span data-stu-id="116a0-105">Overview</span></span>

<span data-ttu-id="116a0-106">Dynamics 365 Commerce では、ページのヘッダーは、ヘッダー、プロモーション バナー、cookie 同意モジュールを含むページ フラグメントとして構成されます。</span><span class="sxs-lookup"><span data-stu-id="116a0-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="116a0-107">ヘッダー モジュールには、サイトのロゴ、ナビゲーション階層へのリンク、サイト上の他のページへのリンク、カート アイコンのモジュール、ウィッシュ リスト記号、サインイン オプション、検索バーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="116a0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="116a0-108">ヘッダー モジュールは、サイトが表示されているデバイス (デスクトップ デバイスまたはモバイル デバイス) に対して自動的に最適化されます。</span><span class="sxs-lookup"><span data-stu-id="116a0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="116a0-109">たとえば、モバイル デバイスでは、ナビゲーションバーを **メニュー** ボタンで折りたたむことができます (このボタンは、 *ハンバーガー メニュー* と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="116a0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu* ).</span></span>

<span data-ttu-id="116a0-110">以下の図は、ホーム ページにおけるヘッダー モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="116a0-110">The following image shows an example of a header module on a home page.</span></span>

![ヘッダー モジュールの例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="116a0-112">ヘッダー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="116a0-112">Properties of a header module</span></span>

<span data-ttu-id="116a0-113">ヘッダー モジュールは、 **ロゴの画像** 、 **ロゴのリンク** 、および **個人用アカウント リンク** のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="116a0-113">A header module supports **Logo image** , **Logo link** , and **My account links** properties.</span></span> 

<span data-ttu-id="116a0-114">**ロゴのイメージ** と **ロゴのリンク** のプロパティは、ページでロゴを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="116a0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="116a0-115">詳細については、[タブの追加](add-logo.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="116a0-116">**個人用アカウント リンク** プロパティを使用すると、サイト所有者がヘッダーでのクイック リンクを表示するためのアカウント ページを定義できます。</span><span class="sxs-lookup"><span data-stu-id="116a0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="116a0-117">ヘッダー モジュールで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-117">Modules that are available within a header module</span></span>

<span data-ttu-id="116a0-118">ヘッダー モジュールで使用できるモジュールは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="116a0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="116a0-119">**ナビゲーション メニュー** – ナビゲーション メニューは、チャネル ナビゲーション階層やその他の静的ナビゲーション リンクを表します。</span><span class="sxs-lookup"><span data-stu-id="116a0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="116a0-120">詳細については、[ナビゲーション メニュー モジュール](nav-menu-module.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="116a0-121">**検索** – 検索モジュールを使用すると、ユーザーは検索用語を入力して製品を検索できます。</span><span class="sxs-lookup"><span data-stu-id="116a0-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="116a0-122">既定の検索ページの URL および検索クエリ パラメーターは、 **サイトの設定 \> 拡張子** で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="116a0-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="116a0-123">検索モジュールには、検索ボタンまたはラベルを必要に応じて非表示にできるプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="116a0-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="116a0-124">また、検索モジュールは、製品、キーワード、カテゴリ検索の結果など、自動提案オプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="116a0-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="116a0-125">**買い物カゴ アイコン** - 買い物カゴ アイコン モジュールは、買い物カゴ内の品目数を随時示す買い物カゴ アイコンを表します。</span><span class="sxs-lookup"><span data-stu-id="116a0-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="116a0-126">詳細については、[買い物カゴ アイコン モジュール](cart-icon-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="116a0-127">**サイト セレクター** - サイト選択モジュールを使用すると、市場、地域、およびロケールに基づいて、さまざまな定義済みサイト間での閲覧が可能になります。</span><span class="sxs-lookup"><span data-stu-id="116a0-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="116a0-128">詳細については、[サイト セレクター モジュール](site-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="116a0-129">**店舗セレクター** - ヘッダー モジュールの店舗セレクター スロットに、ストア選択モジュールを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="116a0-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="116a0-130">この機能を使用すると、ユーザーは近くの店舗を参照および検索できます。</span><span class="sxs-lookup"><span data-stu-id="116a0-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="116a0-131">ユーザーは、優先店舗を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="116a0-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="116a0-132">優先店舗はヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="116a0-132">That store will then be shown in the header.</span></span> <span data-ttu-id="116a0-133">店舗選択モジュールがヘッダー モジュールに含まれている場合、 **モード** プロパティを **店舗検索** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="116a0-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="116a0-134">詳細については、[店舗セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="116a0-135">Dynamics 365 Commerce 10.0.11 リリースは、ヘッダー モジュールでの買い物カゴ アイコン モジュールをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="116a0-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="116a0-136">Dynamics 365 Commerce 10.0.14 リリースは、ヘッダー モジュールでのサイト セレクター モジュールをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="116a0-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="116a0-137">Dynamics 365 Commerce 10.0.15 リリースは、ヘッダー モジュールでの店舗セレクター モジュールをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="116a0-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="116a0-138">ページで使用するヘッダー フラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="116a0-138">Create a header fragment for a page</span></span>

<span data-ttu-id="116a0-139">ヘッダー フラグメントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="116a0-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="116a0-140">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="116a0-140">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="116a0-141">**新規フラグメント** ダイアログ ボックスで、 **コンテナー** モジュールを選択し、フラグメントの名前を入力して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-142">既定の **既定のコンテナー** スロットを選択し、右側のプロパティ ウィンドウで **幅** プロパティを **全画面表示** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="116a0-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="116a0-143">**既定のコンテナー** スロットの省略ボタン ( **...** ) を選択し、 **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-143">In the **Default container** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="116a0-144">**モジュールの追加** ダイアログ ボックスで、 **クッキーの同意** 、 **ヘッダー** 、 **プロモーション バナー** モジュールを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-144">In the **Add Module** dialog box, select the **Cookie consent** , **Header** , and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-145">**プロモーション バナー** モジュールのプロパティ ペインで 、 **メッセージの追加** を選択し、 **メッセージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-145">In the properties pane of the **Promo banner** module, select **Add Message** , and then select **Message**.</span></span>
1. <span data-ttu-id="116a0-146">**メッセージ** ダイアログ ボックスで、テキストとプロモーション コンテンツのリンクを追加し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-147">**Cookie の同意** モジュールのプロパティ ペインで、テキストとサイトのプライバシー ページへのリンクを追加して構成します。</span><span class="sxs-lookup"><span data-stu-id="116a0-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="116a0-148">ヘッダー モジュールの **ナビゲーション メニュー** スロットにて、省略記号 ( **...** ) を選択し、 **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-148">In the **Navigation menu** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="116a0-149">**モジュールの追加** ダイアログ ボックスで、 **ナビゲーション メニュー** を選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-150">ナビゲーション メニュー モジュールのプロパティ ペインで、 **ナビゲーション メニューのソース** 配下の **小売りサーバー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-150">In the property pane for the navigation menu module, under **Source for navigation menu** , select **Retail Server**.</span></span>
1. <span data-ttu-id="116a0-151">ナビゲーション メニュー モジュールのプロパティ ペインで、 **静的メニュー項目** 配下の **メニュー項目の追加** を選択し、 **メニュー項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-151">In the property pane for the navigation menu module, under **Static menu items** , select **Add Menu item** , and then select **Menu item**.</span></span> 
1. <span data-ttu-id="116a0-152">**メニュー項目** ダイアログ ボックスで、 **メニュー項目テキスト** の下に 「連絡先」と入力します。</span><span class="sxs-lookup"><span data-stu-id="116a0-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="116a0-153">**メニュー項目** ダイアログ ボックスの **メニュー項目リンク ターゲット** 配下の、 **リンクの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="116a0-154">**リンクの追加** ダイアログ ボックスで、サイトの「コンタクト」ページに利用する URL を選択し、続いて、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="116a0-155">**メニュー項目** のダイアログ ボックスで、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="116a0-156">ヘッダー モジュールの **検索** スロットで、省略記号 ( **...** ) を選択し、 **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-156">In the **Search** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="116a0-157">**モジュールの追加** ダイアログ ボックスで、 **検索** モジュールを選択して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-158">検索モジュールのプロパティ ウィンドウで、必要に応じてプロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="116a0-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="116a0-159">ヘッダー モジュールの **買い物カゴ アイコン** スロットで、省略記号 ( **...** ) を選択し、 **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-159">In the **Cart icon** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="116a0-160">**モジュールの追加** ダイアログ ボックスで、 **買い物カゴ アイコン** モジュールを選択して、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="116a0-161">買い物カゴ モジュールのプロパティ ウィンドウで、必要に応じてプロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="116a0-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="116a0-162">ユーザーがマウス オーバーした際に買い物カゴの概要 (ミニカートとも呼ばれます) を表示する場合は、 **ミニカートを表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="116a0-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="116a0-163">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="116a0-163">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="116a0-164">すべてのページにヘッダーが表示されるようにするには、サイトで作成されたすべてのページ テンプレートで次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="116a0-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="116a0-165">**既定ページ** モジュールの **ヘッダー** スロットに、作成したフッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="116a0-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="116a0-166">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="116a0-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="116a0-167">追加リソース</span><span class="sxs-lookup"><span data-stu-id="116a0-167">Additional resources</span></span>

[<span data-ttu-id="116a0-168">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="116a0-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="116a0-169">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="116a0-170">カート アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="116a0-171">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="116a0-172">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="116a0-173">Cookie 同意</span><span class="sxs-lookup"><span data-stu-id="116a0-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="116a0-174">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="116a0-175">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="116a0-176">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="116a0-176">Store selector module</span></span>](store-selector.md)
