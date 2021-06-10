---
title: Dynamics 365 Commerce での Microsoft Clarity の設定
description: このトピックでは、Dynamics 365 Commerce 環境内で Microsoft Clarity を設定する方法について説明します。
author: BrianShook
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-25
ms.dyn365.ops.version: ''
ms.openlocfilehash: 942805812d1951dae04c81d0ec380b07232f3ea3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018568"
---
# <a name="set-up-microsoft-clarity-in-dynamics-365-commerce"></a><span data-ttu-id="1bce2-103">Dynamics 365 Commerce での Microsoft Clarity の設定</span><span class="sxs-lookup"><span data-stu-id="1bce2-103">Set up Microsoft Clarity in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1bce2-104">このトピックでは、Dynamics 365 Commerce 環境内で Microsoft Clarity を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-104">This topic covers how to set up Microsoft Clarity in your Dynamics 365 Commerce environment.</span></span> 

<span data-ttu-id="1bce2-105">[Microsoft Clarity](https://clarity.microsoft.com/) は、サイト所有者が自分の e コマース サイトとのユーザー操作を理解するのに役立つユーザー動作分析ツールです。</span><span class="sxs-lookup"><span data-stu-id="1bce2-105">[Microsoft Clarity](https://clarity.microsoft.com/) is a user behavior analytics tool that can help site owners understand user interactions with their e-commerce sites.</span></span> <span data-ttu-id="1bce2-106">Clarity の分析ツールは、セッション記録、ヒートマップ、および機械学習情報を使用して可視性を実現し、ユーザー操作を確認及び調査します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-106">Clarity's analysis tools enable visibility using session recordings, heatmaps, and machine learning insights to review and study user interactions.</span></span> 

<span data-ttu-id="1bce2-107">Clarity を Dynamics 365 Commerce サイトに統合するのは簡単です。このトピックの手順に従うだけで、Clarity がユーザー操作を詳細に確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-107">Integrating Clarity into your Dynamics 365 Commerce site is easy, just follow the steps in this topic to enable Clarity to provide you with an in-depth look at your user interactions.</span></span>

## <a name="sign-up-for-clarity"></a><span data-ttu-id="1bce2-108">Clarity にサインアップします</span><span class="sxs-lookup"><span data-stu-id="1bce2-108">Sign up for Clarity</span></span>

<span data-ttu-id="1bce2-109">Clarity にサインアップするには、[Clarity](https://clarity.microsoft.com/) Web サイトに移動して **開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-109">To sign up for Clarity, go to the [Clarity](https://clarity.microsoft.com/) website and select **Get started**.</span></span> <span data-ttu-id="1bce2-110">設定プロセス中に、Commerce サイトに関連付けられた実稼働環境ドメイン URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-110">During the setup process, use the live production domain URL associated with your Commerce site.</span></span> <span data-ttu-id="1bce2-111">Clarity 設定の詳細については、[はじめに](https://docs.microsoft.com/clarity/getting-started) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1bce2-111">For additional details about Clarity setup, see [Getting started](https://docs.microsoft.com/clarity/getting-started).</span></span>

## <a name="integrate-clarity-with-your-commerce-site"></a><span data-ttu-id="1bce2-112">Clarity を Commerce のサイトに統合する</span><span class="sxs-lookup"><span data-stu-id="1bce2-112">Integrate Clarity with your Commerce site</span></span>

<span data-ttu-id="1bce2-113">Clarity にサインアップした後、Commerce のサイト ビルダで次の手順に従って、Clarity を e コマース サイトに統合します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-113">After you have signed up for Clarity, follow these steps in Commerce site builder to integrate Clarity with your e-commerce site.</span></span>

### <a name="configure-content-security-policy-for-clarity"></a><span data-ttu-id="1bce2-114">Clarity のコンテンツ セキュリティ ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="1bce2-114">Configure Content Security Policy for Clarity</span></span>

<span data-ttu-id="1bce2-115">コンテンツ セキュリティ ポリシー (CSP) は、サイトページの読み込みが許可されているリソースを制御するのに役立つ広範なポリシー ディレクティブのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-115">Content Security Policy (CSP) provides an extensive set of policy directives that help you control the resources that a site page is allowed to load.</span></span> <span data-ttu-id="1bce2-116">各ディレクティブは、特定のタイプのリソースに対する制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-116">Each directive defines the restrictions for a specific type of resource.</span></span> <span data-ttu-id="1bce2-117">Clarity をサイトで機能させるには、Clarity リソースを呼び出すことができるように一部の CSP ディレクティブを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-117">For Clarity to function on your site, some CSP directives must be configured to allow Clarity resources to be called.</span></span> 

<span data-ttu-id="1bce2-118">Commerce サイト ビルダーで Clarity を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1bce2-118">To configure CSP for Clarity in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1bce2-119">Commerce サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-119">Navigate to your Commerce site.</span></span>
1. <span data-ttu-id="1bce2-120">**サイト 設定 \> 拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-120">Select **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="1bce2-121">**コンテンツ セキュリティ ポリシー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-121">Select the **Content security policy** tab.</span></span>
1. <span data-ttu-id="1bce2-122">**child-src** ディレクティブ セクションで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-122">In the **child-src** directive section, select **Add**.</span></span>
1. <span data-ttu-id="1bce2-123">**``https://www.clarity.ms``** を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-123">Enter **``https://www.clarity.ms``**.</span></span>
1. <span data-ttu-id="1bce2-124">**connect-src** および **script-src** ディレクティブについて、手順 4 と 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-124">Repeat steps 4 and 5 for the **connect-src** and **script-src** directives.</span></span>
1. <span data-ttu-id="1bce2-125">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-125">Select **Save and Publish**.</span></span>

### <a name="add-clarity-to-the-correlation-header-excluded-domains-allow-list"></a><span data-ttu-id="1bce2-126">除外ドメイン許可リストの相関ヘッダーに Clarity を追加</span><span class="sxs-lookup"><span data-stu-id="1bce2-126">Add Clarity to the correlation header excluded domains allow list</span></span>

<span data-ttu-id="1bce2-127">Clarity をサイトで機能させるには、Clarity ドメインを **相関ヘッダー除外ドメイン** 許可リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-127">For Clarity to function on your site, you'll need to add the Clarity domain to the **Correlation header excluded domains** allow list.</span></span> 

<span data-ttu-id="1bce2-128">Commerce サイト ビルダーの相関ヘッダー除外ドメインリストに Clarity を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1bce2-128">To add Clarity to the correlation header excluded domains list in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1bce2-129">Commerce サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-129">Navigate to your Commerce site.</span></span>
1. <span data-ttu-id="1bce2-130">**サイト 設定 > 拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-130">Select **Site Settings > Extensions**.</span></span>
1. <span data-ttu-id="1bce2-131">**構成** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-131">Select the **Configuration** tab.</span></span>
1. <span data-ttu-id="1bce2-132">**相関ヘッダー除外ドメイン** セクションで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-132">In the **Correlation header excluded domains** section, select **Add**.</span></span>
1. <span data-ttu-id="1bce2-133">**\*.clarity.ms** を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-133">Enter **\*.clarity.ms**.</span></span>
1. <span data-ttu-id="1bce2-134">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-134">Select **Save and Publish**.</span></span>

### <a name="embed-clarity-tracking-script-code-into-site-pages"></a><span data-ttu-id="1bce2-135">Clarity トラッキング スクリプト コードをサイト ページに埋め込む</span><span class="sxs-lookup"><span data-stu-id="1bce2-135">Embed Clarity tracking script code into site pages</span></span>

<span data-ttu-id="1bce2-136">Clarity で追跡する Commerce サイト ページに、Clarity 追跡スクリプト コードを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="1bce2-136">You can embed Clarity tracking script code into any Commerce site page that you want to track with Clarity.</span></span>

<span data-ttu-id="1bce2-137">開始するには、Clarity ポータルからプロジェクトの追跡スクリプト コードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="1bce2-137">To get started, copy the tracking script code for your project from the Clarity portal.</span></span> <span data-ttu-id="1bce2-138">次に、Clarity 追跡スクリプト コードを Commerce モジュール ライブラリ *インライン スクリプト モジュール* に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-138">The Clarity tracking script code will then need to be added to a Commerce module library *inline script module*.</span></span> <span data-ttu-id="1bce2-139">構成によっては、インライン スクリプト モジュールを特定のサイト ページに直接追加することも、サイト ページのテンプレートで許可されるオプションとして追加する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-139">Depending on your configuration, the inline script module may be added directly to a specific site page, or may be required to be added as an allowable option in a site page template.</span></span> 

> [!NOTE]
> <span data-ttu-id="1bce2-140">Clarity 追跡スクリプト コードをインライン スクリプト モジュールにコピーする時に、文字列から周囲の **\<script\>** タグを削除できます。</span><span class="sxs-lookup"><span data-stu-id="1bce2-140">When copying the Clarity tracking script code to the inline script module, you can remove the surrounding **\<script\>** tags from the string.</span></span> <span data-ttu-id="1bce2-141">インライン スクリプト モジュールは、ページまたはフラグメントが公開および表示されるときに、必要な **\<script\>** タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-141">The inline script module will add the necessary **\<script\>** tags when the page or fragment is published and rendered.</span></span>

<span data-ttu-id="1bce2-142">サイト ページの範囲に Clarity 追跡スクリプト コードを含めるのが最も効率的な方法は、共有サイト ページ テンプレートにスクリプト コードを埋め込む方法です。</span><span class="sxs-lookup"><span data-stu-id="1bce2-142">The most efficient way to include Clarity tracking script code to a range of site pages is to embed the script code in a shared site page template.</span></span> <span data-ttu-id="1bce2-143">次の手順では、サイト ページ テンプレートで使用するインライン スクリプト モジュールを含むフラグメントに Clarity スクリプト コードを挿入する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-143">The following procedure describes how to insert Clarity script code into a fragment containing an inline script module that is then used by a site page template.</span></span> 

<span data-ttu-id="1bce2-144">Clarity 追跡コードを Commerce サイト ビルダーのサイト ページに埋め込むには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1bce2-144">To embed the Clarity tracking code into site pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1bce2-145">Commerce サイト ビルダーでサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-145">Go to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="1bce2-146">**フラグメント** を選択し、**新規** を選択します</span><span class="sxs-lookup"><span data-stu-id="1bce2-146">Select **Fragments**, and then select **New**</span></span>
1. <span data-ttu-id="1bce2-147">**新規フラグメント** ダイアログ ボックスで、**インライン スクリプト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-147">In the **New fragment** dialog box, select the **Inline script** module.</span></span>
1. <span data-ttu-id="1bce2-148">**フラグメント名** に名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-148">For **Fragment name**, enter a name, and then select **OK**.</span></span>
1. <span data-ttu-id="1bce2-149">**既定のインライン スクリプト** モジュール スロットを選択し、モジュールのプロパティ ペインで、**インライン スクリプト** の下の Clarity スクリプトに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="1bce2-149">Select the **Default inline script** module slot, and then in the module property pane, under **Inline script** paste in the Clarity script.</span></span> <span data-ttu-id="1bce2-150">スクリプト文字列をコピーした場合は、周囲の **\<script\>** タグを必ず削除してください。</span><span class="sxs-lookup"><span data-stu-id="1bce2-150">Be sure to remove the surrounding **\<script\>** tags if you copied the script string.</span></span>
1. <span data-ttu-id="1bce2-151">**保存** を選択してから、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-151">Select **Save**, and then select **Publish**.</span></span>
1. <span data-ttu-id="1bce2-152">**テンプレート** を選択し、Clarity スクリプト コードを含むフラグメントを追加するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-152">Select **Templates**, and then select the template to which you want to add the fragment with the Clarity script code.</span></span>
1. <span data-ttu-id="1bce2-153">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-153">Select **Edit**.</span></span>
1. <span data-ttu-id="1bce2-154">**HTML Head** スロットの省略ボタン (...) を選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-154">Select the **HTML Head** slot, select the ellipsis (...), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="1bce2-155">**フラグメントの選択** ダイアログ ボックスで、Clarity スクリプト コードの付いた新しいフラグメントを選択し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-155">In the **Select fragment** dialog box, select the new fragment with the Clarity script code, and then select **OK**.</span></span> <span data-ttu-id="1bce2-156">フラグメントが **HTML ヘッド** スロットの下に表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-156">Verify that the fragment appears under the **HTML Head** slot.</span></span>
1. <span data-ttu-id="1bce2-157">**保存** を選択してから、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-157">Select **Save**, and then select **Publish**.</span></span> <span data-ttu-id="1bce2-158">更新したテンプレートを使用するすべてのサイト ページに、Clarity スクリプト コードが埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="1bce2-158">All site pages that use the updated template will now have the embedded Clarity script code.</span></span>
1. <span data-ttu-id="1bce2-159">Clarity スクリプトコードを追加する追加のテンプレートは、必要に応じて前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-159">Repeat the previous steps as needed for any additional templates to which you want to add the Clarity script code.</span></span>

<span data-ttu-id="1bce2-160">Clarity スクリプトがサイト ページに埋め込まれているかどうかをテストする方法については、[Clarity セットアップ: 検証](https://docs.microsoft.com/clarity/clarity-setup#verification) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="1bce2-160">For information about how to test if the Clarity script is embedded in site pages, see [Clarity Set-Up: Verification](https://docs.microsoft.com/clarity/clarity-setup#verification).</span></span>

### <a name="embed-clarity-tracking-script-code-into-a-specific-site-page"></a><span data-ttu-id="1bce2-161">Clarity 追跡 スクリプト コードを特定のサイト ページに埋め込みます</span><span class="sxs-lookup"><span data-stu-id="1bce2-161">Embed Clarity tracking script code into a specific site page</span></span>

> [!NOTE] 
> <span data-ttu-id="1bce2-162">インライン スクリプト モジュールは Clarity スクリプト コードをページ インスタンスに追加できるように、ページのテンプレートの **HTML ヘッド** セクションに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-162">An inline script module must be present in the **HTML Head** section of a page's template to be able to add Clarity script code to the page instance.</span></span>

<span data-ttu-id="1bce2-163">Clarity 追跡コードを Commerce サイト ビルダーの特定のサイト ページに埋め込むには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1bce2-163">To embed the Clarity tracking code into a specific site page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1bce2-164">Commerce サイト ビルダーでサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-164">Go to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="1bce2-165">**ページ** を選択し、Clarity スクリプト コードを追加するページを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-165">Select **Pages**, select the page to which you want to add Clarity script code, and then select **Edit**.</span></span>
1. <span data-ttu-id="1bce2-166">モジュールのアウトライン ペインでルート ノード スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-166">Select the root node slot in the module outline pane.</span></span>
1. <span data-ttu-id="1bce2-167">**SEO プロパティ** の下のプロパティ ペインで、**スクリプト タグ** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-167">In the properties pane under **SEO Properties**, expand the **script tag** section.</span></span> <span data-ttu-id="1bce2-168">**インライン スクリプト** の下に、Clarity 追跡コードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="1bce2-168">Under **Inline script**, paste the Clarity tracking code.</span></span> <span data-ttu-id="1bce2-169">スクリプト文字列をコピーした場合は、周囲の **\<script\>** タグを必ず削除してください。</span><span class="sxs-lookup"><span data-stu-id="1bce2-169">Be sure to remove the surrounding **\<script\>** tags if you copied the script string.</span></span>
1. <span data-ttu-id="1bce2-170">**保存** を選択し、**編集を終了する** を選択し、続いて **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bce2-170">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>

<span data-ttu-id="1bce2-171">Clarity スクリプトがサイト ページに追加された後、Clarity ポータルででデータとキャプチャの表示を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-171">After Clarity script has been added to your site pages, you should begin to see data and captures in your Clarity portal.</span></span> <span data-ttu-id="1bce2-172">結果を表示する前に、ページ ビューを累積するために追加の時間が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1bce2-172">Additional time may be needed to accumulate page views before you begin seeing results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bce2-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1bce2-173">Additional resources</span></span>

[<span data-ttu-id="1bce2-174">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="1bce2-174">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

