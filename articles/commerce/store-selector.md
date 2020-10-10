---
title: 店舗セレクター モジュール
description: このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 4438e46d4653a0cd2060092695f08613cd696f4e
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818253"
---
# <a name="store-selector-module"></a><span data-ttu-id="1aae8-103">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="1aae8-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1aae8-104">このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1aae8-105">概要</span><span class="sxs-lookup"><span data-stu-id="1aae8-105">Overview</span></span>

<span data-ttu-id="1aae8-106">顧客は、店舗セレクター モジュールを使用して、オンライン購入後に選択した店舗の製品を集荷できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-106">Customers can use the store selector module to pick up a product in a selected store after an online purchase.</span></span> <span data-ttu-id="1aae8-107">Commerce バージョン 10.0.13 では、店舗セレクター モジュールにも、近くにある店舗を表示する **店舗の検索** ページを紹介する機能が追加されています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-107">In Commerce version 10.0.13, the store selector module also includes additional capabilities that can showcase a **Find a Store** page that shows nearby stores.</span></span>

<span data-ttu-id="1aae8-108">店舗セレクター モジュールを使用すると、場所 (市町村、都道府県、住所など) を入力して検索半径内の店舗を検索できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-108">The store selector module lets users enter a location (city, state, address, and so on) to search for stores within a search radius.</span></span> <span data-ttu-id="1aae8-109">モジュールが最初に開かれたとき、顧客のブラウザーの場所を使用して、店舗が検索されます (同意を得ている場合)。</span><span class="sxs-lookup"><span data-stu-id="1aae8-109">When the module is first opened, it uses the customer's browser location to find stores (if consent is provided).</span></span>

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="1aae8-110">E-コマースの店舗セレクター モジュールの使用方法</span><span class="sxs-lookup"><span data-stu-id="1aae8-110">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="1aae8-111">製品の詳細ページ (PDP) では、店舗セレクター モジュールを使用して受け取りのための店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-111">A store selector module can be used on a product details page (PDP) to select a store for pickup.</span></span>
- <span data-ttu-id="1aae8-112">買い物カゴ ページでは、店舗セレクター モジュールを使用して受け取りのための店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-112">A store selector module can be used on a cart page to select a store for pickup.</span></span>
- <span data-ttu-id="1aae8-113">店舗セレクター モジュールは、使用可能なすべての店舗を表示するスタンドアロン ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-113">A store selector module can be used on a standalone page that shows all available stores.</span></span>

## <a name="bing-maps-integration"></a><span data-ttu-id="1aae8-114">Bing Maps の統合</span><span class="sxs-lookup"><span data-stu-id="1aae8-114">Bing Maps integration</span></span>

