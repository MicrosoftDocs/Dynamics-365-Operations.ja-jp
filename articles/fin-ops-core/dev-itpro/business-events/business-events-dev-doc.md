---
title: ビジネス イベント開発者ドキュメント
description: このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 3aeb9e2d21fe2bd6f8bd78d286a57f2ab6d0372a
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249342"
---
# <a name="business-events-developer-documentation"></a>ビジネス イベント開発者ドキュメント

[!include[banner](../includes/banner.md)]

このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。

## <a name="what-is-a-business-event-and-what-isnt-a-business-event"></a>何がビジネス イベントで、何がビジネス イベントではないか。

ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。 仕入先の作成はビジネス イベントですか。 発注書の確認はビジネス イベントですか。 テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。 また、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。 これらの質問は無効であるだけでなく、統合のソリューションを計画および構築する時に考察するキー トピックです。 次のガイドラインは、この思考過程および決定作業を支援するのに役立ちます。

## <a name="intent"></a>目的

ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。 つまり、ビジネス イベントをキャプチャする理由、および受信者が使用する方法です。

ビジネス イベントをキャプチャして、Finance and Operation で発生するビジネス イベントに応じて Dynamics 365 Finance and Operations アプリの外部でビジネス アクションを実行することを目的としている場合、ビジネスイベントの良いユース ケースがあります。 ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文の作成などのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。 ビジネス アクションを実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。

データを受信者に転送し、効果的にデータ エクスポート シナリオを実現することを目的としている場合、ビジネス イベントに対する良いユースケースはありません。 実際、データ転送シナリオのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用になります。 このようなシナリオでは、データ管理で既に使用可能であるデータ エクスポート メカニズムを使用し続ける必要があります。

## <a name="fidelity"></a>忠実性

目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために使用する必要のあるアプローチを評価することです。 このセクションでは、評価する必要があるアプローチについて要約します。

使用するアプローチに関係なく、次の部分が使用されることを保証するために、ビジネス イベントの再現性は重要です。 そのため、ビジネス イベント実装の設計の選択に影響します。 ただし、ビジネス イベントを実装するための設計の選択は、ビジネス イベントの概念に影響しないようにする必要があります。 つまり、選択した設計が、イベントがビジネス イベントかどうかを決定する意思決定ツールとして使用されないようにする必要があります。 目的を考えてこれらの決定を行う必要があります。

- **堅牢なビジネス イベント** - 間違ったビジネス イベントは受信者に送信されません。 発注書確認のビジネス イベントが送信される場合、受取人はその発注書が確認済みであることを信用する必要があります。 この設計の選択は、このトランザクションの性質を保証するのに役立ちます。 そのため、受信者の期待に違反するデザインの選択を行わないようにする必要があります。
- **目標** – ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。 つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にする必要があります。 そのため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。 消費者がペイロードを理解するよう試みてビジネス イベントが何であったか判断する必要があるため、ビジネス イベントは一般的なものであるべきではありません。 デザインの選択は、対象となるビジネス イベントの保持のために許可されている必要があります。
- **ノイズレス** – デザインはノイズを除外するための努力が最小になるようにする必要があります。 ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルター ロジックの記述を避けます。 選択したアプローチは、ノイズ除去が必要でないように、十分に特定された時点でビジネス イベントがコードで実装されていることを保証する必要があります。 ロジックの追加によるノイズ除去の試行すべてはパフォーマンスに影響し、また特定のユースケースが複雑になることがあります。

| ビジネス ロジック レベルでのキャプチャ | テーブル レベルでのキャプチャ |
|-------------------------------------|----------------------------|
| このレベルでのキャプチャは、トランザクションで発生するため、持続性を保証するのに役立ちます。 | このレベルでのキャプチャは、トランザクションで発生するため、持続性を保証するのに役立ちます。 |
| このレベルでのキャプチャは、対象となるビジネス イベントに対して許可されています。 | イベントは下位レベルでキャプチャされるため、対象となるビジネス イベントを提供することは困難です。 |
| ノイズレスのままにすることは簡単です。 | ノイズを除去するためのサウンド ロジックを実装する追加作業が行われるまで、ノイズレスのままにすることは困難です。 |
| このレベルでのキャプチャにより、堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストが提供されます。 | イベントは下位レベルでキャプチャされるため、ビジネス プロセス コンテキストが失われる可能性があります。 |

