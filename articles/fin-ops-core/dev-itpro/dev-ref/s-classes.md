---
title: S クラス
description: 文字 S で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 51751
ms.assetid: cb7c0fd3-34ec-407b-ad78-1007a67d70d5
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18f889ce6d00379d6c1851eb4c32cdc899815550
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191609"
---
# <a name="s-classes"></a>S クラス

[!include [banner](../includes/banner.md)]

文字 S で始まるシステム API クラス。

<a name="class-scannerclass"></a>クラス ScannerClass
------------------

    class ScannerClass extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| public int col()                                                                             |                                                 |
| public Date dateValue()                                                                      |                                                 |
| public int firstSymbol()                                                                     |                                                 |
| public Int64 int64Value()                                                                    |                                                 |
| public int intValue()                                                                        |                                                 |
| public int line()                                                                            |                                                 |
| public int nextSymbol()                                                                      |                                                 |
| public Real realValue()                                                                      |                                                 |
| public int startColumn()                                                                     |                                                 |
| public str string()                                                                          |                                                 |
| public str strValue()                                                                        |                                                 |
| public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos) |                                                 |
| public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)      |                                                 |
| public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)      |                                                 |
| public void new(str source)                                                                  | Object クラスの新しいインスタンスを初期化します。 |
| public void comment(str text, int startLine, int startPos, int endLine, int endPos)          |                                                 |

### <a name="method-col"></a>メソッド col

    public int col()

#### <a name="return-value"></a>戻り値

### <a name="method-datevalue"></a>メソッド dateValue

    public Date dateValue()

#### <a name="return-value"></a>戻り値

### <a name="method-firstsymbol"></a>メソッド firstSymbol

    public int firstSymbol()

#### <a name="return-value"></a>戻り値

### <a name="method-int64value"></a>メソッド int64Value

    public Int64 int64Value()

#### <a name="return-value"></a>戻り値

### <a name="method-intvalue"></a>メソッド intValue

    public int intValue()

#### <a name="return-value"></a>戻り値

### <a name="method-line"></a>メソッド line

    public int line()

#### <a name="return-value"></a>戻り値

### <a name="method-nextsymbol"></a>メソッド nextSymbol

    public int nextSymbol()

#### <a name="return-value"></a>戻り値

### <a name="method-realvalue"></a>メソッド realValue

    public Real realValue()

#### <a name="return-value"></a>戻り値

### <a name="method-startcolumn"></a>メソッド startColumn

    public int startColumn()

#### <a name="return-value"></a>戻り値

### <a name="method-string"></a>メソッド string

    public str string()

#### <a name="return-value"></a>戻り値

### <a name="method-strvalue"></a>メソッド strValue

    public str strValue()

#### <a name="return-value"></a>戻り値

### <a name="method-localmacrodefine"></a>メソッド localMacroDefine

    public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

### <a name="method-linecomment"></a>メソッド lineComment

    public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

### <a name="method-macrodefine"></a>メソッド macroDefine

    public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str source)

#### <a name="parameters"></a>パラメーター

ソース  

### <a name="method-comment"></a>メソッド comment

    public void comment(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a>パラメーター

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

## <a name="class-searchparm"></a>クラス SearchParm
    class SearchParm extends Object

SearchParm クラスは、カーネルと sysTreeSearch クラス間のインターフェイスとして機能し、アプリケーション オブジェクト ツリー (AOT) で検索できるようにします。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                          | 説明 |
|-------------------------------------------------|-------------|
| public str nodeName(\[str name\])               |             |
| public int nodeType(\[int type\])               |             |
| public str nodeTypeArray()                      |             |
| public str propertyName(\[str name\])           |             |
| public str propertyValue(\[str value\])         |             |
| public str replaceString(\[str replaceString\]) |             |
| public int searchFlag(\[int flag\])             |             |
| public str searchString(\[str searchString\])   |             |
| public int searchType(\[int type\])             |             |
| public boolean startSearch()                    |             |
| public TreeNode topNode(\[TreeNode node\])      |             |
| public str topNodeName(\[str name\])            |             |
| public int topNodeType(\[int type\])            |             |
| public void preSearch()                         |             |
| public void killSearch()                        |             |

### <a name="method-nodename"></a>メソッド nodeName

    public str nodeName([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-nodetype"></a>メソッド nodeType

    public int nodeType([int type])

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-nodetypearray"></a>メソッド nodeTypeArray

    public str nodeTypeArray()

#### <a name="return-value"></a>戻り値

### <a name="method-propertyname"></a>メソッド propertyName

    public str propertyName([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-propertyvalue"></a>メソッド propertyValue

    public str propertyValue([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replacestring"></a>メソッド replaceString

    public str replaceString([str replaceString])

#### <a name="parameters"></a>パラメーター

replaceString  

#### <a name="return-value"></a>戻り値

### <a name="method-searchflag"></a>メソッド searchFlag

    public int searchFlag([int flag])

#### <a name="parameters"></a>パラメーター

flag  

#### <a name="return-value"></a>戻り値

### <a name="method-searchstring"></a>メソッド searchString

    public str searchString([str searchString])

#### <a name="parameters"></a>パラメーター

searchString  

#### <a name="return-value"></a>戻り値

### <a name="method-searchtype"></a>メソッド searchType

    public int searchType([int type])

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-startsearch"></a>メソッド startSearch

    public boolean startSearch()

#### <a name="return-value"></a>戻り値

### <a name="method-topnode"></a>メソッド topNode

    public TreeNode topNode([TreeNode node])

#### <a name="parameters"></a>パラメーター

node  

#### <a name="return-value"></a>戻り値

### <a name="method-topnodename"></a>メソッド topNodeName

    public str topNodeName([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-topnodetype"></a>メソッド topNodeType

    public int topNodeType([int type])

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-presearch"></a>メソッド preSearch

    public void preSearch()

### <a name="method-killsearch"></a>メソッド killSearch

    public void killSearch()

## <a name="class-securenode"></a>クラス SecureNode
    class SecureNode extends TreeNode

SecureNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                          | 説明                                                             |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| public boolean checkAccessRights()                                              |                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])        | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。     |
| public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\]) |                                                                         |
| public boolean extendedDataSecurity(\[boolean value\])                          |                                                                         |
| public boolean isWeb()                                                          |                                                                         |
| public int neededAccessLevel(\[int value\])                                     | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。 |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                       |                                                                         |
| public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])     |                                                                         |

### <a name="method-checkaccessrights"></a>メソッド checkAccessRights

    public boolean checkAccessRights()

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-countryconfigurationkey"></a>メソッド countryConfigurationkey

    public ConfigurationKeyId countryConfigurationkey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatasecurity"></a>メソッド extendedDataSecurity

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-isweb"></a>メソッド isWeb

    public boolean isWeb()

#### <a name="return-value"></a>戻り値

### <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

    public int neededAccessLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

neededAccessLevel プロパティの現在の値。

#### <a name="remarks"></a>備考

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess。
-   AccessType::View。
-   AccessType::Edit。
-   AccessType::Add。
-   AccessType::Delete。

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webconfigurationkey"></a>メソッド webConfigurationkey

    public ConfigurationKeyId webConfigurationkey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-securitycontext"></a>クラス SecurityContext
    class SecurityContext extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                | 説明 |
|-------------------------------------------------------------------------------------------------------|-------------|
| public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\]) |             |
| ::public static SecurityContext current()                                                             |             |
| ::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)  |             |
| public boolean equal(SecurityContext context)                                                         |             |
| public SecurableType securableType()                                                                  |             |
| public str securableName()                                                                            |             |
| public str securableChildName()                                                                       |             |
| public void push()                                                                                    |             |
| ::public static void pop()                                                                            |             |
| private void new()                                                                                    |             |

### <a name="method-istableoperationallowed"></a>メソッド isTableOperationAllowed

    public boolean isTableOperationAllowed(int tableId, StatementType operation, [DataAreaId dataArea])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

工程  

<!-- -->

dataArea  

#### <a name="return-value"></a>戻り値

### <a name="method-current"></a>メソッド current

    public static SecurityContext current()

#### <a name="return-value"></a>戻り値

### <a name="method-constructfromentrypoint"></a>メソッド constructFromEntryPoint

    public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

名前  

<!-- -->

childName  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

    public boolean equal(SecurityContext context)

#### <a name="parameters"></a>パラメーター

context  

#### <a name="return-value"></a>戻り値

### <a name="method-securabletype"></a>メソッド securableType

    public SecurableType securableType()

#### <a name="return-value"></a>戻り値

### <a name="method-securablename"></a>メソッド securableName

    public str securableName()

#### <a name="return-value"></a>戻り値

### <a name="method-securablechildname"></a>メソッド securableChildName

    public str securableChildName()

#### <a name="return-value"></a>戻り値

### <a name="method-push"></a>メソッド push

    public void push()

### <a name="method-pop"></a>メソッド pop

    public static void pop()

### <a name="method-new"></a>メソッド new

    private void new()

## <a name="class-securitypolicy"></a>クラス SecurityPolicy
    class SecurityPolicy extends Object

SecurityPolicy クラスには、セキュリティ ポリシーに関する情報が含まれます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                 | 説明                                             |
|------------------------------------------------------------------------|---------------------------------------------------------|
| ::public static void synchronizeAllPolicies()                          |                                                         |
| ::public static void synchronizePolicy(UtilElementName securityPolicy) |                                                         |
| public void new()                                                      | SecurityPolicy クラスの新しいインスタンスを初期化します。 |

### <a name="method-synchronizeallpolicies"></a>メソッド synchronizeAllPolicies

    public static void synchronizeAllPolicies()

### <a name="method-synchronizepolicy"></a>メソッド synchronizePolicy

    public static void synchronizePolicy(UtilElementName securityPolicy)

#### <a name="parameters"></a>パラメーター

securityPolicy  

### <a name="method-new"></a>メソッド new

SecurityPolicy クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-securityrights"></a>クラス SecurityRights
    class SecurityRights extends Object

SecurityRights クラスには、セキュリティの権利とアクセス許可の管理に関する情報が含まれます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                 | 説明                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| public boolean hasDataServiceAccess(SecurableName name, StatementType operation, \[SecurableChildName fieldName\])                                                                     |                                                                        |
| public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)                                                                  |                                                                        |
| public AccessRight dataManagementAccessRight(SecurableName dataEntityName, \[SecurableChildName fieldName\])                                                                           |                                                                        |
| public str listDataServiceAccess(SecurableName name, \[SecurableChildName context\])                                                                                                   |                                                                        |
| public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\]) | テーブルのフィールドのアクセス権を取得します。                |
| public AccessRight formControlAccessRight(FormName form, UtilElementName control, \[Common record\], \[DataAreaId dataArea\])                                                          | フォーム コントロールのアクセス権を取得します。                      |
| public container getSelectableCompanies()                                                                                                                                              |                                                                        |
| public boolean hasMenuAccess(MenuName menu, \[boolean isWebMenu\])                                                                                                                     | ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。              |
| public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, \[Common record\], \[DataAreaId dataArea\])                                                                | ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。         |
| public boolean SysObsoleteAttribute(ClassName class, MethodName method)                                                                                                                |                                                                        |
| public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)                                                                                           | ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。 |
| public boolean isDeveloper()                                                                                                                                                           |                                                                        |
| public boolean isSystemAdministrator()                                                                                                                                                 | 現在のユーザーがシステム管理者であるかどうかを確認します。             |
| public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, \[DataAreaId dataArea\])                                                                             | メニュー項目のアクセス権を取得します。                         |
| public AccessRight tableAccessRight(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])                      | テーブルのアクセス権を取得します。                             |
| public SecurityTableRights tableFieldAccessRights(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])        | テーブルのフィールド アクセス権を取得します。                       |
| public Set variableAccessFields(TableName tableName, \[AccessRight targetAccess\], \[DataAreaId dataArea\])                                                                            | 一連のテーブル フィールド ID を取得します。                                |
| public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)                                                                                                  | Web コンテンツ項目のアクセス権を取得します。                  |
| ::public static SecurityRights construct()                                                                                                                                             | 現在のユーザーの新しいセキュリティ権限インスタンスを作成します。           |
| ::public static SecurityRights newUser(UserId user)                                                                                                                                    | 特定のユーザーの新しいセキュリティ権限インスタンスを作成します。         |
| private void new()                                                                                                                                                                     | SecurityRights クラスの新しいインスタンスを初期化します。                |
| public void populateSelectableCompanies()                                                                                                                                              | 選択できる会社を取得します。                                    |

### <a name="method-hasdataserviceaccess"></a>メソッド hasDataServiceAccess

    public boolean hasDataServiceAccess(SecurableName name, StatementType operation, [SecurableChildName fieldName])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

工程  

<!-- -->

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-hasdataservicemethodaccess"></a>メソッド hasDataServiceMethodAccess

    public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

工程  

<!-- -->

methodName  

#### <a name="return-value"></a>戻り値

### <a name="method-datamanagementaccessright"></a>メソッド dataManagementAccessRight

    public AccessRight dataManagementAccessRight(SecurableName dataEntityName, [SecurableChildName fieldName])

#### <a name="parameters"></a>パラメーター

dataEntityName  

<!-- -->

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-listdataserviceaccess"></a>メソッド listDataServiceAccess

    public str listDataServiceAccess(SecurableName name, [SecurableChildName context])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

context  

#### <a name="return-value"></a>戻り値

### <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

テーブルのフィールドのアクセス権を取得します。

    public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a>パラメーター

tableName  

<!-- -->

fieldName  

<!-- -->

記録  

<!-- -->

dataArea  

<!-- -->

includeDerived  

<!-- -->

autoAuthzMode  

#### <a name="return-value"></a>戻り値

テーブルのフィールドの AccesRight インスタンス。

### <a name="method-formcontrolaccessright"></a>メソッド formControlAccessRight

フォーム コントロールのアクセス権を取得します。

    public AccessRight formControlAccessRight(FormName form, UtilElementName control, [Common record], [DataAreaId dataArea])

#### <a name="parameters"></a>パラメーター

フォーム  

<!-- -->

control  

<!-- -->

記録  

<!-- -->

dataArea  

#### <a name="return-value"></a>戻り値

フォーム コントロールの AccesRight インスタンス。

### <a name="method-getselectablecompanies"></a>メソッド getSelectableCompanies

    public container getSelectableCompanies()

#### <a name="return-value"></a>戻り値

### <a name="method-hasmenuaccess"></a>メソッド hasMenuAccess

ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。

    public boolean hasMenuAccess(MenuName menu, [boolean isWebMenu])

#### <a name="parameters"></a>パラメーター

メニュー  

<!-- -->

isWebMenu  

#### <a name="return-value"></a>戻り値

ユーザーがメニューへのアクセス権を持つ場合は true。それ以外の場合は、false。

### <a name="method-hasmenuitemaccess"></a>メソッド hasMenuItemAccess

ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。

    public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, [Common record], [DataAreaId dataArea])

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

menuItem  

<!-- -->

記録  

<!-- -->

dataArea  

#### <a name="return-value"></a>戻り値

ユーザーがメニュー項目へのアクセス権を持つ場合は true。それ以外の場合は、false。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(ClassName class, MethodName method)

#### <a name="parameters"></a>パラメーター

クラス  

<!-- -->

メソッド  

#### <a name="return-value"></a>戻り値

### <a name="method-hasserviceoperationaccess"></a>メソッド hasServiceOperationAccess

ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。

    public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)

#### <a name="parameters"></a>パラメーター

サービス  

<!-- -->

工程  

#### <a name="return-value"></a>戻り値

ユーザーがサービス操作へのアクセス権を持つ場合は true。それ以外の場合は、false。

### <a name="method-isdeveloper"></a>メソッド isDeveloper

    public boolean isDeveloper()

#### <a name="return-value"></a>戻り値

### <a name="method-issystemadministrator"></a>メソッド isSystemAdministrator

現在のユーザーがシステム管理者であるかどうかを確認します。

    public boolean isSystemAdministrator()

#### <a name="return-value"></a>戻り値

現在のユーザーがシステム管理者である場合は true。それ以外の場合は、false。

### <a name="method-menuitemaccessright"></a>メソッド menuItemAccessRight

メニュー項目のアクセス権を取得します。

    public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, [DataAreaId dataArea])

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

menuItem  

<!-- -->

dataArea  

#### <a name="return-value"></a>戻り値

項目の AccesRight インスタンス。

