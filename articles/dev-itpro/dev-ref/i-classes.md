---
title: I クラス
description: 文字 I で始まるシステム API クラス。
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
ms.custom: 52171
ms.assetid: bd6df991-7b90-40f0-b342-025ab000c24c
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f06f3929aad48c39dc87b18eba406d0521323b71
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368651"
---
# <a name="i-classes"></a>I クラス

[!include [banner](../includes/banner.md)]

文字 I で始まるシステム API クラス。

<a name="class-idispatcherproxy"></a>クラス IDispatcherProxy
----------------------

    class IDispatcherProxy

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明 |
|------------------------------------------------|-------------|
| public AnyType invoke(str methodName, VarArg ) |             |
| public void refresh()                          |             |

### <a name="method-invoke"></a>メソッド invoke

    public AnyType invoke(str methodName, VarArg )

#### <a name="parameters"></a>パラメーター

methodName  

<!-- -->



#### <a name="return-value"></a>戻り値

### <a name="method-refresh"></a>メソッド refresh

    public void refresh()

## <a name="class-iisapplicationobject"></a>クラス IISApplicationObject
    class IISApplicationObject extends Object

IISApplicationObject クラスは、インターネット インフォメーション サービス (IIS) によって提供されるアプリケーション オブジェクトをラップします。

### <a name="remarks"></a>備考

IISApplicationObject クラスのメソッドと、IIS によって提供される Application オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISApplicationObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISApplicationObject クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| public IISVariantDictionary contents()                 |                                                               |
| public ComInterface interface()                        |                                                               |
| public IISVariantDictionary staticObjects()            |                                                               |
| public COMVariant value(str value, \[COMVariant var\]) |                                                               |
| public str valueTxt(str value, \[str var\])            |                                                               |
| public void new()                                      | IISApplicationObject クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                 |                                                               |
| public void lock()                                     |                                                               |
| public void unLock()                                   |                                                               |

### <a name="method-contents"></a>メソッド contents

    public IISVariantDictionary contents()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-staticobjects"></a>メソッド staticObjects

    public IISVariantDictionary staticObjects()

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-valuetxt"></a>メソッド valueTxt

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

IISApplicationObject クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-lock"></a>メソッド lock

    public void lock()

### <a name="method-unlock"></a>メソッド unLock

    public void unLock()

## <a name="class-iiscontextobject"></a>クラス IISContextObject
    class IISContextObject extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| public ComInterface interface()                        |                                                           |
| public boolean isTraceEnabled()                        |                                                           |
| public IISVariantDictionary items()                    |                                                           |
| public int traceMode(int mode)                         |                                                           |
| public COMVariant value(str value, \[COMVariant var\]) |                                                           |
| public str valueTxt(str value, \[str var\])            |                                                           |
| public void traceWrite(str category, str message)      |                                                           |
| public void finalize()                                 |                                                           |
| public void traceWarn(str category, str message)       |                                                           |
| public void new()                                      | IISContextObject クラスの新しいインスタンスを初期化します。 |

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-istraceenabled"></a>メソッド isTraceEnabled

    public boolean isTraceEnabled()

#### <a name="return-value"></a>戻り値

### <a name="method-items"></a>メソッド items

    public IISVariantDictionary items()

#### <a name="return-value"></a>戻り値

### <a name="method-tracemode"></a>メソッド traceMode

    public int traceMode(int mode)

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-valuetxt"></a>メソッド valueTxt

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-tracewrite"></a>メソッド traceWrite

    public void traceWrite(str category, str message)

#### <a name="parameters"></a>パラメーター

カテゴリ  

<!-- -->

メッセージ  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-tracewarn"></a>メソッド traceWarn

    public void traceWarn(str category, str message)

#### <a name="parameters"></a>パラメーター

カテゴリ  

<!-- -->

メッセージ  

### <a name="method-new"></a>メソッド new

IISContextObject クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-iispostedfile"></a>クラス IISPostedFile
    class IISPostedFile extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                 | 説明                                            |
|----------------------------------------|--------------------------------------------------------|
| public int contentLength()             |                                                        |
| public str contentType()               |                                                        |
| public str fileName()                  |                                                        |
| public container read(int countToRead) |                                                        |
| public void finalize()                 |                                                        |
| public void new()                      | IISPostedFile クラスの新しいインスタンスを初期化します。 |

### <a name="method-contentlength"></a>メソッド contentLength

    public int contentLength()

#### <a name="return-value"></a>戻り値

### <a name="method-contenttype"></a>メソッド contentType

    public str contentType()

#### <a name="return-value"></a>戻り値

### <a name="method-filename"></a>メソッド fileName

    public str fileName()

#### <a name="return-value"></a>戻り値

### <a name="method-read"></a>メソッド read

    public container read(int countToRead)

#### <a name="parameters"></a>パラメーター

countToRead  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

IISPostedFile クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-iisreadcookie"></a>クラス IISReadCookie
    class IISReadCookie extends Object

IISReadCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される ReadCookie オブジェクトをラップします。

### <a name="remarks"></a>備考

IISReadCookie クラスのメソッドと、IIS によって提供される ReadCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISReadCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISReadCookie クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                           | 説明                                     |
|----------------------------------|-------------------------------------------------|
| public int count()               |                                                 |
| public COMEnum2Variant getEnum() |                                                 |
| public boolean hasKeys()         |                                                 |
| public ComInterface interface()  |                                                 |
| public str item(\[str item\])    |                                                 |
| public str key(str key)          |                                                 |
| public void finalize()           |                                                 |
| public void new(COM readCookie)  | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-getenum"></a>メソッド getEnum

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a>戻り値

### <a name="method-haskeys"></a>メソッド hasKeys

    public boolean hasKeys()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public str item([str item])

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-key"></a>メソッド key

    public str key(str key)

#### <a name="parameters"></a>パラメーター

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(COM readCookie)

#### <a name="parameters"></a>パラメーター

readCookie  

## <a name="class-iisrequest"></a>クラス IISRequest
    class IISRequest extends Object

IISRequest クラスは、インターネット インフォメーション サービス (IIS) によって提供される Request オブジェクトをラップします。

### <a name="remarks"></a>備考

IISRequest クラスのメソッドと、IIS によって提供される Request オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISRequest クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISRequest クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-binaryread"></a>メソッド binaryRead

    public COMVariant binaryRead(COMVariant countToRead)

#### <a name="parameters"></a>パラメーター

countToRead  

#### <a name="return-value"></a>戻り値

### <a name="method-clientcertificate"></a>メソッド clientCertificate

    public IISRequestDictionary clientCertificate()

#### <a name="return-value"></a>戻り値

### <a name="method-cookies"></a>メソッド cookies

    public IISRequestDictionary cookies()

#### <a name="return-value"></a>戻り値

