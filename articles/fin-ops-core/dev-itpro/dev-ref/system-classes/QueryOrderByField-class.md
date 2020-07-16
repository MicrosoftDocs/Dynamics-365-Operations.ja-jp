---
title: QueryOrderByField クラス
description: このトピックでは、QueryOrderByField クラスについて説明します。
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
ms.openlocfilehash: 32ccfc033f1b949082fc735ec63c5bb57a27509d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502860"
---
# <a name="class-queryorderbyfield"></a><span data-ttu-id="c1437-103">クラス QueryOrderByField</span><span class="sxs-lookup"><span data-stu-id="c1437-103">Class QueryOrderByField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryOrderByField extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="c1437-104">備考</span><span class="sxs-lookup"><span data-stu-id="c1437-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c1437-105">例</span><span class="sxs-lookup"><span data-stu-id="c1437-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c1437-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c1437-106">Methods</span></span>

| <span data-ttu-id="c1437-107">方法</span><span class="sxs-lookup"><span data-stu-id="c1437-107">Method</span></span>                                                  | <span data-ttu-id="c1437-108">説明</span><span class="sxs-lookup"><span data-stu-id="c1437-108">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="c1437-109">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c1437-109">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="c1437-110">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1437-110">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="c1437-111">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c1437-111">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="c1437-112">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c1437-112">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="c1437-113">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="c1437-113">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="c1437-114">public SortOrder direction()</span><span class="sxs-lookup"><span data-stu-id="c1437-114">public SortOrder direction()</span></span>                            |             |
| <span data-ttu-id="c1437-115">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="c1437-115">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="c1437-116">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="c1437-116">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="c1437-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="c1437-117">public void finalize()</span></span>                                  |             |

## <a name="method-autoheader"></a><span data-ttu-id="c1437-118">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="c1437-118">Method autoHeader</span></span>

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a><span data-ttu-id="c1437-119">パラメーター - autoHeader</span><span class="sxs-lookup"><span data-stu-id="c1437-119">Parameters - autoHeader</span></span>

<span data-ttu-id="c1437-120">値</span><span class="sxs-lookup"><span data-stu-id="c1437-120">value</span></span>  

### <a name="return-value---autoheader"></a><span data-ttu-id="c1437-121">戻り値 - autoHeader</span><span class="sxs-lookup"><span data-stu-id="c1437-121">Return Value - autoHeader</span></span>

## <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="c1437-122">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-122">Method autoHeaderDetailLevel</span></span>

```xpp
public int autoHeaderDetailLevel([int value])
```

### <a name="parameters---autoheaderdetaillevel"></a><span data-ttu-id="c1437-123">パラメーター - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-123">Parameters - autoHeaderDetailLevel</span></span>

<span data-ttu-id="c1437-124">値</span><span class="sxs-lookup"><span data-stu-id="c1437-124">value</span></span>  

### <a name="return-value---autoheaderdetaillevel"></a><span data-ttu-id="c1437-125">戻り値 - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-125">Return Value - autoHeaderDetailLevel</span></span>

## <a name="method-autosum"></a><span data-ttu-id="c1437-126">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="c1437-126">Method autoSum</span></span>

```xpp
public boolean autoSum([boolean value])
```

### <a name="parameters---autosum"></a><span data-ttu-id="c1437-127">パラメーター - autoSum</span><span class="sxs-lookup"><span data-stu-id="c1437-127">Parameters - autoSum</span></span>

<span data-ttu-id="c1437-128">値</span><span class="sxs-lookup"><span data-stu-id="c1437-128">value</span></span>  

### <a name="return-value---autosum"></a><span data-ttu-id="c1437-129">戻り値 - autoSum</span><span class="sxs-lookup"><span data-stu-id="c1437-129">Return Value - autoSum</span></span>

## <a name="method-autosumdetaillevel"></a><span data-ttu-id="c1437-130">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-130">Method autoSumDetailLevel</span></span>

```xpp
public int autoSumDetailLevel([int value])
```

### <a name="parameters---autosumdetaillevel"></a><span data-ttu-id="c1437-131">パラメーター - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-131">Parameters - autoSumDetailLevel</span></span>

<span data-ttu-id="c1437-132">値</span><span class="sxs-lookup"><span data-stu-id="c1437-132">value</span></span>  

### <a name="return-value---autosumdetaillevel"></a><span data-ttu-id="c1437-133">戻り値 - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="c1437-133">Return Value - autoSumDetailLevel</span></span>

## <a name="method-datasource"></a><span data-ttu-id="c1437-134">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="c1437-134">Method dataSource</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="c1437-135">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="c1437-135">Return Value - dataSource</span></span>

## <a name="method-direction"></a><span data-ttu-id="c1437-136">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="c1437-136">Method direction</span></span>

```xpp
public SortOrder direction()
```

### <a name="return-value---direction"></a><span data-ttu-id="c1437-137">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="c1437-137">Return Value - direction</span></span>

## <a name="method-fieldid"></a><span data-ttu-id="c1437-138">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="c1437-138">Method fieldID</span></span>

```xpp
public int fieldID()
```

### <a name="return-value---fieldid"></a><span data-ttu-id="c1437-139">戻り値 - fieldID</span><span class="sxs-lookup"><span data-stu-id="c1437-139">Return Value - fieldID</span></span>

## <a name="method-tableselector"></a><span data-ttu-id="c1437-140">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="c1437-140">Method tableSelector</span></span>

```xpp
public TableId tableSelector([TableId tableSelector])
```

### <a name="parameters---tableselector"></a><span data-ttu-id="c1437-141">パラメーター - tableSelector</span><span class="sxs-lookup"><span data-stu-id="c1437-141">Parameters - tableSelector</span></span>

<span data-ttu-id="c1437-142">tableSelector</span><span class="sxs-lookup"><span data-stu-id="c1437-142">tableSelector</span></span>  

### <a name="return-value---tableselector"></a><span data-ttu-id="c1437-143">戻り値 - tableSelector</span><span class="sxs-lookup"><span data-stu-id="c1437-143">Return Value - tableSelector</span></span>

## <a name="method-finalize"></a><span data-ttu-id="c1437-144">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="c1437-144">Method finalize</span></span>

```xpp
public void finalize()
```

