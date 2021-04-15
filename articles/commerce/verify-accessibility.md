---
title: ページ コンテンツのアクセシビリティの検証
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791634"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="64c01-103">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="64c01-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64c01-104">このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64c01-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="64c01-105">ページの変更が完了したら、Web 上の全ユーザーがコンテンツにアクセスできることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c01-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="64c01-106">Commerce 作成ツールにおいて、統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用することで、ページ コンテンツのアクセシビリティを簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="64c01-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="64c01-107">このサービスは、ページと最新の [World Wide Web コンソーシアム (W3C) アクセシビリティ](https://www.w3.org/standards/webdesign/accessibility) ガイドラインを検証します。</span><span class="sxs-lookup"><span data-stu-id="64c01-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="64c01-108">[Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) の統合は、使用する前に、テナントまたはサイト レベルで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c01-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="64c01-109">テナント内のすべてのサイトに対する Microsoft アクセシビリティ インサイトの有効化</span><span class="sxs-lookup"><span data-stu-id="64c01-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="64c01-110">テナント内のすべての Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64c01-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="64c01-111">テナントの設定にアクセスするには、システム管理者として Commerce にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64c01-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="64c01-112">システム管理者として Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="64c01-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="64c01-113">左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="64c01-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="64c01-114">**テナントの設定** で、**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="64c01-115">**アクセシビリティ チェック** オプションを **オン** にします。</span><span class="sxs-lookup"><span data-stu-id="64c01-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="64c01-116">1 つのサイトに対する Microsoft アクセシビリティ インサイトの有効化</span><span class="sxs-lookup"><span data-stu-id="64c01-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="64c01-117">1 つの Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64c01-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="64c01-118">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="64c01-119">左のナビゲーション ウィンドウで、**サイト設定** を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="64c01-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="64c01-120">**サイト設定** で、**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="64c01-121">**アクセシビリティ チェック** オプションを **オン** にします。</span><span class="sxs-lookup"><span data-stu-id="64c01-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="64c01-122">ホーム ページのコンテンツのアクセシビリティを確認する</span><span class="sxs-lookup"><span data-stu-id="64c01-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="64c01-123">統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用して、Commerce のホーム ページのコンテンツのスキャンおよび確認をするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64c01-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="64c01-124">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="64c01-125">左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="64c01-126">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="64c01-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="64c01-127">コマンド バーで、**アクセシビリティのチェック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="64c01-128">**アクセシビリティのチェック** のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64c01-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="64c01-129">スキャンが完了した後、レポートの内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="64c01-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="64c01-130">チェックが失敗した場合、失敗したチェック項目をそれぞれ選択して展開し、詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="64c01-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="64c01-131">確認した後、レポートを閉じるには、**アクセシビリティのチェック** ページの下部までスクロールし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64c01-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64c01-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="64c01-132">Additional resources</span></span>

[<span data-ttu-id="64c01-133">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="64c01-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="64c01-134">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="64c01-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="64c01-135">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="64c01-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="64c01-136">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="64c01-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="64c01-137">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="64c01-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="64c01-138">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="64c01-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="64c01-139">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="64c01-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="64c01-140">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="64c01-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
