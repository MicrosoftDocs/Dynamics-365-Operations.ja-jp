---
title: AsyncTaskResult クラス
description: このトピックでは、AsyncTaskResult クラスについて説明します。
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
ms.openlocfilehash: 3044e816b22544c99f13f39747216537bd2c359c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502723"
---
# <a name="class-asynctaskresult"></a>クラス AsyncTaskResult

[!include [banner](../../includes/banner.md)]

```xpp
class AsyncTaskResult extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                               | 説明 |
|--------------------------------------------------------------------------------------|-------------|
| public container getResult()                                                         |             |
| public System.Exception getException()                                               |             |
| public container getInfologData()                                                    |             |
| public container getAsyncState()                                                     |             |
| ::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task) |             |

## <a name="method-getresult"></a>メソッド getResult

```xpp
public container getResult()
```

### <a name="return-value---getresult"></a>戻り値 - getResult

## <a name="method-getexception"></a>メソッド getException

```xpp
public System.Exception getException()
```

### <a name="return-value---getexception"></a>戻り値 - getException

## <a name="method-getinfologdata"></a>メソッド getInfologData

```xpp
public container getInfologData()
```

### <a name="return-value---getinfologdata"></a>戻り値 - getInfologData

## <a name="method-getasyncstate"></a>メソッド getAsyncState

```xpp
public container getAsyncState()
```

### <a name="return-value---getasyncstate"></a>戻り値 - getAsyncState

## <a name="method-getasynctaskresult"></a>メソッド getAsyncTaskResult

```xpp
public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)
```

### <a name="parameters---getasynctaskresult"></a>パラメーター - getAsyncTaskResult

タスク  

### <a name="return-value---getasynctaskresult"></a>戻り値 - getAsyncTaskResult

