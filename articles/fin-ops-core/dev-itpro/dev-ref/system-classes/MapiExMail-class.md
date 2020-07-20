---
title: MapiExMail クラス
description: このトピックでは、MapiExMail クラスについて説明します。
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
ms.openlocfilehash: 4a11e39b6a7f8a873c646dab8de1d1cdef955826
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502583"
---
# <a name="class-mapiexmail"></a>クラス MapiExMail

[!include [banner](../../includes/banner.md)]

```xpp
class MapiExMail extends MapiExMessage
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                         |
|--------------------------------------------------------|-----------------------------------------------------|
| public str addRecipient(str email, str name, int type) |                                                     |
| public str entryId()                                   |                                                     |
| public boolean getRecipient(int index)                 |                                                     |
| public int getRecipientCount()                         |                                                     |
| public str getRecipientDisplayName()                   |                                                     |
| public str getRecipientEmailAddress()                  |                                                     |
| public str getRecipientEntryId()                       |                                                     |
| public boolean getRecipients()                         |                                                     |
| public str getRecipientSMTPAddress()                   |                                                     |
| public int getRecipientType()                          |                                                     |
| public str getSenderEmail()                            |                                                     |
| public str getSenderName()                             |                                                     |
| public str removeRecipient(str email, int type)        |                                                     |
| public boolean save()                                  |                                                     |
| public boolean saveMsgToFile(str fileName)             |                                                     |
| public boolean send()                                  |                                                     |
| public boolean setBody(str body)                       |                                                     |
| public void finalize()                                 |                                                     |
| public void close()                                    |                                                     |
| public void new()                                      | MapiExMail クラスの新しいインスタンスを初期化します。 |

## <a name="method-addrecipient"></a>メソッド addRecipient

```xpp
public str addRecipient(str email, str name, int type)
```

### <a name="parameters---addrecipient"></a>パラメーター - addRecipient

電子メール  

<!-- -->

名前  

<!-- -->

タイプ  

### <a name="return-value---addrecipient"></a>戻り値 - addRefCnt

## <a name="method-entryid"></a>メソッド entryId

```xpp
public str entryId()
```

### <a name="return-value---entryid"></a>戻り値 - entryId

## <a name="method-getrecipient"></a>メソッド getRecipient

```xpp
public boolean getRecipient(int index)
```

### <a name="parameters---getrecipient"></a>戻り値 - getRecipient

指数  

### <a name="return-value---getrecipient"></a>戻り値 - getRecipient

## <a name="method-getrecipientcount"></a>メソッド getRecipientCount

```xpp
public int getRecipientCount()
```

### <a name="return-value---getrecipientcount"></a>戻り値 - getRecipientCount

## <a name="method-getrecipientdisplayname"></a>メソッド getRecipientDisplayName

```xpp
public str getRecipientDisplayName()
```

### <a name="return-value---getrecipientdisplayname"></a>戻り値 - getRecipientDisplayName

## <a name="method-getrecipientemailaddress"></a>メソッド getRecipientEmailAddress

```xpp
public str getRecipientEmailAddress()
```

### <a name="return-value---getrecipientemailaddress"></a>戻り値 - getRecipientEmailAddress

## <a name="method-getrecipiententryid"></a>メソッド getRecipientEntryId

```xpp
public str getRecipientEntryId()
```

### <a name="return-value---getrecipiententryid"></a>戻り値 - getRecipientCount

## <a name="method-getrecipients"></a>メソッド getRecipients

```xpp
public boolean getRecipients()
```

### <a name="return-value---getrecipients"></a>戻り値 - getRecipients

## <a name="method-getrecipientsmtpaddress"></a>メソッド getRecipientSMTPAddress

```xpp
public str getRecipientSMTPAddress()
```

### <a name="return-value---getrecipientsmtpaddress"></a>戻り値 - getRecipientSMTPAddress

## <a name="method-getrecipienttype"></a>メソッド getRecipientType

```xpp
public int getRecipientType()
```

### <a name="return-value---getrecipienttype"></a>戻り値 - getRecipientType

## <a name="method-getsenderemail"></a>メソッド getSenderEmail

```xpp
public str getSenderEmail()
```

### <a name="return-value---getsenderemail"></a>戻り値 - getSenderEmail

## <a name="method-getsendername"></a>メソッド getSenderName

```xpp
public str getSenderName()
```

### <a name="return-value---getsendername"></a>戻り値 - getSenderName

## <a name="method-removerecipient"></a>メソッド removeRecipient

```xpp
public str removeRecipient(str email, int type)
```

### <a name="parameters---removerecipient"></a>パラメーター - removeRecipient

電子メール  

<!-- -->

タイプ  

### <a name="return-value---removerecipient"></a>戻り値 - removeRecipient

## <a name="method-save"></a>メソッド save

```xpp
public boolean save()
```

### <a name="return-value---save"></a>戻り値 - save

## <a name="method-savemsgtofile"></a>メソッド saveMsgToFile

```xpp
public boolean saveMsgToFile(str fileName)
```

### <a name="parameters---savemsgtofile"></a>パラメーター - saveMsgToFile

fileName  

### <a name="return-value---savemsgtofile"></a>戻り値 - saveMsgToFile

## <a name="method-send"></a>メソッド send

```xpp
public boolean send()
```

### <a name="return-value---send"></a>戻り値 - send

## <a name="method-setbody"></a>メソッド setBody

```xpp
public boolean setBody(str body)
```

### <a name="parameters---setbody"></a>パラメーター - setBody

body  

### <a name="return-value---setbody"></a>戻り値 - setBody

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-close"></a>メソッド close

```xpp
public void close()
```

## <a name="method-new"></a>メソッド new

MapiExMail クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

