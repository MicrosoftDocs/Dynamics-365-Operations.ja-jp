---
title: 拡張機能を使用した税統合へのデータ フィールドの追加
description: この記事では、X++ 拡張機能を使用して税統合のデータ フィールドを追加する方法について説明します。
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 184012dcc0b68e017bb28d8d73caa9e8415bdbfa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871052"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>拡張機能を使用した税統合のデータ フィールドの追加

[!include [banner](../includes/banner.md)]


この記事では、X++ 拡張機能を使用して税統合のデータ フィールドを追加する方法について説明します。 これらのフィールドは、税サービスの税データ モデルに拡張し、税コードを決定するために使用できます。 詳細については、[税コンフィギュレーションにデータ フィールドを追加する](tax-service-add-data-fields-tax-configurations.md)を参照してください。

## <a name="data-model"></a>データ モデル

データ モデルのデータはオブジェクトによって転送され、クラスによって実装されます。

主なオブジェクトの一覧を次に示します。

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

次の図に、これらのオブジェクトを関連付ける方法を示します。

[![データ モデル オブジェクト リレーションシップ。](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

**Document** オブジェクトには 多数の **Document** オブジェクトを含めることができます。 各オブジェクトには、税サービスのメタデータが含まれます。

- `TaxIntegrationDocumentObject` には、ソース アドレスと `includingTax` メタデータに関する情報を含む `originAddress` メタデータがあり、その行に売上税が含まれるかどうかが示されます。
- `TaxIntegrationLineObject`には、`itemId`、`quantity`、および`categoryId` メタデータが含まれます。

> [!NOTE]
> `TaxIntegrationLineObject` には、**Charge** オブジェクトも実装されます。

## <a name="integration-flow"></a>統合フロー

フロー内のデータは活動によって操作されます。

### <a name="key-activities"></a>主な活動

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

活動は次の順序で実行されます。

1. 取得の設定
2. データ取得
3. 計算サービス
4. 通貨為替
5. データ持続性

たとえば、**計算サービス** の前に **データ取得** を拡張します。

#### <a name="data-retrieval-activities"></a>データ取得活動

**データ取得** 活動は、データベースからデータを取得します。 さまざまなトランザクションに対するアダプタにより、次の異なるトランザクション テーブルからデータを取得できます。

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

これらの **データ取得** 活動では、データベースから `TaxIntegrationDocumentObject` と `TaxIntegrationLineObject` にデータがコピーされます。 これらの活動はすべて同じ抽象テンプレート クラスを拡張するので、メソッドは共通です。

#### <a name="calculation-service-activities"></a>計算サービス活動

**税計算** 活動は、税サービスと税統合の間のリンクです。 この活動は、次の機能を担当します。

1. 要求を作成する。
2. 税務サービスへ要求を転記する。
3. 税サービスから応答を取得する。
4. 応答を解析する。

要求に追加するデータ フィールドは、他のメタデータと共に転記されます。 

## <a name="extension-implementation"></a>拡張機能の実装

ここでは、拡張機能の実装方法を説明する詳細な手順を示します。 例として **コスト センター** と **プロジェクト** の財務分析コードが使用されます。

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>手順 1 オブジェクト クラスにデータ変数を追加する

オブジェクト クラスには、データ変数およびデータの getter/setter メソッドが含まれています。 フィールドのレベルに応じて、`TaxIntegrationDocumentObject` または `TaxIntegrationLineObject` にデータ フィールドを追加します。 次の例では行レベルを使用し、ファイル名は `TaxIntegrationLineObject_Extension.xpp` です。

> [!NOTE]
> 追加するデータ フィールドがドキュメント レベルの場合は、ファイル名を `TaxIntegrationDocumentObject_Extension.xpp` に変更します。

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**コスト センター** と **プロジェクト** が、プライベート変数として追加されます。 これらのデータ フィールドでデータを操作するための getter メソッドおよび Setter メソッドを作成します。

### <a name="step-2-retrieve-data-from-the-database"></a>手順 2 データベースからデータを取得する

トランザクションを指定し、適切なアダプタ クラスを拡張してデータを取得します。 たとえば、**発注書** トランザクションを使用する場合は、`TaxIntegrationPurchTableDataRetrieval` および `TaxIntegrationVendInvoiceInfoTableDataRetrieval` を拡張する必要があります。 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` は、`TaxIntegrationPurchTableDataRetrieval` から継承されています。 `purchTable` と `purchParmTable` テーブルのロジックが異なる場合以外、変更することはできません。

すべてのトランザクションにデータ フィールドを追加する必要がある場合は、すべての `DataRetrieval` クラスを拡張します。

すべての **データ取得** 活動は同じテンプレート クラスを拡張するため、クラス構造、変数、およびメソッドは類似しています。

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

次の例では、`PurchTable` テーブルを使用する場合の基本的な構造を示します。

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

`CopyToDocument` メソッドが呼び出されたとき、`this.purchTable` バッファは既に存在します。 このメソッドの目的は、`DocumentObject` クラスで作成された Setter メソッドを使用して、必要なすべてのデータを `this.purchTable` から `document` オブジェクトにコピーすることです。

同様に、`CopyToLine` メソッドには `this.purchLine` バッファが既に存在します。 このメソッドの目的は、`LineObject` クラスで作成された Setter メソッドを使用して、必要なすべてのデータを `this.purchLine` から `_line` オブジェクトにコピーすることです。

最も単純な方法は、`CopyToDocument` と `CopyToLine` メソッドを拡張する方法です。 ただし、最初に `copyToDocumentFromHeaderTable` と `copyToLineFromLineTable` メソッドを試することをお勧めします。 希望通りに機能しない場合、独自のメソッドを実装し、`CopyToDocument` と `CopyToLine` で呼び出 します 。 このメソッドを使用できる一般的な状況には次の 3 種類があります。

- 必須フィールドは、`PurchTable` または `PurchLine` にあります。 この場合、`copyToDocumentFromHeaderTable` と `copyToLineFromLineTable` を拡張できます。 サンプル コードを次に示します。

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- 必要なデータは、トランザクションの既定テーブルにはありません。 ただし、既定のテーブルとの結合リレーションシップがいくつかあるため、フィールドはほとんどの行で必須です。 この場合は、`getDocumentQueryObject` または `getLineObject` を置換して、結合リレーションシップによってテーブルをクエリします。 次の例では、**今すぐ配送** フィールドが行レベルで販売注文と統合されています。

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    この例では、`mcrSalesLineDropShipment` バッファが申告され、クエリが `getLineQueryObject` で定義されています。 クエリは、リレーションシップ `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId` を使用します。 この状況を拡張している間、`getLineQueryObject` を独自に作成したクエリ オブジェクトで置換できます。 ただし、次の点に留意してください。

    * `getLineQueryObject` メソッドの戻り値は `SysDaQueryObject` なので、SysDa法を使用してこの オブジェクトを作成する必要があります。
    * 存在するテーブルは削除できません。

- 必須データがトランザクション テーブルに複雑な結合リレーションシップで関連付けられている、またはリレーションシップが 1 対 1 (1:1) ではなく 1 対多 (1:N) です。 そのような状況では、少し複雑になります。 このような状況は、財務分析コードの例に適用されます。 

    この場合、独自のメソッドを実装してデータを取得できます。 `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` ファイル内のサンプル コードを次に示します。

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>手順 3 要求へデータを追加する

`copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` または `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` メソッドを拡張して、データを要求に追加します。 `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` ファイル内のサンプル コードを次に示します。

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

このコードでは `_destination` が要求の生成に使用されるラッパー オブジェクトであり、`_source` が `TaxIntegrationLineObject` オブジェクトになります。

> [!NOTE]
> 要求内で **private const str** として使用されるフィールド名を定義します。 文字列は、[税コンフィギュレーションへのデータ フィールドの追加](tax-service-add-data-fields-tax-configurations.md)の記事で追加したノード名 (ラベルではない) と同じである必要があります。
> 
> **SetField** メソッドを使用して、**copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** メソッドのフィールドを設定します。 2 番目のパラメータのデータ型は、**文字列** である必要があります。 データ型が **文字列** でない場合、文字列に変換します。
> データ型が X++ **列挙型** の場合、**enum2Symbol** メソッドを使用して列挙値を文字列に変換することをお勧めします。 税コンフィギュレーションで追加する列挙値は、列挙名と完全に同じにしてください。 次に、列挙値、ラベル、および名前の違いのリストを示します。
> 
>   - 列挙型の名前は、コード内のシンボル名です。 **enum2Symbol()** は、列挙値を名前に変換することができます。
>   - 列挙値は整数です。
>   - 列挙のラベルは、優先する言語で異なる場合があります。 **enum2Str()** は、列挙値をラベルに変換することができます。

## <a name="model-dependency"></a>モデルの依存関係

プロジェクトを正常に構築するには、次の参照モデルをモデルの依存関係に追加します。

- ApplicationPlatform
- ApplicationSuite
- 税エンジン
- 分析コード (財務分析コードが使用されている場合)
- コード内で参照されるその他の必要なモデル

## <a name="validation"></a>検証

前の手順を完了したら、プロジェクトをビルドして変更を検証できます。

1. 財務で、**買掛金管理** に移動し、**&debug=vs%2CconfirmExit&** を URL に追加します。 たとえば、`https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&`。 最後の **&** は必須です。
2. **発注書** ページを開いて、**新規** を選択して発注書を作成します。
3. カスタマイズされたフィールドの値を設定し、**売上税** を選択します。 接頭語が付けられているトラブルシューティング ファイルである **TaxServiceTroubleshootingLog** は自動的にダウンロードされます。 このファイルには、税務計算サービスに転記されたトランザクション情報が含まれます。 
4. カスタマイズされた追加フィールドが **税計算入力 JSON** セクションに存在し、値が正しいことを確認します。 値の変更が修正しない場合は、このドキュメントの手順をダブルクリックします。

ファイルの例:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>付録

この付録では、財務分析コード (**コスト センター** および **プロジェクト**) を明細行レベルで統合する完全なサンプル コードを示しています。

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
