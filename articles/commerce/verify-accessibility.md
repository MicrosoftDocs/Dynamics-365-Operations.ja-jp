---
title: ページ コンテンツのアクセシビリティの検証
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946039"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="b9b60-103">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="b9b60-103">Verify page content accessibility</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b9b60-104">このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9b60-105">概要</span><span class="sxs-lookup"><span data-stu-id="b9b60-105">Overview</span></span>

<span data-ttu-id="b9b60-106">ページの変更が完了したら、Web 上の全ユーザーがコンテンツにアクセスできることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b60-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="b9b60-107">Commerce 作成ツールにおいて、統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用することで、ページ コンテンツのアクセシビリティを簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="b9b60-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="b9b60-108">このサービスは、ページと最新の [World Wide Web コンソーシアム (W3C) アクセシビリティ](https://www.w3.org/standards/webdesign/accessibility) ガイドラインを検証します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="b9b60-109">[Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) の統合は、使用する前に、テナントまたはサイト レベルで有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b60-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="b9b60-110">テナント内のすべてのサイトに対する Microsoft アクセシビリティ インサイトの有効化</span><span class="sxs-lookup"><span data-stu-id="b9b60-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="b9b60-111">テナント内のすべての Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="b9b60-112">テナントの設定にアクセスするには、システム管理者として Commerce にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b60-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="b9b60-113">システム管理者として Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b9b60-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="b9b60-114">左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="b9b60-115">**テナントの設定**で、**機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b9b60-116">**アクセシビリティ チェック** オプションを**オン**にします。</span><span class="sxs-lookup"><span data-stu-id="b9b60-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="b9b60-117">1 つのサイトに対する Microsoft アクセシビリティ インサイトの有効化</span><span class="sxs-lookup"><span data-stu-id="b9b60-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="b9b60-118">1 つの Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="b9b60-119">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b9b60-120">左のナビゲーション ウィンドウで、**サイト設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="b9b60-121">**サイト設定**で、**機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b9b60-122">**アクセシビリティ チェック** オプションを**オン**にします。</span><span class="sxs-lookup"><span data-stu-id="b9b60-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="b9b60-123">ホーム ページのコンテンツのアクセシビリティを確認する</span><span class="sxs-lookup"><span data-stu-id="b9b60-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="b9b60-124">統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用して、Commerce のホーム ページのコンテンツのスキャンおよび確認をするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b9b60-125">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b9b60-126">左のナビゲーション ウィンドウで、**ページ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="b9b60-127">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="b9b60-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b9b60-128">コマンド バーで、**アクセシビリティのチェック**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="b9b60-129">**アクセシビリティのチェック**のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9b60-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="b9b60-130">スキャンが完了した後、レポートの内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="b9b60-131">チェックが失敗した場合、失敗したチェック項目をそれぞれ選択して展開し、詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="b9b60-132">確認した後、レポートを閉じるには、**アクセシビリティのチェック** ページの下部までスクロールし、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9b60-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9b60-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b9b60-133">Additional resources</span></span>

[<span data-ttu-id="b9b60-134">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="b9b60-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b9b60-135">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="b9b60-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b9b60-136">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="b9b60-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b9b60-137">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="b9b60-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b9b60-138">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="b9b60-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b9b60-139">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="b9b60-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b9b60-140">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="b9b60-140">Enrich a category landing page</span></span>](enrich-category-page.md)
