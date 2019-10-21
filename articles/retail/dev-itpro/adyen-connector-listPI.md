---
title: Adyen コネクタでオンライン支払手段を保存する
description: このトピックでは、電子商取引の Adyen コネクタを使用して支払手段を保存する方法を説明します。
author: rubendel
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49fe8dc579faa4611b5e1db8a54992f578ef5127
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550498"
---
# <a name="saving-online-payment-instruments-with-the-adyen-connector"></a><span data-ttu-id="cb30a-103">オンライン支払手段を Adyen コネクタで保存</span><span class="sxs-lookup"><span data-stu-id="cb30a-103">Saving online payment instruments with the Adyen connector</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb30a-104">このトピックでは、Dynamics 電子商取引プラットフォームで Adyen の "カードが存在しない" 支払コネクタを使用している場合に、支払手段の保存に関連する設定と機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-104">This topic describes the setup and functionality that are related to saving payment instruments when you use the Adyen "card not present" payment connector for the Dynmics e-Commerce platform.</span></span> 

## <a name="key-terms"></a><span data-ttu-id="cb30a-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="cb30a-105">Key terms</span></span>

| <span data-ttu-id="cb30a-106">相談</span><span class="sxs-lookup"><span data-stu-id="cb30a-106">Term</span></span> | <span data-ttu-id="cb30a-107">説明</span><span class="sxs-lookup"><span data-stu-id="cb30a-107">Description</span></span> |
|---|---|
| <span data-ttu-id="cb30a-108">トークン</span><span class="sxs-lookup"><span data-stu-id="cb30a-108">Token</span></span> | <span data-ttu-id="cb30a-109">支払プロセッサが参照として提供する一連のデータ。</span><span class="sxs-lookup"><span data-stu-id="cb30a-109">A string of data that a payment processor provides as a reference.</span></span> <span data-ttu-id="cb30a-110">トークンは、支払カード番号、支払認証、前回の支払キャプチャを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-110">Tokens can represent payment card numbers, payment authorizations, and previous payment captures.</span></span> <span data-ttu-id="cb30a-111">トークンは、販売時点管理 (POS) システムの外で機密データを保持するのに役立つため重要です。</span><span class="sxs-lookup"><span data-stu-id="cb30a-111">Tokens are important because they help keep sensitive data out of the point of sale (POS) system.</span></span> |
| <span data-ttu-id="cb30a-112">カードのトークン</span><span class="sxs-lookup"><span data-stu-id="cb30a-112">Card token</span></span> | <span data-ttu-id="cb30a-113">POS システムのストレージに対して支払プロセッサが提供するトークン。</span><span class="sxs-lookup"><span data-stu-id="cb30a-113">A token that a payment processor provides for storage in the POS system.</span></span> <span data-ttu-id="cb30a-114">カードのトークン (またはカードの参照) は、それを受け取る販売者のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-114">The card token, or card reference, can be used only by the merchant who receives it</span></span> |
| <span data-ttu-id="cb30a-115">承認 (認証) トークン</span><span class="sxs-lookup"><span data-stu-id="cb30a-115">Authorization (Auth) token</span></span> | <span data-ttu-id="cb30a-116">POS システムが支払プロセッサに承認要求をした後、支払プロセッサはその要求に対する応答の一部として POS システムに固有の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-116">After a POS system makes an authorization request to a payment processor, the payment processor provides a unique ID to the POS system as part of the response to that request.</span></span> <span data-ttu-id="cb30a-117">承認を取り消したり無効にしたりするなどのアクションを実行するためにプロセッサが呼び出されたときに、この承認トークンや承認参照を後で使用できます</span><span class="sxs-lookup"><span data-stu-id="cb30a-117">This authorization token, or authorization reference, can be used later, when the processor is called to perform actions such as reversing or voiding the authorization.</span></span> <span data-ttu-id="cb30a-118">ただし、承認トークンは、注文が履行されたとき、またはトランザクションが確定したときに、資金を取得するために最もよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-118">However, an authorization token is most often used to capture funds when an order is fulfilled or when a transaction is being finalized.</span></span> |
| <span data-ttu-id="cb30a-119">リスト PI</span><span class="sxs-lookup"><span data-stu-id="cb30a-119">List PI</span></span> | <span data-ttu-id="cb30a-120">このトピックで説明されている機能に対して頻繁に使用される一般名。</span><span class="sxs-lookup"><span data-stu-id="cb30a-120">A frequently used generic name for the capability that is described in this topic.</span></span> <span data-ttu-id="cb30a-121">リスト PI は、同じ電子商取引 Web サイトを通じて行われる将来のチェックアウト中に、支払手段を保存し、以前に使用された支払手段を一覧にする機能を意味します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-121">List PI refers to the ability to save payment instruments and to list previously used payment instruments during future checkouts that are done through the same e-commerce website.</span></span> |
| <span data-ttu-id="cb30a-122">名前付きユーザー</span><span class="sxs-lookup"><span data-stu-id="cb30a-122">Named user</span></span> | <span data-ttu-id="cb30a-123">チェックアウト時にオンライン ストアフロントにログインしている電子商取引の顧客。</span><span class="sxs-lookup"><span data-stu-id="cb30a-123">An e-commerce customer who is signed in to the online storefront at the time of checkout.</span></span> <span data-ttu-id="cb30a-124">名前付きユーザーは一意の顧客 ID を持ち、オンライン ストアフロントにログインするたびにそのオンライン購入が常に同じ顧客 ID にマップされます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-124">Named users have a unique customer ID, and their online purchases are always mapped to the same customer ID whenever they are signed in to the online storefront.</span></span> |

