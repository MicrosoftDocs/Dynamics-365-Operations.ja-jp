---
title: コンテンツ配置モジュール
description: このトピックでは、コンテンツ配置とコンテンツ配置項目モジュールについて、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785303"
---
# <a name="content-placement-module"></a><span data-ttu-id="e0371-103">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e0371-104">このトピックでは、コンテンツ配置とコンテンツ配置項目モジュールについて、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0371-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e0371-105">概要</span><span class="sxs-lookup"><span data-stu-id="e0371-105">Overview</span></span>

<span data-ttu-id="e0371-106">コンテンツ配置モジュールは、特定のレイアウトで他のモジュールを中に配置できる特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e0371-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="e0371-107">コンテンツ配置モジュールは、子モジュールとして次のタイプのモジュールをサポートします: コンテンツ配置項目、アカウント ウェルカム項目、アカウント注文項目、アカウント欲しい物リスト項目、およびアカウント プロファイル項目。</span><span class="sxs-lookup"><span data-stu-id="e0371-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="e0371-108">コンテンツ配置モジュールは、サポートする子モジュールからデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0371-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="e0371-109">したがって、コンテンツ配置モジュールは、追加されるモジュールに応じてさまざまな方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="e0371-110">コンテンツ配置項目モジュールでは、プロモーション、ポリシー、および製品機能を紹介するために画像とテキストの両方を使用します。</span><span class="sxs-lookup"><span data-stu-id="e0371-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="e0371-111">たとえば、コンテンツ配置項目モジュールをホーム ページで使用して、店舗ポリシーまたは出荷情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="e0371-112">コンテンツ配置項目モジュールは、コンテンツ管理システム (CMS) からのデータによって発生し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="e0371-113">ただし、コンテンツ配置モジュール内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="e0371-114">E コマースのコンテンツ配置モジュールの例</span><span class="sxs-lookup"><span data-stu-id="e0371-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="e0371-115">コンテンツ配置項目モジュールを含むコンテンツ配置モジュールをホーム ページまたはマーケティング ページで使用して、製品機能、プロモーション、店舗ポリシー、出荷情報、およびその他の情報を画像とテキストの両方で紹介できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="e0371-116">コンテンツ配置項目モジュールを含むコンテンツ配置モジュールを製品の詳細ページで使用して、製品機能を紹介できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="e0371-117">アカウント ウェルカム項目またはアカウント注文項目モジュールを含むコンテンツ配置モジュールは、アカウント管理ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="e0371-118">コンテンツ配置モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0371-118">Content placement module properties</span></span>

| <span data-ttu-id="e0371-119">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e0371-119">Property name</span></span> | <span data-ttu-id="e0371-120">金額</span><span class="sxs-lookup"><span data-stu-id="e0371-120">Value</span></span> | <span data-ttu-id="e0371-121">説明</span><span class="sxs-lookup"><span data-stu-id="e0371-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="e0371-122">幅</span><span class="sxs-lookup"><span data-stu-id="e0371-122">Width</span></span>         | <span data-ttu-id="e0371-123">**コンテナーに適合**または**全画面**</span><span class="sxs-lookup"><span data-stu-id="e0371-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="e0371-124">値が**コンテナーに適合**に設定されている場合、コンテンツ配置モジュール内の項目は、コンテンツ配置モジュールの幅に限定されます。</span><span class="sxs-lookup"><span data-stu-id="e0371-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="e0371-125">値が**全画面**に設定されている場合、項目はコンテンツ配置モジュールの幅に限定されませんが、全画面モードになります。</span><span class="sxs-lookup"><span data-stu-id="e0371-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="e0371-126">コンテンツ配置項目モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="e0371-126">Content placement item module properties</span></span>

