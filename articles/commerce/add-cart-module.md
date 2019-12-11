---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696764"
---
# <a name="cart-module"></a><span data-ttu-id="61f4d-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="61f4d-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="61f4d-105">概要</span><span class="sxs-lookup"><span data-stu-id="61f4d-105">Overview</span></span>

<span data-ttu-id="61f4d-106">カート モジュールは、カートにある品目を紹介するのに必要なすべてのモジュールをホストするために使用されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="61f4d-106">A cart module is container that is used to host all the modules that are required to showcase items that are in the cart.</span></span> <span data-ttu-id="61f4d-107">たとえば、カート、注文集計、およびプロモーション コードに追加されたすべての品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-107">For example, it includes all the items that have been added to the cart, the order summary, and promotional codes.</span></span>

<span data-ttu-id="61f4d-108">カート モジュールは、カート ID に基づくデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-108">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="61f4d-109">カート ID は、サイト全体で使用できるブラウザー Cookie です。</span><span class="sxs-lookup"><span data-stu-id="61f4d-109">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="61f4d-110">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="61f4d-110">Cart module properties and slots</span></span>

<span data-ttu-id="61f4d-111">コンテナーとして、カート モジュールは、ヘッダーおよび幅などのいくつかの基本的なプロパティを制御します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-111">As a container, a cart module controls some basic properties, such as the heading and the width.</span></span> <span data-ttu-id="61f4d-112">ヘッダーは通常、**ショッピング バッグ**、**カート**、または**カート内の品目**などのテキストです。</span><span class="sxs-lookup"><span data-stu-id="61f4d-112">The heading is typically text such as **Shopping bag**, **Your cart**, or **Items in your cart**.</span></span> <span data-ttu-id="61f4d-113">幅の設定により、コンテナー内のモジュールがそのコンテナー内に収まる必要があるかどうか、または画面を埋めれるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-113">The width setting determines whether the modules inside the container must fit within that container, or whether they can fill the screen.</span></span>

<span data-ttu-id="61f4d-114">カート ページは複数の領域に分割されています: カート明細行品目、"注文集計とチェックアウト、および "店舗で検索" 機能。</span><span class="sxs-lookup"><span data-stu-id="61f4d-114">The cart page is divided into multiple regions: cart line items, order summary and checkout, and "find in store" functionality.</span></span> <span data-ttu-id="61f4d-115">各領域はカート モジュールのスロットにマップされ、各スロットは事前定義された一連のモジュールを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-115">Each region is mapped to a slot in the cart module, and every slot accepts a predefined set of modules.</span></span>

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="61f4d-116">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="61f4d-117">**カート明細行品目** – このモジュールでは、カートに追加された各品目の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-117">**Cart line items** – This module shows a summary of every item that has been added to the cart.</span></span> <span data-ttu-id="61f4d-118">情報には、製品タイトル、選択した分析コード、価格、数量、および割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-118">The information includes the product title, selected dimensions, price, quantity, and discounts.</span></span> <span data-ttu-id="61f4d-119">このモジュールは、"カートから削除" や "欲しい物リストに追加" などのアクションもサポートします。</span><span class="sxs-lookup"><span data-stu-id="61f4d-119">This module also supports actions such as "remove from cart" and "add to wish list."</span></span> <span data-ttu-id="61f4d-120">明細行品目ごとに、品目を出荷する、または店舗から受け取るオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-120">For each line item, there is an option to ship the item or pick it up from the store.</span></span> <span data-ttu-id="61f4d-121">このオプションは、"店舗で受取り" モジュールで個別にコンフィギュレーションされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-121">This option must be configured separately in the pick up in store module.</span></span>
- <span data-ttu-id="61f4d-122">**注文集計** – このモジュールは、注文集計を表示します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-122">**Order summary** – This module shows an order summary.</span></span> <span data-ttu-id="61f4d-123">情報には、小計、出荷、税、および割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-123">The information includes the subtotal, shipping, taxes, and savings.</span></span> <span data-ttu-id="61f4d-124">このモジュールに対して、ヘッダーをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-124">A heading can be configured for this module.</span></span>
- <span data-ttu-id="61f4d-125">**プロモーション コード** – このモジュールにより、顧客はプロモーション コードの引換ができます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-125">**Promo code** – This module lets the customer redeem promotional codes.</span></span> <span data-ttu-id="61f4d-126">プロモーション コードを適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-126">A promotional code can be applied or removed.</span></span>
- <span data-ttu-id="61f4d-127">**チェックアウト** – このモジュールによりチェックアウト アクションを開始し、ユーザーをチェックアウト ページにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="61f4d-127">**Checkout** – This module initiates the checkout action and redirects the user to the checkout page.</span></span> <span data-ttu-id="61f4d-128">このモジュールに対して 3 つのリンクをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-128">Three links must be configured for this module:</span></span>

    - <span data-ttu-id="61f4d-129">**チェックアウト** – このリンクでは、まだサインインしていない顧客にサインインさせます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-129">**Checkout** – This link forces customers to sign in if they aren't already signed in.</span></span>
    - <span data-ttu-id="61f4d-130">**ゲスト チェックアウト** – このリンクを使用すると、匿名顧客が注文できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-130">**Guest checkout** – This link lets anonymous customers place orders.</span></span> <span data-ttu-id="61f4d-131">顧客がサインインしていない場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-131">It's shown only when customers aren't signed in.</span></span>
    - <span data-ttu-id="61f4d-132">**ショッピングに戻る** – このリンクを使用すると、顧客はホーム ページまたはその他のページに移動して買い物を継続できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-132">**Back to shopping** – This link lets customers go to the home page or any other page, so that they can continue to shop.</span></span>

