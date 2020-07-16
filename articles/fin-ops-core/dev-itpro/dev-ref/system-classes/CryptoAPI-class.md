---
title: CryptoAPI クラス
description: このトピックでは、CryptoAPI クラスについて説明します。
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
ms.openlocfilehash: c8e96c4690752da8c32d077f87f7b181813000e3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502702"
---
# <a name="class-cryptoapi"></a><span data-ttu-id="41999-103">クラス CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="41999-103">Class CryptoAPI</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CryptoAPI extends Object
```

## <a name="remarks"></a><span data-ttu-id="41999-104">備考</span><span class="sxs-lookup"><span data-stu-id="41999-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="41999-105">例</span><span class="sxs-lookup"><span data-stu-id="41999-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="41999-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="41999-106">Methods</span></span>

| <span data-ttu-id="41999-107">方法</span><span class="sxs-lookup"><span data-stu-id="41999-107">Method</span></span>                                   | <span data-ttu-id="41999-108">説明</span><span class="sxs-lookup"><span data-stu-id="41999-108">Description</span></span>                                     |
|------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="41999-109">public container decrypt(container blob)</span><span class="sxs-lookup"><span data-stu-id="41999-109">public container decrypt(container blob)</span></span> |                                                 |
| <span data-ttu-id="41999-110">public container encrypt(container blob)</span><span class="sxs-lookup"><span data-stu-id="41999-110">public container encrypt(container blob)</span></span> |                                                 |
| <span data-ttu-id="41999-111">public container getKey()</span><span class="sxs-lookup"><span data-stu-id="41999-111">public container getKey()</span></span>                |                                                 |
| <span data-ttu-id="41999-112">public Int64 salt()</span><span class="sxs-lookup"><span data-stu-id="41999-112">public Int64 salt()</span></span>                      |                                                 |
| <span data-ttu-id="41999-113">public void new(Int64 salt)</span><span class="sxs-lookup"><span data-stu-id="41999-113">public void new(Int64 salt)</span></span>              | <span data-ttu-id="41999-114">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="41999-114">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="41999-115">::public static void resetKey()</span><span class="sxs-lookup"><span data-stu-id="41999-115">::public static void resetKey()</span></span>          |                                                 |

## <a name="method-decrypt"></a><span data-ttu-id="41999-116">メソッド decrypt</span><span class="sxs-lookup"><span data-stu-id="41999-116">Method decrypt</span></span>

```xpp
public container decrypt(container blob)
```

### <a name="parameters---decrypt"></a><span data-ttu-id="41999-117">パラメーター - decrypt</span><span class="sxs-lookup"><span data-stu-id="41999-117">Parameters - decrypt</span></span>

<span data-ttu-id="41999-118">blob</span><span class="sxs-lookup"><span data-stu-id="41999-118">blob</span></span>  

### <a name="return-value---decrypt"></a><span data-ttu-id="41999-119">戻り値 - decrypt</span><span class="sxs-lookup"><span data-stu-id="41999-119">Return Value - decrypt</span></span>

## <a name="method-encrypt"></a><span data-ttu-id="41999-120">メソッド encrypt</span><span class="sxs-lookup"><span data-stu-id="41999-120">Method encrypt</span></span>

```xpp
public container encrypt(container blob)
```

### <a name="parameters---encrypt"></a><span data-ttu-id="41999-121">パラメーター - encrypt</span><span class="sxs-lookup"><span data-stu-id="41999-121">Parameters - encrypt</span></span>

<span data-ttu-id="41999-122">blob</span><span class="sxs-lookup"><span data-stu-id="41999-122">blob</span></span>  

### <a name="return-value---encrypt"></a><span data-ttu-id="41999-123">戻り値 - encrypt</span><span class="sxs-lookup"><span data-stu-id="41999-123">Return Value - encrypt</span></span>

## <a name="method-getkey"></a><span data-ttu-id="41999-124">メソッド getKey</span><span class="sxs-lookup"><span data-stu-id="41999-124">Method getKey</span></span>

```xpp
public container getKey()
```

### <a name="return-value---getkey"></a><span data-ttu-id="41999-125">戻り値 - getKey</span><span class="sxs-lookup"><span data-stu-id="41999-125">Return Value - getKey</span></span>

## <a name="method-salt"></a><span data-ttu-id="41999-126">メソッド salt</span><span class="sxs-lookup"><span data-stu-id="41999-126">Method salt</span></span>

```xpp
public Int64 salt()
```

### <a name="return-value---salt"></a><span data-ttu-id="41999-127">戻り値 - salt</span><span class="sxs-lookup"><span data-stu-id="41999-127">Return Value - salt</span></span>

## <a name="method-new"></a><span data-ttu-id="41999-128">メソッド new</span><span class="sxs-lookup"><span data-stu-id="41999-128">Method new</span></span>

<span data-ttu-id="41999-129">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="41999-129">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(Int64 salt)
```

### <a name="parameters---new"></a><span data-ttu-id="41999-130">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="41999-130">Parameters - new</span></span>

<span data-ttu-id="41999-131">salt</span><span class="sxs-lookup"><span data-stu-id="41999-131">salt</span></span>  

## <a name="method-resetkey"></a><span data-ttu-id="41999-132">メソッド resetKey</span><span class="sxs-lookup"><span data-stu-id="41999-132">Method resetKey</span></span>

```xpp
public static void resetKey()
```

