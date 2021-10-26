---
title: 税エンジンの統合
description: このトピックでは、税エンジンの統合について説明します。
author: kailiang
ms.date: 12/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable
audience: IT Pro
ms.reviewer: kfend
ms.search.region: India
ms.author: kailiang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 324bac132e0fb8880793cb150c6f3732346ad195
ms.sourcegitcommit: 2fba4f2ef7e513357366fc640befe0d2f7bc31f5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2021
ms.locfileid: "7601479"
---
# <a name="tax-engine-integration"></a>税エンジンの統合

[!include [banner](../includes/banner.md)]

[税エンジン](tax-engine.md) (GTE とも呼ばれます) を Dynamics 365 Finance と統合するには、税計算のために税エンジンとやり取りする X++ コードを実装する必要があります。それは結果を消費して、伝票および税トランザクションの税金の表示、計算、および転記を行います。 (税計算では、税調整を含める、または除外することができます。) 

> [!NOTE]
> 税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。

## <a name="tax-engine-integration-models"></a>税エンジンの統合モデル
税エンジンの統合には 3 つのモデルがあります。

- 税エンジン サービスを使用した税エンジン インターフェース
- 税 ビジネス サービス
- Finance アプリケーション統合:
    - アプリケーションの統合
    - 会計の統合

![GTE 統合モデル。](./media/gte-3-models.PNG)

###  <a name="tax-engine-interfaces-with-the-tax-engine-service-model"></a>税エンジン サービス モデルを使用した税エンジン インターフェース

このモデルは、Finance の統合フレームワークの一部です。 したがって、パートナーや顧客にはほとんど取得の必要がありません。

ITaxEngine インターフェースとその実装には、税エンジンの基本操作が含まれています。 これらの操作には、税エンジンを介した税の計算、Finance テーブルへの計算結果の保持、トランザクションの税務書類の取得、税エンジンキャッシュと Finance テーブルの両方からの税務書類の削除が含まれます。

ITaxDocument インターフェイスと実装のセットにより、税エンジンが計算して返す税務書類から情報を読み取ることができます。 このセットには、ITaxDocument、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、およびITaxDocumentMeasure が含まれます。

![GTE インターフェイス。](./media/gte-itaxdocument_interfaces.jpg)

これらのインタフェースは、ITaxDocumentLine から指定されたフィールド値 (**ITaxDocumentField**) および ITaxDocumentComponentLine から予測される数値 (**ITaxDocumentMeasure**) を取得するためのメソッドも提供します。

- ITaxDocumentMetaData インターフェイスのセットにより、税務文書からモデル情報を読み取ることができます。 このセットには、ITaxDocumentMetaData、ITaxDocumentLineMetaData、ITaxDocumentComponentLineMetaData、および ITaxDocumentMeasureMetaData が含まれます。
- ITaxDocumentEnumerator および ITaxDocumentMeataDataEnumerator インターフェイスのセットは、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、および ITaxDocumentMeasure などの税務書類関連オブジェクトのリストを読み取るための列挙子を提供します。

### <a name="tax-business-service-model"></a>税ビジネス サービス モデル

税ビジネス サービス モデルは、Finance の統合フレームワークの一部であり、パートナーや顧客にはほとんど取得の必要がありません。 このモデルは、Finance アプリケーションが基本的な操作のために税エンジンと相互作用することをサポートします。 インタフェース モデルとアプリケーション モデルの両方を使用して、税の計算、会計、および転記を行います。 税ビジネス サービス モデルでは、次の方法を提供します。

<table>
<tr>
<td><strong>メソッド</strong></td>
<td><strong>説明</strong>
</td>
</tr>
<tr>
<td>税の計算</td>
    <td> <strong>ダーティー</strong>とマークされている場合は、税務書類を削除してから税金を計算します。<ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 税務署類オブジェクト</li>
</ul>
</td>
</tr>
<tr>
<td>税の再計算</td>
<td>明示的に税務書類を再計算します。
<ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 税務署類オブジェクト</li>
</ul>
</td>
</tr>
<tr>
<td>SaveTaxDocument</td>
<td>税務書類を Finance データベースに保存します。
 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
