---
title: 重複支払の防止
description: このトピックでは、Modern POS で Dynamics 365 for Retail が支払いの重複を防ぐ方法について説明します。
author: rubendel
manager: AnnBe
ms.date: 01/09/2019
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
ms.openlocfilehash: 8952725b266d63411cdfad0adbd2005306eafd18
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2019
ms.locfileid: "377864"
---
# <a name="duplicate-payments-prevention"></a><span data-ttu-id="75fa1-103">重複支払の防止</span><span class="sxs-lookup"><span data-stu-id="75fa1-103">Duplicate payments prevention</span></span>
<span data-ttu-id="75fa1-104">このトピックは、Dynamics 365 for Retail Modern POS の重複支払防止機能の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-104">This topic provides an overview of the duplicate payments protection feature for Dynamics 365 for Retail Modern POS.</span></span>

## <a name="overview"></a><span data-ttu-id="75fa1-105">概要</span><span class="sxs-lookup"><span data-stu-id="75fa1-105">Overview</span></span>
<span data-ttu-id="75fa1-106">このトピックでは、販売時点管理 (POS) が支払ターミナルの通信を喪失し、POS とターミナルの同期がされない状況から回復する時のユーザー エクスペリエンスを説明します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-106">This topic describes the user experience when the point of sale (POS) recovers from a loss of communication with the payment terminal, which causes the POS and the payment terminal to be out of sync.</span></span>

<span data-ttu-id="75fa1-107">重複支払保護機能により、Dynamics 365 for Retail Modern POS は、通信が失われても、顧客が支払ターミナルを使用して別に支払処理をし、結果として重複して支払ってしまうようなことなくシームレスに回復できます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-107">The duplicate payment protection feature ensures that Dynamics 365 for Retail Modern POS can seamlessly recover from a loss of communication without requiring the shopper to process another payment through the payment terminal, which can lead to duplicate payments.</span></span>

<span data-ttu-id="75fa1-108">このトピックでは、重複支払保護機能の次の側面について説明します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-108">This topic covers the following aspects of the duplicate payment protection feature:</span></span>

