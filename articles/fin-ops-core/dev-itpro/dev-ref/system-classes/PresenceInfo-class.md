---
title: PresenceInfo クラス
description: このトピックでは、PresenceInfo クラスについて説明します。
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
ms.openlocfilehash: 70bcf43b42a315f3ae5254fc3b492ae3a7983994
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502540"
---
# <a name="class-presenceinfo"></a>クラス PresenceInfo

[!include [banner](../../includes/banner.md)]

```xpp
class PresenceInfo extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                | 説明                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------|
| public str contactName(\[str contactName\])                           |                                                       |
| public str emailAddress(int index)                                    |                                                       |
| public str emailAlias(int index)                                      |                                                       |
| public int emailCount()                                               |                                                       |
| public str phoneAlias(int index)                                      |                                                       |
| public int phoneCount()                                               |                                                       |
| public str phoneNumber(int index)                                     |                                                       |
| public str sipAddress(\[str sipAddress\])                             |                                                       |
| public void finalize()                                                |                                                       |
| public void new()                                                     | PresenceInfo クラスの新しいインスタンスを初期化します。 |
| public void addEmailAddress(\[str emailAlias\], \[str emailAddress\]) |                                                       |
| public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])   |                                                       |

## <a name="method-contactname"></a>メソッド contactName

```xpp
public str contactName([str contactName])
```

### <a name="parameters---contactname"></a>パラメーター - contactName

contactName  

### <a name="return-value---contactname"></a>戻り値 - contactName

## <a name="method-emailaddress"></a>メソッド emailAddress

```xpp
public str emailAddress(int index)
```

### <a name="parameters---emailaddress"></a>パラメーター - emailAddress

指数  

### <a name="return-value---emailaddress"></a>戻り値 - emailAddress

## <a name="method-emailalias"></a>メソッド emailAlias

```xpp
public str emailAlias(int index)
```

### <a name="parameters---emailalias"></a>パラメーター - emailAlias

指数  

### <a name="return-value---emailalias"></a>戻り値 - emailAlias

## <a name="method-emailcount"></a>メソッド emailCount

```xpp
public int emailCount()
```

### <a name="return-value---emailcount"></a>戻り値 - emailCount

## <a name="method-phonealias"></a>メソッド phoneAlias

```xpp
public str phoneAlias(int index)
```

### <a name="parameters---phonealias"></a>パラメーター - phoneAlias

指数  

### <a name="return-value---phonealias"></a>戻り値 - phoneAlias

## <a name="method-phonecount"></a>メソッド phoneCount

```xpp
public int phoneCount()
```

### <a name="return-value---phonecount"></a>戻り値 - phoneCount

## <a name="method-phonenumber"></a>メソッド phoneNumber

```xpp
public str phoneNumber(int index)
```

### <a name="parameters---phonenumber"></a>パラメーター - phoneNumber

指数  

### <a name="return-value---phonenumber"></a>戻り値 - phoneNumber

## <a name="method-sipaddress"></a>メソッド sipAddress

```xpp
public str sipAddress([str sipAddress])
```

### <a name="parameters---sipaddress"></a>パラメーター - sipAddress

sipAddress  

### <a name="return-value---sipaddress"></a>戻り値 - sipAddress

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

PresenceInfo クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-addemailaddress"></a>メソッド addEmailAddress

```xpp
public void addEmailAddress([str emailAlias], [str emailAddress])
```

### <a name="parameters---addemailaddress"></a>パラメーター - addEmailAddress

emailAlias  

<!-- -->

emailAddress  

## <a name="method-addphonenumber"></a>メソッド addPhoneNumber

```xpp
public void addPhoneNumber([str phoneAlias], [str phoneNumber])
```

### <a name="parameters---addphonenumber"></a>パラメーター - addPhoneNumber

phoneAlias  

<!-- -->

phoneNumber  

