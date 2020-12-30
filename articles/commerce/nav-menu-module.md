---
title: ナビゲーション メニュー モジュール
description: このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4413889"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="2663f-103">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="2663f-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2663f-104">このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2663f-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2663f-105">概要</span><span class="sxs-lookup"><span data-stu-id="2663f-105">Overview</span></span>

<span data-ttu-id="2663f-106">ナビゲーション メニュー モジュールの主な目的は、Dynamics 365 Commerce 本社で定義されているチャンネル ナビゲーション階層に従って、サイトのユーザーが商品やサイトのページを参照できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="2663f-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="2663f-107">ナビゲーション メニュー モジュールでコンフィギュレーションされた品目は、サイトのヘッダーのナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="2663f-108">ナビゲーション メニュー モジュールは、電子商取引サイトの他のページにリンクする静的メニュー項目もサポートします。</span><span class="sxs-lookup"><span data-stu-id="2663f-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="2663f-109">ナビゲーション メニュー モジュールは、ページのヘッダー モジュールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="2663f-110">Fabrikam テーマでは、ナビゲーション メニューは既定では 2 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="2663f-111">Starter テーマでは、ナビゲーション メニューは既定では 3 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="2663f-112">レベル数を変更するには、テーマにビュー拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="2663f-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="2663f-113">次の図は、カテゴリ階層の 2 つのレベルと、いくつかの静的メニュー項目を含む、Fabrikam サイトのナビゲーション メニューの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2663f-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="2663f-114">![ナビゲーション メニュー モジュールの例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="2663f-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="2663f-115">ナビゲーション メニュー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="2663f-115">Navigation menu module properties</span></span>

| <span data-ttu-id="2663f-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="2663f-116">Property name</span></span>             | <span data-ttu-id="2663f-117">先頭値</span><span class="sxs-lookup"><span data-stu-id="2663f-117">Value</span></span>                 | <span data-ttu-id="2663f-118">説明</span><span class="sxs-lookup"><span data-stu-id="2663f-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2663f-119">配賦元</span><span class="sxs-lookup"><span data-stu-id="2663f-119">Source</span></span>                  | <span data-ttu-id="2663f-120">**Retail**、**手動による作成**、**Retail と手動作成**</span><span class="sxs-lookup"><span data-stu-id="2663f-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="2663f-121">**Retail** の値を使用すると、Commerce 本社のチャンネル ナビゲーション階層がナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="2663f-122">**手動作成** の値によって、静的なメニュー項目を選別できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="2663f-123">**Retail および手動作成** 値により、両方を組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="2663f-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="2663f-124">カテゴリ イメージの表示</span><span class="sxs-lookup"><span data-stu-id="2663f-124">Show category images</span></span> | <span data-ttu-id="2663f-125">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="2663f-125">**True** or **False**</span></span>    | <span data-ttu-id="2663f-126">このプロパティを有効にすると、カテゴリごとのカテゴリ イメージがナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="2663f-127">Commerce リリース 10.0.14 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="2663f-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="2663f-128">複数レベルのナビゲーション メニューの有効化</span><span class="sxs-lookup"><span data-stu-id="2663f-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="2663f-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="2663f-129">**True** or **False**</span></span> | <span data-ttu-id="2663f-130">このプロパティを有効にすると、ナビゲーション メニューに複数のレベルのナビゲーション階層を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="2663f-131">この機能は Dynamics 365 Commerce 10.0.15 リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="2663f-132">レベルの数</span><span class="sxs-lookup"><span data-stu-id="2663f-132">Number of levels</span></span> | <span data-ttu-id="2663f-133">integer</span><span class="sxs-lookup"><span data-stu-id="2663f-133">integer</span></span> | <span data-ttu-id="2663f-134">このプロパティは、**複数レベルのナビゲーション メニューの有効化** プロパティが、**True** に設定されている場合に表示されるレベルの数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2663f-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="2663f-135">静的メニュー項目</span><span class="sxs-lookup"><span data-stu-id="2663f-135">Static menu item</span></span>| <span data-ttu-id="2663f-136">値の配列</span><span class="sxs-lookup"><span data-stu-id="2663f-136">Array of values</span></span>| <span data-ttu-id="2663f-137">メニュー項目名を静的サイトページへのリンクに関連付ける静的メニュー項目。</span><span class="sxs-lookup"><span data-stu-id="2663f-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="2663f-138">その他のメニュー項目以下にメニュー項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="2663f-139">既定では、静的メニューはルート レベルで表示され、存在する場合はチャンネル ナビゲーション階層に追加されます。</span><span class="sxs-lookup"><span data-stu-id="2663f-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="2663f-140">ルート メニューを表示</span><span class="sxs-lookup"><span data-stu-id="2663f-140">Show root menu</span></span> | <span data-ttu-id="2663f-141">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="2663f-141">**True** or **False**</span></span> | <span data-ttu-id="2663f-142">このプロパティを有効にすると、ナビゲーション メニューをカスタム ルート (例えば **今すぐ購入**) で定義できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="2663f-143">この機能は Dynamics 365 Commerce 10.0.15 リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="2663f-144">ルート メニュー</span><span class="sxs-lookup"><span data-stu-id="2663f-144">Root menu</span></span> | <span data-ttu-id="2663f-145">文字列</span><span class="sxs-lookup"><span data-stu-id="2663f-145">string</span></span> | <span data-ttu-id="2663f-146">**ルート メニューを表示** プロパティが **True** に設定されている場合、このプロパティを使用してカスタム ルートのテキストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2663f-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="2663f-147">次の図は、Fabrikam サイトのナビゲーション メニューに表示されるカテゴリ イメージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2663f-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="2663f-148">![カテゴリ イメージを含むナビゲーション メニュー モジュールの例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="2663f-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="2663f-149">ヘッダー モジュールへのナビゲーション メニュー モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="2663f-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="2663f-150">ナビゲーション メニュー モジュールをヘッダー モジュールに追加する方法の詳細については、[ヘッダー モジュール](author-header-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2663f-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2663f-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2663f-151">Additional resources</span></span>

[<span data-ttu-id="2663f-152">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="2663f-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2663f-153">階層リンク モジュール</span><span class="sxs-lookup"><span data-stu-id="2663f-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="2663f-154">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="2663f-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="2663f-155">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="2663f-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2663f-156">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="2663f-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="2663f-157">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="2663f-157">Header module</span></span>](author-header-module.md)
