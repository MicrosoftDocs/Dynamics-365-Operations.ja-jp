---
title: 分析コード エントリ コントロールの取得
description: 分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 25551
ms.assetid: dbc5c0af-ae97-463e-b5ff-9bfd242529ff
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b1ddde8008c5473eb28605e99e2de3c59d03ca6
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066164"
---
# <a name="uptake-of-dimension-entry-controls"></a>分析コード エントリ コントロールの取得

[!include [banner](../includes/banner.md)]

分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。

## <a name="general-approach"></a>一般的なアプローチ

設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。 この設計に合わせて、LedgerDimensionEntryController、LedgerDefaultDimensionEntryController などのように、**すべてのフォームは直接コントローラー クラスではなく、分析コードのエントリ コントロール インスタンス API のみと対話する必要があります**。操作されたプロパティおよびコントローラーで呼び出されたメソッドは、コントロールで呼び出される必要があります。

**メモ :**

-   アップグレード スクリプトは、constructInGroupWithValues() メソッドおよび constructInTabWithValues() メソッドを使用して作成された分析コード エントリ コントロールのみを処理します。 他のコントロールは、手動でアップグレードする必要があります。
-   アップグレード スクリプトは、ヘルパー メソッドのパラメーターとして送信された分析コード エントリ コントロールを処理しません。 このコードは、手動でアップグレードする必要があります。
-   Dynamics AX 2012 では、既定の分析コード コントロールのコンテナーは、「必要なアクセス許可」 = 手動に設定することでセキュリティ保護可能なコントロールとして定義できました。 コントロールへのアクセスは、セキュリティ モデルで付与されているため、アクセスを正しく表示および管理することができました。 既定の分析コードのコントロールは、デザイン時のエクスペリエンスになりました。 したがって、フォームでは、コントロールのコンテナーを保護可能なコントロールとして定義する必要がなくなりました。 ほとんどの場合、手動の設定を削除するためにメタデータを制御するフォームを更新して、セキュリティ モデルのコントロールへの参照を削除する必要があります。 Dimension Entry コントロールに対して細かいセキュリティ制御を維持するために使用される場合、この設定は [手動] のままにすることができます。
-   Dynamics AX 2012 では、parmAttributeSetDataSource および parmAttributeValueSetDataSource がデータ ソースと既定の分析コード コントロールに関連付けられたデータ ソースのフィールドを設定するために使用されていました。  これらは通常、DimensionDefaultingController インスタンスを作成した直後にフォームの init メソッドで設定されていました。  すべての呼び出し parmAttributeSetDataSource および parmAttributeValueSetDataSource はアップグレード後に削除されます。  これらの呼び出しの値を使用して、アップグレードされたコントロールのメタデータを設定します。  アップグレード後、これらの呼び出しをすべて削除した後、フォームが正常に機能していることを確認するために、フォームをチェックする必要があります。
-   ディメンション入力コントロールはフォーム デザインでモデル化されるようになりました。 分析コードの入力管理を検索するには、デザイン要素を展開するか、フォーム デザインで "DimensionEntry" を検索します。 デザイン時に新しいコントロールがどのようなものかを次に示します。

[![新しいプロジェクト ダイアログ。](./media/1.png)](./media/1.png)

## <a name="properties"></a>プロパティ
分析コード エントリ コントロールのカスタム プロパティは、**コントローラー** グループの下にあります。

[![コントローラーのプロパティ。](./media/capture1.png)](./media/capture1.png)

#### <a name="details-on-the-properties"></a>プロパティの詳細

