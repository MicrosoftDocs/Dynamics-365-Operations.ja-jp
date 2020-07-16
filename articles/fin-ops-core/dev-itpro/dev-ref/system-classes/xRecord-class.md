---
title: xRecord クラス
description: このトピックでは、xRecord クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6332b76279e6c0f29fa4e58d0b70eb46d33c8049
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502761"
---
# <a name="class-xrecord"></a>クラス xRecord

[!include [banner](../../includes/banner.md)]

```xpp
class xRecord extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                     | 説明                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| public boolean aosValidateDelete()                                                                                         | サーバー上で、指定されたレコードをテーブルから削除できることを検証します。                                                 |
| public boolean aosValidateInsert()                                                                                         | サーバー上で、指定されたレコードを挿入できることを検証します。                                                             |
| public boolean aosValidateRead()                                                                                           | サーバー上で、指定されたレコードを読み取れることを検証します。                                                                 |
| public boolean aosValidateUpdate()                                                                                         | サーバー上で、指定されたレコードを更新できることを検証します。                                                              |
| public container buf2con(\[boolean packOrigBuffer\])                                                                       | X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。                                                          |
| public boolean canSubmitToWorkflow(\[str workflowType\])                                                                   | ワークフローへの送信が可能かどうかを示します。                                                                          |
| public str caption()                                                                                                       | テーブルのキャプション プロパティを取得および設定します。                                                                                 |
| public boolean checkInvalidFieldAccess(\[boolean checkInvalidFieldAccess\])                                                | 無効なフィールド アクセスを取得および設定します。                                                                                            |
| public boolean checkRecord(\[boolean checkMandatoryFields\])                                                               | 必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。                                                   |
| public boolean checkRestrictedDeleteActions(\[boolean checkRestrictedDeleteActions\])                                      | レコードが削除されるかどうかを示すプロパティを取得および設定します。                                                     |
| public SelectableDataArea company(\[SelectableDataArea company\])                                                          | レコードの法人を示すプロパティを取得および設定します。                                                       |
| public Common con2buf(container container)                                                                                 | コンテナをテーブル バッファに展開します。                                                                                    |
| public ConcurrencyModel concurrencyModel(\[ConcurrencyModel concurrencyModel\])                                            | レコードの更新に使用する既定の同時実行モデルを取得および設定します。                                                          |
| public int context(\[int newValue\])                                                                                       | コンテキスト プロパティを取得および設定します。                                                                                            |
| public Common data(\[Common cursor\])                                                                                      | テーブルから行を取得します。                                                                                                |
| public FormObjectSet dataSource()                                                                                          | テーブルのデータ ソースを取得します。                                                                                        |
| public boolean disableCache(\[boolean newValue\])                                                                          | キャッシュが無効かどうかを示すプロパティを取得および設定します。                                                         |
| public boolean doValidateDelete()                                                                                          | レコードを削除できる検証するアクションを実行します。                                                                  |
| public boolean equal(Common cursor)                                                                                        | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                                           |
| public AccessRight fieldAccessRight(FieldName fieldName)                                                                   | フィールドのアクセス権を返します。                                                                                                |
| public AccessRight fieldBufferAccessRight(FieldName fieldName)                                                             | 現在のレコードのフィールド アクセス権を返します。                                                                         |
| public FieldState fieldState(FieldId fieldId, \[FieldState state\])                                                        | テーブル バッファーのフィールドの状態を設定するか返します。                                                                      |
| public container getAllowRedefault()                                                                                       | 既定値に再度設定することを許可されているフィールドの一覧を返します。                                                                     |
| public container getDefaultingDependencies()                                                                               | デフォルトの依存関係を保持するコンテナーを返します。                                                                      |
| public TableExtension getExtension()                                                                                       | テーブル拡張機能を返します。                                                                                                   |
| public AnyType getFieldValue(str fieldName, \[int arrayIndex\])                                                            | テーブル バッファから指定したフィールドの値を取得します。                                                                     |
| public str getInstanceRelationType()                                                                                       | InstanceRelationType ID に対応するテーブルの名前を返します。                                                        |
| public str getPhysicalTableName()                                                                                          | 物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。                       |
| public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)                                              | 指定されたフィールドから PresenceInfo 値を取得します。                                                                     |
| public str getSQLStatement()                                                                                               | レコードをデータベースから取得するために使用される SQL ステートメントを取得します。                                                       |
| public Common getTableInInstanceHierarchy(TableId tableId)                                                                 |                                                                                                                                |
| public TableType getTableType()                                                                                            | テーブルのタイプを示します。                                                                                               |
| public boolean hasRelatedTable(str relatedRoleName)                                                                        | 外部キー制約バッファがテーブルにリンクされているかどうかを示します。                                                    |
| public str helpField(FieldId fieldId)                                                                                      | 指定したフィールドのヘルプ テキストを含む文字列を取得します。                                                        |
| public FieldState inputStatus(\[FieldState inputStatus\])                                                                  | テーブル バッファーの現在の入力ステータスを設定するか返します。                                                                  |
| public boolean interactiveContext(\[boolean context\])                                                                     | テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。                                                           |
| public boolean isFieldDataRetrieved(str fieldName, \[int arrayIndex\])                                                     | 指定されたフィールドのデータが取得されたかどうかをチェックします。                                                                 |
| public boolean isFieldSet(FieldId fieldId)                                                                                 | フィールドがセットまたは既定状態かどうかをチェックします。                                                                           |
| public boolean isFormDataSource()                                                                                          | データ ソースがフォームであるかどうかを示します。                                                                                   |
| public boolean isNewRecord()                                                                                               | レコードがまだ保存されていない新しいレコードである場合は true を返します。                                                     |
| public boolean isPartOfUOWSaveChanges()                                                                                    |                                                                                                                                |
| public boolean isTempDb()                                                                                                  | テーブルのタイプが SQL TempDB であるかどうかを示します。                                                                         |
| public boolean isTmp()                                                                                                     | これが一時テーブルであるかどうかを示します。                                                                                   |
| public Common joinChild()                                                                                                  | 現在のレコードの結合子を検索します。                                                                                    |
| public Common joinParent()                                                                                                 | 現在のレコードの結合の親を検索します。                                                                                   |
| public boolean linkPhysicalTableInstance(\[Common record\])                                                                | レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。                                                 |
| public Common orig()                                                                                                       | 現在のレコードの元の値を取得します。                                                                           |
| public boolean overwriteSystemfields(\[boolean allowOverwrite\])                                                           | システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。                                            |
| public boolean queryTimedOut()                                                                                             | クエリが実行の時間制限を超過したかどうかを示します。                                                             |
| public int queryTimeout(\[int seconds\], \[boolean raiseException\])                                                       | クエリの実行に対する時間制限を示すプロパティを取得および設定します。                                         |
| public boolean readCommittedLock(\[boolean readCommittedLock\])                                                            |                                                                                                                                |
| public boolean readPast(\[boolean skipLockedRows\])                                                                        | レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。       |
| public boolean recordLevelSecurity(\[boolean newValue\])                                                                   | レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。                                         |
| public Common relatedTable(str name, \[Common buffer\])                                                                    | テーブル バッファのリンクに関連するバッファーを設定するか返します。                                                                |
| public Int64 RowCount()                                                                                                    | テーブル内の行数を取得します。                                                                                     |
| public boolean selectForUpdate(\[boolean lockRecordsExclusive\])                                                           | 読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。                             |
| public boolean selectLocked(\[boolean lockRecordsShared\])                                                                 | ロックされているレコードを選択するかどうかを示します。                                                                                    |
| public Common selectRefRecord(FieldId referenceFieldId)                                                                    | 参照されているフィールド ID によりレコードを選択します。                                                                                     |
| public boolean selectWithRepeatableRead(\[boolean useRepeatableRead\])                                                     | 反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。                                                  |
| public boolean setTempDB()                                                                                                 |                                                                                                                                |
| public boolean setTmp()                                                                                                    | データベースに保存されていない場合にテーブルを設定します。                                                                    |
| public boolean skipAosValidation(\[boolean newValue\])                                                                     | Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。 |
| public boolean skipDatabaseLog(\[boolean newValue\])                                                                       | データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipDataMethods(\[boolean newValue\])                                                                       | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipDeleteActions(\[boolean newValue\])                                                                     | テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。                                         |
| public boolean skipDeleteMethod(\[boolean newValue\])                                                                      | オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。                                               |
| public boolean skipEvents(\[boolean newValue\])                                                                            | xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。                  |
| public boolean skipPostLoad(\[boolean newValue\])                                                                          | テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。                  |
| public boolean skipTTSCheck(\[boolean newValue\])                                                                          | 更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。    |
| public boolean suppressWarnings(\[boolean newValue\])                                                                      | このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。                                       |
| public AccessRight tableAccessRight()                                                                                      | テーブルのアクセス権を返します。                                                                                                |
| public AccessRight tableBufferAccessRight()                                                                                | 現在のレコードのテーブル アクセス権を返します。                                                                         |
| public boolean takeOwnershipOfTempDBTable(boolean newValue)                                                                |                                                                                                                                |
| public str toolTipField(FieldId fieldId)                                                                                   | 指定されたフィールドの HelpText 値を取得します。                                                                          |
| public str toolTipRecord()                                                                                                 | 現在のレコードのツールヒント値を取得します。                                                                            |
| public int usageCount()                                                                                                    | オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。                           |
| public boolean useExistingTempDBTable(str physicalTempTableName)                                                           |                                                                                                                                |
| public boolean validateDelete()                                                                                            | 現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。                                      |
| public boolean validateField(FieldId fieldIdToCheck)                                                                       | 指定されたフィールドが有効かどうかを判定します。                                                                               |
| public boolean validateFieldValue(FieldName fieldName, \[int arrayIndex\])                                                 |                                                                                                                                |
| private container validateRelations(\[boolean onlyValidateCompositeRelations\], \[boolean onlyValidateModifiedRelations\]) |                                                                                                                                |
| public boolean validateWrite()                                                                                             | 現在のレコードが有効で、書き込み可能な状態かどうかを判別します。                                                        |
| public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)                        | カーソルで有効な時間状態更新モードを設定します。                                                                             |
| public CachedHow wasCached()                                                                                               | データの取得元となった場所を指定します。                                                                      |
| public str xml(\[int indent\])                                                                                             | 現在のオブジェクトを表す XML 文字列を取得します。                                                                    |
| public void doDelete()                                                                                                     | 現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。                 |
| public void update()                                                                                                       | 現在のレコードを更新します。                                                                                                    |
| public void merge(Common mergeInto)                                                                                        | 現在のテーブルを指定されたテーブルとマージします。                                                                             |
| public void clear()                                                                                                        | テーブル バッファーからすべての行を削除します。                                                                                        |
| public void setXDSContext(\[str contextString\])                                                                           | 新しい XDS コンテキストを設定します。                                                                                                          |
| public void renamePrimaryKey()                                                                                             | この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。         |
| public void dispose()                                                                                                      | XRecord オブジェクトによって使用されているリソースを解放します。                                                                        |
| public void setConnection(Connection connection)                                                                           | この表のユーザー接続を設定します。                                                                                       |
| public void delete()                                                                                                       | テーブルから現在のレコードを削除します。                                                                                     |
| public void defaultField(FieldId fieldId)                                                                                  | テーブルのフィールドの既定値を設定します。                                                                              |
| private void dbOpInTransaction(\[boolean isWriteOperation\])                                                               | 失敗した場合にデータベース操作が正しく閉じられていることを確認します。                                                         |
| public void write()                                                                                                        | レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。                                                                    |
| public void preRemoting()                                                                                                  | 他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。        |
| public void modifiedFieldValue(FieldName fieldName, \[int arrayIndex\])                                                    | 指定したフィールドを元の値に変更します。                                                                            |
| public void defaultRow()                                                                                                   | 非対話型の場合、テーブルのフィールドの既定値を設定します。                                                   |
| public void reread()                                                                                                       | テーブルからレコードを再読み取りします。                                                                                             |
| public void modifiedField(FieldId fieldId)                                                                                 | 指定したフィールドを元通りに変更します。                                                                                  |
| public void ttsabort()                                                                                                     | ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。                                                        |
| public void insert()                                                                                                       | テーブルにレコードを挿入します。                                                                                             |
| public void doClear()                                                                                                      | 現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。                     |
| public void initValue()                                                                                                    | フィールドを既定値に初期化します。                                                                                      |
| public void doUpdate()                                                                                                     | 現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。                                |
| public void ttsbegin()                                                                                                     | ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。                   |
| public void setCrossPartition(boolean newValue)                                                                            | テーブルのパーティション間分割を設定またはリセットします。                                                                               |
| public void setTmpData(Common cursor)                                                                                      | 一時的なテーブルの内容を指定されたデータに設定します。                                                                |
| public void ttscommit()                                                                                                    | ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。                                                       |
| public void setFieldValue(str fieldName, AnyType value, \[int arrayIndex\])                                                | レコード バッファーのフィールド値を設定します。                                                                                     |
| public void doInsert()                                                                                                     | テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。                         |
| public void setSQLTracing(\[boolean tracingmode\])                                                                         | SQL トレース モードを有効または無効にします。                                                                                          |
| public void postLoad()                                                                                                     | レコードが読み取られた後に実行されます。                                                                                            |

## <a name="method-aosvalidatedelete"></a>メソッド aosValidateDelete

サーバー上で、指定されたレコードをテーブルから削除できることを検証します。

```xpp
public boolean aosValidateDelete()
```

### <a name="return-value---aosvalidatedelete"></a>戻り値 - aosValidateDelete

レコードを削除することができる場合は true。それ以外の場合は、false。

## <a name="method-aosvalidateinsert"></a>メソッド aosValidateInsert

サーバー上で、指定されたレコードを挿入できることを検証します。

```xpp
public boolean aosValidateInsert()
```

### <a name="return-value---aosvalidateinsert"></a>戻り値 - aosValidateInsert

レコードを挿入することができる場合は true。それ以外の場合は、false。

## <a name="method-aosvalidateread"></a>メソッド aosValidateRead

サーバー上で、指定されたレコードを読み取れることを検証します。

```xpp
public boolean aosValidateRead()
```

### <a name="return-value---aosvalidateread"></a>戻り値 - aosValidateRead

レコードを読み取ることができる場合は true。それ以外の場合は、false。

## <a name="method-aosvalidateupdate"></a>メソッド aosValidateUpdate

サーバー上で、指定されたレコードを更新できることを検証します。

```xpp
public boolean aosValidateUpdate()
```

### <a name="return-value---aosvalidateupdate"></a>戻り値 - aosValidateUpdate

レコードを更新することができる場合は true。それ以外の場合は、false。

## <a name="method-buf2con"></a>メソッド buf2con

X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。

```xpp
public container buf2con([boolean packOrigBuffer])
```

### <a name="parameters---buf2con"></a>パラメーター - buf2con

packOrigBuffer  

### <a name="return-value---buf2con"></a>戻り値 - buf2con

梱包済みバッファーを保持するコンテナーです。

## <a name="method-cansubmittoworkflow"></a>メソッド canSubmitToWorkflow

ワークフローへの送信が可能かどうかを示します。

```xpp
public boolean canSubmitToWorkflow([str workflowType])
```

### <a name="parameters---cansubmittoworkflow"></a>パラメーター - canSubmitToWorkflow

workflowType  

### <a name="return-value---cansubmittoworkflow"></a>戻り値 - canSubmitToWorkflow

送信が可能な場合は true。それ以外の場合は false。

## <a name="method-caption"></a>メソッド caption

テーブルのキャプション プロパティを取得および設定します。

```xpp
public str caption()
```

### <a name="return-value---caption"></a>戻り値 - caption

テーブルのキャプション。

## <a name="method-checkinvalidfieldaccess"></a>メソッド checkInvalidFieldAccess

無効なフィールド アクセスを取得および設定します。

```xpp
public boolean checkInvalidFieldAccess([boolean checkInvalidFieldAccess])
```

### <a name="parameters---checkinvalidfieldaccess"></a>パラメーター - checkInvalidFieldAccess

checkInvalidFieldAccess  
設定する値 (オプション)。

### <a name="return-value---checkinvalidfieldaccess"></a>戻り値 - checkInvalidFieldAccess

無効なフィールド アクセス権が設定されている場合は true。それ以外の場合は、false。

## <a name="method-checkrecord"></a>メソッド checkRecord

必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean checkRecord([boolean checkMandatoryFields])
```

