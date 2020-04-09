---
title: 店舗セレクター モジュール
description: このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157343"
---
# <a name="store-selector-module"></a><span data-ttu-id="6b8f3-103">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="6b8f3-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b8f3-104">このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6b8f3-105">概要</span><span class="sxs-lookup"><span data-stu-id="6b8f3-105">Overview</span></span>

<span data-ttu-id="6b8f3-106">店舗セレクター モジュールは、"オンラインで購入し、店舗でピックアップ" (BOPIS) 顧客シナリオに使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="6b8f3-107">製品のピックアップが可能な店舗の一覧と、各店舗の営業時間と製品在庫が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="6b8f3-108">店舗セレクター モジュールでは、店舗を検索するために、製品のコンテキストと検索場所が必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="6b8f3-109">検索場所が存在しない場合は、顧客が同意をした顧客のブラウザーの場所が規定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="6b8f3-110">このモジュールには入力ボックスがあり、顧客が場所 (郵便番号、または市町村と都道府県) を入力して、近くにある店舗を検索できます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="6b8f3-111">ストア セレクター モジュールは、Bing Maps 位置情報アプリケーション プログラミング インターフェイス (API) と統合され、場所を緯度と経度に変換します。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="6b8f3-112">Bing Maps API キーは必須で、Dynamics 365 Commerce の Commerce の共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b8f3-113">店舗セレクター モジュールは、製品の詳細ページ (PDP) の購入ボックス モジュールに追加して、製品がピックアップできる店舗を表示できます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="6b8f3-114">また、カート モジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-114">It can also be added to a cart module.</span></span> <span data-ttu-id="6b8f3-115">カート モジュールに追加されると、店舗セレクター モジュールに各カート品目に対するピックアップ オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="6b8f3-116">さらに、カスタムコードを使用して、拡張機能とカスタマイズによって、このモジュールを他のページまたはモジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="6b8f3-117">BOPIS シナリオが機能するためには、"顧客ピックアップ" デリバリー モードを使用して製品をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="6b8f3-118">それ以外の場合、このモジュールは個々のページでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="6b8f3-119">デリバリー モードをコンフィギュレーションする方法の詳細については、[デリバリーの設定モード](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="6b8f3-120">次の図は、PDP で使用される店舗セレクター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![店舗セレクター モジュールの例](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="6b8f3-122">E-コマースの店舗セレクター モジュールの使用方法</span><span class="sxs-lookup"><span data-stu-id="6b8f3-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="6b8f3-123">店舗セレクター モジュールを製品の詳細ページ (PDP) で使用し、製品がピックアップできる近隣の店舗を探すことができます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="6b8f3-124">店舗セレクター モジュールをカート ページで使用し、ピックアップが使用できるカートの製品がある店舗を探すことができます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="6b8f3-125">店舗セレクター モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="6b8f3-125">Store selector module properties</span></span>

| <span data-ttu-id="6b8f3-126">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="6b8f3-126">Property name</span></span>             | <span data-ttu-id="6b8f3-127">先頭値</span><span class="sxs-lookup"><span data-stu-id="6b8f3-127">Value</span></span>                 | <span data-ttu-id="6b8f3-128">説明</span><span class="sxs-lookup"><span data-stu-id="6b8f3-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6b8f3-129">検索半径</span><span class="sxs-lookup"><span data-stu-id="6b8f3-129">Search radius</span></span> | <span data-ttu-id="6b8f3-130">番号</span><span class="sxs-lookup"><span data-stu-id="6b8f3-130">Number</span></span> | <span data-ttu-id="6b8f3-131">店舗の検索半径をマイル単位で定義します。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="6b8f3-132">値が指定されていない場合は、既定の検索半径 (50マイル) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="6b8f3-133">サービス条件</span><span class="sxs-lookup"><span data-stu-id="6b8f3-133">Terms of Service</span></span> | <span data-ttu-id="6b8f3-134">URL</span><span class="sxs-lookup"><span data-stu-id="6b8f3-134">URL</span></span>    |  <span data-ttu-id="6b8f3-135">Bing Maps サービスに必要なサービス URL の条件。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="6b8f3-136">店舗セレクター モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="6b8f3-136">Add a store selector module to a page</span></span>

<span data-ttu-id="6b8f3-137">店舗セレクター モジュールには製品のコンテキストが必要であるため、購入ボックスとカート モジュール内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="6b8f3-138">ストア セレクター モジュールは、これらのモジュールの外では機能しません。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="6b8f3-139">購入ボックス モジュールに店舗セレクター モジュールを追加する方法の詳細については、[購入ボックス モジュール](add-buy-box.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b8f3-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="6b8f3-140">カート モジュールに店舗セレクター モジュールを追加する方法の詳細については、[カート モジュール](add-cart-module.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="6b8f3-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b8f3-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6b8f3-141">Additional resources</span></span>

[<span data-ttu-id="6b8f3-142">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="6b8f3-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6b8f3-143">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="6b8f3-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6b8f3-144">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="6b8f3-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6b8f3-145">PDP のクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="6b8f3-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="6b8f3-146">カートとチェックアウトのクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="6b8f3-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="6b8f3-147">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="6b8f3-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
