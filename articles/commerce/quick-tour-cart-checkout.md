---
title: 買い物カゴと清算ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の買い物カゴとチェックアウト ページの概要を示します。
author: anupamar-ms
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c879b90cf49dcab9cf069e4f3613602bd6673aa9
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527567"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="444d6-103">買い物カゴと清算ページの概要</span><span class="sxs-lookup"><span data-stu-id="444d6-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="444d6-104">このトピックでは、Microsoft Dynamics 365 Commerce の買い物カゴとチェックアウト ページの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="444d6-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="444d6-105">概要</span><span class="sxs-lookup"><span data-stu-id="444d6-105">Overview</span></span>

<span data-ttu-id="444d6-106">E コマース Web サイトの買い物カゴのページには、顧客が買い物カゴに追加したすべての品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="444d6-107">買い物カゴのページは、買い物カゴ モジュールを使用して構築されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="444d6-108">カート モジュールは、カートにある品目を紹介するのに必要なすべてのモジュールをホストするコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="444d6-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="444d6-109">また、買い物カゴ モジュールは他のモジュールを使用して、注文集計および顧客注文に適用されたプロモーション コードも表示します。</span><span class="sxs-lookup"><span data-stu-id="444d6-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="444d6-110">E コマース Web サイトのチェックアウト ページには、顧客が注文を行うために必要な情報すべてを入力するための、ステップバイステップのフローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="444d6-111">チェックアウト モジュールには、出荷先住所、出荷方法、請求情報、注文集計、および顧客の注文に関連するその他の情報を処理するモジュールを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="444d6-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="444d6-112">買い物カゴのページ</span><span class="sxs-lookup"><span data-stu-id="444d6-112">Cart page</span></span>

<span data-ttu-id="444d6-113">買い物カゴのページはショッピング バッグとして機能し、買い物カゴに追加されたすべての品目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="444d6-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="444d6-114">以下の図は、オンライン スタート キットおよび「Fabrikam」のテーマを使用してビルドされた買い物カゴのページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="444d6-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![買い物カゴのページの例](./media/cart2.PNG)

<span data-ttu-id="444d6-116">買い物カゴ ページの本文には、顧客が買い物カゴに追加したすべての品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="444d6-117">適用できる割引すべてが表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="444d6-118">これらの割引には、複雑な割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="444d6-118">These discounts include complex discounts.</span></span> <span data-ttu-id="444d6-119">例には、「3 つの品目を購入し、10% の割引」 または「ボトル 1 本とリュックサックを購入し、10% の割引」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="444d6-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="444d6-120">注文集計モジュールは、割引、出荷、税などが適用された後の金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="444d6-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="444d6-121">また、プロモーション コード モジュールにより、プロモーション コードの適用または削除ができます。</span><span class="sxs-lookup"><span data-stu-id="444d6-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="444d6-122">顧客は匿名またはサインインしたユーザーとして購入できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="444d6-123">顧客がサインインしている場合は、買い物カゴ内の品目はセッションの間は保存されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="444d6-124">このようにして、顧客は複数のデバイスから継続して買い物をすることができます。</span><span class="sxs-lookup"><span data-stu-id="444d6-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="444d6-125">買い物カゴから、顧客はチェックアウトに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="444d6-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="444d6-126">顧客は、ゲスト ユーザーまたはサインインしたユーザーとしてチェックアウトを開始できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="444d6-127">買い物カゴ ページを作成する方法の詳細については、[ページへの買い物カゴ モジュールの追加](add-cart-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="444d6-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="444d6-128">チェックアウト ページ</span><span class="sxs-lookup"><span data-stu-id="444d6-128">Checkout page</span></span>

<span data-ttu-id="444d6-129">チェックアウト ページで、顧客は注文を行うために必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="444d6-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="444d6-130">以下の図は、オンライン スタート キットを使用してビルドされたチェックアウト ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="444d6-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![チェックアウト ページの例](./media/Checkout.PNG)

<span data-ttu-id="444d6-132">チェックアウト ページの本文では、すべての注文情報が収集されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="444d6-133">この情報には、出荷先住所、出荷オプション、および支払情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="444d6-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="444d6-134">処理する特定の注文に情報を入力する必要があるため、チェックアウトにはステップバイステップ フローがあります。</span><span class="sxs-lookup"><span data-stu-id="444d6-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="444d6-135">たとえば、出荷コストを計算して支払を承認できるようにするために、出荷先住所を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="444d6-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="444d6-136">出荷先住所</span><span class="sxs-lookup"><span data-stu-id="444d6-136">Shipping address</span></span>

