---
title: 機能モジュール
description: このトピックでは、機能モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785287"
---
# <a name="feature-module"></a><span data-ttu-id="660b8-103">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="660b8-104">このトピックでは、機能モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="660b8-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="660b8-105">概要</span><span class="sxs-lookup"><span data-stu-id="660b8-105">Overview</span></span>

<span data-ttu-id="660b8-106">画像とテキストの組み合わせを通じて製品またはプロモーションをマーケティングするために、機能モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="660b8-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="660b8-107">たとえば、小売業者は、製品の詳細ページに機能モジュールを追加して製品の機能を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="660b8-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="660b8-108">機能モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動します。</span><span class="sxs-lookup"><span data-stu-id="660b8-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="660b8-109">ページでその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="660b8-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="660b8-110">機能モジュールは、小売業者がマーケティングまたは販売促進を行う (製品、販売、機能など) サイト ページに配置することができます。</span><span class="sxs-lookup"><span data-stu-id="660b8-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="660b8-111">E コマースの機能モジュールの例</span><span class="sxs-lookup"><span data-stu-id="660b8-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="660b8-112">機能モジュールは、次のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="660b8-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="660b8-113">製品の詳細ページで、製品機能について紹介する</span><span class="sxs-lookup"><span data-stu-id="660b8-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="660b8-114">ホーム ページで、製品を販売促進する</span><span class="sxs-lookup"><span data-stu-id="660b8-114">The home page, to promote products</span></span>
- <span data-ttu-id="660b8-115">カテゴリ ページで、製品のカテゴリを強調表示する</span><span class="sxs-lookup"><span data-stu-id="660b8-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="660b8-116">機能モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="660b8-116">Feature module properties</span></span>

| <span data-ttu-id="660b8-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="660b8-117">Property name</span></span>     | <span data-ttu-id="660b8-118">値</span><span class="sxs-lookup"><span data-stu-id="660b8-118">Values</span></span> | <span data-ttu-id="660b8-119">説明</span><span class="sxs-lookup"><span data-stu-id="660b8-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="660b8-120">画像</span><span class="sxs-lookup"><span data-stu-id="660b8-120">Image</span></span>             | <span data-ttu-id="660b8-121">イメージ ファイル</span><span class="sxs-lookup"><span data-stu-id="660b8-121">Image file</span></span> | <span data-ttu-id="660b8-122">画像を使用して製品またはプロモーションのマーケティングを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="660b8-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="660b8-123">画像を画像ギャラリーにアップロードしたり、既存の画像を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="660b8-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="660b8-124">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="660b8-124">Heading</span></span>           | <span data-ttu-id="660b8-125">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="660b8-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="660b8-126">各機能モジュールにヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="660b8-126">Every feature module can have a heading.</span></span> <span data-ttu-id="660b8-127">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="660b8-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="660b8-128">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="660b8-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="660b8-129">段落</span><span class="sxs-lookup"><span data-stu-id="660b8-129">Paragraph</span></span>         | <span data-ttu-id="660b8-130">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="660b8-130">Paragraph text</span></span> | <span data-ttu-id="660b8-131">機能モジュールは、リッチ テキスト形式の段落テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="660b8-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="660b8-132">太字、下線付き、斜体、およびハイパーリンクなど、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="660b8-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="660b8-133">これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="660b8-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="660b8-134">リンク</span><span class="sxs-lookup"><span data-stu-id="660b8-134">Link</span></span>              | <span data-ttu-id="660b8-135">リンク テキスト、リンク URL、アクセス可能リッチ インターネット アプリケーション (ARIA) ラベル、および **新しいタブでリンクを開く**</span><span class="sxs-lookup"><span data-stu-id="660b8-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="660b8-136">機能モジュールは、1 つ以上の "アクションの呼び出し" リンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="660b8-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="660b8-137">リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。</span><span class="sxs-lookup"><span data-stu-id="660b8-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="660b8-138">ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="660b8-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="660b8-139">リンクをコンフィギュレーションして、新しいタブで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="660b8-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="660b8-140">画像の配置</span><span class="sxs-lookup"><span data-stu-id="660b8-140">Image placement</span></span>   | <span data-ttu-id="660b8-141">**右**、**左**、**上**、または**下**</span><span class="sxs-lookup"><span data-stu-id="660b8-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="660b8-142">このプロパティは、テキストに対する画像の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="660b8-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="660b8-143">たとえば、**右**が選択されている場合、テキストの右側に画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="660b8-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="660b8-144">画像の列サイズ</span><span class="sxs-lookup"><span data-stu-id="660b8-144">Image column size</span></span> | <span data-ttu-id="660b8-145">**1** から **12** までの値</span><span class="sxs-lookup"><span data-stu-id="660b8-145">A value from **1** through **12**</span></span> | <span data-ttu-id="660b8-146">このプロパティは、テキストに対する画像のサイズを定義します。</span><span class="sxs-lookup"><span data-stu-id="660b8-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="660b8-147">サイズは、ページの列の数として表されます。</span><span class="sxs-lookup"><span data-stu-id="660b8-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="660b8-148">1 ページに 12 列あります。</span><span class="sxs-lookup"><span data-stu-id="660b8-148">There are 12 columns on a page.</span></span> <span data-ttu-id="660b8-149">既定では、画像とテキストのサイズは等しくなります (各 6 列)。</span><span class="sxs-lookup"><span data-stu-id="660b8-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="660b8-150">ただし、サイズは必要に応じて調整できます。</span><span class="sxs-lookup"><span data-stu-id="660b8-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="660b8-151">機能モジュールを新しいページに追加する</span><span class="sxs-lookup"><span data-stu-id="660b8-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="660b8-152">新しいページに機能モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="660b8-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="660b8-153">**テンプレート**に移動して、**機能テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="660b8-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="660b8-154">既定のページの**メイン** スロットで、機能モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="660b8-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="660b8-155">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="660b8-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="660b8-156">作成した機能テンプレートを使用して、**機能ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="660b8-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="660b8-157">既定のページの**メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="660b8-158">**モジュールの追加**ダイアログ ボックスの、**モジュールの選択**で、機能モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="660b8-159">左側のアウトライン ツリーで、機能モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="660b8-160">右側のプロパティ ウィンドウで、**画像の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="660b8-161">次に、既存の画像を選択するか、新しい画像をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="660b8-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="660b8-162">**ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-162">Select **Heading**.</span></span>
1. <span data-ttu-id="660b8-163">**ヘッダー** ダイアログ ボックスで、ヘッダー テキストを追加し、ヘッダー レベルを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="660b8-164">**リッチ テキスト**で、必要に応じてテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="660b8-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="660b8-165">**アクション リンクの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="660b8-166">**アクション リンク** ダイアログ ボックスで、リンク テキスト、リンク URL、およびリンクの ARIA ラベルを追加し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="660b8-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="660b8-167">ページを保存して、プレビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="660b8-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="660b8-168">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="660b8-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="660b8-169">追加リソース</span><span class="sxs-lookup"><span data-stu-id="660b8-169">Additional resources</span></span>

[<span data-ttu-id="660b8-170">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="660b8-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="660b8-171">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="660b8-172">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="660b8-173">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="660b8-174">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="660b8-175">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="660b8-176">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="660b8-176">Video player module</span></span>](add-video-player.md)
