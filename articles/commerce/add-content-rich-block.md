---
title: テキスト ブロック モジュール
description: このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797770"
---
# <a name="text-block-module"></a><span data-ttu-id="16c49-103">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="16c49-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16c49-104">このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16c49-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="16c49-105">テキスト ブロック モジュールは、テキスト コンテンツを追加するために使用されるモジュールです。</span><span class="sxs-lookup"><span data-stu-id="16c49-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="16c49-106">このコンテンツは、情報提供またはプロモーションです。</span><span class="sxs-lookup"><span data-stu-id="16c49-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="16c49-107">テキスト ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="16c49-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="16c49-108">これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="16c49-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="16c49-109">E コマースのテキスト ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="16c49-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="16c49-110">テキスト ブロック モジュールは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="16c49-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="16c49-111">製品の詳細ページで製品機能について紹介します。</span><span class="sxs-lookup"><span data-stu-id="16c49-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="16c49-112">任意のページで情報提供を目的とします。</span><span class="sxs-lookup"><span data-stu-id="16c49-112">For informational purposes on any page.</span></span> <span data-ttu-id="16c49-113">たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。</span><span class="sxs-lookup"><span data-stu-id="16c49-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="16c49-114">製品の詳細ページでカスタム メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="16c49-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="16c49-115">(たとえば、"$50 以上のご注文で送料無料")。</span><span class="sxs-lookup"><span data-stu-id="16c49-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="16c49-116">製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。</span><span class="sxs-lookup"><span data-stu-id="16c49-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="16c49-117">以下の図は、ホームページ上のテキスト ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="16c49-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![テキスト ブロック モジュールの例](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="16c49-119">テキスト ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="16c49-119">Text block module properties</span></span>

| <span data-ttu-id="16c49-120">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="16c49-120">Property name</span></span>     | <span data-ttu-id="16c49-121">先頭値</span><span class="sxs-lookup"><span data-stu-id="16c49-121">Value</span></span>                                            | <span data-ttu-id="16c49-122">説明</span><span class="sxs-lookup"><span data-stu-id="16c49-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="16c49-123">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="16c49-123">Rich text</span></span>         | <span data-ttu-id="16c49-124">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="16c49-124">Rich text</span></span>                                        | <span data-ttu-id="16c49-125">段落のテキスト。</span><span class="sxs-lookup"><span data-stu-id="16c49-125">Paragraph text.</span></span> <span data-ttu-id="16c49-126">太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="16c49-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="16c49-127">カスタム クラス名</span><span class="sxs-lookup"><span data-stu-id="16c49-127">Custom class name</span></span> | <span data-ttu-id="16c49-128">カスケード スタイル シート (CSS) クラス名</span><span class="sxs-lookup"><span data-stu-id="16c49-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="16c49-129">開発者がこのモジュールをフォーマットするために提供するカスタム CSS クラス名。</span><span class="sxs-lookup"><span data-stu-id="16c49-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="16c49-130">クラス名は、テーマ パックで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16c49-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="16c49-131">フォント サイズ</span><span class="sxs-lookup"><span data-stu-id="16c49-131">Font size</span></span>         | <span data-ttu-id="16c49-132">**小**、**中**、**大**、または **特大**</span><span class="sxs-lookup"><span data-stu-id="16c49-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="16c49-133">コンテンツのフォント サイズ。</span><span class="sxs-lookup"><span data-stu-id="16c49-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="16c49-134">テキスト ブロック モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="16c49-134">Add a text block module to a page</span></span>

<span data-ttu-id="16c49-135">新しいページテキスト ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="16c49-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="16c49-136">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="16c49-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="16c49-137">**テンプレート名** 配下の **新規テンプレート**  ダイアログ ボックスに、**コンテンツ テンプレート** を入力します。</span><span class="sxs-lookup"><span data-stu-id="16c49-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="16c49-138">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="16c49-139">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="16c49-140">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="16c49-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="16c49-141">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="16c49-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="16c49-142">**テンプレートの選択** ダイアログ ボックスで、**コンテンツ テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="16c49-143">**ページ名** 配下で、 **コンテンツ テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="16c49-144">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="16c49-145">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="16c49-146">コンテナー モジュールのプロパティ ウィンドウで、**幅** プロパティを **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="16c49-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="16c49-147">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="16c49-148">**モジュールの追加** ダイアログ ボックスで、**テキスト ブロック** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16c49-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="16c49-149">テキスト ブロック モジュールのプロパティ ウィンドウで、**リッチ テキスト** フィールドにテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="16c49-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="16c49-150">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="16c49-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="16c49-151">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="16c49-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16c49-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="16c49-152">Additional resources</span></span>

[<span data-ttu-id="16c49-153">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="16c49-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="16c49-154">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="16c49-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="16c49-155">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="16c49-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="16c49-156">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="16c49-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="16c49-157">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="16c49-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]