| プロパティ     | 有効な値            | 用途 |
|------------------|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| キャプション テキスト     | すべてのラベル                                                                                | コントロールのキャプション。                                                                                                                                           |
| コントローラー クラス | 8 つのコントローラー クラスのうちの 1 つです。 たとえば、LedgerDefaultDimensionEntryController      | 分析コード エントリ コントロールの動作を決定します。 このプロパティの詳細については以下で説明します。                                                    |
| データ ソース      | フォーム データ ソース一覧のデータ ソース                                             | ここで指定するデータソースは、値データフィールドプロパティおよび/または列挙データフィールドプロパティで指定したフィールドを保持するテーブルをポイントする必要があります。 |
| 列挙データ フィールド  | データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。 | これは、列挙型に格納されているフィールドです。 コントロールが列挙を使用していない場合は、このプロパティを指定しないでください。                  |
| 列挙      | 任意の列挙。 たとえば、NoYes                                                      | コントロールで使用する列挙型です。 列挙型は、分析コード値の代わりにコントロールによって使用されます。                                                      |
| 値 データ フィールド | データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。 | これは、分析コード エントリ コントロールがバインドされているフィールドです。                                                                                                    |

## <a name="controller-class-property"></a>コントローラー クラス プロパティ
各コントローラーの詳細は、以下のテーブルを参照してください。

| コントローラー                                 | 細目  |
|------------------------------------------------|------------------|
| BudgetDefaultDimensionValueSet                 | このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、予算ベースでサポートしています。 予算の既定分析コードでは、主勘定分析コードが必要です。                                                                                                                                                    |
| PurchReqDefaultDimensionValueSet               | このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、PurchReq ベースでサポートしています。 PurchReq の既定分析コードでは、主勘定分析コードが必要です。                                                                                                                                                |
| LedgerDefaultDimensionValueSet                 | このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、元帳ベースでサポートしています。 既定の分析コードでは、値が指定されていない行の名前列に「既定値なし」という語句が表示されている必要があります。 このコントローラーは、通常、設定、マスター データ、およびヘッダー レコードで使用します。 |
| LedgerDimensionValueSet                        | このコントローラーは、分析コード エントリ コントロールのデータ入力の元帳に基づくサポートを提供します。 このコントローラーは通常、明細行品目またはトランザクション データに使用されます。                                                                                                                                                      |
| InventSiteLockedDimensionValueSet              | このコントローラーは、InventSite フォーム専用の分析コード エントリ コントロールのデータ入力をサポートします。                                                                                                                                                                                                      |
| InventSiteLinkedDimensionValueSet              | このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。 このコントローラーでは、会社が変更されたときに、特別な方法で、コントロールを更新します。                                                                                         |
| InventSiteSMAItemDimensionValueSet             | このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。                                                                                                                                                                           |
| InventSiteTmpLedgerBaseLinkedDimensionValueSet | このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。 このコントローラーは、特に TmpLedgerBase テーブルの DefaultDimension フィールドで動作します。                                                                            |

いくつかの分析コード入力コントロールには、コントローラー プロパティが設定されていない可能性があります。 この場合、コントローラーはコントロールの値データ フィールドの EDT から推測されます。 一連の分析コード エントリ コントロールの特定のプロパティを以下に示します。 これらのプロパティは、上記の一般的なアプローチのセクション (DimensionEntryControlHeader) で選択した、分析コード入力コントロールの PurchTable フォームのプロパティです。 この分析コード エントリ コントロールは、PurchTableのTable テーブルの DefaultDimension フィールドを使用しています。 PurchTable の DefaultDimension フィールドの拡張データ型プロパティは、LedgerDefaultDimensionValueSet (以下を参照) に設定されます。 実行時に、この EDT は LedgerDefaultDimensionEntryController にマップされます。 したがって、この場合 DimensionEntryControlHeader コントロールは LedgerDefaultDimensionEntryController を使用します。 次の例は、EDT とそれがマップされているコントローラーを示しています。

![新しい品目を追加。](./media/3.png)

![リソース ファイルの選択。](./media/4.png)

#### <a name="extended-data-types-and-the-controllers-they-are-mapped-to"></a>拡張データ型およびマップされるコントローラー

