---
title: リンクされた払戻 - 以前に承認および確認済みのトランザクションの払戻
description: このトピックでは、リンクされた払戻を有効にして使用する方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 7/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-03-28
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 66517a215597ed36e4569043190049bf404b8cc6
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833058"
---
# <a name="linked-refunds--refunds-of-previously-approved-and-confirmed-transactions"></a><span data-ttu-id="3096e-103">リンクされた払戻 – 以前に承認および確認済みのトランザクションの払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-103">Linked refunds – Refunds of previously approved and confirmed transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3096e-104">返品は小売企業にとって重要な業務です。</span><span class="sxs-lookup"><span data-stu-id="3096e-104">Returns are an important operation for retailers.</span></span> <span data-ttu-id="3096e-105">販売に対する返品を受け入れて顧客への支払いを払い戻す機能により、小売企業は顧客のニーズに対応して問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-105">The ability to accept returns for sales and refund payments to customers gives retailers a way to service the needs of customers and to help resolve their issues.</span></span>

<span data-ttu-id="3096e-106">このトピックでは、リンクされた払戻を構成および使用する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3096e-106">This topic provides information about how to configure and use linked refunds.</span></span> <span data-ttu-id="3096e-107">リンクされた払戻は、以前に承認および確認されたトランザクションの払戻です。</span><span class="sxs-lookup"><span data-stu-id="3096e-107">A linked refund is a refund of a transaction that was previously approved and confirmed.</span></span> <span data-ttu-id="3096e-108">払戻は、トランザクションの全額払戻、または部分払戻のいずれかで、元の承認の全額を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3096e-108">The refund can be either a full refund or a partial refund of the transaction, and it can't exceed the full amount of the original authorization.</span></span> <span data-ttu-id="3096e-109">リンクされた払戻の機能は Microsoft Dynamics 365 for Retail バージョン 10.0.1 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-109">The functionality for linked refunds is available in Microsoft Dynamics 365 for Retail version 10.0.1.</span></span>

<span data-ttu-id="3096e-110">Microsoft Dynamics 365 for Retail バージョン 10.0 以前では、小売企業はカードへの払い戻しを処理できますが、レジ担当者はこれらの払戻を手動で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3096e-110">In Microsoft Dynamics 365 for Retail version 10.0 and earlier, retailers can process refunds to cards, but cashiers must manually specify these refunds.</span></span> <span data-ttu-id="3096e-111">レジ担当者は顧客がその支払い方法を提供した場合にのみ、元の支払い方法への払戻を処理できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-111">Cashiers can process refunds to the original mode of payment only if the customer provides that mode of payment.</span></span> <span data-ttu-id="3096e-112">したがって、新しいカードの詳細を提供することにより、顧客は返品プロセスを使用してあるカードから別のカードに残高を移動できるため、不正なカード残高の移動を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3096e-112">Therefore, by providing new card details, customers can use the return process to move balances from one card to another and therefore do unauthorized card balance transfers.</span></span>

<span data-ttu-id="3096e-113">リンクされた払戻を使用することで、元のトランザクション中に承認されたカードのみに払戻が処理されるようにして、小売業者はリスクを大幅に軽減できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-113">By using linked refunds, retailers can greatly reduce risk by making sure that refunds are processed only to the card that was authorized during the original transaction.</span></span> <span data-ttu-id="3096e-114">承認されていないカード残高の転送を防止するために、システムは確認され承認されたカード トークンを使用して払戻を処理するようレジ担当者に促すことができます。</span><span class="sxs-lookup"><span data-stu-id="3096e-114">To help prevent unauthorized card balance transfers, the system can prompt cashiers to use the confirmed and approved card token to process refunds.</span></span> <span data-ttu-id="3096e-115">払戻に元の支払い方法を使用することで小売企業はカード認証コストを削減できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-115">By using the original mode of payment for refunds, retailers can help reduce their card authorization costs.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3096e-116">必要条件</span><span class="sxs-lookup"><span data-stu-id="3096e-116">Prerequisites</span></span>
[<span data-ttu-id="3096e-117">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="3096e-117">Payment method Setup</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/payment-methods) 

