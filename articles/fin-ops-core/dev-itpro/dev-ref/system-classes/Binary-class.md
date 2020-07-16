---
title: バイナリ クラス
description: このトピックでは、バイナリ クラスについて説明します。
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
ms.openlocfilehash: 90669ef6c0d171ca8ea8a28c88f5137f11698e4b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502720"
---
# <a name="class-binary"></a>クラス バイナリ

[!include [banner](../../includes/banner.md)]


```xpp
class Binary extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-byte"></a>メソッド byte

```xpp
public int byte(int offset, [int value])
```

### <a name="parameters---byte"></a>パラメーター - byte

相殺  

<!-- -->

値  

### <a name="return-value---byte"></a>戻り値 - byte

## <a name="method-double"></a>メソッド double

```xpp
public Real double(int offset, [Real value])
```

### <a name="parameters---double"></a>パラメーター - double

相殺  

<!-- -->

値  

### <a name="return-value---double"></a>戻り値 - double

## <a name="method-dword"></a>メソッド dWord

```xpp
public int dWord(int offset, [int value])
```

### <a name="parameters---dword"></a>パラメーター - dWord

相殺  

<!-- -->

値  

### <a name="return-value---dword"></a>戻り値 - dWord

## <a name="method-getcontainer"></a>メソッド getContainer

```xpp
public container getContainer()
```

### <a name="return-value---getcontainer"></a>戻り値 - getContainer

## <a name="method-getmemorystream"></a>メソッド getMemoryStream

```xpp
public CLRObject getMemoryStream()
```

### <a name="return-value---getmemorystream"></a>戻り値 - getMemoryStream

## <a name="method-qword"></a>メソッド qWord

```xpp
public Int64 qWord(int offset, [Int64 value])
```

### <a name="parameters---qword"></a>パラメーター - qWord

相殺  

<!-- -->

値  

### <a name="return-value---qword"></a>戻り値 - qWord

## <a name="method-string"></a>メソッド string

```xpp
public str string(int offset, [str value])
```

### <a name="parameters---string"></a>パラメーター - string

相殺  

<!-- -->

値  

### <a name="return-value---string"></a>戻り値 - string

## <a name="method-strlenbytes"></a>メソッド strLenBytes

```xpp
public int strLenBytes(int offset)
```

### <a name="parameters---strlenbytes"></a>パラメーター - strLenBytes

相殺  

### <a name="return-value---strlenbytes"></a>戻り値 - strLenBytes

## <a name="method-word"></a>メソッド word

```xpp
public int word(int offset, [int value])
```

### <a name="parameters---word"></a>パラメーター - word

相殺  

<!-- -->

値  

### <a name="return-value---word"></a>戻り値 - word

## <a name="method-wstring"></a>メソッド wString

```xpp
public str wString(int offset, [str value])
```

### <a name="parameters---wstring"></a>パラメーター - wString

相殺  

<!-- -->

値  

### <a name="return-value---wstring"></a>戻り値 - wString

## <a name="method-constructfromcontainer"></a>メソッド constructFromContainer

```xpp
public static Binary constructFromContainer(container data)
```

### <a name="parameters---constructfromcontainer"></a>パラメーター   constructFromContainer

データ  

### <a name="return-value---constructfromcontainer"></a>戻り値 - constructFromContainer

## <a name="method-constructfrommemorystream"></a>メソッド constructFromMemoryStream

```xpp
public static Binary constructFromMemoryStream(CLRObject memoryStream)
```

### <a name="parameters---constructfrommemorystream"></a>パラメーター - constructFromMemoryStream

memoryStream  

### <a name="return-value---constructfrommemorystream"></a>戻り値 - constructFromMemoryStream

## <a name="method-attach"></a>メソッド attach

```xpp
public void attach(Int64 bufPtr, int bufSize)
```

### <a name="parameters---attach"></a>パラメーター - attach

bufPtr  

<!-- -->

bufSize  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-appendsubstring"></a>メソッド appendSubString

```xpp
public void appendSubString([str string])
```

### <a name="parameters---appendsubstring"></a>パラメーター - appendSubString

文字列  

## <a name="method-setbinaryvalue"></a>メソッド setBinaryValue

```xpp
public void setBinaryValue(int offset, Binary value)
```

### <a name="parameters---setbinaryvalue"></a>パラメーター - setBinaryValue

相殺  

<!-- -->

値  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(AnyType buffersizeOrString, [boolean wideString])
```

### <a name="parameters---new"></a>パラメーター - new

buffersizeOrString  

<!-- -->

wideString  

