---
title: 店舗セレクター モジュール
description: このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 04/02/2021
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a9311435264119e8287f1b7da2d0456552231f3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021467"
---
# <a name="store-selector-module"></a><span data-ttu-id="ffb40-103">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="ffb40-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffb40-104">このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ffb40-105">顧客は、店舗セレクター モジュールを使用して、オンライン購入後に選択した店舗の製品を集荷できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-105">Customers can use the store selector module to pick up a product in a selected store after an online purchase.</span></span> <span data-ttu-id="ffb40-106">Commerce バージョン 10.0.13 では、店舗セレクター モジュールにも、近くにある店舗を表示する **店舗の検索** ページを紹介する機能が追加されています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-106">In Commerce version 10.0.13, the store selector module also includes additional capabilities that can showcase a **Find a Store** page that shows nearby stores.</span></span>

<span data-ttu-id="ffb40-107">店舗セレクター モジュールを使用すると、場所 (市町村、都道府県、住所など) を入力して検索半径内の店舗を検索できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-107">The store selector module lets users enter a location (city, state, address, and so on) to search for stores within a search radius.</span></span> <span data-ttu-id="ffb40-108">モジュールが最初に開かれたとき、顧客のブラウザーの場所を使用して、店舗が検索されます (同意を得ている場合)。</span><span class="sxs-lookup"><span data-stu-id="ffb40-108">When the module is first opened, it uses the customer's browser location to find stores (if consent is provided).</span></span>

## <a name="store-selector-module-usage"></a><span data-ttu-id="ffb40-109">店舗セレクター モジュールの使用</span><span class="sxs-lookup"><span data-stu-id="ffb40-109">Store selector module usage</span></span>

- <span data-ttu-id="ffb40-110">製品の詳細ページ (PDP) では、店舗セレクター モジュールを使用して受け取りのための店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-110">A store selector module can be used on a product details page (PDP) to select a store for pickup.</span></span>
- <span data-ttu-id="ffb40-111">買い物カゴ ページでは、店舗セレクター モジュールを使用して受け取りのための店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-111">A store selector module can be used on a cart page to select a store for pickup.</span></span>
- <span data-ttu-id="ffb40-112">店舗セレクター モジュールは、使用可能なすべての店舗を表示するスタンドアロン ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-112">A store selector module can be used on a standalone page that shows all available stores.</span></span>

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a><span data-ttu-id="ffb40-113">Commerce 本社でのフルフィルメント グループの設定</span><span class="sxs-lookup"><span data-stu-id="ffb40-113">Fulfillment group setup in Commerce headquarters</span></span>

