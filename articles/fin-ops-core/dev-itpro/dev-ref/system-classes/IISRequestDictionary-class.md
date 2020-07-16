---
title: IISRequestDictionary クラス
description: このトピックでは、IISRequestDictionary クラスについて説明します。
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
ms.openlocfilehash: fe8377139e71521a62b59517ab8bb44353cb093e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502905"
---
# <a name="class-iisrequestdictionary"></a>クラス IISRequestDictionary

[!include [banner](../../includes/banner.md)]

```xpp
class IISRequestDictionary extends Object
```

IISRequestDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される RequestDictionary オブジェクトをラップします。

## <a name="remarks"></a>備考

IISRequestDictionary クラスのメソッドと、IIS によって提供される RequestDictionary オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。 したがって、IISRequestDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISRequestDictionary クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                              | 説明                                     |
|-----------------------------------------------------|-------------------------------------------------|
| public int count()                                  |                                                 |
| public COMEnum2Variant getEnum()                    |                                                 |
| public ComInterface interface()                     |                                                 |
| public COMVariant item(COMVariant item)             |                                                 |
| public IISReadCookie itemReadCookie(\[str item\])   |                                                 |
| public IISStringList itemStringList(\[str item\])   |                                                 |
| public str itemTxt(str item)                        |                                                 |
| public IISWriteCookie itemWriteCookie(\[str item\]) |                                                 |
| public str key(str key)                             |                                                 |
| public void finalize()                              |                                                 |
| public void new(COM requestDictionary)              | Object クラスの新しいインスタンスを初期化します。 |

## <a name="method-count"></a>メソッド count

```xpp
public int count()
```

### <a name="return-value---count"></a>戻り値 - count

## <a name="method-getenum"></a>メソッド getEnum

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a>戻り値 - getEnum

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-item"></a>メソッド item

```xpp
public COMVariant item(COMVariant item)
```

### <a name="parameters---item"></a>パラメーター - item

品目  

### <a name="return-value---item"></a>戻り値 - item

## <a name="method-itemreadcookie"></a>メソッド itemReadCookie

```xpp
public IISReadCookie itemReadCookie([str item])
```

### <a name="parameters---itemreadcookie"></a>パラメーター - itemReadCookie

品目  

### <a name="return-value---itemreadcookie"></a>戻り値 - itemReadCookie

## <a name="method-itemstringlist"></a>メソッド itemStringList

```xpp
public IISStringList itemStringList([str item])
```

### <a name="parameters---itemstringlist"></a>パラメーター - itemStringList

品目  

### <a name="return-value---itemstringlist"></a>戻り値 - itemStringList

## <a name="method-itemtxt"></a>メソッド itemTxt

```xpp
public str itemTxt(str item)
```

### <a name="parameters---itemtxt"></a>パラメーター - itemTxt

品目  

### <a name="return-value---itemtxt"></a>戻り値 - itemTxt

## <a name="method-itemwritecookie"></a>メソッド itemWriteCookie

```xpp
public IISWriteCookie itemWriteCookie([str item])
```

### <a name="parameters---itemwritecookie"></a>パラメーター - itemWriteCookie

品目  

### <a name="return-value---itemwritecookie"></a>戻り値 - itemWriteCookie

## <a name="method-key"></a>メソッド key

```xpp
public str key(str key)
```

### <a name="parameters---key"></a>パラメーター - key

キー  

### <a name="return-value---key"></a>戻り値 - key

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(COM requestDictionary)
```

### <a name="parameters---new"></a>パラメーター - new

requestDictionary  

