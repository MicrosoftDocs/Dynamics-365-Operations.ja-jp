---
title: コンテンツ リッチ ブロック モジュール
description: このトピックでは、コンテンツ リッチ ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785424"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="5e122-103">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5e122-104">このトピックでは、コンテンツ リッチ ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e122-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e122-105">概要</span><span class="sxs-lookup"><span data-stu-id="5e122-105">Overview</span></span>

<span data-ttu-id="5e122-106">コンテンツ リッチ ブロック モジュールは、1 つ以上のコンテンツ リッチ ブロック項目を中に配置できる特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="5e122-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="5e122-107">コンテンツ リッチ ブロック モジュールは、ページのテキスト コンテンツ用に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e122-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="5e122-108">このコンテンツは、情報提供またはプロモーションのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="5e122-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="5e122-109">コンテンツ リッチ ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="5e122-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="5e122-110">これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="5e122-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="5e122-111">E コマースのコンテンツ リッチ ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="5e122-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="5e122-112">コンテンツ リッチ ブロック モジュールは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e122-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="5e122-113">製品の詳細ページで製品機能について紹介します。</span><span class="sxs-lookup"><span data-stu-id="5e122-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="5e122-114">任意のページで情報提供を目的とします。</span><span class="sxs-lookup"><span data-stu-id="5e122-114">For informational purposes on any page.</span></span> <span data-ttu-id="5e122-115">たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。</span><span class="sxs-lookup"><span data-stu-id="5e122-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="5e122-116">製品の詳細ページでカスタム メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="5e122-117">(たとえば、"$50 以上のご注文で送料無料")。</span><span class="sxs-lookup"><span data-stu-id="5e122-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="5e122-118">製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。</span><span class="sxs-lookup"><span data-stu-id="5e122-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="5e122-119">コンテンツ リッチ ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e122-119">Content rich block module properties</span></span>

| <span data-ttu-id="5e122-120">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5e122-120">Property name</span></span>     | <span data-ttu-id="5e122-121">金額</span><span class="sxs-lookup"><span data-stu-id="5e122-121">Value</span></span>                                 | <span data-ttu-id="5e122-122">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e122-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="5e122-123">列数</span><span class="sxs-lookup"><span data-stu-id="5e122-123">Number of columns</span></span> | <span data-ttu-id="5e122-124">**1** から **4** までの数字</span><span class="sxs-lookup"><span data-stu-id="5e122-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="5e122-125">コンテンツ リッチ ブロックの列の数。</span><span class="sxs-lookup"><span data-stu-id="5e122-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="5e122-126">最大 4 列あります。</span><span class="sxs-lookup"><span data-stu-id="5e122-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="5e122-127">幅</span><span class="sxs-lookup"><span data-stu-id="5e122-127">Width</span></span>             | <span data-ttu-id="5e122-128">**全コンテナー**または**全画面**</span><span class="sxs-lookup"><span data-stu-id="5e122-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="5e122-129">値が**全コンテナー**に設定されている場合、コンテナー内の項目は、コンテナーの幅に限定されます。</span><span class="sxs-lookup"><span data-stu-id="5e122-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="5e122-130">値が**全画面**に設定されている場合、項目はコンテナーの幅に限定されませんが、全画面モードになります。</span><span class="sxs-lookup"><span data-stu-id="5e122-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="5e122-131">目的のレイアウトを実現するよう値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="5e122-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="5e122-132">コンテンツ リッチ ブロック項目モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e122-132">Content rich block item module properties</span></span>

| <span data-ttu-id="5e122-133">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5e122-133">Property name</span></span> | <span data-ttu-id="5e122-134">金額</span><span class="sxs-lookup"><span data-stu-id="5e122-134">Value</span></span>          | <span data-ttu-id="5e122-135">説明</span><span class="sxs-lookup"><span data-stu-id="5e122-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="5e122-136">段落</span><span class="sxs-lookup"><span data-stu-id="5e122-136">Paragraph</span></span>     | <span data-ttu-id="5e122-137">段落のテキスト</span><span class="sxs-lookup"><span data-stu-id="5e122-137">Paragraph text</span></span> | <span data-ttu-id="5e122-138">各コンテンツ リッチ ブロック項目に付属するテキスト。</span><span class="sxs-lookup"><span data-stu-id="5e122-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="5e122-139">太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5e122-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="5e122-140">コンテンツ リッチ ブロック モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="5e122-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="5e122-141">新しいページにコンテンツ リッチ ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5e122-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5e122-142">**コンテンツ テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e122-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="5e122-143">既定のページの**メイン** スロットで、コンテンツ リッチ ブロック モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="5e122-144">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="5e122-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="5e122-145">作成したコンテンツ テンプレートを使用して、**コンテンツ ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e122-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="5e122-146">新しいページの**メイン** スロットで、コンテンツ リッチ ブロック モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="5e122-147">コンテンツ リッチ ブロック モジュールのプロパティで、列の数を **2** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5e122-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="5e122-148">コンテンツ リッチ ブロック モジュールで、**モジュールの追加**を選択し、コンテンツ リッチ ブロック項目 (たとえば、**項目 1**) を追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="5e122-149">新しいコンテンツ リッチ ブロック項目で、段落テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="5e122-150">コンテンツ リッチ ブロック モジュールで、**モジュールの追加**を選択し、コンテンツ リッチ ブロック項目 (たとえば、**項目 2**) を追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="5e122-151">新しいコンテンツ リッチ ブロック項目で、段落テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="5e122-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="5e122-152">ページを保存して、プレビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="5e122-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="5e122-153">2 列のビューに 2 つのリッチ テキスト ブロックが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e122-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="5e122-154">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="5e122-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="5e122-155">3 番目のコンテンツ リッチ ブロック項目を追加すると、前に追加した 2 つの項目の下に積み重ねられます。</span><span class="sxs-lookup"><span data-stu-id="5e122-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="5e122-156">コンテナーの列と項目の数を変更することによって、テキスト コンテンツに対して異なるレイアウトを達成できます。</span><span class="sxs-lookup"><span data-stu-id="5e122-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e122-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e122-157">Additional resources</span></span>

[<span data-ttu-id="5e122-158">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="5e122-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5e122-159">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="5e122-160">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="5e122-161">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="5e122-162">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="5e122-163">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="5e122-164">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="5e122-164">Video player module</span></span>](add-video-player.md)

