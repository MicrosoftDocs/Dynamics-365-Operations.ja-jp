---
title: Dynamics 365 Fraud Protection の Dynamics 365 Commerce との統合
description: このトピックでは、Microsoft Dynamics 365 Fraud Protection と Dynamics 365 Commerce との間で使用可能な標準統合について説明します。
author: rubendel
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Commerce
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: efa2862ad850c26eca9207a06d1065beb4026362
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091812"
---
# <a name="dynamics-365-fraud-protection-integration-with-dynamics-365-commerce"></a><span data-ttu-id="f8764-103">Dynamics 365 Fraud Protection の Dynamics 365 Commerce との統合</span><span class="sxs-lookup"><span data-stu-id="f8764-103">Dynamics 365 Fraud Protection integration with Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f8764-104">このトピックでは、Microsoft Dynamics 365 Commerce と Dynamics 365 Fraud Protection との間で使用可能な標準統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="f8764-104">This topic describes out-of-box integrations that are available between Microsoft Dynamics 365 Commerce and Dynamics 365 Fraud Protection.</span></span>

## <a name="key-terms"></a><span data-ttu-id="f8764-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="f8764-105">Key terms</span></span>

| <span data-ttu-id="f8764-106">相談</span><span class="sxs-lookup"><span data-stu-id="f8764-106">Term</span></span> | <span data-ttu-id="f8764-107">説明</span><span class="sxs-lookup"><span data-stu-id="f8764-107">Description</span></span> |
|---|---|
| <span data-ttu-id="f8764-108">購入保護</span><span class="sxs-lookup"><span data-stu-id="f8764-108">Purchase protection</span></span> | <span data-ttu-id="f8764-109">マーチャントが決定したリスクレベルに基づいて、購入に対して不正の分析をおこないう Fraud Protection モジュール。</span><span class="sxs-lookup"><span data-stu-id="f8764-109">The Fraud Protection module that analyzes purchases for fraud, based on risk levels that are determined by the merchant.</span></span> |
| <span data-ttu-id="f8764-110">店舗</span><span class="sxs-lookup"><span data-stu-id="f8764-110">Storefront</span></span> | <span data-ttu-id="f8764-111">商取引に提供する標準の電子商取引店舗。</span><span class="sxs-lookup"><span data-stu-id="f8764-111">The out-of-box e-commerce storefront that is provided with Commerce.</span></span> |

## <a name="overview"></a><span data-ttu-id="f8764-112">概要</span><span class="sxs-lookup"><span data-stu-id="f8764-112">Overview</span></span>

<span data-ttu-id="f8764-113">Fraud Protection は、小売業者が不正活動を防ぎ、知られていない可能性がある不正の場所を特定するのを助ける Fraud Protection ソリューションを提供するサービスです。</span><span class="sxs-lookup"><span data-stu-id="f8764-113">Fraud Protection is a service that offers fraud protection solutions to help retailers prevent fraudulent activity and identify places where fraud might be unnoticed.</span></span> <span data-ttu-id="f8764-114">このトピックでは、Fraud Protection と Commerce との間で使用可能な標準統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="f8764-114">This topic describes out-of-box integrations between Fraud Protection and Commerce.</span></span> <span data-ttu-id="f8764-115">これは、今後のリリースで 2 つのサービスの間で新しい統合がリリースされると、更新されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-115">It will be updated as new integrations between the two services are released in future releases.</span></span> <span data-ttu-id="f8764-116">Commerce との標準統合ではまだサポートされていないモジュールに関する情報など、Fraud Protection に関する詳しい情報は、[Fraud Protection ランディング ページ](https://dynamics.microsoft.com/ai/fraud-protection/) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f8764-116">For more information about Fraud Protection, including information about modules that aren't yet supported by an out-of-box integration with Commerce, visit the [Fraud Protection landing page](https://dynamics.microsoft.com/ai/fraud-protection/).</span></span> <span data-ttu-id="f8764-117">また、Dynamics 365 の営業担当者から [コールバックを要請](https://dynamics.microsoft.com/get-started/?appname=fraudprotection) し、Fraud Protection が利益性を大幅に増加し、運営経費を削減し、顧客エクスペリエンスを向上させる方法について話をすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f8764-117">You can also [request a callback](https://dynamics.microsoft.com/get-started/?appname=fraudprotection) from a Dynamics 365 sales representative to discuss how Fraud Protection can help boost profitability, reduce operational expenses, and improve customer experiences.</span></span>

