---
title: カスタマイズ分析のレポート (CAR)
description: この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。 また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 49681
ms.assetid: 540b08dd-9af7-42fc-aa0c-ba04af1f8002
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af658e0d358c1803949de086da00e10a6f08affe
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248999"
---
# <a name="customization-analysis-report-car"></a>カスタマイズ分析のレポート (CAR)

[!include [banner](../includes/banner.md)]

この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。 また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。 

## <a name="what-is-the-customization-analysis-report"></a>カスタマイズ分析レポートとは

カスタマイズ分析レポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行するツールです。 このレポートは、ソリューション認証プロセスの要件の 1 つです。 レポートは、Microsoft Excel のブック形式です。

## <a name="how-to-generate-the-report"></a>レポートを生成する方法
カスタマイズ分析レポートを生成するには、開発環境で次のコマンドを実行します。

```Console
xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>
```

### <a name="example"></a>例

```Console
xppbp.exe -metadata=C:\Packages -all -model="MyAppSuiteCustomizations" -xmlLog=C:\temp\BPCheckLogcd.xml -module="ApplicationSuite" -car=c:\temp\CAReport.xlsx
```

xppbp.exe ツール、c:\\packages\\bin または I:\\AosService\\PackagesLocalDirectory\\bin にあります。

## <a name="issues-list"></a>問題リスト
このセクションでは、レポートの**問題リスト**ページに表示されるベスト プラクティスのルール (エラー、警告、または情報メッセージ) をすべて説明し、問題を解決するための提案を示します。 **メタデータ**または**コード**の型の問題です。 すべての**コード**問題に関しては、重ねたメソッドで警告またはエラーが発生する場合、ルールに違反しているコードの明細行は下位レイヤーのモデルに属していることに留意してください。 その場合、自分のものではないコードの警告やエラーを修正する責任はありません。

### <a name="bpcheckpackreturnsconnull"></a>BPCheckPackReturnsConnull

| 説明         | このルールは、**SysPackable** インターフェイスを実装するすべてのクラスに適用されます。 これは、**Pack** メソッドが **Connull()** を返さないことを確認します。 |
|---------------------|-------------------------------------|
| エラー メッセージ       | コンテナー パック メソッドは、Runbase 派生クラスで connull を返します                |
| 出庫タイプ/重要度 | コード/警告  |
| 修正する方法       | 該当する場合、**Pack** メソッドの戻り値を更新するか、**Super()** を返します。                 |

### <a name="bpcheckparametersmodified"></a>BPCheckParametersModified

| 説明         | メソッドのパラメーターがメソッド内で変更された場合、このルールは失敗します。                      |
|---------------------|----------------------------------------------------------------------------------------------|
| エラー メッセージ       | メソッド %1 のパラメーター 1% がメソッド内で変更されています                                     |
| 出庫タイプ/重要度 | コード/警告                                                                                 |
| 修正する方法       | コードをリファクターします。 呼び出されたメソッド内ではなく、呼び出し元によりパラメーターを変更する必要があります。 |

### <a name="bpchecksqlcode"></a>BPCheckSQLCode

| 説明         | このルールは、X++ コードに直接 SQL コードが含まれていると失敗します。       |
|---------------------|------------------------------------------------------------------|
| エラー メッセージ       | メソッド %1 に SQL コードが見つかりました                                      |
| 出庫タイプ/重要度 | コード/警告                                                     |
| 修正する方法       | X++ を使用してデータベースにアクセスするコードをリファクタリングします。 |

### <a name="bpchecknestedloopincode"></a>BPCheckNestedLoopInCode

| 説明         | このルールは、**select** ループがループ内にネストされていることを検出すると失敗します。    |
|---------------------|----------------------------------------------------------------------------|
| エラー メッセージ       | %1 メソッドに入れ子になったデータ アクセス ループが見つかりました                                                |
| 出庫タイプ/重要度 | コード/警告                   |
| 修正する方法       | 入れ子になったデータ アクセス ループの代わりに結合を使うコードをリファクタリングします。 メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。 |

