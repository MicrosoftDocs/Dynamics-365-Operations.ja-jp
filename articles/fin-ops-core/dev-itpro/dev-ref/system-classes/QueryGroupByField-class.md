---
title: QueryGroupByField クラス
description: このトピックでは、QueryGroupByField クラスについて説明します。
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
ms.openlocfilehash: 004530932ede578a1e911b4fa81a244557c2b9c9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502859"
---
# <a name="class-querygroupbyfield"></a><span data-ttu-id="debd9-103">クラス QueryGroupByField</span><span class="sxs-lookup"><span data-stu-id="debd9-103">Class QueryGroupByField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryGroupByField extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="debd9-104">備考</span><span class="sxs-lookup"><span data-stu-id="debd9-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="debd9-105">例</span><span class="sxs-lookup"><span data-stu-id="debd9-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="debd9-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="debd9-106">Methods</span></span>

| <span data-ttu-id="debd9-107">方法</span><span class="sxs-lookup"><span data-stu-id="debd9-107">Method</span></span>                                                  | <span data-ttu-id="debd9-108">説明</span><span class="sxs-lookup"><span data-stu-id="debd9-108">Description</span></span> |
|---------------------------------------------------------|-------------|
| <span data-ttu-id="debd9-109">public boolean autoHeader(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="debd9-109">public boolean autoHeader(\[boolean value\])</span></span>            |             |
| <span data-ttu-id="debd9-110">public int autoHeaderDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="debd9-110">public int autoHeaderDetailLevel(\[int value\])</span></span>         |             |
| <span data-ttu-id="debd9-111">public boolean autoSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="debd9-111">public boolean autoSum(\[boolean value\])</span></span>               |             |
| <span data-ttu-id="debd9-112">public int autoSumDetailLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="debd9-112">public int autoSumDetailLevel(\[int value\])</span></span>            |             |
| <span data-ttu-id="debd9-113">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="debd9-113">public QueryBuildDataSource dataSource()</span></span>                |             |
| <span data-ttu-id="debd9-114">public int fieldID()</span><span class="sxs-lookup"><span data-stu-id="debd9-114">public int fieldID()</span></span>                                    |             |
| <span data-ttu-id="debd9-115">public TableId tableSelector(\[TableId tableSelector\])</span><span class="sxs-lookup"><span data-stu-id="debd9-115">public TableId tableSelector(\[TableId tableSelector\])</span></span> |             |
| <span data-ttu-id="debd9-116">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="debd9-116">public void finalize()</span></span>                                  |             |

## <a name="method-autoheader"></a><span data-ttu-id="debd9-117">メソッド autoHeader</span><span class="sxs-lookup"><span data-stu-id="debd9-117">Method autoHeader</span></span>

```xpp
public boolean autoHeader([boolean value])
```

### <a name="parameters---autoheader"></a><span data-ttu-id="debd9-118">パラメーター - autoHeader</span><span class="sxs-lookup"><span data-stu-id="debd9-118">Parameters - autoHeader</span></span>

<span data-ttu-id="debd9-119">値</span><span class="sxs-lookup"><span data-stu-id="debd9-119">value</span></span>  

### <a name="return-value---autoheader"></a><span data-ttu-id="debd9-120">戻り値 - autoHeader</span><span class="sxs-lookup"><span data-stu-id="debd9-120">Return Value - autoHeader</span></span>

## <a name="method-autoheaderdetaillevel"></a><span data-ttu-id="debd9-121">メソッド autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-121">Method autoHeaderDetailLevel</span></span>

```xpp
public int autoHeaderDetailLevel([int value])
```

### <a name="parameters---autoheaderdetaillevel"></a><span data-ttu-id="debd9-122">パラメーター - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-122">Parameters - autoHeaderDetailLevel</span></span>

<span data-ttu-id="debd9-123">値</span><span class="sxs-lookup"><span data-stu-id="debd9-123">value</span></span>  

### <a name="return-value---autoheaderdetaillevel"></a><span data-ttu-id="debd9-124">戻り値 - autoHeaderDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-124">Return Value - autoHeaderDetailLevel</span></span>

## <a name="method-autosum"></a><span data-ttu-id="debd9-125">メソッド autoSum</span><span class="sxs-lookup"><span data-stu-id="debd9-125">Method autoSum</span></span>

```xpp
public boolean autoSum([boolean value])
```

### <a name="parameters---autosum"></a><span data-ttu-id="debd9-126">パラメーター - autoSum</span><span class="sxs-lookup"><span data-stu-id="debd9-126">Parameters - autoSum</span></span>

<span data-ttu-id="debd9-127">値</span><span class="sxs-lookup"><span data-stu-id="debd9-127">value</span></span>  

### <a name="return-value---autosum"></a><span data-ttu-id="debd9-128">戻り値 - autoSum</span><span class="sxs-lookup"><span data-stu-id="debd9-128">Return Value - autoSum</span></span>

## <a name="method-autosumdetaillevel"></a><span data-ttu-id="debd9-129">メソッド autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-129">Method autoSumDetailLevel</span></span>

```xpp
public int autoSumDetailLevel([int value])
```

### <a name="parameters---autosumdetaillevel"></a><span data-ttu-id="debd9-130">パラメーター - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-130">Parameters - autoSumDetailLevel</span></span>

<span data-ttu-id="debd9-131">値</span><span class="sxs-lookup"><span data-stu-id="debd9-131">value</span></span>  

### <a name="return-value---autosumdetaillevel"></a><span data-ttu-id="debd9-132">戻り値 - autoSumDetailLevel</span><span class="sxs-lookup"><span data-stu-id="debd9-132">Return Value - autoSumDetailLevel</span></span>

## <a name="method-datasource"></a><span data-ttu-id="debd9-133">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="debd9-133">Method dataSource</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="debd9-134">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="debd9-134">Return Value - dataSource</span></span>

## <a name="method-fieldid"></a><span data-ttu-id="debd9-135">メソッド fieldID</span><span class="sxs-lookup"><span data-stu-id="debd9-135">Method fieldID</span></span>

```xpp
public int fieldID()
```

### <a name="return-value---fieldid"></a><span data-ttu-id="debd9-136">戻り値 - fieldID</span><span class="sxs-lookup"><span data-stu-id="debd9-136">Return Value - fieldID</span></span>

## <a name="method-tableselector"></a><span data-ttu-id="debd9-137">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="debd9-137">Method tableSelector</span></span>

```xpp
public TableId tableSelector([TableId tableSelector])
```

### <a name="parameters---tableselector"></a><span data-ttu-id="debd9-138">パラメーター - tableSelector</span><span class="sxs-lookup"><span data-stu-id="debd9-138">Parameters - tableSelector</span></span>

<span data-ttu-id="debd9-139">tableSelector</span><span class="sxs-lookup"><span data-stu-id="debd9-139">tableSelector</span></span>  

### <a name="return-value---tableselector"></a><span data-ttu-id="debd9-140">戻り値 - tableSelector</span><span class="sxs-lookup"><span data-stu-id="debd9-140">Return Value - tableSelector</span></span>

## <a name="method-finalize"></a><span data-ttu-id="debd9-141">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="debd9-141">Method finalize</span></span>

```xpp
public void finalize()
```

