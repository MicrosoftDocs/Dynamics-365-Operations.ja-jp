---
title: モジュール ライブラリの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce モジュール ライブラリの概要を表示します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795336"
---
# <a name="module-library-overview"></a><span data-ttu-id="49140-103">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="49140-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49140-104">このトピックでは、Microsoft Dynamics 365 Commerce モジュール ライブラリの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="49140-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="49140-105">Dynamics 365 Commerce モジュール ライブラリは、E コマース Web サイトを構築するために使用できるモジュールの集合です。</span><span class="sxs-lookup"><span data-stu-id="49140-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="49140-106">モジュールには、ユーザー インターフェイス (UI) の側面と機能的動作の側面の両方があります。</span><span class="sxs-lookup"><span data-stu-id="49140-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="49140-107">モジュール ライブラリのモジュールにテーマを適用して、概観を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="49140-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="49140-108">テーマはカスケード スタイル シート (CSS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="49140-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="49140-109">「Fabrikam」という名前の架空の E コマース サイト用のテーマは、モジュール ライブラリの一部として提供され、参照として使用できます。</span><span class="sxs-lookup"><span data-stu-id="49140-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="49140-110">モジュール ライブラリ モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-110">Module library modules</span></span>

<span data-ttu-id="49140-111">モジュール ライブラリでは、次のタイプのモジュールが提供されます:</span><span class="sxs-lookup"><span data-stu-id="49140-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="49140-112">**コンテナー モジュール** – コンテナー モジュールは他のモジュールのホストとして動作する単純なモジュールです。</span><span class="sxs-lookup"><span data-stu-id="49140-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="49140-113">その中のモジュールのレイアウトを制御します。</span><span class="sxs-lookup"><span data-stu-id="49140-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="49140-114">**マーケティング モジュール** – マーケティング モジュールには、ヒーロー、機能、コンテンツ ブロック、テキスト ブロック、ビデオ プレーヤー、およびカルーセル モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="49140-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="49140-115">これらのモジュールはすべて、コンテンツを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="49140-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="49140-116">任意のページに配置することができ、コンテンツ管理システム (CMS) からのデータによって発生します。</span><span class="sxs-lookup"><span data-stu-id="49140-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="49140-117">**ヘッダー モジュールとフッター モジュール** – ヘッダー モジュールとフッター モジュールは、すべてのサイト ページのヘッダーとフッターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="49140-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="49140-118">これらのモジュールは、必要に応じてプロパティを通じてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="49140-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="49140-119">**検索モジュール** – 製品は、ヘッダーの検索モジュールを使用して検出できます。</span><span class="sxs-lookup"><span data-stu-id="49140-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="49140-120">検索結果は、検索結果ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="49140-120">Search results appear on the search results page.</span></span> <span data-ttu-id="49140-121">チャネル ナビゲーション階層でサポートされる各カテゴリ専用ページのカテゴリ ページで製品を検出することもできます。</span><span class="sxs-lookup"><span data-stu-id="49140-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="49140-122">絞り込みモジュールを使用し、検索結果およびカテゴリ ページで、結果にさらにフィルター処理をすることもできます。</span><span class="sxs-lookup"><span data-stu-id="49140-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="49140-123">**製品の詳細ページのモジュール** – 製品の詳細ページは、さまざまなモジュールを使用して製品情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="49140-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="49140-124">購入ボックス モジュールにより、顧客は製品を表示し、買い物カゴに追加できます。</span><span class="sxs-lookup"><span data-stu-id="49140-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="49140-125">技術仕様モジュールなどの他のモジュールは、製品の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="49140-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="49140-126">評価とレビュー モジュールを使用して、レビューを表示し、提供することができます。</span><span class="sxs-lookup"><span data-stu-id="49140-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="49140-127">**オンライン購入と店舗受取りモジュール** – オンライン購入と店舗受取りモジュールは Bing Maps と統合されます。</span><span class="sxs-lookup"><span data-stu-id="49140-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="49140-128">これを使用し、顧客が購入した製品の受取りができる付近の店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="49140-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="49140-129">**購買モジュール** – 購買モジュールには、買い物カゴに品目を追加するために使用できる買い物カゴ モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="49140-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="49140-130">チェックアウト モジュールは、出荷先住所、出荷オプション、ギフト カードとロイヤルティ プログラム、およびクレジット カード情報を示し、注文を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="49140-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="49140-131">注文が行われた後、注文確認モジュールを使用して、確認の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="49140-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="49140-132">**アカウント管理モジュール** – サインイン モジュールにより、顧客は既存のアカウントにサインインすることができ、サインアップ モジュールにより、新しいアカウントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="49140-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="49140-133">アカウントが作成された後、注文履歴モジュールを使用して最近の注文を表示することができ、注文詳細モジュールを使用して注文の詳細を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="49140-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="49140-134">**推奨モジュール** – 推奨モジュールは製品配置モジュールを使用して表示されます。</span><span class="sxs-lookup"><span data-stu-id="49140-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="49140-135">このモジュールは、任意のページで表示できるアルゴリズムおよび編集リストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="49140-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49140-136">追加リソース</span><span class="sxs-lookup"><span data-stu-id="49140-136">Additional resources</span></span>

[<span data-ttu-id="49140-137">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="49140-138">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="49140-139">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="49140-140">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="49140-141">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="49140-142">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="49140-143">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="49140-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]