[<span data-ttu-id="3096e-118">オムニ チャネル支払の設定</span><span class="sxs-lookup"><span data-stu-id="3096e-118">Omni channel payments setup</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/omni-channel-payments)

### <a name="additional-setup"></a><span data-ttu-id="3096e-119">追加の設定</span><span class="sxs-lookup"><span data-stu-id="3096e-119">Additional setup</span></span>

<span data-ttu-id="3096e-120">標準の Adyen コネクタ実装を使用していない顧客は、クレジットカードのトークン化をサポートするコネクタを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3096e-120">Customers who aren't using the out-of-box implementation of the Adyen Connector must set up the connector that supports tokenization of credit cards.</span></span> <span data-ttu-id="3096e-121">このトピックで説明されるすべてのシナリオは、小売 で提供される標準の支払ソフトウェア開発キット (SDK) を使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-121">All the scenarios that are described in this topic can be implemented by using the standard Payments software development kit (SDK) that is provided with Retail.</span></span> <span data-ttu-id="3096e-122">[Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) では、こちらで説明されるすべてのシナリオの直ぐに使える実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="3096e-122">The [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3) provides an out-of-box implementation of every scenario that is described here.</span></span>

## <a name="turn-on-the-linked-refunds-functionality"></a><span data-ttu-id="3096e-123">リンクされた払戻の機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="3096e-123">Turn on the linked refunds functionality</span></span>

<span data-ttu-id="3096e-124">リンクされた払戻機能は、Microsoft Dynamics 365 for Retail 8.1.3 以降で利用可能なオムニチャネル支払い機能と連携します。</span><span class="sxs-lookup"><span data-stu-id="3096e-124">The linked refunds functionality works with the omni-channel payments functionality that is available in Microsoft Dynamics 365 for Retail 8.1.3 and later.</span></span>

<span data-ttu-id="3096e-125">リンクされた払戻機能を有効にするには **小売 \> 本社の設定 \> パラメーター \> 小売共有パラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3096e-125">To turn on the linked refunds functionality, go to **Retail \> Headquarters setup \> Parameters \> Retail Shared parameters**.</span></span> <span data-ttu-id="3096e-126">**オムニ チャネル支払い** タブで **オムニ チャネル支払いを使用する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3096e-126">On the **Omni-channel payments** tab, set the **Use omni-channel payments** option to **Yes**.</span></span>

![オムニチャネル支払いの構成](media/LinkedRefundsOmniChannel.jpg)

<span data-ttu-id="3096e-128">オムニチャネル支払い機能をオンにすると、配送料とその他の料金を計算して料金を販売時点管理 (POS) 販売に追加するビジネス プロセス フローを変更します。</span><span class="sxs-lookup"><span data-stu-id="3096e-128">When you turn on the omni-channel payments functionality, you change the business process flow for calculating shipping charges and other charges, and for adding those charges to point of sale (POS) sales.</span></span> <span data-ttu-id="3096e-129">したがって、この機能を有効にする前に従業員のテストとトレーニングが必要です。</span><span class="sxs-lookup"><span data-stu-id="3096e-129">Therefore, make sure that you test and train your employees before you turn on this functionality.</span></span>

<span data-ttu-id="3096e-130">オムニチャネル支払い機能が有効の場合、1 つのチャネル (たとえば、コールセンターや Retail Modern POS \[MPOS\]) で使用されるカード支払いトークンは、小売企業に設定されたすべてのチャネルで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3096e-130">When the omni-channel payments functionality is turned on, the card payment tokens that are used in one channel (for example, a call center or Retail Modern POS \[MPOS\]) will be available in all channels that are set up for the retailer.</span></span> <span data-ttu-id="3096e-131">POS アプリケーションの場合は、リンクされた払戻機能も有効になります。</span><span class="sxs-lookup"><span data-stu-id="3096e-131">For POS applications, the linked refunds functionality will also be turned on.</span></span> <span data-ttu-id="3096e-132">コールセンター、MPOS、E コマース アプリケーションの場合、顧客は支払い用のカード番号を手動で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="3096e-132">For call center, MPOS, and e-Commerce applications, customers can still manually enter card numbers for payment.</span></span>

