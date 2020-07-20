---
title: TextIo クラス
description: このトピックでは、TextIo クラスについて説明します。
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
ms.openlocfilehash: 3fb555eb5629b90a4eec4f8af5a0451720f2abd9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502789"
---
# <a name="class-textio"></a>クラス TextIo

[!include [banner](../../includes/banner.md)]

```xpp
class TextIo extends CommaIo
```

TextIo クラスには、テキスト ファイルの読み取りと書き込みを行う機能があります。

## <a name="remarks"></a>備考

TextIO は、非 ANSI コード ページ ファイル I/O のサポートを提供する AsciiIO を置き換えます。 TextIO コンストラクターには、ファイルのコード ページを設定するための追加のオプション パラメーターがあります。 TextIO.new メソッドには、ファイルのコード ページを指定するオプション引数があります。 既定値は UTF-16LE (Microsoft Windows ネイティブ Unicode 表現) です。 ほとんどの場合、特にエンドユーザーが Finance and Operations アプリケーション以外のテキスト エディターでファイルを編集する可能性がある場合に、これを使用することをお勧めします。 詳細については、「TextIo.new」を参照してください。 ファイルが読み取られると、TextIO はファイルの最初の数バイトについてバイト順マーク (BOM) を調べて、UTF-8、UTF-16LE、および UTF-16BE を自動的に取り扱います。 BOM が見つからない場合、ファイルは ANSI コード ページ (ACP) 形式であると見なされます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a>パラメーター - inFieldDelimiter

値  
フィールドの区切り記号として使用される文字 (オプション)。

### <a name="return-value---infielddelimiter"></a>戻り値 - inFieldDelimiter

フィールドの区切り記号として使用される文字。

### <a name="remarks---infielddelimiter"></a>備考 - inFieldDelimiter

出力ファイルのフィールド区切り記号を設定するには、次を使用します。

### <a name="examples---infielddelimiter"></a>例 - inFieldDelimiter

次の例では、入力ファイルのフィールド区切り記号を '\\r\\n' に設定します.

```xpp
protected void openFile() 
{ 
    #define.delimiter('\r\n') 
    super(); 
    importFile.inFieldDelimiter(#delimiter); 
}
```

## <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a>パラメーター - inRecordDelimiter

値  
オプションでレコードの区切り記号として使用される文字。

### <a name="return-value---inrecorddelimiter"></a>戻り値 - inRecordDelimiter

レコードの区切り記号として使用される文字。

### <a name="remarks---inrecorddelimiter"></a>備考 - inRecordDelimiter

出力ファイルのレコード区切り記号を設定するには、次を使用します。

### <a name="examples---inrecorddelimiter"></a>例 - inRecordDelimiter

次の例では、レコード区切り記号を 128 に設定します。

```xpp
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
```

## <a name="method-inrecordlength"></a>メソッド inRecordLength

入力ファイルのレコードの長さを取得または設定します。

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a>パラメーター - inRecordLength

値  
入力ファイルのレコードの長さ (オプション)。

### <a name="return-value---inrecordlength"></a>戻り値 - inRecordLength

入力ファイルのレコードの長さ。

### <a name="remarks---inrecordlength"></a>備考 - inRecordLength

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを確認します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

### <a name="examples---inrecordlength"></a>例 - inRecordLength

次の例では、レコードの長さを 128 に設定します。

```xpp
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
```

## <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a>パラメーター - outFieldDelimiter

値  
フィールドの区切り記号として使用される文字 (オプション)。

### <a name="return-value---outfielddelimiter"></a>戻り値 - outFieldDelimiter

フィールドの区切り記号として使用される文字。

### <a name="remarks---outfielddelimiter"></a>備考 - outFieldDelimiter

入力ファイルのフィールド区切り記号を設定するには、次を使用します。

### <a name="examples---outfielddelimiter"></a>例 - outFieldDelimiter

次の例では、出力ファイルのフィールド区切り記号を ' ' (なし) に設定します。

```xpp
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
```

## <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a>パラメーター - outRecordDelimiter

値  
オプションでレコードの区切り記号として使用される文字。

### <a name="return-value---outrecorddelimiter"></a>戻り値 - outRecordDelimiter

レコードの区切り記号として使用される文字。

### <a name="remarks---outrecorddelimiter"></a>備考 - outRecordDelimiter

入力ファイルのレコード区切り記号を設定するには、次を使用します。

### <a name="examples---outrecorddelimiter"></a>例 - outFieldDelimiter

次の例では、出力ファイルのレコード区切り記号を '\\r\\n'' に設定します。

```xpp
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
```

## <a name="method-read"></a>メソッド read

