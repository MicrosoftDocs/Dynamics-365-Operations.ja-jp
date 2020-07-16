---
title: DictTable クラス
description: このトピックでは、DictTable クラスについて説明します。
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
ms.openlocfilehash: ea1491b083d21dd2b41970e049f0b2c11d0df063
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502982"
---
# <a name="class-dicttable"></a>クラス DictTable

[!include [banner](../../includes/banner.md)]

```xpp
class DictTable extends Object
```

DictTable クラスは、テーブルに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

次の例は、DictTable クラスのインスタンスを作成して、テーブル内のデータが会社ごとに格納されているかどうかを判断する方法を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? 
                      "per company" : "global")); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                                      | 説明                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean doesMethodExist(str name)                                                                                                    | 指定されたメソッドがテーブルに存在するかどうかをチェックします。                                                                                                                        |
| public AOSAuthorization AOSAuthSetting()                                                                                                    | ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。 |
| public RecordCacheLevel cacheLookup()                                                                                                       | テーブルのレコード キャッシュ レベルを返します。                                                                                                                             |
| public int cacheSize()                                                                                                                      | テーブルのキャッシュ サイズをレコードの数で返します。                                                                                                           |
| public AnyType callObject(str methodName, Common Called, VarArg )                                                                           | テーブルの指定されたオブジェクトのメソッドを呼び出します。                                                                                                                            |
| public AnyType callStatic(str methodName, VarArg )                                                                                          | テーブルの指定された静的メソッドを呼び出します。                                                                                                                            |
| public IndexId clusterIndex(\[boolean asDefinedInAOT\])                                                                                     | テーブルのクラスター化されたインデックスの ID を返します。                                                                                                                      |
| public ConfigurationKeyId configurationKeyId()                                                                                              | テーブルのコンフィギュレーション キーの ID を返します。                                                                                                                    |
| public boolean dataPerPartition()                                                                                                           | テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。        |
| public boolean dataPrCompany()                                                                                                              | テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。            |
| public int deleteActionCnt()                                                                                                                | テーブルの削除アクションの数を取得します。                                                                                                                     |
| public str deleteActionRelation(int cnt)                                                                                                    |                                                                                                                                                                           |
| public TableId deleteActionTableId(int cnt)                                                                                                 | インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。                                                                                            |
| public int deleteActionType(int cnt)                                                                                                        | テーブルの削除アクションの種類を取得します。                                                                                                                        |
| public str developerDocumentation()                                                                                                         |                                                                                                                                                                           |
| public str developerDocumentationLabelId()                                                                                                  |                                                                                                                                                                           |
| public boolean enabled()                                                                                                                    | テーブルが有効かどうかを示す値を返します。                                                                                                              |
| public boolean enforceRelationRules()                                                                                                       |                                                                                                                                                                           |
| public EntityRelationshipType entityRelationshipType()                                                                                      |                                                                                                                                                                           |
| public List extendedBy(\[boolean allLevels\])                                                                                               |                                                                                                                                                                           |
| public TableId extends()                                                                                                                    | 基本テーブルのテーブル ID を返します。                                                                                                                                     |
| public int fieldCnt(\[TableScope tableScope\])                                                                                              | テーブルのフィールドの数を返します。                                                                                                                                 |
| public FieldId fieldCnt2Id(int cnt, \[TableScope tableScope\])                                                                              | インデックスで指定されるフィールドのフィールド ID を返します。                                                                                                          |
| public str fieldGroup(int FieldGroupNumber, \[TableScope tableScope\])                                                                      | インデックスで指定されるフィールド グループの名前を返します。                                                                                                             |
| public int fieldGroupCnt(\[TableScope tableScope\])                                                                                         | テーブルのフィールド グループの数を返します。                                                                                                                         |
| public str fieldName(FieldId fieldId, \[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\]) | フィールド ID で指定されるフィールドの名前を返します。                                                                                                              |
| public FieldId fieldName2Id(str name)                                                                                                       | 名前で指定されるフィールドのフィールド ID を返します。                                                                                                                |
| public FieldId fieldNext(FieldId fieldId, \[TableScope tableScope\])                                                                        | テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。                                                                                             |
| public DictField fieldObject(FieldId fieldId)                                                                                               | フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。                                                                                   |
| public IndexId fieldOrigin2Id(Guid fieldOrigin, \[TableScope tableScope\])                                                                  |                                                                                                                                                                           |
| public str fieldSqlDefault(FieldId fieldId)                                                                                                 | フィールド ID で指定されているフィールドの SQL 既定値を返します。                                                                                                |
| public str formRef(\[boolean searchBaseTables\])                                                                                            | テーブルの既定のフォームの名前を返します。                                                                                                                       |
| public container getCountryRegionCodes()                                                                                                    |                                                                                                                                                                           |
| public FieldId getCountryRegionContextField()                                                                                               |                                                                                                                                                                           |
| public FieldId getValidTimeStateValidFromFieldId()                                                                                          |                                                                                                                                                                           |
| public FieldId getValidTimeStateValidToFieldId()                                                                                            |                                                                                                                                                                           |
| public boolean hasRecidIdx()                                                                                                                | テーブルのレコード ID インデックスが有効かどうかを示す値を返します。                                                                                      |
| public boolean hasSurrogateKey()                                                                                                            |                                                                                                                                                                           |
| public TableId id()                                                                                                                         | テーブルの ID を返します。                                                                                                                                              |
| public int indexCnt()                                                                                                                       | テーブルのインデックスの数を返します。                                                                                                                              |
| public IndexId indexCnt2Id(int cnt)                                                                                                         |                                                                                                                                                                           |
| public str indexName(IndexId indexId, \[DbBackend db\])                                                                                     | indexId パラメーターで指定された形式のインデックスの名前を返します。                                                                                                  |
| public IndexId indexName2Id(str name)                                                                                                       | 名前で指定されているインデックスの ID を返します。                                                                                                                     |
| public IndexId indexNext(IndexId id)                                                                                                        | テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。                                                                                            |
| public DictIndex indexObject(IndexId indexId)                                                                                               | ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。                                                                                         |
| public IndexId indexUnique()                                                                                                                | テーブルの一意のインデックスの ID を返します。                                                                                                                         |
| public FieldId instanceRelationType()                                                                                                       |                                                                                                                                                                           |
| public boolean isAbstract()                                                                                                                 | このテーブルが抽象かどうかを示します。                                                                                                                                 |
| public boolean isBaseData()                                                                                                                 | テーブル コンテンツが基本データであるかどうかを示します。                                                                                                                         |
| public boolean isDefaultData()                                                                                                              | テーブルが既定のデータを含むかどうかを示します。                                                                                                                        |
| public boolean isDerivedFrom(TableName baseTableName)                                                                                       | 1 つのテーブル タイプが別から派生しているかどうかを示します。                                                                                                                    |
| public boolean isMap()                                                                                                                      | テーブルがマップであるかどうかを示します。                                                                                                                                     |
| public boolean isSql()                                                                                                                      | テーブルが SQL テーブルであるかどうかを示します。                                                                                                                              |
| public boolean isSystemTable()                                                                                                              | テーブルがシステム テーブルであるかどうかを示します。                                                                                                                            |
| public boolean isTempDb()                                                                                                                   |                                                                                                                                                                           |
| public boolean isTmp()                                                                                                                      | テーブルが一時テーブルであるかどうかを示します。                                                                                                                         |
| public boolean isUnionAllView()                                                                                                             |                                                                                                                                                                           |
| public boolean isValidTimeStateTable()                                                                                                      |                                                                                                                                                                           |
| public boolean isView()                                                                                                                     | テーブルがビューであるかどうかを示します。                                                                                                                                    |
| public str label()                                                                                                                          | テーブルのラベル テキストを返します。                                                                                                                                     |
| public str labelDefined()                                                                                                                   | テーブルの label プロパティの値を返します。                                                                                                                    |
| public str listPageRef(\[boolean searchBaseTables\])                                                                                        |                                                                                                                                                                           |
| public Common makeRecord()                                                                                                                  | テーブルの空白のレコードを作成します。                                                                                                                                     |
| public AccessType maxAccessMode()                                                                                                           | AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。                                                                                           |
| public str name(\[DbBackend db\], \[boolean pseudoname\])                                                                                   | テーブル名を取得します。                                                                                                                                          |
| public str objectMethod(int methodNumber, \[TableScope tableScope\])                                                                        | インデックスで指定されるインスタンス メソッドの名前を返します。                                                                                                        |
| public int objectMethodCnt(\[TableScope tableScope\])                                                                                       | テーブルのインスタンス メソッドの数を返します。                                                                                                                     |
| public DictMethod objectMethodObject(int methodNumber, \[TableScope tableScope\])                                                           | インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。                                                                              |
| public DictTableMap mapObject(int methodNumber)                                                                                             | インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。                                                                            |
| public int mapCnt()                                                                                                                         | この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。                                                                   |
| public boolean occEnabled()                                                                                                                 | テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。                                                                                           |
| public IndexId primaryIndex(\[boolean asDefinedInAOT\])                                                                                     | テーブルのプライマリ インデックスの ID を返します。                                                                                                                        |
| public FieldId primaryKeyField()                                                                                                            | テーブルの主キーに使用されているフィールドの ID を返します。                                                                                                |
| public str relation(int RelationNumber, \[TableScope tableScope\])                                                                          | インデックスで指定される関係の名前を返します。                                                                                                                |
| public int relationCnt(\[TableScope tableScope\])                                                                                           | テーブルの関係の数を返します。                                                                                                                            |
| public IndexId replacementKey()                                                                                                             |                                                                                                                                                                           |
| public str reportRef()                                                                                                                      | テーブルの既定のレポートの名前を返します。                                                                                                                     |
| public AccessType rights(\[boolean ignoreContext\])                                                                                         | テーブルに指定されている、現在のユーザーのアクセス権を返します。                                                                                            |
| public SecurityKeyId securityKeyId()                                                                                                        | テーブルのセキュリティ キーの ID を返します。                                                                                                                         |
| public str singularLabel(\[boolean labelTranslation\])                                                                                      |                                                                                                                                                                           |
| public str staticMethod(int methodNumber)                                                                                                   | インデックスで指定される静的メソッドの名前を返します。                                                                                                           |
| public int staticMethodCnt()                                                                                                                | テーブルの静的メソッドの数を返します。                                                                                                                       |
| public DictMethod staticMethodObject(int methodNumber)                                                                                      | インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。                                                                               |
| public boolean supportInheritance()                                                                                                         |                                                                                                                                                                           |
| public TableGroup tableGroup()                                                                                                              | テーブルのテーブル グループを返します。                                                                                                                                      |
| public TableType tableType()                                                                                                                | テーブルのタイプを示します。                                                                                                                                          |
| public FieldId titleField1(\[boolean includeBaseTables\], \[boolean extendedFieldId\])                                                      | テーブルの titleField1 プロパティを表すフィールドの ID を返します。                                                                                        |
| public FieldId titleField2(\[boolean includeBaseTables\], \[boolean extendedFieldId\])                                                      | テーブルの titleField2 プロパティを表すフィールドの ID を返します。                                                                                        |
| public boolean validRelationship()                                                                                                          |                                                                                                                                                                           |
| public boolean visible()                                                                                                                    | テーブルが表示できるかどうかを判定します。                                                                                                                                  |
| ::public static DictTable construct(str tableName)                                                                                          |                                                                                                                                                                           |
| ::public static RecId getRelationTypeFromTableName(TableName tableName)                                                                     |                                                                                                                                                                           |
| ::public static TableName getTableNameFromRelationType(RecId relationType)                                                                  |                                                                                                                                                                           |
| ::public static Common createRecord(str tableName)                                                                                          |                                                                                                                                                                           |
| public void reloadSecurity()                                                                                                                | テーブルの機能キー システムを再読み込みします。                                                                                                                             |
| public void new(TableId tableId)                                                                                                            | Object クラスの新しいインスタンスを初期化します。                                                                                                                           |
| public void reindex()                                                                                                                       | テーブルのインデックスの再作成を実行します。                                                                                                                                          |

