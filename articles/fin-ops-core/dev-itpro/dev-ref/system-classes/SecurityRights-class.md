---
title: SecurityRights クラス
description: このトピックでは、SecurityRights クラスについて説明します。
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
ms.openlocfilehash: 9fe35b199959089ca2b9e8e9e7acfa846c77db6c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502811"
---
# <a name="class-securityrights"></a>クラス SecurityRights

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityRights extends Object
```

SecurityRights クラスには、セキュリティの権利とアクセス許可の管理に関する情報が含まれます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-hasdataserviceaccess"></a>メソッド hasDataServiceAccess

```xpp
public boolean hasDataServiceAccess(SecurableName name, StatementType operation, [SecurableChildName fieldName])
```

### <a name="parameters---hasdataserviceaccess"></a>パラメーター - hasDataServiceAccess

名前  

<!-- -->

工程  

<!-- -->

fieldName  

### <a name="return-value---hasdataserviceaccess"></a>戻り値 - hasDataServiceAccess

## <a name="method-hasdataservicemethodaccess"></a>メソッド hasDataServiceMethodAccess

```xpp
public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)
```

### <a name="parameters---hasdataservicemethodaccess"></a>パラメーター - hasDataServiceMethodAccess

名前  

<!-- -->

工程  

<!-- -->

methodName  

### <a name="return-value---hasdataservicemethodaccess"></a>戻り値 - hasDataServiceMethodAccess

## <a name="method-datamanagementaccessright"></a>メソッド dataManagementAccessRight

```xpp
public AccessRight dataManagementAccessRight(SecurableName dataEntityName, [SecurableChildName fieldName])
```

### <a name="parameters---datamanagementaccessright"></a>パラメーター - dataManagementAccessRight

dataEntityName  

<!-- -->

fieldName  

### <a name="return-value---datamanagementaccessright"></a>戻り値 - dataManagementAccessRight

## <a name="method-listdataserviceaccess"></a>メソッド listDataServiceAccess

```xpp
public str listDataServiceAccess(SecurableName name, [SecurableChildName context])
```

### <a name="parameters---listdataserviceaccess"></a>パラメーター - listDataServiceAccess

名前  

<!-- -->

context  

### <a name="return-value---listdataserviceaccess"></a>戻り値 - listDataServiceAccess

## <a name="method-fieldaccessright"></a>メソッド fieldAccessRight

テーブルのフィールドのアクセス権を取得します。

```xpp
public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---fieldaccessright"></a>パラメーター - fieldAccessRight

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

### <a name="return-value---fieldaccessright"></a>戻り値 - fieldAccessRight

テーブルのフィールドの AccesRight インスタンス。

## <a name="method-formcontrolaccessright"></a>メソッド formControlAccessRight

フォーム コントロールのアクセス権を取得します。

```xpp
public AccessRight formControlAccessRight(FormName form, UtilElementName control, [Common record], [DataAreaId dataArea])
```

### <a name="parameters---formcontrolaccessright"></a>パラメーター - formControlAccessRight

フォーム  

<!-- -->

control  

<!-- -->

記録  

<!-- -->

dataArea  

### <a name="return-value---formcontrolaccessright"></a>戻り値 - formControlAccessRight

フォーム コントロールの AccesRight インスタンス。

## <a name="method-getselectablecompanies"></a>メソッド getSelectableCompanies

```xpp
public container getSelectableCompanies()
```

### <a name="return-value---getselectablecompanies"></a>戻り値 - getSelectableCompanies

## <a name="method-hasmenuaccess"></a>メソッド hasMenuAccess

ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。

```xpp
public boolean hasMenuAccess(MenuName menu, [boolean isWebMenu])
```

### <a name="parameters---hasmenuaccess"></a>パラメーター - hasMenuAccess

メニュー  

<!-- -->

isWebMenu  

### <a name="return-value---hasmenuaccess"></a>戻り値 - hasMenuAccess

ユーザーがメニューへのアクセス権を持つ場合は true。それ以外の場合は、false。

## <a name="method-hasmenuitemaccess"></a>メソッド hasMenuItemAccess

ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。

```xpp
public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, [Common record], [DataAreaId dataArea])
```

### <a name="parameters---hasmenuitemaccess"></a>パラメーター - hasMenuItemAccess

タイプ  

<!-- -->

menuItem  

<!-- -->

記録  

<!-- -->

dataArea  

### <a name="return-value---hasmenuitemaccess"></a>戻り値 - hasMenuItemAccess

ユーザーがメニュー項目へのアクセス権を持つ場合は true。それ以外の場合は、false。

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute(ClassName class, MethodName method)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