### <a name="parameters---checkrecord"></a>パラメーター - checkRecord

checkMandatoryFields  
必須フィールドをチェックするかどうかを示すブール値; オプション。

### <a name="return-value---checkrecord"></a>戻り値 - checkRecord

必須項目がオンになっている場合は true。それ以外の場合は、false。

## <a name="method-checkrestricteddeleteactions"></a>メソッド checkRestrictedDeleteActions

レコードが削除されるかどうかを示すプロパティを取得および設定します。

```xpp
public boolean checkRestrictedDeleteActions([boolean checkRestrictedDeleteActions])
```

### <a name="parameters---checkrestricteddeleteactions"></a>パラメーター - checkRestrictedDeleteActions

checkRestrictedDeleteActions  
レコードが削除できるかどうかを示すブール値; オプション。

### <a name="return-value---checkrestricteddeleteactions"></a>戻り値 - checkRestrictedDeleteActions

レコードを削除することができる場合は true。それ以外の場合は、false。

### <a name="remarks---checkrestricteddeleteactions"></a>備考 - checkRestrictedDeleteActions

プロパティはテーブルの削除アクションと、対応するレコードが対応するテーブルにあるときにテーブルが削除アクションを許可するかどうかに基づいています。

## <a name="method-company"></a>メソッド company

