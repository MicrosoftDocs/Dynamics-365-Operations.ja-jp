---
title: ヘッダー モジュール
description: このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025673"
---
# <a name="header-module"></a><span data-ttu-id="780f3-103">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="780f3-104">このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce でのページ ヘッダーの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="780f3-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="780f3-105">概要</span><span class="sxs-lookup"><span data-stu-id="780f3-105">Overview</span></span>

<span data-ttu-id="780f3-106">Dynamics 365 Commerce では、ページヘッダーは、ヘッダー、ナビゲーション メニュー、検索、プロモーション バナー、Cookie の同意モジュールなど、複数のモジュールで構成されます。</span><span class="sxs-lookup"><span data-stu-id="780f3-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="780f3-107">ヘッダー モジュールには、サイトのロゴ、ナビゲーション階層へのリンク、サイト上の他のページへのリンク、カート記号、欲しい物記号、サインイン オプション、検索バーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="780f3-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="780f3-108">ヘッダー モジュールは、サイトが表示されているデバイス (デスクトップ デバイスまたはモバイル デバイス) に対して自動的に最適化されます。</span><span class="sxs-lookup"><span data-stu-id="780f3-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="780f3-109">たとえば、モバイル デバイスでは、ナビゲーションバーを**メニュー** ボタンで折りたたむことができます (このボタンは、*ハンバーガー メニュー*と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="780f3-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="780f3-110">ヘッダー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="780f3-110">Properties of a header module</span></span>

<span data-ttu-id="780f3-111">ヘッダー モジュールは、**ロゴの画像**、**ロゴのリンク**、および**個人用アカウント リンク**のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="780f3-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="780f3-112">**ロゴのイメージ**と**ロゴのリンク**のプロパティは、ページでロゴを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="780f3-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="780f3-113">詳細については、[タブの追加](add-logo.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="780f3-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="780f3-114">**個人用アカウント リンク**プロパティを使用すると、サイト所有者がヘッダーでのクイック リンクを表示するためのアカウント ページを定義できます。</span><span class="sxs-lookup"><span data-stu-id="780f3-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="780f3-115">ヘッダー モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-115">Modules that are available in a header module</span></span>

<span data-ttu-id="780f3-116">ヘッダー モジュールで使用できるモジュールは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="780f3-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="780f3-117">**ナビゲーション メニュー** – ナビゲーション メニューは、チャネル ナビゲーション階層やその他の静的ナビゲーション リンクを表します。</span><span class="sxs-lookup"><span data-stu-id="780f3-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="780f3-118">チャネル ナビゲーション階層は、Dynamics 365 Commerce でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="780f3-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="780f3-119">ナビゲーション メニューには、Retail Server ナビゲーション メニュー項目と静的メニュー項目をソースとして指定するために使用される**ナビゲーション ソース** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="780f3-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="780f3-120">静的メニュー項目がソースとして指定されている場合は、サイトの他のページへの相対リンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="780f3-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="780f3-121">コンフィギュレーションされた品目は、ヘッダー ナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="780f3-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="780f3-122">**検索** – 検索モジュールを使用すると、ユーザーは検索用語を入力して製品を検索できます。</span><span class="sxs-lookup"><span data-stu-id="780f3-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="780f3-123">既定の検索ページの URL および検索クエリ パラメーターは、**サイトの設定 \> 拡張子**で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="780f3-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="780f3-124">検索モジュールには、検索ボタンまたはラベルを必要に応じて非表示にできるプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="780f3-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="780f3-125">また、検索モジュールは、製品、キーワード、カテゴリ検索の結果など、自動提案オプションもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="780f3-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="780f3-126">ページのヘッダー モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="780f3-126">Create a header module for a page</span></span>

<span data-ttu-id="780f3-127">ヘッダー モジュールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="780f3-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="780f3-128">**ヘッダー フラグメント**という名前のフラグメントを作成し、それにコンテナー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="780f3-129">コンテナー モジュールのプロパティ ウィンドウで、**幅**プロパティを**全コンテナー**に設定します。</span><span class="sxs-lookup"><span data-stu-id="780f3-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="780f3-130">コンテナー モジュールにプロモーション バナーと Cookie の同意モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="780f3-131">フラグメントに別のコンテナー モジュールを追加し、**幅**プロパティを**全コンテナー**に設定します。</span><span class="sxs-lookup"><span data-stu-id="780f3-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="780f3-132">ヘッダー モジュールを 2つ目のコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="780f3-133">ヘッダーモジュールの**ナビゲーション メニュー** スロットに、ナビゲーション メニュー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="780f3-134">ナビゲーション メニュー モジュールのプロパティ ウィンドウで、ナビゲーション メニュー モジュールのプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="780f3-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="780f3-135">ヘッダー モジュールの**検索**スロットで、検索モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="780f3-136">検索モジュールのプロパティ ウィンドウで、検索モジュールのプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="780f3-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="780f3-137">ページ フラグメントを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="780f3-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="780f3-138">すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="780f3-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="780f3-139">既定のページの**メイン** スロットで、ヘッダー モジュールを含むヘッダー ページ フラグメントをヘッダーに追加します。</span><span class="sxs-lookup"><span data-stu-id="780f3-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="780f3-140">テンプレートを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="780f3-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="780f3-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="780f3-141">Additional resources</span></span>

[<span data-ttu-id="780f3-142">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="780f3-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="780f3-143">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="780f3-144">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="780f3-145">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="780f3-146">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="780f3-147">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="780f3-148">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="780f3-149">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="780f3-149">Footer module</span></span>](author-footer-module.md)
