---
title: IISRequest クラス
description: このトピックでは、IISRequest クラスについて説明します。
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
ms.openlocfilehash: 40e951d8a42d14cd6399d324414d2264010036dd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502603"
---
# <a name="class-iisrequest"></a>クラス IISRequest

[!include [banner](../../includes/banner.md)]

```xpp
class IISRequest extends Object
```

IISRequest クラスは、インターネット インフォメーション サービス (IIS) によって提供される Request オブジェクトをラップします。

## <a name="remarks"></a>備考

IISRequest クラスのメソッドと、IIS によって提供される Request オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISRequest クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISRequest クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                               | 説明                                         |
|------------------------------------------------------|-----------------------------------------------------|
| public COMVariant binaryRead(COMVariant countToRead) |                                                     |
| public IISRequestDictionary clientCertificate()      |                                                     |
| public IISRequestDictionary cookies()                |                                                     |
| public IISPostedFile file(COMVariant index)          |                                                     |
| public int fileCount()                               |                                                     |
| public IISRequestDictionary form()                   |                                                     |
| public ComInterface interface()                      |                                                     |
| public str item(str item)                            |                                                     |
| public IISRequestDictionary queryString()            |                                                     |
| public IISRequestDictionary serverVariables()        |                                                     |
| public int totalBytes()                              |                                                     |
| public void finalize()                               |                                                     |
| public void new()                                    | IISRequest クラスの新しいインスタンスを初期化します。 |

## <a name="method-binaryread"></a>メソッド binaryRead

```xpp
public COMVariant binaryRead(COMVariant countToRead)
```

### <a name="parameters---binaryread"></a>パラメーター - binaryRead

countToRead  

### <a name="return-value---binaryread"></a>戻り値-binaryRead

## <a name="method-clientcertificate"></a>メソッド clientCertificate

```xpp
public IISRequestDictionary clientCertificate()
```

### <a name="return-value---clientcertificate"></a>戻り値 - clientCertificate

## <a name="method-cookies"></a>メソッド cookies

```xpp
public IISRequestDictionary cookies()
```

### <a name="return-value---cookies"></a>戻り値 - cookie

## <a name="method-file"></a>メソッド file

```xpp
public IISPostedFile file(COMVariant index)
```

### <a name="parameters---file"></a>パラメーター - file

指数  

### <a name="return-value---file"></a>戻り値 - file

## <a name="method-filecount"></a>メソッド fileCount

```xpp
public int fileCount()
```

### <a name="return-value---filecount"></a>戻り値 - fileCount

## <a name="method-form"></a>メソッド form

```xpp
public IISRequestDictionary form()
```

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-item"></a>メソッド item

```xpp
public str item(str item)
```

### <a name="parameters---item"></a>パラメーター - item

品目  

### <a name="return-value---item"></a>戻り値 - item

## <a name="method-querystring"></a>メソッド queryString

```xpp
public IISRequestDictionary queryString()
```

### <a name="return-value---querystring"></a>戻り値 - queryString

## <a name="method-servervariables"></a>メソッド serverVariables

```xpp
public IISRequestDictionary serverVariables()
```

### <a name="return-value---servervariables"></a>戻り値 - serverVariables

## <a name="method-totalbytes"></a>メソッド totalBytes

```xpp
public int totalBytes()
```

### <a name="return-value---totalbytes"></a>戻り値 - totalBytes

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

IISRequest クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

