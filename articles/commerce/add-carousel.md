---
title: カルーセル モジュール
description: このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025784"
---
# <a name="carousel-module"></a><span data-ttu-id="3b1ea-103">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="3b1ea-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3b1ea-104">このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3b1ea-105">概要</span><span class="sxs-lookup"><span data-stu-id="3b1ea-105">Overview</span></span>

<span data-ttu-id="3b1ea-106">カルーセル モジュールは、顧客が閲覧できる複数のプロモーション品目 (豊富な画像を含む) を入れ替わるカルーセル バナーに配置するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="3b1ea-107">たとえば、小売業者はホーム ページ上のカルーセル モジュールを使用して、複数の新製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="3b1ea-108">カルーセル モジュール内に、コンテンツ ブロック モジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="3b1ea-109">次に、カルーセル モジュールのプロパティによって、これらのモジュールの表示方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="3b1ea-110">電子商取引サイトのカルーセル モジュールの例</span><span class="sxs-lookup"><span data-stu-id="3b1ea-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="3b1ea-111">中に複数のプロモーション モジュールがあるカルーセルは、ホーム ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="3b1ea-112">中に複数のプロモーション モジュールがあるカルーセルは、製品の詳細ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="3b1ea-113">任意のマーケティング ページでカルーセルを使用して、複数のプロモーションや製品を販売促進できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="3b1ea-114">カルーセル モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b1ea-114">Carousel module properties</span></span>

| <span data-ttu-id="3b1ea-115">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="3b1ea-115">Property name</span></span>             | <span data-ttu-id="3b1ea-116">金額</span><span class="sxs-lookup"><span data-stu-id="3b1ea-116">Value</span></span>                 | <span data-ttu-id="3b1ea-117">説明</span><span class="sxs-lookup"><span data-stu-id="3b1ea-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="3b1ea-118">自動再生</span><span class="sxs-lookup"><span data-stu-id="3b1ea-118">Autoplay</span></span>                  | <span data-ttu-id="3b1ea-119">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="3b1ea-119">**True** or **False**</span></span> | <span data-ttu-id="3b1ea-120">値が **True** に設定されている場合、カルーセル内の品目間の切り替えが自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="3b1ea-121">値が **False** に設定されている場合、ユーザーがキーボードまたはマウスを使用してある品目から次の品目に移動しない限り、切り替えは行われません。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="3b1ea-122">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="3b1ea-122">Slide transition interval</span></span> | <span data-ttu-id="3b1ea-123">値 (秒単位)</span><span class="sxs-lookup"><span data-stu-id="3b1ea-123">A value in seconds</span></span>    | <span data-ttu-id="3b1ea-124">品目間の切り替えの間隔。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="3b1ea-125">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="3b1ea-125">Transition type</span></span>           | <span data-ttu-id="3b1ea-126">**スライド**または**フェード**</span><span class="sxs-lookup"><span data-stu-id="3b1ea-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="3b1ea-127">品目間の切り替え効果。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-127">The transition effect between items.</span></span> |
| <span data-ttu-id="3b1ea-128">カルーセル フリッパーを非表示にする</span><span class="sxs-lookup"><span data-stu-id="3b1ea-128">Hide carousel flipper</span></span>     | <span data-ttu-id="3b1ea-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="3b1ea-129">**True** or **False**</span></span> | <span data-ttu-id="3b1ea-130">この値が **True** に設定されている場合、カルーセル フリッパーとシーケンス インジケーターが非表示になります。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="3b1ea-131">カルーセルを閉じる許可</span><span class="sxs-lookup"><span data-stu-id="3b1ea-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="3b1ea-132">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="3b1ea-132">**True** or **False**</span></span> | <span data-ttu-id="3b1ea-133">値が **True** に設定されている場合、ユーザーはカルーセルを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="3b1ea-134">カルーセル モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="3b1ea-134">Add a carousel module to a page</span></span>

<span data-ttu-id="3b1ea-135">新しいページにカルーセル モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3b1ea-136">**カルーセル テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="3b1ea-137">**本文**スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="3b1ea-138">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="3b1ea-139">作成したカルーセル テンプレートを使用して、**カルーセル ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="3b1ea-140">新しいページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="3b1ea-141">右側のウィンドウで、**幅**の値を**全画面**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="3b1ea-142">**ページ アウトライン**で、カルーセル モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="3b1ea-143">コンテンツ ブロック モジュールをカルーセル モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="3b1ea-144">**ヘッダー**、**リンク**、**レイアウト**およびその他のプロパティを提供して、コンテンツ ブロック モジュールのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="3b1ea-145">別のコンテンツ ブロック モジュールを追加およびコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="3b1ea-146">必要に応じてカルーセル モジュールの追加のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="3b1ea-147">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-147">Save and preview the page.</span></span> <span data-ttu-id="3b1ea-148">このページには、2 つのモジュール (ヒーロー モジュールと機能モジュール) を中に含むカルーセルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="3b1ea-149">目的の効果を達成するため、カルーセル、ヒーロー、および機能モジュールに対する追加のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="3b1ea-150">ページの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="3b1ea-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b1ea-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3b1ea-151">Additional resources</span></span>

[<span data-ttu-id="3b1ea-152">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="3b1ea-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3b1ea-153">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="3b1ea-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3b1ea-154">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="3b1ea-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3b1ea-155">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="3b1ea-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="3b1ea-156">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="3b1ea-156">Video player module</span></span>](add-video-player.md)