レコードの法人を示すプロパティを取得および設定します。

```xpp
public SelectableDataArea company([SelectableDataArea company])
```

### <a name="parameters---company"></a>パラメーター - company

会社  
レコードの新しい法人 (オプション)。

### <a name="return-value---company"></a>戻り値 - company

法人 ID。

## <a name="method-con2buf"></a>メソッド con2buf

コンテナをテーブル バッファに展開します。

```xpp
public Common con2buf(container container)
```

### <a name="parameters---con2buf"></a>パラメーター - con2buf

コンテナー  

### <a name="return-value---con2buf"></a>戻り値 - con2buf

## <a name="method-concurrencymodel"></a>メソッド concurrencyModel

レコードの更新に使用する既定の同時実行モデルを取得および設定します。

```xpp
public ConcurrencyModel concurrencyModel([ConcurrencyModel concurrencyModel])
```

### <a name="parameters---concurrencymodel"></a>パラメーター - concurrencyModel

concurrencyModel  
既定では、新しい同時実行モデル (オプション)。

### <a name="return-value---concurrencymodel"></a>戻り値 - concurrencyModel

既定値では、同時実行モデル プロパティの現在の値です。

## <a name="method-context"></a>メソッド context

コンテキスト プロパティを取得および設定します。

```xpp
public int context([int newValue])
```

### <a name="parameters---context"></a>パラメーター - context

newValue  
コンテキスト プロパティの新しい値 (オプション)。

### <a name="return-value---context"></a>戻り値 - context

コンテキスト プロパティの現在の値。

## <a name="method-data"></a>メソッド data

テーブルから行を取得します。

```xpp
public Common data([Common cursor])
```

### <a name="parameters---data"></a>パラメーター - data

cursor  
取得する行 (オプション)。

### <a name="return-value---data"></a>戻り値 - data

レコード バッファ。

### <a name="remarks---data"></a>備考 - data

1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。

## <a name="method-datasource"></a>メソッド dataSource

テーブルのデータ ソースを取得します。

```xpp
public FormObjectSet dataSource()
```

### <a name="return-value---datasource"></a>戻り値 - dataSource

テーブルのデータ ソース。

## <a name="method-disablecache"></a>メソッド disableCache

キャッシュが無効かどうかを示すプロパティを取得および設定します。