> [!NOTE]
> 一般に、テーブル レベルでビジネス イベントを実装する場合、上記の表で説明した問題に加えて、他の課題に直面する可能性があります。 たとえば、基になるテーブルのデータを更新するストアド プロシージャを使用してビジネス ロジックを実行する場合、X++ のテーブル挿入メソッドでそのビジネス イベントが実装されているため、そのイベントは生成すらされないことがあります。 特定のユース ケースでは、多くの課題が発生する可能性があります。 そのため、テーブル レベルでビジネス イベントを実装することはお勧めしません。

## <a name="implement-a-business-event"></a>ビジネス イベントの実装

ビジネス イベントを実装して送信することは非常に簡単です。

1. 契約を構築します。
2. イベントを構築します。
3. イベントを送信するコードを追加します。 

以下の 2 つのクラスを実装する必要があります。

- **ビジネス イベント** - このクラスは **BusinessEventsBase** クラスを拡張します。 ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信がサポートされます。
- **ビジネス イベント契約** - このクラスは **BusinessEventsContract** クラスを拡張します。 ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。 

### <a name="businesseventsbase-extension"></a>BusinessEventsBase 拡張機能

#### <a name="naming-convention"></a>名前付け規則

ビジネス イベントの名前は、\<名詞/名詞句\>\<過去時制のアクション\>BusinessEvent のパターンに従う必要があります 名前の \<名詞/名詞句\> の部分は、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。

**例**

- VendorInvoicePostedBusinessEvent
- CollectionLetterSentBusinessEvent

#### <a name="implementation"></a>実装

**BusinessEventsBase** クラスの拡張機能を実装するプロセスは簡単です。 **BusinessEventsBase** クラスの拡張、および静的コンストラクター メソッドの実装、プライベート **新規** メソッド、内部状態を保持するメソッド、および **buildContract** メソッドが含まれます。

1. **newFrom\<my\_buffer\>** 静的メソッドを実装します。 メソッド名の \<my\_buffer\> の部分は通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。

    ```
    static public SalesInvoicePostedBusinessEvent
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        SalesInvoicePostedBusinessEvent businessEvent = new
        SalesInvoicePostedBusinessEvent();
        businessEvent.parmCustInvoiceJour(_custInvoiceJour);
        return businessEvent;
    }
    ```

2. **BusinessEventsBase** クラスを拡張します。

    ```
    [BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
    "AccountsReceivable:SalesOrderInvoicePostedBusinessEventName","AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription",ModuleAxapta::SalesOrder)]
    public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
    ```

    **BusinessEvents** 属性に注意してください。 この属性は、ビジネス イベントの契約、名前、説明に関する情報を含む、ビジネス イベント フレームワークを提供します。 また、ビジネス イベントが含まれるモジュールも提供します。 名前および説明の引数のためにラベルを定義する必要があります。 ただし、このようなラベルは記号 (@) なしで参照して、ローカライズされたデータの保存を回避する必要があります。

3. プライベート **新規** メソッドを実装します。 このメソッドは静的コンストラクター メソッドからのみ呼び出されます。

    ```
    private void new()
    {
    }
    ```

4. 内部状態を維持するプライベート **parm** メソッドを実装します。

    ```
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour = custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    ```

5. **buildContract** メソッドを実装します。 このステップには **EventContract** スタブが必要であることに注意してください。

    ```
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return
        SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
    ```

    拡張機能のために、**buildContract** メソッドには **Wrappable(true)** および **Replaceable(true)** 属性がある必要があります。 **buildContract** メソッドは会社のためにビジネス イベントが有効にされる時にのみ呼び出されます。

これは、「転記された販売注文請求書」ビジネス イベントの完全な実装です。

```
/// <summary>
/// Sales order invoice posted business event.
/// </summary>
[BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
'AccountsReceivable:SalesOrderInvoicePostedBusinessEventName',
'AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription',
ModuleAxapta::SalesOrder)]
public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
{
    private CustInvoiceJour custInvoiceJour;
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour =
    custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    /// <summary\>
    /// Creates a SalesInvoicePostedBusinessEvent from a CustInvoiceJour record.
    /// <summary>
    /// param name = "_custInvoiceJour"> CustInvoiceJour record <param>
    /// <returns>A SalesInvoicePostedBusinessEvent </returns>
    static public SalesInvoicePostedBusinessEvent
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        SalesInvoicePostedBusinessEvent businessEvent = new
        SalesInvoicePostedBusinessEvent();
        businessEvent.parmCustInvoiceJour(_custInvoiceJour);
        return businessEvent;
    }
    private void new()
    {
    }
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
}
```

### <a name="businesseventscontract-extension"></a>BusinessEventsContract 拡張機能