### <a name="bpcheckinsertmethodinloop"></a>BPCheckInsertMethodInLoop

| 説明         | このルールは、ループの中に入れ子されたメソッド **insert** への呼び出しを検出すると失敗します。 **InsertRecordList** を使用することをお勧めします。 このルールは、InMemory テーブルには適用されません。 |
|---------------------|-------------------------------|
| エラー メッセージ       | メソッド %1 で、Insert メソッドを RecordInsertList に置き換えることができます。                       |
| 出庫タイプ/重要度 | コード/警告           |
| 修正する方法       | **InsertRecordList** など、設定に基づく操作を使用するコードをリファクターします。            |

### <a name="bpcheckselectwithjoin"></a>BPCheckSelectwithJoin

| 説明         | 結合されていない入れ子になった **select** ステートメントが見つかった場合、このルールは失敗します。  |
|---------------------|------------------------------------------------------------------------|
| エラー メッセージ       | %1 メソッドの入れ子になった select ステートメントは結合できます。                                |
| 出庫タイプ/重要度 | コード/警告                                                                          |
| 修正する方法       | 入れ子になった **select** ステートメントの代わりに結合を使うコードをリファクタリングします。 メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。 |

### <a name="bpfunctioncallwithselect"></a>BPFunctionCallwithSelect

| 説明         | このルールは、**select** ステートメント内で関数呼び出しが見つかった場合に失敗します。   |
|---------------------|------------------|
| エラー メッセージ       | メソッド %1 の select ステートメントに、関数呼び出しが見つかりました     |
| 出庫タイプ/重要度 | コード/警告    |
| 修正する方法       | **選択**ステートメントを呼び出す前に、関数の戻り値をローカル変数へと割り当て、**選択**ステートメントでローカル変数を使用します。 |

### <a name="bpcheckinvalidexecutequery"></a>BPCheckinvalidExecuteQuery

| 説明         | このルールは、**ExecuteQuery** メソッドで **super()** を呼び出した後に **addRange** への呼び出しが見つかった場合に失敗します。 |
|---------------------|-------------------------------------------------------|
| エラー メッセージ       | フォーム %1 の ExecuteQuery メソッドに、super() の後に add range を追加しないでください。               |
| 出庫タイプ/重要度 | コード/警告                                          |
| 修正する方法       | このパターンを回避するために、コードをリファクタリングします。             |

### <a name="bpcheckinvalidinitformmethod"></a>BPCheckInvalidInitFormMethod

| 説明         | このルールは、**super()** を呼び出す前にフォームの**init** メソッドでフォーム コントロールとデータソースを初期化しないようにします。 **element** または **this** を **super()** に対する呼び出し (**this.aMethod()** または **element.aMethod()**) の前に使用するステートメントが検出された場合に失敗します。 情報メッセージは番号順序の初期化など許可されたいくつかのパターンのみを表示します (**numberSeqPreInit**) 。 |
|---------------------|---------------------------------------------------------------------------------------------------------|
| エラー メッセージ       | フォーム要素ステートメントは、フォーム %1 の init メソッドで、super() の前に使用しないでください。      |
| 出庫タイプ/重要度 | コード/情報または警告                                   |
| 修正する方法       | **super()** の呼び出し後、コードをリファクターしてフォーム コントロールおよびデータにアクセスします。 コードが任意のフォーム コントロールを初期化せず、**super()** の前にどのフォーム データ ソースにもアクセスしない場合、Microsoft にカスタマイズ分析のレポートを送信するときに例外をまとめます。   |

### <a name="bpcheckemptyloop"></a>BPCheckEmptyLoop

| 説明         | このルールは、ステートメントがないループを検出すると失敗します。 |
|---------------------|------------------------------------------------------------|
| エラー メッセージ       | クラス %2 の メソッド %1 で空のループが見つかりました                  |
| 出庫タイプ/重要度 | コード/警告                                               |
| 修正する方法       | ループをコードから削除します。                            |

