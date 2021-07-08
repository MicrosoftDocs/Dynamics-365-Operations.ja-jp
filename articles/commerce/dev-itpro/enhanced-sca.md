---
title: 店頭会計の支払を強化
description: このトピックでは、Microsoft Dynamics 365 Commerce での店舗チェックアウトの強化された強力な顧客認証 (SCA) サポートの概要を提供します。
author: rubendel
ms.date: 6/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgri
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7dc8e28879a7158282ab3f72349880e39db2aec9
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222656"
---
# <a name="enhanced-payments-in-storefront-checkout"></a><span data-ttu-id="64fd9-103">店頭会計の支払を強化</span><span class="sxs-lookup"><span data-stu-id="64fd9-103">Enhanced payments in storefront checkout</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64fd9-104">このトピックでは、Microsoft Dynamics 365 Commerce での店舗チェックアウトの強化された強力な顧客認証 (SCA) サポートの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-104">This topic provides an overview of enhanced strong customer authentication (SCA) support for storefront checkout in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="key-terms"></a><span data-ttu-id="64fd9-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="64fd9-105">Key terms</span></span>

| <span data-ttu-id="64fd9-106">相談</span><span class="sxs-lookup"><span data-stu-id="64fd9-106">Term</span></span> | <span data-ttu-id="64fd9-107">説明</span><span class="sxs-lookup"><span data-stu-id="64fd9-107">Description</span></span> |
|---|---|
| <span data-ttu-id="64fd9-108">SCA</span><span class="sxs-lookup"><span data-stu-id="64fd9-108">SCA</span></span> | <span data-ttu-id="64fd9-109">強力な顧客認証により、オンライン購入が試行されるときにカードを発行した銀行がカード所有者の ID を確認できます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-109">Strong customer authentication enables a cardholder's identity to be verified by the bank that issued the card when an online purchase is attempted.</span></span> <span data-ttu-id="64fd9-110">このプロセスは通常、店舗チェックアウト フローからカードの発行銀行によってホストされているページへのリダイレクトを介して完了します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-110">This process is typically completed via a redirect from the storefront checkout flow to a page that is hosted by the card's issuing bank.</span></span> <span data-ttu-id="64fd9-111">そこで、カード所有者の ID が確認されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-111">There, the cardholder's identity is verified.</span></span> <span data-ttu-id="64fd9-112">その後、カード所有者は店舗チェックアウト フローに戻り、チェックアウトを介して注文が続行されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-112">The cardholder is then directed back to the storefront checkout flow, where the order proceeds through checkout.</span></span> |
| <span data-ttu-id="64fd9-113">リダイレクト</span><span class="sxs-lookup"><span data-stu-id="64fd9-113">Redirect</span></span> | <span data-ttu-id="64fd9-114">オンラインの買い物客の閲覧セッションを、販売者の店舗外に移動するアクション。</span><span class="sxs-lookup"><span data-stu-id="64fd9-114">The action of moving an online shopper's browsing session out of the context of the merchant's storefront.</span></span> |
| <span data-ttu-id="64fd9-115">カードのトークン</span><span class="sxs-lookup"><span data-stu-id="64fd9-115">Card token</span></span> | <span data-ttu-id="64fd9-116">実際の支払カード番号を参照するために使用されるエイリアス。</span><span class="sxs-lookup"><span data-stu-id="64fd9-116">An alias that is used to refer to a real payment card number.</span></span> <span data-ttu-id="64fd9-117">カード トークンを使用すると、実際の支払カードへの参照を保存できます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-117">Card tokens enable a reference to an actual payment card to be saved.</span></span> <span data-ttu-id="64fd9-118">同時に、実際の支払カード番号を保存するときに発生するセキュリティ問題を防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-118">At the same time, they help prevent the security issues that can occur when real payment card numbers are saved.</span></span> |

<span data-ttu-id="64fd9-119">従来、店舗チェックアウト プロセスでは、支払プロセッサに対して 2 つの異なる呼び出しが行われました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-119">Traditionally, the storefront checkout process made two distinct calls to the payment processor.</span></span> <span data-ttu-id="64fd9-120">最初の呼び出しは、チェックアウト時に支払プロセッサの埋め込み HTML iframe 要素に入力されたカード番号をトークン化するために使用されました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-120">The first call was used to tokenize the card number that was entered in the payment processor's embedded HTML iframe element during checkout.</span></span> <span data-ttu-id="64fd9-121">呼び出し中に、SCA も有効になり、必要に応じてカード所有者をカードの発行銀行で認証できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-121">During this call, SCA was also enabled, so that the cardholder could be authenticated with the card's issuing bank as required.</span></span> <span data-ttu-id="64fd9-122">2 番目の呼び出しでは、最初の呼び出しから取得したカード トークンを使用して、実際の承認応答を要求します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-122">The second call used the card token that was obtained from the first call to request the actual authorization response.</span></span>

<span data-ttu-id="64fd9-123">支払い承認を取得するためのこの 2 回の呼び出し方法は、次の理由により、すべてのケースにおいて理想的ではありませんでした。</span><span class="sxs-lookup"><span data-stu-id="64fd9-123">This two-call method for acquiring payment authorizations wasn't ideal for all cases, for the following reasons:</span></span>

