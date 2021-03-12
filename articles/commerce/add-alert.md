---
title: プロモーション バナー モジュール
description: このトピックでは、プロモーション バナー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
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
ms.openlocfilehash: a77196be69bb71d917bf84c633199a3af3fbf478
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986032"
---
# <a name="promo-banner-module"></a><span data-ttu-id="d67c8-103">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="d67c8-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d67c8-104">このトピックでは、プロモーション バナー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d67c8-105">概要</span><span class="sxs-lookup"><span data-stu-id="d67c8-105">Overview</span></span>

<span data-ttu-id="d67c8-106">プロモーション バナー モジュールは、ページにインライン情報メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="d67c8-107">電子商取引サイトのすべてのページに表示される、サイト全体のプロモーションを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="d67c8-108">プロモーション バナー モジュールは、テキストメッセージおよびリンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d67c8-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="d67c8-109">プロモーション バナー モジュールに複数のメッセージが追加された場合、すべてのメッセージを循環して表示する、入れ替えカルーセル バナーになります。</span><span class="sxs-lookup"><span data-stu-id="d67c8-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="d67c8-110">プロモーション バナー モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="d67c8-111">E コマースのプロモーション バナーの使用例</span><span class="sxs-lookup"><span data-stu-id="d67c8-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="d67c8-112">次の例に示すように、プロモーション バナーをサイト ヘッダーに使用して、サイト全体のプロモーションまたはメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="d67c8-113">"年間販売は残り 10 日間"</span><span class="sxs-lookup"><span data-stu-id="d67c8-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="d67c8-114">"新学期割引でお買い得。</span><span class="sxs-lookup"><span data-stu-id="d67c8-114">"Save big with back to school sale.</span></span> <span data-ttu-id="d67c8-115">今がチャンス。"</span><span class="sxs-lookup"><span data-stu-id="d67c8-115">Shop Now."</span></span>

<span data-ttu-id="d67c8-116">「感謝祭特別セールを開催中！」</span><span class="sxs-lookup"><span data-stu-id="d67c8-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="d67c8-117">次の図は、プロモーション バナーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="d67c8-117">The following image shows an example of a promo banner.</span></span>

![プロモーション バナー モジュールの例](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="d67c8-119">プロモーション バナー モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="d67c8-119">Promo banner module properties</span></span>

| <span data-ttu-id="d67c8-120">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d67c8-120">Property name</span></span>             | <span data-ttu-id="d67c8-121">先頭値</span><span class="sxs-lookup"><span data-stu-id="d67c8-121">Value</span></span>                              | <span data-ttu-id="d67c8-122">説明</span><span class="sxs-lookup"><span data-stu-id="d67c8-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="d67c8-123">バナー メッセージ</span><span class="sxs-lookup"><span data-stu-id="d67c8-123">Banner messages</span></span>           | <span data-ttu-id="d67c8-124">テキストとリンク</span><span class="sxs-lookup"><span data-stu-id="d67c8-124">Text and links</span></span>                     | <span data-ttu-id="d67c8-125">テキストおよびリンクの配列。</span><span class="sxs-lookup"><span data-stu-id="d67c8-125">An array of text and links.</span></span> |
| <span data-ttu-id="d67c8-126">自動再生</span><span class="sxs-lookup"><span data-stu-id="d67c8-126">Autoplay</span></span>                  | <span data-ttu-id="d67c8-127">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="d67c8-127">**True** or **False**</span></span>              | <span data-ttu-id="d67c8-128">複数のメッセージがコンフィギュレーションされている場合に、メッセージが自動的に循環するかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d67c8-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="d67c8-129">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="d67c8-129">Slide transition interval</span></span> | <span data-ttu-id="d67c8-130">ミリ秒数 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="d67c8-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="d67c8-131">メッセージを循環するために使用される間隔。</span><span class="sxs-lookup"><span data-stu-id="d67c8-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="d67c8-132">すべて無視</span><span class="sxs-lookup"><span data-stu-id="d67c8-132">Allow dismiss</span></span>             | <span data-ttu-id="d67c8-133">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="d67c8-133">**True** or **False**</span></span>              | <span data-ttu-id="d67c8-134">値が **True** に設定されている場合、顧客は警告を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="d67c8-135">カルーセル フリッパーを表示する</span><span class="sxs-lookup"><span data-stu-id="d67c8-135">Show carousel flipper</span></span>     | <span data-ttu-id="d67c8-136">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="d67c8-136">**True** or **False**</span></span>              | <span data-ttu-id="d67c8-137">カルーセル フリッパーを表示するかどうかを示す値なので、顧客は複数のバナー項目を手動で切り替えて、循環させることができます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="d67c8-138">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="d67c8-138">Text alignment</span></span>            | <span data-ttu-id="d67c8-139">**右**、**左**、または **中央**</span><span class="sxs-lookup"><span data-stu-id="d67c8-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="d67c8-140">プロモーション バナー モジュールのテキスト配置。</span><span class="sxs-lookup"><span data-stu-id="d67c8-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="d67c8-141">リンク</span><span class="sxs-lookup"><span data-stu-id="d67c8-141">Link</span></span>                      | <span data-ttu-id="d67c8-142">URL</span><span class="sxs-lookup"><span data-stu-id="d67c8-142">A URL</span></span>                              | <span data-ttu-id="d67c8-143">オプション リンクの URL</span><span class="sxs-lookup"><span data-stu-id="d67c8-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="d67c8-144">プロモーション バナー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="d67c8-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="d67c8-145">ページにプロモーション バナー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d67c8-146">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d67c8-147">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**プロモーション バナーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d67c8-148">**ページ アウトライン** で、**既定のページ** モジュールを **本文** スロットに追加します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="d67c8-149">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="d67c8-150">作成したテンプレートを使用して、**プロモーション バナー ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="d67c8-151">新しいページの **メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="d67c8-152">右側のウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="d67c8-153">**ページ アウトライン** で、プロモーション バナー モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="d67c8-154">バナー モジュールの設定で、1 つ以上のバナー メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="d67c8-155">各メッセージには、リンクと共にテキストを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-155">Each message can have text together with a link.</span></span> <span data-ttu-id="d67c8-156">モジュールをさらにカスタマイズする場合は、他のプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="d67c8-157">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="d67c8-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="d67c8-158">ページの上部に、追加したテキストが表示された警告が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d67c8-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="d67c8-159">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="d67c8-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="d67c8-160">プロモーション バナーは、通常、ページ ヘッダー スロットまたはサブヘッダー スロットで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d67c8-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d67c8-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d67c8-161">Additional resources</span></span>

[<span data-ttu-id="d67c8-162">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="d67c8-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d67c8-163">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="d67c8-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d67c8-164">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="d67c8-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d67c8-165">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="d67c8-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="d67c8-166">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="d67c8-166">Video player module</span></span>](add-video-player.md)
