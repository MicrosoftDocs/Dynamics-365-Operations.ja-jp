---
title: サイト セレクター モジュール
description: このトピックでは、サイト セレクター モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: 6e8eefe7afe385ca77eca6027638ff938e1356e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791778"
---
# <a name="site-selector-module"></a><span data-ttu-id="a99f8-103">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="a99f8-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a99f8-104">このトピックでは、サイト セレクター モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a99f8-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a99f8-105">市場、地域、およびロケールにまたがってサイトが異なる場合は、サイトのユーザーがサイト間を移動したり、使用する買い物サイトを選択したりするための簡単な方法が必要です。</span><span class="sxs-lookup"><span data-stu-id="a99f8-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="a99f8-106">このシナリオに対応するために、サイト選択モジュールを使用すると、ユーザーは複数のサイトにまたがって閲覧できます。</span><span class="sxs-lookup"><span data-stu-id="a99f8-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="a99f8-107">サイト選択モジュールは、サイトユーザーが参照できるサイト (市場、地域、またはロケール) のリストでコンフィギュレーションされていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a99f8-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="a99f8-108">この階層リンク モジュールは、Dynamics 365 Commerce の 10.0.14 リリースで入手できます。</span><span class="sxs-lookup"><span data-stu-id="a99f8-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="a99f8-109">次の図は、サイトページのヘッダーに記載されているサイト選択モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="a99f8-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![サイトページのヘッダーにおけるサイト選択モジュールの例](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="a99f8-111">サイト セレクター モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a99f8-111">Site selector module properties</span></span>

| <span data-ttu-id="a99f8-112">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a99f8-112">Property name</span></span> | <span data-ttu-id="a99f8-113">先頭値</span><span class="sxs-lookup"><span data-stu-id="a99f8-113">Value</span></span>                 | <span data-ttu-id="a99f8-114">説明</span><span class="sxs-lookup"><span data-stu-id="a99f8-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="a99f8-115">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="a99f8-115">Heading</span></span>       | <span data-ttu-id="a99f8-116">テキスト</span><span class="sxs-lookup"><span data-stu-id="a99f8-116">Text</span></span>                  | <span data-ttu-id="a99f8-117">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="a99f8-117">The heading for the module.</span></span> |
| <span data-ttu-id="a99f8-118">サイト オプション</span><span class="sxs-lookup"><span data-stu-id="a99f8-118">Site options</span></span>  | <span data-ttu-id="a99f8-119">名前、イメージ、URL</span><span class="sxs-lookup"><span data-stu-id="a99f8-119">Name, Image, URL</span></span>      | <span data-ttu-id="a99f8-120">このプロパティでは、モジュールに含まれるサイトごとに、名前、サイトのホームページへのリンク、表示するオプションのイメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="a99f8-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="a99f8-121">このイメージは、フラグ、または市場、地域、ロケールのいずれかの一部の表現にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a99f8-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="a99f8-122">サイト セレクター モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="a99f8-122">Add a site selector module to a page</span></span>

<span data-ttu-id="a99f8-123">サイト選択モジュールは、サイトセレクタースロットの下の [ヘッダー モジュール](author-header-module.md) に追加できます。</span><span class="sxs-lookup"><span data-stu-id="a99f8-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="a99f8-124">追加した後、モジュールのヘッダーとサイトのオプションを定義できます。</span><span class="sxs-lookup"><span data-stu-id="a99f8-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a99f8-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a99f8-125">Additional resources</span></span>

[<span data-ttu-id="a99f8-126">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="a99f8-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a99f8-127">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="a99f8-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a99f8-128">階層リンク モジュール</span><span class="sxs-lookup"><span data-stu-id="a99f8-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="a99f8-129">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="a99f8-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]