---
title: バックオフィスの請求の増分取得
description: このトピックでは、注文請求の一部として増分取得をサポートするために支払ソフトウェア開発キット (SDK) に対して行われた機能拡張について説明します。
author: rubendel
manager: annbe
ms.date: 7/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 0fbfec342567de56816989d17a2f8b4e816f1dca
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685399"
---
# <a name="incremental-capture-for-back-office-invoicing"></a><span data-ttu-id="c15c6-103">バックオフィスの請求の増分取得</span><span class="sxs-lookup"><span data-stu-id="c15c6-103">Incremental capture for back-office invoicing</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c15c6-104">このトピックでは、支払ソフトウェア開発キット (SDK) が注文請求の一部として増分取得をどのようにサポートするかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-104">This topic describes how the payments software development kit (SDK) supports incremental capture as part of order invoicing.</span></span> <span data-ttu-id="c15c6-105">増分取得では、支払処理は複数の請求書がある注文の履行をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c15c6-105">In incremental capture, payment processing supports fulfillment of an order that has multiple invoices.</span></span> <span data-ttu-id="c15c6-106">具体的には、請求書は注文に対して処理されるため、以前の支払取得が変更による残高の原因となった場合、新しい支払承認を取得する代わりに、支払取得要求が元の支払承認を参照します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-106">Specifically, as invoices are processed against the order, payment capture requests reference the original payment authorization instead of getting a new payment authorization when previous payment captures have caused the balance due to change.</span></span>

## <a name="overview"></a><span data-ttu-id="c15c6-107">概要</span><span class="sxs-lookup"><span data-stu-id="c15c6-107">Overview</span></span>

<span data-ttu-id="c15c6-108">多くの加盟店は、注文を複数の出荷で処理しています。</span><span class="sxs-lookup"><span data-stu-id="c15c6-108">Many merchants fulfill orders in multiple shipments.</span></span> <span data-ttu-id="c15c6-109">Microsoft Dynamics 365 Commerce バージョン 10.0.12 以前では、複数の出荷に履行される注文に対してクレジット カード支払を処理するための最初から用意されているプロセスは、出荷が請求されると支払を取得し、出荷が必要な残りの品目の残高に新しい支払認証を取得します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-109">In Microsoft Dynamics 365 Commerce version 10.0.12 and earlier, the out-of-box process for handling credit card payments for orders that are fulfilled over multiple shipments is to capture payments as those shipments are invoiced and then get a new payment authorization for the balance due for the remaining items that must be shipped.</span></span> <span data-ttu-id="c15c6-110">この処理によって、支払取得が支払プロセッサ全体で一貫してサポートされることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-110">This process ensures that payment capture can be consistently supported across payment processors.</span></span> <span data-ttu-id="c15c6-111">ただし、いくつかの欠点もあります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-111">However, it also has some downsides.</span></span> <span data-ttu-id="c15c6-112">具体的には、承認が部分的に取得された後、未払い残高に対して新しい承認が作成されると、古い承認と新しい承認が重複する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-112">Specifically, when an authorization is partially captured, and then a new authorization is created for the balance due, the old authorization and new authorization might overlap.</span></span> <span data-ttu-id="c15c6-113">この場合、顧客の支払カードに対して注文合計を超えるオープン承認が表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-113">In this case, open authorizations that exceed the order total might appear against customer payment cards.</span></span> <span data-ttu-id="c15c6-114">したがって、承認がクレジットカードで利用可能なオープン残高を超えたり、カード発行者が不正行為の疑いでカードの処理をブロックしたりする場合があります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-114">Therefore, authorizations might exceed open balances that are available for credit cards, or card issuers might block cards from being processed because of suspicion of fraud.</span></span>

