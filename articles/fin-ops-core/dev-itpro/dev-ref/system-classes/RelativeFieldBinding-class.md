---
title: RelativeFieldBinding クラス
description: このトピックでは、RelativeFieldBinding クラスについて説明します。
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
ms.openlocfilehash: 13ee2d4bd331854c60c5f38240f7286eaa496dc9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502850"
---
# <a name="class-relativefieldbinding"></a><span data-ttu-id="705eb-103">クラス RelativeFieldBinding</span><span class="sxs-lookup"><span data-stu-id="705eb-103">Class RelativeFieldBinding</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RelativeFieldBinding extends FieldBinding
```

## <a name="remarks"></a><span data-ttu-id="705eb-104">備考</span><span class="sxs-lookup"><span data-stu-id="705eb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="705eb-105">例</span><span class="sxs-lookup"><span data-stu-id="705eb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="705eb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="705eb-106">Methods</span></span>

| <span data-ttu-id="705eb-107">方法</span><span class="sxs-lookup"><span data-stu-id="705eb-107">Method</span></span>                                                                                   | <span data-ttu-id="705eb-108">説明</span><span class="sxs-lookup"><span data-stu-id="705eb-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="705eb-109">public RelationPath relationPath()</span><span class="sxs-lookup"><span data-stu-id="705eb-109">public RelationPath relationPath()</span></span>                                                       |                                                               |
| <span data-ttu-id="705eb-110">::public static RelativeFieldBinding construct(str fieldName, RelationPath relationPath)</span><span class="sxs-lookup"><span data-stu-id="705eb-110">::public static RelativeFieldBinding construct(str fieldName, RelationPath relationPath)</span></span> |                                                               |
| <span data-ttu-id="705eb-111">::public static RelativeFieldBinding create(container packedRelativeFieldBinding)</span><span class="sxs-lookup"><span data-stu-id="705eb-111">::public static RelativeFieldBinding create(container packedRelativeFieldBinding)</span></span>        |                                                               |
| <span data-ttu-id="705eb-112">private void new()</span><span class="sxs-lookup"><span data-stu-id="705eb-112">private void new()</span></span>                                                                       | <span data-ttu-id="705eb-113">RelativeFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="705eb-113">Initializes a new instance of the RelativeFieldBinding class.</span></span> |

## <a name="method-relationpath"></a><span data-ttu-id="705eb-114">メソッド relationPath</span><span class="sxs-lookup"><span data-stu-id="705eb-114">Method relationPath</span></span>

```xpp
public RelationPath relationPath()
```

### <a name="return-value---relationpath"></a><span data-ttu-id="705eb-115">戻り値 - relationPath</span><span class="sxs-lookup"><span data-stu-id="705eb-115">Return Value - relationPath</span></span>

## <a name="method-construct"></a><span data-ttu-id="705eb-116">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="705eb-116">Method construct</span></span>

```xpp
public static RelativeFieldBinding construct(str fieldName, RelationPath relationPath)
```

### <a name="parameters---construct"></a><span data-ttu-id="705eb-117">パラメーター - construct</span><span class="sxs-lookup"><span data-stu-id="705eb-117">Parameters - construct</span></span>

<span data-ttu-id="705eb-118">fieldName</span><span class="sxs-lookup"><span data-stu-id="705eb-118">fieldName</span></span>  

<!-- -->

<span data-ttu-id="705eb-119">relationPath</span><span class="sxs-lookup"><span data-stu-id="705eb-119">relationPath</span></span>  

### <a name="return-value---construct"></a><span data-ttu-id="705eb-120">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="705eb-120">Return Value - construct</span></span>

## <a name="method-create"></a><span data-ttu-id="705eb-121">メソッド create</span><span class="sxs-lookup"><span data-stu-id="705eb-121">Method create</span></span>

```xpp
public static RelativeFieldBinding create(container packedRelativeFieldBinding)
```

### <a name="parameters---create"></a><span data-ttu-id="705eb-122">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="705eb-122">Parameters - create</span></span>

<span data-ttu-id="705eb-123">packedRelativeFieldBinding</span><span class="sxs-lookup"><span data-stu-id="705eb-123">packedRelativeFieldBinding</span></span>  

### <a name="return-value---create"></a><span data-ttu-id="705eb-124">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="705eb-124">Return Value - create</span></span>

## <a name="method-new"></a><span data-ttu-id="705eb-125">メソッド new</span><span class="sxs-lookup"><span data-stu-id="705eb-125">Method new</span></span>

<span data-ttu-id="705eb-126">RelativeFieldBinding クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="705eb-126">Initializes a new instance of the RelativeFieldBinding class.</span></span>

```xpp
private void new()
```