## <a name="purchase-protection-in-commerce"></a><span data-ttu-id="f8764-118">Commerce の購入保護</span><span class="sxs-lookup"><span data-stu-id="f8764-118">Purchase protection in Commerce</span></span>

### <a name="purchase-protection-overview"></a><span data-ttu-id="f8764-119">購入保護の概要</span><span class="sxs-lookup"><span data-stu-id="f8764-119">Purchase protection overview</span></span>

<span data-ttu-id="f8764-120">Fraud Protection から最初に使用可能な一般的なオファリングは、マーチャントを組織の Fraud Protection ダッシュボード へとサインインさせ、オンライン購入に当たっての不正ルールを定義させる購入保護モジュールです。</span><span class="sxs-lookup"><span data-stu-id="f8764-120">The first generally available offering from Fraud Protection is a purchase protection module that lets merchants sign in to the Fraud Protection dashboard for their organization and define fraud rules for online purchases.</span></span> <span data-ttu-id="f8764-121">Fraud Protection でマーチャントが構成する設定に基づいて、電子商取引トランザクションは支払認証に送られる前に Fraud Protection を使って検証することができます。</span><span class="sxs-lookup"><span data-stu-id="f8764-121">Based on the settings that a merchant configures in Fraud Protection, e-commerce transactions can be validated with Fraud Protection before they are sent for payment authorization.</span></span>

<span data-ttu-id="f8764-122">注文が Fraud Protection 購入保護モジュールに送信される場合、Fraud Protection は購入を分析し、マーチャントが定義した不正ルールと人工知能 (AI) によって駆動されるインサイト、そしてにコンソーシアムベースの不正分析に基づいてリスク評価を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8764-122">When an order is sent to the Fraud Protection purchase protection module, Fraud Protection analyzes the purchase and provides a risk assessment, based on merchant-defined fraud rules, insights that are driven by artificial intelligence (AI), and consortium-based fraud analytics.</span></span> <span data-ttu-id="f8764-123">不正スコアがマーチャントのリスク トレランスの次元を超過して返された場合は、Fraud Protection は店舗に注文を拒否するように指示を出します。</span><span class="sxs-lookup"><span data-stu-id="f8764-123">If the fraud score that is returned for the order exceeds the merchant's risk tolerance, Fraud Protection instructs the storefront to reject the order.</span></span> <span data-ttu-id="f8764-124">注文が拒否されない場合は、Fraud Protection は店舗が注文のフルフィルメント処理の次のステップを決定するために使用できる不正スコアを返します。</span><span class="sxs-lookup"><span data-stu-id="f8764-124">If an order isn't rejected, Fraud Protection returns a fraud score that the storefront can use to determine the next steps in the order fulfillment process.</span></span> <span data-ttu-id="f8764-125">このようなステップには、注文の手動レビューのために注文を保留にしたり、注文した顧客のフォローアップなどが含まれることがあります。</span><span class="sxs-lookup"><span data-stu-id="f8764-125">Those steps might include putting the order on hold for manual review or follow-up with the customer who placed the order.</span></span>

### <a name="supported-capabilities-in-the-purchase-protection-integration"></a><span data-ttu-id="f8764-126">購入保護統合でサポートされている機能</span><span class="sxs-lookup"><span data-stu-id="f8764-126">Supported capabilities in the purchase protection integration</span></span>

#### <a name="purchase-events"></a><span data-ttu-id="f8764-127">発注イベント</span><span class="sxs-lookup"><span data-stu-id="f8764-127">Purchase events</span></span>

<span data-ttu-id="f8764-128">現在、Commerce はパブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="f8764-128">Currently, Commerce is in public preview.</span></span> <span data-ttu-id="f8764-129">ただし、一般的で入手可能になった場合には、この購入保護統合は Fraud Protection リスク評価の受信とストア店舗での注文の中止をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f8764-129">However, when it becomes generally available, the purchase protection integration will support the receipt of Fraud Protection risk assessments and termination of orders in the online storefront.</span></span>

