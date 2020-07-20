---
title: xSqlEnumerator クラス
description: このトピックでは、xSqlEnumerator クラスについて説明します。
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
ms.openlocfilehash: 9dea15217df193f6ac20fc55c01453f50cf12c6d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502755"
---
# <a name="class-xsqlenumerator"></a>クラス xSqlEnumerator

[!include [banner](../../includes/banner.md)]

```xpp
class xSqlEnumerator extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                               | 説明                                             |
|------------------------------------------------------|---------------------------------------------------------|
| public str getConnStr(str database)                  |                                                         |
| public List getDatabases(str server, \[str driver\]) |                                                         |
| public List getServers(str driver)                   |                                                         |
| public void new()                                    | xSqlEnumerator クラスの新しいインスタンスを初期化します。 |

## <a name="method-getconnstr"></a>メソッド getConnStr

```xpp
public str getConnStr(str database)
```

### <a name="parameters---getconnstr"></a>パラメーター - getConnStr

データベース  

### <a name="return-value---getconnstr"></a>戻り値 - getConnStr

## <a name="method-getdatabases"></a>メソッド getDatabases

```xpp
public List getDatabases(str server, [str driver])
```

### <a name="parameters---getdatabases"></a>パラメーター - getDatabases

server  

<!-- -->

driver  

### <a name="return-value---getdatabases"></a>戻り値 - getDatabases

## <a name="method-getservers"></a>メソッド getServers

```xpp
public List getServers(str driver)
```

### <a name="parameters---getservers"></a>パラメーター - getServers

driver  

### <a name="return-value---getservers"></a>戻り値 - getServers

## <a name="method-new"></a>メソッド new

xSqlEnumerator クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

