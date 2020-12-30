---
title: 出荷先住所モジュール
description: このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413914"
---
# <a name="shipping-address-module"></a><span data-ttu-id="35b57-103">発送先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35b57-104">このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="35b57-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35b57-105">概要</span><span class="sxs-lookup"><span data-stu-id="35b57-105">Overview</span></span>

<span data-ttu-id="35b57-106">出荷先住所モジュールにより、顧客がチェックアウト フロー中に注文の出荷先住所を追加または選択できます。</span><span class="sxs-lookup"><span data-stu-id="35b57-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="35b57-107">顧客がサインインしている場合、その顧客用に以前に保存されたすべての住所が表示され、そこから選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="35b57-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="35b57-108">顧客は、新しい住所を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="35b57-108">The customer can also add a new address.</span></span> <span data-ttu-id="35b57-109">出荷先住所モジュールは、出荷を必要とする注文のすべての品目に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="35b57-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="35b57-110">Commerce 本社では、国や地域ごとに送付先住所の形式を定義することができます。その後、送付先住所モジュールは、国/地域に固有のルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="35b57-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="35b57-111">顧客がチェックアウト フロー中に送付先住所を入力する場合、オプションでその住所を基本住所として保存することができます。</span><span class="sxs-lookup"><span data-stu-id="35b57-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="35b57-112">このオプションは、顧客がログインしている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="35b57-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="35b57-113">送付先住所モジュールでは住所検証はおこないませんが、この機能はカスタマイズを通じて実装できます。</span><span class="sxs-lookup"><span data-stu-id="35b57-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="35b57-114">以下の図は、精算ページのす新規送付先住所モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="35b57-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![精算ページの出荷先住所モジュールの例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="35b57-116">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="35b57-116">Module properties</span></span>

| <span data-ttu-id="35b57-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="35b57-117">Property name</span></span> | <span data-ttu-id="35b57-118">値</span><span class="sxs-lookup"><span data-stu-id="35b57-118">Values</span></span> | <span data-ttu-id="35b57-119">説明</span><span class="sxs-lookup"><span data-stu-id="35b57-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="35b57-120">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="35b57-120">Heading</span></span> | <span data-ttu-id="35b57-121">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="35b57-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="35b57-122">出荷先住所モジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="35b57-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="35b57-123">住所タイプを表示する</span><span class="sxs-lookup"><span data-stu-id="35b57-123">Show address type</span></span> | <span data-ttu-id="35b57-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="35b57-124">**True** or **False**</span></span> | <span data-ttu-id="35b57-125">このオプションのプロパティが **True** に設定されている場合は、**自宅** や **勤務先** などの住所タイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="35b57-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="35b57-126">住所タイプが指定されていない場合、住所は **タイプ**=**その他** として自動的に保存され ます。</span><span class="sxs-lookup"><span data-stu-id="35b57-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="35b57-127">精算ページに出荷先住所モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="35b57-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="35b57-128">出荷先住所モジュールは、精算モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="35b57-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="35b57-129">出荷先住所モジュールをコンフィギュレーションして精算ページに追加する方法の詳細については、[精算モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35b57-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35b57-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="35b57-130">Additional resources</span></span>

[<span data-ttu-id="35b57-131">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="35b57-132">カート アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="35b57-133">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="35b57-134">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="35b57-135">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="35b57-136">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="35b57-137">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="35b57-138">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="35b57-138">Gift card module</span></span>](add-giftcard.md)