## <a name="method-doesmethodexist"></a>メソッド doesMethodExist

指定されたメソッドがテーブルに存在するかどうかをチェックします。

```xpp
public boolean doesMethodExist(str name)
```

### <a name="parameters---doesmethodexist"></a>パラメーター - doesMethodExist

名前  

### <a name="return-value---doesmethodexist"></a>戻り値 - doesMethodExist

指定メソッドがテーブル上に存在する場合は true。それ以外の場合は、false。

### <a name="remarks---doesmethodexist"></a>備考 - doesMethodExist

この API は、メソッドが正常にコンパイルされているかどうかを確認せずに、メソッドがテーブルに存在するかどうかを確認するために推奨される方法です。

## <a name="method-aosauthsetting"></a>メソッド AOSAuthSetting

ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。

```xpp
public AOSAuthorization AOSAuthSetting()
```

### <a name="return-value---aosauthsetting"></a>戻り値 - AOSAuthSetting

AOSAuthorization システム列挙値です。

### <a name="remarks---aosauthsetting"></a>備考 - AOSAuthSetting

AOSAuthorization::None 値は、承認チェックが実行されないことを示します。 テーブルの AOSAuthorization プロパティを設定するには、テーブルのプロパティを使用します。 アプリケーション オブジェクト ツリー (AOT) で、テーブルを右クリックしてからプロパティをクリックしてテーブルのプロパティにアクセスします。

### <a name="examples---aosauthsetting"></a>例 - AOSAuthSetting

次の例は、AOSAuthSetting メソッドの呼び出しを示しています。

```xpp
static public void Main(Args _args) 
{ 
    DictTable dt; 
    AOSAuthorization a; 
    dt = new DictTable(tablenum(CustTable)); 
    a = dt.AOSAuthSetting(); 
}
```

## <a name="method-cachelookup"></a>メソッド cacheLookup

テーブルのレコード キャッシュ レベルを返します。

```xpp
public RecordCacheLevel cacheLookup()
```

### <a name="return-value---cachelookup"></a>戻り値 - cacheLookup

テーブルのレコード キャッシュ レベルを示す RecordCacheLevel 値。

### <a name="examples---cachelookup"></a>例 - cacheLookup

次の例は、テーブルのキャッシュ レベルの取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print dt.cacheLookup(); 
}
```

## <a name="method-cachesize"></a>メソッド cacheSize

テーブルのキャッシュ サイズをレコードの数で返します。

```xpp
public int cacheSize()
```

### <a name="return-value---cachesize"></a>戻り値 - cacheSize

テーブルのキャッシュ サイズです。

### <a name="examples---cachesize"></a>例 - cacheSize

次の例では、テーブルのキャッシュ サイズを取得します。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     print strfmt("Cache size: %1", dt.cacheSize()); 
}
```

## <a name="method-callobject"></a>メソッド callObject

テーブルの指定されたオブジェクトのメソッドを呼び出します。

```xpp
public AnyType callObject(str methodName, Common Called, VarArg )
```

### <a name="parameters---callobject"></a>パラメータ - callObject

methodName  

<!-- -->

呼び出された  

<!-- -->


### <a name="return-value---callobject"></a>戻り値 - callObject

methodName パラメーターへの呼び出しの結果。

### <a name="remarks---callobject"></a>備考 - callObject

攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---callobject"></a>例 - callObject

この例では、SysUserLog テーブルの SysUserLog.onlineTime 静的メソッドを呼び出し、呼び出しから返された値を出力します。

