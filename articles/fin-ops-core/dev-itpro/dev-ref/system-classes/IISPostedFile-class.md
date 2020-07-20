---
title: IISPostedFile クラス
description: このトピックでは、IISPostedFile クラスについて説明します。
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
ms.openlocfilehash: 9bbcdbdbf1b442a9037ae59588849cefbe43407e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502604"
---
# <a name="class-iispostedfile"></a>クラス IISPostedFile

[!include [banner](../../includes/banner.md)]

```xpp
class IISPostedFile extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                 | 説明                                            |
|----------------------------------------|--------------------------------------------------------|
| public int contentLength()             |                                                        |
| public str contentType()               |                                                        |
| public str fileName()                  |                                                        |
| public container read(int countToRead) |                                                        |
| public void finalize()                 |                                                        |
| public void new()                      | IISPostedFile クラスの新しいインスタンスを初期化します。 |

## <a name="method-contentlength"></a>メソッド contentLength

```xpp
public int contentLength()
```

### <a name="return-value---contentlength"></a>戻り値 - contentLength

## <a name="method-contenttype"></a>メソッド contentType

```xpp
public str contentType()
```

### <a name="return-value---contenttype"></a>戻り値 - contentType

## <a name="method-filename"></a>メソッド fileName

```xpp
public str fileName()
```

### <a name="return-value---filename"></a>戻り値 - fileName

## <a name="method-read"></a>メソッド read

```xpp
public container read(int countToRead)
```

### <a name="parameters---read"></a>パラメーター - read

countToRead  

### <a name="return-value---read"></a>戻り値 - read

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

IISPostedFile クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