<tr>
<td>GetTaxDocumentBySource</td>
<td>ソース トランザクション ID に基づいて税務書類を読み取ります。 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 税務署類オブジェクト</li>
</ul>
</td>
</tr>
<tr>
<td>GetTaxDocumentLineBySource</td>
<td>ソース トランザクション明細行 ID に基づいて税務書類明細行を読み取ります。 <ul>
<li><strong>入力</strong>: トランザクション明細行識別子</li>
<li><strong>出力</strong>: 税務署類明細行オブジェクト</li>
</ul>
</td>
</tr>
<tr>
<td>GetTaxDocumentTaxStatus</td>
<td>関連するトランザクションの税務書類のステータスを読み取ります。
 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 税務署類オブジェクト</li>
</ul>
</td>
</tr>
<tr>
<td>MarkTaxDocumentTaxStatus</td>
<td>下線を引いたトランザクションが更新されたら、税務文書を<strong>ダーティー</strong>としてマークします。 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子、税務書類のステータス</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
<tr>
<td>DeleteTaxDocument</td>
<td>トランザクションが削除された場合に、税務書類を削除します。 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
<tr>
<td>PostTax</td>
<td>トランザクションの税金を転記します。 <ul>
<li><strong>入力</strong>: 転記する必要がある税の元帳伝票、課税対象文書の識別子</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
<tr>
<td>TransferTaxDocument</td>
<td>ソースがサポートしているトランザクションから別のトランザクションに税務書類を転送します。
<ul>
<li><strong>入力</strong>: ソース トランザクション、ターゲット トランザクション</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
<tr>
<td>PostTaxDocument</td>
<td>税務文書のステータスを <strong>転記済</strong>に変更するだけです。 <ul>
<li><strong>入力</strong>: 課税対象文書の識別子</li>
<li><strong>出力</strong>: 該当なし</li>
</ul>
</td>
</tr>
</table>

### <a name="finance-application-integration"></a>Finance アプリケーション統合

Finance からのトランザクション情報は、税エンジンに送信する必要があります。 同時に、税の会計と転記は、Finance の実装と整合する必要があります。 そのため、Finance アプリケーションでは 3 つの部分が作成されます。

- 課税対象文書
- 税会計
- 税転記

一方、統合では、輸送文書フレームワークを使用して、Finance トランザクションと税務書類の間の関係を維持します。

#### <a name="application-integration"></a>アプリケーションの統合

##### <a name="taxable-document"></a>課税対象文書

課税対象文書は、一連のデータ プロバイダーを使用して、トランザクションの情報をカプセル化します。 トランザクションの情報は、TaxableDocument オブジェクトによってラップされます。 このオブジェクトの TaxableDocumentDescriptor オブジェクトは、トランザクションとは何かを説明し、税モデル属性をトランザクション データにバインドする一連のデータ プロバイダーをリストする必要があります。

![課税対象文書。](media/gte-taxable-doc.png)

**TaxableDocumentDescriptor** は、一連の TaxableDocumentTypeDefinition インターフェイスを実装し、トランザクションとは何かを説明するクラスです。 技術的には、TaxableDocumentDescriptors は Finance のテーブル ベースですが、TaxableDocumentTypeDefinitions はよりビジネス主導型であり、主に税の設定条件に使用されます。

次の例では、TaxableDocumentDescriptorPurchaseOrderParm は、同じ PurchParmTable テーブルを共有する 3 つのインターフェースを実装します。

![共有テーブルの例。](media/gte-example-shared-table.png)

追加の属性が税コンフィギュレーションに追加され、それらがルックアップ、条件、式、またはその他のコンフィギュレーションに使用される場合は、属性をトランザクション データとバインドする必要があります。 したがって、トランザクションに対応するデータ プロバイダー クラスを変更して、このようなデータ バインディングが行われるようにする必要があります。

