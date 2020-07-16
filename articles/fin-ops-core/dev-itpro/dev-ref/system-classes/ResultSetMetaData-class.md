---
title: ResultSetMetaData クラス
description: このトピックでは、ResultSetMetaData クラスについて説明します。
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
ms.openlocfilehash: ffed55c3fa017e132105e4b799588d26206629a4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502822"
---
# <a name="class-resultsetmetadata"></a><span data-ttu-id="9a4aa-103">クラス ResultSetMetaData</span><span class="sxs-lookup"><span data-stu-id="9a4aa-103">Class ResultSetMetaData</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ResultSetMetaData extends Object
```

## <a name="remarks"></a><span data-ttu-id="9a4aa-104">備考</span><span class="sxs-lookup"><span data-stu-id="9a4aa-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9a4aa-105">例</span><span class="sxs-lookup"><span data-stu-id="9a4aa-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9a4aa-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9a4aa-106">Methods</span></span>

| <span data-ttu-id="9a4aa-107">方法</span><span class="sxs-lookup"><span data-stu-id="9a4aa-107">Method</span></span>                                        | <span data-ttu-id="9a4aa-108">説明</span><span class="sxs-lookup"><span data-stu-id="9a4aa-108">Description</span></span> |
|-----------------------------------------------|-------------|
| <span data-ttu-id="9a4aa-109">public int getColumnCount()</span><span class="sxs-lookup"><span data-stu-id="9a4aa-109">public int getColumnCount()</span></span>                   |             |
| <span data-ttu-id="9a4aa-110">public int getColumnDisplaySize(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-110">public int getColumnDisplaySize(int ColumnID)</span></span> |             |
| <span data-ttu-id="9a4aa-111">public str getColumnName(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-111">public str getColumnName(int ColumnID)</span></span>        |             |
| <span data-ttu-id="9a4aa-112">public int getColumnType(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-112">public int getColumnType(int ColumnID)</span></span>        |             |
| <span data-ttu-id="9a4aa-113">public int getPrecision(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-113">public int getPrecision(int ColumnID)</span></span>         |             |
| <span data-ttu-id="9a4aa-114">public int getScale(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-114">public int getScale(int ColumnID)</span></span>             |             |
| <span data-ttu-id="9a4aa-115">public int isNullable(int ColumnID)</span><span class="sxs-lookup"><span data-stu-id="9a4aa-115">public int isNullable(int ColumnID)</span></span>           |             |

## <a name="method-getcolumncount"></a><span data-ttu-id="9a4aa-116">メソッド getColumnCount</span><span class="sxs-lookup"><span data-stu-id="9a4aa-116">Method getColumnCount</span></span>

```xpp
public int getColumnCount()
```

### <a name="return-value---getcolumncount"></a><span data-ttu-id="9a4aa-117">戻り値 - getColumnCount</span><span class="sxs-lookup"><span data-stu-id="9a4aa-117">Return Value - getColumnCount</span></span>

## <a name="method-getcolumndisplaysize"></a><span data-ttu-id="9a4aa-118">メソッド getColumnDisplaySize</span><span class="sxs-lookup"><span data-stu-id="9a4aa-118">Method getColumnDisplaySize</span></span>

```xpp
public int getColumnDisplaySize(int ColumnID)
```

### <a name="parameters---getcolumndisplaysize"></a><span data-ttu-id="9a4aa-119">パラメーター - getColumnDisplaySize</span><span class="sxs-lookup"><span data-stu-id="9a4aa-119">Parameters - getColumnDisplaySize</span></span>

<span data-ttu-id="9a4aa-120">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-120">ColumnID</span></span>  

### <a name="return-value---getcolumndisplaysize"></a><span data-ttu-id="9a4aa-121">戻り値 - getColumnDisplaySize</span><span class="sxs-lookup"><span data-stu-id="9a4aa-121">Return Value - getColumnDisplaySize</span></span>

## <a name="method-getcolumnname"></a><span data-ttu-id="9a4aa-122">メソッド getColumnName</span><span class="sxs-lookup"><span data-stu-id="9a4aa-122">Method getColumnName</span></span>

```xpp
public str getColumnName(int ColumnID)
```

### <a name="parameters---getcolumnname"></a><span data-ttu-id="9a4aa-123">パラメーター - getColumnName</span><span class="sxs-lookup"><span data-stu-id="9a4aa-123">Parameters - getColumnName</span></span>

<span data-ttu-id="9a4aa-124">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-124">ColumnID</span></span>  

### <a name="return-value---getcolumnname"></a><span data-ttu-id="9a4aa-125">戻り値 - getColumnName</span><span class="sxs-lookup"><span data-stu-id="9a4aa-125">Return Value - getColumnName</span></span>

## <a name="method-getcolumntype"></a><span data-ttu-id="9a4aa-126">メソッド getColumnType</span><span class="sxs-lookup"><span data-stu-id="9a4aa-126">Method getColumnType</span></span>

```xpp
public int getColumnType(int ColumnID)
```

### <a name="parameters---getcolumntype"></a><span data-ttu-id="9a4aa-127">パラメーター - getColumnType</span><span class="sxs-lookup"><span data-stu-id="9a4aa-127">Parameters - getColumnType</span></span>

<span data-ttu-id="9a4aa-128">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-128">ColumnID</span></span>  

### <a name="return-value---getcolumntype"></a><span data-ttu-id="9a4aa-129">戻り値 - getColumnType</span><span class="sxs-lookup"><span data-stu-id="9a4aa-129">Return Value - getColumnType</span></span>

## <a name="method-getprecision"></a><span data-ttu-id="9a4aa-130">メソッド getPrecision</span><span class="sxs-lookup"><span data-stu-id="9a4aa-130">Method getPrecision</span></span>

```xpp
public int getPrecision(int ColumnID)
```

### <a name="parameters---getprecision"></a><span data-ttu-id="9a4aa-131">パラメーター - getPrecision</span><span class="sxs-lookup"><span data-stu-id="9a4aa-131">Parameters - getPrecision</span></span>

<span data-ttu-id="9a4aa-132">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-132">ColumnID</span></span>  

### <a name="return-value---getprecision"></a><span data-ttu-id="9a4aa-133">戻り値 - getPrecision</span><span class="sxs-lookup"><span data-stu-id="9a4aa-133">Return Value - getPrecision</span></span>

## <a name="method-getscale"></a><span data-ttu-id="9a4aa-134">メソッド getScale</span><span class="sxs-lookup"><span data-stu-id="9a4aa-134">Method getScale</span></span>

```xpp
public int getScale(int ColumnID)
```

### <a name="parameters---getscale"></a><span data-ttu-id="9a4aa-135">パラメーター - getScale</span><span class="sxs-lookup"><span data-stu-id="9a4aa-135">Parameters - getScale</span></span>

<span data-ttu-id="9a4aa-136">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-136">ColumnID</span></span>  

### <a name="return-value---getscale"></a><span data-ttu-id="9a4aa-137">戻り値 - getScale</span><span class="sxs-lookup"><span data-stu-id="9a4aa-137">Return Value - getScale</span></span>

## <a name="method-isnullable"></a><span data-ttu-id="9a4aa-138">メソッド isNullable</span><span class="sxs-lookup"><span data-stu-id="9a4aa-138">Method isNullable</span></span>

```xpp
public int isNullable(int ColumnID)
```

### <a name="parameters---isnullable"></a><span data-ttu-id="9a4aa-139">パラメーター - isNullable</span><span class="sxs-lookup"><span data-stu-id="9a4aa-139">Parameters - isNullable</span></span>

<span data-ttu-id="9a4aa-140">ColumnID</span><span class="sxs-lookup"><span data-stu-id="9a4aa-140">ColumnID</span></span>  

### <a name="return-value---isnullable"></a><span data-ttu-id="9a4aa-141">戻り値 - isNullable</span><span class="sxs-lookup"><span data-stu-id="9a4aa-141">Return Value - isNullable</span></span>