ビジネス イベント契約クラスは **BusinessEventsContract** クラスを拡張します。 ビジネス イベントのペイロードを定義および入力します。 ビジネス イベントには一部の変動がありますが、ビジネス イベント契約の基本構造は一貫しています。

ビジネス イベント契約の実装プロセスには、**BusinessEventContract** クラスの拡張、内部状態の定義、初期化メソッドの実装、静的コンストラクター メソッドの実装、および契約状態にアクセスするための **parm** メソッドの実装が含まれます。

1. **BusinessEventContract** クラスを拡張します。

    ```
    [DataContract]
    public final class SalesInvoicePostedBusinessEventContract extends
    BusinessEventsContract
    ```

    このクラスには、**DataContract** 属性がある必要があります。

2. 契約状態を保持するプライベート変数を追加します。

    ```
    private CustInvoiceAccount invoiceAccount;
    private CustInvoiceId invoiceId;
    private SalesIdBase salesId;
    private TransDate invoiceDate;
    private DueDate invoiceDueDate;
    private AmountMST invoiceAmount;
    private TaxAmount invoiceTaxAmount;
    private LegalEntityDataAreaId legalEntity;
    ```

3. プライベート初期化メソッドを実装します。

    ```
    private void initialize(CustInvoiceJour _custInvoiceJour)
    {
        invoiceAccount = _custInvoiceJour.InvoiceAccount;
        invoiceId = _custInvoiceJour.InvoiceId;
        salesId = _custInvoiceJour.SalesId;
        invoiceDate = _custInvoiceJour.InvoiceDate;
        invoiceDueDate = _custInvoiceJour.DueDate;
        invoiceAmount = _custInvoiceJour.InvoiceAmountMST;
        invoiceTaxAmount = _custInvoiceJour.SumTaxMST;
        legalEntity = _custInvoiceJour.DataAreaId;
    }
    ```

    **初期化**メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。

4. 静的コンストラクター メソッドを実装します。

    ```
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    ```

    静的コンストラクター メソッドはプライベート **初期化** メソッドを呼び出して、プライベート クラス状態を初期化します。

5. 契約状態にアクセスするための **parm** メソッドを実装します。

    ```
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    ```

    **parm** メソッドには **DataMember('\<名前\>')** および **BusinessEventsDataMember('\<説明\>')** 属性がある必要があります。 **DataMember** 属性で提供する名前 (たとえば、**'InvoiceAccount'**) はデータ契約消費者に対して表示されます。 **BusinessEventsDataMember** 属性で指定された説明は、ビジネス イベント カタログ UI に表示され、この契約のデータ メンバーを説明するために使用されます。

> [!NOTE]
> - **RecId** 値はビジネス イベントのペイロードの一部にすることはできません。 代わりに代替キー (AK) を使用します。
> - 列挙型 (enum) 値は、公開する前にそのシンボル値に変換する必要があります。 **enum2Symbol** メソッドを使用して列挙型の値をシンボル文字列に変換します。 次に例を示します。
>
>    ```
>    status = enum2Symbol(enumNum(CustVendDisputeStatus), _custDispute.Status);
>    ```

場合によっては、データ契約の内部状態の投入のために、追加の取得メソッドを実装する必要があります。 これらの取得メソッドはプライベート メソッドとして実装し、**初期化** メソッドから呼び出す必要があります。

これは、「転記された販売注文請求書」ビジネス イベント契約の完全な実装です。

