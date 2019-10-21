---
title: B クラス
description: 文字 B で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 50951
ms.assetid: 23a67a79-4f80-4f48-802a-08aba7824259
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5dda690503bdd8f4ba9c7865116eafb14a9d942
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183380"
---
# <a name="b-classes"></a>B クラス

[!include [banner](../includes/banner.md)]

文字 B で始まるシステム API クラス。

<a name="class-binary"></a>クラス バイナリ
------------

    class Binary extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                     |
|--------------------------------------------------------------------------|-------------------------------------------------|
| public int byte(int offset, \[int value\])                               |                                                 |
| public Real double(int offset, \[Real value\])                           |                                                 |
| public int dWord(int offset, \[int value\])                              |                                                 |
| public container getContainer()                                          |                                                 |
| public CLRObject getMemoryStream()                                       |                                                 |
| public Int64 qWord(int offset, \[Int64 value\])                          |                                                 |
| public str string(int offset, \[str value\])                             |                                                 |
| public int strLenBytes(int offset)                                       |                                                 |
| public int word(int offset, \[int value\])                               |                                                 |
| public str wString(int offset, \[str value\])                            |                                                 |
| ::public static Binary constructFromContainer(container data)            |                                                 |
| ::public static Binary constructFromMemoryStream(CLRObject memoryStream) |                                                 |
| public void attach(Int64 bufPtr, int bufSize)                            |                                                 |
| public void finalize()                                                   |                                                 |
| public void appendSubString(\[str string\])                              |                                                 |
| public void setBinaryValue(int offset, Binary value)                     |                                                 |
| public void new(AnyType buffersizeOrString, \[boolean wideString\])      | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-byte"></a>メソッド byte

    public int byte(int offset, [int value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-double"></a>メソッド double

    public Real double(int offset, [Real value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dword"></a>メソッド dWord

    public int dWord(int offset, [int value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getcontainer"></a>メソッド getContainer

    public container getContainer()

#### <a name="return-value"></a>戻り値

### <a name="method-getmemorystream"></a>メソッド getMemoryStream

    public CLRObject getMemoryStream()

#### <a name="return-value"></a>戻り値

### <a name="method-qword"></a>メソッド qWord

    public Int64 qWord(int offset, [Int64 value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-string"></a>メソッド string

    public str string(int offset, [str value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-strlenbytes"></a>メソッド strLenBytes

    public int strLenBytes(int offset)

#### <a name="parameters"></a>パラメーター

相殺  

#### <a name="return-value"></a>戻り値

### <a name="method-word"></a>メソッド word

    public int word(int offset, [int value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-wstring"></a>メソッド wString

    public str wString(int offset, [str value])

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

#### <a name="return-value"></a>戻り値

### <a name="method-constructfromcontainer"></a>メソッド constructFromContainer

    public static Binary constructFromContainer(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-constructfrommemorystream"></a>メソッド constructFromMemoryStream

    public static Binary constructFromMemoryStream(CLRObject memoryStream)

#### <a name="parameters"></a>パラメーター

memoryStream  

#### <a name="return-value"></a>戻り値

### <a name="method-attach"></a>メソッド attach

    public void attach(Int64 bufPtr, int bufSize)

#### <a name="parameters"></a>パラメーター

bufPtr  

<!-- -->

bufSize  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-appendsubstring"></a>メソッド appendSubString

    public void appendSubString([str string])

#### <a name="parameters"></a>パラメーター

string  

### <a name="method-setbinaryvalue"></a>メソッド setBinaryValue

    public void setBinaryValue(int offset, Binary value)

#### <a name="parameters"></a>パラメーター

相殺  

<!-- -->

値  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(AnyType buffersizeOrString, [boolean wideString])

#### <a name="parameters"></a>パラメーター

buffersizeOrString  

<!-- -->

wideString  

## <a name="class-binaryio"></a>クラス BinaryIo
    class BinaryIo extends Io

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                  | 説明                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------|
| public container read()                 | Io オブジェクトから次の完全なレコードを読み取ります。                                  |
| public IO\_Status status()              | Io オブジェクトで実行された最後の操作のステータスを取得します。 |
| public boolean write(VarArg values)     | 単純型の値を記述します。                                                 |
| public boolean writeExp(container data) | コンテナのコンテンツをファイルに記述します。                                    |
| public void new(str filename, str mode) | BinaryIo クラスのインスタンスを作成します。                                      |
| public void finalize()                  | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。     |

### <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

入出力オブジェクトから次の完全なレコードを保持するコンテナーです。

#### <a name="remarks"></a>備考

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 そべての特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。 これらの既定の設定では、最も一般的な形式の入力と出力が可能です。 使用する形式をサポートするために、これらの設定の調整が生じる場合があります。

### <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

IO\_Status システム列挙値としての最後の操作の状態。

#### <a name="remarks"></a>備考

返される可能性のある IO\_Status の値の範囲は、Io クラスによって異なります。

### <a name="method-write"></a>メソッド write

単純型の値を記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
単純型。 単純型は、文字列、整数、実数、列挙型、日付です。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は、false。 書き込み操作が失敗すると、ステータス メソッドで原因について確認できます。

#### <a name="remarks"></a>備考

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。 フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。 各レコードは、outRecordDelimiter メソッドで指定されるレコード 区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

### <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
レコードのデータを保持するコンテナー。

#### <a name="return-value"></a>戻り値

操作が成功する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドが false を返す場合、ステータス メソッドで原因を確認します。 コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。 フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。 レコード区切りは outRecordDelimiter メソッドで定義されます。

### <a name="method-new"></a>メソッド new

BinaryIo クラスのインスタンスを作成します。

    public void new(str filename, str mode)

#### <a name="parameters"></a>パラメーター

filename  
BinaryIo クラスのインスタンスを作成するために使用するモード。

<!-- -->

モード  
BinaryIo クラスのインスタンスを作成するために使用するモード。

#### <a name="remarks"></a>備考

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドはクラス下で実行されます。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

この例では、BinaryIo クラスを使用して、ExampleFile のテキスト ファイルからデータを読み込みます。

    static void BinaryIoExampleW2(Args _args)
    {     
        #define.ExampleFile(@"D:\Writers\GeneMi\_Junk\TestW.BinaryIo")
        #define.ExampleOpenModeW("w")
        #define.ExampleOpenModeR("r")
        BinaryIo binaryIoObject;
        container con1;
        str sConRecs;
        FileIoPermission perm;

        // Set the code access permission to help protect the use of
        // the BinaryIo.new method.
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenModeW);
        if (perm == null)
        {
            return;
        }
        perm.assert();

        // Overwrites the file if it already exists; restarts it as empty.
        binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeW);
        if (binaryIoObject != null)
        {
            info("w binaryIoObject is NOT null, Good.");
            binaryIoObject.write("hello world");
            binaryIoObject.write("goodbye solar system");
        }
        else
        {
            warning("w binaryIoObject is NULL, Bad.");
        }

        binaryIoObject.finalize();
        binaryIoObject = null;
        // Close the file, w?
        // BinaryIo instance can only read files in that
        // are in the exact same esoteric format that BinaryIo
        // writes files to.
        // binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeR);
        if (binaryIoObject != null)
        {
             info("r binaryIoObject is NOT null, Good.");
             while (true)
            {
                con1 = binaryIoObject.read();
                if (con1 == conNull())
                {
                    info("r, no more records.");
                    break;
                }
                sConRecs = con2Str(con1);
                info(sConRecs);
            }
        }
        else
        {
             warning("r binaryIoObject is NULL, Bad.");
        }
        binaryIoObject.finalize();
        binaryIoObject = null;
        WINAPI::deleteFile(#ExampleFile);
         // Clean up after the job.
        CodeAccessPermission::revertAssert();
     }
    /*** Output copied from Infolog:Message (11:22:16 am)w binaryIoObject is NOT null, Good.r binaryIoObject is NOT null, Good.hello worldgoodbye solar systemr, no more records.***/

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

通常、スコープを離れることでオブジェクトを確定します。 したがって、確定メソッドは、通常は直接呼び出されません。 記述された出力はオブジェクトが終了するまで無効です。

## <a name="class-bindata"></a>クラス BinData
    class BinData extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| public boolean appendToFile(str filename)                             |                                               |
| public str ascii85Encode()                                            |                                               |
| public str base64Encode()                                             |                                               |
| public int compressLZ77(int windowBits)                               |                                               |
| public boolean copyData(BinData data, \[int offset\], \[int length\]) |                                               |
| public int decompressLZ77()                                           |                                               |
| public str getAsciiData()                                             |                                               |
| public container getData()                                            |                                               |
| public str getStrData()                                               |                                               |
| public COMVariant getVariant()                                        |                                               |
| public boolean loadFile(str filename, \[int offset\], \[int length\]) |                                               |
| public boolean saveFile(str filename)                                 |                                               |
| public int size()                                                     |                                               |
| ::public static str dataToString(container data)                      |                                               |
| ::public static container loadFromAscii85(str ascii85EncodedString)   |                                               |
| ::public static container loadFromBase64(str base64EncodedString)     |                                               |
| ::public static container stringToData(str string)                    |                                               |
| public void setStrData(str data)                                      |                                               |
| public void setVariant(COMVariant data)                               |                                               |
| public void appendData(BinData binData)                               |                                               |
| public void new()                                                     | BinData クラスのインスタンスを初期化します。 |
| public void setBinaryData(Binary binary)                              |                                               |
| public void setAsciiData(str data, \[int codePage\])                  |                                               |
| public void setData(container data)                                   |                                               |
| public void finalize()                                                |                                               |

### <a name="method-appendtofile"></a>メソッド appendToFile

    public boolean appendToFile(str filename)

#### <a name="parameters"></a>パラメーター

filename  

#### <a name="return-value"></a>戻り値

### <a name="method-ascii85encode"></a>メソッド ascii85Encode

    public str ascii85Encode()

#### <a name="return-value"></a>戻り値

### <a name="method-base64encode"></a>メソッド base64Encode

    public str base64Encode()

#### <a name="return-value"></a>戻り値

### <a name="method-compresslz77"></a>メソッド compressLZ77

    public int compressLZ77(int windowBits)

#### <a name="parameters"></a>パラメーター

windowBits  

#### <a name="return-value"></a>戻り値

### <a name="method-copydata"></a>メソッド copyData

    public boolean copyData(BinData data, [int offset], [int length])

#### <a name="parameters"></a>パラメーター

データ  

<!-- -->

相殺  

<!-- -->

length  

#### <a name="return-value"></a>戻り値

### <a name="method-decompresslz77"></a>メソッド decompressLZ77

    public int decompressLZ77()

#### <a name="return-value"></a>戻り値

### <a name="method-getasciidata"></a>メソッド getAsciiData

    public str getAsciiData()

#### <a name="return-value"></a>戻り値

### <a name="method-getdata"></a>メソッド getData

    public container getData()

#### <a name="return-value"></a>戻り値

### <a name="method-getstrdata"></a>メソッド getStrData

    public str getStrData()

#### <a name="return-value"></a>戻り値

### <a name="method-getvariant"></a>メソッド getVariant

    public COMVariant getVariant()

#### <a name="return-value"></a>戻り値

### <a name="method-loadfile"></a>メソッド loadFile

    public boolean loadFile(str filename, [int offset], [int length])

#### <a name="parameters"></a>パラメーター

filename  

<!-- -->

相殺  

<!-- -->

length  

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

攻撃者が loadFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="method-savefile"></a>メソッド saveFile

    public boolean saveFile(str filename)

#### <a name="parameters"></a>パラメーター

filename  

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

攻撃者が saveFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="method-size"></a>メソッド size

    public int size()

#### <a name="return-value"></a>戻り値

### <a name="method-datatostring"></a>メソッド dataToString

    public static str dataToString(container data)

#### <a name="parameters"></a>パラメーター

データ  

#### <a name="return-value"></a>戻り値

### <a name="method-loadfromascii85"></a>メソッド loadFromAscii85

    public static container loadFromAscii85(str ascii85EncodedString)

#### <a name="parameters"></a>パラメーター

ascii85EncodedString  

#### <a name="return-value"></a>戻り値

### <a name="method-loadfrombase64"></a>メソッド loadFromBase64

    public static container loadFromBase64(str base64EncodedString)

#### <a name="parameters"></a>パラメーター

base64EncodedString  

#### <a name="return-value"></a>戻り値

### <a name="method-stringtodata"></a>メソッド stringToData

    public static container stringToData(str string)

#### <a name="parameters"></a>パラメーター

string  

#### <a name="return-value"></a>戻り値

### <a name="method-setstrdata"></a>メソッド setStrData

    public void setStrData(str data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-setvariant"></a>メソッド setVariant

    public void setVariant(COMVariant data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-appenddata"></a>メソッド appendData

    public void appendData(BinData binData)

#### <a name="parameters"></a>パラメーター

binData  

### <a name="method-new"></a>メソッド new

BinData クラスのインスタンスを初期化します。

    public void new()

### <a name="method-setbinarydata"></a>メソッド setBinaryData

    public void setBinaryData(Binary binary)

#### <a name="parameters"></a>パラメーター

binary  

### <a name="method-setasciidata"></a>メソッド setAsciiData

    public void setAsciiData(str data, [int codePage])

#### <a name="parameters"></a>パラメーター

データ  

<!-- -->

codePage  

### <a name="method-setdata"></a>メソッド setData

    public void setData(container data)

#### <a name="parameters"></a>パラメーター

データ  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()



