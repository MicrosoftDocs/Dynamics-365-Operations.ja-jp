---
title: QueryBuildFieldList クラス
description: このトピックでは、QueryBuildFieldList クラスについて説明します。
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
ms.openlocfilehash: 96b8a8de2a3a02e5fc14abc8b010da40ddf53dd4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502867"
---
# <a name="class-querybuildfieldlist"></a><span data-ttu-id="64a70-103">クラス QueryBuildFieldList</span><span class="sxs-lookup"><span data-stu-id="64a70-103">Class QueryBuildFieldList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildFieldList extends TreeNode
```

<span data-ttu-id="64a70-104">QueryBuildFieldList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="64a70-104">The QueryBuildFieldList class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="64a70-105">備考</span><span class="sxs-lookup"><span data-stu-id="64a70-105">Remarks</span></span>

<span data-ttu-id="64a70-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="64a70-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="64a70-107">例</span><span class="sxs-lookup"><span data-stu-id="64a70-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="64a70-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="64a70-108">Methods</span></span>

| <span data-ttu-id="64a70-109">方法</span><span class="sxs-lookup"><span data-stu-id="64a70-109">Method</span></span>                                                                                                 | <span data-ttu-id="64a70-110">説明</span><span class="sxs-lookup"><span data-stu-id="64a70-110">Description</span></span> |
|--------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="64a70-111">public int addAllFields(TableName tableName)</span><span class="sxs-lookup"><span data-stu-id="64a70-111">public int addAllFields(TableName tableName)</span></span>                                                           |             |
| <span data-ttu-id="64a70-112">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="64a70-112">public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\])</span></span> |             |
| <span data-ttu-id="64a70-113">public int dynamic(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="64a70-113">public int dynamic(\[int value\])</span></span>                                                                      |             |
| <span data-ttu-id="64a70-114">public FieldId field(int index)</span><span class="sxs-lookup"><span data-stu-id="64a70-114">public FieldId field(int index)</span></span>                                                                        |             |
| <span data-ttu-id="64a70-115">public int fieldCount()</span><span class="sxs-lookup"><span data-stu-id="64a70-115">public int fieldCount()</span></span>                                                                                |             |
| <span data-ttu-id="64a70-116">public SelectionField fieldKind(int index)</span><span class="sxs-lookup"><span data-stu-id="64a70-116">public SelectionField fieldKind(int index)</span></span>                                                             |             |
| <span data-ttu-id="64a70-117">public TableId tableSelector(int index)</span><span class="sxs-lookup"><span data-stu-id="64a70-117">public TableId tableSelector(int index)</span></span>                                                                |             |
| <span data-ttu-id="64a70-118">public void clearFieldList()</span><span class="sxs-lookup"><span data-stu-id="64a70-118">public void clearFieldList()</span></span>                                                                           |             |

## <a name="method-addallfields"></a><span data-ttu-id="64a70-119">メソッド addAllFields</span><span class="sxs-lookup"><span data-stu-id="64a70-119">Method addAllFields</span></span>

```xpp
public int addAllFields(TableName tableName)
```

### <a name="parameters---addallfields"></a><span data-ttu-id="64a70-120">パラメーター - addAllFields</span><span class="sxs-lookup"><span data-stu-id="64a70-120">Parameters - addAllFields</span></span>

<span data-ttu-id="64a70-121">tableName</span><span class="sxs-lookup"><span data-stu-id="64a70-121">tableName</span></span>  

### <a name="return-value---addallfields"></a><span data-ttu-id="64a70-122">戻り値 - addAllFields</span><span class="sxs-lookup"><span data-stu-id="64a70-122">Return Value - addAllFields</span></span>

## <a name="method-addfield"></a><span data-ttu-id="64a70-123">メソッド addField</span><span class="sxs-lookup"><span data-stu-id="64a70-123">Method addField</span></span>

```xpp
public QueryBuildFieldList addField(FieldId fieldId, [SelectionField fieldType], [int arrayIndex])
```

### <a name="parameters---addfield"></a><span data-ttu-id="64a70-124">パラメーター - addField</span><span class="sxs-lookup"><span data-stu-id="64a70-124">Parameters - addField</span></span>

<span data-ttu-id="64a70-125">fieldId</span><span class="sxs-lookup"><span data-stu-id="64a70-125">fieldId</span></span>  

<!-- -->

<span data-ttu-id="64a70-126">fieldType</span><span class="sxs-lookup"><span data-stu-id="64a70-126">fieldType</span></span>  

<!-- -->

<span data-ttu-id="64a70-127">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="64a70-127">arrayIndex</span></span>  

### <a name="return-value---addfield"></a><span data-ttu-id="64a70-128">戻り値 - addField</span><span class="sxs-lookup"><span data-stu-id="64a70-128">Return Value - addField</span></span>

## <a name="method-dynamic"></a><span data-ttu-id="64a70-129">メソッド dynamic</span><span class="sxs-lookup"><span data-stu-id="64a70-129">Method dynamic</span></span>

```xpp
public int dynamic([int value])
```

### <a name="parameters---dynamic"></a><span data-ttu-id="64a70-130">パラメーター - dynamic</span><span class="sxs-lookup"><span data-stu-id="64a70-130">Parameters - dynamic</span></span>

<span data-ttu-id="64a70-131">値</span><span class="sxs-lookup"><span data-stu-id="64a70-131">value</span></span>  

### <a name="return-value---dynamic"></a><span data-ttu-id="64a70-132">戻り値 - dynamic</span><span class="sxs-lookup"><span data-stu-id="64a70-132">Return Value - dynamic</span></span>

## <a name="method-field"></a><span data-ttu-id="64a70-133">メソッド field</span><span class="sxs-lookup"><span data-stu-id="64a70-133">Method field</span></span>

```xpp
public FieldId field(int index)
```

### <a name="parameters---field"></a><span data-ttu-id="64a70-134">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="64a70-134">Parameters - field</span></span>

<span data-ttu-id="64a70-135">指数</span><span class="sxs-lookup"><span data-stu-id="64a70-135">index</span></span>  

### <a name="return-value---field"></a><span data-ttu-id="64a70-136">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="64a70-136">Return Value - field</span></span>

## <a name="method-fieldcount"></a><span data-ttu-id="64a70-137">メソッド fieldCount</span><span class="sxs-lookup"><span data-stu-id="64a70-137">Method fieldCount</span></span>

```xpp
public int fieldCount()
```

### <a name="return-value---fieldcount"></a><span data-ttu-id="64a70-138">戻り値 - fieldCount</span><span class="sxs-lookup"><span data-stu-id="64a70-138">Return Value - fieldCount</span></span>

## <a name="method-fieldkind"></a><span data-ttu-id="64a70-139">メソッド fieldKind</span><span class="sxs-lookup"><span data-stu-id="64a70-139">Method fieldKind</span></span>

```xpp
public SelectionField fieldKind(int index)
```

### <a name="parameters---fieldkind"></a><span data-ttu-id="64a70-140">パラメーター - fieldKind</span><span class="sxs-lookup"><span data-stu-id="64a70-140">Parameters - fieldKind</span></span>

<span data-ttu-id="64a70-141">指数</span><span class="sxs-lookup"><span data-stu-id="64a70-141">index</span></span>  

### <a name="return-value---fieldkind"></a><span data-ttu-id="64a70-142">戻り値 - fieldKind</span><span class="sxs-lookup"><span data-stu-id="64a70-142">Return Value - fieldKind</span></span>

## <a name="method-tableselector"></a><span data-ttu-id="64a70-143">メソッド tableSelector</span><span class="sxs-lookup"><span data-stu-id="64a70-143">Method tableSelector</span></span>

```xpp
public TableId tableSelector(int index)
```

### <a name="parameters---tableselector"></a><span data-ttu-id="64a70-144">パラメーター - tableSelector</span><span class="sxs-lookup"><span data-stu-id="64a70-144">Parameters - tableSelector</span></span>

<span data-ttu-id="64a70-145">指数</span><span class="sxs-lookup"><span data-stu-id="64a70-145">index</span></span>  

### <a name="return-value---tableselector"></a><span data-ttu-id="64a70-146">戻り値 - tableSelector</span><span class="sxs-lookup"><span data-stu-id="64a70-146">Return Value - tableSelector</span></span>

## <a name="method-clearfieldlist"></a><span data-ttu-id="64a70-147">メソッド clearFieldList</span><span class="sxs-lookup"><span data-stu-id="64a70-147">Method clearFieldList</span></span>

```xpp
public void clearFieldList()
```

