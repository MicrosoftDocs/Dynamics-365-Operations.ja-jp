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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206586"
---
# <a name="promo-banner-module"></a><span data-ttu-id="42a4c-103">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="42a4c-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42a4c-104">このトピックでは、プロモーション バナー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42a4c-105">プロモーション バナー モジュールは、ページにインライン情報メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="42a4c-106">電子商取引サイトのすべてのページに表示される、サイト全体のプロモーションを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="42a4c-107">プロモーション バナー モジュールは、テキストメッセージおよびリンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="42a4c-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="42a4c-108">プロモーション バナー モジュールに複数のメッセージが追加された場合、すべてのメッセージを循環して表示する、入れ替えカルーセル バナーになります。</span><span class="sxs-lookup"><span data-stu-id="42a4c-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="42a4c-109">プロモーション バナー モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="42a4c-110">E コマースのプロモーション バナーの使用例</span><span class="sxs-lookup"><span data-stu-id="42a4c-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="42a4c-111">次の例に示すように、プロモーション バナーをサイト ヘッダーに使用して、サイト全体のプロモーションまたはメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="42a4c-112">"年間販売は残り 10 日間"</span><span class="sxs-lookup"><span data-stu-id="42a4c-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="42a4c-113">"新学期割引でお買い得。</span><span class="sxs-lookup"><span data-stu-id="42a4c-113">"Save big with back to school sale.</span></span> <span data-ttu-id="42a4c-114">今がチャンス。"</span><span class="sxs-lookup"><span data-stu-id="42a4c-114">Shop Now."</span></span>

<span data-ttu-id="42a4c-115">「感謝祭特別セールを開催中！」</span><span class="sxs-lookup"><span data-stu-id="42a4c-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="42a4c-116">次の図は、プロモーション バナーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="42a4c-116">The following image shows an example of a promo banner.</span></span>

![プロモーション バナー モジュールの例](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="42a4c-118">プロモーション バナー モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="42a4c-118">Promo banner module properties</span></span>

| <span data-ttu-id="42a4c-119">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="42a4c-119">Property name</span></span>             | <span data-ttu-id="42a4c-120">先頭値</span><span class="sxs-lookup"><span data-stu-id="42a4c-120">Value</span></span>                              | <span data-ttu-id="42a4c-121">説明</span><span class="sxs-lookup"><span data-stu-id="42a4c-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="42a4c-122">バナー メッセージ</span><span class="sxs-lookup"><span data-stu-id="42a4c-122">Banner messages</span></span>           | <span data-ttu-id="42a4c-123">テキストとリンク</span><span class="sxs-lookup"><span data-stu-id="42a4c-123">Text and links</span></span>                     | <span data-ttu-id="42a4c-124">テキストおよびリンクの配列。</span><span class="sxs-lookup"><span data-stu-id="42a4c-124">An array of text and links.</span></span> |
| <span data-ttu-id="42a4c-125">自動再生</span><span class="sxs-lookup"><span data-stu-id="42a4c-125">Autoplay</span></span>                  | <span data-ttu-id="42a4c-126">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="42a4c-126">**True** or **False**</span></span>              | <span data-ttu-id="42a4c-127">複数のメッセージがコンフィギュレーションされている場合に、メッセージが自動的に循環するかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="42a4c-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="42a4c-128">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="42a4c-128">Slide transition interval</span></span> | <span data-ttu-id="42a4c-129">ミリ秒数 (ミリ秒)</span><span class="sxs-lookup"><span data-stu-id="42a4c-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="42a4c-130">メッセージを循環するために使用される間隔。</span><span class="sxs-lookup"><span data-stu-id="42a4c-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="42a4c-131">すべて無視</span><span class="sxs-lookup"><span data-stu-id="42a4c-131">Allow dismiss</span></span>             | <span data-ttu-id="42a4c-132">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="42a4c-132">**True** or **False**</span></span>              | <span data-ttu-id="42a4c-133">値が **True** に設定されている場合、顧客は警告を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="42a4c-134">カルーセル フリッパーを表示する</span><span class="sxs-lookup"><span data-stu-id="42a4c-134">Show carousel flipper</span></span>     | <span data-ttu-id="42a4c-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="42a4c-135">**True** or **False**</span></span>              | <span data-ttu-id="42a4c-136">カルーセル フリッパーを表示するかどうかを示す値なので、顧客は複数のバナー項目を手動で切り替えて、循環させることができます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="42a4c-137">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="42a4c-137">Text alignment</span></span>            | <span data-ttu-id="42a4c-138">**右**、**左**、または **中央**</span><span class="sxs-lookup"><span data-stu-id="42a4c-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="42a4c-139">プロモーション バナー モジュールのテキスト配置。</span><span class="sxs-lookup"><span data-stu-id="42a4c-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="42a4c-140">リンク</span><span class="sxs-lookup"><span data-stu-id="42a4c-140">Link</span></span>                      | <span data-ttu-id="42a4c-141">URL</span><span class="sxs-lookup"><span data-stu-id="42a4c-141">A URL</span></span>                              | <span data-ttu-id="42a4c-142">オプション リンクの URL</span><span class="sxs-lookup"><span data-stu-id="42a4c-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="42a4c-143">プロモーション バナー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="42a4c-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="42a4c-144">ページにプロモーション バナー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="42a4c-145">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="42a4c-146">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**プロモーション バナーのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="42a4c-147">**ページ アウトライン** で、**既定のページ** モジュールを **本文** スロットに追加します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="42a4c-148">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="42a4c-149">作成したテンプレートを使用して、**プロモーション バナー ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="42a4c-150">新しいページの **メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="42a4c-151">右側のウィンドウで、**幅** の値を **全コンテナー** に設定します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="42a4c-152">**ページ アウトライン** で、プロモーション バナー モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="42a4c-153">バナー モジュールの設定で、1 つ以上のバナー メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="42a4c-154">各メッセージには、リンクと共にテキストを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-154">Each message can have text together with a link.</span></span> <span data-ttu-id="42a4c-155">モジュールをさらにカスタマイズする場合は、他のプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="42a4c-156">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="42a4c-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="42a4c-157">ページの上部に、追加したテキストが表示された警告が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="42a4c-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="42a4c-158">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="42a4c-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="42a4c-159">プロモーション バナーは、通常、ページ ヘッダー スロットまたはサブヘッダー スロットで使用されます。</span><span class="sxs-lookup"><span data-stu-id="42a4c-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="42a4c-160">追加リソース</span><span class="sxs-lookup"><span data-stu-id="42a4c-160">Additional resources</span></span>

[<span data-ttu-id="42a4c-161">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="42a4c-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="42a4c-162">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="42a4c-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="42a4c-163">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="42a4c-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="42a4c-164">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="42a4c-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="42a4c-165">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="42a4c-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]