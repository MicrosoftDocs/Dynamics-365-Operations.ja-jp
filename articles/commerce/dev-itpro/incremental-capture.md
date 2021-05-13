---
title: 増分支払の取得
description: このトピックでは、Dynamics 365 Commerce での注文請求の一部として増分取得に対するすぐに使えるサポートについて説明します。
author: rubendel
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 56a60e88293d1c75ceb04b435c3395b23f91eb81
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937080"
---
# <a name="incremental-capture-for-order-invoicing"></a><span data-ttu-id="e4121-103">注文請求の増分取得</span><span class="sxs-lookup"><span data-stu-id="e4121-103">Incremental capture for order invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4121-104">このトピックでは、Dynamics 365 Commerce での注文請求の一部として増分取得に対するすぐに使えるサポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e4121-104">This topic describes out-of-box support for incremental capture as part of order invoicing in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e4121-105">また、Adyen 向け Dynamics 365 Payment Connector の増分取得を有効にする方法と、支払ソフトウェア開発キット (SDK) を使用してサード パーティーの支払コネクタに増分取得を追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="e4121-105">This topic also describes how to enable incremental capture for the Dynamics 365 Payment Connector for Adyen, and how incremental capture can be added to third-party payment connectors using the payments software development kit (SDK).</span></span>

<span data-ttu-id="e4121-106">増分取得が有効になると、複数の請求書を使用して長期にわたって履行される注文は、複数の請求書および取得済支払の元の承認を参照します。</span><span class="sxs-lookup"><span data-stu-id="e4121-106">When incremental capture is enabled, orders that are fulfilled over time with multiple invoices will reference the original authorization for multiple invoices and captured payments.</span></span> <span data-ttu-id="e4121-107">これは、複数の請求書を使用して注文を履行するレガシ サポートとは対照的で、注文の一部が履行され、未払残高が変更されるたびに新しい承認が取得されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-107">This contrasts with legacy support for fulfilling orders with multiple invoices, which causes a new authorization to be obtained every time a portion of the order is fulfilled and the balance due changes.</span></span>

<span data-ttu-id="e4121-108">増分取得は、POS および Commerce 本社から注文が履行されたときに、Adyen 向け Dynamics 365 Payment Connector 使用してすぐにサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e4121-108">Incremental capture is supported out-of-box with the Dynamics 365 Payment Connector for Adyen when orders are fulfilled from the POS and Commerce headquarters.</span></span> 

<span data-ttu-id="e4121-109">多くの加盟店は、注文を複数の出荷で処理しています。</span><span class="sxs-lookup"><span data-stu-id="e4121-109">Many merchants fulfill orders in multiple shipments.</span></span> <span data-ttu-id="e4121-110">既定では、複数の出荷に履行される注文に対してクレジット カード支払を処理するための最初から用意されているプロセスは、出荷が請求されると支払を取得し、出荷が必要な残りの品目の残高に新しい支払認証を取得します。</span><span class="sxs-lookup"><span data-stu-id="e4121-110">By default, the out-of-box process for handling credit card payments for orders that are fulfilled over multiple shipments is to capture payments as those shipments are invoiced and then get a new payment authorization for the balance due for the remaining items that must be shipped.</span></span> <span data-ttu-id="e4121-111">この処理によって、支払取得が支払プロセッサ全体で一貫してサポートされることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-111">This process ensures that payment capture can be consistently supported across payment processors.</span></span> 

<span data-ttu-id="e4121-112">ただし、いくつかの欠点もあります。</span><span class="sxs-lookup"><span data-stu-id="e4121-112">However, there are also some downsides.</span></span> <span data-ttu-id="e4121-113">たとえば、承認が部分的に取得された後、未払い残高に対して新しい承認が作成されると、古い承認と新しい承認が重複する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-113">For example, when an authorization is partially captured, and a new authorization is then created for the balance due, the old authorization and new authorization might overlap.</span></span> <span data-ttu-id="e4121-114">この場合、注文合計を超えるオープン承認が顧客の支払カードに対して表示される可能性があり、その結果、クレジット カードで使用可能なオープン残高を超える承認が発生したり、カード発行者が不正の疑いがあるためにカードの処理をブロックしたりする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-114">In this case, open authorizations that exceed the order total might appear against customer payment cards, possibly resulting in authorizations that exceed open balances that are available for credit cards, or card issuers blocking cards from being processed due to suspicion of fraud.</span></span>

