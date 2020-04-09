---
title: 購入ボックス モジュール
description: このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154066"
---
# <a name="buy-box-module"></a><span data-ttu-id="64914-103">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-103">Buy box module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="64914-104">このトピックでは、購入ボックス モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64914-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="64914-105">概要</span><span class="sxs-lookup"><span data-stu-id="64914-105">Overview</span></span>

<span data-ttu-id="64914-106">*購入ボックス*という用語は、通常 "折りたたみの上" である製品の詳細ページの領域を指し、製品購買に必要な最も重要な情報すべてをホストします。</span><span class="sxs-lookup"><span data-stu-id="64914-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="64914-107">("折りたたみの上" である領域はページが最初に読み込まれたときに表示されるため、ユーザーは下にスクロールして表示する必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="64914-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="64914-108">購入ボックス モジュールは、製品の詳細ページの購入ボックス領域に表示されるすべてのモジュールをホストするために使用する特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="64914-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="64914-109">製品の詳細ページの URL には、製品 ID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="64914-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="64914-110">購買ボックス モジュールの表示に必要なすべての情報は、この製品 ID から派生します。</span><span class="sxs-lookup"><span data-stu-id="64914-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="64914-111">製品 ID が指定されていない場合、購入ボックス モジュールはページに正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="64914-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="64914-112">したがって、購入ボックス モジュールは、製品コンテキストがあるページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="64914-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="64914-113">製品コンテキストがないページ (ホーム ページやマーケティング ページなど) で使用するには、追加のカスタマイズを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="64914-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="64914-114">購入ボックス モジュール プロパティおよびスロット</span><span class="sxs-lookup"><span data-stu-id="64914-114">Buy box module properties and slots</span></span> 

<span data-ttu-id="64914-115">製品の詳細ページでは、購入ボックスは 2 つの領域に分割されます: 左側にメディア領域、右側にコンテンツ領域。</span><span class="sxs-lookup"><span data-stu-id="64914-115">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="64914-116">既定では、メディア領域列の幅とコンテンツ領域列の幅の比率は 2:1 になります。</span><span class="sxs-lookup"><span data-stu-id="64914-116">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="64914-117">モバイル デバイスでは 2 つの領域が積み重ねられ、一方の領域がもう一方の領域の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="64914-117">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="64914-118">テーマを使用して、列の幅やスタック ランクをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="64914-118">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="64914-119">購入ボックス モジュールは、製品のタイトル、説明、価格、および評価をレンダリングします。</span><span class="sxs-lookup"><span data-stu-id="64914-119">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="64914-120">また、顧客は、サイズ、スタイル、色などの製品属性が異なる製品バリアントを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="64914-120">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="64914-121">製品バリアントが選択されると、購入ボックスの他のプロパティ (製品の説明や画像など) が更新されて、バリアント情報が反映されます。</span><span class="sxs-lookup"><span data-stu-id="64914-121">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="64914-122">数量セレクターは、顧客が購入する品目の数量を指定できるようにするために用意されています。</span><span class="sxs-lookup"><span data-stu-id="64914-122">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="64914-123">購入できる最大数量は、サイト設定で定義できます。</span><span class="sxs-lookup"><span data-stu-id="64914-123">The maximum quantity that can be purchased can be defined in the site settings.</span></span>
 
<span data-ttu-id="64914-124">購入 ボックスから、カートへの製品の追加、欲しい物リストへの製品の追加、集配場所の選択などのアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="64914-124">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="64914-125">これらのアクションは、製品または製品バリアントに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="64914-125">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="64914-126">製品を欲しい物リストに追加するには、顧客がサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="64914-126">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="64914-127">テーマを使用すると、購入ボックスの製品プロパティとアクション コントロールの順序を削除または変更できます。</span><span class="sxs-lookup"><span data-stu-id="64914-127">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="64914-128">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="64914-128">Module properties</span></span>