| <span data-ttu-id="e0371-127">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e0371-127">Property name</span></span> | <span data-ttu-id="e0371-128">金額</span><span class="sxs-lookup"><span data-stu-id="e0371-128">Value</span></span> | <span data-ttu-id="e0371-129">説明</span><span class="sxs-lookup"><span data-stu-id="e0371-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="e0371-130">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e0371-130">Heading</span></span>       | <span data-ttu-id="e0371-131">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="e0371-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e0371-132">各コンテンツ配置項目モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e0371-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="e0371-133">**ヘッダー** プロパティは、ヘッダー タグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0371-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="e0371-134">既定では、**H2** ヘッダー タグが使用されますが、アクセシビリティ要件を満たすようにヘッダー タグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e0371-135">段落</span><span class="sxs-lookup"><span data-stu-id="e0371-135">Paragraph</span></span>     | <span data-ttu-id="e0371-136">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="e0371-136">Paragraph text</span></span> | <span data-ttu-id="e0371-137">コンテンツ配置項目モジュールは、リッチ テキスト形式の段落テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0371-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="e0371-138">太字、下線付き、斜体、およびハイパーリンクなど、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e0371-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="e0371-139">これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0371-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="e0371-140">画像</span><span class="sxs-lookup"><span data-stu-id="e0371-140">Image</span></span>         | <span data-ttu-id="e0371-141">イメージ ファイル</span><span class="sxs-lookup"><span data-stu-id="e0371-141">Image file</span></span> | <span data-ttu-id="e0371-142">画像をテキストに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e0371-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="e0371-143">リンク</span><span class="sxs-lookup"><span data-stu-id="e0371-143">Link</span></span>          | <span data-ttu-id="e0371-144">リンク URL とリンク テキスト</span><span class="sxs-lookup"><span data-stu-id="e0371-144">Link URL and link text</span></span> | <span data-ttu-id="e0371-145">テキストにリンクを追加して、特定のページにユーザーをリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="e0371-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="e0371-146">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="e0371-146">Tile size</span></span>     | <span data-ttu-id="e0371-147">**1** から **12** までの数字</span><span class="sxs-lookup"><span data-stu-id="e0371-147">A number from **1** through **12**</span></span> | <span data-ttu-id="e0371-148">このプロパティは、コンテンツ配置項目ごとに、項目がコンテンツ配置モジュールを埋めるスロットの数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e0371-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="e0371-149">コンテンツ配置モジュールの最大サイズは、12 スロットです。</span><span class="sxs-lookup"><span data-stu-id="e0371-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="e0371-150">コンテンツ配置モジュールの最初の *n* 項目に対する合計タイル サイズが 12 スロットを超える場合、項目は次の行にラップされます。</span><span class="sxs-lookup"><span data-stu-id="e0371-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="e0371-151">コンテンツ配置項目モジュールを含むコンテンツ配置モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="e0371-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="e0371-152">コンテンツ配置項目モジュールを含むコンテンツ配置モジュールを新しいページに追加して必要なプロパティを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e0371-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e0371-153">**コンテンツ配置テンプレート**という名前のテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="e0371-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="e0371-154">既定のページの**メイン** スロットで、コンテンツ配置モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0371-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="e0371-155">コンテンツ配置モジュールで、コンテンツ配置項目モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0371-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="e0371-156">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="e0371-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e0371-157">作成したコンテンツ配置テンプレートを使用して、**コンテンツ配置ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="e0371-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="e0371-158">新しいページの**メイン** スロットで、コンテンツ配置モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0371-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="e0371-159">コンテンツ配置モジュールで、コンテンツ配置項目モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0371-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="e0371-160">コンテンツ配置項目モジュールのプロパティ ウィンドウで画像を選択し、ヘッダーを追加し、段落を追加し、リンクの追加、リンク URL を設定し、タイル サイズを **6** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0371-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="e0371-161">手順 7 と 8 を繰り返して、同じタイル サイズを持つ他のコンテンツ配置項目モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0371-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="e0371-162">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="e0371-162">Save and preview the page.</span></span> <span data-ttu-id="e0371-163">並んで表示される 2 つのコンテンツ配置項目が確認できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="e0371-164">各コンテンツ配置項目モジュールの**タイル サイズ** プロパティを調整するか、またはモジュールを追加して目的のレイアウトを達成できます。</span><span class="sxs-lookup"><span data-stu-id="e0371-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="e0371-165">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="e0371-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0371-166">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e0371-166">Additional resources</span></span>

[<span data-ttu-id="e0371-167">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="e0371-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e0371-168">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e0371-169">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e0371-170">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e0371-171">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e0371-172">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="e0371-173">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="e0371-173">Video player module</span></span>](add-video-player.md)