<span data-ttu-id="e4121-115">これらの問題に対処するために、Adyen 向け Dynamics 365 Payment Connector および支払 SDKに対して増分取得サポートが導入されています。</span><span class="sxs-lookup"><span data-stu-id="e4121-115">To address these issues, incremental capture support has been introduced for the Dynamics 365 Payment Connector for Adyen and payments SDK.</span></span> <span data-ttu-id="e4121-116">プロセッサが増分取得をサポートしている場合、支払コネクタを更新して、注文処理の過程で 1 つの承認に対して複数回取得できます。</span><span class="sxs-lookup"><span data-stu-id="e4121-116">If a processor supports incremental capture, payment connectors can be updated to capture against a single authorization multiple times over the course of order fulfillment.</span></span> 

<span data-ttu-id="e4121-117">次の図は、1 つの承認に対して複数回の取得が行われる場合の、さまざまな支払取得フレームワークの違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="e4121-117">The following illustration shows the difference between the different payment capture frameworks when multiple captures are done against a single authorization.</span></span>

![現在の支払取得フレームワーク対増分取得](../dev-itpro/media/INC_DIFF.png)

<span data-ttu-id="e4121-119">本社請求 (つまり、本社での注文処理の一部として発生する請求) の増分取得のサポートは、Commerce バージョン 10.0.13 の支払 SDK に最初に追加されました。</span><span class="sxs-lookup"><span data-stu-id="e4121-119">Incremental capture support for headquarters invoicing (in other words, any invoicing that occurs as part of order fulfillment in headquarters) was first added to the payments SDK in Commerce version 10.0.13.</span></span> <span data-ttu-id="e4121-120">Commerce バージョン 10.0.18 では、SDK による増分取得サポートが本社の外部のチャネルに拡張されています。</span><span class="sxs-lookup"><span data-stu-id="e4121-120">In Commerce version 10.0.18, incremental capture support through the SDK has been extended to channels outside of headquarters.</span></span> <span data-ttu-id="e4121-121">店舗、Modern POS、およびコール センターでは、この拡張サポートによって、新しい注文に対して作成された承認を **SupportsMultipleCaptures** としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="e4121-121">For the storefront, Modern POS, and call center this extended support means that authorizations created for new orders can be marked as **SupportsMultipleCaptures**.</span></span> <span data-ttu-id="e4121-122">これらの注文に対して本社または Modern POS で後で請求を行う場合、支払が取得され、以降の請求書で支払が取得されるときに元の承認が保持および参照されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-122">When those orders are later invoiced in headquarters or Modern POS, payments can be captured and the original authorization will be retained and referenced when payments are captured for subsequent invoices.</span></span> 

## <a name="enable-incremental-capture"></a><span data-ttu-id="e4121-123">増分取得を有効にする</span><span class="sxs-lookup"><span data-stu-id="e4121-123">Enable incremental capture</span></span>

### <a name="prerequisite-features"></a><span data-ttu-id="e4121-124">前提条件となる機能</span><span class="sxs-lookup"><span data-stu-id="e4121-124">Prerequisite features</span></span>

<span data-ttu-id="e4121-125">増分取得を有効にする前に、次の機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-125">The following features must be enabled prior to enabling incremental capture.</span></span> 