### <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を取得します。

    public AccessRight tableAccessRight(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a>パラメーター

tableName  

<!-- -->

記録  

<!-- -->

dataArea  

<!-- -->

includeDerived  

<!-- -->

autoAuthzMode  

#### <a name="return-value"></a>戻り値

テーブルの AccesRight インスタンス。

### <a name="method-tablefieldaccessrights"></a>メソッド tableFieldAccessRights

テーブルのフィールド アクセス権を取得します。

    public SecurityTableRights tableFieldAccessRights(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a>パラメーター

tableName  

<!-- -->

記録  

<!-- -->

dataArea  

<!-- -->

includeDerived  

<!-- -->

autoAuthzMode  

#### <a name="return-value"></a>戻り値

テーブルの SecurityTableRights インスタンス。

### <a name="method-variableaccessfields"></a>メソッド variableAccessFields

一連のテーブル フィールド ID を取得します。

    public Set variableAccessFields(TableName tableName, [AccessRight targetAccess], [DataAreaId dataArea])

#### <a name="parameters"></a>パラメーター

tableName  

<!-- -->

targetAccess  

<!-- -->

dataArea  

#### <a name="return-value"></a>戻り値

一連のテーブル フィールド ID。

### <a name="method-webcontentaccessright"></a>メソッド webContentAccessRight

Web コンテンツ項目のアクセス権を取得します。

    public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

名前  

#### <a name="return-value"></a>戻り値

項目の AccesRight インスタンス。

### <a name="method-construct"></a>メソッド construct

現在のユーザーの新しいセキュリティ権限インスタンスを作成します。

    public static SecurityRights construct()

#### <a name="return-value"></a>戻り値

作成された SecurityRights インスタンスです。

### <a name="method-newuser"></a>メソッド newUser

特定のユーザーの新しいセキュリティ権限インスタンスを作成します。

    public static SecurityRights newUser(UserId user)

#### <a name="parameters"></a>パラメーター

ユーザー  

#### <a name="return-value"></a>戻り値

作成された SecurityRights インスタンスです。

### <a name="method-new"></a>メソッド new

SecurityRights クラスの新しいインスタンスを初期化します。

    private void new()

### <a name="method-populateselectablecompanies"></a>メソッド populateSelectableCompanies

選択できる会社を取得します。

    public void populateSelectableCompanies()

## <a name="class-securityskipflush"></a>クラス SecuritySkipFlush
    class SecuritySkipFlush extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法              | 説明                                                |
|---------------------|------------------------------------------------------------|
| public void clear() |                                                            |
| public void new()   | SecuritySkipFlush クラスの新しいインスタンスを初期化します。 |
| public void set()   |                                                            |

### <a name="method-clear"></a>メソッド clear

    public void clear()

### <a name="method-new"></a>メソッド new

SecuritySkipFlush クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-set"></a>メソッド set

    public void set()

## <a name="class-securitytablerights"></a>クラス SecurityTableRights
    class SecurityTableRights extends Object

SecurityTableRights クラスには、テーブル セキュリティ権限に関する情報が含まれます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                   | 説明                                               |
|----------------------------------------------------------|-----------------------------------------------------------|
| public AccessRight fieldAccessRight(FieldName fieldName) | テーブルのフィールドのアクセス権を取得します。        |
| public AccessRight tableAccessRight()                    | テーブルのアクセス権を取得します。                     |
| private void new()                                       | SecurityTableRights クラスのインスタンスを初期化します。 |

### <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

テーブルのフィールドのアクセス権を取得します。

    public AccessRight fieldAccessRight(FieldName fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

フィールドの AccesRight インスタンス。

### <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を取得します。

    public AccessRight tableAccessRight()

#### <a name="return-value"></a>戻り値

テーブルの AccesRight インスタンス。

### <a name="method-new"></a>メソッド new

SecurityTableRights クラスのインスタンスを初期化します。

    private void new()

## <a name="class-securityutil"></a>クラス SecurityUtil
    class SecurityUtil extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                                                                 | 説明                                                                |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| ::public static boolean isImplicitFlushMode()                                                                          | 暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。                   |
| ::public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName) | セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。          |
| ::public static container getRolePermissions(Int64 roleID)                                                             | セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。          |
| ::public static boolean sysAdminMode(\[boolean active\])                                                               | セキュリティ管理者モードを取得および設定します。                             |
| ::public static void refreshRolePermissions(Int64 roleID)                                                              | セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。 |
| ::public static void runSecondPassAutoInference()                                                                      | 2 つ目の合格自動推定が実行されます。                                       |
| ::public static void flushPermissions()                                                                                | アクセス許可をフラッシュします。                                                   |
| public void new()                                                                                                      | SecurityUtil クラスの新しいインスタンスを初期化します。                      |
| ::public static void flushAll()                                                                                        |                                                                            |

### <a name="method-isimplicitflushmode"></a>メソッド isImplicitFlushMode

暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。

    public static boolean isImplicitFlushMode()

#### <a name="return-value"></a>戻り値

ブール値。

### <a name="method-getroleeffectiveaccess"></a>メソッド getRoleEffectiveAccess

セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。

    public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)

#### <a name="parameters"></a>パラメーター

roleID  

<!-- -->

secObjectName  

<!-- -->

secObjectType  

<!-- -->

secObjectChildName  

#### <a name="return-value"></a>戻り値

有効なアクセス値。

### <a name="method-getrolepermissions"></a>メソッド getRolePermissions

セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。

    public static container getRolePermissions(Int64 roleID)

#### <a name="parameters"></a>パラメーター

roleID  
ロール ID。

#### <a name="return-value"></a>戻り値

セキュリティ保護可能なオブジェクトのコンテナーと、有効なアクセスです。

### <a name="method-sysadminmode"></a>メソッド sysAdminMode

セキュリティ管理者モードを取得および設定します。

    public static boolean sysAdminMode([boolean active])

#### <a name="parameters"></a>パラメーター

有効  
ブール値。

#### <a name="return-value"></a>戻り値

セキュリティ管理者モードの古い状態。

### <a name="method-refreshrolepermissions"></a>メソッド refreshRolePermissions

セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。

    public static void refreshRolePermissions(Int64 roleID)

#### <a name="parameters"></a>パラメーター

roleID  

### <a name="method-runsecondpassautoinference"></a>メソッド runSecondPassAutoInference

2 つ目の合格自動推定が実行されます。

    public static void runSecondPassAutoInference()

### <a name="method-flushpermissions"></a>メソッド flushPermissions

アクセス許可をフラッシュします。

    public static void flushPermissions()

### <a name="method-new"></a>メソッド new

SecurityUtil クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-flushall"></a>メソッド flushAll

    public static void flushAll()

## <a name="class-segmententeredeventargs"></a>クラス SegmentEnteredEventArgs
    class SegmentEnteredEventArgs extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                   | 説明 |
|----------------------------------------------------------|-------------|
| public boolean isAllValuesEnabled(\[boolean enabled\])   |             |
| public boolean isMRUEnabled(\[boolean enabled\])         |             |
| public boolean isValidValuesEnabled(\[boolean enabled\]) |             |

### <a name="method-isallvaluesenabled"></a>メソッド isAllValuesEnabled

    public boolean isAllValuesEnabled([boolean enabled])

#### <a name="parameters"></a>パラメーター

有効  

#### <a name="return-value"></a>戻り値

### <a name="method-ismruenabled"></a>メソッド isMRUEnabled

    public boolean isMRUEnabled([boolean enabled])

#### <a name="parameters"></a>パラメーター

有効  

#### <a name="return-value"></a>戻り値

### <a name="method-isvalidvaluesenabled"></a>メソッド isValidValuesEnabled

    public boolean isValidValuesEnabled([boolean enabled])

#### <a name="parameters"></a>パラメーター

有効  

#### <a name="return-value"></a>戻り値

## <a name="class-segmentvaluechangedeventargs"></a>クラス SegmentValueChangedEventArgs
    class SegmentValueChangedEventArgs extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                       | 説明 |
|------------------------------|-------------|
| public FormSegment segment() |             |
| public AnyType selectedTag() |             |

### <a name="method-segment"></a>メソッド segment

    public FormSegment segment()

#### <a name="return-value"></a>戻り値

### <a name="method-selectedtag"></a>メソッド selectedTag

    public AnyType selectedTag()

#### <a name="return-value"></a>戻り値

## <a name="class-sequence"></a>クラスの順序
    class Sequence extends Object

Sequence クラスを使用すると、通常は何らかの順序または伝票番号の生成のために、主要なトランザクション スコープ外でトランザクションを実行できます。

### <a name="remarks"></a>備考

接続には、メインユーザー接続、補助システム接続、ユーザー接続の 3 種類があります。 最初のものはアプリケーション ロジック用に使用されます。 2 番目は、内部シーケンス番号の生成 (特に組み込みフィールド RecId) に使用されます。 3 番目はアプリケーションが別々の接続を維持するために使用されます。 このクラスは、番号生成のための補助システム接続へのインターフェイスを提供します。 ただし、これはアプリケーションの使用するメソッドまたは柔軟性、さらにカーネルの順序番号の生成で同時実行の問題を回避するため、UserConnection クラスを使用する方がより良いソリューションになる可能性があります。

### <a name="examples"></a>例

    static void example() 
    { 
        Sequence S = new Sequence("mySequence",1,100,10000); 
        print S.nextval(10);           // 100 in current company (the subkey) 
        print S.nextval(10);           // 110 in current company (the subkey) 
        print S.nextval(1,"MMM");      // 100 in subkey "MMM" 
        print S.nextval(1,"MMM");      // 101 in subkey "MMM" 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                        | 説明                                                                                 |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| public Int64 currval(\[str Subkey1\], \[int Subkey2\])                                                        | カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。 |
| public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])                                       | シーケンスから次の順序番号を返し、カウンター値を増分します。   |
| public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\]) | Object クラスの新しいインスタンスを初期化します。                                             |

### <a name="method-currval"></a>メソッド currval

カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。

    public Int64 currval([str Subkey1], [int Subkey2])

#### <a name="parameters"></a>パラメーター

Subkey1  

<!-- -->

Subkey2  

#### <a name="return-value"></a>戻り値

シーケンスの現在のシーケンス番号。

### <a name="method-nextval"></a>メソッド nextval

シーケンスから次の順序番号を返し、カウンター値を増分します。

    public Int64 nextval(Int64 Increment, [str Subkey1], [int Subkey2])

#### <a name="parameters"></a>パラメーター

増分  

<!-- -->

Subkey1  

<!-- -->

Subkey2  

#### <a name="return-value"></a>戻り値

利用可能な次の順序番号。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, [boolean Cycle], [Int64 CacheSize])

#### <a name="parameters"></a>パラメーター

氏名  

<!-- -->

ID  

<!-- -->

InitialValue  

<!-- -->

MaxValue  

<!-- -->

サイクル  

<!-- -->

CacheSize  

## <a name="class-set"></a>クラスのセット
    class Set extends Object

Set クラスは、格納されている要素の値が固有であり、自動的に並べ替えられるデータに応じたキー値として機能するコレクションからデータを格納して取得ために使用されます。

### <a name="remarks"></a>備考

値は任意の X++ 型にできます。 セット内のすべての値には同じタイプが必要です。 セットにすでに保存されている値が追加されると、その値は無視され、セット内の要素の数を増加させません。 セットに格納された値は、SetEnumerator 型のオブジェクトを使用してスキャンできます。 セットのコンテンツは、要素の効率的な検索を容易にする方法で格納されます。

### <a name="examples"></a>例