<span data-ttu-id="c15c6-115">これらの問題に対処するために、Commerce バージョン 10.0.13 以降の支払 SDK には、バック オフィス支払取得に対する増分取得サポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c15c6-115">To address these issues, the payments SDK in Commerce version 10.0.13 and later includes incremental capture support for back-office payment captures.</span></span> <span data-ttu-id="c15c6-116">したがって、プロセッサが増分取得をサポートしている場合、支払コネクタを更新して、注文処理の過程で 1 つの認証に対して複数回取得できます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-116">Therefore, if a processor supports incremental capture, payment connectors can be updated to capture against a single authorization multiple times over the course of order fulfillment.</span></span> <span data-ttu-id="c15c6-117">次の図は、1 つの承認に対して複数回の取得が行われる場合の、さまざまな支払取得フレームワークの違いを示しています。</span><span class="sxs-lookup"><span data-stu-id="c15c6-117">The following illustration shows the difference between the different payment capture frameworks when multiple captures are done against a single authorization.</span></span>

![現在の支払取得フレームワーク対増分取得](../dev-itpro/media/INC_DIFF.png)

<span data-ttu-id="c15c6-119">Commerce バージョン 10.0.13 では、増分取得は、バック オフィス請求 (つまり、バック オフィスの注文処理の一部として発生するすべての請求) の一部としてサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c15c6-119">In Commerce version 10.0.13, incremental capture is supported as part of back-office invoicing (that is, any invoicing that occurs as part of order fulfillment in the back office).</span></span> <span data-ttu-id="c15c6-120">今後のリリースでは、販売時点管理 (POS) からの増分取得サポートが、最初から用意されている Adyen 支払コネクタに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-120">In a later release, support for incremental capture from the point of sale (POS) will be added to the out-of-box Adyen payment connector.</span></span>

## <a name="turn-on-incremental-capture-for-back-office-invoicing"></a><span data-ttu-id="c15c6-121">バックオフィス請求の増分取得をオンにする</span><span class="sxs-lookup"><span data-stu-id="c15c6-121">Turn on incremental capture for back-office invoicing</span></span>

<span data-ttu-id="c15c6-122">**機能管理** ワークスペースで、**すべて** フィルターを選択して、使用可能な機能をすべて表示し、**クレジット カードの増分取得をサポートする拡張機能** を検索します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-122">In the **Feature management** workspace, select the **All** filter to show all available features, and then search for **Extensibility to support incremental credit card capture**.</span></span> <span data-ttu-id="c15c6-123">機能を選択し、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-123">Select the feature, and then select **Enable now**.</span></span>

## <a name="uptake-incremental-capture-for-back-office-invoicing"></a><span data-ttu-id="c15c6-124">バックオフィス請求のための増分取得の取り込み</span><span class="sxs-lookup"><span data-stu-id="c15c6-124">Uptake incremental capture for back-office invoicing</span></span>

<span data-ttu-id="c15c6-125">バックオフィスの請求の一部として増分取得のサポートを利用するには、Commerce バージョン 10.0.13 に用意されている支払 SDK にアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-125">To uptake support for incremental capture as part of back-office invoicing, you must upgrade to the payments SDK that is provided in Commerce version 10.0.13.</span></span>

## <a name="ipaymentreferenceprovider"></a><span data-ttu-id="c15c6-126">IPaymentReferenceProvider</span><span class="sxs-lookup"><span data-stu-id="c15c6-126">IPaymentReferenceProvider</span></span>

<span data-ttu-id="c15c6-127">このバージョンの支払 SDK は、**IPaymentReferenceProvider** インターフェイスを追加します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-127">This version of the payment SDK adds the **IPaymentReferenceProvider** interface.</span></span> <span data-ttu-id="c15c6-128">このインターフェイスでは、各要求と応答の **PaymentTrackingID** 値の使用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c15c6-128">This interface supports using a **PaymentTrackingID** value for each request and response.</span></span> <span data-ttu-id="c15c6-129">**PaymentTrackingID** 値は、支払要求を追跡するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-129">The **PaymentTrackingID** value can be used to track payment requests.</span></span> <span data-ttu-id="c15c6-130">また、バックオフィスの請求書発行要求とプロセッサの間で、重複した要求が再送信前に発見されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-130">It also ensures that, between back-office invoicing requests and the processor, duplicate requests can be caught before they are re-sent.</span></span> <span data-ttu-id="c15c6-131">このようにして、重複する支払を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-131">In this way, it helps prevent duplicate payments.</span></span>

