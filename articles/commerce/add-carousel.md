---
title: カルーセル モジュール
description: このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206514"
---
# <a name="carousel-module"></a><span data-ttu-id="e884f-103">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="e884f-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e884f-104">このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e884f-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e884f-105">カルーセル モジュールは、顧客が閲覧できる複数のプロモーション品目 (豊富な画像を含む) を入れ替わるカルーセル バナーに配置するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e884f-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="e884f-106">たとえば、小売業者はホーム ページ上のカルーセル モジュールを使用して、複数の新製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="e884f-107">カルーセル モジュール内に、コンテンツ ブロック モジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="e884f-108">次に、カルーセル モジュールのプロパティによって、これらのモジュールの表示方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="e884f-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="e884f-109">電子商取引サイトのカルーセル モジュールの例</span><span class="sxs-lookup"><span data-stu-id="e884f-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="e884f-110">中に複数のプロモーション モジュールがあるカルーセルは、ホーム ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="e884f-111">中に複数のプロモーション モジュールがあるカルーセルは、製品の詳細ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="e884f-112">任意のマーケティング ページでカルーセルを使用して、複数のプロモーションや製品を販売促進できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="e884f-113">以下の図は、ホームページ上のカルーセル モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e884f-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="e884f-114">このカルーセル モジュールには、複数のコンテンツ ブロック品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e884f-114">This carousel module contains multiple content block items.</span></span>

![カルーセル モジュールの例](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="e884f-116">カルーセル モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="e884f-116">Carousel module properties</span></span>

| <span data-ttu-id="e884f-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e884f-117">Property name</span></span>             | <span data-ttu-id="e884f-118">先頭値</span><span class="sxs-lookup"><span data-stu-id="e884f-118">Value</span></span>                 | <span data-ttu-id="e884f-119">説明</span><span class="sxs-lookup"><span data-stu-id="e884f-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e884f-120">自動再生</span><span class="sxs-lookup"><span data-stu-id="e884f-120">Autoplay</span></span>                  | <span data-ttu-id="e884f-121">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e884f-121">**True** or **False**</span></span> | <span data-ttu-id="e884f-122">値が **True** に設定されている場合、カルーセル内の品目間の切り替えが自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="e884f-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="e884f-123">値が **False** に設定されている場合、ユーザーがキーボードまたはマウスを使用してある品目から次の品目に移動しない限り、切り替えは行われません。</span><span class="sxs-lookup"><span data-stu-id="e884f-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="e884f-124">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="e884f-124">Slide transition interval</span></span> | <span data-ttu-id="e884f-125">値 (秒単位)</span><span class="sxs-lookup"><span data-stu-id="e884f-125">A value in seconds</span></span>    | <span data-ttu-id="e884f-126">品目間の切り替えの間隔。</span><span class="sxs-lookup"><span data-stu-id="e884f-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="e884f-127">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="e884f-127">Transition type</span></span>           | <span data-ttu-id="e884f-128">**スライド** または **フェード**</span><span class="sxs-lookup"><span data-stu-id="e884f-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="e884f-129">品目間の切り替え効果。</span><span class="sxs-lookup"><span data-stu-id="e884f-129">The transition effect between items.</span></span> |
| <span data-ttu-id="e884f-130">カルーセル フリッパーを非表示にする</span><span class="sxs-lookup"><span data-stu-id="e884f-130">Hide carousel flipper</span></span>     | <span data-ttu-id="e884f-131">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e884f-131">**True** or **False**</span></span> | <span data-ttu-id="e884f-132">この値が **True** に設定されている場合、カルーセル フリッパーとシーケンス インジケーターが非表示になります。</span><span class="sxs-lookup"><span data-stu-id="e884f-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="e884f-133">カルーセルを閉じる許可</span><span class="sxs-lookup"><span data-stu-id="e884f-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="e884f-134">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e884f-134">**True** or **False**</span></span> | <span data-ttu-id="e884f-135">値が **True** に設定されている場合、ユーザーはカルーセルを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="e884f-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="e884f-136">カルーセル モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="e884f-136">Add a carousel module to a page</span></span>

<span data-ttu-id="e884f-137">新しいページにカルーセル モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e884f-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e884f-138">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="e884f-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e884f-139">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**カルーセルのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="e884f-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e884f-140">**本文** スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e884f-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="e884f-141">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="e884f-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="e884f-142">作成したカルーセル テンプレートを使用して、**カルーセル ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="e884f-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="e884f-143">新しいページの **メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e884f-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="e884f-144">右側のウィンドウで、**幅** の値を **全画面** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e884f-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="e884f-145">**ページ アウトライン** で、カルーセル モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="e884f-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="e884f-146">コンテンツ ブロック モジュールをカルーセル モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="e884f-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="e884f-147">**ヘッダー**、**リンク**、**レイアウト** およびその他のプロパティを提供して、コンテンツ ブロック モジュールのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e884f-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="e884f-148">別のコンテンツ ブロック モジュールを追加およびコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e884f-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="e884f-149">必要に応じてカルーセル モジュールの追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e884f-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="e884f-150">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="e884f-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e884f-151">このページには、2 つのモジュール (ヒーロー モジュールと機能モジュール) を中に含むカルーセルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e884f-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="e884f-152">目的の効果を達成するため、カルーセル、ヒーロー、および機能モジュールに対する追加のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="e884f-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="e884f-153">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="e884f-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e884f-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e884f-154">Additional resources</span></span>

[<span data-ttu-id="e884f-155">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="e884f-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e884f-156">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="e884f-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e884f-157">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="e884f-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e884f-158">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="e884f-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="e884f-159">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="e884f-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]