### <a name="supported-flows"></a><span data-ttu-id="3096e-133">サポートされているフロー</span><span class="sxs-lookup"><span data-stu-id="3096e-133">Supported flows</span></span>

<span data-ttu-id="3096e-134">レジ担当者は、返品のためにカードが提示されない場合も元のトランザクションで使用されたカードへの払戻を処理できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-134">Cashiers can process a refund to the card that was used during the original transaction, even if the card isn't presented for the return.</span></span>

- <span data-ttu-id="3096e-135">クレジットカードやデビットカードを使用する現金払いトランザクションのリンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-135">Linked refunds for cash-and-carry transactions that use credit or debit cards</span></span>
- <span data-ttu-id="3096e-136">クレジットカードやデビットカードを使用する顧客注文のリンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-136">Linked refunds for customer orders that use credit or debit cards</span></span>
 
### <a name="unsupported-flows"></a><span data-ttu-id="3096e-137">サポートされないフロー</span><span class="sxs-lookup"><span data-stu-id="3096e-137">Unsupported flows</span></span>

- <span data-ttu-id="3096e-138">ギフト カードを使用するトランザクションのリンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-138">Linked refunds for transactions that use gift cards</span></span>
- <span data-ttu-id="3096e-139">ロイヤルティ カードを使用するトランザクションのリンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-139">Linked refunds for transactions that use loyalty cards</span></span>
- <span data-ttu-id="3096e-140">交換注文のリンクされた払戻</span><span class="sxs-lookup"><span data-stu-id="3096e-140">Linked refunds for exchange orders</span></span>
- <span data-ttu-id="3096e-141">同じトランザクションでの複数の返品注文</span><span class="sxs-lookup"><span data-stu-id="3096e-141">Multiple return orders in the same transaction</span></span>
- <span data-ttu-id="3096e-142">レシートや顧客アカウントの詳細なしでの返品</span><span class="sxs-lookup"><span data-stu-id="3096e-142">Returns without a receipt or customer account details</span></span>

## <a name="use-case-examples"></a><span data-ttu-id="3096e-143">ユース ケース例</span><span class="sxs-lookup"><span data-stu-id="3096e-143">Use case examples</span></span>

<span data-ttu-id="3096e-144">このセクションでは、顧客注文やレシートが提示される返品のコンテキストで、リンクされた払戻と支払い承認の構成と使用の理解に役立つユース ケースの例を示します。</span><span class="sxs-lookup"><span data-stu-id="3096e-144">This section presents examples of use cases to help you understand the configuration and use of linked refunds and payment authorizations in the context of a customer order or a return where a receipt is presented.</span></span> <span data-ttu-id="3096e-145">これらの例は **オムニ チャネル支払** パラメーターが有効なときのアプリケーションの動作を示します。</span><span class="sxs-lookup"><span data-stu-id="3096e-145">These examples show the behavior of the application when the **Omni-channel payments** parameter has been turned on.</span></span>

### <a name="customer-accountbased-or-receipt-based-return-that-has-a-single-card-authorization"></a><span data-ttu-id="3096e-146">単一のカード認証を持つ顧客アカウント ベースまたはレシート ベースの返品</span><span class="sxs-lookup"><span data-stu-id="3096e-146">Customer account–based or receipt-based return that has a single card authorization</span></span>