> [!NOTE]
> 追加のトランザクションが GTE をサポートする必要がある場合は、関連する TaxableDocumentTypeDefinitions、TaxableDocumentDescriptors、および TaxableDocumentDataProviders を作成する必要があります。

##### <a name="transit-document"></a>輸送文書

輸送文書は、次の 2 つの目的に使用される Finance の既存のフレームワークです。

- トランザクションおよび輸送文書間の関係を維持します。
- あるトランザクションから別のトランザクションにドキュメントを転送します。

このフレームワークを使用すると、トランザクションのドキュメントを簡単に見つけて輸送履歴を追跡できます。 たとえば、VendInvoiceInfoTable から税務書類が作成され、輸送ドキュメントでは VendInvoiceInfoTable と TaxDocument の関係が維持されます。 発注書が請求されると、VendInvoiceInfoTable からの税務書類が VendInvoiceJour に転送されます。

> [!NOTE] 
> 追加のトランザクションが税エンジンをサポートする必要がある場合は、ヘッダー レベルと明細行レベルの両方から、どのトランザクションに税務書類があるかを説明するための輸送ドキュメント フレームワークのルールを定義する必要があります。 ルールには、ソース トランザクションからターゲット トランザクションへの輸送アクションも定義する必要があります。

#### <a name="transaction-integration"></a>トランザクションの統合

