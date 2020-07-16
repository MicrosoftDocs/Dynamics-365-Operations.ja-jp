---
title: PipeClient クラス
description: このトピックでは、PipeClient クラスについて説明します。
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
ms.openlocfilehash: bb028120e2eb0272185841fda4b819edfb3bce5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502533"
---
# <a name="class-pipeclient"></a><span data-ttu-id="70b19-103">クラス PipeClient</span><span class="sxs-lookup"><span data-stu-id="70b19-103">Class PipeClient</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PipeClient extends Object
```

## <a name="remarks"></a><span data-ttu-id="70b19-104">備考</span><span class="sxs-lookup"><span data-stu-id="70b19-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="70b19-105">例</span><span class="sxs-lookup"><span data-stu-id="70b19-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="70b19-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="70b19-106">Methods</span></span>

| <span data-ttu-id="70b19-107">方法</span><span class="sxs-lookup"><span data-stu-id="70b19-107">Method</span></span>                                                              | <span data-ttu-id="70b19-108">説明</span><span class="sxs-lookup"><span data-stu-id="70b19-108">Description</span></span>                                         |
|---------------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="70b19-109">public boolean blockingMode(\[boolean block\])</span><span class="sxs-lookup"><span data-stu-id="70b19-109">public boolean blockingMode(\[boolean block\])</span></span>                      |                                                     |
| <span data-ttu-id="70b19-110">public int errorCode()</span><span class="sxs-lookup"><span data-stu-id="70b19-110">public int errorCode()</span></span>                                              |                                                     |
| <span data-ttu-id="70b19-111">public str read()</span><span class="sxs-lookup"><span data-stu-id="70b19-111">public str read()</span></span>                                                   |                                                     |
| <span data-ttu-id="70b19-112">public boolean write(str buffer)</span><span class="sxs-lookup"><span data-stu-id="70b19-112">public boolean write(str buffer)</span></span>                                    |                                                     |
| <span data-ttu-id="70b19-113">public void new(str servername, str pipename, \[boolean blocking\])</span><span class="sxs-lookup"><span data-stu-id="70b19-113">public void new(str servername, str pipename, \[boolean blocking\])</span></span> | <span data-ttu-id="70b19-114">PipeClient クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="70b19-114">Initializes a new instance of the PipeClient class.</span></span> |

## <a name="method-blockingmode"></a><span data-ttu-id="70b19-115">メソッド blockingMode</span><span class="sxs-lookup"><span data-stu-id="70b19-115">Method blockingMode</span></span>

```xpp
public boolean blockingMode([boolean block])
```

### <a name="parameters---blockingmode"></a><span data-ttu-id="70b19-116">パラメーター - blockingMode</span><span class="sxs-lookup"><span data-stu-id="70b19-116">Parameters - blockingMode</span></span>

<span data-ttu-id="70b19-117">block</span><span class="sxs-lookup"><span data-stu-id="70b19-117">block</span></span>  

### <a name="return-value---blockingmode"></a><span data-ttu-id="70b19-118">戻り値 - blockingMode</span><span class="sxs-lookup"><span data-stu-id="70b19-118">Return Value - blockingMode</span></span>

## <a name="method-errorcode"></a><span data-ttu-id="70b19-119">メソッド errorCode</span><span class="sxs-lookup"><span data-stu-id="70b19-119">Method errorCode</span></span>

```xpp
public int errorCode()
```

### <a name="return-value---errorcode"></a><span data-ttu-id="70b19-120">戻り値 - errorCode</span><span class="sxs-lookup"><span data-stu-id="70b19-120">Return Value - errorCode</span></span>

## <a name="method-read"></a><span data-ttu-id="70b19-121">メソッド read</span><span class="sxs-lookup"><span data-stu-id="70b19-121">Method read</span></span>

```xpp
public str read()
```

### <a name="return-value---read"></a><span data-ttu-id="70b19-122">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="70b19-122">Return Value - read</span></span>

## <a name="method-write"></a><span data-ttu-id="70b19-123">メソッド write</span><span class="sxs-lookup"><span data-stu-id="70b19-123">Method write</span></span>

```xpp
public boolean write(str buffer)
```

### <a name="parameters---write"></a><span data-ttu-id="70b19-124">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="70b19-124">Parameters - write</span></span>

<span data-ttu-id="70b19-125">バッファ</span><span class="sxs-lookup"><span data-stu-id="70b19-125">buffer</span></span>  

### <a name="return-value---write"></a><span data-ttu-id="70b19-126">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="70b19-126">Return Value - write</span></span>

## <a name="method-new"></a><span data-ttu-id="70b19-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="70b19-127">Method new</span></span>

<span data-ttu-id="70b19-128">PipeClient クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="70b19-128">Initializes a new instance of the PipeClient class.</span></span>

```xpp
public void new(str servername, str pipename, [boolean blocking])
```

### <a name="parameters---new"></a><span data-ttu-id="70b19-129">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="70b19-129">Parameters - new</span></span>

<span data-ttu-id="70b19-130">servername</span><span class="sxs-lookup"><span data-stu-id="70b19-130">servername</span></span>  

<!-- -->

<span data-ttu-id="70b19-131">pipename</span><span class="sxs-lookup"><span data-stu-id="70b19-131">pipename</span></span>  

<!-- -->

<span data-ttu-id="70b19-132">ブロック</span><span class="sxs-lookup"><span data-stu-id="70b19-132">blocking</span></span>  