- <span data-ttu-id="64fd9-124">最初の呼び出しでは、金額ゼロの承認要求を使用して支払トークンを要求しました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-124">The first call used a zero-amount authorization request to request the payment token.</span></span> <span data-ttu-id="64fd9-125">ただし、すべての支払プロセッサが金額ゼロの承認要求をサポートしているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="64fd9-125">However, not all payment processors support zero-amount authorization requests.</span></span>
- <span data-ttu-id="64fd9-126">SCA は最初の呼び出し中に行われたため、SCA が付与した負債シフトは、実際の承認要求ではなく、トークン化要求でのみ明らかでした。</span><span class="sxs-lookup"><span data-stu-id="64fd9-126">Because SCA was done during the first call, the liability shift that SCA granted was evident only in the tokenization request, not in the actual authorization request.</span></span>

<span data-ttu-id="64fd9-127">技術的な問題と別に、従来の店舗チェックアウト プロセスは、支払処理アクティビティを確認したときに金額ゼロの要求が多数見られたため、商社に混乱を引き起こしました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-127">Aside from technical issues, the traditional storefront checkout process also caused confusion for merchants, because they saw many zero-amount requests when they reviewed payment processing activity.</span></span>

<span data-ttu-id="64fd9-128">これらの問題に対処するために、Commerce 店舗チェックアウトでの支払がリファクタリングされたので、1 回の要求のみが必要になりました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-128">To address these issues, payments in Commerce storefront checkout have been refactored so that they require only a single request.</span></span> <span data-ttu-id="64fd9-129">この 1 つの要求で、支払処理に関連するすべての必要な機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-129">This single request performs all the necessary functions that are related to payment processing:</span></span>

- <span data-ttu-id="64fd9-130">カード トークンがサポートされている場合は、承認の有効期限が切れて、フルフィルメントのために新しい承認が必要になった場合に、カード トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-130">It obtains a card token, if card tokens are supported, in case the authorization expires and a new authorization is required for fulfillment.</span></span>
- <span data-ttu-id="64fd9-131">これは、実際の承認要求中に SCA をサポートします。</span><span class="sxs-lookup"><span data-stu-id="64fd9-131">It supports SCA during the actual authorization request.</span></span> <span data-ttu-id="64fd9-132">したがって、負債シフトは、支払金額の承認で明らかになります。</span><span class="sxs-lookup"><span data-stu-id="64fd9-132">Therefore, the liability shift is evident in the authorization for the amount due.</span></span>

## <a name="key-changes-from-the-traditional-storefront-checkout-flow"></a><span data-ttu-id="64fd9-133">従来の店舗チェックアウト フローからの重要な変更</span><span class="sxs-lookup"><span data-stu-id="64fd9-133">Key changes from the traditional storefront checkout flow</span></span>

### <a name="no-order-review-step"></a><span data-ttu-id="64fd9-134">注文確認ステップなし</span><span class="sxs-lookup"><span data-stu-id="64fd9-134">No order review step</span></span>

<span data-ttu-id="64fd9-135">支払フローが開始された後は、注文を確認して送信する手順はありません。</span><span class="sxs-lookup"><span data-stu-id="64fd9-135">After the payments flow is initiated, there is no step to review and submit the order.</span></span> <span data-ttu-id="64fd9-136">支払詳細を入力した後、顧客は **注文** オプションのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-136">After payment details are entered, customers have only the **Place order** option.</span></span> <span data-ttu-id="64fd9-137">指定した支払方法で SCA が必要な場合、顧客は銀行の認証ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-137">If the payment method that was provided requires SCA, customers are redirected to the bank's authentication page.</span></span> <span data-ttu-id="64fd9-138">認証が完了すると、顧客はチェックアウト ページに戻り、注文が処理されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-138">After authentication is completed, customers are directed back to the checkout page, and the order is processed.</span></span>

<span data-ttu-id="64fd9-139">説明したフローは、既定でリダイレクトされる支払方法 (PayPalなど) にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-139">The flow that was just described also applies to payment methods that redirect by default, such as PayPal.</span></span> <span data-ttu-id="64fd9-140">支払いの詳細が PayPal に提供された後、チェックアウト ページに戻って注文が開始されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-140">After payment details are provided to PayPal, the redirect back to the checkout page initiates order placement.</span></span>

