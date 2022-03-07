---
title: システム テーブル
description: このトピックでは、システム テーブルについて説明します。
author: RobinARH
ms.date: 11/06/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0920725f35adcca979c26402e33e3e094dac4e3
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782049"
---
# <a name="system-tables"></a>システム テーブル

[!include [banner](../includes/banner.md)]

このトピックには、システム クラスで使用できるドキュメントが含まれています。 

> [!NOTE]
> このトピックは、システム テーブル メンバーの完全な一覧ではありません。 テーブルとそのメンバーの完全な一覧は、アプリケーション エクスプローラーで確認できます。

## <a name="common"></a>共通

共通テーブルとは、すべてのテーブルに対して基本クラスです。 これにデータは含まれていません。 多様な方法で任意のテーブルを参照するために主に X++ コードで使用されます。

### <a name="methods"></a>メソッド

| 方法                       | 説明                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| aosValidateDelete            | サーバー上で、指定されたレコードをテーブルから削除できることを検証します。                                              |
| aosValidateInsert            | サーバー上で、指定されたレコードを挿入できることを検証します。                                                          |
| aosValidateRead              | サーバー上で、指定されたレコードを読み取れることを検証します。                                                              |
| aosValidateUpdate            | サーバー上で、指定されたレコードを更新できることを検証します。                                                           |
| buf2con                      | X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。                                                       |
| canSubmitToWorkflow          | ワークフローへの送信が可能かどうかを示します。                                                                       |
| caption                      | テーブルのキャプション プロパティを取得および設定します。                                                                              |
| checkInvalidFieldAccess      | 無効なフィールド アクセスを取得および設定します。                                                                                         |
| checkRecord                  | 必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。                                                |
| checkRestrictedDeleteActions | レコードが削除されるかどうかを示すプロパティを取得および設定します。                                                  |
| クリア                        | テーブル バッファーからすべての行を削除します。                                                                                     |
| 会社                      | レコードの法人を示すプロパティを取得および設定します。                                                    |
| con2buf                      | コンテナをテーブル バッファに展開します。                                                                                 |
| concurrencyModel             | レコードの更新に使用する既定の同時実行モデルを取得および設定します。                                                       |
| context                      | コンテキスト プロパティを取得および設定します。                                                                                         |
| データ                         | テーブルから行を取得します。                                                                                             |
| dataSource                   | テーブルのデータ ソースを取得します。                                                                                     |
| dbOpInTransaction            | 失敗した場合にデータベース操作が正しく閉じられていることを確認します。                                                      |
| defaultField                 | テーブルのフィールドの既定値を設定します。                                                                           |
| defaultRow                   | 非対話型の場合、テーブルのフィールドの既定値を設定します。                                                |
| 削除                       | テーブルから現在のレコードを削除します。                                                                                  |
| disableCache                 | キャッシュが無効かどうかを示すプロパティを取得および設定します。                                                      |
| dispose                      | XRecord オブジェクトによって使用されているリソースを解放します。                                                                     |
| doClear                      | 現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。                  |
| doDelete                     | 現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。              |
| doInsert                     | テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。                      |
| doUpdate                     | 現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。                             |
| doValidateDelete             | レコードを削除できる検証するアクションを実行します。                                                               |
| 等しい                        | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                                        |
| fieldAccessRight             | フィールドのアクセス権を返します。                                                                                             |
| fieldBufferAccessRight       | 現在のレコードのフィールド アクセス権を返します。                                                                      |
| fieldState                   | テーブル バッファーのフィールドの状態を設定するか返します。                                                                   |
| getAllowRedefault            | 既定値に再度設定することを許可されているフィールドの一覧を返します。                                                                  |
| getDefaultingDependencies    | デフォルトの依存関係を保持するコンテナーを返します。                                                                   |
| getExtension                 | テーブル拡張機能を返します。                                                                                                |
| getFieldValue                | テーブル バッファから指定したフィールドの値を取得します。                                                                  |
| getInstanceRelationType      | InstanceRelationType ID に対応するテーブルの名前を返します。                                                     |
| getPhysicalTableName         | 物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。                    |
| getPresenceFieldData         | 指定されたフィールドから PresenceInfo 値を取得します。                                                                  |
| getSQLStatement              | レコードをデータベースから取得するために使用される SQL ステートメントを取得します。                                                    |
| getTableInInstanceHierarchy  |                                                                                                                             |
| getTableType                 | テーブルのタイプを示します。                                                                                            |
| helpField                    | 指定したフィールドのヘルプ テキストを含む文字列を取得します。                                                     |
| initValue                    | フィールドを既定値に初期化します。                                                                                   |
| inputStatus                  | テーブル バッファーの現在の入力ステータスを設定するか返します。                                                               |
| insert                       | テーブルにレコードを挿入します。                                                                                          |
| interactiveContext           | テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。                                                        |
| isFieldDataRetrieved         | 指定されたフィールドのデータが取得されたかどうかをチェックします。                                                              |
| isFieldSet                   | フィールドがセットまたは既定状態かどうかをチェックします。                                                                        |
| isFormDataSource             | データ ソースがフォームであるかどうかを示します。                                                                                |
| isNewRecord                  | レコードがまだ保存されていない新しいレコードである場合は true を返します。                                                  |
| isPartOfUOWSaveChanges       |                                                                                                                             |
| isTempDb                     | テーブルのタイプが SQL TempDB であるかどうかを示します。                                                                      |
| isTmp                        | これが一時テーブルであるかどうかを示します。                                                                                |
| joinChild                    | 現在のレコードの結合子を検索します。                                                                                 |
| joinParent                   | 現在のレコードの結合の親を検索します。                                                                                |
| linkPhysicalTableInstance    | レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。                                              |
| マージ                        | 現在のテーブルを指定されたテーブルとマージします。                                                                          |
| modifiedField                | 指定したフィールドを元通りに変更します。                                                                               |
| modifiedFieldValue           | 指定したフィールドを元の値に変更します。                                                                         |
| orig                         | 現在のレコードの元の値を取得します。                                                                        |
| overwriteSystemfields        | システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。                                         |
| postLoad                     | レコードが読み取られた後に実行されます。                                                                                         |
| queryTimedOut                | クエリが実行の時間制限を超過したかどうかを示します。                                                          |
| queryTimeout                 | クエリの実行に対する時間制限を示すプロパティを取得および設定します。                                      |
| readCommittedLock            |                                                                                                                             |
| readPast                     | レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。    |
| recordLevelSecurity          | レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。                                      |
| relatedTable                 | テーブル バッファのリンクに関連するバッファーを設定するか返します。                                                             |
| hasRelatedTable              | 外部キー制約バッファがテーブルにリンクされているかどうかを示します。                                                 |
| renamePrimaryKey             | この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。      |
| reread                       | テーブルからレコードを再読み取りします。                                                                                          |
| RowCount                     | テーブル内の行数を取得します。                                                                                  |
| selectForUpdate              | 読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。                          |
| selectLocked                 | ロックされているレコードを選択するかどうかを示します。                                                                                 |
| selectRefRecord              | 参照されているフィールド ID によりレコードを選択します。                                                                                  |
| selectWithRepeatableRead     | 反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。                                               |
| setConnection                | この表のユーザー接続を設定します。                                                                                    |
| setCrossPartition            | テーブルのパーティション間分割を設定またはリセットします。                                                                            |
| setFieldValue                | レコード バッファーのフィールド値を設定します。                                                                                  |
| setSQLTracing                | SQL トレース モードを有効または無効にします。                                                                                       |
| setTempDB                    |                                                                                                                             |
| setTmp                       | データベースに保存されていない場合にテーブルを設定します。                                                                 |
| setTmpData                   | 一時的なテーブルの内容を指定されたデータに設定します。                                                             |
| setXDSContext                | 新しい XDS コンテキストを設定します。                                                                                                       |
| skipDatabaseLog              | データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。                                            |
| skipDataMethods              | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                            |
| skipDeleteActions            | テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。                                      |
| skipDeleteMethod             | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                            |
| skipEvents                   | xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。               |
| skipPostLoad                 | テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。               |
| skipTTSCheck                 | 更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。 |
| suppressWarnings             | このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。                                    |
| tableAccessRight             | テーブルのアクセス権を返します。                                                                                             |
| tableBufferAccessRight       | 現在のレコードのテーブル アクセス権を返します。                                                                      |
| toolTipField                 | 指定されたフィールドの HelpText 値を取得します。                                                                       |
| toolTipRecord                | 現在のレコードのツールヒント値を取得します。                                                                         |
| ttsabort                     | ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。                                                     |
| ttsbegin                     | ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。                |
| ttscommit                    | ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。                                                    |
| 更新                       | 現在のレコードを更新します。                                                                                                 |
| validateDelete               | 現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。                                   |
| validateField                | 指定されたフィールドが有効かどうかを判定します。                                                                            |
| validateFieldValue           |                                                                                                                             |
| validateRelations            |                                                                                                                             |
| validateWrite                | 現在のレコードが有効で、書き込み可能な状態かどうかを判別します。                                                     |
| validTimeStateUpdateMode     | カーソルで有効な時間状態更新モードを設定します。                                                                          |
| wasCached                    | データの取得元となった場所を指定します。                                                                   |
| write                        | レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。                                                                 |
| xml                          | 現在のオブジェクトを表す XML 文字列を取得します。                                                                 |
| takeOwnershipOfTempDBTable   |                                                                                                                             |
| useExistingTempDBTable       |                                                                                                                             |

### <a name="fields"></a>フィールド

| フィールド                 | 種類        | 拡張型         | 列挙型タイプ | 説明 |
|-----------------------|-------------|-----------------------|------------------|-------------|
| CreatedBy             | 文字列      | CreatedBy             |                  |             |
| CreatedDateTime       | UtcDateTime | CreatedDateTime       |                  |             |
| CreatedTransactionId  | Int64       | CreatedTransactionId  |                  |             |
| dataAreaId            | 文字列      | DataAreaId            |                  |             |
| DEL\_CreatedTime      | Int         | DEL\_CreatedTime      |                  |             |
| DEL\_ModifiedTime     | Int         | DEL\_ModifiedTime     |                  |             |
| ModifiedBy            | 文字列      | ModifiedBy            |                  |             |
| ModifiedDateTime      | UtcDateTime | ModifiedDateTime      |                  |             |
| ModifiedTransactionId | Int64       | ModifiedTransactionId |                  |             |
| パーティション             | Int64       | パーティション             |                  |             |
| RecId                 | Int64       | RecId                 |                  |             |
| recVersion            | 整数     | RecVersion            |                  |             |
| RelationType          | Int64       | RelationType          |                  |             |
| RowNumber             | Int         | RowNumber             |                  |             |
| SequenceNum           | Int64       | SequenceNum           |                  |             |
| TableId               | Int         | TableId               |                  |             |
| UnionAllBranchId      | Int         | UnionAllBranchId      |                  |             |

### <a name="relations"></a>リレーション

| リレーション   | テーブル    |
|------------|----------|
| dataAreaId | DataArea |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| RecId | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common)

## <a name="dataarea"></a>DataArea
DataArea テーブルには、データベースで作成された会社の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型 | 列挙型タイプ | 説明                                                                                                               |
|--------------|---------|---------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| alwaysNative | 列挙    |               | ブール値          |                                                                                                                           |
| id           | 文字列  | DataAreaId    |                  | データ領域の ID                                                                                                    |
| isVirtual    | 列挙    |               | ブール値          |                                                                                                                           |
| 名前         | 文字列  | UserIdStr     |                  | 氏名                                                                                                                      |
| パーティション    | Int64   | パーティション     |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid        | Int64   |  Recid         |                  |                                                                                                                           |
| recVersion   | 整数 | RecVersion    |                  |                                                                                                                           |
| timeZone     | 列挙    |               | タイム ゾーン         |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション  | テーブル      |
|-----------|------------|
| id        | DataArea   |
| パーティション | パーティション |

### <a name="indexes"></a>インデックス

| 指数  | 重複を許可します | フィールド |
|--------|------------------|--------|
| ID     | 無               |        |
| IdOnly | 有              |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [DataArea テーブル](#dataarea)

## <a name="databaselog"></a>DatabaseLog
DatabaseLog テーブルは、SysDatabaseLog テーブルのコンフィギュレーション情報を格納します。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| domainId          | 文字列      | DomainId          |                  | ドメインの ID                                                                                                         |
| logField          | 整数     | FieldId           |                  | フィールド ID                                                                                                          |
| logTable          | 整数     | TableId           |                  | テーブル ID                                                                                                          |
| logType           | 列挙        |                   | DatabaseLogType  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ      | フィールド |
|------------------|--------|
| logFieldRelation |        |

### <a name="relations"></a>リレーション

| リレーション              | テーブル           |
|-----------------------|-----------------|
| Relation\_DatabaseLog | DEL\_DomainInfo |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| ログリスト | 無               |        |
| RecId   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [DatabaseLog テーブル](#databaselog)

## <a name="del_accessrightslist"></a>DEL\_AccessRightsList
このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| accessType        | 列挙        |                   | AccessType       |                                                                                                                           |
| accessTypeFkeyUse | 列挙        |                   | AccessType       |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| domainId          | 文字列      | DomainId          |                  | ドメインの ID                                                                                                         |
| elementName       | 文字列      | UtilElementName   |                  | アプリケーション要素の名前です。                                                                                          |
| groupId           | 文字列      | UserGroupId       |                  | ユーザー グループの ID                                                                                                     |
| id                | Int         |                   |                  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| parentId          | Int         |                   |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| レコード タイプ        | 列挙        |                   | AccessRecordType |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                    | テーブル              |
|-----------------------------|--------------------|
| Relation\_AccessRightsList1 | UtilIdElements     |
| Relation\_AccessRightsList2 | UtilIdElements     |
| Relation\_AccessRightsList3 | DEL\_DomainInfo    |
| Relation\_AccessRightsList4 | DEL\_UserGroupInfo |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| 要素 | 有              |        |
| グループ化   | 無               |        |
| RecId   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) DEL-AccessRightsList テーブル

## <a name="del_companydomainlist"></a>DEL_CompanyDomainList
CompanyDomainList テーブルには、DomainInfo および DataArea テーブル間の関連付けが含まれています。 ドメインごとにセキュリティ権限が付与されます。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型      | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|--------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| companyId         | 文字列      | SelectableDataArea |                  | 選択可能な会社の ID                                                                                         |
| createdBy         | 文字列      | CreatedBy          |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime    |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime   |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| domainId          | 文字列      | DomainId           |                  | ドメインの ID                                                                                                         |
| modifiedBy        | 文字列      | ModifiedBy         |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime   |                  |                                                                                                                           |
| RecId             | Int64       | RecId              |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion         |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション  | テーブル           |
|-----------|-----------------|
| companyId | DataArea        |
| domainId  | DEL\_DomainInfo |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| 法人 | 無               |        |
| ドメイン  | 無               |        |
| RecId   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) DEL_CompanyDomainList テーブル

## <a name="del_domaininfo"></a>DEL_DomainInfo
このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明       |
|------------|---------|---------------|------------------|-------------------|
| id         | 文字列  | DomainId      |                  | ドメインの ID |
| 名前       | 文字列  | UserIdStr     |                  | 氏名              |
| RecId      | Int64   | RecId         |                  |                   |
| recVersion | 整数 | RecVersion    |                  |                   |

### <a name="relations"></a>リレーション

| リレーション | テーブル           |
|----------|-----------------|
| id       | DEL\_DomainInfo |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) DEL_DomainInfo テーブル