次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。 見つかった場合は、yesConfigs セットから削除されます。

    Set             noConfigs; 
    Set             yesConfigs; 
    ConfigId        configId; 
    SetEnumerator   se; 
    ; 
    se = noConfigs.getEnumerator(); 
    while (se.moveNext()) 
    { 
        configId    = se.current(); 
        if (yesConfigs.in(configId)) 
        { 
            yesConfigs.remove(configId); 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                               | 説明                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public boolean add(AnyType arg)                      | セットに要素を追加します。                                                                                                       |
| public str definitionString()                        | セット内のすべての要素のタイプの説明を返します。                                                                     |
| public int elements()                                | セット内の要素の数を返します。                                                                                        |
| public boolean empty()                               | セットが空であるかどうかを判定します。                                                                                              |
| public boolean equal(Set set)                        | セットが現在のセットと同一かどうかを判定します。                                                                         |
| public SetEnumerator getEnumerator()                 | セット内のスキャンを可能にする、セットの列挙子を作成します。                                                            |
| public boolean in(AnyType arg)                       | 指定された要素がセットのメンバーであるかどうかを判定します。                                                                    |
| public container pack()                              | Set クラスの現在のインスタンスをシリアル化します。                                                                                 |
| public boolean remove(AnyType arg)                   | セットから要素を削除します。                                                                                                  |
| public str toString()                                | 設定の内容を説明する文字列を返します。                                                                              |
| public Types typeId()                                | セット内の値のタイプを返します。                                                                                        |
| public str xml(\[int indent\])                       | 現在のオブジェクトを表す XML 文字列を返します。                                                                         |
| ::public static Set create(container container)      | 以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。                                               |
| ::public static Set createFromXML(Object xmlnode)    |                                                                                                                                   |
| ::public static Set difference(Set set1, Set set2)   | set2 で検出されない set1 の要素を含むセットを計算および取得します。                                    |
| ::public static Set intersection(Set set1, Set set2) | 2 つのセット内で検出される同一の値を計算して返します。                                                                    |
| ::public static Set union(Set set1, Set set2)        | 指定された 2 つのセットの和集合を計算および取得します これは、少なくとも 1 つのセットにある値を含むセットです。 |
| public void new(Types Type)                          | 指定した型の要素を含めることができるセットを作成します。                                                                    |

### <a name="method-add"></a>メソッド add

セットに要素を追加します。

    public boolean add(AnyType arg)

#### <a name="parameters"></a>パラメーター

arg  
セットに追加する要素。

#### <a name="return-value"></a>戻り値

要素がセットに追加された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

セットに追加される要素は、セットの作成時にセットに割り当てられたタイプと同じタイプでなければなりません。 既にセットに存在する場合、要素は追加されません。

#### <a name="examples"></a>例

次の例では、セットを作成し、いくつかの整数を追加してから、セットの内容を出力します。

    { 
        // Create a set of integers 
        Set is = new Set (Types::Integer); 
        int i; 
        ;  
        // Add values 0 to 9 to the set 
        for (i = 0; i < 10; i++) 
        { 
            is.add(i); 
        } 
        print is.toString(); 
        pause; 
    }

### <a name="method-definitionstring"></a>メソッド definitionString

セット内のすべての要素のタイプの説明を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

設定の定義を含む文字列。

#### <a name="remarks"></a>備考

セット内の値の一覧を印刷するには、Set.toString を使用します。

#### <a name="examples"></a>例

次の例では、整数のセットを作成します。 definitionString メソッドを使用して、セットの説明を出力します。

    { 
        // Declare a set of integers 
        Set is = new Set (Types::Integer);  
        ; 
        // Add some integers to the set 
        print is.add(1); 
        print is.add(2); 
        print is.add(1); 
        // Print a description of the set 
        print is.definitionString(); 
        // Print a description of the set elements 
        print is.toString(); 
        pause; 
    }

### <a name="method-elements"></a>メソッド elements

セット内の要素の数を返します。

    public int elements()

#### <a name="return-value"></a>戻り値

セット内の要素の数。

#### <a name="examples"></a>例

次の例では、セットの内容をコンテナーにパックします。 要素メソッドは、セットに任意のコンテンツが含まれているかどうかをテストするために使用されます。 コンテンツがない場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) コンテナーが返されます。

    public static container intSet2Con(Set _intSet) 
    { 
        SetEnumerator se; 
        container     intCon; 
        ; 
        if (!_intSet || !_intSet.elements()) 
        { 
            return conNull(); 
        } 
        se = _intSet.getEnumerator(); 
        while (se.moveNext()) 
        { 
            intCon += se.current(); 
        } 
        return intCon; 
    }

### <a name="method-empty"></a>メソッド empty

セットが空であるかどうかを判定します。

    public boolean empty()

#### <a name="return-value"></a>戻り値

セットが空の場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

これは、(elements() == 0) と等価です。

#### <a name="examples"></a>例

次の例では、セットに要素があるかどうかをテストします。

    { 
        Set mySet = new Set(Types::Integer); 
        ; 
        // ... 
        if (mySet.empty()) 
        { 
            print "There are no values in the set"; 
        } 
    }

### <a name="method-equal"></a>メソッド equal

セットが現在のセットと同一かどうかを判定します。

    public boolean equal(Set set)

#### <a name="parameters"></a>パラメーター

set  
現在のセットと比較されるセット。

#### <a name="return-value"></a>戻り値

そのセットが現在のセットと同じである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

2 つのセットが等しくなるためには、それらには同じタイプおよび同じ数の要素があり、すべての要素は同じである必要があります。

#### <a name="examples"></a>例

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加し、それらを比較してセットが同じかどうかを確認します。

    { 
        Set is1 = new Set (Types::Integer); 
        Set is2 = new Set (Types::Integer); 
        ; 
        is1.add(1); 
        is1.add(2); 
        is1.add(3); 
        is2.add(2); 
        is2.add(4); 
        if (is1.equal(is2)) 
        { 
            print "The sets are equal"; 
            pause; 
        } 
        else 
        { 
             print "The sets are not equal"; 
             pause; 
         } 
    }

### <a name="method-getenumerator"></a>メソッド getEnumerator

セット内のスキャンを可能にする、セットの列挙子を作成します。

    public SetEnumerator getEnumerator()

#### <a name="return-value"></a>戻り値

現在のセットの SetEnumerator オブジェクト。

#### <a name="examples"></a>例

次の例では、セットの内容をコンテナーにパックします。 getEnumerator メソッドは、セットの列挙子を作成するために使用されます。 したがって、セット内の要素を横断してコンテナーに追加することができます。

    public static container intSet2Con(Set _intSet) 
    { 
        SetEnumerator se; 
        container     intCon; 
        ; 
        if (!_intSet || !_intSet.elements()) 
        { 
            return conNull(); 
        } 
        se = _intSet.getEnumerator(); 
        while (se.moveNext()) 
        { 
            intCon += se.current(); 
        } 
        return intCon; 
    }

### <a name="method-in"></a>メソッド in

指定された要素がセットのメンバーであるかどうかを判定します。

    public boolean in(AnyType arg)

#### <a name="parameters"></a>パラメーター

arg  
チェックする要素。 要素のタイプは、セットの指定されたタイプと同じである必要があります。

#### <a name="return-value"></a>戻り値

指定した要素がセット内で見つかる場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、in メソッドが false を返す場合、バージョン コントロール システム内の特定の変更リストの内容を読み込みます。 changeSet セットには、コンテンツが既にロードされている変更リスト番号のリストが含まれています。

    public void pageActivated() 
    { 
        SysVersionControlTmpItem contentsAddition; 
        if (!changeSet.in(changes.ChangeNumber)) 
        { 
            startLengthyOperation(); 
            contentsAddition = versioncontrol.getChangeNumberContents( 
                changes.ChangeNumber); 
            while select contentsAddition 
            { 
                contentsItem.data(contentsAddition); 
                contentsItem.insert(); 
            } 
            contents_ds.executeQuery(); 
            changeSet.add(changes.ChangeNumber); 
        } 
        super(); 
    }

### <a name="method-pack"></a>メソッド pack

Set クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

Set クラスの現在のインスタンスを含むコンテナーです。

#### <a name="remarks"></a>備考

このメソッドで作成されたコンテナーには、セットの最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号
-   セット要素のデータ型を識別する整数
-   セット内の要素の数。

キーまたは値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを作成します。 Set::create method を使用することにより、結果のコンテナから新しいセットを作成することができます。

#### <a name="examples"></a>例

次の例では、10 個の整数のセットを作成し、それをコンテナーにパックし、元の内容と同じ内容の新しいセットを作成します。

    { 
        Set is1, is = new Set (Types::Integer); 
        int i; 
        container packedSet; 
        ; 
        // Create a set containing the first 10 integers. 
        for (i = 1; i <= 10; i++) 
        { 
            is.add(i); 
        } 
        // Pack it down in a container... 
        packedSet = is.pack(); 
        // ... and restore it 
        is1 = Set::create(packedSet); 
        print is1.toString(); 
        pause; 
    }

### <a name="method-remove"></a>メソッド remove

セットから要素を削除します。

    public boolean remove(AnyType arg)

#### <a name="parameters"></a>パラメーター

arg  
削除する要素。

#### <a name="return-value"></a>戻り値

要素が見つかり削除された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。 見つかった場合は、yesConfigs セットから削除されます。

    Set             noConfigs; 
    Set             yesConfigs; 
    ConfigId        configId; 
    SetEnumerator   se; 
    ; 
    se = noConfigs.getEnumerator(); 
    while (se.moveNext()) 
    { 
        configId    = se.current(); 
        if (yesConfigs.in(configId)) 
        { 
            yesConfigs.remove(configId); 
        } 
    }

### <a name="method-tostring"></a>メソッド toString

設定の内容を説明する文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

設定の内容を説明する文字列。

#### <a name="remarks"></a>備考

を使用して、セット内の単一要素の説明を取得します。

#### <a name="examples"></a>例

次の例では、文字列のセットを作成し、そのセットの説明とセット内容の説明を出力します。

    { 
        // Declare a set of strings 
        Set names = new Set (Types::String); 
        ; 
        // Add some values to the set. 
        names.add("Peter"); 
        names.add("Paul"); 
        names.add("Mary"); 
        print names.definitionString(); 
        print names.toString(); 
        pause; 
    }

### <a name="method-typeid"></a>メソッド typeId

セット内の値のタイプを返します。

    public Types typeId()

#### <a name="return-value"></a>戻り値

セット内の値のタイプ。

#### <a name="remarks"></a>備考

構成要素のタイプは、そのセットが作成されるときに決定される。

#### <a name="examples"></a>例

次の例では、既存のセットと同じタイプの新しいセットをインスタンス化します。

    { 
        Set set1 = new Set(Types::Integer); 
        Set set2; 
       ; 
        set2 = new Set(set1.typeId()); 
        print set2.typeId(); 
        pause; 
    }

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
返された XML 文字列のインデントの量 (省略可能)。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-create"></a>メソッド create

以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。

    public static Set create(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  
パックされたセットを保持するコンテナー。

#### <a name="return-value"></a>戻り値

コンテナーに梱包されたものと同じセット。

#### <a name="remarks"></a>備考

値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

#### <a name="examples"></a>例

次の例では、セットを作成し、それをコンテナーにパックします。 次に、create メソッドを使用してコンテナーを展開し、元のセットと同じセットを作成します。

    { 
        Set is1, is = new Set (Types::Integer); 
        int i; 
        container packedSet; 
        ; 
        // Add 10 integers (0 - 9) to the set 
        for (i = 1; i <= 10; i++) 
        { 
            is.add(i); 
        } 
        // Pack the set into a container... 
        packedSet = is.pack(); 
        // ... and restore it 
        is1 = Set::create(packedSet); 
        print is1.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a>メソッド createFromXML

    public static Set createFromXML(Object xmlnode)

#### <a name="parameters"></a>パラメーター

xmlnode  

#### <a name="return-value"></a>戻り値

### <a name="method-difference"></a>メソッド difference

set2 で検出されない set1 の要素を含むセットを計算および取得します。

    public static Set difference(Set set1, Set set2)

#### <a name="parameters"></a>パラメーター

set1  
チェックするセット。

<!-- -->

set2  
チェックするセット。

#### <a name="return-value"></a>戻り値

set2 で検出されない set1 の要素を含むセット。

#### <a name="remarks"></a>備考

比較される 2 つのセットは、同じタイプでなければなりません。

#### <a name="examples"></a>例

次の例では、整数 1､2 および 3 を含む 1 つのセットと、整数 2 および 4 を含む 1 つのセットを作成します。 差異メソッドは、最初のセット内の 2 番目のセット (1 および 3) にない要素を含むセットを作成するために使用されます。

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::difference(is, is1); 
        // prints "{1, 3}" 
        print is2.toString(); 
        pause; 
    }

### <a name="method-intersection"></a>メソッド intersection

2 つのセット内で検出される同一の値を計算して返します。

    public static Set intersection(Set set1, Set set2)

#### <a name="parameters"></a>パラメーター

set1  
比較する 2 番目のセット。

<!-- -->

set2  
比較する 2 番目のセット。

#### <a name="return-value"></a>戻り値

両方のセットで検出された要素を含むセット。

#### <a name="examples"></a>例

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。 両方のセットに含まれている値の一覧を出力します。

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::intersection(is, is1); 
        // Prints "{2}" because 2 is contained in both is and is2. 
        print is2.toString(); 
    }

### <a name="method-union"></a>メソッド union

指定された 2 つのセットの和集合を計算および取得します これは、少なくとも 1 つのセットにある値を含むセットです。

    public static Set union(Set set1, Set set2)

#### <a name="parameters"></a>パラメーター

set1  
比較される 2 つのセットのうちの 2 番目のセット。

<!-- -->

set2  
比較される 2 つのセットのうちの 2 番目のセット。

#### <a name="return-value"></a>戻り値

set1 または set2 で検出された要素を含むセット。

#### <a name="remarks"></a>備考

比較される 2 つのセットは、同じタイプでなければなりません。

#### <a name="examples"></a>例

次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。 セットのいずれかに含まれるすべての値を含む新しいセットを作成します。

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::union(is, is1); 
        // Prints "{1, 2, 3, 4}". 
        print is2.toString(); 
        pause; 
    }

### <a name="method-new"></a>メソッド new

指定した型の要素を含めることができるセットを作成します。

    public void new(Types Type)

#### <a name="parameters"></a>パラメーター

種類  
セット内の要素のタイプ。

#### <a name="remarks"></a>備考

セットが作成された後、セットのタイプを変更することはできません。

#### <a name="examples"></a>例

次の例では、一連の整数とオブジェクトのセットを作成します。

    { 
        // Create a set of integers. 
        Set is = new Set (Types::Integer); 
        // Create a set of objects. 
        Set os = new Set (Types::Class); 
    }

## <a name="class-setenumerator"></a>クラス SetEnumerator
    class SetEnumerator extends Object

SetEnumerator クラスを使用すると、セット内の要素上を移動できます。

### <a name="remarks"></a>備考

セット列挙子は、セットの最初の要素の前に開始します。 セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。 ベスト プラクティスとしては、set.getEnumerator メソッドが呼び出されたときに、設定されている同じ層で列挙子が自動的に作成されるため、SetIterator クラスではなく、SetEnumerator クラスを使用します。 これにより、Caller from としてマークされたコードの潜在的な問題を回避できます。反復子とセットは別々の層に置くことができます。 さらに、セット列挙子はセット反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | 列挙子によりポイントされている値を取得します。                                                  |
| public str definitionString() | 列挙子の説明を返します。                                                                   |
| public boolean moveNext()     | 列挙子が有効なセット要素を示すかどうかを決定します。                                             |
| public str toString()         | 列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。 |
| public void reset()           | 列挙子をセットの先頭に移動します。                                                              |

### <a name="method-current"></a>メソッド current

列挙子によりポイントされている値を取得します。

    public AnyType current()

#### <a name="return-value"></a>戻り値

セット内で現在指定されている値。

#### <a name="remarks"></a>備考

戻り値のタイプは、セット内の項目のタイプによって決まります。 現在のメソッドを呼び出す前に、SetEnumerator.moveNext メソッドを呼び出す必要があります。

### <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

列挙子の説明を含む文字列。

#### <a name="remarks"></a>備考

たとえば、整数のセットの列挙子は、int セット列挙子を返します。

#### <a name="examples"></a>例

次の例では、セットとそのセットの列挙子を作成します。 definitionString メソッドを使用して、列挙子の説明を出力します。

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator enumerator; 
        int i; 
        // Add some elements to the set. 
       for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        print enumerator.definitionString(); 
        pause; 
    }

### <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なセット要素を示すかどうかを決定します。

    public boolean moveNext()

#### <a name="return-value"></a>戻り値

セット内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

セット列挙子は、セットの最初の要素の前に開始します。 セットの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

### <a name="method-tostring"></a>メソッド toString

列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。

    public str toString()

#### <a name="return-value"></a>戻り値

設定の現在の要素の説明を含む文字列。

#### <a name="examples"></a>例

次の例では、整数のセットを作成し、最初の要素と 2 番目の要素の内容をセットに出力します。

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator  enumerator; 
        int i; 
         // Add some elements to the set. 
        for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        // Go to the beginning of the enumerator. 
        enumerator.reset(); 
        // Go to the first element in the set. 
        enumerator.moveNext(); 
        // Print the first item in the set. 
        print enumerator.toString(); 
        pause; 
        enumerator.moveNext(); 
        // Print the second element in the set. 
        print enumerator.toString(); 
        pause; 
    }

### <a name="method-reset"></a>メソッド reset

列挙子をセットの先頭に移動します。

    public void reset()

#### <a name="remarks"></a>備考

reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。 セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、セット作成し、そのセットの列挙子を作成します。 reset メソッドを使用してセットの先頭に移動し、moveNext メソッドを使用してセットの最初の要素に移動します。

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator  enumerator; 
        int i; 
         // Add some elements to the set. 
        for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        // Go to beginning of enumerator. 
        enumerator.reset(); 
        // Go to the first element in the set. 
        enumerator.moveNext(); 
        // Print the first item in the set. 
        print enumerator.toString(); 
        pause; 
    }

## <a name="class-setiterator"></a>クラス SetIterator
    class SetIterator extends Object

SetIterator クラスを使用すると、セット内の要素を反復処理できます。

### <a name="remarks"></a>備考

セットの反復子は、反復処理する対象となるセットにポインターとして表示することができます。 繰り返しを開始し、より多くの要素が利用可能であるかどうかを決定し、さらに繰り返しによりポイントされる要素をフェッチする機能が利用可能です。 新しく作成されるセット反復子は、セットの最初の要素に配置されます。 繰り返し中に要素が出現する順序は、要素が挿入される順序ではなく、要素の順序によって定義されます。 より下位の値の要素は、上位の値の要素の前に表示されます。 型の通常の順序が使用されます。 構成要素がオブジェクトである場合、順序を指定するのにオブジェクトのアドレスが使用されます。 特定の注文が推測される可能性はありません。 オブジェクトのアドレスは、本来、一時的です。 SetIterator クラスではなく、そのクラスを使用することをお勧めします。 これにより、別の層の反復子を使用して 1 つの層のセットにアクセスする場合に問題を回避できます。 セット反復子および反復処理するセットは、同じクライアント/サーバー側にある必要があります。 SetIterator を使用し、コードが Called from としてマークされている場合、セットと反復子が別の層で終了しており、コードが失敗する可能性があります。 SetEnumerator を使用する場合、列挙子はセットと同じ層に自動的に作成されます。 また、セット内の次のアイテムに移動するには、反復子セットを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。 SetEnumerator を使用する場合、moveNext メソッドを呼び出すだけです。

### <a name="examples"></a>例

次の例では、整数のセットを作成し、4 つの値をその中に追加します。 各セット要素に関する情報を出力しているセットを通じて反復処理します。

        Set s1 = new Set (Types::Integer); 
        int theElement; 
        SetIterator it; 
        ; 
        // Add some elements. 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1); 
        // Start a traversal of the elements in the set. 
        it = new SetIterator(s1); 
        // Prints "(begin)[1]". 
        print it.toString(); 
        // The elements are fetched in the order: 1, 3, 4, 13. 
        while (it.more()) 
        { 
            theElement = it.value(); 
            print theElement; 
             // Fetch the next element. 
            it.next(); 
        } 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------|
| public str definitionString() | 反復子のタイプのテキスト表現を返します。                                          |
| public boolean more()         | 反復子が有効なセット要素を示すかどうかを決定します。                                           |
| public str toString()         | 反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。 |
| public AnyType value()        | 反復子がポイントしている値を取得します。                                                  |
| public void next()            | 次の要素に反復子を移動します。                                                                |
| public void new(Set set)      | セットに対する新しい反復子を作成します。                                                                      |
| public void begin()           | 反復子をセットの先頭に移動します。                                                            |
| public void delete()          | セットの反復子によってポイントされている要素を削除します。                                     |
| public void end()             | セットで最後の要素の後に反復子を移動します。                                                   |

### <a name="method-definitionstring"></a>メソッド definitionString

反復子のタイプのテキスト表現を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

反復子のタイプを示す文字列。

### <a name="method-more"></a>メソッド more

反復子が有効なセット要素を示すかどうかを決定します。

    public boolean more()

#### <a name="return-value"></a>戻り値

