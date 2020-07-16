---
title: MapiMessage クラス
description: このトピックでは、MapiMessage クラスについて説明します。
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
ms.openlocfilehash: 1f00f6d5bbd880e8f5c8ff69ab94eaeee85ae948
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502579"
---
# <a name="class-mapimessage"></a>クラス MapiMessage

[!include [banner](../../includes/banner.md)]

```xpp
class MapiMessage extends Object
```

MapiMessage クラスには、MAPI システムから送受信されるメッセージが含まれています。 メッセージには、件名、テキスト、受信者情報、および添付ファイル情報が含まれます。

## <a name="remarks"></a>備考

メッセージを送受信するとき、メッセージは、MapiMessage対象として MAPI システムとの間を渡されます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| public str conversationID(\[str conversationId\])             | メッセージが所属する会話スレッドを識別する文字列を取得または設定します。           |
| public str dateReceived(\[Date theDate\])                     | メッセージを受信した日付を返します。                                                         |
| public int flags(\[int flags\])                               | メッセージ ステータス フラグのビットを設定または取得します。                                                       |
| public MapiFileDesc getFileNo(int fileNo)                     | メッセージからの添付ファイルを取得します。                                                                  |
| public MapiRecipDesc getRecipNo(int recipientNo)               | MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。                              |
| public str messageType(\[str messageType\])                   | IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。 |
| public int numFiles(\[int numFiles\])                         |                                                                                                         |
| public int numRecips(\[int numRecips\])                       |                                                                                                         |
| public MapiRecipDesc originator(\[MapiRecipDesc originator\]) |                                                                                                         |
| public str subject(\[str subject\])                           |                                                                                                         |
| public str text(\[str text\])                                 |                                                                                                         |
| public void new()                                             | MapiMessage クラスのインスタンスを初期化します。                                                       |
| public void finalize()                                        |                                                                                                         |
| public void setRecipNo(int recipNo, MapiRecipDesc recipient)  | メッセージに受信者を追加します。                                                                        |
| public void setFileNo(int fileNo, MapiFileDesc file)          | メッセージの添付ファイルを設定します。                                                                 |

## <a name="method-conversationid"></a>メソッド conversationID

メッセージが所属する会話スレッドを識別する文字列を取得または設定します。

```xpp
public str conversationID([str conversationId])
```

### <a name="parameters---conversationid"></a>パラメーター - conversationID

conversationId  
会話スレッドの ID。省略可能。

### <a name="return-value---conversationid"></a>戻り値 - conversationID

メッセージが所属する会話スレッドを識別する文字列。

### <a name="remarks---conversationid"></a>備考 - conversationID

メッセージング システムの中には、無視してこのメンバーを返さないものがあります。

## <a name="method-datereceived"></a>メソッド dateReceived

メッセージを受信した日付を返します。

```xpp
public str dateReceived([Date theDate])
```

### <a name="parameters---datereceived"></a>パラメーター - dateReceived

theDate  
メッセージを受信した日付 (オプション)。

### <a name="return-value---datereceived"></a>戻り値 - dateReceived

メッセージが受信された日付を示す文字列。

### <a name="remarks---datereceived"></a>備考 - dateReceived

返される文字列の形式は、YYYY/MM/DD HH:MMであり、24時間制を使用します。

## <a name="method-flags"></a>メソッド flags

メッセージ ステータス フラグのビットを設定または取得します。

```xpp
public int flags([int flags])
```

### <a name="parameters---flags"></a>パラメーター - flags

flags  
メッセージ ステータス フラグ (オプション)。

### <a name="return-value---flags"></a>戻り値 - flags

メッセージ ステータス フラグのビット。

### <a name="remarks---flags"></a>備考 - flags

次のフラグを設定できます。

-   \#MAPI\_RECEIPT\_REQUESTED � 受領通知のリクエストが要求されました。 クライアント アプリケーションは、メッセージを送信するときにこのビットを設定します。
-   \#MAPI\_SENT � メッセージが送信されました。
-   \#MAPI\_UNREAD � メッセージが未読です。

## <a name="method-getfileno"></a>メソッド getFileNo

メッセージからの添付ファイルを取得します。

```xpp
public MapiFileDesc getFileNo(int fileNo)
```

### <a name="parameters---getfileno"></a>パラメーター - getFileNo

fileNo  
取得する添付ファイルのインデックス。 インデックスは 1 から始まり、numFiles メソッドを使用して添付ファイルの総数を取得できます。

### <a name="return-value---getfileno"></a>戻り値 - getFileNo

添付ファイルに関する情報を含む MapiFileDesc オブジェクトを返します。

