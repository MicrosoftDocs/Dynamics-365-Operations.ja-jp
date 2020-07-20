---
title: IISApplicationObject クラス
description: このトピックでは、IISApplicationObject クラスについて説明します。
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
ms.openlocfilehash: 484ac76d5c519fb6d20d2e4fa48bdea52580d2c0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502605"
---
# <a name="class-iisapplicationobject"></a>クラス IISApplicationObject

[!include [banner](../../includes/banner.md)]

```xpp
class IISApplicationObject extends Object
```

IISApplicationObject クラスは、インターネット インフォメーション サービス (IIS) によって提供されるアプリケーション オブジェクトをラップします。

## <a name="remarks"></a>備考

IISApplicationObject クラスのメソッドと、IIS によって提供される Application オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISApplicationObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISApplicationObject クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| public IISVariantDictionary contents()                 |                                                               |
| public ComInterface interface()                        |                                                               |
| public IISVariantDictionary staticObjects()            |                                                               |
| public COMVariant value(str value, \[COMVariant var\]) |                                                               |
| public str valueTxt(str value, \[str var\])            |                                                               |
| public void new()                                      | IISApplicationObject クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                 |                                                               |
| public void lock()                                     |                                                               |
| public void unLock()                                   |                                                               |

## <a name="method-contents"></a>メソッド contents

```xpp
public IISVariantDictionary contents()
```

### <a name="return-value---contents"></a>戻り値 - contents

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-staticobjects"></a>メソッド staticObjects

```xpp
public IISVariantDictionary staticObjects()
```

### <a name="return-value---staticobjects"></a>戻り値 - staticObjects

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

IISApplicationObject クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-lock"></a>メソッド lock

```xpp
public void lock()
```

## <a name="method-unlock"></a>メソッド unLock

```xpp
public void unLock()
```