| <span data-ttu-id="e4121-126">機能名</span><span class="sxs-lookup"><span data-stu-id="e4121-126">Feature name</span></span> | <span data-ttu-id="e4121-127">説明</span><span class="sxs-lookup"><span data-stu-id="e4121-127">Description</span></span> |
|---|---|
| <span data-ttu-id="e4121-128">コマースの統一支払転記仕訳帳の既定値</span><span class="sxs-lookup"><span data-stu-id="e4121-128">Unified payment posting journal defaults for Commerce</span></span> | <span data-ttu-id="e4121-129">この機能は、コールセンター、POS、または電子商取引チャネルを介して作成された注文に対して、ビジネス ロジックが顧客支払仕訳帳と顧客返金仕訳帳を作成する方法を変更します。</span><span class="sxs-lookup"><span data-stu-id="e4121-129">This feature changes the way that business logic creates customer payment and customer refund payment journals for orders that are created through the call center, POS, or e-commerce channel.</span></span> |
| <span data-ttu-id="e4121-130">オムニ チャネル支払</span><span class="sxs-lookup"><span data-stu-id="e4121-130">Omni-channel payments</span></span> | <span data-ttu-id="e4121-131">この機能を使用すると、「オンラインで購入し、店舗で受け取る」 (BOPIS) などのオムニチャネルの決済シナリオを有効化できます。</span><span class="sxs-lookup"><span data-stu-id="e4121-131">This feature enables omni-channel payment scenarios such as buy online, pick up in store (BOPIS).</span></span> <span data-ttu-id="e4121-132">詳細については、[オムニチャネル決済の概要](../omni-channel-payments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4121-132">For more information, see [Omni-channel payments overview](../omni-channel-payments.md).</span></span> |  
| <span data-ttu-id="e4121-133">請求に対する支払保護の重複</span><span class="sxs-lookup"><span data-stu-id="e4121-133">Duplicate payment protection on invoicing</span></span> | <span data-ttu-id="e4121-134">この機能は、請求書発行のシナリオで重複した決済の保護を可能にします。</span><span class="sxs-lookup"><span data-stu-id="e4121-134">This feature enables duplicate payment protection for invoicing scenarios.</span></span> <span data-ttu-id="e4121-135">Commerce の決済機能は、請求書発行シナリオのカスタマイズに影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-135">Commerce payment functionality may affect customizations in invoicing scenarios.</span></span> <span data-ttu-id="e4121-136">組織に請求書発行のカスタマイズがある場合は、運用環境で Commerce の決済機能を有効にする前に、それらがリファクターされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e4121-136">If your organization has invoicing customizations, make sure that they are refactored before you turn on Commerce payment functionality in production environments.</span></span> | 
| <span data-ttu-id="e4121-137">複数のキャプチャの払戻を有効にする</span><span class="sxs-lookup"><span data-stu-id="e4121-137">Enable refunds over multiple captures</span></span> | <span data-ttu-id="e4121-138">この機能を使用すると、注文に対して複数のリンクされた払戻を実行する機能が改善されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-138">This functionality improves that capability to do multiple linked refunds against an order.</span></span> |
| <span data-ttu-id="e4121-139">認証の有効期限が切れたクレジットカードの決済明細行を手動で無効化する</span><span class="sxs-lookup"><span data-stu-id="e4121-139">Enable manual void of expired credit card payment lines when authorizations are expired</span></span> | <span data-ttu-id="e4121-140">この機能により、決済明細行の期限が切れた場合に手動で削除することができ、承認を更新しません。</span><span class="sxs-lookup"><span data-stu-id="e4121-140">This feature adds support for manual deletion of payment lines if they expire and the authorization cannot be refreshed.</span></span> |
| <span data-ttu-id="e4121-141">オムニチャネル Commerce 注文支払。</span><span class="sxs-lookup"><span data-stu-id="e4121-141">Omni-channel Commerce order payments.</span></span> | <span data-ttu-id="e4121-142">この機能により、チャネル間の支払を合理化し、コール センター内で店舗および POS の注文の支払を編集できます。</span><span class="sxs-lookup"><span data-stu-id="e4121-142">This feature rationalizes payments across channels and enables editing of payments for storefront and POS orders within the call center.</span></span> <span data-ttu-id="e4121-143">前述の機能はこの機能の前提条件なので、この機能を最後に有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-143">Previously listed features are prerequisites for this feature, so this feature should be enabled last.</span></span> <span data-ttu-id="e4121-144">詳細については、[オムニチャネル Commerce 注文支払](commerce-payments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e4121-144">For more information, see [Omni-channel Commerce order payments](commerce-payments.md).</span></span> |

### <a name="enable-the-extensibility-to-support-incremental-credit-card-capture-feature"></a><span data-ttu-id="e4121-145">「クレジット カードの増分取得をサポートする機能拡張」機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="e4121-145">Enable the "Extensibility to support incremental credit card capture" feature</span></span>

<span data-ttu-id="e4121-146">この機能は当初、支払 SDK を介して請求する本社の増分取得のために導入されたもので、Adyen 向け Dynamics 365 Payment Connector およびすべてのチャネルを介した増分取得のサポートを有効にするために拡張されました。</span><span class="sxs-lookup"><span data-stu-id="e4121-146">This feature was originally introduced for incremental capture for headquarters invoicing through the payments SDK and has been augmented to also enable incremental capture support through the Dynamics 365 Payment Connector for Adyen and all channels.</span></span> 

<span data-ttu-id="e4121-147">Commerce 本社で「クレジット カードの増分取得をサポートする機能拡張」機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e4121-147">To enable the "Extensibility to support incremental credit card capture" feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e4121-148">**システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4121-148">Go to **System administration \> Workspaces \> Feature management**.</span></span> 
1. <span data-ttu-id="e4121-149">**すべて** タブを選択すると、使用可能なすべての機能が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-149">Select the **All** tab to show all available features.</span></span>
1. <span data-ttu-id="e4121-150">**クレジット カードの増分取得をサポートする機能拡張** を検索します。</span><span class="sxs-lookup"><span data-stu-id="e4121-150">Search for **Extensibility to support incremental credit card capture**.</span></span>
1. <span data-ttu-id="e4121-151">機能を選択し、**今すぐ有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4121-151">Select the feature and then select **Enable now**.</span></span>

### <a name="enable-incremental-capture-for-the-dynamics-365-payment-connector-for-adyen"></a><span data-ttu-id="e4121-152">Adyen 向け Dynamics 365 Payment Connector で増分取得を有効にする</span><span class="sxs-lookup"><span data-stu-id="e4121-152">Enable incremental capture for the Dynamics 365 Payment Connector for Adyen</span></span>

<span data-ttu-id="e4121-153">「クレジット カードの増分取得をサポートする機能拡張」機能を有効にすることに加え、Adyen 向け Dynamics 365 Payment Connector の商社プロパティの **要求保護を有効にする** プロパティの値も、コネクタが使用されるチャネルごとに **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-153">In addition to enabling the "Extensibility to support incremental credit card capture" feature, the value of the **Enable Request Protection** property must also be set to **True** in the Dynamics 365 Payment Connector for Adyen merchant properties for every channel where the connector is used.</span></span> <span data-ttu-id="e4121-154">値が **False** または空白の場合増分取得はコネクタに対して有効になりません。</span><span class="sxs-lookup"><span data-stu-id="e4121-154">If the value is set to **False** or left blank, incremental capture will not be enabled for the connector.</span></span> <span data-ttu-id="e4121-155">プロパティが **True** に設定されている場合、重複する要求を防ぐため、追跡 ID が支払プロバイダーへの要求に追加されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-155">When the property is set to **True**, a tracking ID is added to requests to the payment provider to prevent duplicate requests.</span></span> <span data-ttu-id="e4121-156">サード パーティ支払コネクタに対する追跡 ID サポートについては、次の「[サード パーティ支払コネクタ用増分取得の取得](#uptake-incremental-capture-for-third-party-payment-connectors)」で説明されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-156">Tracking ID support for third-party payment connectors is explained in the [Uptake incremental capture for third-party payment connectors](#uptake-incremental-capture-for-third-party-payment-connectors) section below.</span></span>

<span data-ttu-id="e4121-157">一部の支払方法では、増分取得がサポートされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-157">Some payment methods do not support incremental capture.</span></span> <span data-ttu-id="e4121-158">これらの支払方法は、Adyen 向け Dynamics 365 Payment Connector のマーチャント プロパティの **増分取得以外の支払方法** フィールドで構成できます。</span><span class="sxs-lookup"><span data-stu-id="e4121-158">Those payment methods can be configured in the **Non incremental capture payment methods** field of the Dynamics 365 Payment Connector for Adyen merchant properties.</span></span> <span data-ttu-id="e4121-159">このフィールドに設定する値は、Adyen が承認応答でカード タイプを識別するために使用する「支払方法バリアント/カード タイプ」文字列と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-159">The value set in this field should match the "Payment Method Variant/Card type" string used by Adyen to identify card types in authorization responses.</span></span> <span data-ttu-id="e4121-160">支払方法バリアント文字列は、Adyen の [PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) にあります。</span><span class="sxs-lookup"><span data-stu-id="e4121-160">The payment method variant strings can be found in Adyen on the [PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant).</span></span> <span data-ttu-id="e4121-161">増分取得を除外する必要がある複数のカード タイプがある場合は、セミコロンで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-161">If there are multiple card types that should be exempt from incremental capture, they should be separated by semicolons.</span></span> 

<span data-ttu-id="e4121-162">増分取得をサポートしない支払方法バリアントの例の 1 つが Interac です。</span><span class="sxs-lookup"><span data-stu-id="e4121-162">One example of a payment method variant that does not support incremental capture is Interac.</span></span> <span data-ttu-id="e4121-163">Adyen のドキュメントでは、Interac 支払方法バリアントに対して一覧表示される文字列は **interac** です。</span><span class="sxs-lookup"><span data-stu-id="e4121-163">In the Adyen documentation, the string listed for the Interac payment method variant is **interac**.</span></span> <span data-ttu-id="e4121-164">Interac を受け入れるカナダのマーチャントに対して支払サービスが構成されている場合は、この支払方法バリアントをコネクタのマーチャント プロパティの「増分取得以外の支払方法」のリストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-164">If payment services are being configured for a Canadian merchant that accepts Interac, this payment method variant should be added to the list of "Non incremental capture payment methods" in the connector merchant properties.</span></span>  

<span data-ttu-id="e4121-165">Adyen 向け Dynamics 365 Payment Connector の増分取得を有効にしているマーチャントは、マーチャント口座で **allowMultiplePartialCapture** フラグが **はい** に設定されていることを確認するため、Adyen にも連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-165">Merchants enabling incremental capture for the Dynamics 365 Payment Connector for Adyen should also contact Adyen to ensure that the **allowMultiplePartialCapture** flag set to **Yes** on their merchant account.</span></span> <span data-ttu-id="e4121-166">このフラグがマーチャント口座レベルで有効になっていない場合、請求時の取得ロジックは、サポートされる従来のフローに戻ります。</span><span class="sxs-lookup"><span data-stu-id="e4121-166">If this flag is not enabled at the merchant account level, the capture logic at the time of invoicing will fall back to legacy supported flows.</span></span> 

## <a name="uptake-incremental-capture-for-third-party-payment-connectors"></a><span data-ttu-id="e4121-167">サード パーティ支払コネクタ用の増分取得を取得する</span><span class="sxs-lookup"><span data-stu-id="e4121-167">Uptake incremental capture for third-party payment connectors</span></span>

<span data-ttu-id="e4121-168">サード パーティ支払コネクタの本社請求の一部として増分取得のサポートを取り込み、すべてのチャネルで増分取得をサポートするには、Commerce バージョン 10.0.18 で提供されている支払 SDK にアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-168">To uptake support for incremental capture as part of headquarters invoicing for third-party payment connectors, and to support incremental capture across all channels, you must upgrade to the payments SDK that is provided in Commerce version 10.0.18.</span></span>

### <a name="ipaymentreferenceprovider"></a><span data-ttu-id="e4121-169">IPaymentReferenceProvider</span><span class="sxs-lookup"><span data-stu-id="e4121-169">IPaymentReferenceProvider</span></span>

<span data-ttu-id="e4121-170">このバージョンの支払 SDK は、**IPaymentReferenceProvider** インターフェイスを追加します。</span><span class="sxs-lookup"><span data-stu-id="e4121-170">This version of the payment SDK adds the **IPaymentReferenceProvider** interface.</span></span> <span data-ttu-id="e4121-171">このインターフェイスでは、各要求と応答の **PaymentTrackingID** 値の使用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4121-171">This interface supports using a **PaymentTrackingID** value for each request and response.</span></span> <span data-ttu-id="e4121-172">**PaymentTrackingID** 値は、支払要求を追跡するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4121-172">The **PaymentTrackingID** value can be used to track payment requests.</span></span> <span data-ttu-id="e4121-173">また、バックオフィスの請求書発行要求とプロセッサの間で、重複した要求が再送信前に発見されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-173">It also ensures that, between back-office invoicing requests and the processor, duplicate requests can be caught before they are re-sent.</span></span> <span data-ttu-id="e4121-174">このようにして、重複する支払を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="e4121-174">In this way, it helps prevent duplicate payments.</span></span>

<span data-ttu-id="e4121-175">次に、支払 SDK の SampleConnector.cs ファイルのサンプル実装を示します。</span><span class="sxs-lookup"><span data-stu-id="e4121-175">Here is a sample implementation from the SampleConnector.cs file in the payments SDK.</span></span>

```xml
#region ITrackingSupport
/// <summary>
/// Get the payment provider reference to safeguard against duplicate requests.
/// </summary>
/// <param name="command">The payment operation that will use the tracking ID.</param>
/// <param name="amount">The payment transaction amount.</param>
/// <returns>Returns the PaymentTransactionReferenceData.</returns>
/// <remarks>List of supported commands can be seen in the constants defined in <see cref="Microsoft.Dynamics.Retail.PaymentSDK.Portable.Constants.SupportedCorrelationCommands"/></remarks>
public PaymentTransactionReferenceData GetPaymentReferenceData(string command, decimal amount)
{
    PaymentTransactionReferenceData paymentTransactionReferenceData = new PaymentTransactionReferenceData();
    paymentTransactionReferenceData.Amount = amount;
    paymentTransactionReferenceData.Command = command;
    paymentTransactionReferenceData.IdFromConnector = Guid.NewGuid().ToString();
    paymentTransactionReferenceData.InitiatedDate = DateTime.UtcNow;
    return paymentTransactionReferenceData;
}
#endregion
```

<span data-ttu-id="e4121-176">支払 SDK の AuthorizeRequest.cs ファイルの次のサンプルでは、**PaymentTrackingID** 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4121-176">The following sample from the AuthorizeRequest.cs file in the payments SDK uses a **PaymentTrackingID** value.</span></span>

```xml
authorizeRequest.PaymentTrackingId = PaymentUtilities.GetPropertyStringValue(
    hashtable,
    GenericNamespace.TransactionData,
    TransactionDataProperties.PaymentTrackingId);
```

### <a name="support-for-multiple-captures"></a><span data-ttu-id="e4121-177">複数回の取得のサポート</span><span class="sxs-lookup"><span data-stu-id="e4121-177">Support for multiple captures</span></span>

<span data-ttu-id="e4121-178">支払プロセッサが複数回の取得をサポートしている場合、コネクタからの承認応答の **SupportsMultipleCaptures** プロパティは **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e4121-178">If a payment processor supports multiple captures, the **SupportsMultipleCaptures** property for authorization responses from the connector should be set to **True**.</span></span> <span data-ttu-id="e4121-179">このプロパティが **False** に設定されている場合、または指定されていない場合、その承認は増分取得の対象にはなりません。</span><span class="sxs-lookup"><span data-stu-id="e4121-179">If the property is set to **False**, or if it isn't provided, the authorization won't be eligible for incremental capture.</span></span> <span data-ttu-id="e4121-180">この場合、請求後に新しい未払い残高があると、新しい承認が取得されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-180">In this case, if there is a new balance due after invoicing, a new authorization will be obtained.</span></span> 

<span data-ttu-id="e4121-181">次に、支払 SDK の AuthorizationResponseProperties.cs ファイルのサンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="e4121-181">Here is a sample from the AuthorizationResponseProperties.cs file in the payments SDK.</span></span>

```xml
/// <summary>
/// Gets the SupportsMultipleCaptures property.
/// </summary>
public static string SupportsMultipleCaptures
{
    get { return "SupportsMultipleCaptures"; }
}
```

<span data-ttu-id="e4121-182">バックオフィス請求プロセスが複数回の取得に対して有効な承認に対して取得すると、取得された合計金額が追跡されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-182">As back-office invoicing processes captures against authorizations that are enabled for multiple captures, the total captured amount is tracked.</span></span> <span data-ttu-id="e4121-183">取得要求は、完全に取得されるまで、元の承認を引き続き参照します。</span><span class="sxs-lookup"><span data-stu-id="e4121-183">Capture requests continue to reference the original authorization until it's fully captured.</span></span>

<span data-ttu-id="e4121-184">売掛金勘定パラメータに従って期限切れになる承認は、増分取得の対象にはなりません。</span><span class="sxs-lookup"><span data-stu-id="e4121-184">Authorizations that are expired according to Accounts receivable parameters aren't eligible for incremental capture.</span></span> 

<span data-ttu-id="e4121-185">**SupportsMultipleCaptures** プロパティはグローバルではありません。</span><span class="sxs-lookup"><span data-stu-id="e4121-185">The **SupportsMultipleCaptures** property isn't global.</span></span> <span data-ttu-id="e4121-186">これは承認に固有です。</span><span class="sxs-lookup"><span data-stu-id="e4121-186">It's specific to the authorization.</span></span> <span data-ttu-id="e4121-187">環境には、増分取得をサポートするコネクタと、それをサポートしないコネクタの両方がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e4121-187">An environment might have both connectors that support incremental capture and connectors that don't support it.</span></span>

## <a name="incremental-capture-user-experience"></a><span data-ttu-id="e4121-188">増分取得のユーザー エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="e4121-188">Incremental capture user experience</span></span>

<span data-ttu-id="e4121-189">増分取得のユーザー エクスペリエンスは、増分取得が有効になっていない場合のユーザー エクスペリエンスと変わりません。</span><span class="sxs-lookup"><span data-stu-id="e4121-189">The incremental capture user experience is no different from the user experience when incremental capture is not enabled.</span></span> <span data-ttu-id="e4121-190">重要な違いは、増分取得が有効な場合に元の承認が有効な場合、注文が部分的に請求された後に新しい承認を取得できない点です。</span><span class="sxs-lookup"><span data-stu-id="e4121-190">The key difference is that when incremental capture is enabled, if the original authorization is still valid, a new authorization will not be obtained after an order is partially invoiced.</span></span> <span data-ttu-id="e4121-191">代わりに、既存の承認が保持され、後続の支払の取得に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-191">Instead, the existing authorization will be retained and used for subsequent payment captures.</span></span> 

<span data-ttu-id="e4121-192">本社またはプロセッサのポータルで支払の問題を調査しているユーザーの場合、承認と取得の比率が 1:1 である従来のフローとは対照的に、複数の支払取得がマップされた単一の承認を持つように、増分取得順序が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4121-192">For users investigating payment issues in headquarters or in their processor's portal, incremental capture orders will appear as having a single authorization with multiple payment captures mapped to it, as opposed to legacy flows where authorizations and captures would have a 1:1 ratio.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e4121-193">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e4121-193">Additional resources</span></span>

[<span data-ttu-id="e4121-194">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="e4121-194">Payments FAQ</span></span>](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[<span data-ttu-id="e4121-195">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="e4121-195">Dynamics 365 Payment Connector for Adyen</span></span>](adyen-connector.md?tabs=8-1-3)

[<span data-ttu-id="e4121-196">オムニチャネル Commerce 注文支払</span><span class="sxs-lookup"><span data-stu-id="e4121-196">Omni-channel Commerce order payments</span></span>](commerce-payments.md)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]