```
/// <summary>
/// The data contract for a SalesInvoicePostedBusinessEvent
/// </summary>
[DataContract]
public final class SalesInvoicePostedBusinessEventContract extends
BusinessEventsContract
{
    private CustInvoiceAccount invoiceAccount;
    private CustInvoiceId invoiceId;
    private SalesIdBase salesId;
    private TransDate invoiceDate;
    private DueDate invoiceDueDate;
    private AmountMST invoiceAmount;
    private TaxAmount invoiceTaxAmount;
    private LegalEntityDataAreaId legalEntity;
    /// <summary>
    /// Creates a SalesInvoicePostedBusinessEventContract from a CustInvoiceJour record.
    /// </summary>
    /// <param name = "_custInvoiceJour"> CustInvoiceJour record</param>
    /// <returns>A SalesInvoicePostedBusinessEventContract </returns>
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    private void initialize(CustInvoiceJour _custInvoiceJour)
    {
        invoiceAccount = _custInvoiceJour.InvoiceAccount;
        invoiceId = _custInvoiceJour.InvoiceId;
        salesId = _custInvoiceJour.SalesId;
        invoiceDate = _custInvoiceJour.InvoiceDate;
        invoiceDueDate = _custInvoiceJour.DueDate;
        invoiceAmount = _custInvoiceJour.InvoiceAmountMST;
        invoiceTaxAmount = _custInvoiceJour.SumTaxMST;
        legalEntity = _custInvoiceJour.DataAreaId;
    }
    private void new()
    {
    }
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
    = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    [DataMember('InvoiceId'), BusinessEventsDataMember("@AccountsReceivable:BusinessEventInvoiceId")]
    public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId = invoiceId)
    {
    invoiceId = _invoiceId;
    return invoiceId;
    }
    [DataMember('SalesOrderId'), BusinessEventsDataMember("@AccountsReceivable:SalesOrderId")]
    public SalesIdBase parmSaleOrderId(SalesIdBase _salesId = salesId)
    {
        salesId = _salesId;
        return salesId;
    }
    [DataMember('InvoiceDate'), BusinessEventsDataMember("@AccountsReceivable:BusinessEventInvoiceDate")]
    public TransDate parmInvoiceDate(TransDate _invoiceDate = invoiceDate)
    {
        invoiceDate = _invoiceDate;
        return invoiceDate;
    }
    [DataMember('InvoiceDueDate'), BusinessEventsDataMember("@AccountsReceivable:InvoiceDueDate")]
    public DueDate parmInvoiceDueDate(DueDate _invoiceDueDate = invoiceDueDate)
    {
        invoiceDueDate = _invoiceDueDate;
        return invoiceDueDate;
    }
    [DataMember('InvoiceAmountInAccountingCurrency'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAmountInAccountingCurrency")]
    public AmountMST parmInvoiceAmount(AmountMST _invoiceAmount = invoiceAmount)
    {
        invoiceAmount = _invoiceAmount;
        return invoiceAmount;
    }
    [DataMember('InvoiceTaxAmount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceTaxAmount")]
    public TaxAmount parmInvoiceTaxAmount(TaxAmount _invoiceTaxAmount =
    invoiceTaxAmount)
    {
        invoiceTaxAmount = _invoiceTaxAmount;
        return invoiceTaxAmount;
    }
    [DataMember('LegalEntity'), BusinessEventsDataMember("@AccountsReceivable:LegalEntity")]
    public LegalEntityDataAreaId parmLegalEntity(LegalEntityDataAreaId _legalEntity
    = legalEntity)
    {
        legalEntity = _legalEntity;
        return legalEntity;
    }
}
```

## <a name="sending-a-business-event"></a>ビジネス イベントの送信

