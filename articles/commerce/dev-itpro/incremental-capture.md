---
title: 増分支払の取得
description: このトピックでは、Dynamics 365 Commerce での注文請求の一部として増分取得に対するすぐに使えるサポートについて説明します。
author: BrianShook
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: fb57b8bc7b478dcd05296f7b32a05b5b18da582d
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781721"
---
# <a name="incremental-capture-for-order-invoicing"></a>注文請求の増分取得

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce での注文請求の一部として増分取得に対するすぐに使えるサポートについて説明します。 また、Adyen 向け Dynamics 365 Payment Connector の増分取得を有効にする方法と、支払ソフトウェア開発キット (SDK) を使用してサード パーティーの支払コネクタに増分取得を追加する方法についても説明します。

増分取得が有効になると、複数の請求書を使用して長期にわたって履行される注文は、複数の請求書および取得済支払の元の承認を参照します。 これは、複数の請求書を使用して注文を履行するレガシ サポートとは対照的で、注文の一部が履行され、未払残高が変更されるたびに新しい承認が取得されます。

増分取得は、POS および Commerce 本社から注文が履行されたときに、Adyen 向け Dynamics 365 Payment Connector 使用してすぐにサポートされます。 

多くの加盟店は、注文を複数の出荷で処理しています。 既定では、複数の出荷に履行される注文に対してクレジット カード支払を処理するための最初から用意されているプロセスは、出荷が請求されると支払を取得し、出荷が必要な残りの品目の残高に新しい支払認証を取得します。 この処理によって、支払取得が支払プロセッサ全体で一貫してサポートされることが保証されます。 

ただし、いくつかの欠点もあります。 たとえば、承認が部分的に取得された後、未払い残高に対して新しい承認が作成されると、古い承認と新しい承認が重複する可能性があります。 この場合、注文合計を超えるオープン承認が顧客の支払カードに対して表示される可能性があり、その結果、クレジット カードで使用可能なオープン残高を超える承認が発生したり、カード発行者が不正の疑いがあるためにカードの処理をブロックしたりする可能性があります。

これらの問題に対処するために、Adyen 向け Dynamics 365 Payment Connector および支払 SDKに対して増分取得サポートが導入されています。 プロセッサが増分取得をサポートしている場合、支払コネクタを更新して、注文処理の過程で 1 つの承認に対して複数回取得できます。 

次の図は、1 つの承認に対して複数回の取得が行われる場合の、さまざまな支払取得フレームワークの違いを示しています。

![現在の支払取得フレームワーク対増分取得。](../dev-itpro/media/INC_DIFF.png)

本社請求 (つまり、本社での注文処理の一部として発生する請求) の増分取得のサポートは、Commerce バージョン 10.0.13 の支払 SDK に最初に追加されました。 Commerce バージョン 10.0.18 では、SDK による増分取得サポートが本社の外部のチャネルに拡張されています。 店舗、Modern POS、およびコール センターでは、この拡張サポートによって、新しい注文に対して作成された承認を **SupportsMultipleCaptures** としてマークすることができます。 これらの注文に対して本社または Modern POS で後で請求を行う場合、支払が取得され、以降の請求書で支払が取得されるときに元の承認が保持および参照されます。 

## <a name="enable-incremental-capture"></a>増分取得を有効にする

### <a name="prerequisite-features"></a>前提条件となる機能

増分取得を有効にする前に、次の機能を有効にする必要があります。 

| 機能名 | 説明 |
|---|---|
| コマースの統一支払転記仕訳帳の既定値 | この機能は、コールセンター、POS、または電子商取引チャネルを介して作成された注文に対して、ビジネス ロジックが顧客支払仕訳帳と顧客返金仕訳帳を作成する方法を変更します。 |
| オムニ チャネル支払 | この機能を使用すると、「オンラインで購入し、店舗で受け取る」 (BOPIS) などのオムニチャネルの決済シナリオを有効化できます。 詳細については、[オムニチャネル決済の概要](../omni-channel-payments.md) を参照してください。 |  
| 請求に対する支払保護の重複 | この機能は、請求書発行のシナリオで重複した決済の保護を可能にします。 Commerce の決済機能は、請求書発行シナリオのカスタマイズに影響する可能性があります。 組織に請求書発行のカスタマイズがある場合は、運用環境で Commerce の決済機能を有効にする前に、それらがリファクターされていることを確認してください。 | 
| 複数のキャプチャの払戻を有効にする | この機能を使用すると、注文に対して複数のリンクされた払戻を実行する機能が改善されます。 |
| 認証の有効期限が切れたクレジットカードの決済明細行を手動で無効化する | この機能により、決済明細行の期限が切れた場合に手動で削除することができ、承認を更新しません。 |
| オムニチャネル Commerce 注文支払。 | この機能により、チャネル間の支払を合理化し、コール センター内で店舗および POS の注文の支払を編集できます。 前述の機能はこの機能の前提条件なので、この機能を最後に有効にする必要があります。 詳細については、[オムニチャネル Commerce 注文支払](commerce-payments.md) を参照してください。 |