<span data-ttu-id="f8764-130">こちらが購入イベントのフローです。</span><span class="sxs-lookup"><span data-stu-id="f8764-130">Here is the flow for purchase events.</span></span>

1. <span data-ttu-id="f8764-131">店舗の顧客が、商品を買い物かごに追加してチェックアウトへと進みます。</span><span class="sxs-lookup"><span data-stu-id="f8764-131">A storefront customer adds items to the basket and proceeds to checkout.</span></span>
2. <span data-ttu-id="f8764-132">顧客が配送先と支払の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8764-132">The customer enters shipping and payment details.</span></span>
3. <span data-ttu-id="f8764-133">前提条件が完了した後、顧客が **注文する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8764-133">After the prerequisites are completed, the customer selects **Place order**.</span></span>
4. <span data-ttu-id="f8764-134">購入保護評価のために、注文の詳細が Fraud Protection に送信されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-134">Order details are sent to Fraud Protection for purchase protection assessment.</span></span>
5. <span data-ttu-id="f8764-135">Fraud Protection で定義されたマーチャント ルールがこのオーダーを拒否すべきと判断した場合は、応答が店舗に送信され、注文は中止されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-135">If the merchant rules that are defined in Fraud Protection determine that the order should be rejected, a response is sent to the storefront, and the order is terminated.</span></span>

<span data-ttu-id="f8764-136">Fraud Protection 購入保護が注文の中止をおこなった場合は、ユーザーは次のメッセージを受信します : 「このオーダーは現時点では処理できません</span><span class="sxs-lookup"><span data-stu-id="f8764-136">If Fraud Protection purchase protection causes an order to be terminated, the user receives the following error message: "The order cannot be processed at this time.</span></span> <span data-ttu-id="f8764-137">後でもう一度お試しください。」</span><span class="sxs-lookup"><span data-stu-id="f8764-137">Please try again later."</span></span>

![参照となる店舗から拒否された注文の例](../media/Payments/SampleDFPReject.png)

<span data-ttu-id="f8764-139">あるいは、マーチャント ルールがこの注文は承認されるべきと判断した場合は、不正スコアと Fraud Protection で判定された理由コードを含む回答が店舗へ送信されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-139">Alternatively, if the merchant rules determine that the order should be approved, the response that is sent to the storefront includes the fraud score and the reason code that were determined by Fraud Protection.</span></span> <span data-ttu-id="f8764-140">初期統合では、Fraud Protection 評価はどちらにしても使われておらず、承認と拒否の両セクションの回答は保存されません。</span><span class="sxs-lookup"><span data-stu-id="f8764-140">For the initial integration, the Fraud Protection assessment isn't used in any way, and the response for both approval and rejection scenarios isn't saved.</span></span>

<span data-ttu-id="f8764-141">拒否された注文は、支払プロセスの承認には送信されず、バック オフィスの注文作成プロセスには進みません。</span><span class="sxs-lookup"><span data-stu-id="f8764-141">Rejected orders aren't sent to payment processors for authorization, and they don't go through the order creation process in the back office.</span></span>

#### <a name="bank-events"></a><span data-ttu-id="f8764-142">銀行イベント</span><span class="sxs-lookup"><span data-stu-id="f8764-142">Bank events</span></span>

<span data-ttu-id="f8764-143">オンライン注文が Fraud Protection 評価に基づいて許可された場合は、次のステップは、その注文が支払承認が該当する場合は、支払いの承認になります。</span><span class="sxs-lookup"><span data-stu-id="f8764-143">If an online order is approved based on the Fraud Protection assessment, the next step is to authorize payments for that order, if payment authorizations are applicable.</span></span> <span data-ttu-id="f8764-144">支払プロセッサがこの注文を承認したら、Fraud Protection に承認結果が通知されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-144">Once the order is authorized with the payment processor, Fraud Protection is notified of the authorization result.</span></span> <span data-ttu-id="f8764-145">この結果を Fraud Protection に送信することで、高度な AI は生来の承認結果を予測するためにさらに学習することができ、それによって将来の Fraud Protection 評価の質を著しく向上させます。</span><span class="sxs-lookup"><span data-stu-id="f8764-145">By sending these results to Fraud Protection, the advanced AI can be trained to better predict future authorization results, thereby boosting the quality of future Fraud Protection assessments.</span></span>

