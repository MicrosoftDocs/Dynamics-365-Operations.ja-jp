---
title: ScannerClass クラス
description: このトピックでは、ScannerClass クラスについて説明します。
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
ms.openlocfilehash: 30cbff5dd2982379b2b385fecbc48022704c1324
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502817"
---
# <a name="class-scannerclass"></a>クラス ScannerClass

[!include [banner](../../includes/banner.md)]


```xpp
class ScannerClass extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| public int col()                                                                             |                                                 |
| public Date dateValue()                                                                      |                                                 |
| public int firstSymbol()                                                                     |                                                 |
| public Int64 int64Value()                                                                    |                                                 |
| public int intValue()                                                                        |                                                 |
| public int line()                                                                            |                                                 |
| public int nextSymbol()                                                                      |                                                 |
| public Real realValue()                                                                      |                                                 |
| public int startColumn()                                                                     |                                                 |
| public str string()                                                                          |                                                 |
| public str strValue()                                                                        |                                                 |
| public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos) |                                                 |
| public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)      |                                                 |
| public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)      |                                                 |
| public void new(str source)                                                                  | Object クラスの新しいインスタンスを初期化します。 |
| public void comment(str text, int startLine, int startPos, int endLine, int endPos)          |                                                 |

## <a name="method-col"></a>メソッド col

```xpp
public int col()
```

### <a name="return-value---col"></a>戻り値 - col

## <a name="method-datevalue"></a>メソッド dateValue

```xpp
public Date dateValue()
```

### <a name="return-value---datevalue"></a>戻り値 - dateValue

## <a name="method-firstsymbol"></a>メソッド firstSymbol

```xpp
public int firstSymbol()
```

### <a name="return-value---firstsymbol"></a>戻り値 - firstSymbol

## <a name="method-int64value"></a>メソッド int64Value

```xpp
public Int64 int64Value()
```

### <a name="return-value---int64value"></a>戻り値 - int64Value

## <a name="method-intvalue"></a>メソッド intValue

```xpp
public int intValue()
```

### <a name="return-value---intvalue"></a>戻り値 - intValue

## <a name="method-line"></a>メソッド line

```xpp
public int line()
```

### <a name="return-value---line"></a>戻り値 - line

## <a name="method-nextsymbol"></a>メソッド nextSymbol

```xpp
public int nextSymbol()
```

### <a name="return-value---nextsymbol"></a>戻り値 - nextSymbol

## <a name="method-realvalue"></a>メソッド realValue

```xpp
public Real realValue()
```

### <a name="return-value---realvalue"></a>戻り値 - realValue

## <a name="method-startcolumn"></a>メソッド startColumn

```xpp
public int startColumn()
```

### <a name="return-value---startcolumn"></a>戻り値 - startColumn

## <a name="method-string"></a>メソッド string

```xpp
public str string()
```

### <a name="return-value---string"></a>戻り値 - string

## <a name="method-strvalue"></a>メソッド strValue

```xpp
public str strValue()
```

### <a name="return-value---strvalue"></a>戻り値 - strValue

## <a name="method-localmacrodefine"></a>メソッド localMacroDefine

```xpp
public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---localmacrodefine"></a>パラメーター - localMacroDefine

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

## <a name="method-linecomment"></a>メソッド lineComment

```xpp
public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---linecomment"></a>パラメーター - lineComment

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

## <a name="method-macrodefine"></a>メソッド macroDefine

```xpp
public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---macrodefine"></a>パラメーター - macroDefine

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(str source)
```

### <a name="parameters---new"></a>パラメーター - new

ソース  

## <a name="method-comment"></a>メソッド comment

```xpp
public void comment(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---comment"></a>パラメーター - comment

テキスト  

<!-- -->

startLine  

<!-- -->

startPos  

<!-- -->

endLine  

<!-- -->

endPos  

