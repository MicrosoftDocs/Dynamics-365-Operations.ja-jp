---
title: プライバシー ポリシー ページの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにプライバシー ポリシー ページを追加する方法について説明します。
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797530"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="95eda-103">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="95eda-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95eda-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトにプライバシー ポリシー ページを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="95eda-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="95eda-105">プライバシー コンプライアンスには、データの収集および処理方法をサイト ユーザーに通知する組織的手段が含まれます。</span><span class="sxs-lookup"><span data-stu-id="95eda-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="95eda-106">その後ユーザーは、個人データの処理方法を決定し、適切なアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="95eda-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="95eda-107">Dynamics 365 Commerce の Microsoft のプライバシーに関する声明を確認する</span><span class="sxs-lookup"><span data-stu-id="95eda-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="95eda-108">Dynamics 365 Commerce オーサリング ツールにサインインしている間に Microsoft のプライバシーに関する声明を確認するには、右上隅にある **ヘルプ** ボタン **?** をクリックしてから、**プライバシーと Cookie** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="95eda-109">[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) へのリンクを含む新しいタブが開きます。</span><span class="sxs-lookup"><span data-stu-id="95eda-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="95eda-110">サイトのプライバシー ポリシー ページを構築する</span><span class="sxs-lookup"><span data-stu-id="95eda-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="95eda-111">Dynamics 365 Commerce には、サイトのユーザーにプライバシー ポリシーへのアクセスを許可する方法がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="95eda-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="95eda-112">このセクションでは、プライバシー ポリシー ページを構築し、フッター フラグメントを使用してページを参照する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="95eda-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="95eda-113">次のガイダンスは、コマース サイトの汎用プライバシー ポリシー ページの構築方法を示す例です。</span><span class="sxs-lookup"><span data-stu-id="95eda-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="95eda-114">会社の法的要件に最適なプライバシー ポリシー ページ ソリューションをデザインおよび実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="95eda-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="95eda-115">最初に、オーサリング ツールで、プライバシー ポリシー ページを構築するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="95eda-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="95eda-116">テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="95eda-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="95eda-117">プライバシー ポリシー ページで使用できるテンプレートが既に作成されている場合は、[プライバシー ポリシー ページを構築する](#build-a-privacy-policy-page) セクションにスキップします。</span><span class="sxs-lookup"><span data-stu-id="95eda-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="95eda-118">テンプレートを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="95eda-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="95eda-119">**テンプレート** に移動し、続いて **新規** を選択してページのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="95eda-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="95eda-120">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**プロモーション バナーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="95eda-121">テンプレートで、必要なページ スロットに必要なモジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="95eda-122">ガイダンスで、赤い感嘆符をポイントします。</span><span class="sxs-lookup"><span data-stu-id="95eda-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="95eda-123">（たとえば、**HTML ヘッド** スロットには、**既定の外部スクリプト** モジュールが必要になる場合があります）</span><span class="sxs-lookup"><span data-stu-id="95eda-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="95eda-124">**本文** スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="95eda-125">**既定のページ** モジュールの、**メイン** スロットで、**コンテンツ リッチ ブロック** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="95eda-126">**コンテンツ リッチ ブロック** モジュールで、**コンテンツ リッチ ブロック項目** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="95eda-127">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="95eda-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="95eda-128">プライバシー ポリシー ページの構築</span><span class="sxs-lookup"><span data-stu-id="95eda-128">Build a privacy policy page</span></span>

<span data-ttu-id="95eda-129">プライバシー ポリシー ページを構築するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="95eda-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="95eda-130">**ページ** に移動し、続いて **新規** を選択してページを作成します。</span><span class="sxs-lookup"><span data-stu-id="95eda-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="95eda-131">**テンプレートの選択** ダイアログ ボックスで、[プライバシーポリシー] ページのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="95eda-132">ページ名と ページの URL を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="95eda-133">ページの **メイン** スロットで、**コンテンツ リッチ ブロック** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="95eda-134">**コンテンツ リッチ ブロック** モジュールで、**コンテンツ リッチ ブロック項目** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="95eda-135">**コンテンツ リッチ ブロック** モジュールのプロパティ ウィンドウで、**データ ソースの追加** を選択してから、**リッチ テキスト コンテンツ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="95eda-136">リッチ テキスト エディターで、プライバシー ポリシー ページのコンテンツを入力します。</span><span class="sxs-lookup"><span data-stu-id="95eda-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="95eda-137">必要に応じてリッチ テキスト エディターをフルスクリーン モードに拡張します。</span><span class="sxs-lookup"><span data-stu-id="95eda-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="95eda-138">コンテンツの入力が完了したら、**プレビュー** を選択して Web ブラウザーでページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="95eda-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="95eda-139">ページおよびモジュール プロパティへの残りの追加を完了します。</span><span class="sxs-lookup"><span data-stu-id="95eda-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="95eda-140">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="95eda-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="95eda-141">プライバシー ポリシー ページの URL を公開するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="95eda-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="95eda-142">**URL** に移動し、プライバシー ポリシー ページの URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="95eda-143">**公開** を選択して、選択した URL を公開します。</span><span class="sxs-lookup"><span data-stu-id="95eda-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="95eda-144">フッターにプライバシー ポリシー ページへのリンクを作成する</span><span class="sxs-lookup"><span data-stu-id="95eda-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="95eda-145">プライバシー ポリシー ページへのリンクをフラグメントに追加できます。</span><span class="sxs-lookup"><span data-stu-id="95eda-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="95eda-146">この方法により、フラグメントを参照することによって、リンクを共有し複数のサイト ページにわたって更新できます。</span><span class="sxs-lookup"><span data-stu-id="95eda-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="95eda-147">この例では、フッター フラグメントにプライバシー ポリシー ページへのリンクの追加方法を示します。</span><span class="sxs-lookup"><span data-stu-id="95eda-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="95eda-148">フッター フラグメントにリンクを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="95eda-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="95eda-149">**フラグメント** に移動し、続いて **新規** を選択してページ フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="95eda-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="95eda-150">**ページ フラグメント** ダイアログ ボックスで、**フッター** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="95eda-151">**フラグメント名** で、フラグメントの名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="95eda-152">**フッター カテゴリ** スロットで、**フッター項目** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="95eda-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="95eda-153">右側のプロパティ ウィンドウで、**リンク テキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="95eda-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="95eda-154">**リンク テキスト** ダイアログ ボックスで、プライバシー ポリシー ページのリンク テキストとリンク先を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="95eda-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="95eda-155">プライバシー ポリシー ページの URL を取得するには、**ページ** に移動し、プライバシー ポリシー ページに移動して、プロパティ ウィンドウから URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="95eda-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="95eda-156">**保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="95eda-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="95eda-157">フラグメントをプレビューし、プライバシー ポリシー ページへのリンクをテストします。</span><span class="sxs-lookup"><span data-stu-id="95eda-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="95eda-158">他のサイト ページのテンプレートからフラグメントを参照できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="95eda-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="95eda-159">テンプレートの **フッター** モジュールでこのフラグメントが参照される場合、そのテンプレートを使用して構築された任意のページにリンク参照が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95eda-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95eda-160">追加リソース</span><span class="sxs-lookup"><span data-stu-id="95eda-160">Additional resources</span></span>

[<span data-ttu-id="95eda-161">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="95eda-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="95eda-162">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="95eda-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="95eda-163">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="95eda-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="95eda-164">追跡しているコンテンツの変更に関連付けられたユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="95eda-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
