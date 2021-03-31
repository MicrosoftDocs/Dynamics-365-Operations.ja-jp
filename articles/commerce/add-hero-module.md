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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad95dc943f075e088f5e13b507fa08f11548282f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206274"
---
# <a name="content-block-module"></a><span data-ttu-id="4cff3-103">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="4cff3-103">Content block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4cff3-104">このトピックでは、コンテンツ ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4cff3-105">画像とテキストの組み合わせを通じて製品またはプロモーションをマーケティングするために、コンテンツ ブロック モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-105">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="4cff3-106">たとえば、小売業者は E コマース サイトのホーム ページにコンテンツ ブロック モジュールを追加して、新しい製品を販売促進し、顧客の注意を引き付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-106">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="4cff3-107">コンテンツ ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-107">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="4cff3-108">ページでその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="4cff3-108">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="4cff3-109">コンテンツ ブロック モジュールは、小売業者がマーケティングまたは販売促進を行う (製品、販売、機能など) サイト ページに配置することができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-109">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="4cff3-110">E コマースのコンテンツ ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="4cff3-110">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="4cff3-111">コンテンツ ブロック モジュールは、E コマース サイトのホーム ページで使用して、プロモーションや新製品を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-111">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="4cff3-112">製品の詳細ページでコンテンツ ブロック モジュールを使用して、製品情報を紹介することができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-112">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="4cff3-113">複数のコンテンツ ブロック モジュールをカルーセル モジュール内に配置することにより、複数の製品またはプロモーションを強調表示できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-113">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="4cff3-114">コンテンツ ブロック モジュールとテーマ</span><span class="sxs-lookup"><span data-stu-id="4cff3-114">Content block modules and themes</span></span>

<span data-ttu-id="4cff3-115">コンテンツ ブロック モジュールは、テーマに基づく各種レイアウトおよびスタイルをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-115">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="4cff3-116">たとえば、Fabrikam のテーマは、コンテンツ ブロック モジュールの 3 つのレイアウト (ヒーロー、フィーチャー、およびタイル) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4cff3-116">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="4cff3-117">ヒーロー レイアウトでは、背景上にテキストが重なって画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-117">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="4cff3-118">フィーチャー レイアウトでは、画像とテキストが並べて表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-118">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="4cff3-119">タイル レイアウトでは、タイル形式で複数のコンテンツ ブロックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-119">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="4cff3-120">さらに、テーマによって、各レイアウトのさまざまなプロパティを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-120">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="4cff3-121">テーマの開発者は、コンテンツ ブロック モジュールを使用して、さらに多くのスタイルを持つレイアウトをさらに作成できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-121">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="4cff3-122">次の図は、ヒーロー レイアウトを備えたコンテンツ ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4cff3-122">The following image shows an example of a content block module with a hero layout.</span></span>

![ヒーロー モジュールの例](./media/Hero.PNG)

<span data-ttu-id="4cff3-124">次の図は、フィーチャー レイアウトを備えたコンテンツ ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="4cff3-124">The following image shows an example of a content block module with a feature layout.</span></span>

