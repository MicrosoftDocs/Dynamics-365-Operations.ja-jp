---
title: ビジネス イベント開発者ドキュメント
description: このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/21/2019
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
ms.openlocfilehash: 5ebf72da20a517e67433db9ff7134aa841ee7278
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "975839"
---
# <a name="business-events-developer-documentation"></a>ビジネス イベント開発者ドキュメント

[!include[banner](../includes/banner.md)]

このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。

## <a name="what-is-a-business-event-and-what-is-not-a-business-event"></a>何がビジネス イベントで、何がビジネス イベントではないか。
ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。 仕入先の作成はビジネス イベントですか。 または、発注書の確認はビジネス イベントですか。 テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。 または、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。 これらは有効な質問であるだけでなく、統合のソリューションを計画および構築するときに考察するキー トピックです。 次のガイドラインは、この思考過程および決定作業を支援するために使用することができます。

<a name="intent"></a>目的
------

ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。 つまり、ビジネス イベントをキャプチャする理由および受信者が使用する方法です。

ビジネス イベントをキャプチャする目的が、Finance and Operations で発生したビジネス イベントに応答して Finance and Operations 外でビジネス アクションを実行することである場合は、これはビジネス イベントをキャプチャする有効な目的です。 ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文を作成するなどのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。 ビジネス アクションを、実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。

ビジネス イベントをキャプチャする目的がデータを他の受信者に転送して、事実上データ エクスポート シナリオを実現することである場合、これはビジネス イベントを使用するための良いユース ケースではありません。 実際、データ転送ユース ケースのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用となります。
このようなシナリオでは、データ管理で既に使用可能なデータ エクスポート メカニズムを使用し続ける必要があります。

<a name="fidelity"></a>忠実性
--------

目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために必要なアプローチを評価することです。 次のセクションでは、評価する必要があるアプローチを要約します。

どのアプローチを採用するかに関わらず、ビジネス イベントの忠実性のためには以下の点を考慮することが重要で、結果として、ビジネス イベントを実装するためのデザイン選択に影響を与えます。 ただし、ビジネス イベントを実装するためのデザイン選択がビジネス イベントのコンセプトには影響を与えないようにします。選択されたデザインは、それがビジネス イベントであるか決定するための決定ツールとして使用すべきではありません。 このような決定には、事前に考慮された目的を使用する必要があります。

-   **堅牢なビジネス イベント** - 間違ったビジネス イベントを受信者に送信するべきではありません。 発注書確認ビジネス イベントが送信済みの場合、受取人はその発注書が確認済みであることを信用する必要があります。 デザイン選択はこの取引の性質を保証する必要があり、この予想に反するデザイン選択を採用しないようにします。

-   **目標** - ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。 つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にします。 このため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。 そのためビジネス イベントは一般的なものではなく、コンシューマーがペイロードを理解するよう試みてビジネス イベントが何であったか判断させるべきではありません。 実行されたデザイン選択は、これが順守されるようにする必要があります。

-   **ノイズレス** - デザイン内でノイズを除外するための努力が最小になるようにする必要があります。 ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルタ ロジックの記述を避けます。 選択したアプローチは、ビジネス イベントがコードで実装されるポイントが、ノイズのフィルター処理が必要ないほど明確である必要があります。 ロジックの追加によってノイズをフィルター処理する試みはパフォーマンスの負荷になるだけでなく、特定のユース ケースに基づき複雑になる機能性があります。

| **ビジネス ロジック レベルでのキャプチャ**                                                                                    | **テーブル レベルでのキャプチャ**                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| トランザクション内に置いて堅牢性を確保する                                                                           | トランザクション内に置いて堅牢性を確保します。                                                                      |
| 対象となるビジネス イベントを許可します。                                                                                     | イベントのキャプチャが低レベルであるため対象となるビジネス イベントを有効にすることが困難です。                             |
| 簡単にノイズレスのままにすることができます。                                                                                       | ノイズを除去するためのサウンド ロジックを導入する追加作業が行われるまで、ノイズレスのままにすることは困難です。 |
| 堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストを提供します。 | イベントのキャプチャが低レベルであると、ビジネス プロセスのコンテキストが失われる可能性が高くなります。                             |


