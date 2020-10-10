---
title: コンテンツ ブロック モジュール
description: このトピックでは、コンテンツ ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 7a8b1c214ba31b7c47cecbe67bef493f5fa450fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817357"
---
# <a name="content-block-module"></a><span data-ttu-id="36ec9-103">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="36ec9-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="36ec9-104">このトピックでは、コンテンツ ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36ec9-105">概要</span><span class="sxs-lookup"><span data-stu-id="36ec9-105">Overview</span></span>

<span data-ttu-id="36ec9-106">画像とテキストの組み合わせを通じて製品またはプロモーションをマーケティングするために、コンテンツ ブロック モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="36ec9-107">たとえば、小売業者は E コマース サイトのホーム ページにコンテンツ ブロック モジュールを追加して、新しい製品を販売促進し、顧客の注意を引き付けることができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="36ec9-108">コンテンツ ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="36ec9-109">ページでその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="36ec9-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="36ec9-110">コンテンツ ブロック モジュールは、小売業者がマーケティングまたは販売促進を行う (製品、販売、機能など) サイト ページに配置することができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="36ec9-111">E コマースのコンテンツ ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="36ec9-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="36ec9-112">コンテンツ ブロック モジュールは、E コマース サイトのホーム ページで使用して、プロモーションや新製品を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="36ec9-113">製品の詳細ページでコンテンツ ブロック モジュールを使用して、製品情報を紹介することができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="36ec9-114">複数のコンテンツ ブロック モジュールをカルーセル モジュール内に配置することにより、複数の製品またはプロモーションを強調表示できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="36ec9-115">コンテンツ ブロック モジュールとテーマ</span><span class="sxs-lookup"><span data-stu-id="36ec9-115">Content block modules and themes</span></span>

<span data-ttu-id="36ec9-116">コンテンツ ブロック モジュールは、テーマに基づく各種レイアウトおよびスタイルをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="36ec9-117">たとえば、Fabrikam のテーマは、コンテンツ ブロック モジュールの 3 つのレイアウト (ヒーロー、フィーチャー、およびタイル) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="36ec9-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="36ec9-118">ヒーロー レイアウトでは、背景上にテキストが重なって画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="36ec9-119">フィーチャー レイアウトでは、画像とテキストが並べて表示されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="36ec9-120">タイル レイアウトでは、タイル形式で複数のコンテンツ ブロックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="36ec9-121">さらに、テーマによって、各レイアウトのさまざまなプロパティを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="36ec9-122">テーマの開発者は、コンテンツ ブロック モジュールを使用して、さらに多くのスタイルを持つレイアウトをさらに作成できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="36ec9-123">次の図は、ヒーロー レイアウトを備えたコンテンツ ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="36ec9-123">The following image shows an example of a content block module with a hero layout.</span></span>

![ヒーロー モジュールの例](./media/Hero.PNG)

<span data-ttu-id="36ec9-125">次の図は、フィーチャー レイアウトを備えたコンテンツ ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="36ec9-125">The following image shows an example of a content block module with a feature layout.</span></span>