| 拡張データ型                         | コントローラー                                        |
|------------------------------------------------|-------------------------------------------------------|
| BudgetDefaultDimensionValueSet                 | BudgetDefaultDimensionEntryController                 |
| PurchReqDefaultDimensionValueSet               | PurchReqDefaultDimensionEntryController               |
| LedgerDefaultDimensionValueSet                 | LedgerDefaultDimensionEntryController                 |
| LedgerDimensionValueSet                        | LedgerDimensionEntryController                        |
| InventSiteLockedDimensionValueSet              | InventSiteLockedDimensionEntryController              |
| InventSiteLinkedDimensionValueSet              | InventSiteLinkedDimensionEntryController              |
| InventSiteSMAItemDimensionValueSet             | InventSiteSMAItemDimensionEntryController             |
| InventSiteTmpLedgerBaseLinkedDimensionValueSet | InventSiteTmpLedgerBaseLinked-<br>DimensionEntryController |

## <a name="upgrade-script-todos"></a>スクリプト TODO のアップグレード
### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.reactivate();
```

### <a name="finance-and-operations"></a>財務と運用
reactivate メソッドは、分析コード エントリ コントロールを現在の設定でリフレッシュします。 このメソッドは、会社または表示された分析コード リストが変更された場合にのみ、コントロールを更新します。 この呼び出しは、これらのどちらも以前に変更されていない場合に削除できます。 それ以外の場合は、呼び出しはそのままにします。 reactivate() の直前で parmCompany() が呼び出され、それが reactivate() より前に呼び出された唯一の DEC API であり、そのメソッドがデータソースの active() 中に呼び出された場合、最適化を手動で行うことでパフォーマンスを向上させ、コードの取り込みを削減することができます。

1.  データ ソースのアクティブ プロセス中に、parmCompany() および reactivate() 呼び出しを削除します。
2.  最初のユーザーとフォームとのやりとりの前に呼び出されるフォーム init()、run()、datasource init()、または同様のメソッドでは、次のコード行を追加します。

    ```xpp
    DimensionEntryControl.parmCompanyReference(
        fieldStr([myTable], [myCompanyContextField]);
    ```

    この変更により、DEC はアクティブなレコードが変更されたときに更新される会社フィールド参照を自動的に見つけ出し、それに応じてディメンションのリストを更新できます。

> [!NOTE]
> これを parmDisplayedDimensionSet() の使用と組み合わせないでください。そうすると、分析コードの一覧が想定外のものになることがあります。 会社の選択フィールドの変更されたメソッドなど、他のすべての場所で、データ ソースがその時点で読み取られるプロセスではないため、会社内の変更をすぐに反映するように parmCompany() を呼び出す必要があります。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.setEditability(true, 0);
```


### <a name="finance-and-operations"></a>財務と運用
特定の編集可能なディメンション セットが必要な場合は、この呼び出しを次のように置き換えます。

```xpp
DimensionEntryControl.parmEditableDimensionSet(
    editableDimensionSet);
```

> [!NOTE]
> editableDimensionSet パラメーターのタイプは、 DimensionEnumeration です。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
This method can be removed if there is
no custom implementation */
// dimensionDefaultingController.pageActivated();
```

### <a name="finance-and-operations"></a>財務と運用
このコールを、分析コード エントリ コントロールの親コントロールの pageActivated メソッドまたは Form Init メソッド内で実行する場合、削除することができます。 上記の場所以外のメソッド呼び出しの意図は明確ではありません。 呼び出しを削除して、コントロールをテストします。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.deleted();
```

### <a name="finance-and-operations"></a>財務と運用
データ ソースの削除メソッド内にはない deleted() の呼び出しのために、TODO が残されます。 これらの呼び出しは、データソースの削除メソッド内にのみ存在すると予想され、置換はありません。 呼び出しを削除して、コントロールをテストしてみてください。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
// dimensionDefaultingController.writing();
```

### <a name="finance-and-operations"></a>財務と運用
分析コード エントリ コントロール フレームワークは、値を保存します。 呼び出しを削除して、コントロールをテストします。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
dimensionDefaultingController::findBackingEntityInstance();
```

### <a name="finance-and-operations"></a>財務と運用
エンティティを検索するには、getEntityInstance メソッドを DimensionAttributeValue から呼び出す必要があります。 この呼び出しを次のようなものに置き換えます。

```xpp
DimensionAttributeValue dimAttrValue =
    DimensionAttributeValue::
        findByDimensionAttributeAndValueNoError(
            dimensionAttributeTable, dimensionValue);
if (dimAttrValue) {
    common = dimAttrValue.getEntityInstance();
}
```

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(NoYesUnchanged::Yes);
```

### <a name="finance-and-operations"></a>財務と運用
ここに 1 つのパラメーターがある場合のみ updateValues() メソッドが呼び出されるため、呼び出しは allowEdit() の呼び出しに置き換えることができます。

```xpp
DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::Yes);
```

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(
    NoYesUnchanged::No, true);
```

