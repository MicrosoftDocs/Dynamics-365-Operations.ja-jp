---
title: 配送オプション モジュール
description: このトピックでは、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f97dcd42e22e319d9af7cbf57fce7c10d8565d04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801999"
---
# <a name="delivery-options-module"></a><span data-ttu-id="b0686-103">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0686-104">このトピックでは、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0686-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b0686-105">配送オプション モジュールを使用すると、顧客は、オンライン注文の配送や受取などの配送方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b0686-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="b0686-106">配送モードを決定するには、配送先住所が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0686-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="b0686-107">配送先住所が変更になると、配送オプションを再度取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0686-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="b0686-108">注文に店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="b0686-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="b0686-109">配送モードのコンフィギュレーションについては、[オンライン チャネル設定](channel-setup-online.md) と [配送モードの設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0686-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="b0686-110">各配送モードでは、関連付けられている料金を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="b0686-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="b0686-111">オンライン ストアの諸費用を設定する方法の詳細については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0686-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="b0686-112">Commerce バージョン 10.0.13 では、配送オプション モジュールが、**比例配分なしのヘッダー料金** と **明細行手数料での配送** 機能をサポートするように更新されました。</span><span class="sxs-lookup"><span data-stu-id="b0686-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="b0686-113">比例配分がオフになっている場合、電子商取引ワークフローでは、カート内の品目に対して配送の混合モードを許可しないことが予想されます (つまり、いくつかの品目は配送用に選択されていますが、他の品目は受取用に選択されています)。</span><span class="sxs-lookup"><span data-stu-id="b0686-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="b0686-114">**比例配分なしのヘッダー料金** 機能を使用するには、**チャネルで一貫した配送モード処理を有効にする** フラグを Commerce Headquarters でオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0686-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="b0686-115">フラグがオンになっているとき、送料は Commerce Headquarters でのコンフィギュレーションに応じて、ヘッダー レベルまたは明細行レベルのいずれかで適用されます。</span><span class="sxs-lookup"><span data-stu-id="b0686-115">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="b0686-116">Fabrikam のテーマは、一部の品目が配送用に選択されていて、その他の品目が受取用に選択される、配送の混合モードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b0686-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="b0686-117">このモードでは、発送方法として選択されたすべての品目について、送料が比例配分になります。</span><span class="sxs-lookup"><span data-stu-id="b0686-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="b0686-118">配送の混在モードを機能させるには、最初に、**比例配分ありのヘッダー料金** 機能を Commerce Headquarters でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0686-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="b0686-119">このコンフィギュレーションの詳細については、[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0686-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="b0686-120">明細行品目に送料が適用される場合は、品目ごとにカート明細に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0686-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="b0686-121">この機能を使用するには、**明細行品目で送料を表示** プロパティをカート モジュールとチェックアウト モジュールの両方に対してオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0686-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="b0686-122">詳細については、[カート モジュール](add-cart-module.md) と [チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0686-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="b0686-123">次の図は、Fabrikam のチェックアウト ページにおける配送オプション モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="b0686-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![チェックアウトページにおける配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="b0686-125">配送オプション モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0686-125">Delivery options module properties</span></span>

| <span data-ttu-id="b0686-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0686-126">Property</span></span> | <span data-ttu-id="b0686-127">値</span><span class="sxs-lookup"><span data-stu-id="b0686-127">Values</span></span> | <span data-ttu-id="b0686-128">説明</span><span class="sxs-lookup"><span data-stu-id="b0686-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="b0686-129">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b0686-129">Heading</span></span> | <span data-ttu-id="b0686-130">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="b0686-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b0686-131">配送オプションモジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="b0686-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="b0686-132">カスタム CSS クラス名</span><span class="sxs-lookup"><span data-stu-id="b0686-132">Custom CSS class name</span></span> | <span data-ttu-id="b0686-133">テキスト</span><span class="sxs-lookup"><span data-stu-id="b0686-133">Text</span></span> | <span data-ttu-id="b0686-134">該当する場合、このモジュールをレンダリングするために使用される カスタム カスケード スタイル シート (CSS) クラス名。</span><span class="sxs-lookup"><span data-stu-id="b0686-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="b0686-135">フィルター配送モードのオプション</span><span class="sxs-lookup"><span data-stu-id="b0686-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="b0686-136">**フィルター処理しない** または **非発送モード**</span><span class="sxs-lookup"><span data-stu-id="b0686-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="b0686-137">配送オプション モジュールがすべての発送以外の配送モードを除外するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="b0686-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b0686-138">チェックアウト ページに配送オプション モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="b0686-138">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b0686-139">配送オプション モジュールは、チェックアウト モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="b0686-139">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="b0686-140">配送オプション モジュールをコンフィギュレーションしてチェックアウト ページに追加する方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0686-140">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0686-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b0686-141">Additional resources</span></span>

[<span data-ttu-id="b0686-142">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b0686-143">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b0686-144">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b0686-145">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b0686-146">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-146">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b0686-147">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b0686-148">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="b0686-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b0686-149">オンライン チャネル設定</span><span class="sxs-lookup"><span data-stu-id="b0686-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="b0686-150">オムニ チャネルの高度な自動請求</span><span class="sxs-lookup"><span data-stu-id="b0686-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b0686-151">ヘッダー料金を販売明細行と一致するよう比例配分する</span><span class="sxs-lookup"><span data-stu-id="b0686-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="b0686-152">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="b0686-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]