## <a name="overview"></a><span data-ttu-id="cb30a-125">概要</span><span class="sxs-lookup"><span data-stu-id="cb30a-125">Overview</span></span>

<span data-ttu-id="cb30a-126">電子商取引の注文を作成する場合、小売企業は将来のトランザクションで使用できるように顧客の支払カード情報を保存するよう促すことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="cb30a-126">When e-commerce orders are created, retailers often offer to save the customer's payment card information so that it can be used for future transactions.</span></span> <span data-ttu-id="cb30a-127">このトピックでは、この機能 ("リストPI") が Adyen の Microsoft Dynamics 365 支払コネクタを通じて配送される方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-127">This topic explains how that capability ("List PI") is delivered through the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="cb30a-128">Adyen 支払コネクタはこの機能をそのままではサポートしておらず、サード パーティの支払コネクタについてはカスタマイズが必要です。</span><span class="sxs-lookup"><span data-stu-id="cb30a-128">Although the Adyen payment connector supports this capability out of the box, third-party payment connectors require customization.</span></span> <span data-ttu-id="cb30a-129">また、すべての支払プロセッサが同じ方法で支払カード情報の保存をサポートしているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="cb30a-129">Additionally, not all payment processors might support the same method of saving payment card information.</span></span> 

<span data-ttu-id="cb30a-130">リスト PI 機能の初期状態の実装では、支払プロセッサを使用して、その支払コネクタで既に処理された支払手段に対して、オンライン顧客の一意な ID のマッピングを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb30a-130">The out-of-box implementation of the List PI capability relies on the payment processor to keep a mapping of an online customer's unique ID to the payment instruments that have previously been processed through that payment connector.</span></span> <span data-ttu-id="cb30a-131">名前付きユーザーとして Web サイトにログインしている顧客のみに、支払カード情報を次回のオンライン訪問のために保存するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="cb30a-131">Only customers who are signed in to the website as named users have the option to save their payment card information for their next online visit.</span></span> <span data-ttu-id="cb30a-132">"ゲスト チェックアウト" オプションを使用してオンライン注文を作成する顧客は、将来のトランザクションに対して支払カードの情報を保存できません。</span><span class="sxs-lookup"><span data-stu-id="cb30a-132">Customers who use a "guest checkout" option when they create an online order won't be able to save payment card information for future transactions.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cb30a-133">必要条件</span><span class="sxs-lookup"><span data-stu-id="cb30a-133">Prerequisites</span></span>

<span data-ttu-id="cb30a-134">リスト PI 機能には次の要素が必要です:</span><span class="sxs-lookup"><span data-stu-id="cb30a-134">The List PI capability requires the following elements:</span></span>

- <span data-ttu-id="cb30a-135">電子商取引と Microsoft Dynamics 365 Retail の統合</span><span class="sxs-lookup"><span data-stu-id="cb30a-135">An e-commerce integration with Microsoft Dynamics 365 Retail</span></span>
- <span data-ttu-id="cb30a-136">リスト PI 機能と互換性のある支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="cb30a-136">A payment connector that is compatible with the List PI capability</span></span>
- <span data-ttu-id="cb30a-137">顧客がその支払プロセッサに保存させたい支払手段に一意の顧客 ID をマッピングする支払プロセッサ</span><span class="sxs-lookup"><span data-stu-id="cb30a-137">A payment processor that maps unique customer IDs to the payment instruments that the customers want that payment processor to save</span></span>