### <a name="method-file"></a>メソッド file

    public IISPostedFile file(COMVariant index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-filecount"></a>メソッド fileCount

    public int fileCount()

#### <a name="return-value"></a>戻り値

### <a name="method-form"></a>メソッド form

    public IISRequestDictionary form()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public str item(str item)

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-querystring"></a>メソッド queryString

    public IISRequestDictionary queryString()

#### <a name="return-value"></a>戻り値

### <a name="method-servervariables"></a>メソッド serverVariables

    public IISRequestDictionary serverVariables()

#### <a name="return-value"></a>戻り値

### <a name="method-totalbytes"></a>メソッド totalBytes

    public int totalBytes()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

IISRequest クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-iisrequestdictionary"></a>クラス IISRequestDictionary
    class IISRequestDictionary extends Object

IISRequestDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される RequestDictionary オブジェクトをラップします。

### <a name="remarks"></a>備考

IISRequestDictionary クラスのメソッドと、IIS によって提供される RequestDictionary オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。 したがって、IISRequestDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISRequestDictionary クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                              | 説明                                     |
|-----------------------------------------------------|-------------------------------------------------|
| public int count()                                  |                                                 |
| public COMEnum2Variant getEnum()                    |                                                 |
| public ComInterface interface()                     |                                                 |
| public COMVariant item(COMVariant item)             |                                                 |
| public IISReadCookie itemReadCookie(\[str item\])   |                                                 |
| public IISStringList itemStringList(\[str item\])   |                                                 |
| public str itemTxt(str item)                        |                                                 |
| public IISWriteCookie itemWriteCookie(\[str item\]) |                                                 |
| public str key(str key)                             |                                                 |
| public void finalize()                              |                                                 |
| public void new(COM requestDictionary)              | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-getenum"></a>メソッド getEnum

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public COMVariant item(COMVariant item)

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-itemreadcookie"></a>メソッド itemReadCookie

    public IISReadCookie itemReadCookie([str item])

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-itemstringlist"></a>メソッド itemStringList

    public IISStringList itemStringList([str item])

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-itemtxt"></a>メソッド itemTxt

    public str itemTxt(str item)

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-itemwritecookie"></a>メソッド itemWriteCookie

    public IISWriteCookie itemWriteCookie([str item])

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-key"></a>メソッド key

    public str key(str key)

#### <a name="parameters"></a>パラメーター

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(COM requestDictionary)

#### <a name="parameters"></a>パラメーター

requestDictionary  

## <a name="class-iisresponse"></a>クラス IISResponse
    class IISResponse extends Object

IISResponse クラスは、インターネット インフォメーション サービス (IIS) によって提供される Response オブジェクトをラップします。

### <a name="remarks"></a>備考

IISResponse クラスのメソッドと、IIS によって提供される Response オブジェクトのメソッドとの間には、1 対 1 のリレーションシップがあります。 したがって、IISResponse クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISResponse クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-buffer"></a>メソッド buffer

    public boolean buffer([boolean isBuffering])

#### <a name="parameters"></a>パラメーター

isBuffering  

#### <a name="return-value"></a>戻り値

### <a name="method-cachecontrol"></a>メソッド cacheControl

    public str cacheControl([str cacheControl])

#### <a name="parameters"></a>パラメーター

cacheControl  

#### <a name="return-value"></a>戻り値

### <a name="method-cachewrite"></a>メソッド cacheWrite

    public boolean cacheWrite([boolean cache])

#### <a name="parameters"></a>パラメーター

cache  

#### <a name="return-value"></a>戻り値

### <a name="method-charset"></a>メソッド charSet

    public str charSet([str charSet])

#### <a name="parameters"></a>パラメーター

charSet  

#### <a name="return-value"></a>戻り値

### <a name="method-contenttype"></a>メソッド contentType

    public str contentType([str contentType])

#### <a name="parameters"></a>パラメーター

contentType  

#### <a name="return-value"></a>戻り値

### <a name="method-cookies"></a>メソッド cookies

    public IISRequestDictionary cookies()

#### <a name="return-value"></a>戻り値

### <a name="method-expires"></a>メソッド expires

    public int expires([int expiresMinutes])

#### <a name="parameters"></a>パラメーター

expiresMinutes  

#### <a name="return-value"></a>戻り値

### <a name="method-expiresabsolute"></a>メソッド expiresAbsolute

    public COMVariant expiresAbsolute([COMVariant expires])

#### <a name="parameters"></a>パラメーター

expires  

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-isclientconnected"></a>メソッド isClientConnected

    public boolean isClientConnected()

#### <a name="return-value"></a>戻り値

### <a name="method-status"></a>メソッド status

オブジェクトの状態を取得または設定します。

    public str status([str status])

#### <a name="parameters"></a>パラメーター

ステータス  

#### <a name="return-value"></a>戻り値

オブジェクトのステータスの現在の値。

### <a name="method-addheader"></a>メソッド addHeader

    public void addHeader(str headerName, str headerValue)

#### <a name="parameters"></a>パラメーター

headerName  

<!-- -->

headerValue  

### <a name="method-writetxt"></a>メソッド writeTxt

    public void writeTxt(str text)

#### <a name="parameters"></a>パラメーター

テキスト  

### <a name="method-write"></a>メソッド write

    public void write(COMVariant text)

#### <a name="parameters"></a>パラメーター

テキスト  

### <a name="method-clear"></a>メソッド clear

    public void clear()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-binarywrite"></a>メソッド binaryWrite

    public void binaryWrite(COMVariant input)

#### <a name="parameters"></a>パラメーター

input  

### <a name="method-appendtolog"></a>メソッド appendToLog

    public void appendToLog(str logEntry)

#### <a name="parameters"></a>パラメーター

logEntry  

### <a name="method-new"></a>メソッド new

IISResponse クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-redirect"></a>メソッド redirect

    public void redirect(str url)

#### <a name="parameters"></a>パラメーター

URL  

### <a name="method-flush"></a>メソッド flush

    public void flush()

### <a name="method-pics"></a>メソッド pics

    public void pics(str headerValue)

#### <a name="parameters"></a>パラメーター

headerValue  

### <a name="method-end"></a>メソッド end

    public void end()

## <a name="class-iisserver"></a>クラス IISServer
    class IISServer extends Object

IISServer クラスは、インターネット インフォメーション サービス (IIS) によって提供される Server オブジェクトをラップします。

### <a name="remarks"></a>備考

IISServer クラスのメソッドと、IIS によって提供される Server オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISServer クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISServer クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                        |
|--------------------------------------------------|----------------------------------------------------|
| public COM createObject(str progID)              |                                                    |
| public str htmlEncode(str txt)                   |                                                    |
| public ComInterface interface()                  |                                                    |
| public str mapPath(str logicalPath)              |                                                    |
| public int scriptTimeout(\[int timeoutSeconds\]) |                                                    |
| public str urlEncode(str txt)                    |                                                    |
| public str urlPathEncode(str txt)                |                                                    |
| public void execute(str logicalPath)             |                                                    |
| public void transfer(str logicalPath)            |                                                    |
| public void new()                                | IISServer クラスの新しいインスタンスを初期化します。 |
| public void finalize()                           |                                                    |

### <a name="method-createobject"></a>メソッド createObject

    public COM createObject(str progID)

#### <a name="parameters"></a>パラメーター

progID  

#### <a name="return-value"></a>戻り値

### <a name="method-htmlencode"></a>メソッド htmlEncode

    public str htmlEncode(str txt)

#### <a name="parameters"></a>パラメーター

txt  

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-mappath"></a>メソッド mapPath

    public str mapPath(str logicalPath)

#### <a name="parameters"></a>パラメーター

logicalPath  

#### <a name="return-value"></a>戻り値

### <a name="method-scripttimeout"></a>メソッド scriptTimeout

    public int scriptTimeout([int timeoutSeconds])

#### <a name="parameters"></a>パラメーター

timeoutSeconds  

#### <a name="return-value"></a>戻り値

### <a name="method-urlencode"></a>メソッド urlEncode

    public str urlEncode(str txt)

#### <a name="parameters"></a>パラメーター

txt  

#### <a name="return-value"></a>戻り値

### <a name="method-urlpathencode"></a>メソッド urlPathEncode

    public str urlPathEncode(str txt)

#### <a name="parameters"></a>パラメーター

txt  

#### <a name="return-value"></a>戻り値

### <a name="method-execute"></a>メソッド execute

    public void execute(str logicalPath)

#### <a name="parameters"></a>パラメーター

logicalPath  

### <a name="method-transfer"></a>メソッド transfer

    public void transfer(str logicalPath)

#### <a name="parameters"></a>パラメーター

logicalPath  

### <a name="method-new"></a>メソッド new

IISServer クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-iissessionobject"></a>クラス IISSessionObject
    class IISSessionObject extends Object

IISSessionObject クラスは、インターネット インフォメーション サービス (IIS) によって提供される Session オブジェクトをラップします。

### <a name="remarks"></a>備考

IISSessionObject クラスのメソッドと、IIS によって提供される Session オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISSessionObject クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISSessionObject クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| public int codePage(\[int codePage\])                  |                                                           |
| public IISVariantDictionary contents()                 |                                                           |
| public str getSessionID()                              |                                                           |
| public ComInterface interface()                        |                                                           |
| public int lcid(\[int lcid\])                          |                                                           |
| public IISVariantDictionary staticObjects()            |                                                           |
| public int timeout(\[int timeout\])                    |                                                           |
| public COMVariant value(str value, \[COMVariant var\]) |                                                           |
| public str valueTxt(str value, \[str var\])            |                                                           |
| public void new()                                      | IISSessionObject クラスの新しいインスタンスを初期化します。 |
| public void abandon()                                  |                                                           |
| public void finalize()                                 |                                                           |

### <a name="method-codepage"></a>メソッド codePage

    public int codePage([int codePage])

#### <a name="parameters"></a>パラメーター

codePage  

#### <a name="return-value"></a>戻り値

### <a name="method-contents"></a>メソッド contents

    public IISVariantDictionary contents()

#### <a name="return-value"></a>戻り値

### <a name="method-getsessionid"></a>メソッド getSessionID

    public str getSessionID()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-lcid"></a>メソッド lcid

    public int lcid([int lcid])

#### <a name="parameters"></a>パラメーター

lcid  

#### <a name="return-value"></a>戻り値

### <a name="method-staticobjects"></a>メソッド staticObjects

    public IISVariantDictionary staticObjects()

#### <a name="return-value"></a>戻り値

### <a name="method-timeout"></a>メソッド timeout

    public int timeout([int timeout])

#### <a name="parameters"></a>パラメーター

timeout  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public COMVariant value(str value, [COMVariant var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-valuetxt"></a>メソッド valueTxt

    public str valueTxt(str value, [str var])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

IISSessionObject クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-abandon"></a>メソッド abandon

    public void abandon()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-iisstringlist"></a>クラス IISStringList
    class IISStringList extends Object

IISStringList クラスは、インターネット インフォメーション サービス (IIS) によって提供される StringList オブジェクトをラップします。

### <a name="remarks"></a>備考

IISStringList クラスのメソッドと、IIS によって提供される StringList オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISStringList クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISStringList クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                           | 説明                                     |
|----------------------------------|-------------------------------------------------|
| public int count()               |                                                 |
| public COMEnum2Variant getEnum() |                                                 |
| public ComInterface interface()  |                                                 |
| public str item(\[str item\])    |                                                 |
| public void finalize()           |                                                 |
| public void new(COM stringList)  | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-getenum"></a>メソッド getEnum

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public str item([str item])

#### <a name="parameters"></a>パラメーター

項目  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(COM stringList)

#### <a name="parameters"></a>パラメーター

stringList  

## <a name="class-iisvariantdictionary"></a>クラス IISVariantDictionary
    class IISVariantDictionary extends Object

IISVariantDictionary クラスは、インターネット インフォメーション サービス (IIS) によって提供される VariantDictionary オブジェクトをラップします。

### <a name="remarks"></a>備考

IISVariantDictionary クラスのメソッドと、IIS によって提供される VariantDictionary オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISVariantDictionary クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISVariantDictionary クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                     |
|-------------------------------------------------------------|-------------------------------------------------|
| public int count()                                          |                                                 |
| public COMEnum2Variant getEnum()                            |                                                 |
| public ComInterface interface()                             |                                                 |
| public COMVariant item(COMVariant item, \[COMVariant var\]) |                                                 |
| public COM itemObj(str item, \[COM var\])                   |                                                 |
| public str itemTxt(str item, \[str var\])                   |                                                 |
| public str key(str key)                                     |                                                 |
| public void finalize()                                      |                                                 |
| public void remove(str key)                                 |                                                 |
| public void removeAll()                                     |                                                 |
| public void new(COM variantDictionary)                      | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-getenum"></a>メソッド getEnum

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public COMVariant item(COMVariant item, [COMVariant var])

#### <a name="parameters"></a>パラメーター

項目  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-itemobj"></a>メソッド itemObj

    public COM itemObj(str item, [COM var])

#### <a name="parameters"></a>パラメーター

項目  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-itemtxt"></a>メソッド itemTxt

    public str itemTxt(str item, [str var])

#### <a name="parameters"></a>パラメーター

項目  

<!-- -->

var  

#### <a name="return-value"></a>戻り値

### <a name="method-key"></a>メソッド key

    public str key(str key)

#### <a name="parameters"></a>パラメーター

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-remove"></a>メソッド remove

    public void remove(str key)

#### <a name="parameters"></a>パラメーター

キー  

### <a name="method-removeall"></a>メソッド removeAll

    public void removeAll()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(COM variantDictionary)

#### <a name="parameters"></a>パラメーター

variantDictionary  

## <a name="class-iisviewstate"></a>クラス IISViewState
    class IISViewState extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明                                           |
|------------------------------------------------|-------------------------------------------------------|
| public boolean viewStateContains(str key)      |                                                       |
| public str viewStateItem(str key, \[str val\]) |                                                       |
| public void finalize()                         |                                                       |
| public void viewStateDelete(str key)           |                                                       |
| public void new()                              | IISViewState クラスの新しいインスタンスを初期化します。 |

### <a name="method-viewstatecontains"></a>メソッド viewStateContains

    public boolean viewStateContains(str key)

#### <a name="parameters"></a>パラメーター

キー  

#### <a name="return-value"></a>戻り値

### <a name="method-viewstateitem"></a>メソッド viewStateItem

    public str viewStateItem(str key, [str val])

#### <a name="parameters"></a>パラメーター

キー  

<!-- -->

val  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-viewstatedelete"></a>メソッド viewStateDelete

    public void viewStateDelete(str key)

#### <a name="parameters"></a>パラメーター

キー  

### <a name="method-new"></a>メソッド new

IISViewState クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-iiswritecookie"></a>クラス IISWriteCookie
    class IISWriteCookie extends Object

IISWriteCookie クラスは、インターネット インフォメーション サービス (IIS) によって提供される WriteCookie オブジェクトをラップします。

### <a name="remarks"></a>備考

IISWriteCookie クラスのメソッドと、IIS によって提供される WriteCookie オブジェクトのメソッドとの間には、1 対 1 の接続があります。 したがって、IISWriteCookie クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。 IISWriteCookie クラスの使用は、IIS が Finance and Operations インターネット コネクタによって実行されている場合にのみ有効です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                  | 説明                                     |
|-----------------------------------------|-------------------------------------------------|
| public COMEnum2Variant getEnum()        |                                                 |
| public boolean hasKeys()                |                                                 |
| public ComInterface interface()         |                                                 |
| public void new(COM writeCookie)        | Object クラスの新しいインスタンスを初期化します。 |
| public void secure(boolean secure)      |                                                 |
| public void path(str path)              |                                                 |
| public void finalize()                  |                                                 |
| public void domain(str domain)          |                                                 |
| public void expires(COMVariant expires) |                                                 |
| public void item(str item, str value)   |                                                 |

### <a name="method-getenum"></a>メソッド getEnum

    public COMEnum2Variant getEnum()

#### <a name="return-value"></a>戻り値

### <a name="method-haskeys"></a>メソッド hasKeys

    public boolean hasKeys()

#### <a name="return-value"></a>戻り値

### <a name="method-interface"></a>メソッド interface

    public ComInterface interface()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(COM writeCookie)

#### <a name="parameters"></a>パラメーター

writeCookie  

### <a name="method-secure"></a>メソッド secure

    public void secure(boolean secure)

#### <a name="parameters"></a>パラメーター

secure  

### <a name="method-path"></a>メソッド path

    public void path(str path)

#### <a name="parameters"></a>パラメーター

path  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-domain"></a>メソッド domain

    public void domain(str domain)

#### <a name="parameters"></a>パラメーター

domain  

### <a name="method-expires"></a>メソッド expires

    public void expires(COMVariant expires)

#### <a name="parameters"></a>パラメーター

expires  

### <a name="method-item"></a>メソッド item

    public void item(str item, str value)

#### <a name="parameters"></a>パラメーター

項目  

<!-- -->

値  

## <a name="class-image"></a>クラス イメージ
    class Image extends BinData

読み込み、保存、および画像を操作するためのメソッドを提供します。 複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。

### <a name="remarks"></a>備考

次のファイル タイプからイメージ オブジェクトを作成することができます。

-   ラスター (ビットマップ) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif
-   ベクター形式 - .emf および .wmf

複数のイメージを同時に操作する場合は、Imagelist クラスを使用します。 次のファイル タイプからイメージ オブジェクトを作成することができます。

-   ラスター (ビットマップである) 形式 - .bmp、.gif、.jpg、.png、.tiff、.exif
-   ベクター形式 - .emf および .wmf

Finance and Operations では、イメージ クラスはクライアントにバインドされています。 ファイル操作に伴うセキュリティ上のリスクのため、クラスをサーバーから実行できなくなりました。

### <a name="examples"></a>例

次の例では、Picture.jpg の高さをピクセル単位で出力します。

    Image img = new  Image(); 
    img.loadFile(@'C:\MyPictures\Picture.jpg'); 
    print img.height(); 
    pause;

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public int captureScreen(int left, int top, int right, int bottom)                                          | パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。                                           |
| public int captureWindow(int hWnd)                                                                          | パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。                                                              |
| public int clipboardCopy()                                                                                  | イメージをクリップボードにコピーします。                                                                                                             |
| public int clipboardPaste()                                                                                 | システムのクリップボードの内容で既存のイメージを上書きします。                                                                        |
| public int copyImage(Image image)                                                                           | 現在のイメージ オブジェクトをコピーします。                                                                                                              |
| public int createImage(int Width, int Height, int BitsPerPixel)                                             | パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。                                         |
| public int crop(int x, int y, int w, int h)                                                                 | 画像をトリミングします。                                                                                                                              |
| public int displayImage(Int64 HDC, \[int Mode\], \[int Xpos\], \[int Ypos\], \[int Width\], \[int Height\]) | HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。                                                                        |
| public Int64 exportBitmap()                                                                                 | 画像のハンドルを取得します。                                                                                                                  |
| public int flip(FlipType FlipType)                                                                          | 画像を垂直または水平方向に 180 度回転します。                                                                          |
| public container getImageDimensionUnits()                                                                   |                                                                                                                                               |
| public int getPixel(int x, int y)                                                                           | パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。                                                 |
| public int height()                                                                                         | ピクセル単位の画像の高さを取得します。                                                                                                  |
| public container imageInfo()                                                                                | 画像の幅、高さ、色深度を取得します。                                                                                    |
| public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)                           | センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。                                      |
| public int importBitmap(Int64 hBitmap)                                                                      | hBitmap パラメータで指定されたイメージからビットマップをクローンします。                                                                    |
| public int importFileIcon(str fileName)                                                                     | ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。                              |
| public int importIcon(str fileName, int iconIdx)                                                            | Finance and Operations の実行可能ファイルからアイコンへのハンドルを取得します。 このアイコンは、fileName および iconIdx パラメーターで指定します。 |
| public int loadImage(str fileName)                                                                          | fileName パラメーターで指定されたファイルからイメージを読み込みます。                                                                             |
| public int loadResource(int id)                                                                             | Ax32.exe からリソースを読み込みます。                                                                                                               |
| public int promoteColor(int noOfColorBits)                                                                  | 画像の色深度を向上させます。                                                                                                       |
| public int reduceColorOctree(int maxColors)                                                                 | 画像の色深度を減少させます。                                                                                                          |
| public int removeImage()                                                                                    | 画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。                                                                    |
| public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)                         | newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。                                                     |
| public int rotate(RotateType RotateType)                                                                    | 画像を回転します。                                                                                                                            |
| public int saveImage(str fileName, \[ImageSaveType Type\])                                                  | 指定されたファイル名に画像を保存します。                                                                                                   |
| public ImageSaveType saveType(\[ImageSaveType Type\])                                                       | イメージ デコーダを取得または設定します。                                                                                                               |
| public int setPixel(int x, int y, int pixel)                                                                | x と y パラメーターで指定されているピクセルの色を設定します。                                                                     |
| public int transparent(\[boolean Set\], \[int RValue\], \[int GValue\], \[int BValue\])                     | 画像の透明な色を設定します。                                                                                                     |
| public int width()                                                                                          | ピクセル単位の画像の幅を取得します。                                                                                                   |
| ::public static int canLoad(str filename)                                                                   | 画像ファイルが存在し、開くことができるかどうかを決定します。                                                                                    |
| ::public static container loadExt(int idx)                                                                  | Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。                                                 |
| ::public static int resourceType(int resourceIdx)                                                           | 特定のリソースがビットマップかアイコンかを判別します。                                                                              |
| ::public static int rgb(int R, int G, int B)                                                                | RGB 値を ARGB 値に変換します。                                                                                                       |
| ::public static int validResource(int id)                                                                   | id パラメータで指定されたリソースが有効かどうかを判定します。                                                                       |
| public void new(\[AnyType image\], \[int width\], \[int height\])                                           | 新しい画像を作成します                                                                                                                          |
| public void displayOrign(int Xpos, int Ypos)                                                                | オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。                                                                      |
| public void finalize()                                                                                      |                                                                                                                                               |

### <a name="method-capturescreen"></a>メソッド captureScreen

パラメータ リストで指定された座標を使用して、スクリーンからイメージをキャプチャします。

    public int captureScreen(int left, int top, int right, int bottom)

#### <a name="parameters"></a>パラメーター

left  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

戻る  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

権限  
キャプチャする画面の右下隅部分の Y 座標です。

<!-- -->

bottom  
キャプチャする画面の右下隅部分の Y 座標です。

#### <a name="return-value"></a>戻り値

0 は、成功を示します。 その他の値はエラーを示します。

#### <a name="examples"></a>例

次の例では、画面の一部をキャプチャし、test.bmp という名前のファイルに保存します。

    Image img = new Image(); 
    img.captureScreen(0, 0, 100, 100); 
    img.saveFile(@'C:\test.bmp');

### <a name="method-capturewindow"></a>メソッド captureWindow

パラメータとして指定されたハンドルを使用して、ウィンドウをイメージとしてキャプチャします。

    public int captureWindow(int hWnd)

#### <a name="parameters"></a>パラメーター

hWnd  
キャプチャするウィンドウのハンドル。整数として指定する必要があります。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-clipboardcopy"></a>メソッド clipboardCopy

イメージをクリップボードにコピーします。

    public int clipboardCopy()

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、Test.bmp という名前のファイルからコンテンツをコピーします。

    Image img = new Image(); 
    img.loadFile(@'C:\Test.bmp'); 
    img.clipboardCopy(); 
    // Image can now be pasted into an application.

### <a name="method-clipboardpaste"></a>メソッド clipboardPaste

システムのクリップボードの内容で既存のイメージを上書きします。

    public int clipboardPaste()

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

正常に使用されるメソッドについては、クリップボードにコンテンツが必要です。

#### <a name="examples"></a>例

次の例では、以前にクリップボードにコピーされたコンテンツを使用して新しいイメージ ファイルを作成します。

    Image img = new Image();
    // Copy an image to the clipboard before this test 
    img.clipboardPaste(); 
    img.saveFile(@'C:\test.jpg');

### <a name="method-copyimage"></a>メソッド copyImage

現在のイメージ オブジェクトをコピーします。

    public int copyImage(Image image)

#### <a name="parameters"></a>パラメーター

image  
コピーする画像。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、2 つの新しいイメージを作成し、1 つのイメージの内容をもう一方のイメージの内容で上書きします。

    Image img =  new Image(); 
    Image img2 = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    img2.loadFile(@'C:\test2.bmp'); 
    img2.copyImage(img); //img2 now the same as img

### <a name="method-createimage"></a>メソッド createImage

パラメーターで指定された幅、高さ、および色深度を持つ空のビットマップ画像を作成します。

    public int createImage(int Width, int Height, int BitsPerPixel)

#### <a name="parameters"></a>パラメーター

幅  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

<!-- -->

高さ  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

<!-- -->

BitsPerPixel  
画像の色深度。 有効値は 1、4、8、16、24、32 です。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、高さと幅が 16 ピクセル、色深度がピクセルあたり 32 ビットのイメージを作成します。

    int i;
    int j;
    Image image;
    image.createImage(
        Imagelist::smallIconWidth(),
        Imagelist::smallIconHeight(),
        32);
    for (i=0; i < Imagelist::smallIconWidth(); i++)
    {
        for (j=0; j < Imagelist::smallIconHeight(); j++)
        {
            if (i >= Imagelist::smallIconWidth()-2)
            {
                image.setPixel(i, j, WinAPI::RGB2int(0, 255, 255));
            }
            else
            {
                image.setPixel(i, j, WinAPI::imageTransparentColor());
            }
        }
    }

### <a name="method-crop"></a>メソッド crop

画像をトリミングします。

    public int crop(int x, int y, int w, int h)

#### <a name="parameters"></a>パラメーター

x  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

y  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

w  
点 (x、y) からトリミングする領域の高さ。

<!-- -->

h  
点 (x、y) からトリミングする領域の高さ。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-displayimage"></a>メソッド displayImage

HDC パラメーターで指定されたデバイス コンテキストに画像を描画します。

    public int displayImage(Int64 HDC, [int Mode], [int Xpos], [int Ypos], [int Width], [int Height])

#### <a name="parameters"></a>パラメーター

HDC  
オプションのパラメーター。

<!-- -->

モード  
オプションのパラメーター。

<!-- -->

Xpos  
オプションのパラメーター。

<!-- -->

Ypos  
オプションのパラメーター。

<!-- -->

幅  
オプションのパラメーター。

<!-- -->

高さ  
オプションのパラメーター。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-exportbitmap"></a>メソッド exportBitmap

画像のハンドルを取得します。

    public Int64 exportBitmap()

#### <a name="return-value"></a>戻り値

画像のハンドル を表す整数。

#### <a name="examples"></a>例

次の例では、イメージのハンドルを取得し、ハンドルを使用してイメージを複製します。

    { 
        int hdlBitmap; 
        Image img = new Image(); 
        Image img2 = new Image(); 
        img.loadImage(@'C:\MyImage.bmp'); 
        //Set hdlBitmap to handle for MyImage.bmp 
        hdlBitmap = img.exportBitmap(); 
        //Load MyImage.bmp to img2 using image handle 
        if (hdlBitmap) 
        { 
            img2.importBitmap(hdlBitmap); 
        } 
    }

### <a name="method-flip"></a>メソッド flip

画像を垂直または水平方向に 180 度回転します。

    public int flip(FlipType FlipType)

#### <a name="parameters"></a>パラメーター

FlipType  
イメージを反転させる方法を決定する FlipType 列挙。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

FlipType パラメーターの使用可能な値は FlipType システム列挙で使用可能な次の値です。

|     |                    |                                                          |
|-----|--------------------|----------------------------------------------------------|
| 0   | RotateNoneFlipNone | 反転なし                                                  |
| 1   | RotateNoneFlipX    | 画像を水平方向に 180 度回転します。 |
| 2   | RotateNoneFlipX    | 画像を垂直方向に 180 度回転します。   |

### <a name="method-getimagedimensionunits"></a>メソッド getImageDimensionUnits

    public container getImageDimensionUnits()

#### <a name="return-value"></a>戻り値

### <a name="method-getpixel"></a>メソッド getPixel

パラメーターで指定されたポイントで、ピクセルの ARGB カラーの値を取得します。

    public int getPixel(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
ピクセルの垂直座標。

<!-- -->

y  
ピクセルの垂直座標。

#### <a name="return-value"></a>戻り値

ピクセルの ARGB 値である整数 (RGB カラーの 32 ビット表示) 。

### <a name="method-height"></a>メソッド height

ピクセル単位の画像の高さを取得します。

    public int height()

#### <a name="return-value"></a>戻り値

画像の高さをピクセル単位で表す整数。

#### <a name="examples"></a>例

次の例では、test.bmp に含まれるイメージの高さを出力します。

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    print img.height(); 
    pause;

### <a name="method-imageinfo"></a>メソッド imageInfo

画像の幅、高さ、色深度を取得します。

    public container imageInfo()

#### <a name="return-value"></a>戻り値

画像の幅、画像の高さ、およびピクセルあたりのビット数を指定する値を保持するコンテナーです。

#### <a name="examples"></a>例

次の例では、イメージ test.bmp の幅と高さを出力し、ピクセルあたりのビット数で色深度を指定しています。

    Image img = new Image(); 
    container c; 
    img.loadFile(@'C:\Test.bmp'); 
    c = img.imageInfo(); 
    print con2str(c); 
    pause;

### <a name="method-imagespotlight"></a>メソッド imageSpotlight

センター座標 x および y で半径により定義された円内のスポットライト効果を生成します。

    public int imageSpotlight(int x, int y, int radius, int smoothing, int intensity)

#### <a name="parameters"></a>パラメーター

x  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

y  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

radius  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

平滑化  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

<!-- -->

intensity  
周辺のピクセルの強度。 可能な値は 0 ～ 100 (%) までです。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

円内のピクセルは変更されませんが、イメージ内の他のピクセルはその明度を減らすことで暗くなります。

### <a name="method-importbitmap"></a>メソッド importBitmap

hBitmap パラメータで指定されたイメージからビットマップをクローンします。

    public int importBitmap(Int64 hBitmap)

#### <a name="parameters"></a>パラメーター

hBitmap  
複製する画像のハンドルです。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、イメージのハンドルを取得してから、importBitmap メソッドを使用してイメージを複製します。

    { 
        int hdlBitmap; 
        Image img = new Image(); 
        Image img2 = new Image(); 
        img.loadImage(@'C:\MyImage.bmp'); 
        //Set hdlBitmap to handle for MyImage.bmp 
        hdlBitmap = img.exportBitmap(); 
        //Load MyImage.bmp to img2 using image handle 
        if (hdlBitmap) 
        { 
            img2.importBitmap(hdlBitmap); 
        } 
    }

### <a name="method-importfileicon"></a>メソッド importFileIcon

ファイルに使用されているアイコンをコピーすることにより、fileName パラメーターで指定されたファイルからアイコンを作成します。

    public int importFileIcon(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  
アイコンを作成するファイルの名前とパス。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、ファイル test.bmp に使用されているアイコンをコピーします。

    Image img = new Image(); 
    img.importFileIcon(@'C:\test.bmp'); 
    img.clipboardCopy(); 
    // Icon used for test.bmp can now be pasted into an application.

### <a name="method-importicon"></a>メソッド importIcon

Finance and Operations の実行可能ファイルからアイコンへのハンドルを取得します。 このアイコンは、fileName および iconIdx パラメーターで指定します。

    public int importIcon(str fileName, int iconIdx)

#### <a name="parameters"></a>パラメーター

fileName  
指定したファイル内のリソース。

<!-- -->

iconIdx  
指定したファイル内のリソース。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-loadimage"></a>メソッド loadImage

fileName パラメーターで指定されたファイルからイメージを読み込みます。

    public int loadImage(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  
画像を読み込む元となるリソース。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-loadresource"></a>メソッド loadResource

Ax32.exe からリソースを読み込みます。

    public int loadResource(int id)

#### <a name="parameters"></a>パラメーター

id  
読み込むリソースの ID。 リソースの値は、Resources マクロにあります。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="examples"></a>例

次の例では、イメージ リストに 2つ のリソースを追加します。

    #Resource 
    Image img; 
    ImageList imageList; 
    imageList = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    img = new Image(); 
    img.loadResource(#RES_NODE_CLOSED); 
    imageList.add(img); 
    img = new Image(); 
    img.loadResource(#RES_NODE_OPEN); 
    imageList.add(img);

### <a name="method-promotecolor"></a>メソッド promoteColor

画像の色深度を向上させます。

    public int promoteColor(int noOfColorBits)

#### <a name="parameters"></a>パラメーター

noOfColorBits  
イメージのレベルを上げるビット数。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

このメソッドは次を推進します。

-   8 ビット画像を 24、32 ビットに。
-   4 ビット画像を 8、24、32 ビットに。
-   1 ビット画像を 4、8、24、32 ビットに。

#### <a name="examples"></a>例

次の例では、イメージの色深度が 8 ビット以上でない場合は、ピクセルあたり 8 ビットに増やしています。

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    if (conpeek(img.imageInfo(),3) <8) 
    { 
        img.promoteColor(8); 
    }

### <a name="method-reducecoloroctree"></a>メソッド reduceColorOctree

画像の色深度を減少させます。

    public int reduceColorOctree(int maxColors)

#### <a name="parameters"></a>パラメーター

maxColors  
最大色数。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

このメソッドは、他の指示が maxColors パラメーターで指定されていない限り、24 ビット イメージを 8 ビットに、または 8 ビット イメージを 4 ビットに縮小します。 MaxColors パラメーターが 16 以下の場合は、4 ビット イメージが生成されます。 MaxColors が 16 を超える場合は、8 ビット画像が生成されます。

### <a name="method-removeimage"></a>メソッド removeImage

画像に関するデータを削除します。オブジェクトはまだ存在しますが、データを持ちません。

    public int removeImage()

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

### <a name="method-resize"></a>メソッド resize

newWidth および newHeight パラメーターにより指定されたサイズに画像をサイズ変更します。

    public int resize(int newWidth, int newHeight, InterpolationMode InterpolationMode)

#### <a name="parameters"></a>パラメーター

newWidth  
resizing メソッド。

<!-- -->

newHeight  
resizing メソッド。

<!-- -->

InterpolationMode  
resizing メソッド。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

InterpolationMode パラメーターの使用可能な値は InterpolationMode システム列挙で使用可能な次の値です。

|     |                                      |                                                                                                                                                                        |
|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0   | InterpolationModeDefault             | 既定の補間モードを指定します。                                                                                                                              |
| 1   | InterpolationModeLowQuality          | 低品質モードを指定します。                                                                                                                                          |
| 2   | InterpolationModeHighQuality         | 高品質モードを指定します。                                                                                                                                         |
| 3   | InterpolationModeBilinear            | 線状補間を指定します。 事前フィルター処理は行われません。 このメソッドは、画像を元のサイズの 50％ 以下に縮小するのには適していません。                         |
| 4   | InterpolationModeBicubic             | バイキュービック補間を指定します。 事前フィルター処理は行われません。 このメソッドは、画像を元のサイズの 25％ 以下に縮小するのには適していません。                          |
| 5   | InterpolationModeNearestNeighbor     | ニアレストネイバー補間を指定します。                                                                                                                              |
| 6   | InterpolationModeHighQualityBilinear | 高品質な線状補間を指定します。 高品質圧縮を確実に行うため、事前フィルター処理が実行されます。                                                           |
| 7   | InterpolationModeHighQualityBicubic  | 高品質なバイキュービック補間を指定します。 高品質圧縮を確実に行うため、事前フィルター処理が実行されます。 このモードでは、最高品質の変換画像が生成されます。 |

### <a name="method-rotate"></a>メソッド rotate

画像を回転します。

    public int rotate(RotateType RotateType)

#### <a name="parameters"></a>パラメーター

RotateType  
イメージを回転する量。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

RotateType パラメーターの使用可能な値は RotateType システム列挙で使用可能な次の値です。

|     |                    |                          |
|-----|--------------------|--------------------------|
| 0   | RotateNoneFlipNone | 回転なし。             |
| 1   | Rotate90FlipNone   | 90 度回転します。  |
| 2   | Rotate180FlipNone  | 180 度回転します。 |
| 3   | Rotate270FlipNone  | 270 度回転します。 |

### <a name="method-saveimage"></a>メソッド saveImage

指定されたファイル名に画像を保存します。

    public int saveImage(str fileName, [ImageSaveType Type])

#### <a name="parameters"></a>パラメーター

fileName  
ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。

<!-- -->

種類  
ファイル拡張子で指定された形式とは異なる形式でファイルを保存するように指定できる ImageSaveType (オプション)。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

#### <a name="remarks"></a>備考

Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な値です。 たとえば、.jpg ファイルとして test.bmp を保存することができます。

|     |                |
|-----|----------------|
| 0   | \_エクステンションの使用 |
| 1   | BMP            |
| 2   | GIF            |
| 3   | JPG            |
| 4   | PNG            |
| 5   | TIFF           |
| 6   | BMP\_UNCOMP    |
| 7   | TIF\_UNCOMP    |

#### <a name="examples"></a>例

次の例では、画面の一部をファイルにキャプチャし、その画像をロードします。

    Image img = new Image(); 
    img.captureScreen(0, 0, 100, 100); 
    img.saveImage(@'C:\test.bmp'); 
    img.loadFile(@'C:\test.bmp');

### <a name="method-savetype"></a>メソッド saveType

イメージ デコーダを取得または設定します。

    public ImageSaveType saveType([ImageSaveType Type])

#### <a name="parameters"></a>パラメーター

種類  
設定するデコーダのタイプ (オプション)。

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

Type パラメーターの使用可能な値は ImageSaveType システム列挙で使用可能な次の値です。

|     |                |
|-----|----------------|
| 0   | \_エクステンションの使用 |
| 1   | BMP            |
| 2   | GIF            |
| 3   | JPG            |
| 4   | PNG            |
| 5   | TIFF           |
| 6   | BMP\_UNCOMP    |
| 7   | TIF\_UNCOMP    |

### <a name="method-setpixel"></a>メソッド setPixel

x と y パラメーターで指定されているピクセルの色を設定します。

    public int setPixel(int x, int y, int pixel)

#### <a name="parameters"></a>パラメーター

x  
使用する色の ARGB 値。

<!-- -->

y  
使用する色の ARGB 値。

<!-- -->

pixel  
使用する色の ARGB 値。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

RGB カラー値を ARGB 値に変換するには、Image::rgb メソッドを使用します。

### <a name="method-transparent"></a>メソッド transparent

画像の透明な色を設定します。

    public int transparent([boolean Set], [int RValue], [int GValue], [int BValue])

#### <a name="parameters"></a>パラメーター

セット  
設定する色の青の値; オプション。

<!-- -->

RValue  
設定する色の青の値; オプション。

<!-- -->

GValue  
設定する色の青の値; オプション。

<!-- -->

BValue  
設定する色の青の値; オプション。

#### <a name="return-value"></a>戻り値

0 は、成功を示し、それ以外の場合は、失敗を示します。

#### <a name="remarks"></a>備考

入力パラメーターのいずれかがない場合は、画像内の位置 (0, 0) での色が使用されます。 色を指定する場合、パラメーター 2 から 4 を使用すると、RGB カラーとして表記されます。

### <a name="method-width"></a>メソッド width

ピクセル単位の画像の幅を取得します。

    public int width()

#### <a name="return-value"></a>戻り値

画像の幅をピクセル単位で表す整数。

#### <a name="examples"></a>例

次の例では、test.bmp ファイル内のイメージの幅を出力します。

    Image img = new Image(); 
    img.loadFile(@'C:\test.bmp'); 
    print img.width(); 
    pause;

### <a name="method-canload"></a>メソッド canLoad

画像ファイルが存在し、開くことができるかどうかを決定します。

    public static int canLoad(str filename)

#### <a name="parameters"></a>パラメーター

filename  
確認するファイルの名前とパス。

#### <a name="return-value"></a>戻り値

画像が検索され、開くことができる場合は 1、それ以外の場合、0 です。

### <a name="method-loadext"></a>メソッド loadExt

Image クラスでサポートされているファイル形式の拡張機能の一覧を取得します。

    public static container loadExt(int idx)

#### <a name="parameters"></a>パラメーター

idx  

#### <a name="return-value"></a>戻り値

サポートされているファイル形式の一覧を保持するコンテナーです。

### <a name="method-resourcetype"></a>メソッド resourceType

特定のリソースがビットマップかアイコンかを判別します。

    public static int resourceType(int resourceIdx)

#### <a name="parameters"></a>パラメーター

resourceIdx  
読み込むリソースの ID。

#### <a name="return-value"></a>戻り値

画像がビットマップの場合は 0、アイコンの場合は 1 です。

#### <a name="remarks"></a>備考

リソースの値は、Resources マクロにあります。

#### <a name="examples"></a>例

次の例では、リソース 3020 がアイコンかビットマップかどうかをテストします。

    #Resource 
    print Image::resourceType(3020); 
    pause;

### <a name="method-rgb"></a>メソッド rgb

RGB 値を ARGB 値に変換します。

    public static int rgb(int R, int G, int B)

#### <a name="parameters"></a>パラメーター

R  
色の青の値。

<!-- -->

G  
色の青の値。

<!-- -->

B  
色の青の値。

#### <a name="return-value"></a>戻り値

パラメーターで指定された色の ARGB 値を表す整数。

### <a name="method-validresource"></a>メソッド validResource

id パラメータで指定されたリソースが有効かどうかを判定します。

    public static int validResource(int id)

#### <a name="parameters"></a>パラメーター

id  
チェックするリソースの ID。

#### <a name="return-value"></a>戻り値

ID が有効な場合、0 です。

### <a name="method-new"></a>メソッド new

新しい画像を作成します

    public void new([AnyType image], [int width], [int height])

#### <a name="parameters"></a>パラメーター

image  
ピクセル単位の画像の高さ (オプション)。

<!-- -->

width  
ピクセル単位の画像の高さ (オプション)。

<!-- -->

height  
ピクセル単位の画像の高さ (オプション)。

#### <a name="remarks"></a>備考

パラメーターを指定する必要はありませんが、イメージの内容とサイズを指定することができます。 画像パラメーターについては、ファイル名および場所、リソース、配列での特定の画像、または別の画像オブジェクトを指定できます。

#### <a name="examples"></a>例

次の例は、新しいイメージ オブジェクトの既存のコンテンツをオプションで指定する方法を示しています。

    Image img1 = new Image(@"C:\MyPicture.jpg", 100, 100); 
    Image img2 = new Image(121,100, 100); // Uses resource 121 in Ax32.exe 
    Image img4 = new Image(img1, 200, 200);

### <a name="method-displayorign"></a>メソッド displayOrign

オリジナルの発注元 (0, 0) から、オフセット (X, Y) を指定できるようにします。

    public void displayOrign(int Xpos, int Ypos)

#### <a name="parameters"></a>パラメーター

Xpos  
原点に対する新しい Y (垂直) 座標。

<!-- -->

Ypos  
原点に対する新しい Y (垂直) 座標。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-imagelist"></a>クラス Imagelist
    class Imagelist extends BinData

Imagelist クラスを使用すると、イメージの一覧を操作できます。

### <a name="remarks"></a>備考

1 つの画像を操作するには、イメージ クラスを使用します。

### <a name="examples"></a>例

次の例では、イメージ リストを作成し、Shell32.dll ファイルにアイコンを追加します。 一覧の 4 番目のメンバーを削除します。

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    list.remove(4); 
    print list.count(); 
    pause;

### <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                                                                                                        |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| public int add(Image image)                                                    | イメージ リストに新しい画像を追加します。                                                                                                |
| public boolean autoResize(\[boolean value\])                                   | 新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。                                   |
| public int clear()                                                             | イメージ リストからすべての画像を削除します。                                                                                            |
| public int count()                                                             | 画像リスト内のイメージの数を取得します。                                                                                   |
| public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)             | イメージのドラッグを開始します。                                                                                                          |
| public boolean dragEnd()                                                       | ドラッグ操作を終了します。                                                                                                             |
| public boolean dragEnter(int hWnd, int x, int y)                               | ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。 |
| public boolean dragLeave(int hWnd)                                             | 指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。                                           |
| public boolean dragMove(int x, int y)                                          | ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。                                                            |
| public boolean dragShowImage(boolean show)                                     | ドラッグされている画像の表示と非表示を切り替えます。                                                                                    |
| public int height()                                                            | イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。                                                                  |
| public int loadIcons(str moduleName)                                           | イメージ リストに、指定されたリソースからアイコンを読み込みます。                                                                       |
| public int remove(int imageIdx)                                                | イメージ リストから画像を削除します。                                                                                               |
| public int replace(int imageIdx, Image image)                                  | リスト内の既存の画像を置き換えます。                                                                                            |
| public boolean setOverlayImage(int imageIdx, int overlayIdx)                   | オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。                                                                       |
| public int width()                                                             | イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。                                                                   |
| ::public static int iconHeight()                                               | 標準アイコンの高さのシステム メトリックを取得します。                                                                    |
| ::public static int iconWidth()                                                | 標準アイコンの幅のシステム メトリックを取得します。                                                                     |
| ::public static int smallIconHeight()                                          | 小さなアイコンの高さのシステム メトリックを取得します。                                                                       |
| ::public static int smallIconWidth()                                           | 小さなアイコンの幅のシステム メトリックを取得します。                                                                        |
| public void maskColor(int Color)                                               | マスキング色を設定します。                                                                                                            |
| public void draw(int HDC, int imageIdx, int x, int y, \[boolean transparent\]) | 指定されたデバイス コンテキストで画像リスト項目を描画します。                                                                          |
| public void finalize()                                                         |                                                                                                                                    |
| public void new(int cx, int cy, \[boolean transparent\])                       | 画像を保持する新しい空のリストを作成します。                                                                                           |

### <a name="method-add"></a>メソッド add

イメージ リストに新しい画像を追加します。

    public int add(Image image)

#### <a name="parameters"></a>パラメーター

image  
リストに追加する新しい画像。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

#### <a name="remarks"></a>備考

autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。

#### <a name="examples"></a>例

次の例では、新しいイメージ リストを作成し、3 つのイメージを追加します。

    ImageList list = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    list.add(new Image(3104)); 
    list.add(new Image(1097)); 
    list.add(new Image(1200)); 
    // Prints 3 
    print list.count(); 
    pause;

### <a name="method-autoresize"></a>メソッド autoResize

新しいイメージを自動的にサイズ変更するかどうかを決定するブール値の autoResize フラグを設定します。

    public boolean autoResize([boolean value])

#### <a name="parameters"></a>パラメーター

値  
autoResize フラグが設定されているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

autoResize フラッグが true に設定されている場合、リストに追加する任意の画像サイズは、画像リストの作成時に指定された分析コードに自動的に再調整されます。

### <a name="method-clear"></a>メソッド clear

イメージ リストからすべての画像を削除します。

    public int clear()

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

### <a name="method-count"></a>メソッド count

画像リスト内のイメージの数を取得します。

    public int count()

#### <a name="return-value"></a>戻り値

リスト内の画像の数を表す整数。

#### <a name="examples"></a>例

次の例では、イメージ リストを作成し、shell.dll ファイルからアイコンを読み込み、リスト内のイメージの数を出力します。

    Imagelist list; 
    int       counter; 
    list = new Imagelist( 
       Imagelist::iconWidth(), 
       Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    pause;

### <a name="method-dragbegin"></a>メソッド dragBegin

イメージのドラッグを開始します。

    public boolean dragBegin(int imageIdx, int hotSpotX, int hotSpotY)

#### <a name="parameters"></a>パラメーター

imageIdx  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

<!-- -->

hotSpotX  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

<!-- -->

hotSpotY  
画像の左上隅を基準とした、ドラッグ位置の Y 座標。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1 です。

#### <a name="remarks"></a>備考

残りのドラッグ操作は、dragEnter、dragMove、dragLeave、dragEnd の各メソッドで指定します。

### <a name="method-dragend"></a>メソッド dragEnd

ドラッグ操作を終了します。

    public boolean dragEnd()

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1、それ以外の場合は 0 です。

#### <a name="remarks"></a>備考

残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragLeave の各メソッドで指定します。

### <a name="method-dragenter"></a>メソッド dragEnter

ドラッグ操作中に指定されたウィンドウの更新をロックし、ウィンドウの指定された位置にドラッグ イメージを表示します。

    public boolean dragEnter(int hWnd, int x, int y)

#### <a name="parameters"></a>パラメーター

hWnd  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

x  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

y  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1、それ以外の場合は 0 です。

#### <a name="remarks"></a>備考

ドラッグ操作を開始するには、dragBegin メソッドを呼び出します。 残りのドラッグ操作は、dragMove、dragLeave、dragEnd の各メソッドで指定します。

### <a name="method-dragleave"></a>メソッド dragLeave

指定したウィンドウのロックを解除し、ドラッグ イメージを非表示にして、ウィンドウを更新します。

    public boolean dragLeave(int hWnd)

#### <a name="parameters"></a>パラメーター

hWnd  
ドラッグ イメージを所有するウィンドウのハンドルです。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1、それ以外の場合は 0 です。

#### <a name="remarks"></a>備考

残りのドラッグ操作は、dragBegin、dragEnter、dragMove、dragEnd の各メソッドで指定します。

### <a name="method-dragmove"></a>メソッド dragMove

ドラッグ アンド ドロップ操作中にドラッグされているイメージを移動します。

    public boolean dragMove(int x, int y)

#### <a name="parameters"></a>パラメーター

x  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

<!-- -->

y  
ウィンドウの左上隅を基準とした、ドラッグ アイコンの表示位置の Y 座標。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1、それ以外の場合は 0 です。

#### <a name="remarks"></a>備考

ドラッグ操作を開始するには、dragBegin メソッドを呼び出してから dragEnter メソッドを呼び出します。 残りのドラッグ操作は、dragLeave メソッドおよび dragEnd メソッドで指定します。

### <a name="method-dragshowimage"></a>メソッド dragShowImage

ドラッグされている画像の表示と非表示を切り替えます。

    public boolean dragShowImage(boolean show)

#### <a name="parameters"></a>パラメーター

show  
画像を表示するかどうかを指定する値。

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

イメージ リスト内のイメージの高さ (ピクセル単位) を取得します。

    public int height()

#### <a name="return-value"></a>戻り値

画像の高さをピクセル単位で表す整数。

#### <a name="remarks"></a>備考

リスト内の画像の高さは、リストをインスタンス化するときに設定されます。

#### <a name="examples"></a>例

次の例では、イメージ リストを作成し、イメージの高さと幅を iconWidth メソッドと iconHeight メソッドで指定された寸法に設定します。 一覧内のイメージの高さを出力します。

    Imagelist list; 
    list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight()); 
    print list.height();   
    pause;

### <a name="method-loadicons"></a>メソッド loadIcons

イメージ リストに、指定されたリソースからアイコンを読み込みます。

    public int loadIcons(str moduleName)

#### <a name="parameters"></a>パラメーター

moduleName  
イメージの読み込み元ファイルの名前。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

#### <a name="examples"></a>例

次の例では、イメージのリストを作成し、shell32.dll ファイルに含まれるイメージをロードします。

    Imagelist list; 
    list = new Imagelist(Imagelist::iconWidth(),Imagelist::iconHeight()); 
    list.loadIcons('shell32.dll');

### <a name="method-remove"></a>メソッド remove

イメージ リストから画像を削除します。

    public int remove(int imageIdx)

#### <a name="parameters"></a>パラメーター

imageIdx  
一覧から削除する画像の位置。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

#### <a name="examples"></a>例

次の例では、イメージ リストを作成し、アイコンを shell32.dll ファイルに追加して、リストの 4 番目のメンバーを削除します。

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.loadIcons('shell32.dll'); 
    print list.count(); 
    list.remove(4); 
    print list.count(); 
    pause;

### <a name="method-replace"></a>メソッド replace

リスト内の既存の画像を置き換えます。

    public int replace(int imageIdx, Image image)

#### <a name="parameters"></a>パラメーター

imageIdx  
既存のイメージを置き換えるために使用するイメージ。

<!-- -->

image  
既存のイメージを置き換えるために使用するイメージ。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合、0 です。

### <a name="method-setoverlayimage"></a>メソッド setOverlayImage

オーバーレイ マスクとして使用する画像の一覧に、画像を追加します。

    public boolean setOverlayImage(int imageIdx, int overlayIdx)

#### <a name="parameters"></a>パラメーター

imageIdx  
オーバーレイ マスクの 1 から始まるインデックス。

<!-- -->

overlayIdx  
オーバーレイ マスクの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

メソッドが成功した場合は 1 です。

#### <a name="examples"></a>例

次の例では、3 つのイメージを持つイメージ リストを作成し、最後のイメージをオーバーレイ マスクとして設定します。

    Imagelist list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight() ); 
    list.add(new Image(824)); // Image 0 
    list.add(new Image(815)); // Image 1 
    list.add(new Image(936)); //Image 2 
    list.setOverlayImage (2,1);

### <a name="method-width"></a>メソッド width

イメージ リスト内のイメージの幅 (ピクセル単位) を取得します。

    public int width()

#### <a name="return-value"></a>戻り値

画像の幅をピクセル単位で表す整数。

#### <a name="remarks"></a>備考

リスト内の画像の幅は、リストをインスタンス化するときに設定されます。

#### <a name="examples"></a>例

次の例では、アイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。

    Imagelist list; 
    list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight()); 
    print list.width();   
    pause;

### <a name="method-iconheight"></a>メソッド iconHeight

標準アイコンの高さのシステム メトリックを取得します。

    public static int iconHeight()

#### <a name="return-value"></a>戻り値

標準アイコンの高さを表す整数。

#### <a name="examples"></a>例

次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。

    ImageList list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight());

### <a name="method-iconwidth"></a>メソッド iconWidth

標準アイコンの幅のシステム メトリックを取得します。

    public static int iconWidth()

#### <a name="return-value"></a>戻り値

標準アイコンの幅を表す整数。

#### <a name="examples"></a>例

次の例では、イメージのリストを作成し、標準のアイコンの幅と高さに設定します。

    ImageList list = new Imagelist( 
        Imagelist::iconWidth(), 
        Imagelist::iconHeight());

### <a name="method-smalliconheight"></a>メソッド smallIconHeight

小さなアイコンの高さのシステム メトリックを取得します。

    public static int smallIconHeight()

#### <a name="return-value"></a>戻り値

小さなアイコンの高さを表す整数。

#### <a name="examples"></a>例

次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの高さをリストに出力します。

    Imagelist list = new Imagelist( 
        Imagelist::smallIconWidth(), 
        Imagelist::smallIconHeight()); 
    print list.height();   
    pause;

### <a name="method-smalliconwidth"></a>メソッド smallIconWidth

小さなアイコンの幅のシステム メトリックを取得します。

    public static int smallIconWidth()

#### <a name="return-value"></a>戻り値

小さなアイコンの幅を表す整数。

#### <a name="examples"></a>例

次の例では、小さなアイコンの標準的な高さと幅を持つイメージ リストを作成し、イメージの幅をリストに出力します。

    Imagelist list = new Imagelist( 
       Imagelist::smallIconWidth(), 
       Imagelist::smallIconHeight()); 
    print list.width();   
    pause;

### <a name="method-maskcolor"></a>メソッド maskColor

マスキング色を設定します。

    public void maskColor(int Color)

#### <a name="parameters"></a>パラメーター

色  
ARGB 値としての色。

### <a name="method-draw"></a>メソッド draw

指定されたデバイス コンテキストで画像リスト項目を描画します。

    public void draw(int HDC, int imageIdx, int x, int y, [boolean transparent])

#### <a name="parameters"></a>パラメーター

HDC  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

imageIdx  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

x  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

y  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

<!-- -->

透明  
背景の色に関係なく、マスクを使用して、画像が透過的に描画されているかどうかを示すブール値; オプション。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

画像を保持する新しい空のリストを作成します。

    public void new(int cx, int cy, [boolean transparent])

#### <a name="parameters"></a>パラメーター

cx  

<!-- -->

cy  

<!-- -->

透明  

#### <a name="remarks"></a>備考

autoResize メソッドを使用すると、リストに追加するときにイメージのサイズを自動的に変更することができます。

#### <a name="examples"></a>例

次の例では、標準アイコンの幅と高さの項目を保持するイメージ リストを作成します。

    Imagelist list; 
    list = new Imagelist( 
       Imagelist::iconWidth(), 
       Imagelist::iconHeight());

## <a name="class-importtabledatainfo"></a>クラス ImportTableDataInfo
    class ImportTableDataInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明                                     |
|---------------------------------------------------------|-------------------------------------------------|
| public int addColumnData(str szColName, AnyType colVal) |                                                 |
| public int copyDataRow()                                |                                                 |
| public void new(int usTableId)                          | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-addcolumndata"></a>メソッド addColumnData

    public int addColumnData(str szColName, AnyType colVal)

#### <a name="parameters"></a>パラメーター

szColName  

<!-- -->

colVal  

#### <a name="return-value"></a>戻り値

### <a name="method-copydatarow"></a>メソッド copyDataRow

    public int copyDataRow()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(int usTableId)

#### <a name="parameters"></a>パラメーター

usTableId  

## <a name="class-importtableschemainfo"></a>クラス ImportTableSchemaInfo
    class ImportTableSchemaInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                             | 説明                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------|
| public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd) |                                                 |
| public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)        |                                                 |
| public int hasEqualityCriteria(boolean fHasEqualityCriteria)                       |                                                 |
| public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)                 |                                                 |
| public void new(int usTableId)                                                     | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-addcolumninfo"></a>メソッド addColumnInfo

    public int addColumnInfo(str szColName, Types eColType, int eColRole, int lColOrd)

