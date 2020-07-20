---
title: IISSessionObject クラス
description: このトピックでは、IISSessionObject クラスについて説明します。
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
ms.openlocfilehash: 2803da002fdbaf3dd3f62176019f8fdb102ba4a5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502601"
---
# <a name="class-iissessionobject"></a>クラス IISSessionObject

[!include [banner](../../includes/banner.md)]

```xpp
class IISSessionObject extends Object
```

IISSessionObject クラスは、インターネット インフォメーション サービス (IIS) によって提供される Session オブジェクトをラップします。

## <a name="remarks"></a>備考

IISSessionObject クラスのメソッドと、IIS によって提供される Session オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISSessionObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISSessionObject クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| public int codePage(\[int codePage\])                  |                                                           |
| public IISVariantDictionary contents()                 |                                                           |
| public str getSessionID()                              |                                                           |
| public ComInterface interface()                        |                                                           |
| public int lcid(\[int lcid\])                          |                                                           |
| public IISVariantDictionary staticObjects()            |                                                           |
| public int timeout(\[int timeout\])                    |                                                           |
| public COMVariant value(str value, \[COMVariant var\]) |                                                           |
| public str valueTxt(str value, \[str var\])            |                                                           |
| public void new()                                      | IISSessionObject クラスの新しいインスタンスを初期化します。 |
| public void abandon()                                  |                                                           |
| public void finalize()                                 |                                                           |

## <a name="method-codepage"></a>メソッド codePage

```xpp
public int codePage([int codePage])
```

### <a name="parameters---codepage"></a>パラメーター - codePage

codePage  

### <a name="return-value---codepage"></a>戻り値 - codePage

## <a name="method-contents"></a>メソッド contents

```xpp
public IISVariantDictionary contents()
```

### <a name="return-value---contents"></a>戻り値 - contents

## <a name="method-getsessionid"></a>メソッド getSessionID

```xpp
public str getSessionID()
```

### <a name="return-value---getsessionid"></a>戻り値 - getSessionID

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-lcid"></a>メソッド lcid

```xpp
public int lcid([int lcid])
```

### <a name="parameters---lcid"></a>パラメーター - lcid

lcid  

### <a name="return-value---lcid"></a>戻り値 - lcid

## <a name="method-staticobjects"></a>メソッド staticObjects

```xpp
public IISVariantDictionary staticObjects()
```

### <a name="return-value---staticobjects"></a>戻り値 - staticObjects

## <a name="method-timeout"></a>メソッド timeout

```xpp
public int timeout([int timeout])
```

### <a name="parameters---timeout"></a>パラメーター - timeout

timeout  

### <a name="return-value---timeout"></a>戻り値 - timeout

## <a name="method-value"></a>メソッド value

```xpp
public COMVariant value(str value, [COMVariant var])
```

### <a name="parameters---value"></a>パラメーター - value

値  

<!-- -->

var  

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-valuetxt"></a>メソッド valueTxt

```xpp
public str valueTxt(str value, [str var])
```

### <a name="parameters---valuetxt"></a>パラメーター - valueTxt

値  

<!-- -->

var  

### <a name="return-value---valuetxt"></a>戻り値 - valueTxt

## <a name="method-new"></a>メソッド new

IISSessionObject クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-abandon"></a>メソッド abandon

```xpp
public void abandon()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