```xpp
{ 
    Dicttable         dictTable; 
    int               onlineTime; 
    Common            common; 
    str               resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    dictTable= new DictTable(tablenum(SysUserLog)); 
    if (dictTable != null) 
    { 
        common = dictTable.makeRecord(); 
        // Grants permission to execute the 
        // DictTable.callObject method. DictTable.callObject runs 
        // under code access security. 
        perm.assert(); 
        onlineTime   = dictTable.callObject("onlineTime", common); 
        resultOutput = strfmt("User online time is %1", onlineTime); 
        print resultOutput; 
        pause; 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-callstatic"></a>メソッド callStatic

テーブルの指定された静的メソッドを呼び出します。

```xpp
public AnyType callStatic(str methodName, VarArg )
```

### <a name="parameters---callstatic"></a>パラメーター - callStatic

methodName  

<!-- -->


### <a name="return-value---callstatic"></a>戻り値 - callStatic

methodName パラメーターへの呼び出しの結果。

### <a name="remarks---callstatic"></a>備考 - callStatic

攻撃者がこの機能への入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、callStatic メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---callstatic"></a>例 - callStatic

この例では、SysUserInfo テーブル内の SysUserInfo:find static method メソッドを呼び出し、呼び出しから返された値を callStatic メソッドに出力します。

```xpp
 { 
    Dicttable   dictTable; 
    SysUserInfo userInfo; 
    str         resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictTable.callStatic method. 
    // DictTable.callStatic runs under code access security. 
    perm.assert(); 
    dictTable= new DictTable(tablenum(SysUserInfo)); 
    if (dictTable != null) 
    { 
        userInfo     = dictTable.callStatic("find"); 
        resultOutput = strfmt("Current user ID is %1", userInfo.Id); 
        print resultOutput; 
        pause; 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-clusterindex"></a>メソッド clusterIndex

テーブルのクラスター化されたインデックスの ID を返します。

```xpp
public IndexId clusterIndex([boolean asDefinedInAOT])
```

### <a name="parameters---clusterindex"></a>パラメーター - clusterIndex

asDefinedInAOT  
取得するクラスター インデックスが AOT で定義されているかどうかを示す値。 true の値は、AOT で定義されたクラスター インデックスを返します。 false の値は、SQL テーブルで定義されたクラスター インデックスを返します、オプション。

### <a name="return-value---clusterindex"></a>戻り値 - clusterIndex

テーブルのクラスター化されたインデックスの ID。テーブルのクラスター化されたインデックスがない場合は 0 (ゼロ)。

### <a name="examples---clusterindex"></a>例 - clusterIndex

次の例は、テーブルのクラスター インデックスの取得を示しています。

```xpp
DictTable dt; 
DictIndex di; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    i = dt.clusterIndex(); 
    if (0 != i) 
    { 
        di = new DictIndex(tablenum(CustTable), i); 
        print di.name(); 
    } 
}
```

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

テーブルのコンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

テーブルのコンフィギュレーション キーの ID。テーブルのコンフィギュレーション キーがない場合は 0 (ゼロ)。

### <a name="examples---configurationkeyid"></a>例 - configurationKeyId

次の例は、テーブルのコンフィギュレーション キー ID の取得を示しています。

```xpp
DictTable dt; 
DictConfigurationKey dck; 
dt = new DictTable(tablenum(AddressCountryRegionBLWI)); 
if (dt) 
{ 
    if (0 != dt.configurationKeyId()) 
    dck = new DictConfigurationKey(dt.configurationKeyId()); 
    if (dck) 
    { 
        print (strfmt("The table's configuration key is %1.", dck.name())); 
    } 
}
```

## <a name="method-dataperpartition"></a>メソッド dataPerPartition

テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。

```xpp
public boolean dataPerPartition()
```

### <a name="return-value---dataperpartition"></a>戻り値 - dataPerPartition

データがパーティション単位で保存される場合は true。それ以外の場合は false で、データはすべてのパーティションに対してグローバルに保存されます。

## <a name="method-dataprcompany"></a>メソッド dataPrCompany

テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。

```xpp
public boolean dataPrCompany()
```

### <a name="return-value---dataprcompany"></a>戻り値 - dataPrCompany

データが会社単位で保存される場合は true。それ以外の場合は false で、データはすべての会社に対してグローバルに保存されます。

### <a name="examples---dataprcompany"></a>例 - dataPrCompany

次の例は、データが会社ごとに保存されるかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? "per company" : "global")); 
}
```

## <a name="method-deleteactioncnt"></a>メソッド deleteActionCnt

テーブルの削除アクションの数を取得します。

```xpp
public int deleteActionCnt()
```

### <a name="return-value---deleteactioncnt"></a>戻り値 - deleteActionCnt

テーブルの削除アクションの数。

### <a name="examples---deleteactioncnt"></a>例 - deleteActionCnt

次の例は、テーブルの削除アクション数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 delete actions.", dt.deleteActionCnt())); 
}
```

## <a name="method-deleteactionrelation"></a>メソッド deleteActionRelation

```xpp
public str deleteActionRelation(int cnt)
```

### <a name="parameters---deleteactionrelation"></a>パラメーター - deleteActionRelation

cnt  

### <a name="return-value---deleteactionrelation"></a>戻り値 - deleteActionRelation

## <a name="method-deleteactiontableid"></a>メソッド deleteActionTableId

インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。

```xpp
public TableId deleteActionTableId(int cnt)
```

### <a name="parameters---deleteactiontableid"></a>パラメーター - deleteActionTableId

cnt  
テーブルの削除アクションのリストへの 1 から始まるインデックス。 リストは AOT の順です。

### <a name="return-value---deleteactiontableid"></a>戻り値 - deleteActionTableId

cnt によって指定されたテーブルの削除アクションのテーブル ID。cnt 値が有効な削除アクション索引を表していない場合は 0 (ゼロ)。

### <a name="examples---deleteactiontableid"></a>例 - deleteActionTableId

次の例は、deleteActionTableId メソッドを使用して CustTable テーブルの削除アクションを持つテーブルの名前を取得する方法を示しています。

```xpp
DictTable dt, dt2; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.deleteActionCnt(); i++) 
    { 
        dt2 = new DictTable(dt.deleteActionTableId(i)); 
        if (dt2) 
        { 
            print dt2.name(); 
        } 
    } 
}
```

## <a name="method-deleteactiontype"></a>メソッド deleteActionType

テーブルの削除アクションの種類を取得します。

```xpp
public int deleteActionType(int cnt)
```

### <a name="parameters---deleteactiontype"></a>パラメーター - deleteActionType

cnt  
テーブルの削除アクションのリストへの 1 から始まるインデックス。 リストは AOT の順です。

### <a name="return-value---deleteactiontype"></a>戻り値 - deleteActionType

cnt パラメーターで指定されているテーブルの削除アクションのタイプを表す整数。 これは、次のテーブルの値の 1 つになります。

|     |                      |
|-----|----------------------|
| 0   | None                 |
| 1   | 重ねて表示              |
| 2   | 制限           |
| 3   | 重ねて表示 + 制限 |

### <a name="examples---deleteactiontype"></a>例 - deleteActionType

次の例は、テーブルの削除アクションのタイプの取得を示しています。

```xpp
DictTable dt, dt2; 
str       strDelActType; 
int       i, nDelActType; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.deleteActionCnt(); i++) 
    { 
        dt2 = new DictTable(dt.deleteActionTableId(i)); 
        if (dt2) 
        { 
            nDelActType = dt.deleteActionType(i); 
            switch (nDelActType) 
            { 
               case 0: 
                strDelActType = "None"; 
                break; 
               case 1: 
                strDelActType = "Cascade"; 
                break; 
               case 2: 
                strDelActType = "Restricted"; 
                break; 
               case 3: 
                strDelActType = "Cascade + Restricted"; 
                break; 
            } 
            print strfmt("Delete action table: %1 Type: %2", 
                         dt2.name(), 
                         strDelActType); 
        } 
    } 
}
```

## <a name="method-developerdocumentation"></a>メソッド developerDocumentation

```xpp
public str developerDocumentation()
```

### <a name="return-value---developerdocumentation"></a>戻り値 - developerDocumentation

## <a name="method-developerdocumentationlabelid"></a>メソッド developerDocumentationLabelId

```xpp
public str developerDocumentationLabelId()
```

### <a name="return-value---developerdocumentationlabelid"></a>戻り値 - developerDocumentationLabelId

## <a name="method-enabled"></a>メソッド enabled

テーブルが有効かどうかを示す値を返します。

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a>戻り値 - enabled

テーブルが有効である場合は true。それ以外の場合は、false。

### <a name="examples---enabled"></a>例 - enabled

