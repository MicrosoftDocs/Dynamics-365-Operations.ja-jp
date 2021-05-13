---
title: 配送オプション モジュール
description: このトピックでは、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
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
ms.openlocfilehash: 12b0281a27dcf5f567bcd6be5530fa8e26a4ae99
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937485"
---
# <a name="delivery-options-module"></a><span data-ttu-id="7b3b0-103">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7b3b0-104">このトピックでは、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7b3b0-105">配送オプション モジュールを使用すると、顧客は、オンライン注文の配送や受取などの配送方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="7b3b0-106">配送モードを決定するには、配送先住所が必要です。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="7b3b0-107">配送先住所が変更になると、配送オプションを再度取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="7b3b0-108">注文に店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="7b3b0-109">配送モードのコンフィギュレーションについては、[オンライン チャネル設定](channel-setup-online.md) と [配送モードの設定](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="7b3b0-110">各配送モードでは、関連付けられている料金を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="7b3b0-111">オンライン ストアの諸費用を設定する方法の詳細については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="7b3b0-112">Commerce バージョン 10.0.13 では、配送オプション モジュールが、**比例配分なしのヘッダー料金** と **明細行手数料での配送** 機能をサポートするように更新されました。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="7b3b0-113">比例配分がオフになっている場合、電子商取引ワークフローでは、カート内の品目に対して配送の混合モードを許可しないことが予想されます (つまり、いくつかの品目は配送用に選択されていますが、他の品目は受取用に選択されています)。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="7b3b0-114">**比例配分なしのヘッダー料金** 機能を使用するには、**チャネルで一貫した配送モード処理を有効にする** フラグが Commerce 本社でオンになっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="7b3b0-115">機能フラグがオンになっているとき、送料は Commerce 本社でのコンフィギュレーションに応じて、ヘッダー レベルまたは明細行レベルのいずれかで適用されます。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="7b3b0-116">Fabrikam のテーマは、一部の品目が配送用に選択されていて、その他の品目が受取用に選択される、配送の混合モードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="7b3b0-117">このモードでは、発送方法として選択されたすべての品目について、送料が比例配分になります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="7b3b0-118">配送の混在モードを機能させるには、最初に、**比例配分ありのヘッダー料金** 機能を Commerce Headquarters でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="7b3b0-119">このコンフィギュレーションの詳細については、[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="7b3b0-120">明細行品目に送料が適用される場合は、品目ごとにカート明細に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="7b3b0-121">この機能を使用するには、**明細行品目で送料を表示** プロパティをカート モジュールとチェックアウト モジュールの両方に対してオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="7b3b0-122">詳細については、[カート モジュール](add-cart-module.md) と [チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="7b3b0-123">次の図は、Fabrikam のチェックアウト ページにおける配送オプション モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![チェックアウトページにおける配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="7b3b0-125">配送オプション モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b3b0-125">Delivery options module properties</span></span>

| <span data-ttu-id="7b3b0-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7b3b0-126">Property</span></span> | <span data-ttu-id="7b3b0-127">値</span><span class="sxs-lookup"><span data-stu-id="7b3b0-127">Values</span></span> | <span data-ttu-id="7b3b0-128">説明</span><span class="sxs-lookup"><span data-stu-id="7b3b0-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="7b3b0-129">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="7b3b0-129">Heading</span></span> | <span data-ttu-id="7b3b0-130">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="7b3b0-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="7b3b0-131">配送オプションモジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="7b3b0-132">カスタム CSS クラス名</span><span class="sxs-lookup"><span data-stu-id="7b3b0-132">Custom CSS class name</span></span> | <span data-ttu-id="7b3b0-133">テキスト</span><span class="sxs-lookup"><span data-stu-id="7b3b0-133">Text</span></span> | <span data-ttu-id="7b3b0-134">該当する場合、このモジュールをレンダリングするために使用される カスタム カスケード スタイル シート (CSS) クラス名。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="7b3b0-135">フィルター配送モードのオプション</span><span class="sxs-lookup"><span data-stu-id="7b3b0-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="7b3b0-136">**フィルター処理しない** または **非発送モード**</span><span class="sxs-lookup"><span data-stu-id="7b3b0-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="7b3b0-137">配送オプション モジュールがすべての発送以外の配送モードを除外するかどうかを指定する値。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="7b3b0-138">配送オプションの自動選択</span><span class="sxs-lookup"><span data-stu-id="7b3b0-138">Auto select a delivery option</span></span> | <span data-ttu-id="7b3b0-139">**フィルター処理しない**、**配送オプションを自動選択して集計を表示する**、または **配送オプションを自動選択して集計を表示しない**</span><span class="sxs-lookup"><span data-stu-id="7b3b0-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="7b3b0-140">このプロパティは、ユーザーが選択しなくても、最初に使用可能な配送オプションを自動的にチェック アウトに適用します。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="7b3b0-141">このオプションは、使用可能な配送オプションが 1 つしかない場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="7b3b0-142">このプロパティは、Commerce バージョン 10.0.19 リリース以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="7b3b0-143">チェックアウト ページに配送オプション モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="7b3b0-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="7b3b0-144">配送オプション モジュールは、チェックアウト モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="7b3b0-145">配送オプション モジュールをコンフィギュレーションしてチェックアウト ページに追加する方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3b0-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b3b0-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7b3b0-146">Additional resources</span></span>

[<span data-ttu-id="7b3b0-147">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7b3b0-148">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7b3b0-149">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7b3b0-150">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7b3b0-151">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="7b3b0-152">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7b3b0-153">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="7b3b0-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="7b3b0-154">オンライン チャネル設定</span><span class="sxs-lookup"><span data-stu-id="7b3b0-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="7b3b0-155">オムニ チャネルの高度な自動請求</span><span class="sxs-lookup"><span data-stu-id="7b3b0-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="7b3b0-156">ヘッダー料金を販売明細行と一致するよう比例配分する</span><span class="sxs-lookup"><span data-stu-id="7b3b0-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="7b3b0-157">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="7b3b0-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