<span data-ttu-id="3096e-147">顧客は単一のクレジット カードを使用して購入したアイテムを返品します。</span><span class="sxs-lookup"><span data-stu-id="3096e-147">A customer comes to return an item that was purchased by using a single credit card.</span></span> <span data-ttu-id="3096e-148">顧客はレシートを提出し、返品が許可された期間内で返品が行われます。</span><span class="sxs-lookup"><span data-stu-id="3096e-148">The customer provides a receipt, and the return is being made within the allowed period for returns.</span></span> <span data-ttu-id="3096e-149">レジ担当者がレシートをスキャンすると、返品するアイテムが処理されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-149">When the cashier scans the receipt, the item for return is processed.</span></span> <span data-ttu-id="3096e-150">レジ担当者が支払い方法のボタンを選択して支払いの払戻を処理すると、既存のクレジットカード認証が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-150">When the cashier processes the payment refund by selecting the button for any payment method, the existing credit card authorization is shown.</span></span>

![単一のカード認証](media/LinkedRefundsSingleAuthorization.jpg)

<span data-ttu-id="3096e-152">レジ係がクレジットカード認証を選択すると、支払いの払戻が処理され **トランザクションの終了** 画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-152">When the cashier selects the credit card authorization, the payment refund is processed, and the **Transaction end** screen appears.</span></span> <span data-ttu-id="3096e-153">レシートの印刷が構成されている場合、レジ担当者はレシートを印刷するように求められます。</span><span class="sxs-lookup"><span data-stu-id="3096e-153">If a receipt printing is configured, the cashier is prompted to print a receipt.</span></span>

### <a name="customer-accountbased-or-receipt-based-return-that-has-multiple-card-authorizations"></a><span data-ttu-id="3096e-154">複数のカード認証を持つ顧客アカウント ベースまたはレシート ベースの返品</span><span class="sxs-lookup"><span data-stu-id="3096e-154">Customer account–based or receipt-based return that has multiple card authorizations</span></span>

<span data-ttu-id="3096e-155">顧客は複数のクレジット カードを使用して購入したアイテムを返品します。</span><span class="sxs-lookup"><span data-stu-id="3096e-155">A customer comes to return an item that was purchased by using multiple credit cards.</span></span> <span data-ttu-id="3096e-156">レジ担当者がレシートをスキャンすると、返品するアイテムが処理されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-156">When the cashier scans the receipt, the item for return is processed.</span></span> <span data-ttu-id="3096e-157">レジ担当者が支払い方法のボタンを選択して支払いの払戻を処理すると、既存のクレジットカード認証がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-157">When the cashier processes the payment refund by selecting the button for any payment method, all the existing credit card authorizations are shown.</span></span>

![複数のカード認証](media/LinkedRefundsMultipleAuthorization.jpg)

<span data-ttu-id="3096e-159">レジ担当者がクレジットカード認証を選択すると、支払いの払戻が処理されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-159">When the cashier selects a credit card authorization, the payment refund is processed.</span></span> <span data-ttu-id="3096e-160">さらに返金する必要がある場合、現在のトランザクション画面に残額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-160">If more must be refunded, the current transaction screen shows the remaining amount.</span></span> <span data-ttu-id="3096e-161">レジ担当者がこの金額の支払いの払戻を処理すると、残りのクレジットカードの承認が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3096e-161">When the cashier processes the payment refund for this amount, the remaining credit card authorizations are shown.</span></span> <span data-ttu-id="3096e-162">このプロセスは払戻が必要な残額がなくなるまで続きます。</span><span class="sxs-lookup"><span data-stu-id="3096e-162">This process continues until there is no remaining amount that must be refunded.</span></span>

<span data-ttu-id="3096e-163">全額払戻が成功したら、レジ担当者はトランザクションを完了して構成済としてレシートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="3096e-163">After the full amount is successfully refunded, the cashier can complete the transaction, and a receipt can be printed as configured.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3096e-164">関連トピック</span><span class="sxs-lookup"><span data-stu-id="3096e-164">Related topics</span></span>

- [<span data-ttu-id="3096e-165">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3096e-165">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [<span data-ttu-id="3096e-166">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="3096e-166">Dynamics 365 Payment Connector for Adyen</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