### <a name="enable-the-extensibility-to-support-incremental-credit-card-capture-feature"></a>「クレジット カードの増分取得をサポートする機能拡張」機能を有効にする

この機能は当初、支払 SDK を介して請求する本社の増分取得のために導入されたもので、Adyen 向け Dynamics 365 Payment Connector およびすべてのチャネルを介した増分取得のサポートを有効にするために拡張されました。 

Commerce 本社で「クレジット カードの増分取得をサポートする機能拡張」機能を有効にするには、次の手順に従います。

1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。 
1. **すべて** タブを選択すると、使用可能なすべての機能が表示されます。
1. **クレジット カードの増分取得をサポートする機能拡張** を検索します。
1. 機能を選択し、**今すぐ有効化** を選択します。

### <a name="enable-incremental-capture-for-the-dynamics-365-payment-connector-for-adyen"></a>Adyen 向け Dynamics 365 Payment Connector で増分取得を有効にする

「クレジット カードの増分取得をサポートする機能拡張」機能を有効にすることに加え、Adyen 向け Dynamics 365 Payment Connector の商社プロパティの **要求保護を有効にする** プロパティの値も、コネクタが使用されるチャネルごとに **True** に設定する必要があります。 値が **False** または空白の場合増分取得はコネクタに対して有効になりません。 プロパティが **True** に設定されている場合、重複する要求を防ぐため、追跡 ID が支払プロバイダーへの要求に追加されます。 サード パーティ支払コネクタに対する追跡 ID サポートについては、次の「[サード パーティ支払コネクタ用増分取得の取得](#uptake-incremental-capture-for-third-party-payment-connectors)」で説明されます。

一部の支払方法では、増分取得がサポートされない場合があります。 これらの支払方法は、Adyen 向け Dynamics 365 Payment Connector のマーチャント プロパティの **増分取得以外の支払方法** フィールドで構成できます。 このフィールドに設定する値は、Adyen が承認応答でカード タイプを識別するために使用する「支払方法バリアント/カード タイプ」文字列と一致する必要があります。 支払方法バリアント文字列は、Adyen の [PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) にあります。 増分取得を除外する必要がある複数のカード タイプがある場合は、セミコロンで区切る必要があります。 

増分取得をサポートしない支払方法バリアントの例の 1 つが Interac です。 Adyen のドキュメントでは、Interac 支払方法バリアントに対して一覧表示される文字列は **interac** です。 Interac を受け入れるカナダのマーチャントに対して支払サービスが構成されている場合は、この支払方法バリアントをコネクタのマーチャント プロパティの「増分取得以外の支払方法」のリストに追加する必要があります。  

Adyen 向け Dynamics 365 Payment Connector の増分取得を有効にしているマーチャントは、マーチャント口座で **allowMultiplePartialCapture** フラグが **はい** に設定されていることを確認するため、Adyen にも連絡する必要があります。 このフラグがマーチャント口座レベルで有効になっていない場合、請求時の取得ロジックは、サポートされる従来のフローに戻ります。 

## <a name="uptake-incremental-capture-for-third-party-payment-connectors"></a>サード パーティ支払コネクタ用の増分取得を取得する

サード パーティ支払コネクタの本社請求の一部として増分取得のサポートを取り込み、すべてのチャネルで増分取得をサポートするには、Commerce バージョン 10.0.18 で提供されている支払 SDK にアップグレードする必要があります。

### <a name="ipaymentreferenceprovider"></a>IPaymentReferenceProvider

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

### <a name="support-for-multiple-captures"></a>複数回の取得のサポート

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

## <a name="incremental-capture-user-experience"></a>増分取得のユーザー エクスペリエンス

増分取得のユーザー エクスペリエンスは、増分取得が有効になっていない場合のユーザー エクスペリエンスと変わりません。 重要な違いは、増分取得が有効な場合に元の承認が有効な場合、注文が部分的に請求された後に新しい承認を取得できない点です。 代わりに、既存の承認が保持され、後続の支払の取得に使用されます。 

本社またはプロセッサのポータルで支払の問題を調査しているユーザーの場合、承認と取得の比率が 1:1 である従来のフローとは対照的に、複数の支払取得がマップされた単一の承認を持つように、増分取得順序が表示されます。 

## <a name="additional-resources"></a>追加リソース

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[Adyen 向け Dynamics 365 Payment Connector](adyen-connector.md?tabs=8-1-3)

[オムニチャネル Commerce 注文支払](commerce-payments.md)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]