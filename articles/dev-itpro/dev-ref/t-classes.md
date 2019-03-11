---
title: T クラス
description: 文字 T で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 51774
ms.assetid: c83d7228-86a5-404b-a978-7f6d316b7b7e
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fc536f70a5f91f6c058e14fb28469f7a966a383
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369554"
---
# <a name="t-classes"></a>T クラス

[!include [banner](../includes/banner.md)]

文字 T で始まるシステム API クラス。

<a name="class-tableextension"></a>クラス TableExtension
--------------------

    class TableExtension extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                    | 説明                                             |
|-----------------------------------------------------------|---------------------------------------------------------|
| public void new()                                         | TableExtension クラスの新しいインスタンスを初期化します。 |
| public void modifiedField(Common record, FieldId fieldId) |                                                         |
| public void defaultRow(Common record)                     |                                                         |
| public void defaultField(Common record, FieldId fieldId)  |                                                         |

### <a name="method-new"></a>メソッド new

TableExtension クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-modifiedfield"></a>メソッド modifiedField

    public void modifiedField(Common record, FieldId fieldId)

#### <a name="parameters"></a>パラメーター

記録  

<!-- -->

fieldId  

### <a name="method-defaultrow"></a>メソッド defaultRow

    public void defaultRow(Common record)

#### <a name="parameters"></a>パラメーター

記録  

### <a name="method-defaultfield"></a>メソッド defaultField

    public void defaultField(Common record, FieldId fieldId)

#### <a name="parameters"></a>パラメーター

記録  

<!-- -->

fieldId  

## <a name="class-textbuffer"></a>クラス TextBuffer
    class TextBuffer extends Object

TextBuffer クラスは、任意のテキスト ファイル内容を管理し、テキストを生成して操作します。

### <a name="remarks"></a>備考

このクラスは、さまざまな文字列操作、シンプルなクリップボード、ファイル インターフェイスを備えています。

### <a name="examples"></a>例

    static void example() 
    { 
        FileIoPermission _perm = new FileIoPermission("myfile.txt",'r'); 
        TextBuffer txtb = new TextBuffer(); 
        _perm.assert(); 
        txtb.fromFile("myfile.txt"); // Read text from file 
        txtb.toClipboard(); // Copy it to the clipboard 
    }

### <a name="methods"></a>メソッド

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

### <a name="method-accept"></a>メソッド accept

    public boolean accept(str searchText)

#### <a name="parameters"></a>パラメーター

searchText  

#### <a name="return-value"></a>戻り値

### <a name="method-decryptold"></a>メソッド decryptOld

    public int decryptOld(int cryptKey)

#### <a name="parameters"></a>パラメーター

cryptKey  

#### <a name="return-value"></a>戻り値

### <a name="method-find"></a>メソッド find

TextBuffer オブジェクトで文字列式の発生を検索します。

    public boolean find(str searchText, [int start])

#### <a name="parameters"></a>パラメーター

searchText  
各検索の開始位置を設定する数式 (オプション)。 このパラメータを省略すると、検索は、最初の文字位置から開始します。

<!-- -->

開始  
各検索の開始位置を設定する数式 (オプション)。 このパラメータを省略すると、検索は、最初の文字位置から開始します。

#### <a name="return-value"></a>戻り値

searchText が見つかった場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは、正規表現を使用して、大文字と小文字を区別しないテキスト比較を実行します。 詳細については、「一致する機能」を参照してください。 大文字と小文字を区別しないようにするには、ignoreCase メソッドを使用します。 正規表現は、regularExpressions メソッドを使用してオフにすることができます。

#### <a name="examples"></a>例

次の例では、指定した文字列の発生のすべてについて TextBuffer オブジェクトを検索し、一致が検出された位置を出力します。

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

### <a name="method-fromclipboard"></a>メソッド fromClipboard

TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。

    public boolean fromClipboard()

#### <a name="return-value"></a>戻り値

置換が成功した場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

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

### <a name="method-fromfile"></a>メソッド fromFile

TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。

    public boolean fromFile(str filename, [int encoding])

#### <a name="parameters"></a>パラメーター

filename  
エンコードに使用できるオプション (オプション)。

<!-- -->

encoding  
エンコードに使用できるオプション (オプション)。

#### <a name="return-value"></a>戻り値

フィールド操作が成功した場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

FileEncoding システム列挙によって提供されるエンコーディング パラメーターの可能な値は次のとおりです。

-   ACP
-   UTF8
-   UTF16BE
-   UTF16LE
-   GB18030
-   AUTO

ファイルの操作に失敗した場合、TextBuffer オブジェクトは変更されません。 攻撃者が fromFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="method-gettext"></a>メソッド getText

TextBuffer オブジェクトの現在の内容を取得します。

    public str getText()

#### <a name="return-value"></a>戻り値

TextBuffer オブジェクトのコンテンツを含む文字列。

#### <a name="remarks"></a>備考

TextBuffer は、新しい明細行を含むことができ、これが、返される文字列に含まれます。

### <a name="method-getvalue"></a>メソッド getValue

    public int getValue()

#### <a name="return-value"></a>戻り値

### <a name="method-ignorecase"></a>メソッド ignoreCase

    public boolean ignoreCase([boolean ignoreCase])

#### <a name="parameters"></a>パラメーター

ignoreCase  

#### <a name="return-value"></a>戻り値

### <a name="method-isnext"></a>メソッド isNext

    public boolean isNext(str searchText)

#### <a name="parameters"></a>パラメーター

searchText  

#### <a name="return-value"></a>戻り値

### <a name="method-matchlen"></a>メソッド matchLen

TextBuffer オブジェクトで最初に一致する文字列の長さを返します。

    public int matchLen()

#### <a name="return-value"></a>戻り値

見つかった一致の長さ。一致するものが見つからない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。

### <a name="method-matchpos"></a>メソッド matchPos

TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。

    public int matchPos()

#### <a name="return-value"></a>戻り値

一致が見つかった位置。一致しない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。

### <a name="method-nexttoken"></a>メソッド nextToken

    public str nextToken([boolean includeWholeLine], [str stopAtChar])

#### <a name="parameters"></a>パラメーター

includeWholeLine  

<!-- -->

stopAtChar  

#### <a name="return-value"></a>戻り値

### <a name="method-numlines"></a>メソッド numLines

TextBuffer オブジェクトの明細行の数を取得します。

    public int numLines()

#### <a name="return-value"></a>戻り値

コンテンツ内の行数。

#### <a name="remarks"></a>備考

行は改行 ('\\n') で区切られます。

#### <a name="examples"></a>例

    { 
        TextBuffer txtb = new TextBuffer(); 
        if (txtb.fromClipboard()) 
        { 
            print "Clipboard contains ",txtb.numLines()," lines."; 
        } 
    }

### <a name="method-regularexpressions"></a>メソッド regularExpressions

    public boolean regularExpressions([boolean useRegularExpressions])

#### <a name="parameters"></a>パラメーター

useRegularExpressions  

#### <a name="return-value"></a>戻り値

### <a name="method-size"></a>メソッド size

    public int size()

#### <a name="return-value"></a>戻り値

### <a name="method-substr"></a>メソッド subStr

TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。

    public str subStr(int start, int length)

#### <a name="parameters"></a>パラメーター

開始  
目的のサブ文字列の長さ。

<!-- -->

length  
目的のサブ文字列の長さ。

#### <a name="return-value"></a>戻り値

TextBuffer オブジェクト コンテンツの指定された部分を含む文字列。

#### <a name="remarks"></a>備考

部分文字列の開始位置を指定するときは、コンテンツの最初の文字に 1 を、2 番目の文字に 2 というように使用します。

#### <a name="examples"></a>例

    { 
        TextBuffer txtb = new TextBuffer(); 
        str mystr; 
        if (txtb.fromClipboard()) 
        { 
            mystr = txtb.subStr(10,15);  
            // 15 long substring starting at position 10. 
        } 
    }

### <a name="method-tofile"></a>メソッド toFile

TextBuffer オブジェクトの内容をファイルに保存します。

    public boolean toFile(str filename, [int encoding])

#### <a name="parameters"></a>パラメーター

filename  

<!-- -->

encoding  

#### <a name="return-value"></a>戻り値

操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

指定したファイルが既に存在する場合は、確認なしで上書きされます。 攻撃者が toFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="method-token"></a>メソッド token

    public str token()

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-strhashkey"></a>メソッド strHashKey

    public static int strHashKey(str sourceString)

#### <a name="parameters"></a>パラメーター

sourceString  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TextBuffer クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-removechar"></a>メソッド removeChar

    public void removeChar(str charList)

#### <a name="parameters"></a>パラメーター

charList  

### <a name="method-toclipboard"></a>メソッド toClipboard

