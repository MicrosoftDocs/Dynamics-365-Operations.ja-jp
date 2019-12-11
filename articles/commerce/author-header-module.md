---
title: ヘッダー モジュール
description: このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697278"
---
# <a name="header-module"></a><span data-ttu-id="edd40-103">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-103">Header module</span></span>

<span data-ttu-id="edd40-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="edd40-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="edd40-105">このトピックでは、ヘッダー モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="edd40-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="edd40-106">概要</span><span class="sxs-lookup"><span data-stu-id="edd40-106">Overview</span></span>

<span data-ttu-id="edd40-107">ヘッダー モジュールは、ページのヘッダーに表示されるすべてのモジュールをホストするために使用される特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="edd40-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="edd40-108">たとえば、サイトのロゴ、ナビゲーション階層へのリンク、サイト上の他のページへのリンク、検索バーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="edd40-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="edd40-109">ヘッダー モジュールは、サイトが表示されているデバイス (デスクトップ デバイスまたはモバイル デバイス) に対して自動的に最適化されます。</span><span class="sxs-lookup"><span data-stu-id="edd40-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="edd40-110">たとえば、モバイル デバイスでは、ナビゲーションバーを**メニュー** ボタンで折りたたむことができます (このボタンは、*ハンバーガー メニュー*と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="edd40-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="edd40-111">ヘッダーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="edd40-111">Properties of a header</span></span>

<span data-ttu-id="edd40-112">汎用コンテナーと同様に、ヘッダー モジュールは、**見出し**プロパティおよび**幅**プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="edd40-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="edd40-113">ヘッダー モジュールには複数のスロットがあります。</span><span class="sxs-lookup"><span data-stu-id="edd40-113">A header module has multiple slots.</span></span> <span data-ttu-id="edd40-114">たとえば、情報メッセージ、ナビゲーション メニュー、ロゴ、検索バー、カート アイコン、欲しい物リスト アイコン、およびアカウント情報に使用するスロットがあります。</span><span class="sxs-lookup"><span data-stu-id="edd40-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="edd40-115">各スロットは、特定のモジュールのセットをサポートします。</span><span class="sxs-lookup"><span data-stu-id="edd40-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="edd40-116">ヘッダー モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-116">Modules that are available in a header module</span></span>

<span data-ttu-id="edd40-117">ヘッダー モジュールで使用できるモジュールは次の通りです。</span><span class="sxs-lookup"><span data-stu-id="edd40-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="edd40-118">**ナビゲーション メニュー** – ナビゲーション メニューは、チャネル ナビゲーション階層やその他の静的ナビゲーション リンクを表します。</span><span class="sxs-lookup"><span data-stu-id="edd40-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="edd40-119">チャネル ナビゲーション階層は、Dynamics 365 Retail でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="edd40-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="edd40-120">コンフィギュレーションされた品目は、ヘッダー ナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="edd40-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="edd40-121">さらに、静的なナビゲーション リンクをコンフィギュレーションして、E コマース サイトの他のページへの相対リンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="edd40-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="edd40-122">ヘッダー自体は左揃え、右揃え、または中央揃えにすることができます。</span><span class="sxs-lookup"><span data-stu-id="edd40-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="edd40-123">**カート アイコン** – カート アイコンは、買い物カゴを表す特別なアイコンです。</span><span class="sxs-lookup"><span data-stu-id="edd40-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="edd40-124">ヘッダーに表示され、カート内の品目の数を示します。</span><span class="sxs-lookup"><span data-stu-id="edd40-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="edd40-125">カートのページへのリンクをカート アイコンに添付して、顧客がアイコンを操作したときにカートのページにリダイレクトできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd40-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="edd40-126">**欲しい物リスト アイコン** – 欲しい物リスト アイコンがヘッダーに表示され、顧客の欲しい物リストに追加された品目の数を示します。</span><span class="sxs-lookup"><span data-stu-id="edd40-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="edd40-127">欲しい物リストのページへのリンクをカート アイコンに添付して、顧客がアイコンを操作したときに欲しい物リストのページにリダイレクトできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd40-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="edd40-128">**サインイン モジュール** – サインイン モジュールがヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="edd40-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="edd40-129">顧客は、自分のアカウントにサインインすることも、アカウントにサインアップすることもできます。</span><span class="sxs-lookup"><span data-stu-id="edd40-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="edd40-130">顧客が既にサインインしている場合は、このモジュールをコンフィギュレーションして、アカウント ページ、注文履歴ページ、または別のページへのリンクを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="edd40-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="edd40-131">**ロゴ モジュール** – このモジュールは、小売業者とブランドを表すロゴを表示します。</span><span class="sxs-lookup"><span data-stu-id="edd40-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="edd40-132">この画像にはリンクがあります。</span><span class="sxs-lookup"><span data-stu-id="edd40-132">It's an image that has a link.</span></span> <span data-ttu-id="edd40-133">通常、リンクはホーム ページへのリダイレクトを持つようにコンフィギュレーションされます。したがって、顧客はサイト上の任意のページからホーム ページにすばやく戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="edd40-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="edd40-134">**警告** – ヘッダーに警告が表示され、サイトのすべてのページに適用するインライン メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="edd40-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="edd40-135">たとえば、警告には、「年間セールはあと 2 日で終了します」などのメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="edd40-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="edd40-136">**検索バー** – 検索バーを使用すると、ユーザーは検索用語を入力して製品を検索できます。</span><span class="sxs-lookup"><span data-stu-id="edd40-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="edd40-137">モジュールは、検索結果ページの URL でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="edd40-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="edd40-138">クエリ文字列パラメーターをコンフィギュレーションできます (既定値は **"q"** です)。</span><span class="sxs-lookup"><span data-stu-id="edd40-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="edd40-139">検索バーには、自動提案モジュールを追加する自動提案スロットがあります。</span><span class="sxs-lookup"><span data-stu-id="edd40-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="edd40-140">**自動提案** – 自動提案モジュールは、自動的に提案された結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="edd40-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="edd40-141">これらの結果は、検索用語が見つかったキーワード、製品、またはカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="edd40-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="edd40-142">ヘッダー モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="edd40-142">Create a header module</span></span>

<span data-ttu-id="edd40-143">ヘッダー モジュールを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="edd40-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="edd40-144">ヘッダー モジュールを含むページ フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="edd40-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="edd40-145">ヘッダー モジュールのスロットにモジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="edd40-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="edd40-146">各モジュールの設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="edd40-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="edd40-147">ページ フラグメントを保存します。</span><span class="sxs-lookup"><span data-stu-id="edd40-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="edd40-148">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="edd40-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="edd40-149">すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="edd40-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="edd40-150">既定のページで、ヘッダー モジュールを含むページ フラグメントをメイン スロットのヘッダーに追加します。</span><span class="sxs-lookup"><span data-stu-id="edd40-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="edd40-151">テンプレートを保存します。</span><span class="sxs-lookup"><span data-stu-id="edd40-151">Save the template.</span></span> 
1. <span data-ttu-id="edd40-152">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="edd40-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edd40-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="edd40-153">Additional resources</span></span>

[<span data-ttu-id="edd40-154">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="edd40-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="edd40-155">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="edd40-156">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="edd40-157">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="edd40-158">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="edd40-159">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="edd40-160">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="edd40-161">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="edd40-161">Footer module</span></span>](author-footer-module.md)
