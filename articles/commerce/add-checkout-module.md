---
title: チェックアウト モジュール
description: このトピックでは、ページにチェックアウト モジュールを追加し、必要なプロパティを設定する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e800daa6eeb54a2eda535cb57aa45559b59b4ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206466"
---
# <a name="checkout-module"></a><span data-ttu-id="24bda-103">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-103">Checkout module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24bda-104">このトピックでは、ページにチェックアウト モジュールを追加し、必要なプロパティを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="24bda-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

<span data-ttu-id="24bda-105">チェックアウト モジュールは、注文を作成するために必要なすべてのモジュールをホストする特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="24bda-105">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="24bda-106">これは、顧客が購買を行うのに必要なすべての情報を入力するために使用する、ステップバイステップのフローを示します。</span><span class="sxs-lookup"><span data-stu-id="24bda-106">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="24bda-107">これは、出荷先住所、配送方法、および請求書情報を示します。</span><span class="sxs-lookup"><span data-stu-id="24bda-107">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="24bda-108">また、注文集計や、顧客注文に関連するその他の情報も表示されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-108">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="24bda-109">チェックアウト モジュールは、カート ID に基づくデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="24bda-109">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="24bda-110">このカート ID は、ブラウザー Cookie として保存されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-110">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="24bda-111">カート ID は、注文の品目、合計金額、割引などの情報をチェックアウト モジュールで表示するために必要です。</span><span class="sxs-lookup"><span data-stu-id="24bda-111">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="24bda-112">以下の図は、Fabrikam の精算ページにおける精算モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="24bda-112">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![精算モジュールの例](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="24bda-114">チェックアウト モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="24bda-114">Checkout module properties</span></span>

<span data-ttu-id="24bda-115">チェックアウト モジュールは、注文集計および注文を行うための機能を表示します。</span><span class="sxs-lookup"><span data-stu-id="24bda-115">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="24bda-116">注文を配置する前に必要なすべての顧客情報を収集するには、追加モジュールをチェックアウト モジュールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24bda-116">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="24bda-117">したがって、小売業者は、各自の要件に基づいてカスタム モジュールをチェックアウト フローに追加したり、モジュールを除外したりする柔軟性を備えています。</span><span class="sxs-lookup"><span data-stu-id="24bda-117">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

| <span data-ttu-id="24bda-118">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="24bda-118">Property name</span></span> | <span data-ttu-id="24bda-119">値</span><span class="sxs-lookup"><span data-stu-id="24bda-119">Values</span></span> | <span data-ttu-id="24bda-120">説明</span><span class="sxs-lookup"><span data-stu-id="24bda-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="24bda-121">チェックアウト ヘッダー</span><span class="sxs-lookup"><span data-stu-id="24bda-121">Checkout heading</span></span> | <span data-ttu-id="24bda-122">ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**)</span><span class="sxs-lookup"><span data-stu-id="24bda-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="24bda-123">チェックアウト モジュールのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="24bda-123">A heading for the checkout module.</span></span> |
| <span data-ttu-id="24bda-124">注文集計のヘッダー</span><span class="sxs-lookup"><span data-stu-id="24bda-124">Order summary heading</span></span> | <span data-ttu-id="24bda-125">ヘッダー テキスト</span><span class="sxs-lookup"><span data-stu-id="24bda-125">Heading text</span></span> | <span data-ttu-id="24bda-126">モジュールの注文集計セクションのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="24bda-126">A heading for the order summary section of the module.</span></span> |
| <span data-ttu-id="24bda-127">カート明細行品目のヘッダー</span><span class="sxs-lookup"><span data-stu-id="24bda-127">Cart line items heading</span></span> | <span data-ttu-id="24bda-128">ヘッダー テキスト</span><span class="sxs-lookup"><span data-stu-id="24bda-128">Heading text</span></span> | <span data-ttu-id="24bda-129">チェックアウト モジュールに表示されるカート明細行品目のヘッダー。</span><span class="sxs-lookup"><span data-stu-id="24bda-129">A heading for cart line items that are shown in the checkout module.</span></span> |
| <span data-ttu-id="24bda-130">明細行品目での出荷費用の表示</span><span class="sxs-lookup"><span data-stu-id="24bda-130">Show shipping charges on line item</span></span> | <span data-ttu-id="24bda-131">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="24bda-131">**True** or **False**</span></span> | <span data-ttu-id="24bda-132">このプロパティが **True** に設定されている場合、明細行品目に適用される出荷費用がカート明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-132">If this property is set to **True**, the shipping charges that are applicable for line items will be shown on cart lines.</span></span> <span data-ttu-id="24bda-133">**比例配分なしのヘッダー料金** 機能が Commerce Headquarters で有効になっている場合、出荷費用は明細行レベルではなくヘッダー レベルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-133">If the **Header charge with no proration** feature is turned on in Commerce headquarters, the shipping charge will be applied at the header level, not the line level.</span></span> <span data-ttu-id="24bda-134">この機能は、Commerce バージョン 10.0.13 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="24bda-134">This feature was added in Commerce version 10.0.13.</span></span> |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="24bda-135">チェックアウト モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-135">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="24bda-136">**出荷先住所** – このモジュールにより、顧客が注文の出荷先住所を追加または選択できます。</span><span class="sxs-lookup"><span data-stu-id="24bda-136">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="24bda-137">このモジュールの詳細については、[出荷先住所モジュール](ship-address-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24bda-137">For more information about this module, see [Shipping address module](ship-address-module.md).</span></span>

    <span data-ttu-id="24bda-138">以下の図は、Fabrikam の精算ページにおける配送先住所モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="24bda-138">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![配送先住所モジュールの例](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="24bda-140">**配送オプション** – このモジュールにより、顧客は注文の配送モードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="24bda-140">**Delivery options** – This module lets a customer select a mode of delivery for an order.</span></span> <span data-ttu-id="24bda-141">このモジュールの詳細については、[配送オプション モジュール](delivery-options-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24bda-141">For more information about this module, see [Delivery options module](delivery-options-module.md).</span></span>

    <span data-ttu-id="24bda-142">以下の図は、Fabrikam の精算ページにおける配送オプション モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="24bda-142">The following image shows an example of a delivery options module on a checkout page.</span></span>
 
    ![配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="24bda-144">**チェックアウト セクション コンテナー** – このモジュールは、複数のモジュールを内側に配置して、チェックアウト フロー内にセクションを作成できるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="24bda-144">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="24bda-145">たとえば、すべての支払関連モジュールをこのコンテナー内に配置し、1 つのセクションとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="24bda-145">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="24bda-146">このモジュールは、フローのレイアウトにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="24bda-146">This module affects only the layout of the flow.</span></span>

- <span data-ttu-id="24bda-147">**ギフト カード** – このモジュールにより、顧客はギフト カードを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="24bda-147">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="24bda-148">このモジュールの詳細については、[ギフト カード モジュール](add-giftcard.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24bda-148">For more information about this module, see [Gift card module](add-giftcard.md).</span></span>

- <span data-ttu-id="24bda-149">**ロイヤルティ ポイント** – このモジュールにより、顧客はロイヤルティ ポイントを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="24bda-149">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="24bda-150">利用可能なポイントと期限が切れるポイントの概要を提供し、顧客が引き換えるポイント数を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="24bda-150">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="24bda-151">顧客がサインインしていないかロイヤルティ メンバーではない場合、またはカート内の合計金額が 0 (ゼロ) の場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="24bda-151">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>

- <span data-ttu-id="24bda-152">**支払** – このモジュールにより、顧客はクレジット カードやデビット カードを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="24bda-152">**Payment** – This module lets a customer pay for an order by using a credit or debit card.</span></span> <span data-ttu-id="24bda-153">顧客は、選択した支払オプションの請求先住所を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="24bda-153">Customers can also provide a billing address for the payment option that they select.</span></span> <span data-ttu-id="24bda-154">このモジュールの詳細については、[支払モジュール](payment-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24bda-154">For more information about this module, see [Payment module](payment-module.md).</span></span>

    <span data-ttu-id="24bda-155">次の図は、チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="24bda-155">The following image shows an example of gift card, loyalty points, and payment modules on a checkout page.</span></span>

    ![チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例](./media/ecommerce-payments.PNG)

- <span data-ttu-id="24bda-157">**連絡先情報** – このモジュールにより、顧客は注文に対する連絡先情報 (電子メール アドレス) を追加または変更できます。</span><span class="sxs-lookup"><span data-stu-id="24bda-157">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="24bda-158">**テキスト ブロック** – このモジュールには、コンテンツ管理システム (CMS) によって発生する任意のメッセージングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="24bda-158">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="24bda-159">たとえば、"注文に関する問題については、1-800-Fabrikam にお問い合わせください" というメッセージが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="24bda-159">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

- <span data-ttu-id="24bda-160">**チェックアウトの使用条件**: このモジュールでは、使用条件を含むリッチ テキストと、顧客入力のチェック ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="24bda-160">**Checkout terms and conditions** – This module shows rich text that contains the terms and conditions and a check box for the customer input.</span></span> <span data-ttu-id="24bda-161">このチェック ボックスはオプションで、コンフィギュレーション可能です。</span><span class="sxs-lookup"><span data-stu-id="24bda-161">The check box is optional and configurable.</span></span> <span data-ttu-id="24bda-162">入力はモジュールによってキャプチャされ、発注が開始される前のチェックとして使用できますが、注文の概要情報には含まれません。</span><span class="sxs-lookup"><span data-stu-id="24bda-162">The input is captured by the module and can be used as a check before order placement is triggered, but it isn't included in the order summary information.</span></span> <span data-ttu-id="24bda-163">このモジュールは、ビジネス ニーズに応じて、チェックアウト コンテナー、チェックアウト セクション コンテナー、または使用条件スロットに追加できます。</span><span class="sxs-lookup"><span data-stu-id="24bda-163">This module can be added to the checkout container, checkout section container, or terms and conditions slot, according to business needs.</span></span> <span data-ttu-id="24bda-164">チェックアウト コンテナーまたはチェックアウト セクション コンテナーのスロットに追加された場合は、チェックアウト プロセスでステップとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-164">If it's added to the checkout container or checkout section container slot, it will appear as a step in the checkout process.</span></span> <span data-ttu-id="24bda-165">使用条件スロットに追加されると、発注ボタンの近くに表示されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-165">If it's added to the terms and conditions slot, it will appear near the order placement button.</span></span>

    <span data-ttu-id="24bda-166">次の図は、チェックアウト ページの使用条件の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="24bda-166">The following image shows an example of terms and conditions on a checkout page.</span></span>

    ![チェックアウト ページの使用条件の例](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="24bda-168">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="24bda-168">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="24bda-169">出荷先住所や出荷方法など、チェックアウト情報のほとんどはカートに保管され、注文の一部として処理されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-169">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="24bda-170">唯一の例外は、クレジット カード情報です。</span><span class="sxs-lookup"><span data-stu-id="24bda-170">The only exception is the credit card information.</span></span> <span data-ttu-id="24bda-171">この情報は、Adyen 支払コネクタを使用して直接処理されます。</span><span class="sxs-lookup"><span data-stu-id="24bda-171">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="24bda-172">支払は承認されていますが、注文が履行されるまで請求されません。</span><span class="sxs-lookup"><span data-stu-id="24bda-172">The payment is authorized, but it isn't charged until the order is fulfilled.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="24bda-173">新規ページに精算モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="24bda-173">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="24bda-174">新しいページにチェックアウト モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="24bda-174">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="24bda-175">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="24bda-175">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="24bda-176">**新規フラグメント** ダイアログ ボックスで、**チェックアウト** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-176">In the **New fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="24bda-177">**フラグメント名** で、**チェックアウト フラグメント** と名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-177">Under **Fragment name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="24bda-178">**精算モジュール** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-178">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="24bda-179">右側の [プロパティ] ウィンドウで、鉛筆の記号を選択し、フィールドに見出しテキストを入力し、続いてチェックマーク記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-179">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="24bda-180">**精算情報** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-180">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="24bda-181">**モジュールの追加** ダイアログ ボックスで、**配送先住所**、 **出荷オプション**、**精算セクション コンテナー**、**連絡先情報** の各モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-181">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="24bda-182">**精算セクション コンテナー** モジュールで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-182">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="24bda-183">**モジュールの追加** ダイアログ ボックスで、**ギフト カード**, **ロイヤルティ**、**支払い** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24bda-183">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="24bda-184">このようにして、すべての支払方法が 1 つのセクションにまとめて表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="24bda-184">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="24bda-185">**使用条件** スロットで、必要に応じて、**チェックアウトの使用条件** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="24bda-185">In the **Terms and conditions** slot, add a **Checkout terms and conditions** module if it's required.</span></span> <span data-ttu-id="24bda-186">モジュールのプロパティ ペインで、使用条件テキストを必要に応じてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="24bda-186">In the module's properties pane, configure the terms and condition text as appropriate.</span></span>
1. <span data-ttu-id="24bda-187">**保存** を選択し、 続いて **プレビュー** を選択してフラグメントをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="24bda-187">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="24bda-188">カート コンテキストがない一部のモジュールは、プレビューで表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="24bda-188">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="24bda-189">**編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="24bda-189">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="24bda-190">新しいチェックアウト フラグメントを使用するテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="24bda-190">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="24bda-191">新しいテンプレートを使用するチェックアウト ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="24bda-191">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24bda-192">追加リソース</span><span class="sxs-lookup"><span data-stu-id="24bda-192">Additional resources</span></span>

[<span data-ttu-id="24bda-193">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-193">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="24bda-194">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-194">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="24bda-195">支払モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-195">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="24bda-196">出荷先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-196">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="24bda-197">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-197">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="24bda-198">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-198">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="24bda-199">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-199">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="24bda-200">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="24bda-200">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]