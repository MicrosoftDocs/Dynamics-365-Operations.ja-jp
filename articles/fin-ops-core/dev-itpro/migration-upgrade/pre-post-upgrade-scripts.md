---
title: Dynamics 365 Finance + Operations へのアップグレード時の PreSync および PostSync アップグレード スクリプトのトラブルシューティング
description: この記事では、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) へのアップグレードの一部として実行する PreSync および PostSync アップグレード スクリプトのトラブルシューティングについて説明します。
author: ttreen
ms.date: 04/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: 840db8baf0d212bb80161994277ecc7a21d081bf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866140"
---
# <a name="troubleshoot-presync-and-postsync-upgrade-scripts-during-upgrade-to-dynamics-365-finance--operations"></a>Dynamics 365 Finance + Operations へのアップグレード時の PreSync および PostSync アップグレード スクリプトのトラブルシューティング

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) へのアップグレードの一部として実行する PreSync および PostSync アップグレード スクリプトのトラブルシューティングについて説明します。

## <a name="scenario-1-you-receive-the-following-error-duplicate-key-was-found-for-the-object-name-dboinventdim-and-the-index-name-i_xxxsha1hashidx"></a>シナリオ 1: 次のようなエラーが発生しました: "オブジェクト名 'dbo.INVENTDIM' とインデックス名 'I_XXXSHA1HASHIDX' に重複するキーが見つかりました。"

最終同期中に、ダウンロードした同期ログの次の例のようなエラーが表示される場合があります。 (インデックス内のテーブル ID が異なる場合があります。)

> オブジェクト名 'dbo.INVENTDIM' およびインデックス名 'I\_698SHA1HASHIDX' の重複キーが検出されたため、CREATE UNIQUE INDEX ステートメントが終了しました。 重複キーの値は (5637144576、gsmp、B92BAF2504FD67FC15A56F2DFACE09127715B54B) です。 明細書は終了しました。 CREATE UNIQUE INDEX I\_698SHA1HASHIDX ON DBO.INVENTDIM(PARTITION,DATAAREAID,SHA1HASHHEX) WITH (MAXDOP = 1) ;

**原因**

この問題には、いくつかの原因が考えられます:

- このエラーは通常、Dynamics AX 2012 で **InventDim** テーブルの分析コード フィールドの 1 つの文字列サイズが拡張されているが、同じフィールドが Dynamics 365 で拡張されていない場合に表示されます。 拡張子はテーブル上で直接作成されたか、フィールドが派生する拡張データ型 (EDT) で作成された可能性があります。

    次のフィールドがハッシュ値を作成するのに使用されます:

    - ConfigId、InventBatchId
    - InventColorId
    - InventGtdId\_RU
    - InventLocationId
    - InventOwnerId\_RU
    - InventProfileId\_RU
    - InventSerialId
    - InventSiteId
    - InventSizeId
    - InventStatusId
    - InventStyleId
    - LicensePlateId
    - WMSlocationId

    テーブルのデータは切り詰められません。 ただし、実行時にハッシュ値が作成されると、バッファー内のデータが切り詰まれます。

    たとえば、**InventSizeId** フィールドの既定のサイズは 10 文字ですが、お客様が Dynamics AX 2012 でサイズを 12 文字に増やしたとします。 この場合、フィールド値 **1234567890AA** と **1234567890BB** は、実行時にバッファーに読み込まれると、両方とも **1234567890** に短縮されます。 したがって、ランタイム バッファーに重複する値が生じ、新しいハッシュ値を生成する **ReleaseUpdateDB72\_Invent::updateSHA1HashHexInInventDim** アップグレード メソッドでは、すべてのハッシュ値が一意として生成されません。