### <a name="bpchecklockqueryrange"></a>BPCheckLockQueryRange

| 説明         | フォームの **init** メソッドでコードが **AddRange** を呼び出し、その範囲をロックまたは非表示として設定しないと、このルールは失敗します。      |
|---------------------|-------------------------------------------|
| エラー メッセージ       | フォーム %1で、範囲はロックするか、非表示にする必要があります    |
| 出庫タイプ/重要度 | コード/警告     |
| 修正する方法       | **AddRange** の呼び出しの後に、**QueryBuildRange.status(RangeStatus::Locked)** または **QueryBuildRange.status(RangeStatus::Hidden)** を追加します。 |

### <a name="bpcheckskipstatementvalidation"></a>BPCheckSkipStatementValidation

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>説明</td>
<td>このルールは、<strong>Skip</strong> ステートメントを持たないセットベースの操作を検出した場合に通知メッセージを報告します。
<ul>
<li><strong>update_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。 テーブルの <strong>update</strong> メソッドが上書きされる場合にのみルールが適用されます。</li>
<li><strong>insert_recordset</strong> が見つかると、ルールによって <strong>skipDataMethods(true)</strong> がチェックされます。 テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</li>
<li><strong>delete_from</strong> が見つかると、ルールによって <strong>skipDeleteActions(true)</strong> がチェックされます。 テーブルの <strong>insert</strong> メソッドが上書きされる場合にのみルールが適用されます。</li>
</ul>
これは、セットベースの操作のパフォーマンス向上を最大限に活用するために、<strong>スキップ</strong>メソッドを呼び出す必要があることを示す情報メッセージです。 <strong>スキップ</strong>  メソッドが使用されていない場合は、実行は行ごとの操作に戻ります。</td>
</tr>
<tr class="even">
<td>エラー メッセージ</td>
<td>セット ベースの操作はクラス %2 のメソッド %1 で Skip ステートメントを呼び出す必要があります。それ以外の場合、行ごとの操作にフォールバックされます。</td>
</tr>
<tr class="odd">
<td>出庫タイプ/重要度</td>
<td>コード/情報</td>
</tr>
<tr class="even">
<td>修正する方法</td>
<td>該当する場合は、<strong>skipDataMethods(true)</strong> または <strong>skipDeleteActions(true)</strong> を使用します。</td>
</tr>
</tbody>
</table>

### <a name="bpchecknottstryblock"></a>BPCheckNoTTSTryBlock

| 説明 | このルールは、正しく処理されない <strong>tts</strong> ブロック内の <strong>try</strong> ステートメントを検出すると失敗します。 |
|---|---|
| エラー メッセージ | try 文の tts ブロックは、メソッド %1 の例外を明示的にキャッチしません。 |
| 出庫タイプ/重要度 | コード/警告 |
| 修正する方法 | この表に続くコードの例を使用します。 |

次の例では、ルールが失敗するか、合格するかを示しています。 次の例を参考にして、コードをリファクタリングします。

```xpp
ttsbegin;
try {
}
// fail
catch {
}
try {
}
// pass
catch(Exception::UpdateConflict) {
}
try {
}
// pass
catch(Exception::UpdateConflictNotRecovered) {}
```

### <a name="bpcheckemptytablemethod"></a>BPCheckEmptyTableMethod

| 説明         | このルールは、ソース コードのないテーブル メソッドをチェックします。 空テーブルのメソッドは、テーブルのレコードセット オペレーションを行単位の操作に戻す原因となります。 |
|---------------------|-------------------------------------------|
| エラー メッセージ       | %1 テーブルに空の %2 メソッドがあります           |
| 出庫タイプ/重要度 | コード/警告                              |
| 修正する方法       | このメソッドをコードから削除します。        |