次の例は、テーブルが有効化されているかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table is %1.", dt.enabled() ? "enabled" : "not enabled")); 
}
```

## <a name="method-enforcerelationrules"></a>メソッド enforceRelationRules

```xpp
public boolean enforceRelationRules()
```

### <a name="return-value---enforcerelationrules"></a>戻り値 - enforceRelationRules

## <a name="method-entityrelationshiptype"></a>メソッド entityRelationshipType

```xpp
public EntityRelationshipType entityRelationshipType()
```

### <a name="return-value---entityrelationshiptype"></a>戻り値 - entityRelationshipType

## <a name="method-extendedby"></a>メソッド extendedBy

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a>パラメーター - extendedBy

allLevels  

### <a name="return-value---extendedby"></a>戻り値 - extendedBy

## <a name="method-extends"></a>メソッド extends

基本テーブルのテーブル ID を返します。

```xpp
public TableId extends()
```

### <a name="return-value---extends"></a>戻り値 - extends

ベース テーブルのテーブル ID

## <a name="method-fieldcnt"></a>メソッド fieldCnt

テーブルのフィールドの数を返します。

```xpp
public int fieldCnt([TableScope tableScope])
```

### <a name="parameters---fieldcnt"></a>パラメーター - fieldCnt

tableScope  

### <a name="return-value---fieldcnt"></a>戻り値 - fieldCnt

テーブルのフィールドの数。

### <a name="examples---fieldcnt"></a>例 - fieldCnt

次の例は、テーブルのフィールド数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 fields.", dt.fieldCnt())); 
}
```

## <a name="method-fieldcnt2id"></a>メソッド fieldCnt2Id

インデックスで指定されるフィールドのフィールド ID を返します。

```xpp
public FieldId fieldCnt2Id(int cnt, [TableScope tableScope])
```

### <a name="parameters---fieldcnt2id"></a>パラメーター - fieldCnt2Id

cnt  

<!-- -->

tableScope  

### <a name="return-value---fieldcnt2id"></a>戻り値 - fieldCnt2Id

インデックスで指定されたフィールドのフィールド ID。

### <a name="examples---fieldcnt2id"></a>例 - fieldCnt2Id

次の例は、インデックスによるテーブルのフィールドの取得を示しています。

```xpp
DictTable dt; 
int       i, fId, tId; 
DictField df; 
str       strFieldName; 
tId = tablenum(CustTable); 
dt = new DictTable(tId); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
        fId = dt.fieldCnt2Id(i); 
        df = new DictField(tId, fId); 
        strFieldName = (df ? df.name() : ""); 
        print(strfmt("%1) %2 %3", i, fId, strFieldName)); 
    } 
}
```

## <a name="method-fieldgroup"></a>メソッド fieldGroup

インデックスで指定されるフィールド グループの名前を返します。

```xpp
public str fieldGroup(int FieldGroupNumber, [TableScope tableScope])
```

### <a name="parameters---fieldgroup"></a>パラメーター - fieldGroup

FieldGroupNumber  

<!-- -->

tableScope  

### <a name="return-value---fieldgroup"></a>戻り値 - fieldGroup

FieldGroupNumber パラメーターで指定されるフィールド グループの名前。

### <a name="examples---fieldgroup"></a>例 - fieldGroup

次の例は、テーブルのフィールド グループの名前の取得を示しています。

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i =1; i <= dt.fieldGroupCnt(); i++) 
    { 
        print (dt.fieldGroup(i)); 
    } 
}
```

## <a name="method-fieldgroupcnt"></a>メソッド fieldGroupCnt

テーブルのフィールド グループの数を返します。

```xpp
public int fieldGroupCnt([TableScope tableScope])
```

### <a name="parameters---fieldgroupcnt"></a>パラメーター - fieldGroupCnt

tableScope  

### <a name="return-value---fieldgroupcnt"></a>戻り値 - fieldGroupCnt

テーブルのフィールド グループの数。

### <a name="examples---fieldgroupcnt"></a>例 - fieldGroupCnt

次の例は、テーブルのフィールド グループ数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 field groups.", dt.fieldGroupCnt())); 
}
```

## <a name="method-fieldname"></a>メソッド fieldName

フィールド ID で指定されるフィールドの名前を返します。

```xpp
public str fieldName(FieldId fieldId, [DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])
```

### <a name="parameters---fieldname"></a>パラメーター - fieldName

fieldId  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

db  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

arrayindex  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

generationMode  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

tableAlias  
テーブルのエイリアスの名前 (省略可能)。

### <a name="return-value---fieldname"></a>戻り値 - fieldName

フィールド ID で指定されるフィールド グループの名前。

### <a name="remarks---fieldname"></a>備考 - fieldName

db が指定されていない場合は、DbBackend::Native オブジェクトが使用されます。

### <a name="examples---fieldname"></a>例 - fieldName

次の例は、フィールド ID で指定されたテーブルのフィールド名の取得を示しています。

```xpp
DictTable dt; 
int       i, tId, fId; 
tId = tablenum(CustTable); 
dt = new DictTable(tId); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
        fId = dt.fieldCnt2Id(i); 
        print(strfmt("%1) %2 %3", i, fId, dt.fieldName(fId))); 
    } 
}
```

## <a name="method-fieldname2id"></a>メソッド fieldName2Id

名前で指定されるフィールドのフィールド ID を返します。

```xpp
public FieldId fieldName2Id(str name)
```

### <a name="parameters---fieldname2id"></a>パラメーター - fieldName2Id

名前  
フィールド ID が取得されているフィールドの名前。

### <a name="return-value---fieldname2id"></a>戻り値 - fieldName2Id

name パラメーターで指定されたフィールドのフィールド ID。name がテーブルの有効なフィールド名を表していない場合は 0 (ゼロ) です。

### <a name="examples---fieldname2id"></a>例 - fieldName2Id

次の例は、フィールド名によるフィールド ID の取得を示しています。

```xpp
DictTable dt; 
fieldId   fId; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    fId = dt.fieldName2Id("Pager"); 
    // Use the field ID as needed. 
    // This example merely prints out the field ID. 
    print (strfmt("fId: %1", fId)); 
}
```

## <a name="method-fieldnext"></a>メソッド fieldNext

テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。

```xpp
public FieldId fieldNext(FieldId fieldId, [TableScope tableScope])
```

### <a name="parameters---fieldnext"></a>パラメーター - fieldNext

fieldId  

<!-- -->

tableScope  

### <a name="return-value---fieldnext"></a>戻り値 - fieldNext

テーブルのフィールド反復における次のフィールドの ID。反復処理するフィールドがない場合は 0 (ゼロ)。

### <a name="remarks---fieldnext"></a>備考 - fieldNext

フィールドの反復を開始するには、fieldId パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。

### <a name="examples---fieldnext"></a>例 - fieldNext

次の例では、テーブルのフィールドを反復処理します。

```xpp
DictTable   dt; 
DictField   df; 
int         counter; 
counter = 0; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    counter = dt.fieldNext(counter); 
    while (counter) 
    { 
        df = dt.fieldObject(counter); 
        if (df) 
        { 
            print strfmt("ID: %1 Name: %2", 
                         df.id(), 
                         df.name() ); 
        } 
        counter = dt.fieldNext(counter); 
    } 
}
```

## <a name="method-fieldobject"></a>メソッド fieldObject

フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。

```xpp
public DictField fieldObject(FieldId fieldId)
```

### <a name="parameters---fieldobject"></a>パラメーター - fieldObject

fieldId  
作成するフィールドの ID。

### <a name="return-value---fieldobject"></a>戻り値 - fieldObject

fieldId パラメーターで指定されたフィールドの DictField オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="examples---fieldobject"></a>例 - fieldObject

次の例は、テーブル内のフィールドの DictField オブジェクトを作成する方法を示しています。

```xpp
DictTable dt; 
DictField df; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.fieldCnt(); i++) 
    { 
      df = dt.fieldObject(dt.fieldCnt2Id(i)); 
      if (df) 
      { 
          print df.name(); 
      } 
    } 
}
```

## <a name="method-fieldorigin2id"></a>メソッド fieldOrigin2Id

```xpp
public IndexId fieldOrigin2Id(Guid fieldOrigin, [TableScope tableScope])
```

### <a name="parameters---fieldorigin2id"></a>パラメーター - fieldOrigin2Id

fieldOrigin  

<!-- -->

tableScope  

### <a name="return-value---fieldorigin2id"></a>戻り値 - fieldOrigin2Id

## <a name="method-fieldsqldefault"></a>メソッド fieldSqlDefault

フィールド ID で指定されているフィールドの SQL 既定値を返します。

```xpp
public str fieldSqlDefault(FieldId fieldId)
```

### <a name="parameters---fieldsqldefault"></a>パラメーター - fieldSqlDefault

fieldId  
SQL の既定のデータが取得されるフィールドの ID。

### <a name="return-value---fieldsqldefault"></a>戻り値 - fieldSqlDefault

