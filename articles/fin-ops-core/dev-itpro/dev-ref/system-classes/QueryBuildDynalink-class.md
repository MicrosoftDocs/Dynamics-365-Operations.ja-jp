---
title: QueryBuildDynalink クラス
description: このトピックでは、QueryBuildDynalink クラスについて説明します。
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
ms.openlocfilehash: 53e43d748f93f35443640b237c22f296db24a84e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502866"
---
# <a name="class-querybuilddynalink"></a><span data-ttu-id="3a25c-103">クラス QueryBuildDynalink</span><span class="sxs-lookup"><span data-stu-id="3a25c-103">Class QueryBuildDynalink</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildDynalink extends Object
```

## <a name="remarks"></a><span data-ttu-id="3a25c-104">備考</span><span class="sxs-lookup"><span data-stu-id="3a25c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3a25c-105">例</span><span class="sxs-lookup"><span data-stu-id="3a25c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3a25c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3a25c-106">Methods</span></span>

| <span data-ttu-id="3a25c-107">方法</span><span class="sxs-lookup"><span data-stu-id="3a25c-107">Method</span></span>                                                | <span data-ttu-id="3a25c-108">説明</span><span class="sxs-lookup"><span data-stu-id="3a25c-108">Description</span></span> |
|-------------------------------------------------------|-------------|
| <span data-ttu-id="3a25c-109">public Common cursor(\[Common cursor\])</span><span class="sxs-lookup"><span data-stu-id="3a25c-109">public Common cursor(\[Common cursor\])</span></span>               |             |
| <span data-ttu-id="3a25c-110">public QueryBuildDataSource dataSource()</span><span class="sxs-lookup"><span data-stu-id="3a25c-110">public QueryBuildDataSource dataSource()</span></span>              |             |
| <span data-ttu-id="3a25c-111">public FieldId dynamicField(\[FieldId dynamicField\])</span><span class="sxs-lookup"><span data-stu-id="3a25c-111">public FieldId dynamicField(\[FieldId dynamicField\])</span></span> |             |
| <span data-ttu-id="3a25c-112">public FieldId field(\[FieldId fieldId\])</span><span class="sxs-lookup"><span data-stu-id="3a25c-112">public FieldId field(\[FieldId fieldId\])</span></span>             |             |
| <span data-ttu-id="3a25c-113">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="3a25c-113">public int fieldArrayIndex()</span></span>                          |             |
| <span data-ttu-id="3a25c-114">public FieldName fieldName()</span><span class="sxs-lookup"><span data-stu-id="3a25c-114">public FieldName fieldName()</span></span>                          |             |
| <span data-ttu-id="3a25c-115">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="3a25c-115">public void finalize()</span></span>                                |             |

## <a name="method-cursor"></a><span data-ttu-id="3a25c-116">メソッド cursor</span><span class="sxs-lookup"><span data-stu-id="3a25c-116">Method cursor</span></span>

```xpp
public Common cursor([Common cursor])
```

### <a name="parameters---cursor"></a><span data-ttu-id="3a25c-117">パラメーター - cursor</span><span class="sxs-lookup"><span data-stu-id="3a25c-117">Parameters - cursor</span></span>

<span data-ttu-id="3a25c-118">cursor</span><span class="sxs-lookup"><span data-stu-id="3a25c-118">cursor</span></span>  

### <a name="return-value---cursor"></a><span data-ttu-id="3a25c-119">戻り値 - cursor</span><span class="sxs-lookup"><span data-stu-id="3a25c-119">Return Value - cursor</span></span>

## <a name="method-datasource"></a><span data-ttu-id="3a25c-120">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="3a25c-120">Method dataSource</span></span>

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="3a25c-121">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="3a25c-121">Return Value - dataSource</span></span>

## <a name="method-dynamicfield"></a><span data-ttu-id="3a25c-122">メソッド dynamicField</span><span class="sxs-lookup"><span data-stu-id="3a25c-122">Method dynamicField</span></span>

```xpp
public FieldId dynamicField([FieldId dynamicField])
```

### <a name="parameters---dynamicfield"></a><span data-ttu-id="3a25c-123">パラメーター - dynamicField</span><span class="sxs-lookup"><span data-stu-id="3a25c-123">Parameters - dynamicField</span></span>

<span data-ttu-id="3a25c-124">dynamicField</span><span class="sxs-lookup"><span data-stu-id="3a25c-124">dynamicField</span></span>  

### <a name="return-value---dynamicfield"></a><span data-ttu-id="3a25c-125">戻り値 - dynamicField</span><span class="sxs-lookup"><span data-stu-id="3a25c-125">Return Value - dynamicField</span></span>

## <a name="method-field"></a><span data-ttu-id="3a25c-126">メソッド field</span><span class="sxs-lookup"><span data-stu-id="3a25c-126">Method field</span></span>

```xpp
public FieldId field([FieldId fieldId])
```

### <a name="parameters---field"></a><span data-ttu-id="3a25c-127">パラメーター - field</span><span class="sxs-lookup"><span data-stu-id="3a25c-127">Parameters - field</span></span>

<span data-ttu-id="3a25c-128">fieldId</span><span class="sxs-lookup"><span data-stu-id="3a25c-128">fieldId</span></span>  

### <a name="return-value---field"></a><span data-ttu-id="3a25c-129">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="3a25c-129">Return Value - field</span></span>

## <a name="method-fieldarrayindex"></a><span data-ttu-id="3a25c-130">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="3a25c-130">Method fieldArrayIndex</span></span>

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a><span data-ttu-id="3a25c-131">戻り値 - fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="3a25c-131">Return Value - fieldArrayIndex</span></span>

## <a name="method-fieldname"></a><span data-ttu-id="3a25c-132">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="3a25c-132">Method fieldName</span></span>

```xpp
public FieldName fieldName()
```

### <a name="return-value---fieldname"></a><span data-ttu-id="3a25c-133">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="3a25c-133">Return Value - fieldName</span></span>

## <a name="method-finalize"></a><span data-ttu-id="3a25c-134">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="3a25c-134">Method finalize</span></span>

```xpp
public void finalize()
```