<span data-ttu-id="cb30a-138">一般的な支払コネクタと小売ソフトウェア開発キット (SDK) の実装方法の詳細については、[IT プロおよび開発者向けの小売ホーム ページ](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="cb30a-138">For more information about how to implement payment connectors and the Retail software development kit (SDK) in general, visit the [Retail for IT pros and developers home page](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors).</span></span>

## <a name="setup"></a><span data-ttu-id="cb30a-139">セットアップ</span><span class="sxs-lookup"><span data-stu-id="cb30a-139">Setup</span></span>

<span data-ttu-id="cb30a-140">リスト PI 機能には次のコンポーネントと設定手順が必要です:</span><span class="sxs-lookup"><span data-stu-id="cb30a-140">The List PI capability requires the following components and setup steps:</span></span>

- <span data-ttu-id="cb30a-141">**電子商取引の統合** – オンライン ストアフロントと小売の統合が必要です。</span><span class="sxs-lookup"><span data-stu-id="cb30a-141">**E-commerce integration** – An online storefront integration with Retail is required.</span></span> <span data-ttu-id="cb30a-142">小売の電子商取引 SDK の詳細は [電子商取引プラットフォーム ソフトウェア開発キット (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb30a-142">For more information about the Retail e-Commerce SDK, see [e-Commerce platform software development kit (SDK)](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk).</span></span>
- <span data-ttu-id="cb30a-143">**オンライン支払コンフィギュレーション** – Adyen の Dynamics 365 支払コネクタは、そのままでリスト PI をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cb30a-143">**Online payments configuration** – The Dynamics 365 Payment Connector for Adyen supports List PI out of the box.</span></span> <span data-ttu-id="cb30a-144">オンライン ストアの支払いを構成する方法については [Adyen の Dynamics 365 支払コネクタ](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb30a-144">For information about how to configure payments for online stores, see [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce).</span></span> 

    <span data-ttu-id="cb30a-145">このトピックで説明されている電子商取引の設定手順を完了することに加えて、**オンライン ストア** フォームの支払口座クイック タブの **電子商取引で支払情報の保存を許可する** オプションを **はい** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb30a-145">In addition to completing the ecommerce setup steps that are described in that topic, you must set the **Allow saving payment information in e-commerce** option in the Payment accounts fasttab of the **Online store** form to **Yes**.</span></span> 

- <span data-ttu-id="cb30a-146">**オムニ チャネルの支払コンフィギュレーション** – バック オフィスで **小売 \> 本社の設定 \> パラメーター \> 小売共有パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-146">**Omni-channel payments configuration** – In the back office, go to **Retail \> Headquarters setup \> Parameters \> Retail shared parameters**.</span></span> <span data-ttu-id="cb30a-147">次に **オムニ チャネルの支払** タブで **オムニ チャネルの支払を使用する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-147">Then, on the **Omni-channel payments** tab, set the **Use omni-channel payments** option to **Yes**.</span></span> 

## <a name="functional-experience"></a><span data-ttu-id="cb30a-148">機能のエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="cb30a-148">Functional experience</span></span>

### <a name="guest-checkout"></a><span data-ttu-id="cb30a-149">ゲスト チェックアウト</span><span class="sxs-lookup"><span data-stu-id="cb30a-149">Guest checkout</span></span>

<span data-ttu-id="cb30a-150">電子商取引の訪問者がゲストとしてチェックアウトを選択した場合、チェックアウト時に顧客レコードが作成されず、顧客は次の訪問時に支払手段を保存できません。</span><span class="sxs-lookup"><span data-stu-id="cb30a-150">When e-commerce visitors choose to check out as guests, customer records aren't created during checkout, and the customers can't save payment instruments for their next visit.</span></span> 

### <a name="named-user-checkout"></a><span data-ttu-id="cb30a-151">名前付きユーザー チェックアウト</span><span class="sxs-lookup"><span data-stu-id="cb30a-151">Named user checkout</span></span>

<span data-ttu-id="cb30a-152">名前付きユーザー (サインインした顧客) が、チェックアウト プロセスの支払手順に進むとリスト PI 機能を経験します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-152">When named users (signed-in customers) go to the payment step of the checkout process, they will experience the List PI capability.</span></span> <span data-ttu-id="cb30a-153">名前付きユーザーが初めてチェックアウトしたとき、クレジットカード情報が入力されるセクションに **次回の支払のために保存する** チェック ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-153">The first time that a named user checks out, a **Save for my next payment** check box appears in the section where credit card information is entered.</span></span> 

![[次回の支払のために保存する] オプション](../media/Payments/Save_PI.png)

<span data-ttu-id="cb30a-155">このチェックボックスが選択された場合、支払のために新しいクレジットカードを送信すると、名前付きユーザーの一意の顧客 ID が支払プロセッサに送信され、クレジットカードが安全に保存されてその一意の顧客 ID にマップされます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-155">If this check box is selected, when a new credit card is submitted for payment, the named user's unique customer ID is sent to the payment processor, and the credit card is securely saved and mapped to the that unique customer ID.</span></span> 

<span data-ttu-id="cb30a-156">同じ顧客が将来ストアフロントを訪れる際にサインインした場合、チェックアウト時の支払いに同じクレジットカードを選択ができます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-156">If the same customer signs in during future visits to the storefront, he or she will be able to select the same credit card for payment at checkout.</span></span> 

![以前に保存された支払手段](../media/Payments/Saved_PI.jpg)

### <a name="order-fulfillment-and-processing"></a><span data-ttu-id="cb30a-158">注文のフルフィルメントと処理</span><span class="sxs-lookup"><span data-stu-id="cb30a-158">Order fulfillment and processing</span></span>

<span data-ttu-id="cb30a-159">顧客がリスト PI 機能を使用して支払/入金明細行を適用した電子商取引の注文は、保存されたカード支払を使用せずに作成された注文と同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-159">E-Commerce orders where the customer applied a tender line by using the List PI capability work in the same way as orders that were created without using a saved card payment.</span></span> <span data-ttu-id="cb30a-160">注文処理およびフルフィルメントの観点から 2 種類の支払を区別できません。</span><span class="sxs-lookup"><span data-stu-id="cb30a-160">From the standpoint of order processing and fulfillment, the two types of payment are indistinguishable.</span></span> 

## <a name="details-of-ecommerce-payment-card-tokenization"></a><span data-ttu-id="cb30a-161">電子商取引の支払カード トークン化の詳細</span><span class="sxs-lookup"><span data-stu-id="cb30a-161">Details of eCommerce payment card tokenization</span></span>

### <a name="standard-flow"></a><span data-ttu-id="cb30a-162">標準フロー</span><span class="sxs-lookup"><span data-stu-id="cb30a-162">Standard flow</span></span>

<span data-ttu-id="cb30a-163">小売の電子商取引の統合で、支払カードはチェックアウト プロセスの一部として通常は入力され、完了前の注文と共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-163">In Retail e-Commerce integrations, the payment card is typically entered as part of the checkout process and is saved together with the order before finalization.</span></span> <span data-ttu-id="cb30a-164">カードの詳細は、支払プロセッサが提供する支払承認ページに直接入力されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-164">The card details are entered directly on a payment acceptance page that a payment processor provides.</span></span> <span data-ttu-id="cb30a-165">カードの詳細を入力し、チェックアウト プロセスの次のステップに進むと、プロセッサが注文作成プロセスで使用するトークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-165">After card details are entered and the customer moves on to the next step of the checkout process, the processor creates a token that is used later in the order creation process.</span></span> 

<span data-ttu-id="cb30a-166">顧客がオンライン注文を終了すると、承認要求の一部として支払カード トークンが支払プロセッサに送信されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-166">When the customer finalizes the online order, the payment card token is sent to the payment processor as part of an authorization request.</span></span> <span data-ttu-id="cb30a-167">支払承認要求が成功した場合、支払プロセッサは承認トークンを送信して返信します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-167">If the payment authorization request is successful, the payment processor replies by sending an authorization token.</span></span> <span data-ttu-id="cb30a-168">この承認トークンは顧客の注文と共に保存され、その注文がバック オフィスから履行されるときに参照されます。</span><span class="sxs-lookup"><span data-stu-id="cb30a-168">This authorization token is saved together with the customer's order and is referenced when that order is fulfilled from the back office.</span></span> 

### <a name="list-pi-flow"></a><span data-ttu-id="cb30a-169">リスト PI のフロー</span><span class="sxs-lookup"><span data-stu-id="cb30a-169">List PI flow</span></span>

<span data-ttu-id="cb30a-170">標準フローとリスト PI フローの主な違いは、顧客がクレジットカード番号を完全に入力する必要がないことです。</span><span class="sxs-lookup"><span data-stu-id="cb30a-170">The main difference between the standard flow and the List PI flow is that the customer doesn't have to enter the full credit card number.</span></span> <span data-ttu-id="cb30a-171">代わりに顧客は以前に保存したクレジット カードを選択し、カード検証値 (CVV 番号) を提供するだけです。</span><span class="sxs-lookup"><span data-stu-id="cb30a-171">Instead, the customer just has to select a previously saved credit card and provide the Card Verification Value (CVV number).</span></span> <span data-ttu-id="cb30a-172">顧客が正しい CVV 番号を提供し、チェックアウト プロセスの次の手順に進むと、支払プロセッサが承認要求を含む支払カード トークンを提供します。</span><span class="sxs-lookup"><span data-stu-id="cb30a-172">If the customer provides the correct CVV number and moves on to the next step of the checkout process, the payment processor provides a payment card token that will be included in the authorization request.</span></span> 

## <a name="related-articles"></a><span data-ttu-id="cb30a-173">関連記事</span><span class="sxs-lookup"><span data-stu-id="cb30a-173">Related articles</span></span>

- [<span data-ttu-id="cb30a-174">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="cb30a-174">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
