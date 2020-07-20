---
title: IISVariantDictionary クラス
description: このトピックでは、IISVariantDictionary クラスについて説明します。
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
ms.openlocfilehash: 95c68565667495ddda16ae5fd53f75972df00d43
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502600"
---
# <a name="class-iisvariantdictionary"></a>クラス IISVariantDictionary

[!include [banner](../../includes/banner.md)]

```xpp
class IISVariantDictionary extends Object
```

IISVariantDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される VariantDictionary オブジェクトをラップします。

## <a name="remarks"></a>備考

IISVariantDictionary クラスのメソッドと、IIS によって提供される VariantDictionary オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISVariantDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISVariantDictionary クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                     |
|-------------------------------------------------------------|-------------------------------------------------|
| public int count()                                          |                                                 |
| public COMEnum2Variant getEnum()                            |                                                 |
| public ComInterface interface()                             |                                                 |
| public COMVariant item(COMVariant item, \[COMVariant var\]) |                                                 |
| public COM itemObj(str item, \[COM var\])                   |                                                 |
| public str itemTxt(str item, \[str var\])                   |                                                 |
| public str key(str key)                                     |                                                 |
| public void finalize()                                      |                                                 |
| public void remove(str key)                                 |                                                 |
| public void removeAll()                                     |                                                 |
| public void new(COM variantDictionary)                      | Object クラスの新しいインスタンスを初期化します。 |

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
public COMVariant item(COMVariant item, [COMVariant var])
```

### <a name="parameters---item"></a>パラメーター - item

品目  

<!-- -->

var  

### <a name="return-value---item"></a>戻り値 - item

## <a name="method-itemobj"></a>メソッド itemObj

```xpp
public COM itemObj(str item, [COM var])
```

### <a name="parameters---itemobj"></a>パラメーター - itemObj

品目  

<!-- -->

var  

### <a name="return-value---itemobj"></a>戻り値 - itemObj

## <a name="method-itemtxt"></a>メソッド itemTxt

```xpp
public str itemTxt(str item, [str var])
```

### <a name="parameters---itemtxt"></a>パラメーター - itemTxt

品目  

<!-- -->

var  

### <a name="return-value---itemtxt"></a>戻り値 - itemTxt

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

## <a name="method-remove"></a>メソッド remove

```xpp
public void remove(str key)
```

### <a name="parameters---remove"></a>パラメーター - remove

キー  

## <a name="method-removeall"></a>メソッド removeAll

```xpp
public void removeAll()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(COM variantDictionary)
```

### <a name="parameters---new"></a>パラメーター - new

variantDictionary  