クラス  

<!-- -->

メソッド  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-hasserviceoperationaccess"></a>メソッド hasServiceOperationAccess

ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。

```xpp
public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)
```

### <a name="parameters---hasserviceoperationaccess"></a>パラメーター - hasServiceOperationAccess

サービス  

<!-- -->

工程  

### <a name="return-value---hasserviceoperationaccess"></a>戻り値 - hasServiceOperationAccess

ユーザーがサービス操作へのアクセス権を持つ場合は true。それ以外の場合は、false。

## <a name="method-isdeveloper"></a>メソッド isDeveloper

```xpp
public boolean isDeveloper()
```

### <a name="return-value---isdeveloper"></a>戻り値 - isDeveloper

## <a name="method-issystemadministrator"></a>メソッド isSystemAdministrator

現在のユーザーがシステム管理者であるかどうかを確認します。

```xpp
public boolean isSystemAdministrator()
```

### <a name="return-value---issystemadministrator"></a>戻り値 - isSystemAdministrator

現在のユーザーがシステム管理者である場合は true。それ以外の場合は、false。

## <a name="method-menuitemaccessright"></a>メソッド menuItemAccessRight

メニュー項目のアクセス権を取得します。

```xpp
public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, [DataAreaId dataArea])
```

### <a name="parameters---menuitemaccessright"></a>パラメーター - menuItemAccessRight

タイプ  

<!-- -->

menuItem  

<!-- -->

dataArea  

### <a name="return-value---menuitemaccessright"></a>戻り値 - menuItemAccessRight

項目の AccesRight インスタンス。

## <a name="method-tableaccessright"></a>メソッド tableAccessRight

テーブルのアクセス権を取得します。

```xpp
public AccessRight tableAccessRight(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---tableaccessright"></a>パラメーター - tableAccessRight

tableName  

<!-- -->

記録  

<!-- -->

dataArea  

<!-- -->

includeDerived  

<!-- -->

autoAuthzMode  

### <a name="return-value---tableaccessright"></a>戻り値 - tableAccessRight

テーブルの AccesRight インスタンス。

## <a name="method-tablefieldaccessrights"></a>メソッド tableFieldAccessRights

テーブルのフィールド アクセス権を取得します。

```xpp
public SecurityTableRights tableFieldAccessRights(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---tablefieldaccessrights"></a>パラメーター - tableFieldAccessRights

tableName  

<!-- -->

記録  

<!-- -->

dataArea  

<!-- -->

includeDerived  

<!-- -->

autoAuthzMode  

### <a name="return-value---tablefieldaccessrights"></a>戻り値 - tableFieldAccessRights

テーブルの SecurityTableRights インスタンス。

## <a name="method-variableaccessfields"></a>メソッド variableAccessFields

一連のテーブル フィールド ID を取得します。

```xpp
public Set variableAccessFields(TableName tableName, [AccessRight targetAccess], [DataAreaId dataArea])
```

### <a name="parameters---variableaccessfields"></a>パラメーター - variableAccessFields

tableName  

<!-- -->

targetAccess  

<!-- -->

dataArea  

### <a name="return-value---variableaccessfields"></a>戻り値 - variableAccessFields

一連のテーブル フィールド ID。

## <a name="method-webcontentaccessright"></a>メソッド webContentAccessRight

Web コンテンツ項目のアクセス権を取得します。

```xpp
public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)
```

### <a name="parameters---webcontentaccessright"></a>パラメーター - webContentAccessRight

タイプ  

<!-- -->

名前  

### <a name="return-value---webcontentaccessright"></a>戻り値 - webContentAccessRight

項目の AccesRight インスタンス。

## <a name="method-construct"></a>メソッド construct

現在のユーザーの新しいセキュリティ権限インスタンスを作成します。

```xpp
public static SecurityRights construct()
```

### <a name="return-value---construct"></a>戻り値 - construct

作成された SecurityRights インスタンスです。

## <a name="method-newuser"></a>メソッド newUser

特定のユーザーの新しいセキュリティ権限インスタンスを作成します。

```xpp
public static SecurityRights newUser(UserId user)
```

### <a name="parameters---newuser"></a>パラメーター - newUser

ユーザー  

### <a name="return-value---newuser"></a>戻り値 - newUser

作成された SecurityRights インスタンスです。

## <a name="method-new"></a>メソッド new

SecurityRights クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

## <a name="method-populateselectablecompanies"></a>メソッド populateSelectableCompanies

選択できる会社を取得します。

```xpp
public void populateSelectableCompanies()
```