#### <a name="purchase-status-events"></a><span data-ttu-id="f8764-146">注文ステータスイベント</span><span class="sxs-lookup"><span data-stu-id="f8764-146">Purchase status events</span></span>

<span data-ttu-id="f8764-147">注文ステータスは銀行イベントと類似しています。</span><span class="sxs-lookup"><span data-stu-id="f8764-147">Purchase status events resemble bank events.</span></span> <span data-ttu-id="f8764-148">注文が Commerce の銀行オフィスで作成された後、信号が Fraud Protection に発信され、注文が正常に作成されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="f8764-148">After an order is created in the Commerce back office, a signal is sent to Fraud Protection to indicate that the order was successfully created.</span></span> <span data-ttu-id="f8764-149">銀行イベントと購入ステータスは両方とも情報を提供するイベントです。</span><span class="sxs-lookup"><span data-stu-id="f8764-149">Both bank events and purchase status events are informational events.</span></span> <span data-ttu-id="f8764-150">従って、Fraud Protection からの回答はありません。</span><span class="sxs-lookup"><span data-stu-id="f8764-150">Therefore, no response is expected from Fraud Protection.</span></span>

### <a name="availability"></a><span data-ttu-id="f8764-151">在庫状態</span><span class="sxs-lookup"><span data-stu-id="f8764-151">Availability</span></span>

