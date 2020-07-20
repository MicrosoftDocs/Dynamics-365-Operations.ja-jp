---
title: SecurityUtil クラス
description: このトピックでは、SecurityUtil クラスについて説明します。
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
ms.openlocfilehash: 5c464354beec197104248964067d25be851720a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502810"
---
# <a name="class-securityutil"></a>クラス SecurityUtil

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityUtil extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-isimplicitflushmode"></a>メソッド isImplicitFlushMode

暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。

```xpp
public static boolean isImplicitFlushMode()
```

### <a name="return-value---isimplicitflushmode"></a>戻り値 - isImplicitFlushMode

ブール値。

## <a name="method-getroleeffectiveaccess"></a>メソッド getRoleEffectiveAccess

セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。

```xpp
public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)
```

### <a name="parameters---getroleeffectiveaccess"></a>パラメーター - getRoleEffectiveAccess

roleID  

<!-- -->

secObjectName  

<!-- -->

secObjectType  

<!-- -->

secObjectChildName  

### <a name="return-value---getroleeffectiveaccess"></a>戻り値 - getRoleEffectiveAccess

有効なアクセス値。

## <a name="method-getrolepermissions"></a>メソッド getRolePermissions

セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。

```xpp
public static container getRolePermissions(Int64 roleID)
```

### <a name="parameters---getrolepermissions"></a>パラメーター - getRolePermissions

roleID  
ロール ID。

### <a name="return-value---getrolepermissions"></a>戻り値 - getRolePermissions

セキュリティ保護可能なオブジェクトのコンテナーと、有効なアクセスです。

## <a name="method-sysadminmode"></a>メソッド sysAdminMode

セキュリティ管理者モードを取得および設定します。

```xpp
public static boolean sysAdminMode([boolean active])
```

### <a name="parameters---sysadminmode"></a>パラメーター - sysAdminMode

有効  
ブール値。

### <a name="return-value---sysadminmode"></a>戻り値 - sysAdminMode

セキュリティ管理者モードの古い状態。

## <a name="method-refreshrolepermissions"></a>メソッド refreshRolePermissions

セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。

```xpp
public static void refreshRolePermissions(Int64 roleID)
```

### <a name="parameters---refreshrolepermissions"></a>パラメーター - refreshRolePermissions

roleID  

## <a name="method-runsecondpassautoinference"></a>メソッド runSecondPassAutoInference

2 つ目の合格自動推定が実行されます。

```xpp
public static void runSecondPassAutoInference()
```

## <a name="method-flushpermissions"></a>メソッド flushPermissions

アクセス許可をフラッシュします。

```xpp
public static void flushPermissions()
```

## <a name="method-new"></a>メソッド new

SecurityUtil クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-flushall"></a>メソッド flushAll

```xpp
public static void flushAll()
```