## <a name="implementing-a-business-event"></a>ビジネス イベントの実装

ビジネス イベントを実装して送信することは非常に簡単なプロセスです。
1. 契約を構築します。
2. イベントを構築します。
3. イベントを送信するコードを追加します。 

以下の 2 つのクラスを実装する必要があります。

- **ビジネス イベント** - このクラスは **BusinessEventsBase** クラスを拡張します。 ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信のサポートを提供します。
- **ビジネス イベント契約** - このクラスは **BusinessEventsContract** クラスを拡張します。 ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。 

### <a name="businesseventsbase-extension"></a>BusinessEventsBase 拡張機能

#### <a name="naming-convention"></a>名前付け規則

ビジネス イベントの名前は以下のパターンに従う必要があります: <名詞/名詞句><past tense action>BusinessEvent

**例**

- VendorInvoicePostedBusinessEvent
- CollectionLetterSentBusinessEvent

名前の <名詞/名詞句> パートは、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。

#### <a name="implementation"></a>実装

**BusinessEventsBase** 拡張機能を実装するプロセスは簡単です。 **BusinessEventsBase** クラスの拡張、および静的コンストラクター メソッドの実装、プライベート **新規** メソッド、内部状態を保持するメソッド、および **buildContract** メソッドが含まれます。

1. **BusinessEventsBase** クラスを拡張します。

    ```
    [BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
    "AccountsReceivable:SalesOrderInvoicePostedBusinessEventName","AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription",ModuleAxapta::SalesOrder)]
    public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
    ```

    **BusinessEvents** 属性に注意してください。 この属性は、ビジネス イベントの契約、名前、説明、および含まれるモジュールに関する情報を含む、ビジネス イベント フレームワークを提供します。 ラベルは、名前と説明の引数に定義する必要がありますが、ローカライズされたデータの保存を避けるため、「@」記号なしで参照する必要があります。

2. 静的 **newFrom<my_buffer>** メソッドを実装します。 メソッド名の <my_buffer> パートは通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。

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

5. **buildContract** メソッドを実装します。 このステップには EventContract スタブが必要であることに注意してください。

    ```
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return
        SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
    ```

    拡張機能のために、**buildContract** メソッドは **Wrappable(true)** および **Replaceable(true)** 属性に帰属する必要があります。 **buildContract** メソッドは会社のためにビジネス イベントが有効にされるときにのみ呼び出されます。

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

    クラスは **DataContract** 属性に帰属する必要があります。

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

    **初期化** メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。

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

    **parm** メソッドは **DataMember('<name>')** および **BusinessEventsDataMember('<description>')** 属性に帰属する必要があります。 属性で提供する名前 (たとえば、 **'InvoiceAccount'**) はデータ契約消費者に対して表示されます。 BusinessEventsDataMember で指定された説明は、この契約のデータ メンバーを記述するときにビジネス イベント カタログ UI に表示されます。

> [!NOTE]
> - **RecId** 値はビジネス イベント ペイロードの一部にすることはできません。 代わりに代替キー (AK) を使用します。
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

適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。 多くの場合、フレームワーク内の共通ポイントを使用することができます。 **SourceDocument** を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。 詳細については、以下をサポートする元伝票フレームワークのセクションを参照してください。

また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。 たとえば、AOT 内の **CustVendVoucher** クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、**転記** メソッドがあります。 基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。 例については、AOT の **CustVoucher.createBusinessEvent** または **VendVoucher.createBusinessEvent** を参照してください。

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

#### <a name="step-5-add-parms-methods-for-additional-payload-data"></a>ステップ 5: 追加ペイロード データのために parm メソッドを追加する

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

## <a name="summary"></a>集計

標準ビジネス イベント契約を補うビジネス イベント契約を実装し、 **buildContract** メソッドの実装をラップするためにコマンド チェーン (CoC) を使用する拡張クラスを実装することにより、ビジネス イベントのペイロードを容易に拡張することができます。
