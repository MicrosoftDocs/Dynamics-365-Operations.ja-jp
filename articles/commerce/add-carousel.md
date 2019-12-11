---
title: カルーセル モジュール
description: このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785240"
---
# <a name="carousel-module"></a><span data-ttu-id="87431-103">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="87431-104">このトピックでは、カルーセル モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87431-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87431-105">概要</span><span class="sxs-lookup"><span data-stu-id="87431-105">Overview</span></span>

<span data-ttu-id="87431-106">カルーセル モジュールは、顧客が閲覧できる複数のプロモーション品目をカルーセルに配置するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="87431-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="87431-107">これは、他のモジュールをホストする特別なコンテナ モジュールです。</span><span class="sxs-lookup"><span data-stu-id="87431-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="87431-108">たとえば、小売業者はホーム ページ上のカルーセル モジュールを使用して、複数の新製品またはプロモーションを紹介できます。</span><span class="sxs-lookup"><span data-stu-id="87431-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="87431-109">カルーセル モジュール内に、ヒーローや機能モジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="87431-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="87431-110">次に、カルーセル モジュールのプロパティによって、これらのモジュールの表示方法が定義されます。</span><span class="sxs-lookup"><span data-stu-id="87431-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="87431-111">電子商取引サイトのカルーセル モジュールの例</span><span class="sxs-lookup"><span data-stu-id="87431-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="87431-112">中に複数のプロモーション モジュールがあるカルーセルは、ホーム ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="87431-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="87431-113">中に複数のプロモーション モジュールがあるカルーセルは、製品の詳細ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="87431-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="87431-114">任意のマーケティング ページでカルーセルを使用して、複数のプロモーションや製品を販売促進できます。</span><span class="sxs-lookup"><span data-stu-id="87431-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="87431-115">カルーセル モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="87431-115">Carousel module properties</span></span>

| <span data-ttu-id="87431-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="87431-116">Property name</span></span>             | <span data-ttu-id="87431-117">金額</span><span class="sxs-lookup"><span data-stu-id="87431-117">Value</span></span>                                | <span data-ttu-id="87431-118">説明</span><span class="sxs-lookup"><span data-stu-id="87431-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="87431-119">自動再生</span><span class="sxs-lookup"><span data-stu-id="87431-119">Autoplay</span></span>                  | <span data-ttu-id="87431-120">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="87431-120">**True** or **False**</span></span>                | <span data-ttu-id="87431-121">値が **True** に設定されている場合、カルーセル内の品目間の切り替えが自動的に行われます。</span><span class="sxs-lookup"><span data-stu-id="87431-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="87431-122">値が **False** に設定されている場合、ユーザーがキーボードまたはマウスを使用してある品目から次の品目に移動しない限り、切り替えは行われません。</span><span class="sxs-lookup"><span data-stu-id="87431-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="87431-123">スライド切り替え間隔</span><span class="sxs-lookup"><span data-stu-id="87431-123">Slide transition interval</span></span> | <span data-ttu-id="87431-124">値 (秒単位)</span><span class="sxs-lookup"><span data-stu-id="87431-124">A value in seconds</span></span>                   | <span data-ttu-id="87431-125">品目間の切り替えの間隔。</span><span class="sxs-lookup"><span data-stu-id="87431-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="87431-126">切り替えアニメーション</span><span class="sxs-lookup"><span data-stu-id="87431-126">Transition animation</span></span>      | <span data-ttu-id="87431-127">**スライド**または**フェード**</span><span class="sxs-lookup"><span data-stu-id="87431-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="87431-128">切り替え効果。</span><span class="sxs-lookup"><span data-stu-id="87431-128">The transition effect.</span></span> |
| <span data-ttu-id="87431-129">幅</span><span class="sxs-lookup"><span data-stu-id="87431-129">Width</span></span>                     | <span data-ttu-id="87431-130">**コンテナーに適合**または**全画面**</span><span class="sxs-lookup"><span data-stu-id="87431-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="87431-131">値が**コンテナーに適合**に設定されている場合、カルーセル内の項目は、カルーセルの幅に限定されます。</span><span class="sxs-lookup"><span data-stu-id="87431-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="87431-132">値が**全画面**に設定されている場合、品目はカルーセルの幅に限定されませんが、全画面モードになります。</span><span class="sxs-lookup"><span data-stu-id="87431-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="87431-133">目的のレイアウトを実現するよう値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="87431-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="87431-134">カルーセル モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="87431-134">Add a carousel module to a page</span></span>

<span data-ttu-id="87431-135">新しいページにカルーセル モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="87431-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="87431-136">**カルーセル テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="87431-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="87431-137">既定のページの**メイン** スロットで、カルーセル モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="87431-138">カルーセル モジュールにヒーロー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="87431-139">カルーセル モジュールに機能モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="87431-140">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="87431-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="87431-141">作成したカルーセル テンプレートを使用して、**カルーセル ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="87431-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="87431-142">新しいページの**メイン** スロットで、カルーセル モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="87431-143">カルーセル モジュールの**幅**プロパティを、**全画面**に設定します。</span><span class="sxs-lookup"><span data-stu-id="87431-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="87431-144">**切り替えアニメーション** プロパティを**スライド**に設定します。</span><span class="sxs-lookup"><span data-stu-id="87431-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="87431-145">カルーセル モジュールにヒーロー モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="87431-146">ヒーロー モジュールで、画像とヘッダーを追加してから、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87431-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="87431-147">カルーセル モジュールに機能モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="87431-148">機能モジュールで、画像、見出し、およびテキストの段落を追加します。</span><span class="sxs-lookup"><span data-stu-id="87431-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="87431-149">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="87431-149">Save and preview the page.</span></span> <span data-ttu-id="87431-150">このページには、2 つのモジュール (ヒーロー モジュールと機能モジュール) を中に含むカルーセルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="87431-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="87431-151">目的の効果を達成するため、カルーセル、ヒーロー、および機能モジュールに対する追加のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="87431-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="87431-152">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="87431-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87431-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="87431-153">Additional resources</span></span>

[<span data-ttu-id="87431-154">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="87431-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="87431-155">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="87431-156">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="87431-157">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="87431-158">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="87431-159">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="87431-160">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="87431-160">Video player module</span></span>](add-video-player.md)
