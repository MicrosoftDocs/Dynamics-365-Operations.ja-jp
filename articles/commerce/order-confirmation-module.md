---
title: 注文確認モジュール
description: このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698329"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="1c66c-103">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1c66c-104">このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1c66c-105">概要</span><span class="sxs-lookup"><span data-stu-id="1c66c-105">Overview</span></span>

<span data-ttu-id="1c66c-106">注文確認モジュールは、注文の完了後に注文確認のページに確認メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="1c66c-107">注文確認モジュールは、注文確認書番号およびチェックアウト時に指定された顧客の電子メール アドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="1c66c-108">注文がチェックアウト中に配置されると、注文の確認書番号および顧客の電子メールアドレスが、ページの URL のクエリ文字列として注文確認ページに渡されます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="1c66c-109">注文の確認モジュールは、この情報を受け取り、注文の確認ページに注文状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="1c66c-110">注文確認モジュールでは、このページのコンテキストを使用して注文状態を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c66c-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="1c66c-111">注文確認モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="1c66c-111">Order confirmation module properties</span></span>

| <span data-ttu-id="1c66c-112">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="1c66c-112">Property name</span></span> | <span data-ttu-id="1c66c-113">値</span><span class="sxs-lookup"><span data-stu-id="1c66c-113">Values</span></span> | <span data-ttu-id="1c66c-114">説明</span><span class="sxs-lookup"><span data-stu-id="1c66c-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="1c66c-115">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="1c66c-115">Heading</span></span>       | <span data-ttu-id="1c66c-116">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="1c66c-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1c66c-117">注文確認モジュールには、ヘッダーを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="1c66c-118">既定では、**H2** ヘッダー タグがヘッダーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1c66c-119">ただし、アクセシビリティ要件を満たすようにタグを変更できます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="1c66c-120">注文確認ページのモジュールで使用可能なモジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="1c66c-121">**推奨** - 推奨モジュールを注文確認ページに追加して、顧客に他の製品を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="1c66c-122">**マーケティング** - マーケティング モジュールは、注文確認ページにマーケティングのコンテンツを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="1c66c-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="1c66c-123">注文確認ページのモジュールの作成</span><span class="sxs-lookup"><span data-stu-id="1c66c-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="1c66c-124">**注文確認のテンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="1c66c-125">既定ページの**メイン**スロットで、注文確認モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="1c66c-126">注文確認モジュールで、推奨モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="1c66c-127">テンプレートを保存およびプレビューします。</span><span class="sxs-lookup"><span data-stu-id="1c66c-127">Save and preview the template.</span></span> <span data-ttu-id="1c66c-128">注文確認番号のコンテキストを必要とするため、注文確認モジュールは表示されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c66c-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="1c66c-129">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1c66c-130">作成した注文確認テンプレートを使用して、**注文確認ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="1c66c-131">既定のページをページ アウトラインに追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="1c66c-132">**ヘッダー**スロットで、ヘッダー フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="1c66c-133">**フッター**スロットで、フッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="1c66c-134">**メイン**スロットで、注文確認モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="1c66c-135">注文確認モジュールのプロパティ ウィンドウで、見出しの**注文確認**を追加します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="1c66c-136">注文確認モジュールの下で、推奨モジュールを追加し、**新規**および**ベストセラー**設定を使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="1c66c-137">ページを保存およびプレビューし、チェック イン後に発行します。</span><span class="sxs-lookup"><span data-stu-id="1c66c-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c66c-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1c66c-138">Additional resources</span></span>

[<span data-ttu-id="1c66c-139">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="1c66c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1c66c-140">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1c66c-141">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1c66c-142">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1c66c-143">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1c66c-144">ヘッダーモジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1c66c-145">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="1c66c-145">Footer module</span></span>](author-footer-module.md)