- データ アップグレード ジョブは期待通り実行されなかったか、期待通りに完了しませんでした。

    まず次の SQL クエリを実行します。

    ```SQL
    SELECT PARTITION, DATAAREAID, SHA1HASHHEX, COUNT(*)
    FROM INVENTDIM
    GROUP BY PARTITION, DATAAREAID, SHA1HASHHEX
    HAVING COUNT(*) > 1
    ```

    **SHA1HASHHEX** が空白の場合、ジョブは実行されませんでした。 この場合、次のコマンドを使用して、データ アップグレード ジョブを確認します。

    ```SQL
    select * from RELEASEUPDATESCRIPTSLOG
    where METHODNAME = 'updateSHA1HashHexInInventDim'
    ```

    **ソリューション**

    1. Dynamics AX 2012 **InventDim** テーブルのフィールド サイズを Dynamics 365 のフィールド サイズと比較します。 差異がある場合は、カスタマイズ拡張機能を使用して、関連するフィールドの文字列サイズを拡張することで、差異を調整する必要があります。
    1. ジョブが実行されなかった場合は、Dynamics 365 用 AX 2012 データベース アップグレード ツールキットからアップグレードを再開するか、またはレベル-1 開発環境の場合は Runbook の手順を再実行するようにしてください。

## <a name="scenario-2-an-error-occurs-when-you-run-the-releaseupdatedb72_fixedassetspostsyncupgradeassetdepbookjournaltransdimresolve-job"></a>シナリオ 2: ReleaseUpdateDB72_FixedAssets::postSyncUpgradeAssetDepBookJournalTransDimResolve ジョブを実行すると、エラーが発生します

**ReleaseUpdateDB72\_FixedAssets::postSyncUpgradeAssetDepBookJournalTransDimResolve** 転記の同期ジョブを実行すると、次のエラーが表示されることがあります:

> ビュー DimAttributeAssetTable 経由のテーブル AssetTable にレコードが存在しないため、法人 USMF で、値 ASSET00001 を持つ分析コード SystemGeneratedAttributeFixedAsset の DimensionAttributeValue レコードを返すことができません。  バッチ タスクが失敗しました: ビュー DimAttributeAssetTable 経由のテーブル AssetTable にレコードが存在しないため、法人 USMF で、値 ASSET00001 を持つ分析コード SystemGeneratedAttributeFixedAsset の DimensionAttributeValue レコードを返すことができません。 

**原因**

このエラーは、Dynamics AX 2012 **AssetTable** テーブルから資産が削除されたものの、**ledgerjournaltrans\_asset** テーブルの関連レコードが残っているために発生します。

これらの孤立レコードについては、次の SQL スクリプトを使用して確認できます。

```SQL
select * from ledgerjournaltrans_asset
where assetid not in (select assetid from assettable)
```

**ソリューション**

> [!IMPORTANT]
> データを削除する前に、データベース バックアップがあることを確認してください。

次の SQL ステートメントを実行することで、レコードを削除できます。

```SQL
--
-- This source code or script is freeware and is provided on an "as is" basis without warranties of any kind, 
-- whether express or implied, including without limitation warranties that the code is free of defect, 
-- fit for a particular purpose or non-infringing. The entire risk as to the quality and performance of 
-- the code is with the end user.
--
delete from ledgerjournaltrans_asset
where assetid not in (select assetid from assettable)
```

## <a name="scenario-3-an-error-occurs-when-you-run-the-releaseupdatedb10_casemanagementupdatecasecategorytypemajor-job"></a>シナリオ 3: ReleaseUpdateDB10_CaseManagement::updateCaseCategoryTypeMajor ジョブを実行すると、エラーが発生します

**ReleaseUpdateDB10\_CaseManagement::updateCaseCategoryTypeMajor** 転記の同期ジョブを実行すると、**ReleaseUpdateScriptsErrorLog** テーブルからの次のエラーが表示されることがあります:

