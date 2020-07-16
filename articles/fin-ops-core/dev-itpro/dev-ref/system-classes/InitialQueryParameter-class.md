---
title: InitialQueryParameter クラス
description: このトピックでは、InitialQueryParameter クラスについて説明します。
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
ms.openlocfilehash: 419ff1a480309f1874ed8b11dfc5aa4ecf0d4219
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502897"
---
# <a name="class-initialqueryparameter"></a><span data-ttu-id="01449-103">クラス InitialQueryParameter</span><span class="sxs-lookup"><span data-stu-id="01449-103">Class InitialQueryParameter</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class InitialQueryParameter extends Object
```

## <a name="remarks"></a><span data-ttu-id="01449-104">備考</span><span class="sxs-lookup"><span data-stu-id="01449-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="01449-105">例</span><span class="sxs-lookup"><span data-stu-id="01449-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="01449-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="01449-106">Methods</span></span>

| <span data-ttu-id="01449-107">方法</span><span class="sxs-lookup"><span data-stu-id="01449-107">Method</span></span>                                                                                                       | <span data-ttu-id="01449-108">説明</span><span class="sxs-lookup"><span data-stu-id="01449-108">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="01449-109">public boolean applyQuery(FormDataSource datasource)</span><span class="sxs-lookup"><span data-stu-id="01449-109">public boolean applyQuery(FormDataSource datasource)</span></span>                                                         |                                                                |
| <span data-ttu-id="01449-110">public str dataSourceName(\[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="01449-110">public str dataSourceName(\[str dataSourceName\])</span></span>                                                            |                                                                |
| <span data-ttu-id="01449-111">public str modeledQueryName(\[str modeledQueryName\])</span><span class="sxs-lookup"><span data-stu-id="01449-111">public str modeledQueryName(\[str modeledQueryName\])</span></span>                                                        |                                                                |
| <span data-ttu-id="01449-112">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="01449-112">public Query query(\[Query query\])</span></span>                                                                          |                                                                |
| <span data-ttu-id="01449-113">::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="01449-113">::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\])</span></span> |                                                                |
| <span data-ttu-id="01449-114">::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])</span><span class="sxs-lookup"><span data-stu-id="01449-114">::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])</span></span>                     |                                                                |
| <span data-ttu-id="01449-115">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="01449-115">public void finalize()</span></span>                                                                                       |                                                                |
| <span data-ttu-id="01449-116">public void new()</span><span class="sxs-lookup"><span data-stu-id="01449-116">public void new()</span></span>                                                                                            | <span data-ttu-id="01449-117">InitialQueryParameter クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="01449-117">Initializes a new instance of the InitialQueryParameter class.</span></span> |

## <a name="method-applyquery"></a><span data-ttu-id="01449-118">メソッド applyQuery</span><span class="sxs-lookup"><span data-stu-id="01449-118">Method applyQuery</span></span>

```xpp
public boolean applyQuery(FormDataSource datasource)
```

### <a name="parameters---applyquery"></a><span data-ttu-id="01449-119">パラメーター - applyQuery</span><span class="sxs-lookup"><span data-stu-id="01449-119">Parameters - applyQuery</span></span>

<span data-ttu-id="01449-120">datasource</span><span class="sxs-lookup"><span data-stu-id="01449-120">datasource</span></span>  

### <a name="return-value---applyquery"></a><span data-ttu-id="01449-121">戻り値 - applyQuery</span><span class="sxs-lookup"><span data-stu-id="01449-121">Return Value - applyQuery</span></span>

## <a name="method-datasourcename"></a><span data-ttu-id="01449-122">メソッド dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-122">Method dataSourceName</span></span>

```xpp
public str dataSourceName([str dataSourceName])
```

### <a name="parameters---datasourcename"></a><span data-ttu-id="01449-123">パラメーター - dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-123">Parameters - dataSourceName</span></span>

<span data-ttu-id="01449-124">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-124">dataSourceName</span></span>  

### <a name="return-value---datasourcename"></a><span data-ttu-id="01449-125">戻り値 - dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-125">Return Value - dataSourceName</span></span>

## <a name="method-modeledqueryname"></a><span data-ttu-id="01449-126">メソッド modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-126">Method modeledQueryName</span></span>

```xpp
public str modeledQueryName([str modeledQueryName])
```

### <a name="parameters---modeledqueryname"></a><span data-ttu-id="01449-127">パラメーター - modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-127">Parameters - modeledQueryName</span></span>

<span data-ttu-id="01449-128">modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-128">modeledQueryName</span></span>  

### <a name="return-value---modeledqueryname"></a><span data-ttu-id="01449-129">戻り値 - modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-129">Return Value - modeledQueryName</span></span>

## <a name="method-query"></a><span data-ttu-id="01449-130">メソッド query</span><span class="sxs-lookup"><span data-stu-id="01449-130">Method query</span></span>

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a><span data-ttu-id="01449-131">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="01449-131">Parameters - query</span></span>

<span data-ttu-id="01449-132">クエリ</span><span class="sxs-lookup"><span data-stu-id="01449-132">query</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="01449-133">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="01449-133">Return Value - query</span></span>

## <a name="method-createbymodeledqueryname"></a><span data-ttu-id="01449-134">メソッド createByModeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-134">Method createByModeledQueryName</span></span>

```xpp
public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, [str dataSourceName])
```

### <a name="parameters---createbymodeledqueryname"></a><span data-ttu-id="01449-135">パラメーター - createByModeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-135">Parameters - createByModeledQueryName</span></span>

<span data-ttu-id="01449-136">modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-136">modeledQueryName</span></span>  

<!-- -->

<span data-ttu-id="01449-137">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-137">dataSourceName</span></span>  

### <a name="return-value---createbymodeledqueryname"></a><span data-ttu-id="01449-138">戻り値 - createByModeledQueryName</span><span class="sxs-lookup"><span data-stu-id="01449-138">Return Value - createByModeledQueryName</span></span>

## <a name="method-createbyquery"></a><span data-ttu-id="01449-139">メソッド createByQuery</span><span class="sxs-lookup"><span data-stu-id="01449-139">Method createByQuery</span></span>

```xpp
public static InitialQueryParameter createByQuery(Query query, [str dataSourceName])
```

### <a name="parameters---createbyquery"></a><span data-ttu-id="01449-140">パラメーター - createByQuery</span><span class="sxs-lookup"><span data-stu-id="01449-140">Parameters - createByQuery</span></span>

<span data-ttu-id="01449-141">クエリ</span><span class="sxs-lookup"><span data-stu-id="01449-141">query</span></span>  

<!-- -->

<span data-ttu-id="01449-142">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="01449-142">dataSourceName</span></span>  

### <a name="return-value---createbyquery"></a><span data-ttu-id="01449-143">戻り値 - createByQuery</span><span class="sxs-lookup"><span data-stu-id="01449-143">Return Value - createByQuery</span></span>

## <a name="method-finalize"></a><span data-ttu-id="01449-144">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="01449-144">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="01449-145">メソッド new</span><span class="sxs-lookup"><span data-stu-id="01449-145">Method new</span></span>

<span data-ttu-id="01449-146">InitialQueryParameter クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="01449-146">Initializes a new instance of the InitialQueryParameter class.</span></span>

```xpp
public void new()
```

