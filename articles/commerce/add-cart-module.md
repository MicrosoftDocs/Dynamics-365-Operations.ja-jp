---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025439"
---
# <a name="cart-module"></a><span data-ttu-id="ee5de-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ee5de-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ee5de-105">概要</span><span class="sxs-lookup"><span data-stu-id="ee5de-105">Overview</span></span>

<span data-ttu-id="ee5de-106">カート モジュールは、顧客がチェックアウトに進む前にカートに追加された品目を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="ee5de-107">たとえば、カートおよび注文集計に追加されたすべての品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="ee5de-108">また、顧客はプロモーション コードを適用または削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ee5de-109">カート モジュールでは、サインインしたチェックアウトとゲスト チェックアウトがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ee5de-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="ee5de-110">また、**ショッピングに戻る**リンクもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ee5de-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="ee5de-111">**サイト設定 \> 拡張子 \> 工順**で、このリンクの工順をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="ee5de-112">カート モジュールは、カート ID に基づくデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="ee5de-113">カート ID は、サイト全体で使用できるブラウザー Cookie です。</span><span class="sxs-lookup"><span data-stu-id="ee5de-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="ee5de-114">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="ee5de-114">Cart module properties and slots</span></span>

<span data-ttu-id="ee5de-115">カート モジュールには、**ヘッダー** プロパティがあり、**ショッピング バッグ**や**カート内の品目**などの値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="ee5de-116">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="ee5de-117">**テキスト ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ee5de-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="ee5de-118">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="ee5de-119">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="ee5de-120">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="ee5de-121">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="ee5de-122">ストア セレクター モジュールは、Bing Maps 位置情報アプリケーション プログラミング インターフェイス (API) と統合され、場所を緯度と経度に変換します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="ee5de-123">Bing Maps API キーが必要なので、Dynamics 365 Retail の小売共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee5de-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="ee5de-124">このモジュールでは、**検索半径**および**使用条件のリンク**の 2 つのプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ee5de-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="ee5de-125">**検索半径**プロパティでは、店舗の検索半径をマイル単位で定義します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="ee5de-126">値が指定されていない場合は、既定の検索半径 (50マイル) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="ee5de-127">Bing Maps または外部サービスを使用する場合、**使用条件リンク** プロパティを使用して、使用条件へのリンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="ee5de-128">Bing Maps サービスには使用条件のリンクが必要です。</span><span class="sxs-lookup"><span data-stu-id="ee5de-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="ee5de-129">カート モジュール設定</span><span class="sxs-lookup"><span data-stu-id="ee5de-129">Cart module settings</span></span>

<span data-ttu-id="ee5de-130">カート モジュールには、**サイト設定 \> 拡張子**でコンフィギュレーションできる次の設定があります。</span><span class="sxs-lookup"><span data-stu-id="ee5de-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="ee5de-131">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="ee5de-132">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee5de-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="ee5de-133">**在庫確認** – 値が **True** に設定されている場合、購入ボックス モジュールが品目が在庫にあることを確認した後にのみ、品目がカートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="ee5de-134">この在庫確認は、品目が出荷されるシナリオと、品目を店舗で受け取るシナリオの両方に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="ee5de-135">値が **False** に設定されている場合、品目がカートに追加されて注文が行われる前に、在庫確認は実行されません。</span><span class="sxs-lookup"><span data-stu-id="ee5de-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="ee5de-136">**在庫バッファー** – このプロパティは、在庫のバッファー数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="ee5de-137">在庫はリアルタイムで管理されるため、多くの顧客が注文する場合、正確な在庫数を管理するのが困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee5de-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="ee5de-138">在庫確認が実行されると、在庫がバッファー額を下回る場合、その製品は在庫切れとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="ee5de-139">したがって、複数のチャネルで販売が迅速に行われ、在庫数が完全に同期されていない場合、在庫切れの品目が販売されるリスクは低くなります。</span><span class="sxs-lookup"><span data-stu-id="ee5de-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="ee5de-140">**ショッピングに戻る** – このプロパティは、**ショッピングに戻る**リンクの工順を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="ee5de-141">この工順は、サイトレベルでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-141">This route can be configured at the site level.</span></span> <span data-ttu-id="ee5de-142">このコンフィギュレーションにより、小売業者は、顧客をサイトのホームページまたはサイトの他のページに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="ee5de-143">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="ee5de-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="ee5de-144">カート モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="ee5de-145">ブラウザー Cookie からのカート ID は、Commerce Scale Unit API からすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee5de-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="ee5de-146">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="ee5de-146">Add a cart module to a page</span></span>

<span data-ttu-id="ee5de-147">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ee5de-148">**カート フラグメント**という名前のフラグメントを作成し、それにカート モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="ee5de-149">ヘッダーをカート モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="ee5de-150">カート モジュールにストア セレクター モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="ee5de-151">フラグメントを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="ee5de-152">**カート テンプレート**という名前のテンプレートを作成し、作成したカート フラグメントをそこに追加します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="ee5de-153">テンプレートを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="ee5de-154">新しいテンプレートを使用するページを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="ee5de-155">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="ee5de-155">Save and preview the page.</span></span>
1. <span data-ttu-id="ee5de-156">ページの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="ee5de-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee5de-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ee5de-157">Additional resources</span></span>

[<span data-ttu-id="ee5de-158">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="ee5de-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ee5de-159">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ee5de-160">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ee5de-161">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ee5de-162">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ee5de-163">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ee5de-164">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="ee5de-164">Footer module</span></span>](author-footer-module.md)
