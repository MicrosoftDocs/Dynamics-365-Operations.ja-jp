---
title: ライブ同期に関する問題のトラブルシューティング
description: この記事では、ライブ同期の問題修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 1211f7da15686f1c55a4c942f04c73d671e0ba6b
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111429"
---
# <a name="troubleshoot-live-synchronization-issues"></a>ライブ同期に関する問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]



この記事では、財務と運用アプリと Microsoft Dataverse 間の二重書き込み統合に関するトラブル シューティングの情報を提供します。 このトピックでは、ライブ同期の問題修正に役立つトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> この記事説明されている問題の中には、システム管理者ロールまたは Azure Active Directory (Azure AD) テナント管理者の資格情報のいずれかが必要な場合があります。 各セクションでは、特定のロールまたは特定の資格情報が必要な場合について説明しています。

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>行の作成時にライブ同期でエラーが表示される

財務と運用アプリで行を作成した際に、次のエラー メッセージが表示される場合があります:

*\[{\\"エラー\\"：{\\"コード\\"：\\"0x 80072560\\"、\\"メッセージ\\"：\\"ユーザーは組織のメンバではありません。\\}}\]、リモートサーバーからエラーが返されました：（403）権限がありません。"}}"*

この問題を修正するには、[システム要件と前提条件](requirements-and-prerequisites.md) に記載されている手順を実行してください。 これらの手順を完了するには、Dataverse で作成された二重書き込みアプリケーションのユーザーにシステム管理者ロールが割り当てられている必要があります。 また、既定の所有チームにシステム管理者ロールが割り当てられている必要があります。

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>テーブル データを保存しようとする場合、ライブ同期にエラーが表示される

**問題の修正に必要な役割：** システム管理者

財務と運用アプリでテーブル データを保存しようとする際に、次のエラー メッセージが表示される場合があります:

*データベースへの変更を保存できません。作業単位で取引をコミットすることはできません。エンティティ uoms にデータを書き込むことができません。UnitOfMeasureEntity への書き込みが失敗し、次のエラーメッセージが表示されました。エンティティ uoms と同期することはできません。*

問題を修正するには、前提条件となる参照データが財務と運用アプリと Dataverse の両方に存在していることを確認する必要があります。 たとえば、顧客レコードが特定の顧客グループに属している場合は、その顧客グループ レコードが Dataverse に存在することを確認します。

データが両方の場所に存在し、問題がデータに起因するものではないことが分かった場合は、次の手順を実行してください。

1. Excel アドインを使用して **DualWriteProjectConfigurationEntity** エンティティを開きます。 アドインを使用するには、財務と運用の Excel アドインでデザイン モードを有効にし、ワークシートに **DualWriteProjectConfigurationEntity** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
2. 二重書き込みマップおよびプロジェクトで問題があるレコードを選択および削除します。 二重書き込みマッピングごとに 2 つのレコードがあります。
3. Excel アドインを使用して変更を公開します。 エンティティおよび基になるテーブルからレコードが削除されるので、この手順は重要です。

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>財務と運用アプリにデータを作成する際の、読み取り、書き込み権限に関するエラーを処理する

財務と運用アプリでデータを作成した際に、「不正な要求」というエラー メッセージが表示される場合があります。

![不正な要求のエラー メッセージの例。](media/error_record_id_source.png)

この問題を修正するには、マッピングされた Dynamics 365 Sales または Dynamics 365 Customer Service 事業単位のチームに適切なセキュリティロールを割り当てて、不足している権限を有効にする必要があります。

1. 財務と運用アプリで、データ統合の接続セットにマッピングされている事業単位を検索します。

    ![組織のマッピング。](media/mapped_business_unit.png)

2. Customer Engagement アプリで環境にログインし、**設定 \> セキュリティ** の順に移動し、マッピングされた事業単位のチームを検索します。

    ![マッピングされた事業単位のチーム。](media/setting_security_page.png)

3. 編集用のチームのページを開き、**ロールの管理** を選択します。

    ![ロールの管理ボタン。](media/manage_team_roles.png)

4. **チーム ロールの管理** ダイアログ ボックスで、関連するテーブルの読み取り/書き込み特権を持つロールを割り当てて、**OK** を選択します。

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>最近変更された Dataverse 環境の存在する環境にて、同期の問題を修正する

**問題の修正に必要な役割：** システム管理者

財務と運用アプリでデータを作成した際に、次のエラー メッセージが表示される場合があります:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**エンティティ CustCustomerV3Entity のペイロードを生成できません。**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":" ペイロードの作成に失敗しました。エラー 無効な URI です：URI が入力されていません。}\],"isErrorCountUpdated":true}*