TextIO オブジェクトから次の完全なレコードを読み取ります。

```xpp
public container read()
```

### <a name="return-value---read"></a>戻り値 - read

1 つのレコードを保持するコンテナーです。

### <a name="remarks---read"></a>備考 - read

コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。 これらのプロパティには、最も一般的な形式の入力と出力を可能にする既定値があります。 inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッドを使用して、プロパティを調整する必要がある場合があります。

### <a name="examples---read"></a>例 - read

次の例では、ファイルからレコードを読み取り、conpeek 関数を使用してレコードから値を抽出します。

```xpp
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
```

## <a name="method-status"></a>メソッド status

TextIo オブジェクトで実行された最後の操作のステータスを取得します。

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a>戻り値 - status

最後の操作の状態。

### <a name="examples---status"></a>例 - status

次の例では、ファイルが存在しない場合、またはファイルの最後の操作が、IO\_Status::Ok 列挙値のステータスを持たない場合にエラーをスローします。

```xpp
protected void checkDiskFileStatus() 
{ 
    if (!diskFile || diskFile.status() != IO_Status::Ok) 
    { 
        throw error(strfmt("@SYS76826", diskFileName)); 
    } 
}
```

## <a name="method-write"></a>メソッド write

TextIO オブジェクトによって表されるファイルにデータを記述します。

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a>パラメーター - write

値  
ファイルに書き込む値。 値はさまざまなデータ型にすることができます。

### <a name="return-value---write"></a>戻り値 - write

書き込み操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---write"></a>備考 - write

書き込み操作が失敗した場合は、その原因を突き止めるために使用できます。 書き込みメソッドは、可変数の引数を受け入れます。 各値は、フィールドとして出力レコードに配置されます。 フィールドは、で指定されたフィールド区切り記号で区切られます。 各レコードは、によって指定された区切り記号で区切られます。 完全なコンテナーを書き込むには、次を使用します。

## <a name="method-writechar"></a>メソッド writeChar

Unicode 文字をファイルに記述します。

```xpp
public boolean writeChar(int int)
```

### <a name="parameters---writechar"></a>パラメーター - writeChar

int  

### <a name="return-value---writechar"></a>戻り値 - writeChar

書き込み操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---writechar"></a>備考 - writeChar

書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。 複数の値を書き込んだり、さまざまな種類のデータをファイルに書き込むには、TextIO.write メソッドを使用します。

## <a name="method-writeexp"></a>メソッド writeExp

TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a>パラメーター - writeExp

データ  
ファイルへの書き込みのデータを持つコンテナーです。

### <a name="return-value---writeexp"></a>戻り値 - writeExp

書き込み操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---writeexp"></a>備考 - writeExp

書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。 コンテナー内のエントリは、outFieldDelimiter メソッドで設定された区切り文字で区切られます。 コンテナーは、outRecordDelimiter メソッドで設定された区切り文字で区切られます。

## <a name="method-writeraw"></a>メソッド writeRaw

予約済み。

```xpp
public boolean writeRaw(str data)
```

### <a name="parameters---writeraw"></a>パラメーター - writeRaw

データ  

### <a name="return-value---writeraw"></a>戻り値 - writeRaw

## <a name="method-new"></a>メソッド new

TextIO クラスの新しいインスタンスを作成します。

```xpp
public void new(str filename, str mode, [int codepage])
```

### <a name="parameters---new"></a>パラメーター - new

filename  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

<!-- -->

モード  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

<!-- -->

codepage  
ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。 既定値は 1200 (UTF-16LE) です。 このパラメーターはオプションです。 以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。 無効なコード ページが要求された場合にエラーが報告されます。 コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。 たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。

### <a name="remarks---new"></a>備考 - new

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
<td>ユーザー&#39;の現在の言語の文字のみをサポートするコード ページ。 コード ページは、多言語データを含む可能性のあるものや、異なるコード ページを使用して 2 つのシステム間で転送される単一言語データ用には適していません。</td>
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

### <a name="examples---new"></a>例 - new

次の例では、コード ページ 850 エンコードを使用して、読み取りモードで filename という名前のファイルにアクセスする TextIO オブジェクトを作成します。

```xpp
protected void openFile(str _fileOpen = #io_read) 
{ 
    importFile = new TextIo(filename, _fileOpen, 850); 
    if (! importFile) 
    { 
        throw error(strfmt("@SYS18678", filename)); 
    } 
}
```

## <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a>備考 - finalize

通常、TextIO オブジェクトは、スコープを離れることによって確定されます。 確定メソッドは、通常は直接呼び出されません。 TextIO オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。