```xpp
public boolean disableCache([boolean newValue])
```

### <a name="parameters---disablecache"></a>パラメーター - disableCache

newValue  
キャッシュが無効かどうかを示すブール値。

### <a name="return-value---disablecache"></a>戻り値 - disableCache

無効なキャッシュ プロパティの新しい値。

## <a name="method-dovalidatedelete"></a>メソッド doValidateDelete

レコードを削除できる検証するアクションを実行します。

```xpp
public boolean doValidateDelete()
```

### <a name="return-value---dovalidatedelete"></a>戻り値 - doValidateDelete

## <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

```xpp
public boolean equal(Common cursor)
```

### <a name="parameters---equal"></a>パラメーター - equal

cursor  
等しいかどうかをチェックするオブジェクト。

### <a name="return-value---equal"></a>戻り値 - equal

オブジェクトが等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

このメソッドは上書きされます。 Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 派生クラスは、値の等価性をサポートするために Object::equal メソッドを上書きできます。

## <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

フィールドのアクセス権を返します。

```xpp
public AccessRight fieldAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldaccessright"></a>パラメーター - fieldAccessRight

fieldName  
フィールド アクセス権を取得するフィールドの名前。

### <a name="return-value---fieldaccessright"></a>戻り値 - fieldAccessRight

フィールドのフィールド アクセス権限。

## <a name="method-fieldbufferaccessright"></a>メソッド fieldBufferAccessRight

現在のレコードのフィールド アクセス権を返します。

```xpp
public AccessRight fieldBufferAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldbufferaccessright"></a>パラメーター - fieldBufferAccessRight

fieldName  
フィールド アクセス権を取得するフィールドの名前。

### <a name="return-value---fieldbufferaccessright"></a>戻り値 - fieldBufferAccessRight

フィールド アクセス権限。

## <a name="method-fieldstate"></a>メソッド fieldState

テーブル バッファーのフィールドの状態を設定するか返します。

```xpp
public FieldState fieldState(FieldId fieldId, [FieldState state])
```

### <a name="parameters---fieldstate"></a>パラメーター - fieldState

fieldId  

<!-- -->

状態  

### <a name="return-value---fieldstate"></a>戻り値 - fieldState

フィールドの古い状態。

## <a name="method-getallowredefault"></a>メソッド getAllowRedefault

既定値に再度設定することを許可されているフィールドの一覧を返します。

```xpp
public container getAllowRedefault()
```

### <a name="return-value---getallowredefault"></a>戻り値 - getAllowRedefault

フィールドを保持するコンテナー。

## <a name="method-getdefaultingdependencies"></a>メソッド getDefaultingDependencies

デフォルトの依存関係を保持するコンテナーを返します。

```xpp
public container getDefaultingDependencies()
```

### <a name="return-value---getdefaultingdependencies"></a>戻り値 - getDefaultingDependencies

デフォルトの依存関係を保持するコンテナー。

## <a name="method-getextension"></a>メソッド getExtension

テーブル拡張機能を返します。

```xpp
public TableExtension getExtension()
```

### <a name="return-value---getextension"></a>戻り値 - getExtension

テーブル拡張

## <a name="method-getfieldvalue"></a>メソッド getFieldValue

テーブル バッファから指定したフィールドの値を取得します。

```xpp
public AnyType getFieldValue(str fieldName, [int arrayIndex])
```

### <a name="parameters---getfieldvalue"></a>パラメーター - getFieldValue

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

### <a name="return-value---getfieldvalue"></a>戻り値 - getFieldValue

フィールドの値。

### <a name="remarks---getfieldvalue"></a>備考 - getFieldValue

arrayIndex パラメーターは、配列フィールドにのみ適用されます。 配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。 指定されたフィールドが不明な場合、このメソッドは ArgumentOutOfRange 例外をスローします。

## <a name="method-getinstancerelationtype"></a>メソッド getInstanceRelationType

InstanceRelationType ID に対応するテーブルの名前を返します。

```xpp
public str getInstanceRelationType()
```

### <a name="return-value---getinstancerelationtype"></a>戻り値 - getInstanceRelationType

InstanceRelationType ID に対応するテーブルの名前。

## <a name="method-getphysicaltablename"></a>メソッド getPhysicalTableName

物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。

```xpp
public str getPhysicalTableName()
```

### <a name="return-value---getphysicaltablename"></a>戻り値 - getPhysicalTableName

物理テーブル名またはテーブル インスタンス名。

## <a name="method-getpresencefielddata"></a>メソッド getPresenceFieldData

指定されたフィールドから PresenceInfo 値を取得します。

```xpp
public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)
```

### <a name="parameters---getpresencefielddata"></a>パラメーター - getPresenceFieldData

fieldId  

<!-- -->

fieldValue  

### <a name="return-value---getpresencefielddata"></a>戻り値 - getPresenceFieldData

## <a name="method-getsqlstatement"></a>メソッド getSQLStatement

レコードをデータベースから取得するために使用される SQL ステートメントを取得します。

```xpp
public str getSQLStatement()
```

### <a name="return-value---getsqlstatement"></a>戻り値 - getSQLStatement

SQL ステートメントを含む文字列。

## <a name="method-gettableininstancehierarchy"></a>メソッド getTableInInstanceHierarchy

```xpp
public Common getTableInInstanceHierarchy(TableId tableId)
```

### <a name="parameters---gettableininstancehierarchy"></a>パラメーター - getTableInInstanceHierarchy

tableId  

### <a name="return-value---gettableininstancehierarchy"></a>戻り値 - getTableInInstanceHierarchy

## <a name="method-gettabletype"></a>メソッド getTableType

テーブルのタイプを示します。

```xpp
public TableType getTableType()
```

### <a name="return-value---gettabletype"></a>戻り値 - getTableType

テーブルのタイプ (Regular、InMemory、TempDB)。

## <a name="method-hasrelatedtable"></a>メソッド hasRelatedTable

外部キー制約バッファがテーブルにリンクされているかどうかを示します。

```xpp
public boolean hasRelatedTable(str relatedRoleName)
```

### <a name="parameters---hasrelatedtable"></a>パラメーター - hasRelatedTable

relatedRoleName  

### <a name="return-value---hasrelatedtable"></a>戻り値 - hasRelatedTable

外部キー制約バッファがテーブルにリンクされている場合は true。それ以外の場合は、false。

## <a name="method-helpfield"></a>メソッド helpField

指定したフィールドのヘルプ テキストを含む文字列を取得します。

```xpp
public str helpField(FieldId fieldId)
```

### <a name="parameters---helpfield"></a>パラメーター - helpField

fieldId  
ヘルプ テキストを取得するフィールド。

### <a name="return-value---helpfield"></a>戻り値 - helpField

指定されたフィールドのヘルプ文字列。