反復子が有効な要素を表す場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。 このメソッドは、反復子が有効な要素を指しているかどうかだけをチェックします。 セットにより多くの要素があるかどうかは確認されません。

#### <a name="examples"></a>例

次の例では、SetIterator.more メソッドを使用して、while ループを実行する前にセット内に要素があるかどうかを確認します。これにより、奇数要素がすべてセットから削除されます。

    { 
        Set iset = new Set (Types::Integer); 
        SetIterator it; 
        int i; 
        ; 
        for (i = 1; i <= 10; i++) 
        { 
            iset.add(i); 
        } 
        // Delete all odd elements 
        it = new SetIterator(iset); 
        while (it.more()) 
        { 
            if (it.value() mod 2 != 0) 
            { 
                // The value is odd. Delete and skip to next element. 
                it.delete(); 
            } 
            else 
            { 
                it.next(); 
            } 
        } 
        print iset.toString(); 
        pause; 
    }

### <a name="method-tostring"></a>メソッド toString

反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

設定の現在の要素のテキスト形式表記である文字列。

#### <a name="remarks"></a>備考

反復子がセット内の最初の要素を指している場合、その文字列には "(開始)\[値\]" という形式の指示が含まれます。反復子が要素を指していない場合(つまり、more() が false を返す場合)、返される文字列は "(終了)" になります。反復子が値を指す場合、文字列は "\[値\]" になります。値は要素値の文字列表現です。

#### <a name="examples"></a>例

次の例では、SetIterator.toString メソッドを使用して、反復子がセットのスキャンを開始する前にポイントする、そのセットの値の説明を出力します。

    { 
        Set s1 = new Set (Types::Integer); 
        int theElement; 
        SetIterator it; 
        // Add some elements 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1);  
        // Start a traversal of the elements in the set 
        it = new SetIterator(s1); 
        // The elements are fetched in the order: 1, 3, 4, 13 
        print it.toString(); // Prints "(begin)[1]" 
        while (it.more()) 
        { 
            theElement = it.value(); 
            print theElement; 
            // Fetch the next element 
            it.next(); 
        } 
        pause; 
    }

### <a name="method-value"></a>メソッド value

反復子がポイントしている値を取得します。

    public AnyType value()

#### <a name="return-value"></a>戻り値

反復子で示される値。

#### <a name="remarks"></a>備考

SetIterator.more を使用して、set 要素のキー値を取得する前に要素が存在するかどうかを確認します。

#### <a name="examples"></a>例

次の例では、SetIterator.value メソッドを使用して、セット内の現在の項目の値を出力します。

    { 
        Set s1 = new Set (Types::Integer); 
        SetIterator it; 
        // Add some elements 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1);  
        // Start a traversal of the elements in the set 
        it = new SetIterator(s1); 
        // Prints "(begin)[1]" 
        print it.toString();  
        // The elements are fetched in the order: 1, 3, 4, 13 
        while (it.more()) 
        { 
            print it.value(); 
            // Fetch the next element 
            it.next(); 
        } 
        pause; 
    }

### <a name="method-next"></a>メソッド next

次の要素に反復子を移動します。

    public void next()

#### <a name="remarks"></a>備考

SetIterator.more を使用して、反復子が有効な要素を指しているかどうかを判断します。

#### <a name="examples"></a>例

次の例では、SetIterator.next メソッドを使用して、反復子をセット内の次の要素に移動し、別の要素が存在するかどうかをテストし、別の要素がある場合はその値をコンテナーに追加します。

    static public void saveSequence(classId _classId, Set _sequence) 
    { 
        SysCheckListItemTable sysCheckListItemTable; 
        SetIterator           si; 
        container             con = connull(); 
        if (_sequence) 
        { 
            si = new SetIterator(_sequence); 
            si.begin(); 
            while (si.more()) 
            { 
                 con += si.value(); 
                 si.next(); 
            } 
        } 
        //... 
    }

### <a name="method-new"></a>メソッド new

セットに対する新しい反復子を作成します。

    public void new(Set set)

#### <a name="parameters"></a>パラメーター

set  
繰り返し処理するセット。

#### <a name="remarks"></a>備考

反復子は、セットが空でない場合、セットの最初の値に配置されます。

#### <a name="examples"></a>例

次の例では、整数のセットを作成し、セットの反復子を作成します。

    Set s1 = new Set (Types::Integer); 
    SetIterator it; 
    it = new SetIterator(s1);

### <a name="method-begin"></a>メソッド begin

反復子をセットの先頭に移動します。

    public void begin()

#### <a name="remarks"></a>備考

新しく作成されるセット反復子は、セットの最初の要素に配置されます。 通常はセットを反復処理する前に begin メソッドを呼び出す必要はありません。後でポインタをリセットしたい場合にのみ、その操作を行う必要があります。

#### <a name="examples"></a>例

次の例では、指定されたインターフェイス、つまり \_id クラスを実装するクラスのクラス ID のセットを返します。 スーパークラスの場合、反復子は設定からクラスを削除するために使用され、\_onlyLeafClasses パラメーターは true に設定されます。 開始メソッドを使用して、セットからスーパークラスが削除された後に反復子をリセットします。

    public static Set getImplements( 
        classId _id,  
        boolean _onlyLeafClasses = true) 
    { 
        Dictionary dictionary = new Dictionary(); 
        SysDictClass sysDictClass; 
        boolean removed; 
        Set set = new Set(Types::Integer); 
        SetIterator setIterator = new SetIterator(set); 
        int i; 
        for (i=1;i<=dictionary.classCnt();i++) 
        { 
            sysDictClass = new SysDictClass(dictionary.classCnt2Id(i)); 
            if (sysDictClass.isImplementing(_id)) 
            { 
                set.add(sysDictClass.id()); 
            } 
        } 
        //No superclasses included in return set 
        if (_onlyLeafClasses) 
        { 
            // begin method not needed here; only for clarity 
            setIterator.begin();  
            while (setIterator.more()) 
            { 
                removed = false; 
                sysDictClass = new SysDictClass(setIterator.value()); 
                while (sysDictClass.extend()) 
                { 
                    removed = removed | set.remove(sysDictClass.extend()); 
                    sysDictClass = new SysDictClass(sysDictClass.extend()); 
                } 
                if (removed) 
                { 
                    // Restart search 
                    setIterator.begin();  
                } 
                else 
                { 
                    setIterator.next(); 
                } 
            } 
        } 
        return set; 
    }

### <a name="method-delete"></a>メソッド delete

セットの反復子によってポイントされている要素を削除します。

    public void delete()

#### <a name="remarks"></a>備考

反復子は、このメソッドを呼び出した後に次の要素を指します。

#### <a name="examples"></a>例

次の例では、すべての奇数要素をセットから削除します。

    { 
        Set iset = new Set (Types::Integer); 
        SetIterator it; 
        int i; 
        for (i = 1; i <= 10; i++) 
        { 
            iset.add(i); 
        } 
        // Delete all odd elements 
        it = new SetIterator(iset); 
        while (it.more()) 
        { 
            if (it.value() mod 2 != 0) 
            { 
                // The value is odd. Delete and skip to next element. 
                it.delete(); 
            } 
            else 
            { 
                it.next(); 
            } 
        } 
        print iset.toString(); 
        pause; 
    }

### <a name="method-end"></a>メソッド end

セットで最後の要素の後に反復子を移動します。

    public void end()

#### <a name="remarks"></a>備考

このメソッドを実行した後、より多くのメソッドは false を返します。

## <a name="class-skipaosvalidationpermission"></a>クラス SkipAOSValidationPermission
    class SkipAOSValidationPermission extends CodeAccessPermission

SkipAOSValidationPermission クラスは、AOS 検証を省略して、特定の API のアクセス許可をチェックする機能を制御します。

### <a name="remarks"></a>備考

保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します。サーバー静的メソッド または RunOn クラス プロパティを使用してサーバー上で実行するように設定されているクラス インスタンス メソッド。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                            |
| public boolean isSubsetOf(CodeAccessPermission target) | 派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new()                                      | SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。                                                |

### <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在の派生クラスオブジェクトのコピーです。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。 詳細については、「」を参照してください。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。 詳細については、「」を参照してください。

### <a name="method-new"></a>メソッド new

SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。

    public void new()

#### <a name="examples"></a>例

次のコード例は、SkipAOSValidationPermission クラスのインスタンスを作成する方法を示しています。

    server static void main(Args args) 
    { 
        SkipAOSValidationPermission perm; 
        ; 
        perm = new SkipAOSValidationPermission(); 
    }

## <a name="class-sqldatadictionary"></a>クラス SqlDataDictionary
    class SqlDataDictionary extends Object

SqlDataDictionary クラスは、データ ディクショナリ保守のメソッドのコレクションを提供します。

### <a name="remarks"></a>備考

この API には、実行時に呼び出される組み込み認証チェックがあります。 開発セキュリティ キー (SysDevelopment) にアクセスせずにユーザーが SQLDataDictionary クラスのメンバーを呼び出すと、例外が発生します。

### <a name="examples"></a>例

次の例では、UserInfo テーブルがデータベースに存在するかどうかを確認します。

    server static public void Main(Args _args) 
    { 
        SqlDataDictionary sqlDict; 
        boolean b; 
        sqlDict = new SqlDataDictionary(); 
        if (sqlDict) 
        { 
            b = sqlDict.tableExist("USERINFO"); 
            print b; 
            pause; 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                               | 説明                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| public int indexCreate(\[TableId tableId\], \[IndexId indexId\])                                                     | テーブルのインデックスを SQL データベースで作成します。 このメソッドを使用してインデックスを再作成することもできます。 |
| public str indexCreateDDL(TableId tableId)                                                                           | テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。                      |
| public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])                            | テーブルのインデックスを SQL データベースでドロップします。                                                      |
| public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])                                                | 任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。        |
| public int tableCreate(\[boolean indexes\], \[TableId tableId\])                                                     | 1 つ以上のテーブルを SQL データベース内に作成します。 また、インデックス用に作成するオプションを提供します。           |
| public str tableCreateDDL(TableId tableId)                                                                           | テーブルを作成するため SQL ステートメントを生成および返します。                                             |
| public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])                                              | テーブルを SQL データベースでドロップします。                                                                    |
| public str tableDropDDL(TableId tableId)                                                                             | テーブルをドロップするため SQL ステートメントを生成および返します。                                               |
| public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])                          | テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。                                                                          |
| public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])                                    | テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。                                                                                |
| public int tableMetaData(TableId tableId)                                                                            | データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。                                                                   |
| public int tableReindex(\[TableId tableId\], \[IndexId indexId\])                                                    | テーブルのインデックスを更新します。                                                                                                  |
| public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])       | テーブルと、SQL データベースのテーブルを同期します。                                               |
| public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\]) | テーブルの切り詰め                                                                                    |
| public str tableTruncateDDL(TableId tableId)                                                                         | テーブルを切り詰めるため SQL ステートメントを生成および返します。                                             |
| ::public static int synchronize(\[boolean synchronize\_all\])                                                        | データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。                           |
| public void new()                                                                                                    | SqlDataDictionary クラスの新しいインスタンスを初期化します。                                                                    |
| public void tableDelete(TableId tableId)                                                                             | SQL データベースでテーブルを削除します。                                                                  |

### <a name="method-indexcreate"></a>メソッド indexCreate

テーブルのインデックスを SQL データベースで作成します。 このメソッドを使用してインデックスを再作成することもできます。

    public int indexCreate([TableId tableId], [IndexId indexId])

#### <a name="parameters"></a>パラメーター

tableId  
インデックス ハンドル (すべて0) (オプション)。

<!-- -->

indexId  
インデックス ハンドル (すべて0) (オプション)。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0 です。

#### <a name="remarks"></a>備考

このメソッドを使用すると、インデックスを再作成できます。 パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。

#### <a name="examples"></a>例

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.indexCreate(TableName2Id("Address")); 
    }

### <a name="method-indexcreateddl"></a>メソッド indexCreateDDL

テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。

    public str indexCreateDDL(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
インデックスを作成する必要があるテーブル ハンドル。

#### <a name="return-value"></a>戻り値

テーブルのインデックスを作成するための SQL ステートメントを返します。

### <a name="method-indexdrop"></a>メソッド indexDrop

テーブルのインデックスを SQL データベースでドロップします。

    public int indexDrop([TableId tableId], [IndexId indexId], [boolean onlyNonUnique])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

indexId  

<!-- -->

onlyNonUnique  

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0。

#### <a name="remarks"></a>備考

パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。

#### <a name="examples"></a>例

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.indexDrop(TableName2Id("Address")); 
    }

### <a name="method-name"></a>メソッド名

任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。

    public str name(str bmsname, [FieldId fieldId], [int arrayindex])

#### <a name="parameters"></a>パラメーター

bmsname  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

<!-- -->

fieldId  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

<!-- -->

arrayindex  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

#### <a name="return-value"></a>戻り値

有効なオブジェクト名。

#### <a name="remarks"></a>備考

名前は切り捨てられる可能性があるため、固有のオブジェクト識別子が指定される場合があります。 また、3 番目のパラメータは、メソッドが配列フィールドの個別の SQL フィールド名を返すことを可能にします。

### <a name="method-tablecreate"></a>メソッド tableCreate

1 つ以上のテーブルを SQL データベース内に作成します。 また、インデックス用に作成するオプションを提供します。

    public int tableCreate([boolean indexes], [TableId tableId])

#### <a name="parameters"></a>パラメーター

indexes  
テーブル ハンドル (すべて0) (オプション)。

<!-- -->

tableId  
テーブル ハンドル (すべて0) (オプション)。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0。

#### <a name="remarks"></a>備考

低レベルのメンテナンスにのみ使用されます。

#### <a name="examples"></a>例

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.tableCreate(TableName2Id("Address")); 
    }

### <a name="method-tablecreateddl"></a>メソッド tableCreateDDL