- <span data-ttu-id="64914-129">**ヘッダー タグ** ー このプロパティは、製品タイトルのヘッダー タグを定義します。</span><span class="sxs-lookup"><span data-stu-id="64914-129">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="64914-130">購入ボックスがページの一番上にある場合は、アクセシビリティ標準を満たすため、このプロパティを **h1** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64914-130">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="64914-131">購入用ボックス モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="64914-131">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="64914-132">**メディア ギャラリー** – このモジュールは、製品の詳細ページに製品の画像を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="64914-132">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="64914-133">一対多の画像をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="64914-133">It can support one to many images.</span></span> <span data-ttu-id="64914-134">サムネイル画像もサポートします。</span><span class="sxs-lookup"><span data-stu-id="64914-134">It also supports thumbnail images.</span></span> <span data-ttu-id="64914-135">サムネイル画像は、水平方向 (画像の下の行) または垂直方向 (画像の横の列) のいずれかに配置できます。</span><span class="sxs-lookup"><span data-stu-id="64914-135">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="64914-136">メディア ギャラリー モジュールは、購入ボックス モジュールの**メディア** スロットに追加できます。</span><span class="sxs-lookup"><span data-stu-id="64914-136">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="64914-137">現在、画像のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="64914-137">It currently supports only images.</span></span> 
- <span data-ttu-id="64914-138">**ストア セレクタ―** – このモジュールでは、品目の受け取り可能な近隣店舗の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="64914-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="64914-139">これにより、ユーザーは場所を入力して、近隣にある店舗を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="64914-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="64914-140">このモジュールの詳細については、[ストア セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64914-140">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="64914-141">購入ボックス モジュール設定</span><span class="sxs-lookup"><span data-stu-id="64914-141">Buy box module settings</span></span>

<span data-ttu-id="64914-142">購入ボックス モジュールには、**サイト設定 \> 拡張子**でコンフィギュレーションできる 3 つの設定があります:</span><span class="sxs-lookup"><span data-stu-id="64914-142">Buy box modules have three settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="64914-143">**最大数量** – このプロパティは、カートに追加できる各品目の最大数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="64914-143">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="64914-144">たとえば、小売業者が、単一のトランザクションで販売できるのは各製品 10 個のみと決定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="64914-144">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="64914-145">**在庫確認** – 値が **True** に設定されている場合、購入ボックス モジュールが品目が在庫にあることを確認した後にのみ、品目がカートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="64914-145">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="64914-146">この在庫確認は、品目が出荷されるシナリオと、品目を店舗で受け取るシナリオの両方に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="64914-146">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="64914-147">値が **False** に設定されている場合、品目がカートに追加されて注文が行われる前に、在庫確認は実行されません。</span><span class="sxs-lookup"><span data-stu-id="64914-147">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="64914-148">**在庫バッファー** – このプロパティは、在庫のバッファー数を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="64914-148">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="64914-149">在庫はリアルタイムで管理されるため、多くの顧客が注文する場合、正確な在庫数を管理するのが困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="64914-149">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="64914-150">在庫確認が実行されると、在庫がバッファー額を下回る場合、その製品は在庫切れとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="64914-150">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="64914-151">したがって、複数のチャネルで販売が迅速に行われ、在庫数が完全に同期されていない場合、在庫切れの品目が販売されるリスクは低くなります。</span><span class="sxs-lookup"><span data-stu-id="64914-151">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="64914-152">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="64914-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="64914-153">購入ボックス モジュールでは、Commerce Scale Unit API を使用して製品情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="64914-153">The buy box module retrieves product information using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="64914-154">製品の詳細ページの製品 ID は、すべての情報を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="64914-154">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="64914-155">購入ボックス モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="64914-155">Add a buy box module to a page</span></span>

<span data-ttu-id="64914-156">新しいページに購入ボックス モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64914-156">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="64914-157">**購入ボックス フラグメント**という名前のフラグメントを作成し、それに購入ボックス モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-157">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="64914-158">購入ボックス モジュールの**メディア** スロットで、メディア ギャラリー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-158">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="64914-159">購入ボックス モジュールの**ストア セレクタ―** スロットで、ストア セレクター モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-159">In the **Store selector** slot of the buy box module, add a store selector module.</span></span>
1. <span data-ttu-id="64914-160">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="64914-160">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="64914-161">製品の詳細ページのテンプレートを作成し、**PDP テンプレート**という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="64914-161">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="64914-162">既定のページを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-162">Add a default page.</span></span>
1. <span data-ttu-id="64914-163">既定ページの**メイン** スロットで、購入ボックス フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-163">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="64914-164">テンプレートを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="64914-164">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="64914-165">作成したテンプレートを使用して、**PDP ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="64914-165">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="64914-166">新しいページの**メイン** スロットで、購入ボックス フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-166">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="64914-167">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="64914-167">Save and preview the page.</span></span> <span data-ttu-id="64914-168">**?productid=&lt;product id&gt;** クエリ文字列パラメーターをプレビュー ページの URL に追加します。</span><span class="sxs-lookup"><span data-stu-id="64914-168">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="64914-169">このようにして、製品コンテキストを使用してプレビュー ページの読み込みと表示を行います。</span><span class="sxs-lookup"><span data-stu-id="64914-169">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="64914-170">ページを保存し、編集を終了してから、公開します。</span><span class="sxs-lookup"><span data-stu-id="64914-170">Save the page, finish editing it, and publish it.</span></span> <span data-ttu-id="64914-171">製品の詳細ページに、購入ボックスが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="64914-171">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64914-172">追加リソース</span><span class="sxs-lookup"><span data-stu-id="64914-172">Additional resources</span></span>

[<span data-ttu-id="64914-173">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="64914-173">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="64914-174">ストア セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-174">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="64914-175">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="64914-176">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-176">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="64914-177">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="64914-178">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="64914-179">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="64914-180">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="64914-180">Footer module</span></span>](author-footer-module.md)
