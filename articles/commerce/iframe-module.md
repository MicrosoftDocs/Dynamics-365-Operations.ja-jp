---
title: IFRAME​​ モジュール
description: このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665399"
---
# <a name="iframe-module"></a><span data-ttu-id="5b03f-103">IFRAME​​ モジュール</span><span class="sxs-lookup"><span data-stu-id="5b03f-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b03f-104">このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5b03f-105">概要</span><span class="sxs-lookup"><span data-stu-id="5b03f-105">Overview</span></span>

<span data-ttu-id="5b03f-106">iframe モジュールは、サイトの外部コンテンツをホストする iframe (インライン フレーム) を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="5b03f-107">たとえば、どのサイトのページでも YouTube の動画や PDF ファイル ビューアをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="5b03f-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="5b03f-108">iframe モジュールにはターゲットの URL が必要となります。</span><span class="sxs-lookup"><span data-stu-id="5b03f-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="5b03f-109">そして、HTML の **iframe** 要素の中にターゲット ページのコンテンツをホストします。</span><span class="sxs-lookup"><span data-stu-id="5b03f-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="5b03f-110">外部 URL は、サイトのコンテンツ セキュリティポリシー (CSP) の指示に従って、許可リストに登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b03f-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="5b03f-111">iframe のコンテンツでは、**frame-ancestor** のディレクティブを使用して URL を許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b03f-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="5b03f-112">詳細については、[コンテンツ セキュリティ  ポリシー (CSP) の管理](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b03f-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5b03f-113">iFrame モジュールは、Dynamics 365 Commerce 10.0.13 リリースで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="5b03f-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="5b03f-114">以下の画像は、サイトページに外部動画を表示する iframe モジュールの例です。</span><span class="sxs-lookup"><span data-stu-id="5b03f-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![外部動画を表示する iframe モジュールの例](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="5b03f-116">iframe モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="5b03f-116">Iframe module properties</span></span>

| <span data-ttu-id="5b03f-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5b03f-117">Property name</span></span>             | <span data-ttu-id="5b03f-118">先頭値</span><span class="sxs-lookup"><span data-stu-id="5b03f-118">Value</span></span>                 | <span data-ttu-id="5b03f-119">説明</span><span class="sxs-lookup"><span data-stu-id="5b03f-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5b03f-120">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5b03f-120">Heading</span></span> | <span data-ttu-id="5b03f-121">テキスト</span><span class="sxs-lookup"><span data-stu-id="5b03f-121">Text</span></span> | <span data-ttu-id="5b03f-122">モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="5b03f-122">The heading for the module.</span></span> |
| <span data-ttu-id="5b03f-123">ターゲット URL</span><span class="sxs-lookup"><span data-stu-id="5b03f-123">Target URL</span></span> | <span data-ttu-id="5b03f-124">URL</span><span class="sxs-lookup"><span data-stu-id="5b03f-124">URL</span></span> | <span data-ttu-id="5b03f-125">モジュール内でホストされている URL。</span><span class="sxs-lookup"><span data-stu-id="5b03f-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="5b03f-126">Height</span><span class="sxs-lookup"><span data-stu-id="5b03f-126">Height</span></span> | <span data-ttu-id="5b03f-127">数値またはパーセンテージ</span><span class="sxs-lookup"><span data-stu-id="5b03f-127">Number or percentage</span></span> | <span data-ttu-id="5b03f-128">モジュールの高さをピクセル、パーセンテージで指定します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="5b03f-129">たとえば、値が **100** の場合はピクセル数として扱われ、値が **100%** の場合はパーセンテージとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="5b03f-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="5b03f-130">aria ラベル</span><span class="sxs-lookup"><span data-stu-id="5b03f-130">Aria label</span></span> | <span data-ttu-id="5b03f-131">テキスト</span><span class="sxs-lookup"><span data-stu-id="5b03f-131">Text</span></span> | <span data-ttu-id="5b03f-132">アクセシビリティを実現する目的で、Accessible Rich Internet Applications (ARIA) ラベルを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="5b03f-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="5b03f-133">iFrame モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="5b03f-133">Add an iframe module to a page</span></span>

<span data-ttu-id="5b03f-134">iframe モジュールをページに追加して外部動画を表示するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="5b03f-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="5b03f-135">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="5b03f-136">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="5b03f-137">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="5b03f-138">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="5b03f-139">**テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="5b03f-140">**ページ名** 配下で、**マーケティング ページ** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="5b03f-141">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5b03f-142">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5b03f-143">モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="5b03f-144">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5b03f-145">**モジュールの追加** ダイアログ ボックスで、**iframe** モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5b03f-146">モジュールのプロパティ ペインで、動画に使用する外部 URL を **ターゲット URL** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="5b03f-147">必要に応じて、 **ヘッダー** や **高さ** などのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="5b03f-148">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="5b03f-149">ご利用のサイトのマーケティング ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="5b03f-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="5b03f-150">動画が iframe モジュールでレンダリングされていることが確認できます。</span><span class="sxs-lookup"><span data-stu-id="5b03f-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="5b03f-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5b03f-151">Additional resources</span></span>

[<span data-ttu-id="5b03f-152">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="5b03f-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5b03f-153">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="5b03f-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
