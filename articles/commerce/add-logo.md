---
title: ロゴの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914625"
---
# <a name="add-a-logo"></a><span data-ttu-id="9945b-103">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="9945b-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9945b-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9945b-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9945b-105">概要</span><span class="sxs-lookup"><span data-stu-id="9945b-105">Overview</span></span>

<span data-ttu-id="9945b-106">サイトの構築時には、まず最初に会社またはブランド ロゴをサイトのヘッダーに追加するのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="9945b-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="9945b-107">Dynamics 365 Commerce オンライン スタート キットでは、このタスクを簡単にするためのモジュールが提供されます。</span><span class="sxs-lookup"><span data-stu-id="9945b-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="9945b-108">テンプレート、レイアウト、またはページに、ロゴを直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="9945b-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="9945b-109">この方法により、特定のページまたはページ グループに表示されるロゴを簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="9945b-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="9945b-110">ただし、このトピックでは、サイトのすべてのページで再利用できるヘッダー フラグメントにロゴを追加する最もよくあるシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9945b-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9945b-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="9945b-111">Prerequisites</span></span>

<span data-ttu-id="9945b-112">サイトのすべてのページにロゴを追加する前に、これらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9945b-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="9945b-113">**資産**ページからアクセスできるデジタル資産マネージャーにロゴをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="9945b-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="9945b-114">ヘッダー フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="9945b-114">Create a header fragment.</span></span> <span data-ttu-id="9945b-115">フラグメントの作成および使用方法の詳細については、[フラグメントの使用](work-with-fragments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9945b-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="9945b-116">サイトのページがレイアウトやモジュール オプションとして使用するヘッダー フラグメントをテンプレートに含めます。</span><span class="sxs-lookup"><span data-stu-id="9945b-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="9945b-117">テンプレートの詳細については、[テンプレートの使用](work-with-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9945b-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="9945b-118">ヘッダー フラグメントへのロゴの追加</span><span class="sxs-lookup"><span data-stu-id="9945b-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="9945b-119">サイトのヘッダー フラグメントにロゴを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9945b-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="9945b-120">左側のナビゲーション ウィンドウで**フラグメント**を選択し、作成したヘッダー フラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="9945b-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="9945b-121">**チェック アウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9945b-121">Select **Check out**.</span></span>
3. <span data-ttu-id="9945b-122">**ヘッダー** スロットおよび**ロゴ** スロットを展開します。</span><span class="sxs-lookup"><span data-stu-id="9945b-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="9945b-123">**ロゴ** スロットの省略ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9945b-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="9945b-124">ロゴ モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9945b-124">Select the logo module.</span></span>
6. <span data-ttu-id="9945b-125">右側のプロパティ ウィンドウで、ロゴ モジュールをコンフィギュレーションしてロゴが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="9945b-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="9945b-126">ヘッダー フラグメントを保存し、チェック イン後に公開します。</span><span class="sxs-lookup"><span data-stu-id="9945b-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="9945b-127">更新されたヘッダー フラグメントを公開すると、ヘッダー フラグメントを含むテンプレートを使用するすべてのサイト ページにロゴが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9945b-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9945b-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9945b-128">Additional resources</span></span>

[<span data-ttu-id="9945b-129">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="9945b-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="9945b-130">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="9945b-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="9945b-131">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="9945b-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="9945b-132">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="9945b-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="9945b-133">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="9945b-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="9945b-134">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="9945b-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="9945b-135">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="9945b-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