## <a name="method-inputstatus"></a>メソッド inputStatus

テーブル バッファーの現在の入力ステータスを設定するか返します。

```xpp
public FieldState inputStatus([FieldState inputStatus])
```

### <a name="parameters---inputstatus"></a>パラメーター - inputStatus

inputStatus  

### <a name="return-value---inputstatus"></a>戻り値 - inputStatus

古い入力のステータス。

## <a name="method-interactivecontext"></a>メソッド interactiveContext

テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。

```xpp
public boolean interactiveContext([boolean context])
```

### <a name="parameters---interactivecontext"></a>パラメーター - interactiveContext

context  

### <a name="return-value---interactivecontext"></a>戻り値 - interactiveContext

テーブル バッファーの現在の対話型コンテキスト。

## <a name="method-isfielddataretrieved"></a>メソッド isFieldDataRetrieved

指定されたフィールドのデータが取得されたかどうかをチェックします。

```xpp
public boolean isFieldDataRetrieved(str fieldName, [int arrayIndex])
```

### <a name="parameters---isfielddataretrieved"></a>パラメーター - isFieldDataRetrieved

fieldName  

<!-- -->

arrayIndex  

### <a name="return-value---isfielddataretrieved"></a>戻り値 - isFieldDataRetrieved

データが取得済みの場合は true。それ以外の場合は、false。

## <a name="method-isfieldset"></a>メソッド isFieldSet

フィールドがセットまたは既定状態かどうかをチェックします。

```xpp
public boolean isFieldSet(FieldId fieldId)
```

### <a name="parameters---isfieldset"></a>パラメーター - isFieldSet

fieldId  

### <a name="return-value---isfieldset"></a>戻り値 - isFieldSet

フィールドがセット状態または既定状態の場合は true。それ以外の場合は、false。

## <a name="method-isformdatasource"></a>メソッド isFormDataSource

データ ソースがフォームであるかどうかを示します。

```xpp
public boolean isFormDataSource()
```

### <a name="return-value---isformdatasource"></a>戻り値 - isFormDataSource

データ ソースがフォームである場合は true。それ以外の場合は、false。

## <a name="method-isnewrecord"></a>メソッド isNewRecord

レコードがまだ保存されていない新しいレコードである場合は true を返します。

```xpp
public boolean isNewRecord()
```

### <a name="return-value---isnewrecord"></a>戻り値 - isNewRecord

レコードがまだ保存されていない新しいレコードである場合は true。それ以外の場合は、false。

## <a name="method-ispartofuowsavechanges"></a>メソッド isPartOfUOWSaveChanges

```xpp
public boolean isPartOfUOWSaveChanges()
```

### <a name="return-value---ispartofuowsavechanges"></a>戻り値 - isPartOfUOWSaveChanges

## <a name="method-istempdb"></a>メソッド isTempDb

テーブルのタイプが SQL TempDB であるかどうかを示します。

```xpp
public boolean isTempDb()
```

### <a name="return-value---istempdb"></a>戻り値 - isTempDb

テーブルのタイプが SQL TempDB である場合は true。それ以外の場合は false。

## <a name="method-istmp"></a>メソッド isTmp

これが一時テーブルであるかどうかを示します。

```xpp
public boolean isTmp()
```

### <a name="return-value---istmp"></a>戻り値 - isTmp

これが一時テーブルである場合は true。それ以外の場合は false。

## <a name="method-joinchild"></a>メソッド joinChild

現在のレコードの結合子を検索します。

```xpp
public Common joinChild()
```

### <a name="return-value---joinchild"></a>戻り値 - joinChild

現在のレコードの結合子。

## <a name="method-joinparent"></a>メソッド joinParent

現在のレコードの結合の親を検索します。

```xpp
public Common joinParent()
```

### <a name="return-value---joinparent"></a>戻り値 - joinParent

現在のレコードの結合の親。

## <a name="method-linkphysicaltableinstance"></a>メソッド linkPhysicalTableInstance

レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。

```xpp
public boolean linkPhysicalTableInstance([Common record])
```

### <a name="parameters---linkphysicaltableinstance"></a>パラメーター - linkPhysicalTableInstance

記録  

### <a name="return-value---linkphysicaltableinstance"></a>戻り値 - linkPhysicalTableInstance

リンク使用可能かどうかを示すブール値。

## <a name="method-orig"></a>メソッド orig

現在のレコードの元の値を取得します。

```xpp
public Common orig()
```

### <a name="return-value---orig"></a>戻り値 - orig

### <a name="remarks---orig"></a>備考 - orig

1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。

## <a name="method-overwritesystemfields"></a>メソッド overwriteSystemfields

システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。

```xpp
public boolean overwriteSystemfields([boolean allowOverwrite])
```

### <a name="parameters---overwritesystemfields"></a>パラメーター - overwriteSystemfields

allowOverwrite  
システム フィールドを上書きできるかどうかを示すブール値; オプション。

### <a name="return-value---overwritesystemfields"></a>戻り値 - overwriteSystemfields

システム フィールドを上書きすることができる場合は true。それ以外の場合は、false。

## <a name="method-querytimedout"></a>メソッド queryTimedOut

クエリが実行の時間制限を超過したかどうかを示します。

```xpp
public boolean queryTimedOut()
```

### <a name="return-value---querytimedout"></a>戻り値 - queryTimedOut

クエリが実行の時間制限を超過した場合は true。それ以外の場合は、false。

## <a name="method-querytimeout"></a>メソッド queryTimeout

クエリの実行に対する時間制限を示すプロパティを取得および設定します。

```xpp
public int queryTimeout([int seconds], [boolean raiseException])
```

### <a name="parameters---querytimeout"></a>パラメーター - queryTimeout

秒  

<!-- -->

raiseException  

### <a name="return-value---querytimeout"></a>戻り値 - queryTimeout

クエリ タイムアウト プロパティの現在の値。

## <a name="method-readcommittedlock"></a>メソッド readCommittedLock

```xpp
public boolean readCommittedLock([boolean readCommittedLock])
```

### <a name="parameters---readcommittedlock"></a>パラメーター - readCommittedLock

readCommittedLock  

### <a name="return-value---readcommittedlock"></a>戻り値 - readCommittedLock

## <a name="method-readpast"></a>メソッド readPast

レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean readPast([boolean skipLockedRows])
```

### <a name="parameters---readpast"></a>パラメーター - readPast

skipLockedRows  
ロックされている行をスキップするかどうかを示すブール値; オプション。

### <a name="return-value---readpast"></a>戻り値 - readPast

ロックされた行をスキップする必要がある場合は true。それ以外の場合は、false。

## <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。

```xpp
public boolean recordLevelSecurity([boolean newValue])
```

### <a name="parameters---recordlevelsecurity"></a>パラメーター - recordLevelSecurity

newValue  
レコード レベルのセキュリティを適用するかどうかを示すブール値; オプション。

### <a name="return-value---recordlevelsecurity"></a>戻り値 - recordLevelSecurity

セキュリティをレコード レベルで適用する必要がある場合は true。それ以外の場合は、false。

## <a name="method-relatedtable"></a>メソッド relatedTable

テーブル バッファのリンクに関連するバッファーを設定するか返します。

```xpp
public Common relatedTable(str name, [Common buffer])
```

### <a name="parameters---relatedtable"></a>パラメーター - relatedTable

名前  

<!-- -->

バッファ  

### <a name="return-value---relatedtable"></a>戻り値 - relatedTable

テーブル バッファのリンクに関連するバッファ。

## <a name="method-rowcount"></a>メソッド RowCount

テーブル内の行数を取得します。

```xpp
public Int64 RowCount()
```

### <a name="return-value---rowcount"></a>戻り値 - RowCount

テーブルの行数。

## <a name="method-selectforupdate"></a>メソッド selectForUpdate

読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。

```xpp
public boolean selectForUpdate([boolean lockRecordsExclusive])
```

### <a name="parameters---selectforupdate"></a>パラメーター - selectForUpdate

lockRecordsExclusive  
更新のためにレコードを読み込むかどうかを示すブール値; オプション。

### <a name="return-value---selectforupdate"></a>戻り値 - selectForUpdate

更新のためにレコードを読み取る必要がある場合は true。それ以外の場合は、false。

## <a name="method-selectlocked"></a>メソッド selectLocked

ロックされているレコードを選択するかどうかを示します。

```xpp
public boolean selectLocked([boolean lockRecordsShared])
```

### <a name="parameters---selectlocked"></a>パラメーター - selectLocked

lockRecordsShared  
ロックされているレコードを選択するかどうかを示すブール値。

### <a name="return-value---selectlocked"></a>戻り値 - selectLocked

ロックされたレコードを選択する必要がある場合は true。それ以外の場合は、false。

## <a name="method-selectrefrecord"></a>メソッド selectRefRecord

参照されているフィールド ID によりレコードを選択します。

```xpp
public Common selectRefRecord(FieldId referenceFieldId)
```

### <a name="parameters---selectrefrecord"></a>パラメーター - selectRefRecord

referenceFieldId  
参照フィールド ID。

### <a name="return-value---selectrefrecord"></a>戻り値 - selectRefRecord

レコード バッファ。

## <a name="method-selectwithrepeatableread"></a>メソッド selectWithRepeatableRead

反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。

```xpp
public boolean selectWithRepeatableRead([boolean useRepeatableRead])
```

### <a name="parameters---selectwithrepeatableread"></a>パラメーター - selectWithRepeatableRead

useRepeatableRead  
反復可能な読み取りが有効かどうかを示すブール値; オプション。

### <a name="return-value---selectwithrepeatableread"></a>戻り値 - selectWithRepeatableRead

反復可能な読み取りが有効な場合は true。それ以外の場合は、false。

## <a name="method-settempdb"></a>メソッド setTempDB

```xpp
public boolean setTempDB()
```

### <a name="return-value---settempdb"></a>戻り値 - setTempDB

## <a name="method-settmp"></a>メソッド setTmp

データベースに保存されていない場合にテーブルを設定します。

```xpp
public boolean setTmp()
```

### <a name="return-value---settmp"></a>戻り値 - setTmp

操作が成功した場合は true。それ以外の場合は、false。

## <a name="method-skipaosvalidation"></a>メソッド skipAosValidation

Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipAosValidation([boolean newValue])
```

### <a name="parameters---skipaosvalidation"></a>パラメーター - skipAosValidation

newValue  
AOS の検証をスキップするかどうかを示すブール値。

### <a name="return-value---skipaosvalidation"></a>戻り値 - skipAosValidation

AOS 検証をスキップする必要がある場合は true。それ以外の場合は false。

### <a name="remarks---skipaosvalidation"></a>備考 - skipAosValidation

攻撃者が skipAosValidation メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、SkipAOSValidationPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発ユーザー権を持っていることを確認します。

## <a name="method-skipdatabaselog"></a>メソッド skipDatabaseLog

データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipDatabaseLog([boolean newValue])
```

### <a name="parameters---skipdatabaselog"></a>パラメーター - skipDatabaseLog

newValue  
データベース ログ要求をスキップするかどうかを示すブール値; オプション。

### <a name="return-value---skipdatabaselog"></a>戻り値 - skipDatabaseLog

データベース ログ要求をスキップする必要がある場合は true。それ以外の場合は、false。

## <a name="method-skipdatamethods"></a>メソッド skipDataMethods

オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipDataMethods([boolean newValue])
```

### <a name="parameters---skipdatamethods"></a>パラメーター - skipDataMethods

newValue  
オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。

### <a name="return-value---skipdatamethods"></a>戻り値 - skipDataMethods

オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。

## <a name="method-skipdeleteactions"></a>メソッド skipDeleteActions

テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipDeleteActions([boolean newValue])
```

### <a name="parameters---skipdeleteactions"></a>パラメーター - skipDeleteActions

newValue  
レコードの削除要求を無視するかどうかを示すブール値; オプション。

### <a name="return-value---skipdeleteactions"></a>戻り値 - skipDeleteActions

レコードを削除する要求を無視する必要がある場合は true。それ以外の場合は、false。

### <a name="remarks---skipdeleteactions"></a>備考 - skipDeleteActions

このメソッドは、delete\_from ステートメントなど、セットベースの操作を使用している場合にのみ機能します。 xRecord.delete メソッドなどの行ベースの操作でそれを使用する場合、プロパティは重視されず、削除アクションは引き続き呼び出されます。

## <a name="method-skipdeletemethod"></a>メソッド skipDeleteMethod

オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipDeleteMethod([boolean newValue])
```

### <a name="parameters---skipdeletemethod"></a>パラメーター - skipDeleteMethod

newValue  
オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。

### <a name="return-value---skipdeletemethod"></a>戻り値 - skipDeleteMethod

オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。

## <a name="method-skipevents"></a>メソッド skipEvents

xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。

```xpp
public boolean skipEvents([boolean newValue])
```

### <a name="parameters---skipevents"></a>パラメーター - skipEvents

newValue  
イベントをスキップするかどうかを示すブール値; オプション。

### <a name="return-value---skipevents"></a>戻り値 - skipEvents

イベントがスキップされる場合は true。それ以外の場合は、false。

### <a name="remarks---skipevents"></a>備考 - skipEvents

このメソッドは、xRecord.skipDatabaseLog メソッドに似ています。 skipEvents メソッドは、カーネル内で生成するのに意味のないイベントをスキップするためにも内部的に使用されます。これは xRecord.skipDatabaseLog メソッドの現在の動作と一致しています。

