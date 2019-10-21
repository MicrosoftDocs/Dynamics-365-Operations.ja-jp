---
title: 承認テスト ライブラリのエンティティ
description: このトピックでは、データと関連する動作を表すテスト エンティティ クラスについて説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 85e44f64310472fa39deed20df4faaf928279d92
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191814"
---
# <a name="entities-in-the-acceptance-test-library"></a>承認テスト ライブラリのエンティティ

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

テスト エンティティ クラスは、単一の概念として認識されるデータと動作を表します。 テスト エンティティ クラスは **販売注文**、**移動オーダー**、そして **リリースされた製品** のようなページに基づいています。 テスト エンティティ クラスは、テスト シナリオで最も頻繁に使用されるプロパティと、テスト データの設定やシナリオ テストの観点から最も重要な動作を公開します。

承認テスト ライブラリ (ATL) のエンティティには、次のメソッドが **必ず** 必要です:

+ エンティティのプロパティを取得および設定するために使用されるプロパティ メソッド。
+ エンティティ プロパティを Fluent な方法で設定できるように有効化する Fluent セッター メソッド。
+ エンティティをデータベースに保存するメソッド。

ATL のエンティティは、次のメソッドを持つことが *可能* です:

+ エンティティに関連する事業運営を公開するために使用されるアクション メソッド。
+ コンポーネントおよび関連エンティティに対してナビゲーションを有効にするのに使用されるクエリ メソッド。

## <a name="naming-convention"></a>名前付け規則

`[AtlEntity]<ModuleName><EntityName>`

この命名規則で:

+ `<ModuleName>` はメイン メニューのモジュール名に基づいています。 短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。
+ `<EntityName>` はテーブル名の代わりにユーザー インターフェイス (UI) 名に基づいています。 たとえば、`SalesTable` ではなく `SalesOrder` を使用します。

エンティティに 2 つの UI 名がある場合は、短い方の名前を使用できます。 たとえば、代替可能な名前であるため `ReleasedProduct` の代わりに `Item` を使用できます。

### <a name="examples"></a>例

```
AtlEntitySalesOrder

AtlEntityTransferOrderLine
```

## <a name="property-methods"></a>プロパティ メソッド

テスト エンティティの主な目的のひとつは、データを公開することです。 エンティティのプロパティは `parm` (プロパティ) メソッドを使用して設定または取得できます。

### <a name="primitive-type-properties"></a>プリミティブ型のプロパティ

プリミティブ型のプロパティを公開するための `parm` メソッドを作成します。

#### <a name="example"></a>例

```
public SalesQty parmQuantity(SalesQty _qty = 0)
{
    if (!prmisDefault(_qty))
    { // setter
        salesLine.SalesQty = _qty;
        this.onSalesQtyOrInventDimChange();
    }
    return salesLine.SalesQty;
}
```

### <a name="entity-references"></a>エンティティ参照

たとえば `AtlEntityCustomer` という名前の顧客エンティティがある場合、`AtlEntitySalesOrder` エンティティのプロパティ メソッドとして `customer` への参照を公開する必要があります。

```
public AtlEntityCustomer parmCustomer(AtlEntityCustomer _custTable = null)
```

プロパティ メソッドをセッターやゲッターとして使用できます。

```
salesOrder.parmCustomer(customer); // setter

customer = salesOrder.parmCustomer(); // getter
```

#### <a name="entity-reference-methods-naming-conventions"></a>エンティティ参照メソッドの命名規則

プロパティ メソッドを識別するために `parm` プレフィックスを使用する必要があります。 エンティティ参照プロパティを公開するときは、アプリケーション オブジェクト ツリー (AOT) 名の代わりにフィールドの UI 名を使用します。 UI 名に `Id`、`Code`、または `Number` 接尾語が含まれている場合は、その接尾語を省略します。 たとえば、`parmItemNumber` の代わりに `parmItem` を使用します。

### <a name="record-references"></a>レコード参照

