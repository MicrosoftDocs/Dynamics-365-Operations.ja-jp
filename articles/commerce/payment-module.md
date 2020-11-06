---
title: 支払いモジュール
description: このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055384"
---
# <a name="payment-module"></a><span data-ttu-id="f7c9a-103">支払いモジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7c9a-104">このトピックでは、支払いモジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f7c9a-105">概要</span><span class="sxs-lookup"><span data-stu-id="f7c9a-105">Overview</span></span>

<span data-ttu-id="f7c9a-106">支払モジュールにより、顧客はクレジット カードやデビット カードを使用して注文の支払を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="f7c9a-107">このモジュールの支払い統合は、 Dynamics 365 Payment Connector によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="f7c9a-108">支払いコネクタを設定および構成方法についての詳細は、[Adyen 用の Dynamics 365 Payment Connector ](dev-itpro/adyen-connector.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="f7c9a-109">支払モジュールは、HTML インライン フレーム (iframe) でAdyen 経由で提供される支払情報をホストします。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="f7c9a-110">支払モジュールは、Commerce Scale Unit とやり取りして、Adyen 支払情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="f7c9a-111">Commerce Scale Unit のやり取りの一部として、支払モジュールでは、入力した請求先住所情報を iframe で処理するか、別のモジュールとして処理するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="f7c9a-112">Fabrikam テーマでは、請求先住所が別のモジュールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="f7c9a-113">この方法を使用すると、住所の行を出荷先住所の行と類似したものに表示することができるので、書式設定上の柔軟性が高まります。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="f7c9a-114">支払モジュールでは、顧客は支払情報を保存することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="f7c9a-115">支払情報と請求先住所は、Adyen 支払コネクタを介して保存および管理されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="f7c9a-116">支払モジュールは、ロイヤルティ ポイントまたはギフトカードで既にカバーされていない注文費用を対象とします。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="f7c9a-117">注文の合計がロイヤルティ ポイントまたはギフトカード クレジットによって完全に覆われている場合は、支払モジュールが非表示になり、顧客は注文をそのままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="f7c9a-118">Adyen 支払いコネクタは強力な顧客認証 (SCA) もサポートします。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="f7c9a-119">欧州連合 (EU) 決済サービス指令 2.0 (PSD 2.0) の一部では、オンラインで買い物をする人は電子決済方法で決済する場合、自分たちのオンライン ショッピング体験以外で認証を受けることを義務付けています。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="f7c9a-120">チェックアウト フローでは、顧客は銀行のサイトにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="f7c9a-121">その後、認証後に Commerce のチェックアウト フローにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="f7c9a-122">このリダイレクトでは、顧客がチェックアウト フローに入力した情報 (たとえば、出荷先住所、配送オプション、ギフトカード情報、ロイヤルティ情報など) が維持されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="f7c9a-123">この機能を有効にするには、Commerce 本社の SCA 用に支払コネクタをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="f7c9a-124">詳細については、[Adyen を使用した強力な顧客認証](adyen_redirect.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f7c9a-125">Adyen 支払コネクタの場合、サイトの許可リストに Adyen URL を追加した場合にのみ、支払モジュールの iframe モジュールはレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-125">For the Adyen payment connector, the iframe module in the payment module can be rendered only if you add the Adyen URL to your site's allow list.</span></span> <span data-ttu-id="f7c9a-126">この手順を完了するには、 **\*.adyen.com** をサイトのコンテンツ セキュリティ ポリシーの **child-src** 、 **connect-src** 、 **img-src** 、 **script-src** 、 **style-src** の各ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-126">To complete this step, add **\*.adyen.com** to the **child-src** , **connect-src** , **img-src** , **script-src** , and **style-src** directives of your site's content security policy.</span></span> <span data-ttu-id="f7c9a-127">詳細については、[コンテンツ セキュリティ ポリシーの管理](manage-csp.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-127">For more information, see [Manage Content Security Policy](manage-csp.md).</span></span> 

<span data-ttu-id="f7c9a-128">次の図は、チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-128">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![チェックアウト ページのギフト カード、ロイヤルティ ポイント、支払モジュールの例](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="f7c9a-130">支払モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="f7c9a-130">Payment module properties</span></span>

| <span data-ttu-id="f7c9a-131">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="f7c9a-131">Property name</span></span> | <span data-ttu-id="f7c9a-132">値</span><span class="sxs-lookup"><span data-stu-id="f7c9a-132">Values</span></span> | <span data-ttu-id="f7c9a-133">説明</span><span class="sxs-lookup"><span data-stu-id="f7c9a-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f7c9a-134">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f7c9a-134">Heading</span></span> | <span data-ttu-id="f7c9a-135">ヘッダー テキスト</span><span class="sxs-lookup"><span data-stu-id="f7c9a-135">Heading text</span></span> | <span data-ttu-id="f7c9a-136">支払いモジュールのオプション ヘッダー。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-136">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="f7c9a-137">iframe の高さ</span><span class="sxs-lookup"><span data-stu-id="f7c9a-137">Height of the iframe</span></span> | <span data-ttu-id="f7c9a-138">ピクセル</span><span class="sxs-lookup"><span data-stu-id="f7c9a-138">Pixels</span></span> | <span data-ttu-id="f7c9a-139">ピクセル単位での iframe の高さ。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-139">The iframe height, in pixels.</span></span> <span data-ttu-id="f7c9a-140">高さは必要に応じて調整できます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-140">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="f7c9a-141">請求先住所の表示</span><span class="sxs-lookup"><span data-stu-id="f7c9a-141">Show billing address</span></span> | <span data-ttu-id="f7c9a-142">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="f7c9a-142">**True** or **False**</span></span> | <span data-ttu-id="f7c9a-143">このプロパティが **True** に設定されている場合、請求先住所は、支払モジュール iframe 内の Adyen で処理されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-143">If this property is set to **True** , the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="f7c9a-144">この値が **False** に設定されている場合は、請求先住所が Adyen によって処理されないため、Commerce ユーザーは、チェックアウト ページで請求先住所を表示するようにモジュールをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-144">If it's set to **False** , the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="f7c9a-145">支払スタイルの上書き</span><span class="sxs-lookup"><span data-stu-id="f7c9a-145">Payment style override</span></span> | <span data-ttu-id="f7c9a-146">カスケード スタイル シート (CSS) コード</span><span class="sxs-lookup"><span data-stu-id="f7c9a-146">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="f7c9a-147">支払モジュールは iframe でホストされるため、スタイル機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-147">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="f7c9a-148">このプロパティを使用すると、何らかのスタイルを実現できます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-148">You can achieve some styling by using this property.</span></span> <span data-ttu-id="f7c9a-149">サイト スタイルをオーバーライドするには、CSS コードをこのプロパティの値として貼り付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-149">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="f7c9a-150">サイト ビルダー CSS が上書きし、スタイルはこのモジュールには適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-150">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="f7c9a-151">請求先住所</span><span class="sxs-lookup"><span data-stu-id="f7c9a-151">Billing address</span></span>

<span data-ttu-id="f7c9a-152">支払モジュールを使用すると、顧客は支払情報の請求先住所を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-152">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="f7c9a-153">また、請求先住所として配送先住所を使用することもできます。この場合、チェックアウト フローをより簡単かつ迅速にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-153">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="f7c9a-154">**請求先住所の表示** プロパティが、 **False** に設定されている場合は、支払モジュールをチェックアウト ページでコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-154">If the **Show billing address** property is set to **False** , the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="f7c9a-155">チェックアウト ページに支払い モジュールを追加して、必要なプロパティを設定する</span><span class="sxs-lookup"><span data-stu-id="f7c9a-155">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="f7c9a-156">支払い モジュールは、チェックアウト モジュールにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-156">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="f7c9a-157">チェックアウト ページをコンフィギュレーションする方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7c9a-157">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7c9a-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f7c9a-158">Additional resources</span></span>

[<span data-ttu-id="f7c9a-159">買い物カゴ モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f7c9a-160">買い物カゴ アイコン モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-160">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f7c9a-161">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f7c9a-162">配送先住所モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-162">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f7c9a-163">配送オプション モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-163">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f7c9a-164">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-164">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f7c9a-165">ギフト カード モジュール</span><span class="sxs-lookup"><span data-stu-id="f7c9a-165">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="f7c9a-166">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="f7c9a-166">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="f7c9a-167">Adyen を使用した強力な顧客認証 (SCA)</span><span class="sxs-lookup"><span data-stu-id="f7c9a-167">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
