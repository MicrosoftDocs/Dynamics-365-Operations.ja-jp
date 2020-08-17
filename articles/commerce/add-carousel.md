---
title: カルーセル モジュール
description: このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620989"
---
# <a name="carousel-module"></a><span data-ttu-id="81354-103">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="81354-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81354-104">このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81354-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="81354-105">概要</span><span class="sxs-lookup"><span data-stu-id="81354-105">Overview</span></span>

<span data-ttu-id="81354-106">カルーセル モジュールは、顧客が閲覧できる複数のプロモーション品目 (豊富な画像を含む) を入れ替わるカルーセル バナーに配置するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="81354-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="81354-107">たとえば、小売業者はホーム ページ上のカルーセル モジュールを使用して、複数の新製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="81354-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="81354-108">カルーセル モジュール内に、コンテンツ ブロック モジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="81354-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="81354-109">次に、カルーセル モジュールのプロパティによって、これらのモジュールの表示方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="81354-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="81354-110">電子商取引サイトのカルーセル モジュールの例</span><span class="sxs-lookup"><span data-stu-id="81354-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="81354-111">中に複数のプロモーション モジュールがあるカルーセルは、ホーム ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="81354-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="81354-112">中に複数のプロモーション モジュールがあるカルーセルは、製品の詳細ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="81354-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="81354-113">任意のマーケティング ページでカルーセルを使用して、複数のプロモーションや製品を販売促進できます。</span><span class="sxs-lookup"><span data-stu-id="81354-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="81354-114">以下の図は、ホームページ上のカルーセル モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="81354-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="81354-115">このカルーセル モジュールには、複数のコンテンツ ブロック品目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81354-115">This carousel module contains multiple content block items.</span></span>

![カルーセル モジュールの例](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="81354-117">カルーセル モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="81354-117">Carousel module properties</span></span>

| <span data-ttu-id="81354-118">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="81354-118">Property name</span></span>             | <span data-ttu-id="81354-119">先頭値</span><span class="sxs-lookup"><span data-stu-id="81354-119">Value</span></span>                 | <span data-ttu-id="81354-120">説明</span><span class="sxs-lookup"><span data-stu-id="81354-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="81354-121">自動再生</span><span class="sxs-lookup"><span data-stu-id="81354-121">Autoplay</span></span>                  | <span data-ttu-id="81354-122">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="81354-122">**True** or **False**</span></span> | <span data-ttu-id="81354-123">値が **True** に設定されている場合、カルーセル内の品目間の切り替えが自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="81354-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="81354-124">値が **False** に設定されている場合、ユーザーがキーボードまたはマウスを使用してある品目から次の品目に移動しない限り、切り替えは行われません。</span><span class="sxs-lookup"><span data-stu-id="81354-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="81354-125">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="81354-125">Slide transition interval</span></span> | <span data-ttu-id="81354-126">値 (秒単位)</span><span class="sxs-lookup"><span data-stu-id="81354-126">A value in seconds</span></span>    | <span data-ttu-id="81354-127">品目間の切り替えの間隔。</span><span class="sxs-lookup"><span data-stu-id="81354-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="81354-128">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="81354-128">Transition type</span></span>           | <span data-ttu-id="81354-129">**スライド**または**フェード**</span><span class="sxs-lookup"><span data-stu-id="81354-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="81354-130">品目間の切り替え効果。</span><span class="sxs-lookup"><span data-stu-id="81354-130">The transition effect between items.</span></span> |
| <span data-ttu-id="81354-131">カルーセル フリッパーを非表示にする</span><span class="sxs-lookup"><span data-stu-id="81354-131">Hide carousel flipper</span></span>     | <span data-ttu-id="81354-132">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="81354-132">**True** or **False**</span></span> | <span data-ttu-id="81354-133">この値が **True** に設定されている場合、カルーセル フリッパーとシーケンス インジケーターが非表示になります。</span><span class="sxs-lookup"><span data-stu-id="81354-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="81354-134">カルーセルを閉じる許可</span><span class="sxs-lookup"><span data-stu-id="81354-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="81354-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="81354-135">**True** or **False**</span></span> | <span data-ttu-id="81354-136">値が **True** に設定されている場合、ユーザーはカルーセルを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="81354-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="81354-137">カルーセル モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="81354-137">Add a carousel module to a page</span></span>

<span data-ttu-id="81354-138">新しいページにカルーセル モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="81354-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="81354-139">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="81354-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="81354-140">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**カルーセルのテンプレート** を入力し、**OK**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="81354-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="81354-141">**本文**スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="81354-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="81354-142">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="81354-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="81354-143">作成したカルーセル テンプレートを使用して、**カルーセル ページ** という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="81354-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="81354-144">新しいページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="81354-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="81354-145">右側のウィンドウで、**幅**の値を**全画面**に設定します。</span><span class="sxs-lookup"><span data-stu-id="81354-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="81354-146">**ページ アウトライン**で、カルーセル モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="81354-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="81354-147">コンテンツ ブロック モジュールをカルーセル モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="81354-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="81354-148">**ヘッダー**、**リンク**、**レイアウト**およびその他のプロパティを提供して、コンテンツ ブロック モジュールのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81354-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="81354-149">別のコンテンツ ブロック モジュールを追加およびコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="81354-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="81354-150">必要に応じてカルーセル モジュールの追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="81354-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="81354-151">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="81354-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="81354-152">このページには、2 つのモジュール (ヒーロー モジュールと機能モジュール) を中に含むカルーセルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="81354-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="81354-153">目的の効果を達成するため、カルーセル、ヒーロー、および機能モジュールに対する追加のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="81354-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="81354-154">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="81354-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81354-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="81354-155">Additional resources</span></span>

[<span data-ttu-id="81354-156">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="81354-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="81354-157">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="81354-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="81354-158">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="81354-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="81354-159">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="81354-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="81354-160">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="81354-160">Video player module</span></span>](add-video-player.md)