<span data-ttu-id="ffb40-114">店舗セレクターで利用可能な店舗を表示するには、Commerce 本社でフルフィルメント グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-114">For the store selector to display available stores, the fulfillment group must be set up in Commerce headquarters.</span></span> <span data-ttu-id="ffb40-115">詳細については、[フルフィルメント グループの設定](customer-orders-overview.md#set-up-fulfillment-groups)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-115">For more information, see [Set up fulfillment groups](customer-orders-overview.md#set-up-fulfillment-groups).</span></span>

<span data-ttu-id="ffb40-116">さらに、フルフィルメント グループ内の各店舗に関しては、店舗の場所の緯度と経度を本社に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-116">In addition, for each store in the fulfillment group, the latitude and longitude of the store location must be defined in headquarters.</span></span>

<span data-ttu-id="ffb40-117">Commerce 本社の店舗の場所の経度と緯度値を入力するには次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ffb40-117">To enter the latitude and longitude values for a store location in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ffb40-118">**在庫管理 \> 設定 \> 在庫詳細** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-118">Go to **Inventory management \> Setup \> Inventory breakdown**.</span></span>
1. <span data-ttu-id="ffb40-119">左ウィンドウで、倉庫の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-119">Select the warehouse location in the left pane.</span></span>
1. <span data-ttu-id="ffb40-120">**住所** クイックタブで、**詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-120">On the **Addresses** FastTab, select **Advanced**.</span></span>

    ![本社の店舗詳細の例](./media/Store-address.png)

1. <span data-ttu-id="ffb40-122">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ffb40-123">**一般** クイックタブで、**緯度** および **軽度** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-123">On the **General** FastTab, enter values for **Latitude** and **Longitude**.</span></span>

    ![本社の店舗に対する緯度と経度設定の例](./media/Store-latitude-longitude.png)

1. <span data-ttu-id="ffb40-125">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-125">On the Action Pane, select **Save**.</span></span> 

## <a name="bing-maps-integration"></a><span data-ttu-id="ffb40-126">Bing Maps の統合</span><span class="sxs-lookup"><span data-stu-id="ffb40-126">Bing Maps integration</span></span>

<span data-ttu-id="ffb40-127">Bing の Geocoding および Autosuggest 機能を使用するために、ストア選択モジュールは [Bing Maps REST アプリケーション プログラミング インターフェイス (API)](/bingmaps/rest-services/) と統合されています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-127">The store selector module is integrated with the [Bing Maps REST application programming interfaces (APIs)](/bingmaps/rest-services/) to use Bing's Geocoding and Autosuggest features.</span></span> <span data-ttu-id="ffb40-128">Bing Maps API キーは必須で、Commerce 本社の共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-128">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="ffb40-129">Geocoding API は、場所を緯度と経度の値に変換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-129">The Geocoding API is used to convert a location to latitude and longitude values.</span></span> <span data-ttu-id="ffb40-130">Autosuggest API との統合は、ユーザーが検索フィールドに場所を入力したときに検索候補を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-130">The integration with the Autosuggest API is used to show search suggestions when users enter locations in the search field.</span></span>

<span data-ttu-id="ffb40-131">Autosuggest REST API の場合は、サイトのコンテンツ セキュリティ ポリシー (CSP) に対して、次の URL が許可されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-131">For the Autosuggest REST API, you must ensure that the following URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="ffb40-132">この設定は、Commerce サイト ビルダーで、サイトのさまざまな CSP ディレクティブ (**img-src** など) に許可された URL を追加することによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-132">This setup is done in Commerce site builder, by adding allowed URLs to various CSP directives for the site (for example, **img-src**).</span></span> <span data-ttu-id="ffb40-133">詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-133">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="ffb40-134">**connect-src** ディレクティブに **&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-134">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="ffb40-135">**img-src** ディレクティブに **&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-135">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="ffb40-136">**script-src** ディレクティブに、**&#42;.bing.com, &#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-136">To the **script-src** directive, **add &#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="ffb40-137">**script style-src** ディレクティブに、**&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-137">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

 
## <a name="pickup-in-store-mode"></a><span data-ttu-id="ffb40-138">店舗で受け取りモード</span><span class="sxs-lookup"><span data-stu-id="ffb40-138">Pickup in store mode</span></span>

<span data-ttu-id="ffb40-139">店舗セレクター モジュールでは、製品を受け取ることができる店舗の一覧を表示する **店舗で受け取り** モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-139">The store selector module supports a **Pick up in store** mode that shows a list of stores where a product is available for pickup.</span></span> <span data-ttu-id="ffb40-140">また、この一覧には店舗の営業時間と店舗ごとの製品在庫も表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-140">It also shows store hours and product inventory for each store in the list.</span></span> <span data-ttu-id="ffb40-141">店舗セレクター モジュールでは、製品の利用可能性を表示するためと、選択した店舗で製品の配送モードが **受け取り** に設定されている場合はユーザーが製品を買い物カゴに追加できるように、製品のコンテキストが必要です 。</span><span class="sxs-lookup"><span data-stu-id="ffb40-141">The store selector module requires the context of a product to render product availability and to let the user add the product to the cart, if the product's delivery mode is set to **pickup** at the selected store.</span></span> <span data-ttu-id="ffb40-142">詳細については、[在庫設定](inventory-settings.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-142">For more information, see [Inventory settings](inventory-settings.md).</span></span> 

<span data-ttu-id="ffb40-143">店舗セレクター モジュールは、PDP の購入ボックス モジュールに追加して、製品を受け取ることができる店舗を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-143">The store selector module can be added to a buy box module on a PDP to show stores where a product is available for pickup.</span></span> <span data-ttu-id="ffb40-144">また、カート モジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-144">It can also be added to a cart module.</span></span> <span data-ttu-id="ffb40-145">この場合、店舗セレクター モジュールは、買い物カゴ内の各品目に対する受け取りオプションを表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-145">In this case, the store selector module shows pickup options for each line item in the cart.</span></span> <span data-ttu-id="ffb40-146">店舗セレクター モジュールは、拡張機能とカスタマイズによって、他のページまたはモジュールに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-146">The store selector module can also be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="ffb40-147">このシナリオが機能するためには、**受け取り** 配送モードが使用されるように製品をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-147">For this scenario to work, products should be configured so that the **pickup** delivery mode is used.</span></span> <span data-ttu-id="ffb40-148">それ以外の場合、このモジュールは製品ページでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="ffb40-148">Otherwise, the module won't be shown on the product pages.</span></span> <span data-ttu-id="ffb40-149">配送モードをコンフィギュレーションする方法の詳細については、[荷渡方法の設定](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-149">For more information about how to configure the delivery mode, see [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="ffb40-150">次の図は、PDP で使用される店舗セレクター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-150">The following image shows an example of a store selector module used on a PDP.</span></span>

![PDP で使用される店舗セレクター モジュールの例](./media/BOPIS.PNG)

> [!NOTE]
> <span data-ttu-id="ffb40-152">バージョン 10.0.16 では、新しい機能を有効にして、組織が顧客に対して複数のピッキング モードを定義できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-152">In version 10.0.16 and later, a new feature can be enabled which allows an organization to define multiple pick up modes of delivery options for customers.</span></span>  <span data-ttu-id="ffb40-153">この機能が有効になっている場合、電子商取引の店舗セレクターとその他のモジュールが強化され、複数の集荷配送オプション (コンフィギュレーションされている場合) の中から買い物客が選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-153">If this feature is enabled, the store selector and other modules of e-Commerce will be enhanced to allow the shopper to choose from potentially multiple pick up delivery options if configured.</span></span>  <span data-ttu-id="ffb40-154">この機能の詳細については、[このドキュメント](./multiple-pickup-modes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-154">To learn more about this feature, refer to [this documentation](./multiple-pickup-modes.md).</span></span> 

## <a name="find-stores-mode"></a><span data-ttu-id="ffb40-155">店舗検索モード</span><span class="sxs-lookup"><span data-stu-id="ffb40-155">Find stores mode</span></span>

<span data-ttu-id="ffb40-156">また、店舗セレクター モジュールは、**検索店舗** モードもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-156">The store selector module also supports a **Find stores** mode.</span></span> <span data-ttu-id="ffb40-157">このモードを使用すると、使用可能な店舗とその情報を表示する店舗の場所ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-157">This mode can be used to create a store locations page that shows available stores and their information.</span></span> <span data-ttu-id="ffb40-158">このモードでは、店舗セレクター モジュールは製品コンテキストなしで動作し、任意のサイト ページでスタンドアロン モジュールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-158">In this mode, the store selector module works without product context and can be used as a standalone module on any site page.</span></span> <span data-ttu-id="ffb40-159">さらに、モジュールに関連する設定が有効になっている場合、ユーザーは、その店舗を優先ストアとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-159">In addition, if the relevant settings are turned on for the module, users can select a store as their preferred store.</span></span> <span data-ttu-id="ffb40-160">店舗がユーザーの優先ストアとして選択されている場合、その店舗 ID はブラウザーの Cookie に保持されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-160">When a store is selected as a user's preferred store, the store ID is maintained in the browser cookie.</span></span> <span data-ttu-id="ffb40-161">したがって、ユーザーは Cookie の同意メッセージに同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-161">Therefore, the user must accept a cookie consent message.</span></span>

<span data-ttu-id="ffb40-162">次の図は、店舗の場所ページのマップ モジュールと共に使用される店舗セレクター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="ffb40-162">The following illustration shows an example of a store selector module that is used together with a map module on a store locations page.</span></span>

![保管場所ページの店舗セレクター モジュールとマップ モジュールの例](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a><span data-ttu-id="ffb40-164">マップのレンダリング</span><span class="sxs-lookup"><span data-stu-id="ffb40-164">Render a map</span></span>

<span data-ttu-id="ffb40-165">マップ モジュールを使用して、マップ上で店舗の場所を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-165">The store selector module can be used together with the map module to show the store locations on a map.</span></span> <span data-ttu-id="ffb40-166">マップ モジュールの詳細については、[マップ モジュール](map-module.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="ffb40-166">For more information about the map module, see [Map module](map-module.md)</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="ffb40-167">店舗セレクター モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ffb40-167">Store selector module properties</span></span>

| <span data-ttu-id="ffb40-168">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="ffb40-168">Property name</span></span> | <span data-ttu-id="ffb40-169">先頭値</span><span class="sxs-lookup"><span data-stu-id="ffb40-169">Value</span></span> | <span data-ttu-id="ffb40-170">説明</span><span class="sxs-lookup"><span data-stu-id="ffb40-170">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="ffb40-171">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="ffb40-171">Heading</span></span> | <span data-ttu-id="ffb40-172">テキスト</span><span class="sxs-lookup"><span data-stu-id="ffb40-172">Text</span></span> | <span data-ttu-id="ffb40-173">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="ffb40-173">The heading for the module.</span></span> |
| <span data-ttu-id="ffb40-174">モード</span><span class="sxs-lookup"><span data-stu-id="ffb40-174">Mode</span></span> | <span data-ttu-id="ffb40-175">**店舗の検索** または **店舗で受け取り**</span><span class="sxs-lookup"><span data-stu-id="ffb40-175">**Find stores** or **Pick up in store**</span></span> | <span data-ttu-id="ffb40-176">**店舗の検索** モードでは、利用可能な店舗が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-176">**Find stores** mode shows available stores.</span></span> <span data-ttu-id="ffb40-177">**店舗で受け取り** モードでは、ユーザーは受け取り用の店舗を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-177">**Pick up in store** mode lets users select a store for pickup.</span></span> |
| <span data-ttu-id="ffb40-178">スタイル</span><span class="sxs-lookup"><span data-stu-id="ffb40-178">Style</span></span> | <span data-ttu-id="ffb40-179">**ダイアログ** または **インライン**</span><span class="sxs-lookup"><span data-stu-id="ffb40-179">**Dialog** or **Inline**</span></span> | <span data-ttu-id="ffb40-180">このモジュールは、インラインまたはダイアログ ボックスのいずれかでレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-180">The module can be rendered either inline or in a dialog box.</span></span> |
| <span data-ttu-id="ffb40-181">優先店舗に設定する</span><span class="sxs-lookup"><span data-stu-id="ffb40-181">Set as preferred store</span></span> | <span data-ttu-id="ffb40-182">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="ffb40-182">**True** or **False**</span></span> | <span data-ttu-id="ffb40-183">このプロパティが **True** に設定されている場合、ユーザーは優先ストアを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-183">When this property is set to **True**, users can set a preferred store.</span></span> <span data-ttu-id="ffb40-184">この機能を使用するには、ユーザーが Cookie の同意メッセージを受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-184">This feature requires that users accept a cookie consent message.</span></span> |
| <span data-ttu-id="ffb40-185">全店舗を表示する</span><span class="sxs-lookup"><span data-stu-id="ffb40-185">Show all stores</span></span> | <span data-ttu-id="ffb40-186">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="ffb40-186">**True** or **False**</span></span> | <span data-ttu-id="ffb40-187">このプロパティが **True** に設定されている場合、ユーザーは、**検索半径** プロパティを省略して、すべての店舗を表示することができ ます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-187">When this property is set to **True**, users can bypass the **Search radius** property and view all stores.</span></span> |
| <span data-ttu-id="ffb40-188">Autosuggest オプション: 最大結果</span><span class="sxs-lookup"><span data-stu-id="ffb40-188">Autosuggest options: Max results</span></span> | <span data-ttu-id="ffb40-189">番号</span><span class="sxs-lookup"><span data-stu-id="ffb40-189">Number</span></span> | <span data-ttu-id="ffb40-190">このプロパティは、Bing Autosuggest API を介して表示できる Autosuggest 結果の最大数を定義します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-190">This property defines the maximum number of autosuggest results that can be shown via the Bing Autosuggest API.</span></span> |
| <span data-ttu-id="ffb40-191">検索半径</span><span class="sxs-lookup"><span data-stu-id="ffb40-191">Search radius</span></span> | <span data-ttu-id="ffb40-192">番号</span><span class="sxs-lookup"><span data-stu-id="ffb40-192">Number</span></span> | <span data-ttu-id="ffb40-193">このプロパティは、店舗の検索半径をマイル単位で定義します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-193">This property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="ffb40-194">値が指定されていない場合は、既定の検索半径 (50マイル) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-194">If no value is specified, the default search radius of 50 miles is used.</span></span> |
| <span data-ttu-id="ffb40-195">サービス条件</span><span class="sxs-lookup"><span data-stu-id="ffb40-195">Terms of service</span></span> | <span data-ttu-id="ffb40-196">URL</span><span class="sxs-lookup"><span data-stu-id="ffb40-196">URL</span></span> |  <span data-ttu-id="ffb40-197">このプロパティは、Bing Maps サービスを使用するために必要なサービス URL の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-197">This property specifies the terms of service URL that is required to use the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="ffb40-198">店舗セレクター モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="ffb40-198">Add a store selector module to a page</span></span>

<span data-ttu-id="ffb40-199">**店舗で受け取り** モードの場合 、モジュールは PDP およびカート ページでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb40-199">For **Pickup in store** mode, the module can be used only on PDPs and cart pages.</span></span> <span data-ttu-id="ffb40-200">このモードは、モジュールのプロパティ ウィンドウで、**店舗で受け取り** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb40-200">You must set the mode to **Pickup in store** in the module's property pane.</span></span>

- <span data-ttu-id="ffb40-201">購入ボックス モジュールに店舗セレクター モジュールを追加する方法の詳細については、[購入ボックス モジュール](add-buy-box.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffb40-201">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="ffb40-202">カート モジュールに店舗セレクター モジュールを追加する方法の詳細については、[カート モジュール](add-cart-module.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="ffb40-202">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

<span data-ttu-id="ffb40-203">店舗の場所ページで利用可能な店舗を表示するように店舗セレクター モジュールをコンフィギュレーションするには、このトピックの前の図に示すように、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-203">To configure the store selector module to show available stores for a store locations page, as in the illustration that appears earlier in this topic, follow these steps.</span></span>

1. <span data-ttu-id="ffb40-204">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-204">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ffb40-205">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-205">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-206">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-206">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ffb40-207">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-207">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="ffb40-208">**テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-208">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="ffb40-209">**ページ名** 配下で、**店舗の場所** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-209">Under **Page name**, enter **Store locations**, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-210">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-210">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffb40-211">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-211">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-212">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-212">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffb40-213">**モジュールの追加** ダイアログ ボックスで、**2 列のコンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-213">In the **Add Module** dialog box, select the **Container with 2 columns** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-214">モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-214">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="ffb40-215">**超小型表示ポート列コンフィギュレーション** 値を **100%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-215">Set the **X-Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="ffb40-216">**小型表示ポート列コンフィギュレーション** 値を **100%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-216">Set the **Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="ffb40-217">**中型表示ポート列コンフィギュレーション** 値を **33% 67%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-217">Set the **Medium view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="ffb40-218">**大型表示ポート列コンフィギュレーション** 値を **33% 67%** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-218">Set the **Large view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="ffb40-219">**2 列のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-219">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffb40-220">**モジュールの追加** ダイアログ ボックスで、**店舗セレクター** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-220">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-221">モジュールのプロパティ ウィンドウで、**モード** の値を **店舗の検索** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-221">In the module's properties pane, set the **Mode** value to **Find stores**.</span></span>
1. <span data-ttu-id="ffb40-222">**検索半径** 値をマイル単位で設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-222">Set the **Search radius** value in miles.</span></span>
1. <span data-ttu-id="ffb40-223">必要に応じて、その他のプロパティ (**優先ストアとして設定**、**すべての店舗を表示**、**自動提案を有効にする** など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-223">Set other properties, such as **Set as preferred store**, **Show all stores**, and **Enable auto suggestion**, as you require.</span></span>
1. <span data-ttu-id="ffb40-224">**2 列のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-224">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ffb40-225">**モジュールの追加** ダイアログ ボックスで、**マップ** モジュールを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-225">In the **Add Module** dialog box, select the **Map** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ffb40-226">モジュールのプロパティ ウィンドウで、必要に応じて追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-226">In the module's properties pane, set any additional properties as you require.</span></span>
1. <span data-ttu-id="ffb40-227">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="ffb40-227">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="ffb40-228">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ffb40-228">Additional resources</span></span>

[<span data-ttu-id="ffb40-229">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="ffb40-229">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ffb40-230">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="ffb40-230">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ffb40-231">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="ffb40-231">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ffb40-232">PDP のクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="ffb40-232">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="ffb40-233">カートとチェックアウトのクイック ツアー</span><span class="sxs-lookup"><span data-stu-id="ffb40-233">Quick tour of cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="ffb40-234">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="ffb40-234">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="ffb40-235">組織の Bing 地図の管理</span><span class="sxs-lookup"><span data-stu-id="ffb40-235">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="ffb40-236">Bing Maps REST API</span><span class="sxs-lookup"><span data-stu-id="ffb40-236">Bing Maps REST APIs</span></span>](/bingmaps/rest-services/)

[<span data-ttu-id="ffb40-237">マップ モジュール</span><span class="sxs-lookup"><span data-stu-id="ffb40-237">Maps module</span></span>](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]