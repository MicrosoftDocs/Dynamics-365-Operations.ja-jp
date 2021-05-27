---
title: 買い物カゴと清算ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の買い物カゴとチェックアウト ページの概要を示します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a574494784e9a534307cceff584e047d870dc401
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027942"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="ffdf0-103">買い物カゴとチェック アウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="ffdf0-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffdf0-104">このトピックでは、Microsoft Dynamics 365 Commerce の買い物カゴとチェックアウト ページの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ffdf0-105">E コマース Web サイトの買い物カゴのページには、顧客が買い物カゴに追加したすべての品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-105">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="ffdf0-106">買い物カゴのページは、買い物カゴ モジュールを使用して構築されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-106">The cart page is built by using the cart module.</span></span> <span data-ttu-id="ffdf0-107">カート モジュールは、カートにある品目を紹介するのに必要なすべてのモジュールをホストするコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-107">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="ffdf0-108">また、買い物カゴ モジュールは他のモジュールを使用して、注文集計および顧客注文に適用されたプロモーション コードも表示します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-108">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="ffdf0-109">E コマース Web サイトのチェックアウト ページには、顧客が注文を行うために必要な情報すべてを入力するための、ステップバイステップのフローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-109">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="ffdf0-110">チェックアウト モジュールには、出荷先住所、出荷方法、請求情報、注文集計、および顧客の注文に関連するその他の情報を処理するモジュールを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-110">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="ffdf0-111">買い物カゴのページ</span><span class="sxs-lookup"><span data-stu-id="ffdf0-111">Cart page</span></span>

<span data-ttu-id="ffdf0-112">買い物カゴのページはショッピング バッグとして機能し、買い物カゴに追加されたすべての品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-112">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="ffdf0-113">以下の図は、モジュール ライブラリおよび 「Fabrikam」 のテーマを使用してビルドされた買い物カゴのページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-113">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![買い物カゴのページの例](./media/cart2.PNG)

