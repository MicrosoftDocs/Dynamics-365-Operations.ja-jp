---
title: プライバシー ポリシー ページの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにプライバシー ポリシー ページを追加する方法について説明します。
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946043"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="de7eb-103">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="de7eb-103">Add a privacy policy page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="de7eb-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトにプライバシー ポリシー ページを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de7eb-105">概要</span><span class="sxs-lookup"><span data-stu-id="de7eb-105">Overview</span></span>

<span data-ttu-id="de7eb-106">プライバシー コンプライアンスには、データの収集および処理方法をサイト ユーザーに通知する組織的手段が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="de7eb-107">その後ユーザーは、個人データの処理方法を決定し、適切なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="de7eb-108">Dynamics 365 Commerce の Microsoft のプライバシーに関する声明を確認する</span><span class="sxs-lookup"><span data-stu-id="de7eb-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="de7eb-109">Dynamics 365 Commerce オーサリング ツールにサインインしている間に Microsoft のプライバシーに関する声明を確認するには、右上隅にある**ヘルプ** ボタン **?** をクリックしてから、**プライバシーと Cookie** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="de7eb-110">[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) へのリンクを含む新しいタブが開きます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="de7eb-111">サイトのプライバシー ポリシー ページを構築する</span><span class="sxs-lookup"><span data-stu-id="de7eb-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="de7eb-112">Dynamics 365 Commerce には、サイトのユーザーにプライバシー ポリシーへのアクセスを許可する方法がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="de7eb-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="de7eb-113">このセクションでは、プライバシー ポリシー ページを構築し、フッター フラグメントを使用してページを参照する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="de7eb-114">次のガイダンスは、コマース サイトの汎用プライバシー ポリシー ページの構築方法を示す例です。</span><span class="sxs-lookup"><span data-stu-id="de7eb-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="de7eb-115">会社の法的要件に最適なプライバシー ポリシー ページ ソリューションをデザインおよび実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="de7eb-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="de7eb-116">最初に、オーサリング ツールで、プライバシー ポリシー ページを構築するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="de7eb-117">テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="de7eb-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="de7eb-118">プライバシー ポリシー ページで使用できるテンプレートが既に作成されている場合は、[プライバシー ポリシー ページを構築する](#build-a-privacy-policy-page) セクションにスキップします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="de7eb-119">テンプレートを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="de7eb-120">**テンプレート \> 新しいテンプレート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="de7eb-121">テンプレート名を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="de7eb-122">テンプレートで、必要なページ スロットに必要なモジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="de7eb-123">ガイダンスで、赤い感嘆符をポイントします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="de7eb-124">たとえば、**HTML ヘッド** スロットには、**既定の外部スクリプト** モジュールが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="de7eb-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="de7eb-125">**本文**スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="de7eb-126">**既定のページ** モジュールの、**メイン** スロットで、**コンテンツ リッチ ブロック** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="de7eb-127">**コンテンツ リッチ ブロック** モジュールで、**コンテンツ リッチ ブロック項目**モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="de7eb-128">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="de7eb-129">プライバシー ポリシー ページの構築</span><span class="sxs-lookup"><span data-stu-id="de7eb-129">Build a privacy policy page</span></span>

<span data-ttu-id="de7eb-130">プライバシー ポリシー ページを構築するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="de7eb-131">**ページ \> 新しいページ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="de7eb-132">プライバシー ポリシー ページのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="de7eb-133">ページ名および URL を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="de7eb-134">ページの**メイン** スロットで、**コンテンツ リッチ ブロック** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="de7eb-135">**コンテンツ リッチ ブロック** モジュールで、**コンテンツ リッチ ブロック項目**モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="de7eb-136">**コンテンツ リッチ ブロック** モジュールのプロパティ ウィンドウで、**データ ソースの追加**を選択してから、**リッチ テキスト コンテンツ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="de7eb-137">リッチ テキスト エディターで、プライバシー ポリシー ページのコンテンツを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="de7eb-138">必要に応じてリッチ テキスト エディターをフルスクリーン モードに拡張します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="de7eb-139">コンテンツの入力が完了したら、**プレビュー**を選択して Web ブラウザーでページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="de7eb-140">ページおよびモジュール プロパティへの残りの追加を完了します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="de7eb-141">プライバシー ポリシー ページを確認して、公開します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="de7eb-142">プライバシー ポリシー ページの URL を公開するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="de7eb-143">**URL** に移動し、プライバシー ポリシー ページの URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="de7eb-144">選択した URL を公開します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="de7eb-145">フッターにプライバシー ポリシー ページへのリンクを作成する</span><span class="sxs-lookup"><span data-stu-id="de7eb-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="de7eb-146">プライバシー ポリシー ページへのリンクをフラグメントに追加できます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="de7eb-147">この方法により、フラグメントを参照することによって、リンクを共有し複数のサイト ページにわたって更新できます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="de7eb-148">この例では、フッター フラグメントにプライバシー ポリシー ページへのリンクの追加方法を示します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="de7eb-149">フッター フラグメントにリンクを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de7eb-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="de7eb-150">**ページ フラグメント \> 新しいページ フラグメント**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="de7eb-151">**フッター** モジュールを選択し、**ページ フラグメント名**フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="de7eb-152">**フッター カテゴリ** スロットで、**フッター項目**モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="de7eb-153">右側のプロパティ ウィンドウで、**リンク テキスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="de7eb-154">**リンク テキスト** ダイアログ ボックスで、プライバシー ポリシー ページのリンク テキストとリンク先を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="de7eb-155">プライバシー ポリシー ページの URL を取得するには、**ページ**に移動し、プライバシー ポリシー ページに移動して、プロパティ ウィンドウから URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="de7eb-156">フラグメントを保存し、確認後に公開します。</span><span class="sxs-lookup"><span data-stu-id="de7eb-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="de7eb-157">フラグメントをプレビューし、プライバシー ポリシー ページへのリンクをテストします。</span><span class="sxs-lookup"><span data-stu-id="de7eb-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="de7eb-158">他のサイト ページのテンプレートからフラグメントを参照できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="de7eb-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="de7eb-159">テンプレートの**フッター** モジュールでこのフラグメントが参照される場合、そのテンプレートを使用して構築された任意のページにリンク参照が表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7eb-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de7eb-160">追加リソース</span><span class="sxs-lookup"><span data-stu-id="de7eb-160">Additional resources</span></span>

[<span data-ttu-id="de7eb-161">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="de7eb-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="de7eb-162">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="de7eb-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="de7eb-163">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="de7eb-163">Cookie compliance</span></span>](cookie-compliance.md)
