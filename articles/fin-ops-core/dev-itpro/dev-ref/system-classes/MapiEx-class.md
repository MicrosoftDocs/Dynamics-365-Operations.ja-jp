---
title: MapiEx クラス
description: このトピックでは、MapiEx クラスについて説明します。
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
ms.openlocfilehash: ce6d856e09654c75fc4b9ef13640c068b8295892
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502587"
---
# <a name="class-mapiex"></a>クラス MapiEx

[!include [banner](../../includes/banner.md)]

```xpp
class MapiEx extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                          | 説明                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| public MapiExAppointment getAppointmentFromEntryId(str entryID) |                                                 |
| public MapiExContact getContactFromEntryId(str entryID)         |                                                 |
| public int getCurrentUser()                                     |                                                 |
| public str getCurrentUserEmail()                                |                                                 |
| public str getCurrentUserEntryId()                              |                                                 |
| public str getCurrentUserName()                                 |                                                 |
| public MapiExMail getMailFromEntryId(str entryID)               |                                                 |
| public MapiExTask getTaskFromEntryId(str entryID)               |                                                 |
| public int logon(str profileName, str password, int flags)      |                                                 |
| public boolean mapiInitialised()                                |                                                 |
| public boolean openMessageStore(str str)                        |                                                 |
| public void finalize()                                          |                                                 |
| public void new()                                               | MapiEx クラスの新しいインスタンスを初期化します。 |
| public void logout()                                            |                                                 |

## <a name="method-getappointmentfromentryid"></a>メソッド getAppointmentFromEntryId

```xpp
public MapiExAppointment getAppointmentFromEntryId(str entryID)
```

### <a name="parameters---getappointmentfromentryid"></a>パラメーター - getAppointmentFromEntryId

entryID  

### <a name="return-value---getappointmentfromentryid"></a>戻り値 - getAppointmentFromEntryId

## <a name="method-getcontactfromentryid"></a>メソッド getContactFromEntryId

```xpp
public MapiExContact getContactFromEntryId(str entryID)
```

### <a name="parameters---getcontactfromentryid"></a>パラメーター - getContactFromEntryId

entryID  

### <a name="return-value---getcontactfromentryid"></a>戻り値 - getContactFromEntryId

## <a name="method-getcurrentuser"></a>メソッド getCurrentUser

```xpp
public int getCurrentUser()
```

### <a name="return-value---getcurrentuser"></a>戻り値 - getCurrentUser

## <a name="method-getcurrentuseremail"></a>メソッド getCurrentUserEmail

```xpp
public str getCurrentUserEmail()
```

### <a name="return-value---getcurrentuseremail"></a>戻り値 - getCurrentUserEmail

## <a name="method-getcurrentuserentryid"></a>メソッド getCurrentUserEntryId

```xpp
public str getCurrentUserEntryId()
```

### <a name="return-value---getcurrentuserentryid"></a>戻り値 - getCurrentUserEntryId

## <a name="method-getcurrentusername"></a>メソッド getCurrentUserName

```xpp
public str getCurrentUserName()
```

### <a name="return-value---getcurrentusername"></a>戻り値 - getCurrentUserName

## <a name="method-getmailfromentryid"></a>メソッド getMailFromEntryId

```xpp
public MapiExMail getMailFromEntryId(str entryID)
```

### <a name="parameters---getmailfromentryid"></a>パラメーター - getMailFromEntryId

entryID  

### <a name="return-value---getmailfromentryid"></a>戻り値 - getMailFromEntryId

## <a name="method-gettaskfromentryid"></a>メソッド getTaskFromEntryId

```xpp
public MapiExTask getTaskFromEntryId(str entryID)
```

### <a name="parameters---gettaskfromentryid"></a>パラメーター - getTaskFromEntryId

entryID  

### <a name="return-value---gettaskfromentryid"></a>戻り値 - getTaskFromEntryId

## <a name="method-logon"></a>メソッド logon

```xpp
public int logon(str profileName, str password, int flags)
```

### <a name="parameters---logon"></a>パラメーター - logon

profileName  

<!-- -->

パスワード  

<!-- -->

flags  

### <a name="return-value---logon"></a>戻り値 - logon

## <a name="method-mapiinitialised"></a>メソッド mapiInitialised

```xpp
public boolean mapiInitialised()
```

### <a name="return-value---mapiinitialised"></a>戻り値 - mapiInitialised

## <a name="method-openmessagestore"></a>メソッド openMessageStore

```xpp
public boolean openMessageStore(str str)
```

### <a name="parameters---openmessagestore"></a>パラメーター - openMessageStore

str  

### <a name="return-value---openmessagestore"></a>戻り値 - openMessageStore

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

MapiEx クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-logout"></a>メソッド logout

```xpp
public void logout()
```

