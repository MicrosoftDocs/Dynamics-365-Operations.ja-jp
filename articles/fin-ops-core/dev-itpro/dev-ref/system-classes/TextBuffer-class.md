---
title: TextBuffer クラス
description: このトピックでは、TextBuffer クラスについて説明します。
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
ms.openlocfilehash: ac38afd29dbc6511333ecc5eacf9bfdc4d186419
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502790"
---
# <a name="class-textbuffer"></a>クラス TextBuffer

[!include [banner](../../includes/banner.md)]

```xpp
class TextBuffer extends Object
```

TextBuffer クラスは、任意のテキスト ファイル内容を管理し、テキストを生成して操作します。

## <a name="remarks"></a>備考

このクラスは、さまざまな文字列操作、シンプルなクリップボード、ファイル インターフェイスを備えています。

## <a name="examples"></a>例

```xpp
static void example() 
{ 
    FileIoPermission _perm = new FileIoPermission("myfile.txt",'r'); 
    TextBuffer txtb = new TextBuffer(); 
    _perm.assert(); 
    txtb.fromFile("myfile.txt"); // Read text from file 
    txtb.toClipboard(); // Copy it to the clipboard 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                 | 説明                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| public boolean accept(str searchText)                                  |                                                                                                       |
| public int decryptOld(int cryptKey)                                    |                                                                                                       |
| public boolean find(str searchText, \[int start\])                     | TextBuffer オブジェクトで文字列式の発生を検索します。                             |
| public boolean fromClipboard()                                         | TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。                      |
| public boolean fromFile(str filename, \[int encoding\])                | TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。                   |
| public str getText()                                                   | TextBuffer オブジェクトの現在の内容を取得します。                                               |
| public int getValue()                                                  |                                                                                                       |
| public boolean ignoreCase(\[boolean ignoreCase\])                      |                                                                                                       |
| public boolean isNext(str searchText)                                  |                                                                                                       |
| public int matchLen()                                                  | TextBuffer オブジェクトで最初に一致する文字列の長さを返します。                                |
| public int matchPos()                                                  | TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。 |
| public str nextToken(\[boolean includeWholeLine\], \[str stopAtChar\]) |                                                                                                       |
| public int numLines()                                                  | TextBuffer オブジェクトの明細行の数を取得します。                                               |
| public boolean regularExpressions(\[boolean useRegularExpressions\])   |                                                                                                       |
| public int size()                                                      |                                                                                                       |
| public str subStr(int start, int length)                               | TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。                                 |
| public boolean toFile(str filename, \[int encoding\])                  | TextBuffer オブジェクトの内容をファイルに保存します。                                                 |
| public str token()                                                     |                                                                                                       |
| public str toString()                                                  | 現在のオブジェクトを表す文字列を返します。                                                  |
| ::public static int strHashKey(str sourceString)                       |                                                                                                       |
| public void new()                                                      | TextBuffer クラスの新しいインスタンスを初期化します。                                                   |
| public void removeChar(str charList)                                   |                                                                                                       |
| public void toClipboard()                                              | TextBuffer オブジェクトの内容をクリップボードにコピーします。                                           |
| public void insert(str insertString, int position)                     |                                                                                                       |
| public void setText(str string)                                        | 既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。  |
| public void appendText(str string)                                     | TextBuffer オブジェクトの内容に文字列を追加します。                                             |
| public void replace(str findString, str replaceString)                 |                                                                                                       |
| public void delete(int start, int length)                              |                                                                                                       |

## <a name="method-accept"></a>メソッド accept

```xpp
public boolean accept(str searchText)
```

### <a name="parameters---accept"></a>パラメーター - accept

searchText  

### <a name="return-value---accept"></a>戻り値 - accept

## <a name="method-decryptold"></a>メソッド decryptOld

```xpp
public int decryptOld(int cryptKey)
```

### <a name="parameters---decryptold"></a>パラメーター - decryptOld

cryptKey  

### <a name="return-value---decryptold"></a>戻り値 - decryptOld

## <a name="method-find"></a>メソッド find

TextBuffer オブジェクトで文字列式の発生を検索します。

```xpp
public boolean find(str searchText, [int start])
```

### <a name="parameters---find"></a>パラメーター - find

searchText  
各検索の開始位置を設定する数式 (オプション)。 このパラメータを省略すると、検索は、最初の文字位置から開始します。

<!-- -->

開始  
各検索の開始位置を設定する数式 (オプション)。 このパラメータを省略すると、検索は、最初の文字位置から開始します。

### <a name="return-value---find"></a>戻り値 - find

searchText が見つかった場合は true。それ以外の場合は、false。

### <a name="remarks---find"></a>備考 - find

このメソッドは、正規表現を使用して、大文字と小文字を区別しないテキスト比較を実行します。 詳細については、「一致する機能」を参照してください。 大文字と小文字を区別しないようにするには、ignoreCase メソッドを使用します。 正規表現は、regularExpressions メソッドを使用してオフにすることができます。

### <a name="examples---find"></a>例 - find

次の例では、指定した文字列の発生のすべてについて TextBuffer オブジェクトを検索し、一致が検出された位置を出力します。

```xpp
int pos; 
TextBuffer textBuffer; 
textBuffer = new TextBuffer(); 
textBuffer.setText("ABC DEF GHI JKL MNO ABC ABC"); 
pos = 0; 
while (textBuffer.find("ABC",pos)) 
{ 
    print "String found at position: ", textBuffer.matchPos(); 
    pause; 
    pos = textBuffer.matchPos()+1; 
}
```

## <a name="method-fromclipboard"></a>メソッド fromClipboard

TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。

```xpp
public boolean fromClipboard()
```

### <a name="return-value---fromclipboard"></a>戻り値 - fromClipboard

置換が成功した場合は true。それ以外の場合は、false。

### <a name="examples---fromclipboard"></a>例 - fromClipboard

```xpp
{ 
    TextBuffer txtb = new textBuffer(); 
    FileIoPermission perm; 
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("w") 
    // Set code access permission to help protect the use of 
    // TextBuffer.tofile 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    perm.assert(); 
    if ( txtb.fromClipboard() ) 
    { 
        // Got text from clipboard - save it to file 
        txtb.toFile(#ExampleFile); 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-fromfile"></a>メソッド fromFile

TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。

```xpp
public boolean fromFile(str filename, [int encoding])
```

### <a name="parameters---fromfile"></a>パラメーター - fromFile

filename  
エンコードに使用できるオプション (オプション)。

<!-- -->

encoding  
エンコードに使用できるオプション (オプション)。

### <a name="return-value---fromfile"></a>戻り値 - fromFile

フィールド操作が成功した場合は true。それ以外の場合は、false。

### <a name="remarks---fromfile"></a>備考 - fromFile

FileEncoding システム列挙によって提供されるエンコーディング パラメーターの可能な値は次のとおりです。

-   ACP
-   UTF8
-   UTF16BE
-   UTF16LE
-   GB18030
-   AUTO

ファイルの操作に失敗した場合、TextBuffer オブジェクトは変更されません。 攻撃者が fromFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="method-gettext"></a>メソッド getText

TextBuffer オブジェクトの現在の内容を取得します。

```xpp
public str getText()
```

### <a name="return-value---gettext"></a>戻り値 - getText

TextBuffer オブジェクトのコンテンツを含む文字列。

### <a name="remarks---gettext"></a>備考 - getText

TextBuffer は、新しい明細行を含むことができ、これが、返される文字列に含まれます。

## <a name="method-getvalue"></a>メソッド getValue

```xpp
public int getValue()
```

### <a name="return-value---getvalue"></a>戻り値 - getValue

## <a name="method-ignorecase"></a>メソッド ignoreCase

```xpp
public boolean ignoreCase([boolean ignoreCase])
```

### <a name="parameters---ignorecase"></a>パラメーター - ignoreCase

ignoreCase  

### <a name="return-value---ignorecase"></a>戻り値 - ignoreCase

## <a name="method-isnext"></a>メソッド isNext

```xpp
public boolean isNext(str searchText)
```

### <a name="parameters---isnext"></a>パラメーター - isNext

searchText  

### <a name="return-value---isnext"></a>戻り値 - isNext

## <a name="method-matchlen"></a>メソッド matchLen

TextBuffer オブジェクトで最初に一致する文字列の長さを返します。

```xpp
public int matchLen()
```

### <a name="return-value---matchlen"></a>戻り値 - matchLen

見つかった一致の長さ。一致するものが見つからない場合は 0 (ゼロ)。

### <a name="remarks---matchlen"></a>備考 - matchLen

このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。

## <a name="method-matchpos"></a>メソッド matchPos

TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。

```xpp
public int matchPos()
```

### <a name="return-value---matchpos"></a>戻り値 - matchPos

一致が見つかった位置。一致しない場合は 0 (ゼロ)。

### <a name="remarks---matchpos"></a>備考 - matchPos

このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。

## <a name="method-nexttoken"></a>メソッド nextToken

```xpp
public str nextToken([boolean includeWholeLine], [str stopAtChar])
```

### <a name="parameters---nexttoken"></a>パラメーター - nextToken

includeWholeLine  

<!-- -->

stopAtChar  

### <a name="return-value---nexttoken"></a>戻り値 - nextToken

## <a name="method-numlines"></a>メソッド numLines

TextBuffer オブジェクトの明細行の数を取得します。

```xpp
public int numLines()
```

### <a name="return-value---numlines"></a>戻り値 - numLines

コンテンツ内の行数。

### <a name="remarks---numlines"></a>備考 - numLines

行は改行 ('\\n') で区切られます。

### <a name="examples---numlines"></a>例 - numLines

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    if (txtb.fromClipboard()) 
    { 
        print "Clipboard contains ",txtb.numLines()," lines."; 
    } 
}
```

## <a name="method-regularexpressions"></a>メソッド regularExpressions

```xpp
public boolean regularExpressions([boolean useRegularExpressions])
```

### <a name="parameters---regularexpressions"></a>パラメーター - regularExpressions

useRegularExpressions  

### <a name="return-value---regularexpressions"></a>戻り値 - regularExpressions

## <a name="method-size"></a>メソッド size

```xpp
public int size()
```

### <a name="return-value---size"></a>戻り値 - size

## <a name="method-substr"></a>メソッド subStr

TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。

```xpp
public str subStr(int start, int length)
```

### <a name="parameters---substr"></a>パラメーター - subStr

開始  
目的のサブ文字列の長さ。

<!-- -->

length  
目的のサブ文字列の長さ。

### <a name="return-value---substr"></a>戻り値 - subStr

TextBuffer オブジェクト コンテンツの指定された部分を含む文字列。

### <a name="remarks---substr"></a>備考 - subStr

部分文字列の開始位置を指定するときは、コンテンツの最初の文字に 1 を、2 番目の文字に 2 というように使用します。

### <a name="examples---substr"></a>例 - subStr

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    str mystr; 
    if (txtb.fromClipboard()) 
    { 
        mystr = txtb.subStr(10,15);  
        // 15 long substring starting at position 10. 
    } 
}
```

## <a name="method-tofile"></a>メソッド toFile

TextBuffer オブジェクトの内容をファイルに保存します。

```xpp
public boolean toFile(str filename, [int encoding])
```

### <a name="parameters---tofile"></a>パラメーター - toFile

filename  

<!-- -->

encoding  

### <a name="return-value---tofile"></a>戻り値 - toFile

操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---tofile"></a>備考 - toFile

指定したファイルが既に存在する場合は、確認なしで上書きされます。 攻撃者が toFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="method-token"></a>メソッド token

```xpp
public str token()
```

### <a name="return-value---token"></a>戻り値 - token

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-strhashkey"></a>メソッド strHashKey

```xpp
public static int strHashKey(str sourceString)
```

### <a name="parameters---strhashkey"></a>パラメーター - strHashKey

sourceString  

### <a name="return-value---strhashkey"></a>戻り値 - strHashKey

## <a name="method-new"></a>メソッド new

TextBuffer クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-removechar"></a>メソッド removeChar

```xpp
public void removeChar(str charList)
```

### <a name="parameters---removechar"></a>パラメーター - removeChar

charList  

## <a name="method-toclipboard"></a>メソッド toClipboard

TextBuffer オブジェクトの内容をクリップボードにコピーします。

```xpp
public void toClipboard()
```

## <a name="method-insert"></a>メソッド insert

```xpp
public void insert(str insertString, int position)
```

### <a name="parameters---insert"></a>パラメーター - insert

insertString  

<!-- -->

職位  

## <a name="method-settext"></a>メソッド setText

既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。

```xpp
public void setText(str string)
```

### <a name="parameters---settext"></a>パラメーター - setText

文字列  
TextBuffer オブジェクトの新しいテキストを含む文字列。

### <a name="remarks---settext"></a>備考 - setText

TextBuffer オブジェクトに任意のコンテンツが含まれている場合は、新しいコンテンツで上書きされます。

### <a name="examples---settext"></a>例 - setText

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    txtb.setText("This is the first text."); 
    // Now txtb contains exactly that text. 
}
```

## <a name="method-appendtext"></a>メソッド appendText

TextBuffer オブジェクトの内容に文字列を追加します。

```xpp
public void appendText(str string)
```

### <a name="parameters---appendtext"></a>パラメーター - appendText

文字列  
追加する文字列。

### <a name="examples---appendtext"></a>例 - appendText

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    txtb.setText("[One]"); 
    txtb.appendText("[Another]"); 
    print txtb.getText(); // Will print "[One][Another]" 
}
```

## <a name="method-replace"></a>メソッド replace

```xpp
public void replace(str findString, str replaceString)
```

### <a name="parameters---replace"></a>パラメーター - replace

findString  

<!-- -->

replaceString  

## <a name="method-delete"></a>メソッド delete

```xpp
public void delete(int start, int length)
```

### <a name="parameters---delete"></a>パラメーター - delete

開始  

<!-- -->

length  

