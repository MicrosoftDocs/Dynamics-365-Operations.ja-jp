---
title: ナビゲーション メニュー モジュール
description: このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817877"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="0b221-103">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="0b221-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0b221-104">このトピックでは、ナビゲーション メニュー モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b221-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0b221-105">概要</span><span class="sxs-lookup"><span data-stu-id="0b221-105">Overview</span></span>

<span data-ttu-id="0b221-106">ナビゲーション メニュー モジュールの主な目的は、Dynamics 365 Commerce 本社で定義されているチャンネル ナビゲーション階層に従って、サイトのユーザーが商品やサイトのページを参照できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="0b221-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="0b221-107">ナビゲーション メニュー モジュールでコンフィギュレーションされた品目は、サイトのヘッダーのナビゲーションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="0b221-108">ナビゲーション メニュー モジュールは、電子商取引サイトの他のページにリンクする静的メニュー項目もサポートします。</span><span class="sxs-lookup"><span data-stu-id="0b221-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="0b221-109">ナビゲーション メニュー モジュールは、ページのヘッダー モジュールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="0b221-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="0b221-110">Fabrikam テーマでは、ナビゲーション メニューは既定では 2 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="0b221-111">Starter テーマでは、ナビゲーション メニューは既定では 3 つのレベルで表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="0b221-112">レベル数を変更するには、テーマにビュー拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="0b221-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="0b221-113">次の図は、カテゴリ階層の 2 つのレベルと、いくつかの静的メニュー項目を含む、Fabrikam サイトのナビゲーション メニューの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0b221-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="0b221-114">![ナビゲーション メニュー モジュールの例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="0b221-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="0b221-115">ナビゲーション メニュー モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="0b221-115">Navigation menu module properties</span></span>

| <span data-ttu-id="0b221-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="0b221-116">Property name</span></span>             | <span data-ttu-id="0b221-117">先頭値</span><span class="sxs-lookup"><span data-stu-id="0b221-117">Value</span></span>                 | <span data-ttu-id="0b221-118">説明</span><span class="sxs-lookup"><span data-stu-id="0b221-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0b221-119">配賦元</span><span class="sxs-lookup"><span data-stu-id="0b221-119">Source</span></span>                  | <span data-ttu-id="0b221-120">**Retail**、**手動による作成**、**Retail と手動作成**</span><span class="sxs-lookup"><span data-stu-id="0b221-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="0b221-121">**Retail** の値を使用すると、Commerce 本社のチャンネル ナビゲーション階層がナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="0b221-122">**手動作成** の値によって、静的なメニュー項目を選別できます。</span><span class="sxs-lookup"><span data-stu-id="0b221-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="0b221-123">**Retail および手動作成** 値により、両方を組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="0b221-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="0b221-124">カテゴリ イメージの表示</span><span class="sxs-lookup"><span data-stu-id="0b221-124">Show category images</span></span> | <span data-ttu-id="0b221-125">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0b221-125">**True** or **False**</span></span>    | <span data-ttu-id="0b221-126">このプロパティを有効にすると、カテゴリごとのカテゴリ イメージがナビゲーション メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="0b221-127">Commerce リリース 10.0.14 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="0b221-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="0b221-128">静的メニュー項目</span><span class="sxs-lookup"><span data-stu-id="0b221-128">Static menu item</span></span>| <span data-ttu-id="0b221-129">値の配列</span><span class="sxs-lookup"><span data-stu-id="0b221-129">Array of values</span></span>| <span data-ttu-id="0b221-130">メニュー項目名を静的サイトページへのリンクに関連付ける静的メニュー項目。</span><span class="sxs-lookup"><span data-stu-id="0b221-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="0b221-131">その他のメニュー項目以下にメニュー項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0b221-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="0b221-132">既定では、静的メニューはルート レベルで表示され、存在する場合はチャンネル ナビゲーション階層に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0b221-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="0b221-133">次の図は、Fabrikam サイトのナビゲーション メニューに表示されるカテゴリ イメージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0b221-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="0b221-134">![カテゴリ イメージを含むナビゲーション メニュー モジュールの例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="0b221-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="0b221-135">ヘッダー モジュールへのナビゲーション メニュー モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="0b221-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="0b221-136">ナビゲーション メニュー モジュールをヘッダー モジュールに追加する方法の詳細については、[ヘッダー モジュール](author-header-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b221-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b221-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0b221-137">Additional resources</span></span>

[<span data-ttu-id="0b221-138">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="0b221-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0b221-139">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="0b221-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0b221-140">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="0b221-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="0b221-141">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="0b221-141">Header module</span></span>](author-header-module.md)
