---
title: PerformanceMonitor クラス
description: このトピックでは、PerformanceMonitor クラスについて説明します。
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
ms.openlocfilehash: e52265cfd029b9b60882b1d2b78fd901fc752668
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502541"
---
# <a name="class-performancemonitor"></a><span data-ttu-id="39afd-103">クラス PerformanceMonitor</span><span class="sxs-lookup"><span data-stu-id="39afd-103">Class PerformanceMonitor</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitor extends Object
```

<span data-ttu-id="39afd-104">PerformanceMonitor クラスは、システムで実行されているプロセスのデータをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="39afd-104">The PerformanceMonitor class fetches data for processes that are running on the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="39afd-105">備考</span><span class="sxs-lookup"><span data-stu-id="39afd-105">Remarks</span></span>

<span data-ttu-id="39afd-106">いつでもシステムのスナップショットを取得して、システムで実行されている任意のプロセスのカウンター上で移動することができます。</span><span class="sxs-lookup"><span data-stu-id="39afd-106">You can take a snapshot of the system at any time and traverse the counters for any process that is running on the system.</span></span>

## <a name="examples"></a><span data-ttu-id="39afd-107">例</span><span class="sxs-lookup"><span data-stu-id="39afd-107">Examples</span></span>

<span data-ttu-id="39afd-108">次の例は、現在実行中のすべてのプロセスの processId および workingset 値を出力します。</span><span class="sxs-lookup"><span data-stu-id="39afd-108">The following example prints the processId and workingset values for all the currently running processes.</span></span>

```xpp
static void pvPerformanceMonitorTest(args a) 
{ 
    int i, j;  
    PerformanceMonitorInstance instance;  
    PerformanceMonitorCounter counter1, counter2;  
    PerformanceMonitor pm = new PerformanceMonitor();  
    // Take a current snapshot of the system. 
    pm.takeSnapshot ();  
    // Traverse all the running processes. 
    for (i= 1; i <= pm.instanceCount(); i++)  
    {  
        instance = pm.instance(i);  
        counter1 = instance.getCounter("ID Process");  
        counter2 = instance.getCounter("Working Set");  
        print instance.name(), " ",  
        counter1.intData(), " ",  
        counter2.intData();  
    } 
    pause;  
}
```

## <a name="methods"></a><span data-ttu-id="39afd-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="39afd-109">Methods</span></span>

| <span data-ttu-id="39afd-110">方法</span><span class="sxs-lookup"><span data-stu-id="39afd-110">Method</span></span>                                                     | <span data-ttu-id="39afd-111">説明</span><span class="sxs-lookup"><span data-stu-id="39afd-111">Description</span></span>                                                                                    |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39afd-112">public PerformanceMonitorInstance instance(int instanceNo)</span><span class="sxs-lookup"><span data-stu-id="39afd-112">public PerformanceMonitorInstance instance(int instanceNo)</span></span> |                                                                                                |
| <span data-ttu-id="39afd-113">public int instanceCount()</span><span class="sxs-lookup"><span data-stu-id="39afd-113">public int instanceCount()</span></span>                                 | <span data-ttu-id="39afd-114">インスタンス数 (現在のスナップショットのプロセスの数) を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-114">Returns the instance count, which is the number of processes in the current snapshot.</span></span>          |
| <span data-ttu-id="39afd-115">public int processId()</span><span class="sxs-lookup"><span data-stu-id="39afd-115">public int processId()</span></span>                                     | <span data-ttu-id="39afd-116">このメソッドを実行しているプロセスの processId 値を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-116">Returns the processId value of the process that is running this method.</span></span>                        |
| <span data-ttu-id="39afd-117">public str systemName()</span><span class="sxs-lookup"><span data-stu-id="39afd-117">public str systemName()</span></span>                                    |                                                                                                |
| <span data-ttu-id="39afd-118">public boolean takeSnapshot(\[str processName\])</span><span class="sxs-lookup"><span data-stu-id="39afd-118">public boolean takeSnapshot(\[str processName\])</span></span>           |                                                                                                |
| <span data-ttu-id="39afd-119">public str toString()</span><span class="sxs-lookup"><span data-stu-id="39afd-119">public str toString()</span></span>                                      | <span data-ttu-id="39afd-120">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-120">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |
| <span data-ttu-id="39afd-121">public void new()</span><span class="sxs-lookup"><span data-stu-id="39afd-121">public void new()</span></span>                                          | <span data-ttu-id="39afd-122">PerformanceMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="39afd-122">Initializes a new instance of the PerformanceMonitor class.</span></span>                                    |

## <a name="method-instance"></a><span data-ttu-id="39afd-123">メソッド instance</span><span class="sxs-lookup"><span data-stu-id="39afd-123">Method instance</span></span>

```xpp
public PerformanceMonitorInstance instance(int instanceNo)
```

### <a name="parameters---instance"></a><span data-ttu-id="39afd-124">パラメーター - instance</span><span class="sxs-lookup"><span data-stu-id="39afd-124">Parameters - instance</span></span>

<span data-ttu-id="39afd-125">instanceNo</span><span class="sxs-lookup"><span data-stu-id="39afd-125">instanceNo</span></span>  

### <a name="return-value---instance"></a><span data-ttu-id="39afd-126">戻り値 - instance</span><span class="sxs-lookup"><span data-stu-id="39afd-126">Return Value - instance</span></span>

## <a name="method-instancecount"></a><span data-ttu-id="39afd-127">メソッド instanceCount</span><span class="sxs-lookup"><span data-stu-id="39afd-127">Method instanceCount</span></span>

<span data-ttu-id="39afd-128">インスタンス数 (現在のスナップショットのプロセスの数) を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-128">Returns the instance count, which is the number of processes in the current snapshot.</span></span>

```xpp
public int instanceCount()
```

### <a name="return-value---instancecount"></a><span data-ttu-id="39afd-129">戻り値 - instanceCount</span><span class="sxs-lookup"><span data-stu-id="39afd-129">Return Value - instanceCount</span></span>

<span data-ttu-id="39afd-130">現在のスナップショット内のプロセス数。</span><span class="sxs-lookup"><span data-stu-id="39afd-130">The number of processes in the current snapshot.</span></span>

### <a name="remarks---instancecount"></a><span data-ttu-id="39afd-131">備考 - instanceCount</span><span class="sxs-lookup"><span data-stu-id="39afd-131">Remarks - instanceCount</span></span>

<span data-ttu-id="39afd-132">現在実行中のプロセスのスナップショットを取得するには、takeSnapshot メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="39afd-132">Use the takeSnapshot method to take a snapshot of the currently running processes.</span></span>

### <a name="examples---instancecount"></a><span data-ttu-id="39afd-133">例 - instanceCount</span><span class="sxs-lookup"><span data-stu-id="39afd-133">Examples - instanceCount</span></span>

```xpp
static void pvPerformanceMonitorTest(args a) 
{ 
    int i, j; 
    PerformanceMonitorInstance instance; 
    PerformanceMonitorCounter counter1, counter2; 
    PerformanceMonitor pm = new PerformanceMonitor(); 
    // Take a current snapshot of the system. 
    pm.takeSnapshot (); 
    // Traverse all the running processes. 
    for (i= 1; i <= pm.instanceCount(); i++) 
    { 
        instance = pm.instance(i); 
        counter1 = instance.getCounter("ID Process"); 
        counter2 = instance.getCounter("Working Set"); 
        print instance.name(), " ",  
            counter1.intData(), " ",  
            counter2.intData(); 
    } 
    pause; 
}
```

## <a name="method-processid"></a><span data-ttu-id="39afd-134">メソッド processId</span><span class="sxs-lookup"><span data-stu-id="39afd-134">Method processId</span></span>

<span data-ttu-id="39afd-135">このメソッドを実行しているプロセスの processId 値を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-135">Returns the processId value of the process that is running this method.</span></span>

```xpp
public int processId()
```

### <a name="return-value---processid"></a><span data-ttu-id="39afd-136">戻り値 - processId</span><span class="sxs-lookup"><span data-stu-id="39afd-136">Return Value - processId</span></span>

<span data-ttu-id="39afd-137">このメソッドを実行しているプロセスの processId 値です。</span><span class="sxs-lookup"><span data-stu-id="39afd-137">The processId value of the process that is running this method.</span></span>

### <a name="examples---processid"></a><span data-ttu-id="39afd-138">例 - processId</span><span class="sxs-lookup"><span data-stu-id="39afd-138">Examples - processId</span></span>

```xpp
static void processIdDemo(args a) 
{ 
    PerformanceMonitor pm = new PerformanceMonitor(); 
    print pm.processId(); 
    pause; 
}
```

## <a name="method-systemname"></a><span data-ttu-id="39afd-139">メソッド systemName</span><span class="sxs-lookup"><span data-stu-id="39afd-139">Method systemName</span></span>

```xpp
public str systemName()
```

### <a name="return-value---systemname"></a><span data-ttu-id="39afd-140">戻り値 - systemName</span><span class="sxs-lookup"><span data-stu-id="39afd-140">Return Value - systemName</span></span>

## <a name="method-takesnapshot"></a><span data-ttu-id="39afd-141">メソッド takeSnapshot</span><span class="sxs-lookup"><span data-stu-id="39afd-141">Method takeSnapshot</span></span>

```xpp
public boolean takeSnapshot([str processName])
```

### <a name="parameters---takesnapshot"></a><span data-ttu-id="39afd-142">パラメーター - takeSnapshot</span><span class="sxs-lookup"><span data-stu-id="39afd-142">Parameters - takeSnapshot</span></span>

<span data-ttu-id="39afd-143">processName</span><span class="sxs-lookup"><span data-stu-id="39afd-143">processName</span></span>  

### <a name="return-value---takesnapshot"></a><span data-ttu-id="39afd-144">戻り値 - takeSnapshot</span><span class="sxs-lookup"><span data-stu-id="39afd-144">Return Value - takeSnapshot</span></span>

## <a name="method-tostring"></a><span data-ttu-id="39afd-145">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="39afd-145">Method toString</span></span>

<span data-ttu-id="39afd-146">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-146">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="39afd-147">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="39afd-147">Return Value - toString</span></span>

<span data-ttu-id="39afd-148">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="39afd-148">A textual description of the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="39afd-149">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="39afd-149">Remarks - toString</span></span>

<span data-ttu-id="39afd-150">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="39afd-150">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="39afd-151">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="39afd-151">However, in some classes, additional information is returned in the string.</span></span>

## <a name="method-new"></a><span data-ttu-id="39afd-152">メソッド new</span><span class="sxs-lookup"><span data-stu-id="39afd-152">Method new</span></span>

<span data-ttu-id="39afd-153">PerformanceMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="39afd-153">Initializes a new instance of the PerformanceMonitor class.</span></span>

```xpp
public void new()
```

