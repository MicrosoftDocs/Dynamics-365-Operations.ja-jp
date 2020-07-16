---
title: FormDesignView クラス
description: このトピックでは、FormDesignView クラスについて説明します。
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
ms.openlocfilehash: 25d8b6974cbd766d02c2337a3fb5b0ba40467387
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502946"
---
# <a name="class-formdesignview"></a><span data-ttu-id="5e8cb-103">クラス FormDesignView</span><span class="sxs-lookup"><span data-stu-id="5e8cb-103">Class FormDesignView</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDesignView extends ObjectRun
```

## <a name="remarks"></a><span data-ttu-id="5e8cb-104">備考</span><span class="sxs-lookup"><span data-stu-id="5e8cb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5e8cb-105">例</span><span class="sxs-lookup"><span data-stu-id="5e8cb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5e8cb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5e8cb-106">Methods</span></span>

| <span data-ttu-id="5e8cb-107">方法</span><span class="sxs-lookup"><span data-stu-id="5e8cb-107">Method</span></span>                                                 | <span data-ttu-id="5e8cb-108">説明</span><span class="sxs-lookup"><span data-stu-id="5e8cb-108">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="5e8cb-109">public FormBuildDesign design(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5e8cb-109">public FormBuildDesign design(\[int value\])</span></span>           |                                                 |
| <span data-ttu-id="5e8cb-110">public Form form(\[Form value\])</span><span class="sxs-lookup"><span data-stu-id="5e8cb-110">public Form form(\[Form value\])</span></span>                       |                                                 |
| <span data-ttu-id="5e8cb-111">public str name()</span><span class="sxs-lookup"><span data-stu-id="5e8cb-111">public str name()</span></span>                                      |                                                 |
| <span data-ttu-id="5e8cb-112">public FormBuildObjectSet objectPool(\[AnyType pool\])</span><span class="sxs-lookup"><span data-stu-id="5e8cb-112">public FormBuildObjectSet objectPool(\[AnyType pool\])</span></span> |                                                 |
| <span data-ttu-id="5e8cb-113">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="5e8cb-113">public void finalize()</span></span>                                 |                                                 |
| <span data-ttu-id="5e8cb-114">public void new(\[str name\], \[Form form\])</span><span class="sxs-lookup"><span data-stu-id="5e8cb-114">public void new(\[str name\], \[Form form\])</span></span>           | <span data-ttu-id="5e8cb-115">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5e8cb-115">Initializes a new instance of the Object class.</span></span> |

## <a name="method-design"></a><span data-ttu-id="5e8cb-116">メソッド design</span><span class="sxs-lookup"><span data-stu-id="5e8cb-116">Method design</span></span>

```xpp
public FormBuildDesign design([int value])
```

### <a name="parameters---design"></a><span data-ttu-id="5e8cb-117">パラメーター - design</span><span class="sxs-lookup"><span data-stu-id="5e8cb-117">Parameters - design</span></span>

<span data-ttu-id="5e8cb-118">値</span><span class="sxs-lookup"><span data-stu-id="5e8cb-118">value</span></span>  

### <a name="return-value---design"></a><span data-ttu-id="5e8cb-119">戻り値 - design</span><span class="sxs-lookup"><span data-stu-id="5e8cb-119">Return Value - design</span></span>

## <a name="method-form"></a><span data-ttu-id="5e8cb-120">メソッド form</span><span class="sxs-lookup"><span data-stu-id="5e8cb-120">Method form</span></span>

```xpp
public Form form([Form value])
```

### <a name="parameters---form"></a><span data-ttu-id="5e8cb-121">パラメーター - form</span><span class="sxs-lookup"><span data-stu-id="5e8cb-121">Parameters - form</span></span>

<span data-ttu-id="5e8cb-122">値</span><span class="sxs-lookup"><span data-stu-id="5e8cb-122">value</span></span>  

### <a name="return-value---form"></a><span data-ttu-id="5e8cb-123">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="5e8cb-123">Return Value - form</span></span>

## <a name="method-name"></a><span data-ttu-id="5e8cb-124">メソッド名</span><span class="sxs-lookup"><span data-stu-id="5e8cb-124">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="5e8cb-125">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="5e8cb-125">Return Value - name</span></span>

## <a name="method-objectpool"></a><span data-ttu-id="5e8cb-126">メソッド objectPool</span><span class="sxs-lookup"><span data-stu-id="5e8cb-126">Method objectPool</span></span>

```xpp
public FormBuildObjectSet objectPool([AnyType pool])
```

### <a name="parameters---objectpool"></a><span data-ttu-id="5e8cb-127">パラメーター - objectPool</span><span class="sxs-lookup"><span data-stu-id="5e8cb-127">Parameters - objectPool</span></span>

<span data-ttu-id="5e8cb-128">管理グループ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-128">pool</span></span>  

### <a name="return-value---objectpool"></a><span data-ttu-id="5e8cb-129">戻り値 - objectPool</span><span class="sxs-lookup"><span data-stu-id="5e8cb-129">Return Value - objectPool</span></span>

## <a name="method-finalize"></a><span data-ttu-id="5e8cb-130">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="5e8cb-130">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="5e8cb-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5e8cb-131">Method new</span></span>

<span data-ttu-id="5e8cb-132">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5e8cb-132">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([str name], [Form form])
```

### <a name="parameters---new"></a><span data-ttu-id="5e8cb-133">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5e8cb-133">Parameters - new</span></span>

<span data-ttu-id="5e8cb-134">名前</span><span class="sxs-lookup"><span data-stu-id="5e8cb-134">name</span></span>  

<!-- -->

<span data-ttu-id="5e8cb-135">フォーム</span><span class="sxs-lookup"><span data-stu-id="5e8cb-135">form</span></span>  