顧客エンティティがまだ作成されておらず、近い将来にも作成されない場合、参照プロパティは対応するレコード バッファ (`CustTable`) を公開する必要があります。

```
public CustTable parmCustomer(CustTable _custTable = null)
```

#### <a name="record-reference-naming-conventions"></a>レコード参照の命名規則

エンティティ参照に使用されているのと同じ命名規則を使用してください。

### <a name="id-references"></a>ID 参照

エンティティやレコード参照を持つことに加えて、`Id` 参照プロパティを導入できます。

```
public CustAccount customerId(CustAccount _custTable = null)
```

対応するエンティティまたはバッファー参照も導入しない限り、`Id` 参照を導入しないでください。 `Id` 参照は、エンティティやバッファー参照メソッドへのショートカットです。 `Id` 参照の実装は、エンティティやバッファー参照に呼び出しを委任する必要があります。

#### <a name="id-reference-naming-conventions"></a>ID 参照の命名規則

`Id`、`Number`、`Account`、`Code`、また `Name` などの語句が含まれる場合は UI 名を使用してください。 それ以外の場合、エンティティやレコード参照の名前に適切な接尾語を追加します。

#### <a name="id-reference-methods-contract"></a>ID 参照メソッドの契約

`Id` 参照メソッドは参照エンティティを見つけるために常に提供された `Id` を使用し、そしてエンティティやレコード参照メソッドに呼び出しを委任します。 指定された `Id` 値に基づいてエンティティやレコードが見つからない場合は、エラー メッセージがスローされます。

## <a name="fluent-setter-methods"></a>Fluent セッター メソッド

Fluent な初期化とエンティティの変更をサポートする Fluent なセッター メソッドを作成します。

### <a name="declaration-example"></a>宣言の例

```
public AtlEntitySalesLine setQty(SalesQty _qty)
```
    
### <a name="code-example"></a>コードの例

```
salesLine.setItem(batchItem).setInventDims([warehouse]).setQty(10).save();
```

### <a name="naming-convention"></a>名前付け規則

`set<PropertyName>`

この命名規則では `<PropertyName>` が対応するプロパティ メソッドの名前で使用されているものと一致する必要があります。

## <a name="action-methods"></a>アクション メソッド

エンティティはデータだけでなく関連するアクションも表します。 アクションは単純なアクション メソッドとしても、コマンド オブジェクト初期化子としても実装できます。

### <a name="simple-action-methods"></a>単純なアクション メソッド

単純なアクション メソッドは、完全なアクションを表します。 これらを Fluent に連鎖してはいけません。 例外は `save` メソッドで、Fluent である必要があります。

#### <a name="naming-convention"></a>名前付け規則

`<ExecuteBusinessOperation>`

この命名規則では `<ExecuteBusinessOperation>` は事業運営を表す動詞です。 それは UI のメニュー項目で使用されているのと同じ用語である必要があります。

#### <a name="examples"></a>例

```
salesOrder.save();

salesOrder.postInvoice();
```

### <a name="command-object-initializers"></a>コマンド オブジェクト初期化子

コマンド オブジェクト初期化子は、コマンドのパラメーターを指定し実行できるコマンド オブジェクトを返します。

```
transferLine.pick().setQty(10).setWMSLocation(bulkLocation).execute();
```

#### <a name="naming-convention"></a>名前付け規則

`<ExecuteBusinessOperation>`

この命名規則では `<ExecuteBusinessOperation>` は事業運営を表す動詞です。 それは UI のメニュー項目で使用されているのと同じ用語である必要があります。

#### <a name="examples"></a>例

```
salesOrder.pick().execute();

purchaseOrder.register().execute();
```

### <a name="action-entities"></a>アクション エンティティ

エンティティで利用可能ないくつかのアクションは、エンティティそのものと考えることができます。 仕入先の請求書がひとつの例です。 請求書を転記する前に、請求書のパラメータを設定し、行を編集して、後のために請求書を保存することができます。 これらのコマンドは、個別のエンティティ クラスを導入できます。

