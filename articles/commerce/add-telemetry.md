---
title: サイト ページにスクリプト コードを追加してテレメトリをサポートする
description: このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797434"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="96c20-103">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="96c20-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96c20-104">このトピックでは、クライアント側のテレメトリの収集をサポートするクライアント側のスクリプト コードをサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="96c20-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="96c20-105">Web Analytics は、顧客がサイトとどのように対話するかを理解し、最大のコンバージョンのためにエクスペリエンスを最適化するのに役立つ決定を下したい場合に、重要なツールとなります。</span><span class="sxs-lookup"><span data-stu-id="96c20-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="96c20-106">Google Analytics、Clicky、Moz Analytics、KISSMetrics など、これらの目標を達成するために、多くの Web Analytics パッケージが用意されています。</span><span class="sxs-lookup"><span data-stu-id="96c20-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="96c20-107">ほとんどの Web Analytics パッケージでは、サイトのすべてのページの HTML の **\<head\>** 要素にクライアント側のスクリプト コードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96c20-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="96c20-108">このトピックの手順は、Microsoft Dynamics 365 Commerce がネイティブに提供していない他のカスタム クライアント側機能にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="96c20-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="96c20-109">スクリプ トコードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="96c20-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="96c20-110">フラグメントを使用すると、使用するテンプレートに関係なく、サイト上のすべてのページでインラインまたは外部スクリプト コードを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="96c20-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="96c20-111">インライン スクリプト コードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="96c20-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="96c20-112">サイト ビルダーのインライン スクリプト コードに再利用可能なフラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96c20-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="96c20-113">**フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="96c20-114">**新規フラグメント** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="96c20-115">**フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="96c20-116">作成したフラグメントで、**既定のインライン スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="96c20-117">右側のプロパティウィンドウの **インライン スクリプト** で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="96c20-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="96c20-118">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="96c20-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="96c20-119">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96c20-120">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="96c20-121">外部スクリプト コードに再利用可能なフラグメントを作成する</span><span class="sxs-lookup"><span data-stu-id="96c20-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="96c20-122">サイト ビルダーの外部スクリプト コードに再利用可能なフラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96c20-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="96c20-123">**フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="96c20-124">**新規フラグメント** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="96c20-125">**フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="96c20-126">作成したフラグメントで、**既定の外部スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="96c20-127">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="96c20-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="96c20-128">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="96c20-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="96c20-129">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96c20-130">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="96c20-131">サイトのコンテンツ セキュリティ ポリシー (CSP) が有効になっている場合は、すべての外部 URL が Commerce サイト ビルダーの **script-src** CSP ディレクティブに追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="96c20-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="96c20-132">詳細については、[コンテンツ セキュリティ  ポリシー (CSP) の管理](manage-csp.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96c20-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="96c20-133">スクリプト コードを含むフラグメントをテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="96c20-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="96c20-134">サイト ビルダーのテンプレートにスクリプト コードを含むフラグメントを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96c20-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="96c20-135">**テンプレート** に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="96c20-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="96c20-136">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="96c20-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="96c20-137">**HTML Head** スロットの省略ボタン (**...**) を選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="96c20-138">スクリプト コードに対して作成したフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="96c20-139">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96c20-140">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="96c20-141">外部スクリプトまたはインライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="96c20-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="96c20-142">単一のテンプレートによって制御される一連のページにインラインまたは外部スクリプトを直接挿入する場合は、最初にフラグメントを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="96c20-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="96c20-143">インライン スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="96c20-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="96c20-144">サイト ビルダーのテンプレートにインライン スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96c20-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="96c20-145">**テンプレート** に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="96c20-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="96c20-146">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="96c20-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="96c20-147">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96c20-148">**モジュールの追加** ダイアログ ボックスで、**インライン スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="96c20-149">右側のプロパティウィンドウの **インライン スクリプト** で、クライアント サイド スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="96c20-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="96c20-150">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="96c20-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="96c20-151">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96c20-152">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="96c20-153">外部スクリプトを直接テンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="96c20-153">Add an external script directly to a template</span></span>

<span data-ttu-id="96c20-154">サイト ビルダーのテンプレートに外部スクリプトを直接追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="96c20-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="96c20-155">**テンプレート** に移動して、スクリプト コードを追加するページのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="96c20-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="96c20-156">左ウィンドウでテンプレート階層を展開し、**HTML ヘッド** スロットを表示します。</span><span class="sxs-lookup"><span data-stu-id="96c20-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="96c20-157">**HTML Head** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="96c20-158">**モジュールの追加** ダイアログ ボックスで、**外部スクリプト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="96c20-159">右側のプロパティウィンドウの **スクリプト ソース** で、外部スクリプト ソースの外部または相対 URL を追加します。</span><span class="sxs-lookup"><span data-stu-id="96c20-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="96c20-160">次に、必要に応じて他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="96c20-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="96c20-161">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="96c20-162">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96c20-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96c20-163">追加リソース</span><span class="sxs-lookup"><span data-stu-id="96c20-163">Additional resources</span></span>

[<span data-ttu-id="96c20-164">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="96c20-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="96c20-165">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="96c20-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="96c20-166">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="96c20-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="96c20-167">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="96c20-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="96c20-168">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="96c20-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="96c20-169">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="96c20-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="96c20-170">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="96c20-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