<span data-ttu-id="1aae8-115">Bing の Geocoding および Autosuggest 機能を使用するために、ストア選択モジュールは [Bing Maps REST アプリケーション プログラミング インターフェイス (API)](https://docs.microsoft.com/bingmaps/rest-services/) と統合されています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-115">The store selector module is integrated with the [Bing Maps REST application programming interfaces (APIs)](https://docs.microsoft.com/bingmaps/rest-services/) to use Bing's Geocoding and Autosuggest features.</span></span> <span data-ttu-id="1aae8-116">Bing Maps API キーは必須で、Commerce 本社の共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aae8-116">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="1aae8-117">Geocoding API は、場所を緯度と経度の値に変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-117">The Geocoding API is used to convert a location to latitude and longitude values.</span></span> <span data-ttu-id="1aae8-118">Autosuggest API との統合は、ユーザーが検索フィールドに場所を入力したときに検索候補を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-118">The integration with the Autosuggest API is used to show search suggestions when users enter locations in the search field.</span></span>

<span data-ttu-id="1aae8-119">Autosuggest REST API の場合は、サイトのコンテンツ セキュリティ ポリシー (CSP) に対して、次の URL が許可されていることを確認する必要があります ("ホワイトリスト登録" と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="1aae8-119">For the Autosuggest REST API, you must ensure that the following URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="1aae8-120">この設定は、Commerce サイト ビルダーで、サイトのさまざまな CSP ディレクティブ (**img-src** など) に許可された URL を追加することによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-120">This setup is done in Commerce site builder, by adding allowed URLs to various CSP directives for the site (for example, **img-src**).</span></span> <span data-ttu-id="1aae8-121">詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aae8-121">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="1aae8-122">**connect-src** ディレクティブに **&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-122">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="1aae8-123">**img-src** ディレクティブに **&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-123">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="1aae8-124">**script-src** ディレクティブに、**&#42;.bing.com, &#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-124">To the **script-src** directive, **add &#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="1aae8-125">**script style-src** ディレクティブに、**&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-125">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>
 
## <a name="pickup-in-store-mode"></a><span data-ttu-id="1aae8-126">店舗で受け取りモード</span><span class="sxs-lookup"><span data-stu-id="1aae8-126">Pickup in store mode</span></span>

<span data-ttu-id="1aae8-127">店舗セレクター モジュールでは、製品を受け取ることができる店舗の一覧を表示する **店舗で受け取り** モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-127">The store selector module supports a **Pick up in store** mode that shows a list of stores where a product is available for pickup.</span></span> <span data-ttu-id="1aae8-128">また、この一覧には店舗の営業時間と店舗ごとの製品在庫も表示されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-128">It also shows store hours and product inventory for each store in the list.</span></span> <span data-ttu-id="1aae8-129">店舗セレクター モジュールでは、製品の利用可能性を表示するためと、選択した店舗で製品の配送モードが **受け取り** に設定されている場合はユーザーが製品を買い物カゴに追加できるように、製品のコンテキストが必要です 。</span><span class="sxs-lookup"><span data-stu-id="1aae8-129">The store selector module requires the context of a product to render product availability and to let the user add the product to the cart, if the product's delivery mode is set to **pickup** at the selected store.</span></span> <span data-ttu-id="1aae8-130">詳細については、[在庫設定](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aae8-130">For more information, see [Inventory settings](inventory-settings.md).</span></span> 

<span data-ttu-id="1aae8-131">店舗セレクター モジュールは、PDP の購入ボックス モジュールに追加して、製品を受け取ることができる店舗を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-131">The store selector module can be added to a buy box module on a PDP to show stores where a product is available for pickup.</span></span> <span data-ttu-id="1aae8-132">また、カート モジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-132">It can also be added to a cart module.</span></span> <span data-ttu-id="1aae8-133">この場合、店舗セレクター モジュールは、買い物カゴ内の各品目に対する受け取りオプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-133">In this case, the store selector module shows pickup options for each line item in the cart.</span></span> <span data-ttu-id="1aae8-134">店舗セレクター モジュールは、拡張機能とカスタマイズによって、他のページまたはモジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-134">The store selector module can also be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="1aae8-135">このシナリオが機能するためには、**受け取り** 配送モードが使用されるように製品をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aae8-135">For this scenario to work, products should be configured so that the **pickup** delivery mode is used.</span></span> <span data-ttu-id="1aae8-136">それ以外の場合、このモジュールは製品ページでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="1aae8-136">Otherwise, the module won't be shown on the product pages.</span></span> <span data-ttu-id="1aae8-137">配送モードをコンフィギュレーションする方法の詳細については、[荷渡方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aae8-137">For more information about how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="1aae8-138">次の図は、PDP で使用される店舗セレクター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-138">The following image shows an example of a store selector module used on a PDP.</span></span>

![PDP で使用される店舗セレクター モジュールの例](./media/BOPIS.PNG)

## <a name="find-stores-mode"></a><span data-ttu-id="1aae8-140">店舗検索モード</span><span class="sxs-lookup"><span data-stu-id="1aae8-140">Find stores mode</span></span>

<span data-ttu-id="1aae8-141">また、店舗セレクター モジュールは、**検索店舗**モードもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-141">The store selector module also supports a **Find stores** mode.</span></span> <span data-ttu-id="1aae8-142">このモードを使用すると、使用可能な店舗とその情報を表示する店舗の場所ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-142">This mode can be used to create a store locations page that shows available stores and their information.</span></span> <span data-ttu-id="1aae8-143">このモードでは、店舗セレクター モジュールは製品コンテキストなしで動作し、任意のサイト ページでスタンドアロン モジュールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-143">In this mode, the store selector module works without product context and can be used as a standalone module on any site page.</span></span> <span data-ttu-id="1aae8-144">さらに、モジュールに関連する設定が有効になっている場合、ユーザーは、その店舗を優先ストアとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-144">In addition, if the relevant settings are turned on for the module, users can select a store as their preferred store.</span></span> <span data-ttu-id="1aae8-145">店舗がユーザーの優先ストアとして選択されている場合、その店舗 ID はブラウザーの Cookie に保持されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-145">When a store is selected as a user's preferred store, the store ID is maintained in the browser cookie.</span></span> <span data-ttu-id="1aae8-146">したがって、ユーザーは Cookie の同意メッセージに同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aae8-146">Therefore, the user must accept a cookie consent message.</span></span>

<span data-ttu-id="1aae8-147">次の図は、店舗の場所ページのマップ モジュールと共に使用される店舗セレクター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1aae8-147">The following illustration shows an example of a store selector module that is used together with a map module on a store locations page.</span></span>

![保管場所ページの店舗セレクター モジュールとマップ モジュールの例](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a><span data-ttu-id="1aae8-149">マップのレンダリング</span><span class="sxs-lookup"><span data-stu-id="1aae8-149">Render a map</span></span>

<span data-ttu-id="1aae8-150">マップ モジュールを使用して、マップ上で店舗の場所を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-150">The store selector module can be used together with the map module to show the store locations on a map.</span></span> <span data-ttu-id="1aae8-151">マップ モジュールの詳細については、[マップ モジュール](map-module.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="1aae8-151">For more information about the map module, see [Map module](map-module.md)</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="1aae8-152">店舗セレクター モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="1aae8-152">Store selector module properties</span></span>

| <span data-ttu-id="1aae8-153">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="1aae8-153">Property name</span></span> | <span data-ttu-id="1aae8-154">先頭値</span><span class="sxs-lookup"><span data-stu-id="1aae8-154">Value</span></span> | <span data-ttu-id="1aae8-155">説明</span><span class="sxs-lookup"><span data-stu-id="1aae8-155">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="1aae8-156">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="1aae8-156">Heading</span></span> | <span data-ttu-id="1aae8-157">テキスト</span><span class="sxs-lookup"><span data-stu-id="1aae8-157">Text</span></span> | <span data-ttu-id="1aae8-158">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="1aae8-158">The heading for the module.</span></span> |
| <span data-ttu-id="1aae8-159">モード</span><span class="sxs-lookup"><span data-stu-id="1aae8-159">Mode</span></span> | <span data-ttu-id="1aae8-160">**店舗の検索** または **店舗で受け取り**</span><span class="sxs-lookup"><span data-stu-id="1aae8-160">**Find stores** or **Pick up in store**</span></span> | <span data-ttu-id="1aae8-161">**店舗の検索**モードでは、利用可能な店舗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-161">**Find stores** mode shows available stores.</span></span> <span data-ttu-id="1aae8-162">**店舗で受け取り**モードでは、ユーザーは受け取り用の店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-162">**Pick up in store** mode lets users select a store for pickup.</span></span> |
| <span data-ttu-id="1aae8-163">スタイル</span><span class="sxs-lookup"><span data-stu-id="1aae8-163">Style</span></span> | <span data-ttu-id="1aae8-164">**ダイアログ**または**インライン**</span><span class="sxs-lookup"><span data-stu-id="1aae8-164">**Dialog** or **Inline**</span></span> | <span data-ttu-id="1aae8-165">このモジュールは、インラインまたはダイアログ ボックスのいずれかでレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-165">The module can be rendered either inline or in a dialog box.</span></span> |
| <span data-ttu-id="1aae8-166">優先店舗に設定する</span><span class="sxs-lookup"><span data-stu-id="1aae8-166">Set as preferred store</span></span> | <span data-ttu-id="1aae8-167">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="1aae8-167">**True** or **False**</span></span> | <span data-ttu-id="1aae8-168">このプロパティが **True** に設定されている場合、ユーザーは優先ストアを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-168">When this property is set to **True**, users can set a preferred store.</span></span> <span data-ttu-id="1aae8-169">この機能を使用するには、ユーザーが Cookie の同意メッセージを受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aae8-169">This feature requires that users accept a cookie consent message.</span></span> |
| <span data-ttu-id="1aae8-170">全店舗を表示する</span><span class="sxs-lookup"><span data-stu-id="1aae8-170">Show all stores</span></span> | <span data-ttu-id="1aae8-171">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="1aae8-171">**True** or **False**</span></span> | <span data-ttu-id="1aae8-172">このプロパティが **True** に設定されている場合、ユーザーは、**検索半径** プロパティを省略して、すべての店舗を表示することができ ます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-172">When this property is set to **True**, users can bypass the **Search radius** property and view all stores.</span></span> |
| <span data-ttu-id="1aae8-173">Autosuggest オプション: 最大結果</span><span class="sxs-lookup"><span data-stu-id="1aae8-173">Autosuggest options: Max results</span></span> | <span data-ttu-id="1aae8-174">番号</span><span class="sxs-lookup"><span data-stu-id="1aae8-174">Number</span></span> | <span data-ttu-id="1aae8-175">このプロパティは、Bing Autosuggest API を介して表示できる Autosuggest 結果の最大数を定義します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-175">This property defines the maximum number of autosuggest results that can be shown via the Bing Autosuggest API.</span></span> |
| <span data-ttu-id="1aae8-176">検索半径</span><span class="sxs-lookup"><span data-stu-id="1aae8-176">Search radius</span></span> | <span data-ttu-id="1aae8-177">番号</span><span class="sxs-lookup"><span data-stu-id="1aae8-177">Number</span></span> | <span data-ttu-id="1aae8-178">このプロパティは、店舗の検索半径をマイル単位で定義します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-178">This property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="1aae8-179">値が指定されていない場合は、既定の検索半径 (50マイル) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-179">If no value is specified, the default search radius of 50 miles is used.</span></span> |
| <span data-ttu-id="1aae8-180">サービス条件</span><span class="sxs-lookup"><span data-stu-id="1aae8-180">Terms of service</span></span> | <span data-ttu-id="1aae8-181">URL</span><span class="sxs-lookup"><span data-stu-id="1aae8-181">URL</span></span> |  <span data-ttu-id="1aae8-182">このプロパティは、Bing Maps サービスを使用するために必要なサービス URL の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-182">This property specifies the terms of service URL that is required to use the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="1aae8-183">店舗セレクター モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="1aae8-183">Add a store selector module to a page</span></span>

<span data-ttu-id="1aae8-184">**店舗で受け取り**モードの場合 、モジュールは PDP およびカート ページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="1aae8-184">For **Pickup in store** mode, the module can be used only on PDPs and cart pages.</span></span> <span data-ttu-id="1aae8-185">このモードは、モジュールのプロパティ ウィンドウで、**店舗で受け取り** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1aae8-185">You must set the mode to **Pickup in store** in the module's property pane.</span></span>

- <span data-ttu-id="1aae8-186">購入ボックス モジュールに店舗セレクター モジュールを追加する方法の詳細については、[購入ボックス モジュール](add-buy-box.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1aae8-186">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="1aae8-187">カート モジュールに店舗セレクター モジュールを追加する方法の詳細については、[カート モジュール](add-cart-module.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="1aae8-187">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

<span data-ttu-id="1aae8-188">店舗の場所ページで利用可能な店舗を表示するように店舗セレクター モジュールをコンフィギュレーションするには、このトピックの前の図に示すように、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-188">To configure the store selector module to show available stores for a store locations page, as in the illustration that appears earlier in this topic, follow these steps.</span></span>

1. <span data-ttu-id="1aae8-189">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-189">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1aae8-190">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-190">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-191">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-191">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1aae8-192">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-192">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="1aae8-193">**テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-193">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="1aae8-194">**ページ名**配下で、**店舗の場所**を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-194">Under **Page name**, enter **Store locations**, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-195">新規ページの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-195">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1aae8-196">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-196">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-197">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-197">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1aae8-198">**モジュールの追加** ダイアログ ボックスで、**2 列のコンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-198">In the **Add Module** dialog box, select the **Container with 2 columns** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-199">モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-199">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="1aae8-200">**超小型表示ポート列コンフィギュレーション** 値を **100%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-200">Set the **X-Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="1aae8-201">**小型表示ポート列コンフィギュレーション** 値を **100%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-201">Set the **Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="1aae8-202">**中型表示ポート列コンフィギュレーション** 値を **33% 67%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-202">Set the **Medium view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="1aae8-203">**大型表示ポート列コンフィギュレーション** 値を **33% 67%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-203">Set the **Large view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="1aae8-204">**2 列のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-204">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1aae8-205">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-205">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-206">モジュールのプロパティ ウィンドウで、**モード** の値を **店舗の検索** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-206">In the module's properties pane, set the **Mode** value to **Find stores**.</span></span>
1. <span data-ttu-id="1aae8-207">**検索半径** 値をマイル単位で設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-207">Set the **Search radius** value in miles.</span></span>
1. <span data-ttu-id="1aae8-208">必要に応じて、その他のプロパティ (**優先ストアとして設定**、**すべての店舗を表示**、**自動提案を有効にする** など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-208">Set other properties, such as **Set as preferred store**, **Show all stores**, and **Enable auto suggestion**, as you require.</span></span>
1. <span data-ttu-id="1aae8-209">**2 列のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-209">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1aae8-210">**モジュールの追加** ダイアログ ボックスで、**マップ** モジュールを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-210">In the **Add Module** dialog box, select the **Map** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1aae8-211">モジュールのプロパティ ウィンドウで、必要に応じて追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-211">In the module's properties pane, set any additional properties as you require.</span></span>
1. <span data-ttu-id="1aae8-212">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="1aae8-212">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="1aae8-213">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1aae8-213">Additional resources</span></span>

[<span data-ttu-id="1aae8-214">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="1aae8-214">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1aae8-215">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="1aae8-215">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1aae8-216">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="1aae8-216">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1aae8-217">PDP のクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="1aae8-217">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="1aae8-218">カートとチェックアウトのクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="1aae8-218">Quick tour of cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="1aae8-219">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="1aae8-219">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="1aae8-220">組織の Bing 地図の管理</span><span class="sxs-lookup"><span data-stu-id="1aae8-220">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="1aae8-221">Bing Maps REST API</span><span class="sxs-lookup"><span data-stu-id="1aae8-221">Bing Maps REST APIs</span></span>](https://docs.microsoft.com/bingmaps/rest-services/)

[<span data-ttu-id="1aae8-222">マップ モジュール</span><span class="sxs-lookup"><span data-stu-id="1aae8-222">Maps module</span></span>](map-module.md)