### <a name="finance-and-operations"></a>財務と運用
この場合、updateValues() の呼び出しには 2 つのパラメーターがあるので、コントロールの編集機能を変更するには allowEdit() の呼び出しと置き換え、コントロールの値をクリアするには loadAttributeValueSet() の呼び出しと置き換える必要があります。

```xpp
DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::No);
DimensionEntryControlHeader.loadAttributeValueSet(0);
```

> [!NOTE]
> updateValues メソッド 呼び出しの最初の パラメーター が NoYesUnchangedUnchanged::の場合は、allowEdit の新しい呼び出しは必要ありません。 同様に、updateValues メソッドの 2 番目のパラメーターの呼び出しが false の場合、loadAttributeValueSet への呼び出しは必要ありません。

## <a name="methods-to-potentially-remove"></a>削除する可能性のあるメソッド
分析コード エントリ コントロールを保持するデータソースまたは tabpage/グループの残りのメソッドは、カスタム ロジックがない場合、削除することができます。 次のテーブルは、削除する必要があるカスタマイズのないメソッドの例を示しています。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public int active(){int ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void delete(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void deleted(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void deleting(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public boolean validateDelete(){boolean ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void write(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void writing(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void written(){super();}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public boolean validateWrite(){boolean ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a>財務と運用
このメソッドはデータソースにあります。 カスタム ロジックがない場合に削除することができます。

### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

```xpp
public void pageActivated()
{
    super();
    /* TODO: (Code Upgrade) [Dimension entry control] This method can be removed if
    there is no custom implementation */
    // dimensionDefaultingController.pageActivated();
}
```

### <a name="finance-and-operations"></a>財務と運用
この方法は分析コード エントリ コントロールを保持する TabPage またはグループになります。 カスタム ロジックがない場合は、メソッドを削除することができます。

## <a name="compile-errors"></a>コンパイル エラー
このセクションでは、取り残される可能性のある一般的なコンパイル エラーに対処する方法について説明します。


### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

<strong>フォームで (PurchTable)。</strong>

```xpp
purchTableForm.parmDimensionDefaultingControllerHeader(
    dimensionDefaultingControllerHeader);
```

<strong>クラス内 (PurchTableForm):</strong>

```xpp
public DimensionDefaultingController
parmDimensionDefaultingControllerHeader(
    DimensionDefaultingController
        _dimensionDefaultingControllerHeader =
        dimensionDefaultingControllerHeader)
{
   dimensionDefaultingControllerHeader =
       _dimensionDefaultingControllerHeader;
   return dimensionDefaultingControllerHeader;
}
```

### <a name="finance-and-operations"></a>財務と運用

<strong>フォームで (PurchTable)。</strong>

```xpp
purchTableForm.parmDimensionEntryControlHeader(
    DimensionEntryControlHeader);
```

<strong>クラス内 (PurchTableForm):</strong>

```xpp
public DimensionEntryControl
parmDimensionEntryControlHeader(
    DimensionEntryControl
       _dimensionEntryControlHeader =
       dimensionEntryControlHeader)

{
    dimensionEntryControlHeader =
        _dimensionEntryControlHeader;
    return dimensionEntryControlHeader;
}
```


## <a name="additional-resources"></a>追加リソース

[既定の分析コード コントロールの分析コード エントリ コントロールへの移行](dimension-entry-control-migration.md)

[ダイアログの分析コード エントリ コントロールのサポート](dimension-entry-control-dialog-support.md)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

