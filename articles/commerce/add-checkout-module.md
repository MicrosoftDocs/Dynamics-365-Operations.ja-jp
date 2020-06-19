---
title: チェックアウト モジュール
description: このトピックでは、ページにチェックアウト モジュールを追加し、必要なプロパティを設定する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411207"
---
# <a name="checkout-module"></a><span data-ttu-id="9583d-103">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-103">Checkout module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9583d-104">このトピックでは、ページにチェックアウト モジュールを追加し、必要なプロパティを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9583d-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="9583d-105">概要</span><span class="sxs-lookup"><span data-stu-id="9583d-105">Overview</span></span>

<span data-ttu-id="9583d-106">チェックアウト モジュールは、注文を作成するために必要なすべてのモジュールをホストする特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="9583d-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="9583d-107">これは、顧客が購買を行うのに必要なすべての情報を入力するために使用する、ステップバイステップのフローを示します。</span><span class="sxs-lookup"><span data-stu-id="9583d-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="9583d-108">これは、出荷先住所、配送方法、および請求書情報を示します。</span><span class="sxs-lookup"><span data-stu-id="9583d-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="9583d-109">また、注文集計や、顧客注文に関連するその他の情報も表示されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="9583d-110">チェックアウト モジュールは、カート ID に基づくデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="9583d-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="9583d-111">このカート ID は、ブラウザー Cookie として保存されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="9583d-112">カート ID は、注文の品目、合計金額、割引などの情報をチェックアウト モジュールで表示するために必要です。</span><span class="sxs-lookup"><span data-stu-id="9583d-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="9583d-113">以下の図は、Fabrikam の精算ページにおける精算モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9583d-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![精算モジュールの例](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="9583d-115">チェックアウト モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="9583d-115">Checkout module properties</span></span>

<span data-ttu-id="9583d-116">チェックアウト モジュールは、注文集計および注文を行うための機能を表示します。</span><span class="sxs-lookup"><span data-stu-id="9583d-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="9583d-117">注文を配置する前に必要なすべての顧客情報を収集するには、追加モジュールをチェックアウト モジュールに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9583d-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="9583d-118">したがって、小売業者は、各自の要件に基づいてカスタム モジュールをチェックアウト フローに追加したり、モジュールを除外したりする柔軟性を備えています。</span><span class="sxs-lookup"><span data-stu-id="9583d-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

