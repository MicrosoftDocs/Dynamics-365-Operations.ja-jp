---
title: 重複支払の防止
description: このトピックでは、Modern POS で Dynamics 365 Commerce が支払いの重複を防ぐ方法について説明します。
author: rubendel
manager: AnnBe
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2018-11-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 161d24480f4d970153e82b4e07f324669c216f65
ms.sourcegitcommit: 4c6d31f3ebd88212d3d1497a4bba9c64c5300444
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2020
ms.locfileid: "4409584"
---
# <a name="duplicate-payments-prevention"></a><span data-ttu-id="97a9c-103">重複支払の防止</span><span class="sxs-lookup"><span data-stu-id="97a9c-103">Duplicate payments prevention</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97a9c-104">このトピックは、Dynamics 365 Commerce Modern POS の重複支払防止機能の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-104">This topic provides an overview of the duplicate payments protection feature for Dynamics 365 Commerce Modern POS.</span></span>

## <a name="overview"></a><span data-ttu-id="97a9c-105">概要</span><span class="sxs-lookup"><span data-stu-id="97a9c-105">Overview</span></span>

<span data-ttu-id="97a9c-106">このトピックでは、販売時点管理 (POS) が支払ターミナルの通信を喪失し、POS とターミナルの同期がされない状況から回復する時のユーザー エクスペリエンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-106">This topic describes the user experience when the point of sale (POS) recovers from a loss of communication with the payment terminal, which causes the POS and the payment terminal to be out of sync.</span></span>

<span data-ttu-id="97a9c-107">重複支払保護機能により、Modern POS は、通信が失われても、顧客が支払ターミナルを使用して別に支払処理をし、結果として重複して支払ってしまうようなことなくシームレスに回復できます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-107">The duplicate payment protection feature ensures that Modern POS can seamlessly recover from a loss of communication without requiring the shopper to process another payment through the payment terminal, which can lead to duplicate payments.</span></span>

> [!NOTE]
> <span data-ttu-id="97a9c-108">重複支払保護機能は、支払ターミナルを使用して行われた支払に対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="97a9c-108">The duplicate payments protection feature is only supported for payments made using payment terminals.</span></span>

<span data-ttu-id="97a9c-109">このトピックでは、重複支払保護機能の次の側面について説明します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-109">This topic covers the following aspects of the duplicate payment protection feature:</span></span>

