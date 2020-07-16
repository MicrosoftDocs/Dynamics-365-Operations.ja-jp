---
title: FieldBinding クラス
description: このトピックでは、FieldBinding クラスについて説明します。
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
ms.openlocfilehash: 9528d2c7ea59bb5fef17ecf6f27b6385dc437c9e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502980"
---
# <a name="class-fieldbinding"></a><span data-ttu-id="e8570-103">クラス FieldBinding</span><span class="sxs-lookup"><span data-stu-id="e8570-103">Class FieldBinding</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FieldBinding extends Object
```

## <a name="remarks"></a><span data-ttu-id="e8570-104">備考</span><span class="sxs-lookup"><span data-stu-id="e8570-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e8570-105">例</span><span class="sxs-lookup"><span data-stu-id="e8570-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e8570-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8570-106">Methods</span></span>

| <span data-ttu-id="e8570-107">方法</span><span class="sxs-lookup"><span data-stu-id="e8570-107">Method</span></span>                                                   | <span data-ttu-id="e8570-108">説明</span><span class="sxs-lookup"><span data-stu-id="e8570-108">Description</span></span>                                                |
|----------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e8570-109">public int fieldArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="e8570-109">public int fieldArrayIndex()</span></span>                             |                                                            |
| <span data-ttu-id="e8570-110">public int fieldId()</span><span class="sxs-lookup"><span data-stu-id="e8570-110">public int fieldId()</span></span>                                     |                                                            |
| <span data-ttu-id="e8570-111">public str fieldName()</span><span class="sxs-lookup"><span data-stu-id="e8570-111">public str fieldName()</span></span>                                   |                                                            |
| <span data-ttu-id="e8570-112">public boolean isEqualTo(FieldBinding otherFieldBinding)</span><span class="sxs-lookup"><span data-stu-id="e8570-112">public boolean isEqualTo(FieldBinding otherFieldBinding)</span></span> |                                                            |
| <span data-ttu-id="e8570-113">public boolean isNull()</span><span class="sxs-lookup"><span data-stu-id="e8570-113">public boolean isNull()</span></span>                                  |                                                            |
| <span data-ttu-id="e8570-114">public boolean isValid()</span><span class="sxs-lookup"><span data-stu-id="e8570-114">public boolean isValid()</span></span>                                 |                                                            |
| <span data-ttu-id="e8570-115">public container pack()</span><span class="sxs-lookup"><span data-stu-id="e8570-115">public container pack()</span></span>                                  | <span data-ttu-id="e8570-116">FieldBinding クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e8570-116">Serializes the current instance of the FieldBinding class.</span></span> |
| <span data-ttu-id="e8570-117">public int tableId()</span><span class="sxs-lookup"><span data-stu-id="e8570-117">public int tableId()</span></span>                                     |                                                            |
| <span data-ttu-id="e8570-118">public str tableName()</span><span class="sxs-lookup"><span data-stu-id="e8570-118">public str tableName()</span></span>                                   |                                                            |
| <span data-ttu-id="e8570-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="e8570-119">public void new()</span></span>                                        | <span data-ttu-id="e8570-120">FieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e8570-120">Initializes a new instance of the FieldBinding class.</span></span>      |

## <a name="method-fieldarrayindex"></a><span data-ttu-id="e8570-121">メソッド fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="e8570-121">Method fieldArrayIndex</span></span>

```xpp
public int fieldArrayIndex()
```

### <a name="return-value---fieldarrayindex"></a><span data-ttu-id="e8570-122">戻り値 - fieldArrayIndex</span><span class="sxs-lookup"><span data-stu-id="e8570-122">Return Value - fieldArrayIndex</span></span>

## <a name="method-fieldid"></a><span data-ttu-id="e8570-123">メソッド fieldId</span><span class="sxs-lookup"><span data-stu-id="e8570-123">Method fieldId</span></span>

```xpp
public int fieldId()
```

### <a name="return-value---fieldid"></a><span data-ttu-id="e8570-124">戻り値 - fieldId</span><span class="sxs-lookup"><span data-stu-id="e8570-124">Return Value - fieldId</span></span>

## <a name="method-fieldname"></a><span data-ttu-id="e8570-125">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="e8570-125">Method fieldName</span></span>

```xpp
public str fieldName()
```

### <a name="return-value---fieldname"></a><span data-ttu-id="e8570-126">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="e8570-126">Return Value - fieldName</span></span>

## <a name="method-isequalto"></a><span data-ttu-id="e8570-127">メソッド isEqualTo</span><span class="sxs-lookup"><span data-stu-id="e8570-127">Method isEqualTo</span></span>

```xpp
public boolean isEqualTo(FieldBinding otherFieldBinding)
```

### <a name="parameters---isequalto"></a><span data-ttu-id="e8570-128">パラメーター - isEqualTo</span><span class="sxs-lookup"><span data-stu-id="e8570-128">Parameters - isEqualTo</span></span>

<span data-ttu-id="e8570-129">otherFieldBinding</span><span class="sxs-lookup"><span data-stu-id="e8570-129">otherFieldBinding</span></span>  

### <a name="return-value---isequalto"></a><span data-ttu-id="e8570-130">戻り値 - isEqualTo</span><span class="sxs-lookup"><span data-stu-id="e8570-130">Return Value - isEqualTo</span></span>

## <a name="method-isnull"></a><span data-ttu-id="e8570-131">メソッド isNull</span><span class="sxs-lookup"><span data-stu-id="e8570-131">Method isNull</span></span>

```xpp
public boolean isNull()
```

### <a name="return-value---isnull"></a><span data-ttu-id="e8570-132">戻り値 - isNull</span><span class="sxs-lookup"><span data-stu-id="e8570-132">Return Value - isNull</span></span>

## <a name="method-isvalid"></a><span data-ttu-id="e8570-133">メソッド isValid</span><span class="sxs-lookup"><span data-stu-id="e8570-133">Method isValid</span></span>

```xpp
public boolean isValid()
```

### <a name="return-value---isvalid"></a><span data-ttu-id="e8570-134">戻り値 - isValid</span><span class="sxs-lookup"><span data-stu-id="e8570-134">Return Value - isValid</span></span>

## <a name="method-pack"></a><span data-ttu-id="e8570-135">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="e8570-135">Method pack</span></span>

<span data-ttu-id="e8570-136">FieldBinding クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="e8570-136">Serializes the current instance of the FieldBinding class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="e8570-137">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="e8570-137">Return Value - pack</span></span>

<span data-ttu-id="e8570-138">FieldBinding クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e8570-138">A container that contains the current instance of the FieldBinding class.</span></span>

## <a name="method-tableid"></a><span data-ttu-id="e8570-139">メソッド tableId</span><span class="sxs-lookup"><span data-stu-id="e8570-139">Method tableId</span></span>

```xpp
public int tableId()
```

### <a name="return-value---tableid"></a><span data-ttu-id="e8570-140">戻り値 - tableId</span><span class="sxs-lookup"><span data-stu-id="e8570-140">Return Value - tableId</span></span>

## <a name="method-tablename"></a><span data-ttu-id="e8570-141">メソッド tableName</span><span class="sxs-lookup"><span data-stu-id="e8570-141">Method tableName</span></span>

```xpp
public str tableName()
```

### <a name="return-value---tablename"></a><span data-ttu-id="e8570-142">戻り値 - tableName</span><span class="sxs-lookup"><span data-stu-id="e8570-142">Return Value - tableName</span></span>

## <a name="method-new"></a><span data-ttu-id="e8570-143">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e8570-143">Method new</span></span>

<span data-ttu-id="e8570-144">FieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e8570-144">Initializes a new instance of the FieldBinding class.</span></span>

```xpp
public void new()
```

