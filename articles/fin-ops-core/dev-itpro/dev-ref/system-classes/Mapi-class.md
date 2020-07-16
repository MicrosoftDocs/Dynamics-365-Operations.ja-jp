---
title: Mapi クラス
description: このトピックでは、Mapi クラスについて説明します。
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
ms.openlocfilehash: a98fdc0ff1735e4458eb9885b66212f1144a7392
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502588"
---
# <a name="class-mapi"></a>クラス Mapi

[!include [banner](../../includes/banner.md)]

```xpp
class Mapi extends Object
```

Mapi クラスを使用すると、Microsoft Exchange ベースのシステム、Microsoft Outlook Express、Lotus CCMail などのほとんどの主要なメール システムで、メールを送信、受信、管理できます。

## <a name="remarks"></a>備考

他の Mapi クラス、MapiMessage、MapiRecipDesc、MapiFileDesc とともに、このクラスでは、複数の受信者、添付ファイル、メッセージ テキスト、件名を指定できます。 最も簡単な方法は、マシン上に作業用のメール クライアントを設定し、いくつかの電子メール メッセージを送受信することによって正しく動作することを確認することです。 Mapi メソッドのフラグは、Mapi マクロに配置されます。 \#MAPI ステートメントと共に Mapi クラスを使用するコードにこのマクロを含めます。

## <a name="examples"></a>例

次の例は、このクラスを使用して電子メール メッセージを送信する方法を示しています。

