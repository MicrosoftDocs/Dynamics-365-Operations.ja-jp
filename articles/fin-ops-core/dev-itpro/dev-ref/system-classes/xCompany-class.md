---
title: xCompany クラス
description: このトピックでは、xCompany クラスについて説明します。
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
ms.openlocfilehash: 7760ce004fe45ba138e7aa727798d7cbe58ff5bb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502768"
---
# <a name="class-xcompany"></a>クラス xCompany

[!include [banner](../../includes/banner.md)]

```xpp
class xCompany extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                              | 説明                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| public DataAreaId dataArea(TableId tableId)                                         |                                                    |
| public SelectableDataArea ext()                                                     |                                                    |
| public boolean log(DatabaseLogType typeOfLog, TableId tableId, \[FieldId fieldId\]) |                                                    |
| public boolean logAlways(DatabaseLogType typeOfLog, \[boolean log\])                | システム以外のテーブルのログを有効または無効にします。 |
| public boolean reindex(\[TableId tableId\])                                         |                                                    |
| public void reloadLog()                                                             |                                                    |
| public void new(SelectableDataArea company)                                         | Object クラスの新しいインスタンスを初期化します。    |
| public void check()                                                                 |                                                    |
| public void reloadRights()                                                          |                                                    |
| public void flushCache(TableId tableId)                                             |                                                    |
| public void reloadTableCollections()                                                |                                                    |

## <a name="method-dataarea"></a>メソッド dataArea

```xpp
public DataAreaId dataArea(TableId tableId)
```

### <a name="parameters---dataarea"></a>パラメーター - dataArea

tableId  

### <a name="return-value---dataarea"></a>戻り値 - dataArea

## <a name="method-ext"></a>メソッド ext

```xpp
public SelectableDataArea ext()
```

### <a name="return-value---ext"></a>戻り値 - ext

## <a name="method-log"></a>メソッド log

```xpp
public boolean log(DatabaseLogType typeOfLog, TableId tableId, [FieldId fieldId])
```

### <a name="parameters---log"></a>パラメーター - log

typeOfLog  

<!-- -->

tableId  

<!-- -->

fieldId  

### <a name="return-value---log"></a>戻り値 - log

## <a name="method-logalways"></a>メソッド logAlways

システム以外のテーブルのログを有効または無効にします。

```xpp
public boolean logAlways(DatabaseLogType typeOfLog, [boolean log])
```

### <a name="parameters---logalways"></a>パラメーター - logAlways

typeOfLog  

<!-- -->

ログ  

### <a name="return-value---logalways"></a>戻り値 - logAlways

呼び出し前の指定された操作のデータベース ロギングの状況。

### <a name="remarks---logalways"></a>備考 - logAlways

オプションの typeOfLog パラメーターがない場合、このメソッドは指定されたオペレーションのデータベース ログの状態をレポートします。 オプションのパラメーターを指定する場合は、メソッドは CAS で保護されており、呼び出しコードは SysDatabaselogPermission をアサートする必要があることに注意してください。

## <a name="method-reindex"></a>メソッド reindex

```xpp
public boolean reindex([TableId tableId])
```

### <a name="parameters---reindex"></a>パラメーター - reindex

tableId  

### <a name="return-value---reindex"></a>戻り値 - reindex

## <a name="method-reloadlog"></a>メソッド reloadLog

```xpp
public void reloadLog()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(SelectableDataArea company)
```

### <a name="parameters---new"></a>パラメーター - new

会社  

## <a name="method-check"></a>メソッド check

```xpp
public void check()
```

## <a name="method-reloadrights"></a>メソッド reloadRights

```xpp
public void reloadRights()
```

## <a name="method-flushcache"></a>メソッド flushCache

```xpp
public void flushCache(TableId tableId)
```

### <a name="parameters---flushcache"></a>パラメーター - flushCache

tableId  

## <a name="method-reloadtablecollections"></a>メソッド reloadTableCollections

```xpp
public void reloadTableCollections()
```

