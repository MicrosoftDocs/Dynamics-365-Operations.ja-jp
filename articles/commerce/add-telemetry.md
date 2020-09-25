---
title: サイト ページにスクリプト コードを追加してテレメトリをサポートする
description: このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761252"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="0fad3-103">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="0fad3-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fad3-104">このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="0fad3-105">概要</span><span class="sxs-lookup"><span data-stu-id="0fad3-105">Overview</span></span>

<span data-ttu-id="0fad3-106">Web Analytics は、顧客がサイトとどのように対話するかを理解し、最大のコンバージョンのためにエクスペリエンスを最適化するのに役立つ決定を下したい場合に、重要なツールとなります。</span><span class="sxs-lookup"><span data-stu-id="0fad3-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="0fad3-107">Google Analytics、Clicky、Moz Analytics、KISSMetrics など、これらの目標を達成するために、多くの Web Analytics パッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0fad3-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="0fad3-108">ほとんどの Web Analytics パッケージでは、サイトのすべてのページの HTML の **\<head\>** 要素にクライアント側のスクリプト コードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fad3-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="0fad3-109">このトピックの手順は、Microsoft Dynamics 365 Commerce がネイティブに提供していない他のカスタム クライアント側機能にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="0fad3-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="0fad3-110">スクリプ トコードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="0fad3-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="0fad3-111">フラグメントを使用すると、使用するテンプレートに関係なく、サイト上のすべてのページでインラインまたは外部スクリプト コードを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="0fad3-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="0fad3-112">インライン スクリプト コードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="0fad3-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="0fad3-113">サイト ビルダーのインライン スクリプト コードに再利用可能なフラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0fad3-114">**フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="0fad3-115">**新規フラグメント** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="0fad3-116">**フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0fad3-117">作成したフラグメントで、**既定のインライン スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="0fad3-118">右側のプロパティウィンドウの **インライン スクリプト**で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="0fad3-119">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="0fad3-120">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0fad3-121">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="0fad3-122">外部スクリプト コードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="0fad3-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="0fad3-123">サイト ビルダーの外部スクリプト コードに再利用可能なフラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0fad3-124">**フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="0fad3-125">**新規フラグメント** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="0fad3-126">**フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0fad3-127">作成したフラグメントで、**既定の外部スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="0fad3-128">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="0fad3-129">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="0fad3-130">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0fad3-131">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="0fad3-132">スクリプト コードを含むフラグメントをテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="0fad3-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="0fad3-133">サイト ビルダーのテンプレートにスクリプト コードを含むフラグメントを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0fad3-134">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="0fad3-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="0fad3-135">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="0fad3-136">**HTML Head** スロットの省略ボタン (**...**) を選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="0fad3-137">スクリプト コードに対して作成したフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="0fad3-138">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0fad3-139">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="0fad3-140">外部スクリプトまたはインライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="0fad3-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="0fad3-141">単一のテンプレートによって制御される一連のページにインラインまたは外部スクリプトを直接挿入する場合は、最初にフラグメントを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0fad3-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="0fad3-142">インライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="0fad3-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="0fad3-143">サイト ビルダーのテンプレートにインライン スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0fad3-144">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="0fad3-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="0fad3-145">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="0fad3-146">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0fad3-147">**モジュールの追加** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="0fad3-148">右側のプロパティウィンドウの **インライン スクリプト**で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="0fad3-149">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="0fad3-150">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0fad3-151">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="0fad3-152">外部スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="0fad3-152">Add an external script directly to a template</span></span>

<span data-ttu-id="0fad3-153">サイト ビルダーのテンプレートに外部スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0fad3-154">**テンプレート**に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="0fad3-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="0fad3-155">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="0fad3-156">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0fad3-157">**モジュールの追加** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="0fad3-158">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="0fad3-159">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="0fad3-160">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0fad3-161">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0fad3-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fad3-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0fad3-162">Additional resources</span></span>

[<span data-ttu-id="0fad3-163">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="0fad3-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0fad3-164">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="0fad3-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0fad3-165">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="0fad3-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0fad3-166">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="0fad3-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0fad3-167">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="0fad3-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0fad3-168">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="0fad3-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0fad3-169">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="0fad3-169">Add languages to your site</span></span>](add-languages-to-site.md)