以下に Customer Engagement アプリのエラー メッセージは次のとおりです。

> ISV コードから予期しないエラーが発生しました。 (ErrorType = ClientError) プラグインから予期しない例外が発生しました (実行): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: エンティティ アカウントの処理に失敗しました - (接続先が一定期間応答しなかったために接続に失敗したか、接続ホストが応答しなかったために確立された接続が失敗しました。

このエラーは、財務と運用アプリでのデータ作成時に、Dataverse 環境が正しくリセットされていない場合に発生します。

> [!IMPORTANT]
> 環境を再リンクした場合は、軽減策手順を続行する前に、すべてのエンティティ マップを停止する必要があります。

問題を修正するには、Dataverse および財務と運用アプリの両方で手順を完了する必要があります。

1. 財務と運用アプリで、次の手順に従います:

    1. Excel アドインを使用して **DualWriteProjectConfigurationEntity** エンティティを開きます。 アドインを使用するには、財務と運用の Excel アドインでデザイン モードを有効にし、ワークシートに **DualWriteProjectConfigurationEntity** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
    2. 二重書き込みマップおよびプロジェクトで問題があるレコードを選択および削除します。 二重書き込みマッピングごとに 2 つのレコードがあります。
    3. Excel アドインを使用して変更を公開します。 エンティティおよび基になるテーブルからレコードが削除されるので、この手順は重要です。
    4. 財務と運用または Dataverse 環境を再リンクする際にエラーを防ぐには、二重書き込みの構成が残っていないことを確認してください。

2. Dataverse で、以下の手順を実行します。

    1. Dataverse 環境にサインインします (例えば、`https://*****.crm.dynamics.com/`)。
    2. **詳細設定** \> **高度な検索** に移動します。
    3. **DualWrite ランタイムのコンフィギュレーション** を選択します。
    4. 表示する列を選択します。
    5. **結果** を表示して、コンフィギュレーションを表示します。
    6. すべてのインスタンスを削除します。

3. 財務と運用アプリで、次の手順に従います:

    1. Excel アドインを使用して **DualWriteProjectConfigurationEntity** エンティティを開きます。 アドインを使用するには、財務と運用の Excel アドインでデザイン モードを有効にし、ワークシートに **DualWriteProjectConfigurationEntity** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
    2. 二重書き込みマップおよびプロジェクトで問題があるレコードを選択および削除します。 二重書き込みマッピングごとに 2 つのレコードがあります。
    3. Excel アドインを使用して変更を公開します。 エンティティおよび基になるテーブルからレコードが削除されるので、この手順は重要です。
    4. 財務と運用または Dataverse 環境を再リンクする際にエラーを防ぐには、二重書き込みの構成が残っていないことを確認してください。

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>データベース全体のコピーを実行した後のライブ同期エラー

あるシステムから別のシステムにデータベース全体のコピーを実行してからデータベース操作を実行しようとすると、次のエラー メッセージが表示される場合があります。

*SecureConfig 組織 (???) は、実際の CRM 組織 (???) と一致しません。*

あるシステムで設定された二重書き込みの構成を別のシステムで使用できないようにするために、二重書き込みランタイム プラグインからエラー メッセージが表示されます。

問題を修正するには、データベースを復元した後、**msdyn_dualwriteruntimeconfig** テーブルのすべてのレコードを削除します。 詳細については、[二重書き込み環境のリンクの解除および再リンク](relink-environments.md) を参照してください。

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>二重書き込みマップでのクエリ フィルターの構文が正しくない場合に発生するライブ同期の問題

二重書き込みマップ フィルターのクエリ式は構文的に正しい場合でも、期待どおりに機能しない可能性があります。 フィルター式は、クエリ オブジェクトの個々のデータ ソースではなくエンティティ上に存在します。 したがって、生成された SQL クエリは予期される結果を返しません。

次に例を示します。

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

親がないプロジェクトは除外されると予想される場合があります。ただし、フィルターは次の例のようなクエリに変換されるため、フィルターは機能しません。

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

実際の結果は、`parentProject` フィールドが `null` と評価されます。 ただし、`null` は空の文字列と同じではありません。 この不一致により、クエリ フィルターは有効な結果を返しません。

問題を解決するには、次の手順に従います。

1. 拡張モデルに追加でき、`null` を空の文字列に変換するロジックでサポートされた計算列を追加します。

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. 既定の列の代わりに新しい計算列のフィルターを使用します。

フィルターを開発環境で評価するには、次の X++ コードを使用して結果を検証します。 このコードをスタンドアロン プログラムとして実行します。 二重書き込みマップでこれらのフィルターを使用する前に、エンティティに適用できるさまざまな種類のフィルターを評価するために使用できます。 クエリをデータベースに対して実行すると、不一致を評価できます。

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>財務と運用アプリのデータが Dataverse に同期されません

ライブ同期中に、データの一部のみが財務と運用アプリから Dataverse に同期されるか、データがまったく同期されないという問題が発生する可能性があります。

> [!NOTE]
> 開発時に、この問題を修正する必要があります。

問題の修正を開始する前に、次の前提条件を確認してください。

+ カスタム変更が単一のトランザクション スコープで記述されていることを確認してください。
+ ビジネス イベントおよび二重書き込みフレームワークは、`doinsert()`、`doUpdate()`、および `recordset()` 操作、または `skipBusinessEvents(true)` がマークされているレコードを処理しません。 コードがこれらの機能内にある場合、二重書き込みはトリガーされません。
+ ビジネス イベントは、マップされているデータ ソースに登録する必要があります。 一部のデータ ソースは、プログラム外部結合を使用し、財務と運用アプリでは読み取り専用としてマーク されている可能性があります。 これらのデータ ソースは追跡されません。
+ 変更は、マップされたフィールドに変更がある場合にのみトリガーされます。 マップされていないフィールド変更では、二重書き込みをトリガーできません。
+ フィルター評価が有効な結果を提供することを確認してください。

### <a name="troubleshooting-steps"></a>トラブルシューティングの手順

1. 二重書き込み管理者ページ上のフィールド マッピングを確認します。 フィールドが財務と運用アプリから Dataverse にマップされていない場合、フィールド は追跡されません。 たとえば、次の図では、**説明** フィールドは Dataverse から追跡されていますが、財務と運用アプリからは追跡されていません。 財務と運用アプリ内のそのフィールドへの変更は追跡されません。

    ![追跡されるフィールド。](media/live-sync-troubleshooting-1.png)

2. データ ソースがビジネス イベント定義で追跡されているかどうかを決定します。 たとえば、次の図では、**DefaultDimensionDAVs** テーブルと基になるテーブルのフィールドは変更のために追跡されません。 外部結合を使用し、読み取り専用としてマークされているデータ ソースは追跡されません。

    ![追跡されていないフィールド。](media/live-sync-troubleshooting-2.png)

3. 次の図に示すように、マップされたテーブル フィールドが **BUSINESSEVENTSDEFINITION** テーブルに表示されるかどうかを決定します。 クエリ結果で探しているフィールドが見つらない場合は、二重書き込みによってトリガーされません。

    ![テーブル内の追跡フィールド。](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>サンプル シナリオ

財務と運用アプリでは、連絡先レコードの住所は更新されますが、住所の変更は Dataverse に同期されません。 このシナリオは、**BusinessEventsDefinition** テーブルのレコードに、影響を受けるテーブルとエンティティの組み合わせがないために発生します。 具体的には、**LogisticsPostalAddress** テーブルは **smmContactpersonCDSV2Entity** エンティティの直接データ ソースではありません。 **smmContactpersonCDSV2Entity** エンティティには **smmContactPersonV2Entity** がデータ ソースとしてあり、**smmContactPersonV2Entity** には **LogisticsPostalAddressBaseEntity** がデータ ソースとしてあります。 **LogisticsPostalAddress** テーブルは、**LogisticsPostalAddressBaseEntity** のデータ ソースです。

同様の状況は、財務と運用アプリで変更されているテーブルが、それを含むエンティティに明らかにリンクされていない場合など、一部の非標準パターンで発生する可能性があります。 たとえば、基本住所データは **smmContactPersonCDSV2Entity** エンティティで計算されます。 二重書き込みフレームワークは、基になるテーブルに対する変更がエンティティにマップされる方法を決定しようとします。 通常、この方法で十分です。 ただし、場合によっては、リンクが非常に複雑であるため、具体的にする必要があります。 関連するテーブルの **RecId** がエンティティで直接利用可能であることを確認する必要があります。 次に、静的メソッドを追加して、テーブルの変更を監視します。

例については、**smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** 方法を確認します。 **CustCustomerV3entity** および **VendVendorV2Entity** は、この状況を処理するために変更されました。

問題を解決するには、次の手順に従います。

1. **PrimaryPostalAddressRecId** フィールドを **smmContactPersonV2Entity** エンティティに追加します。 内部用にします。

    ![smmContactPersonV2Entity エンティティに追加されたフィールド。](media/Troubleshoot_live_sync_issue_1.png)

2. **smmContactPersonCDSV2Entity** エンティティに同じフィールドを追加します。

    ![smmContactPersonCDSV2Entity エンティティに追加されたフィールド。](media/Troubleshoot_live_sync_issue_2.png)

3. **smmContactPersonCDSV2Entity** クラスに、次の方法を追加します。

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. データベースを同期し、アプリケーションをビルドします。
5. **smmContactPersonCDSV2Entity** エンティティで作成されたすべての二重書き込みマップを停止します。
6. マップを開始します。 **refentityname** の値が **BusinessEventsDefinition** テーブルの **smmContactPersonCDSV2Entity** に等しい行の **RefTableName** 列を使用して追跡を開始した新しいテーブル (この例では **LogisticsPostalAddress**) が表示されます。

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>複数のレコードが財務と運用アプリから Dataverse に同じバッチで送信されるレコードを作成する場合のエラー

どのトランザクションでも、財務と運用アプリはデータをバッチで作成し、それをバッチとして Dataverse に送信します。 2 つのレコードが同じトランザクションの一部として作成され、それらが相互に参照している場合、財務と運用アプリの次の例のようなエラーメッセージが表示される場合があります:

*エンティティ aaa_fundingsources にデータを書き込めません。値 {PC00...} で ebecsfs_contracts を検索できません。値が {PC00...} の aaa_fundingsources を検索できません。aaa_fundingsources への書き込みがエラー メッセージの例外メッセージで失敗しました: リモート サーバーがエラーを返しました: (400) 不正な要求。*

この問題を修正するには、財務と運用アプリでエンティティの関係を作成して、2 つのエンティティが相互に関連していること、および関連するレコードが同じトランザクションで処理されることを示します。

## <a name="enable-verbose-logging-of-error-messages"></a>エラー メッセージの詳細ログの有効化

財務と運用アプリでは、Dataverse 環境に関連するエラーが発生する場合があります。 エラー メッセージには、メッセージの全文またはその他の関連データが含まれていない場合があります。 詳細情報を取得するには、財務と運用アプリのすべてのプロジェクト構成の **DualWriteProjectConfigurationEntity** エンティティに存在する **IsDebugMode** フラグを設定することにより、詳細ログを有効にできます。

1. Excel アドインを使用して **DualWriteProjectConfigurationEntity** エンティティを開きます。 アドインを使用するには、財務と運用の Excel アドインでデザイン モードを有効にし、ワークシートに **DualWriteProjectConfigurationEntity** を追加します。 詳細については、[Excel でのエンティティ データの表示と更新](../../office-integration/use-excel-add-in.md) を参照してください。
2. プロジェクトの **IsDebugMode** フラグを **はい** に設定します。
3. シナリオを実行します。
4. 詳細なログは、**DualWriteErrorLog** テーブルで確認できます。 テーブル ブラウザを使用してデータを検索するには、次の URL を使用します: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`。
5. デバッグ モードでさらにログを取得するには、[KB 4595434 (二重書き込みライブ同期で反映される空白値の修正)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9) に更新をインストールします。

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>顧客または連絡先の住所を追加する際のエラー

財務と運用アプリや Dataverse の顧客または連絡先に住所を追加しようとする場合、次のようなエラー メッセージが表示される場合があります。

*エンティティ msdyn_partypostaladdresses へのデータの書き込みに失敗しました。DirPartyPostalAdlocationCDSEntity への書き込みに失敗し、次のエラー メッセージが表示されました。要求に失敗しました。ステータス コード BadRequest、CDS エラー コード: 0x80040265、応答メッセージ: プラグインでエラーが発生しました。場所 ID の属性値を持つレコードが既に存在します。エンティティ キーの場所 ID キーは固有の値がこの属性のセットに含まれている必要があります。一意の値を選択してやり直してください。*

この問題を修正するには、二重書き込みオーケストレーション パッケージ バージョン (2.2.2.60) をインストールして、次の表に示すように **アドレス** テーブルのキーを定義します。

| プロパティ | 先頭値 |
|---|---|
| 表示名 | **場所キー** |
| 氏名 | **msdyn_locationkey** |
| フィールド | **msdyn_locationid**、**parentid** |
| 状態 | **有効** |
| システム ジョブ | 空白 |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Dataverse で顧客を追加する際のエラー

Dataverse で顧客を追加しようとする際に、次のエラー メッセージが表示される場合があります。

*"RecordError0": "書き込みに失敗したエンティティ顧客 V3 に対して不明な例外 - 当事者タイプ '組織' の当事者レコードが見つかりませんでした"}。*

Dataverse で顧客を作成すると、新しい当事者番号が生成されます。 エラー メッセージは、顧客レコードが当事者と共に財務と運用アプリに同期されたときに表示されますが、別の当事者番号を持つ顧客レコードはすでに存在しています。

問題を修正するには、当事者ルックアップで顧客を検索します。 顧客が存在しない場合、新しい顧客レコードを作成します。 顧客が存在する場合は、既存の当事者を使用して新しい顧客レコードを作成します。

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>新規の顧客、仕入先、または連絡先を Dataverse に作成する場合のエラー

新規の顧客、仕入先、連絡先を Dataverse に作成しようとする場合、次のエラー メッセージが表示される場合があります。

*当事者のタイプを「DirOrdirization」から「DirPerson」に更新することはできません。代わりに、既存の当事者を削除し、その後、新しいタイプの挿入を実行する必要があります。*

Dataverse では、**msdyn_party** テーブルに番号順序があります。 Dataverse でアカウントが作成されると、新しい当事者が作成されます (例えば、**組織** タイプの **Party-001**)。 このデータは財務と運用アプリに送信されます。 Dataverse 環境がリセットされるか、財務と運用の環境が別の Dataverse 環境にリンクされ、Dataverse に新しい連絡先レコードが作成されると、**Party-001** で始まる新しい当事者値が作成されます。 この時、作成される当事者レコードは、**個人** タイプの **Party-001** です。 このデータが同期されると、**組織** タイプの当事者レコード **Party-001** がすでに存在するため、財務と運用アプリは上記のエラー メッセージを表示します。

この問題を修正するには、Dataverse の **msdyn_party** テーブルの **msdyn_partynumber** フィールドの自動番号順序を別の自動番号順序に変更します。

## <a name="performance-issue-with-customer-or-contact-mappings"></a>顧客マッピングまたは連絡先マッピングに関するパフォーマンスの問題

**getEntityDataSourceToFieldMapping** メソッド (**CustCustomerV3Entity** エンティティ内) メソッドと **getEntityDataSourceToFieldMapping** メソッド (**smmContactPersonCDSV2Entity** エンティティ内) をカスタマイズすることで、顧客と連絡先のライブ同期のパフォーマンスをわずかに改善できる場合があります。 これらのカスタマイズにより、**BusinessEventsDefinition** テーブルのレコード数が削減されます。 レコード数を減らすと、発生するイベントの数も減ります。

**CustCustomerV3Entity** エンティティの **getEntityDataSourceToFieldMapping** メソッドは、顧客の電子アドレスまたは住所の更新がビジネス イベントをトリガーすることを確認し、更新されたデータが Dataverse に送信されるようにします。 すべてのフィールドを使用せず、二重書き込みで情報を必要としない場合は、メソッドの適切な行をコメントアウトします。 このメソッドで追加されるすべての追跡フィールドとテーブルは、追跡テーブルと追跡エンティティの組み合わせのレコードを **BusinessEventsDefinition** テーブルに追加します。

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

同様に、**smmContactPersonCDSV2Entity** エンティティの **getEntityDataSourceToFieldMapping** メソッドは、連絡先の電子アドレスまたは住所の更新がビジネス イベントをトリガーすることを確認し、更新されたデータが Dataverse に送信されるようにします。 このメソッドでは、使用しないフィールドの行をコメントアウトできます。

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

メソッドを更新した後、次の手順に従います。

1. データベースを同期し、アプリケーションをビルドします。
2. **smmContactPersonCDSV2Entity** および **CustCustomerV3Entity** エンティティのすべての二重書き込みマップを停止します。
3. マップを開始します。 **smmContactPersonCDSV2Entity** および **CustCustomerV3Entity** エンティティと **BusinessEventsDefinition** テーブルに表示されるレコードが少なくなり、パフォーマンスがわずかに向上する可能性があります。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

