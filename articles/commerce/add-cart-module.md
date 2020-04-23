---
title: カート モジュール
description: このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261424"
---
# <a name="cart-module"></a><span data-ttu-id="fdcc6-103">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fdcc6-104">このトピックでは、カート モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fdcc6-105">概要</span><span class="sxs-lookup"><span data-stu-id="fdcc6-105">Overview</span></span>

<span data-ttu-id="fdcc6-106">カート モジュールでは、顧客がチェックアウトに進む前にカートに追加された品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="fdcc6-107">モジュールには注文集計も表示され、顧客はプロモーション コードを適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="fdcc6-108">カート モジュールでは、サインインしたチェックアウトとゲスト チェックアウトがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="fdcc6-109">また、**ショッピングに戻る**リンクもサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="fdcc6-110">**サイト設定 \> 拡張子 \> 工順**で、このリンクの工順をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="fdcc6-111">カート モジュールは、サイト全体で利用可能なブラウザー Cookie であるカート ID に基づいてデータをレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="fdcc6-112">カート モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="fdcc6-112">Cart module properties and slots</span></span>

<span data-ttu-id="fdcc6-113">カート モジュールには、**ヘッダー** プロパティがあり、**ショッピング バッグ**や**カート内の品目**などの値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="fdcc6-114">カート モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="fdcc6-115">**テキスト ブロック** – このモジュールは、カート モジュールのカスタム メッセージングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="fdcc6-116">メッセージは、コンテンツ管理システム (CMS) よって発生します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="fdcc6-117">"注文に関する問題については、1-800-Fabrikam にお問い合わせください" などのメッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="fdcc6-118">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="fdcc6-119">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="fdcc6-120">このモジュールの詳細については、[ストア セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="fdcc6-121">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="fdcc6-121">Module properties</span></span>

<span data-ttu-id="fdcc6-122">カート モジュールには、**サイト設定 \> 拡張子**でコンフィギュレーションできる次の設定があります。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="fdcc6-123">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="fdcc6-124">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="fdcc6-125">**在庫確認** – 値が **True** に設定されている場合、購入ボックス モジュールが品目が在庫にあることを確認した後にのみ、品目がカートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="fdcc6-126">この在庫チェックは、品目が出荷されるシナリオと、品目を店舗で受け取るシナリオで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="fdcc6-127">値が **False** に設定されている場合、品目がカートに追加されて注文が行われる前に、在庫確認は実行されません。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="fdcc6-128">バック オフィスの在庫の設定をコンフィギュレーションする方法については、[小売チャンネルの引当可能在庫数量の計算](calculated-inventory-retail-channels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="fdcc6-129">**在庫バッファー** – このプロパティは、在庫のバッファー数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="fdcc6-130">在庫はリアルタイムで管理されるため、多くの顧客が注文する場合、正確な在庫数を管理するのが困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="fdcc6-131">在庫確認が実行されると、在庫がバッファー額を下回る場合、その製品は在庫切れとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="fdcc6-132">したがって、複数のチャネルで販売が迅速に行われ、在庫数が完全に同期されていない場合、在庫切れの品目が販売されるリスクは低くなります。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="fdcc6-133">**ショッピングに戻る** – このプロパティは、**ショッピングに戻る**リンクの工順を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="fdcc6-134">このルートはサイト レベルで設定でき、小売業者は、顧客をサイトのホーム ページや他のページに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="fdcc6-135">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="fdcc6-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="fdcc6-136">カート モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="fdcc6-137">ブラウザー Cookie からのカート ID は、Commerce Scale Unit API からすべての製品情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="fdcc6-138">カート モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="fdcc6-138">Add a cart module to a page</span></span>

<span data-ttu-id="fdcc6-139">新しいページにカート モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fdcc6-140">**カート フラグメント** という名前のフラグメントを作成し、新しいフラグメントにカート モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="fdcc6-141">ヘッダーをカート モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="fdcc6-142">カート モジュールにストア セレクター モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="fdcc6-143">フラグメントを保存し、編集を終了して、フラグメントを公開します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="fdcc6-144">**カート テンプレート** という名前のテンプレートを作成し、作成したカート フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="fdcc6-145">テンプレートを保存し、編集を終了して、テンプレートを公開します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="fdcc6-146">新しいテンプレートを使用するページを作成します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="fdcc6-147">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-147">Save and preview the page.</span></span>
1. <span data-ttu-id="fdcc6-148">ページの編集を終了してから、ページを公開します。</span><span class="sxs-lookup"><span data-stu-id="fdcc6-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdcc6-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fdcc6-149">Additional resources</span></span>

[<span data-ttu-id="fdcc6-150">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="fdcc6-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fdcc6-151">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fdcc6-152">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="fdcc6-153">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fdcc6-154">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fdcc6-155">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fdcc6-156">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fdcc6-157">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fdcc6-158">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="fdcc6-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="fdcc6-159">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="fdcc6-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