- <span data-ttu-id="97a9c-110">[前提条件](#prerequisites) – Modern POS でこの機能を活用するため、一連の前提条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-110">[Prerequisites](#prerequisites) – Set of prerequisites to leverage this feature in Modern POS.</span></span>
- <span data-ttu-id="97a9c-111">[シナリオの詳細](#scenario-details) – 重複支払保護機能の対象となるシナリオの詳細な説明。</span><span class="sxs-lookup"><span data-stu-id="97a9c-111">[Scenario details](#scenario-details) – Detailed description of the scenarios covered by the duplicate payment protection feature.</span></span>
- <span data-ttu-id="97a9c-112">[トラブルシューティング](#troubleshooting) – 重複支払保護機能で問題が発生したときに実行する手順です。</span><span class="sxs-lookup"><span data-stu-id="97a9c-112">[Troubleshooting](#troubleshooting) – Steps to take when encountering issues with the duplicate payment protection feature.</span></span>
- <span data-ttu-id="97a9c-113">[追加リソース](#additional-resources) – 重複支払保護機能を使用する場合に役に立つ関連記事の一覧。</span><span class="sxs-lookup"><span data-stu-id="97a9c-113">[Additional resources](#additional-resources) – List of related articles you might find useful when using the duplicate payment protection feature.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97a9c-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="97a9c-114">Prerequisites</span></span>

- <span data-ttu-id="97a9c-115">支払コネクタおよび対応する支払ゲートウェイまたはプロセッサは、この機能をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-115">The payment connector and corresponding payment gateway or processor must support this feature.</span></span> <span data-ttu-id="97a9c-116">*支払コネクタ* は、コマース (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="97a9c-116">The *payment connector* is an extension which facilitates communication between Commerce (and associated components) and a payment service.</span></span> <span data-ttu-id="97a9c-117">このトピックで説明されているコネクタは、標準支払 SDK を使用して実装されています。</span><span class="sxs-lookup"><span data-stu-id="97a9c-117">The connector described in this topic was implemented using the standard payments SDK.</span></span>
- <span data-ttu-id="97a9c-118">コネクタが対応する重複支払保護インターフェイスを実装する場合、 その機能は Modern POS で自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-118">If a connector implements the corresponding duplicate payment protection interfaces, the feature is automatically enabled in Modern POS.</span></span> <span data-ttu-id="97a9c-119">それ以外の場合、自動的に無効になっています。</span><span class="sxs-lookup"><span data-stu-id="97a9c-119">Otherwise, it is automatically turned off.</span></span>

<!---
The [Implement Duplicate Payment Protection](TODO) article describes in detail how to implement support for the duplicate payment protection feature for a given payment connector.
The [Dynamics 365 Payment Connector for Adyen](TODO) has built in support for the duplicate payment protection feature.
-->

## <a name="scenario-details"></a><span data-ttu-id="97a9c-120">シナリオの詳細</span><span class="sxs-lookup"><span data-stu-id="97a9c-120">Scenario details</span></span>

<span data-ttu-id="97a9c-121">重複支払保護機能は、支払が開始され、支払ターミナルで完了するどのようなシナリオにも適用可能ですが、Modern POS に対応する応答を受信することはできません。</span><span class="sxs-lookup"><span data-stu-id="97a9c-121">The duplicate payment protection feature is applicable to any scenario in which a payment is initiated and completed on a payment terminal, but Modern POS is unable to receive the corresponding response.</span></span> <span data-ttu-id="97a9c-122">その結果、顧客のカード (クレジット_カード) などに請求されますが、支払明細行は POS に追加されません。</span><span class="sxs-lookup"><span data-stu-id="97a9c-122">As a result, the customer's card (such as a credit card) is charged but the payment line is not added to the POS.</span></span> <span data-ttu-id="97a9c-123">ほとんどの場合、レジ担当者は支払ターミナルで後続支払をトリガーし、結果として顧客の重複支払が発生します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-123">In most cases, the cashier will trigger a subsequent payment on the payment terminal, which results in a duplicate payment for the customer.</span></span>

### <a name="how-duplicate-payments-scenarios-are-triggered"></a><span data-ttu-id="97a9c-124">重複する支払のシナリオが発生する方法</span><span class="sxs-lookup"><span data-stu-id="97a9c-124">How duplicate payments scenarios are triggered</span></span>

1. <span data-ttu-id="97a9c-125">**レジ担当者が支払を開始します。**</span><span class="sxs-lookup"><span data-stu-id="97a9c-125">**Cashier initiates payment**</span></span>

    <span data-ttu-id="97a9c-126">レジ担当者が、**カードで支払う** をクリックし、**支払** ページに移り、**支払/入金** をクリックして、カード支払を開始します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-126">The cashier initiates a card payment by clicking **Pay card**, navigates to the **Payment** page, and clicks **Tender**.</span></span>

2. <span data-ttu-id="97a9c-127">**顧客は支払ターミナルを操作します。**</span><span class="sxs-lookup"><span data-stu-id="97a9c-127">**Customer interacts with payment terminal**</span></span>

    <span data-ttu-id="97a9c-128">支払が開始された後、支払ターミナルは、顧客に支払を求めます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-128">After the payment is initiated, the payment terminal prompts the customer for payment.</span></span> <span data-ttu-id="97a9c-129">顧客は、支払ターミナルで支払プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-129">The customer initiates the payment process on the payment terminal.</span></span> 

3. <span data-ttu-id="97a9c-130">**Modern POS が支払ターミナルへの接続を失います**</span><span class="sxs-lookup"><span data-stu-id="97a9c-130">**Modern POS loses connectivity to the payment terminal**</span></span>

    - <span data-ttu-id="97a9c-131">顧客が支払ターミナルで支払を実行中に、Modern POS は、クラッシュ、ネットワーク接続の喪失、終了、もしくはターミナルの再起動のいずれかにより、支払ターミナルへの接続を失います。</span><span class="sxs-lookup"><span data-stu-id="97a9c-131">While the customer is running a payment on the payment terminal, Modern POS loses connectivity to the payment terminal because it either crashes, loses network connectivity, is closed, or the terminal is rebooted.</span></span>
    - <span data-ttu-id="97a9c-132">レジ担当者は Modern POS を再起動し、いかなる接続の問題も報告します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-132">The cashier will re-launch Modern POS and address any connectivity issues.</span></span>

4. <span data-ttu-id="97a9c-133">**顧客は支払ターミナルでの支払を完了**</span><span class="sxs-lookup"><span data-stu-id="97a9c-133">**Customer completes payment on the payment terminal**</span></span>

    <span data-ttu-id="97a9c-134">Modern POS をリセットし、顧客が支払ターミナルで支払を完了すると、請求されます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-134">As Modern POS is being reset, the customer completes the payment on the payment terminal and is charged.</span></span>

5. <span data-ttu-id="97a9c-135">**Modern POS を起動します**</span><span class="sxs-lookup"><span data-stu-id="97a9c-135">**Modern POS is launched**</span></span>

    <span data-ttu-id="97a9c-136">レジ担当者が Modern POS のリセット/起動を完了しますが、支払が買い物カゴに追加されません。</span><span class="sxs-lookup"><span data-stu-id="97a9c-136">The cashier completes the reset/launch of Modern POS but the payment is not added to the cart.</span></span>

### <a name="payment-recovery-scenarios"></a><span data-ttu-id="97a9c-137">支払の回収シナリオ</span><span class="sxs-lookup"><span data-stu-id="97a9c-137">Payment recovery scenarios</span></span>

<span data-ttu-id="97a9c-138">POS またはネットワーク通信が回復した後は、レジ担当者が前の支払を使用するように要求されるいくつかのシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-138">Once the POS or network communications have been recovered, there are several scenarios that will result in the cashier being prompted to use the previous payment.</span></span> <span data-ttu-id="97a9c-139">支払の回収をトリガーできるいくつかのシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-139">Here are a few scenarios that can trigger payment recovery:</span></span>

<span data-ttu-id="97a9c-140">回復されない支払があり、レジ担当者が次のアクションのいずれかを実行する場合、支払が既にされていることを示すダイアログ ボックスがレジ担当者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-140">If there is an unrecovered payment and the cashier takes one of the following actions, the cashier is shown a dialog box indicating that a payment has already been made.</span></span>

- <span data-ttu-id="97a9c-141">カード支払を使用して金額に対して別の支払を起動します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-141">Invokes another payment for any amount using a card payment.</span></span>
- <span data-ttu-id="97a9c-142">カード支払を使用して支払額に対して別の支払を起動します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-142">Invokes another payment for any amount using a cash payment.</span></span>
- <span data-ttu-id="97a9c-143">買い物カゴの明細行を無効化しようとします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-143">Attempts to void a line on the cart.</span></span>
- <span data-ttu-id="97a9c-144">取引を無効化しようとします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-144">Attempts to void the transaction.</span></span>
- <span data-ttu-id="97a9c-145">取引を停止しますか?</span><span class="sxs-lookup"><span data-stu-id="97a9c-145">Attempts to suspend the transaction.</span></span>

![支払の回復](media/Payments/Duplicate-Payment-Protection/Recover-Payment.png)

<span data-ttu-id="97a9c-147">レジ担当者が **OK** をクリックすると、支払が復旧し、支払明細行として買い物カゴに追加されます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-147">When the cashier clicks **OK**, the payment is recovered and added as a payment line to the cart.</span></span>

<span data-ttu-id="97a9c-148">重複支払保護機能の主な機能は、元の支払が正常に処理され、対応する支払明細行が買い物カゴに追加されたのと同じ、あるべき状態に Modern POS を戻すことです。</span><span class="sxs-lookup"><span data-stu-id="97a9c-148">The primary function of the duplicate payment protection feature is to put Modern POS back into the same state it would be if the original payment would have been successfully processed and the corresponding payment line was added to the cart.</span></span>

### <a name="how-to-skip-payment-recovery"></a><span data-ttu-id="97a9c-149">支払の回復をスキップする方法</span><span class="sxs-lookup"><span data-stu-id="97a9c-149">How to skip payment recovery</span></span>

<span data-ttu-id="97a9c-150">場合によっては、レジ担当者は明示的に重複支払保護をスキップし、前の支払を復元しないように選択できます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-150">In some cases, the cashier might explicitly choose to skip the duplicate payment protection and opt not to recover a previous payment.</span></span> <span data-ttu-id="97a9c-151">その場合、レジ担当者は、支払を復元しないで取引を無効化するための次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-151">In those cases, the cashier can use the following steps described to void the transaction without recovering the payment.</span></span>

1. <span data-ttu-id="97a9c-152">**Modern POS の再起動**</span><span class="sxs-lookup"><span data-stu-id="97a9c-152">**Re-launch Modern POS**</span></span>

    <span data-ttu-id="97a9c-153">Modern POS の支払ターミナルへの接続が失われた後、POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-153">After Modern POS has lost connectivity to the payment terminal, re-launch the POS.</span></span>

2. <span data-ttu-id="97a9c-154">**取引を無効にします**</span><span class="sxs-lookup"><span data-stu-id="97a9c-154">**Void the transaction**</span></span>

    <span data-ttu-id="97a9c-155">買い物カゴページに移動し、**トランザクションの無効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-155">Navigate to the cart page and click **Void Transaction**.</span></span>

3. <span data-ttu-id="97a9c-156">**回復した支払を無視します。**</span><span class="sxs-lookup"><span data-stu-id="97a9c-156">**Ignore the recovered payment**</span></span>

    <span data-ttu-id="97a9c-157">回復した支払が使用可能であることを示す新しいダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="97a9c-157">A new dialog box will appear indicating that a recovered payment is available.</span></span> <span data-ttu-id="97a9c-158">**無視** をクリックして復元した支払をスキップします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-158">Click **Ignore** to skip the payment recovery.</span></span>

![支払の回復をスキップします](media/Payments/Duplicate-Payment-Protection/Void-Transaction.png)

### <a name="what-to-do-if-the-customer-leaves-the-store"></a><span data-ttu-id="97a9c-160">顧客が店舗を出てしまった場合にすること</span><span class="sxs-lookup"><span data-stu-id="97a9c-160">What to do if the customer leaves the store</span></span>

<span data-ttu-id="97a9c-161">場合によっては、レジ担当者が取引を確定する前に顧客が店舗から出て行ってしまうことがあります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-161">In some cases, the customer might leave the store before the cashier can finalize the transaction.</span></span> <span data-ttu-id="97a9c-162">そのような場合は、[支払の回復をスキップする方法](#how-to-skip-payment-recovery)セクションで説明されている手順に従い、取引を無効にして、支払ゲートウェイ/プロセッサのポータルで支払を手動で無効にします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-162">In those cases, follow the steps described in the [How to skip payment recovery](#how-to-skip-payment-recovery) section to void the transaction and manually void the payment on the portal of the payment gateway/processor.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="97a9c-163">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="97a9c-163">Troubleshooting</span></span>

### <a name="general-issues"></a><span data-ttu-id="97a9c-164">一般的な問題</span><span class="sxs-lookup"><span data-stu-id="97a9c-164">General issues</span></span>

<span data-ttu-id="97a9c-165">すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。</span><span class="sxs-lookup"><span data-stu-id="97a9c-165">For all general issues, you should always consult the Modern POS or IIS Hardware Station event logs first.</span></span> <span data-ttu-id="97a9c-166">ログは、Windows イベント ログの以下のノードにあります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-166">The logs can be found under these nodes in the Windows event log:</span></span>

- <span data-ttu-id="97a9c-167">アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="97a9c-167">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="97a9c-168">アプリケーションおよびサービス ログ \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="97a9c-168">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

### <a name="validate-that-the-customer-is-not-double-charged"></a><span data-ttu-id="97a9c-169">顧客が重複して請求されていないか検証します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-169">Validate that the customer is not double charged</span></span>

<span data-ttu-id="97a9c-170">重複支払保護機能が有効になっている場合でも、販売者が、二重請求が発生していないことを検証することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="97a9c-170">Even if the duplicate payment protection feature is enabled, it is generally recommended that the merchant verifies that no double charge has occurred.</span></span> <span data-ttu-id="97a9c-171">これを行うには、対応する支払ゲートウェイ/プロセッサ ポータル上のすべての取引を確認します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-171">To do this, check all transactions on the corresponding payment gateway/processor portal.</span></span>

### <a name="payment-recovery-fails"></a><span data-ttu-id="97a9c-172">支払の回復が失敗する時</span><span class="sxs-lookup"><span data-stu-id="97a9c-172">Payment recovery fails</span></span>

<span data-ttu-id="97a9c-173">Modern POS で、前の支払の復元中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="97a9c-173">An error may occur while a previous payment is being recovered on Modern POS.</span></span> <span data-ttu-id="97a9c-174">これは、支払コネクタまたは支払ゲートウェイ/プロセッサが前の支払の復元を許可しないという問題がある時に発生します。</span><span class="sxs-lookup"><span data-stu-id="97a9c-174">This can happen if there is an issue in the payment connector or payment gateway/processor that does not allow the previous payment to be recovered.</span></span> <span data-ttu-id="97a9c-175">この問題を解決するには、前の支払を復元できないために起きているので、レジ担当者は [支払の回復をスキップする方法](#how-to-skip-payment-recovery) セクションで説明されているように、回復をスキップしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="97a9c-175">To resolve this issue, because the previous payment cannot be recovered, the cashier must skip the recovery as described in the [How to skip Payment Recovery](#how-to-skip-payment-recovery) section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97a9c-176">追加リソース</span><span class="sxs-lookup"><span data-stu-id="97a9c-176">Additional resources</span></span>

- [<span data-ttu-id="97a9c-177">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="97a9c-177">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