![機能モジュールの例](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="36ec9-127">コンテンツ ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="36ec9-127">Content block module properties</span></span>

| <span data-ttu-id="36ec9-128">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="36ec9-128">Property name</span></span>  | <span data-ttu-id="36ec9-129">値</span><span class="sxs-lookup"><span data-stu-id="36ec9-129">Values</span></span> | <span data-ttu-id="36ec9-130">説明</span><span class="sxs-lookup"><span data-stu-id="36ec9-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="36ec9-131">画像</span><span class="sxs-lookup"><span data-stu-id="36ec9-131">Image</span></span>          | <span data-ttu-id="36ec9-132">イメージ ファイル</span><span class="sxs-lookup"><span data-stu-id="36ec9-132">Image file</span></span> | <span data-ttu-id="36ec9-133">画像を使用して製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="36ec9-134">画像を画像ギャラリーにアップロードしたり、既存の画像を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="36ec9-135">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="36ec9-135">Heading</span></span>        | <span data-ttu-id="36ec9-136">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="36ec9-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="36ec9-137">各ヒーロー モジュールにヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-137">Every hero module can have a heading.</span></span> <span data-ttu-id="36ec9-138">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="36ec9-139">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="36ec9-140">段落</span><span class="sxs-lookup"><span data-stu-id="36ec9-140">Paragraph</span></span>      | <span data-ttu-id="36ec9-141">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="36ec9-141">Paragraph text</span></span> | <span data-ttu-id="36ec9-142">ヒーロー モジュールは、リッチ テキスト形式の段落テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="36ec9-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="36ec9-143">太字、下線付き、斜体、およびハイパーリンクなど、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="36ec9-144">これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="36ec9-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="36ec9-145">リンク</span><span class="sxs-lookup"><span data-stu-id="36ec9-145">Link</span></span>           | <span data-ttu-id="36ec9-146">リンク テキスト、リンク URL、アクセス可能リッチ インターネット アプリケーション (ARIA) ラベル、および **新しいタブでリンクを開く**</span><span class="sxs-lookup"><span data-stu-id="36ec9-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="36ec9-147">ヒーロー モジュールは、1 つ以上の "アクションの呼び出し" リンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="36ec9-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="36ec9-148">リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。</span><span class="sxs-lookup"><span data-stu-id="36ec9-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="36ec9-149">ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36ec9-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="36ec9-150">リンクをコンフィギュレーションして、新しいタブで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="36ec9-151">Fabrikam テーマによって公開されるコンテンツ ブロック モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="36ec9-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="36ec9-152">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="36ec9-152">Property name</span></span>  | <span data-ttu-id="36ec9-153">値</span><span class="sxs-lookup"><span data-stu-id="36ec9-153">Values</span></span> | <span data-ttu-id="36ec9-154">説明</span><span class="sxs-lookup"><span data-stu-id="36ec9-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="36ec9-155">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="36ec9-155">Text placement</span></span> | <span data-ttu-id="36ec9-156">**左**、**右**、**中央**</span><span class="sxs-lookup"><span data-stu-id="36ec9-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="36ec9-157">このプロパティは、画像上のテキストの位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="36ec9-158">ヒーロー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="36ec9-159">テキストのテーマ</span><span class="sxs-lookup"><span data-stu-id="36ec9-159">Text theme</span></span>     | <span data-ttu-id="36ec9-160">**明るい**または**暗い**</span><span class="sxs-lookup"><span data-stu-id="36ec9-160">**Light** or **Dark**</span></span> | <span data-ttu-id="36ec9-161">背景画像に基づいて、テキストに対する配色を定義できます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="36ec9-162">たとえば、画像の背景が暗い場合、明るいテーマを適用してテキストを表示より見やすくし、アクセシビリティ目的で色のコントラスト比を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="36ec9-163">ヒーロー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="36ec9-164">画像の配置</span><span class="sxs-lookup"><span data-stu-id="36ec9-164">Image placement</span></span>       | <span data-ttu-id="36ec9-165">**左**、**右**</span><span class="sxs-lookup"><span data-stu-id="36ec9-165">**Left**,  **Right**</span></span> | <span data-ttu-id="36ec9-166">このプロパティは、画像をテキストの左に表示するか、右に表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="36ec9-167">フィーチャー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="36ec9-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="36ec9-168">コンテンツ ブロック モジュールを新しいページに追加する</span><span class="sxs-lookup"><span data-stu-id="36ec9-168">Add a content block module to a new page</span></span>

<span data-ttu-id="36ec9-169">新しいページにヒーロー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="36ec9-170">**テンプレート** に移動して、**コンテンツ ブロック テンプレート** という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="36ec9-171">既定のページの**メイン** スロットで、ヒーロー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="36ec9-172">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="36ec9-173">作成したヒーロー テンプレートを使用して、**コンテンツ ブロック ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="36ec9-174">既定のページの**メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="36ec9-175">**モジュールの追加**ダイアログ ボックスの、**モジュールの選択**で、ヒーロー モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="36ec9-176">左側のアウトライン ツリーで、コンテンツ ブロック モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="36ec9-177">右側のプロパティ ウィンドウで、**画像の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="36ec9-178">次に、既存の画像を選択するか、新しい画像をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="36ec9-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="36ec9-179">**ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-179">Select **Heading**.</span></span>
1. <span data-ttu-id="36ec9-180">**ヘッダー** ダイアログ ボックスで、ヘッダー テキストを追加し、ヘッダー レベルを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="36ec9-181">**リッチ テキスト**で、必要に応じてテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="36ec9-182">**リンクの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="36ec9-183">**リンク** ダイアログ ボックスで、リンク テキスト、リンク URL、およびリンクの ARIA ラベルを追加し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="36ec9-184">**ヒーロー** レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="36ec9-185">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="36ec9-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="36ec9-186">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="36ec9-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="36ec9-187">追加リソース</span><span class="sxs-lookup"><span data-stu-id="36ec9-187">Additional resources</span></span>

[<span data-ttu-id="36ec9-188">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="36ec9-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="36ec9-189">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="36ec9-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="36ec9-190">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="36ec9-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="36ec9-191">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="36ec9-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="36ec9-192">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="36ec9-192">Video player module</span></span>](add-video-player.md)
