---
title: CommaIo クラス
description: このトピックでは、CommaIo クラスについて説明します。
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
ms.openlocfilehash: 0b06da10de9d8e11e70e69b209ff5aa85b514f46
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502710"
---
# <a name="class-commaio"></a>クラス CommaIo

[!include [banner](../../includes/banner.md)]

```xpp
class CommaIo extends Io
```

CommaIo クラスには、コンマ区切りファイルの読み取りと書き込みを行う機能があります。

## <a name="remarks"></a>備考

このクラスは、CommaTextIo クラスに置き換えられました。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| public int filePosition()                    |                                                                                                                              |
| public str inFieldDelimiter(\[str value\])   | \*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。                                    |
| public str inRecordDelimiter(\[str value\])  | 完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。  |
| public int inRecordLength(\[int value\])     | ファイル内の各レコードを読み取る文字数を取得または設定します。                                                     |
| public str outFieldDelimiter(\[str value\])  | レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。          |
| public str outRecordDelimiter(\[str value\]) | 出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。 |
| public container read()                      | Io オブジェクトから次の完全なレコードを読み取ります。                                                                               |
| public IO\_Status status()                   | Io オブジェクトで実行された最後の操作のステータスを取得します。                                              |
| public boolean write(VarArg values)          | 単純型の値を記述します。                                                                                              |
| public boolean writeExp(container data)      | コンテナのコンテンツをファイルに記述します。                                                                                 |
| public void new(str filename, str mode)      | CommaIo クラスの新しいオブジェクトを作成します。                                                                                   |
| public void finalize()                       | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。                                                  |

## <a name="method-fileposition"></a>メソッド filePosition

```xpp
public int filePosition()
```

### <a name="return-value---fileposition"></a>戻り値 - filePosition

## <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a>パラメーター - inFieldDelimiter

値  

### <a name="return-value---infielddelimiter"></a>戻り値 - inFieldDelimiter

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。

## <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a>パラメーター - inRecordDelimiter

値  

### <a name="return-value---inrecorddelimiter"></a>戻り値 - inRecordDelimiter

完全なレコードが読み込まれたかどうかを示す文字。

### <a name="remarks---inrecorddelimiter"></a>備考 - inRecordDelimiter

標準的なテキストについては、区切り記号は改行文字です。

## <a name="method-inrecordlength"></a>メソッド inRecordLength

ファイル内の各レコードを読み取る文字数を取得または設定します。

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a>パラメーター - inRecordLength

値  

### <a name="return-value---inrecordlength"></a>戻り値 - inRecordLength

ファイル内の各レコードを読み取る文字数。

### <a name="remarks---inrecordlength"></a>備考 - inRecordLength

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

## <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a>パラメーター - outFieldDelimiter

値  

### <a name="return-value---outfielddelimiter"></a>戻り値 - outFieldDelimiter

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。

## <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a>パラメーター - outRecordDelimiter

値  

### <a name="return-value---outrecorddelimiter"></a>戻り値 - outRecordDelimiter

出力ファイルに書き込まれる文字のシーケンス。

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

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 それぞれの特殊な Io クラスでは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定を使用し、最も一般的な形式の入出力を有効にします。 ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

## <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a>戻り値 - status

最後の操作の状態。システム列挙形式。

### <a name="remarks---status"></a>備考 - status

戻り値は、IO\_ステータス システムの列挙によって表されます。 可能性のある IO\_Status 値の範囲はクラスによって異なります。

### <a name="examples---status"></a>例 - status

この例は、状態メソッドを使用する方法を示しています。 ただし、この例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。

```xpp
{ 
    // Create an Io object and perform some operations. 
    if (myIo.status() == IO_Status::OK) 
    { 
        // Go ahead - the last operation was successful. 
    } 
}
```

## <a name="method-write"></a>メソッド write

単純型の値を記述します。

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a>パラメーター - write

値  
1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。 単純型は、文字列、整数、実数、列挙型、日付です。

### <a name="return-value---write"></a>戻り値 - write

書き込み操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし障害について確認できます。

### <a name="remarks---write"></a>備考 - write

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初の引数は最初のフィールドになり、2 番目の引数は 2 番目のフィールドなどになります。 フィールドは、outFieldDelimiter メソッドで指定されるフィールド区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

## <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a>パラメーター - writeExp

データ  
レコードのデータを保持するコンテナー。

### <a name="return-value---writeexp"></a>戻り値 - writeExp

操作が成功する場合は true。それ以外の場合は、false。 工程が失敗すると、ステータスをチェックし障害について確認できます。

### <a name="remarks---writeexp"></a>備考 - writeExp

コンテナー内のエントリはフィールドとして扱われます。 コンテナー自体は、完全なレコードとして扱われます。 フィールドは、outFieldDelimiter メソッドを使用して指定される区切り記号で区切られます。 レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。

### <a name="examples---writeexp"></a>例 - writeExp

この例では、CommaIO オブジェクトを使用してサンプル ファイルから読み取ります。

```xpp
{ 
    container c; 
    CommaIo myfile; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\myfile.txt") 
    #define.ExampleOpenMode("w") 
```

```xpp
    // Set code access permission to help protect the use 
    // of CommaIO.new 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    perm.assert(); 
```

```xpp
    myfile = new CommaIo(#ExampleFile, #ExampleOpenMode); 
```

```xpp
    // Assign the entries in the container according to record layout. 
    c = [1,"MyText",1.324,"Last field"]; 
    // Write this record according to file format  
    // (record/field delimiters). 
    myfile.writeExp(c); 
```

```xpp
    // Close the code access permission. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-new"></a>メソッド new

CommaIo クラスの新しいオブジェクトを作成します。

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a>パラメーター - new

filename  
ファイルを開く必要があるモード。 次のようにモードを指定します。

<!-- -->

モード  
ファイルを開く必要があるモード。 次のようにモードを指定します。

### <a name="remarks---new"></a>備考 - new

ランタイム エラーは、現在のモードに対応していないメソッドを使用してファイルにアクセスした場合に発生します。 たとえば、ユーザーが読み取りモードで開いているファイルへの書き込みしようとすると、エラーが発生します。 攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---new"></a>例 - new

次の例では、CommaIO オブジェクトを使用して ExampleFile ファイルから読み取ります。

```xpp
{ 
    CommaIo         io; 
    container       con; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("r") 
```

```xpp
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    if (perm == null) 
    { 
        return; 
    } 
    // Grants permission to execute the CommaIo.new method. 
    // CommaIo.new runs under code access security. 
    perm.assert(); 
```

```xpp
    io = new CommaIo(#ExampleFile, #ExampleOpenMode); 
    if (io != null) 
    { 
        con = io.read(); 
    } 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a>備考 - finalize

このメソッドは通常は直接呼び出されません。代わりに、オブジェクトはスコープを離れることによって確定されます。 記述された出力はオブジェクトが終了するまで無効です。

