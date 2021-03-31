---
title: クレジット カードの設定、認証、および取得
description: この記事は、Microsoft Dynamics 365 Finance でのクレジット カード認証の概要を提供します。 これには、支払サービスの設定、クレジット カードを販売注文に追加、および認証を無効にする方法に関する情報が含まれます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baeaf6c47e9d799b729bb3f0b09a5e9e4511eac6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217461"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="f0609-104">クレジット カードの設定、認証、および取得</span><span class="sxs-lookup"><span data-stu-id="f0609-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0609-105">この記事は、Microsoft Dynamics 365 Finance でのクレジット カード認証の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="f0609-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="f0609-106">これには、支払サービスの設定、クレジット カードを販売注文に追加、および認証を無効にする方法に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f0609-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="f0609-107">クレジット カード支払サービスの設定</span><span class="sxs-lookup"><span data-stu-id="f0609-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="f0609-108">にクレジット カードを使用するには、[支払サービス] ページの支払サービスを設定して有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0609-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="f0609-109">支払サービスは、法人と、顧客のクレジット カード請求を処理する銀行とを橋渡しする役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="f0609-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="f0609-110">[支払コネクタ] フィールドに表示されるクレジット カード プロバイダーについて、そのプロバイダで使用するアカウントを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0609-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="f0609-111">その後、[支払サービス] ページの他のオプションを設定し、[クレジット カード タイプ] ページで American Express、Discover、MasterCard、Discover のクレジット カード タイプを設定し、既定プロバイダーを有効化します。</span><span class="sxs-lookup"><span data-stu-id="f0609-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="f0609-112">また、次の手順に従って設定を完了します:</span><span class="sxs-lookup"><span data-stu-id="f0609-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="f0609-113">[売掛金勘定パラメーター] ページで、クレジット カード認証に使用するパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0609-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="f0609-114">[支払条件] ページで、クレジット カードの支払条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="f0609-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="f0609-115">[支払タイプ] フィールドで、クレジット カードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f0609-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="f0609-116">[顧客のクレジット カード] ページで、顧客のクレジット カード情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f0609-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="f0609-117">新しいクレジット カードの追加</span><span class="sxs-lookup"><span data-stu-id="f0609-117">Adding a new credit card</span></span>
<span data-ttu-id="f0609-118">新しいクレジット カード レコードを作成するには、[顧客] ページで [顧客]、[設定]、[クレジット カード] の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="f0609-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="f0609-119">また、[販売注文] ページで販売注文を入力するときに、[管理]、[顧客]、[クレジット カード]、[登録] の順に進むとクレジット カード レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f0609-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="f0609-120">販売注文にクレジット カードを追加</span><span class="sxs-lookup"><span data-stu-id="f0609-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="f0609-121">販売注文にクレジット カードを追加するには、[販売注文] ページの [価格と割引] クイック タブで、クレジット カードのルックアップでクレジット カードを選択します。</span><span class="sxs-lookup"><span data-stu-id="f0609-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="f0609-122">認証プロセスを開始するには、[管理] タブの [アクション] ペインで、[クレジット カード] と [認証] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0609-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="f0609-123">クレジット カードの認証</span><span class="sxs-lookup"><span data-stu-id="f0609-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="f0609-124">クレジット カードが認証されると、カード番号とカード所有者の名前が確認された後で、利用可能な与信残高が確認されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="f0609-125">必要に応じて、カード検証番号とカード所有者の住所が確認されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="f0609-126">次に、顧客の利用可能な与信残高から請求金額が差し引かれます。</span><span class="sxs-lookup"><span data-stu-id="f0609-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="f0609-127">支払サービスは、クレジット カードの承認または否認を通知する情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="f0609-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="f0609-128">販売注文の請求時に、クレジット カードに対して請求金額が課金 (キャプチャ) されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="f0609-129">カード検証値</span><span class="sxs-lookup"><span data-stu-id="f0609-129">Card verification value</span></span>