### <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="9583d-119">チェックアウト モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-119">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="9583d-120">**出荷先住所** – このモジュールにより、顧客が注文の出荷先住所を追加または選択できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-120">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="9583d-121">顧客がサインインしている場合、その顧客用に以前に保存されたすべての住所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-121">If the customer is signed in, any addresses that were previously saved for that customer are shown.</span></span> <span data-ttu-id="9583d-122">顧客は、それらの住所の中から選択できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-122">The customer can then select among those addresses.</span></span> <span data-ttu-id="9583d-123">顧客は、新しい住所を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="9583d-123">The customer can also add a new address.</span></span> <span data-ttu-id="9583d-124">出荷先住所は、出荷を必要とする注文のすべての品目に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-124">The shipping address is used for all the items in the order that require shipping.</span></span> <span data-ttu-id="9583d-125">個別の明細行品目に対してカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9583d-125">It can't be customized for individual line items.</span></span> <span data-ttu-id="9583d-126">出荷先住所の形式は国または地域ごとに定義され、このモジュールでは国/地域固有のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-126">Shipping address formats are defined for each country or region, and the country/region-specific rules are enforced by this module.</span></span> <span data-ttu-id="9583d-127">このモジュールでは住所検証は提供されませんが、住所検証はカスタマイズを通じて実装できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-127">Although this module doesn't provide address validation, address validation can be implemented through customization.</span></span> <span data-ttu-id="9583d-128">注文に、店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="9583d-128">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>

    <span data-ttu-id="9583d-129">以下の図は、Fabrikam の精算ページにおける配送先住所モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9583d-129">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![配送先住所モジュールの例](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="9583d-131">**出荷オプション** – このモジュールにより、顧客は注文の出荷オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-131">**Delivery options** – This module lets a customer select a delivery option for an order.</span></span> <span data-ttu-id="9583d-132">出荷オプションは、出荷先住所に基づきます。</span><span class="sxs-lookup"><span data-stu-id="9583d-132">Delivery options are based on the shipping address.</span></span> <span data-ttu-id="9583d-133">出荷先住所が変更された場合、出荷オプションを再度取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9583d-133">If the shipping address is changed, the delivery options must be retrieved again.</span></span> <span data-ttu-id="9583d-134">注文に、店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="9583d-134">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>

    <span data-ttu-id="9583d-135">以下の図は、Fabrikam の精算ページにおける配送オプション モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9583d-135">The following image shows an example of a delivery options module on a checkout page.</span></span>

    ![配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="9583d-137">**チェックアウト セクション コンテナー** – このモジュールは、複数のモジュールを内側に配置して、チェックアウト フロー内にセクションを作成できるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="9583d-137">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="9583d-138">たとえば、すべての支払関連モジュールをこのコンテナー内に配置し、1 つのセクションとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-138">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="9583d-139">このモジュールは、フローのレイアウトにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="9583d-139">This module affects only the layout of the flow.</span></span>
- <span data-ttu-id="9583d-140">**ギフト カード** – このモジュールにより、顧客はギフト カードを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-140">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="9583d-141">Microsoft Dynamics 365 Commerce ギフト カードのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9583d-141">It supports only Microsoft Dynamics 365 Commerce gift cards.</span></span> <span data-ttu-id="9583d-142">1 枚以上のギフト カードを注文に適用できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-142">One or more gift cards can be applied to an order.</span></span> <span data-ttu-id="9583d-143">ギフト カードの残高がカート内の金額に対応しない場合は、ギフト カードと他の支払方法とを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-143">If the balance of the gift card doesn't cover the amount in the cart, the gift card can be combined with another payment method.</span></span> <span data-ttu-id="9583d-144">ギフト カードは、顧客がサインインしている場合にのみ引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-144">Gift cards can be redeemed only if the customer is signed in.</span></span>
- <span data-ttu-id="9583d-145">**ロイヤルティ ポイント** – このモジュールにより、顧客はロイヤルティ ポイントを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-145">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="9583d-146">利用可能なポイントと期限が切れるポイントの概要を提供し、顧客が引き換えるポイント数を選択できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9583d-146">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="9583d-147">顧客がサインインしていないかロイヤルティ メンバーではない場合、またはカート内の合計金額が 0 (ゼロ) の場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="9583d-147">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>
- <span data-ttu-id="9583d-148">**支払** – このモジュールにより、顧客はクレジット カードを使用して注文に対する支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9583d-148">**Payment** – This module lets a customer pay for an order by using a credit card.</span></span> <span data-ttu-id="9583d-149">カート内の合計金額がロイヤルティ ポイントまたはギフト カードの対象となる場合、または合計金額が 0 (ゼロ) の場合、このモジュールは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="9583d-149">If the total amount in the cart is covered by loyalty points or a gift card, or if it's 0 (zero), this module is automatically hidden.</span></span> <span data-ttu-id="9583d-150">クレジット カード統合は、このモジュールの Adyen 支払コネクタによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-150">Credit card integration is provided by the Adyen payment connector for this module.</span></span> <span data-ttu-id="9583d-151">このコネクタの使用方法の詳細については、[Adyen 向け Dynamics 365 Payment Connector](dev-itpro/adyen-connector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9583d-151">For more information about how to use this connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>
- <span data-ttu-id="9583d-152">**請求先住所** – このモジュールにより、顧客が請求情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-152">**Billing address** – This module lets a customer provide billing information.</span></span> <span data-ttu-id="9583d-153">この情報は、クレジット カード情報と共に Adyen によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-153">This information is processed, together with the credit card information, by Adyen.</span></span> <span data-ttu-id="9583d-154">このモジュールには、顧客が請求先住所を出荷先住所として使用できるようにするオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9583d-154">This module includes an option that lets customers use their billing address as the shipping address.</span></span>

    <span data-ttu-id="9583d-155">次の図は、精算ページのギフト カード、ロイヤルティ ポイント、支払、請求先住所のモジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="9583d-155">The following image shows an example of gift card, loyalty points, payment, and billing address modules on a checkout page.</span></span>

    ![ギフトカード、ロイヤルティ ポイント、支払、請求先住所のモジュールの例](./media/ecommerce-payments.PNG)

- <span data-ttu-id="9583d-157">**連絡先情報** – このモジュールにより、顧客は注文に対する連絡先情報 (電子メール アドレス) を追加または変更できます。</span><span class="sxs-lookup"><span data-stu-id="9583d-157">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="9583d-158">**テキスト ブロック** – このモジュールには、コンテンツ管理システム (CMS) によって発生する任意のメッセージングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9583d-158">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="9583d-159">たとえば、"注文に関する問題については、1-800-Fabrikam にお問い合わせください" というメッセージが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="9583d-159">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="9583d-160">Commerce Scale Unit インタラクション</span><span class="sxs-lookup"><span data-stu-id="9583d-160">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="9583d-161">出荷先住所や出荷方法など、チェックアウト情報のほとんどはカートに保管され、注文の一部として処理されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-161">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="9583d-162">唯一の例外は、クレジット カード情報です。</span><span class="sxs-lookup"><span data-stu-id="9583d-162">The only exception is the credit card information.</span></span> <span data-ttu-id="9583d-163">この情報は、Adyen 支払コネクタを使用して直接処理されます。</span><span class="sxs-lookup"><span data-stu-id="9583d-163">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="9583d-164">支払は承認されていますが、請求されていません。</span><span class="sxs-lookup"><span data-stu-id="9583d-164">The payment is authorized but isn't charged.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="9583d-165">新規ページに精算モジュールを追加して必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="9583d-165">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="9583d-166">新しいページにチェックアウト モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9583d-166">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9583d-167">**ページ フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="9583d-167">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="9583d-168">**新規ページ フラグメント** ダイアログ ボックスで、**精算** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-168">In the **New Page Fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="9583d-169">**ページ フラグメント名**配下で、**精算フラグメント**の名前を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-169">Under **Page Fragment Name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="9583d-170">**精算モジュール** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-170">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="9583d-171">右側の [プロパティ] ウィンドウで、鉛筆の記号を選択し、フィールドに見出しテキストを入力し、続いてチェックマーク記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-171">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="9583d-172">**精算情報**スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-172">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9583d-173">**モジュールの追加**ダイアログ ボックスで、**配送先住所**、 **出荷オプション**、**精算セクション コンテナー**、**連絡先情報** の各モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-173">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="9583d-174">**精算セクション コンテナー**モジュールで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-174">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9583d-175">**モジュールの追加** ダイアログ ボックスで、**ギフト カード**, **ロイヤルティ**、**支払い**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9583d-175">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="9583d-176">このようにして、すべての支払方法が 1 つのセクションにまとめて表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9583d-176">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="9583d-177">**保存** を選択し、 続いて**プレビュー** を選択してフラグメントをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="9583d-177">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="9583d-178">カート コンテキストがない一部のモジュールは、プレビューで表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9583d-178">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="9583d-179">**編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="9583d-179">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="9583d-180">新しいチェックアウト フラグメントを使用するテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="9583d-180">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="9583d-181">新しいテンプレートを使用するチェックアウト ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="9583d-181">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9583d-182">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9583d-182">Additional resources</span></span>

[<span data-ttu-id="9583d-183">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="9583d-183">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9583d-184">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-184">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9583d-185">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-185">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9583d-186">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="9583d-187">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-187">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9583d-188">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-188">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="9583d-189">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="9583d-189">Footer module</span></span>](author-footer-module.md)
