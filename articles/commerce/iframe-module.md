---
title: IFRAME​​ モジュール
description: このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646981"
---
# <a name="iframe-module"></a><span data-ttu-id="74148-103">IFRAME​​ モジュール</span><span class="sxs-lookup"><span data-stu-id="74148-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="74148-104">このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="74148-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74148-105">概要</span><span class="sxs-lookup"><span data-stu-id="74148-105">Overview</span></span>

<span data-ttu-id="74148-106">iframe モジュールは、サイトの外部コンテンツをホストする iframe (インライン フレーム) を提供します。</span><span class="sxs-lookup"><span data-stu-id="74148-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="74148-107">たとえば、どのサイトのページでも YouTube の動画や PDF ファイル ビューアをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="74148-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="74148-108">iframe モジュールにはターゲットの URL が必要となります。</span><span class="sxs-lookup"><span data-stu-id="74148-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="74148-109">そして、HTML の **iframe** 要素の中にターゲット ページのコンテンツをホストします。</span><span class="sxs-lookup"><span data-stu-id="74148-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="74148-110">外部 URL は、サイトのコンテンツ セキュリティポリシー (CSP) の指示に従って、許可リスト (「ホワイトリスト」とも呼ばれます) に登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="74148-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="74148-111">iframe のコンテンツでは、**frame-ancestor** のディレクティブを使用して URL を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74148-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="74148-112">詳細については、[コンテンツ セキュリティ  ポリシー (CSP) の管理](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74148-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="74148-113">以下の画像は、サイトページに外部動画を表示する iframe モジュールの例です。</span><span class="sxs-lookup"><span data-stu-id="74148-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![外部動画を表示する iframe モジュールの例](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="74148-115">iframe モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="74148-115">Iframe module properties</span></span>

| <span data-ttu-id="74148-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="74148-116">Property name</span></span>             | <span data-ttu-id="74148-117">先頭値</span><span class="sxs-lookup"><span data-stu-id="74148-117">Value</span></span>                 | <span data-ttu-id="74148-118">説明</span><span class="sxs-lookup"><span data-stu-id="74148-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="74148-119">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="74148-119">Heading</span></span> | <span data-ttu-id="74148-120">テキスト</span><span class="sxs-lookup"><span data-stu-id="74148-120">Text</span></span> | <span data-ttu-id="74148-121">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="74148-121">The heading for the module.</span></span> |
| <span data-ttu-id="74148-122">ターゲット URL</span><span class="sxs-lookup"><span data-stu-id="74148-122">Target URL</span></span> | <span data-ttu-id="74148-123">URL</span><span class="sxs-lookup"><span data-stu-id="74148-123">URL</span></span> | <span data-ttu-id="74148-124">モジュール内でホストされている URL。</span><span class="sxs-lookup"><span data-stu-id="74148-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="74148-125">Height</span><span class="sxs-lookup"><span data-stu-id="74148-125">Height</span></span> | <span data-ttu-id="74148-126">数値またはパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="74148-126">Number or percentage</span></span> | <span data-ttu-id="74148-127">モジュールの高さをピクセル、パーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="74148-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="74148-128">たとえば、値が **100** の場合はピクセル数として扱われ、値が **100%** の場合はパーセンテージとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="74148-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="74148-129">aria ラベル</span><span class="sxs-lookup"><span data-stu-id="74148-129">Aria label</span></span> | <span data-ttu-id="74148-130">テキスト</span><span class="sxs-lookup"><span data-stu-id="74148-130">Text</span></span> | <span data-ttu-id="74148-131">アクセシビリティを実現する目的で、Accessible Rich Internet Applications (ARIA) ラベルを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="74148-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="74148-132">iFrame モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="74148-132">Add an iframe module to a page</span></span>

<span data-ttu-id="74148-133">iframe モジュールをページに追加して外部動画を表示するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="74148-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="74148-134">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="74148-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="74148-135">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="74148-136">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="74148-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="74148-137">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="74148-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="74148-138">**テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="74148-139">**ページ名**配下で、**マーケティング ページ**と入力し、**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="74148-140">新規ページの**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74148-141">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74148-142">モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="74148-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="74148-143">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="74148-144">**モジュールの追加**ダイアログ ボックスで、**iframe**モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="74148-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="74148-145">モジュールのプロパティ ペインで、動画に使用する外部 URL を**ターゲット URL** に設定します。</span><span class="sxs-lookup"><span data-stu-id="74148-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="74148-146">必要に応じて、 **ヘッダー** や **高さ** などのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74148-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="74148-147">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="74148-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="74148-148">ご利用のサイトのマーケティング ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="74148-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="74148-149">動画が iframe モジュールでレンダリングされていることが確認できます。</span><span class="sxs-lookup"><span data-stu-id="74148-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="74148-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="74148-150">Additional resources</span></span>

[<span data-ttu-id="74148-151">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="74148-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="74148-152">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="74148-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