テーブルを作成するため SQL ステートメントを生成および返します。

    public str tableCreateDDL(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
作成するテーブルのテーブル ハンドルです。

#### <a name="return-value"></a>戻り値

テーブルを作成する SQL ステートメント。

### <a name="method-tabledrop"></a>メソッド tableDrop

テーブルを SQL データベースでドロップします。

    public int tableDrop(TableId tableId, [boolean prompt_before_drop])

#### <a name="parameters"></a>パラメーター

tableId  
テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。 既定では、true です。

<!-- -->

prompt\_before\_drop  
テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。 既定では、true です。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0。

### <a name="method-tabledropddl"></a>メソッド tableDropDDL

テーブルをドロップするため SQL ステートメントを生成および返します。

    public str tableDropDDL(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
削除するテーブル。

#### <a name="return-value"></a>戻り値

指定されたテーブルを削除する SQL ステートメント。

### <a name="method-tableempty"></a>メソッド tableEmpty

テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。

    public boolean tableEmpty(TableId tableId, [str company], [boolean not_this_company])

#### <a name="parameters"></a>パラメーター

tableId  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

<!-- -->

会社  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

<!-- -->

not\_this\_company  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

#### <a name="return-value"></a>戻り値

テーブルが空の場合は true。それ以外の場合は、false。

### <a name="method-tableexist"></a>メソッド tableExist

テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。

    public boolean tableExist(str sqltablename, [boolean use_within_transaction])

#### <a name="parameters"></a>パラメーター

sqltablename  
トランザクションを使用するかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

use\_within\_transaction  
トランザクションを使用するかどうかを決定するブール フラグ; オプション。 既定では、false です。

#### <a name="return-value"></a>戻り値

テーブルが存在する場合は true。それ以外の場合は、false。

### <a name="method-tablemetadata"></a>メソッド tableMetaData

データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。

    public int tableMetaData(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ハンドル。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は true。

### <a name="method-tablereindex"></a>メソッド tableReindex

テーブルのインデックスを更新します。

    public int tableReindex([TableId tableId], [IndexId indexId])

#### <a name="parameters"></a>パラメーター

tableId  
インデックス ハンドル (すべて0) (オプション)。 既定では 0 です。

<!-- -->

indexId  
インデックス ハンドル (すべて0) (オプション)。 既定では 0 です。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0。

### <a name="method-tablesynchronize"></a>メソッド tableSynchronize

テーブルと、SQL データベースのテーブルを同期します。

    public int tableSynchronize(TableId tableId, [boolean update_dict_info_only], [boolean check_indexes])

#### <a name="parameters"></a>パラメーター

tableId  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

<!-- -->

update\_dict\_info\_only  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

<!-- -->

check\_indexes  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は true。

### <a name="method-tabletruncate"></a>メソッド tableTruncate

テーブルの切り詰め

    public int tableTruncate(TableId tableId, [boolean prompt_before_truncate], [boolean truncate_system_table])

#### <a name="parameters"></a>パラメーター

tableId  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

prompt\_before\_truncate  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

truncate\_system\_table  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 0。

### <a name="method-tabletruncateddl"></a>メソッド tableTruncateDDL

テーブルを切り詰めるため SQL ステートメントを生成および返します。

    public str tableTruncateDDL(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
切り詰めるテーブルのテーブル ハンドルです。

#### <a name="return-value"></a>戻り値

テーブルを切り詰める SQL ステートメント。

### <a name="method-synchronize"></a>メソッド synchronize

データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。

    public static int synchronize([boolean synchronize_all])

#### <a name="parameters"></a>パラメーター

synchronize\_all  
すべてのテーブルを同期するかどうかを示すブール フラグ; オプション。 True の場合、このメソッドは (カーネルによって欠陥とマークされているテーブルのみでなく) すべてのテーブルを同期します。 既定では、false です。

#### <a name="return-value"></a>戻り値

同期が成功した場合は true。それ以外の場合は、false。

### <a name="method-new"></a>メソッド new

SqlDataDictionary クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-tabledelete"></a>メソッド tableDelete

SQL データベースでテーブルを削除します。

    public void tableDelete(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

## <a name="class-sqldatadictionarypermission"></a>クラス SqlDataDictionaryPermission
    class SqlDataDictionaryPermission extends CodeAccessPermission

SqlDataDictionaryPermission クラスは、メソッドにアクセスする機能を制御し、特定の API のアクセス許可を確認するように設計されています。 保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。

### <a name="remarks"></a>備考

保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。

### <a name="examples"></a>例

次の例では、xRefNames テーブルからデータを削除します。 assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。

    { 
        DictTable dictTable = new DictTable(tablenum(xRefNames)); 
        str sqlTableName; 
        SqlDataDictionary sqlTable; 
        if (dictTable && dictTable.enabled()) 
        { 
            sqlTableName = dictTable.name(DbBackend::Sql); 
            sqlTable = new SqlDataDictionary(); 
            // Try to truncate only if the table does exist 
            // in the SQL database. 
            if (sqlTable.tableExist(sqlTableName)) 
            { 
                new SqlDataDictionaryPermission( 
                    methodstr(SqlDataDictionary, tableTruncate)).assert(); 
                sqlTable.tableTruncate(tablenum(xRefNames)); 
                CodeAccessPermission::revertAssert(); 
            } 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new(IdentifierName methodName)             | SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。                 |

### <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在のアクセス許可オブジェクトのコピーです。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

### <a name="method-new"></a>メソッド new

SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。

    public void new(IdentifierName methodName)

#### <a name="parameters"></a>パラメーター

methodName  
呼び出されるメソッドの名前を表す文字列。

#### <a name="examples"></a>例

次のコード例は、xRefNames テーブルのデータを削除します。

    server static void main(Args _args) 
    { 
        DictTable dictTable = new DictTable(tablenum(xRefNames)); 
        str sqlTableName; 
        SqlDataDictionary sqlTable; 
        if (dictTable && dictTable.enabled()) 
        { 
            sqlTableName = dictTable.name(DbBackend::Sql); 
            sqlTable = new SqlDataDictionary(); 
            // Only try to truncate if the table does exist 
            // in the SQL database 
            if (sqlTable.tableExist(sqlTableName)) 
            { 
                new SqlDataDictionaryPermission( 
                    methodstr(SqlDataDictionary, tableTruncate)).assert(); 
                sqlTable.tableTruncate(tablenum(xRefNames)); 
                CodeAccessPermission::revertAssert(); 
            } 
        } 
    }

## <a name="class-sqlstatementexecutepermission"></a>クラス SqlStatementExecutePermission
    class SqlStatementExecutePermission extends CodeAccessPermission

SQL を使用する機能をコントロールします。

### <a name="remarks"></a>備考

このクラスは、特定の API のアクセス許可をチェックするように設計されています。 保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッドまたは
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

### <a name="examples"></a>例

この例では、サーバー上で実行される CustTable テーブルで SQL クエリを実行します。 クエリの結果は、\_resultSet オブジェクトに格納されます。 assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。

    server static void main(Args _args) 
    { 
        DictTable  _dictTable; 
        Connection _connection; 
        Statement  _statement; 
        str        _sql; 
        ResultSet  _resultSet; 
        SqlStatementExecutePermission _perm; 
        _dictTable = new DictTable(tableNum(CustTable)); 
        if (_dictTable != null) 
            { 
               _connection = new Connection(); 
               _sql = strfmt( "SELECT * FROM %1", _dictTable.name(DbBackend::Sql) ); 
               _perm = new SqlStatementExecutePermission(_sql); 
               // Check for permission to use the _statement. 
               _perm.assert(); 
               _statement = _connection.createStatement(); 
               _resultSet = _statement.executeQuery(_sql); 
               // End the scope of the assert call. 
               CodeAccessPermission::revertAssert(); 
            } 
    }

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new(str sqlStatement)                      | SQLStatementExecutePermission クラスの新しいインスタンスを作成します。               |

### <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在のアクセス許可オブジェクトのコピーです。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

### <a name="method-new"></a>メソッド new

SQLStatementExecutePermission クラスの新しいインスタンスを作成します。

    public void new(str sqlStatement)

#### <a name="parameters"></a>パラメーター

sqlStatement  
実行する SQL 文字列。

#### <a name="examples"></a>例

次の例では、サーバー上で実行される、CustTable テーブルで SQL クエリを実行します。 クエリの結果は、resultSet オブジェクトに格納されます。

    server static void main(Args _args) 
    { 
        DictTable  dictTable; 
        Connection connection; 
        Statement  statement; 
        str        sql; 
        ResultSet  resultSet; 
        SqlStatementExecutePermission perm; 
        dictTable = new DictTable(tableNum(CustTable)); 
        if (dictTable != null) 
            { 
               connection = new Connection(); 
               sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
               //Instantiate the permission class 
               perm = new SqlStatementExecutePermission(sql); 
               //check for permission to use statement 
               perm.assert(); 
               statement = connection.createStatement(); 
               resultSet = statement.executeQuery(sql); 
               //end the scope of the assert call 
               CodeAccessPermission::revertAssert(); 
            } 
    }

## <a name="class-sqlsyncpending"></a>クラス SqlSyncPending
    class SqlSyncPending extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                               | 説明                                             |
|------------------------------------------------------|---------------------------------------------------------|
| public ConfigurationKeyId configurationKeyTouched()  |                                                         |
| public boolean databaseTouched(\[boolean newValue\]) |                                                         |
| public ExtendedTypeId extendedDataTypeTouched()      |                                                         |
| public TableId indexesTouched()                      |                                                         |
| public TableId relationTouched()                     |                                                         |
| public TableId tableDeleted()                        |                                                         |
| public TableId tableTouched()                        |                                                         |
| public void new()                                    | SqlSyncPending クラスの新しいインスタンスを初期化します。 |

### <a name="method-configurationkeytouched"></a>メソッド configurationKeyTouched

    public ConfigurationKeyId configurationKeyTouched()

#### <a name="return-value"></a>戻り値

### <a name="method-databasetouched"></a>メソッド databaseTouched

    public boolean databaseTouched([boolean newValue])

#### <a name="parameters"></a>パラメーター

newValue  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatypetouched"></a>メソッド extendedDataTypeTouched

    public ExtendedTypeId extendedDataTypeTouched()

#### <a name="return-value"></a>戻り値

### <a name="method-indexestouched"></a>メソッド indexesTouched

    public TableId indexesTouched()

#### <a name="return-value"></a>戻り値

### <a name="method-relationtouched"></a>メソッド relationTouched

    public TableId relationTouched()

#### <a name="return-value"></a>戻り値

### <a name="method-tabledeleted"></a>メソッド tableDeleted

    public TableId tableDeleted()

#### <a name="return-value"></a>戻り値

### <a name="method-tabletouched"></a>メソッド tableTouched

    public TableId tableTouched()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

SqlSyncPending クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-sqlsystem"></a>クラス SqlSystem
    class SqlSystem extends Object

SqlSystem クラスには、有効な SQL システムに関する情報 (通常はログイン情報) が含まれます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                   | 説明                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| public LoginProperty createLoginProperty()                                                                                               | データベースにログイン プロパティを作成します。                                       |
| public DatabaseId databaseId()                                                                                                           | SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。          |
| public str databaseName()                                                                                                                | SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。                               |
| public boolean dbRequestedUnicodeEnabled()                                                                                               | Unicode がデータベースでサポートされているかどうかを示す値を取得します。                             |
| public str filenameDeadlocks(str Userid)                                                                                                 | デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。                                        |
| public str filenameQuerytimelimit(str Userid)                                                                                            | ユーザー固有の querytime 期限ログ ファイルの名前を取得します。                                        |
| public str filenameSqlTrace(str Userid)                                                                                                  | 特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。                                     |
| public str filenameWarnings(str Userid)                                                                                                  | 警告ログ ファイルに固有のユーザーの名前を取得します。                                              |
| public str logfileName(\[boolean fromCommandline\])                                                                                      | 標準的な SQL エラー ログ ファイルの名前を取得します。                            |
| public str loginConnectString()                                                                                                          | ODBC の完全な接続文字列を取得します。                                                              |
| public str loginDatabase()                                                                                                               | 現在接続されているデータベースの名前を取得します。                                              |
| public str loginDSN()                                                                                                                    | データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。 |
| public str loginName()                                                                                                                   | データベースにログインするために使用されるユーザー名を取得します。                                         |
| public str loginServer()                                                                                                                 | 現在接続されているデータベース サーバーの名前を取得します。                                       |
| public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])    | 文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。    |
| public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\]) | SQL タイプを修正するため入力 AX データ型を書式設定します。                                                      |
| ::public static boolean clusteredIndexes()                                                                                               |                                                                                                         |
| ::public static str databaseBackendDesc()                                                                                                |                                                                                                         |
| ::public static DatabaseId databaseBackendId()                                                                                           |                                                                                                         |
| ::public static str databaseBackendName()                                                                                                |                                                                                                         |
| ::public static DatabaseCLI databaseCallLevelInterface()                                                                                 |                                                                                                         |
| ::public static int databaseHints(\[int new\_hint\_value\])                                                                              |                                                                                                         |
| ::public static boolean functionalIndexes()                                                                                              |                                                                                                         |
| ::public static str modelDatabaseBackendName()                                                                                           | 現在接続されているモデル データベース AOS の名前を取得します。                                    |
| ::public static str managedConnectionString()                                                                                            |                                                                                                         |
| public void new()                                                                                                                        | SqlSystem クラスの新しいインスタンスを初期化します。                                                      |
| public void logfileWrite(str Text)                                                                                                       | テキスト文字列を標準 SQL エラー ログファイルに記述します。                         |

### <a name="method-createloginproperty"></a>メソッド createLoginProperty

データベースにログイン プロパティを作成します。

    public LoginProperty createLoginProperty()

#### <a name="return-value"></a>戻り値

作成されたログイン プロパティ。

### <a name="method-databaseid"></a>メソッド databaseId

SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。

    public DatabaseId databaseId()

#### <a name="return-value"></a>戻り値

SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID。

#### <a name="remarks"></a>備考

データベースの仕入先が、何らかの理由で特定できない場合、列挙 DbBackend::UNKNOWN が返されます。

### <a name="method-databasename"></a>メソッド databaseName

SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。

    public str databaseName()

#### <a name="return-value"></a>戻り値

SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前。

### <a name="method-dbrequestedunicodeenabled"></a>メソッド dbRequestedUnicodeEnabled

Unicode がデータベースでサポートされているかどうかを示す値を取得します。

    public boolean dbRequestedUnicodeEnabled()

#### <a name="return-value"></a>戻り値

Unicode がデータベースでサポートされているかどうかを示す値。

### <a name="method-filenamedeadlocks"></a>メソッド filenameDeadlocks

デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。

    public str filenameDeadlocks(str Userid)

#### <a name="parameters"></a>パラメーター

Userid  

#### <a name="return-value"></a>戻り値

デッドロックのトレース ログ ファイルに固有のユーザーの名前。

### <a name="method-filenamequerytimelimit"></a>メソッド filenameQuerytimelimit

ユーザー固有の querytime 期限ログ ファイルの名前を取得します。

    public str filenameQuerytimelimit(str Userid)

#### <a name="parameters"></a>パラメーター

Userid  

#### <a name="return-value"></a>戻り値

ユーザー固有の querytime 期限ログ ファイルの名前。

### <a name="method-filenamesqltrace"></a>メソッド filenameSqlTrace

特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。

    public str filenameSqlTrace(str Userid)

#### <a name="parameters"></a>パラメーター

Userid  
ユーザー ID。

#### <a name="return-value"></a>戻り値

SQL 追跡ログのファイル名。

### <a name="method-filenamewarnings"></a>メソッド filenameWarnings

警告ログ ファイルに固有のユーザーの名前を取得します。

    public str filenameWarnings(str Userid)

#### <a name="parameters"></a>パラメーター

Userid  
関係ユーザーの識別子。

#### <a name="return-value"></a>戻り値

警告ログ ファイルに固有のユーザーの名前。

### <a name="method-logfilename"></a>メソッド logfileName

標準的な SQL エラー ログ ファイルの名前を取得します。

    public str logfileName([boolean fromCommandline])

#### <a name="parameters"></a>パラメーター

fromCommandline  
ブール値。 パラメーターとしてゼロ以外の値を渡すと、コマンド ラインで渡されるログファイル名が呼び出しにより返されます (オプション)。

#### <a name="return-value"></a>戻り値

標準 SQL エラー ログ ファイルのファイル名。

#### <a name="remarks"></a>備考

バージョン 2.11 以降では、空の文字列が返されます (下位互換性のため)。 ログ ファイル名を取得するには、filenameSqlError メソッドを使用します。

### <a name="method-loginconnectstring"></a>メソッド loginConnectString

ODBC の完全な接続文字列を取得します。

    public str loginConnectString()

#### <a name="return-value"></a>戻り値

ODBC の完全な接続文字列。

### <a name="method-logindatabase"></a>メソッド loginDatabase

現在接続されているデータベースの名前を取得します。

    public str loginDatabase()

#### <a name="return-value"></a>戻り値

現在接続されているデータベースの名前。

#### <a name="examples"></a>例

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginDatabase(); 
    }

### <a name="method-logindsn"></a>メソッド loginDSN

データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。

    public str loginDSN()

#### <a name="return-value"></a>戻り値

データベースへの接続に使用される ODBC データ ソース名の名前。

#### <a name="remarks"></a>備考

既定の DSN は「BMSDSN」です。

#### <a name="examples"></a>例

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginDSN(); 
    }

### <a name="method-loginname"></a>メソッド loginName

データベースにログインするために使用されるユーザー名を取得します。

    public str loginName()

#### <a name="return-value"></a>戻り値

データベースにログインするために使用されるユーザー名。

#### <a name="examples"></a>例

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginName(); 
    }

### <a name="method-loginserver"></a>メソッド loginServer

現在接続されているデータベース サーバーの名前を取得します。

    public str loginServer()

#### <a name="return-value"></a>戻り値

現在接続されているデータベースの名前。

#### <a name="remarks"></a>備考

データベースがサーバーの概念をサポートしていない場合は、空の文字列が返されます。

#### <a name="examples"></a>例

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginServer(); 
    }

### <a name="method-monocasefmt"></a>メソッド monocaseFmt

文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。

    public str monocaseFmt([TableId tableId], [FieldId fieldId], [boolean includingFieldName], [boolean considerSystemVariables])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

fieldId  

<!-- -->

includingFieldName  

<!-- -->

considerSystemVariables  

#### <a name="return-value"></a>戻り値

文字列を 1 つのケースにキャストするために使用される書式文字列。

#### <a name="remarks"></a>備考

プレースホルダの Finance and Operations アプリケーション スタイルが使用されます (「%1」など)。

### <a name="method-sqlliteral"></a>メソッド sqlLiteral

SQL タイプを修正するため入力 AX データ型を書式設定します。

    public str sqlLiteral(AnyType data, [boolean forWhereClause], [boolean likeOperand], [boolean rightJustify], [int stringLength])