<span data-ttu-id="c15c6-132">次に、支払 SDK の SampleConnector.cs ファイルのサンプル実装を示します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-132">Here is a sample implementation from the SampleConnector.cs file in the payments SDK.</span></span>

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

<span data-ttu-id="c15c6-133">支払 SDK の AuthorizeRequest.cs ファイルの次のサンプルでは、**PaymentTrackingID** 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-133">The following sample from the AuthorizeRequest.cs file in the payments SDK uses a **PaymentTrackingID** value.</span></span>

```xml
authorizeRequest.PaymentTrackingId = PaymentUtilities.GetPropertyStringValue(
    hashtable,
    GenericNamespace.TransactionData,
    TransactionDataProperties.PaymentTrackingId);
```

## <a name="support-for-multiple-captures"></a><span data-ttu-id="c15c6-134">複数回の取得のサポート</span><span class="sxs-lookup"><span data-stu-id="c15c6-134">Support for multiple captures</span></span>

<span data-ttu-id="c15c6-135">支払プロセッサが複数回の取得をサポートしている場合、コネクタからの承認応答の **SupportsMultipleCaptures** プロパティは **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-135">If a payment processor supports multiple captures, the **SupportsMultipleCaptures** property for authorization responses from the connector should be set to **True**.</span></span> <span data-ttu-id="c15c6-136">このプロパティが **False** に設定されている場合、または指定されていない場合、その承認は増分取得の対象にはなりません。</span><span class="sxs-lookup"><span data-stu-id="c15c6-136">If the property is set to **False**, or if it isn't provided, the authorization won't be eligible for incremental capture.</span></span> <span data-ttu-id="c15c6-137">この場合、請求後に新しい未払い残高があると、新しい承認が取得されます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-137">In this case, if there is a new balance due after invoicing, a new authorization will be obtained.</span></span> 

<span data-ttu-id="c15c6-138">次に、支払 SDK の AuthorizationResponseProperties.cs ファイルのサンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-138">Here is a sample from the AuthorizationResponseProperties.cs file in the payments SDK.</span></span>

```xml
/// <summary>
/// Gets the SupportsMultipleCaptures property.
/// </summary>
public static string SupportsMultipleCaptures
{
    get { return "SupportsMultipleCaptures"; }
}
```

<span data-ttu-id="c15c6-139">バックオフィス請求プロセスが複数回の取得に対して有効な承認に対して取得すると、取得された合計金額が追跡されます。</span><span class="sxs-lookup"><span data-stu-id="c15c6-139">As back-office invoicing processes captures against authorizations that are enabled for multiple capture, the total captured amount is tracked.</span></span> <span data-ttu-id="c15c6-140">取得要求は、完全に取得されるまで、元の承認を引き続き参照します。</span><span class="sxs-lookup"><span data-stu-id="c15c6-140">Capture requests continue to reference the original authorization until it's fully captured.</span></span>

<span data-ttu-id="c15c6-141">売掛金勘定パラメータに従って期限切れになる承認は、増分取得の対象にはなりません。</span><span class="sxs-lookup"><span data-stu-id="c15c6-141">Authorizations that are expired according to Accounts receivable parameters aren't eligible for incremental capture.</span></span> 

<span data-ttu-id="c15c6-142">**SupportsMultipleCaptures** プロパティはグローバルではありません。</span><span class="sxs-lookup"><span data-stu-id="c15c6-142">The **SupportsMultipleCaptures** property isn't global.</span></span> <span data-ttu-id="c15c6-143">これは承認に固有です。</span><span class="sxs-lookup"><span data-stu-id="c15c6-143">It's specific to the authorization.</span></span> <span data-ttu-id="c15c6-144">環境には、増分取得をサポートするコネクタと、それをサポートしないコネクタの両方がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c15c6-144">An environment might have both connectors that support incremental capture and connectors that don't support it.</span></span>
