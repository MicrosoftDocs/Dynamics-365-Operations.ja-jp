---
title: IISContextObject クラス
description: このトピックでは、IISContextObject クラスについて説明します。
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
ms.openlocfilehash: d5d1d513ba3c70be4b3e7670c47c917ce896008c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502606"
---
# <a name="class-iiscontextobject"></a>クラス IISContextObject

[!include [banner](../../includes/banner.md)]

```xpp
class IISContextObject extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| public ComInterface interface()                        |                                                           |
| public boolean isTraceEnabled()                        |                                                           |
| public IISVariantDictionary items()                    |                                                           |
| public int traceMode(int mode)                         |                                                           |
| public COMVariant value(str value, \[COMVariant var\]) |                                                           |
| public str valueTxt(str value, \[str var\])            |                                                           |
| public void traceWrite(str category, str message)      |                                                           |
| public void finalize()                                 |                                                           |
| public void traceWarn(str category, str message)       |                                                           |
| public void new()                                      | IISContextObject クラスの新しいインスタンスを初期化します。 |

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-istraceenabled"></a>メソッド isTraceEnabled

```xpp
public boolean isTraceEnabled()
```

### <a name="return-value---istraceenabled"></a>戻り値 - isTraceEnabled

## <a name="method-items"></a>メソッド items

```xpp
public IISVariantDictionary items()
```

### <a name="return-value---items"></a>戻り値 - items

## <a name="method-tracemode"></a>メソッド traceMode

```xpp
public int traceMode(int mode)
```

### <a name="parameters---tracemode"></a>パラメーター - traceMode

モード  

### <a name="return-value---tracemode"></a>戻り値 - traceMode

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

## <a name="method-tracewrite"></a>メソッド traceWrite

```xpp
public void traceWrite(str category, str message)
```

### <a name="parameters---tracewrite"></a>パラメーター - traceWrite

カテゴリ  

<!-- -->

メッセージ  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-tracewarn"></a>メソッド traceWarn

```xpp
public void traceWarn(str category, str message)
```

### <a name="parameters---tracewarn"></a>パラメーター - traceWarn

カテゴリ  

<!-- -->

メッセージ  

## <a name="method-new"></a>メソッド new

IISContextObject クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

