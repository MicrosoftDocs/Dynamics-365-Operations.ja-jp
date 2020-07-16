---
title: Editor クラス
description: このトピックでは、Editor クラスについて説明します。
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
ms.openlocfilehash: a84952684ecc666ca85a5cdf31babd73d4660e5e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502669"
---
# <a name="class-editor"></a>クラス エディター

[!include [banner](../../includes/banner.md)]


```xpp
class Editor extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                          | 説明                                     |
|---------------------------------------------------------------------------------|-------------------------------------------------|
| public int columnNo()                                                           |                                                 |
| public str currentLine()                                                        |                                                 |
| public int currentLineNo()                                                      |                                                 |
| public str getLine()                                                            |                                                 |
| public int gotoCol(int ColumnNo)                                                |                                                 |
| public int lineNo()                                                             |                                                 |
| public MarkMode markMode()                                                      |                                                 |
| public boolean matchCase(\[boolean UseMatchCase\])                              |                                                 |
| public boolean moreLines()                                                      |                                                 |
| public boolean moreSelectedLines()                                              |                                                 |
| public str path()                                                               |                                                 |
| public boolean regexp(\[boolean UseRegExp\])                                    |                                                 |
| public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll) |                                                 |
| public boolean search(str SearchString)                                         |                                                 |
| public str searchString()                                                       |                                                 |
| public int selectionEndCol()                                                    |                                                 |
| public int selectionEndLine()                                                   |                                                 |
| public int selectionStartCol()                                                  |                                                 |
| public int selectionStartLine()                                                 |                                                 |
| ::public static Editor open (str documentPath)                                   |                                                 |
| public void gotoLine(int LineNo)                                                |                                                 |
| public void closeApplicationObjectDialog()                                      |                                                 |
| public void mark(int line, int col)                                             |                                                 |
| public void executeScript(str scriptName)                                       |                                                 |
| public void nextLine()                                                          |                                                 |
| public void firstSelectedLine()                                                 |                                                 |
| private void new()                                                              | Editor クラスの新しいインスタンスを初期化します。 |
| public void unmark()                                                            |                                                 |
| public void insertString(str InsString)                                         |                                                 |
| public void close()                                                             |                                                 |
| public void nextSelectedLine()                                                  |                                                 |
| public void closeSearchDialog()                                                 |                                                 |
| public void deleteLines(\[int noOfLines\])                                      |                                                 |
| public void insertLines(str InsString)                                          |                                                 |
| public void firstLine()                                                         |                                                 |
| public void deleteChars(\[int noOfChars\])                                      |                                                 |

## <a name="method-columnno"></a>メソッド columnNo

```xpp
public int columnNo()
```

### <a name="return-value---columnno"></a>戻り値 - columnNo

## <a name="method-currentline"></a>メソッド currentLine

```xpp
public str currentLine()
```

### <a name="return-value---currentline"></a>戻り値 - currentLine

## <a name="method-currentlineno"></a>メソッド currentLineNo

```xpp
public int currentLineNo()
```

### <a name="return-value---currentlineno"></a>戻り値 - currentLineNo

## <a name="method-getline"></a>メソッド getLine

```xpp
public str getLine()
```

### <a name="return-value---getline"></a>戻り値 - getLine

## <a name="method-gotocol"></a>メソッド gotoCol

```xpp
public int gotoCol(int ColumnNo)
```

### <a name="parameters---gotocol"></a>パラメーター - gotoCol

ColumnNo  

### <a name="return-value---gotocol"></a>戻り値 - gotoCol

## <a name="method-lineno"></a>メソッド lineNo

```xpp
public int lineNo()
```

### <a name="return-value---lineno"></a>戻り値 - lineNo

## <a name="method-markmode"></a>メソッド markMode

```xpp
public MarkMode markMode()
```

### <a name="return-value---markmode"></a>戻り値 - markMode

## <a name="method-matchcase"></a>メソッド matchCase

```xpp
public boolean matchCase([boolean UseMatchCase])
```

### <a name="parameters---matchcase"></a>パラメーター - matchCase

UseMatchCase  

### <a name="return-value---matchcase"></a>戻り値 - matchCase

## <a name="method-morelines"></a>メソッド moreLines

```xpp
public boolean moreLines()
```

### <a name="return-value---morelines"></a>戻り値 - moreLines

## <a name="method-moreselectedlines"></a>メソッド moreSelectedLines

```xpp
public boolean moreSelectedLines()
```

### <a name="return-value---moreselectedlines"></a>戻り値 - moreSelectedLines

## <a name="method-path"></a>メソッド path

```xpp
public str path()
```

### <a name="return-value---path"></a>戻り値 - path

## <a name="method-regexp"></a>メソッド regexp

```xpp
public boolean regexp([boolean UseRegExp])
```

### <a name="parameters---regexp"></a>パラメーター - regexp

UseRegExp  

### <a name="return-value---regexp"></a>戻り値 - regexp

## <a name="method-replace"></a>メソッド replace

```xpp
public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)
```

### <a name="parameters---replace"></a>パラメーター - replace

SearchString  

<!-- -->

ReplaceString  

<!-- -->

ReplaceAll  

### <a name="return-value---replace"></a>戻り値 - replace

## <a name="method-search"></a>メソッド search

```xpp
public boolean search(str SearchString)
```

### <a name="parameters---search"></a>パラメーター - search

SearchString  

### <a name="return-value---search"></a>戻り値 - search

## <a name="method-searchstring"></a>メソッド searchString

```xpp
public str searchString()
```

### <a name="return-value---searchstring"></a>戻り値 - searchString

## <a name="method-selectionendcol"></a>メソッド selectionEndCol

```xpp
public int selectionEndCol()
```

### <a name="return-value---selectionendcol"></a>戻り値 - selectionEndCol

## <a name="method-selectionendline"></a>メソッド selectionEndLine

```xpp
public int selectionEndLine()
```

### <a name="return-value---selectionendline"></a>戻り値 - selectionEndLine

## <a name="method-selectionstartcol"></a>メソッド selectionStartCol

```xpp
public int selectionStartCol()
```

### <a name="return-value---selectionstartcol"></a>戻り値 - selectionStartCol

## <a name="method-selectionstartline"></a>メソッド selectionStartLine

```xpp
public int selectionStartLine()
```

### <a name="return-value---selectionstartline"></a>戻り値 - selectionStartLine

## <a name="method-open"></a>メソッド open

```xpp
public static Editor open(str documentPath)
```

### <a name="parameters---open"></a>パラメーター - open

documentPath  

### <a name="return-value---open"></a>戻り値 - open

## <a name="method-gotoline"></a>メソッド gotoLine

```xpp
public void gotoLine(int LineNo)
```

### <a name="parameters---gotoline"></a>パラメーター - gotoLine

LineNo  

## <a name="method-closeapplicationobjectdialog"></a>メソッド closeApplicationObjectDialog

```xpp
public void closeApplicationObjectDialog()
```

## <a name="method-mark"></a>メソッド mark

```xpp
public void mark(int line, int col)
```

### <a name="parameters---mark"></a>パラメーター - mark

明細行  

<!-- -->

col  

## <a name="method-executescript"></a>メソッド executeScript

```xpp
public void executeScript(str scriptName)
```

### <a name="parameters---executescript"></a>パラメーター - executeScript

scriptName  

## <a name="method-nextline"></a>メソッド nextLine

```xpp
public void nextLine()
```

## <a name="method-firstselectedline"></a>メソッド firstSelectedLine

```xpp
public void firstSelectedLine()
```

## <a name="method-new"></a>メソッド new

Editor クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

## <a name="method-unmark"></a>メソッド unmark

```xpp
public void unmark()
```

## <a name="method-insertstring"></a>メソッド insertString

```xpp
public void insertString(str InsString)
```

### <a name="parameters---insertstring"></a>パラメーター - insertString

InsString  

## <a name="method-close"></a>メソッド close

```xpp
public void close()
```

## <a name="method-nextselectedline"></a>メソッド nextSelectedLine

```xpp
public void nextSelectedLine()
```

## <a name="method-closesearchdialog"></a>メソッド closeSearchDialog

```xpp
public void closeSearchDialog()
```

## <a name="method-deletelines"></a>メソッド deleteLines

```xpp
public void deleteLines([int noOfLines])
```

### <a name="parameters---deletelines"></a>パラメーター - deleteLines

noOfLines  

## <a name="method-insertlines"></a>メソッド insertLines

```xpp
public void insertLines(str InsString)
```

### <a name="parameters---insertlines"></a>パラメーター - insertLines

InsString  

## <a name="method-firstline"></a>メソッド firstLine

```xpp
public void firstLine()
```

## <a name="method-deletechars"></a>メソッド deleteChars

```xpp
public void deleteChars([int noOfChars])
```

### <a name="parameters---deletechars"></a>パラメーター - deleteChars

noOfChars  