![機能モジュールの例](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="4cff3-126">コンテンツ ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cff3-126">Content block module properties</span></span>

| <span data-ttu-id="4cff3-127">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="4cff3-127">Property name</span></span>  | <span data-ttu-id="4cff3-128">値</span><span class="sxs-lookup"><span data-stu-id="4cff3-128">Values</span></span> | <span data-ttu-id="4cff3-129">説明</span><span class="sxs-lookup"><span data-stu-id="4cff3-129">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4cff3-130">画像</span><span class="sxs-lookup"><span data-stu-id="4cff3-130">Image</span></span>          | <span data-ttu-id="4cff3-131">イメージ ファイル</span><span class="sxs-lookup"><span data-stu-id="4cff3-131">Image file</span></span> | <span data-ttu-id="4cff3-132">画像を使用して製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-132">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="4cff3-133">画像を画像ギャラリーにアップロードしたり、既存の画像を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-133">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="4cff3-134">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4cff3-134">Heading</span></span>        | <span data-ttu-id="4cff3-135">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="4cff3-135">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4cff3-136">各ヒーロー モジュールにヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-136">Every hero module can have a heading.</span></span> <span data-ttu-id="4cff3-137">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-137">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="4cff3-138">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-138">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="4cff3-139">段落</span><span class="sxs-lookup"><span data-stu-id="4cff3-139">Paragraph</span></span>      | <span data-ttu-id="4cff3-140">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="4cff3-140">Paragraph text</span></span> | <span data-ttu-id="4cff3-141">ヒーロー モジュールは、リッチ テキスト形式の段落テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4cff3-141">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="4cff3-142">太字、下線付き、斜体、およびハイパーリンクなど、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-142">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="4cff3-143">これらの機能の一部は、モジュールに適用されるページ テーマによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4cff3-143">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="4cff3-144">リンク</span><span class="sxs-lookup"><span data-stu-id="4cff3-144">Link</span></span>           | <span data-ttu-id="4cff3-145">リンク テキスト、リンク URL、アクセス可能リッチ インターネット アプリケーション (ARIA) ラベル、および **新しいタブでリンクを開く**</span><span class="sxs-lookup"><span data-stu-id="4cff3-145">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="4cff3-146">ヒーロー モジュールは、1 つ以上の "アクションの呼び出し" リンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4cff3-146">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="4cff3-147">リンクを追加すると、リンク テキスト、URL、および ARIA ラベルが必要になります。</span><span class="sxs-lookup"><span data-stu-id="4cff3-147">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="4cff3-148">ARIA ラベルは、アクセシビリティ要件を満たしていることを説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cff3-148">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="4cff3-149">リンクをコンフィギュレーションして、新しいタブで開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-149">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="4cff3-150">Fabrikam テーマによって公開されるコンテンツ ブロック モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="4cff3-150">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="4cff3-151">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="4cff3-151">Property name</span></span>  | <span data-ttu-id="4cff3-152">値</span><span class="sxs-lookup"><span data-stu-id="4cff3-152">Values</span></span> | <span data-ttu-id="4cff3-153">説明</span><span class="sxs-lookup"><span data-stu-id="4cff3-153">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4cff3-154">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="4cff3-154">Text placement</span></span> | <span data-ttu-id="4cff3-155">**左**、**右**、**中央**</span><span class="sxs-lookup"><span data-stu-id="4cff3-155">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="4cff3-156">このプロパティは、画像上のテキストの位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-156">This property defines the position of the text on the image.</span></span> <span data-ttu-id="4cff3-157">ヒーロー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-157">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="4cff3-158">テキストのテーマ</span><span class="sxs-lookup"><span data-stu-id="4cff3-158">Text theme</span></span>     | <span data-ttu-id="4cff3-159">**明るい** または **暗い**</span><span class="sxs-lookup"><span data-stu-id="4cff3-159">**Light** or **Dark**</span></span> | <span data-ttu-id="4cff3-160">背景画像に基づいて、テキストに対する配色を定義できます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-160">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="4cff3-161">たとえば、画像の背景が暗い場合、明るいテーマを適用してテキストを表示より見やすくし、アクセシビリティ目的で色のコントラスト比を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-161">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="4cff3-162">ヒーロー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-162">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="4cff3-163">画像の配置</span><span class="sxs-lookup"><span data-stu-id="4cff3-163">Image placement</span></span>       | <span data-ttu-id="4cff3-164">**左**、**右**</span><span class="sxs-lookup"><span data-stu-id="4cff3-164">**Left**,  **Right**</span></span> | <span data-ttu-id="4cff3-165">このプロパティは、画像をテキストの左に表示するか、右に表示するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-165">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="4cff3-166">フィーチャー レイアウトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cff3-166">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="4cff3-167">コンテンツ ブロック モジュールを新しいページに追加する</span><span class="sxs-lookup"><span data-stu-id="4cff3-167">Add a content block module to a new page</span></span>

<span data-ttu-id="4cff3-168">新しいページにヒーロー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-168">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4cff3-169">**テンプレート** に移動して、**コンテンツ ブロック テンプレート** という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-169">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="4cff3-170">既定のページの **メイン** スロットで、ヒーロー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-170">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="4cff3-171">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-171">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4cff3-172">作成したヒーロー テンプレートを使用して、**コンテンツ ブロック ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-172">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="4cff3-173">既定のページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-173">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4cff3-174">**モジュールの追加** ダイアログ ボックスの、**モジュールの選択** で、ヒーロー モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-174">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="4cff3-175">左側のアウトライン ツリーで、コンテンツ ブロック モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-175">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="4cff3-176">右側のプロパティ ウィンドウで、**画像の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-176">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="4cff3-177">次に、既存の画像を選択するか、新しい画像をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="4cff3-177">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="4cff3-178">**ヘッダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-178">Select **Heading**.</span></span>
1. <span data-ttu-id="4cff3-179">**ヘッダー** ダイアログ ボックスで、ヘッダー テキストを追加し、ヘッダー レベルを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-179">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="4cff3-180">**リッチ テキスト** で、必要に応じてテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-180">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="4cff3-181">**リンクの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-181">Select **Add Link**.</span></span>
1. <span data-ttu-id="4cff3-182">**リンク** ダイアログ ボックスで、リンク テキスト、リンク URL、およびリンクの ARIA ラベルを追加し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-182">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="4cff3-183">**ヒーロー** レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-183">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="4cff3-184">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="4cff3-184">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="4cff3-185">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="4cff3-185">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4cff3-186">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4cff3-186">Additional resources</span></span>

[<span data-ttu-id="4cff3-187">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="4cff3-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4cff3-188">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="4cff3-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="4cff3-189">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="4cff3-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4cff3-190">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="4cff3-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4cff3-191">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="4cff3-191">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]