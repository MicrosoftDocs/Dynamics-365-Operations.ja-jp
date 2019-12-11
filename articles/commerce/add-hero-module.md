---
title: ヒーロー モジュール
description: このトピックでは、ヒーロー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785396"
---
# <a name="hero-module"></a><span data-ttu-id="bc561-103">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bc561-104">このトピックでは、ヒーロー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc561-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bc561-105">概要</span><span class="sxs-lookup"><span data-stu-id="bc561-105">Overview</span></span>

<span data-ttu-id="bc561-106">画像とテキストの組み合わせを通じて製品またはプロモーションをマーケティングするために、ヒーロー モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc561-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="bc561-107">たとえば、小売業者は E コマース サイトのホーム ページにヒーロー モジュールを追加して、新しい製品を販売促進し、顧客の注意を引き付けることができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="bc561-108">ヒーロー モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動します。</span><span class="sxs-lookup"><span data-stu-id="bc561-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="bc561-109">ページでその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="bc561-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="bc561-110">ヒーロー モジュールは、小売業者がマーケティングまたは販売促進を行う (製品、販売、機能など) サイト ページに配置することができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="bc561-111">E コマースのヒーロー モジュールの例</span><span class="sxs-lookup"><span data-stu-id="bc561-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="bc561-112">ヒーロー モジュールは、E コマース サイトのホーム ページで使用して、プロモーションや新製品を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="bc561-113">製品の詳細ページでヒーロー モジュールを使用して、製品情報を紹介することができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="bc561-114">複数のヒーロー モジュールをカルーセル モジュール内に配置することにより、複数の製品またはプロモーションを強調表示できます。</span><span class="sxs-lookup"><span data-stu-id="bc561-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="bc561-115">ヒーロー モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="bc561-115">Hero module properties</span></span>

| <span data-ttu-id="bc561-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="bc561-116">Property name</span></span>  | <span data-ttu-id="bc561-117">値</span><span class="sxs-lookup"><span data-stu-id="bc561-117">Values</span></span> | <span data-ttu-id="bc561-118">説明</span><span class="sxs-lookup"><span data-stu-id="bc561-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="bc561-119">画像</span><span class="sxs-lookup"><span data-stu-id="bc561-119">Image</span></span>          | <span data-ttu-id="bc561-120">イメージ ファイル</span><span class="sxs-lookup"><span data-stu-id="bc561-120">Image file</span></span> | <span data-ttu-id="bc561-121">画像を使用して製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="bc561-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="bc561-122">画像を画像ギャラリーにアップロードしたり、既存の画像を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="bc561-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="bc561-123">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="bc561-123">Heading</span></span>        | <span data-ttu-id="bc561-124">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="bc561-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="bc561-125">各ヒーロー モジュールにヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-125">Every hero module can have a heading.</span></span> <span data-ttu-id="bc561-126">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc561-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="bc561-127">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="bc561-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="bc561-128">段落</span><span class="sxs-lookup"><span data-stu-id="bc561-128">Paragraph</span></span>      | <span data-ttu-id="bc561-129">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="bc561-129">Paragraph text</span></span> | <span data-ttu-id="bc561-130">ヒーロー モジュールは、リッチ テキスト形式の段落テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bc561-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="bc561-131">太字、下線付き、斜体、およびハイパーリンクなど、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="bc561-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="bc561-132">これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bc561-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="bc561-133">リンク</span><span class="sxs-lookup"><span data-stu-id="bc561-133">Link</span></span>           | <span data-ttu-id="bc561-134">リンク テキスト、リンク URL、アクセス可能リッチ インターネット アプリケーション (ARIA) ラベル、および **新しいタブでリンクを開く**</span><span class="sxs-lookup"><span data-stu-id="bc561-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="bc561-135">ヒーロー モジュールは、1 つ以上の "アクションの呼び出し" リンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bc561-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="bc561-136">リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。</span><span class="sxs-lookup"><span data-stu-id="bc561-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="bc561-137">ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc561-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="bc561-138">リンクをコンフィギュレーションして、新しいタブで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="bc561-139">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="bc561-139">Text placement</span></span> | <span data-ttu-id="bc561-140">**左上**、**右上**、**中央上**、**左下**、**右下**、**中央下**、**中央左**、**中央右**、または**中央の中央**</span><span class="sxs-lookup"><span data-stu-id="bc561-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="bc561-141">このプロパティは、テキストに対する画像の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="bc561-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="bc561-142">たとえば、**右**が選択されている場合、テキストの右側に画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc561-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="bc561-143">テキストのテーマ</span><span class="sxs-lookup"><span data-stu-id="bc561-143">Text theme</span></span>     | <span data-ttu-id="bc561-144">**明るい**または**暗い**</span><span class="sxs-lookup"><span data-stu-id="bc561-144">**Light** or **Dark**</span></span> | <span data-ttu-id="bc561-145">背景画像に基づいて、テキストに対する配色を定義できます。</span><span class="sxs-lookup"><span data-stu-id="bc561-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="bc561-146">たとえば、画像の背景が暗い場合、明るいテーマを適用してテキストを表示より見やすくし、アクセシビリティ目的で色のコントラスト比を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="bc561-147">グラデーション</span><span class="sxs-lookup"><span data-stu-id="bc561-147">Gradient</span></span>       | <span data-ttu-id="bc561-148">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="bc561-148">**True** or **False**</span></span> | <span data-ttu-id="bc561-149">画像にグラデーションを適用して、アクセシビリティ目的で色のコントラスト比を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="bc561-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="bc561-150">ヒーロー モジュールを新しいページに追加する</span><span class="sxs-lookup"><span data-stu-id="bc561-150">Add a hero module to a new page</span></span>

<span data-ttu-id="bc561-151">新しいページにヒーロー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc561-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bc561-152">**テンプレート**に移動して、**ヒーロー テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="bc561-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="bc561-153">既定のページの**メイン** スロットで、ヒーロー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="bc561-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="bc561-154">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="bc561-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="bc561-155">作成したヒーロー テンプレートを使用して、**ヒーロー ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="bc561-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="bc561-156">既定のページの**メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bc561-157">**モジュールの追加**ダイアログ ボックスの、**モジュールの選択**で、ヒーロー モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="bc561-158">左側のアウトライン ツリーで、ヒーロー モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="bc561-159">右側のプロパティ ウィンドウで、**画像の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="bc561-160">次に、既存の画像を選択するか、新しい画像をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="bc561-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="bc561-161">**ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-161">Select **Heading**.</span></span>
1. <span data-ttu-id="bc561-162">**ヘッダー** ダイアログ ボックスで、ヘッダー テキストを追加し、ヘッダー レベルを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="bc561-163">**リッチ テキスト**で、必要に応じてテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="bc561-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="bc561-164">**アクション リンクの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="bc561-165">**アクション リンク** ダイアログ ボックスで、リンク テキスト、リンク URL、およびリンクの ARIA ラベルを追加し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc561-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="bc561-166">ページを保存して、プレビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="bc561-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="bc561-167">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="bc561-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc561-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bc561-168">Additional resources</span></span>

[<span data-ttu-id="bc561-169">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="bc561-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bc561-170">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="bc561-171">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="bc561-172">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="bc561-173">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="bc561-174">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="bc561-175">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="bc561-175">Video player module</span></span>](add-video-player.md)