- <span data-ttu-id="75fa1-109">[前提条件](#Prerequisites) - Dynamics 365 for Retail Modern POS でこの機能を活用するため、一連の前提条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-109">[Prerequisites](#Prerequisites) - Set of prerequisites to leverage this feature in Dynamics 365 for Retail Modern POS.</span></span>
- <span data-ttu-id="75fa1-110">[シナリオの詳細](#Scenario-details) - 重複支払保護機能の対象となるシナリオの詳細な説明。</span><span class="sxs-lookup"><span data-stu-id="75fa1-110">[Scenario details](#Scenario-details) - Detailed description of the scenarios covered by the duplicate payment protection feature.</span></span>
- <span data-ttu-id="75fa1-111">[トラブルシューティングの手順](#Troubleshooting) - 重複支払保護機能で問題が発生したときに実行する手順です。</span><span class="sxs-lookup"><span data-stu-id="75fa1-111">[Troubleshooting](#Troubleshooting) - Steps to take when encountering issues with the duplicate payment protection feature.</span></span>
- <span data-ttu-id="75fa1-112">[追加リソース](#Additional-resources) - 重複支払保護機能を使用する場合に役に立つ関連記事の一覧。</span><span class="sxs-lookup"><span data-stu-id="75fa1-112">[Additional resources](#Additional-resources) - List of related articles you might find useful when using the duplicate payment protection feature.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75fa1-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="75fa1-113">Prerequisites</span></span>
- <span data-ttu-id="75fa1-114">支払コネクタおよび対応する支払ゲートウェイまたはプロセッサは、この機能をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-114">The payment connector and corresponding payment gateway or processor must support this feature.</span></span> <span data-ttu-id="75fa1-115">*支払コネクタ*は、Dynamics 365 for Retail (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。</span><span class="sxs-lookup"><span data-stu-id="75fa1-115">The *payment connector* is an extension which facilitates communication between Dynamics 365 for Retail (and associated components) and a payment service.</span></span> <span data-ttu-id="75fa1-116">このトピックで説明されているコネクタは、標準支払 SDK を使用して実装されています。</span><span class="sxs-lookup"><span data-stu-id="75fa1-116">The connector described in this topic was implemented using the standard payments SDK.</span></span>
- <span data-ttu-id="75fa1-117">コネクタが対応する重複支払保護インターフェイスを実装する場合、 その機能は Dynamics 365 for Retail Modern POS で自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-117">If a connector implements the corresponding duplicate payment protection interfaces, the feature is automatically enabled in Dynamics 365 for Retail Modern POS.</span></span> <span data-ttu-id="75fa1-118">それ以外の場合、自動的に無効になっています。</span><span class="sxs-lookup"><span data-stu-id="75fa1-118">Otherwise, it is automatically turned off.</span></span>

<!---
The [Implement Duplicate Payment Protection](TODO) article describes in detail how to implement support for the duplicate payment protection feature for a given payment connector.
The [Dynamics 365 Payment Connector for Adyen](TODO) has built in support for the duplicate payment protection feature.
-->


## <a name="scenario-details"></a><span data-ttu-id="75fa1-119">シナリオの詳細</span><span class="sxs-lookup"><span data-stu-id="75fa1-119">Scenario details</span></span>
<span data-ttu-id="75fa1-120">重複支払保護機能は、支払が開始され、支払ターミナルで完了するどのようなシナリオにも適用可能ですが、Dynamics 365 for Retail Modern POS に対応する応答を受信することはできません。</span><span class="sxs-lookup"><span data-stu-id="75fa1-120">The duplicate payment protection feature is applicable to any scenario in which a payment is initiated and completed on a payment terminal, but Dynamics 365 for Retail Modern POS is unable to receive the corresponding response.</span></span> <span data-ttu-id="75fa1-121">その結果、顧客のカード (クレジット_カード) などに請求されますが、支払明細行は POS に追加されません。</span><span class="sxs-lookup"><span data-stu-id="75fa1-121">As a result, the customer's card (such as a credit card) is charged but the payment line is not added to the POS.</span></span> <span data-ttu-id="75fa1-122">ほとんどの場合、レジ担当者は支払ターミナルで後続支払をトリガーし、結果として顧客の重複支払が発生します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-122">In most cases, the cashier will trigger a subsequent payment on the payment terminal, which results in a duplicate payment for the customer.</span></span>

### <a name="how-duplicate-payments-scenarios-are-triggered"></a><span data-ttu-id="75fa1-123">重複する支払のシナリオが発生する方法</span><span class="sxs-lookup"><span data-stu-id="75fa1-123">How duplicate payments scenarios are triggered</span></span>
1. <span data-ttu-id="75fa1-124">**レジ担当者が支払を開始します。**</span><span class="sxs-lookup"><span data-stu-id="75fa1-124">**Cashier initiates payment**</span></span>
    - <span data-ttu-id="75fa1-125">レジ担当者が、Dynamics 365 for Retail Morern POS で**支払カード**をクリックし、**支払**ページに移り、**支払/入金**をクリックして、カード支払を開始します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-125">The cashier initiates a card payment by clicking **Pay card** in Dynamics 365 for Retail Modern POS, navigates to the **Payment** page, and clicks **Tender**.</span></span>
2. <span data-ttu-id="75fa1-126">**顧客は支払ターミナルを操作します。**</span><span class="sxs-lookup"><span data-stu-id="75fa1-126">**Customer interacts with payment terminal**</span></span>
    - <span data-ttu-id="75fa1-127">支払が開始された後、支払ターミナルは、顧客に支払を求めます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-127">After the payment is initiated, the payment terminal prompts the customer for payment.</span></span> <span data-ttu-id="75fa1-128">顧客は、支払ターミナルで支払プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-128">The customer initiates the payment process on the payment terminal.</span></span> 
3. <span data-ttu-id="75fa1-129">**Dynamics 365 for Retail Modern POS が支払ターミナルへの接続を失います**</span><span class="sxs-lookup"><span data-stu-id="75fa1-129">**Dynamics 365 for Retail Modern POS loses connectivity to the payment terminal**</span></span>
    - <span data-ttu-id="75fa1-130">顧客が支払ターミナルで支払を実行中に、Dynamics 365 for Retail Modern POS は、クラッシュ、ネットワーク接続の喪失、終了、もしくはターミナルの再起動のいずれかにより、支払ターミナルへの接続を失います。</span><span class="sxs-lookup"><span data-stu-id="75fa1-130">While the customer is running a payment on the payment terminal, Dynamics 365 for Retail Modern POS loses connectivity to the payment terminal because it either crashes, loses network connectivity, is closed, or the terminal is rebooted.</span></span>
    - <span data-ttu-id="75fa1-131">レジ担当者は Dynamics 365 for Retail Modern POS を再起動し、いかなる接続の問題も報告します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-131">The cashier will re-launch Dynamics 365 for Retail Modern POS and address any connectivity issues.</span></span>
4. <span data-ttu-id="75fa1-132">**顧客は支払ターミナルでの支払を完了**</span><span class="sxs-lookup"><span data-stu-id="75fa1-132">**Customer completes payment on the payment terminal**</span></span>
    - <span data-ttu-id="75fa1-133">Dynamics 365 for Retail Modern POS をリセットし、顧客が支払ターミナルで支払を完了すると、請求されます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-133">As Dynamics 365 for Retail Modern POS is being reset, the customer completes the payment on the payment terminal and is charged.</span></span>
5. <span data-ttu-id="75fa1-134">**Dynamics 365 for Retail Modern POS を起動します**</span><span class="sxs-lookup"><span data-stu-id="75fa1-134">**Dynamics 365 for Retail Modern POS is launched**</span></span>
    - <span data-ttu-id="75fa1-135">レジ担当者が Dynamics 365 for Retail のリセット/起動を完了しますが、支払が買い物カゴに追加されません。</span><span class="sxs-lookup"><span data-stu-id="75fa1-135">The cashier completes the reset/launch of Dynamics 365 for Retail Modern POS but the payment is not added to the cart.</span></span>

### <a name="payment-recovery-scenarios"></a><span data-ttu-id="75fa1-136">支払の回収シナリオ</span><span class="sxs-lookup"><span data-stu-id="75fa1-136">Payment recovery scenarios</span></span>
<span data-ttu-id="75fa1-137">販売またはネットワークの通信の点が回復した後は、レジ担当者が前の支払を使用するように要求されるいくつかのシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-137">Once the point of sale or network communications have been recovered, there are several scenarios that will result in the cashier being prompted to use the previous payment.</span></span> <span data-ttu-id="75fa1-138">支払の回収をトリガーできるいくつかのシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-138">Here are a few scenarios that can trigger payment recovery:</span></span>

<span data-ttu-id="75fa1-139">回復されない支払があり、レジ担当者が次のアクションのいずれかを実行する場合、支払が既にされていることを示すダイアログ ボックスがレジ担当者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-139">If there is a unrecovered payment and the cashier takes one of the following actions, the cashier is shown a dialog box indicating that a payment has already been made.</span></span>
- <span data-ttu-id="75fa1-140">カード支払を使用して金額に対して別の支払を起動します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-140">Invokes another payment for any amount using a card payment.</span></span>
- <span data-ttu-id="75fa1-141">カード支払を使用して支払額に対して別の支払を起動します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-141">Invokes another payment for any amount using a cash payment.</span></span>
- <span data-ttu-id="75fa1-142">買い物カゴの明細行を無効化しようとします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-142">Attempts to void a line on the cart.</span></span>
- <span data-ttu-id="75fa1-143">取引を無効化しようとします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-143">Attempts to void the transaction.</span></span>
- <span data-ttu-id="75fa1-144">取引を停止しますか?</span><span class="sxs-lookup"><span data-stu-id="75fa1-144">Attempts to suspend the transaction.</span></span>

![支払の回復](media/Payments/Duplicate-Payment-Protection/Recover-Payment.png)

<span data-ttu-id="75fa1-146">レジ担当者が **OK** をクリックすると、支払が復旧し、支払明細行として買い物カゴに追加されます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-146">When the cashier clicks **OK**, the payment is recovered and added as a payment line to the cart.</span></span>

<span data-ttu-id="75fa1-147">重複支払保護機能の主な機能は、元の支払が正常に処理され、対応する支払明細行が買い物カゴに追加されたのと同じ、あるべき状態に Dynamics 365 for Retail Modern POS を戻すことです。</span><span class="sxs-lookup"><span data-stu-id="75fa1-147">The primary function of the duplicate payment protection feature is to put Dynamics 365 for Retail Modern POS back into the same state it would be if the original payment would have been successfully processed and the corresponding payment line was added to the cart.</span></span>

### <a name="how-to-skip-payment-recovery"></a><span data-ttu-id="75fa1-148">支払の回復をスキップする方法</span><span class="sxs-lookup"><span data-stu-id="75fa1-148">How to skip payment recovery</span></span>
<span data-ttu-id="75fa1-149">場合によっては、レジ担当者は明示的に重複支払保護をスキップし、前の支払を復元しないように選択できます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-149">In some cases, the cashier might explicitly choose to skip the duplicate payment protection and opt not to recover a previous payment.</span></span> <span data-ttu-id="75fa1-150">その場合、レジ担当者は、支払を復元しないで取引を無効化するための次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-150">In those cases, the cashier can use the following steps described to void the transaction without recovering the payment.</span></span>

1. <span data-ttu-id="75fa1-151">**Dynamics 365 for Retail Modern POS の再起動**</span><span class="sxs-lookup"><span data-stu-id="75fa1-151">**Re-launch Dynamics 365 for Retail Modern POS**</span></span>
    - <span data-ttu-id="75fa1-152">Dynamics 365 for Retail Modern POS の支払ターミナルへの接続が失われた後、POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-152">After Dynamics 365 for Retail Modern POS has lost connectivity to the payment terminal, re-launch the POS.</span></span>
2. <span data-ttu-id="75fa1-153">**取引を無効にします**</span><span class="sxs-lookup"><span data-stu-id="75fa1-153">**Void the transaction**</span></span>
    - <span data-ttu-id="75fa1-154">買い物カゴページに移動し、**トランザクションの無効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-154">Navigate to the cart page and click **Void Transaction**.</span></span>
3. <span data-ttu-id="75fa1-155">**回復した支払を無視します。**</span><span class="sxs-lookup"><span data-stu-id="75fa1-155">**Ignore the recovered payment**</span></span>
    - <span data-ttu-id="75fa1-156">回復した支払が使用可能であることを示す新しいダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="75fa1-156">A new dialog box will appear indicating that a recovered payment is available.</span></span> <span data-ttu-id="75fa1-157">**無視** をクリックして復元した支払をスキップします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-157">Click **Ignore** to skip the payment recovery.</span></span>
    
![支払の回復をスキップします](media/Payments/Duplicate-Payment-Protection/Void-Transaction.png)

### <a name="what-to-do-if-the-customer-leaves-the-store"></a><span data-ttu-id="75fa1-159">顧客が店舗を出てしまった場合にすること</span><span class="sxs-lookup"><span data-stu-id="75fa1-159">What to do if the customer leaves the store</span></span>
<span data-ttu-id="75fa1-160">場合によっては、レジ担当者が取引を確定する前に顧客が店舗から出て行ってしまうことがあります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-160">In some cases, the customer might leave the store before the cashier can finalize the transaction.</span></span> <span data-ttu-id="75fa1-161">そのような場合は、[支払の回復をスキップする方法](#How-to-skip-payment-recovery)セクションで説明されている手順に従い、取引を無効にして、支払ゲートウェイ/プロセッサのポータルで支払を手動で無効にします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-161">In those cases, follow the steps described in the [How to skip payment recovery](#How-to-skip-payment-recovery) section to void the transaction and manually void the payment on the portal of the payment gateway/processor.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="75fa1-162">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="75fa1-162">Troubleshooting</span></span>

### <a name="general-issues"></a><span data-ttu-id="75fa1-163">一般的な問題</span><span class="sxs-lookup"><span data-stu-id="75fa1-163">General issues</span></span>
<span data-ttu-id="75fa1-164">すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。</span><span class="sxs-lookup"><span data-stu-id="75fa1-164">For all general issues, you should always consult the Modern POS or IIS Hardware Station event logs first.</span></span> <span data-ttu-id="75fa1-165">ログは、Windows イベント ログの以下のノードにあります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-165">The logs can be found under these nodes in the Windows event log:</span></span>
  - <span data-ttu-id="75fa1-166">**Application and Services Logs > Microsoft > Dynamics > Commerce-ModernPOS**</span><span class="sxs-lookup"><span data-stu-id="75fa1-166">**Application and Services Logs > Microsoft > Dynamics > Commerce-ModernPOS**</span></span>
  - <span data-ttu-id="75fa1-167">**Application and Services Logs > Microsoft > Dynamics > Commerce-Hardware Station**</span><span class="sxs-lookup"><span data-stu-id="75fa1-167">**Application and Services Logs > Microsoft > Dynamics > Commerce-Hardware Station**</span></span>

### <a name="validate-that-the-customer-is-not-double-charged"></a><span data-ttu-id="75fa1-168">顧客が重複して請求されていないか検証します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-168">Validate that the customer is not double charged</span></span>
<span data-ttu-id="75fa1-169">重複支払保護機能が有効になっている場合でも、販売者が、二重請求が発生していないことを検証することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="75fa1-169">Even if the duplicate payment protection feature is enabled, it is generally recommended that the merchant verifies that no double charge has occurred.</span></span> <span data-ttu-id="75fa1-170">これを行うには、対応する支払ゲートウェイ/プロセッサ ポータル上のすべての取引を確認します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-170">To do this, check all transactions on the corresponding payment gateway/processor portal.</span></span>

### <a name="payment-recovery-fails"></a><span data-ttu-id="75fa1-171">支払の回復が失敗する時</span><span class="sxs-lookup"><span data-stu-id="75fa1-171">Payment recovery fails</span></span>
<span data-ttu-id="75fa1-172">Dynamics 365 for Retail Modern POS で、前の支払の復元中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="75fa1-172">An error may occur while a previous payment is being recovered on Dynamics 365 for Retail Modern POS.</span></span> <span data-ttu-id="75fa1-173">これは、支払コネクタまたは支払ゲートウェイ/プロセッサが前の支払の復元を許可しないという問題がある時に発生します。</span><span class="sxs-lookup"><span data-stu-id="75fa1-173">This can happen if there is an issue in the payment connector or payment gateway/processor that does not allow the previous payment to be recovered.</span></span> <span data-ttu-id="75fa1-174">この問題を解決するには、前の支払を復元できないために起きているので、レジ担当者は[支払の回復をスキップする方法](#How-to-skip-payment-recovery)セクションで説明されているように、回復をスキップしなければなりません。</span><span class="sxs-lookup"><span data-stu-id="75fa1-174">To resolve this issue, because  the previous payment cannot be recovered, the cashier must skip the recovery as described in the [How to skip Payment Recovery](#How-to-skip-payment-recovery) section.</span></span> | 

## <a name="additional-resources"></a><span data-ttu-id="75fa1-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="75fa1-175">Additional resources</span></span>
- [<span data-ttu-id="75fa1-176">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="75fa1-176">Payments FAQ</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
