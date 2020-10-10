---
title: 配送オプション モジュール
description: このトピックでは、配送オプション モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。
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
ms.openlocfilehash: 39e597b88afcca69623b1a23acc95e4da3873082
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818302"
---
# <a name="delivery-options-module"></a><span data-ttu-id="87bbe-103">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87bbe-104">このトピックでは、配送オプション モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87bbe-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87bbe-105">概要</span><span class="sxs-lookup"><span data-stu-id="87bbe-105">Overview</span></span>

<span data-ttu-id="87bbe-106">配送オプション モジュールを使用すると、顧客は、オンライン注文の配送や受取などの配送方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="87bbe-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="87bbe-107">配送モードを決定するには、配送先住所が必要です。</span><span class="sxs-lookup"><span data-stu-id="87bbe-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="87bbe-108">配送先住所が変更になると、配送オプションを再度取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="87bbe-109">注文に店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="87bbe-110">配送モードのコンフィギュレーションについては、[オンライン チャネル設定](channel-setup-online.md) と [配送モードの設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87bbe-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="87bbe-111">各配送モードでは、関連付けられている料金を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="87bbe-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="87bbe-112">オンライン ストアの諸費用を設定する方法の詳細については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87bbe-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="87bbe-113">Commerce バージョン 10.0.13 では、配送オプション モジュールが、**比例配分なしのヘッダー料金** と **明細行手数料での配送** 機能をサポートするように更新されました。</span><span class="sxs-lookup"><span data-stu-id="87bbe-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="87bbe-114">比例配分がオフになっている場合、電子商取引ワークフローでは、カート内の品目に対して配送の混合モードを許可しないことが予想されます (つまり、いくつかの品目は配送用に選択されていますが、他の品目は受取用に選択されています)。</span><span class="sxs-lookup"><span data-stu-id="87bbe-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="87bbe-115">**比例配分なしのヘッダー料金** 機能を使用するには、**チャネルで一貫した配送モード処理を有効にする** フラグを Commerce Headquarters でオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="87bbe-116">フラグがオンになっているとき、送料は Commerce Headquarters でのコンフィギュレーションに応じて、ヘッダー レベルまたは明細行レベルのいずれかで適用されます。</span><span class="sxs-lookup"><span data-stu-id="87bbe-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="87bbe-117">Fabrikam のテーマは、一部の品目が配送用に選択されていて、その他の品目が受取用に選択される、配送の混合モードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="87bbe-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="87bbe-118">このモードでは、発送方法として選択されたすべての品目について、送料が比例配分になります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="87bbe-119">配送の混在モードを機能させるには、最初に、**比例配分ありのヘッダー料金** 機能を Commerce Headquarters でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="87bbe-120">このコンフィギュレーションの詳細については、[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87bbe-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="87bbe-121">明細行品目に送料が適用される場合は、品目ごとにカート明細に表示されます。</span><span class="sxs-lookup"><span data-stu-id="87bbe-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="87bbe-122">この機能を使用するには、**明細行品目で送料を表示** プロパティをカート モジュールとチェックアウト モジュールの両方に対してオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="87bbe-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="87bbe-123">詳細については、[カート モジュール](add-cart-module.md) と [チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87bbe-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="87bbe-124">次の図は、Fabrikam のチェックアウト ページにおける配送オプション モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="87bbe-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![チェックアウトページにおける配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="87bbe-126">配送オプション モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="87bbe-126">Delivery options module properties</span></span>

| <span data-ttu-id="87bbe-127">プロパティ</span><span class="sxs-lookup"><span data-stu-id="87bbe-127">Property</span></span> | <span data-ttu-id="87bbe-128">値</span><span class="sxs-lookup"><span data-stu-id="87bbe-128">Values</span></span> | <span data-ttu-id="87bbe-129">説明</span><span class="sxs-lookup"><span data-stu-id="87bbe-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="87bbe-130">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="87bbe-130">Heading</span></span> | <span data-ttu-id="87bbe-131">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="87bbe-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="87bbe-132">配送オプションモジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="87bbe-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="87bbe-133">カスタム CSS クラス名</span><span class="sxs-lookup"><span data-stu-id="87bbe-133">Custom CSS class name</span></span> | <span data-ttu-id="87bbe-134">テキスト</span><span class="sxs-lookup"><span data-stu-id="87bbe-134">Text</span></span> | <span data-ttu-id="87bbe-135">該当する場合、このモジュールをレンダリングするために使用される カスタム カスケード スタイル シート (CSS) クラス名。</span><span class="sxs-lookup"><span data-stu-id="87bbe-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="87bbe-136">フィルター配送モードのオプション</span><span class="sxs-lookup"><span data-stu-id="87bbe-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="87bbe-137">**フィルター処理しない** または **非発送モード**</span><span class="sxs-lookup"><span data-stu-id="87bbe-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="87bbe-138">配送オプション モジュールがすべての発送以外の配送モードを除外するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="87bbe-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="87bbe-139">チェックアウト ページに配送オプション モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="87bbe-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="87bbe-140">配送オプション モジュールは、チェックアウト モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="87bbe-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="87bbe-141">配送オプション モジュールをコンフィギュレーションしてチェックアウト ページに追加する方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87bbe-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87bbe-142">追加リソース</span><span class="sxs-lookup"><span data-stu-id="87bbe-142">Additional resources</span></span>

[<span data-ttu-id="87bbe-143">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="87bbe-144">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="87bbe-145">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="87bbe-146">配送先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="87bbe-147">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="87bbe-148">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="87bbe-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="87bbe-149">オンライン チャネル設定</span><span class="sxs-lookup"><span data-stu-id="87bbe-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="87bbe-150">オムニ チャネルの高度な自動請求</span><span class="sxs-lookup"><span data-stu-id="87bbe-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="87bbe-151">ヘッダー料金を販売明細行と一致するよう比例配分する</span><span class="sxs-lookup"><span data-stu-id="87bbe-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="87bbe-152">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="87bbe-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