#### <a name="naming-convention"></a>名前付け規則

`new<ActionName>`

この命名規則では `<ActionName>` は事業運営を表す名詞です。 名前は事業運営の UI 名にする必要があります。

#### <a name="example"></a>例

```
receipt = transfer.newReceipt().setEditLines(true).setExplodeLines(true);
receipt.lines().withBatch(batch1).single().setReceiptQty(6).setScrapQty(1).save();
receipt.lines().withBatch(batch2).single().setReceiptQty(4).setScrapQty(1).save();
receipt.post();
```

#### <a name="class-naming-convention"></a>クラスの命名規則

`AtlEntity<ModuleName><EntityName><ActionName>`

#### <a name="example"></a>例

```
AtlEntityInventTransferOrderReceipt
```

## <a name="adding-components"></a>コンポーネントの追加

コンポジションは複合エンティティがコンポーネント パーツの配置に対して唯一の責任を持つ関係です。 複合オブジェクトがコンポーネントの所有権を持っているため、複合とコンポーネントの関係は強い "持っている" の関係です。 したがって、複合はコンポーネント パーツの作成と破棄を担当します。

オブジェクト インスタンスのひとつを、ひとつの複合の一部にすることができます。 複合オブジェクトが破棄された場合は、すべてのコンポーネント パーツを破棄する必要があります。 コンポーネント パーツは複合オブジェクトの外部に独立した存在を持たず、他のオブジェクトに転送することはできません。 コンポーネント パーツは通常は複合オブジェクトのメンバーであるため、合成はカプセル化を強制します。

複合オブジェクトの例は、元伝票行で構成されている元伝票です。

### <a name="example"></a>例

元伝票の例では、ドキュメント エンティティは複合ルートとして機能し、ドキュメント行の新しいインスタンスの作成に責任があります。 この場合、元伝票エンティティはドキュメントの新しい行を初期化して返す `addLine()` メソッドを持ちます。


```
public AtlEntitySalesLine addLine()
```

`addLine()` メソッドは、行オブジェクト (この例では `salesLine`) を行のコレクションに追加して、アプリケーション プログラミング インターフェイス (API) の Fluent を維持するために親エンティティ (この例では `SalesOrder`) を返します。 新しい行を作成するには、`newLine()` メソッドを作成します。

### <a name="naming-convention-for-adding-components"></a>コンポーネント追加の命名規則

コンポーネントを追加するメソッドは、ボタンの UI 名を使う必要があります。

#### <a name="example"></a>例

```
salesLine = salesOrder.addLine();
```

### <a name="component-collections"></a>コンポーネント コレクション

クエリ メソッドを使用してコンポーネントを検索できます。

#### <a name="naming-convention-for-component-collections"></a>コンポーネント コレクションの命名規則

コンポーネント コレクションにアクセスするメソッドは、ホスティング ページのグリッドの UI 名を使用する必要があります。

## <a name="query-methods"></a>クエリ メソッド

エンティティのクエリ メソッドを使用して、コンポーネントと関連エンティティを検索できます。

### <a name="example"></a>例

```
transferOrderLine = transferOrder.lines().withItem(item).single();
```

この例では、`lines()` は `AtlQueryTransferOrderLines` クエリを返すクエリ メソッドです。 このクエリは既にフィルターされてるため、`lines()` メソッドが呼び出された移動オーダーの移動オーダー行のみを返します。

### <a name="naming-convention"></a>名前付け規則

可能な限り UI 名を使用してください。 UI 名がテスト自動化に使用するのに長すぎる場合は、省略形を使用できます。

### <a name="example"></a>例

```
public AtlQueryWHSLoadLines lines()
{
    return new AtlQueryWHSLoadLines().forLoadId(this.parmLoadId());
}
```

## <a name="additional-resources"></a>追加リソース

[承認テスト ライブラリのクエリ](concepts-queries.md)