<span data-ttu-id="64fd9-141">従来のフローでは、埋め込み iFrame 要素に支払詳細を入力すると、**保存して続行** ボタンが使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-141">In the traditional flow, after the payment details were entered in the embedded iframe element, a **Save and continue** button became available.</span></span> <span data-ttu-id="64fd9-142">顧客がこのボタンを選択すると、トークン化された支払がチェックアウトに追加されました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-142">When the customer selected this button, the tokenized payment was added to the checkout.</span></span> <span data-ttu-id="64fd9-143">デモ環境では、顧客の電子メール アドレスを収集するか、顧客に使用条件に同意してもらう手順もあります。</span><span class="sxs-lookup"><span data-stu-id="64fd9-143">In demonstration environments, there could also be a step that either collected the customer's email address or had the customer agree to terms of use.</span></span> <span data-ttu-id="64fd9-144">新しいフローでは、顧客が最後の **保存して続行** ボタンを選択したときに以前に行われていた検証が、顧客が **注文** ボタンを選択したときに行われるようになりました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-144">In the new flow, the validation that was previously done when the customer selected the final **Save and continue** button is now done when the customer selects the **Place order** button.</span></span> <span data-ttu-id="64fd9-145">したがって、顧客側で必要なクリックが 1 回少なくなり、ページの読み込みがチェックアウト フローから削除されます。</span><span class="sxs-lookup"><span data-stu-id="64fd9-145">Therefore, one fewer click is required on the customer's part, and a page load is eliminated from the checkout flow.</span></span>

## <a name="payment-connector-support"></a><span data-ttu-id="64fd9-146">支払コネクタ サポート</span><span class="sxs-lookup"><span data-stu-id="64fd9-146">Payment connector support</span></span>

<span data-ttu-id="64fd9-147">既定では、Adyen と PayPal の既成の支払コネクタは、チェックアウト時の強化された支払フローをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="64fd9-147">By default, the out-of-box payment connectors for Adyen and PayPal support the enhanced payment flows during checkout.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="64fd9-148">Adyen コネクタ バージョン **V002** のみが、拡張 SCA をサポートします。</span><span class="sxs-lookup"><span data-stu-id="64fd9-148">Only Adyen connector version **V002** truly supports enhanced SCA.</span></span> <span data-ttu-id="64fd9-149">バージョン **V001** は、チェックアウトが拡張 SCA 用に構成されている場合でも機能します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-149">Version **V001** still works when the checkout is configured for enhanced SCA.</span></span> <span data-ttu-id="64fd9-150">ただし、バックグラウンドでは、そのバージョンはまだ 2 つの呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="64fd9-150">However, behind the scenes, that version still makes two calls.</span></span>
> - <span data-ttu-id="64fd9-151">2021 年 1 月 1 日に欧州連合 (EU) で施行された SCA 要件のため、Adyen コネクタのバージョン **V001** は使用しなくまりました。</span><span class="sxs-lookup"><span data-stu-id="64fd9-151">Because of SCA requirements that went into effect in the European Union (EU) on January 1, 2021, version **V001** of the Adyen connector should no longer be used.</span></span> <span data-ttu-id="64fd9-152">バージョン **V002** を使用するために Adyen コネクタを構成する方法については、[新しいクレジット カード用のプロセッサの設定](adyen-connector.md?tabs=8-1-3#set-up-a-processor-for-new-credit-cards) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64fd9-152">For information about how to configure the Adyen connector to use version **V002**, see [Set up a processor for new credit cards](adyen-connector.md?tabs=8-1-3#set-up-a-processor-for-new-credit-cards).</span></span>

## <a name="enable-enhanced-payments-in-storefront-checkout-in-commerce-site-builder"></a><span data-ttu-id="64fd9-153">Commerce サイト ビルダーでの店舗チェックアウトでの拡張支払の有効化</span><span class="sxs-lookup"><span data-stu-id="64fd9-153">Enable enhanced payments in storefront checkout in Commerce site builder</span></span>

<span data-ttu-id="64fd9-154">Commerce サイト ビルダーで強化された支払機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="64fd9-154">To enable the enhanced payments feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="64fd9-155">編集するサイトで、**サイトの設定** を展開します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-155">In the site that you want to edit, expand **Site settings**.</span></span>
2. <span data-ttu-id="64fd9-156">**拡張子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-156">Select **Extensions**.</span></span>
3. <span data-ttu-id="64fd9-157">**カートとチェックアウト** まで下にスクロールし、**単一の支払承認チェックアウトを有効にする** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="64fd9-157">Scroll down to **Cart and checkout**, and select the **Enable single payment authorization checkout** checkbox.</span></span>
4. <span data-ttu-id="64fd9-158">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="64fd9-158">Select **Save and publish**.</span></span>

![Commerce サイト ビルダーでの店舗チェックアウトでの拡張支払の有効化](media/rfac.png)

## <a name="additional-resources"></a><span data-ttu-id="64fd9-160">追加リソース</span><span class="sxs-lookup"><span data-stu-id="64fd9-160">Additional resources</span></span>

[<span data-ttu-id="64fd9-161">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="64fd9-161">Payments FAQ</span></span>](payments-retail.md)

[<span data-ttu-id="64fd9-162">PayPal 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="64fd9-162">Dynamics 365 Payment Connector for PayPal</span></span>](../paypal.md)

[<span data-ttu-id="64fd9-163">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="64fd9-163">Dynamics 365 Payment Connector for Adyen</span></span>](adyen-connector.md)

[<span data-ttu-id="64fd9-164">Adyen リダイレクト</span><span class="sxs-lookup"><span data-stu-id="64fd9-164">Adyen redirect</span></span>](../adyen_redirect.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