## <a name="del_usergroupinfo"></a>DEL_UserGroupInfo
UserGroupInfo テーブルには、使用可能なユーザー グループの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明           |
|------------|---------|---------------|------------------|-----------------------|
| id         | 文字列  | UserGroupId   |                  | ユーザー グループの ID |
| 名前       | 文字列  | UserIdStr     |                  | 氏名                  |
| RecId      | Int64   | RecId         |                  |                       |
| recVersion | 整数 | RecVersion    |                  |                       |

### <a name="relations"></a>リレーション

| リレーション | テーブル         |
|----------|---------------|
| id       | UserGroupInfo |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) DEL_UserGroupInfo テーブル

## <a name="del_usergrouplist"></a>DEL_UserGroupList
UserGroupList テーブルには、各ユーザー グループに関連付けられているユーザーのリストが含まれています。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| groupId           | 文字列      | UserGroupId       |                  | ユーザー グループの ID                                                                                                     |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| userId            | 文字列      | UserId            |                  | ユーザー ID                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                 | テーブル              |
|--------------------------|--------------------|
| Relation\_UserGroupList1 | DEL\_UserGroupInfo |
| Relation\_UserGroupList2 | UserInfo           |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| GroupId | 無               |        |
| RecId   | 無               |        |
| UserId  | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) DEL_UserGroupList テーブル

## <a name="modelsecpolruntimeex"></a>ModelSecPolRuntimeEx
ModelSecPolRuntimeEx テーブルは、セキュリティ ポリシーを適用するために必要なランタイム メタデータが保存されます。

### <a name="fields"></a>フィールド

| フィールド                 | 種類      | 拡張型 | 列挙型タイプ | 説明 |
|-----------------------|-----------|---------------|------------------|-------------|
| ConstrainedTable      | 文字列    |               |                  |             |
| ContextString         | 文字列    |               |                  |             |
| ContextType           | Int       |               |                  |             |
| DEL\_ElementHandle    | Int       |               |                  |             |
| DEL\_IsEnabled        | Int       |               |                  |             |
| DEL\_LayerId          | Int       |               |                  |             |
| ElementHandle         | Int       |               |                  |             |
| IsDirty               | Int       |               |                  |             |
| IsEnabled             | Int       |               |                  |             |
| IsModeled             | Int       |               |                  |             |
| LayerId               | Int       |               |                  |             |
| ModeledQueryDebugInfo | 文字列    |               |                  |             |
| ModeledQueryPackData  | コンテナー |               |                  |             |
| 氏名                  | 文字列    |               |                  |             |
| 工程             | Int       |               |                  |             |
| PrimaryTableAOTName   | 文字列    |               |                  |             |
| QueryObjectAOTName    | 文字列    |               |                  |             |
| RecId                 | Int64     | RecId         |                  |             |
| recVersion            | 整数   | RecVersion    |                  |             |

### <a name="indexes"></a>インデックス

| 指数               | 重複を許可します | フィールド           |
|---------------------|------------------|------------------|
| ConstrainedTableIdx | 有              | ConstrainedTable |
| RecIDIdx            | 無               | RecId            |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [ModelSecPolRuntimeEx テーブル](#modelsecpolruntimeex)

## <a name="modelsecpolruntimeview"></a>ModelSecPolRuntimeView
ModelSecPolRuntimeView ビューは、現在アクティブなセキュリティ ポリシーのランタイム メタデータを表示します。

### <a name="fields"></a>フィールド

| フィールド                 | 種類      | 拡張型 | 列挙型タイプ | 説明 |
|-----------------------|-----------|---------------|------------------|-------------|
| ConstrainedTable      | 文字列    |               |                  |             |
| ContextString         | 文字列    |               |                  |             |
| ContextType           | Int       |               |                  |             |
| ElementHandle         | Int       |               |                  |             |
| IsDirty               | Int       |               |                  |             |
| IsModeled             | Int       |               |                  |             |
| LayerId               | Int       |               |                  |             |
| ModeledQueryDebugInfo | 文字列    |               |                  |             |
| ModeledQueryPackData  | コンテナー |               |                  |             |
| 氏名                  | 文字列    |               |                  |             |
| 工程             | Int       |               |                  |             |
| PrimaryTableAOTName   | 文字列    |               |                  |             |
| QueryObjectAOTName    | 文字列    |               |                  |             |
| RecId                 | Int64     | RecId         |                  |             |
| recVersion            | 整数   | RecVersion    |                  |             |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [ModelSecPolRuntimeView テーブル](#modelsecpolruntimeview)

## <a name="partitions"></a>パーティション
Partitions テーブルには、システム内のデータ パーティションの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                                             |
|-------------------|-------------|-------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| createdBy         | 文字列      | CreatedBy         |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| modifiedBy        | 文字列      | ModifiedBy        |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| 名前              | 文字列      | UserIdStr         |                  | 名前 (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))          |
| PartitionKey      | 文字列      | PartitionKey      |                  | パーティション キー (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid             | Int64       |  Recid             |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |
| recVersion        | 整数     | RecVersion        |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS))               |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="relations"></a>リレーション

