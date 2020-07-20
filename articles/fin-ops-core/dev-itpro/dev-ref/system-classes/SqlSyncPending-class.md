---
title: SqlSyncPending クラス
description: このトピックでは、SqlSyncPending クラスについて説明します。
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
ms.openlocfilehash: 7e19820aaf415e27f1c6da0440df3691e237b624
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502798"
---
# <a name="class-sqlsyncpending"></a>クラス SqlSyncPending

[!include [banner](../../includes/banner.md)]

```xpp
class SqlSyncPending extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-configurationkeytouched"></a>メソッド configurationKeyTouched

```xpp
public ConfigurationKeyId configurationKeyTouched()
```

### <a name="return-value---configurationkeytouched"></a>戻り値 - configurationKeyTouched

## <a name="method-databasetouched"></a>メソッド databaseTouched

```xpp
public boolean databaseTouched([boolean newValue])
```

### <a name="parameters---databasetouched"></a>パラメーター - databaseTouched

newValue  

### <a name="return-value---databasetouched"></a>戻り値 - databaseTouched

## <a name="method-extendeddatatypetouched"></a>メソッド extendedDataTypeTouched

```xpp
public ExtendedTypeId extendedDataTypeTouched()
```

### <a name="return-value---extendeddatatypetouched"></a>戻り値 - extendedDataTypeTouched

## <a name="method-indexestouched"></a>メソッド indexesTouched

```xpp
public TableId indexesTouched()
```

### <a name="return-value---indexestouched"></a>戻り値 - indexesTouched

## <a name="method-relationtouched"></a>メソッド relationTouched

```xpp
public TableId relationTouched()
```

### <a name="return-value---relationtouched"></a>戻り値 - relationTouched

## <a name="method-tabledeleted"></a>メソッド tableDeleted

```xpp
public TableId tableDeleted()
```

### <a name="return-value---tabledeleted"></a>戻り値 - tableDeleted

## <a name="method-tabletouched"></a>メソッド tableTouched

```xpp
public TableId tableTouched()
```

### <a name="return-value---tabletouched"></a>戻り値 - tableTouched

## <a name="method-new"></a>メソッド new

SqlSyncPending クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