### <a name="remarks---getfileno"></a>備考 - getFileNo

添付ファイルは、MapiFileDesc オブジェクトで返されます。

### <a name="examples---getfileno"></a>例 - getFileNo

```xpp
{ 
    MapiFileDesc attachment; 
    MapiMessage message; 
    // Retrieve message. 
    // ...  
    if (message.NumFiles() >= 1) 
    { 
        attachment = message.GetFileNo(1); 
    } 
}
```

## <a name="method-getrecipno"></a>メソッド getRecipNo

MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。

```xpp
public MapiRecipDesc getRecipNo(int recipientNo)
```

### <a name="parameters---getrecipno"></a>パラメーター - getRecipNo

recipientNo  
取得する受信者の番号。 番号付けは 1 から始まり、numRecips メソッドを使用して受信者の総数を読み込むことができます。

### <a name="return-value---getrecipno"></a>戻り値 - getRecipNo

受信者または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を説明する MapiRecipDesc オブジェクト。

## <a name="method-messagetype"></a>メソッド messageType

IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。

```xpp
public str messageType([str messageType])
```

### <a name="parameters---messagetype"></a>パラメーター - messageType

messageType  
メッセージに設定する messageType 値 (オプション)。

### <a name="return-value---messagetype"></a>戻り値 - messageType

messagetype 文字列。

### <a name="remarks---messagetype"></a>備考 - messageType

アプリケーションは、IPM ではないメッセージのメッセージ タイプを選択できます。 IPM だけをサポートするクライアントは、メッセージを読むときに MessageType メンバーを無視し、メッセージを送信するときに空にすることができます。

## <a name="method-numfiles"></a>メソッド numFiles

```xpp
public int numFiles([int numFiles])
```

### <a name="parameters---numfiles"></a>パラメーター - numFiles

numFiles  

### <a name="return-value---numfiles"></a>戻り値 - numFiles

## <a name="method-numrecips"></a>メソッド numRecips

```xpp
public int numRecips([int numRecips])
```

### <a name="parameters---numrecips"></a>パラメーター - numRecips

numRecips  

### <a name="return-value---numrecips"></a>戻り値 - numRecips

## <a name="method-originator"></a>メソッド originator

```xpp
public MapiRecipDesc originator([MapiRecipDesc originator])
```

### <a name="parameters---originator"></a>パラメーター - originator

originator  

### <a name="return-value---originator"></a>戻り値 - originator

## <a name="method-subject"></a>メソッド subject

```xpp
public str subject([str subject])
```

### <a name="parameters---subject"></a>パラメーター - subject

subject  

### <a name="return-value---subject"></a>戻り値 - subject

## <a name="method-text"></a>メソッド text

```xpp
public str text([str text])
```

### <a name="parameters---text"></a>パラメーター - text

テキスト  

### <a name="return-value---text"></a>戻り値 - text

## <a name="method-new"></a>メソッド new

MapiMessage クラスのインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-setrecipno"></a>メソッド setRecipNo

メッセージに受信者を追加します。

```xpp
public void setRecipNo(int recipNo, MapiRecipDesc recipient)
```

### <a name="parameters---setrecipno"></a>パラメーター - setRecipNo

recipNo  
受信者を説明する MapiRecipDesc オブジェクト。

<!-- -->

recipient  
受信者を説明する MapiRecipDesc オブジェクト。

### <a name="remarks---setrecipno"></a>備考 - setRecipNo

正しい MapiRecipDesc オブジェクトをユーザーが入力した名前から取得する必要がある場合は、resolveName メソッドを使用します。

## <a name="method-setfileno"></a>メソッド setFileNo

メッセージの添付ファイルを設定します。

```xpp
public void setFileNo(int fileNo, MapiFileDesc file)
```

### <a name="parameters---setfileno"></a>パラメーター - setFileNo

fileNo  
添付ファイルを説明する MapiFileDesc オブジェクト。

<!-- -->

ファイル  
添付ファイルを説明する MapiFileDesc オブジェクト。

### <a name="remarks---setfileno"></a>備考 - setFileNo

添付ファイルには、1 から始まる番号が付けられます。 したがって、最初の添付ファイルには番号 1 を付ける必要があります。 numFiles メソッドを呼び出してアタッチメントの数を取得することができます。

### <a name="examples---setfileno"></a>例 - setFileNo

```xpp
{ 
    MapiMessage msg = new MapiMessage(); 
    MapiFileDesc attachment = new MapiFileDesc(); 
    attachment.Path("C:\\files\\info.txt"); 
    msg.SetFileNo(1,attachment); 
}
```