<span data-ttu-id="f8764-152">Dynamics 365 Retail バージョン 10.0.8 では、Retail には Fraud Protection 統合のバック オフィス設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f8764-152">As of Dynamics 365 Retail version 10.0.8, Retail includes the back-office setup for Fraud Protection integration.</span></span> <span data-ttu-id="f8764-153">ただし、標準のフル統合には Commerce に含まれている店舗が必要ですが、Commerce は現在パブリック プレビューをしています。</span><span class="sxs-lookup"><span data-stu-id="f8764-153">However, the full out-of-box integration requires the storefront that is included in Commerce, and Commerce is currently in public preview.</span></span> <span data-ttu-id="f8764-154">Commerce が一般に利用可能となりましたら、既存の Retail の顧客はそちらに更新できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f8764-154">When Commerce becomes generally available, existing Retail customers will be able to update to it.</span></span> <span data-ttu-id="f8764-155">詳細については、[Dynamics 365 Commerce のランディング ページ](https://dynamics.microsoft.com/commerce/overview/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8764-155">For more information, visit the [Dynamics 365 Commerce landing page](https://dynamics.microsoft.com/commerce/overview/).</span></span>

#### <a name="setup"></a><span data-ttu-id="f8764-156">セットアップ</span><span class="sxs-lookup"><span data-stu-id="f8764-156">Setup</span></span>

<span data-ttu-id="f8764-157">標準の購入保護統合には、Fraud Protection 環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="f8764-157">The out-of-box purchase protection integration requires a Fraud Protection environment.</span></span> <span data-ttu-id="f8764-158">Fraud Protection を設定するには、 Dynamics 365 の営業担当者からの [コールバックを要求してください](https://dynamics.microsoft.com/get-started/?appname=fraudprotection)。</span><span class="sxs-lookup"><span data-stu-id="f8764-158">To set up Fraud Protection, [request a callback](https://dynamics.microsoft.com/get-started/?appname=fraudprotection) from a Dynamics 365 sales representative.</span></span>

<span data-ttu-id="f8764-159">マーチャントの Fraud Protection 環境が利用可能になると、購入保護設定が構成され、Commerce バック オフィスで設定を続行できます。</span><span class="sxs-lookup"><span data-stu-id="f8764-159">After the merchant's Fraud Protection environment is available, and purchase protection settings have been configured, the setup can continue in the Commerce back office.</span></span>

##### <a name="key-vault-setup"></a><span data-ttu-id="f8764-160">Key Vault の設定</span><span class="sxs-lookup"><span data-stu-id="f8764-160">Key Vault setup</span></span>

<span data-ttu-id="f8764-161">統合設定では、Commerce が Fraud Protection と通信して、購入保護の結果を得る際にシークレットを使用することが求められます。</span><span class="sxs-lookup"><span data-stu-id="f8764-161">The integration setup requires that a secret be used when Commerce communicates with Fraud Protection to get a purchase protection result.</span></span> <span data-ttu-id="f8764-162">このシークレットは  Azure Key Vault クライアントの使用によって保存されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f8764-162">That secret must be stored by using an Azure Key Vault client.</span></span> <span data-ttu-id="f8764-163">位置情報検出を設定する方法の詳細については [位置情報検出の設定](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8764-163">For information about how to set up a Key Vault client, see [Setting up Azure Key Vault Client](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).</span></span>

<span data-ttu-id="f8764-164">Key Vault に保管されている Fraud Protection 証明書は、Commerce のバック オフィスにある Key Vault パラメーターによって参照される場合のみ参照されることができます。</span><span class="sxs-lookup"><span data-stu-id="f8764-164">The Fraud Protection certificate that is stored in Key Vault can be referenced only if it's referenced by Key Vault parameters in the Commerce back office.</span></span> <span data-ttu-id="f8764-165">Key Vault パラメーターを設定するには、Commerce で、**Retail と Commerce** \> **本社の設定** \> **パラメーター** \> **Key Vault パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8764-165">To set up Key Vault parameters, go to **Retail and Commerce** \> **Headquarters setup** \> **Parameters** \> **Key Vault parameters** in Commerce.</span></span>

<span data-ttu-id="f8764-166">次に、Fraud Protection シークレットを補完するために使用される Key Vault URL を選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8764-166">Next, select the Key Vault URL that is used to store the Fraud Protection secret, and select **Add**.</span></span> <span data-ttu-id="f8764-167">その後、購入保護評価のために注文を送る際、Commerce を承認するために使用される、Key Vault シークレットの名前、説明、パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="f8764-167">Then specify the name, description, and path of the Key Vault secret that is used to authenticate Commerce when it sends orders for purchase protection assessment.</span></span>

##### <a name="retail-parameters-setup"></a><span data-ttu-id="f8764-168">Retail のパラメーター設定</span><span class="sxs-lookup"><span data-stu-id="f8764-168">Retail parameters setup</span></span>

1. <span data-ttu-id="f8764-169">**Retail と Commerce** \> **本社の設定** \> **パラメーター** \> **Retail パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8764-169">Go to **Retail and Commerce** \> **Headquarters setup** \> **Parameters** \> **Retail parameters**.</span></span>
2. <span data-ttu-id="f8764-170">**Dynamics Fraud Protection** タブで、**Dynamics Fraud Protection 統合を有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8764-170">On the **Dynamics Fraud Protection** tab, set the **Enable Dynamics Fraud Protection integration** option to **Yes**.</span></span>
3. <span data-ttu-id="f8764-171">**構成** ファストタブで、Azure Active Directory (Azure AD) クライアント ID を追加し、その後、前に構成した Key Vault シークレットの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8764-171">On the **Configuration** FastTab, add the Azure Active Directory (Azure AD) client ID, and then select the name of the Key Vault secret that you configured earlier.</span></span>

    <span data-ttu-id="f8764-172">規定では、**評価の種類** フィールドは **評価** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8764-172">By default, the **Assessment type** field is set to **Evaluate**.</span></span> <span data-ttu-id="f8764-173">この場合は、Fraud Protection は不正の注文を従順にチェックしますが、積極的に注文の拒否はしません。</span><span class="sxs-lookup"><span data-stu-id="f8764-173">In this case, Fraud Protection will passively check orders for fraud but won't actively reject orders.</span></span> <span data-ttu-id="f8764-174">従って、マーチャントは Fraud Protection のリスク評価を自分たちの不正ツールと比較をし、承諾レートで Fraud Protection の影響を理解することができます。</span><span class="sxs-lookup"><span data-stu-id="f8764-174">Therefore, merchants can compare Fraud Protection risk assessments with their current fraud tools to understand the impact of Fraud Protection on acceptance rates.</span></span>

    <span data-ttu-id="f8764-175">または、**評価の種類** フィールドは **保護** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8764-175">Alternatively, the **Assessment type** field can be set to **Protect**.</span></span> <span data-ttu-id="f8764-176">この場合、Fraud Protection は「拒否」評価を返答し、承認に送信またはバック オフィスで作成される前に、不正な注文は中止されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-176">In this case, Fraud Protection will return "Reject" assessments, and fraudulent orders will be terminated before they are sent for authorization or created in the back office.</span></span>

4. <span data-ttu-id="f8764-177">**Dynamics Fraud Protection エンドポイント URL** フィールドは設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8764-177">The **Dynamics Fraud Protection endpoint URL** field must be set.</span></span> <span data-ttu-id="f8764-178">この URL は Fraud Protection から提供され、ユーザー受け入れテスト (UAT) と運用環境に渡り異なります。</span><span class="sxs-lookup"><span data-stu-id="f8764-178">This URL is provided by Fraud Protection and will vary across user acceptance testing (UAT) and production environments.</span></span>

![Retail パラメーターでの Fraud Protection 設定](../media/Payments/DFPSetupParams.png)

> [!NOTE]
> <span data-ttu-id="f8764-180">Key Vault 設定と Fraud Protection 設定は会社固有です。</span><span class="sxs-lookup"><span data-stu-id="f8764-180">The Key Vault and Fraud Protection settings are company-specific.</span></span> <span data-ttu-id="f8764-181">Fraud Protection を運用環境に対して有効にするには、ユーザーインターフェイス (UI) を通して Azure AD クライアント ID は入力しません。</span><span class="sxs-lookup"><span data-stu-id="f8764-181">To enable Fraud Protection for production environments, you don't enter the Azure AD client ID through the user interface (UI).</span></span> <span data-ttu-id="f8764-182">その代わり、[サービス要求](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team) を作成および提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8764-182">Instead, you must create and submit a [service request](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team).</span></span> <span data-ttu-id="f8764-183">要求のタイトルには、この要求が運用版 Commerce または Retail のための Fraud Protection 購入保護を構成するためであることを明確に示します。</span><span class="sxs-lookup"><span data-stu-id="f8764-183">In the title of your request, clearly indicate that the request is to configure Fraud Protection purchase protection for a production Commerce or Retail environment.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f8764-184">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="f8764-184">Privacy notice</span></span>

<span data-ttu-id="f8764-185">この機能を有効にする場合、データの一部はその他の Microsoft オンライン サービスと共有されます。</span><span class="sxs-lookup"><span data-stu-id="f8764-185">When you enable this feature, some of your data is shared with other Microsoft online services.</span></span> <span data-ttu-id="f8764-186">このデータには、支払い、クレジット、返却、トランザクション状況や個人データについての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f8764-186">This data includes information about payments, credit, returns, and transaction status, or personal data.</span></span> <span data-ttu-id="f8764-187">Fraud Protection の購入保護評価は、Retail または Commerce のオンラインサービスによって並べ替えはされません。</span><span class="sxs-lookup"><span data-stu-id="f8764-187">Fraud Protection purchase protection assessments aren't stored by the Retail or Commerce online services.</span></span>

<span data-ttu-id="f8764-188">Microsoft にとってお客様のプライバシーは重要です。</span><span class="sxs-lookup"><span data-stu-id="f8764-188">Your privacy is important to Microsoft.</span></span> <span data-ttu-id="f8764-189">詳細については、[Microsoft のプライバシーに関する声明](https://go.microsoft.com/fwlink/?LinkId=521839) をお読みください。</span><span class="sxs-lookup"><span data-stu-id="f8764-189">To learn more, read the [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

## <a name="related-articles"></a><span data-ttu-id="f8764-190">関連記事</span><span class="sxs-lookup"><span data-stu-id="f8764-190">Related articles</span></span>

- [<span data-ttu-id="f8764-191">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f8764-191">Payments FAQ</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [<span data-ttu-id="f8764-192">Dynamics 365 支払データの使用</span><span class="sxs-lookup"><span data-stu-id="f8764-192">Dynamics 365 payment data use</span></span>](https://docs.microsoft.com/dynamics365/retail/payment-connector-data-fields)
