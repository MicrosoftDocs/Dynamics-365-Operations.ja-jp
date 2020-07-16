---
title: IISResponse クラス
description: このトピックでは、IISResponse クラスについて説明します。
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
ms.openlocfilehash: e339d0d9d7d93a68b8d0ea268a430e1854e8c97c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502602"
---
# <a name="class-iisresponse"></a>クラス IISResponse

[!include [banner](../../includes/banner.md)]

```xpp
class IISResponse extends Object
```

IISResponse クラスは、インターネット インフォメーション サービス (IIS) によって提供される Response オブジェクトをラップします。

## <a name="remarks"></a>備考

IISResponse クラスのメソッドと、IIS によって提供される Response オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。 したがって、IISResponse クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISResponse クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                    | 説明                                          |
|-----------------------------------------------------------|------------------------------------------------------|
| public boolean buffer(\[boolean isBuffering\])            |                                                      |
| public str cacheControl(\[str cacheControl\])             |                                                      |
| public boolean cacheWrite(\[boolean cache\])              |                                                      |
| public str charSet(\[str charSet\])                       |                                                      |
| public str contentType(\[str contentType\])               |                                                      |
| public IISRequestDictionary cookies()                     |                                                      |
| public int expires(\[int expiresMinutes\])                |                                                      |
| public COMVariant expiresAbsolute(\[COMVariant expires\]) |                                                      |
| public ComInterface interface()                           |                                                      |
| public boolean isClientConnected()                        |                                                      |
| public str status(\[str status\])                         | オブジェクトの状態を取得または設定します。                |
| public void addHeader(str headerName, str headerValue)    |                                                      |
| public void writeTxt(str text)                            |                                                      |
| public void write(COMVariant text)                        |                                                      |
| public void clear()                                       |                                                      |
| public void finalize()                                    |                                                      |
| public void binaryWrite(COMVariant input)                 |                                                      |
| public void appendToLog(str logEntry)                     |                                                      |
| public void new()                                         | IISResponse クラスの新しいインスタンスを初期化します。 |
| public void redirect(str url)                             |                                                      |
| public void flush()                                       |                                                      |
| public void pics(str headerValue)                         |                                                      |
| public void end()                                         |                                                      |

## <a name="method-buffer"></a>メソッド buffer

```xpp
public boolean buffer([boolean isBuffering])
```

### <a name="parameters---buffer"></a>パラメーター - buffer

isBuffering  

### <a name="return-value---buffer"></a>戻り値 - buffer

## <a name="method-cachecontrol"></a>メソッド cacheControl

```xpp
public str cacheControl([str cacheControl])
```

### <a name="parameters---cachecontrol"></a>パラメーター - cacheControl

cacheControl  

### <a name="return-value---cachecontrol"></a>戻り値 - cacheControl

## <a name="method-cachewrite"></a>メソッド cacheWrite

```xpp
public boolean cacheWrite([boolean cache])
```

### <a name="parameters---cachewrite"></a>パラメーター - cacheWrite

cache  

### <a name="return-value---cachewrite"></a>戻り値 - cacheWrite

## <a name="method-charset"></a>メソッド charSet

```xpp
public str charSet([str charSet])
```

### <a name="parameters---charset"></a>パラメーター - charSet

charSet  

### <a name="return-value---charset"></a>戻り値 - charSet

## <a name="method-contenttype"></a>メソッド contentType

```xpp
public str contentType([str contentType])
```

### <a name="parameters---contenttype"></a>パラメーター - contentType

contentType  

### <a name="return-value---contenttype"></a>戻り値 - contentType

## <a name="method-cookies"></a>メソッド cookies

```xpp
public IISRequestDictionary cookies()
```

### <a name="return-value---cookies"></a>戻り値 - cookie

## <a name="method-expires"></a>メソッド expires

```xpp
public int expires([int expiresMinutes])
```

### <a name="parameters---expires"></a>パラメーター - expires

expiresMinutes  

### <a name="return-value---expires"></a>戻り値 - expires

## <a name="method-expiresabsolute"></a>メソッド expiresAbsolute

```xpp
public COMVariant expiresAbsolute([COMVariant expires])
```

### <a name="parameters---expiresabsolute"></a>パラメーター - expiresAbsolute

expires  

### <a name="return-value---expiresabsolute"></a>戻り値 - expiresAbsolute

## <a name="method-interface"></a>メソッド interface

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a>戻り値 - interface

## <a name="method-isclientconnected"></a>メソッド isClientConnected

```xpp
public boolean isClientConnected()
```

### <a name="return-value---isclientconnected"></a>戻り値 - isClientConnected

## <a name="method-status"></a>メソッド status

オブジェクトの状態を取得または設定します。

```xpp
public str status([str status])
```

### <a name="parameters---status"></a>パラメーター - status

状態  

### <a name="return-value---status"></a>戻り値 - status

オブジェクトのステータスの現在の値。

## <a name="method-addheader"></a>メソッド addHeader

```xpp
public void addHeader(str headerName, str headerValue)
```

### <a name="parameters---addheader"></a>パラメーター - addHeader

headerName  

<!-- -->

headerValue  

## <a name="method-writetxt"></a>メソッド writeTxt

```xpp
public void writeTxt(str text)
```

### <a name="parameters---writetxt"></a>パラメーター - writeTxt

テキスト  

## <a name="method-write"></a>メソッド write

```xpp
public void write(COMVariant text)
```

### <a name="parameters---write"></a>パラメーター - write

テキスト  

## <a name="method-clear"></a>メソッド clear

```xpp
public void clear()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-binarywrite"></a>メソッド binaryWrite

```xpp
public void binaryWrite(COMVariant input)
```

### <a name="parameters---binarywrite"></a>パラメーター - binaryWrite

入力  

## <a name="method-appendtolog"></a>メソッド appendToLog

```xpp
public void appendToLog(str logEntry)
```

### <a name="parameters---appendtolog"></a>パラメーター - appendToLog

logEntry  

## <a name="method-new"></a>メソッド new

IISResponse クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-redirect"></a>メソッド redirect

```xpp
public void redirect(str url)
```

### <a name="parameters---redirect"></a>パラメーター - redirect

URL  

## <a name="method-flush"></a>メソッド flush

```xpp
public void flush()
```

## <a name="method-pics"></a>メソッド pics

```xpp
public void pics(str headerValue)
```

### <a name="parameters---pics"></a>パラメーター - pics

headerValue  

## <a name="method-end"></a>メソッド end

```xpp
public void end()
```