#### <a name="parameters"></a>パラメーター

データ  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

forWhereClause  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

likeOperand  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

rightJustify  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

stringLength  
文字列の長さ。 既定ではゼロに等しくなります。

#### <a name="return-value"></a>戻り値

書式設定された SQL 型文字列。

### <a name="method-clusteredindexes"></a>メソッド clusteredIndexes

    public static boolean clusteredIndexes()

#### <a name="return-value"></a>戻り値

### <a name="method-databasebackenddesc"></a>メソッド databaseBackendDesc

    public static str databaseBackendDesc()

#### <a name="return-value"></a>戻り値

### <a name="method-databasebackendid"></a>メソッド databaseBackendId

    public static DatabaseId databaseBackendId()

#### <a name="return-value"></a>戻り値

### <a name="method-databasebackendname"></a>メソッド databaseBackendName

    public static str databaseBackendName()

#### <a name="return-value"></a>戻り値

### <a name="method-databasecalllevelinterface"></a>メソッド databaseCallLevelInterface

    public static DatabaseCLI databaseCallLevelInterface()

#### <a name="return-value"></a>戻り値

### <a name="method-databasehints"></a>メソッド databaseHints

    public static int databaseHints([int new_hint_value])

#### <a name="parameters"></a>パラメーター

new\_hint\_value  

#### <a name="return-value"></a>戻り値

### <a name="method-functionalindexes"></a>メソッド functionalIndexes

    public static boolean functionalIndexes()

#### <a name="return-value"></a>戻り値

### <a name="method-modeldatabasebackendname"></a>メソッド modelDatabaseBackendName

現在接続されているモデル データベース AOS の名前を取得します。

    public static str modelDatabaseBackendName()

#### <a name="return-value"></a>戻り値

現在接続されているモデル データベースの名前。

### <a name="method-managedconnectionstring"></a>メソッド managedConnectionString

    public static str managedConnectionString()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

SqlSystem クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-logfilewrite"></a>メソッド logfileWrite

テキスト文字列を標準 SQL エラー ログファイルに記述します。

    public void logfileWrite(str Text)

#### <a name="parameters"></a>パラメーター

テキスト  
ログファイルに書き込むテキスト (ブックマークなど)。

#### <a name="remarks"></a>備考

あらゆる種類のエラー状況 (ログ ファイルに記録される) に従い、現在のシナリオを説明する個人用ブックマークを挿入します。

#### <a name="examples"></a>例

    static void myExample(Args _args) 
    { 
        SqlSystem SqlSystem; 
        SqlSystem = new SqlSystem(); 
        SqlSystem.logfileWrite("Recheck the returned data."); 
    }

## <a name="class-ssrsreportautodesignnode"></a>クラス SSRSReportAutoDesignNode
    class SSRSReportAutoDesignNode extends SSRSReportDesignNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                        |
|-----------------------------------------------------|------------------------------------------------------------------------------------|
| public str getCrossReferences()                     | 指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。 |
| public void setCrossReferences(str crossReferences) | 指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。      |

### <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。

    public str getCrossReferences()

#### <a name="return-value"></a>戻り値

XML 形式での相互参照。

### <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a>パラメーター

crossReferences  
XML 形式での相互参照。

#### <a name="remarks"></a>備考

このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。

## <a name="class-ssrsreportconceptnode"></a>クラス SSRSReportConceptNode
    class SSRSReportConceptNode extends xResourceNode

SSRSReportConceptNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の SSRS レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。

### <a name="remarks"></a>備考

ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | このノードのソース コードを返します。                                         |
| public str getCrossReferences()                            | 指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。 |
| public void allowCaching(\[boolean allow\])                |                                                                               |
| public void setCrossReferences(str crossReferences)        | 指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。      |
| public void AOTsetSource(str source, \[boolean isStatic\]) | このノードのソース コードを設定します。                                            |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。

    public str getCrossReferences()

#### <a name="return-value"></a>戻り値

XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。

### <a name="method-allowcaching"></a>メソッド allowCaching

    public void allowCaching([boolean allow])

#### <a name="parameters"></a>パラメーター

allow  

### <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a>パラメーター

crossReferences  
XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。

#### <a name="remarks"></a>備考

このメソッドは、指定された SSRSReportConceptNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

このノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを指定する値 (オプション)。

<!-- -->

isStatic  
メソッドが静的かどうかを指定する値 (オプション)。

#### <a name="remarks"></a>備考

このメソッドは、ソース コードを持つノードによって上書きされます。

## <a name="class-ssrsreportdesignnode"></a>クラス SSRSReportDesignNode
    class SSRSReportDesignNode extends xResourceNode

SSRSReportDesignNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の Microsoft SQL Server Reporting Services レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。

### <a name="remarks"></a>備考

ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| public str getCrossReferences()                     | 指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。 |
| public void setCrossReferences(str crossReferences) | 指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。      |

### <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。

    public str getCrossReferences()

#### <a name="return-value"></a>戻り値

XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。

### <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a>パラメーター

crossReferences  
XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。

#### <a name="remarks"></a>備考

このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。

## <a name="class-ssrsreportprecisiondesignnode"></a>クラス SSRSReportPrecisionDesignNode
    class SSRSReportPrecisionDesignNode extends SSRSReportDesignNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| public str getCrossReferences()                     | 指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。 |
| public void setCrossReferences(str crossReferences) | 指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。      |

### <a name="method-getcrossreferences"></a>メソッド getCrossReferences

指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。

    public str getCrossReferences()

#### <a name="return-value"></a>戻り値

XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。

### <a name="method-setcrossreferences"></a>メソッド setCrossReferences

指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a>パラメーター

crossReferences  
XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。

#### <a name="remarks"></a>備考

このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。 相互参照システムは更新されません。

## <a name="class-statement"></a>クラスの明細書
    class Statement extends Object

Statement クラスは、静的 SQL ステートメントを実行し、生成された結果を取得します。

### <a name="remarks"></a>備考

明細書ごとに 1 つだけ、任意の時点で開くことができます。 したがって、1 つの ResultSet の読み込みが別の ResultSet の読み込みとインターリーブされている場合は、それぞれ異なるステートメントによって生成されている必要があります。 レコードとフィールド レベルのセキュリティは、明細書クラスでは適用されません。 したがって、明示的なセキュリティ検証を行わずにユーザーに返されるデータを公開していないことを、確認してください。 すべての実行可能な明細メソッドは現在 ResultSet で開いている場合明細書は暗黙的に閉じます。

