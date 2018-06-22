---
title: "E クラス"
description: "文字 E で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 68633
ms.assetid: c7fea535-c44d-4e78-96b2-77e180076ac9
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: fbd1db066c23f59fddd6fd20508b6d487c116396
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="e-classes"></a>E クラス

[!include [banner](../includes/banner.md)]

文字 E で始まるシステム API クラス。

<a name="class-editor"></a>クラス エディター
------------

    class Editor extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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
| ::public static Editor open(str documentPath)                                   |                                                 |
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

### <a name="method-columnno"></a>メソッド columnNo

    public int columnNo()

#### <a name="return-value"></a>戻り値

### <a name="method-currentline"></a>メソッド currentLine

    public str currentLine()

#### <a name="return-value"></a>戻り値

### <a name="method-currentlineno"></a>メソッド currentLineNo

    public int currentLineNo()

#### <a name="return-value"></a>戻り値

### <a name="method-getline"></a>メソッド getLine

    public str getLine()

#### <a name="return-value"></a>戻り値

### <a name="method-gotocol"></a>メソッド gotoCol

    public int gotoCol(int ColumnNo)

#### <a name="parameters"></a>パラメーター

ColumnNo  

#### <a name="return-value"></a>戻り値

### <a name="method-lineno"></a>メソッド lineNo

    public int lineNo()

#### <a name="return-value"></a>戻り値

### <a name="method-markmode"></a>メソッド markMode

    public MarkMode markMode()

#### <a name="return-value"></a>戻り値

### <a name="method-matchcase"></a>メソッド matchCase

    public boolean matchCase([boolean UseMatchCase])

#### <a name="parameters"></a>パラメーター

UseMatchCase  

#### <a name="return-value"></a>戻り値

### <a name="method-morelines"></a>メソッド moreLines

    public boolean moreLines()

#### <a name="return-value"></a>戻り値

### <a name="method-moreselectedlines"></a>メソッド moreSelectedLines

    public boolean moreSelectedLines()

#### <a name="return-value"></a>戻り値

### <a name="method-path"></a>メソッド path

    public str path()

#### <a name="return-value"></a>戻り値

### <a name="method-regexp"></a>メソッド regexp

    public boolean regexp([boolean UseRegExp])

#### <a name="parameters"></a>パラメーター

UseRegExp  

#### <a name="return-value"></a>戻り値

### <a name="method-replace"></a>メソッド replace

    public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)

#### <a name="parameters"></a>パラメーター

SearchString  

<!-- -->

ReplaceString  

<!-- -->

ReplaceAll  

#### <a name="return-value"></a>戻り値

### <a name="method-search"></a>メソッド search

    public boolean search(str SearchString)

#### <a name="parameters"></a>パラメーター

SearchString  

#### <a name="return-value"></a>戻り値

### <a name="method-searchstring"></a>メソッド searchString

    public str searchString()

#### <a name="return-value"></a>戻り値

### <a name="method-selectionendcol"></a>メソッド selectionEndCol

    public int selectionEndCol()

#### <a name="return-value"></a>戻り値

### <a name="method-selectionendline"></a>メソッド selectionEndLine

    public int selectionEndLine()

#### <a name="return-value"></a>戻り値

### <a name="method-selectionstartcol"></a>メソッド selectionStartCol

    public int selectionStartCol()

#### <a name="return-value"></a>戻り値

### <a name="method-selectionstartline"></a>メソッド selectionStartLine

    public int selectionStartLine()

#### <a name="return-value"></a>戻り値

### <a name="method-open"></a>メソッド open

    public static Editor open(str documentPath)

#### <a name="parameters"></a>パラメーター

documentPath  

#### <a name="return-value"></a>戻り値

### <a name="method-gotoline"></a>メソッド gotoLine

    public void gotoLine(int LineNo)

#### <a name="parameters"></a>パラメーター

LineNo  

### <a name="method-closeapplicationobjectdialog"></a>メソッド closeApplicationObjectDialog

    public void closeApplicationObjectDialog()

### <a name="method-mark"></a>メソッド mark

    public void mark(int line, int col)

#### <a name="parameters"></a>パラメーター

明細行  

<!-- -->

col  

### <a name="method-executescript"></a>メソッド executeScript

    public void executeScript(str scriptName)

#### <a name="parameters"></a>パラメーター

scriptName  

### <a name="method-nextline"></a>メソッド nextLine

    public void nextLine()

### <a name="method-firstselectedline"></a>メソッド firstSelectedLine

    public void firstSelectedLine()

### <a name="method-new"></a>メソッド new

Editor クラスの新しいインスタンスを初期化します。

    private void new()

### <a name="method-unmark"></a>メソッド unmark

    public void unmark()

### <a name="method-insertstring"></a>メソッド insertString

    public void insertString(str InsString)

#### <a name="parameters"></a>パラメーター

InsString  

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-nextselectedline"></a>メソッド nextSelectedLine

    public void nextSelectedLine()

### <a name="method-closesearchdialog"></a>メソッド closeSearchDialog

    public void closeSearchDialog()

### <a name="method-deletelines"></a>メソッド deleteLines

    public void deleteLines([int noOfLines])

#### <a name="parameters"></a>パラメーター

noOfLines  

### <a name="method-insertlines"></a>メソッド insertLines

    public void insertLines(str InsString)

#### <a name="parameters"></a>パラメーター

InsString  

### <a name="method-firstline"></a>メソッド firstLine

    public void firstLine()

### <a name="method-deletechars"></a>メソッド deleteChars

    public void deleteChars([int noOfChars])

#### <a name="parameters"></a>パラメーター

noOfChars  

## <a name="class-enumerator"></a>クラス列挙子
    class Enumerator extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                          |
|-------------------------------|------------------------------------------------------|
| public AnyType current()      |                                                      |
| public str definitionString() |                                                      |
| public boolean moveNext()     |                                                      |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。 |
| public void reset()           |                                                      |

### <a name="method-current"></a>メソッド current

    public AnyType current()

#### <a name="return-value"></a>戻り値

### <a name="method-definitionstring"></a>メソッド definitionString

    public str definitionString()

#### <a name="return-value"></a>戻り値

### <a name="method-movenext"></a>メソッド moveNext

    public boolean moveNext()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-reset"></a>メソッド reset

    public void reset()

## <a name="class-executepermission"></a>クラス ExecutePermission
    class ExecutePermission extends CodeAccessPermission

ExecutePermission クラスは、X++ コードの実行を制御します。

### <a name="remarks"></a>備考

このクラスは、特定の API のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::dema メソッドが呼び出される同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。 次のいずれかの方法でサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

### <a name="examples"></a>例

次のコード例は、ExecutePermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが Thread.new メソッドを呼び出して新規スレッドを作成できることが宣言されます。

    server static void main(Args args) 
    { 
        Thread _t; 
        ExecutePermission _perm; 
        _perm = new ExecutePermission(); 
        if (!_perm) 
        { 
            return; 
        } 
        _perm.assert(); 
        // Invoke the protected API. 
         _t = new Thread(); 
        // Call member methods. 
        if (_t) 
        { 
            _t.removeOnComplete(true); 
            _t.run(classnum(SysCodeProfiler), identifierstr(transferFile)); 
        } 
        // Optionally, call revertAssert() to limit scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new()                                      | ExecutePermission クラスの新しいインスタンスを初期化します。                       |

### <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在のアクセス許可オブジェクトのコピーです。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。

### <a name="method-new"></a>メソッド new

ExecutePermission クラスの新しいインスタンスを初期化します。 終了。

    public void new()