fieldId パラメーターで指定されたフィールドの SQL 既定値を表す文字列、フィールドに SQL のデフォルト値がない場合、またはテーブルが SQL テーブルではない場合は空の文字列。

## <a name="method-formref"></a>メソッド formRef

テーブルの既定のフォームの名前を返します。

```xpp
public str formRef([boolean searchBaseTables])
```

### <a name="parameters---formref"></a>パラメーター - formRef

searchBaseTables  

### <a name="return-value---formref"></a>戻り値 - formRef

テーブルの既定のフォームの名前。

### <a name="remarks---formref"></a>備考 - formRef

AOT に、テーブルの FormRef プロパティの値が表示されない場合、テーブルの既定のフォームの名前は、テーブルの名前と同じであると見なされます。 この場合、このメソッドは空の文字列を返しません。

### <a name="examples---formref"></a>例 - formRef

次の例は、テーブルの既定のフォームの取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("Default form: %1", dt.formRef()); 
}
```

## <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a>戻り値 - getCountryRegionCodes

## <a name="method-getcountryregioncontextfield"></a>メソッド getCountryRegionContextField

```xpp
public FieldId getCountryRegionContextField()
```

### <a name="return-value---getcountryregioncontextfield"></a>戻り値 - getCountryRegionContextField

## <a name="method-getvalidtimestatevalidfromfieldid"></a>メソッド getValidTimeStateValidFromFieldId

```xpp
public FieldId getValidTimeStateValidFromFieldId()
```

### <a name="return-value---getvalidtimestatevalidfromfieldid"></a>戻り値 - getValidTimeStateValidFromFieldId

## <a name="method-getvalidtimestatevalidtofieldid"></a>メソッド getValidTimeStateValidToFieldId

```xpp
public FieldId getValidTimeStateValidToFieldId()
```

### <a name="return-value---getvalidtimestatevalidtofieldid"></a>戻り値 - getValidTimeStateValidToFieldId

## <a name="method-hasrecididx"></a>メソッド hasRecidIdx

テーブルのレコード ID インデックスが有効かどうかを示す値を返します。

```xpp
public boolean hasRecidIdx()
```

### <a name="return-value---hasrecididx"></a>戻り値 - hasRecidIdx

レコード ID インデックスがテーブルで有効な場合は true。それ以外の場合は、false。

### <a name="remarks---hasrecididx"></a>備考 - hasRecidIdx

戻り値は、テーブルの CreateRecIdIndex プロパティが Yes に設定されているかどうかに対応します。

### <a name="examples---hasrecididx"></a>例 - hasRecidIdx

次の例は、テーブルのレコード ID インデックスが有効かどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("A record ID index for the table %1 in effect.", 
           dt.hasRecidIdx() ? "is" : "is not") ); 
}
```

## <a name="method-hassurrogatekey"></a>メソッド hasSurrogateKey

```xpp
public boolean hasSurrogateKey()
```

### <a name="return-value---hassurrogatekey"></a>戻り値 - hasSurrogateKey

## <a name="method-id"></a>メソッド id

テーブルの ID を返します。

```xpp
public TableId id()
```

### <a name="return-value---id"></a>戻り値 - id

テーブルの ID。

### <a name="examples---id"></a>例 - id

次の例は、テーブルの ID の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table ID is: %1", dt.id())); 
}
```

## <a name="method-indexcnt"></a>メソッド indexCnt

テーブルのインデックスの数を返します。

```xpp
public int indexCnt()
```

### <a name="return-value---indexcnt"></a>戻り値 - indexCnt

テーブルのインデックスの数。

### <a name="examples---indexcnt"></a>例 - indexCnt

次の例は、テーブルのインデックス数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 indexes.", dt.indexCnt())); 
}
```

## <a name="method-indexcnt2id"></a>メソッド indexCnt2Id

```xpp
public IndexId indexCnt2Id(int cnt)
```

### <a name="parameters---indexcnt2id"></a>パラメーター - indexCnt2Id

cnt  

### <a name="return-value---indexcnt2id"></a>戻り値 - indexCnt2Id

## <a name="method-indexname"></a>メソッド indexName

indexId パラメーターで指定された形式のインデックスの名前を返します。

```xpp
public str indexName(IndexId indexId, [DbBackend db])
```

### <a name="parameters---indexname"></a>パラメーター - indexName

indexId  
データベース バックエンドのタイプを指定する DbBackend 値; オプション。

<!-- -->

db  
データベース バックエンドのタイプを指定する DbBackend 値; オプション。

### <a name="return-value---indexname"></a>戻り値 - indexName

indexId パラメーターで指定された形式のインデックスの名前。

### <a name="examples---indexname"></a>例 - indexName

次の例は、テーブルのインデックスの名前の取得を示しています。

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.indexCnt(); i++) 
    { 
        print (dt.indexName(i)); 
    } 
}
```

## <a name="method-indexname2id"></a>メソッド indexName2Id

名前で指定されているインデックスの ID を返します。

```xpp
public IndexId indexName2Id(str name)
```

### <a name="parameters---indexname2id"></a>パラメーター - indexName2Id

名前  
インデックスの名前。

### <a name="return-value---indexname2id"></a>戻り値 - indexName2Id

名前パラメーターで指定されているインデックスの ID。名前値と同じ名前が付けられたインデックスがない場合は 0 (ゼロ)。

### <a name="examples---indexname2id"></a>例 - indexName2Id

次の例は、名前で指定されたインデックスの ID の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("Index ID: %1", dt.indexName2Id("TypeIdx"))); 
}
```

## <a name="method-indexnext"></a>メソッド indexNext

テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。

```xpp
public IndexId indexNext(IndexId id)
```

### <a name="parameters---indexnext"></a>パラメーター - indexNext

id  
次のインデックス ID が照会されるインデックスの ID。

### <a name="return-value---indexnext"></a>戻り値 - indexNext

テーブルのインデックス反復における次のインデックスの ID。反復処理するインデックスがない場合は 0 (ゼロ)。

### <a name="remarks---indexnext"></a>備考 - indexNext

インデックスの反復を開始するには、id パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。

### <a name="examples---indexnext"></a>例 - indexNext

次の例では、テーブルのインデックスを反復処理します。

```xpp
DictTable   dt; 
DictIndex   di; 
int         counter; 
counter = 0; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    counter = dt.indexNext(counter); 
    while (counter) 
    { 
        di = dt.indexObject(counter); 
        if (di) 
        { 
            print strfmt("ID: %1 Name: %2", 
                         di.id(), 
                         di.name() ); 
        } 
        counter = dt.indexNext(counter); 
    } 
}
```

## <a name="method-indexobject"></a>メソッド indexObject

ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。

```xpp
public DictIndex indexObject(IndexId indexId)
```

### <a name="parameters---indexobject"></a>パラメーター - indexObject

indexId  
作成するインデックスの ID。

### <a name="return-value---indexobject"></a>戻り値 - indexObject

indexId パラメーターで指定されたインデックスの DictIndex オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="examples---indexobject"></a>例 - indexObject

次の例は、テーブルの固有インデックスの DictIndex オブジェクトを作成する方法を示しています。

```xpp
DictTable dt; 
DictIndex di; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     di = dt.indexObject(dt.indexUnique()); 
     if (di) 
     { 
        print di.name(); 
     } 
}
```

## <a name="method-indexunique"></a>メソッド indexUnique

テーブルの一意のインデックスの ID を返します。

```xpp
public IndexId indexUnique()
```

### <a name="return-value---indexunique"></a>戻り値 - indexUnique

テーブルの一意のインデックスの ID。

### <a name="remarks---indexunique"></a>備考 - indexUnique

テーブルに複数の一意のインデックスが存在するとき、戻り値は次のいずれかです。

-   RecID 列を持つインデックス。
-   インデックスにレコードの ID がない場合、最短サイズを持つインデックスは、列のサイズの合計に基づきます。
-   最短サイズに関して複数のインデックスが一致する場合、インデックスが最初に追加されました。

### <a name="examples---indexunique"></a>例 - indexUnique

次の例は、テーブルの固有インデックスの取得を示しています。

```xpp
DictTable dt; 
DictIndex di; 
dt = new DictTable(tablenum(SysUserInfo)); 
if (dt) 
{ 
     di = dt.indexObject(dt.indexUnique()); 
     if (di) 
     { 
        print di.name(); 
     } 
}
```

