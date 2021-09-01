---
title: 財務分析コードとして使用可能なバッキング テーブルの作成
description: このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。
author: RyanCCarlson2
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 191363
ms.assetid: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82824c09571b74cd8a386487fe108e37e22ef6fc919a5e1d124340108da80182
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729019"
---
# <a name="make-backing-tables-consumable-as-financial-dimensions"></a>財務分析コードとして使用可能なバッキング テーブルの作成

[!include [banner](../includes/banner.md)]

このトピックでは、サポート テーブルを財務分析コードとして使用できるようにするために必要な手順について説明します。

> [!IMPORTANT]
> 再利用できない値を持つまたは 1 対 1 の分析コード値を使用する、財務分析コードを作成しないでください。 ビューを、DimAttribute の分析コード値のソースとして使用することはできません。 これはうまくいくように見えますが、分析コードのファクト データがデータベースにインポートされるようにするため、MR が行ごとの処理にフォールバックされます。 これにより、パフォーマンスがかなり低下したり、レポートが遮断されます。 
>
> 財務分析コードのデータのソースとして使用する基本テーブルには、30 文字以内の固有ナチュラル キー値が必用であり、その値はそのテーブル内の 1 つの RECID を解決する必要があります。 拡張された名前列は、追加のコンテキストをユーザーに表示する場合にのみ使用され、ナチュラル キー エントリの一意性を解決するためには使用されないため、もう 1 つのソース結合 (DirPartyTable や別の場所など) から取得できます。
     
財務分析コードは、トランザクションおよび分析プロセスに必要な再利用可能な値にする必要があります。 これらの分析コードは、複数のトランザクションにわたって全体的な再利用を提供できるデータのソースを表す必要があります。 他の分析コード値に表示される際、高変動を表す ID データを供給するバッキング テーブルを選択しないでください。 これにより、ストレージと処理のコストが増加し、パフォーマンスと分析の価値に悪影響を及ぼします。

揮発性の非常に高いデータの例としては、以下のように、頻繁に増分されるタイムスタンプや識別子などがあります。

 - ドキュメント
 - 販売注文
 - 発注書
 - トランザクション
 - 小切手
 - シリアル
 - チケット
 - ライセンス番号 

これらは縮退分析コードと呼ばれます。 これらの値の追跡は、財務分析コード以外で行う必要があります。 つまり、情報を必要とするトランザクション レコードのカスタマイズを使用する必要があります。これらの値は、財務分析コード値と共に保存しないでください。

次の手順に従うことにより、**財務分析コード** ページの **値の使用元** のドロップダウン メニューにビューが自動的に表示され、値は **財務分析コード値** ページに入力されます。