| リレーション     | テーブル      |
|--------------|------------|
| PartitionKey | パーティション |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| PartitionIdx | 無               |        |
| RecIDIdx     | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [Partitions テーブル](#partitions)

## <a name="printjobheader"></a>PrintJobHeader
PrintJobHeader テーブルには、現在のプリント ジョブに関する情報が含まれています

### <a name="fields"></a>フィールド

| フィールド               | 種類        | 拡張型    | 列挙型タイプ | 説明                                                                                                               |
|---------------------|-------------|------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdBy           | 文字列      | CreatedBy        |                  |                                                                                                                           |
| createdDateTime     | UtcDateTime | CreatedDateTime  |                  |                                                                                                                           |
| dataAreaId          | 文字列      | DataAreaId       |                  |                                                                                                                           |
| dEL\_CreatedTime    | 整数     | DEL\_CreatedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| deviceName          | 文字列      |                  |                  |                                                                                                                           |
| 形式              | 列挙        |                  | PrintFormat      |                                                                                                                           |
| ジョブの説明      | 文字列      |                  |                  |                                                                                                                           |
| ジョブ ステータス           | 列挙        |                  | PrintJobStatus   |                                                                                                                           |
| ジョブ タイプ             | 文字列      |                  |                  |                                                                                                                           |
| ページ数       | Int         |                  |                  |                                                                                                                           |
| パーティション           | Int64       | パーティション        |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| printedBy           | 文字列      | ユーザー ID           |                  | ユーザー ID                                                                                                           |
| 印刷日         | 日付        |                  |                  |                                                                                                                           |
| 印刷時刻         | Int         |                  |                  |                                                                                                                           |
| printerInfo         | コンテナー   |                  |                  |                                                                                                                           |
| printFromPage       | Int         |                  |                  |                                                                                                                           |
| printNumcopies      | Int         |                  |                  |                                                                                                                           |
| printOnServer       | 列挙        |                  | ブール値          |                                                                                                                           |
| printToPage         | Int         |                  |                  |                                                                                                                           |
| RecId               | Int64       | RecId            |                  |                                                                                                                           |
| recVersion          | 整数     | RecVersion       |                  |                                                                                                                           |
| unlimitedPageHeight | 列挙        |                  | ブール値          |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション   | テーブル      |
|------------|------------|
| dataAreaId | DataArea   |
| パーティション  | パーティション |
| printedBy  | UserInfo   |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| CreatedBy   | 有              |        |
| CreatedDate | 有              |        |
| JobType     | 有              |        |
| RecId       | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [PrintJobHeader テーブル](#printjobheader)

## <a name="printjobpages"></a>PrintJobPages
PrintJobPages テーブルには、プリント ジョブの現在印刷中のページに関する情報が含まれています

### <a name="fields"></a>フィールド

| フィールド            | 種類      | 拡張型 | 列挙型タイプ | 説明                                                                                                               |
|------------------|-----------|---------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| dataAreaId       | 文字列    | DataAreaId    |                  |                                                                                                                           |
| numberOfLines    | Int       |               |                  |                                                                                                                           |
| pageContents     | コンテナー |               |                  |                                                                                                                           |
| pageNo           | Int       |               |                  |                                                                                                                           |
| pagesHeaderRecId | Int64     | RecId         |                  | データベースのレコードの固有 ID                                                                                  |
| パーティション        | Int64     | パーティション     |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid            | Int64     |  Recid         |                  |                                                                                                                           |
| recVersion       | 整数   | RecVersion    |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                 | テーブル          |
|--------------------------|----------------|
| dataAreaId               | DataArea       |
| pagesHeaderRecId         | PrintJobHeader |
| パーティション                | パーティション     |
| Relation\_PrintJobPages1 | PrintJobHeader |

### <a name="indexes"></a>インデックス

| 指数  | 重複を許可します | フィールド |
|--------|------------------|--------|
| PageNo | 無               |        |
| RecId  | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [PrintJobPages テーブル](#printjobpages)

## <a name="securableobject"></a>SecurableObject
SecurableObject テーブルには、セキュリティ フレームワークによるすべてのセキュリティ コンポーネント参照が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型      | 列挙型タイプ | 説明                             |
|------------|---------|--------------------|------------------|-----------------------------------------|
| ChildName  | 文字列  | SecurableChildName |                  | セキュリティ保護可能なオブジェクトの子の名前です。 |
| 氏名       | 文字列  | SecurableName      |                  | セキュリティ保護可能なオブジェクトの名前です。       |
| RecId      | Int64   | RecId              |                  |                                         |
| recVersion | 整数 | RecVersion         |                  |                                         |
| 種類       | 列挙    |                    | SecurableType    |                                         |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ | フィールド |
|-------------|--------|
| AutoLookup  |        |

### <a name="indexes"></a>インデックス

| 指数            | 重複を許可します | フィールド |
|------------------|------------------|--------|
| NameChildTypeIdx | 無               |        |
| RecIDIdx         | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurableObject テーブル](#securableobject)

## <a name="securityduty"></a>SecurityDuty
### <a name="fields"></a>フィールド

| フィールド       | 種類   | 拡張型           | 列挙型タイプ | 説明 |
|-------------|--------|-------------------------|------------------|-------------|
| 識別子  | 文字列 | SecurityDutyIdentifier  |                  |             |
| 氏名        | 文字列 | SecurityDutyName        |                  |             |
| 説明 | 文字列 | SecurityDutyDescription |                  |             |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification | 氏名   |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド     |
|---------------|------------------|------------|
| RecIDIdx      | 無               | RecId      |
| IdentifierIdx | 無               | 識別子 |
| NameIdx       | 有              | 氏名       |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityDuty テーブル](#securityduty)

## <a name="securityentrypointinferredtables"></a>SecurityEntryPointInferredTables
### <a name="fields"></a>フィールド

| フィールド                | 種類   | 拡張型 | 列挙型タイプ     | 説明 |
|----------------------|--------|---------------|----------------------|-------------|
| EntryPointName       | 文字列 | SecurableName |                      |             |
| 種類                 | 列挙   |               | SecurableType        |             |
| TableName            | 文字列 | SecurableName |                      |             |
| AllowEdit            | 列挙   |               | ブール値              |             |
| AllowCreate          | 列挙   |               | ブール値              |             |
| AllowDelete          | 列挙   |               | ブール値              |             |
| ValidTimeStateUpdate | 列挙   |               | ValidTimeStateUpdate |             |

### <a name="indexes"></a>インデックス

| 指数              | 重複を許可します | フィールド                                                |
|--------------------|------------------|-------------------------------------------------------|
| RecIDIdx           | 無               | RecId                                                 |
| EntryPointTableIdx | 無               | EntryPointName, Type, TableName, ValidTimeStateUpdate |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityEntryPointInferredTables テーブル](#securityentrypointinferredtables)

## <a name="securityentrypointlink"></a>SecurityEntryPointLink
SecurityEntryPointLink テーブルには、メニュー項目や Web メニュー項目の AOT ノードで指定されているセキュリティ保護可能なオブジェクト マッピングへのエントリ ポイントが含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| EntryPoint      | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| PermissionOwner | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                          | テーブル           |
|-----------------------------------|-----------------|
| Relation\_SecurityEntryPointLink1 | SecurableObject |
| Relation\_SecurityEntryPointLink2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| EntryPointIdx | 無               |        |
| RecIDIdx      | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityEntryPointLink テーブル](#securityentrypointlink)

## <a name="securitypermission"></a>SecurityPermission
SecurityPermission テーブルには、フォーム、レポート、セキュリティ コードのアクセス許可、およびサービス操作の AOT ノードで指定されているアクセス許可の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| アクセス          | 列挙        |               | AccessRight      |                                          |
| グループ化           | 列挙        |               | AccessRight      |                                          |
| 所有者           | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecurableObject | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                      | テーブル           |
|-------------------------------|-----------------|
| Relation\_SecurityPermission1 | SecurableObject |
| Relation\_SecurityPermission2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数               | 重複を許可します | フィールド |
|---------------------|------------------|--------|
| OwnerGroupObjectIdx | 無               |        |
| RecIDIdx            | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityPermission テーブル](#securitypermission)

## <a name="securityprivilege"></a>SecurityPrivilege
### <a name="fields"></a>フィールド

| フィールド       | 種類   | 拡張型                | 列挙型タイプ | 説明 |
|-------------|--------|------------------------------|------------------|-------------|
| 識別子  | 文字列 | SecurityPrivilegeIdentifier  |                  |             |
| 氏名        | 文字列 | SecurityPrivilegeName        |                  |             |
| 説明 | 文字列 | SecurityPrivilegeDescription |                  |             |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification | 氏名   |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド     |
|---------------|------------------|------------|
| RecIDIdx      | 無               | RecId      |
| IdentifierIdx | 無               | 識別子 |
| NameIdx       | 有              | 氏名       |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityPrivilege テーブル](#securityprivilege)

## <a name="securityrole"></a>SecurityRole
SecurityRole テーブルには、セキュリティ AOT ロール ノードで定義したロールの一覧が反映されます。

### <a name="fields"></a>フィールド

| フィールド                    | 種類    | 拡張型           | 列挙型タイプ | 説明                       |
|--------------------------|---------|-------------------------|------------------|-----------------------------------|
| AllowCurrentRecords      | 列挙    |                         | AccessRight      |                                   |
| AllowFutureRecords       | 列挙    |                         | AccessRight      |                                   |
| AllowPastRecords         | 列挙    |                         | AccessRight      |                                   |
| AotName                  | 文字列  | SecurityRoleAotName     |                  | AOT のロールの名前です。  |
| ContextString            | 文字列  |                         |                  |                                   |
| DEL\_AllowCurrentRecords | 列挙    |                         | AccessRight      |                                   |
| DEL\_AllowFutureRecords  | 列挙    |                         | AccessRight      |                                   |
| DEL\_AllowPastRecords    | 列挙    |                         | AccessRight      |                                   |
| DEL\_IsEnabled           | 列挙    |                         | ブール値          |                                   |
| 説明              | 文字列  | SecurityRoleDescription |                  | セキュリティ ロールの説明です。 |
| IsEnabled                | 列挙    |                         | ブール値          |                                   |
| 氏名                     | 文字列  | SecurityRoleName        |                  | セキュリティ ロールの名前です。    |
| RecId                    | Int64   | RecId                   |                  |                                   |
| recVersion               | 整数 | RecVersion              |                  |                                   |
| UserLicenseType          | 列挙    |                         | UserLicenseType  |                                   |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="indexes"></a>インデックス

| 指数      | 重複を許可します | フィールド |
|------------|------------------|--------|
| AotNameIdx | 無               |        |
| NameIdx    | 有              |        |
| RecIDIdx   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRole テーブル](#securityrole)

## <a name="securityroleassignmentrule"></a>SecurityRoleAssignmentRule
動的にユーザーをロールに割り当てるためのルール

### <a name="fields"></a>フィールド

| フィールド                     | 種類        | 拡張型             | 列挙型タイプ | 説明                                                                                                               |
|---------------------------|-------------|---------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| MembershipRuleDescription | 文字列      | MembershipRuleDescription |                  | 自動ロール メンバーシップ ルールの説明                                                                         |
| MembershipRuleName        | 文字列      | MembershipRuleName        |                  | 自動ロール メンバーシップ ルールの名前                                                                                |
| パーティション                 | Int64       | パーティション                 |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid                     | Int64       |  Recid                     |                  |                                                                                                                           |
| recVersion                | 整数     | RecVersion                |                  |                                                                                                                           |
| RuleQuery                 | コンテナー   |                           |                  |                                                                                                                           |
| SecurityRole              | Int64       | RecId                     |                  | データベースのレコードの固有 ID                                                                                  |
| 有効期間開始日                 | UtcDateTime |                           |                  |                                                                                                                           |
| ValidTo                   | UtcDateTime |                           |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                 | テーブル        |
|--------------------------|--------------|
| パーティション                | パーティション   |
| SecurityRole             | SecurityRole |
| SecurityRoleRelationShip | SecurityRole |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| AlternateKey | 無               |        |
| RecIDIdx     | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRoleAssignmentRule テーブル](#securityroleassignmentrule)

## <a name="securityroledutyexplodedgraph"></a>SecurityRoleDutyExplodedGraph
### <a name="fields"></a>フィールド

| フィールド        | 種類  | 拡張型 | 列挙型タイプ | 説明 |
|--------------|-------|---------------|------------------|-------------|
| SecurityRole | Int64 | RecId         |                  |             |
| SecurityDuty | Int64 | RecId         |                  |             |

### <a name="relations"></a>リレーション

| リレーション     | テーブル        |
|--------------|--------------|
| SecurityRole | SecurityRole |
| SecurityDuty | SecurityDuty |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド                     |
|-------------|------------------|----------------------------|
| RecIDIdx    | 無               | RecId                      |
| RoleDutyIdx | 無               | SecurityRole、SecurityDuty |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRoleDutyExplodedGraph テーブル](#securityroledutyexplodedgraph)

## <a name="securityroleexplodedgraph"></a>SecurityRoleExplodedGraph
SecurityRoleExplodedGraph テーブルには、セキュリティ ロール ノードの AOT サブロール ノードで定義されているすべてのロール関係 (直接または間接) が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|---------|---------------|------------------|------------------------------------------|
| RecId           | Int64   | RecId         |                  |                                          |
| recVersion      | 整数 | RecVersion    |                  |                                          |
| RefCount        | Int     |               |                  |                                          |
| SecurityRole    | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| SecuritySubRole | Int64   | RecId         |                  | データベースのレコードの固有 ID |

### <a name="relations"></a>リレーション

| リレーション                | テーブル        |
|-------------------------|--------------|
| Relation\_SecurityRole1 | SecurityRole |
| Relation\_SecurityRole2 | SecurityRole |
| SecurityRole            | SecurityRole |
| SecuritySubRole         | SecurityRole |

### <a name="indexes"></a>インデックス

| 指数          | 重複を許可します | フィールド |
|----------------|------------------|--------|
| RecIDIdx       | 無               |        |
| RoleSubRoleIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRoleExplodedGraph テーブル](#securityroleexplodedgraph)

## <a name="securityrolepermissionoverride"></a>SecurityRolePermissionOverride
SecurityRolePermissionOverride テーブルには、セキュリティ ロール AOT ノードで指定されているアクセス許可の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| アクセス          | 列挙        |               | AccessRight      |                                          |
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecurableObject | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| SecurityRole    | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                                  | テーブル           |
|-------------------------------------------|-----------------|
| Relation\_SecurityRolePermissionOverride1 | SecurityRole    |
| Relation\_SecurityRolePermissionOverride2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| RecIDIdx      | 無               |        |
| RoleObjectIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRolePermissionOverride テーブル](#securityrolepermissionoverride)

## <a name="securityroleprivilegeexplodedgraph"></a>SecurityRolePrivilegeExplodedGraph
### <a name="fields"></a>フィールド

| フィールド             | 種類  | 拡張型 | 列挙型タイプ | 説明 |
|-------------------|-------|---------------|------------------|-------------|
| SecurityRole      | Int64 | RecId         |                  |             |
| SecurityPrivilege | Int64 | RecId         |                  |             |

### <a name="relations"></a>リレーション

| リレーション          | テーブル             |
|-------------------|-------------------|
| SecurityRole      | SecurityRole      |
| SecurityPrivilege | SecurityPrivilege |

### <a name="indexes"></a>インデックス

| 指数            | 重複を許可します | フィールド                          |
|------------------|------------------|---------------------------------|
| RecIDIdx         | 無               | RecId                           |
| RolePrivilegeIdx | 無               | SecurityRole、SecurityPrivilege |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRolePrivilegeExplodedGraph テーブル](#securityroleprivilegeexplodedgraph)

## <a name="securityroleruntime"></a>SecurityRoleRuntime
### <a name="fields"></a>フィールド

| フィールド                | 種類   | 拡張型      | 列挙型タイプ | 説明 |
|----------------------|--------|--------------------|------------------|-------------|
| SecurityRole         | Int64  | RecId              |                  |             |
| 氏名                 | 文字列 | SecurableName      |                  |             |
| ChildName            | 文字列 | SecurableChildName |                  |             |
| 種類                 | 列挙   |                    | SecurableType    |             |
| CreateAccess         | Int    |                    |                  |             |
| ReadAccess           | Int    |                    |                  |             |
| UpdateAccess         | Int    |                    |                  |             |
| DeleteAccess         | Int    |                    |                  |             |
| CorrectAccess        | Int    |                    |                  |             |
| InvokeAccess         | Int    |                    |                  |             |
| PastCreateAccess     | Int    |                    |                  |             |
| PastReadAccess       | Int    |                    |                  |             |
| PastUpdateAccess     | Int    |                    |                  |             |
| PastDeleteAccess     | Int    |                    |                  |             |
| PastCorrectAccess    | Int    |                    |                  |             |
| PastInvokeAccess     | Int    |                    |                  |             |
| CurrentCreateAccess  | Int    |                    |                  |             |
| CurrentReadAccess    | Int    |                    |                  |             |
| CurrentUpdateAccess  | Int    |                    |                  |             |
| CurrentDeleteAccess  | Int    |                    |                  |             |
| CurrentCorrectAccess | Int    |                    |                  |             |
| CurrentInvoke        | Int    |                    |                  |             |
| FutureCreateAccess   | Int    |                    |                  |             |
| FutureReadAccess     | Int    |                    |                  |             |
| FutureUpdateAccess   | Int    |                    |                  |             |
| FutureDeleteAccess   | Int    |                    |                  |             |
| FutureCorrectAccess  | Int    |                    |                  |             |
| FutureInvokeAccess   | Int    |                    |                  |             |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド                |
|--------------------|-----------------------|
| AutoIdentification | Name、ChildName、Type |

### <a name="indexes"></a>インデックス

| 指数              | 重複を許可します | フィールド                |
|--------------------|------------------|-----------------------|
| RecIDIdx           | 無               | RecId                 |
| RoleIDIdx          | 有              | SecurityRole          |
| SecurableObjectIdx | 有              | タイプ、名前、ChildName |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRoleRuntime テーブル](#securityroleruntime)

## <a name="securityroletaskgrant"></a>SecurityRoleTaskGrant
SecurityRoleTaskGrant テーブルには、AOT セキュリティ ロール ノードによって定義されるとおり、ローカルから職務権限へのマッピングとロールから特権へのマッピングの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|--------------|---------|---------------|------------------|------------------------------------------|
| RecId        | Int64   | RecId         |                  |                                          |
| recVersion   | 整数 | RecVersion    |                  |                                          |
| SecurityRole | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| SecurityTask | Int64   | RecId         |                  | データベースのレコードの固有 ID |

### <a name="relations"></a>リレーション

| リレーション                         | テーブル        |
|----------------------------------|--------------|
| Relation\_SecurityRoleTaskGrant1 | SecurityRole |
| Relation\_SecurityRoleTaskGrant2 | SecurityTask |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| RecIDIdx    | 無               |        |
| RoleTaskIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityRoleTaskGrant テーブル](#securityroletaskgrant)

## <a name="securitysegregationofdutiesconflict"></a>SecuritySegregationOfDutiesConflict
SecuritySegregationOfDutiesConflict テーブルには、ロールへのユーザーの割り当て試行の結果生じた職務分掌競合と、権限のあるユーザーから提供された競合の解決策に関する情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド                   | 種類        | 拡張型                      | 列挙型タイプ              | 説明                                                                                                               |
|-------------------------|-------------|------------------------------------|-------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| AssignmentMode          | 列挙        |                                    | RoleAssignmentMode            |                                                                                                                           |
| createdBy               | 文字列      | CreatedBy                          |                               |                                                                                                                           |
| createdDateTime         | UtcDateTime | CreatedDateTime                    |                               |                                                                                                                           |
| dEL\_CreatedTime        | 整数     | DEL\_CreatedTime                   |                               | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| DEL\_ExistingTask       | Int64       |  Recid                              |                               |                                                                                                                           |
| dEL\_ModifiedTime       | 整数     | DEL\_ModifiedTime                  |                               | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| DEL\_NewTask            | Int64       |  Recid                              |                               |                                                                                                                           |
| ExistingDuty            | Int64       |  Recid                              |                               |                                                                                                                           |
| ExistingRole            | Int64       | RecId                              |                               | データベースのレコードの固有 ID                                                                                  |
| ExistingTask            | Int64       | RecId                              |                               | データベースのレコードの固有 ID                                                                                  |
| modifiedBy              | 文字列      | ModifiedBy                         |                               |                                                                                                                           |
| modifiedDateTime        | UtcDateTime | ModifiedDateTime                   |                               |                                                                                                                           |
| NewDuty                 | Int64       | RecId                              |                               |                                                                                                                           |
| NewRole                 | Int64       | RecId                              |                               | データベースのレコードの固有 ID                                                                                  |
| NewTask                 | Int64       | RecId                              |                               | データベースのレコードの固有 ID                                                                                  |
| パーティション               | Int64       | パーティション                          |                               | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| ReasonForOverride       | VarString   | SegregationOfDutiesOverrideComment |                               | 職務分掌違反を上書きする理由に関するコメント                                          |
| RecId                   | Int64       | RecId                              |                               |                                                                                                                           |
| recVersion              | 整数     | RecVersion                         |                               |                                                                                                                           |
| 解像度              | 列挙        |                                    | SegregationOfDutiesResolution |                                                                                                                           |
| SegregationOfDutiesRule | Int64       | RecId                              |                               | データベースのレコードの固有 ID                                                                                  |
| ユーザー                    | 文字列      | UserId                             |                               | ユーザー ID                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                       | テーブル                           |
|--------------------------------|---------------------------------|
| ExistingDuty                   | SecurityDuty                    |
| ExistingRole                   | SecurityRole                    |
| ExistingRoleRelationship       | SecurityRole                    |
| ExistingTaskRelationship       | SecurityTask                    |
| NewDuty                        | SecurityDuty                    |
| NewRole                        | SecurityRole                    |
| NewRoleRelationship            | SecurityRole                    |
| NewTaskRelationship            | SecurityTask                    |
| パーティション                      | パーティション                      |
| Relation\_SecuritySegregation7 | UserInfo                        |
| SecuritySODRuleRelationship    | SecuritySegregationOfDutiesRule |
| SegregationOfDutiesRule        | SecuritySegregationOfDutiesRule |
| ユーザー                           | UserInfo                        |

### <a name="indexes"></a>インデックス

| 指数           | 重複を許可します | フィールド       |
|-----------------|------------------|--------------|
| AlternateKey    | 無               |              |
| ExistingDutyIdx | 有              | ExistingDuty |
| ExistingRoleIdx | 有              |              |
| ExistingTaskIdx | 有              |              |
| NewDutyIdx      | 有              | NewDuty      |
| NewRoleIdx      | 有              |              |
| NewTaskIdx      | 有              |              |
| RecIDIdx        | 無               |              |
| UserInfoIdx     | 有              |              |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecuritySegregationOfDutiesConflict テーブル](#securitysegregationofdutiesconflict)

## <a name="securitysegregationofdutiesrule"></a>SecuritySegregationOfDutiesRule
SecuritySegregationOfDutiesRule テーブルは、職務分掌を規定するルールを格納します。

### <a name="fields"></a>フィールド

| フィールド                   | 種類        | 拡張型               | 列挙型タイプ            | 説明                                                                      |
|-------------------------|-------------|-----------------------------|-----------------------------|----------------------------------------------------------------------------------|
| DEL\_FirstSecurityTask  | Int64       | RecId                       |                             |                                                                                  |
| DEL\_SecondSecurityTask | Int64       | RecId                       |                             |                                                                                  |
| FirstDuty               | Int64       | RecId                       |                             |                                                                                  |
| FirstSecurityTask       | Int64       | RecId                       |                             | データベースのレコードの固有 ID                                         |
| 軽減策              | 文字列      | SecurityMitigation          |                             | 職務分掌ルールの違反に関するリスクの軽減策 |
| 氏名                    | 文字列      | SegregationOfDutiesRuleName |                             | 職務分掌ルールの名前                                           |
| RecId                   | Int64       | RecId                       |                             |                                                                                  |
| recVersion              | 整数     | RecVersion                  |                             |                                                                                  |
| リスク                    | 文字列      | SecurityRisk                |                             | 職務分掌ルールの違反に関するリスク                    |
| SecondDuty              | Int64       | RecId                       |                             |                                                                                  |
| SecondSecurityTask      | Int64       | RecId                       |                             | データベースのレコードの固有 ID                                         |
| 重要度                | 列挙        |                             | SegregationOfDutiesSeverity |                                                                                  |
| 有効期間開始日               | UtcDateTime |                             |                             |                                                                                  |
| ValidTo                 | UtcDateTime |                             |                             |                                                                                  |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="relations"></a>リレーション

| リレーション                       | テーブル        |
|--------------------------------|--------------|
| FirstDuty                      | SecurityDuty |
| FirstSecurityTaskRelationship  | SecurityTask |
| SecondDuty                     | SecurityDuty |
| SecondSecurityTaskRelationship | SecurityTask |

### <a name="indexes"></a>インデックス

| 指数              | 重複を許可します | フィールド     |
|--------------------|------------------|------------|
| AlternateKey       | 無               |            |
| FirstSecurityDuty  | 有              | FirstDuty  |
| NameIdx            | 無               |            |
| RecIDIdx           | 無               |            |
| SecondSecurityDuty | 有              | SecondDuty |
| SecondSecurityTask | 有              |            |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecuritySegregationOfDutiesRule テーブル](#securitysegregationofdutiesrule)

## <a name="securitysubrole"></a>SecuritySubRole
SecuritySubRole テーブルには、セキュリティ ロール AOT ノードで指定されているすべてのサブロールが含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecurityRole    | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| SecuritySubRole | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                          | テーブル        |
|-----------------------------------|--------------|
| Relation\_SecuritySubRole1        | SecurityRole |
| Relation\_SecurityTaskPermission2 | SecurityRole |
| SecurityRole                      | SecurityRole |
| SecuritySubRole                   | SecurityRole |

### <a name="indexes"></a>インデックス

| 指数          | 重複を許可します | フィールド |
|----------------|------------------|--------|
| RecIDIdx       | 無               |        |
| RoleSubRoleIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecuritySubRole テーブル](#securitysubrole)

## <a name="securitysubtask"></a>SecuritySubTask
SecuritySubTask テーブルには、セキュリティ職務権限 AOT ノードで指定されている職務権限から特権へのマッピングが含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecuritySubTask | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| SecurityTask    | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                   | テーブル        |
|----------------------------|--------------|
| Relation\_SecuritySubTask1 | SecurityTask |
| Relation\_SecuritySubTask2 | SecurityTask |

### <a name="indexes"></a>インデックス

| 指数          | 重複を許可します | フィールド |
|----------------|------------------|--------|
| RecIDIdx       | 無               |        |
| TaskSubTaskIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecuritySubTask テーブル](#securitysubtask)

## <a name="securitytask"></a>SecurityTask
SecurityTask テーブルには、AOT セキュリティ職務権限およびセキュリティ特権ノードで定義されている職務権限と権限の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型           | 列挙型タイプ | 説明                                           |
|-----------------|---------|-------------------------|------------------|-------------------------------------------------------|
| AotName         | 文字列  | SecurityTaskAotName     |                  | AOT のタスクの名前です。                      |
| 説明     | 文字列  | SecurityTaskDescription |                  | プロセス サイクル、職務権限、または権限の説明です。 |
| IsEnabled       | 列挙    |                         | ブール値          |                                                       |
| IsPermissionSet | 列挙    |                         | ブール値          |                                                       |
| 氏名            | 文字列  | SecurityTaskName        |                  | プロセス サイクル、職務権限、または権限の名前です。    |
| RecId           | Int64   | RecId                   |                  |                                                       |
| recVersion      | 整数 | RecVersion              |                  |                                                       |
| 種類            | 列挙    |                         | SecurityTaskType |                                                       |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="indexes"></a>インデックス

| 指数      | 重複を許可します | フィールド |
|------------|------------------|--------|
| AotNameIdx | 無               |        |
| NameIdx    | 有              |        |
| RecIDIdx   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityTask テーブル](#securitytask)

## <a name="securitytaskentrypoint"></a>SecurityTaskEntryPoint
SecurityTaskEntryPoint テーブルには、AOT セキュリティ権限ノードで指定されている特権からエントリ ポイントへのマッピングの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| EntryPoint      | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| PermissionGroup | 列挙        |               | AccessRight      |                                          |
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecurityTask    | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                          | テーブル           |
|-----------------------------------|-----------------|
| Relation\_SecurityTaskEntryPoint1 | SecurityTask    |
| Relation\_SecurityTaskEntryPoint2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数             | 重複を許可します | フィールド |
|-------------------|------------------|--------|
| RecIDIdx          | 無               |        |
| TaskEntryPointIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityTaskEntryPoint テーブル](#securitytaskentrypoint)

## <a name="securitytaskexplodedgraph"></a>SecurityTaskExplodedGraph
SecurityTaskExplodedGraph テーブルには、セキュリティ職務権限 AOT ノードで指定されている職務権限から特権へのマッピングが含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|---------|---------------|------------------|------------------------------------------|
| RecId           | Int64   | RecId         |                  |                                          |
| recVersion      | 整数 | RecVersion    |                  |                                          |
| RefCount        | Int     |               |                  |                                          |
| SecuritySubTask | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| SecurityTask    | Int64   | RecId         |                  | データベースのレコードの固有 ID |

### <a name="relations"></a>リレーション

| リレーション                             | テーブル        |
|--------------------------------------|--------------|
| Relation\_SecurityTaskExplodedGraph1 | SecurityTask |
| Relation\_SecurityTaskExplodedGraph2 | SecurityTask |

### <a name="indexes"></a>インデックス

| 指数          | 重複を許可します | フィールド |
|----------------|------------------|--------|
| RecIDIdx       | 無               |        |
| SubTaskIdx     | 有              |        |
| TaskSubTaskIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityTaskExplodedGraph テーブル](#securitytaskexplodedgraph)

## <a name="securitytaskpermission"></a>SecurityTaskPermission
SecurityTaskPermission テーブルは使用されていません。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|---------|---------------|------------------|------------------------------------------|
| アクセス          | Int     |               |                  |                                          |
| レベル           | Int     |               |                  |                                          |
| RecId           | Int64   | RecId         |                  |                                          |
| recVersion      | 整数 | RecVersion    |                  |                                          |
| SecurableObject | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| SecurityTask    | Int64   | RecId         |                  | データベースのレコードの固有 ID |

### <a name="relations"></a>リレーション

| リレーション                          | テーブル           |
|-----------------------------------|-----------------|
| Relation\_SecurityTaskPermission1 | SecurityTask    |
| Relation\_SecurityTaskPermission2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| RecIDIdx      | 無               |        |
| TaskObjectIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityTaskPermission テーブル](#securitytaskpermission)

## <a name="securitytaskpermissionoverride"></a>SecurityTaskPermissionOverride
SecurityTaskPermissionOverride テーブルには、セキュリティ権限 AOT ノードで指定されているアクセス許可の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型 | 列挙型タイプ | 説明                              |
|-----------------|-------------|---------------|------------------|------------------------------------------|
| アクセス          | 列挙        |               | AccessRight      |                                          |
| RecId           | Int64       | RecId         |                  |                                          |
| recVersion      | 整数     | RecVersion    |                  |                                          |
| SecurableObject | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| SecurityTask    | Int64       | RecId         |                  | データベースのレコードの固有 ID |
| 有効期間開始日       | UtcDateTime |               |                  |                                          |
| ValidTo         | UtcDateTime |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                                  | テーブル           |
|-------------------------------------------|-----------------|
| Relation\_SecurityTaskPermissionOverride1 | SecurityTask    |
| Relation\_SecurityTaskPermissionOverride2 | SecurableObject |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| RecIDIdx      | 無               |        |
| TaskObjectIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityTaskPermissionOverride テーブル](#securitytaskpermissionoverride)

## <a name="securityuserrole"></a>SecurityUserRole
SecurityUserRole テーブルには、ユーザーからロールへのマッピングが含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型 | 列挙型タイプ     | 説明                                                                                                               |
|------------------|-------------|---------------|----------------------|---------------------------------------------------------------------------------------------------------------------------|
| AssignmentMode   | 列挙        |               | RoleAssignmentMode   |                                                                                                                           |
| AssignmentStatus | 列挙        |               | RoleAssignmentStatus |                                                                                                                           |
| パーティション        | Int64       | パーティション     |                      | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid            | Int64       |  Recid         |                      |                                                                                                                           |
| recVersion       | 整数     | RecVersion    |                      |                                                                                                                           |
| SecurityRole     | Int64       | RecId         |                      | データベースのレコードの固有 ID                                                                                  |
| ユーザー             | 文字列      | UserId        |                      | ユーザー ID                                                                                                           |
| 有効期間開始日        | UtcDateTime |               |                      |                                                                                                                           |
| ValidTo          | UtcDateTime |               |                      |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                    | テーブル        |
|-----------------------------|--------------|
| パーティション                   | パーティション   |
| Relation\_SecurityRole      | SecurityRole |
| Relation\_SecurityUserRole3 | UserInfo     |
| SecurityRole                | SecurityRole |
| ユーザー                        | UserInfo     |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| RecIDIdx    | 無               |        |
| UserRoleIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityUserRole テーブル](#securityuserrole)

## <a name="securityuserrolecondition"></a>SecurityUserRoleCondition
SecurityUserRoleCondition テーブルには、ユーザーからロールへのマッピングを制限する会社の一覧が含まれています。 役割のマッピングに特定のユーザーのエントリが存在しない場合、ユーザーには、その役割の権限がすべての企業に付与されます。

### <a name="fields"></a>フィールド

| フィールド            | 種類    | 拡張型 | 列挙型タイプ | 説明                                                                                                               |
|------------------|---------|---------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| ControllingKey   | int64   |               |                  |                                                                                                                           |
| DataArea         | 文字列  | DataAreaId    |                  | データ領域の ID                                                                                                    |
| パーティション        | Int64   | パーティション     |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid            | Int64   |  Recid         |                  |                                                                                                                           |
| recVersion       | 整数 | RecVersion    |                  |                                                                                                                           |
| SecurityUserRole | Int64   | RecId         |                  | データベースのレコードの固有 ID                                                                                  |

### <a name="relations"></a>リレーション

| リレーション                             | テーブル            |
|--------------------------------------|------------------|
| DataArea                             | DataArea         |
| パーティション                            | パーティション       |
| Relation\_SecurityUserRoleCondition1 | SecurityUserRole |
| Relation\_SecurityUserRoleCondition2 | DataArea         |
| SecurityUserRole                     | SecurityUserRole |

### <a name="indexes"></a>インデックス

| 指数               | 重複を許可します | フィールド |
|---------------------|------------------|--------|
| RecIDIdx            | 無               |        |
| UserRoleDataAreaIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SecurityUserRoleCondition テーブル](#securityuserrolecondition)

## <a name="sqldescribe"></a>SqlDescribe
SqlDescribe テーブルは、テーブルおよびフィールドのメタデータを格納するために使用します。 SqlDataDictionary::tablemetadata メソッドは、バックエンド データベース クエリを使用して、このテーブルを設定します。

### <a name="fields"></a>フィールド

| フィールド            | 種類    | 拡張型   | 列挙型タイプ | 説明                      |
|------------------|---------|-----------------|------------------|----------------------------------|
| array            | Int     |                 |                  |                                  |
| fieldId          | 整数 | FieldId         |                  | フィールド ID                 |
| fieldType        | 列挙    |                 | 種類            |                                  |
| flags            | Int     |                 |                  |                                  |
| 名前             | 文字列  | UtilElementName |                  | アプリケーション要素の名前です。 |
| nullable         | 列挙    |                 | ブール値          |                                  |
| numericPrecision | Int     |                 |                  |                                  |
| numericScale     | Int     |                 |                  |                                  |
| RecId            | Int64   | RecId           |                  |                                  |
| recVersion       | 整数 | RecVersion      |                  |                                  |
| rightJustify     | 列挙    |                 | ブール値          |                                  |
| 影付き           | 列挙    |                 | ブール値          |                                  |
| sqlName          | 文字列  | UtilElementName |                  | アプリケーション要素の名前です。 |
| strSize          | Int     |                 |                  |                                  |
| tabId            | 整数 | TableId         |                  | テーブル ID                 |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ     | フィールド |
|-----------------|--------|
| fieldIdRelation |        |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| フィールド   | 無               |        |
| RecId   | 無               |        |
| SqlName | 有              |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlDescribe テーブル](#sqldescribe)

## <a name="sqldictionary"></a>SqlDictionary
SqlDictionary テーブルは、テーブルおよびフィールド メタデータに関するデータベースの現在の状態について説明します。 このテーブルには、ビューおよび表の依存関係情報も含まれています。 データベース同期エンジンは、SqlDictionary テーブルを使用して、AOT とデータベースを同期させるために必要なアクションを決定します。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型   | 列挙型タイプ | 説明                      |
|--------------|---------|-----------------|------------------|----------------------------------|
| array        | Int     |                 |                  |                                  |
| fieldId      | 整数 | FieldId         |                  | フィールド ID                 |
| fieldType    | 列挙    |                 | 種類            |                                  |
| flags        | Int     |                 |                  |                                  |
| 名前         | 文字列  | UtilElementName |                  | アプリケーション要素の名前です。 |
| nullable     | 列挙    |                 | ブール値          |                                  |
| RecId        | Int64   | RecId           |                  |                                  |
| recVersion   | 整数 | RecVersion      |                  |                                  |
| rightJustify | 列挙    |                 | ブール値          |                                  |
| 影付き       | 列挙    |                 | ブール値          |                                  |
| sqlName      | 文字列  | UtilElementName |                  | アプリケーション要素の名前です。 |
| strSize      | Int     |                 |                  |                                  |
| tabId        | 整数 | TableId         |                  | テーブル ID                 |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ     | フィールド |
|-----------------|--------|
| fieldIdRelation |        |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| フィールド | 無               |        |
| RecId | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlDictionary テーブル](#sqldictionary)

## <a name="sqlparameters"></a>SqlParameters
SqlParameters テーブルは、パラメーターと値の組み合わせの形式でデータベースに関連する情報を格納します。 このテーブルは Microsoft Dynamics Ax 2009 では使用されません。

### <a name="fields"></a>フィールド

| フィールド      | 型    | 拡張型 | 列挙型タイプ | 説明 |
|------------|---------|---------------|------------------|-------------|
| id         | Int     |               |                  |             |
| iParm      | Int     |               |                  |             |
| iValue     | Int     |               |                  |             |
| parm       | 文字列  |               |                  |             |
| RecId      | Int64   | RecId         |                  |             |
| recVersion | 整数 | RecVersion    |                  |             |
| 値      | 文字列  |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| Parm  | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlParameters テーブル](#sqlparameters)

## <a name="sqlstatistics"></a>SqlStatistics
SqlStatistics テーブルは、ユーザーの関連するデータベースの統計情報を格納します。 このテーブルは Microsoft Dynamics Ax 2009 では使用されません。

### <a name="fields"></a>フィールド

| フィールド             | 型        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| indexId           | 整数     | IndexId           |                  | インデックス ID                                                                                                          |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| objectType        | 列挙        |                   | SqlStatType      |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| tabId             | 整数     | TableId           |                  | テーブル ID                                                                                                          |
| userId            | 文字列      | UserId            |                  | ユーザー ID                                                                                                           |
| value1            | Int         |                   |                  |                                                                                                                           |
| value10           | Int         |                   |                  |                                                                                                                           |
| value11           | Int         |                   |                  |                                                                                                                           |
| value12           | Int         |                   |                  |                                                                                                                           |
| value2            | Int         |                   |                  |                                                                                                                           |
| value3            | Int         |                   |                  |                                                                                                                           |
| value4            | Int         |                   |                  |                                                                                                                           |
| value5            | Int         |                   |                  |                                                                                                                           |
| value6            | Int         |                   |                  |                                                                                                                           |
| value7            | Int         |                   |                  |                                                                                                                           |
| value8            | Int         |                   |                  |                                                                                                                           |
| value9            | Int         |                   |                  |                                                                                                                           |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ     | フィールド |
|-----------------|--------|
| indexIdRelation |        |

### <a name="relations"></a>リレーション

| リレーション            | テーブル         |
|---------------------|---------------|
| Relation\_SqlStats1 | SqlStatistics |
| Relation\_SqlStats2 | UserInfo      |
| tabId               | SqlStatistics |
| userId              | UserInfo      |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |
| RecId | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlStatistics テーブル](#sqlstatistics)

## <a name="sqlstorage"></a>SqlStorage
SqlStorage テーブルには、テーブル スペースに関する情報とその Oracle 属性が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明      |
|------------|---------|---------------|------------------|------------------|
| id         | Int     |               |                  |                  |
| indexId    | 整数 | IndexId       |                  | インデックス ID |
| objectType | Int     |               |                  |                  |
| 上書き   | 列挙    |               | ブール値          |                  |
| parm       | 文字列  |               |                  |                  |
| RecId      | Int64   | RecId         |                  |                  |
| recVersion | 整数 | RecVersion    |                  |                  |
| tabId      | 整数 | TableId       |                  | テーブル ID |
| 値      | 文字列  |               |                  |                  |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ     | フィールド |
|-----------------|--------|
| indexIdRelation |        |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlStorageテーブル](#sqlstorage)

## <a name="sqlsyncinfo"></a>SqlSyncInfo
SqlSyncInfo テーブルは、データベース同期プロセス中にメッセージと DDL ステートメントをキャプチャします。 同期プロセスが完了すると、テーブル内の情報が削除されます。

### <a name="fields"></a>フィールド

| フィールド       | 種類    | 拡張型 | 列挙型タイプ   | 説明 |
|-------------|---------|---------------|--------------------|-------------|
| ID          | Int     |               |                    |             |
| LogType     | 列挙    |               | SqlSyncLogType     |             |
| MessageType | 列挙    |               | SqlSyncMessageType |             |
| ParentID    | Int     |               |                    |             |
| RecId       | Int64   | RecId         |                    |             |
| recVersion  | 整数 | RecVersion    |                    |             |
| 順番    | Int     |               |                    |             |
| SyncTable   | 列挙    |               | ブール値            |             |
| TableName   | 文字列  |               |                    |             |
| テキスト        | 文字列  |               |                    |             |
| WarningOk   | 列挙    |               | ブール値            |             |

### <a name="indexes"></a>インデックス

| 指数     | 重複を許可します | フィールド |
|-----------|------------------|--------|
| TableName | 有              |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateReadUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、読み取り、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SqlSyncInfo テーブル](#sqlsyncinfo)

## <a name="subquery"></a>サブクエリ
Subquery テーブルは、職位に基づくページング機能によって使用されます。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|------------|---------|---------------|------------------|-------------|
| dataAreaId | 文字列  | DataAreaId    |                  |             |
| RecId      | Int64   | RecId         |                  |             |
| recVersion | 整数 | RecVersion    |                  |             |

### <a name="relations"></a>リレーション

| リレーション   | テーブル    |
|------------|----------|
| dataAreaId | DataArea |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| RecId | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [Sebquery テーブル](#subquery)

## <a name="sysactivetemptable"></a>SysActiveTempTable
SysActiveTempTable テーブルは、現在作成されている一時データベース テーブルに関するデータを提供します。 このテーブルは、これらのテーブルの存続期間を管理するためにフレームワークによって使用されます。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型    | 列挙型タイプ | 説明                                                                                                               |
|------------------|-------------|------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdDateTime  | UtcDateTime | CreatedDateTime  |                  |                                                                                                                           |
| dEL\_CreatedTime | 整数     | DEL\_CreatedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| InstanceId       | 文字列      | UtilElementName  |                  | アプリケーション要素の名前です。                                                                                          |
| RecId            | Int64       | RecId            |                  |                                                                                                                           |
| recVersion       | 整数     | RecVersion       |                  |                                                                                                                           |
| RelationTypeId   | Int64       | RecId            |                  | データベースのレコードの固有 ID                                                                                  |
| ServerId         | Int64       | RecId            |                  | データベースのレコードの固有 ID                                                                                  |
| SessionId        | Int64       | RecId            |                  | データベースのレコードの固有 ID                                                                                  |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| InstanceIdIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysActiveTempTable テーブル](#sysactivetemptable)

## <a name="sysbcproxyuseraccount"></a>SysBCProxyUserAccount
SysBCProxyUserAccount テーブルは、SysBcAliasForm セキュリティ フォームを通じて入力されているビジネス コネクタ プロキシ情報を格納します。 このテーブルには、常に 1 つのレコードが格納されます。

### <a name="fields"></a>フィールド

| フィールド         | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|---------------|---------|---------------|------------------|-------------|
| networkAlias  | 文字列  | NetworkAlias  |                  |             |
| networkDomain | 文字列  | NetworkDomain |                  |             |
| RecId         | Int64   | RecId         |                  |             |
| recVersion    | 整数 | RecVersion    |                  |             |
| sid           | 文字列  | Sid           |                  |             |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| RecID | 無               |        |
| Sid   | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysBCProxyUserAccount テーブル](#sysbcproxyuseraccount)

## <a name="sysbreakpointlist"></a>SysBreakpointList
SysBreakpointList テーブルには、MorphX にブレークポイントを持つ開発者の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型    | 列挙型タイプ | 説明                                                                                                               |
|------------------|-------------|------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdBy        | 文字列      | CreatedBy        |                  |                                                                                                                           |
| createdDateTime  | UtcDateTime | CreatedDateTime  |                  |                                                                                                                           |
| dEL\_CreatedTime | 整数     | DEL\_CreatedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| machineName      | 文字列      | NetworkDomain    |                  |                                                                                                                           |
|  Recid            | Int64       | RecId            |                  |                                                                                                                           |
| recVersion       | 整数     | RecVersion       |                  |                                                                                                                           |
| userId           | 文字列      | UserId           |                  | ユーザー ID                                                                                                           |
| のバージョン          | Int         |                  |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション | テーブル    |
|----------|----------|
| userId   | UserInfo |

### <a name="indexes"></a>インデックス

| 指数  | 重複を許可します | フィールド |
|--------|------------------|--------|
| RecId  | 無               |        |
| UserId | 有              |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysBreakpointList テーブル](#sysbreakpointlist)

## <a name="sysbreakpoints"></a>SysBreakpoints
SysBreakpoints テーブルには、MorphX にあるすべてのブレークポイントの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類      | 拡張型 | 列挙型タイプ | 説明                              |
|------------|-----------|---------------|------------------|------------------------------------------|
| codePath   | コンテナー |               |                  |                                          |
| lineNo     | Int       |               |                  |                                          |
| listRecId  | Int64     | RecId         |                  | データベースのレコードの固有 ID |
| RecId      | Int64     | RecId         |                  |                                          |
| recVersion | 整数   | RecVersion    |                  |                                          |
| ステータス     | Int       |               |                  |                                          |
| のバージョン    | Int       |               |                  |                                          |

### <a name="relations"></a>リレーション

| リレーション                  | テーブル             |
|---------------------------|-------------------|
| listRecId                 | SysBreakpointList |
| Relation\_SysBreakpoints1 | SysBreakpointList |

### <a name="indexes"></a>インデックス

| 指数     | 重複を許可します | フィールド |
|-----------|------------------|--------|
| ListRecId | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysBreakpoints テーブル](#sysbreakpoints)

## <a name="syscacheflush"></a>SysCacheFlush
SysCacheFlush テーブルには、複数の AOS サーバー間のキャッシュの同期に使用されるデータが含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型          | 列挙型タイプ | 説明                                     |
|------------------|-------------|------------------------|------------------|-------------------------------------------------|
| ClearData        | コンテナー   |                        |                  |                                                 |
| FlushData        | コンテナー   |                        |                  |                                                 |
| FlushVersion     | Int         |                        |                  |                                                 |
| modifiedDateTime | UtcDateTime | ModifiedDateTime       |                  |                                                 |
| RecId            | Int64       | RecId                  |                  |                                                 |
| recVersion       | 整数     | RecVersion             |                  |                                                 |
| スコープ            | 文字列      | GlobalObjectCacheScope |                  | グローバル オブジェクト キャッシュのインスタンスの名前です。 |

### <a name="indexes"></a>インデックス

| 指数         | 重複を許可します | フィールド |
|---------------|------------------|--------|
| CacheScopeIdx | 無               |        |
| RecIDIdx      | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysCacheFlush テーブル](#syscacheflush)

## <a name="sysclientaccesslog"></a>SysClientAccessLog
### <a name="fields"></a>フィールド

| フィールド           | 種類        | 拡張型   | 列挙型タイプ | 説明                                                                                                               |
|-----------------|-------------|-----------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| ClientComputer  | 文字列      | UserIdStr       |                  | 氏名                                                                                                                      |
| createdBy       | 文字列      | CreatedBy       |                  |                                                                                                                           |
| createdDateTime | UtcDateTime | CreatedDateTime |                  |                                                                                                                           |
| EventsContainer | コンテナー   |                 |                  |                                                                                                                           |
| パーティション       | Int64       | パーティション       |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid           | Int64       |  Recid           |                  |                                                                                                                           |
| recVersion      | 整数     | RecVersion      |                  |                                                                                                                           |
| SessionId       | Int         |                 |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション  | テーブル      |
|-----------|------------|
| パーティション | パーティション |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| CreatedByIdx | 有              |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysClientAccessLog テーブル](#sysclientaccesslog)

## <a name="sysclientsessions"></a>SysClientSessions
SysClientSessions には、システムで現在アクティブなクライアント セッションのデータが含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型       | 列挙型タイプ | 説明                                                                                                                             |
|------------------|-------------|---------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| clientComputer   | 文字列      | UserIdStr           |                  | 氏名                                                                                                                                    |
| clientType       | Int         |                     |                  |                                                                                                                                         |
| DataPartition    | 文字列      | PartitionKey        |                  | パーティション キー (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| DEL\_会社     | 文字列      |                     |                  |                                                                                                                                         |
| DEL\_ログイン\_時間 | Int         |                     |                  |                                                                                                                                         |
| helpLanguage     | 文字列      | InstalledLanguageId |                  |                                                                                                                                         |
| LoginDateTime    | UtcDateTime |                     |                  |                                                                                                                                         |
| RecId            | Int64       | RecId               |                  |                                                                                                                                         |
| recVersion       | 整数     | RecVersion          |                  |                                                                                                                                         |
| ServerId         | Int         |                     |                  |                                                                                                                                         |
| SessionId        | Int         |                     |                  |                                                                                                                                         |
| sessionType      | Int         |                     |                  |                                                                                                                                         |
| sid              | 文字列      | Sid                 |                  |                                                                                                                                         |
| ステータス           | Int         |                     |                  |                                                                                                                                         |
| userId           | 文字列      | UserId              |                  | ユーザー ID                                                                                                                         |
| userLanguage     | 文字列      | InstalledLanguageId |                  |                                                                                                                                         |
| バージョン          | Int         |                     |                  |                                                                                                                                         |

### <a name="relations"></a>リレーション

| リレーション                     | テーブル             |
|------------------------------|-------------------|
| DataPartition                | パーティション        |
| Relation\_SysClientSessions1 | SysServerSessions |
| Relation\_SysClientSessions2 | UserInfo          |
| ServerId                     | SysServerSessions |
| userId                       | UserInfo          |

### <a name="indexes"></a>インデックス

| 指数                      | 重複を許可します | フィールド |
|----------------------------|------------------|--------|
| ServerId                   | 有              |        |
| SessionId                  | 無               |        |
| ステータス                     | 有              | ステータス |
| Status\_ClientType\_UserId | 有              |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysClientSessions テーブル](#sysclientsessions)

## <a name="sysconfig"></a>SysConfig
SysConfig テーブルには、ライセンスおよびコンフィギュレーション情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| configType        | 列挙        |                   | ConfigType       |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| expiration        | 文字列      |                   |                  |                                                                                                                           |
| id                | Int         |                   |                  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| shadowValue       | 文字列      |                   |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| timestamp         | 文字列      |                   |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| userCount         | Int         |                   |                  |                                                                                                                           |
| 値             | 文字列      |                   |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数      | 重複を許可します | フィールド |
|------------|------------------|--------|
| ConfigType | 無               |        |
| RecId      | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysConfig テーブル](#sysconfig)

## <a name="sysencryptionkey"></a>SysEncryptionKey
SysEncryptionKey テーブルには、EP クエリ文字列を暗号化し、データ パラメーターを転記するために使用される暗号化キーが格納されます。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| キー               | コンテナー   |                   |                  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| RecID | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysEncryptionKey テーブル](#sysencryptionkey)

## <a name="sysglobalconfiguration"></a>SysGlobalConfiguration
SysGlobalConfiguration テーブルには、特定のコンポーネントを構成するために使用できるシステム レベル グローバル設定が保存されます。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|--------------|---------|---------------|------------------|-------------|
| 氏名         | 文字列  |               |                  |             |
| RecId        | Int64   | RecId         |                  |             |
| recVersion   | 整数 | RecVersion    |                  |             |
| ServerId     | 文字列  |               |                  |             |
| SettingLevel | Int     |               |                  |             |
| 先頭値        | 文字列  |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| NameIdx  | 無               |        |
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysGlobalConfiguration テーブル](#sysglobalconfiguration)

## <a name="sysinheritancerelations"></a>SysInheritanceRelations
テーブル継承の SysInheritanceRelations フレームワーク ヘルパー テーブル。 テーブルには、テーブル継承階層関連の情報が格納されます。

### <a name="fields"></a>フィールド

| フィールド          | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|----------------|---------|---------------|------------------|-------------|
| MainTableId    | Int     |               |                  |             |
| RecId          | Int64   | RecId         |                  |             |
| recVersion     | 整数 | RecVersion    |                  |             |
| RelatedTableId | Int     |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| 主要        | 無               |        |
| RelatedMain | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysInheritanceRelations テーブル](#sysinheritancerelations)

## <a name="syslastvalue"></a>SysLastValue
SysLastValue テーブルは、ユーザーがシステムを移動したときに記録される使用状況データの記憶域です。

### <a name="fields"></a>フィールド

| フィールド       | 種類      | 拡張型      | 列挙型タイプ | 説明                                                                                                               |
|-------------|-----------|--------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| 会社     | 文字列    | SelectableDataArea |                  | 選択可能な会社の ID                                                                                         |
| designName  | 文字列    | UtilElementName    |                  | アプリケーション要素の名前です。                                                                                          |
| elementName | 文字列    | UtilElementName    |                  | アプリケーション要素の名前です。                                                                                          |
| Is Kernel    | 列挙      |                    | ブール値          |                                                                                                                           |
| パーティション   | Int64     | パーティション          |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid       | Int64     |  Recid              |                  |                                                                                                                           |
| レコード タイプ  | 列挙      |                    | UtilElementType  |                                                                                                                           |
| recVersion  | 整数   | RecVersion         |                  |                                                                                                                           |
| userId      | 文字列    | UserId             |                  | ユーザー ID                                                                                                           |
| 値       | コンテナー |                    |                  |                                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション                | テーブル      |
|-------------------------|------------|
| isVirtual\_Extern       | DataArea   |
| パーティション               | パーティション |
| Relation\_SysLastValue1 | UserInfo   |
| Relation\_SysLastValue2 | DataArea   |
| userId                  | UserInfo   |

### <a name="indexes"></a>インデックス

| 指数      | 重複を許可します | フィールド |
|------------|------------------|--------|
| RecordType | 有              |        |
| UserId     | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysLastValue テーブル](#syslastvalue)

## <a name="sysmodel"></a>SysModel
SysModel テーブルには、システムにインストールされているモデルに関する情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型    | 列挙型タイプ | 説明          |
|------------------|-------------|------------------|------------------|----------------------|
| createdBy        | 文字列      | CreatedBy        |                  |                      |
| createdDateTime  | UtcDateTime | CreatedDateTime  |                  |                      |
| レイヤー            | Int64       | LayerRecid       |                  | レイヤーの ID です。 |
| modifiedBy       | 文字列      | ModifiedBy       |                  |                      |
| modifiedDateTime | UtcDateTime | ModifiedDateTime |                  |                      |
| RecId            | Int64       | RecId            |                  |                      |
| recVersion       | 整数     | RecVersion       |                  |                      |
| 行政単位 (区画)            | 文字列      |                  |                  |                      |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModel テーブル](#sysmodel)

## <a name="sysmodelelement"></a>SysModelElement
SysModelElement テーブルは、インストールが保持する ModelElements を一覧表示します。

### <a name="fields"></a>フィールド

| フィールド              | 種類    | 拡張型           | 列挙型タイプ | 説明                                                              |
|--------------------|---------|-------------------------|------------------|--------------------------------------------------------------------------|
| AxId               | 整数 | UtilElementId           |                  | アプリケーション オブジェクトの一意の内部識別番号です。         |
| ElementType        | Int64   | ModelElementType        |                  | ElementType の ID                                                 |
| 氏名               | 文字列  |                         |                  |                                                                          |
| 元金額             |         |                         |                  |                                                                          |
| ParentId           | 整数 | UtilElementParentId     |                  | 親アプリケーション オブジェクトの一意の内部識別番号 |
| ParentModelElement | Int64   | ParentModelElementRecid |                  | 親モデル要素の ID                                         |
| PartOfInheritance  | Int     |                         |                  |                                                                          |
| RecId              | Int64   | RecId                   |                  |                                                                          |
| recVersion         | 整数 | RecVersion              |                  |                                                                          |
| RootModelElement   | Int64   | RootModelElementRecid   |                  | ルート モデル要素の ID                                           |

### <a name="relations"></a>リレーション

| リレーション                      | テーブル               |
|-------------------------------|---------------------|
| ElementType                   | SysModelElementType |
| Relation\_SysModelElementType | SysModelElementType |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElement テーブル](#sysmodelelement)

## <a name="sysmodelelementdata"></a>SysModelElementData
SysModelElementData テーブルは、任意の SysModelElement のレイヤー固有のデータを提供します。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型     | 列挙型タイプ | 説明              |
|------------------|-------------|-------------------|------------------|--------------------------|
| createdBy        | 文字列      | CreatedBy         |                  |                          |
| createdDateTime  | UtcDateTime | CreatedDateTime   |                  |                          |
| レイヤー            | Int64       | LayerRecid        |                  | レイヤーの ID です。     |
| LegacyId         | Int         |                   |                  |                          |
| ModelElement     | Int64       | ModelElementRecid |                  | ModelElement の ID |
| ModelId          | 整数     | ModelId           |                  | モデルの ID です。     |
| modifiedBy       | 文字列      | ModifiedBy        |                  |                          |
| modifiedDateTime | UtcDateTime | ModifiedDateTime  |                  |                          |
| RecId            | Int64       | RecId             |                  |                          |
| recVersion       | 整数     | RecVersion        |                  |                          |
| SaveCount        | Int         |                   |                  |                          |

### <a name="relations"></a>リレーション

| リレーション                  | テーブル           |
|---------------------------|-----------------|
| レイヤー                     | SysModelLayer   |
| ModelElement              | SysModelElement |
| ModelId                   | SysModel        |
| Relation\_SysModel        | SysModel        |
| Relation\_SysModelElement | SysModelElement |
| Relation\_SysModelLayer   | SysModelLayer   |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementData テーブル](#sysmodelelementdata)

## <a name="sysmodelelementdataold"></a>SysModelElementDataOld
SysModelElementDataOld テーブルは、任意の SysModelElementOld のレイヤー固有のデータを提供します。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型     | 列挙型タイプ | 説明              |
|------------------|-------------|-------------------|------------------|--------------------------|
| createdBy        | 文字列      | CreatedBy         |                  |                          |
| createdDateTime  | UtcDateTime | CreatedDateTime   |                  |                          |
| レイヤー            | Int64       | LayerRecid        |                  | レイヤーの ID です。     |
| LegacyId         | Int         |                   |                  |                          |
| ModelElement     | Int64       | ModelElementRecid |                  | ModelElement の ID |
| ModelId          | 整数     | ModelId           |                  | モデルの ID です。     |
| modifiedBy       | 文字列      | ModifiedBy        |                  |                          |
| modifiedDateTime | UtcDateTime | ModifiedDateTime  |                  |                          |
| RecId            | Int64       | RecId             |                  |                          |
| recVersion       | 整数     | RecVersion        |                  |                          |
| SaveCount        | Int         |                   |                  |                          |

### <a name="relations"></a>リレーション

| リレーション                     | テーブル              |
|------------------------------|--------------------|
| レイヤー                        | SysModelLayerOld   |
| ModelElement                 | SysModelElementOld |
| ModelId                      | SysModelOld        |
| Relation\_SysModelElementOld | SysModelElementOld |
| Relation\_SysModelLayerOld   | SysModelLayerOld   |
| Relation\_SysModelOld        | SysModelOld        |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementDataOld テーブル](#sysmodelelementdataold)

## <a name="sysmodelelementlabel"></a>SysModelElementLabel
SysModelElementLabel テーブルには、特定の言語のラベル テキストが含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|------------|---------|---------------|------------------|-------------|
| コメント    | 文字列  |               |                  |             |
| ID         | Int     |               |                  |             |
| LabelId    | 文字列  |               |                  |             |
| 言語   | 文字列  |               |                  |             |
| モジュール     | 文字列  |               |                  |             |
| RecId      | Int64   | RecId         |                  |             |
| recVersion | 整数 | RecVersion    |                  |             |
| テキスト       | 文字列  |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数           | 重複を許可します | フィールド |
|-----------------|------------------|--------|
| ModuleLangIDIdx | 無               |        |
| RecIDIdx        | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementLabel テーブル](#sysmodelelementlabel)

## <a name="sysmodelelementlabelold"></a>SysModelElementLabelOld
SysModelElementLabelOld テーブルには、特定の言語のラベル テキストが含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|------------|---------|---------------|------------------|-------------|
| コメント    | 文字列  |               |                  |             |
| ID         | Int     |               |                  |             |
| LabelId    | 文字列  |               |                  |             |
| 言語   | 文字列  |               |                  |             |
| モジュール     | 文字列  |               |                  |             |
| RecId      | Int64   | RecId         |                  |             |
| recVersion | 整数 | RecVersion    |                  |             |
| テキスト       | 文字列  |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementLabelOld テーブル](#sysmodelelementlabelold)

## <a name="sysmodelelementold"></a>SysModelElementOld
SysModelElementOld テーブルは、インストールが保持する ModelElements を一覧表示します。

### <a name="fields"></a>フィールド

| フィールド              | 種類    | 拡張型           | 列挙型タイプ | 説明                                                              |
|--------------------|---------|-------------------------|------------------|--------------------------------------------------------------------------|
| AxId               | 整数 | UtilElementId           |                  | アプリケーション オブジェクトの一意の内部識別番号です。         |
| ElementType        | Int64   | ModelElementType        |                  | ElementType の ID                                                 |
| 氏名               | 文字列  |                         |                  |                                                                          |
| 元金額             |         |                         |                  |                                                                          |
| ParentId           | 整数 | UtilElementParentId     |                  | 親アプリケーション オブジェクトの一意の内部識別番号 |
| ParentModelElement | Int64   | ParentModelElementRecid |                  | 親モデル要素の ID                                         |
| PartOfInheritance  | Int     |                         |                  |                                                                          |
| RecId              | Int64   | RecId                   |                  |                                                                          |
| recVersion         | 整数 | RecVersion              |                  |                                                                          |
| RootModelElement   | Int64   | RootModelElementRecid   |                  | ルート モデル要素の ID                                           |

### <a name="relations"></a>リレーション

| リレーション                         | テーブル                  |
|----------------------------------|------------------------|
| ElementType                      | SysModelElementTypeOld |
| Relation\_SysModelElementTypeOld | SysModelElementTypeOld |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementOld テーブル](#sysmodelelementold)

## <a name="sysmodelelementsource"></a>SysModelElementSource
SysModelElementSource テーブルには、ソースを持つすべての SysModelElements のソース テキストが含まれています。

### <a name="fields"></a>フィールド

| フィールド        | 種類      | 拡張型     | 列挙型タイプ | 説明              |
|--------------|-----------|-------------------|------------------|--------------------------|
| レイヤー        | Int64     | LayerRecid        |                  | レイヤーの ID です。     |
| ModelElement | Int64     | ModelElementRecid |                  | ModelElement の ID |
| RecId        | Int64     | RecId             |                  |                          |
| recVersion   | 整数   | RecVersion        |                  |                          |
| 配賦元       | コンテナー |                   |                  |                          |

### <a name="relations"></a>リレーション

| リレーション                      | テーブル               |
|-------------------------------|---------------------|
| レイヤー                         | SysModelElementData |
| Relation\_SysModelElementData | SysModelElementData |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementSource テーブル](#sysmodelelementsource)

## <a name="sysmodelelementsourceold"></a>SysModelElementSourceOld
SysModelElementSourceOld テーブルには、ソースを持つすべての SysModelElementsOld のソース テキストが含まれています。

### <a name="fields"></a>フィールド

| フィールド        | 種類      | 拡張型     | 列挙型タイプ | 説明              |
|--------------|-----------|-------------------|------------------|--------------------------|
| レイヤー        | Int64     | LayerRecid        |                  | レイヤーの ID です。     |
| ModelElement | Int64     | ModelElementRecid |                  | ModelElement の ID |
| RecId        | Int64     | RecId             |                  |                          |
| recVersion   | 整数   | RecVersion        |                  |                          |
| 配賦元       | コンテナー |                   |                  |                          |

### <a name="relations"></a>リレーション

| リレーション                         | テーブル                  |
|----------------------------------|------------------------|
| レイヤー                            | SysModelElementDataOld |
| Relation\_SysModelElementDataOld | SysModelElementDataOld |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementSourceOld テーブル](#sysmodelelementsourceold)

## <a name="sysmodelelementtype"></a>SysModelElementType
SysModelElementType テーブルは、使用可能な SysModelElement 型を指定します。 その Recid は「古い」要素タイプの UtilRecordType 列挙の下位互換性です。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型        | 列挙型タイプ | 説明                   |
|--------------|---------|----------------------|------------------|-------------------------------|
| 氏名         | 文字列  | ModelElementTypeName |                  | 要素タイプの名前です。 |
| ParentType   | Int64   | ModelElementType     |                  | ElementType の ID      |
| RecId        | Int64   | RecId                |                  |                               |
| recVersion   | 整数 | RecVersion           |                  |                               |
| TreeNodeName | 文字列  |                      |                  |                               |

### <a name="relations"></a>リレーション

| リレーション | テーブル               |
|----------|---------------------|
| 氏名     | SysModelElementType |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| RecIDIdx    | 無               |        |
| TypeNameIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementType テーブル](#sysmodelelementtype)

## <a name="sysmodelelementtypeold"></a>SysModelElementTypeOld
SysModelElementTypeOld テーブルは、使用可能な SysModelElementOld 型を指定します。 その Recid は「古い」要素タイプの UtilRecordType 列挙の下位互換性です。

### <a name="fields"></a>フィールド

| フィールド        | 種類    | 拡張型        | 列挙型タイプ | 説明                   |
|--------------|---------|----------------------|------------------|-------------------------------|
| 氏名         | 文字列  | ModelElementTypeName |                  | 要素タイプの名前です。 |
| ParentType   | Int64   | ModelElementType     |                  | ElementType の ID      |
| RecId        | Int64   | RecId                |                  |                               |
| recVersion   | 整数 | RecVersion           |                  |                               |
| TreeNodeName | 文字列  |                      |                  |                               |

### <a name="relations"></a>リレーション

| リレーション | テーブル               |
|----------|---------------------|
| 氏名     | SysModelElementType |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelElementTypeOld テーブル](#sysmodelelementtypeold)

## <a name="sysmodellayer"></a>SysModelLayer
SysModelLayer テーブルは、考えられる LayerId と Name を一覧表示します。 レイヤーにモデル データが存在する場合は、そのレイヤーの集計バージョン番号を報告します。

### <a name="fields"></a>フィールド

| フィールド         | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|---------------|---------|---------------|------------------|-------------|
| IsDirty       | Int     |               |                  |             |
| レイヤー         | 列挙    |               | UtilEntryLevel   |             |
| RecId         | Int64   | RecId         |                  |             |
| recVersion    | 整数 | RecVersion    |                  |             |
| VersionNumber | Int     |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelLayer テーブル](#sysmodellayer)

## <a name="sysmodellayerold"></a>SysModelLayerOld
SysModelLayerOld テーブルは、考えられる LayerId と Name を一覧表示します。 レイヤーにモデル データが存在する場合は、そのレイヤーの集計バージョン番号を報告します。

### <a name="fields"></a>フィールド

| フィールド         | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|---------------|---------|---------------|------------------|-------------|
| レイヤー         | 列挙    |               | UtilEntryLevel   |             |
| RecId         | Int64   | RecId         |                  |             |
| recVersion    | 整数 | RecVersion    |                  |             |
| VersionNumber | Int     |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelLayerOld テーブル](#sysmodellayerold)

## <a name="sysmodelmanifest"></a>SysModelManifest
SysModelManifest テーブルには、説明、発行元、モデルのバージョンなど、配置されたモデルに関するマニフェスト情報が含まれます。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型              | 列挙型タイプ | 説明                               |
|-----------------|---------|----------------------------|------------------|-------------------------------------------|
| カテゴリ        | 整数 | ModelManifestCategoryRecId |                  | モデル カテゴリの ID              |
| 説明     | 文字列  | ModelDescription           |                  | モデルの説明です。             |
| DisplayName     | 文字列  | ModelDisplayName           |                  | モデルの表示名です。            |
| モデル           | Int64   | ModelRecid                 |                  | モデルの ID です。                      |
| 氏名            | 文字列  | ModelName                  |                  | モデル ストアのモデル名です。 |
| パブリッシャー       | 文字列  | ModelPublisher             |                  | モデルの発行元です。               |
| RecId           | Int64   | RecId                      |                  |                                           |
| recVersion      | 整数 | RecVersion                 |                  |                                           |
| 署名済          | Int     |                            |                  |                                           |
| VersionBuildNo  | Int     |                            |                  |                                           |
| VersionMajor    | Int     |                            |                  |                                           |
| VersionMinor    | Int     |                            |                  |                                           |
| VersionRevision | Int     |                            |                  |                                           |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="relations"></a>リレーション

| リレーション                           | テーブル                    |
|------------------------------------|--------------------------|
| カテゴリ                           | SysModelManifestCategory |
| モデル                              | SysModel                 |
| Relation\_SysModel                 | SysModel                 |
| Relation\_SysModelManifestCategory | SysModelManifestCategory |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| ModelNameIdx | 無               |        |
| RecIDIdx     | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelManifest テーブル](#sysmodelmanifest)

## <a name="sysmodelmanifestcategory"></a>SysModelManifestCategory
SysModelManifestCategory テーブルには、展開されたモデルのマニフェスト情報のカテゴリ面が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型             | 列挙型タイプ | 説明                     |
|------------|---------|---------------------------|------------------|---------------------------------|
| 氏名       | 文字列  | ModelManifestCategoryName |                  | モデル カテゴリの名前です。 |
| RecId      | Int64   | RecId                     |                  |                                 |
| recVersion | 整数 | RecVersion                |                  |                                 |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| NameIdx  | 無               |        |
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelManifestCategory テーブル](#sysmodelmanifestcategory)

## <a name="sysmodelmanifestcategoryold"></a>SysModelManifestCategoryOld
SysModelManifestCategoryOld テーブルには、展開されたモデルのマニフェスト情報のカテゴリ面が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型             | 列挙型タイプ | 説明                     |
|------------|---------|---------------------------|------------------|---------------------------------|
| 氏名       | 文字列  | ModelManifestCategoryName |                  | モデル カテゴリの名前です。 |
| RecId      | Int64   | RecId                     |                  |                                 |
| recVersion | 整数 | RecVersion                |                  |                                 |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelManifestCategoryOld テーブル](#sysmodelmanifestcategoryold)

## <a name="sysmodelmanifestold"></a>SysModelManifestOld
SysModelManifestOld テーブルには、説明、発行元、モデルのバージョンなど、配置されたモデルに関するマニフェスト情報が含まれます。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型              | 列挙型タイプ | 説明                               |
|-----------------|---------|----------------------------|------------------|-------------------------------------------|
| カテゴリ        | 整数 | ModelManifestCategoryRecId |                  | モデル カテゴリの ID              |
| 説明     | 文字列  | ModelDescription           |                  | モデルの説明です。             |
| DisplayName     | 文字列  | ModelDisplayName           |                  | モデルの表示名です。            |
| モデル           | Int64   | ModelRecidOld              |                  | 古いモデルの ID です。                |
| 氏名            | 文字列  | ModelName                  |                  | モデル ストアのモデル名です。 |
| パブリッシャー       | 文字列  | ModelPublisher             |                  | モデルの発行元です。               |
| RecId           | Int64   | RecId                      |                  |                                           |
| recVersion      | 整数 | RecVersion                 |                  |                                           |
| 署名済          | Int     |                            |                  |                                           |
| VersionBuildNo  | Int     |                            |                  |                                           |
| VersionMajor    | Int     |                            |                  |                                           |
| VersionMinor    | Int     |                            |                  |                                           |
| VersionRevision | Int     |                            |                  |                                           |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ        | フィールド |
|--------------------|--------|
| AutoIdentification |        |

### <a name="relations"></a>リレーション

| リレーション                              | テーブル                       |
|---------------------------------------|-----------------------------|
| カテゴリ                              | SysModelManifestCategoryOld |
| モデル                                 | SysModelOld                 |
| Relation\_SysModelManifestCategoryOld | SysModelManifestCategoryOld |
| Relation\_SysModelOld                 | SysModelOld                 |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| ModelNameIdx | 無               |        |
| RecIDIdx     | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelManifestOld テーブル](#sysmodelmanifestold)

## <a name="sysmodelold"></a>SysModelOld
SysModelOld テーブルには、システムにインストールされているモデルに関する情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類        | 拡張型    | 列挙型タイプ | 説明          |
|------------------|-------------|------------------|------------------|----------------------|
| createdBy        | 文字列      | CreatedBy        |                  |                      |
| createdDateTime  | UtcDateTime | CreatedDateTime  |                  |                      |
| レイヤー            | Int64       | LayerRecid       |                  | レイヤーの ID です。 |
| modifiedBy       | 文字列      | ModifiedBy       |                  |                      |
| modifiedDateTime | UtcDateTime | ModifiedDateTime |                  |                      |
| RecId            | Int64       | RecId            |                  |                      |
| recVersion       | 整数     | RecVersion       |                  |                      |
| 行政単位 (区画)            | 文字列      |                  |                  |                      |

### <a name="indexes"></a>インデックス

| 指数    | 重複を許可します | フィールド |
|----------|------------------|--------|
| RecIDIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysModelOld Table](#sysmodelold)

## <a name="sysoccconfiguration"></a>SysOccConfiguration
SysOccConfiguration テーブルは、グローバルな同時実行モデルの設定を保存し、競合例外ログイン ポリシーを更新します。

### <a name="fields"></a>フィールド

| フィールド                     | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|---------------------------|---------|---------------|------------------|-------------|
| AutoUpdateRecVersion      | 列挙    |               | ブール値          |             |
| GlobalOccMode             | 列挙    |               | GlobalOccMode    |             |
| LogHandledUpdateConflicts | 列挙    |               | ブール値          |             |
| RecId                     | Int64   | RecId         |                  |             |
| recVersion                | 整数 | RecVersion    |                  |             |
| UniqueIndex               | Int     |               |                  |             |
| UseReadUncommitedForAll   | 列挙    |               | ブール値          |             |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| UniqueIndex | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysOccConfiguration テーブル](#sysoccconfiguration)

## <a name="sysrecordlevelsecurity"></a>SysRecordLevelSecurity
SysRecordLevelSecurity テーブルには、システム管理者によって構成されているすべてのレコード レベルのセキュリティ制限が含まれています。 この制限は、企業ごと、グループごとに保持されます。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型      | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|--------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| \_未使用          | 列挙        |                    | ブール値          |                                                                                                                           |
| companyId         | 文字列      | SelectableDataArea |                  | 選択可能な会社の ID                                                                                         |
| createdBy         | 文字列      | CreatedBy          |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime    |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime   |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| DEL\_groupId      | 文字列      | UserGroupId        |                  | ユーザー グループの ID                                                                                                     |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| modifiedBy        | 文字列      | ModifiedBy         |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime   |                  |                                                                                                                           |
| パーティション         | Int64       | パーティション          |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid             | Int64       |  Recid              |                  |                                                                                                                           |
| recVersion        | 整数     | RecVersion         |                  |                                                                                                                           |
| 制限       | コンテナー   |                    |                  |                                                                                                                           |
| SecurityRole      | Int64       | RecId              |                  | セキュリティ ロールの名前です                                                                                                 |
| tabId             | 整数     | TableId            |                  | テーブル ID                                                                                                          |

### <a name="relations"></a>リレーション

| リレーション               | テーブル         |
|------------------------|---------------|
| companyId              | DataArea      |
| DEL\_groupId           | UserGroupInfo |
| パーティション              | パーティション    |
| Relation\_SecurityRole | SecurityRole  |
| SecurityRole           | SecurityRole  |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| RecId | 無               |        |
| 役割  | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysRecordLevelSecurity テーブル](#sysrecordlevelsecurity)

## <a name="sysserversessions"></a>SysServerSessions
SysServerSessions テーブルを使用して、システムにアクティブな AOS サーバーに関する情報を格納します。

### <a name="fields"></a>フィールド

| フィールド               | 種類        | 拡張型 | 列挙型タイプ | 説明 |
|---------------------|-------------|---------------|------------------|-------------|
| AOSAccount          | 文字列      |               |                  |             |
| AOSId               | 文字列      |               |                  |             |
| DEL\_LastUpdateTime | Int         |               |                  |             |
| DEL\_ログイン\_時間    | Int         |               |                  |             |
| Instance\_Name      | 文字列      |               |                  |             |
| LastUpdateDateTime  | UtcDateTime |               |                  |             |
| LoadBalance         | Int         |               |                  |             |
| LoginDateTime       | UtcDateTime |               |                  |             |
| RecId               | Int64       | RecId         |                  |             |
| recVersion          | 整数     | RecVersion    |                  |             |
| ServerId            | Int         |               |                  |             |
| ステータス              | Int         |               |                  |             |
| バージョン             | Int         |               |                  |             |
| ワークロード            | Int         |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| LoadBalance | 有              |        |
| ServerId    | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysServerSessions テーブル](#sysserversessions)

## <a name="syssetbasedhelper"></a>SysSetbasedHelper
テーブル継承セットに基づく操作の SysSetbasedHelper フレームワーク ヘルパー テーブル。

### <a name="fields"></a>フィールド

| フィールド          | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|----------------|---------|---------------|------------------|------------------------------------------|
| CandidateRecId | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| RecId          | Int64   | RecId         |                  |                                          |
| recVersion     | 整数 | RecVersion    |                  |                                          |

### <a name="indexes"></a>インデックス

| 指数             | 重複を許可します | フィールド |
|-------------------|------------------|--------|
| CandidateRecIDIdx | 無               |        |
| RecIDIdx          | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SysSetbasedHelper テーブル](#syssetbasedhelper)

## <a name="systemsequences"></a>SystemSequences
SystemSequences テーブルには、各テーブルの次に利用可能なレコード ID ブロックが保持されます。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明                              |
|------------|---------|---------------|------------------|------------------------------------------|
| cycle      | 列挙    |               | ブール値          |                                          |
| dataAreaId | 文字列  | DataAreaId    |                  |                                          |
| id         | Int     |               |                  |                                          |
| maxVal     | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| minVal     | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| 名前       | 文字列  |               |                  |                                          |
| nextVal    | Int64   | RecId         |                  | データベースのレコードの固有 ID |
| RecId      | Int64   | RecId         |                  |                                          |
| recVersion | 整数 | RecVersion    |                  |                                          |
| tabId      | 整数 | TableId       |                  | テーブル ID                         |

### <a name="relations"></a>リレーション

| リレーション   | テーブル    |
|------------|----------|
| dataAreaId | DataArea |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [SystemSequences テーブル](#systemsequences)

## <a name="tablecollectionlist"></a>TableCollectionList
TableCollectionList テーブルには、テーブル コレクションと仮想会社の間のマッピングが格納されます。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型   | 列挙型タイプ | 説明                                                                                                               |
|-----------------|---------|-----------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| パーティション       | Int64   | パーティション       |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid           | Int64   |  Recid           |                  |                                                                                                                           |
| recVersion      | 整数 | RecVersion      |                  |                                                                                                                           |
| tableCollection | 文字列  | UtilElementName |                  | アプリケーション要素の名前です。                                                                                          |
| virtualDataArea | 文字列  | VirtualDataArea |                  | 仮想会社の ID                                                                                                  |

### <a name="relations"></a>リレーション

| リレーション                  | テーブル        |
|---------------------------|--------------|
| isVirtual\_Extern         | DataArea     |
| parentId\_Extern          | UtilElements |
| パーティション                 | パーティション   |
| Relation\_CollectionList1 | UtilElements |
| Relation\_CollectionList2 | DataArea     |

### <a name="indexes"></a>インデックス

| 指数           | 重複を許可します | フィールド |
|-----------------|------------------|--------|
| VirtualDataArea | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [TableCollectionList テーブル](#tablecollectionlist)

## <a name="timezoneslist"></a>TimeZonesList
TimeZonesList テーブルには、サポートされているタイム ゾーンの一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|-----------------|---------|---------------|------------------|-------------|
| EnumName        | 文字列  |               |                  |             |
| EnumPosition    | Int     |               |                  |             |
| RecId           | Int64   | RecId         |                  |             |
| recVersion      | 整数 | RecVersion    |                  |             |
| TimeZoneKeyName | 文字列  |               |                  |             |
| TzEnum          | 列挙    |               | タイム ゾーン         |             |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| EnumPosition | 無               |        |
| TzEnum       | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [TimeZonesList テーブル](#timezoneslist)

## <a name="timezonesrulesdata"></a>TimeZonesRulesData
TimeZonesRulesData テーブルには、GMT オフセット、およびサポートされているすべてのタイム ゾーンの夏時間情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明 |
|------------|---------|---------------|------------------|-------------|
| バイアス       | Int     |               |                  |             |
| DBias      | Int     |               |                  |             |
| DDay       | Int     |               |                  |             |
| DDayOfWeek | Int     |               |                  |             |
| DHour      | Int     |               |                  |             |
| DMinute    | Int     |               |                  |             |
| DMonth     | Int     |               |                  |             |
| DSecond    | Int     |               |                  |             |
| DYear      | Int     |               |                  |             |
| RecId      | Int64   | RecId         |                  |             |
| recVersion | 整数 | RecVersion    |                  |             |
| RuleId     | Int     |               |                  |             |
| SBias      | Int     |               |                  |             |
| SDay       | Int     |               |                  |             |
| SDayOfWeek | Int     |               |                  |             |
| SHour      | Int     |               |                  |             |
| SMinute    | Int     |               |                  |             |
| SMonth     | Int     |               |                  |             |
| SSecond    | Int     |               |                  |             |
| SYear      | Int     |               |                  |             |
| TzEnum     | 列挙    |               | タイム ゾーン         |             |
| 年       | Int     |               |                  |             |

### <a name="relations"></a>リレーション

| リレーション                      | テーブル         |
|-------------------------------|---------------|
| Relation\_TimeZonesRulesData1 | TimeZonesList |
| TzEnum                        | TimeZonesList |

### <a name="indexes"></a>インデックス

| 指数  | 重複を許可します | フィールド |
|--------|------------------|--------|
| RuleId | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [TimeZonesRulesData テーブル](#timezonesrulesdata)

## <a name="userdataareafilter"></a>UserDataAreaFilter
UserDataAreaFilter テーブルには、ユーザーが選択できる会社の一覧が含まれています。 これは、SecurityRights クラスの populateSelectableCompanies メソッドを呼び出すことによって入力されます。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明                                                                                                               |
|------------|---------|---------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| DataArea   | 文字列  | DataAreaId    |                  | データ領域の ID                                                                                                    |
| パーティション  | Int64   | パーティション     |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid      | Int64   |  Recid         |                  |                                                                                                                           |
| recVersion | 整数 | RecVersion    |                  |                                                                                                                           |
| ユーザー       | 文字列  | UserId        |                  | ユーザー ID                                                                                                           |

### <a name="relations"></a>リレーション

| リレーション           | テーブル      |
|--------------------|------------|
| DataArea           | DataArea   |
| パーティション          | パーティション |
| Relation\_DataArea | DataArea   |
| Relation\_User     | UserInfo   |
| ユーザー               | UserInfo   |

### <a name="indexes"></a>インデックス

| 指数       | 重複を許可します | フィールド |
|-------------|------------------|--------|
| DataAreaIdx | 無               |        |
| RecIdIdx    | 無               |        |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UserDataAreaFilter テーブル](#userdataareafilter)

## <a name="userinfo"></a>UserInfo
UserInfo テーブルには、ユーザー、そのアクティブなディレクトリ、および既定の情報の一覧が含まれています。

### <a name="fields"></a>フィールド

| フィールド                     | 種類    | 拡張型       | 列挙型タイプ     | 説明                                                                                                               |
|---------------------------|---------|---------------------|----------------------|---------------------------------------------------------------------------------------------------------------------------|
| accountType               | 列挙    |                     | UserAccountType      |                                                                                                                           |
| autoInfo                  | Int     |                     |                      |                                                                                                                           |
| autoLogOff                | Int     |                     |                      |                                                                                                                           |
| autoUpdate                | Int     |                     |                      |                                                                                                                           |
| clientAccessLogLevel      | Int     |                     |                      |                                                                                                                           |
| 会社                   | 文字列  | SelectableDataArea  |                      | 選択可能な会社の ID                                                                                         |
| compilerWarningLevel      | 列挙    |                     | CompilerWarningLevel |                                                                                                                           |
| confirmDelete             | Int     |                     |                      |                                                                                                                           |
| confirmUpdate             | Int     |                     |                      |                                                                                                                           |
| credentialRecId           | int64   |                     |                      |                                                                                                                           |
| debuggerPopup             | Int     |                     |                      |                                                                                                                           |
| debugInfo                 | Int     |                     |                      |                                                                                                                           |
| defaultPartition          | 列挙    |                     | ブール値              | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| DEL\_\_unused1            | 文字列  |                     |                      |                                                                                                                           |
| DEL\_\_unused2            | 文字列  |                     |                      |                                                                                                                           |
| DEL\_defaultModelId       | Int     |                     |                      |                                                                                                                           |
| DEL\_osAccountName        | 文字列  |                     |                      |                                                                                                                           |
| DEL\_パスワード             | 文字列  |                     |                      |                                                                                                                           |
| DEL\_startupMenu          | 文字列  | UtilElementName     |                      | アプリケーション要素の名前です。                                                                                          |
| enable                    | 列挙    |                     | ブール値              |                                                                                                                           |
| enabledOnce               | 列挙    |                     | ブール値              |                                                                                                                           |
| externalId                | 文字列  |                     |                      |                                                                                                                           |
| externalIdType            | 列挙    |                     | ExternalIdType       |                                                                                                                           |
| externalUser              | 列挙    |                     | ブール値              |                                                                                                                           |
| filterByGridOnByDefault   | 列挙    |                     | ブール値              |                                                                                                                           |
| formFontName              | 文字列  |                     |                      |                                                                                                                           |
| formFontSize              | Int     |                     |                      |                                                                                                                           |
| garbagecollectlimit       | Int     |                     |                      |                                                                                                                           |
| generalInfo               | Int     |                     |                      |                                                                                                                           |
| globalExcelExportFilePath | 文字列  |                     |                      | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| globalExcelExportLocation | Int     |                     |                      |                                                                                                                           |
| globalExcelExportMode     | Int     |                     |                      |                                                                                                                           |
| globalFormOpenMode        | Int     |                     |                      |                                                                                                                           |
| globalListPageLinkMode    | Int     |                     |                      |                                                                                                                           |
| helplanguage              | 文字列  | InstalledLanguageId |                      |                                                                                                                           |
| historyLimit              | Int     |                     |                      |                                                                                                                           |
| homePageRefreshDuration   | Int     |                     |                      |                                                                                                                           |
| id                        | 文字列  | UserId              |                      | ユーザー ID                                                                                                           |
| IdentityProvider          | 文字列  | NetworkDomain       |                      |                                                                                                                           |
| infologLevel              | Int     |                     |                      |                                                                                                                           |
| issuerRecId               | int64   |                     |                      |                                                                                                                           |
| 言語                  | 文字列  | InstalledLanguageId |                      |                                                                                                                           |
| messageLimit              | Int     |                     |                      |                                                                                                                           |
| 名前                      | 文字列  | UserIdStr           |                      | 氏名                                                                                                                      |
| networkAlias              | 文字列  | NetworkAlias        |                      |                                                                                                                           |
| networkDomain             | 文字列  | NetworkDomain       |                      |                                                                                                                           |
| notifyTimeZoneMismatch    | 列挙    |                     | ブール値              |                                                                                                                           |
| パーティション                 | Int64   | パーティション           |                      | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| preferredCalendar         | 列挙    |                     | PreferredCalendar    |                                                                                                                           |
| PreferredLocale           | 文字列  | PreferredLocale     |                      |                                                                                                                           |
| preferredTimeZone         | 列挙    |                     | タイム ゾーン             |                                                                                                                           |
| propertyFontName          | 文字列  |                     |                      |                                                                                                                           |
| propertyFontSize          | Int     |                     |                      |                                                                                                                           |
| querytimeLimit            | Int     |                     |                      |                                                                                                                           |
| RecId                     | Int64   | RecId               |                      |                                                                                                                           |
| recVersion                | 整数 | RecVersion          |                      |                                                                                                                           |
| reportBottomMargin        | 文字列  |                     |                      |                                                                                                                           |
| reportFontName            | 文字列  |                     |                      |                                                                                                                           |
| reportFontSize            | Int     |                     |                      |                                                                                                                           |
| reportLeftMargin          | 文字列  |                     |                      |                                                                                                                           |
| reportRightMargin         | 文字列  |                     |                      |                                                                                                                           |
| reportTopMargin           | 文字列  |                     |                      |                                                                                                                           |
| showAOTLayer              | Int     |                     |                      |                                                                                                                           |
| showModelNameInAOT        | Int     |                     |                      |                                                                                                                           |
| showStatusLine            | Int     |                     |                      |                                                                                                                           |
| showToolbar               | Int     |                     |                      |                                                                                                                           |
| sid                       | 文字列  | Sid                 |                      |                                                                                                                           |
| startupProject            | 文字列  | UtilElementName     |                      | アプリケーション要素の名前です。                                                                                          |
| statuslineInfo            | Int     |                     |                      |                                                                                                                           |
| toolbarInfo               | Int     |                     |                      |                                                                                                                           |
| traceInfo                 | Int     |                     |                      |                                                                                                                           |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ | フィールド                                                     |
|-------------|------------------------------------------------------------|
| AutoLookup  | id, accountType, name, networkAlias, networkDomain, enable |
| AutoReport  |                                                            |

### <a name="relations"></a>リレーション

| リレーション           | テーブル      |
|--------------------|------------|
| id                 | UserInfo   |
| isVirtual\_Extern  | DataArea   |
| パーティション          | パーティション |
| Relation\_UserInfo | DataArea   |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| ID      | 無               |        |
| IdOnly  | 有              |        |
| Sid     | 有              |        |
| SidOnly | 有              |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UserInfo テーブル](#userinfo)

## <a name="userinfostartupmodel"></a>UserInfoStartupModel
UserInfoStartupModel テーブルには、各ユーザーの各レイヤーの優先スタートアップ モデルが保持されます。

### <a name="fields"></a>フィールド

| フィールド      | 種類    | 拡張型 | 列挙型タイプ | 説明                                                                                                               |
|------------|---------|---------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| レイヤー      | 列挙    |               | UtilEntryLevel   |                                                                                                                           |
| ModelId    | Int64   | ModelRecid    |                  | モデルの ID です。                                                                                                      |
| パーティション  | Int64   | パーティション     |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid      | Int64   |  Recid         |                  |                                                                                                                           |
| recVersion | 整数 | RecVersion    |                  |                                                                                                                           |
| UserId     | 文字列  | UserGroupId   |                  | ユーザー グループの ID                                                                                                     |

### <a name="relations"></a>リレーション

| リレーション                        | テーブル              |
|---------------------------------|--------------------|
| ModelId                         | SysModelManifest   |
| パーティション                       | パーティション         |
| Relation\_SysModelManifest      | SysModelManifest   |
| Relation\_UserInfo              | UserInfo           |
| Relation\_UserInfoStartupModel3 | DEL\_UserGroupInfo |
| UserId                          | UserInfo           |

### <a name="indexes"></a>インデックス

| 指数              | 重複を許可します | フィールド |
|--------------------|------------------|--------|
| RecIDIdx           | 無               |        |
| UserID\_Layer\_Idx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UserInfoStartupModel テーブル](#userinfostartupmodel)

## <a name="utilelements"></a>UtilElements
UtilElements テーブルには、AOT 内に表示されるアプリケーションが含まれています。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| baseVersion       | Int         |                   |                  |                                                                                                                           |
| コード              | コンテナー   |                   |                  |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| 名前              | 文字列      | UtilElementName   |                  | アプリケーション要素の名前です。                                                                                          |
| parentId          | Int         |                   |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| レコード タイプ        | 列挙        |                   | UtilElementType  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| saveCount         | Int         |                   |                  |                                                                                                                           |
| ソース            | コンテナー   |                   |                  |                                                                                                                           |
| utilLevel         | 列挙        |                   | UtilEntryLevel   |                                                                                                                           |
| のバージョン           | Int         |                   |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド                                |
|-------|------------------|---------------------------------------|
| 名前  | 無               | recordType, parentId, name, utilLevel |
| RecId | 無               |                                       |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UtilElements テーブル](#utilelements)

## <a name="utilelementsold"></a>UtilElementsOld
UtilElementsOld テーブルには、アプリケーション フォルダーに格納されているアプリケーション モデルが含まれています。 アップグレード プロセス中に使用されます。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| baseVersion       | Int         |                   |                  |                                                                                                                           |
| コード              | コンテナー   |                   |                  |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| 名前              | 文字列      | UtilElementName   |                  | アプリケーション要素の名前です。                                                                                          |
| parentId          | Int         |                   |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| レコード タイプ        | 列挙        |                   | UtilElementType  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| saveCount         | Int         |                   |                  |                                                                                                                           |
| ソース            | コンテナー   |                   |                  |                                                                                                                           |
| utilLevel         | 列挙        |                   | UtilEntryLevel   |                                                                                                                           |
| のバージョン           | Int         |                   |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド                                |
|-------|------------------|---------------------------------------|
| 名前  | 無               | recordType, parentId, name, utilLevel |
| RecId | 無               |                                       |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UtilElementsOld テーブル](#utilelementsold)

## <a name="utilidelements"></a>UtilIdElements
UtilIdElements テーブルには、AOT 内に表示されるアプリケーション モデルが含まれています。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| baseVersion       | Int         |                   |                  |                                                                                                                           |
| コード              | コンテナー   |                   |                  |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| id                | Int         |                   |                  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| 名前              | 文字列      | UtilElementName   |                  | アプリケーション要素の名前です。                                                                                          |
| parentId          | Int         |                   |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| レコード タイプ        | 列挙        |                   | UtilElementType  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| saveCount         | Int         |                   |                  |                                                                                                                           |
| utilLevel         | 列挙        |                   | UtilEntryLevel   |                                                                                                                           |
| のバージョン           | Int         |                   |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド                                |
|-------|------------------|---------------------------------------|
| ID    | 無               |                                       |
| 名前  | 無               | recordType, parentId, name, utilLevel |
| RecId | 無               |                                       |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UtilIdElements テーブル](#utilidelements)

## <a name="utilidelementsold"></a>UtilIdElementsOld
UtilIdElementsOld テーブルには、アプリケーション フォルダーに格納されているアプリケーション モデルが含まれています。 アップグレード プロセス中に使用されます。

### <a name="fields"></a>フィールド

| フィールド             | 種類        | 拡張型     | 列挙型タイプ | 説明                                                                                                               |
|-------------------|-------------|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| baseVersion       | Int         |                   |                  |                                                                                                                           |
| コード              | コンテナー   |                   |                  |                                                                                                                           |
| createdBy         | 文字列      | CreatedBy         |                  |                                                                                                                           |
| createdDateTime   | UtcDateTime | CreatedDateTime   |                  |                                                                                                                           |
| dEL\_CreatedTime  | 整数     | DEL\_CreatedTime  |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| dEL\_ModifiedTime | 整数     | DEL\_ModifiedTime |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
| id                | Int         |                   |                  |                                                                                                                           |
| modifiedBy        | 文字列      | ModifiedBy        |                  |                                                                                                                           |
| modifiedDateTime  | UtcDateTime | ModifiedDateTime  |                  |                                                                                                                           |
| 名前              | 文字列      | UtilElementName   |                  | アプリケーション要素の名前です。                                                                                          |
| parentId          | Int         |                   |                  |                                                                                                                           |
| RecId             | Int64       | RecId             |                  |                                                                                                                           |
| レコード タイプ        | 列挙        |                   | UtilElementType  |                                                                                                                           |
| recVersion        | 整数     | RecVersion        |                  |                                                                                                                           |
| saveCount         | Int         |                   |                  |                                                                                                                           |
| utilLevel         | 列挙        |                   | UtilEntryLevel   |                                                                                                                           |
| のバージョン           | Int         |                   |                  |                                                                                                                           |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド                                |
|-------|------------------|---------------------------------------|
| ID    | 無               |                                       |
| 名前  | 無               | recordType, parentId, name, utilLevel |
| RecId | 無               |                                       |

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UtilIdElementsOld テーブル](#utilidelementsold)

## <a name="utilmodels"></a>UtilModels
UtilModels テーブルには、システムにインストールされているモデルに関する情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド            | 種類    | 拡張型    | 列挙型タイプ | 説明                               |
|------------------|---------|------------------|------------------|-------------------------------------------|
| CategoryId       | Int     |                  |                  |                                           |
| 説明      | 文字列  | ModelDescription |                  | モデルの説明です。             |
| DisplayName      | 文字列  | ModelDisplayName |                  | モデルの表示名です。            |
| ID               | Int     |                  |                  |                                           |
| InstallMode      | Int     |                  |                  |                                           |
| レイヤー            | 列挙    |                  | UtilEntryLevel   |                                           |
| MarkedForRemoval | Int     |                  |                  |                                           |
| ModelGroupId     | Int     |                  |                  |                                           |
| 氏名             | 文字列  | ModelName        |                  | モデル ストアのモデル名です。 |
| パブリッシャー        | 文字列  | ModelPublisher   |                  | モデルの発行元です。               |
| RecId            | Int64   | RecId            |                  |                                           |
| recVersion       | 整数 | RecVersion       |                  |                                           |
| 署名済           | Int     |                  |                  |                                           |
| 行政単位 (区画)            | 文字列  |                  |                  |                                           |
| VersionBuildNo   | Int     |                  |                  |                                           |
| VersionMajor     | Int     |                  |                  |                                           |
| VersionMinor     | Int     |                  |                  |                                           |
| VersionRevision  | Int     |                  |                  |                                           |

### <a name="indexes"></a>インデックス

| 指数        | 重複を許可します | フィールド |
|--------------|------------------|--------|
| ModelIDIdx   | 無               |        |
| ModelNameIdx | 無               |        |
| RecIDIdx     | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [UtilModels テーブル](#utilmodels)

## <a name="virtualdataarealist"></a>VirtualDataAreaList
VirtualDataAreaList テーブルには、実際の会社と仮想会社の間のマッピングが格納されます。

### <a name="fields"></a>フィールド

| フィールド           | 種類    | 拡張型      | 列挙型タイプ | 説明                                                                                                               |
|-----------------|---------|--------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| id              | 文字列  | SelectableDataArea |                  | 選択可能な会社の ID                                                                                         |
| パーティション       | Int64   | パーティション          |                  | (このフィールドは次のバージョンにのみ適用されます: Microsoft Dynamics AX 2012 R3、Microsoft Dynamics AX 2012 R2 (SYS)) |
|  Recid           | Int64   |  Recid              |                  |                                                                                                                           |
| recVersion      | 整数 | RecVersion         |                  |                                                                                                                           |
| virtualDataArea | 文字列  | VirtualDataArea    |                  | 仮想会社の ID                                                                                                  |

### <a name="field-groups"></a>フィールド グループ

| フィールド グループ             | フィールド |
|-------------------------|--------|
| virtualDataAreaRelation |        |

### <a name="relations"></a>リレーション

| リレーション                | テーブル      |
|-------------------------|------------|
| isVirtual\_Extern       | DataArea   |
| パーティション               | パーティション |
| Relation\_DataAreaList1 | DataArea   |
| Relation\_DataAreaList2 | DataArea   |

### <a name="indexes"></a>インデックス

| 指数 | 重複を許可します | フィールド |
|-------|------------------|--------|
| ID    | 無               |        |
| RecId | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [VirtualDataAreaList テーブル](#virtualdataarealist)

## <a name="vsassembly"></a>VSAssembly
VSAssembly テーブルには、AOT 内で Visual Studio プロジェクト ノードの下に格納されているアセンブリの最後の配置を説明する同期情報が含まれています。

### <a name="fields"></a>フィールド

| フィールド       | 型        | 拡張型 | 列挙型タイプ | 説明 |
|-------------|-------------|---------------|------------------|-------------|
| DeployTo    | 列挙        |               | DeployTo         |             |
| 氏名        | 文字列      | AssemblyName  |                  |             |
| ProjectName | 文字列      | ProjectName   |                  |             |
| ProjectType | 文字列      | ProjectType   |                  |             |
| RecId       | Int64       | RecId         |                  |             |
| recVersion  | 整数     | RecVersion    |                  |             |
| ServerId    | Int         |               |                  |             |
| UpdatedDate | UtcDateTime |               |                  |             |

### <a name="indexes"></a>インデックス

| 指数   | 重複を許可します | フィールド |
|---------|------------------|--------|
| NameIdx | 無               |        |

### <a name="security-note"></a>セキュリティ メモ

このテーブルを使用すると、権限昇格攻撃またはサービス拒否攻撃につながるおそれがあります。 したがって、AOSAuthorization プロパティは CreateUpdateDelete の列挙値に設定されます。 Application Object Server は、現在のユーザーがそのテーブルで要求された操作を実行するためのアクセス許可を持っていることを確認することで、テーブルに対する作成、更新、および削除アクションをそれぞれ許可します。 操作を開始したユーザーが操作を実行する権限がない場合は、例外が発生します。

### <a name="inheritance-hierarchy"></a>継承階層

[xRecord クラス](/dotnet/api/dynamics.ax.application) [共通テーブル](#common) [VSAssembly テーブル](#vsassembly)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