### <a name="bpcheckbatchjobsenabled"></a>BPCheckBatchJobsEnabled

| 説明         | このルールは、**RunBaseBatch** を拡張するすべてのクラスが **true** を返す **canGoBatch** メソッドを持つことを保証します。 |
|---------------------|----------------------------------------------------------------|
| エラー メッセージ       | カスタム ジョブがクラス %1 でバッチ対応でありません         |
| 出庫タイプ/重要度 | コード/警告       |
| 修正する方法       | **canGoBatch** メソッドは、すべてのバッチ クラスに **true** を返します。     |

### <a name="bpcheckdisplaymethodcached"></a>BPCheckDisplayMethodCached

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>説明</td>
<td>データ メソッドにバインドされている各コントロールについては、これらの条件のいずれかが満たされている場合、このルールは失敗します。
<ul>
<li><strong>データのキャッシュ方法</strong>プロパティが<strong>自動</strong>に設定され、対応するテーブルの <strong>display</strong>/<strong>edit</strong> メソッドには <strong>SysClientCacheDataMethodAttribute</strong> がなく、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</li>
<li><strong>データのキャッシュ方法</strong> プロパティは <strong>いいえ</strong> に設定され、データ ソースの <strong>init</strong> メソッドは <strong>CacheAddMethod</strong> を使用しません。</li>
</ul></td>
</tr>
<tr class="even">
<td>エラー メッセージ</td>
<td>フォーム %2 の 表示メソッド %1 がキャッシュされていません</td>
</tr>
<tr class="odd">
<td>出庫タイプ/重要度</td>
<td>コード/警告</td>
</tr>
<tr class="even">
<td>修正する方法</td>
<td>この表に続くメモを使用します。</td>
</tr>
</tbody>
</table>

この警告は、次のいずれかのパターンを使用して修正することができます。

+ **キャッシュ データ メソッド** プロパティを **はい** に設定します。
+ **キャッシュ データ メソッド** プロパティを **自動** に設定し、**SysClientCacheDataMethodAttribute** 属性を使用してテーブルのデータ メソッドをマークします。 次に例を示します。

    ```xp
    [SysClientCacheDataMethodAttribute(true)]
    Display TransDate myDateMethod()
    {
        //...
    }
    ```

+ フォームの **init** メソッドで **CacheAddMethod** を使用すると、そのメソッドをキャッシュ済みとしてマークします。

### <a name="bpchecksqlqueryininit"></a>BPCheckSQLQueryInInit

| 説明         | このルールは、フォームの **init** メソッドで **while** ループを持つデータ アクセス クエリが見つかった場合に失敗します。 このパターンは、フォームの初期化時にパフォーマンスの問題を引き起こす場合があります。 |
|---------------------|--------------------------------------|
| エラー メッセージ       | フォーム %1 の init メソッドで、while ループを持つ SQL クエリが見つかりました            |
| 出庫タイプ/重要度 | コード/警告   |
| 修正する方法       | このパターンを回避するために、コードをリファクタリングします。  |

### <a name="bpchecknewquerywithform"></a>BPCheckNewQueryWithForm

| 説明         | このルールは、フォームの **init** または **executeQuery** メソッドで **new Query()** ステートメントを検出すると失敗します。 |
|---------------------|--------------------------------------------------|
| エラー メッセージ       | フォーム メソッド %1 で、データ ソース クエリが上書きされます      |
| 出庫タイプ/重要度 | コード/警告                                |
| 修正する方法       | このパターンを回避するために、コードをリファクタリングします。            |

### <a name="bpcheckselectforupdateabsent"></a>BPCheckSelectForUpdateAbsent

| 説明         | **Select ForUpdate** を使用してレコードを選択したが、更新が実行されていない場合、このルールは失敗します。 このルールは、オプティミスティック同時実行制御 (OCC) が有効になっているテーブルには適用されません。 |
|---------------------|------------------|
| エラー メッセージ       | メソッド %1 に Select ForUpdate が実装されていません   |
| 出庫タイプ/重要度 | コード/警告      |
| 修正する方法       | **ForUpdate を選択** の代わりに **選択** を使用するか、**OCC を有効** プロパティを **はい** に設定します。                                                                                          |

