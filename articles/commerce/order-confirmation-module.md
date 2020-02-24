---
title: 注文詳細のモジュール
description: このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026020"
---
# <a name="order-details-module"></a><span data-ttu-id="93a03-103">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="93a03-104">このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="93a03-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93a03-105">概要</span><span class="sxs-lookup"><span data-stu-id="93a03-105">Overview</span></span>

<span data-ttu-id="93a03-106">注文詳細モジュールを使用して、注文が行われた後、注文確認の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="93a03-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="93a03-107">注文の確認 ID、注文の連絡先情報、およびその他の注文の詳細 (購入された品目、支払情報、出荷方法など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93a03-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="93a03-108">注文確認モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93a03-108">Order confirmation module properties</span></span>

| <span data-ttu-id="93a03-109">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="93a03-109">Property name</span></span>  | <span data-ttu-id="93a03-110">値</span><span class="sxs-lookup"><span data-stu-id="93a03-110">Values</span></span> | <span data-ttu-id="93a03-111">説明</span><span class="sxs-lookup"><span data-stu-id="93a03-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="93a03-112">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="93a03-112">Heading</span></span>        | <span data-ttu-id="93a03-113">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="93a03-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="93a03-114">注文確認モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="93a03-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="93a03-115">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93a03-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="93a03-116">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="93a03-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="93a03-117">連絡先番号</span><span class="sxs-lookup"><span data-stu-id="93a03-117">Contact number</span></span> | <span data-ttu-id="93a03-118">テキスト</span><span class="sxs-lookup"><span data-stu-id="93a03-118">Text</span></span> | <span data-ttu-id="93a03-119">連絡先番号は、注文に関連する質問に対して発行できます。</span><span class="sxs-lookup"><span data-stu-id="93a03-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="93a03-120">注文詳細ページで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="93a03-121">注文の詳細ページを作成するときに、注文明細モジュールに加えて、他の関連モジュールを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="93a03-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="93a03-122">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="93a03-122">Here are some examples:</span></span>

- <span data-ttu-id="93a03-123">**推奨モジュール** - 推奨モジュールを注文詳細ページに追加して、顧客に他の製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="93a03-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="93a03-124">**マーケティング モジュール** - 注文詳細ページにマーケティング モジュールを追加して、マーケティング コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="93a03-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="93a03-125">注文詳細ページのモジュールの作成</span><span class="sxs-lookup"><span data-stu-id="93a03-125">Create an order details page module</span></span>

1. <span data-ttu-id="93a03-126">**注文詳細のテンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="93a03-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="93a03-127">既定ページの**メイン**スロットで、注文詳細モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="93a03-128">注文詳細モジュールで、推奨モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="93a03-129">テンプレートを保存およびプレビューします。</span><span class="sxs-lookup"><span data-stu-id="93a03-129">Save and preview the template.</span></span> <span data-ttu-id="93a03-130">注文確認番号のコンテキストを必要とするため、注文詳細モジュールは表示されません。</span><span class="sxs-lookup"><span data-stu-id="93a03-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="93a03-131">テンプレートの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="93a03-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="93a03-132">作成した注文詳細テンプレートを使用して、**注文詳細ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="93a03-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="93a03-133">既定のページをページ アウトラインに追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="93a03-134">**ヘッダー**スロットで、ヘッダー フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="93a03-135">**フッター**スロットで、フッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="93a03-136">**メイン** スロットで、注文詳細モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="93a03-137">注文詳細モジュールのプロパティ ウィンドウで、見出しの**注文詳細**を追加します。</span><span class="sxs-lookup"><span data-stu-id="93a03-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="93a03-138">注文詳細モジュールの下で、推奨モジュールを追加し、**新規**および**ベストセラー**設定を使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="93a03-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="93a03-139">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="93a03-139">Save and preview the page.</span></span>
1. <span data-ttu-id="93a03-140">ページの編集を終了し、公開します。</span><span class="sxs-lookup"><span data-stu-id="93a03-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93a03-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="93a03-141">Additional resources</span></span>

[<span data-ttu-id="93a03-142">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="93a03-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="93a03-143">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="93a03-144">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="93a03-145">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="93a03-146">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="93a03-147">ヘッダーモジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="93a03-148">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="93a03-148">Footer module</span></span>](author-footer-module.md)
