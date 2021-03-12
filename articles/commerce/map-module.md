---
title: マップ モジュール
description: このトピックでは、マップ モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e93358a9c76e8eb7bfb4ade4f772dece2aa5f7d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982494"
---
# <a name="map-module"></a><span data-ttu-id="aa088-103">マップ モジュール</span><span class="sxs-lookup"><span data-stu-id="aa088-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="aa088-104">このトピックでは、マップ モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa088-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aa088-105">概要</span><span class="sxs-lookup"><span data-stu-id="aa088-105">Overview</span></span>

<span data-ttu-id="aa088-106">マップ モジュールは、[Bing Maps V8 Web コントロール](https://docs.microsoft.com/bingmaps/v8-web-control/) を使用してレンダリングされるインタラクティブなマップ上の店舗の場所を示します。</span><span class="sxs-lookup"><span data-stu-id="aa088-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="aa088-107">Bing Maps API キーは必須で、Commerce 本社の共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa088-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="aa088-108">マップ モジュールには、マップの場所を表示するためにユーザーが選択できる、道路、航空写真、路上などのさまざまなビューが用意されています。</span><span class="sxs-lookup"><span data-stu-id="aa088-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="aa088-109">また、ズームやユーザーの位置の使用などの操作も可能になります。</span><span class="sxs-lookup"><span data-stu-id="aa088-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="aa088-110">マップ モジュールは、マップにレンダリングする必要がある店舗の地理的な場所を決定するために、店舗セレクター モジュールと連携して機能します。</span><span class="sxs-lookup"><span data-stu-id="aa088-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="aa088-111">店舗セレクターとマップ モジュールは、ユーザーがサイト ページのいずれかのモジュールで店舗を選択したときに相互作用します。</span><span class="sxs-lookup"><span data-stu-id="aa088-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="aa088-112">マップ モジュールは、店舗セレクター モジュールとの相互作用を超えて、他のシナリオにも拡張できます。</span><span class="sxs-lookup"><span data-stu-id="aa088-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="aa088-113">ただし、モジュールのカスタマイズは必須です。</span><span class="sxs-lookup"><span data-stu-id="aa088-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="aa088-114">マップ モジュールは、Dynamics 365 Commerce 10.0.13 リリースで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="aa088-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="aa088-115">以下の図は、店舗ロケーション ページで使用されるマップ モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="aa088-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![店舗セレクター モジュールの例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="aa088-117">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="aa088-117">Module properties</span></span>

| <span data-ttu-id="aa088-118">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="aa088-118">Property name</span></span>             | <span data-ttu-id="aa088-119">先頭値</span><span class="sxs-lookup"><span data-stu-id="aa088-119">Value</span></span>                 | <span data-ttu-id="aa088-120">説明</span><span class="sxs-lookup"><span data-stu-id="aa088-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="aa088-121">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="aa088-121">Heading</span></span> | <span data-ttu-id="aa088-122">テキスト</span><span class="sxs-lookup"><span data-stu-id="aa088-122">Text</span></span> | <span data-ttu-id="aa088-123">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="aa088-123">The heading for the module.</span></span> |
| <span data-ttu-id="aa088-124">押しピン オプション: 既定のアイコン</span><span class="sxs-lookup"><span data-stu-id="aa088-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="aa088-125">画像</span><span class="sxs-lookup"><span data-stu-id="aa088-125">Image</span></span> | <span data-ttu-id="aa088-126">マップに表示される店舗に使用する押しピンのシンボル イメージ。</span><span class="sxs-lookup"><span data-stu-id="aa088-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="aa088-127">押しピン オプション: アクティブ アイコン</span><span class="sxs-lookup"><span data-stu-id="aa088-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="aa088-128">画像</span><span class="sxs-lookup"><span data-stu-id="aa088-128">Image</span></span> | <span data-ttu-id="aa088-129">マップで選択された店舗に使用する押しピンのシンボル イメージ。</span><span class="sxs-lookup"><span data-stu-id="aa088-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="aa088-130">押しピン オプション: 既定のアイコン色</span><span class="sxs-lookup"><span data-stu-id="aa088-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="aa088-131">文字列</span><span class="sxs-lookup"><span data-stu-id="aa088-131">Character string</span></span> | <span data-ttu-id="aa088-132">マップ上の押しピン シンボル色のテキストまたは 16 進値。</span><span class="sxs-lookup"><span data-stu-id="aa088-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="aa088-133">押しピン オプション: アクティブ アイコン色</span><span class="sxs-lookup"><span data-stu-id="aa088-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="aa088-134">文字列</span><span class="sxs-lookup"><span data-stu-id="aa088-134">Character string</span></span> | <span data-ttu-id="aa088-135">マップ上の選択された押しピン シンボル色のテキストまたは 16 進値。</span><span class="sxs-lookup"><span data-stu-id="aa088-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="aa088-136">インデックスの表示</span><span class="sxs-lookup"><span data-stu-id="aa088-136">Show index</span></span> | <span data-ttu-id="aa088-137">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="aa088-137">**True** or **False**</span></span> | <span data-ttu-id="aa088-138">このプロパティが **True** に設定されている場合、店舗を示すすべての押しピン シンボルにインデックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa088-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="aa088-139">このインデックスは、店舗セレクター モジュールが表示するリスト表示のインデックスと一致します。</span><span class="sxs-lookup"><span data-stu-id="aa088-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="aa088-140">サイトのコンテンツ セキュリティ ポリシー ディレクティブに許可されたマッピング URLを追加する</span><span class="sxs-lookup"><span data-stu-id="aa088-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="aa088-141">マップ モジュールが Bing Maps と連携するには、サイトのコンテンツ セキュリティ ポリシー (CSP) に従って、次のマッピング URL が許可されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa088-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="aa088-142">この設定は、Commerce サイト ビルダーで、さまざまなサイト CSP ディレクティブ (**img-src** など) に許可された URL を追加することによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="aa088-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="aa088-143">詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa088-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="aa088-144">**connect-src** ディレクティブに **&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="aa088-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="aa088-145">**img-src** ディレクティブに **&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="aa088-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="aa088-146">**script-src** ディレクティブに、**&#42;.bing.com、&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="aa088-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="aa088-147">**script style-src** ディレクティブに、**&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="aa088-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="aa088-148">マップ モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="aa088-148">Add a map module to a page</span></span>

<span data-ttu-id="aa088-149">ページにマップ モジュールを構成する方法の詳細については、[店舗セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa088-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="aa088-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aa088-150">Additional resources</span></span>

[<span data-ttu-id="aa088-151">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="aa088-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aa088-152">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="aa088-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="aa088-153">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="aa088-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="aa088-154">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="aa088-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="aa088-155">組織の Bing 地図の管理</span><span class="sxs-lookup"><span data-stu-id="aa088-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="aa088-156">Bing Maps V8 Web コントロール</span><span class="sxs-lookup"><span data-stu-id="aa088-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