### <a name="bpchecktablepropertymismatch"></a>BPCheckTablePropertyMismatch

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>説明</td>
<td>このルールは、テーブルがテーブル グループに属しているが、適切な<strong>キャッシュ ルックアップ</strong>値を持たない場合に失敗します。 次の条件がすべて満たされていると、ルールは失敗します。
<ul>
<li><strong>テーブル グループ</strong> プロパティは <strong>メイン</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> または <strong>EntireTable</strong> に設定されます。</li>
<li><strong>テーブル グループ</strong> プロパティは <strong>グループ</strong> または <strong>パラメーター</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>NotinTTS</strong> に設定されます。</li>
<li><strong>テーブル グループ</strong> プロパティは <strong>WorksheetHeader</strong>、<strong>WorksheetLine</strong>、または <strong>Transaction</strong> に設定され、<strong>キャッシュ ルックアップ</strong> プロパティは <strong>Found</strong>、<strong>FoundAndEmpty</strong>、または <strong>EntireTable</strong> に設定されます。</li>
</ul></td>
</tr>
<tr class="even">
<td>エラー メッセージ</td>
<td>%1 テーブルにテーブル グループとキャッシュ ルックアップの無効な組み合わせがあります</td>
</tr>
<tr class="odd">
<td>出庫タイプ/重要度</td>
<td>メタデータ/警告</td>
</tr>
<tr class="even">
<td>修正する方法</td>
<td>テーブルで適切な <strong>キャッシュ ルックアップ</strong> 値を設定します。</td>
</tr>
</tbody>
</table>

### <a name="bpcheckmissingdeleteactions"></a>BPCheckMissingDeleteActions

| 説明         | このルールは、テーブル関係の**削除**アクションまたは**削除時**プロパティの値が**なし**と等しくないことを検証します。 関連するテーブルまたは現在のテーブルが tempDB、メモリ テーブル、参照テーブル、ステージング テーブル、パラメーター テーブルの場合、ルールはトリガーされません。 |
|---------------------|---------------------------------------------------|
| エラー メッセージ       | リレーション名 %3 でテーブル %2 に関連付けられているテーブル %1 に欠けているアクションを削除します      |
| 出庫タイプ/重要度 | メタデータ/警告   |
| 修正する方法       | **None** と等しくない **delete** アクションを設定します。 |

### <a name="bpcheckaddressmodel"></a>BPCheckAddressModel

| 説明         | テーブル フィールドが **AddressZipCodeId** または **AddressStateId** タイプの場合、このルールは失敗します。 これらのタイプは、コードが新しいアドレス フレームワークを受け入れなかったことを示します。 |
|---------------------|-------------------------|
| エラー メッセージ       | テーブル %2 のフィールド %1 は、アドレスの場所モデルの一部ではありません   |
| 出庫タイプ/重要度 | メタデータ/警告  |
| 修正する方法       | これらのタイプをディレクトリ モデルのその他の適切な EDT タイプに置き換えます。        |

### <a name="bpcheckdimensionmodel"></a>BPCheckDimensionModel

| 説明         | テーブル フィールドが、**分析コード**または **LedgerAccount** タイプの場合、このルールは失敗します。 これらのタイプは、コードが新しい財務分析コード フレームワークを受け入れなかったことを示します。 |
|---------------------|----------|
| エラー メッセージ       | テーブル %2 のフィールド %1 は、財務分析コード フレームワークの一部ではありません               |
| 出庫タイプ/重要度 | メタデータ/警告   |
| 修正する方法       | これらのタイプを分析コード モデルのその他の適切な EDT タイプに置き換えます。       |