適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。 多くの場合、フレームワークの共通ポイントを使用することができます。 **SourceDocument** を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。 詳細については、このトピックの後半の [ソース ドキュメント フレームワークのサポート](#source-document-framework-support) セクションを参照してください。

また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。 たとえば、アプリケーション オブジェクト ツリー (AOT) 内の **CustVendVoucher** クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、**転記** メソッドがあります。 基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。 例については、AOT の **CustVoucher.createBusinessEvent** または **VendVoucher.createBusinessEvent** を参照してください。

ビジネス イベントの送信は、基になる取引のコミットにリンクされます。 基になる取引が中止される場合、ビジネス イベントは送信されません。 そのため、アプリケーションはペイロード情報が使用可能なポイントでビジネス イベントを送信することができます。

ビジネス イベント フレームワークは、ビジネス イベントが消費者に公開されるかどうか決定します。 一般的なルールとして、ビジネス イベントが有効かどうかに関わらず、アプリケーションはビジネス イベントを常に送信する必要があります。 重要な追加ロジックが必要な場合、またはビジネス イベントを送信するためのロジックがパフォーマンスに影響する場合は、ビジネス イベントの送信に関連付けられたビジネス ロジックを実行する前に、アプリケーションは特定のビジネス イベントが有効化されているかどうか確認することができます。 この確認は **BusinessEventsConfigurationReader::isBusinessEventEnabled** メソッドを介して実行されます。

```
if (BusinessEventsConfigurationReader::isBusinessEventEnabled(classStr(CollectionStatusUpdatedBusinessEvent)))
{
    while select dispute
    where dispute.Status == CustVendDisputeStatus::PromiseToPay
    && dispute.FollowUpDate _currentDate
    exists join custTrans
    where custTrans.RecId == dispute.CustTrans
    && !custTrans.Closed
    exists join _tmpCustAging
    where _tmpCustAging.AccountNum == custTrans.AccountNum
    {
        CollectionStatusUpdatedBusinessEvent::newFromCustDispute(dispute).send();
    }
}
```

## <a name="source-document-framework-support"></a>ソース ドキュメント フレームワークのサポート

元伝票フレームワークは、ドキュメントのプロセス内状態から完了状態への移行の一部として、ビジネス イベントの自動送信をサポートします。 この機能を活用するには、元伝票フレームワークを拡張するドキュメントが **SourceDocumentStateInProcess.getBusinessEvent** メソッドの拡張機能を実装して、正確な **BusinessEventsBase** 拡張子タイプを作成して戻す必要があります。

## <a name="extending-a-business-event-payload"></a>ビジネス イベント ペイロードの拡張

ビジネス イベントのペイロードの一部として、追加情報を公開する場合があります。 この追加情報を送信するには、ビジネス イベントの標準ペイロードを拡張する必要があります。

### <a name="example-scenario"></a>シナリオ例

この例では、**CustFreeTextInvoicePostedBusinessEventContract** を拡張して顧客の分類を含める方法を示します。 この顧客分類は業界に基づくカスタム分類です。

#### <a name="step-1-create-an-extended-business-event-contract"></a>ステップ 1: 拡張されたビジネス イベント契約の作成

標準的なビジネス イベント契約、およびペイロードに含める必要がある追加情報で構成される契約を作成します。

```
[DataContract]
public class CustFreeTextInvoicePostedBusinessEventExtendedContract
extends BusinessEventsContract
{
    // standard contract
    private CustFreeTextInvoicePostedBusinessEventContract
    custFreeTextInvoicePostedBusinessEventContract;
    // contract extensions
    private str customerClassification;
}
```

#### <a name="step-2-create-an-initialize-method"></a>ステップ 2: 初期化メソッドの作成

プライベート契約の値を初期化する **初期化** メソッドを作成します。

```
private void initialize(CustFreeTextInvoicePostedBusinessEventContract
_custFreeTextInvoicePostedBusinessEventContract)
{
    custFreeTextInvoicePostedBusinessEventContract =
    _custFreeTextInvoicePostedBusinessEventContract;
}
```

#### <a name="step-3-create-a-static-newfrom-method"></a>ステップ 3: 静的 newFrom メソッドの作成

標準契約を引数として取得し **初期化** メソッドを呼び出す、静的 **newFrom** メソッドを作成します。

```
public static CustFreeTextInvoicePostedBusinessEventExtendedContract
newFromCustFreeTextInvoicePostedBusinessEventContract(CustFreeTextInvoicePostedBusinessEventContract
_custFreeTextInvoicePostedBusinessEventContract)
{
    var contract = new CustFreeTextInvoicePostedBusinessEventExtendedContract();
    contract.initialize(_custFreeTextInvoicePostedBusinessEventContract);
    return contract;
}
```

#### <a name="step-4-map-parm-methods"></a>ステップ 4: parm メソッドのマッピング

**parm** メソッドを標準データ コントラクトからコピーして、クラスの標準契約インスタンス内で値を取得およびセットするように各メソッドを修正します。

```
[DataMember('InvoiceAccount')]
public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
= custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount())
{
    return
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount(_invoiceAccount);
}
[DataMember('InvoiceId')]
public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId =
custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId())
{
    return custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId(_invoiceId);
}
```

#### <a name="step-5-add-parm-methods-for-additional-payload-data"></a>ステップ 5: 追加ペイロード データのために parm メソッドを追加する

```
[DataMember('CustomerClassification')]
public CustomerClassification parmCustomerClassification(CustomerClassification
_customerClassification = customerClassification)
{
    customerClassification = _customerClassification;
    return customerClassification;
}
```

これは拡張ビジネス契約の完全な実装です。

```
[DataContract]
public class CustFreeTextInvoicePostedBusinessEventExtendedContract
extends BusinessEventsContract
{
    // standard contract
    private CustFreeTextInvoicePostedBusinessEventContract
    custFreeTextInvoicePostedBusinessEventContract;
    // contract extensions
    private str customerClassification;
    public static CustFreeTextInvoicePostedBusinessEventExtendedContract
    newFromCustFreeTextInvoicePostedBusinessEventContract(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        var contract = new CustFreeTextInvoicePostedBusinessEventExtendedContract();
        contract.initialize(_custFreeTextInvoicePostedBusinessEventContract);
        return contract;
    }
    private void initialize(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        custFreeTextInvoicePostedBusinessEventContract =
        _custFreeTextInvoicePostedBusinessEventContract;
    }
    private void new()
    {
    }
    [DataMember('InvoiceAccount')]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
    = custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount(_invoiceAccount);
    }
    [DataMember('InvoiceId')]
    public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId())
    {
        return custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId(_invoiceId);
    }
    [DataMember('InvoiceDate')]
    public TransDate parmInvoiceDate(TransDate _invoiceDate =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDate())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDate(_invoiceDate);
    }
    [DataMember('InvoiceDueDate')]
    public DueDate parmInvoiceDueDate(DueDate _invoiceDueDate =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDueDate())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDueDate(_invoiceDueDate);
    }
    [DataMember('InvoiceAmountInAccountingCurrency')]
    public AmountMST parmInvoiceAmount(AmountMST _invoiceAmount =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAmount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAmount(_invoiceAmount);
    }
    [DataMember('InvoiceTaxAmount')]
    public TaxAmount parmInvoiceTaxAmount(TaxAmount _invoiceTaxAmount =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceTaxAmount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceTaxAmount(_invoiceTaxAmount);
    }
    [DataMember('LegalEntity')]
    public LegalEntityDataAreaId parmLegalEntity(LegalEntityDataAreaId _legalEntity
    = custFreeTextInvoicePostedBusinessEventContract.parmLegalEntity())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmLegalEntity(_legalEntity);
    }
    // contract extensions
    [DataMember('CustomerClassification')]
    public CustomerClassification parmCustomerClassification(CustomerClassification
    _customerClassification = customerClassification)
    {
        customerClassification = _customerClassification;
        return customerClassification;
    }
}
```

#### <a name="step-6-wrap-the-buildcontract-method"></a>ステップ 6: buildContract メソッドをラップします。

標準ビジネス イベント契約をロードしてペイロード拡張機能を投入する **next** を呼び出す、ビルド契約の実装を提供します。 これは完全なクラスです。

```
[ExtensionOf(classStr(CustFreeTextInvoicePostedBusinessEvent))]
public final class FreeTextInvoicePostedBusinessEventContract_Extension
{
    public BusinessEventsContract buildContract()
    {
        var businessEventContract =
        CustFreeTextInvoicePostedBusinessEventExtendedContract::newFromCustFreeTextInvoicePostedBusinessEventContract(next
        buildContract());
        businessEventContract.parmCustomerClassification(CustomerClassifier::deriveCustomerClassification(businessEventContract.parmInvoiceAccount()));
        return businessEventContract;
    }
}
```

## <a name="extending-filters-so-that-they-have-custom-fields-if-the-middleware-supports-this-extension"></a>カスタム フィールドを持つようにフィルターを拡張する (ミドルウェアがこの拡張機能をサポートしている場合)

一部のミドルウェア システムはイベントのフィルター処理を許可します。 たとえば、Microsoft Azure Service Bus にはキーと値のペアを設定できるプロパティ バッグがあります。 これらのキーと値のペアは、Service Bus のキューやトピックからの読み込み時にイベントをフィルター処理するために使用できます。 また、Azure イベント グリッドには**件名**、**イベント タイプ**、および **ID** などのフィルター処理が可能なメッセージ プロパティがあります。 異なるシステムに対してこれら各種プロパティをサポートするために、ビジネス イベントのフレームワークは、*ペイロード コンテキスト*という名前の概念を使用します。 この概念を拡張して、さまざまなイベント システムがフィルター処理のために使用できるカスタム フィールドを含めることができます

### <a name="payload-context"></a>ペイロード コンテキスト

ビジネス イベント フレームワークは、ペイロード コンテキストの概念をサポートします。 ペイロード コンテキストは、フレームワークがペイロードに関するコンテキストと共に送信するメッセージを装飾する方法を提供します。 一部のシナリオでは、メッセージがエンドポイントに送信される時、追加のコンテキストが必要になることがあります。 そのため、フレームワークにはコンテキストの上書きやアダプタのカスタマイズができるフックポイントがあります。

### <a name="step-1-add-a-custom-payload-context"></a>ステップ 1: カスタム ペイロード コンテキストを追加します

カスタム ペイロード コンテキストは **BusinessEventsCommitLogPayloadContext** クラスから拡張される必要があります。

```
class CustomCommitLogPayloadContext extends BusinessEventsCommitLogPayloadContext
{
    private utcdatetime eventTime;
    public utcdatetime parmEventTime(utcdatetime \_eventTime = eventTime)
    {
        eventTime = \_eventTime;
        return eventTime;
    }
}
```

### <a name="step-2-construct-the-custom-payload-context"></a>ステップ 2: カスタム ペイロード コンテキストを構築します

新しいペイロード コンテキスト タイプを構築するには、**BusinessEventsSender.buildPayloadContext** メソッドに対してコマンド チェーン (CoC) 拡張機能を記述する必要があります。

```
[ExtensionOf(classStr(BusinessEventsSender))]
public final class CustomPayloadContextBusinessEventsSender_Extension
{
    protected BusinessEventsCommitLogPayloadContext
    buildPayloadContext(BusinessEventsCommitLogEntry \_commitLogEntry)
    {
        BusinessEventsCommitLogPayloadContext payloadContext = next
        buildPayloadContext(_commitLogEntry);
        CustomCommitLogPayloadContext customPayloadContext = new
        CustomCommitLogPayloadContext();
        customPayloadContext.initFromBusinessEventsCommitLogEntry(_commitLogEntry);
        customPayloadContext.parmEventTime(_commitLogEntry.parmEventTime());
        return customPayloadContext;
    }
}
```

### <a name="step-3-consume-the-custom-payload-context-from-an-adapter"></a>ステップ 3: アダプターからカスタム ペイロード コンテキストを使用します

ペイロード コンテキストを使用するアダプターは、新しいペイロード コンテキストの使用を許可する CoC メソッドを公開するように記述されます。 次の例は、サービス バス アダプターに対するこのステップの概要を示しています。 このアダプターには、サービス バスの消費者がフィルター処理できる汎用のプロパティ バッグがあります。

**BusinessEventsServiceBusAdapter** には **addProperties** という名前の CoC メソッドがあります。

```
[ExtensionOf(classStr(BusinessEventsServiceBusAdapter))]
public final class CustomBusinessEventsServiceBusAdapter_Extension
{
    protected void addProperties(BrokeredMessage \_message,
    BusinessEventsEndpointPayloadContext \_context)
    {
        if (_context is CustomCommitLogPayloadContext)
        {
            CustomCommitLogPayloadContext customPayloadContext = \_context as
            CustomCommitLogPayloadContext;
            var propertyBag = \_message.Properties;
            propertyBag.Add('EventId', customPayloadContext.parmEventId());
            propertyBag.Add('BusinessEventId', customPayloadContext.parmBusinessEventId());
            // Convert the enum to string to be able to serialize the property.
            propertyBag.Add('BusinessEventCategory', enum2Symbol(enumNum(ModuleAxapta),
            customPayloadContext.parmBusinessEventCategory()));
            propertyBag.Add('LegalEntity', customPayloadContext.parmLegalEntity());
            propertyBag.Add('EventTime', customPayloadContext.parmEventTime());
        }
    }
}
```

## <a name="adding-a-custom-endpoint-type"></a>カスタム エンドポイント タイプの追加
ビジネス イベント フレームワークは、最初から用意されているエンドポイント タイプに加え、新しいエンドポイント タイプの追加物もサポートしています。 このセクションでは、新しいカスタム エンドポイント タイプの追加方法を示す例を提供します。

### <a name="step-1-add-a-new-endpoint-type"></a>ステップ 1: 新しいエンドポイント タイプを追加します

各エンドポイント タイプは、列挙 **BusinessEventsEndpointType** によって表されます。 新しいエンドポイントを追加するプロセスの最初のステップは、次のセクションに示すように、この列挙を拡張することです。

![ビジネス イベントのエンドポイント](../media/customendpoint1.png)

### <a name="step-2-add-a-new-endpoint-table-to-the-hierarchy"></a>ステップ 2: 新しいエンドポイント テーブルを階層に追加します

すべてのエンドポイント データは階層テーブルに保存されます。 このテーブルのルートは、BusinessEventsEndpoint テーブルです。 新しいエンドポイント テーブルは、**サポート継承**プロパティを **Yes** に、**拡張**プロパティを **"BusinessEventsEndpoint"** (または BusinessEventsEndpoint 階層内の他の任意のエンドポイント) に設定して、このルート テーブルを拡張する必要があります。

![ビジネス イベントのエンドポイント](../media/customendpoint2.png)

その後、新しいテーブルに、初期化およびコード内でのエンドポイントとの通信に必要なカスタム フィールドの定義が保持されます。 競合を回避するには、属している特定のエンドポイントに対してフィールド名を限定する必要があります。 たとえば、2 つのエンドポイントは、**URL** フィールドの概念を持つことができます。 フィールドを区別するために、名前はカスタム エンドポイントに対して固有である必要があります。 たとえば、カスタム エンドポイントの **CustomURL** のフィールドに名前を付けます。

![ビジネス イベントのエンドポイント](../media/customendpoint3.png)

### <a name="step-3-add-a-new-endpoint-adapter-class-that-implements-the-ibusinesseventsendpoint-interface"></a>ステップ 3: IBusinessEventsEndpoint インターフェイスを実装する新しいエンドポイント アダプター クラスを追加します

新しいエンドポイント アダプター クラスは、**IBusinessEventsEndpoint** インターフェイスを実装している必要があります。 また、**BusinessEventsEndpointAttribute** 属性で装飾する必要もあります。

```
[BusinessEventsEndpoint(BusinessEventsEndpointType::CustomEndpoint)]
public class CustomEndpointAdapter implements IBusinessEventsEndpoint
{
```

**初期化**メソッドを実装して、渡された **BusinessEventsEndpoint** バッファーのタイプを確認し、次の例が示すように、バッファーが適切な型である場合は初期化します。

```
if (!(_endpoint is CustomBusinessEventsEndpoint))
{
    BusinessEventsEndpointManager::logUnknownEndpointRecord(tableStr(CustomBusinessEventsEndpoint),
    \_endpoint.RecId);
}
CustomBusinessEventsEndpoint customBusinessEventsEndpoint = \_endpoint as
CustomBusinessEventsEndpoint;
customField = customBusinessEventsEndpoint.CustomField;
if (!customField)
{
    throw warning(strFmt("\@BusinessEvents:MissingAdapterConstructorParameter",
    classStr(CustomEndpointAdapter), varStr(customField)));
}
```

### <a name="step-4-extend-the-endpointconfiguration-form"></a>ステップ 4: EndpointConfiguration フォームを拡張します

カスタム フィールド入力を保持するには FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ の下に新しいグループ コントロールを追加します。

![ビジネス イベントのエンドポイント](../media/customendpoint4.png)

カスタム フィールドの入力は、前の手順で作成した新しいテーブルとフィールドにバインドする必要があります。 次の例に示すように、**BusinessEventsEndpointConfiguration** フォームの **getConcreteType** と **showOtherFields** メソッドを拡張するクラス拡張機能を作成します。

![ビジネス イベントのエンドポイント](../media/customendpoint5.png)

```
[ExtensionOf(formStr(BusinessEventsEndpointConfiguration))]
final public class CustomBusinessEventsEndpointConfiguration_Extension
{
    public TableName getConcreteTableType(BusinessEventsEndpointType \_endpointType)
    {
        TableName tableName = next getConcreteTableType(_endpointType);
        if (_endpointType == BusinessEventsEndpointType::CustomEndpoint)
        {
            tableName = tableStr(CustomBusinessEventsEndpoint);
        }
        return tableName;
    }
    public void showOtherFields()
    {
        next showOtherFields();
        BusinessEventsEndpointType selection =
        any2Enum(EndpointTypeSelection.selection());
        if (selection == BusinessEventsEndpointType::CustomEndpoint)
        {
            this.control(this.controlId(formControlStr(BusinessEventsEndpointConfiguration,
            CustomFields))).visible(true);
        }
    }
}
```

## <a name="adding-human-readable-data-fields-to-the-payload"></a>ペイロードに人が判読可能なデータ フィールドを追加します。

この機能は、Platform 更新 30 以降でのみ利用できます。

ビジネス イベントのシリアル化には、FormJsonSerializer を使用してデータ契約内のオブジェクトをシリアル化します。 FormJsonSerializer は、**UtcDataTime** の値を ISO 8601 の日時形式にすることができます。 ビジネス イベンのペイロードを表示する時、人が判読可能な形式になります。 たとえば、**UtcDataTime**の値を、**/Date(1196865000000)/** の代わりに、**2007-12-05T14:30Z**の形式にすることができます。 「/Date(N)」形式では、N は 1970 年 1 月 1 日 (UTC+0) から経過したミリ秒数です。 ISO 形式は、JavaScript Object Notation (JSON) を解析するツールで、より頻繁に理解されます。

人が判読可能な形式にするため、**DateTimeIso8601** という名前の拡張データ型 (EDT) をデータ契約の値の型として使用します。 または、**DateTimeIso8601** EDTから派生した EDT を使用します。

```X++
[DataMember("TestIsoEdtUtcDateTime")]
public DateTimeIso8601 testIsoEdtUtcDateTime(DateTimeIso8601 _value = this._testIsoDateTime)
{
    if (!prmIsDefault(_value))
    {
        this._testIsoDateTime = _value;
    }
    return this._testIsoDateTime;
}
```
