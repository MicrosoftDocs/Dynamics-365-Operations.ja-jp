---
title: 出荷先住所モジュール
description: このトピックでは、出荷先住所モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234416"
---
# <a name="shipping-address-module"></a><span data-ttu-id="607c5-103">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="607c5-104">このトピックでは、出荷先住所モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="607c5-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="607c5-105">出荷先住所モジュールにより、顧客がチェックアウト フロー中に注文の出荷先住所を追加または選択できます。</span><span class="sxs-lookup"><span data-stu-id="607c5-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="607c5-106">顧客がサインインしている場合、その顧客用に以前に保存されたすべての住所が表示され、そこから選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="607c5-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="607c5-107">顧客は、新しい住所を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="607c5-107">The customer can also add a new address.</span></span> <span data-ttu-id="607c5-108">出荷先住所モジュールは、出荷を必要とする注文のすべての品目に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="607c5-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="607c5-109">Commerce 本社では、国や地域ごとに送付先住所の形式を定義することができます。その後、送付先住所モジュールは、国/地域に固有のルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="607c5-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="607c5-110">顧客がチェックアウト フロー中に送付先住所を入力する場合、オプションでその住所を基本住所として保存することができます。</span><span class="sxs-lookup"><span data-stu-id="607c5-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="607c5-111">このオプションは、顧客がログインしている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="607c5-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="607c5-112">送付先住所モジュールでは住所検証はおこないませんが、この機能はカスタマイズを通じて実装できます。</span><span class="sxs-lookup"><span data-stu-id="607c5-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="607c5-113">以下の図は、精算ページのす新規送付先住所モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="607c5-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![精算ページの出荷先住所モジュールの例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="607c5-115">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="607c5-115">Module properties</span></span>

| <span data-ttu-id="607c5-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="607c5-116">Property name</span></span> | <span data-ttu-id="607c5-117">値</span><span class="sxs-lookup"><span data-stu-id="607c5-117">Values</span></span> | <span data-ttu-id="607c5-118">説明</span><span class="sxs-lookup"><span data-stu-id="607c5-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="607c5-119">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="607c5-119">Heading</span></span> | <span data-ttu-id="607c5-120">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="607c5-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="607c5-121">出荷先住所モジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="607c5-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="607c5-122">住所タイプを表示する</span><span class="sxs-lookup"><span data-stu-id="607c5-122">Show address type</span></span> | <span data-ttu-id="607c5-123">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="607c5-123">**True** or **False**</span></span> | <span data-ttu-id="607c5-124">このオプションのプロパティが **True** に設定されている場合は、**自宅** や **勤務先** などの住所タイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="607c5-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="607c5-125">住所タイプが指定されていない場合、住所は **タイプ**=**その他** として自動的に保存され ます。</span><span class="sxs-lookup"><span data-stu-id="607c5-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="607c5-126">自動提案の有効化</span><span class="sxs-lookup"><span data-stu-id="607c5-126">Enable auto suggestion</span></span>| <span data-ttu-id="607c5-127">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="607c5-127">**True** or **False**</span></span> | <span data-ttu-id="607c5-128">このオプションのプロパティが **True** に設定されている場合は、住所の自動提案が提供されます。</span><span class="sxs-lookup"><span data-stu-id="607c5-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="607c5-129">これらの提案は、Bing Maps を利用しています。</span><span class="sxs-lookup"><span data-stu-id="607c5-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="607c5-130">サイトに Bing Maps を統合する設定方法の詳細については、[店舗のセレクター モジュール](store-selector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="607c5-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="607c5-131">この機能は、Commerce バージョン 10.0.15 リリース以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="607c5-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="607c5-132">自動提案のオプション</span><span class="sxs-lookup"><span data-stu-id="607c5-132">Auto suggest options</span></span>| <span data-ttu-id="607c5-133">数</span><span class="sxs-lookup"><span data-stu-id="607c5-133">A number</span></span>| <span data-ttu-id="607c5-134">住所の自動提案が有効になっている場合は、提供する必要のある提案の最大数など、追加のオプションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="607c5-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="607c5-135">精算ページに出荷先住所モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="607c5-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="607c5-136">出荷先住所モジュールは、精算モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="607c5-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="607c5-137">出荷先住所モジュールをコンフィギュレーションして精算ページに追加する方法の詳細については、[精算モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="607c5-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="607c5-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="607c5-138">Additional resources</span></span>

[<span data-ttu-id="607c5-139">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="607c5-140">カート アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="607c5-141">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="607c5-142">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="607c5-143">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="607c5-144">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="607c5-145">注文詳細モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="607c5-146">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="607c5-147">店舗セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="607c5-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]