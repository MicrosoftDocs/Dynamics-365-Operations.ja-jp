---
title: サイト ページにスクリプト コードを追加してテレメトリをサポートする
description: このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154089"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="b2ea0-103">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="b2ea0-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2ea0-104">このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="b2ea0-105">概要</span><span class="sxs-lookup"><span data-stu-id="b2ea0-105">Overview</span></span>

<span data-ttu-id="b2ea0-106">Web Analytics は、顧客がサイトとどのように対話するかを理解し、最大のコンバージョンのためにエクスペリエンスを最適化するのに役立つ決定を下したい場合に、重要なツールとなります。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="b2ea0-107">Google Analytics、Clicky、Moz Analytics、KISSMetrics など、これらの目標を達成するために、多くの Web Analytics パッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="b2ea0-108">ほとんどの Web Analytics パッケージでは、サイトのすべてのページの HTML の **\<head\>** 要素にクライアント側のスクリプト コードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="b2ea0-109">このトピックの手順は、Microsoft Dynamics 365 Commerce がネイティブに提供していない他のカスタム クライアント側機能にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="b2ea0-110">スクリプト コードに再利用可能なページ フラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="b2ea0-111">ページ フラグメントを使用すると、使用するテンプレートに関係なく、サイト上のすべてのページでインラインまたは外部スクリプト コードを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="b2ea0-112">インライン スクリプト コードに再利用可能なページ フラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="b2ea0-113">サイト ビルダーのインライン スクリプト コードに再利用可能なページ フラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2ea0-114">**ページ フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b2ea0-115">**新規ページ フラグメント** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b2ea0-116">**ページ フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b2ea0-117">作成したページ フラグメントで、**既定のインライン スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="b2ea0-118">右側のプロパティウィンドウの **インライン スクリプト**で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b2ea0-119">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2ea0-120">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2ea0-121">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="b2ea0-122">外部スクリプト コードに再利用可能なページ フラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="b2ea0-123">サイト ビルダーの外部スクリプト コードに再利用可能なページ フラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2ea0-124">**ページ フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="b2ea0-125">**新規ページ フラグメント** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b2ea0-126">**ページ フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b2ea0-127">作成したページ フラグメントで、**既定の外部スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="b2ea0-128">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b2ea0-129">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2ea0-130">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2ea0-131">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="b2ea0-132">スクリプト コードを含むページ フラグメントをテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="b2ea0-133">サイト ビルダーのテンプレートにスクリプト コードを含むページ フラグメントを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2ea0-134">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2ea0-135">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2ea0-136">**HTML Head** スロットの省略ボタン (**...**) を選択し、**ページ フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="b2ea0-137">スクリプト コードに対して作成したフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="b2ea0-138">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2ea0-139">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="b2ea0-140">外部スクリプトまたはインライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="b2ea0-141">単一のテンプレートによって制御される一連のページにインラインまたは外部スクリプトを直接挿入する場合は、最初にページ フラグメントを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="b2ea0-142">インライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="b2ea0-143">サイト ビルダーのテンプレートにインライン スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2ea0-144">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2ea0-145">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2ea0-146">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2ea0-147">**モジュールの追加** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="b2ea0-148">右側のプロパティウィンドウの **インライン スクリプト**で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="b2ea0-149">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2ea0-150">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2ea0-151">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="b2ea0-152">外部スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-152">Add an external script directly to a template</span></span>

<span data-ttu-id="b2ea0-153">サイト ビルダーのテンプレートに外部スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b2ea0-154">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="b2ea0-155">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="b2ea0-156">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b2ea0-157">**モジュールの追加** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="b2ea0-158">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="b2ea0-159">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="b2ea0-160">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="b2ea0-161">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2ea0-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b2ea0-162">Additional resources</span></span>

[<span data-ttu-id="b2ea0-163">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="b2ea0-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b2ea0-164">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="b2ea0-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b2ea0-165">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="b2ea0-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b2ea0-166">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="b2ea0-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b2ea0-167">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="b2ea0-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b2ea0-168">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="b2ea0-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b2ea0-169">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="b2ea0-169">Add languages to your site</span></span>](add-languages-to-site.md)
