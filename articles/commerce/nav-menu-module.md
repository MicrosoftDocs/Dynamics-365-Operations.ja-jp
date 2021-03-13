---
title: ナビゲーション メニュー モジュール
description: このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 65f8b6128b140f3fa776659d8920dfc5e095213f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097393"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="e6fc4-103">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="e6fc4-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e6fc4-104">このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e6fc4-105">ナビゲーション メニュー モジュールの主な目的は、Dynamics 365 Commerce 本社で定義されているチャンネル ナビゲーション階層に従って、サイトのユーザーが商品やサイトのページを参照できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="e6fc4-106">ナビゲーション メニュー モジュールでコンフィギュレーションされた品目は、サイトのヘッダーのナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="e6fc4-107">ナビゲーション メニュー モジュールは、電子商取引サイトの他のページにリンクする静的メニュー項目もサポートします。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="e6fc4-108">ナビゲーション メニュー モジュールは、ページのヘッダー モジュールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="e6fc4-109">Fabrikam テーマでは、ナビゲーション メニューは既定では 2 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="e6fc4-110">Starter テーマでは、ナビゲーション メニューは既定では 3 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="e6fc4-111">レベル数を変更するには、テーマにビュー拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="e6fc4-112">次の図は、カテゴリ階層の 2 つのレベルと、いくつかの静的メニュー項目を含む、Fabrikam サイトのナビゲーション メニューの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="e6fc4-113">![ナビゲーション メニュー モジュールの例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="e6fc4-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="e6fc4-114">ナビゲーション メニュー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="e6fc4-114">Navigation menu module properties</span></span>

| <span data-ttu-id="e6fc4-115">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e6fc4-115">Property name</span></span>             | <span data-ttu-id="e6fc4-116">先頭値</span><span class="sxs-lookup"><span data-stu-id="e6fc4-116">Value</span></span>                 | <span data-ttu-id="e6fc4-117">説明</span><span class="sxs-lookup"><span data-stu-id="e6fc4-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e6fc4-118">配賦元</span><span class="sxs-lookup"><span data-stu-id="e6fc4-118">Source</span></span>                  | <span data-ttu-id="e6fc4-119">**Retail**、**手動による作成**、**Retail と手動作成**</span><span class="sxs-lookup"><span data-stu-id="e6fc4-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="e6fc4-120">**Retail** の値を使用すると、Commerce 本社のチャンネル ナビゲーション階層がナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="e6fc4-121">**手動作成** の値によって、静的なメニュー項目を選別できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="e6fc4-122">**Retail および手動作成** 値により、両方を組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="e6fc4-123">カテゴリ イメージの表示</span><span class="sxs-lookup"><span data-stu-id="e6fc4-123">Show category images</span></span> | <span data-ttu-id="e6fc4-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e6fc4-124">**True** or **False**</span></span>    | <span data-ttu-id="e6fc4-125">このプロパティを有効にすると、カテゴリごとのカテゴリ イメージがナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="e6fc4-126">Commerce リリース 10.0.14 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="e6fc4-127">プロモーションの表示</span><span class="sxs-lookup"><span data-stu-id="e6fc4-127">Show promotions</span></span> | <span data-ttu-id="e6fc4-128">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e6fc4-128">**True** or **False**</span></span> | <span data-ttu-id="e6fc4-129">このプロパティを有効にすると、画像、リンク、テキストを使用してプロモーションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="e6fc4-130">このプロパティは、Commerce のバージョン 10.0.17 リリースで追加されました。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="e6fc4-131">プロモーションの追加</span><span class="sxs-lookup"><span data-stu-id="e6fc4-131">Add promotions</span></span> | <span data-ttu-id="e6fc4-132">テキスト、画像、またはリンク</span><span class="sxs-lookup"><span data-stu-id="e6fc4-132">Text, image, or link</span></span> | <span data-ttu-id="e6fc4-133">**プロモーションの表示** プロパティが有効になっている場合は、ナビゲーション メニューで、プロモーション コンテンツにテキスト、画像、リンクを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="e6fc4-134">複数レベルのナビゲーション メニューの有効化</span><span class="sxs-lookup"><span data-stu-id="e6fc4-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="e6fc4-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e6fc4-135">**True** or **False**</span></span> | <span data-ttu-id="e6fc4-136">このプロパティを有効にすると、ナビゲーション メニューに複数のレベルのナビゲーション階層を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="e6fc4-137">この機能は、Commerce のバージョン 10.0.15 リリースで利用できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="e6fc4-138">レベルの数</span><span class="sxs-lookup"><span data-stu-id="e6fc4-138">Number of levels</span></span> | <span data-ttu-id="e6fc4-139">integer</span><span class="sxs-lookup"><span data-stu-id="e6fc4-139">integer</span></span> | <span data-ttu-id="e6fc4-140">このプロパティは、**複数レベルのナビゲーション メニューの有効化** プロパティが、**True** に設定されている場合に表示されるレベルの数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="e6fc4-141">静的メニュー項目</span><span class="sxs-lookup"><span data-stu-id="e6fc4-141">Static menu item</span></span>| <span data-ttu-id="e6fc4-142">値の配列</span><span class="sxs-lookup"><span data-stu-id="e6fc4-142">Array of values</span></span>| <span data-ttu-id="e6fc4-143">メニュー項目名を静的サイトページへのリンクに関連付ける静的メニュー項目。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="e6fc4-144">その他のメニュー項目以下にメニュー項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="e6fc4-145">既定では、静的メニューはルート レベルで表示され、存在する場合はチャンネル ナビゲーション階層に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="e6fc4-146">ルート メニューを表示</span><span class="sxs-lookup"><span data-stu-id="e6fc4-146">Show root menu</span></span> | <span data-ttu-id="e6fc4-147">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e6fc4-147">**True** or **False**</span></span> | <span data-ttu-id="e6fc4-148">このプロパティを有効にすると、ナビゲーション メニューをカスタム ルート (例えば **今すぐ購入**) で定義できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="e6fc4-149">この機能は Dynamics 365 Commerce 10.0.15 リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="e6fc4-150">ルート メニュー</span><span class="sxs-lookup"><span data-stu-id="e6fc4-150">Root menu</span></span> | <span data-ttu-id="e6fc4-151">文字列</span><span class="sxs-lookup"><span data-stu-id="e6fc4-151">string</span></span> | <span data-ttu-id="e6fc4-152">**ルート メニューを表示** プロパティが **True** に設定されている場合、このプロパティを使用してカスタム ルートのテキストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="e6fc4-153">次の図は、Fabrikam サイトのナビゲーション メニューに表示されるカテゴリ イメージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="e6fc4-154">![カテゴリ イメージを含むナビゲーション メニュー モジュールの例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="e6fc4-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="e6fc4-155">ヘッダー モジュールへのナビゲーション メニュー モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="e6fc4-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="e6fc4-156">ナビゲーション メニュー モジュールをヘッダー モジュールに追加する方法の詳細については、[ヘッダー モジュール](author-header-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e6fc4-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6fc4-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e6fc4-157">Additional resources</span></span>

[<span data-ttu-id="e6fc4-158">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="e6fc4-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e6fc4-159">階層リンク モジュール</span><span class="sxs-lookup"><span data-stu-id="e6fc4-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="e6fc4-160">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="e6fc4-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="e6fc4-161">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="e6fc4-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e6fc4-162">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="e6fc4-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="e6fc4-163">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="e6fc4-163">Header module</span></span>](author-header-module.md)
