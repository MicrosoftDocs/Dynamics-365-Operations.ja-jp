---
title: SecurityContext クラス
description: このトピックでは、SecurityContext クラスについて説明します。
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
ms.openlocfilehash: 25cd9a5c6c79e919123df223af8558c8c4823c54
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502813"
---
# <a name="class-securitycontext"></a><span data-ttu-id="d8355-103">クラス SecurityContext</span><span class="sxs-lookup"><span data-stu-id="d8355-103">Class SecurityContext</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityContext extends Object
```

## <a name="remarks"></a><span data-ttu-id="d8355-104">備考</span><span class="sxs-lookup"><span data-stu-id="d8355-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d8355-105">例</span><span class="sxs-lookup"><span data-stu-id="d8355-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d8355-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d8355-106">Methods</span></span>

| <span data-ttu-id="d8355-107">方法</span><span class="sxs-lookup"><span data-stu-id="d8355-107">Method</span></span>                                                                                                | <span data-ttu-id="d8355-108">説明</span><span class="sxs-lookup"><span data-stu-id="d8355-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="d8355-109">public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="d8355-109">public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\])</span></span> |             |
| <span data-ttu-id="d8355-110">::public static SecurityContext current()</span><span class="sxs-lookup"><span data-stu-id="d8355-110">::public static SecurityContext current()</span></span>                                                             |             |
| <span data-ttu-id="d8355-111">::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)</span><span class="sxs-lookup"><span data-stu-id="d8355-111">::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)</span></span>  |             |
| <span data-ttu-id="d8355-112">public boolean equal(SecurityContext context)</span><span class="sxs-lookup"><span data-stu-id="d8355-112">public boolean equal(SecurityContext context)</span></span>                                                         |             |
| <span data-ttu-id="d8355-113">public SecurableType securableType()</span><span class="sxs-lookup"><span data-stu-id="d8355-113">public SecurableType securableType()</span></span>                                                                  |             |
| <span data-ttu-id="d8355-114">public str securableName()</span><span class="sxs-lookup"><span data-stu-id="d8355-114">public str securableName()</span></span>                                                                            |             |
| <span data-ttu-id="d8355-115">public str securableChildName()</span><span class="sxs-lookup"><span data-stu-id="d8355-115">public str securableChildName()</span></span>                                                                       |             |
| <span data-ttu-id="d8355-116">public void push()</span><span class="sxs-lookup"><span data-stu-id="d8355-116">public void push()</span></span>                                                                                    |             |
| <span data-ttu-id="d8355-117">::public static void pop()</span><span class="sxs-lookup"><span data-stu-id="d8355-117">::public static void pop()</span></span>                                                                            |             |
| <span data-ttu-id="d8355-118">private void new()</span><span class="sxs-lookup"><span data-stu-id="d8355-118">private void new()</span></span>                                                                                    |             |

## <a name="method-istableoperationallowed"></a><span data-ttu-id="d8355-119">メソッド isTableOperationAllowed</span><span class="sxs-lookup"><span data-stu-id="d8355-119">Method isTableOperationAllowed</span></span>

```xpp
public boolean isTableOperationAllowed(int tableId, StatementType operation, [DataAreaId dataArea])
```

### <a name="parameters---istableoperationallowed"></a><span data-ttu-id="d8355-120">パラメーター - isTableOperationAllowed</span><span class="sxs-lookup"><span data-stu-id="d8355-120">Parameters - isTableOperationAllowed</span></span>

<span data-ttu-id="d8355-121">tableId</span><span class="sxs-lookup"><span data-stu-id="d8355-121">tableId</span></span>  

<!-- -->

<span data-ttu-id="d8355-122">工程</span><span class="sxs-lookup"><span data-stu-id="d8355-122">operation</span></span>  

<!-- -->

<span data-ttu-id="d8355-123">dataArea</span><span class="sxs-lookup"><span data-stu-id="d8355-123">dataArea</span></span>  

### <a name="return-value---istableoperationallowed"></a><span data-ttu-id="d8355-124">戻り値 - isTableOperationAllowed</span><span class="sxs-lookup"><span data-stu-id="d8355-124">Return Value - isTableOperationAllowed</span></span>

## <a name="method-current"></a><span data-ttu-id="d8355-125">メソッド current</span><span class="sxs-lookup"><span data-stu-id="d8355-125">Method current</span></span>

```xpp
public static SecurityContext current()
```

### <a name="return-value---current"></a><span data-ttu-id="d8355-126">戻り値 - current</span><span class="sxs-lookup"><span data-stu-id="d8355-126">Return Value - current</span></span>

## <a name="method-constructfromentrypoint"></a><span data-ttu-id="d8355-127">メソッド constructFromEntryPoint</span><span class="sxs-lookup"><span data-stu-id="d8355-127">Method constructFromEntryPoint</span></span>

```xpp
public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)
```

### <a name="parameters---constructfromentrypoint"></a><span data-ttu-id="d8355-128">パラメーター - constructFromEntryPoint</span><span class="sxs-lookup"><span data-stu-id="d8355-128">Parameters - constructFromEntryPoint</span></span>

<span data-ttu-id="d8355-129">タイプ</span><span class="sxs-lookup"><span data-stu-id="d8355-129">type</span></span>  

<!-- -->

<span data-ttu-id="d8355-130">名前</span><span class="sxs-lookup"><span data-stu-id="d8355-130">name</span></span>  

<!-- -->

<span data-ttu-id="d8355-131">childName</span><span class="sxs-lookup"><span data-stu-id="d8355-131">childName</span></span>  

### <a name="return-value---constructfromentrypoint"></a><span data-ttu-id="d8355-132">戻り値 - constructFromEntryPoint</span><span class="sxs-lookup"><span data-stu-id="d8355-132">Return Value - constructFromEntryPoint</span></span>

## <a name="method-equal"></a><span data-ttu-id="d8355-133">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="d8355-133">Method equal</span></span>

```xpp
public boolean equal(SecurityContext context)
```

### <a name="parameters---equal"></a><span data-ttu-id="d8355-134">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="d8355-134">Parameters - equal</span></span>

<span data-ttu-id="d8355-135">context</span><span class="sxs-lookup"><span data-stu-id="d8355-135">context</span></span>  

### <a name="return-value---equal"></a><span data-ttu-id="d8355-136">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="d8355-136">Return Value - equal</span></span>

## <a name="method-securabletype"></a><span data-ttu-id="d8355-137">メソッド securableType</span><span class="sxs-lookup"><span data-stu-id="d8355-137">Method securableType</span></span>

```xpp
public SecurableType securableType()
```

### <a name="return-value---securabletype"></a><span data-ttu-id="d8355-138">戻り値 - securableType</span><span class="sxs-lookup"><span data-stu-id="d8355-138">Return Value - securableType</span></span>

## <a name="method-securablename"></a><span data-ttu-id="d8355-139">メソッド securableName</span><span class="sxs-lookup"><span data-stu-id="d8355-139">Method securableName</span></span>

```xpp
public str securableName()
```

### <a name="return-value---securablename"></a><span data-ttu-id="d8355-140">戻り値 - securableName</span><span class="sxs-lookup"><span data-stu-id="d8355-140">Return Value - securableName</span></span>

## <a name="method-securablechildname"></a><span data-ttu-id="d8355-141">メソッド securableChildName</span><span class="sxs-lookup"><span data-stu-id="d8355-141">Method securableChildName</span></span>

```xpp
public str securableChildName()
```

### <a name="return-value---securablechildname"></a><span data-ttu-id="d8355-142">戻り値 - securableChildName</span><span class="sxs-lookup"><span data-stu-id="d8355-142">Return Value - securableChildName</span></span>

## <a name="method-push"></a><span data-ttu-id="d8355-143">メソッド push</span><span class="sxs-lookup"><span data-stu-id="d8355-143">Method push</span></span>

```xpp
public void push()
```

## <a name="method-pop"></a><span data-ttu-id="d8355-144">メソッド pop</span><span class="sxs-lookup"><span data-stu-id="d8355-144">Method pop</span></span>

```xpp
public static void pop()
```

## <a name="method-new"></a><span data-ttu-id="d8355-145">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d8355-145">Method new</span></span>

```xpp
private void new()
```