> [!NOTE]
> 分析コードが **OMOperatingUnit** テーブルによってサポートされている場合、手順の多くは既に完了しています。 「[新しい OMOperatingUnit タイプがサポートしているエンティティを追加](#add-a-new-omoperatingunit-type-backed-entity)」セクション の手順に従います。

## <a name="step-1-create-a-view"></a>手順 1: ビューを作成する

最初のステップは、バッキング テーブルと同じモデルでビューを作成することです。 以下の手順を実行する前に、**テーブルのプロパティ** ウィンドウでバッキング テーブルが **Create Rec Id Index = Yes** であることを確認します。 または、テーブルに一意のインデックスがあり、RECID がそのインデックスの最初のセグメントであることを確認してください。

1.  プロジェクトで **追加** > **新しい項目** とクリックします。 **表示** を選択し、**追加** をクリックします。
1.  **表示** を右クリックし、**名前の変更** を選択します。 **DimAttribute**[BackingTableName] ビューに名前を付けます。 たとえば、DimAttributeCustTable。
1.  **メタデータの表示** を展開し、テーブルを画面上の **データ ソース** ノードにドラッグします。
1.  ノードの名前を **BackingTableName** から **BackingEntity** に変更します。
1.  財務分析コードとして使用するテーブルのキー、値、および名前を識別します。 フィールドを検索して、BackingEntity データ ソースの一覧にドラッグし、またはデータ ソース上のフィールドにコピーして貼り付けます。 3 つのフィールドの名前を変更します。
      + **キー** – これは代理キーで、通常は RecID です。
      + **値** - これは、AccountNum のようなナチュラル キーです。 最大 30 文字の文字列です。
      + **名前** – これは説明で、通常は **名前** または **説明** フィールドです。 最大 60 文字の文字列です。
1.  バッキング テーブルがデータを削除する場合、ビューで **範囲** を作成することが必要な場合があります。 たとえば、作業単位を使用し部門のみを必要とする場合、その作業単位の範囲を使用します。
1.  **新しいインデックス** を右クリックし、**新しいインデックス** を選択します。 **プロパティ** ウィンドウでデータ フィールドとして **値** を選択します。 必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **いいえ** にセットする必要があります。
1. **新しいインデックス** を右クリックし、**新しいインデックス** を選択します。 **プロパティ** ウィンドウでデータ フィールドとして **名前** を選択します。 必要に応じてインデックスの名前を変更することができますが、**重複の許可** を **はい** にセットする必要があります。
1. **表示** をクリックし、**プロパティ** ウィンドウで、選択した参照ラベル ID に **単数形ラベル** フィールドを設定します。 これは、顧客などの単一の値を示すラベルである必要があります。
1. **ラベル** フィールドを選択した参照ラベル ID に設定します。 これは、顧客などの複数の値を示すラベルである必要があります。 この値は、**財務分析コード** ページの **値の使用元** フィールドのドロップダウン リストに表示されます。
1. **プロパティ** ウィンドウの **TitleField1** フィールドに、**値** を入力します。
1. **プロパティ** ウィンドウの **TitleField2** フィールドに、**名前** を入力します。
1. バッキング テーブルのプロパティを確認し、使用している config キーを識別します。 **表示** で、バッキング テーブルと同じ **コンフィギュレーション キー** を入力します。

    > [!IMPORTANT]
    > 管理者以外のユーザーに、新しいビューのセキュリティ アクセス権を付与する必要があります。
    > - オーバーレイが使用されるリリース 7.2 およびそれ以前では、**DimensionEssentials** を検索し、プロジェクトに追加します。 **DimensionEssentials** を展開し、**アクセス許可** を右クリックし、その後 **新しいアクセス許可** を選択します。 **プロパティ** ウィンドウで、**アクセス レベル** を **読み取り** に設定します。 **セキュリティ権限** をクリックし、**読み取り** の **アクセス レベル** を **アクセス許可** ノードの下に追加します。 これらの 1 つを使用しているモデルに拡張することが必要な場合があります。
    > - 拡張機能が使用されているリリース 7.3 以降では、新しいビューと共にカスタム モデルで新しいセキュリティ権限を作成します。 **アクセス許可** ノードを右クリックし、**新しいアクセス許可** を選択します。 上記の手順 2 で作成した新しい DimAttribute[DimensionName] ビューの名前を入力し、**アクセス レベル** を **読み取り** に設定します。 **セキュリティ職務権限 SysServerAXBasicMaintain** を検索します。 右クリックし、**拡張機能の作成** を作成します。 必要に応じて拡張機能の名前を変更します。 新たに作成された **セキュリティ特権** を **特権リスト** にドラッグ アンド ドロップします。  
       
14. **表示** を右クリックし、**コードの表示** を選択します。 ビューに次のコードを追加します。 これにより、分析コード フレームワークに登録されます。 CustTable に対して作成されたビューを使用する例を次に示します。

      ```xpp
      [SubscribesTo(classstr(DimensionEnabledType),
      delegatestr(DimensionEnabledType,
      registerDimensionEnabledTypeIdentifiersDelegate))]

      public static void registerDimensionEnabledTypeIdentifier(DimensionIEnabledType _dimensionEnabledType)
      {
         _dimensionEnabledType.registerViewIdentifier(tablestr(DimAttribute**CustTable**));
      }
      ```

15. **Microsoft Dynamics 365** を選択し、**オプション** をクリックします。 **ベスト プラクティス** を選択します。 モデルを選択し、**Microsoft.Dynamics.AX.Framework.ViewRules/ViewDimensionEnabledTypeChecker** が表示されるまでスクロールします。 ルールとその子が選択されていることを確認します。
16.  ビューをビルドしてから同期します。

## <a name="step-2-validate-that-the-view-returns-the-correct-data-in-sql"></a>手順 2: ビューが SQL で正しいデータを返すことを検証する

この時点で SQL Server Management Studio で次のクエリを実行して、正しいデータが引き出されているかを確認をする必要があります。 CustTable に対して作成されたビューを使用する省略例を次に示します。

```sql
select * from DIMATTRIBUTECUSTTABLE
```
    

| キー   | 値    | データ範囲 ID | パーティション | RECID   | NAME           | パーティション 2 |
|-------------|--------------|----------------|---------------|-------------|--------------------|------------------|
| 22565425322 | US\_SI\_0129 | ussi           | 5637144576    | 22565425322 | Adventure Services | 5637144576       |
| 22565424579 | US\_SI\_0128 | ussi           | 5637144576    | 22565424579 | アルペン エレクトロニクス | 5637144576       |


## <a name="step-3-override-methods-on-the-backing-table"></a>手順 3: バッキング テーブルでメソッドを上書きする

バッキング テーブルのナチュラル キーを削除または名前を変更するときに分析コード フレームワークと統合するには、バッキング テーブルの delete メソッドと、update または renamePrimaryKey メソッドにカスタム コードを記述する必要があります。 テーブルがナチュラル キーの更新をブロックする場合、renamePrimaryKey のオーバーライドを使用する必要があります。 存在しない場合は、更新メソッドでコードを格納できます。 CustTable からの例を次に示します。

```xpp
public void delete()
{
    if (!DimensionValidation::canDeleteEntityValue(this))
    {
        throw error(strFmt("@SYS134392", this.AccountNum));
    }
      
    ttsbegin;
    DimensionAttributeValue::updateForEntityValueDelete(this);
    ttscommit;
}
   
public void update()
{
    Common originalRecord = this.orig();
    super();
    DimensionValueRename::syncRenamedValue(this, originalRecord);
}
   
public void renamePrimaryKey()
{
    Common originalRecord = this.orig();
    super();
    DimensionValueRename::syncRenamedValue(this, originalRecord);
}
```

## <a name="step-4-clear-caches-to-force-detection-of-the-new-view"></a>手順 4: キャッシュをクリアして新しいビューの検出を強制的する

分析コードとして消費できるエンティティのリストはサーバー上でキャッシュされるため、キャッシュをクリアする呼び出しが実行されるか、クライアントとサーバーの両方が再起動されるまで新しいエンティティの作成は既存のエンティティのリストに表示されません。 キャッシュをクリアして新しいビューをすぐに表示させるには、実行可能なクラス内で次のコード行を実行する必要があります。

```xpp
DimensionCache::clearAllScopes();
```

## <a name="step-5-verify-that-the-dimension-appears-in-the-use-value-from-lookup"></a>手順 5: 分析コードが [ルックアップからの値を使用] に表示されることを確認する

手順を完了したら、総勘定元帳の **財務分析コード** ページに移動します。 **値の使用元** フィールドのドロップダウン メニューをクリックし、値が使用可能であることを確認します。


## <a name="add-a-new-omoperatingunit-type-backed-entity"></a>新しい OMOperatingUnit タイプがサポートしているエンティティの追加

新しい組織モデル OMOperatingUnitType 列挙が追加された場合、次元として使用可能にする手順は類似していますが、次のように短くすることができます。

1. 既存の DimAttributeOM[BackingTableName] ビューの 1 つをコピーし、適切に名前を変更して、関連するすべてのラベルとヘルプ テキストを調整します。
1. コピーしたビューで、Datasource\BackingEntity (OMOperatingUnit) \Ranges ノードを展開します。 範囲内の値プロパティを、追加された新しい OMOperatingUnitType 列挙型に変更します。
1. プロジェクトをビルドして同期します。
1. SQL でデータを検証するステップ２で始まるこのトピックの手順に従い、**値の使用** ルックアップで表示される分析コードを検証するステップ 5 まで続けます。

**OMOperatingUnitType** は **OMOperatingUnit** テーブルによってサポートされているため、削除、更新および **renamePrimaryKey** メソッドを処理するための汎用コードがすでに存在します。 したがって、これらのメソッドを更新する必要はありません。

## <a name="step-6-setting-a-dimension-to-be-self-referenced"></a>手順 6: 自己参照される分析コードを設定する 

新しいエンティティのデータ エンティティも作成し、そのエンティティが既定の分析コードへの参照を持っている場合、persistEntity() メソッドにこのコードを追加します。

```xpp
if (_entityCtx.getDatabaseOperation() == DataEntityDatabaseOperation::Insert)
{
    this.<Your entity ‘private’ RecId Dimension field> = DimensionDefaultResolver::checkAndCreateSelfReference(tablenum(<Your backing table>), this.<Your entity Key field>, this.<Your entity ‘public’ DisplayValue field>);
}
```                                                                                            
**例**

```xpp
public void persistEntity(DataEntityRuntimeContext _entityCtx)
{
    if (_entityCtx.getDatabaseOperation() == DataEntityDatabaseOperation::Insert)
    {
        this.DefaultDimension = DimensionDefaultResolver::checkAndCreateSelfReference(tablenum(BankAccountTable), this.BankAccountId, this.DefaultDimensionDisplayValue);
    }

    super(_entityCtx);
}
```

> [!NOTE]
> これにより、分析コードが自身を既定の既定値として使用するようにする場合、情報が正しい順序で作成されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]