<span data-ttu-id="ffdf0-115">買い物カゴ ページの本文には、顧客が買い物カゴに追加したすべての品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-115">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="ffdf0-116">適用できる割引すべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-116">All applicable discounts are showcased.</span></span> <span data-ttu-id="ffdf0-117">これらの割引には、複雑な割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-117">These discounts include complex discounts.</span></span> <span data-ttu-id="ffdf0-118">例には、「3 つの品目を購入し、10% の割引」 または「ボトル 1 本とリュックサックを購入し、10% の割引」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-118">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="ffdf0-119">注文集計モジュールは、割引、出荷、税などが適用された後の金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-119">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="ffdf0-120">また、プロモーション コード モジュールにより、プロモーション コードの適用または削除ができます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-120">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ffdf0-121">顧客は匿名またはサインインしたユーザーとして購入できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-121">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="ffdf0-122">顧客がサインインしている場合は、買い物カゴ内の品目はセッションの間は保存されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-122">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="ffdf0-123">このようにして、顧客は複数のデバイスから継続して買い物をすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-123">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="ffdf0-124">買い物カゴから、顧客はチェックアウトに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-124">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="ffdf0-125">顧客は、ゲスト ユーザーまたはサインインしたユーザーとしてチェックアウトを開始できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-125">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="ffdf0-126">買い物カゴ ページを作成する方法の詳細については、[ページへの買い物カゴ モジュールの追加](add-cart-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-126">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="ffdf0-127">チェックアウト ページ</span><span class="sxs-lookup"><span data-stu-id="ffdf0-127">Checkout page</span></span>

<span data-ttu-id="ffdf0-128">チェックアウト ページで、顧客は注文を行うために必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-128">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="ffdf0-129">以下の図は、モジュール ライブラリを使用してビルドされたチェックアウト ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-129">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![チェックアウト ページの例](./media/Checkout.PNG)

<span data-ttu-id="ffdf0-131">チェックアウト ページの本文では、すべての注文情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-131">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="ffdf0-132">この情報には、出荷先住所、出荷オプション、および支払情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-132">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="ffdf0-133">処理する特定の注文に情報を入力する必要があるため、チェックアウトにはステップバイステップ フローがあります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-133">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="ffdf0-134">たとえば、出荷コストを計算して支払を承認できるようにするために、出荷先住所を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-134">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="ffdf0-135">出荷先住所</span><span class="sxs-lookup"><span data-stu-id="ffdf0-135">Shipping address</span></span>

<span data-ttu-id="ffdf0-136">品目を出荷する必要がある場合、出荷先住所を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-136">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="ffdf0-137">各ロケールの出荷先住所の形式は、Dynamics 365 Commerce でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-137">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ffdf0-138">たとえば、品目が米国に出荷される場合、出荷先住所には番地、都道府県、および郵便番号が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-138">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="ffdf0-139">英数字の検証、最大の長さ、および数字に対する検証など、基本的な入力検証が、出荷先住所フィールドに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-139">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="ffdf0-140">アドレス自体の有効性は検証されませんが、この検証はカスタマイズされたサード パーティ サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-140">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="ffdf0-141">出荷先住所は、「出荷」オプションが選択されている買い物カゴ内のすべての品目に対して適用されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-141">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="ffdf0-142">モジュール ライブラリで提供されているチェックアウト フローを使用する場合、買い物カゴの個別の品目を異なる住所に出荷することはできません。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-142">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="ffdf0-143">この機能が必要な場合、チェックアウト モジュールをカスタマイズすることによって実装できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-143">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="ffdf0-144">出荷先住所が指定された後、Dynamics 365 Commerce オンライン ストアから使用可能な出荷方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-144">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="ffdf0-145">出荷方法およびサポートされる住所は、コマースでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-145">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="ffdf0-146">支払</span><span class="sxs-lookup"><span data-stu-id="ffdf0-146">Payment</span></span>

<span data-ttu-id="ffdf0-147">チェックアウト フローの次のステップは支払です。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-147">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="ffdf0-148">E コマースでは、クレジット カード、ギフト カード、およびロイヤルティ ポイントなど、注文のために複数の支払方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-148">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="ffdf0-149">これらの支払方法を組み合わせて使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-149">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="ffdf0-150">使用する支払方法によって、追加情報が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-150">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="ffdf0-151">たとえば、クレジット カード支払には請求先住所が必要です。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-151">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="ffdf0-152">クレジット カード支払は、Adyen 支払コネクタを使用して処理されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-152">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="ffdf0-153">ロイヤルティ ポイント</span><span class="sxs-lookup"><span data-stu-id="ffdf0-153">Loyalty points</span></span>

<span data-ttu-id="ffdf0-154">チェックアウト フロー中、ロイヤルティ プログラムのメンバーである顧客および未収のロイヤルティ ポイントがある顧客は、注文に対してロイヤルティ ポイントを引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-154">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="ffdf0-155">顧客に既存のロイヤルティ メンバーシップがある場合のみ、ロイヤルティ ポイント モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-155">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="ffdf0-156">メンバー以外およびゲスト ユーザーの場合、このモジュールは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-156">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="ffdf0-157">ギフト カード</span><span class="sxs-lookup"><span data-stu-id="ffdf0-157">Gift cards</span></span>

<span data-ttu-id="ffdf0-158">モジュール ライブラリにより、注文に対して内部ギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-158">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="ffdf0-159">内部ギフト カードを適用するには、顧客はサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-159">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="ffdf0-160">追加のセキュリティのために、内部ギフト カードの ID 番号 (PIN) を使用してフローをカスタマイズすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-160">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="ffdf0-161">サインインおよびゲスト ユーザー</span><span class="sxs-lookup"><span data-stu-id="ffdf0-161">Signed-in and guest users</span></span>

<span data-ttu-id="ffdf0-162">顧客は、ゲスト ユーザーまたはサインインしたユーザーとしてチェックアウト プロセスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-162">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="ffdf0-163">顧客がサインインしている場合、保存されている出荷先住所および保存されているクレジット カードの詳細などのアカウント情報が自動的に取得されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-163">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="ffdf0-164">注文集計</span><span class="sxs-lookup"><span data-stu-id="ffdf0-164">Order summary</span></span>

<span data-ttu-id="ffdf0-165">チェックアウトには、注文を行う前に検証できるように、買い物カゴ内の品目の集計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-165">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before placing the order.</span></span> <span data-ttu-id="ffdf0-166">チェックアウト フロー中は、明細行品目を編集できません。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-166">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="ffdf0-167">ただし、ユーザーが戻って明細行品目を編集したい場合のために買い物カゴへのリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-167">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="ffdf0-168">顧客が出荷および請求書作成情報を提供した後、注文集計には、ロイヤルティ ポイント、ギフト カード、および他の支払が適用された後の金額が反映されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-168">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="ffdf0-169">注文確認および電子メール</span><span class="sxs-lookup"><span data-stu-id="ffdf0-169">Order confirmation and email</span></span>

<span data-ttu-id="ffdf0-170">顧客が注文を行う時、確認番号が提供されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-170">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="ffdf0-171">この時点で、支払は承認されていますが、請求されていません。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-171">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="ffdf0-172">支払は、注文が履行される時にのみ請求されます (つまり、出荷時または受取り時)。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-172">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="ffdf0-173">注文が作成された後、注文確認電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-173">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="ffdf0-174">チェックアウト ページを作成する方法の詳細については、[ページへのチェックアウト モジュールの追加](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffdf0-174">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffdf0-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ffdf0-175">Additional resources</span></span>

[<span data-ttu-id="ffdf0-176">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="ffdf0-176">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="ffdf0-177">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="ffdf0-177">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="ffdf0-178">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="ffdf0-178">Account management pages overview</span></span>](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