-   Application.deleteCompany メソッド: 会社の削除操作の期間にイベント生成が無効になります。 これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。
-   SqlDataDictionary.tableDelete メソッド: テーブル削除時にイベント生成がオフになります。 これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。
-   カーネルで配列挿入機能を実装する RecordInsertList クラスは、開発者によって指定されたイベントを条件付きでスキップする新しいメソッドで、オプション引数 \_skipEvents = false を取得します。 イベントがスキップされない場合でも、カーネルは SQL を書き換えません。
-   主キーの名前を変更するとき、名前の変更操作が終了するまで、イベントの生成が停止されます。 これには、1 つのレコード内の主キーが含まれ、多くのレコードに外部キーを含まれることができます。 リネーム操作後、eventRenameKey メソッドが呼び出されます。

## <a name="method-skippostload"></a>メソッド skipPostLoad

テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipPostLoad([boolean newValue])
```

### <a name="parameters---skippostload"></a>パラメーター - skipPostLoad

newValue  
テーブルの postLoad メソッドの実行をスキップするかどうかを示すブール値; オプション。

### <a name="return-value---skippostload"></a>戻り値 - skipPostLoad

postLoad メソッドの実行をスキップする場合は true。それ以外の場合は、false。

## <a name="method-skipttscheck"></a>メソッド skipTTSCheck

更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean skipTTSCheck([boolean newValue])
```

### <a name="parameters---skipttscheck"></a>パラメーター - skipTTSCheck

newValue  
チェックをスキップするかどうかを示すブール値; オプション。

### <a name="return-value---skipttscheck"></a>戻り値 - skipTTSCheck

TTS チェックをスキップする必要がある場合は true。それ以外の場合は false。

## <a name="method-suppresswarnings"></a>メソッド suppressWarnings

このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。

```xpp
public boolean suppressWarnings([boolean newValue])
```

### <a name="parameters---suppresswarnings"></a>パラメーター - suppressWarnings

newValue  
このポインタの警告を非表示にするかどうかを示すブール値; オプション。

### <a name="return-value---suppresswarnings"></a>戻り値 - suppressWarnings

このポインターの警告を抑制する必要がある場合は true。それ以外の場合は、false。

## <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を返します。

```xpp
public AccessRight tableAccessRight()
```

### <a name="return-value---tableaccessright"></a>戻り値 - tableAccessRight

テーブル アクセス権の値。

## <a name="method-tablebufferaccessright"></a>メソッド tableBufferAccessRight

現在のレコードのテーブル アクセス権を返します。

```xpp
public AccessRight tableBufferAccessRight()
```

### <a name="return-value---tablebufferaccessright"></a>戻り値 - tableBufferAccessRight

現在のレコードのテーブル アクセス権。

## <a name="method-takeownershipoftempdbtable"></a>メソッド takeOwnershipOfTempDBTable

```xpp
public boolean takeOwnershipOfTempDBTable(boolean newValue)
```

### <a name="parameters---takeownershipoftempdbtable"></a>パラメーター - takeOwnershipOfTempDBTable

newValue  

### <a name="return-value---takeownershipoftempdbtable"></a>戻り値 - takeOwnershipOfTempDBTable

## <a name="method-tooltipfield"></a>メソッド toolTipField

指定されたフィールドの HelpText 値を取得します。

```xpp
public str toolTipField(FieldId fieldId)
```

### <a name="parameters---tooltipfield"></a>パラメーター - toolTipField

fieldId  
HelpText の値を取得するフィールド。

### <a name="return-value---tooltipfield"></a>戻り値 - toolTipField

指定されたフィールドの HelpText 値。

## <a name="method-tooltiprecord"></a>メソッド toolTipRecord

現在のレコードのツールヒント値を取得します。

```xpp
public str toolTipRecord()
```

### <a name="return-value---tooltiprecord"></a>戻り値 - toolTipRecord

現在のレコードのツールヒント値。

## <a name="method-usagecount"></a>メソッド usageCount

オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。

```xpp
public int usageCount()
```

### <a name="return-value---usagecount"></a>戻り値 - usageCount

オブジェクトが持つ参照の現在の数。

### <a name="remarks---usagecount"></a>備考 - usageCount

このメソッドは上書きされます。 オブジェクトが作成されると、その参照カウンターが 1 になります。 新しい参照が作成されると、その値が増加します。 スコープ外の参照は、値が減少します。

## <a name="method-useexistingtempdbtable"></a>メソッド useExistingTempDBTable

```xpp
public boolean useExistingTempDBTable(str physicalTempTableName)
```

### <a name="parameters---useexistingtempdbtable"></a>パラメーター - useExistingTempDBTable

physicalTempTableName  

### <a name="return-value---useexistingtempdbtable"></a>戻り値 - useExistingTempDBTable

## <a name="method-validatedelete"></a>メソッド validateDelete

現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a>戻り値 - validateDelete

現在のレコードを削除することができる場合は true。それ以外の場合は、false。

## <a name="method-validatefield"></a>メソッド validateField

指定されたフィールドが有効かどうかを判定します。

```xpp
public boolean validateField(FieldId fieldIdToCheck)
```

### <a name="parameters---validatefield"></a>パラメーター - validateField

fieldIdToCheck  
検証対象のフィールドのフィールド ID です。

### <a name="return-value---validatefield"></a>戻り値 - validateField

指定したフィールドが有効である場合は true。それ以外の場合は false。

## <a name="method-validatefieldvalue"></a>メソッド validateFieldValue

```xpp
public boolean validateFieldValue(FieldName fieldName, [int arrayIndex])
```

### <a name="parameters---validatefieldvalue"></a>パラメーター - validateFieldValue

fieldName  

<!-- -->

arrayIndex  

### <a name="return-value---validatefieldvalue"></a>戻り値 - validateFieldValue

## <a name="method-validaterelations"></a>メソッド validateRelations

```xpp
private container validateRelations([boolean onlyValidateCompositeRelations], [boolean onlyValidateModifiedRelations])
```

### <a name="parameters---validaterelations"></a>パラメーター - validateRelations

onlyValidateCompositeRelations  

<!-- -->

onlyValidateModifiedRelations  

### <a name="return-value---validaterelations"></a>戻り値 - validateRelations

## <a name="method-validatewrite"></a>メソッド validateWrite

現在のレコードが有効で、書き込み可能な状態かどうかを判別します。

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a>戻り値 - validateWrite

現在のレコードを記述することができる場合は true。それ以外の場合は、false。

## <a name="method-validtimestateupdatemode"></a>メソッド validTimeStateUpdateMode

カーソルで有効な時間状態更新モードを設定します。

```xpp
public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)
```

### <a name="parameters---validtimestateupdatemode"></a>パラメーター - validTimeStateUpdateMode

validTimeStateUpdateMode  

### <a name="return-value---validtimestateupdatemode"></a>戻り値 - validTimeStateUpdateMode

有効時間状態の更新モードの古い値。

## <a name="method-wascached"></a>メソッド wasCached

データの取得元となった場所を指定します。

```xpp
public CachedHow wasCached()
```

### <a name="return-value---wascached"></a>戻り値 - wasCached

データが取得された場所を示す CachedHow 列挙値。

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を取得します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
XML 文字列のインデントに使用するスペースの数を示す整数。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-dodelete"></a>メソッド doDelete

現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。

```xpp
public void doDelete()
```

## <a name="method-update"></a>メソッド update

現在のレコードを更新します。

```xpp
public void update()
```

## <a name="method-merge"></a>メソッド merge

現在のテーブルを指定されたテーブルとマージします。

```xpp
public void merge(Common mergeInto)
```

### <a name="parameters---merge"></a>パラメーター - merge

mergeInto  
マージするテーブル。

## <a name="method-clear"></a>メソッド clear

テーブル バッファーからすべての行を削除します。

```xpp
public void clear()
```

## <a name="method-setxdscontext"></a>メソッド setXDSContext

新しい XDS コンテキストを設定します。

```xpp
public void setXDSContext([str contextString])
```

### <a name="parameters---setxdscontext"></a>パラメーター - setXDSContext

contextString  

## <a name="method-renameprimarykey"></a>メソッド renamePrimaryKey

この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。

```xpp
public void renamePrimaryKey()
```

## <a name="method-dispose"></a>メソッド dispose

XRecord オブジェクトによって使用されているリソースを解放します。

```xpp
public void dispose()
```

## <a name="method-setconnection"></a>メソッド setConnection

この表のユーザー接続を設定します。

```xpp
public void setConnection(Connection connection)
```

### <a name="parameters---setconnection"></a>パラメーター - setConnection

connection  

## <a name="method-delete"></a>メソッド delete

テーブルから現在のレコードを削除します。

```xpp
public void delete()
```

## <a name="method-defaultfield"></a>メソッド defaultField

テーブルのフィールドの既定値を設定します。

```xpp
public void defaultField(FieldId fieldId)
```

### <a name="parameters---defaultfield"></a>パラメーター - defaultField

fieldId  

## <a name="method-dbopintransaction"></a>メソッド dbOpInTransaction

失敗した場合にデータベース操作が正しく閉じられていることを確認します。

```xpp
private void dbOpInTransaction([boolean isWriteOperation])
```

### <a name="parameters---dbopintransaction"></a>パラメーター - dbOpInTransaction

isWriteOperation  
操作が書き込み操作かどうかを示すブール値; オプション。

## <a name="method-write"></a>メソッド write

レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。

```xpp
public void write()
```

## <a name="method-preremoting"></a>メソッド preRemoting

他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。

```xpp
public void preRemoting()
```

## <a name="method-modifiedfieldvalue"></a>メソッド modifiedFieldValue

指定したフィールドを元の値に変更します。

```xpp
public void modifiedFieldValue(FieldName fieldName, [int arrayIndex])
```

### <a name="parameters---modifiedfieldvalue"></a>パラメーター - modifiedFieldValue

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

## <a name="method-defaultrow"></a>メソッド defaultRow

非対話型の場合、テーブルのフィールドの既定値を設定します。

```xpp
public void defaultRow()
```

## <a name="method-reread"></a>メソッド reread

テーブルからレコードを再読み取りします。

```xpp
public void reread()
```

## <a name="method-modifiedfield"></a>メソッド modifiedField

指定したフィールドを元通りに変更します。

```xpp
public void modifiedField(FieldId fieldId)
```

### <a name="parameters---modifiedfield"></a>パラメーター - modifiedField

fieldId  
変更対象のフィールド ID。

## <a name="method-ttsabort"></a>メソッド ttsabort

ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。

```xpp
public void ttsabort()
```

## <a name="method-insert"></a>メソッド insert

テーブルにレコードを挿入します。

```xpp
public void insert()
```

## <a name="method-doclear"></a>メソッド doClear

現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。

```xpp
public void doClear()
```

## <a name="method-initvalue"></a>メソッド initValue

フィールドを既定値に初期化します。

```xpp
public void initValue()
```

## <a name="method-doupdate"></a>メソッド doUpdate

現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。

```xpp
public void doUpdate()
```

## <a name="method-ttsbegin"></a>メソッド ttsbegin

ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。

```xpp
public void ttsbegin()
```

## <a name="method-setcrosspartition"></a>メソッド setCrossPartition

テーブルのパーティション間分割を設定またはリセットします。

```xpp
public void setCrossPartition(boolean newValue)
```

### <a name="parameters---setcrosspartition"></a>パラメーター - setCrossPartition

newValue  
クロス パーティションをセットまたはリセットする新しいブール値。

## <a name="method-settmpdata"></a>メソッド setTmpData

一時的なテーブルの内容を指定されたデータに設定します。

```xpp
public void setTmpData(Common cursor)
```

### <a name="parameters---settmpdata"></a>パラメーター - setTmpData

cursor  
一時テーブルの新しいデータ。

## <a name="method-ttscommit"></a>メソッド ttscommit

ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。

```xpp
public void ttscommit()
```

## <a name="method-setfieldvalue"></a>メソッド setFieldValue

レコード バッファーのフィールド値を設定します。

```xpp
public void setFieldValue(str fieldName, AnyType value, [int arrayIndex])
```

### <a name="parameters---setfieldvalue"></a>パラメーター - setFieldValue

fieldName  
フィールドの配列インデックス (省略可能)。

<!-- -->

値  
フィールドの配列インデックス (省略可能)。

<!-- -->

arrayIndex  
フィールドの配列インデックス (省略可能)。

### <a name="remarks---setfieldvalue"></a>備考 - setFieldValue

arrayIndex パラメーターは、配列フィールドにのみ適用されます。 配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。 このメソッドは、指定されたフィールドが不明な場合は ArgumentOutOfRange 例外をスローし、値パラメーターが指定されたフィールドと互換性がない場合は TypeMismatch 例外をスローします。

## <a name="method-doinsert"></a>メソッド doInsert

テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。

```xpp
public void doInsert()
```

## <a name="method-setsqltracing"></a>メソッド setSQLTracing

SQL トレース モードを有効または無効にします。

```xpp
public void setSQLTracing([boolean tracingmode])
```

### <a name="parameters---setsqltracing"></a>パラメーター - setSQLTracing

tracingmode  

## <a name="method-postload"></a>メソッド postLoad

レコードが読み取られた後に実行されます。

```xpp
public void postLoad()
```

