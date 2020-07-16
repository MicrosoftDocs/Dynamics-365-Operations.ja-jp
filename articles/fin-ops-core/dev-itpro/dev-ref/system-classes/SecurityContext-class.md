---
title: SecurityContext クラス
description: このトピックでは、SecurityContext クラスについて説明します。
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
ms.openlocfilehash: 25cd9a5c6c79e919123df223af8558c8c4823c54
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502813"
---
# <a name="class-securitycontext"></a>クラス SecurityContext

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityContext extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                | 説明 |
|-------------------------------------------------------------------------------------------------------|-------------|
| public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\]) |             |
| ::public static SecurityContext current()                                                             |             |
| ::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)  |             |
| public boolean equal(SecurityContext context)                                                         |             |
| public SecurableType securableType()                                                                  |             |
| public str securableName()                                                                            |             |
| public str securableChildName()                                                                       |             |
| public void push()                                                                                    |             |
| ::public static void pop()                                                                            |             |
| private void new()                                                                                    |             |

## <a name="method-istableoperationallowed"></a>メソッド isTableOperationAllowed

```xpp
public boolean isTableOperationAllowed(int tableId, StatementType operation, [DataAreaId dataArea])
```

### <a name="parameters---istableoperationallowed"></a>パラメーター - isTableOperationAllowed

tableId  

<!-- -->

工程  

<!-- -->

dataArea  

### <a name="return-value---istableoperationallowed"></a>戻り値 - isTableOperationAllowed

## <a name="method-current"></a>メソッド current

```xpp
public static SecurityContext current()
```

### <a name="return-value---current"></a>戻り値 - current

## <a name="method-constructfromentrypoint"></a>メソッド constructFromEntryPoint

```xpp
public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)
```

### <a name="parameters---constructfromentrypoint"></a>パラメーター - constructFromEntryPoint

タイプ  

<!-- -->

名前  

<!-- -->

childName  

### <a name="return-value---constructfromentrypoint"></a>戻り値 - constructFromEntryPoint

## <a name="method-equal"></a>メソッド equal

```xpp
public boolean equal(SecurityContext context)
```

### <a name="parameters---equal"></a>パラメーター - equal

context  

### <a name="return-value---equal"></a>戻り値 - equal

## <a name="method-securabletype"></a>メソッド securableType

```xpp
public SecurableType securableType()
```

### <a name="return-value---securabletype"></a>戻り値 - securableType

## <a name="method-securablename"></a>メソッド securableName

```xpp
public str securableName()
```

### <a name="return-value---securablename"></a>戻り値 - securableName

## <a name="method-securablechildname"></a>メソッド securableChildName

```xpp
public str securableChildName()
```

### <a name="return-value---securablechildname"></a>戻り値 - securableChildName

## <a name="method-push"></a>メソッド push

```xpp
public void push()
```

## <a name="method-pop"></a>メソッド pop

```xpp
public static void pop()
```

## <a name="method-new"></a>メソッド new

```xpp
private void new()
```

