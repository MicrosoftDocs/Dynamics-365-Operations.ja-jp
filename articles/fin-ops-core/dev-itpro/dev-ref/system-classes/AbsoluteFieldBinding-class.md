---
title: AbsoluteFieldBinding クラス
description: このトピックでは、AbsoluteFieldBinding クラスについて説明します。
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
ms.openlocfilehash: 54e97e459ce54d1ec95accd037748e7a17ffb470
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502750"
---
# <a name="class-absolutefieldbinding"></a><span data-ttu-id="34b5c-103">クラス AbsoluteFieldBinding</span><span class="sxs-lookup"><span data-stu-id="34b5c-103">Class AbsoluteFieldBinding</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class AbsoluteFieldBinding extends FieldBinding
```

## <a name="remarks"></a><span data-ttu-id="34b5c-104">備考</span><span class="sxs-lookup"><span data-stu-id="34b5c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="34b5c-105">例</span><span class="sxs-lookup"><span data-stu-id="34b5c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="34b5c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="34b5c-106">Methods</span></span>

| <span data-ttu-id="34b5c-107">方法</span><span class="sxs-lookup"><span data-stu-id="34b5c-107">Method</span></span>                                                                            | <span data-ttu-id="34b5c-108">説明</span><span class="sxs-lookup"><span data-stu-id="34b5c-108">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="34b5c-109">::public static AbsoluteFieldBinding construct(str fieldName, str tableName)</span><span class="sxs-lookup"><span data-stu-id="34b5c-109">::public static AbsoluteFieldBinding construct(str fieldName, str tableName)</span></span>      |                                                               |
| <span data-ttu-id="34b5c-110">::public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)</span><span class="sxs-lookup"><span data-stu-id="34b5c-110">::public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)</span></span> |                                                               |
| <span data-ttu-id="34b5c-111">private void new()</span><span class="sxs-lookup"><span data-stu-id="34b5c-111">private void new()</span></span>                                                                | <span data-ttu-id="34b5c-112">AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="34b5c-112">Initializes a new instance of the AbsoluteFieldBinding class.</span></span> |

## <a name="method-construct"></a><span data-ttu-id="34b5c-113">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="34b5c-113">Method construct</span></span>

```xpp
public static AbsoluteFieldBinding construct(str fieldName, str tableName)
```

### <a name="parameters---construct"></a><span data-ttu-id="34b5c-114">パラメーター - construct</span><span class="sxs-lookup"><span data-stu-id="34b5c-114">Parameters - construct</span></span>

<span data-ttu-id="34b5c-115">fieldName</span><span class="sxs-lookup"><span data-stu-id="34b5c-115">fieldName</span></span>  

<!-- -->

<span data-ttu-id="34b5c-116">tableName</span><span class="sxs-lookup"><span data-stu-id="34b5c-116">tableName</span></span>  

### <a name="return-value---construct"></a><span data-ttu-id="34b5c-117">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="34b5c-117">Return Value - construct</span></span>

## <a name="method-create"></a><span data-ttu-id="34b5c-118">メソッド create</span><span class="sxs-lookup"><span data-stu-id="34b5c-118">Method create</span></span>

```xpp
public static AbsoluteFieldBinding create(container packedAbsoluteFieldBinding)
```

### <a name="parameters---create"></a><span data-ttu-id="34b5c-119">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="34b5c-119">Parameters - create</span></span>

<span data-ttu-id="34b5c-120">packedAbsoluteFieldBinding</span><span class="sxs-lookup"><span data-stu-id="34b5c-120">packedAbsoluteFieldBinding</span></span>  

### <a name="return-value---create"></a><span data-ttu-id="34b5c-121">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="34b5c-121">Return Value - create</span></span>

## <a name="method-new"></a><span data-ttu-id="34b5c-122">メソッド new</span><span class="sxs-lookup"><span data-stu-id="34b5c-122">Method new</span></span>

<span data-ttu-id="34b5c-123">AbsoluteFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="34b5c-123">Initializes a new instance of the AbsoluteFieldBinding class.</span></span>

```xpp
private void new()
```

