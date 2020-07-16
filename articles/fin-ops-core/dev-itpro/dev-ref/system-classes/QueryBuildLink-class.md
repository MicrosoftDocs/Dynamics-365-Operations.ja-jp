---
title: QueryBuildLink クラス
description: このトピックでは、QueryBuildLink クラスについて説明します。
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
ms.openlocfilehash: b0c1b10d5ecc0d70b6389d4f667a5eb9557ffdd7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502865"
---
# <a name="class-querybuildlink"></a><span data-ttu-id="80166-103">クラス QueryBuildLink</span><span class="sxs-lookup"><span data-stu-id="80166-103">Class QueryBuildLink</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildLink extends TreeNode
```

<span data-ttu-id="80166-104">QueryBuildLink クラスは、X++ コードおよびメタデータの作成、読み取り、更新、および削除を可能にします。</span><span class="sxs-lookup"><span data-stu-id="80166-104">The QueryBuildLink class enables for the creating, reading, updating, and deleting of X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="80166-105">備考</span><span class="sxs-lookup"><span data-stu-id="80166-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="80166-106">例</span><span class="sxs-lookup"><span data-stu-id="80166-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="80166-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="80166-107">Methods</span></span>

| <span data-ttu-id="80166-108">方法</span><span class="sxs-lookup"><span data-stu-id="80166-108">Method</span></span>                      | <span data-ttu-id="80166-109">説明</span><span class="sxs-lookup"><span data-stu-id="80166-109">Description</span></span> |
|-----------------------------|-------------|
| <span data-ttu-id="80166-110">public int delete()</span><span class="sxs-lookup"><span data-stu-id="80166-110">public int delete()</span></span>         |             |
| <span data-ttu-id="80166-111">public int field()</span><span class="sxs-lookup"><span data-stu-id="80166-111">public int field()</span></span>          |             |
| <span data-ttu-id="80166-112">public boolean incomplete()</span><span class="sxs-lookup"><span data-stu-id="80166-112">public boolean incomplete()</span></span> |             |
| <span data-ttu-id="80166-113">public str joinRelation()</span><span class="sxs-lookup"><span data-stu-id="80166-113">public str joinRelation()</span></span>   |             |
| <span data-ttu-id="80166-114">public int relatedField()</span><span class="sxs-lookup"><span data-stu-id="80166-114">public int relatedField()</span></span>   |             |
| <span data-ttu-id="80166-115">public int relatedTable()</span><span class="sxs-lookup"><span data-stu-id="80166-115">public int relatedTable()</span></span>   |             |
| <span data-ttu-id="80166-116">public int table()</span><span class="sxs-lookup"><span data-stu-id="80166-116">public int table()</span></span>          |             |
| <span data-ttu-id="80166-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="80166-117">public void finalize()</span></span>      |             |

## <a name="method-delete"></a><span data-ttu-id="80166-118">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="80166-118">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="80166-119">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="80166-119">Return Value - delete</span></span>

## <a name="method-field"></a><span data-ttu-id="80166-120">メソッド field</span><span class="sxs-lookup"><span data-stu-id="80166-120">Method field</span></span>

```xpp
public int field()
```

### <a name="return-value---field"></a><span data-ttu-id="80166-121">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="80166-121">Return Value - field</span></span>

## <a name="method-incomplete"></a><span data-ttu-id="80166-122">メソッド incomplete</span><span class="sxs-lookup"><span data-stu-id="80166-122">Method incomplete</span></span>

```xpp
public boolean incomplete()
```

### <a name="return-value---incomplete"></a><span data-ttu-id="80166-123">戻り値 - incomplete</span><span class="sxs-lookup"><span data-stu-id="80166-123">Return Value - incomplete</span></span>

## <a name="method-joinrelation"></a><span data-ttu-id="80166-124">メソッド joinRelation</span><span class="sxs-lookup"><span data-stu-id="80166-124">Method joinRelation</span></span>

```xpp
public str joinRelation()
```

### <a name="return-value---joinrelation"></a><span data-ttu-id="80166-125">戻り値 - joinRelation</span><span class="sxs-lookup"><span data-stu-id="80166-125">Return Value - joinRelation</span></span>

## <a name="method-relatedfield"></a><span data-ttu-id="80166-126">メソッド relatedField</span><span class="sxs-lookup"><span data-stu-id="80166-126">Method relatedField</span></span>

```xpp
public int relatedField()
```

### <a name="return-value---relatedfield"></a><span data-ttu-id="80166-127">戻り値 - relatedField</span><span class="sxs-lookup"><span data-stu-id="80166-127">Return Value - relatedField</span></span>

## <a name="method-relatedtable"></a><span data-ttu-id="80166-128">メソッド relatedTable</span><span class="sxs-lookup"><span data-stu-id="80166-128">Method relatedTable</span></span>

```xpp
public int relatedTable()
```

### <a name="return-value---relatedtable"></a><span data-ttu-id="80166-129">戻り値 - relatedTable</span><span class="sxs-lookup"><span data-stu-id="80166-129">Return Value - relatedTable</span></span>

## <a name="method-table"></a><span data-ttu-id="80166-130">メソッド table</span><span class="sxs-lookup"><span data-stu-id="80166-130">Method table</span></span>

```xpp
public int table()
```

### <a name="return-value---table"></a><span data-ttu-id="80166-131">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="80166-131">Return Value - table</span></span>

## <a name="method-finalize"></a><span data-ttu-id="80166-132">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="80166-132">Method finalize</span></span>

```xpp
public void finalize()
```

