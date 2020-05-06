---
title: プロモーション バナー モジュール
description: このトピックでは、プロモーション バナー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269777"
---
# <a name="promo-banner-module"></a><span data-ttu-id="13c9c-103">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="13c9c-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="13c9c-104">このトピックでは、プロモーション バナー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="13c9c-105">概要</span><span class="sxs-lookup"><span data-stu-id="13c9c-105">Overview</span></span>

<span data-ttu-id="13c9c-106">プロモーション バナー モジュールは、ページにインライン情報メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="13c9c-107">電子商取引サイトのすべてのページに表示される、サイト全体のプロモーションを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="13c9c-108">プロモーション バナー モジュールは、テキストメッセージおよびリンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="13c9c-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="13c9c-109">プロモーション バナー モジュールに複数のメッセージが追加された場合、すべてのメッセージを循環して表示する、入れ替えカルーセル バナーになります。</span><span class="sxs-lookup"><span data-stu-id="13c9c-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="13c9c-110">プロモーション バナー モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="13c9c-111">E コマースのプロモーション バナーの使用例</span><span class="sxs-lookup"><span data-stu-id="13c9c-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="13c9c-112">次の例に示すように、プロモーション バナーをサイト ヘッダーに使用して、サイト全体のプロモーションまたはメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="13c9c-113">"年間販売は残り 10 日間"</span><span class="sxs-lookup"><span data-stu-id="13c9c-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="13c9c-114">"新学期割引でお買い得。</span><span class="sxs-lookup"><span data-stu-id="13c9c-114">"Save big with back to school sale.</span></span> <span data-ttu-id="13c9c-115">今がチャンス。"</span><span class="sxs-lookup"><span data-stu-id="13c9c-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="13c9c-116">プロモーション バナー モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="13c9c-116">Promo banner module properties</span></span>

| <span data-ttu-id="13c9c-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="13c9c-117">Property name</span></span>             | <span data-ttu-id="13c9c-118">Value</span><span class="sxs-lookup"><span data-stu-id="13c9c-118">Value</span></span>                              | <span data-ttu-id="13c9c-119">説明</span><span class="sxs-lookup"><span data-stu-id="13c9c-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="13c9c-120">バナー メッセージ</span><span class="sxs-lookup"><span data-stu-id="13c9c-120">Banner messages</span></span>           | <span data-ttu-id="13c9c-121">テキストとリンク</span><span class="sxs-lookup"><span data-stu-id="13c9c-121">Text and links</span></span>                     | <span data-ttu-id="13c9c-122">テキストおよびリンクの配列。</span><span class="sxs-lookup"><span data-stu-id="13c9c-122">An array of text and links.</span></span> |
| <span data-ttu-id="13c9c-123">自動再生</span><span class="sxs-lookup"><span data-stu-id="13c9c-123">Autoplay</span></span>                  | <span data-ttu-id="13c9c-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="13c9c-124">**True** or **False**</span></span>              | <span data-ttu-id="13c9c-125">複数のメッセージがコンフィギュレーションされている場合に、メッセージが自動的に循環するかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="13c9c-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="13c9c-126">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="13c9c-126">Slide transition interval</span></span> | <span data-ttu-id="13c9c-127">ミリ秒数 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="13c9c-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="13c9c-128">メッセージを循環するために使用される間隔。</span><span class="sxs-lookup"><span data-stu-id="13c9c-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="13c9c-129">すべて無視</span><span class="sxs-lookup"><span data-stu-id="13c9c-129">Allow dismiss</span></span>             | <span data-ttu-id="13c9c-130">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="13c9c-130">**True** or **False**</span></span>              | <span data-ttu-id="13c9c-131">値が **True** に設定されている場合、顧客は警告を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="13c9c-132">カルーセル フリッパーを表示する</span><span class="sxs-lookup"><span data-stu-id="13c9c-132">Show carousel flipper</span></span>     | <span data-ttu-id="13c9c-133">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="13c9c-133">**True** or **False**</span></span>              | <span data-ttu-id="13c9c-134">カルーセル フリッパーを表示するかどうかを示す値なので、顧客は複数のバナー項目を手動で切り替えて、循環させることができます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="13c9c-135">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="13c9c-135">Text alignment</span></span>            | <span data-ttu-id="13c9c-136">**右**、**左**、または**中央**</span><span class="sxs-lookup"><span data-stu-id="13c9c-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="13c9c-137">プロモーション バナー モジュールのテキスト配置。</span><span class="sxs-lookup"><span data-stu-id="13c9c-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="13c9c-138">リンク</span><span class="sxs-lookup"><span data-stu-id="13c9c-138">Link</span></span>                      | <span data-ttu-id="13c9c-139">URL</span><span class="sxs-lookup"><span data-stu-id="13c9c-139">A URL</span></span>                              | <span data-ttu-id="13c9c-140">オプション リンクの URL</span><span class="sxs-lookup"><span data-stu-id="13c9c-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="13c9c-141">プロモーション バナー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="13c9c-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="13c9c-142">ページにプロモーション バナー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="13c9c-143">**新規** を選択して、ページのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="13c9c-144">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**プロモーション バナーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="13c9c-145">**ページ アウトライン**で、**既定のページ** モジュールを**本文**スロットに追加します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="13c9c-146">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="13c9c-147">作成したテンプレートを使用して、**プロモーション バナー ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="13c9c-148">新しいページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="13c9c-149">右側のウィンドウで、**幅**の値を**全コンテナー**に設定します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="13c9c-150">**ページ アウトライン**で、プロモーション バナー モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="13c9c-151">バナー モジュールの設定で、1 つ以上のバナー メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="13c9c-152">各メッセージには、リンクと共にテキストを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-152">Each message can have text together with a link.</span></span> <span data-ttu-id="13c9c-153">モジュールをさらにカスタマイズする場合は、他のプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="13c9c-154">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="13c9c-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="13c9c-155">ページの上部に、追加したテキストが表示された警告が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="13c9c-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="13c9c-156">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="13c9c-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="13c9c-157">プロモーション バナーは、通常、ページ ヘッダー スロットまたはサブヘッダー スロットで使用されます。</span><span class="sxs-lookup"><span data-stu-id="13c9c-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="13c9c-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="13c9c-158">Additional resources</span></span>

[<span data-ttu-id="13c9c-159">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="13c9c-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13c9c-160">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="13c9c-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="13c9c-161">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="13c9c-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="13c9c-162">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="13c9c-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="13c9c-163">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="13c9c-163">Video player module</span></span>](add-video-player.md)