トランザクションの統合は個別でのみ発生します。 各トランザクションおよびシナリオに対して、税 ビジネス サービスは税計算、税の仮定、および税転記に対して適切な方法で呼び出す必要があります。 例については、このトピックで後述する [Finance 統合の例 – 発注請求書](#example-finance-integration--purchase-order-invoice) セクションを参照してください。

#### <a name="accounting-integration"></a>会計の統合

##### <a name="tax-accounting"></a>税会計

Finance トランザクションの会計には、元伝票会計と非元伝票会計の 2 つの部分があります。 同じ動作が税エンジンの税務会計にも当てはまります。税務会計は、以下の両面で Finance の実装と統合されています。

- 発注書やフ自由書式の請求書などの元伝票のトランザクションでは、税務書類が作成されたときに税のアカウント情報が取得されます。
- 販売注文や一般仕訳帳などの非元伝票トランザクションの場合、アカウント情報は税が転記されるときに決定されます。

> [!NOTE]
> 追加の元伝票トランザクションに税エンジンのサポートが必要な場合は、指定されたビジネス イベントと金額に対して AccountingJournalizationRule と AccountingDistributionRule を拡張するための元伝票関連クラスを作成する必要があります。

##### <a name="tax-engine-tax-posting"></a>税エンジン税転記

現在、税エンジンの税転記により、TaxTrans、TaxTrans\_IN (インドの国/地域コードで実行している場合)、および TaxTrans の関連伝票が生成されます。 **taxTrans** フィールドに税務書類の属性または基準を入力するには、**TaxAcctTaxTransTaxDocAttrMapping** および **TaxAcctTxTransTaxDocMeasureMapping** を使用してマッピングを提供する必要があります。

次の図は、TaxTrans および伝票の作成方法を示します。

![TaxTrans および伝票を作成します。](media/gte-create-taxtrans-voucher.png)

> [!NOTE]
> **taxTrans** フィールドに税務書類の追加フィールドを入力する必要がある場合は、 **TaxAcctTaxTransTaxDocAttrMapping** クラス、**TaxAcctTxTransTaxDocMeasureMapping** クラス、またはこれらのクラスのいずれかの拡張クラスをデータ バインディングに適切な方法で更新する必要があります。

## <a name="example-finance-integration--purchase-order-invoice"></a>例: Finance の統合 – 発注請求書

このセクションでは、税エンジンが発注請求書とどのように統合されるかの例を示します。 関連するトランザクション テーブルには、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、およびVendInvoiceTrans が含まれます。

### <a name="integration-checklist"></a>統合 チェックリスト

以下の表は、発注請求書との統合に関連するすべての該当する変更をまとめたものです。

<table>
<tr>
<th colspan="2">トランザクションの取得のチェックリスト</th>
<th>説明</th>
<th>AOT オブジェクト</th>
</tr>
<tr>
<td rowspan="2">定義</td>
<td>課税対象文書を定義します。</td>
<td>課税対象文書タイプとトランザクションの説明を作成します。</td>
<td>TaxableDocumentTypeDefinitionPurchaseInvoice<br>
TaxableDocumentDescriptorPurchaseInvoice</td>
</tr>
<tr>
<td>データ プロバイダーを定義します。</td>
<td>トランザクション データを GTE に提供するデータ プロバイダーを作成します。</td>
<td>TaxableDocumentTypeDefinitionPurchaseInvoice<br>
TaxableDocumentDescriptorPurchaseInvoice</td>
</tr>
<tr>
<td rowspan="3">作成</td>
<td>トランザクションに<strong>税務書類</strong>ボタンを追加します。</td>
<td>トランザクション ページに<strong>税務書類</strong>ボタンを追加します。</td>
<td>VendEditInvoice<br>
VendInvoiceInfoListPage</td>
</tr>
<tr>
<td>トランザクションの合計と統合します。</td>
<td><strong>合計</strong>ボタンをクリックすると、税務書類を作成します。</td>
<td>PurchTotals_ParmTrans.calcTax()<br>
PurchTotals_ParmTransEdit.calcTax()<br>
PurchTotals_ParmTransEditInvoice.calcTax()</td>
</tr>
<tr>
<td>元伝票と統合します。</td>
<td>仕入請求書は元伝票トランザクションなので、税が計算されるときに元伝票を作成します。</td>
<td>AccDistRuleProductTaxMeasure<br>
AccJourRuleVendPaymReqTaxMeasure</td>
</tr>
<tr>
<td rowspan="2">削除 </td>
<td>トランザクションを削除します。</td>
<td>トランザクションが削除される場合、税務書類を削除します。</td>
<td>VendInvoiceInfoTable.delete()</td>
</tr>
<tr>
<td>トランザクション明細行を削除します。</td>
<td>トランザクション明細行が削除される場合に、税を再計算します。</td>
<td>VendInvoiceInfoLine.delete()</td>
</tr>
<tr>
<td rowspan="3">更新</td>
<td>トランザクション ヘッダー情報を更新します。</td>
<td>トランザクション ヘッダー レベルで税に影響するフィールドが更新されると、税を再計算します。</td>
<td>VendInvoiceInfoTable.update()</td>
</tr>
<tr>
<td>トランザクション明細行情報を更新します。</td>
<td>トランザクション明細行で税に影響するフィールドが更新されると、税を再計算します。</td>
<td>VendInvoiceInfoLine.update()</td>
</tr>
<tr>
<td>税情報を更新します。</td>
<td>税情報のフィールドが更新されると、税を再計算します。</td>
<td>TransTaxinformation.Write() (ページのデータ ソース)</td>
</tr>
<tr>
<td rowspan="5">転記</td>
<td>税務書類の移行ルールを定義します。</td>
<td>あるトランザクションから別のトランザクションへの税務書類の転送に関するルールを定義します。</td>
<td>TaxDocumentTransitRuleEventHandler.initTransitDocumentTransactionRuleList()</td>
</tr>
<tr>
<td>税務書類を転送します。</td>
<td>転記中にあるトランザクションから別のトランザクションに税務書類を転送します。</td>
<td>PurchaseInvoiceJournalCreate.endCreate()</td>
</tr>
<tr>
<td>税金を転記します。</td>
<td>トランザクションの転記時に、税を転記します。</td>
<td>PurchaseInvoiceJournalPost.PostTax()</td>
</tr>
<tr>
<td>在庫税を追加します。</td>
<td>在庫に対する課税が可能な場合は、在庫に税を追加します。</td>
<td>PurchaseInvoiceJournalPost.PostInventory()</td>
</tr>
<tr>
<td>税務書類を転記します。</td>
<td>トランザクションの伝票が転記された後に、税務書類を転記します。 結果として、税務書類のステータスが、<strong>転記済</strong>に更新され、レコードが関連テーブルに生成されます。</td>
<td>PurchaseInvoiceJournalPost.endUpdate()</td>
</tr>
<tr>
<td>照会</td>
<td>仕訳帳に<strong>税務書類</strong>ボタンを追加します。</td>
<td>照会用に、ジャーナル ページに<strong>税務書類</strong>ボタンを追加します。</td>
<td>VendInvoiceJournal</td>
</tr>
</table>

### <a name="define-a-taxable-document"></a>課税対象文書の定義

**TaxableDocumentTypeDefintionPurchaseInvoice** および **TaxableDocumentDescriptorPurchaseInvoice** は、税エンジンの課税対象文書として仕入請求書を定義するクラスです。

![課税対象文書クラス。](media/gte-classes-taxable-document.png)

TaxableDocumentTypeDefinitionPurchaseInvoice は、課税対象文書として仕入請求書を定義するインターフェイスです。

![仕入請求書の課税対象文書。](media/gte-purch-invoice-taxable-doc.png)

**TaxableDocumentDescriptorPurchaseInvoice.getDataProvider()** は、仕入請求書に使用されるデータ プロバイダー クラスを指定します。

![仕入請求書のデータ プロバイダー。](media/gte-data-provider-class-purch.png)

### <a name="define-data-providers"></a>データ プロバイダーの定義

次の図は、税関連の操作でトランザクション データを税エンジンに送信するために使用されるデータ プロバイダーを示しています。

![GTE のデータ プロバイダー。](media/gte-data-providers.png)

**TaxableDocPurchaseInvoiceDataProvider.buildQuery()** は、VendInvoiceInfoTable や VendInvoiceInfoLine など、すべての関連トランザクションに対するクエリを提供します。 また、行のデータ プロバイダーで各データ ソースを登録します。 たとえば、VendInvoiceInfoTable データ ソースは、TableDocVendInvoiceInfoTableRowDP で登録されます。

![VendInvoiceInfoTable データ ソース。](media/gte-example-vend-invoice.png)

TaxableDocVendInvoiceInfoTableRowDP は **TaxableDocPurchTableRowDataProvider** クラスを拡張してトランザクション ヘッダー関連情報を設定し、TaxableDocVendInvoiceInfoLineRowDP は **TaxableDocPurchLineRowDataProvider** を拡張して請求明細行関連の情報を設定します。

次の表に、Finance にマップされている課税対象文書フィールドの一覧を示します。

| 課税対象文書フィールド         | AOT オブジェクトのロジック                                                     | 必須                     | 既定値 |
|--------------------------------|-----------------------------------------------------------------------------|------------------------------|---------------|
| SubLines                       | TaxableDocumentLineObject.getSubLines                                       | 有                          | |
| フィールド                         | TaxableDocumentLineObject.getFields                                         | 有                          | |
| ModelFieldName                 | TaxableDocumentLineObject.parmModelFieldName                                | 有                          | |
| TaxAdjustment                  | TaxEngineIntegrationAXContractEventHandler.getLineAdjustment                | 無                           | |
| TableId                        | TaxableDocumentLineObject.getTransactionLineTableId                         | 有                          | |
|  Recid                          | TaxableDocumentLineObject.getTransactionLineRecordId                        | 有                          | |
| 課税対象文書タイプ          | TaxableDocumentDescriptor.createRow                                         | 有                          | |
| スキップ済 (ドキュメント レベル)       | TaxableDocumentDescriptor.createRow                                         | 有                          | 無 |
| DistributionSide               | TaxableDocumentObject.getDistributionSide                                   | 有                          | 自動 |
| ExchangeRates                  | TaxEngineIntegrationAXContractEventHandler.getExchangeRate                  | 有                          | |
| ReportingCurrencyExchangeRates | TaxEngineIntegrationAXContractEventHandler.getReportingCurrencyExchangeRate | 有                          | |
| 税務書類の目的           | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | 取引 |
| トランザクション通貨           | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | |
| トランザクション日付               | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | |
| スキップ済 (明細行レベル)           | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | 無 |
| 税提示方法                  | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | 消費税収入 |
| 元帳への転記                 | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | 有 |
| 会計の有効化              | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | 有 |
| 行タイプ                      | TaxableDocumentRowDataProviderLine.fillInFrameworkFields                    | 有                          | ライン |
| インポート注文                   | TaxableDocumentRowDataProviderHeader.fillInFields                           | 有                          | 無 |
| エクスポート注文                   | TaxableDocumentRowDataProviderHeader.fillInFields                           | 有                          | 無 |
| GST 構成スキーム         | TaxableDocumentRowDataProviderHeader.fillInFields                           | 有                          | 無 |
| 構成スキーム             | TaxableDocumentRowDataProviderHeader.fillInFields                           | 無                           | 無 |
| 顧客タイプ                  | TaxableDocumentRowDataProviderHeader.fillInFields                           | 有                          | なし |
| 仮評価         | TaxableDocumentRowDataProviderHeader.fillInFields                           | 無                           | 無 |
| 外部関係者                  | TaxableDocumentRowDataProviderHeader.fillInFields                           | なし                           | なし |
| 評価の種類              | TaxableDocumentRowDataProviderHeader.fillInFields                           | なし                           | 会社 |
| 優先的関係者            | TaxableDocumentRowDataProviderHeader.fillInFields                           | 無                           | 無 |
| GTA 商業仕入先          | TaxableDocumentRowDataProviderHeader.fillInFields                           | 無                           | 無 |
| 元帳通貨                | TaxableDocumentRowDataProviderHeader.fillInFields                           | 有                          | |
| 合計割引率      | TaxableDocumentRowDataProviderHeader.fillInFields                           | 無                           | |
| 免税                         | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 無 |
| 目的                        | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 取引 |
| 税込価格       | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 無 |
| 配送日                  | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| DiscountAmount                 | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| 正味金額                     | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| 件数                       | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| 消費状態              | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| 返金                         | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 無 |
| 処分アクション             | TaxableDocumentRowDataProviderLine.fillInFields                             | いいえ (返品あり)        | クレジット |
| 課税金額               | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | |
| 州間                    | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 無 |
| カスタム税率コードのインポート      | TaxableDocumentRowDataProviderLine.fillInFields                             | いいえ (インポート注文はあり) | |
| カスタム税率コードのエクスポート      | TaxableDocumentRowDataProviderLine.fillInFields                             | いいえ (エクスポート注文はあり) | |
| IEC 番号                     | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| 最大小売価格           | TaxableDocumentRowDataProviderLine.fillInFields                             | 無                           | |
| パーティ GST 登録番号  | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | |
| GST 登録番号        | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | |
| HSN コード                       | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | |
| SAC                            | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | |
| サービス カテゴリ               | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 内向き |
| ITC カテゴリ                   | TaxableDocumentRowDataProviderLine.fillInFields                             | 有                          | 入力 |
| 仕損                       | TaxableDocumentRowDataProviderLine.fillInFields                             | いいえ (販売注文はあり)   | 無 |

### <a name="add-the-tax-document-button-on-a-transaction"></a>トランザクションに税務書類ボタンを追加する

税エンジンで税計算をトリガーする 1 つの方法は、トランザクションに追加する **税務書類** ボタンを使用することです。 このボタンをクリックすると、トランザクション データが事前定義された課税対象文書オブジェクトとして税エンジンに送信され、税計算が税エンジンでトリガーされます。 ボタンは通常、**VendEditInvoice** などのトランザクション ページに追加されます。 税が計算された直後に、結果が税務書類のユーザー インターフェイス (UI) に表示されます。

![アクション ウィンドウの税務書類ボタン。](media/gte-vend-taxdocument.png)

![taxdocumentlauncher プロパティ。](media/gte-vend-taxdocumentlauncher.png)

### <a name="integrate-with-transaction-totals"></a>トランザクションの合計との統合

**合計** ボタンは税金額、割引額、合計額などのトランザクションの財務情報を表示するために使用されます。 合計ページに表示される税額も、仕訳帳の請求金額に追加されます。

Finance の既存の実装では、この機能を処理するために **PurchTotals** クラスのセットが作成されています。 したがって、税エンジン関連のコードがクラスの **calcTax** メソッドに挿入され、予想される税金の合計金額が確実に開始されるようになります。

![calcTax メソッド。](media/gte-trx-totals.png)

既存のロジックとの調整のため、既存の **taxTotal** パラメーターを使用して、トランザクション全体の税額を表示します。 **taxTotalGTE** という名前の新しいパラメーターは、仕入先に転記される税を表示するために使用されます。 逆請求など、場合によっては、**taxTotal** の値が **taxTotalGTE** の値と一致しません。 したがって、**taxTotal** が仕訳の転記に使用され、**taxTotalGTE** は **合計** ページで合計税額を表示するために使用されます。

### <a name="integrate-with-a-source-document"></a>元伝票との統合

仕入請求書は、元伝票のトランザクションです。 したがって、税エンジンから計算された税の結果は、Finance の既存の元伝票フレームワークと統合する必要があります。 主要なロジックはすでに完成しており、税エンジン統合フレームワークによって処理されています。 ただし、各元伝票トランザクションについては、配分ルールおよび仕訳ルールを会計目的で定義する必要があります。

![配分ルールと仕訳ルール。](media/gte-distribution-journalization-rule.png)

仕入請求書用に **AcctDistRuleProductTaxMeasure** および **AccJourRuleVendPaymReqTaxMeasure** の 2 つのクラスが作成されます。

![AcctDistRuleProductTaxMeasure クラス。](media/gte-class1.png)

![AccJourRuleVendPaymReqTaxMeasure クラス。](media/gte-class2.png)

元伝票クラスが正しく作成されると、配分ページには、計算された税金とコンポーネント ラベル、税額、および勘定科目が表示されます。

![勘定配布。](media/gte-accounting-distribution.png)

### <a name="delete-a-transaction"></a>トランザクションの削除

仕入請求書が削除されると、関連する税務書類も削除されます。 関連する税務書類を削除するには、VendInvoiceInfoTable の **削除** メソッドで TaxBusinessService を呼び出します。

![トランザクションの削除方法。](media/gte-delete-trx.png)

### <a name="delete-a-transaction-line"></a>トランザクション明細行を削除する

トランザクション明細行が削除されると、税務書類を再計算する必要があります。 パフォーマンス上の理由から、トランザクション明細行が削除された直後に GTE が税を再計算することはありません。 代わりに、税務書類のステータスを **ダーティー** に更新します。 表示または転記できるように税務書類が取得されると、GTE は状態が **ダーティー** かどうかを確認します。 ステータスによっては、再計算が行われます。

![税務書類のステータス。](media/gte-tax-doc-status1.png)

![税務書類のステータスの変更。](media/gte-tax-doc-status2.png)

### <a name="update-transaction-header-information"></a>トランザクション ヘッダー情報を更新する

一部のトランザクション ヘッダー情報は税の計算に影響を与えることがあります。 例には、トランザクションの日付と通貨が含まれます。 したがって、この種の情報が別の値に更新された場合は、後で再計算できるよう税務書類を **ダーティー** としてマークする必要があります。

![税務書類のダーティー ステータス。](media/gte-trx-header-info.png)

次の方法は、仕入請求書の税計算に影響を与える可能性のあるフィールドを一覧表示します。

![税計算に影響を与えるフィールドを一覧表示する方法。](media/gte-tax-calc-purchase.png)

### <a name="update-transaction-line-information"></a>トランザクション明細行情報を更新する

同様に、いくつかのトランザクション明細行フィールドの更新も、税計算に影響します。

![税計算に影響を与えるトランザクション明細行。](media/gte-update-trx-line-info.png)

### <a name="update-tax-information"></a>税情報を更新する

トランザクション明細行の税情報は、税計算に大きな影響を与えます。 ロジックはアプリケーション オブジェクト ツリー (AOT) **TransTaxInformation** ページで管理されています。 このページはそれ以上の取得を必要としない可能性があります。

### <a name="define-a-tax-document-transit-rule"></a>税務書類の輸送ルールを定義する

仕入請求書および仕訳帳に税務書類を関連付けるには、ルールを定義する必要があります。 **TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleList()** では、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、VendInvoiceTrans の各ルールを定義して、税務書類または税務書類行をトランザクション テーブルに関連付ける必要があります。

![税務書類の輸送ルール。](media/gte-tax-doc-transit-rule.png)

**TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleExtList()** には、トランザクションから仕訳帳への輸送アクションの拡張ルールの定義が含まれています。

![税務書類の輸送ルールの拡張。](media/gte-tax-doc-transit-rule-ext.png)

### <a name="transfer-a-tax-document"></a>税務書類を転送する

トランザクションから仕訳帳が作成される場合、税務書類を仕訳帳に転送する必要があります。 次のコードは、税務書類を仕入請求書から仕入請求書の仕訳帳に転送します。

![税務書類を転送します。](media/gte-transfer-tax-document.png)

### <a name="post-tax"></a>税を転記する

税の転記は、仕入請求書の仕訳帳が転記されるときに発生します。 したがって、**FormLetterJournalPost.postTax()** 基本クラスで **TaxBusinessService::PostTax()** が仕入請求書の仕訳帳を転記するために呼び出されます。

![税の転記。](media/gte-post-tax.png)

### <a name="add-inventory-tax"></a>在庫税を追加する

在庫に転記する必要がある税は、在庫トランザクションに追加する必要があります。

次の例は、**taxEngineInventMovement().updateTaxFinancial()** クラス メソッドを使用して、在庫に対する税を転記する **在庫** モジュールのロジックを示しています。

![在庫税を追加する。](media/gte-purchinvoicejournalpost.png)

### <a name="post-a-tax-document"></a>税務書類を転記する

税が転記されたら、税務書類を転記したことを示すステータスに税務書類を更新する必要があります。

![税務書類を転記します。](media/gte-tax-document-status.png)

上記のメソッドが呼び出されると、GeneralDournalEntry と仕訳帳トランザクションの関係を維持するために、TaxDocumentGeneralJournalEntryLink テーブルに追加のレコードが作成されます。 このレコードは GTE が GeneralJournalEntry レベルで税務書類を簡単に取得するのに役立ちます。

![税務書類の仕訳帳入力。](media/gte-taxdocumentgeneraljournalentrylink.png)

## <a name="debugging"></a>デバッグ

税エンジンのデバッグは、主にトランザクション データの検証と計算された税務書類の結果に基づいて行われます。 トランザクションデータと計算結果はどちらも JavaScript Object Notation (JSON) 文字列形式です。

### <a name="debugging-transaction-data"></a>トランザクション データのデバッグ

次の図に示すように、**TaxEngineServiceProxy.calculate()** にブレークポイントを設定します。

![トランザクション データのデバッグ。](media/gte-debug-transaction-data.png)

**JsonStr** には、データ プロバイダーによって作成されたすべてのトランザクション データ情報が含まれています。 オンラインの JSON ビューアーを使用して、税モデルの属性にデータが正しく設定されているかどうかを簡単に識別できます。

### <a name="debugging-the-tax-document"></a>税務書類のデバッグ

税エンジンが計算に対してエラーを返した場合、すべての結果は上記のメソッドの **RET** 属性に設定されます。 属性にクイック ウォッチ コマンドを使用すると、税エンジンからの完全なエラーを簡単に理解できます。

税エンジンが問題を返さない場合、税務書類の結果は以下の表に保持されます。

- TaxDocument
- TaxDocumentRow
- TaxDocumentJson

これらのテーブルを照会して JSON 文字列を取得することで、オンラインの JSON ビューアーを介して結果の詳細を簡単に確認できます。

## <a name="additional-resources"></a>追加リソース

- [税エンジンの概要](tax-engine.md)
- [税エンジン コンフィギュレーションの拡張](extend-tax-engine-configurations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
