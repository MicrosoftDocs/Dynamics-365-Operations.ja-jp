---
title: IISWriteCookie クラス
description: このトピックでは、IISWriteCookie クラスについて説明します。
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
ms.openlocfilehash: a6500260b30867958bad1528ba6803f4c1ecf07a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502599"
---
# <a name="class-iiswritecookie"></a>クラス IISWriteCookie

[!include [banner](../../includes/banner.md)]

```xpp
class IISWriteCookie extends Object
```

IISWriteCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される WriteCookie オブジェクトをラップします。

## <a name="remarks"></a>備考

IISWriteCookie クラスのメソッドと、IIS によって提供される WriteCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISWriteCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISWriteCookie クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                  | 説明                                     |
|-----------------------------------------|-------------------------------------------------|
| public COMEnum2Variant getEnum()        |                                                 |
| public boolean hasKeys()                |                                                 |
| public ComInterface interface()         |                                                 |
| public void new(COM writeCookie)        | Object クラスの新しいインスタンスを初期化します。 |
| public void secure(boolean secure)      |                                                 |
| public void path(str path)              |                                                 |
| public void finalize()                  |                                                 |
| public void domain(str domain)          |                                                 |
| public void expires(COMVariant expires) |                                                 |
| public void item(str item, str value)   |                                                 |

## <a name="method-getenum"></a>メソッド getEnum

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a>戻り値 - getEnum

## <a name="method-haskeys"></a>メソッド hasKeys

```xpp
public boolean hasKeys()
```

### <a name="return-value---haskeys"></a>戻り値 - hasKeys

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(COM writeCookie)
```

### <a name="parameters---new"></a>パラメーター - new

writeCookie  

## <a name="method-secure"></a>メソッド secure

```xpp
public void secure(boolean secure)
```

### <a name="parameters---secure"></a>パラメーター - secure

secure  

## <a name="method-path"></a>メソッド path

```xpp
public void path(str path)
```

### <a name="parameters---path"></a>パラメーター - path

path  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-domain"></a>メソッド domain

```xpp
public void domain(str domain)
```

### <a name="parameters---domain"></a>パラメーター - domain

domain  

## <a name="method-expires"></a>メソッド expires

```xpp
public void expires(COMVariant expires)
```

### <a name="parameters---expires"></a>パラメーター - expires

expires  

## <a name="method-item"></a>メソッド item

```xpp
public void item(str item, str value)
```

### <a name="parameters---item"></a>パラメーター - item

品目  

<!-- -->

値  