### <a name="examples"></a>例

    static void example() 
    { 
        Connection Con; 
        Statement Stmt; 
        ResultSet R; 
        SqlStatementExecutePermission perm; 
        str sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
        Con = new Connection(); 
        Stmt = Con.createStatement(); 
        perm = new SqlStatementExecutePermission(sql); 
        perm.assert(); 
        R = Stmt.executeQuery(sql); 
        while ( R.next() ) 
        { 
            print R.getString(1); 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| public ResultSet executeQuery(str statement) | インスタンスの the を返す SQL ステートメントを実行します。                                       |
| public int executeUpdate(str statement)      | SQL INSERT、UPDATE、または DELETE ステートメントを実行します。                                               |
| public int getLastError()                    | 最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。         |
| public str getLastErrorText()                | 最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。 |
| public int getMaxFieldSize()                 | 現在の列の最大サイズ制限を返します (ある場合)。                                            |
| public void close()                          | ステートメント オブジェクトのデータベースのリソースを解放します。                                            |
| public void setMaxFieldSize(int max)         | 列の最大サイズ制限を設定します。                                                               |

### <a name="method-executequery"></a>メソッド executeQuery

インスタンスの the を返す SQL ステートメントを実行します。

    public ResultSet executeQuery(str statement)

#### <a name="parameters"></a>パラメーター

明細書  
結果セットを取得するために使用される SQL ステートメントを含む文字列。

#### <a name="return-value"></a>戻り値

クエリから返されたデータを含むオブジェクト。

#### <a name="remarks"></a>備考

ユーザーが executeQuery メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 SQL ステートメントを実行するための安全な方法は次のとおりです。

-   クエリ
-   ビュー
-   X++ select ステートメント

レコード レベル セキュリティは、明細書クラスでは適用されません。 データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。

#### <a name="examples"></a>例

次の例では、サーバー上で実行される、CustTable で SQL クエリを実行します。 クエリの結果は、resultSet オブジェクトに格納されます。

    server static void main(Args _args) 
    { 
        DictTable  dictTable; 
        Connection connection; 
        Statement  statement; 
        str        sql; 
        ResultSet  resultSet; 
        SqlStatementExecutePermission perm; 
        dictTable = new DictTable(tableNum(CustTable)); 
        if (dictTable != null) 
            { 
               connection = new Connection(); 
               sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
               perm = new SqlStatementExecutePermission(sql); 
               // Check for permission to use the statement. 
               perm.assert(); 
               statement = connection.createStatement(); 
               resultSet = statement.executeQuery(sql); 
               // End the scope of the assert call. 
               CodeAccessPermission::revertAssert(); 
            } 
    }

### <a name="method-executeupdate"></a>メソッド executeUpdate

SQL INSERT、UPDATE、または DELETE ステートメントを実行します。

    public int executeUpdate(str statement)

#### <a name="parameters"></a>パラメーター

明細書  
データベースに渡される SQL ステートメントを含む文字列。

#### <a name="return-value"></a>戻り値

更新された行数。それ以外は、何も返さない SQL ステートメントの 0 (ゼロ)。

#### <a name="remarks"></a>備考

SQLDDL ステートメントなど、何も返さない SQL ステートメントを実行することもできます。 ユーザーが executeUpdate メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 データベースとやり取りするための安全な方法は次のとおりです。

-   クエリ
-   ビュー
-   X++ select ステートメント

レコード レベル セキュリティは、明細書クラスでは適用されません。 データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。

### <a name="method-getlasterror"></a>メソッド getLastError

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。

    public int getLastError()

#### <a name="return-value"></a>戻り値

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コード。成功の場合は 0 です。

#### <a name="examples"></a>例

    static void StatementGetLastError()  
    { 
        str sql, sql2; 
        UserConnection Connection = new UserConnection(); 
        Statement Statement = Connection.createStatement(); 
        boolean clear_infolog = false; 
        print "-Delete-a-non-existing-record-(valid statement)-----------"; 
        sql = "delete from zipcode where Recid = 2"; 
        new SqlStatementExecutePermission(sql).assert(); 
        Statement.executeUpdate(sql); 
        print " Error code was: ", Statement.getLastError(); 
        print " Error message was '", Statement.getLastErrorText(), "'"; 
        try 
        { 
            print "\n"; 
            print "-Delete-from-a-non-existing-table-(invalid statement)---    --"; 
            sql2 = "delete from StrangeTable07"; 
            new SqlStatementExecutePermission(sql2).assert(); 
            Statement.executeUpdate(sql2); 
        } 
        catch (exception::Error) 
        { 
            print "Exception was caught:"; 
            print " Error code was: ", Statement.getLastError(); 
            print " Error message was '", Statement.getLastErrorText(), "'"; 
        } 
        CodeAccessPermission::revertAssert(); 
        pause; 
    }

### <a name="method-getlasterrortext"></a>メソッド getLastErrorText

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。

    public str getLastErrorText()

#### <a name="return-value"></a>戻り値

最後の SQL 操作の SQL データベースによって提供されるエラー テキスト。

### <a name="method-getmaxfieldsize"></a>メソッド getMaxFieldSize

現在の列の最大サイズ制限を返します (ある場合)。

    public int getMaxFieldSize()

#### <a name="return-value"></a>戻り値

現在の列の最大サイズ制限。0 は無制限を意味します。

#### <a name="remarks"></a>備考

maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータの最大量です。binary、varbinary、longvarbinary、char、varchar、および longvarchar 列にのみ適用されます。 制限を超過した場合、余分なデータは通知なしに破棄されます。

### <a name="method-close"></a>メソッド close

ステートメント オブジェクトのデータベースのリソースを解放します。

    public void close()

### <a name="method-setmaxfieldsize"></a>メソッド setMaxFieldSize

列の最大サイズ制限を設定します。

    public void setMaxFieldSize(int max)

#### <a name="parameters"></a>パラメーター

最大  
列の新しい最大サイズ制限。0 は無制限を意味します。

#### <a name="remarks"></a>備考

maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータのサイズを制限するように設定されています。binary、varbinary、longvarbinary、char、varchar、および longvarchar フィールドにのみ適用されます。 制限を超過した場合、余分なデータは通知なしに破棄されます。 最大可搬性については、256 より大きい値を使用します。

## <a name="class-struct"></a>クラス構造体
    class Struct extends Object

構造体は、特定のエンティティに関する情報をグループ化するために、任意の X++ 型の複数値を保持します。

### <a name="remarks"></a>備考

構造体 (略構造) は、すべての X++ 型の複数値を保持できるエンティティです。 構造体は、特定のエンティティに関する情報をグループ化するために使用されます。 たとえば、顧客の名前、年齢、および住所に関する情報を格納し、それからこの複合情報を 1つの項目として扱う場合があります。 構造体内の項目は、データ型と名前で指定されます。 項目は、new メソッドを使用して構造体が作成される場合に追加されるか、add メソッドを使用して構造体が作成された後に作成されます。 Add メソッドを使用して品目を追加する場合は、同時に品目の値を指定し、この値からデータ型が推測されます。 構造体のインスタンス化中に品目を追加する場合は、値または valueIndex メソッドを使用して、値を割り当てる必要があります。 構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。 構造体内の項目は、項目名のアルファベット順に並べられます。 構造体のフィールドは、fields、fieldName、および fieldType メソッドを使用してスキャンできます。 構造体は、コンテナーに梱包し、後で Struct::create メソッドを使用して復元できます。 構造体には、X++ コンテナーとのいくつかの類似点があります。 ただし、コンテナーは値の型であり、X++ 言語に組み込まれています。 入れ子になったコンテナを作成することができますが、入れ子になった構造体は作成することができません。 X++ クラスは、構造とほぼ同じ方法で情報を保管することができます。 クラスはデータを操作する方法を供給することができますが、構造体のための該当する機能は提供されておらず、上書きまたは拡張の概念はありません。 クラスは AOT でのみ作成できますが、構造体は作成されたコードのコンテキスト内にのみ存在します。 クラス メンバーの変数はクラス専用なので、アクセサー関数はクラスの外部から使用される値のためにコード化されている必要があります。 構造体内の項目は一般にアクセス可能です。

### <a name="examples"></a>例

次の例では、2 つの項目を含む構造体を作成し、その項目に値を割り当てます。 Struct.add メソッドを使用して新しい項目が追加されます。項目のデータ型は割り当てられた値から推測されます。 次に、構造体はコンテナーに梱包され、元の構造体のコピーである新しい構造体を作成するために使用されます。

    { 
        Struct s = new struct ("int age; str name"); 
        Struct copy; 
        container c; 
        int i; 
        // Add values to the items 
        s.value("age", 25); 
        s.value("name", "Jane Dow"); 
      // Add a new item; data type is inferred from value 
        s.add("Shoesize", 45); 
        // Print the definition of the struct 
        print s.definitionString(); 
        // Prints the type and name of all items in the struct 
        for (i =  1;   i <= s.fields();i++) 
        { 
             print s.fieldType(i), " ", s.fieldName(i); 
        }  
        // Pack the struct into a container and restore it into copy 
        c = s.pack(); 
        copy = Struct::create(c); 
        print copy.definitionString(); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| public boolean add(str fieldName, AnyType value)              | 構造体に新しい項目を追加し、指定した値を割り当てます。                          |
| public str definitionString()                                 | 構造体の要素の名前およびタイプの説明を返します。                   |
| public boolean exists(str fieldName)                          | 特定の項目が構造体に存在するかどうかを判定します。                                      |
| public str fieldName(int index)                               | 指定された位置にある構造体内の項目の名前を返します。                         |
| public int fields()                                           | 構造体内の項目の数を返します。                                                    |
| public Types fieldType(int index)                             | 指定された位置にある構造体内の項目のデータ型を返します。                    |
| public int index(str fieldName)                               | 名前に基づいて構造体の項目の位置を計算します。                           |
| public container pack()                                       | Struct クラスの現在のインスタンスをシリアル化します。                                          |
| public boolean remove(str fieldName)                          | 構造体から品目を削除します。                                                                |
| public str toString()                                         | 構造体の内容を説明する文字列を返します。                                   |
| public AnyType value(str fieldName, \[AnyType value\])        | 構造体で指定される品目の値を取得または設定します。                                      |
| public str valueImage(int index)                              | 構造体内の特定の位置にある品目の値を説明する文字列を返します。 |
| public AnyType valueIndex(int index, \[AnyType value\])       | 構造体で指定される位置での品目の値を取得または設定します。                       |
| public str xml(\[int indent\])                                | 現在のオブジェクトを表す XML 文字列を返します。                                     |
| ::public static Struct create(container container)            | 以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。          |
| ::public static Struct createFromXML(Object xmlnode)          |                                                                                               |
| ::public static boolean equal(Struct struct1, Struct struct2) | 2 つの構造体が等しいかどうかを判断します。                                                     |
| ::public static Struct merge(Struct struct1, Struct struct2)  | 2 つの構造体を組み合わせ、新しい構造体を作成します。                                                  |
| public void new(VarArg specifier)                             | 構造体を作成します。                                                                             |

### <a name="method-add"></a>メソッド add

構造体に新しい項目を追加し、指定した値を割り当てます。

    public boolean add(str fieldName, AnyType value)

#### <a name="parameters"></a>パラメーター

fieldName  
新しい項目に割り当てる値 (オプション)。 この値は、アイテムのタイプを定義します。

<!-- -->

値  
新しい項目に割り当てる値 (オプション)。 この値は、アイテムのタイプを定義します。

#### <a name="return-value"></a>戻り値

値が構造体に追加された場合は true。値を追加することができなかった場合は (既に構造体に存在していた場合は) false。

#### <a name="remarks"></a>備考

値のタイプは値の内容から推測されます。 構造体内の項目は、項目名に従ってアルファベット順に並べられます。 構造体の項目の値は、Struct.value メソッドまたは Struct.valueIndex メソッドを使用して変更できます。

#### <a name="examples"></a>例

次の例では、名前および年齢フィールドの 2 つの項目を持つ構造体を作成し、それらの項目に値を割り当てます。 その後、add メソッドを使用して、43 という値の shoeSize 変数が追加項目として作成されます。 値のタイプによって、新しい項目のタイプ int が決まります。

    { 
        Struct s = new Struct ("str name; int age"); 
        // Prints number of items (2) 
        print s.fields(); 
        // Values are assigned to the two items 
        s.value("name", "John"); 
        s.value("age", 34); 
        //Another item is added to the struct 
        s.add("shoeSize", 43); 
        // Prints number of item (3) 
        print s.fields(); 
        // Prints a description of the items in the struct 
        print s.definitionString(); 
        pause; 
    }

### <a name="method-definitionstring"></a>メソッド definitionString

構造体の要素の名前およびタイプの説明を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

構造体の定義を含む文字列。

#### <a name="remarks"></a>備考

definitionString メソッドを使用すると、構文 newStruct = new struct(oldStruct.definitionString()); を用いて構造体のコピーを作成することができます。

### <a name="method-exists"></a>メソッド exists

特定の項目が構造体に存在するかどうかを判定します。

    public boolean exists(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  
チェックするアイテムの名前。

#### <a name="return-value"></a>戻り値

項目が構造体内に存在する場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、特定の項目が構造体に存在するかどうかを検査し、存在しない場合は、項目を追加し、Struct.add メソッドを使用して項目に値を割り当てます。

    client server static void setProp( 
        Struct     properties, 
        str        name, 
        anytype   value 
        ) 
    { 
        if (! properties.exists(name)) 
        { 
            properties.add(name,nullValue(value)); 
        } 
        properties.value(name,value); 
    }

### <a name="method-fieldname"></a>メソッド fieldName

指定された位置にある構造体内の項目の名前を返します。

    public str fieldName(int index)

#### <a name="parameters"></a>パラメーター

指数  
項目名を取得する構造体内の位置。

#### <a name="return-value"></a>戻り値

インデックスで指定された位置にある項目の名前。

#### <a name="remarks"></a>備考

インデックスが見つからない場合は、空の文字列が返されます。

#### <a name="examples"></a>例

次の例では、コンテナーから構造体を作成し、Struct.fields メソッドを使用してコンテナーの内容を反復処理します。 fieldName メソッドは、構造体の各項目の名前をテストするために使用され、この名前の値に応じて特定のアクションが実行されます。

    boolean unpack(container packed) 
    { 
        Struct      unpackedProperties; 
        container   structCon; 
        Counter     i; 
        [#currentList,structCon] = packed; 
        unpackedProperties = Struct::create(structCon); 
        for (i=1;i<=unpackedProperties.fields();i++) 
        { 
            switch (unpackedProperties.fieldName(i)) 
            { 
                case #closedOk: 
                    break; 
                case #PropertyCaption: 
                    if (! dialogForm  
                        || dialogForm  
                        && ! dialogForm.form().design().caption()) 
                        this.caption(unpackedProperties.valueIndex(i)); 
                    break; 
                case #dialogFormname: 
                    // Do nothing 
                    break; 
                case #PropertyAlwaysOnTop: 
                    this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                    break; 
                case #PropertyWindowType: 
                    this.windowType(unpackedProperties.valueIndex(i)); 
                    break; 
                case #defaultButton: 
                    this.defaultButton(unpackedProperties.valueIndex(i)); 
                    break; 
                default: 
                    throw error(strfmt( 
                        "@SYS67326",unpackedProperties.fieldName(i), 
                         classId2Name(classidget(this)))); 
            } 
        } 
        return true; 
    }

### <a name="method-fields"></a>メソッド fields

構造体内の項目の数を返します。

    public int fields()

#### <a name="return-value"></a>戻り値

構造体内の項目の数。

#### <a name="remarks"></a>備考

構造体内の項目の位置を見つけるには、Struct.index メソッドを使用します。

#### <a name="examples"></a>例

次の例では、コンテナーから構造体を作成し、フィールド メソッドを使用してコンテナーの内容を反復処理します。

    boolean unpack(container packed) 
    { 
        Struct      unpackedProperties; 
        container   structCon; 
        Counter     i; 
        [#currentList,structCon] = packed; 
        unpackedProperties = Struct::create(structCon); 
        for (i=1;i<=unpackedProperties.fields();i++) 
        { 
            switch (unpackedProperties.fieldName(i)) 
            { 
                case #closedOk: 
                    break; 
                case #PropertyCaption: 
                    if (! dialogForm  
                        || dialogForm  
                        && ! dialogForm.form().design().caption()) 
                        this.caption(unpackedProperties.valueIndex(i)); 
                    break; 
                case #dialogFormname: 
                    // Do nothing 
                    break; 
                case #PropertyAlwaysOnTop: 
                    this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                    break; 
                case #PropertyWindowType: 
                    this.windowType(unpackedProperties.valueIndex(i)); 
                    break; 
                case #defaultButton: 
                    this.defaultButton(unpackedProperties.valueIndex(i)); 
                    break; 
                default: 
                    throw error(strfmt( 
                        "@SYS67326",unpackedProperties.fieldName(i), 
                         classId2Name(classidget(this)))); 
            } 
        } 
        return true; 
    }

### <a name="method-fieldtype"></a>メソッド fieldType

指定された位置にある構造体内の項目のデータ型を返します。

    public Types fieldType(int index)

#### <a name="parameters"></a>パラメーター

指数  
データ型を取得する構造体内の位置。

#### <a name="return-value"></a>戻り値

インデックスで指定された位置にある項目のデータ型。

#### <a name="remarks"></a>備考

可能な値は、システム列挙で提供されます。 インデックスが見つからない場合は、返す値は Types::void です。 Struct.index メソッドを使用することにより、構造体内の特定の品目の位置を決定することができます。

### <a name="method-index"></a>メソッド index

名前に基づいて構造体の項目の位置を計算します。

    public int index(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  
位置を返す項目の名前。

#### <a name="return-value"></a>戻り値

項目の位置。

#### <a name="remarks"></a>備考

構造体内の項目は、項目名に従ってアルファベット順に並べられます。 fieldName という名前の項目がない場合は、0 が返されます。

### <a name="method-pack"></a>メソッド pack

Struct クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

Struct クラスの現在のインスタンスを含むコンテナーです。

#### <a name="remarks"></a>備考

pack メソッドは、オブジェクトを保持する各フィールドで呼び出され、(サブ) コンテナーを生成します。 構造体は、Struct.create メソッドを使用してコンテナーから再作成できます。

#### <a name="examples"></a>例

次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。 構造体はコンテナーに梱包され、このコンテナーが使用されて新しい構造体が作成されます。

    {  
        container packedStruct;  
        Struct s1, s = new Struct ("str name; int age"); 
        s.value ("name", "Jane Dow");  
        s.value ("age", 34); 
        // Struct is packed into a container 
        packedStruct = s.pack();  
        // A new struct is created from the container 
        s1 = Struct::create(packedStruct); 
        // Both structs have the same contents 
        print s.toString();  
        print s1.toString();  
        pause;  
    }

### <a name="method-remove"></a>メソッド remove

構造体から品目を削除します。

    public boolean remove(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  
削除する項目の名前。

#### <a name="return-value"></a>戻り値

項目が見つかった (そして削除された) 場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

fieldName パラメーターに指定する名前は、構造体のインスタンス化で指定されたアイテムの名前または Struct.add メソッドを使用して追加されたアイテムの名前でなければなりません。 名前は引用符 (" ") で囲む必要があります。

#### <a name="examples"></a>例

次の例では、2 つの項目を含む構造体を作成し、これらの項目の説明を出力します。 品目のいずれかは、メソッドの削除を使用して削除されます。

    { 
        Struct s = new Struct ("str name; int age"); 
        // Values are assigned to the two items 
        s.value("name", "John"); 
        s.value("age", 34); 
        // Prints a description of the items in the struct 
        print s.definitionString(); 
        pause; 
        // Removes the name field 
        s.remove("name"); 
        // Describes remaining items in the struct 
        print s.definitionString(); 
        pause; 
    }

### <a name="method-tostring"></a>メソッド toString

構造体の内容を説明する文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

構造体の内容を説明する文字列。

### <a name="method-value"></a>メソッド value

構造体で指定される品目の値を取得または設定します。

    public AnyType value(str fieldName, [AnyType value])

#### <a name="parameters"></a>パラメーター

fieldName  
項目に割り当てる値 (オプション)。

<!-- -->

値  
項目に割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

指定項目の値。

#### <a name="remarks"></a>備考

構造体内で指定された名前に項目がない場合は例外が発生します。 構造体内の項目名は、Struct.fieldName メソッドを使用して取得できます。 Struct.add メソッドを使用することにより、新しい品目を構造体に追加すると同時に値を割り当てることができます。 構造体内の位置に基づいてアイテムに新しい値を割り当てるには、Struct.valueIndex メソッドを使用します。

#### <a name="examples"></a>例

次の例では、2 つの項目を含む構造体を作成し、value メソッドを使用してこれらの 2 つの項目に値を割り当てます。

    { 
        Struct s = new Struct ("str name; int age"); 
        // Set the values 
        s.value("name", "Jane Dow"); 
        s.value("age", 34); 
        // Print the values 
        print s.value("name"); 
        print s.value("age"); 
        pause; 
    }

### <a name="method-valueimage"></a>メソッド valueImage

構造体内の特定の位置にある品目の値を説明する文字列を返します。

    public str valueImage(int index)

#### <a name="parameters"></a>パラメーター

指数  
説明を返す項目の位置。

#### <a name="return-value"></a>戻り値

品目の価値を説明する文字列。

#### <a name="remarks"></a>備考

構造体内の項目は、項目の名前に従ってアルファベット順に表示されます。 インデックスで指定された位置に項目がない場合は例外が発生します。

### <a name="method-valueindex"></a>メソッド valueIndex

構造体で指定される位置での品目の値を取得または設定します。

    public AnyType valueIndex(int index, [AnyType value])

#### <a name="parameters"></a>パラメーター

指数  
インデックスで指定された位置のアイテムに割り当てる値 (オプション)。

<!-- -->

値  
インデックスで指定された位置のアイテムに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

インデックスで指定された位置にある項目の値。

#### <a name="remarks"></a>備考

インデックスで指定された位置に項目がない場合は例外が発生します。 構造体内の項目の位置は、Struct.index メソッドを使用して取得できます。

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
返された XML 文字列のインデントの量 (省略可能)。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-create"></a>メソッド create

以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。

    public static Struct create(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  
梱包済みの構造体を含むコンテナーです。

#### <a name="return-value"></a>戻り値

特定のコンテナーに梱包されたものと同じ構造体。

#### <a name="remarks"></a>備考

構造体にオブジェクトが含まれている場合、これらのオブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

#### <a name="examples"></a>例

次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。 構造体はコンテナーに梱包され、このコンテナーは開梱されて新しい構造体が作成されます。

    {  
        container packedStruct;  
        Struct s1, s = new Struct ("str name; int age"); 
        s.value ("name", "Jane Dow");  
        s.value ("age", 34); 
        // Struct is packed into a container 
        packedStruct = s.pack();  
        // A new struct is created from the container 
        s1 = Struct::create(packedStruct); 
        // Both structs have the same contents 
        print s.toString();  
        print s1.toString();  
        pause;  
    }

### <a name="method-createfromxml"></a>メソッド createFromXML

    public static Struct createFromXML(Object xmlnode)

#### <a name="parameters"></a>パラメーター

xmlnode  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

2 つの構造体が等しいかどうかを判断します。

    public static boolean equal(Struct struct1, Struct struct2)

#### <a name="parameters"></a>パラメーター

struct1  
比較される 2 つの構造体のうちの 2 番目の構造体。

<!-- -->

struct2  
比較される 2 つの構造体のうちの 2 番目の構造体。

#### <a name="return-value"></a>戻り値

構造体が等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

同じ数のフィールドを持ち、フィールド名が同じで、各フィールドが同じ型で同じ値を持つ場合、2 つの構造体は同等です。

### <a name="method-merge"></a>メソッド merge

2 つの構造体を組み合わせ、新しい構造体を作成します。

    public static Struct merge(Struct struct1, Struct struct2)

#### <a name="parameters"></a>パラメーター

struct1  
新しい構造体を作成するために最初の構造体の最後に追加される構造体。

<!-- -->

struct2  
新しい構造体を作成するために最初の構造体の最後に追加される構造体。

#### <a name="return-value"></a>戻り値

新しい構造体。

#### <a name="remarks"></a>備考

struct2 は struct1 の最後に追加されます。 つまり、新しい構造体の項目の順序は、項目名のアルファベット順に並べられた struct1 のすべての項目と、項目名のアルファベット順に並べられた struct2 のすべての項目です。 両方の構造体に同じ名前を持つ品目が含まれている場合は、最初の構造体からの品目のみが含まれるようになります。

#### <a name="examples"></a>例

次の例では、person と address という 2 つの構造体を作成し、それらを allInfo という新しい構造体にマージします。

    { 
        container packedStruct; 
        Struct person = new Struct ("str name; int age"); 
        Struct address = new Struct ("str street; str city; str country"); 
        Struct allInfo; 
        person.value ("name", "Jane Dow"); 
        person.value ("age", 34); 
        address.value ("street", "Downing street 10"); 
        address.value ("country", "Great Britain"); 
        address.value ("city", " London"); 
        allInfo = Struct::merge(person, address); 
        print allInfo.toString(); 
        pause; 
    }

### <a name="method-new"></a>メソッド new

構造体を作成します。

    public void new(VarArg specifier)

#### <a name="parameters"></a>パラメーター

指定子  
文字列として品目の名前の後には、品目のデータ型を指定した 1 つ以上の組み合わせ。

#### <a name="remarks"></a>備考

項目のデータ型は、プリミティブ データ型の名前を使用するか、システム列挙を使用して指定できます。 構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。 以下の例に説明されているように、Struct.definitionString メソッドを使用して新しい構造体を作成し、構造体のコピーを作成することができます。 構造体を作成した後は、Struct.add メソッドを使用して新しい項目を追加し、Struct.value または Struct.valueIndex メソッドを使用して構造体に項目の値を設定することができます。

#### <a name="examples"></a>例

次の例では、同じ定義を持つ 2 つの構造体を作成し、2 つの値と追加の項目および値をその 1 つ (s1) に追加します。 この構造体をコピーして、Struct.definitionString メソッドを使用することにより新しい構造体を作成します。

    { 
        Struct s1, s2, s3; 
        // The two constructors below create the same struct 
        s1 = new Struct(Types::Integer, "age", Types::String, "name"); 
        s2 = new Struct ("int age; str name"); 
        // Print the definitions 
        print s1.definitionString(); 
        print s2.definitionString(); 
        s1.value("age", 25); 
        s1.value("name", "Jane Dow"); 
        // Add a field at runtime 
        s1.add("Shoesize", 45); 
        print s1.definitionString(); 
        print s1.toString(); 
        // Create a container with age, name and shoesize, 
        // using definitionString 
        s3 = new struct(s1.definitionString()); 
        print s3.definitionString(); 
        pause; 
    }

## <a name="class-surrogatefkreplacementhelper"></a>クラス SurrogateFKReplacementHelper
    class SurrogateFKReplacementHelper extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                             | 説明                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)                                                                                             |                                                 |
| public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)                                                              |                                                 |
| public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])                                                                                                                       |                                                 |
| public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])                   |                                                 |
| public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])                                                               |                                                 |
| public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\]) |                                                 |
| public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])                                                                                        |                                                 |
| public str extendedDataType()                                                                                                                                                                                      |                                                 |
| public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)                                                                                               |                                                 |
| public boolean isResolvedReferenceAmbiguous(Query query)                                                                                                                                                           |                                                 |
| public str primaryKeyTableName()                                                                                                                                                                                   |                                                 |
| public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])                                                                                |                                                 |
| public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)                                                     |                                                 |
| public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])                                                                                                                                  |                                                 |
| public FieldBinding surrogateForeignKeyFieldBinding()                                                                                                                                                              |                                                 |
| ::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)                                                                                                                    |                                                 |
| ::public static SurrogateFKReplacementHelper constructForEDT(str edtName)                                                                                                                                          |                                                 |
| ::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)                                                                                                                                  |                                                 |
| ::public static str defaultPrimaryKeyQueryDataSourceName()                                                                                                                                                         |                                                 |
| ::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)                                                                                                                    |                                                 |
| ::public static str implicitReplacementFieldGroupName()                                                                                                                                                            |                                                 |
| private void new(FieldBinding surrogateForeignKeyBinding)                                                                                                                                                          | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-adddefaultrequiredjoins"></a>メソッド addDefaultRequiredJoins

    public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a>パラメーター