- <span data-ttu-id="61f4d-133">**コンテンツ リッチ ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="61f4d-133">**Content rich block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="61f4d-134">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-134">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="61f4d-135">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-135">Any message can be added, such as "For issues with the order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="61f4d-136">**店舗で受け取り** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-136">**Pick up in store** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="61f4d-137">既定では、このモジュールは顧客の場所から半径 50 マイル以内の店舗を表示します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-137">By default, this module shows stores that are within a 50-mile radius of the customer's location.</span></span> <span data-ttu-id="61f4d-138">ただし、モジュールで検索する半径をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-138">However, the search radius can be customized in the module.</span></span> <span data-ttu-id="61f4d-139">各店舗で、在庫確認機能がオンになっている場合は、在庫確認が行われ、適切な在庫または在庫切れのメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-139">For each store, an inventory check is done, if the inventory check functionality is turned on, and an appropriate in-stock or out-of-stock message is shown.</span></span>
- <span data-ttu-id="61f4d-140">**Bing Maps による店舗検索** – このモジュールは、店舗で受け取りモジュール内で使用されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-140">**Store search by Bing Maps** – This module can be used inside the pick up in store module.</span></span> <span data-ttu-id="61f4d-141">顧客は、場所を入力することによって店舗を検索できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-141">It lets customers search for stores by entering a location.</span></span> <span data-ttu-id="61f4d-142">Bing Maps 位置情報アプリケーション プログラミング インターフェイス (API) は顧客が入力した場所を緯度と経度に変換するために使用します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-142">The Bing Maps geocoding application programming interface (API) is used to convert the location that the customer entered to a latitude and a longitude.</span></span> <span data-ttu-id="61f4d-143">このモジュールを使用しない場合、顧客の現在の場所に近い店舗だけが表示され、顧客は別の場所を検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="61f4d-143">If this module isn't used, only stores that are near the customer's current location are shown, and the customer can't search for a different location.</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="61f4d-144">カート モジュール設定</span><span class="sxs-lookup"><span data-stu-id="61f4d-144">Cart module settings</span></span>

<span data-ttu-id="61f4d-145">カート モジュールには、コンフィギュレーション可能な 3 つの設定があります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-145">Cart modules have three settings that can be configured:</span></span>

