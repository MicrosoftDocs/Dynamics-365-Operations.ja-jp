---
title: NumberSequence クラス
description: このトピックでは、SecurityPolicy クラスについて説明します。
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
ms.openlocfilehash: b9c14759063527bce8fa04af114ddcaf76d7704b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502568"
---
# <a name="class-numbersequence"></a><span data-ttu-id="ec33d-103">クラス NumberSequence</span><span class="sxs-lookup"><span data-stu-id="ec33d-103">Class NumberSequence</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class NumberSequence extends Object
```

## <a name="remarks"></a><span data-ttu-id="ec33d-104">備考</span><span class="sxs-lookup"><span data-stu-id="ec33d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ec33d-105">例</span><span class="sxs-lookup"><span data-stu-id="ec33d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ec33d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ec33d-106">Methods</span></span>

| <span data-ttu-id="ec33d-107">方法</span><span class="sxs-lookup"><span data-stu-id="ec33d-107">Method</span></span>                                                                                                                                                                | <span data-ttu-id="ec33d-108">説明</span><span class="sxs-lookup"><span data-stu-id="ec33d-108">Description</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ec33d-109">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span><span class="sxs-lookup"><span data-stu-id="ec33d-109">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span></span> |                                                         |
| <span data-ttu-id="ec33d-110">public void new()</span><span class="sxs-lookup"><span data-stu-id="ec33d-110">public void new()</span></span>                                                                                                                                                     | <span data-ttu-id="ec33d-111">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ec33d-111">Initializes a new instance of the NumberSequence class.</span></span> |

## <a name="method-getnextnumber"></a><span data-ttu-id="ec33d-112">メソッド getNextNumber</span><span class="sxs-lookup"><span data-stu-id="ec33d-112">Method getNextNumber</span></span>

```xpp
public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)
```

### <a name="parameters---getnextnumber"></a><span data-ttu-id="ec33d-113">パラメーター - getNextNumber</span><span class="sxs-lookup"><span data-stu-id="ec33d-113">Parameters - getNextNumber</span></span>

<span data-ttu-id="ec33d-114">connection</span><span class="sxs-lookup"><span data-stu-id="ec33d-114">connection</span></span>  

<!-- -->

<span data-ttu-id="ec33d-115">numbersequencerecordid</span><span class="sxs-lookup"><span data-stu-id="ec33d-115">numbersequencerecordid</span></span>  

<!-- -->

<span data-ttu-id="ec33d-116">globaltransid</span><span class="sxs-lookup"><span data-stu-id="ec33d-116">globaltransid</span></span>  

<!-- -->

<span data-ttu-id="ec33d-117">userid</span><span class="sxs-lookup"><span data-stu-id="ec33d-117">userid</span></span>  

<!-- -->

<span data-ttu-id="ec33d-118">sessionid</span><span class="sxs-lookup"><span data-stu-id="ec33d-118">sessionid</span></span>  

<!-- -->

<span data-ttu-id="ec33d-119">sessionLoginDateTime</span><span class="sxs-lookup"><span data-stu-id="ec33d-119">sessionLoginDateTime</span></span>  

### <a name="return-value---getnextnumber"></a><span data-ttu-id="ec33d-120">返り値 - getNextNumber</span><span class="sxs-lookup"><span data-stu-id="ec33d-120">Return Value - getNextNumber</span></span>

## <a name="method-new"></a><span data-ttu-id="ec33d-121">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ec33d-121">Method new</span></span>

<span data-ttu-id="ec33d-122">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ec33d-122">Initializes a new instance of the NumberSequence class.</span></span>

```xpp
public void new()
```

