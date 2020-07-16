---
title: xRef クラス
description: このトピックでは、xRef クラスについて説明します。
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
ms.openlocfilehash: c790f8540773f3039301fcc91ba75b14a5a677d0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502677"
---
# <a name="class-xref"></a>クラス xRef

[!include [banner](../../includes/banner.md)]

```xpp
class xRef extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                         | 説明                                     |
|------------------------------------------------|-------------------------------------------------|
| public AccessLevel accessLevel()               |                                                 |
| public int column()                            |                                                 |
| public container contents()                    |                                                 |
| public xRefKind kind()                         |                                                 |
| public int line()                              |                                                 |
| public XRefMode mode()                         |                                                 |
| public str name()                              |                                                 |
| public str path()                              |                                                 |
| public XRefReference reference()               |                                                 |
| public int typeHandle()                        |                                                 |
| public str typeName(xRefKind kind, int handle) |                                                 |
| public void new(container data)                | Object クラスの新しいインスタンスを初期化します。 |
| public void init()                             |                                                 |
| public void finalize()                         |                                                 |
| public void next()                             |                                                 |

## <a name="method-accesslevel"></a>メソッド accessLevel

```xpp
public AccessLevel accessLevel()
```

### <a name="return-value---accesslevel"></a>戻り値 - accessLevel

## <a name="method-column"></a>メソッド column

```xpp
public int column()
```

### <a name="return-value---column"></a>戻り値 - column

## <a name="method-contents"></a>メソッド contents

```xpp
public container contents()
```

### <a name="return-value---contents"></a>戻り値 - contents

## <a name="method-kind"></a>メソッド kind

```xpp
public xRefKind kind()
```

### <a name="return-value---kind"></a>戻り値 - kind

## <a name="method-line"></a>メソッド line

```xpp
public int line()
```

### <a name="return-value---line"></a>戻り値 - line

## <a name="method-mode"></a>メソッド mode

```xpp
public XRefMode mode()
```

### <a name="return-value---mode"></a>戻り値 - mode

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-path"></a>メソッド path

```xpp
public str path()
```

### <a name="return-value---path"></a>戻り値 - path

## <a name="method-reference"></a>メソッド reference

```xpp
public XRefReference reference()
```

### <a name="return-value---reference"></a>戻り値 - reference

## <a name="method-typehandle"></a>メソッド typeHandle

```xpp
public int typeHandle()
```

### <a name="return-value---typehandle"></a>戻り値 - typeHandle

## <a name="method-typename"></a>メソッド typeName

```xpp
public str typeName(xRefKind kind, int handle)
```

### <a name="parameters---typename"></a>パラメーター - typeName

kind  

<!-- -->

handle  

### <a name="return-value---typename"></a>戻り値 - typeName

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(container data)
```

### <a name="parameters---new"></a>パラメーター - new

データ  

## <a name="method-init"></a>メソッド init

```xpp
public void init()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-next"></a>メソッド next

```xpp
public void next()
```