- <span data-ttu-id="61f4d-146">**最大数量** – カートに追加できる各品目の最大数量。</span><span class="sxs-lookup"><span data-stu-id="61f4d-146">**Maximum quantity** – The maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="61f4d-147">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="61f4d-148">**在庫確認** – 値が **True** に設定されている場合、購入ボックス モジュールが品目が在庫にあることを確認した後にのみ、品目がカートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-148">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="61f4d-149">この在庫確認は、品目が出荷されるシナリオと、品目を店舗で受け取るシナリオの両方に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-149">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="61f4d-150">値が **False** に設定されている場合、品目がカートに追加されて注文が行われる前に、在庫確認は実行されません。</span><span class="sxs-lookup"><span data-stu-id="61f4d-150">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="61f4d-151">**在庫バッファー** – 在庫はリアルタイムで管理されるため、多くの顧客が注文する場合、正確な在庫数を管理するのが困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-151">**Inventory buffer** – Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="61f4d-152">したがって、バッファーは在庫に対して定義できます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-152">Therefore, a buffer can be defined for inventory.</span></span> <span data-ttu-id="61f4d-153">在庫確認が実行されると、在庫がバッファー額を下回る場合、その製品は在庫切れとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-153">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="61f4d-154">したがって、在庫数が完全に同期されないよう、販売が複数のチャンネルを通じて迅速に行われる場合、在庫切れの品目が販売されるリスクは少なくなります。</span><span class="sxs-lookup"><span data-stu-id="61f4d-154">Therefore, when sales occur quickly through several channels, so that the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="61f4d-155">小売サーバー インタラクション</span><span class="sxs-lookup"><span data-stu-id="61f4d-155">Retail Server interaction</span></span>

<span data-ttu-id="61f4d-156">カート モジュールでは、Retail Server API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-156">The cart module retrieves product information by using Retail Server APIs.</span></span> <span data-ttu-id="61f4d-157">ブラウザー Cookie からのカート ID は、小売サーバーからすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="61f4d-157">The cart ID from the browser cookie is used to retrieve all the product information from Retail Server.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="61f4d-158">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="61f4d-158">Add a cart module to a page</span></span>

<span data-ttu-id="61f4d-159">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-159">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="61f4d-160">**カート フラグメント**という名前のフラグメントを作成し、それにカート モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-160">Create a fragment that is named **cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="61f4d-161">カート モジュールの**カート明細行品目**で、カート明細行品目モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-161">In the **Cart line items** slot of the cart module, add a cart line items module.</span></span>
1. <span data-ttu-id="61f4d-162">**注文集計**スロットで、注文集計モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-162">In the **Order summary** slot, add an order summary module.</span></span>
1. <span data-ttu-id="61f4d-163">**プロモーション コード** スロットで、プロモーション コード モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-163">In the **Promo code** slot, add a promo code module.</span></span>
1. <span data-ttu-id="61f4d-164">**チェックアウト** スロットで、チェックアウト モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-164">In the **Checkout** slot, add a checkout module.</span></span>
1. <span data-ttu-id="61f4d-165">**店舗で検索**スロットで、店舗で受け取りモジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-165">In the **Find in Store** slot, add a pick up in store module.</span></span>
1. <span data-ttu-id="61f4d-166">店舗で受け取りモジュールで、**店舗検索**スロットを選択し、Bing Maps による店舗検索モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-166">In the pick up in store module, select the **Store search** slot, and add a store search by Bing Maps module.</span></span>
1. <span data-ttu-id="61f4d-167">フラグメントをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-167">Check in the fragment, and publish it.</span></span>
1. <span data-ttu-id="61f4d-168">**カート テンプレート**という名前のテンプレートを作成し、作成したカート フラグメントをそこに追加します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-168">Create a template that is named **cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="61f4d-169">テンプレートを保存し、チェック イン後に発行します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-169">Save the template, check it in, and publish it.</span></span>
1. <span data-ttu-id="61f4d-170">新しいテンプレートを使用するページを作成します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-170">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="61f4d-171">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="61f4d-171">Save and preview the page.</span></span>
1. <span data-ttu-id="61f4d-172">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="61f4d-172">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61f4d-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="61f4d-173">Additional resources</span></span>

[<span data-ttu-id="61f4d-174">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="61f4d-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="61f4d-175">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="61f4d-176">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-176">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="61f4d-177">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="61f4d-178">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="61f4d-179">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="61f4d-180">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="61f4d-180">Footer module</span></span>](author-footer-module.md)
