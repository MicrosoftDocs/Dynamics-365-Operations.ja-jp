---
title: PerformanceMonitorInstance クラス
description: このトピックでは、PerformanceMonitorInstance クラスについて説明します。
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
ms.openlocfilehash: 7bbbbc368736fe767d301cc8479c305039e94865
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502535"
---
# <a name="class-performancemonitorinstance"></a><span data-ttu-id="9b4ab-103">クラス PerformanceMonitorInstance</span><span class="sxs-lookup"><span data-stu-id="9b4ab-103">Class PerformanceMonitorInstance</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitorInstance extends Object
```

<span data-ttu-id="9b4ab-104">PerformanceMonitorInstance クラスは、プロセス モニターが実行されるコンピューターで実行されているプロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-104">The PerformanceMonitorInstance class represents a process that is running on the machine on which the Process Monitor runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4ab-105">備考</span><span class="sxs-lookup"><span data-stu-id="9b4ab-105">Remarks</span></span>

<span data-ttu-id="9b4ab-106">このクラスは、プロセス カウンターのクエリを可能にします。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-106">This class allows for queries of the process counters.</span></span> <span data-ttu-id="9b4ab-107">このクラスのオブジェクトを使用してプロセス カウンターをクエリすることができます。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-107">You can use objects of this class to query the processes counters.</span></span> <span data-ttu-id="9b4ab-108">各カウンターは、プロセス パラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-108">Each counter represents a process parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="9b4ab-109">例</span><span class="sxs-lookup"><span data-stu-id="9b4ab-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9b4ab-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="9b4ab-110">Methods</span></span>

| <span data-ttu-id="9b4ab-111">方法</span><span class="sxs-lookup"><span data-stu-id="9b4ab-111">Method</span></span>                                                       | <span data-ttu-id="9b4ab-112">説明</span><span class="sxs-lookup"><span data-stu-id="9b4ab-112">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4ab-113">public PerformanceMonitorCounter getCounter(str counterName)</span><span class="sxs-lookup"><span data-stu-id="9b4ab-113">public PerformanceMonitorCounter getCounter(str counterName)</span></span> |                                                                                                |
| <span data-ttu-id="9b4ab-114">public str name()</span><span class="sxs-lookup"><span data-stu-id="9b4ab-114">public str name()</span></span>                                            |                                                                                                |
| <span data-ttu-id="9b4ab-115">public str toString()</span><span class="sxs-lookup"><span data-stu-id="9b4ab-115">public str toString()</span></span>                                        | <span data-ttu-id="9b4ab-116">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-116">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |

## <a name="method-getcounter"></a><span data-ttu-id="9b4ab-117">メソッド getCounter</span><span class="sxs-lookup"><span data-stu-id="9b4ab-117">Method getCounter</span></span>

```xpp
public PerformanceMonitorCounter getCounter(str counterName)
```

### <a name="parameters---getcounter"></a><span data-ttu-id="9b4ab-118">パラメーター - getCounter</span><span class="sxs-lookup"><span data-stu-id="9b4ab-118">Parameters - getCounter</span></span>

<span data-ttu-id="9b4ab-119">counterName</span><span class="sxs-lookup"><span data-stu-id="9b4ab-119">counterName</span></span>  

### <a name="return-value---getcounter"></a><span data-ttu-id="9b4ab-120">戻り値 - getCounter</span><span class="sxs-lookup"><span data-stu-id="9b4ab-120">Return Value - getCounter</span></span>

## <a name="method-name"></a><span data-ttu-id="9b4ab-121">メソッド名</span><span class="sxs-lookup"><span data-stu-id="9b4ab-121">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="9b4ab-122">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="9b4ab-122">Return Value - name</span></span>

## <a name="method-tostring"></a><span data-ttu-id="9b4ab-123">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="9b4ab-123">Method toString</span></span>

<span data-ttu-id="9b4ab-124">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-124">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="9b4ab-125">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="9b4ab-125">Return Value - toString</span></span>

<span data-ttu-id="9b4ab-126">クラスのテキストの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-126">Returns a textual description of the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="9b4ab-127">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="9b4ab-127">Remarks - toString</span></span>

<span data-ttu-id="9b4ab-128">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-128">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="9b4ab-129">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="9b4ab-129">However, in some classes additional information is returned in the string.</span></span>

