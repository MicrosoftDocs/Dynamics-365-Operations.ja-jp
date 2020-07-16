---
title: WinAPINative クラス
description: このトピックでは、WinAPINative クラスについて説明します。
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
ms.openlocfilehash: b1866cc870e8f5913412b0f8ee2bf79478a05353
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502683"
---
# <a name="class-winapinative"></a>クラス WinAPINative

[!include [banner](../../includes/banner.md)]

```xpp
class WinAPINative extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                  | 説明                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| ::public static Int64 createFontIndirect(Binary logfont)                                                                |                                                       |
| ::public static boolean deleteObject(Int64 hGDIObject)                                                                  |                                                       |
| ::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths) |                                                       |
| ::public static int getDeviceCaps(Int64 hDC, int index)                                                                 |                                                       |
| ::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])                              |                                                       |
| ::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])                                                    |                                                       |
| ::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)                                           |                                                       |
| ::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)                                                       |                                                       |
| ::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)                        |                                                       |
| ::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)                                                         |                                                       |
| private void new()                                                                                                      | WinAPINative クラスの新しいインスタンスを初期化します。 |

## <a name="method-createfontindirect"></a>メソッド createFontIndirect

```xpp
public static Int64 createFontIndirect(Binary logfont)
```

### <a name="parameters---createfontindirect"></a>パラメーター - createFontIndirect

logfont  

### <a name="return-value---createfontindirect"></a>戻り値 - createFontIndirect

## <a name="method-deleteobject"></a>メソッド deleteObject

```xpp
public static boolean deleteObject(Int64 hGDIObject)
```

### <a name="parameters---deleteobject"></a>パラメーター - deleteObject

hGDIObject  

### <a name="return-value---deleteobject"></a>戻り値 - deleteObject

## <a name="method-getcharabcwidthsi"></a>メソッド getCharABCWidthsI

```xpp
public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)
```

### <a name="parameters---getcharabcwidthsi"></a>パラメーター - getCharABCWidthsI

hDC  

<!-- -->

firstGlyphIndex  

<!-- -->

glyphIndicesCount  

<!-- -->

charWidths  

### <a name="return-value---getcharabcwidthsi"></a>戻り値 - getCharABCWidthsI

## <a name="method-getdevicecaps"></a>メソッド getDeviceCaps

```xpp
public static int getDeviceCaps(Int64 hDC, int index)
```

### <a name="parameters---getdevicecaps"></a>パラメーター - getDeviceCaps

hDC  

<!-- -->

指数  

### <a name="return-value---getdevicecaps"></a>戻り値 - getDeviceCaps

## <a name="method-getfontdata"></a>メソッド getFontData

```xpp
public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])
```

### <a name="parameters---getfontdata"></a>パラメーター - getFontData

hDC  

<!-- -->

dwTable  

<!-- -->

dwOffset  

<!-- -->

pvBuffer  

### <a name="return-value---getfontdata"></a>戻り値 - getFontData

## <a name="method-getfontunicoderanges"></a>メソッド getFontUnicodeRanges

```xpp
public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])
```

### <a name="parameters---getfontunicoderanges"></a>パラメーター - getFontUnicodeRanges

hDC  

<!-- -->

lpgs  

### <a name="return-value---getfontunicoderanges"></a>戻り値 - getFontUnicodeRanges

## <a name="method-getglyphindices"></a>メソッド getGlyphIndices

```xpp
public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)
```

### <a name="parameters---getglyphindices"></a>パラメーター - getGlyphIndices

hDC  

<!-- -->

lpstr  

<!-- -->

pgi  

<!-- -->

fl  

### <a name="return-value---getglyphindices"></a>戻り値 - getGlyphIndices

## <a name="method-gettextmetrics"></a>メソッド getTextMetrics

```xpp
public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)
```

### <a name="parameters---gettextmetrics"></a>パラメーター - getTextMetrics

hDC  

<!-- -->

lpMetrics  

### <a name="return-value---gettextmetrics"></a>戻り値 - getTextMetrics

## <a name="method-getuniscribeglyphindices"></a>メソッド getUniscribeGlyphIndices

```xpp
public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)
```

### <a name="parameters---getuniscribeglyphindices"></a>パラメーター - getUniscribeGlyphIndices

hDC  

<!-- -->

hGDIObject  

<!-- -->

lpstr  

<!-- -->

pgi  

### <a name="return-value---getuniscribeglyphindices"></a>戻り値 - getUniscribeGlyphIndices

## <a name="method-selectobject"></a>メソッド selectObject

```xpp
public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)
```

### <a name="parameters---selectobject"></a>パラメーター - selectObject

hDC  

<!-- -->

hGDIObject  

### <a name="return-value---selectobject"></a>戻り値 - selectObject

## <a name="method-new"></a>メソッド new

WinAPINative クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```