```xpp
static void example() 
{ 
    #Mapi 
    Mapi m = new Mapi(); 
    MapiMessage msg = new MapiMessage(); 
    MapiRecipDesc recip = new MapiRecipDesc(); 
    // Set up the recipient. 
    recip.Name("someone"); 
    recip.RecipClass(#MAPI_TO); 
    msg.setRecipNo(1,recip); 
    // Log on using default profile. 
    m.Logon("","",#MAPI_USE_DEFAULT); 
    // Send the mail, and allow the user to modify the 
    // Subject, Text and Recipients in the Send Mail Dialog. 
    m.SendMail(msg,#MAPI_DIALOG); 
    // Log off. 
    m.Logoff(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| public int deleteMail(str messageID)                                           | メッセージ ストアから指定されたメッセージを削除します。                                                |
| public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\]) | メッセージ店舗で最初または次のメッセージを検索します。                                                |
| public int logoff()                                                            | メール システムからログオフすることができます。                                                                    |
| public int logon(str profileName, str password, int flags)                     | 指定されたプロファイルとパスワードを使用して、メール システムにログオンします。                              |
| public MapiMessage readMail(str messageID, \[int flags\])                      | メッセージ ストアからメッセージを取得します。                                                          |
| public MapiRecipDesc resolveName(str mame, int flags)                          | ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。 |
| public int saveMail(MapiMessage message, int flags, str messageId)             | メッセージ ストアにメッセージを保存します。                                                                |
| public int sendMail(MapiMessage message, \[int flags\])                        | 特定の受信者にメッセージを送信します。                                                         |
| public int status()                                                            | 最後の Mapi 操作のステータスを取得します。                                                     |
| public void new()                                                              | Mapi クラスのインスタンスを初期化します。                                                           |
| public void finalize()                                                         |                                                                                                      |

## <a name="method-deletemail"></a>メソッド deleteMail

メッセージ ストアから指定されたメッセージを削除します。

```xpp
public int deleteMail(str messageID)
```

### <a name="parameters---deletemail"></a>パラメーター - deleteMail

messageID  
削除するメッセージの一意のメッセージ ID。

### <a name="return-value---deletemail"></a>戻り値 - deleteMail

状態 \#SUCCESS\_SUCCES またはエラー コード。これは \#MAPI マクロにあります。

### <a name="remarks---deletemail"></a>備考 - deleteMail

メッセージ ID は、findNext メソッドを使用して取得できます。

## <a name="method-findnext"></a>メソッド findNext

メッセージ店舗で最初または次のメッセージを検索します。

```xpp
public str findNext([str messageType], [str seedMessageID], [int flags])
```

### <a name="parameters---findnext"></a>パラメーター - findNext

messageType  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

<!-- -->

seedMessageID  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

<!-- -->

flags  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

### <a name="return-value---findnext"></a>戻り値 - findNext

見つかったメッセージのメッセージ ID。メッセージが見つからない場合は空の文字列です。

### <a name="remarks---findnext"></a>備考 - findNext

このメソッドを呼び出して最初のメッセージを検索し、続く呼び出しを発行して次のメッセージを取得します。 このメソッドを呼び出した後、status メソッドを使用して Mapi エラーを確認します。

## <a name="method-logoff"></a>メソッド logoff

メール システムからログオフすることができます。

```xpp
public int logoff()
```

### <a name="return-value---logoff"></a>戻り値 - logoff

状態 \#SUCCESS\_SUCCESS またはエラー コード。これは \#MAPI マクロにあります。

## <a name="method-logon"></a>メソッド logon

指定されたプロファイルとパスワードを使用して、メール システムにログオンします。

```xpp
public int logon(str profileName, str password, int flags)
```

### <a name="parameters---logon"></a>パラメーター - logon

profileName  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

パスワード  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧。 有効なフラグは次のとおりです。

### <a name="return-value---logon"></a>戻り値 - logon

ログオンに成功した場合は、状態 \#SUCCESS\_SUCCESS です。そうでない場合は、エラー コードを返します。これは、\#MAPI マクロにあります。

### <a name="remarks---logon"></a>備考 - logon

ログオンするための簡単で一般的な方法は、既定のプロファイルを使用してログオンする \#MAPI\_USE\_DEFAULT フラグを指定することです。

## <a name="method-readmail"></a>メソッド readMail

メッセージ ストアからメッセージを取得します。

```xpp
public MapiMessage readMail(str messageID, [int flags])
```

### <a name="parameters---readmail"></a>パラメーター - readMail

messageID  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

### <a name="return-value---readmail"></a>戻り値-readMail

取得された MapiMessage オブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

## <a name="method-resolvename"></a>メソッド resolveName

ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。

```xpp
public MapiRecipDesc resolveName(str mame, int flags)
```

### <a name="parameters---resolvename"></a>パラメーター - resolveName

mame  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧。 有効なフラグは次のとおりです。

### <a name="return-value---resolvename"></a>戻り値 - resolveName

明確なアドレス一覧エントリを持つ MapiRecipDesc クラス オブジェクト。

## <a name="method-savemail"></a>メソッド saveMail

メッセージ ストアにメッセージを保存します。

```xpp
public int saveMail(MapiMessage message, int flags, str messageId)
```

### <a name="parameters---savemail"></a>パラメーター - saveMail

メッセージ  
取得するメッセージの一意の ID。

<!-- -->

flags  
取得するメッセージの一意の ID。

<!-- -->

messageId  
取得するメッセージの一意の ID。

### <a name="return-value---savemail"></a>戻り値 - saveMail

状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。

## <a name="method-sendmail"></a>メソッド sendMail

特定の受信者にメッセージを送信します。

```xpp
public int sendMail(MapiMessage message, [int flags])
```

### <a name="parameters---sendmail"></a>パラメーター - sendMail

メッセージ  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

### <a name="return-value---sendmail"></a>戻り値 - sendMail

状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。

## <a name="method-status"></a>メソッド status

最後の Mapi 操作のステータスを取得します。

```xpp
public int status()
```

### <a name="return-value---status"></a>戻り値 - status

最後の Mapi 操作のステータス コード。

### <a name="remarks---status"></a>備考 - status

ステータス コードは \#MAPI マクロにあります。

## <a name="method-new"></a>メソッド new

Mapi クラスのインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