> === 'PostSync' ステップで失敗した x++ データ アップグレード スクリプトの開始。 ===  
{ ClassName: "ReleaseUpdateDB10\_CaseManagement"、MethodName: "updateCaseCategoryTypeMajor"、会社: "DAT", DataParition: "initial", ErrorCount: "1"、ErrorMessage: " ロール別ケース カテゴリ セキュリティ (CaseCategoryRole) のレコードを編集できません。 カテゴリ タイプ: なし。  
レコードが既に存在します。 バッチ タスクが失敗しました: ロール別ケース カテゴリ セキュリティ (CaseCategoryRole) のレコードを編集できません。 カテゴリ タイプ: なし。  
レコードが既に存在します。" }  
{ ClassName: "ReleaseUpdateDB72  
=== 'PostSync' ステップで失敗した x++ データ アップグレード スクリプトの開始。 ===  
{ ClassName: "ReleaseUpdateDB10\_CaseManagement"、MethodName: "updateCaseCategoryTypeMajor"、会社: "DAT", DataParition: "initial", ErrorCount: "1"、ErrorMessage: " ロール別ケース カテゴリ セキュリティ (CaseCategoryRole) のレコードを編集できません。 カテゴリ タイプ: なし。  
レコードが既に存在します。 バッチ タスクが失敗しました: ロール別ケース カテゴリ セキュリティ (CaseCategoryRole) のレコードを編集できません。 カテゴリ タイプ: なし。  
レコードが既に存在します。" }  
_停止された DBSync モニタリング。Microsot.Dynamics.Ax.Xpp.ErrorException: セッションの作成に失敗しました; ユーザーに Microsoft Dynamics 365 for Finance and Operations にログオンするための適切な権限があることを確認してください。_

**原因**

Dynamics AX 2012 では、**Web** タイプの **CaseCategoryType** 列挙 (enum) で、ほとんどの場合に値 "9" が使用されているため、このエラーが発生します。 ただし、Dynamics 365 では、**Web** 値は使用されなくなり、同じ値が列挙値 **CaseCategoryType::FMLA** で使用できます。 列挙は拡張可能であるため、同じ値を割り当てることができます。

列挙値を確認するには、次の SQL ステートメントを実行します。

```SQL
select t1.name as enumvaluename, t1.enumvalue
from enumvaluetable  t1
join enumidtable t2 on t2.id = t1.enumid
where t2.name = 'CaseCategoryType'
```

**ソリューション**

1. **CaseCategoryRole** テーブルで、**Web** タイプのレコードを削除します。
1. Dynamics AX 2012 の列挙の値を確認します。 前述のとおり、ほとんどの場合にこの値は "9" になります。
1. 次の SQL ステートメントを使用して、**CaseCategoryRole** テーブルのレコードを削除します。 (必要に応じて値を編集します。)

```SQL
--
-- This source code or script is freeware and is provided on an "as is" basis without warranties of any kind, 
-- whether express or implied, including without limitation warranties that the code is free of defect, 
-- fit for a particular purpose or non-infringing. The entire risk as to the quality and performance of 
-- the code is with the end user.
--
delete from CaseCategoryRole
where CaseCategoryType = 9 --Edit to be the enum value of CaseCategoryType::Web in AX2012
```

## <a name="scenario-4-you-receive-the-following-error-cannot-edit-a-record-in-table-name-tablename---invalid-column-name-columnname"></a>シナリオ 4: 次のエラーが表示されます: "テーブル名 (TableName) のレコードを編集できません - 列名 'COLUMNNAME' が無効です。"

PreSync または PostSync アップグレード ジョブを実行すると、次の例に似たエラーが表示されることがあります。 参照フィールドが Dynamics 365 に存在しない場合は、レガシ テーブル トリガーに関連したエラーである可能性があります。

> テーブル名 (TableName) のレコードを編集できません。  
SQL データベースによってエラーが出されました。 オブジェクト サーバー DataUpgrade\_バッチ: \[Microsoft\]\[SQL Server の ODBC ドライバー 17\]\[SQL Server\]列名 'DEPRACATEDCOLUMNNAME' が無効です。 UPDATE T1 SET VALUE=?,RECVERSION=? FROM TABLENAME セッション 10 (管理者) バッチ タスクに失敗しました: 銀行口座 (TableName) のレコードを編集できません。  
SQL データベースによってエラーが出されました。"

**ソリューション**

1. SQL Management Studio (SSMS) を使用してデータベースに接続します。
1. オブジェクト エクスプローラーで、データベースとテーブルを展開し、エラー メッセージで参照されているテーブルを検索します。
1. そのテーブルでトリガーをレビューし、カスタム トリガーがあるかどうかを確認します。 Dynamics 365 で作成されるほとんどの標準トリガーには、**SysDbLog**、**SysEvenCud**、または **AIF** などの接頭語が付けられます。
1. 問題の原因と思われるカスタムトリガーをスクリプト化するには、各トリガーを選択したまま (または右クリック) にしてから、**トリガーのスクリプト名 \> 作成先 \> 新規クエリ編集ウィンドウ** の順に選択します。
1. スクリプトの完了後、**編集 \> 検索** に移動して、エラー メッセージで参照されるフィールドがスクリプトに存在するかどうかを特定します。 トリガー内で一致が見つかった場合は、トリガーを無効またはドロップする必要があります。
