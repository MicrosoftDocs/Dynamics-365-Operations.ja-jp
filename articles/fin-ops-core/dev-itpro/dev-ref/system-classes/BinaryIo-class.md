---
title: BinaryIo クラス
description: このトピックでは、BinaryIo クラスについて説明します。
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
ms.openlocfilehash: bc23aa8f224926191dc3aa69ff7b965ae1259ebc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502719"
---
# <a name="class-binaryio"></a>クラス BinaryIo

[!include [banner](../../includes/banner.md)]

```xpp
class BinaryIo extends Io
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                  | 説明                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------|
| public container read()                 | Io オブジェクトから次の完全なレコードを読み取ります。                                  |
| public IO\_Status status()              | Io オブジェクトで実行された最後の操作のステータスを取得します。 |
| public boolean write(VarArg values)     | 単純型の値を記述します。                                                 |
| public boolean writeExp(container data) | コンテナのコンテンツをファイルに記述します。                                    |
| public void new(str filename, str mode) | BinaryIo クラスのインスタンスを作成します。                                      |
| public void finalize()                  | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。     |

## <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

```xpp
public container read()
```

### <a name="return-value---read"></a>戻り値 - read

入出力オブジェクトから次の完全なレコードを保持するコンテナーです。

### <a name="remarks---read"></a>備考 - read

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 そべての特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。 これらの既定の設定では、最も一般的な形式の入力と出力が可能です。 使用する形式をサポートするために、これらの設定の調整が生じる場合があります。

## <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a>戻り値 - status

IO\_Status システム列挙値としての最後の操作の状態。

### <a name="remarks---status"></a>備考 - status

返される可能性のある IO\_Status の値の範囲は、Io クラスによって異なります。

## <a name="method-write"></a>メソッド write

単純型の値を記述します。

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a>パラメーター - write

値  
単純型。 単純型は、文字列、整数、実数、列挙型、日付です。

### <a name="return-value---write"></a>戻り値 - write

書き込み操作が成功する場合は true。それ以外の場合は、false。 書き込み操作が失敗すると、ステータス メソッドで原因について確認できます。

### <a name="remarks---write"></a>備考 - write

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。 フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。 各レコードは、outRecordDelimiter メソッドで指定されるレコード 区切り記号で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

## <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをファイルに記述します。

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a>パラメーター - writeExp

データ  
レコードのデータを保持するコンテナー。

### <a name="return-value---writeexp"></a>戻り値 - writeExp

操作が成功する場合は true。それ以外の場合は、false。

### <a name="remarks---writeexp"></a>備考 - writeExp

このメソッドが false を返す場合、ステータス メソッドで原因を確認します。 コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。 フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。 レコード区切りは outRecordDelimiter メソッドで定義されます。

## <a name="method-new"></a>メソッド new

BinaryIo クラスのインスタンスを作成します。

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a>パラメーター - new

filename  
BinaryIo クラスのインスタンスを作成するために使用するモード。

<!-- -->

モード  
BinaryIo クラスのインスタンスを作成するために使用するモード。

### <a name="remarks---new"></a>備考 - new

攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドはクラス下で実行されます。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---new"></a>例 - new

この例では、BinaryIo クラスを使用して、ExampleFile のテキスト ファイルからデータを読み込みます。

```xpp
static void BinaryIoExampleW2(Args _args)
{     
    #define.ExampleFile(@"D:\Writers\GeneMi\_Junk\TestW.BinaryIo")
    #define.ExampleOpenModeW("w")
    #define.ExampleOpenModeR("r")
    BinaryIo binaryIoObject;
    container con1;
    str sConRecs;
    FileIoPermission perm;
```

```xpp
    // Set the code access permission to help protect the use of
    // the BinaryIo.new method.
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenModeW);
    if (perm == null)
    {
        return;
    }
    perm.assert();
```

```xpp
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
```

```xpp
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
```

## <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a>備考 - finalize

通常、スコープを離れることでオブジェクトを確定します。 したがって、確定メソッドは、通常は直接呼び出されません。 記述された出力はオブジェクトが終了するまで無効です。

