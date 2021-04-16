---
title: マップ モジュール
description: このトピックでは、マップ モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794190"
---
# <a name="map-module"></a><span data-ttu-id="0c4a7-103">地図モジュール</span><span class="sxs-lookup"><span data-stu-id="0c4a7-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0c4a7-104">このトピックでは、マップ モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c4a7-105">マップ モジュールは、[Bing Maps V8 Web コントロール](https://docs.microsoft.com/bingmaps/v8-web-control/) を使用してレンダリングされるインタラクティブなマップ上の店舗の場所を示します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="0c4a7-106">Bing Maps API キーは必須で、Commerce 本社の共有パラメータ ページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="0c4a7-107">マップ モジュールには、マップの場所を表示するためにユーザーが選択できる、道路、航空写真、路上などのさまざまなビューが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="0c4a7-108">また、ズームやユーザーの位置の使用などの操作も可能になります。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="0c4a7-109">マップ モジュールは、マップにレンダリングする必要がある店舗の地理的な場所を決定するために、店舗セレクター モジュールと連携して機能します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="0c4a7-110">店舗セレクターとマップ モジュールは、ユーザーがサイト ページのいずれかのモジュールで店舗を選択したときに相互作用します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="0c4a7-111">マップ モジュールは、店舗セレクター モジュールとの相互作用を超えて、他のシナリオにも拡張できます。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="0c4a7-112">ただし、モジュールのカスタマイズは必須です。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="0c4a7-113">マップ モジュールは、Dynamics 365 Commerce 10.0.13 リリースで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="0c4a7-114">以下の図は、店舗ロケーション ページで使用されるマップ モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![店舗セレクター モジュールの例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="0c4a7-116">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="0c4a7-116">Module properties</span></span>

| <span data-ttu-id="0c4a7-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0c4a7-117">Property name</span></span>             | <span data-ttu-id="0c4a7-118">先頭値</span><span class="sxs-lookup"><span data-stu-id="0c4a7-118">Value</span></span>                 | <span data-ttu-id="0c4a7-119">説明</span><span class="sxs-lookup"><span data-stu-id="0c4a7-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0c4a7-120">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="0c4a7-120">Heading</span></span> | <span data-ttu-id="0c4a7-121">テキスト</span><span class="sxs-lookup"><span data-stu-id="0c4a7-121">Text</span></span> | <span data-ttu-id="0c4a7-122">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-122">The heading for the module.</span></span> |
| <span data-ttu-id="0c4a7-123">押しピン オプション: 既定のアイコン</span><span class="sxs-lookup"><span data-stu-id="0c4a7-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="0c4a7-124">画像</span><span class="sxs-lookup"><span data-stu-id="0c4a7-124">Image</span></span> | <span data-ttu-id="0c4a7-125">マップに表示される店舗に使用する押しピンのシンボル イメージ。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="0c4a7-126">押しピン オプション: アクティブ アイコン</span><span class="sxs-lookup"><span data-stu-id="0c4a7-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="0c4a7-127">画像</span><span class="sxs-lookup"><span data-stu-id="0c4a7-127">Image</span></span> | <span data-ttu-id="0c4a7-128">マップで選択された店舗に使用する押しピンのシンボル イメージ。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="0c4a7-129">押しピン オプション: 既定のアイコン色</span><span class="sxs-lookup"><span data-stu-id="0c4a7-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="0c4a7-130">文字列</span><span class="sxs-lookup"><span data-stu-id="0c4a7-130">Character string</span></span> | <span data-ttu-id="0c4a7-131">マップ上の押しピン シンボル色のテキストまたは 16 進値。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="0c4a7-132">押しピン オプション: アクティブ アイコン色</span><span class="sxs-lookup"><span data-stu-id="0c4a7-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="0c4a7-133">文字列</span><span class="sxs-lookup"><span data-stu-id="0c4a7-133">Character string</span></span> | <span data-ttu-id="0c4a7-134">マップ上の選択された押しピン シンボル色のテキストまたは 16 進値。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="0c4a7-135">インデックスの表示</span><span class="sxs-lookup"><span data-stu-id="0c4a7-135">Show index</span></span> | <span data-ttu-id="0c4a7-136">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0c4a7-136">**True** or **False**</span></span> | <span data-ttu-id="0c4a7-137">このプロパティが **True** に設定されている場合、店舗を示すすべての押しピン シンボルにインデックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="0c4a7-138">このインデックスは、店舗セレクター モジュールが表示するリスト表示のインデックスと一致します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="0c4a7-139">サイトのコンテンツ セキュリティ ポリシー ディレクティブに許可されたマッピング URLを追加する</span><span class="sxs-lookup"><span data-stu-id="0c4a7-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="0c4a7-140">マップ モジュールが Bing Maps と連携するには、サイトのコンテンツ セキュリティ ポリシー (CSP) に従って、次のマッピング URL が許可されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="0c4a7-141">この設定は、Commerce サイト ビルダーで、さまざまなサイト CSP ディレクティブ (**img-src** など) に許可された URL を追加することによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="0c4a7-142">詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="0c4a7-143">**connect-src** ディレクティブに **&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="0c4a7-144">**img-src** ディレクティブに **&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="0c4a7-145">**script-src** ディレクティブに、**&#42;.bing.com、&#42;.virtualearth.net** を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="0c4a7-146">**script style-src** ディレクティブに、**&#42;.bing.com** を追加します。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="0c4a7-147">マップ モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="0c4a7-147">Add a map module to a page</span></span>

<span data-ttu-id="0c4a7-148">ページにマップ モジュールを構成する方法の詳細については、[店舗セレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c4a7-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="0c4a7-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0c4a7-149">Additional resources</span></span>

[<span data-ttu-id="0c4a7-150">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="0c4a7-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c4a7-151">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="0c4a7-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0c4a7-152">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="0c4a7-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0c4a7-153">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="0c4a7-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="0c4a7-154">組織の Bing 地図の管理</span><span class="sxs-lookup"><span data-stu-id="0c4a7-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="0c4a7-155">Bing Maps V8 Web コントロール</span><span class="sxs-lookup"><span data-stu-id="0c4a7-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]