### <a name="bpchecknumberofnewfields"></a>BPCheckNumberofNewFields

| 説明         | このルールは、そのテーブルのカスタマイズまたは拡張のプロセスで、テーブルに 10 個以下のフィールドが追加されたことを確認します。 このルールは、ステージング テーブルには適用されません。 |
|---------------------|-------------------------------------|
| エラー メッセージ       | 次の値より大きいテーブル %1 の新しいフィールドの数      |
| 出庫タイプ/重要度 | メタデータ/警告   |
| 修正する方法       | スキーマをリファクタリングし、既存のテーブルに多数のフィールドを追加する代わりに関連するテーブルを作成します。 |

### <a name="bpcheckenumupgradeissue"></a>BPCheckEnumUpgradeIssue

| 説明         | このルールは、次の条件が満たされた場合に失敗します。列挙型 (オーバーレイ) をカスタマイズすると、新しい列挙型の値は既存の最大値 + 10 未満になります。 このルールは、拡張可能な列挙型には適用されません。 |
|---------------------|--------------------------------------|
| エラー メッセージ       | 列挙 %1 で、アップグレード問題があります。    |
| 出庫タイプ/重要度 | メタデータ/警告       |
| 修正する方法       | 大きな列挙値を使用するか、列挙型を拡張します。       |

### <a name="bpcheckpassivejoinuse"></a>BPCheckPassiveJoinUse

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>説明</td>
<td>このルールは、フォームがデータのプリロードを許可する場合、タブ ページ データソースのリンク タイプがパッシブであることを検証します。 次の条件がすべて満たされていると、ルールは失敗します。
<ul>
<li><strong>Yes</strong> に設定された <strong>AllowPreLoading</strong> プロパティのフォームがあります。</li>
<li>フォームのタブ ページは、最上位レベルのデータ ソースにバインドされています。</li>
<li>データ ソースの<strong>結合ソース</strong>プロパティが設定されます。</li>
<li>データ ソースの <strong>リンク タイプ</strong> プロパティが <strong>パッシブ</strong> に設定されていません。</li>
</ul></td>
</tr>
<tr class="even">
<td>エラー メッセージ</td>
<td>新しいメッセージは、「フォームの %2 タブ ページ コントロールにバインドされたデータソース %1 でパッシブ結合を使用する」 ことを提案しています</td>
</tr>
<tr class="odd">
<td>出庫タイプ/重要度</td>
<td>メタデータ/警告</td>
</tr>
<tr class="even">
<td>修正する方法</td>
<td>フォームで <strong>AllowPreLoading</strong> プロパティを <strong>いいえ</strong> に設定するか、データ ソースでパッシブ結合を使用します。 パッシブ結合では、タブ ページのクエリの実行時に明示的にプログラミングする必要があります。</td>
</tr>
</tbody>
</table>

### <a name="bpcheckalternatekeyabsent"></a>BPCheckAlternateKeyAbsent

| 説明         | このルールは、一意のインデックスを持つテーブルに少なくとも 1 つの代替キーがあることを確認します。 |
|---------------------|------------------------------------------------------------------------------------------|
| エラー メッセージ       | テーブル %1 には、代替キーがありません                                                  |
| 出庫タイプ/重要度 | メタデータ/警告                                                                         |
| 修正する方法       | テーブルの一意のインデックスで **代替キー** プロパティを **はい** に設定します。            |

### <a name="bpcheckbasetablemodified"></a>BPCheckBaseTableModified

| 説明         | このルールは、Microsoft によって出荷される特定のベース テーブルの一覧のカスタマイズ (オーバーレイ化) を推奨しません。 例では、SourceDocumentHeader および SourceDocumentLine テーブルがあります。 |
|---------------------|----------------------------|
| エラー メッセージ       | %1 はベース テーブルであり、変更することはできません。   |
| 出庫タイプ/重要度 | メタデータ/警告     |
| 修正する方法       | テーブルをカスタマイズしないでください。    |