#### <a name="parameters"></a>パラメーター

szColName  

<!-- -->

eColType  

<!-- -->

eColRole  

<!-- -->

lColOrd  

#### <a name="return-value"></a>戻り値

### <a name="method-addcolumnmapping"></a>メソッド addColumnMapping

    public int addColumnMapping(str szRefRecIdColName, str szRefTableIdColName)

#### <a name="parameters"></a>パラメーター

szRefRecIdColName  

<!-- -->

szRefTableIdColName  

#### <a name="return-value"></a>戻り値

### <a name="method-hasequalitycriteria"></a>メソッド hasEqualityCriteria

    public int hasEqualityCriteria(boolean fHasEqualityCriteria)

#### <a name="parameters"></a>パラメーター

fHasEqualityCriteria  

#### <a name="return-value"></a>戻り値

### <a name="method-shreddedmetadatatable"></a>メソッド shreddedMetadataTable

    public int shreddedMetadataTable(boolean fIsShreddedMetadataTable)

#### <a name="parameters"></a>パラメーター

fIsShreddedMetadataTable  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(int usTableId)

#### <a name="parameters"></a>パラメーター

usTableId  

## <a name="class-infopart"></a>クラス InfoPart
    class InfoPart extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                   | 説明                                                                                                                               |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str caption(\[str value\])        | コントロールのキャプションを取得または設定します。                                                                                                   |