## <a name="method-instancerelationtype"></a>メソッド instanceRelationType

```xpp
public FieldId instanceRelationType()
```

### <a name="return-value---instancerelationtype"></a>戻り値 - instanceRelationType

## <a name="method-isabstract"></a>メソッド isAbstract

このテーブルが抽象かどうかを示します。

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a>戻り値 - isAbstract

このテーブルが抽象である場合は true。それ以外の場合は、false。

## <a name="method-isbasedata"></a>メソッド isBaseData

テーブル コンテンツが基本データであるかどうかを示します。

```xpp
public boolean isBaseData()
```

### <a name="return-value---isbasedata"></a>戻り値 - isBaseData

テーブル コンテンツがベース データであることを AOT 内の TableContents プロパティが示す場合は true。それ以外の場合は、false。

### <a name="examples---isbasedata"></a>例 - isBaseData

次の例は、テーブルの内容が基本データかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("isBaseData: %1", dt.isBaseData()); 
    print strfmt("isDefaultData: %1", dt.isDefaultData()); 
}
```

## <a name="method-isdefaultdata"></a>メソッド isDefaultData

テーブルが既定のデータを含むかどうかを示します。

```xpp
public boolean isDefaultData()
```

### <a name="return-value---isdefaultdata"></a>戻り値 - isDefaultData

テーブルに既定のデータが含まれている場合は true。それ以外の場合は、false。

### <a name="examples---isdefaultdata"></a>例 - isDefaultData

次の例は、テーブルに既定のデータが含まれているかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("isDefaultData: %1", dt.isDefaultData()); 
}
```

## <a name="method-isderivedfrom"></a>メソッド isDerivedFrom

1 つのテーブル タイプが別から派生しているかどうかを示します。

```xpp
public boolean isDerivedFrom(TableName baseTableName)
```

### <a name="parameters---isderivedfrom"></a>パラメータ - isDerivedFrom

baseTableName  

### <a name="return-value---isderivedfrom"></a>戻り値 - isDerivedFrom

このテーブルが baseTableName パラメーターで指定されたテーブルに由来する場合は true。

## <a name="method-ismap"></a>メソッド isMap

テーブルがマップであるかどうかを示します。

```xpp
public boolean isMap()
```

### <a name="return-value---ismap"></a>戻り値 - isMap

テーブルがマップである場合は true。それ以外の場合は false。

### <a name="examples---ismap"></a>例 - isMap

次の例は、テーブルがマップかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(AddressMap)); 
if (dt) 
{ 
    print(strfmt("Map: %1", dt.isMap())); 
}
```

## <a name="method-issql"></a>メソッド isSql

テーブルが SQL テーブルであるかどうかを示します。

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a>戻り値 - isSql

テーブルが SQL テーブルである場合は true。それ以外の場合は false。

### <a name="examples---issql"></a>例 - isSql

次の例は、テーブルが SQL テーブルかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("SQL table: %1", dt.isSql())); 
}
```

## <a name="method-issystemtable"></a>メソッド isSystemTable

テーブルがシステム テーブルであるかどうかを示します。

```xpp
public boolean isSystemTable()
```

### <a name="return-value---issystemtable"></a>戻り値 - isSystemTable

テーブルがシステム テーブルである場合は true。それ以外の場合は false。

### <a name="examples---issystemtable"></a>例 - isSystemTable

次の例は、テーブルがシステム テーブルかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("System table: %1", dt.isSystemTable())); 
}
```

## <a name="method-istempdb"></a>メソッド isTempDb

```xpp
public boolean isTempDb()
```

### <a name="return-value---istempdb"></a>戻り値 - isTempDb

## <a name="method-istmp"></a>メソッド isTmp

テーブルが一時テーブルであるかどうかを示します。

```xpp
public boolean isTmp()
```

### <a name="return-value---istmp"></a>戻り値 - isTmp

テーブルが一時テーブルである場合は true。それ以外の場合は false。

### <a name="examples---istmp"></a>例 - isTmp

次の例は、テーブルが一時テーブルかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(TmpWMSOrder)); 
if (dt) 
{ 
    print(strfmt("Temporary table: %1", dt.isTmp())); 
}
```

## <a name="method-isunionallview"></a>メソッド isUnionAllView

```xpp
public boolean isUnionAllView()
```

### <a name="return-value---isunionallview"></a>戻り値 - isUnionAllView

## <a name="method-isvalidtimestatetable"></a>メソッド isValidTimeStateTable

```xpp
public boolean isValidTimeStateTable()
```

### <a name="return-value---isvalidtimestatetable"></a>戻り値 - isValidTimeStateTable

## <a name="method-isview"></a>メソッド isView

テーブルがビューであるかどうかを示します。

```xpp
public boolean isView()
```

### <a name="return-value---isview"></a>戻り値 - isView

テーブルがビューである場合は true。それ以外の場合は false。

### <a name="examples---isview"></a>例 - isView

次の例は、テーブルがビューかどうかを示す値の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print(strfmt("View: %1", dt.isView())); 
}
```

## <a name="method-label"></a>メソッド label

テーブルのラベル テキストを返します。

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

テーブルのラベル テキスト。テーブルにラベル テキストがない場合は空の文字列。

### <a name="examples---label"></a>例 - label

次の例は、テーブルのラベル テキストの取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
     print(strfmt("Label: %1", dt.label())); 
}
```

## <a name="method-labeldefined"></a>メソッド labelDefined

テーブルの label プロパティの値を返します。

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a>戻り値 - labelDefined

テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。

## <a name="method-listpageref"></a>メソッド listPageRef

```xpp
public str listPageRef([boolean searchBaseTables])
```

### <a name="parameters---listpageref"></a>パラメーター - listPageRef

searchBaseTables  

### <a name="return-value---listpageref"></a>戻り値 - listPageRef

## <a name="method-makerecord"></a>メソッド makeRecord

テーブルの空白のレコードを作成します。

```xpp
public Common makeRecord()
```

### <a name="return-value---makerecord"></a>戻り値 - makeRecord

レコードが正常に作成された場合の共通の値。レコードを作成できなかった場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="remarks---makerecord"></a>備考 - makeRecord

返される共通値は、DictTable.callObject メソッドの呼び出しで使用できます。

## <a name="method-maxaccessmode"></a>メソッド maxAccessMode

AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。

```xpp
public AccessType maxAccessMode()
```

### <a name="return-value---maxaccessmode"></a>戻り値 - maxAccessMode

テーブルの最大アクセス モードを表す AccessType 値。

### <a name="examples---maxaccessmode"></a>例 - maxAccessMode

次の例は、テーブルの最大アクセス モードの取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print strfmt("Maximum Access Mode: %1",dt.maxAccessMode()); 
}
```

## <a name="method-name"></a>メソッド名

テーブル名を取得します。

```xpp
public str name([DbBackend db], [boolean pseudoname])
```

### <a name="parameters---name"></a>パラメーター - 名前

db  
疑似名が返されるかどうかを示すブール値; オプション。

<!-- -->

pseudoname  
疑似名が返されるかどうかを示すブール値; オプション。

### <a name="return-value---name"></a>戻り値 - name

テーブルの名前。

### <a name="remarks---name"></a>備考 - 名前

テーブル名が 30 文字よりも長い場合は、ネイティブ名およびテーブルの SQL 名は一致しません。

### <a name="examples---name"></a>例 - 名前

次の例は、テーブルの名前の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(1);  // 1 == tablenum(CustTable) 
if (dt) 
{ 
    print(strfmt("The table name is %1.", dt.name())); 
}
```

## <a name="method-objectmethod"></a>メソッド objectMethod

インデックスで指定されるインスタンス メソッドの名前を返します。

```xpp
public str objectMethod(int methodNumber, [TableScope tableScope])
```

### <a name="parameters---objectmethod"></a>パラメーター - objectMethod

methodNumber  

<!-- -->

tableScope  

### <a name="return-value---objectmethod"></a>戻り値 - objectMethod

methodNumber パラメーターで指定されているインスタンス メソッドの名前。methodNumber 値が有効なインスタンス メソッド インデックスでない場合は空の文字列。

### <a name="examples---objectmethod"></a>例 - objectMethod

次の例は、テーブル内の各インスタンス メソッドの名前の取得を示しています。

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.objectMethodCnt() ; i++) 
    { 
        print dt.objectMethod(i); 
    } 
}
```

## <a name="method-objectmethodcnt"></a>メソッド objectMethodCnt

テーブルのインスタンス メソッドの数を返します。

```xpp
public int objectMethodCnt([TableScope tableScope])
```

### <a name="parameters---objectmethodcnt"></a>パラメーター - objectMethodCnt

tableScope  

### <a name="return-value---objectmethodcnt"></a>戻り値 - objectMethodCnt

テーブルのインスタンス メソッドの数。

### <a name="examples---objectmethodcnt"></a>例 - objectMethodCnt

次の例は、テーブルのインスタンス メソッド数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 instance methods.", dt.objectMethodCnt())); 
}
```

## <a name="method-objectmethodobject"></a>メソッド objectMethodObject

インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。

```xpp
public DictMethod objectMethodObject(int methodNumber, [TableScope tableScope])
```

### <a name="parameters---objectmethodobject"></a>パラメーター - objectMethodObject

methodNumber  

<!-- -->

tableScope  

### <a name="return-value---objectmethodobject"></a>戻り値 - objectMethodObject

methodNumber パラメーターで指定されているオブジェクト メソッドの MethodInfo クラスのインスタンス。インスタンスを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="examples---objectmethodobject"></a>例 - objectMethodObject

次の例は、テーブルのオブジェクト メソッドの取得を示しています。

```xpp
DictTable dt; 
int       i; 
MethodInfo mi; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.objectMethodCnt(); i++) 
    { 
        mi = dt.objectMethodObject(i); 
        if (mi) 
        { 
            print mi.name(); 
        } 
    } 
}
```

## <a name="method-mapobject"></a>メソッド mapObject

インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。

```xpp
public DictTableMap mapObject(int methodNumber)
```

### <a name="parameters---mapobject"></a>パラメーター - mapObject

methodNumber  

### <a name="return-value---mapobject"></a>戻り値 - mapObject

\_cnt パラメーターで指定されたフィールドの DictTableMap オブジェクト。オブジェクトを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-mapcnt"></a>メソッド mapCnt

この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。

```xpp
public int mapCnt()
```

### <a name="return-value---mapcnt"></a>戻り値 - mapCnt

カウント。

## <a name="method-occenabled"></a>メソッド occEnabled

テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。

```xpp
public boolean occEnabled()
```

### <a name="return-value---occenabled"></a>戻り値 - occEnabled

オプティミスティック同時モードが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---occenabled"></a>備考 - occEnabled

このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。 データは、実際の更新の実行時にのみロックされます。

### <a name="examples---occenabled"></a>例 - occEnabled

次の例は、occEnabled メソッドの呼び出しを示しています。

```xpp
static public void Main(Args _args) 
{ 
    DictTable dt; 
    boolean enabled; 
    dt = new DictTable(tablenum(CustTable)); 
    enabled = dt.occEnabled(); 
}
```

## <a name="method-primaryindex"></a>メソッド primaryIndex

テーブルのプライマリ インデックスの ID を返します。

```xpp
public IndexId primaryIndex([boolean asDefinedInAOT])
```

### <a name="parameters---primaryindex"></a>パラメーター - primaryIndex

asDefinedInAOT  
取得するプライマリ インデックスが、AOT で定義されているかどうかを示すブール値。 true の値は、AOT で定義されたプライマリ インデックスを返します。 false の値は、SQL テーブルで定義されたプライマリ インデックスを返します、オプション。

### <a name="return-value---primaryindex"></a>戻り値 - primaryIndex

テーブルの主インデックスの ID。テーブルの主インデックスがない場合は 0 (ゼロ)。

### <a name="examples---primaryindex"></a>例 - primaryIndex

次の例は、テーブルのプライマリ インデックスの取得を示しています。

```xpp
DictTable dt; 
DictIndex di; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    i = dt.primaryIndex(); 
    if (0 != i) 
    { 
        di = new DictIndex(tablenum(CustTable), i); 
        print di.name(); 
    } 
}
```

## <a name="method-primarykeyfield"></a>メソッド primaryKeyField

テーブルの主キーに使用されているフィールドの ID を返します。

```xpp
public FieldId primaryKeyField()
```

### <a name="return-value---primarykeyfield"></a>戻り値 - primaryKeyField

テーブルの主キーで使用されるフィールドの ID。テーブルの主キーとして機能する単一のフィールドがない場合は 0 (ゼロ)。

### <a name="examples---primarykeyfield"></a>例 - primaryKeyField

次の例は、テーブルの主キーのフィールド ID の取得を示しています。

```xpp
DictTable dt; 
DictField df; 
tableId   tID; 
fieldId   fID; 
tID = tablenum(CustTable); 
dt = new DictTable(tID); 
if (dt) 
{ 
   fID = dt.primaryKeyField(); 
   if (0 != fID) 
   { 
       df = new DictField(tID, fID); 
       if (df) 
       { 
            print strfmt("Primary key field name: %1", df.name()); 
       } 
   } 
}
```

## <a name="method-relation"></a>メソッド relation

インデックスで指定される関係の名前を返します。

```xpp
public str relation(int RelationNumber, [TableScope tableScope])
```

### <a name="parameters---relation"></a>パラメーター - relation

RelationNumber  

<!-- -->

tableScope  

### <a name="return-value---relation"></a>戻り値 - relation

RelationNumber パラメーターで指定されているリレーションの名前。RelationNumber 値が有効なリレーション インデックスでない場合は空の文字列。

### <a name="examples---relation"></a>例 - relation

次の例は、テーブル内の各リレーションの名前の取得を示しています。

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.relationCnt() ; i++) 
    { 
        print dt.relation(i); 
    } 
}
```

## <a name="method-relationcnt"></a>メソッド relationCnt

テーブルの関係の数を返します。

```xpp
public int relationCnt([TableScope tableScope])
```

### <a name="parameters---relationcnt"></a>パラメーター - relationCnt

tableScope  

### <a name="return-value---relationcnt"></a>戻り値 - relationCnt

テーブルのリレーションの番号。

### <a name="examples---relationcnt"></a>例 - relationCnt

次の例は、テーブルのリレーション数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 relations.", dt.relationCnt())); 
}
```

## <a name="method-replacementkey"></a>メソッド replacementKey

```xpp
public IndexId replacementKey()
```

### <a name="return-value---replacementkey"></a>戻り値 - replacementKey

## <a name="method-reportref"></a>メソッド reportRef

テーブルの既定のレポートの名前を返します。

```xpp
public str reportRef()
```

### <a name="return-value---reportref"></a>戻り値 - reportRef

テーブルの既定のレポートの名前。テーブルの既定のレポートがない場合は空の文字列。

### <a name="examples---reportref"></a>例 - reportRef

以下は、テーブルの既定のレポートの名前の取得を示しています。

```xpp
DictTable dt; 
str       strReport; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    strReport = dt.reportRef(); 
    print strfmt("Default report: %1", strReport != "" ? strReport : "None specified"); 
}
```

## <a name="method-rights"></a>メソッド rights

テーブルに指定されている、現在のユーザーのアクセス権を返します。

```xpp
public AccessType rights([boolean ignoreContext])
```

### <a name="parameters---rights"></a>パラメーター - rights

ignoreContext  

### <a name="return-value---rights"></a>戻り値 - rights

テーブルに指定されている、現在のユーザーのアクセス権。 戻り値は、AccessType システム列挙値の 1 つです。

## <a name="method-securitykeyid"></a>メソッド securityKeyId

テーブルのセキュリティ キーの ID を返します。

```xpp
public SecurityKeyId securityKeyId()
```

### <a name="return-value---securitykeyid"></a>戻り値 - securityKeyId

テーブルのセキュリティ キーの ID。テーブルのセキュリティ キーがない場合は 0 (ゼロ)。

## <a name="method-singularlabel"></a>メソッド singularLabel

```xpp
public str singularLabel([boolean labelTranslation])
```

### <a name="parameters---singularlabel"></a>パラメーター - singularLabel

labelTranslation  

### <a name="return-value---singularlabel"></a>戻り値 - singularLabel

## <a name="method-staticmethod"></a>メソッド staticMethod

インデックスで指定される静的メソッドの名前を返します。

```xpp
public str staticMethod(int methodNumber)
```

