---
title: サイト セレクター モジュール
description: このトピックでは、サイト セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985589"
---
# <a name="site-selector-module"></a><span data-ttu-id="84160-103">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="84160-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84160-104">このトピックでは、サイト セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84160-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="84160-105">概要</span><span class="sxs-lookup"><span data-stu-id="84160-105">Overview</span></span>

<span data-ttu-id="84160-106">市場、地域、およびロケールにまたがってサイトが異なる場合は、サイトのユーザーがサイト間を移動したり、使用する買い物サイトを選択したりするための簡単な方法が必要です。</span><span class="sxs-lookup"><span data-stu-id="84160-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="84160-107">このシナリオに対応するために、サイト選択モジュールを使用すると、ユーザーは複数のサイトにまたがって閲覧できます。</span><span class="sxs-lookup"><span data-stu-id="84160-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="84160-108">サイト選択モジュールは、サイトユーザーが参照できるサイト (市場、地域、またはロケール) のリストでコンフィギュレーションされていなければなりません。</span><span class="sxs-lookup"><span data-stu-id="84160-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="84160-109">この階層リンク モジュールは、Dynamics 365 Commerce の 10.0.14 リリースで入手できます。</span><span class="sxs-lookup"><span data-stu-id="84160-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="84160-110">次の図は、サイトページのヘッダーに記載されているサイト選択モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="84160-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![サイトページのヘッダーにおけるサイト選択モジュールの例](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="84160-112">サイト セレクター モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="84160-112">Site selector module properties</span></span>

| <span data-ttu-id="84160-113">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="84160-113">Property name</span></span> | <span data-ttu-id="84160-114">先頭値</span><span class="sxs-lookup"><span data-stu-id="84160-114">Value</span></span>                 | <span data-ttu-id="84160-115">説明</span><span class="sxs-lookup"><span data-stu-id="84160-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="84160-116">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="84160-116">Heading</span></span>       | <span data-ttu-id="84160-117">テキスト</span><span class="sxs-lookup"><span data-stu-id="84160-117">Text</span></span>                  | <span data-ttu-id="84160-118">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="84160-118">The heading for the module.</span></span> |
| <span data-ttu-id="84160-119">サイト オプション</span><span class="sxs-lookup"><span data-stu-id="84160-119">Site options</span></span>  | <span data-ttu-id="84160-120">名前、イメージ、URL</span><span class="sxs-lookup"><span data-stu-id="84160-120">Name, Image, URL</span></span>      | <span data-ttu-id="84160-121">このプロパティでは、モジュールに含まれるサイトごとに、名前、サイトのホームページへのリンク、表示するオプションのイメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="84160-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="84160-122">このイメージは、フラグ、または市場、地域、ロケールのいずれかの一部の表現にすることができます。</span><span class="sxs-lookup"><span data-stu-id="84160-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="84160-123">サイト セレクター モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="84160-123">Add a site selector module to a page</span></span>

<span data-ttu-id="84160-124">サイト選択モジュールは、サイトセレクタースロットの下の [ヘッダー モジュール](author-header-module.md) に追加できます。</span><span class="sxs-lookup"><span data-stu-id="84160-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="84160-125">追加した後、モジュールのヘッダーとサイトのオプションを定義できます。</span><span class="sxs-lookup"><span data-stu-id="84160-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84160-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="84160-126">Additional resources</span></span>

[<span data-ttu-id="84160-127">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="84160-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="84160-128">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="84160-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="84160-129">階層リンク モジュール</span><span class="sxs-lookup"><span data-stu-id="84160-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="84160-130">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="84160-130">Navigation menu module</span></span>](nav-menu-module.md)
