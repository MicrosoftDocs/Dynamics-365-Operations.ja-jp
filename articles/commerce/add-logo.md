---
title: ロゴの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817333"
---
# <a name="add-a-logo"></a><span data-ttu-id="47e78-103">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="47e78-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47e78-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="47e78-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="47e78-105">概要</span><span class="sxs-lookup"><span data-stu-id="47e78-105">Overview</span></span>

<span data-ttu-id="47e78-106">サイトの構築時には、まず最初に会社またはブランド ロゴをサイトのヘッダーに追加するのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="47e78-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="47e78-107">Dynamics 365 Commerce オンライン モジュール ライブラリでは、このタスクを簡単にするためのモジュールが提供されます。</span><span class="sxs-lookup"><span data-stu-id="47e78-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="47e78-108">テンプレート、レイアウト、またはページに、ロゴを直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="47e78-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="47e78-109">この方法により、特定のページまたはページ グループに表示されるロゴを簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="47e78-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="47e78-110">ただし、このトピックでは、サイトのすべてのページで再利用できるヘッダー フラグメントにロゴを追加する最もよくあるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="47e78-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="47e78-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="47e78-111">Prerequisites</span></span>

<span data-ttu-id="47e78-112">サイトのすべてのページにロゴを追加する前に、これらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47e78-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="47e78-113">ロゴをメディア ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="47e78-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="47e78-114">ヘッダー フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="47e78-114">Create a header fragment.</span></span> <span data-ttu-id="47e78-115">フラグメントの作成および使用方法の詳細については、[フラグメントの使用](work-with-fragments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47e78-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="47e78-116">サイトのページがレイアウトやモジュール オプションとして使用するヘッダー フラグメントをテンプレートに含めます。</span><span class="sxs-lookup"><span data-stu-id="47e78-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="47e78-117">テンプレートの詳細については、[テンプレートの使用](work-with-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47e78-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="47e78-118">ヘッダー フラグメントへのロゴの追加</span><span class="sxs-lookup"><span data-stu-id="47e78-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="47e78-119">サイトのヘッダー フラグメントにロゴを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="47e78-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="47e78-120">左のナビゲーション ウィンドウで、**フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="47e78-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="47e78-121">作成したヘッダー フラグメントを選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="47e78-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="47e78-122">ヘッダー モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="47e78-122">Expand the header module.</span></span>
1. <span data-ttu-id="47e78-123">ヘッダー モジュールのプロパティ ウィンドウで、ロゴの画像とリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="47e78-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="47e78-124">ヘッダー フラグメントを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="47e78-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="47e78-125">更新されたヘッダー フラグメントを公開すると、ヘッダー フラグメントを含むテンプレートを使用するすべてのサイト ページにロゴが表示されます。</span><span class="sxs-lookup"><span data-stu-id="47e78-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47e78-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="47e78-126">Additional resources</span></span>

[<span data-ttu-id="47e78-127">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="47e78-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="47e78-128">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="47e78-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="47e78-129">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="47e78-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="47e78-130">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="47e78-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="47e78-131">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="47e78-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="47e78-132">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="47e78-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="47e78-133">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="47e78-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

