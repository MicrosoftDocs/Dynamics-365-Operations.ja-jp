---
title: ロゴの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797602"
---
# <a name="add-a-logo"></a><span data-ttu-id="05acf-103">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="05acf-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05acf-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="05acf-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="05acf-105">サイトの構築時には、まず最初に会社またはブランド ロゴをサイトのヘッダーに追加するのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="05acf-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="05acf-106">Dynamics 365 Commerce オンライン モジュール ライブラリでは、このタスクを簡単にするためのモジュールが提供されます。</span><span class="sxs-lookup"><span data-stu-id="05acf-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="05acf-107">テンプレート、レイアウト、またはページに、ロゴを直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="05acf-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="05acf-108">この方法により、特定のページまたはページ グループに表示されるロゴを簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="05acf-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="05acf-109">ただし、このトピックでは、サイトのすべてのページで再利用できるヘッダー フラグメントにロゴを追加する最もよくあるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="05acf-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="05acf-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="05acf-110">Prerequisites</span></span>

<span data-ttu-id="05acf-111">サイトのすべてのページにロゴを追加する前に、これらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05acf-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="05acf-112">ロゴをメディア ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="05acf-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="05acf-113">ヘッダー フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="05acf-113">Create a header fragment.</span></span> <span data-ttu-id="05acf-114">フラグメントの作成および使用方法の詳細については、[フラグメントの使用](work-with-fragments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05acf-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="05acf-115">サイトのページがレイアウトやモジュール オプションとして使用するヘッダー フラグメントをテンプレートに含めます。</span><span class="sxs-lookup"><span data-stu-id="05acf-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="05acf-116">テンプレートの詳細については、[テンプレートの使用](work-with-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05acf-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="05acf-117">ヘッダー フラグメントへのロゴの追加</span><span class="sxs-lookup"><span data-stu-id="05acf-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="05acf-118">サイトのヘッダー フラグメントにロゴを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="05acf-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="05acf-119">左のナビゲーション ウィンドウで、**フラグメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05acf-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="05acf-120">作成したヘッダー フラグメントを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05acf-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="05acf-121">ヘッダー モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="05acf-121">Expand the header module.</span></span>
1. <span data-ttu-id="05acf-122">ヘッダー モジュールのプロパティ ウィンドウで、ロゴの画像とリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="05acf-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="05acf-123">ヘッダー フラグメントを保存し、編集を終了して、公開します。</span><span class="sxs-lookup"><span data-stu-id="05acf-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="05acf-124">更新されたヘッダー フラグメントを公開すると、ヘッダー フラグメントを含むテンプレートを使用するすべてのサイト ページにロゴが表示されます。</span><span class="sxs-lookup"><span data-stu-id="05acf-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05acf-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="05acf-125">Additional resources</span></span>

[<span data-ttu-id="05acf-126">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="05acf-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="05acf-127">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="05acf-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="05acf-128">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="05acf-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="05acf-129">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="05acf-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="05acf-130">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="05acf-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="05acf-131">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="05acf-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="05acf-132">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="05acf-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
