---
title: AsciiIo クラス
description: このトピックでは、AsciiIo クラスについて説明します。
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
ms.openlocfilehash: 94dc3749f1ad3029946ee763c7f7f47f7e946be0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502746"
---
# <a name="class-asciiio"></a>クラス AsciiIo

[!include [banner](../../includes/banner.md)]

```xpp
class AsciiIo extends CommaIo
```

AsciiIo クラスには、ASCII ファイルの読み取りと書き込みを行う機能があります。

## <a name="remarks"></a>備考

TextIo クラスには、さまざまなコード ページを使用するファイルの読み取りと書き込みを行う機能があります。 AsciiIO クラスは、ANSI コード ページ (ACP) 文字のみサポートします。 AsciiIO クラスを使用する既存のコードは、ファイルに ACP 以外の文字が含まれている場合や、.xpo ファイルなどの Finance and Operations アプリケーションでのみ使用されるファイルの場合に TextIO クラスを使用するように変換する必要があります。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                      |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| public str inFieldDelimiter(\[str value\])   | AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。   |
| public str inRecordDelimiter(\[str value\])  | AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。  |
| public int inRecordLength(\[int value\])     | 入力ファイルのレコードの長さを設定または取得します。                                                                           |
| public str outFieldDelimiter(\[str value\])  | AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。  |
| public str outRecordDelimiter(\[str value\]) | AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。 |
| public container read()                      | Io オブジェクトから次の完全なレコードを読み取ります。                                                                                   |
| public IO\_Status status()                   | ファイルでの最後の操作のステータスを返します。                                                                            |
| public boolean write(VarArg values)          | 単純型の値を記述します。                                                                                                  |
| public boolean writeChar(int int)            |                                                                                                                                  |
| public boolean writeExp(container data)      | コンテナのコンテンツをファイルに記述します。                                                                                     |
| public boolean writeRaw(str data)            |                                                                                                                                  |
| public void finalize()                       | ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。                                                                       |
| public void new(str filename, str mode)      | AsciiIo クラスのインスタンスを作成します。                                                                                        |

## <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a>パラメーター - inFieldDelimiter

値  
フィールドの区切り記号として割り当てられる文字。

### <a name="return-value---infielddelimiter"></a>戻り値 - inFieldDelimiter

フィールドの区切り記号として使用される文字。

## <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a>パラメーター - inRecordDelimiter

値  
レコードの区切り記号として割り当てられる文字。

### <a name="return-value---inrecorddelimiter"></a>戻り値 - inRecordDelimiter

レコードの区切り記号として使用される文字。

### <a name="remarks---inrecorddelimiter"></a>備考 - inRecordDelimiter

標準的なテキストについては、区切り記号は改行文字です。

## <a name="method-inrecordlength"></a>メソッド inRecordLength

入力ファイルのレコードの長さを設定または取得します。

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a>パラメーター - inRecordLength

値  
入力ファイルのレコード長として割り当てる値。

### <a name="return-value---inrecordlength"></a>戻り値 - inRecordLength

入力ファイルのレコードの長さ。

### <a name="remarks---inrecordlength"></a>備考 - inRecordLength

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合 (つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、それ以上のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さのチェックを無効にするには、inRecordDelimiter プロパティ値を 0 (ゼロ) に設定します。

## <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a>パラメーター - outFieldDelimiter

値  
フィールドの区切り記号として割り当てられる文字。

### <a name="return-value---outfielddelimiter"></a>戻り値 - outFieldDelimiter

フィールドの区切り記号として使用される文字。

## <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a>パラメーター - outRecordDelimiter

値  
レコードの区切り記号として割り当てられる文字。

### <a name="return-value---outrecorddelimiter"></a>戻り値 - outRecordDelimiter

レコードの区切り記号として使用される文字。

### <a name="remarks---outrecorddelimiter"></a>備考 - outRecordDelimiter

標準的なテキスト ファイルについては、区切り記号は改行文字です。

## <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

```xpp
public container read()
```

### <a name="return-value---read"></a>戻り値 - read

Io オブジェクトからの次の完全なレコード。

### <a name="remarks---read"></a>備考 - read

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength によって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドを表します。 それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定があります。 これらの設定では、最も一般的な形式の入力と出力が可能です。 ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

## <a name="method-status"></a>メソッド status

ファイルでの最後の操作のステータスを返します。

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a>戻り値 - status

最後のファイル操作の状態。

## <a name="method-write"></a>メソッド write

単純型の値を記述します。

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a>パラメーター - write

値  
1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。 単純型は、文字列、整数、実数、列挙型、日付です。

### <a name="return-value---write"></a>戻り値 - write

書き込み操作が成功する場合は true。それ以外の場合は、false。 書き込み操作が失敗すると、ステータスをチェックし、原因について確認できます。

### <a name="remarks---write"></a>備考 - write

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます: 最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。 フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

## <a name="method-writechar"></a>メソッド writeChar

```xpp
public boolean writeChar(int int)
```

### <a name="parameters---writechar"></a>パラメーター - writeChar

int  

### <a name="return-value---writechar"></a>戻り値 - writeChar

## <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a>パラメーター - writeExp

データ  
レコードのデータを保持するコンテナー。

### <a name="return-value---writeexp"></a>戻り値 - writeExp

操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし原因について確認します。

### <a name="remarks---writeexp"></a>備考 - writeExp

コンテナー内のエントリはフィールドとして扱われます。 コンテナーは、完全なレコードとして扱われます。 フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。

## <a name="method-writeraw"></a>メソッド writeRaw

```xpp
public boolean writeRaw(str data)
```

### <a name="parameters---writeraw"></a>パラメーター - writeRaw

データ  

### <a name="return-value---writeraw"></a>戻り値 - writeRaw

## <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a>備考 - finalize

AsciiIo オブジェクトは通常そのスコープの終了後に確定されます。 このメソッドは、通常は直接呼び出されません。 AsciiIo オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。

## <a name="method-new"></a>メソッド new

AsciiIo クラスのインスタンスを作成します。

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a>パラメーター - new

filename  
AsciiIo クラスのこのインスタンスを作成するために使用するモード。

<!-- -->

モード  
AsciiIo クラスのこのインスタンスを作成するために使用するモード。

### <a name="remarks---new"></a>備考 - new

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---new"></a>例 - new

次の例では、AsciiIo クラスを使用してテキスト ファイルから読み込みます。

```xpp
void AsciiIoExample() 
{ 
    AsciiIo asciiIo; 
    container con; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("r") 
```

```xpp
    // The AsciiIo.new method runs under code access permission. 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Code access permission scope starts here. 
     perm.assert(); 
```

```xpp
     asciiIo = new AsciiIo(#ExampleFile, #ExampleOpenMode); 
    if (asciiIo != null) 
    { 
          con = asciiIo.read(); 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

