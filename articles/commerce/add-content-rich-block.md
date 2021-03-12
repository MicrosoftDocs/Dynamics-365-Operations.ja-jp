---
title: テキスト ブロック モジュール
description: このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cad6a26ea1858d6afac33ef8eab10e16b404035b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980484"
---
# <a name="text-block-module"></a><span data-ttu-id="2a907-103">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="2a907-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a907-104">このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2a907-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2a907-105">概要</span><span class="sxs-lookup"><span data-stu-id="2a907-105">Overview</span></span>

<span data-ttu-id="2a907-106">テキスト ブロック モジュールは、テキスト コンテンツを追加するために使用されるモジュールです。</span><span class="sxs-lookup"><span data-stu-id="2a907-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="2a907-107">このコンテンツは、情報提供またはプロモーションです。</span><span class="sxs-lookup"><span data-stu-id="2a907-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="2a907-108">テキスト ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="2a907-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2a907-109">これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="2a907-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="2a907-110">E コマースのテキスト ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="2a907-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="2a907-111">テキスト ブロック モジュールは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2a907-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="2a907-112">製品の詳細ページで製品機能について紹介します。</span><span class="sxs-lookup"><span data-stu-id="2a907-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="2a907-113">任意のページで情報提供を目的とします。</span><span class="sxs-lookup"><span data-stu-id="2a907-113">For informational purposes on any page.</span></span> <span data-ttu-id="2a907-114">たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。</span><span class="sxs-lookup"><span data-stu-id="2a907-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="2a907-115">製品の詳細ページでカスタム メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a907-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="2a907-116">(たとえば、"$50 以上のご注文で送料無料")。</span><span class="sxs-lookup"><span data-stu-id="2a907-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="2a907-117">製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。</span><span class="sxs-lookup"><span data-stu-id="2a907-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="2a907-118">以下の図は、ホームページ上のテキスト ブロック モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2a907-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![テキスト ブロック モジュールの例](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="2a907-120">テキスト ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="2a907-120">Text block module properties</span></span>

| <span data-ttu-id="2a907-121">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="2a907-121">Property name</span></span>     | <span data-ttu-id="2a907-122">先頭値</span><span class="sxs-lookup"><span data-stu-id="2a907-122">Value</span></span>                                            | <span data-ttu-id="2a907-123">説明</span><span class="sxs-lookup"><span data-stu-id="2a907-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="2a907-124">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="2a907-124">Rich text</span></span>         | <span data-ttu-id="2a907-125">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="2a907-125">Rich text</span></span>                                        | <span data-ttu-id="2a907-126">段落のテキスト。</span><span class="sxs-lookup"><span data-stu-id="2a907-126">Paragraph text.</span></span> <span data-ttu-id="2a907-127">太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2a907-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="2a907-128">カスタム クラス名</span><span class="sxs-lookup"><span data-stu-id="2a907-128">Custom class name</span></span> | <span data-ttu-id="2a907-129">カスケード スタイル シート (CSS) クラス名</span><span class="sxs-lookup"><span data-stu-id="2a907-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="2a907-130">開発者がこのモジュールをフォーマットするために提供するカスタム CSS クラス名。</span><span class="sxs-lookup"><span data-stu-id="2a907-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="2a907-131">クラス名は、テーマ パックで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a907-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="2a907-132">フォント サイズ</span><span class="sxs-lookup"><span data-stu-id="2a907-132">Font size</span></span>         | <span data-ttu-id="2a907-133">**小**、**中**、**大**、または **特大**</span><span class="sxs-lookup"><span data-stu-id="2a907-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="2a907-134">コンテンツのフォント サイズ。</span><span class="sxs-lookup"><span data-stu-id="2a907-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="2a907-135">テキスト ブロック モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="2a907-135">Add a text block module to a page</span></span>

<span data-ttu-id="2a907-136">新しいページテキスト ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2a907-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2a907-137">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="2a907-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2a907-138">**テンプレート名** 配下の **新規テンプレート**  ダイアログ ボックスに、**コンテンツ テンプレート** を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a907-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="2a907-139">**本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a907-140">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a907-141">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="2a907-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2a907-142">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="2a907-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2a907-143">**テンプレートの選択** ダイアログ ボックスで、**コンテンツ テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="2a907-144">**ページ名** 配下で、 **コンテンツ テンプレート** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2a907-145">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a907-146">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2a907-147">コンテナー モジュールのプロパティ ウィンドウで、**幅** プロパティを **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2a907-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2a907-148">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a907-149">**モジュールの追加** ダイアログ ボックスで、**テキスト ブロック** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a907-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="2a907-150">テキスト ブロック モジュールのプロパティ ウィンドウで、**リッチ テキスト** フィールドにテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a907-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="2a907-151">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="2a907-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2a907-152">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="2a907-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a907-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2a907-153">Additional resources</span></span>

[<span data-ttu-id="2a907-154">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="2a907-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2a907-155">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="2a907-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2a907-156">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="2a907-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2a907-157">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="2a907-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2a907-158">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="2a907-158">Video player module</span></span>](add-video-player.md)