<span data-ttu-id="f0609-130">カード セキュリティ コードとも呼ばれているカード検証値を要求できます。</span><span class="sxs-lookup"><span data-stu-id="f0609-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="f0609-131">アメリカン エキスプレスの場合、これは 4 桁の値です。</span><span class="sxs-lookup"><span data-stu-id="f0609-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="f0609-132">Discover、MasterCard、Visa の場合、これは 3 桁の値です。</span><span class="sxs-lookup"><span data-stu-id="f0609-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="f0609-133">住所の検証</span><span class="sxs-lookup"><span data-stu-id="f0609-133">Address verification</span></span>

<span data-ttu-id="f0609-134">住所の検証情報は、常に支払プロバイダーに送信されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="f0609-135">トランザクションの承認にどの程度の情報が必要かを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0609-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="f0609-136">その情報が受け入れられるかどうかは、プロバイダーに確認してください。</span><span class="sxs-lookup"><span data-stu-id="f0609-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="f0609-137">住所検証のオプションは次の通りです:</span><span class="sxs-lookup"><span data-stu-id="f0609-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="f0609-138">**トランザクションを常に承諾** – 住所の検証結果に関係なく、トランザクションを承認します。</span><span class="sxs-lookup"><span data-stu-id="f0609-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="f0609-139">**口座の名義** – トランザクションのカード保有者の名前をクレジット カード法人の情報と比較します。</span><span class="sxs-lookup"><span data-stu-id="f0609-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="f0609-140">**請求先住所** – トランザクションのカード保有者の名前と請求先住所をクレジット カード法人の情報と比較します。</span><span class="sxs-lookup"><span data-stu-id="f0609-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="f0609-141">**請求先郵便番号** – トランザクションのカード保有者の名前、請求先住所、郵便番号をクレジット カード法人の情報と比較します。</span><span class="sxs-lookup"><span data-stu-id="f0609-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="f0609-142">データ サポート</span><span class="sxs-lookup"><span data-stu-id="f0609-142">Data support</span></span>
<span data-ttu-id="f0609-143">サポートされている各クレジット カード タイプには、データ サポートのレベルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f0609-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="f0609-144">レベルにより、支払サービスに転送されるトランザクションに関する情報の程度が制御されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="f0609-145">この情報が提供されるかどうかは、プロバイダーに確認してください。</span><span class="sxs-lookup"><span data-stu-id="f0609-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="f0609-146">データ サポートのレベルのオプションは次の通りです:</span><span class="sxs-lookup"><span data-stu-id="f0609-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="f0609-147">**レベル 1** – トランザクションの日付、トランザクション金額、および説明を転送します。</span><span class="sxs-lookup"><span data-stu-id="f0609-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="f0609-148">**レベル 2** – レベル 1 の情報に加えて、出荷先住所と販売者の住所、および税金情報を転送します。</span><span class="sxs-lookup"><span data-stu-id="f0609-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="f0609-149">**レベル 3** – レベル 2 の情報に加えて、注文明細行情報を転送します。</span><span class="sxs-lookup"><span data-stu-id="f0609-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="f0609-150">一部支払</span><span class="sxs-lookup"><span data-stu-id="f0609-150">Partial payments</span></span>
<span data-ttu-id="f0609-151">注文の一部を出荷すると、部分注文の金額が取得され、その注文全体の金額の認証がクローズされます。</span><span class="sxs-lookup"><span data-stu-id="f0609-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="f0609-152">出荷されていない残りの注文については、新しい認証が送信されます。</span><span class="sxs-lookup"><span data-stu-id="f0609-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="f0609-153">承認の無効化</span><span class="sxs-lookup"><span data-stu-id="f0609-153">Voiding an authorization</span></span>
<span data-ttu-id="f0609-154">クレジット カード認証を無効にする場合、クレジット カード以外のタイプを持つ別の支払方法に変更できます。</span><span class="sxs-lookup"><span data-stu-id="f0609-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]