| public str changedBy(\[str value\])      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\]) | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])   |                                                                                                                                           |
| public str name(\[str value\])           | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])       |                                                                                                                                           |
| public str query(\[str value\])          |                                                                                                                                           |
| public void new()                        | InfoPart クラスの新しいインスタンスを初期化します。                                                                                         |

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-query"></a>メソッド query

    public str query([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

InfoPart クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-infopartfield"></a>クラス InfoPartField
    class InfoPartField extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public str dataField(\[str value\])               |                                                                                                                                           |
| public str dataMethod(\[str value\])              |                                                                                                                                           |
| public str dataSource(\[str value\])              | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public str label(\[str value\])                   | コントロールのラベルを取得または設定します。                                                                                                     |
| public boolean manualRetrieval(\[boolean value\]) |                                                                                                                                           |
| public str name(\[str value\])                    | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int style(\[int value\])                   |                                                                                                                                           |
| public void new()                                 | InfoPartField クラスの新しいインスタンスを初期化します。                                                                                    |

### <a name="method-datafield"></a>メソッド dataField

    public str dataField([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public str dataSource([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-manualretrieval"></a>メソッド manualRetrieval

    public boolean manualRetrieval([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

InfoPartField クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-infopartgroup"></a>クラス InfoPartGroup
    class InfoPartGroup extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                         | 説明                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str caption(\[str value\])                              | コントロールのキャプションを取得または設定します。                                                                                                      |
| public str dataGroup(\[str value\])                            |                                                                                                                                               |
| public str dataSource(\[str value\])                           | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                      |
| public int labelPosition(\[int value\])                        |                                                                                                                                               |
| public str name(\[str value\])                                 | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean repeating(\[boolean value\])                    |                                                                                                                                               |
| public int rowCountWhenSmall(\[int value\], \[AutoMode mode\]) |                                                                                                                                               |
| public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])       |                                                                                                                                               |
| public int rowCountWhenSmallValue(\[int value\])               |                                                                                                                                               |
| public boolean showCaption(\[boolean value\])                  |                                                                                                                                               |
| public boolean showLabels(\[boolean value\])                   |                                                                                                                                               |
| public int showWhenPartSize(\[int value\])                     |                                                                                                                                               |
| public boolean verticalSpacing(\[boolean value\])              |                                                                                                                                               |
| public void new()                                              | InfoPartGroup クラスの新しいインスタンスを初期化します。                                                                                        |

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-datagroup"></a>メソッド dataGroup

    public str dataGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public str dataSource([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-repeating"></a>メソッド repeating

    public boolean repeating([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rowcountwhensmall"></a>メソッド rowCountWhenSmall

    public int rowCountWhenSmall([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rowcountwhensmallmode"></a>メソッド rowCountWhenSmallMode

    public AutoMode rowCountWhenSmallMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rowcountwhensmallvalue"></a>メソッド rowCountWhenSmallValue

    public int rowCountWhenSmallValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showcaption"></a>メソッド showCaption

    public boolean showCaption([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabels"></a>メソッド showLabels

    public boolean showLabels([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showwhenpartsize"></a>メソッド showWhenPartSize

    public int showWhenPartSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public boolean verticalSpacing([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

InfoPartGroup クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-infopartlayout"></a>クラス InfoPartLayout
    class InfoPartLayout extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                             |
|----------------------------------------------|---------------------------------------------------------|
| public boolean showMore(\[boolean value\])   |                                                         |
| public str showMoreDataSource(\[str value\]) |                                                         |
| public void new()                            | InfoPartLayout クラスの新しいインスタンスを初期化します。 |

### <a name="method-showmore"></a>メソッド showMore

    public boolean showMore([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showmoredatasource"></a>メソッド showMoreDataSource

    public str showMoreDataSource([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

InfoPartLayout クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-initialqueryparameter"></a>クラス InitialQueryParameter
    class InitialQueryParameter extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                       | 説明                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| public boolean applyQuery(FormDataSource datasource)                                                         |                                                                |
| public str dataSourceName(\[str dataSourceName\])                                                            |                                                                |
| public str modeledQueryName(\[str modeledQueryName\])                                                        |                                                                |
| public Query query(\[Query query\])                                                                          |                                                                |
| ::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\]) |                                                                |
| ::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])                     |                                                                |
| public void finalize()                                                                                       |                                                                |
| public void new()                                                                                            | InitialQueryParameter クラスの新しいインスタンスを初期化します。 |

### <a name="method-applyquery"></a>メソッド applyQuery

    public boolean applyQuery(FormDataSource datasource)

#### <a name="parameters"></a>パラメーター

datasource  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcename"></a>メソッド dataSourceName

    public str dataSourceName([str dataSourceName])

#### <a name="parameters"></a>パラメーター

dataSourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-modeledqueryname"></a>メソッド modeledQueryName

    public str modeledQueryName([str modeledQueryName])

#### <a name="parameters"></a>パラメーター

modeledQueryName  

#### <a name="return-value"></a>戻り値

### <a name="method-query"></a>メソッド query

    public Query query([Query query])

#### <a name="parameters"></a>パラメーター

クエリ  

#### <a name="return-value"></a>戻り値

### <a name="method-createbymodeledqueryname"></a>メソッド createByModeledQueryName

    public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, [str dataSourceName])

#### <a name="parameters"></a>パラメーター

modeledQueryName  

<!-- -->

dataSourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-createbyquery"></a>メソッド createByQuery

    public static InitialQueryParameter createByQuery(Query query, [str dataSourceName])

#### <a name="parameters"></a>パラメーター

クエリ  

<!-- -->

dataSourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

InitialQueryParameter クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-interoppermission"></a>クラス InteropPermission
    class InteropPermission extends CodeAccessPermission

InteropPermission クラスは、アンマネージド コードとマネージド コードを呼び出す機能を制御します。

### <a name="remarks"></a>備考

InteropPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。 アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API を実行する前に、対応する CodeAccessPermission::demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。 次のいずれかの方法でサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。

### <a name="examples"></a>例

次のコード例は、InteropPermission クラスの新しいインスタンスを示しています。 assert メソッドが呼び出され、コードが、Microsoft Windows ダイナミックリンク ライブラリ (DLL) と通信する機能を提供する DLL クラスをインスタンス化できることが宣言されます。

    server static void main(Args args) 
    { 
        InteropPermission _perm; 
        DLL _dll; 
        _perm = new InteropPermission(InteropKind::DllInterop); 
        _perm.assert(); 
        // Invoke the protected API. 
        _dll = new DLL('cfx2032.dll'); 
        // Optionally, call revertAssert() to limit the scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a>方法

| 方法                                                 | 説明                                                                        |
|--------------------------------------------------------|------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。                 |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。 |
| public void new(InteropKind kind)                      | InteropPermission クラスの新しいインスタンスを作成します。                            |

### <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

    public CodeAccessPermission copy()

#### <a name="return-value"></a>戻り値

現在のアクセス許可オブジェクトのコピーです。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「メソッドのコピー」を参照してください。

### <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a>パラメーター

target  
CodeAccessPermission クラス オブジェクト。

#### <a name="return-value"></a>戻り値

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「isSubsetOf メソッド」を参照してください。

### <a name="method-new"></a>メソッド new

InteropPermission クラスの新しいインスタンスを作成します。

    public void new(InteropKind kind)

#### <a name="parameters"></a>パラメーター

kind  
マネージドまたはアンマネージド コードへのアクセスを指定する InteropKind システム列挙値です。

#### <a name="examples"></a>例

次のコード例は、Win32 DLL へのアクセス許可を指定する InteropPermission クラスの新しいインスタンスを示しています。

    server static void main(Args args) 
    { 
        InteropPermission _perm; 
        _perm = new InteropPermission(InteropKind::DllInterop); 
    }

## <a name="class-io"></a>クラス入出力
    class Io extends Object

Io クラスは、外部ファイルにアクセスするための、ファイル固有の Io クラスの基本クラスとして機能します。

### <a name="remarks"></a>備考

基本的な Io クラスには、実際のデータ入出力機能はありませんが、形式固有の Io クラスの基本クラスとして動作します。 ここでは、すべての Io クラスに共通するメソッドについて説明します。 形式固有の機能およびメンバー機能の動作については、各 I/O クラスのドキュメントを参照してください。 異なるフォーマットの外部ファイルの読み書きをサポートするため、MorphX はコンマで区切られたファイル、コンマで区切られた 7 ビット ファイル、バイナリ ファイル、およびプレーン テキスト ファイルのためのさまざまな Io クラスを備えています。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| public str inFieldDelimiter(\[str value\])   | \*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。                                    |
| public str inRecordDelimiter(\[str value\])  | 完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。  |
| public int inRecordLength(\[int value\])     | ファイル内の各レコードを読み取る文字数を取得または設定します。                                                     |
| public str outFieldDelimiter(\[str value\])  | レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。          |
| public str outRecordDelimiter(\[str value\]) | 出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。 |
| public container read()                      | Io オブジェクトから次の完全なレコードを読み取ります。                                                                               |
| public IO\_Status status()                   | Io オブジェクトで実行された最後の操作のステータスを取得します。                                                       |
| public boolean write(VarArg values)          | 単純型の値を記述します。                                                                                              |
| public boolean writeExp(container data)      | コンテナのコンテンツをそのファイルに記述します。                                                                               |
| public void finalize()                       | ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。                                                  |
| public void new(str filename, str mode)      | Io クラスの新しいインスタンスを作成します。                                                                                      |

### <a name="method-infielddelimiter"></a>メソッド inFieldDelimiter

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。

### <a name="method-inrecorddelimiter"></a>メソッド inRecordDelimiter

完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

完全なレコードが読み込まれたかどうかを示す文字。

#### <a name="remarks"></a>備考

標準的なテキストについては、区切り記号は改行文字です。

### <a name="method-inrecordlength"></a>メソッド inRecordLength

ファイル内の各レコードを読み取る文字数を取得または設定します。

    public int inRecordLength([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ファイル内の各レコードを読み取る文字数。

#### <a name="remarks"></a>備考

固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。 レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。 固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。 inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。 レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。

### <a name="method-outfielddelimiter"></a>メソッド outFieldDelimiter

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。

### <a name="method-outrecorddelimiter"></a>メソッド outRecordDelimiter

出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

出力ファイルに書き込まれる文字のシーケンス。

#### <a name="remarks"></a>備考

標準的なテキスト ファイルについては、区切り記号は改行文字です。

### <a name="method-read"></a>メソッド read

Io オブジェクトから次の完全なレコードを読み取ります。

    public container read()

#### <a name="return-value"></a>戻り値

入出力オブジェクトから次の完全なレコードを保持するコンテナーです。

#### <a name="remarks"></a>備考

次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。 レコードはコンテナーとして返されます。 コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。 それぞれの特殊な Io クラスは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定を使用し、最も一般的な形式の入出力を可能にします。 目的の形式をサポートするために、これらの設定の調整が生じる場合があります。

#### <a name="examples"></a>例

このメソッドは、run メソッドの使用方法を示します。 ただし、次の例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。

    static void Job1(Args _args) 
    { 
        FileIoPermission _perm; 
        AsciiIo myfileio; 
        Container c; 
        _perm = new FileIoPermission("myfile.txt","r"); 
        myfileio = new AsciiIo("myfile.txt","r"); 
        while(myfileio.status()==IO_Status::OK) 
        { 
            c = myfileio.read(); 
            // ...do something with the container 
        } 
    }

### <a name="method-status"></a>メソッド status

Io オブジェクトで実行された最後の操作のステータスを取得します。

    public IO_Status status()

#### <a name="return-value"></a>戻り値

IO\_Status システム列挙値としての最後の操作の状態。

#### <a name="remarks"></a>備考

返される可能性のある IO\_Status 値の範囲はクラスによって異なります。

#### <a name="examples"></a>例

    static void myExample(Args _args) 
    { 
        Io myIo; 
        //.. create io object and perform some operations 
        if (myIo.status()==IO_Status::OK) 
        { 
            // ...go ahead - last operation was successful 
        } 
    }

### <a name="method-write"></a>メソッド write

単純型の値を記述します。

    public boolean write(VarArg values)

#### <a name="parameters"></a>パラメーター

値  
単純型は、文字列、整数、実数、列挙型、日付です。

#### <a name="return-value"></a>戻り値

書き込み操作が成功する場合は true。それ以外の場合は false。 書き込みが失敗した場合は、ステータス メソッドがその原因を調べることができます。

#### <a name="remarks"></a>備考

このメソッドは、可変数の引数を受け入れます。 指定された各値は、フィールドとして出力レコードに配置されます。 最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。 フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。 各レコードは、outRecordDelimiter 方法で区切られます。 完全なコンテナーを書き込むには、writeExp メソッドを使用します。

### <a name="method-writeexp"></a>メソッド writeExp

コンテナのコンテンツをそのファイルに記述します。

    public boolean writeExp(container data)

#### <a name="parameters"></a>パラメーター

データ  
レコードのデータを含むコンテナー。

#### <a name="return-value"></a>戻り値

操作が成功した場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

このメソッドが false を返す場合、ステータス メソッドで原因を確認します。 コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。 フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。 レコード区切りは outRecordDelimiter メソッドで定義されます。

#### <a name="examples"></a>例

    static void testMethod(Args _args) 
    { 
        FileIOPermission _perm; 
        container c; 
        CommaIo myfile; 
        _perm = new FileIOPermission("myfile.txt","w"); 
        _perm.assert(); 
        myfile = new CommaIo("myfile.txt","w"); 
        // Assign the entries in the container according to record layout. 
        c = [1,"MyText",1.324,"Last field"]; 
        // write this record according to file format (record/field delimiters). 
        myfile.writeExp(c); 
    }

### <a name="method-finalize"></a>メソッド finalize

ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。

    public void finalize()

#### <a name="remarks"></a>備考

オブジェクトは、通常、スコープから離れることによって確定されるため、確定は通常は直接呼び出されません。 記述された出力はオブジェクトの終了前は無効です。

### <a name="method-new"></a>メソッド new

Io クラスの新しいインスタンスを作成します。

    public void new(str filename, str mode)

#### <a name="parameters"></a>パラメーター

filename  
ファイルを開く必要があるモード。

<!-- -->

モード  
ファイルを開く必要があるモード。

#### <a name="remarks"></a>備考

mode パラメーターは、次のモードのいずれかになります。

-   R – 読み取り
-   W – 書き込み
-   A – 追加 (意味 W)
-   T – 翻訳 (テキスト)
-   B – バイナリ

ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 . ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。

#### <a name="examples"></a>例

この例では、Io クラスを使用して ExampleFile に書き込みます。

    void IoExample() 
    { 
        Io io; 
        container con; 
        FileIoPermission perm; 
        #define.ExampleFile(@"c:\test.txt") 
        #define.ExampleOpenMode("w") 
        // Grants permission to execute the 
        // Io.new method. 
        // Io.new runs under code access security. 
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        io = new Io(#ExampleFile, #ExampleOpenMode); 
        if (io != null) 
        { 
            io.write("Test"); 
        } 
        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }



