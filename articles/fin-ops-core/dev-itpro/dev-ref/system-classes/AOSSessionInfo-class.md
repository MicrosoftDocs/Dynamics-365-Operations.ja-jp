---
title: AOSSessionInfo クラス
description: このトピックでは、AOSSessionInfo クラスについて説明します。
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
ms.openlocfilehash: 6a834ddbe74577370f0e4eb0dbae700d196c784a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502753"
---
# <a name="class-aossessioninfo"></a><span data-ttu-id="28001-103">クラス AOSSessionInfo</span><span class="sxs-lookup"><span data-stu-id="28001-103">Class AOSSessionInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AOSSessionInfo extends Object
```

<span data-ttu-id="28001-104">AOSSessionInfo クラスは、Application Object Server (AOS) のセッションに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="28001-104">The AOSSessionInfo class is used to provide information about a session for the Application Object Server (AOS).</span></span>

## <a name="remarks"></a><span data-ttu-id="28001-105">備考</span><span class="sxs-lookup"><span data-stu-id="28001-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="28001-106">例</span><span class="sxs-lookup"><span data-stu-id="28001-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="28001-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="28001-107">Methods</span></span>

| <span data-ttu-id="28001-108">方法</span><span class="sxs-lookup"><span data-stu-id="28001-108">Method</span></span>                             | <span data-ttu-id="28001-109">説明</span><span class="sxs-lookup"><span data-stu-id="28001-109">Description</span></span>                                                               |
|------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="28001-110">public AOSClientMode clientMode()</span><span class="sxs-lookup"><span data-stu-id="28001-110">public AOSClientMode clientMode()</span></span>  | <span data-ttu-id="28001-111">AOS セッションのクライアント モードを返します。</span><span class="sxs-lookup"><span data-stu-id="28001-111">Returns the client mode for the AOS session.</span></span>                              |
| <span data-ttu-id="28001-112">public int cpuTime()</span><span class="sxs-lookup"><span data-stu-id="28001-112">public int cpuTime()</span></span>               | <span data-ttu-id="28001-113">CPU が AOS セッションに使用するミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-113">Returns the number of milliseconds that the CPU uses for the AOS session.</span></span> |
| <span data-ttu-id="28001-114">public int idleTicks()</span><span class="sxs-lookup"><span data-stu-id="28001-114">public int idleTicks()</span></span>             | <span data-ttu-id="28001-115">AOS との最後の通信以降のミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-115">Returns the number of milliseconds since the last communication with AOS.</span></span> |
| <span data-ttu-id="28001-116">public int sessionId()</span><span class="sxs-lookup"><span data-stu-id="28001-116">public int sessionId()</span></span>             | <span data-ttu-id="28001-117">AOS セッションの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-117">Returns the ID of the AOS session.</span></span>                                        |
| <span data-ttu-id="28001-118">public void new(\[int sessionId\])</span><span class="sxs-lookup"><span data-stu-id="28001-118">public void new(\[int sessionId\])</span></span> | <span data-ttu-id="28001-119">AOSSessionInfo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="28001-119">Creates an instance of the AOSSessionInfo class.</span></span>                          |

## <a name="method-clientmode"></a><span data-ttu-id="28001-120">メソッド clientMode</span><span class="sxs-lookup"><span data-stu-id="28001-120">Method clientMode</span></span>

<span data-ttu-id="28001-121">AOS セッションのクライアント モードを返します。</span><span class="sxs-lookup"><span data-stu-id="28001-121">Returns the client mode for the AOS session.</span></span>

```xpp
public AOSClientMode clientMode()
```

### <a name="return-value---clientmode"></a><span data-ttu-id="28001-122">戻り値 - clientMode</span><span class="sxs-lookup"><span data-stu-id="28001-122">Return Value - clientMode</span></span>

<span data-ttu-id="28001-123">AOS セッションのクライアント モード。</span><span class="sxs-lookup"><span data-stu-id="28001-123">The client mode for the AOS session.</span></span>

## <a name="method-cputime"></a><span data-ttu-id="28001-124">メソッド cpuTime</span><span class="sxs-lookup"><span data-stu-id="28001-124">Method cpuTime</span></span>

<span data-ttu-id="28001-125">CPU が AOS セッションに使用するミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-125">Returns the number of milliseconds that the CPU uses for the AOS session.</span></span>

```xpp
public int cpuTime()
```

### <a name="return-value---cputime"></a><span data-ttu-id="28001-126">戻り値 - cpuTime</span><span class="sxs-lookup"><span data-stu-id="28001-126">Return Value - cpuTime</span></span>

<span data-ttu-id="28001-127">CPU が AOS セッションに使用するミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="28001-127">The number of milliseconds that the CPU uses for the AOS session.</span></span>

## <a name="method-idleticks"></a><span data-ttu-id="28001-128">メソッド idleTicks</span><span class="sxs-lookup"><span data-stu-id="28001-128">Method idleTicks</span></span>

<span data-ttu-id="28001-129">AOS との最後の通信以降のミリ秒数を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-129">Returns the number of milliseconds since the last communication with AOS.</span></span>

```xpp
public int idleTicks()
```

### <a name="return-value---idleticks"></a><span data-ttu-id="28001-130">戻り値 - idleTicks</span><span class="sxs-lookup"><span data-stu-id="28001-130">Return Value - idleTicks</span></span>

<span data-ttu-id="28001-131">AOS との最後の通信以降のミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="28001-131">The number of milliseconds since the last communication with AOS.</span></span>

## <a name="method-sessionid"></a><span data-ttu-id="28001-132">メソッド sessionId</span><span class="sxs-lookup"><span data-stu-id="28001-132">Method sessionId</span></span>

<span data-ttu-id="28001-133">AOS セッションの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="28001-133">Returns the ID of the AOS session.</span></span>

```xpp
public int sessionId()
```

### <a name="return-value---sessionid"></a><span data-ttu-id="28001-134">戻り値 - sessionId</span><span class="sxs-lookup"><span data-stu-id="28001-134">Return Value - sessionId</span></span>

<span data-ttu-id="28001-135">AOS セッションの ID。</span><span class="sxs-lookup"><span data-stu-id="28001-135">The ID of the AOS session.</span></span>

## <a name="method-new"></a><span data-ttu-id="28001-136">メソッド new</span><span class="sxs-lookup"><span data-stu-id="28001-136">Method new</span></span>

<span data-ttu-id="28001-137">AOSSessionInfo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="28001-137">Creates an instance of the AOSSessionInfo class.</span></span>

```xpp
public void new([int sessionId])
```

### <a name="parameters---new"></a><span data-ttu-id="28001-138">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="28001-138">Parameters - new</span></span>

<span data-ttu-id="28001-139">sessionId</span><span class="sxs-lookup"><span data-stu-id="28001-139">sessionId</span></span>  
<span data-ttu-id="28001-140">AOSSessionInfo クラスのインスタンスを作成するために使用されるセッション ID。</span><span class="sxs-lookup"><span data-stu-id="28001-140">The session ID that is used to create the instance of the AOSSessionInfo class.</span></span> <span data-ttu-id="28001-141">セッション ID が指定されていない場合、現在のセッションが使用されます; 省略。</span><span class="sxs-lookup"><span data-stu-id="28001-141">If a session ID is not specified, the current session is used; optional.</span></span>