TextBuffer オブジェクトの内容をクリップボードにコピーします。

    public void toClipboard()

### <a name="method-insert"></a>メソッド insert

    public void insert(str insertString, int position)

#### <a name="parameters"></a>パラメーター

insertString  

<!-- -->

職位  

### <a name="method-settext"></a>メソッド setText

既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。

    public void setText(str string)

#### <a name="parameters"></a>パラメーター

string  
TextBuffer オブジェクトの新しいテキストを含む文字列。

#### <a name="remarks"></a>備考

TextBuffer オブジェクトに任意のコンテンツが含まれている場合は、新しいコンテンツで上書きされます。

#### <a name="examples"></a>例

    { 
        TextBuffer txtb = new TextBuffer(); 
        txtb.setText("This is the first text."); 
        // Now txtb contains exactly that text. 
    }

### <a name="method-appendtext"></a>メソッド appendText

TextBuffer オブジェクトの内容に文字列を追加します。

    public void appendText(str string)

#### <a name="parameters"></a>パラメーター

string  
追加する文字列。

#### <a name="examples"></a>例

    { 
        TextBuffer txtb = new TextBuffer(); 
        txtb.setText("[One]"); 
        txtb.appendText("[Another]"); 
        print txtb.getText(); // Will print "[One][Another]" 
    }

### <a name="method-replace"></a>メソッド replace

    public void replace(str findString, str replaceString)

#### <a name="parameters"></a>パラメーター

findString  

<!-- -->

replaceString  

### <a name="method-delete"></a>メソッド delete

    public void delete(int start, int length)

#### <a name="parameters"></a>パラメーター

開始  

<!-- -->

length  

## <a name="class-textio"></a>クラス TextIo
    class TextIo extends CommaIo

TextIo クラスには、テキスト ファイルの読み取りと書き込みを行う機能があります。

### <a name="remarks"></a>備考

TextIO は、非 ANSI コード ページ ファイル I/O のサポートを提供する AsciiIO を置き換えます。 TextIO コンストラクターには、ファイルのコード ページを設定するための追加のオプション パラメーターがあります。 TextIO.new メソッドには、ファイルのコード ページを指定するオプション引数があります。 既定値は UTF-16LE (Microsoft Windows ネイティブ Unicode 表現) です。 ほとんどの場合、特にエンドユーザーが Finance and Operations 以外のテキスト エディターでファイルを編集する可能性がある場合に、これを使用することをお勧めします。 詳細については、「TextIo.new」を参照してください。 ファイルが読み取られると、TextIO はファイルの最初の数バイトについてバイト順マーク (BOM) を調べて、UTF-8、UTF-16LE、および UTF-16BE を自動的に取り扱います。 BOM が見つからない場合、ファイルは ANSI コード ページ (ACP) 形式であると見なされます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                    | 説明                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| public str inFieldDelimiter(\[str value\])                | TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。   |
| public str inRecordDelimiter(\[str value\])               | TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。  |
| public int inRecordLength(\[int value\])                  | 入力ファイルのレコードの長さを取得または設定します。                                                                  |
| public str outFieldDelimiter(\[str value\])               | TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。  |
| public str outRecordDelimiter(\[str value\])              | TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。 |
| public container read()                                   | TextIO オブジェクトから次の完全なレコードを読み取ります。                                                                   |
| public IO\_Status status()                                | TextIo オブジェクトで実行された最後の操作のステータスを取得します。                                           |
| public boolean write(VarArg values)                       | TextIO オブジェクトによって表されるファイルにデータを記述します。                                                              |
| public boolean writeChar(int int)                         | Unicode 文字をファイルに記述します。                                                                              |
| public boolean writeExp(container data)                   | TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。                                       |
| public boolean writeRaw(str data)                         | 予約済み。                                                                                                          |
| public void new(str filename, str mode, \[int codepage\]) | TextIO クラスの新しいインスタンスを作成します。                                                                        |
| public void finalize()                                    | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。                                        |

### <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
フィールドの区切り記号として使用される文字 (オプション)。

#### <a name="return-value"></a>戻り値

フィールドの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

出力ファイルのフィールド区切り記号を設定するには、次を使用します。

#### <a name="examples"></a>例