### <a name="parameters---staticmethod"></a>パラメーター - staticMethod

methodNumber  
テーブルの静的メソッドのリストへの AOT の順で、1 から始まるインデックス。

### <a name="return-value---staticmethod"></a>戻り値 - staticMethod

methodNumber パラメーターで指定されている静的メソッドの名前。methodNumber 値が有効な静的メソッド インデックスでない場合は空の文字列。

### <a name="examples---staticmethod"></a>例 - staticMethod

次の例は、テーブル内の各静的メソッドの名前の取得を示しています。

```xpp
DictTable dt; 
int       i; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.staticMethodCnt() ; i++) 
    { 
        print dt.staticMethod(i); 
    } 
}
```

## <a name="method-staticmethodcnt"></a>メソッド staticMethodCnt

テーブルの静的メソッドの数を返します。

```xpp
public int staticMethodCnt()
```

### <a name="return-value---staticmethodcnt"></a>戻り値 - staticMethodCnt

テーブルの静的メソッドの数。

### <a name="examples---staticmethodcnt"></a>例 - staticMethodCnt

次の例は、テーブルの静的メソッド数の取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    print (strfmt("The table has %1 static methods.", dt. staticMethodCnt())); 
}
```

## <a name="method-staticmethodobject"></a>メソッド staticMethodObject

インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。

```xpp
public DictMethod staticMethodObject(int methodNumber)
```

### <a name="parameters---staticmethodobject"></a>パラメーター - staticMethodObject

methodNumber  
テーブルの静的メソッドへの AOT の順で、1 から始まるインデックス。

### <a name="return-value---staticmethodobject"></a>戻り値 - staticMethodObject

methodNumber パラメーターで指定されている静的メソッドの MethodInfo クラスのインスタンス。インスタンスを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="examples---staticmethodobject"></a>例 - staticMethodObject

次の例は、テーブルの静的メソッドの取得を示しています。

```xpp
DictTable dt; 
int       i; 
MethodInfo mi; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    for (i=1; i <= dt.staticMethodCnt(); i++) 
    { 
        mi = dt.staticMethodObject(i); 
        if (mi) 
        { 
            print mi.name(); 
        } 
    } 
}
```

## <a name="method-supportinheritance"></a>メソッド supportInheritance

```xpp
public boolean supportInheritance()
```

### <a name="return-value---supportinheritance"></a>戻り値 - supportInheritance

## <a name="method-tablegroup"></a>メソッド tableGroup

テーブルのテーブル グループを返します。

```xpp
public TableGroup tableGroup()
```

### <a name="return-value---tablegroup"></a>戻り値 - tableGroup

テーブルのテーブル グループを表す TableGroup 値。

### <a name="remarks---tablegroup"></a>備考 - tableGroup

戻り値は、AOT テーブルの TableGroup プロパティに対応します。

### <a name="examples---tablegroup"></a>例 - tableGroup

次の例は、テーブルのテーブル グループの取得を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
   print strfmt("Table Group: %1", dt.tableGroup()); 
}
```

## <a name="method-tabletype"></a>メソッド tableType

テーブルのタイプを示します。

```xpp
public TableType tableType()
```

### <a name="return-value---tabletype"></a>戻り値 - tableType

エラー状態がある場合は、エラー状態です。

## <a name="method-titlefield1"></a>メソッド titleField1

テーブルの titleField1 プロパティを表すフィールドの ID を返します。

```xpp
public FieldId titleField1([boolean includeBaseTables], [boolean extendedFieldId])
```

### <a name="parameters---titlefield1"></a>パラメーター - titleField1

includeBaseTables  

<!-- -->

extendedFieldId  

### <a name="return-value---titlefield1"></a>戻り値 - titleField1

テーブルの titleField1 プロパティを表すフィールドの ID。

### <a name="remarks---titlefield1"></a>備考 - titleField1

ベスト プラクティスのガイドラインに従うと、titleField1 プロパティは、テーブルのレコードのキー フィールドを表します。

### <a name="examples---titlefield1"></a>例 - titleField1

次の例は、テーブルの titleField1 プロパティに使用されるフィールドの ID の取得を示しています。

```xpp
DictTable dt; 
DictField df; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    df = new DictField(tablenum(CustTable),dt.titleField1()); 
    if (df) 
    { 
        print df.name(); 
    } 
} 
pause;
```

## <a name="method-titlefield2"></a>メソッド titleField2

テーブルの titleField2 プロパティを表すフィールドの ID を返します。

```xpp
public FieldId titleField2([boolean includeBaseTables], [boolean extendedFieldId])
```

### <a name="parameters---titlefield2"></a>パラメーター - titleField2

includeBaseTables  

<!-- -->

extendedFieldId  

### <a name="return-value---titlefield2"></a>戻り値 - titleField2

テーブルの titleField2 プロパティを表すフィールドの ID。

### <a name="remarks---titlefield2"></a>備考 - titleField2

ベスト プラクティスのガイドラインに従うと、titleField2 プロパティは、テーブルのレコードの説明を表します。

### <a name="examples---titlefield2"></a>例 - titleField2

次の例は、テーブルの titleField2 プロパティに使用されるフィールドの ID の取得を示しています。

```xpp
DictTable dt; 
DictField df; 
dt = new DictTable(tablenum(CustTable)); 
if (dt) 
{ 
    df = new DictField(tablenum(CustTable),dt.titleField2()); 
    if (df) 
    { 
        print df.name(); 
    } 
}
```

## <a name="method-validrelationship"></a>メソッド validRelationship

```xpp
public boolean validRelationship()
```

### <a name="return-value---validrelationship"></a>戻り値 - validRelationship

## <a name="method-visible"></a>メソッド visible

テーブルが表示できるかどうかを判定します。

```xpp
public boolean visible()
```

### <a name="return-value---visible"></a>戻り値 - visible

テーブルが可視である場合は true。それ以外の場合は false。

## <a name="method-construct"></a>メソッド construct

```xpp
public static DictTable construct(str tableName)
```

### <a name="parameters---construct"></a>パラメーター - construct

tableName  

### <a name="return-value---construct"></a>戻り値 - construct

## <a name="method-getrelationtypefromtablename"></a>メソッド getRelationTypeFromTableName

```xpp
public static RecId getRelationTypeFromTableName(TableName tableName)
```

### <a name="parameters---getrelationtypefromtablename"></a>パラメーター - getRelationTypeFromTableName

tableName  

### <a name="return-value---getrelationtypefromtablename"></a>戻り値 - getRelationTypeFromTableName

## <a name="method-gettablenamefromrelationtype"></a>メソッド getTableNameFromRelationType

```xpp
public static TableName getTableNameFromRelationType(RecId relationType)
```

### <a name="parameters---gettablenamefromrelationtype"></a>パラメーター - getTableNameFromRelationType

relationType  

### <a name="return-value---gettablenamefromrelationtype"></a>戻り値 - getTableNameFromRelationType

## <a name="method-createrecord"></a>メソッド createRecord

```xpp
public static Common createRecord(str tableName)
```

### <a name="parameters---createrecord"></a>パラメーター - createRecord

tableName  

### <a name="return-value---createrecord"></a>戻り値 - createRecord

## <a name="method-reloadsecurity"></a>メソッド reloadSecurity

テーブルの機能キー システムを再読み込みします。

```xpp
public void reloadSecurity()
```

### <a name="examples---reloadsecurity"></a>例 - reloadSecurity

次の例では、テーブルの機能キー システムを再読み込みします。

```xpp
dt.reloadSecurity()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a>パラメーター - new

tableId  
DictTable クラスのインスタンスを作成するために使用されるテーブルの ID。

### <a name="examples---new"></a>例 - new

次の例は、DictTable クラスのインスタンスを作成する方法を示しています。

```xpp
DictTable dt; 
dt = new DictTable(tablenum(CustTable)); 
if (!dt) 
{ 
    // Take error action. 
}
```

## <a name="method-reindex"></a>メソッド reindex

テーブルのインデックスの再作成を実行します。

```xpp
public void reindex()
```

### <a name="remarks---reindex"></a>備考 - reindex

SQL テーブルのインデックスの再作成にこのメソッドを使用しないでください。代わりに、SqlDataDictionary::tableReindex メソッドを使用してください。 また、クライアントで実行時に DictTable::reindex メソッドはサポートされません。

