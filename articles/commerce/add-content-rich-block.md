---
title: テキスト ブロック モジュール
description: このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025600"
---
# <a name="text-block-module"></a><span data-ttu-id="b6638-103">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="b6638-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b6638-104">このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6638-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b6638-105">概要</span><span class="sxs-lookup"><span data-stu-id="b6638-105">Overview</span></span>

<span data-ttu-id="b6638-106">テキスト ブロック モジュールは、テキスト コンテンツを追加するために使用されるモジュールです。</span><span class="sxs-lookup"><span data-stu-id="b6638-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="b6638-107">このコンテンツは、情報提供またはプロモーションです。</span><span class="sxs-lookup"><span data-stu-id="b6638-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="b6638-108">テキスト ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="b6638-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="b6638-109">これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。</span><span class="sxs-lookup"><span data-stu-id="b6638-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="b6638-110">E コマースのテキスト ブロック モジュールの例</span><span class="sxs-lookup"><span data-stu-id="b6638-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="b6638-111">テキスト ブロック モジュールは、次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b6638-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="b6638-112">製品の詳細ページで製品機能について紹介します。</span><span class="sxs-lookup"><span data-stu-id="b6638-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="b6638-113">任意のページで情報提供を目的とします。</span><span class="sxs-lookup"><span data-stu-id="b6638-113">For informational purposes on any page.</span></span> <span data-ttu-id="b6638-114">たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。</span><span class="sxs-lookup"><span data-stu-id="b6638-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="b6638-115">製品の詳細ページでカスタム メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="b6638-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="b6638-116">(たとえば、"$50 以上のご注文で送料無料")。</span><span class="sxs-lookup"><span data-stu-id="b6638-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="b6638-117">製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。</span><span class="sxs-lookup"><span data-stu-id="b6638-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="b6638-118">テキスト ブロック モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6638-118">Text block module properties</span></span>

| <span data-ttu-id="b6638-119">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="b6638-119">Property name</span></span>     | <span data-ttu-id="b6638-120">Value</span><span class="sxs-lookup"><span data-stu-id="b6638-120">Value</span></span>                                            | <span data-ttu-id="b6638-121">説明</span><span class="sxs-lookup"><span data-stu-id="b6638-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="b6638-122">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="b6638-122">Rich text</span></span>         | <span data-ttu-id="b6638-123">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="b6638-123">Rich text</span></span>                                        | <span data-ttu-id="b6638-124">段落のテキスト。</span><span class="sxs-lookup"><span data-stu-id="b6638-124">Paragraph text.</span></span> <span data-ttu-id="b6638-125">太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b6638-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="b6638-126">カスタム クラス名</span><span class="sxs-lookup"><span data-stu-id="b6638-126">Custom class name</span></span> | <span data-ttu-id="b6638-127">カスケード スタイル シート (CSS) クラス名</span><span class="sxs-lookup"><span data-stu-id="b6638-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="b6638-128">開発者がこのモジュールをフォーマットするために提供するカスタム CSS クラス名。</span><span class="sxs-lookup"><span data-stu-id="b6638-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="b6638-129">クラス名は、テーマ パックで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6638-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="b6638-130">フォント サイズ</span><span class="sxs-lookup"><span data-stu-id="b6638-130">Font size</span></span>         | <span data-ttu-id="b6638-131">**小**、**中**、**大**、または**特大**</span><span class="sxs-lookup"><span data-stu-id="b6638-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="b6638-132">コンテンツのフォント サイズ。</span><span class="sxs-lookup"><span data-stu-id="b6638-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="b6638-133">テキスト ブロック モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="b6638-133">Add a text block module to a page</span></span>

<span data-ttu-id="b6638-134">新しいページテキスト ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6638-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b6638-135">**コンテンツ テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6638-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="b6638-136">**本文**スロットで、**既定のページ** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="b6638-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="b6638-137">テンプレートの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="b6638-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="b6638-138">作成したコンテンツ テンプレートを使用して、**コンテンツ ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6638-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="b6638-139">新しいページの**メイン** スロットで、コンテナ― モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="b6638-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="b6638-140">コンテナー モジュールのプロパティ ウィンドウで、**幅**プロパティを**全コンテナー**に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6638-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="b6638-141">テキスト ブロック モジュールをコンテナー モジュールに追加します。</span><span class="sxs-lookup"><span data-stu-id="b6638-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="b6638-142">テキスト ブロック モジュールのプロパティ ウィンドウで、**リッチ テキスト** フィールドにテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="b6638-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="b6638-143">ページの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="b6638-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6638-144">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b6638-144">Additional resources</span></span>

[<span data-ttu-id="b6638-145">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="b6638-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b6638-146">プロモーション バナー モジュール</span><span class="sxs-lookup"><span data-stu-id="b6638-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b6638-147">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="b6638-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b6638-148">コンテンツ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="b6638-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="b6638-149">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="b6638-149">Video player module</span></span>](add-video-player.md)