次の例では、入力ファイルのフィールド区切り記号を '\\r\\n' に設定します.

    protected void openFile() 
    { 
        #define.delimiter('\r\n') 
        super(); 
        importFile.inFieldDelimiter(#delimiter); 
    }

### <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
オプションでレコードの区切り記号として使用される文字。

#### <a name="return-value"></a>戻り値

レコードの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

出力ファイルのレコード区切り記号を設定するには、次を使用します。

#### <a name="examples"></a>例

次の例では、レコード区切り記号を 128 に設定します。

    boolean openFile() 
    { 
        boolean ret = false; 
        int     recordLength = 128; 
        int     numOflastCharacter = 255; 
        textFile = new TextIo(filename, 'r'); 
        if (textFile) 
        { 
            if (textFile.status()) 
            { 
                throw error("@SYS52680"); 
            } 
            textFile.inFieldDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordLength(recordLength); 
            ret = true; 
        } 
        return ret; 
    }

### <a name="method-inrecordlength"></a>メソッド inRecordLength

入力ファイルのレコードの長さを取得または設定します。

    public int inRecordLength([int value])

#### <a name="parameters"></a>パラメーター

値  
入力ファイルのレコードの長さ (オプション)。

#### <a name="return-value"></a>戻り値

入力ファイルのレコードの長さ。

#### <a name="remarks"></a>備考

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを確認します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

#### <a name="examples"></a>例

次の例では、レコードの長さを 128 に設定します。

    boolean openFile() 
    { 
        boolean ret = false; 
        int     recordLength = 128; 
        int     numOflastCharacter = 255; 
        textFile = new TextIo(filename, 'r'); 
        if (textFile) 
        { 
            if (textFile.status()) 
            { 
                throw error("@SYS52680"); 
            } 
            textFile.inFieldDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordLength(recordLength); 
            ret = true; 
        } 
        return ret; 
    }

### <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
フィールドの区切り記号として使用される文字 (オプション)。

#### <a name="return-value"></a>戻り値

フィールドの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

入力ファイルのフィールド区切り記号を設定するには、次を使用します。

#### <a name="examples"></a>例

次の例では、出力ファイルのフィールド区切り記号を ' ' (なし) に設定します。

    void defineFile() 
    { 
        diskFile = new TextIo(diskFileName,'W'); 
        if (!diskFile) 
        { 
            throw error("@SYS26757"); 
        } 
        diskFile.outRecordDelimiter('\r\n'); 
        diskFile.outFieldDelimiter(''); 
    }

### <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  
オプションでレコードの区切り記号として使用される文字。

#### <a name="return-value"></a>戻り値

レコードの区切り記号として使用される文字。

#### <a name="remarks"></a>備考

入力ファイルのレコード区切り記号を設定するには、次を使用します。

#### <a name="examples"></a>例

次の例では、出力ファイルのレコード区切り記号を '\\r\\n'' に設定します。

    void defineFile() 
    { 
        diskFile = new TextIo(diskFileName,'W'); 
        if (!diskFile) 
        { 
            throw error("@SYS26757"); 
        } 
        diskFile.outRecordDelimiter('\r\n'); 
        diskFile.outFieldDelimiter(''); 
    }

### <a name="method-read"></a>メソッド read

TextIO オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

1 つのレコードを保持するコンテナーです。

#### <a name="remarks"></a>備考

コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。 これらのプロパティには、最も一般的な形式の入力と出力を可能にする既定値があります。 inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッドを使用して、プロパティを調整する必要がある場合があります。

#### <a name="examples"></a>例

次の例では、ファイルからレコードを読み取り、conpeek 関数を使用してレコードから値を抽出します。

    public void run() 
    { 
        container         fileRecord; 
        IntrastatToProdCom intrastatToProdCom; 
        if (filename) 
        { 
            this.initializeFile(); 
            fileRecord = prodComFile.read(); 
            ttsbegin; 
            while (fileRecord) 
            { 
                intrastatToProdCom.IntrastatItemCodeID = conpeek(fileRecord, 1); 
                intrastatToProdCom.InventProdComCodeID = conpeek (fileRecord, 2); 
                intrastatToProdCom.ValidFromYear = conpeek (fileRecord, 3); 
                intrastatToProdCom.ValidTillYear = conpeek (fileRecord, 4); 
                intrastatToProdCom.insert(); 
                filerecord = prodComFile.read(); 
            } 
            ttscommit; 
        } 
    }

### <a name="method-status"></a>メソッド status

TextIo オブジェクトで実行された最後の操作のステータスを取得します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

最後の操作の状態。

#### <a name="examples"></a>例

次の例では、ファイルが存在しない場合、またはファイルの最後の操作が、IO\_Status::Ok 列挙値のステータスを持たない場合にエラーをスローします。

    protected void checkDiskFileStatus() 
    { 
        if (!diskFile || diskFile.status() != IO_Status::Ok) 
        { 
            throw error(strfmt("@SYS76826", diskFileName)); 
        } 
    }

### <a name="method-write"></a>メソッド write

TextIO オブジェクトによって表されるファイルにデータを記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
ファイルに書き込む値。 値はさまざまなデータ型にすることができます。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

書き込み操作が失敗した場合は、その原因を突き止めるために使用できます。 書き込みメソッドは、可変数の引数を受け入れます。 各値は、フィールドとして出力レコードに配置されます。 フィールドは、で指定されたフィールド区切り記号で区切られます。 各レコードは、によって指定された区切り記号で区切られます。 完全なコンテナーを書き込むには、次を使用します。

### <a name="method-writechar"></a>メソッド writeChar

Unicode 文字をファイルに記述します。

    public boolean writeChar(int int)

#### <a name="parameters"></a>パラメーター

int  

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。 複数の値を書き込んだり、さまざまな種類のデータをファイルに書き込むには、TextIO.write メソッドを使用します。

### <a name="method-writeexp"></a>メソッド writeExp

TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
ファイルへの書き込みのデータを持つコンテナーです。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。 コンテナー内のエントリは、outFieldDelimiter メソッドで設定された区切り文字で区切られます。 コンテナーは、outRecordDelimiter メソッドで設定された区切り文字で区切られます。

### <a name="method-writeraw"></a>メソッド writeRaw

予約済み。

    public boolean writeRaw(str data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TextIO クラスの新しいインスタンスを作成します。

    public void new(str filename, str mode, [int codepage])

#### <a name="parameters"></a>パラメーター

filename  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下は最も一般的な値です。これらのオプションの詳細については、http://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409 の一覧を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

<!-- -->

モード  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下は最も一般的な値です。これらのオプションの詳細については、http://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409 の一覧を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

<!-- -->

codepage  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下は最も一般的な値です。これらのオプションの詳細については、http://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409 の一覧を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

#### <a name="remarks"></a>備考

ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIoPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。 次のテーブルは、\_codePage パラメーターに指定できる、より一般的なコード ページの一部を示しています。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>0</td>
<td>ANSI コード ページ (ACP)</td>
<td>ユーザーの現在の言語の文字のみをサポートするコード ページ。 コード ページは、多言語データを含む可能性のあるものや、異なるコード ページを使用して 2 つのシステム間で転送される単一言語データ用には適していません。</td>
</tr>
<tr class="even">
<td>437</td>
<td>OEM コード ページ 437</td>
<td>IBM PC または MS-DOS コード ページ 437。 これは、CP437 と省略されることが多く、DOS-US や OEM-US とも呼ばれます。</td>
</tr>
<tr class="odd">
<td>850</td>
<td>コード ページ 850</td>
<td>西ヨーロッパで MS-DOS などのオペレーティング システムで使用されていたコード ページ。</td>
</tr>
<tr class="even">
<td>1200</td>
<td>UTF-16LE</td>
<td>Microsoft Windows x86 システムでのネイティブ Unicode 表現。 ほとんどすべての文字は 16 ビットとして保存されます。 一部の中国語文字には、32 ビットが必要です。 文字の残りの部分を読み取ると、識別バイト オーダー マークが書き込まれ、検査され、次に破棄されます。</td>
</tr>
<tr class="odd">
<td>1201</td>
<td>UTF-16BE</td>
<td>UTF-16LE と同じですが、バイトスワップします。 下位から上位ではなく左から右へバイトを格納する x86 以外のシステムとの互換性のために使用されます。 文字の残りの部分を読み取ると、識別バイト オーダー マークが最初に書き込まれ、検査され、次に破棄されます。</td>
</tr>
<tr class="even">
<td>65001</td>
<td>UTF-8</td>
<td>バイト ストリームしやすい方法で Unicode を保存します。
<ul>
<li>ASCII 文字は、1 バイトです。</li>
<li>欧州のアルファベット (基本分音記号を含む) は文字あたり 2 バイト</li>
<li>中国語、日本語、韓国語の場合、文字あたり 3 バイト必要</li>
</ul>
このコード ページは、ファイルに含まれているASCIIの割合が非常に高く、その他の文字が比較的少なく、スペースを節約することが重要な場合に適しています。 たとえば、.xpo ファイルは、UTF-8 に格納されます。 UTF-8 ファイルは、3 バイトのバイト順序マーク列で始まり、この項目が最初に書き込まれます。 それを調べてから、文字の残りの部分を読み取ると破棄されます。</td>
</tr>
<tr class="odd">
<td>54936</td>
<td>GB-18030</td>
<td>中国政府によって求められている GB-18030 文字表現でデータを格納します。 バイト順序マークは書き込まれません。 これらのファイルは、ファイルに GB-2312 のレパートリー外の文字が含まれていない限り、コード ページ 20936 (GB-2312、中国語 (簡体) システム用の ACP) で記述されたファイルと区別できません。</td>
</tr>
</tbody>
</table>

#### <a name="examples"></a>例

次の例では、コード ページ 850 エンコードを使用して、読み取りモードで filename という名前のファイルにアクセスする TextIO オブジェクトを作成します。

    protected void openFile(str _fileOpen = #io_read) 
    { 
        importFile = new TextIo(filename, _fileOpen, 850); 
        if (! importFile) 
        { 
            throw error(strfmt("@SYS18678", filename)); 
        } 
    }

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

通常、TextIO オブジェクトは、スコープを離れることによって確定されます。 確定メソッドは、通常は直接呼び出されません。 TextIO オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。

## <a name="class-tilereference"></a>クラス TileReference
    class TileReference extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明 |
|-----------------------------------------------------|-------------|
| public str tile()                                   |             |
| public int copyCallerQuery()                        |             |
| public int formViewOption()                         |             |
| public int openMode()                               |             |
| public str parameters()                             |             |
| public boolean isFound()                            |             |
| public ConfigurationKeyId configurationKeyId()      |             |
| public ConfigurationKeyId countryConfigurationKey() |             |
| public str countryRegionCodes()                     |             |
| public str helpText()                               |             |
| public int imageLocation()                          |             |
| public str kpiName()                                |             |
| public MenuItemType menuItemType()                  |             |
| public str menuItemName()                           |             |
| public str normalImage()                            |             |
| public int size()                                   |             |
| public int tileType()                               |             |
| public int tileDisplay()                            |             |
| public int buttonDisplay()                          |             |
| public str url()                                    |             |
| public str label()                                  |             |
| public int refreshFrequency()                       |             |
| public int applyFilter()                            |             |
| public int allowUserCacheRefresh()                  |             |
| public str query()                                  |             |
| public boolean visible(\[boolean value\])           |             |

### <a name="method-tile"></a>メソッド tile

    public str tile()

#### <a name="return-value"></a>戻り値

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public int copyCallerQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-formviewoption"></a>メソッド formViewOption

    public int formViewOption()

#### <a name="return-value"></a>戻り値

### <a name="method-openmode"></a>メソッド openMode

    public int openMode()

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

    public str parameters()

#### <a name="return-value"></a>戻り値

### <a name="method-isfound"></a>メソッド isFound

    public boolean isFound()

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

### <a name="method-countryconfigurationkey"></a>メソッド countryConfigurationKey

    public ConfigurationKeyId countryConfigurationKey()

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes()

#### <a name="return-value"></a>戻り値

### <a name="method-helptext"></a>メソッド helpText

    public str helpText()

#### <a name="return-value"></a>戻り値

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation()

#### <a name="return-value"></a>戻り値

### <a name="method-kpiname"></a>メソッド kpiName

    public str kpiName()

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public MenuItemType menuItemType()

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName()

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage()

#### <a name="return-value"></a>戻り値

### <a name="method-size"></a>メソッド size

    public int size()

#### <a name="return-value"></a>戻り値

### <a name="method-tiletype"></a>メソッド tileType

    public int tileType()

#### <a name="return-value"></a>戻り値

### <a name="method-tiledisplay"></a>メソッド tileDisplay

    public int tileDisplay()

#### <a name="return-value"></a>戻り値

### <a name="method-buttondisplay"></a>メソッド buttonDisplay

    public int buttonDisplay()

#### <a name="return-value"></a>戻り値

### <a name="method-url"></a>メソッド url

    public str url()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

    public str label()

#### <a name="return-value"></a>戻り値

### <a name="method-refreshfrequency"></a>メソッド refreshFrequency

    public int refreshFrequency()

#### <a name="return-value"></a>戻り値

### <a name="method-applyfilter"></a>メソッド applyFilter

    public int applyFilter()

#### <a name="return-value"></a>戻り値

### <a name="method-allowusercacherefresh"></a>メソッド allowUserCacheRefresh

    public int allowUserCacheRefresh()

#### <a name="return-value"></a>戻り値

### <a name="method-query"></a>メソッド query

    public str query()

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-treenode"></a>クラス TreeNode
    class TreeNode extends Object

TreeNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内のノードを取得し、表します。

### <a name="remarks"></a>備考

このクラスとそれを拡張するクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API またはこのクラスから派生した API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 TreeNode クラスを使用すると、AOT 内の任意のノードへのハンドルを取得できます。 TreeNode クラスは、AOT内の任意の種類のノードへの参照となることができる一般的なクラスです。 このクラスには、AOT のショートカット メニューの一部の機能へのアクセスを提供することに加えて、ツリーで操作するために使用するメソッドも含まれます。 TreeNodeTraverser クラスは、AOT 内のナビゲーションでも役立ちます。 TreeNode::findNode および TreeNode::rootNode メソッドは treeNode オブジェクトを返します。これらのオブジェクトから、その他のノードを操作できます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                              | 説明                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public TreeNode SysObsoleteAttribute(UtilElementName name)                                                                                          |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute(str name, Types type)                                                                                          |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute()                                                                                                              |                                                                                                                                                                      |
| public TreeNode SysObsoleteAttribute(int nodetype)                                                                                                  |                                                                                                                                                                      |
| public boolean AOTAllowEdit()                                                                                                                       |                                                                                                                                                                      |
| public int AOTbitmapId()                                                                                                                            | ツリー ノードのビットマップのリソース ID を返します。                                                                                                              |
| public int AOTchildNodeCount()                                                                                                                      | 指定されたツリー ノードにある子ノードの数をカウントします。                                                                                                         |
| public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])                                                    |                                                                                                                                                                      |
| public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])                                                                                     | 指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。                                                                                           |
| public TreeNode AOTDuplicate()                                                                                                                      |                                                                                                                                                                      |
| public TreeNode AOTfindChild(str name, \[int nodeType\])                                                                                            | このノードの指定した子ノードを検索します。                                                                                                                         |
| public TreeNode AOTfirstChild()                                                                                                                     | ツリー ノードの最初の子ノードを取得します。                                                                                                                          |
| public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])                                                                                           |                                                                                                                                                                      |
| public int AOTgetExecutableLineCount()                                                                                                              | このノードのコードの実行可能な行の数を返します。                                                                                                        |
| public Set AOTgetExecutableLines()                                                                                                                  | このノードのコードの実行可能な行を返します。                                                                                                                  |
| public int AOTGetModel()                                                                                                                            |                                                                                                                                                                      |
| public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])                            | ツリー ノードのプロパティを含む文字列を返します。                                                                                                         |
| public Struct AOTgetPropertiesExt(\[str filter\])                                                                                                   |                                                                                                                                                                      |
| public AnyType AOTgetProperty(str name)                                                                                                             |                                                                                                                                                                      |
| public str AOTgetSource()                                                                                                                           | このノードのソース コードを返します。                                                                                                                                |
| public boolean AOTIncludeInCompare()                                                                                                                |                                                                                                                                                                      |
| public boolean AOTIsDirty()                                                                                                                         |                                                                                                                                                                      |
| public boolean AOTIsOld()                                                                                                                           | このノードが、古いモデル ストアにあるファイルのものかどうかを示します。                                                                                             |
| public boolean AOTIsPersisted()                                                                                                                     | このノードがモデル ストアに保持されているかどうかを示します。                                                                                                   |
| public boolean AOTIsProxyNode()                                                                                                                     |                                                                                                                                                                      |
| public TreeNodeIterator AOTiterator()                                                                                                               | ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。                                                                                     |
| public KernelHelpType AOTKernelHelpType()                                                                                                           |                                                                                                                                                                      |
| public UtilEntryLevel AOTLayer()                                                                                                                    | ツリー ノードのレイヤーを返します。                                                                                                                                  |
| public Set AOTLayers(\[boolean old\])                                                                                                               | そのツリー ノードで定義されているレイヤーのコレクションを返します。                                                                                                      |
| public str AOTname()                                                                                                                                | ノードの name プロパティの値を返します。                                                                                                                  |
| public int AOTnewWindow()                                                                                                                           | ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。                                                                                                          |
| public TreeNode AOTnextSibling()                                                                                                                    | ツリー ノードと同じレベルにある次のノードを返します。                                                                                                            |
| public boolean AOTObjectNode()                                                                                                                      | ノードがアプリケーション オブジェクトであるかどうかを示します。                                                                                                                 |
| public int AOToverlayBitmapId()                                                                                                                     | このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。                                                                                         |
| public TreeNode AOTparent()                                                                                                                         | ツリー ノードの親ノードを返します。                                                                                                                            |
| public TreeNode AOTprevious()                                                                                                                       | このツリー ノードの前の兄弟を返します。                                                                                                                      |
| public boolean SysObsoleteAttribute(str name)                                                                                                       |                                                                                                                                                                      |
| public str AOTtoolTip()                                                                                                                             | そのツリー ノードに関連付けられているツールヒントを返します。                                                                                                                  |
| public str AOTToString()                                                                                                                            |                                                                                                                                                                      |
| public str AOTtypeStr()                                                                                                                             | XPO ファイルで使用される要素タイプの文字列の内部コードを返します。                                                                                             |
| public UtilFileType AOTUtilFileType()                                                                                                               | TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。 UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。 |
| public int applObjectId()                                                                                                                           | 該当する場合は、アプリケーション オブジェクト ID を返します。                                                                                                                    |
| public int applObjectLayerMask()                                                                                                                    | この要素を含むレイヤーを指定するビットを返します。                                                                                                  |
| public int applObjectOldLayerMask()                                                                                                                 | ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。                                                                      |
| public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])                                                                               | 指定したレイヤーからツリー ノードのバージョンを取得します。                                                                                                         |
| public Int64 hashKey()                                                                                                                              |                                                                                                                                                                      |
| public TreeNode makeCopy()                                                                                                                          |                                                                                                                                                                      |
| public str newObjectName(\[str oldName\])                                                                                                           | 新しい要素の名前を含む文字列を返します。                                                                                                          |
| public str toString()                                                                                                                               | 現在のオブジェクトを表す文字列を返します。                                                                                                                 |
| public str treeNodeName()                                                                                                                           | ツリー ノードの名前を返します。                                                                                                                                   |
| public str treeNodePath()                                                                                                                           | アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。                                                                                   |
| public TreeNodeType treeNodeType()                                                                                                                  | ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。                                                                |
| public int updateNodePermissions(boolean throwExceptions)                                                                                           |                                                                                                                                                                      |
| public UtilElements utilElement()                                                                                                                   | ノードに関連する UtilElements レコードを返します。                                                                                                           |
| public UtilIdElements utilIdElement()                                                                                                               | ノードに関連する UtilIdElements レコードを返します。                                                                                                         |
| public boolean validateNameCharacters(str name)                                                                                                     |                                                                                                                                                                      |
| ::public static TreeNode findNode(str path)                                                                                                         | アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。                                                                                                       |
| ::public static str generateObjectName(str template)                                                                                                |                                                                                                                                                                      |
| ::public static int getMaximumNodeNameLength(int modelElementTypeId)                                                                                |                                                                                                                                                                      |
| ::public static boolean isNodeReferenceValid(TreeNode treeNode)                                                                                     |                                                                                                                                                                      |
| ::public static boolean isValidObjectName(str name)                                                                                                 | 引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。                                           |
| ::public static TreeNode rootNode()                                                                                                                 | AOT のルート ノードを返します。                                                                                                                                    |
| public void SysObsoleteAttribute()                                                                                                                  |                                                                                                                                                                      |
| public void treeNodeRelease()                                                                                                                       | ツリー ノードが明示的に解放されます。                                                                                                                                   |
| public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\]) |                                                                                                                                                                      |
| public void AOTrun()                                                                                                                                | アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。                                                                                             |
| public void SysObsoleteAttribute()                                                                                                                  |                                                                                                                                                                      |
| public void AOTrefresh()                                                                                                                            | .aod ファイルを最新版に変更することによりノードを更新します。                                                                                                         |
| public void SysObsoleteAttribute(Struct struct1)                                                                                                    |                                                                                                                                                                      |
| public void SysObsoleteAttribute(str properties)                                                                                                    |                                                                                                                                                                      |
| public void AOTconfigure()                                                                                                                          |                                                                                                                                                                      |
| public void AOTload()                                                                                                                               | オブジェクトが読み込み済みであるか確認します。                                                                                                                                   |
| public void treeNodeExport(str filename, \[int flag\])                                                                                              | アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。                                                                                            |
| public void SysObsoleteAttribute(str source, \[boolean isStatic\])                                                                                  |                                                                                                                                                                      |
| public void AOTendXref()                                                                                                                            |                                                                                                                                                                      |
| public void AOTmessageLine(str text, int linenumber)                                                                                                | アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。                                                                                                     |
| public void SysObsoleteAttribute(str name, AnyType value)                                                                                           |                                                                                                                                                                      |
| public void AOTrestore(\[boolean forceReload\])                                                                                                     | 該当する場合は、ディスクからこのノードを再読み込みします。                                                                                                                      |
| public void AOTregenerate()                                                                                                                         |                                                                                                                                                                      |
| public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])                                                                                          | このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。                                                                                  |
| public void AOTedit(\[int Line\], \[int Column\])                                                                                                   | このノードの適切なエディタを開きます。                                                                                                                          |
| public void AOTshowProperties()                                                                                                                     | プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。                                                                               |
| public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])                                                              | このノードのサブノード間にノードを挿入します。                                                                                                                      |
| public void new()                                                                                                                                   | TreeNode クラスの新しいインスタンスを初期化します。                                                                                                                    |
| public void AOTMove(TreeNode parent, \[TreeNode after\])                                                                                            |                                                                                                                                                                      |
| public void SysObsoleteAttribute(int modelId)                                                                                                       |                                                                                                                                                                      |

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public TreeNode SysObsoleteAttribute(UtilElementName name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public TreeNode SysObsoleteAttribute(str name, Types type)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public TreeNode SysObsoleteAttribute()

#### <a name="return-value"></a>戻り値

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public TreeNode SysObsoleteAttribute(int nodetype)

#### <a name="parameters"></a>パラメーター

nodetype  

#### <a name="return-value"></a>戻り値

### <a name="method-aotallowedit"></a>メソッド AOTAllowEdit

    public boolean AOTAllowEdit()

#### <a name="return-value"></a>戻り値

### <a name="method-aotbitmapid"></a>メソッド AOTbitmapId

ツリー ノードのビットマップのリソース ID を返します。

    public int AOTbitmapId()

#### <a name="return-value"></a>戻り値

ツリー ノードのビットマップのリソース ID。

#### <a name="examples"></a>例

次の例では、アプリケーション オブジェクト ツリー (AOT) 内の拡張データ型ノードのリソース ID を出力します。

    #AOT 
    static void myJobAOTbitmapId(Args _args) 
    { 
        treeNode treeNode = TreeNode::findNode(#ExtendedDataTypesPath); 
        print treeNode.AOTbitmapId(); 
        pause; 
    }

このジョブは整数 895 を出力します。 チュートリアルのリソース フォームを実行すると、ビットマップを参照し、それが AOT 内での拡張データ型に使用されるものと同じであることが分かります。

### <a name="method-aotchildnodecount"></a>メソッド AOTchildNodeCount

指定されたツリー ノードにある子ノードの数をカウントします。

    public int AOTchildNodeCount()

#### <a name="return-value"></a>戻り値

ツリー ノードの子ノードの数を示す整数。

#### <a name="examples"></a>例

次の例では、アプリケーション オブジェクト ツリー (AOT) のメニュー アイテム ノードの下に表示される子ノードの数を出力します。

    #AOT 
    static void myJobAOTchildNodeCount(Args _args) 
    { 
        treeNode treeNode = TreeNode::findNode(#MenuItemsPath); 
        print "Number of nodes below Menu Items: ", treeNode.AOTchildNodeCount(); 
        pause; 
    }

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute([int flag], [boolean forceNoXRef], [boolean fastMode])

#### <a name="parameters"></a>パラメーター

flag  

<!-- -->

forceNoXRef  

<!-- -->

fastMode  

#### <a name="return-value"></a>戻り値

### <a name="method-aotdrop"></a>メソッド AOTDrop

指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。

    public boolean AOTDrop(TreeNode sourcenode, [TreeNode after])

#### <a name="parameters"></a>パラメーター

sourcenode  
ソースが後で挿入されるツリー ノードの子ノード (オプション)。

<!-- -->

以後  
ソースが後で挿入されるツリー ノードの子ノード (オプション)。

#### <a name="return-value"></a>戻り値

ドロップ操作が成功した場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、tutorial\_Form\_Controls フォームの underTab:Tab の最後のノードとして、tabPage:CopyOfContainers ツリー ノードを作成します。

    #AOT 
    static void myJobAOTDrop(Args _args) 
    { 
        treeNode treeNodeTab; 
        treeNode treeNodeTabPageContainers; 
        treeNodeTab = TreeNode::findNode(#FormsPath + '\\' +  
            formStr(tutorial_form_controls)+ '\\Designs\\Design\\[Tab:Tab]'); 
        treeNodeTabPageContainers = TreeNode::findNode(#FormsPath + '\\' +  
            formStr(tutorial_form_controls)+  
            '\\Designs\\Design\\[Tab:Tab]\\[TabPage:Containers]'); 
        if (treeNodeTab && treeNodeTabPageContainers) 
        { 
            // Drop the TabPage:Containers node on the Tab:Tab node. 
            print treeNodeTab.AOTDrop(treeNodeTabPageContainers); 
        } 
        else 
        { 
            print "Could not find treeNodeTab or treeNodeTabPageContainers"; 
        } 
        pause; 
    }

### <a name="method-aotduplicate"></a>メソッド AOTDuplicate

    public TreeNode AOTDuplicate()

#### <a name="return-value"></a>戻り値

### <a name="method-aotfindchild"></a>メソッド AOTfindChild

このノードの指定した子ノードを検索します。

    public TreeNode AOTfindChild(str name, [int nodeType])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

nodeType  

#### <a name="return-value"></a>戻り値

指定した TreeNode。

### <a name="method-aotfirstchild"></a>メソッド AOTfirstChild

ツリー ノードの最初の子ノードを取得します。

    public TreeNode AOTfirstChild()

#### <a name="return-value"></a>戻り値

ツリー ノードの最初の子ノード。

### <a name="method-aotfirstchildex"></a>メソッド AOTfirstChildEx

    public TreeNode AOTfirstChildEx([boolean loadFullNode])

#### <a name="parameters"></a>パラメーター

loadFullNode  

#### <a name="return-value"></a>戻り値

### <a name="method-aotgetexecutablelinecount"></a>メソッド AOTgetExecutableLineCount

このノードのコードの実行可能な行の数を返します。

    public int AOTgetExecutableLineCount()

#### <a name="return-value"></a>戻り値

存在する場合のこのノードの実行可能コード行数。存在しない場合は、ゼロ。

#### <a name="remarks"></a>備考

この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。

### <a name="method-aotgetexecutablelines"></a>メソッド AOTgetExecutableLines

このノードのコードの実行可能な行を返します。

    public Set AOTgetExecutableLines()

#### <a name="return-value"></a>戻り値

このノードに実行可能なコード行が含まれているセット オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。

### <a name="method-aotgetmodel"></a>メソッド AOTGetModel

    public int AOTGetModel()

#### <a name="return-value"></a>戻り値

### <a name="method-aotgetproperties"></a>メソッド AOTgetProperties

ツリー ノードのプロパティを含む文字列を返します。

    public str AOTgetProperties([boolean includeInvisible], [boolean includeReadOnly], [boolean includeNonExportable])

#### <a name="parameters"></a>パラメーター

includeInvisible  

<!-- -->

includeReadOnly  

<!-- -->

includeNonExportable  

#### <a name="return-value"></a>戻り値

ツリー ノードのプロパティを含む文字列。

#### <a name="examples"></a>例

次の例では、Finance and Operations の一時テーブルのリストを示します。

    { 
        #aot 
        #properties 
        TreeNode        tn = TreeNode::findNode(#TablesPath); 
        str             tableName; 
        str             temporaryProperty; 
        tn = tn.AOTfirstChild(); 
        while (tn) 
        { 
            tableName = findProperty(tn.AOTgetProperties(), #PropertyName); 
            temporaryProperty = findProperty( 
                tn.AOTgetProperties(), 
                #PropertyTemporary); 
            info (strfmt( 
                'Table %1 has the temporary property specified as %2', 
                tableName, temporaryProperty)); 
            tn = tn.AOTnextSibling(); 
        } 
    }

### <a name="method-aotgetpropertiesext"></a>メソッド AOTgetPropertiesExt

    public Struct AOTgetPropertiesExt([str filter])

#### <a name="parameters"></a>パラメーター

フィルタ  

#### <a name="return-value"></a>戻り値

### <a name="method-aotgetproperty"></a>メソッド AOTgetProperty

    public AnyType AOTgetProperty(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

このノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

この関数はソース コードを持つノードによってオーバーライドされます。

### <a name="method-aotincludeincompare"></a>メソッド AOTIncludeInCompare

    public boolean AOTIncludeInCompare()

#### <a name="return-value"></a>戻り値

### <a name="method-aotisdirty"></a>メソッド AOTIsDirty

    public boolean AOTIsDirty()

#### <a name="return-value"></a>戻り値

### <a name="method-aotisold"></a>メソッド AOTIsOld

このノードが、古いモデル ストアにあるファイルのものかどうかを示します。

    public boolean AOTIsOld()

#### <a name="return-value"></a>戻り値

このノードが古いモデル ストアに由来する場合は true。それ以外の場合は、false。

### <a name="method-aotispersisted"></a>メソッド AOTIsPersisted

このノードがモデル ストアに保持されているかどうかを示します。

    public boolean AOTIsPersisted()

#### <a name="return-value"></a>戻り値

このノードが保持された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isModelElement() メソッドを使用します。

### <a name="method-aotisproxynode"></a>メソッド AOTIsProxyNode

    public boolean AOTIsProxyNode()

#### <a name="return-value"></a>戻り値

### <a name="method-aotiterator"></a>メソッド AOTiterator

ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。

    public TreeNodeIterator AOTiterator()

#### <a name="return-value"></a>戻り値

ツリー ノードの子を反復処理するために使用する TreeNodeIterator オブジェクト。

### <a name="method-aotkernelhelptype"></a>メソッド AOTKernelHelpType

    public KernelHelpType AOTKernelHelpType()

#### <a name="return-value"></a>戻り値

### <a name="method-aotlayer"></a>メソッド AOTLayer

ツリー ノードのレイヤーを返します。

    public UtilEntryLevel AOTLayer()

#### <a name="return-value"></a>戻り値

このノードが存在するレイヤー。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。

### <a name="method-aotlayers"></a>メソッド AOTLayers

そのツリー ノードで定義されているレイヤーのコレクションを返します。

    public Set AOTLayers([boolean old])

#### <a name="parameters"></a>パラメーター

old  
古いモデル ストアからツリー ノード定義のレイヤーを返すかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

レイヤーを持つセット オブジェクト。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。

### <a name="method-aotname"></a>メソッド AOTname

ノードの name プロパティの値を返します。

    public str AOTname()

#### <a name="return-value"></a>戻り値

name プロパティの値を含む文字列

#### <a name="remarks"></a>備考

ほとんどの場合、メソッド TreeNodeName と同じ結果が得られます。

#### <a name="examples"></a>例

次の例では、ツリー ノードの最初の子の名前を出力します。

    static void Job(Args _args) 
    { 
        treeNode t = infolog.findNode('\\Reports\\AssetAcquisition\\Designs\\ReportDesign1\\AutoDesignSpecs'); 
        t = t.AOTfirstChild(); 
        print "treeNodeName: " + t.treeNodeName(); 
        print "AOTName:" + t.AOTName(); 
        pause; 
    }

### <a name="method-aotnewwindow"></a>メソッド AOTnewWindow

ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。

    public int AOTnewWindow()

#### <a name="return-value"></a>戻り値

### <a name="method-aotnextsibling"></a>メソッド AOTnextSibling

ツリー ノードと同じレベルにある次のノードを返します。

    public TreeNode AOTnextSibling()

#### <a name="return-value"></a>戻り値

現在のツリー ノードと同じレベルにある次のノード。

### <a name="method-aotobjectnode"></a>メソッド AOTObjectNode

ノードがアプリケーション オブジェクトであるかどうかを示します。

    public boolean AOTObjectNode()

#### <a name="return-value"></a>戻り値

ノードがアプリケーション オブジェクトである場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

フォームまたはレポートは、アプリケーション オブジェクトです。 フォーム、またはその他のサブパートのコントロールはありません。

### <a name="method-aotoverlaybitmapid"></a>メソッド AOToverlayBitmapId

このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。

    public int AOToverlayBitmapId()

#### <a name="return-value"></a>戻り値

このノードに関連付けられた AOT のオーバーレイのリソース ID。

### <a name="method-aotparent"></a>メソッド AOTparent

ツリー ノードの親ノードを返します。

    public TreeNode AOTparent()

#### <a name="return-value"></a>戻り値

ツリー ノードの親ノード。

### <a name="method-aotprevious"></a>メソッド AOTprevious

このツリー ノードの前の兄弟を返します。

    public TreeNode AOTprevious()

#### <a name="return-value"></a>戻り値

同じレベルにある、このツリー ノードの前のツリー ノード。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public boolean SysObsoleteAttribute(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-aottooltip"></a>メソッド AOTtoolTip

そのツリー ノードに関連付けられているツールヒントを返します。

    public str AOTtoolTip()

#### <a name="return-value"></a>戻り値

ツール チップを含む文字列。

### <a name="method-aottostring"></a>メソッド AOTToString

    public str AOTToString()

#### <a name="return-value"></a>戻り値

### <a name="method-aottypestr"></a>メソッド AOTtypeStr

XPO ファイルで使用される要素タイプの文字列の内部コードを返します。

    public str AOTtypeStr()

#### <a name="return-value"></a>戻り値

ツリー ノードのタイプを含む文字列。

### <a name="method-aotutilfiletype"></a>メソッド AOTUtilFileType

TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。 UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。

    public UtilFileType AOTUtilFileType()

#### <a name="return-value"></a>戻り値

ツリー ノードの UtilFileType 列挙値。 可能な値を次の一覧に示します。 UtilFileType::Application は、要素 (フォーム、レポート、クエリ、テーブルなど) が .aod ファイルに保存されていることを意味します。 UtilFileType::ApplicationCodeDocumentation は、要素が .add ファイルに保存されていることを意味します。 UtilFileType::ApplicationHelp は、要素が .ahd ファイルに保存されていることを意味します。 UtilFileType::KernelHelp は、要素が .akh ファイルに保存されていることを意味します。

#### <a name="examples"></a>例

次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。

    static void myJob(Args _args) 
    { 
        treeNode tn; 
        tn = treeNode::findNode("\\Forms"); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\System Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Developer Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
    }

### <a name="method-applobjectid"></a>メソッド applObjectId

該当する場合は、アプリケーション オブジェクト ID を返します。

    public int applObjectId()

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトの ID。

### <a name="method-applobjectlayermask"></a>メソッド applObjectLayerMask

この要素を含むレイヤーを指定するビットを返します。

    public int applObjectLayerMask()

#### <a name="return-value"></a>戻り値

この要素を含むレイヤーを指定するビット。

### <a name="method-applobjectoldlayermask"></a>メソッド applObjectOldLayerMask

ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。

    public int applObjectOldLayerMask()

#### <a name="return-value"></a>戻り値

この要素を含むレイヤーを指定するビット。

### <a name="method-getnodeinlayer"></a>メソッド getNodeInLayer

指定したレイヤーからツリー ノードのバージョンを取得します。

    public TreeNode getNodeInLayer(UtilEntryLevel layer, [boolean old])

#### <a name="parameters"></a>パラメーター

 レイヤー  
古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。

<!-- -->

old  
古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。

#### <a name="return-value"></a>戻り値

新しい TreeNode。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。 このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isGetNodeInLayerSupported メソッドを使用します。

### <a name="method-hashkey"></a>メソッド hashKey

    public Int64 hashKey()

#### <a name="return-value"></a>戻り値

### <a name="method-makecopy"></a>メソッド makeCopy

    public TreeNode makeCopy()

#### <a name="return-value"></a>戻り値

### <a name="method-newobjectname"></a>メソッド newObjectName

新しい要素の名前を含む文字列を返します。

    public str newObjectName([str oldName])

#### <a name="parameters"></a>パラメーター

oldName  
ノードの新しい名前 (オプション)。 引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。

#### <a name="return-value"></a>戻り値

新しい要素の名前を含む文字列。

#### <a name="remarks"></a>備考

引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。 たとえば、TreeNode に子としてフォームがある場合、引数なしのこのメソッドの呼び出しは「Form1」を返します。 ツリー ノードに複数の子ノードがある場合は、メソッドは "object" という文字列を返します。

#### <a name="examples"></a>例

次の Treenode.newObjectName の呼び出しでは、データ ディクショナリ ノードに複数のオブジェクト型を表す子があるため、「object」が返されます。

    { 
        TreeNode t; 
        str s; 
        t = TreeNode::findNode("\Data dictionary"); 
        s = t.newObjectName(); 
        print s; 
        pause; 
    }

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

### <a name="method-treenodename"></a>メソッド treeNodeName

ツリー ノードの名前を返します。

    public str treeNodeName()

#### <a name="return-value"></a>戻り値

ツリー ノードの名前を含む文字列。

### <a name="method-treenodepath"></a>メソッド treeNodePath

アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。

    public str treeNodePath()

#### <a name="return-value"></a>戻り値

AOT 内のツリー ノードの一意のパスを返します。

#### <a name="examples"></a>例

次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。

    static void myJob(Args _args) 
    { 
        treeNode tn; 
        tn = treeNode::findNode("\\Forms"); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\System Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Developer Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
    }

### <a name="method-treenodetype"></a>メソッド treeNodeType

ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。

    public TreeNodeType treeNodeType()

#### <a name="return-value"></a>戻り値

TreeNodeType クラスのインスタンス。

### <a name="method-updatenodepermissions"></a>メソッド updateNodePermissions

    public int updateNodePermissions(boolean throwExceptions)

#### <a name="parameters"></a>パラメーター

throwExceptions  

#### <a name="return-value"></a>戻り値

### <a name="method-utilelement"></a>メソッド utilElement

ノードに関連する UtilElements レコードを返します。

    public UtilElements utilElement()

#### <a name="return-value"></a>戻り値

ノードに関連する UtilElements レコード。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。

### <a name="method-utilidelement"></a>メソッド utilIdElement

ノードに関連する UtilIdElements レコードを返します。

    public UtilIdElements utilIdElement()

#### <a name="return-value"></a>戻り値

ノードに関連する UtilIdElements レコード。

#### <a name="remarks"></a>備考

メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。

### <a name="method-validatenamecharacters"></a>メソッド validateNameCharacters

    public boolean validateNameCharacters(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-findnode"></a>メソッド findNode

アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。

    public static TreeNode findNode(str path)

#### <a name="parameters"></a>パラメーター

path  
検索で使用されるパスを示す文字列。

#### <a name="return-value"></a>戻り値

指定されたパスのノードが存在しない場合の、要求された TreeNode オブジェクトまたは nullNothingnullptrunita null 参照 (Visual Basic ではなし)。

#### <a name="remarks"></a>備考

TreeNode オブジェクトを取得する別の方法は、Info.getNode メソッドを使用することです。 2 つのメソッド間の重要な違いは、Info.getNode メソッドが AOT から分離されているノードを提供するのに対して一方 findNode メソッドは AOT のノードを返します。 つまり、Info.getNode メソッドから返されるノードは親ノードを持たず、findNode メソッドから返されるノードは親ノードを持ちます。

#### <a name="examples"></a>例

次の例では、TreeNode::findNode メソッドが呼び出される時に検出される ツリー ノードの名前を取得します。 この例では、TreeNode.findNode メソッドを呼び出す前に、ユーザーに必要なセキュリティ キーがあるかどうかを確認します。

    server static public void Main(Args _args) 
    { 
        TreeNode tn; 
        str name; 
        tn = TreeNode::findNode(@"\Classes"); 
        if (tn) 
        { 
            name = tn.treeNodeName(); 
        } 
    }

### <a name="method-generateobjectname"></a>メソッド generateObjectName

    public static str generateObjectName(str template)

#### <a name="parameters"></a>パラメーター

テンプレート  

#### <a name="return-value"></a>戻り値

### <a name="method-getmaximumnodenamelength"></a>メソッド getMaximumNodeNameLength

    public static int getMaximumNodeNameLength(int modelElementTypeId)

#### <a name="parameters"></a>パラメーター

modelElementTypeId  

#### <a name="return-value"></a>戻り値

### <a name="method-isnodereferencevalid"></a>メソッド isNodeReferenceValid

    public static boolean isNodeReferenceValid(TreeNode treeNode)

#### <a name="parameters"></a>パラメーター

treeNode  

#### <a name="return-value"></a>戻り値

### <a name="method-isvalidobjectname"></a>メソッド isValidObjectName

引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。

    public static boolean isValidObjectName(str name)

#### <a name="parameters"></a>パラメーター

名前  
検証するツリー ノードの名前を含む文字列。

#### <a name="return-value"></a>戻り値

各条件が一致している場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

候補者の名前は、次の条件を満たす必要があります:

-   最初の文字は数字、記号ではない文字でなければなりません。
-   文字、数字、またはアンダースコアだけを含めることができます。
-   トークンに対して評価してはなりません。

このメソッドは、同じ名前の要素がすでに存在するかどうかをチェックしません。 これは引数が AOT オブジェクトの有効な名前であることのみを検証します。 重複する名前は、クラス、テーブル、拡張データ型または列挙内では存在しません。

#### <a name="examples"></a>例

次の例では、有効な引数と無効な引数の例を示しています。

    boolean validName; 
    validName = TreeNode::isValidObjectName('ValidName'); //true 
    validName = TreeNode::isValidObjectName('Name with spaces'); //false 
    validName = TreeNode::isValidObjectName('4StartsWithDigit'); //false 
    validName = TreeNode::isValidObjectName('Illegal;Character'); //false 
    validName = TreeNode::isValidObjectName('if'); // false (token name)

### <a name="method-rootnode"></a>メソッド rootNode

AOT のルート ノードを返します。

    public static TreeNode rootNode()

#### <a name="return-value"></a>戻り値

AOT のルート ノード。

#### <a name="remarks"></a>備考

このメソッドは、同様の機能を rootNode メソッドに提供します。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute()

### <a name="method-treenoderelease"></a>メソッド treeNodeRelease

ツリー ノードが明示的に解放されます。

    public void treeNodeRelease()

#### <a name="remarks"></a>備考

ガベージコレクターが自動的にオブジェクトをアンロードするので、通常、オブジェクトを明示的にアンロードする必要はありません。 ただし、ツリー ノードは、通常 AOT にリンクされているため、ガベージ コレクションではありません。 同じ方法で多くのツリー ノードでこのメソッドを実行する場合、リソースを要求する可能性があります。 ガベージ コレクターがツリー ノードを削除できるようにするには、作業中にツリー ノードをアンロードする必要があります。 このメソッドを呼び出す前に、そのツリー ノードとそのサブノードに対するすべての参照を削除してください。 このメソッドを呼び出す必要があるかどうかを判断するには、TreeNode.TreeNodeType().isConsumingMemory メソッドを使用します。

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, [XRefReference xrefRef], [ClassId parentTypeId])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

xrefKind  

<!-- -->

lineNumber  

<!-- -->

columNumber  

<!-- -->

xrefRef  

<!-- -->

parentTypeId  

### <a name="method-aotrun"></a>メソッド AOTrun

アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。

    public void AOTrun()

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute()

### <a name="method-aotrefresh"></a>メソッド AOTrefresh

.aod ファイルを最新版に変更することによりノードを更新します。

    public void AOTrefresh()

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(Struct struct1)

#### <a name="parameters"></a>パラメーター

struct1  

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(str properties)

#### <a name="parameters"></a>パラメーター

プロパティ  

### <a name="method-aotconfigure"></a>メソッド AOTconfigure

    public void AOTconfigure()

### <a name="method-aotload"></a>メソッド AOTload

オブジェクトが読み込み済みであるか確認します。

    public void AOTload()

### <a name="method-treenodeexport"></a>メソッド treeNodeExport

アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。

    public void treeNodeExport(str filename, [int flag])

#### <a name="parameters"></a>パラメーター

filename  

<!-- -->

flag  

#### <a name="remarks"></a>備考

攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。

#### <a name="examples"></a>例

この例では、treeNodeExport メソッドを使用して、ExampleClass クラスを .xpo ファイルにエクスポートします。

    void TreeNodeExample() 
    { 
        TreeNode treeNode; 
        TreeNode childNode; 
        FileIoPermission perm; 
        #define.ExportFile(@"c:\TreeNodeExportExampleClass.xpo") 
        #define.ExportMode("w") 
        perm = new FileIoPermission(#ExportFile, #ExportMode); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        treeNode = TreeNode::findNode(@"\Classes"); 
        if (treeNode != null) 
        { 
            childNode = treeNode.AOTfindChild(@"ExampleClass"); 
            // BP deviation documented. 
            childNode.treeNodeExport(#ExportFile); 
        } 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  

<!-- -->

isStatic  

### <a name="method-aotendxref"></a>メソッド AOTendXref

    public void AOTendXref()

### <a name="method-aotmessageline"></a>メソッド AOTmessageLine

アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。

    public void AOTmessageLine(str text, int linenumber)

#### <a name="parameters"></a>パラメーター

テキスト  
無視される整数。 出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。

<!-- -->

linenumber  
無視される整数。 出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。

#### <a name="remarks"></a>備考

このメソッドは、テキストを出力するために使用されます。そのためユーザーは後でメッセージ ウィンドウ内のそのテキスト行をダブルクリックすると、このノードに関して何らかのアクションが発生します。

#### <a name="examples"></a>例

次の例では、フォームが TreeNode からこのメソッドを継承するために、フォーム オブジェクトに対して AOTmessageLine メソッドを実行します。

    static void JobAOTmessageLineDemo(Args _args) 
    { 
        Form f = new Form('testAOTMessageLine'); 
        // 
        f.AOTmessageLine('test message 1a',1); 
        f.AOTmessageLine('test message 2a',2); 
        f.AOTmessageLine('test message 3a',3); 
        f.AOTmessageLine('test message 1b',1); 
        f.AOTmessageLine('test message 2b',2); 
        f.AOTmessageLine('test message 3b',3); 
        f.AOTmessageLine('test message 2c',2); 
        // 
        /******* 
        Actual Output in the Message window 
        (the 7 identical lines): 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        *******/ 
    }

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(str name, AnyType value)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

値  

### <a name="method-aotrestore"></a>メソッド AOTrestore

該当する場合は、ディスクからこのノードを再読み込みします。

    public void AOTrestore([boolean forceReload])

#### <a name="parameters"></a>パラメーター

forceReload  

### <a name="method-aotregenerate"></a>メソッド AOTregenerate

    public void AOTregenerate()

### <a name="method-aotmakexref"></a>メソッド AOTmakeXref

このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。

    public void AOTmakeXref([int flag], [boolean xRefAll])

#### <a name="parameters"></a>パラメーター

flag  

<!-- -->

xRefAll  

#### <a name="remarks"></a>備考

このメソッドは、任意の場所で呼び出すことができます。

-   リスト ノード (AOT、テーブル、フォーム、プロジェクトのルート、およびグループ)
-   アプリケーション オブジェクト (テーブルやフォームなど)
-   メソッドの分岐
-   メソッド

### <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a>パラメーター

明細行  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

#### <a name="remarks"></a>備考

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。

#### <a name="examples"></a>例

次のコード例は、X++ エディターを開き、クラス Tax のクラス宣言を表示し、ポインタを 6 行目、8 列目に配置します。

    #AOT 
    static void myJobAOTEdit(Args _args) 
    { 
        treeNode treeNode; 
        treeNode = TreeNode::findNode(#ClassesPath + '\\' + classStr(Tax)+ '\\ClassDeclaration'); 
        if (treeNode) 
        { 
            treeNode.AOTedit(6,8); 
        } 
        else 
        { 
            print "Could not find treeNode"; 
        } 
        pause; 
    }

### <a name="method-aotshowproperties"></a>メソッド AOTshowProperties

プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。

    public void AOTshowProperties()

### <a name="method-aotinsert"></a>メソッド AOTinsert

このノードのサブノード間にノードを挿入します。

    public void AOTinsert(TreeNode parent, [TreeNode after], [boolean doNotDuplicate])

#### <a name="parameters"></a>パラメーター

parent  

<!-- -->

以後  

<!-- -->

doNotDuplicate  

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-aotmove"></a>メソッド AOTMove

    public void AOTMove(TreeNode parent, [TreeNode after])

#### <a name="parameters"></a>パラメーター

parent  

<!-- -->

以後  

### <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

    public void SysObsoleteAttribute(int modelId)

#### <a name="parameters"></a>パラメーター

modelId  

## <a name="class-treenodeiterator"></a>クラス TreeNodeIterator
    class TreeNodeIterator extends Object

TreeNodeIterator クラスは、ツリー ノードの子ノード上を移動します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

次の例では、ルート ノードのすべての子ノードの名前を出力します。

    static void example()  
    { 
        treeNode myTreeNode; 
        xInfo xi = new xInfo(); 
        void printChildNames (treeNode t) 
        { 
            treeNode child; 
            treenodeIterator it; 
            it = t.AOTiterator(); 
            child = it.next(); 
            while (child) 
            { 
                print child.treeNodeName(); 
                child = it.next(); 
            } 
        } 
        myTreeNode = xi.rootNode(); 
        printChildNames(myTreeNode); 
        pause; 
    }

### <a name="methods"></a>メソッド

| 方法                 | 説明                                                                                            |
|------------------------|--------------------------------------------------------------------------------------------------------|
| public TreeNode next() | 子ノードの一覧の次の要素を取得します。                                                 |
| public void reset()    | 次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。 |

### <a name="method-next"></a>メソッド next

子ノードの一覧の次の要素を取得します。

    public TreeNode next()

#### <a name="return-value"></a>戻り値

ツリー内の次の子ノード。

### <a name="method-reset"></a>メソッド reset

次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。

    public void reset()

## <a name="class-treenodetype"></a>クラス TreeNodeType
    class TreeNodeType extends Object

TreeNodeType クラスは、TreeNode クラスのタイプに関する情報を取得します。

### <a name="remarks"></a>備考

このクラスを使用すると、TreeNode クラスのインスタンスを反映させることができます。 リフレクション情報は、TreeNode クラスのインスタンスに固有ではありません。 同じ NodeType を持つすべての TreeNode インスタンスは、同じ TreeNodeType を共有します。 TreeNode.TreeNodeType メソッドは、リフレクション情報を含む treeNodeType オブジェクトを返します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                     | 説明                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| public int id()                            | タイプの ID を返します。                                                                                 |
| public boolean isConsumingMemory()         | このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。 |
| public boolean isGetNodeInLayerSupported() | このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。              |
| public boolean isLayerAware()              | このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。                    |
| public boolean isModelElement()            | このノード タイプのインスタンスがモデル要素かどうかを示します。                                      |
| public boolean isRootElement()             | このノード タイプのインスタンスがルート要素かどうかを示します。                                       |
| public boolean isUtilElement()             | このノード タイプのインスタンスがユーティリティ要素かどうかを示します。                                       |
| public boolean isVCSControllableElement()  |                                                                                                        |
| private void new()                         | TreeNodeType クラスの新しいインスタンスを初期化します。                                                  |

### <a name="method-id"></a>メソッド id

タイプの ID を返します。

    public int id()

#### <a name="return-value"></a>戻り値

TreeNodeType の ID。

### <a name="method-isconsumingmemory"></a>メソッド isConsumingMemory

このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。

    public boolean isConsumingMemory()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードがメモリを消費する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このタイプの TreeNode インスタンスで作業した後は、TreeNode.TreeNodeRelease メソッドを呼び出して、消費されたメモリを解放することが重要です。 これを行わないと、メモリ不足の例外が発生します。 構成階層における TreeNode クラスの全てのインスタンスがガベージ コレクションになる前に、TreeNode.TreeNodeRelease メソッドを呼び出さないでください。 たとえば、MyClass.myMethod の TreeNode がまだある場合、MyClass で TreeNode.TreeNodeRelease() メソッドを呼び出さないでください。

### <a name="method-isgetnodeinlayersupported"></a>メソッド isGetNodeInLayerSupported

このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。

    public boolean isGetNodeInLayerSupported()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードが TreeNode.GetNodeInLayer メソッドをサポートする場合は true。それ以外の場合は、false。

### <a name="method-islayeraware"></a>メソッド isLayerAware

このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。

    public boolean isLayerAware()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードがレイヤーで修飾された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このタイプのツリー ノードは、AOTLayer メソッドと AOTLayers メソッドをサポートします。

### <a name="method-ismodelelement"></a>メソッド isModelElement

このノード タイプのインスタンスがモデル要素かどうかを示します。

    public boolean isModelElement()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードがモデル要素である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

モデル要素は、モデル ストアに保持される (または保持できる) ツリー ノードです。 各モデル要素ツリー ノードについては、1 つのレコードはモデル ストアの ModelElements テーブル内に表示されます。 モデル要素は、AOT 内で含まれているモデルの名前で視覚的に修飾されます。

### <a name="method-isrootelement"></a>メソッド isRootElement

このノード タイプのインスタンスがルート要素かどうかを示します。

    public boolean isRootElement()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードがルート要素である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

ルート要素は、ツリー ノードの構成階層のルートです。 ルート要素は、モデル要素の親を持つことはありません。 例には、MyTable、MyClass、MyForm が含まれます。

### <a name="method-isutilelement"></a>メソッド isUtilElement

このノード タイプのインスタンスがユーティリティ要素かどうかを示します。

    public boolean isUtilElement()

#### <a name="return-value"></a>戻り値

このタイプのツリー ノードがユーティリティ要素である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

ユーティリティ要素は UtilElements と UtilIdElements ビューからアクセスできるツリー ノードです。 Util 要素はモデル要素のサブセットです。

### <a name="method-isvcscontrollableelement"></a>メソッド isVCSControllableElement

    public boolean isVCSControllableElement()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

TreeNodeType クラスの新しいインスタンスを初期化します。

    private void new()