<span data-ttu-id="444d6-137">品目を出荷する必要がある場合、出荷先住所を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="444d6-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="444d6-138">各ロケールの出荷先住所の形式は、Dynamics 365 Commerce でコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="444d6-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="444d6-139">たとえば、品目が米国に出荷される場合、出荷先住所には番地、都道府県、および郵便番号が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="444d6-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="444d6-140">英数字の検証、最大の長さ、および数字に対する検証など、基本的な入力検証が、出荷先住所フィールドに対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="444d6-141">アドレス自体の有効性は検証されませんが、この検証はカスタマイズされたサード パーティ サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="444d6-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="444d6-142">出荷先住所は、「出荷」オプションが選択されている買い物カゴ内のすべての品目に対して適用されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="444d6-143">オンライン スタート キットで提供されているチェックアウト フローを使用する場合、買い物カゴの個別の品目を異なる住所に出荷することはできません。</span><span class="sxs-lookup"><span data-stu-id="444d6-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="444d6-144">この機能が必要な場合、チェックアウト モジュールをカスタマイズすることによって実装できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="444d6-145">出荷先住所が指定された後、Dynamics 365 Commerce オンライン ストアから使用可能な出荷方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="444d6-146">出荷方法およびサポートされる住所は、コマースでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="444d6-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="444d6-147">支払</span><span class="sxs-lookup"><span data-stu-id="444d6-147">Payment</span></span>

<span data-ttu-id="444d6-148">チェックアウト フローの次のステップは支払です。</span><span class="sxs-lookup"><span data-stu-id="444d6-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="444d6-149">E コマースでは、クレジット カード、ギフト カード、およびロイヤルティ ポイントなど、注文のために複数の支払方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="444d6-150">これらの支払方法を組み合わせて使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="444d6-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="444d6-151">使用する支払方法によって、追加情報が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="444d6-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="444d6-152">たとえば、クレジット カード支払には請求先住所が必要です。</span><span class="sxs-lookup"><span data-stu-id="444d6-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="444d6-153">クレジット カード支払は、Adyen 支払コネクタを使用して処理されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="444d6-154">ロイヤルティ ポイント</span><span class="sxs-lookup"><span data-stu-id="444d6-154">Loyalty points</span></span>

<span data-ttu-id="444d6-155">チェックアウト フロー中、ロイヤルティ プログラムのメンバーである顧客および未収のロイヤルティ ポイントがある顧客は、注文に対してロイヤルティ ポイントを引き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="444d6-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="444d6-156">顧客に既存のロイヤルティ メンバーシップがある場合のみ、ロイヤルティ ポイント モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="444d6-157">メンバー以外およびゲスト ユーザーの場合、このモジュールは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="444d6-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="444d6-158">ギフト カード</span><span class="sxs-lookup"><span data-stu-id="444d6-158">Gift cards</span></span>

<span data-ttu-id="444d6-159">オンライン スタート キットにより、注文に対して内部ギフトカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="444d6-160">内部ギフト カードを適用するには、顧客はサインインしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="444d6-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="444d6-161">追加のセキュリティのために、内部ギフト カードの ID 番号 (PIN) を使用してフローをカスタマイズすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="444d6-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="444d6-162">サインインおよびゲスト ユーザー</span><span class="sxs-lookup"><span data-stu-id="444d6-162">Signed-in and guest users</span></span>

<span data-ttu-id="444d6-163">顧客は、ゲスト ユーザーまたはサインインしたユーザーとしてチェックアウト プロセスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="444d6-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="444d6-164">顧客がサインインしている場合、保存されている出荷先住所および保存されているクレジット カードの詳細などのアカウント情報が自動的に取得されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="444d6-165">注文集計</span><span class="sxs-lookup"><span data-stu-id="444d6-165">Order summary</span></span>

<span data-ttu-id="444d6-166">チェックアウトには、顧客が注文を行う前に検証できるように、買い物カゴ内の品目の集計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="444d6-167">チェックアウト フロー中は、明細行品目を編集できません。</span><span class="sxs-lookup"><span data-stu-id="444d6-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="444d6-168">ただし、ユーザーが戻って明細行品目を編集したい場合のために買い物カゴへのリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="444d6-169">顧客が出荷および請求書作成情報を提供した後、注文集計には、ロイヤルティ ポイント、ギフト カード、および他の支払が適用された後の金額が反映されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="444d6-170">注文確認および電子メール</span><span class="sxs-lookup"><span data-stu-id="444d6-170">Order confirmation and email</span></span>

<span data-ttu-id="444d6-171">顧客が注文を行う時、確認番号が提供されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="444d6-172">この時点で、支払は承認されていますが、請求されていません。</span><span class="sxs-lookup"><span data-stu-id="444d6-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="444d6-173">支払は、注文が履行される時にのみ請求されます (つまり、出荷時または受取り時)。</span><span class="sxs-lookup"><span data-stu-id="444d6-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="444d6-174">注文が作成された後、注文確認電子メールが顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="444d6-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="444d6-175">チェックアウト ページを作成する方法の詳細については、[ページへのチェックアウト モジュールの追加](add-checkout-module.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="444d6-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="444d6-176">追加リソース</span><span class="sxs-lookup"><span data-stu-id="444d6-176">Additional resources</span></span>

[<span data-ttu-id="444d6-177">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="444d6-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="444d6-178">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="444d6-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="444d6-179">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="444d6-179">Account management pages overview</span></span>](quick-tour-account-management.md)
