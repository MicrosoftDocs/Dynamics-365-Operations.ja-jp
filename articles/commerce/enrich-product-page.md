---
title: 製品ページの拡充
description: このトピックでは、Microsoft Dynamics 365 Commerce で製品ページを拡充する方法について説明します。
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799050"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="4b788-103">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="4b788-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b788-104">このトピックでは、Microsoft Dynamics 365 Commerce で製品ページを拡充する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b788-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4b788-105">既定では、サイトは汎用ページを使用して製品データを表示します。</span><span class="sxs-lookup"><span data-stu-id="4b788-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="4b788-106">このページには、製品とその販売に必要なコントロールに関する基本的な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b788-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="4b788-107">ただし、特定の製品の追加画像またはテキストを使用して、Commerce Scale Unit から取得した情報を補足することができます。</span><span class="sxs-lookup"><span data-stu-id="4b788-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="4b788-108">このプロセスは、製品ページの拡充と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="4b788-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="4b788-109">多くの場合、製品に特定の追加コンテンツを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b788-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="4b788-110">オーサリング ツールで **Retail と Commerce** にアクセスすると、サイトに割り当てられているチャネルの製品の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b788-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="4b788-111">この一覧の **拡充** 列は、製品の製品ページが拡充されているかどうかを示しています。</span><span class="sxs-lookup"><span data-stu-id="4b788-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="4b788-112">列にチェック マークが表示される場合は、製品に対して拡充された製品ページが存在します。</span><span class="sxs-lookup"><span data-stu-id="4b788-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="4b788-113">チェック マークが表示されない場合は、製品に対して既定の製品ページとコンテンツが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b788-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="4b788-114">一覧で製品名を選択して、拡充された製品ページと非拡充の製品ページの両方をプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="4b788-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="4b788-115">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="4b788-115">Enrich a product page</span></span>

<span data-ttu-id="4b788-116">製品ページを拡充するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4b788-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="4b788-117">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4b788-118">左のナビゲーション ウィンドウで、**製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="4b788-119">拡充された製品ページがない製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="4b788-120">アクション ウィンドウで、**製品ページの拡充** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="4b788-121">**PDP テンプレート** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4b788-122">左側のページのアウトライン ツリーで、**メイン** スロットを展開します。</span><span class="sxs-lookup"><span data-stu-id="4b788-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="4b788-123">**メイン** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4b788-124">**コンテナー 2** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="4b788-125">**コンテナー 2** の省略ボタンを選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="4b788-126">**機能** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="4b788-127">右側のプロパティ ウィンドウの **リッチ テキスト** フィールドに、更新された製品の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b788-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="4b788-128">**ヘッダー** フィールドに、ヘッダーのテキストを入力してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="4b788-129">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4b788-130">**コメント** フィールドに、**製品を拡充した** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="4b788-131">**プレビュー** を選択して、拡充された製品ページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="4b788-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="4b788-132">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="4b788-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="4b788-133">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4b788-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b788-134">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4b788-134">Additional resources</span></span>

[<span data-ttu-id="4b788-135">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="4b788-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4b788-136">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="4b788-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4b788-137">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="4b788-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4b788-138">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="4b788-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="4b788-139">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="4b788-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4b788-140">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="4b788-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4b788-141">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="4b788-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="4b788-142">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="4b788-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
