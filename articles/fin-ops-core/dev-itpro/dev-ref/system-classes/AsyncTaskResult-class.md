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
# <a name="class-asynctaskresult"></a><span data-ttu-id="2f39d-103">クラス AsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-103">Class AsyncTaskResult</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AsyncTaskResult extends Object
```

## <a name="remarks"></a><span data-ttu-id="2f39d-104">備考</span><span class="sxs-lookup"><span data-stu-id="2f39d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2f39d-105">例</span><span class="sxs-lookup"><span data-stu-id="2f39d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2f39d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2f39d-106">Methods</span></span>

| <span data-ttu-id="2f39d-107">方法</span><span class="sxs-lookup"><span data-stu-id="2f39d-107">Method</span></span>                                                                               | <span data-ttu-id="2f39d-108">説明</span><span class="sxs-lookup"><span data-stu-id="2f39d-108">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="2f39d-109">public container getResult()</span><span class="sxs-lookup"><span data-stu-id="2f39d-109">public container getResult()</span></span>                                                         |             |
| <span data-ttu-id="2f39d-110">public System.Exception getException()</span><span class="sxs-lookup"><span data-stu-id="2f39d-110">public System.Exception getException()</span></span>                                               |             |
| <span data-ttu-id="2f39d-111">public container getInfologData()</span><span class="sxs-lookup"><span data-stu-id="2f39d-111">public container getInfologData()</span></span>                                                    |             |
| <span data-ttu-id="2f39d-112">public container getAsyncState()</span><span class="sxs-lookup"><span data-stu-id="2f39d-112">public container getAsyncState()</span></span>                                                     |             |
| <span data-ttu-id="2f39d-113">::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)</span><span class="sxs-lookup"><span data-stu-id="2f39d-113">::public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)</span></span> |             |

## <a name="method-getresult"></a><span data-ttu-id="2f39d-114">メソッド getResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-114">Method getResult</span></span>

```xpp
public container getResult()
```

### <a name="return-value---getresult"></a><span data-ttu-id="2f39d-115">戻り値 - getResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-115">Return Value - getResult</span></span>

## <a name="method-getexception"></a><span data-ttu-id="2f39d-116">メソッド getException</span><span class="sxs-lookup"><span data-stu-id="2f39d-116">Method getException</span></span>

```xpp
public System.Exception getException()
```

### <a name="return-value---getexception"></a><span data-ttu-id="2f39d-117">戻り値 - getException</span><span class="sxs-lookup"><span data-stu-id="2f39d-117">Return Value - getException</span></span>

## <a name="method-getinfologdata"></a><span data-ttu-id="2f39d-118">メソッド getInfologData</span><span class="sxs-lookup"><span data-stu-id="2f39d-118">Method getInfologData</span></span>

```xpp
public container getInfologData()
```

### <a name="return-value---getinfologdata"></a><span data-ttu-id="2f39d-119">戻り値 - getInfologData</span><span class="sxs-lookup"><span data-stu-id="2f39d-119">Return Value - getInfologData</span></span>

## <a name="method-getasyncstate"></a><span data-ttu-id="2f39d-120">メソッド getAsyncState</span><span class="sxs-lookup"><span data-stu-id="2f39d-120">Method getAsyncState</span></span>

```xpp
public container getAsyncState()
```

### <a name="return-value---getasyncstate"></a><span data-ttu-id="2f39d-121">戻り値 - getAsyncState</span><span class="sxs-lookup"><span data-stu-id="2f39d-121">Return Value - getAsyncState</span></span>

## <a name="method-getasynctaskresult"></a><span data-ttu-id="2f39d-122">メソッド getAsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-122">Method getAsyncTaskResult</span></span>

```xpp
public static AsyncTaskResult getAsyncTaskResult(System.Threading.Tasks.Task task)
```

### <a name="parameters---getasynctaskresult"></a><span data-ttu-id="2f39d-123">パラメーター - getAsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-123">Parameters - getAsyncTaskResult</span></span>

<span data-ttu-id="2f39d-124">タスク</span><span class="sxs-lookup"><span data-stu-id="2f39d-124">task</span></span>  

### <a name="return-value---getasynctaskresult"></a><span data-ttu-id="2f39d-125">戻り値 - getAsyncTaskResult</span><span class="sxs-lookup"><span data-stu-id="2f39d-125">Return Value - getAsyncTaskResult</span></span>