foreignKeyQueryBuildDataSource  

<!-- -->

replacementFieldGroupName  

#### <a name="return-value"></a>戻り値

### <a name="method-addrequiredjoins"></a>メソッド addRequiredJoins

    public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a>パラメーター

requiredJoinsAsRelationPathList  

<!-- -->

foreignKeyQueryBuildDataSource  

<!-- -->

replacementFieldGroupName  

#### <a name="return-value"></a>戻り値

### <a name="method-displaybindings"></a>メソッド displayBindings

    public List displayBindings(str replacementFieldGroupName, [boolean distinctBindingsOnly])

#### <a name="parameters"></a>パラメーター

replacementFieldGroupName  

<!-- -->

distinctBindingsOnly  

#### <a name="return-value"></a>戻り値

### <a name="method-displayvaluesfromqueryrun"></a>メソッド displayValuesFromQueryRun

    public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource], [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a>パラメーター

queryRun  

<!-- -->

replacementFieldGroupName  

<!-- -->

isRootPrimaryKeyDataSource  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

#### <a name="return-value"></a>戻り値

### <a name="method-displayvaluesfromrecid"></a>メソッド displayValuesFromRecID

    public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a>パラメーター

recIDValue  

<!-- -->

replacementFieldGroupName  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

#### <a name="return-value"></a>戻り値

### <a name="method-displayvaluesfromrootds"></a>メソッド displayValuesFromRootDS

    public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a>パラメーター

rootQueryBuildDataSource  

<!-- -->

isPrimaryKeyDataSource  

<!-- -->

replacementFieldGroupName  

<!-- -->

trimSecuredValues  

<!-- -->

distinctBindingsOnly  

#### <a name="return-value"></a>戻り値

### <a name="method-displayvalue"></a>メソッド displayValue

    public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, [boolean isRootPrimaryKeyDataSource])

#### <a name="parameters"></a>パラメーター

resolvedCursor  

<!-- -->

displayBinding  

<!-- -->

isRootPrimaryKeyDataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public str extendedDataType()

#### <a name="return-value"></a>戻り値

### <a name="method-generateresolvereferencequery"></a>メソッド generateResolveReferenceQuery

    public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)

#### <a name="parameters"></a>パラメーター

requiredJoinsAsRelationPathList  

<!-- -->

filterValuesAsFilterValueList  

#### <a name="return-value"></a>戻り値

### <a name="method-isresolvedreferenceambiguous"></a>メソッド isResolvedReferenceAmbiguous

    public boolean isResolvedReferenceAmbiguous(Query query)

#### <a name="parameters"></a>パラメーター

クエリ  

#### <a name="return-value"></a>戻り値

### <a name="method-primarykeytablename"></a>メソッド primaryKeyTableName

    public str primaryKeyTableName()

#### <a name="return-value"></a>戻り値

### <a name="method-querybuilddatasourcebindingsforquery"></a>メソッド queryBuildDataSourceBindingsForQuery

    public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource])

#### <a name="parameters"></a>パラメーター

クエリ  

<!-- -->

replacementFieldGroupName  

<!-- -->

isRootPrimaryKeyDataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-querybuilddatasourcebindingsforrootds"></a>メソッド queryBuildDataSourceBindingsForRootDS

    public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a>パラメーター

rootQueryBuildDataSource  

<!-- -->

isPrimaryKeyDataSource  

<!-- -->

replacementFieldGroupName  

#### <a name="return-value"></a>戻り値

### <a name="method-resolvereference"></a>メソッド resolveReference

    public Common resolveReference(Query query, [boolean ignoreAmbiguousReference])

#### <a name="parameters"></a>パラメーター

クエリ  

<!-- -->

ignoreAmbiguousReference  

#### <a name="return-value"></a>戻り値

### <a name="method-surrogateforeignkeyfieldbinding"></a>メソッド surrogateForeignKeyFieldBinding

    public FieldBinding surrogateForeignKeyFieldBinding()

#### <a name="return-value"></a>戻り値

### <a name="method-construct"></a>メソッド construct

    public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)

#### <a name="parameters"></a>パラメーター

surrogateForeignKeyBinding  

#### <a name="return-value"></a>戻り値

### <a name="method-constructforedt"></a>メソッド constructForEDT

    public static SurrogateFKReplacementHelper constructForEDT(str edtName)

#### <a name="parameters"></a>パラメーター

edtName  

#### <a name="return-value"></a>戻り値

### <a name="method-constructforpktable"></a>メソッド constructForPKTable

    public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)

#### <a name="parameters"></a>パラメーター

pkTableName  

#### <a name="return-value"></a>戻り値

### <a name="method-defaultprimarykeyquerydatasourcename"></a>メソッド defaultPrimaryKeyQueryDataSourceName

    public static str defaultPrimaryKeyQueryDataSourceName()

#### <a name="return-value"></a>戻り値

### <a name="method-deprecated_workflowcaption"></a>メソッド DEPRECATED\_WorkflowCaption

    public static str DEPRECATED_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)

#### <a name="parameters"></a>パラメーター

tableName  

<!-- -->

fieldName  

<!-- -->

recIDValue  

#### <a name="return-value"></a>戻り値

### <a name="method-implicitreplacementfieldgroupname"></a>メソッド implicitReplacementFieldGroupName

    public static str implicitReplacementFieldGroupName()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    private void new(FieldBinding surrogateForeignKeyBinding)

#### <a name="parameters"></a>パラメーター

surrogateForeignKeyBinding  

## <a name="class-sysglobalobjectcache"></a>クラス SysGlobalObjectCache
    class SysGlobalObjectCache extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                           | 説明                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| public container find(GlobalObjectCacheScope scope, container key)               |                                                               |
| public void finalize()                                                           |                                                               |
| public void remove(GlobalObjectCacheScope scope, container key)                  |                                                               |
| public void print(GlobalObjectCacheScope scope)                                  |                                                               |
| public void clear(GlobalObjectCacheScope scope)                                  |                                                               |
| ::public static void clearAllCaches()                                            |                                                               |
| public void new()                                                                | SysGlobalObjectCache クラスの新しいインスタンスを初期化します。 |
| public void insert(GlobalObjectCacheScope scope, container key, container value) |                                                               |

### <a name="method-find"></a>メソッド find

    public container find(GlobalObjectCacheScope scope, container key)

#### <a name="parameters"></a>パラメーター

scope  

<!-- -->

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-remove"></a>メソッド remove

    public void remove(GlobalObjectCacheScope scope, container key)

#### <a name="parameters"></a>パラメーター

scope  

<!-- -->

キー  

### <a name="method-print"></a>メソッド print

    public void print(GlobalObjectCacheScope scope)

#### <a name="parameters"></a>パラメーター

scope  

### <a name="method-clear"></a>メソッド clear

    public void clear(GlobalObjectCacheScope scope)

#### <a name="parameters"></a>パラメーター

scope  

### <a name="method-clearallcaches"></a>メソッド clearAllCaches

    public static void clearAllCaches()

### <a name="method-new"></a>メソッド new

SysGlobalObjectCache クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-insert"></a>メソッド insert

    public void insert(GlobalObjectCacheScope scope, container key, container value)

#### <a name="parameters"></a>パラメーター

scope  

<!-- -->

キー  

<!-- -->

値  

## <a name="class-systemmonitor"></a>クラス SystemMonitor
    class SystemMonitor extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>方法

| 方法                                                                | 説明                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------|
| ::public static container allClientCounters()                         |                                                        |
| ::public static container allServerCounters()                         |                                                        |
| ::public static int getClientCounter(SystemMonitorCounter counter)    |                                                        |
| ::public static container getClientInternals()                        |                                                        |
| ::public static int getCounter(SystemMonitorCounter counter)          |                                                        |
| ::public static int getServerCounter(SystemMonitorCounter counter)    |                                                        |
| ::public static container getServerInternals()                        |                                                        |
| ::public static boolean isRunning()                                   |                                                        |
| ::public static boolean isServerCounter(SystemMonitorCounter counter) |                                                        |
| ::public static container sqlDump()                                   |                                                        |
| ::public static void systemDump(boolean includeSQL)                   |                                                        |
| ::public static void start()                                          |                                                        |
| ::public static void resetServer()                                    |                                                        |
| ::public static void stop()                                           |                                                        |
| public void new()                                                     | SystemMonitor クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                |                                                        |
| ::public static void reset()                                          |                                                        |
| ::public static void resetClient()                                    |                                                        |

### <a name="method-allclientcounters"></a>メソッド allClientCounters

    public static container allClientCounters()

#### <a name="return-value"></a>戻り値

### <a name="method-allservercounters"></a>メソッド allServerCounters

    public static container allServerCounters()

#### <a name="return-value"></a>戻り値

### <a name="method-getclientcounter"></a>メソッド getClientCounter

    public static int getClientCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a>パラメーター

counter  

#### <a name="return-value"></a>戻り値

### <a name="method-getclientinternals"></a>メソッド getClientInternals

    public static container getClientInternals()

#### <a name="return-value"></a>戻り値

### <a name="method-getcounter"></a>メソッド getCounter

    public static int getCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a>パラメーター

counter  

#### <a name="return-value"></a>戻り値

### <a name="method-getservercounter"></a>メソッド getServerCounter

    public static int getServerCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a>パラメーター

counter  

#### <a name="return-value"></a>戻り値

### <a name="method-getserverinternals"></a>メソッド getServerInternals

    public static container getServerInternals()

#### <a name="return-value"></a>戻り値

### <a name="method-isrunning"></a>メソッド isRunning

    public static boolean isRunning()

#### <a name="return-value"></a>戻り値

### <a name="method-isservercounter"></a>メソッド isServerCounter

    public static boolean isServerCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a>パラメーター

counter  

#### <a name="return-value"></a>戻り値

### <a name="method-sqldump"></a>メソッド sqlDump

    public static container sqlDump()

#### <a name="return-value"></a>戻り値

### <a name="method-systemdump"></a>メソッド systemDump

    public static void systemDump(boolean includeSQL)

#### <a name="parameters"></a>パラメーター

includeSQL  

### <a name="method-start"></a>メソッド start

    public static void start()

### <a name="method-resetserver"></a>メソッド resetServer

    public static void resetServer()

### <a name="method-stop"></a>メソッド stop

    public static void stop()

### <a name="method-new"></a>メソッド new

SystemMonitor クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-reset"></a>メソッド reset

    public static void reset()

### <a name="method-resetclient"></a>メソッド resetClient

    public static void resetClient()

## <a name="class-systemsequence"></a>クラス systemSequence
    class systemSequence extends Object

systemSequence クラスは、システム シーケンス ジェネレータを手動で制御し、すべての SQL テーブルに対して一意の RecIds を提供します。

### <a name="remarks"></a>備考

SQL テーブルにレコードが挿入されると、各レコードが関連付けられている会社に関係なく、各レコードに一意の RecId が割り当てられます。 このクラスを使用するときは十分に注意してください。データの整合性が失われる可能性があります。 このクラスは、通常、データのインポートやエクスポート ルーチン、または非常に大きなジョブに使用されます。 レコード ID は、int64 データ型の値です。 レコード ID が割り当てられる範囲は、5637144576 から 2 ^ 63 (9223372036854775808) までです。 大きい未使用の RecId 範囲が作成された場合、途中で RecId がなくなることがあります。 使用されている Recid 範囲の間にある未使用の RecId 範囲を再利用するのは、非常に複雑なプロセスです。

### <a name="examples"></a>例

次の例では、CustTable テーブルの int64max 値を予約しています。

    static public void Main(Args _args) 
    { 
        systemSequence seq; 
        seq = new SystemSequence(); 
        if (seq) 
        { 
            // Allocate 20 recordIds for CustTable table. 
            seq.reserveValues(20, tablenum(CustTable)); 
            // Suspend automatic recId allocation. 
            Seq.suspendRecIds(tablenum(CustTable)); 
            // Manually generate recIds in the range allocated. 
            // Remove the recId suspension. 
            Seq.removeRecIdSuspension(); 
          } 
    }

### <a name="methods"></a>メソッド

| 方法                                                             | 説明                                                                                                                     |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| public Int64 flushValues(TableId tableId)                          | 指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。                                                    |
| public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\]) |                                                                                                                                 |
| public Int64 reserveValues(Int64 nReserved, TableId tableId)       | recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。 |
| public void suspendTransIds(TableId tableId)                       |                                                                                                                                 |
| public void suspendRecIds(TableId tableId)                         |                                                                                                                                 |
| public void removeRecIdSuspension(\[TableId tableId\])             |                                                                                                                                 |
| public void new()                                                  | systemSequence クラスの新しいインスタンスを初期化します。                                                                         |
| public void removeTransIdSuspension(\[TableId tableId\])           |                                                                                                                                 |

### <a name="method-flushvalues"></a>メソッド flushValues

指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。

    public Int64 flushValues(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

#### <a name="return-value"></a>戻り値

キャッシュからフラッシュされた recIds の数。

#### <a name="remarks"></a>備考

テーブルへのその後挿入によりテーブルの recId が予約され、システム シーケンス キャッシュにはテーブルの recId の予約済み範囲が入力されます。

### <a name="method-reservetransids"></a>メソッド reserveTransids

    public Int64 reserveTransids(Int64 nReserved, [TableId tableId])

#### <a name="parameters"></a>パラメーター

nReserved  

<!-- -->

tableId  

#### <a name="return-value"></a>戻り値

### <a name="method-reservevalues"></a>メソッド reserveValues

recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。

    public Int64 reserveValues(Int64 nReserved, TableId tableId)

#### <a name="parameters"></a>パラメーター

nReserved  

<!-- -->

tableId  

#### <a name="return-value"></a>戻り値

最初に使用可能な予約済み recId。

#### <a name="remarks"></a>備考

予約した recIds の範囲は、すぐに予約されています。

### <a name="method-suspendtransids"></a>メソッド suspendTransIds

    public void suspendTransIds(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-suspendrecids"></a>メソッド suspendRecIds

    public void suspendRecIds(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-removerecidsuspension"></a>メソッド removeRecIdSuspension

    public void removeRecIdSuspension([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  

### <a name="method-new"></a>メソッド new

systemSequence クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-removetransidsuspension"></a>メソッド removeTransIdSuspension

    public void removeTransIdSuspension([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  





