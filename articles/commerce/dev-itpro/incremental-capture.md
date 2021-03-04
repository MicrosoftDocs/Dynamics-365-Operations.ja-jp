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
# <a name="incremental-capture-for-back-office-invoicing"></a>バックオフィスの請求の増分取得

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、支払ソフトウェア開発キット (SDK) が注文請求の一部として増分取得をどのようにサポートするかについて説明します。 増分取得では、支払処理は複数の請求書がある注文の履行をサポートします。 具体的には、請求書は注文に対して処理されるため、以前の支払取得が変更による残高の原因となった場合、新しい支払承認を取得する代わりに、支払取得要求が元の支払承認を参照します。

## <a name="overview"></a>概要

多くの加盟店は、注文を複数の出荷で処理しています。 Microsoft Dynamics 365 Commerce バージョン 10.0.12 以前では、複数の出荷に履行される注文に対してクレジット カード支払を処理するための最初から用意されているプロセスは、出荷が請求されると支払を取得し、出荷が必要な残りの品目の残高に新しい支払認証を取得します。 この処理によって、支払取得が支払プロセッサ全体で一貫してサポートされることが保証されます。 ただし、いくつかの欠点もあります。 具体的には、承認が部分的に取得された後、未払い残高に対して新しい承認が作成されると、古い承認と新しい承認が重複する可能性があります。 この場合、顧客の支払カードに対して注文合計を超えるオープン承認が表示される可能性があります。 したがって、承認がクレジットカードで利用可能なオープン残高を超えたり、カード発行者が不正行為の疑いでカードの処理をブロックしたりする場合があります。

これらの問題に対処するために、Commerce バージョン 10.0.13 以降の支払 SDK には、バック オフィス支払取得に対する増分取得サポートが含まれています。 したがって、プロセッサが増分取得をサポートしている場合、支払コネクタを更新して、注文処理の過程で 1 つの認証に対して複数回取得できます。 次の図は、1 つの承認に対して複数回の取得が行われる場合の、さまざまな支払取得フレームワークの違いを示しています。

![現在の支払取得フレームワーク対増分取得](../dev-itpro/media/INC_DIFF.png)

Commerce バージョン 10.0.13 では、増分取得は、バック オフィス請求 (つまり、バック オフィスの注文処理の一部として発生するすべての請求) の一部としてサポートされています。 今後のリリースでは、販売時点管理 (POS) からの増分取得サポートが、最初から用意されている Adyen 支払コネクタに追加されます。

## <a name="turn-on-incremental-capture-for-back-office-invoicing"></a>バックオフィス請求の増分取得をオンにする

**機能管理** ワークスペースで、**すべて** フィルターを選択して、使用可能な機能をすべて表示し、**クレジット カードの増分取得をサポートする拡張機能** を検索します。 機能を選択し、**直ちに有効化** を選択します。

## <a name="uptake-incremental-capture-for-back-office-invoicing"></a>バックオフィス請求のための増分取得の取り込み

バックオフィスの請求の一部として増分取得のサポートを利用するには、Commerce バージョン 10.0.13 に用意されている支払 SDK にアップグレードする必要があります。

## <a name="ipaymentreferenceprovider"></a>IPaymentReferenceProvider

このバージョンの支払 SDK は、**IPaymentReferenceProvider** インターフェイスを追加します。 このインターフェイスでは、各要求と応答の **PaymentTrackingID** 値の使用をサポートします。 **PaymentTrackingID** 値は、支払要求を追跡するために使用できます。 また、バックオフィスの請求書発行要求とプロセッサの間で、重複した要求が再送信前に発見されることが保証されます。 このようにして、重複する支払を防ぐことができます。

次に、支払 SDK の SampleConnector.cs ファイルのサンプル実装を示します。

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

支払 SDK の AuthorizeRequest.cs ファイルの次のサンプルでは、**PaymentTrackingID** 値を使用します。

```xml
authorizeRequest.PaymentTrackingId = PaymentUtilities.GetPropertyStringValue(
    hashtable,
    GenericNamespace.TransactionData,
    TransactionDataProperties.PaymentTrackingId);
```

## <a name="support-for-multiple-captures"></a>複数回の取得のサポート

支払プロセッサが複数回の取得をサポートしている場合、コネクタからの承認応答の **SupportsMultipleCaptures** プロパティは **True** に設定します。 このプロパティが **False** に設定されている場合、または指定されていない場合、その承認は増分取得の対象にはなりません。 この場合、請求後に新しい未払い残高があると、新しい承認が取得されます。 

次に、支払 SDK の AuthorizationResponseProperties.cs ファイルのサンプルを示します。

```xml
/// <summary>
/// Gets the SupportsMultipleCaptures property.
/// </summary>
public static string SupportsMultipleCaptures
{
    get { return "SupportsMultipleCaptures"; }
}
```

バックオフィス請求プロセスが複数回の取得に対して有効な承認に対して取得すると、取得された合計金額が追跡されます。 取得要求は、完全に取得されるまで、元の承認を引き続き参照します。

売掛金勘定パラメータに従って期限切れになる承認は、増分取得の対象にはなりません。 

**SupportsMultipleCaptures** プロパティはグローバルではありません。 これは承認に固有です。 環境には、増分取得をサポートするコネクタと、それをサポートしないコネクタの両方がある場合があります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]