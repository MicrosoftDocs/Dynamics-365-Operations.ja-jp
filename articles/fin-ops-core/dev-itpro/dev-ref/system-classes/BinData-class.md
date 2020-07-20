---
title: BinData クラス
description: このトピックでは、BinData クラスについて説明します。
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
ms.openlocfilehash: 693f2179ce7344cfa565456b8ee539d4708a6142
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502721"
---
# <a name="class-bindata"></a>クラス BinData

[!include [banner](../../includes/banner.md)]

```xpp
class BinData extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-appendtofile"></a>メソッド appendToFile

```xpp
public boolean appendToFile(str filename)
```

### <a name="parameters---appendtofile"></a>パラメーター - appendToFile

filename  

### <a name="return-value---appendtofile"></a>戻り値 - appendToFile

## <a name="method-ascii85encode"></a>メソッド ascii85Encode

```xpp
public str ascii85Encode()
```

### <a name="return-value---ascii85encode"></a>戻り値 - ascii85Encode

## <a name="method-base64encode"></a>メソッド base64Encode

```xpp
public str base64Encode()
```

### <a name="return-value---base64encode"></a>戻り値 - base64Encode

## <a name="method-compresslz77"></a>メソッド compressLZ77

```xpp
public int compressLZ77(int windowBits)
```

### <a name="parameters---compresslz77"></a>パラメーター - compressLZ77

windowBits  

### <a name="return-value---compresslz77"></a>戻り値 - compressLZ77

## <a name="method-copydata"></a>メソッド copyData

```xpp
public boolean copyData(BinData data, [int offset], [int length])
```

### <a name="parameters---copydata"></a>パラメーター - copyData

データ  

<!-- -->

相殺  

<!-- -->

length  

### <a name="return-value---copydata"></a>戻り値 - copyData

## <a name="method-decompresslz77"></a>メソッド decompressLZ77

```xpp
public int decompressLZ77()
```

### <a name="return-value---decompresslz77"></a>戻り値 - decompressLZ77

## <a name="method-getasciidata"></a>メソッド getAsciiData

```xpp
public str getAsciiData()
```

### <a name="return-value---getasciidata"></a>戻り値 - getAsciiData

## <a name="method-getdata"></a>メソッド getData

```xpp
public container getData()
```

### <a name="return-value---getdata"></a>戻り値 - getData

## <a name="method-getstrdata"></a>メソッド getStrData

```xpp
public str getStrData()
```

### <a name="return-value---getstrdata"></a>戻り値 - getStrData

## <a name="method-getvariant"></a>メソッド getVariant

```xpp
public COMVariant getVariant()
```

### <a name="return-value---getvariant"></a>戻り値 - getVariant

## <a name="method-loadfile"></a>メソッド loadFile

```xpp
public boolean loadFile(str filename, [int offset], [int length])
```

### <a name="parameters---loadfile"></a>パラメーター - loadFile

filename  

<!-- -->

相殺  

<!-- -->

length  

### <a name="return-value---loadfile"></a>戻り値 - loadFile

### <a name="remarks---loadfile"></a>備考 - loadFile

攻撃者が loadFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="method-savefile"></a>メソッド saveFile

```xpp
public boolean saveFile(str filename)
```

### <a name="parameters---savefile"></a>パラメーター - saveFile

filename  

### <a name="return-value---savefile"></a>戻り値 - saveFile

### <a name="remarks---savefile"></a>備考 - saveFile

攻撃者が saveFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

## <a name="method-size"></a>メソッド size

```xpp
public int size()
```

### <a name="return-value---size"></a>戻り値 - size

## <a name="method-datatostring"></a>メソッド dataToString

```xpp
public static str dataToString(container data)
```

### <a name="parameters---datatostring"></a>パラメーター - dataToString

データ  

### <a name="return-value---datatostring"></a>戻り値 - dataToString

## <a name="method-loadfromascii85"></a>メソッド loadFromAscii85

```xpp
public static container loadFromAscii85(str ascii85EncodedString)
```

### <a name="parameters---loadfromascii85"></a>パラメーター - loadFromAscii85

ascii85EncodedString  

### <a name="return-value---loadfromascii85"></a>戻り値 - loadFromAscii85

## <a name="method-loadfrombase64"></a>メソッド loadFromBase64

```xpp
public static container loadFromBase64(str base64EncodedString)
```

### <a name="parameters---loadfrombase64"></a>パラメーター - loadFromBase64

base64EncodedString  

### <a name="return-value---loadfrombase64"></a>戻り値 - loadFromBase64

## <a name="method-stringtodata"></a>メソッド stringToData

```xpp
public static container stringToData(str string)
```

### <a name="parameters---stringtodata"></a>パラメーター - stringToData

文字列  

### <a name="return-value---stringtodata"></a>戻り値 - stringToData

## <a name="method-setstrdata"></a>メソッド setStrData

```xpp
public void setStrData(str data)
```

### <a name="parameters---setstrdata"></a>パラメーター - setStrData

データ  

## <a name="method-setvariant"></a>メソッド setVariant

```xpp
public void setVariant(COMVariant data)
```

### <a name="parameters---setvariant"></a>パラメーター - setVariant

データ  

## <a name="method-appenddata"></a>メソッド appendData

```xpp
public void appendData(BinData binData)
```

### <a name="parameters---appenddata"></a>パラメーター - appendData

binData  

## <a name="method-new"></a>メソッド new

BinData クラスのインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-setbinarydata"></a>メソッド setBinaryData

```xpp
public void setBinaryData(Binary binary)
```

### <a name="parameters---setbinarydata"></a>パラメーター - setBinaryData

binary  

## <a name="method-setasciidata"></a>メソッド setAsciiData

```xpp
public void setAsciiData(str data, [int codePage])
```

### <a name="parameters---setasciidata"></a>パラメーター - setAsciiData

データ  

<!-- -->

codePage  

## <a name="method-setdata"></a>メソッド setData

```xpp
public void setData(container data)
```

### <a name="parameters---setdata"></a>パラメーター - setData

データ  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```


