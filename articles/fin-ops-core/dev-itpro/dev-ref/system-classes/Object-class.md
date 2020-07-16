---
title: Object クラス
description: このトピックでは、Object クラスについて説明します。
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
ms.openlocfilehash: 12a3c9e9fccfe809ea5011e63c956ac37b256a34
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502566"
---
# <a name="class-object"></a><span data-ttu-id="60ac4-103">クラス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="60ac4-103">Class Object</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Object
```

<span data-ttu-id="60ac4-104">Object クラスは、その他のすべてのクラスの派生元となる基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="60ac4-104">The Object class is the base class from which all other classes are derived.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ac4-105">備考</span><span class="sxs-lookup"><span data-stu-id="60ac4-105">Remarks</span></span>

<span data-ttu-id="60ac4-106">オブジェクト クラスのメソッドは、任意のオブジェクトに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-106">Methods in the Object class can be called for any object.</span></span> <span data-ttu-id="60ac4-107">Object クラスは、開発者がオブジェクトの実際のタイプを知らなくても、割り当ておよび等価チェックを実行できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-107">The Object class is used to allow assignment and equality checks to be performed without the developer having to know the actual type of the object.</span></span> <span data-ttu-id="60ac4-108">メソッドは 3 つのグループにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-108">The methods can be grouped into three groups:</span></span>

-   <span data-ttu-id="60ac4-109">タイム アウト メソッド - 指定した時間が経過した後にメソッドをアクティブにするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-109">Time out methods - can be used to activate a method after a specified period of time has passed.</span></span>
-   <span data-ttu-id="60ac4-110">プロセス フローを制御したり、別のオブジェクトがそのタスクを終了するを待機するために使用される、Wait、Notify、NotifyAll メソッドなどのメソッドを処理します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-110">Process methods, such as the Wait, Notify, and NotifyAll method - used to control process flow and to wait for another object to finish its task.</span></span>
-   <span data-ttu-id="60ac4-111">クラス メソッド - オブジェクトに関する基本情報を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-111">Class methods - return basic information about the object.</span></span>

## <a name="examples"></a><span data-ttu-id="60ac4-112">例</span><span class="sxs-lookup"><span data-stu-id="60ac4-112">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="60ac4-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="60ac4-113">Methods</span></span>

| <span data-ttu-id="60ac4-114">方法</span><span class="sxs-lookup"><span data-stu-id="60ac4-114">Method</span></span>                                                                      | <span data-ttu-id="60ac4-115">説明</span><span class="sxs-lookup"><span data-stu-id="60ac4-115">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ac4-116">public boolean equal(Object object)</span><span class="sxs-lookup"><span data-stu-id="60ac4-116">public boolean equal(Object object)</span></span>                                         | <span data-ttu-id="60ac4-117">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-117">Determines whether the specified object is equal to the current one.</span></span>                                        |
| <span data-ttu-id="60ac4-118">public int getTimeOutTimerHandle()</span><span class="sxs-lookup"><span data-stu-id="60ac4-118">public int getTimeOutTimerHandle()</span></span>                                          | <span data-ttu-id="60ac4-119">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-119">Returns the timer handle for the object.</span></span>                                                                    |
| <span data-ttu-id="60ac4-120">public ClassId handle()</span><span class="sxs-lookup"><span data-stu-id="60ac4-120">public ClassId handle()</span></span>                                                     | <span data-ttu-id="60ac4-121">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-121">Retrieves the handle of the class of the object.</span></span>                                                            |
| <span data-ttu-id="60ac4-122">public boolean SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="60ac4-122">public boolean SysObsoleteAttribute()</span></span>                                       |                                                                                                             |
| <span data-ttu-id="60ac4-123">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span><span class="sxs-lookup"><span data-stu-id="60ac4-123">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span></span> |                                                                                                             |
| <span data-ttu-id="60ac4-124">public str toString()</span><span class="sxs-lookup"><span data-stu-id="60ac4-124">public str toString()</span></span>                                                       | <span data-ttu-id="60ac4-125">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-125">Returns a string that represents the current object.</span></span>                                                        |
| <span data-ttu-id="60ac4-126">public int usageCount()</span><span class="sxs-lookup"><span data-stu-id="60ac4-126">public int usageCount()</span></span>                                                     | <span data-ttu-id="60ac4-127">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-127">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span> |
| <span data-ttu-id="60ac4-128">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="60ac4-128">public str xml(\[int indent\])</span></span>                                              | <span data-ttu-id="60ac4-129">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-129">Returns an XML string that represents the current object.</span></span>                                                   |
| <span data-ttu-id="60ac4-130">public boolean Equals(System.Object obj)</span><span class="sxs-lookup"><span data-stu-id="60ac4-130">public boolean Equals(System.Object obj)</span></span>                                    |                                                                                                             |
| <span data-ttu-id="60ac4-131">public int GetHashCode()</span><span class="sxs-lookup"><span data-stu-id="60ac4-131">public int GetHashCode()</span></span>                                                    |                                                                                                             |
| <span data-ttu-id="60ac4-132">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="60ac4-132">public void finalize()</span></span>                                                      |                                                                                                             |
| <span data-ttu-id="60ac4-133">public void wait()</span><span class="sxs-lookup"><span data-stu-id="60ac4-133">public void wait()</span></span>                                                          | <span data-ttu-id="60ac4-134">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-134">Pauses a process.</span></span>                                                                                           |
| <span data-ttu-id="60ac4-135">public void cancelTimeOut(int timerHandle)</span><span class="sxs-lookup"><span data-stu-id="60ac4-135">public void cancelTimeOut(int timerHandle)</span></span>                                  | <span data-ttu-id="60ac4-136">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-136">Cancels a previous method call to the setTimeOut method.</span></span>                                                    |
| <span data-ttu-id="60ac4-137">public void new()</span><span class="sxs-lookup"><span data-stu-id="60ac4-137">public void new()</span></span>                                                           | <span data-ttu-id="60ac4-138">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-138">Initializes a new instance of the Object class.</span></span>                                                             |
| <span data-ttu-id="60ac4-139">public void notify()</span><span class="sxs-lookup"><span data-stu-id="60ac4-139">public void notify()</span></span>                                                        | <span data-ttu-id="60ac4-140">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-140">Releases the hold on an object that has called the wait method on this object.</span></span>                              |
| <span data-ttu-id="60ac4-141">public void notifyAll()</span><span class="sxs-lookup"><span data-stu-id="60ac4-141">public void notifyAll()</span></span>                                                     | <span data-ttu-id="60ac4-142">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-142">Releases a lock on the object that was issued by the wait method on this object.</span></span>                            |

## <a name="method-equal"></a><span data-ttu-id="60ac4-143">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="60ac4-143">Method equal</span></span>

<span data-ttu-id="60ac4-144">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-144">Determines whether the specified object is equal to the current one.</span></span>

```xpp
public boolean equal(Object object)
```

### <a name="parameters---equal"></a><span data-ttu-id="60ac4-145">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="60ac4-145">Parameters - equal</span></span>

<span data-ttu-id="60ac4-146">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="60ac4-146">object</span></span>  
<span data-ttu-id="60ac4-147">現在のオブジェクトと比較するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="60ac4-147">The object to compare with the current object.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="60ac4-148">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="60ac4-148">Return Value - equal</span></span>

<span data-ttu-id="60ac4-149">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60ac4-149">true if the specified object is equal to the current object; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="60ac4-150">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="60ac4-150">Remarks - equal</span></span>

<span data-ttu-id="60ac4-151">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-151">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="60ac4-152">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-152">Derived classes can, however, override the Object::equal method to support value equality.</span></span>

### <a name="examples---equal"></a><span data-ttu-id="60ac4-153">例 - equal</span><span class="sxs-lookup"><span data-stu-id="60ac4-153">Examples - equal</span></span>

<span data-ttu-id="60ac4-154">次の例では、現在のインスタンスと別のオブジェクトを比較します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-154">The following example compares the current instance with another object.</span></span>

```xpp
static void Object_Equal(Args _args) 
{ 
    Object objA = new Object(); 
    Object objB = new Object(); 
    print objA.equal(objA);  // true. 
    print objA.equal(objB);  // false. 
    objA = objB; 
    print objA.equal(objB);  // true. 
 }
```

## <a name="method-gettimeouttimerhandle"></a><span data-ttu-id="60ac4-155">メソッド getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="60ac4-155">Method getTimeOutTimerHandle</span></span>

<span data-ttu-id="60ac4-156">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-156">Returns the timer handle for the object.</span></span>

```xpp
public int getTimeOutTimerHandle()
```

### <a name="return-value---gettimeouttimerhandle"></a><span data-ttu-id="60ac4-157">戻り値 - getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="60ac4-157">Return Value - getTimeOutTimerHandle</span></span>

<span data-ttu-id="60ac4-158">オブジェクトのタイマー ハンドル。</span><span class="sxs-lookup"><span data-stu-id="60ac4-158">The timer handle of the object.</span></span>

### <a name="remarks---gettimeouttimerhandle"></a><span data-ttu-id="60ac4-159">備考 - getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="60ac4-159">Remarks - getTimeOutTimerHandle</span></span>

<span data-ttu-id="60ac4-160">オブジェクトのタイマー ハンドルは、setTimeOut メソッドを呼び出すことによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-160">The timer handle of the object is set by calling the setTimeOut method.</span></span>

### <a name="examples---gettimeouttimerhandle"></a><span data-ttu-id="60ac4-161">例 - getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="60ac4-161">Examples - getTimeOutTimerHandle</span></span>

<span data-ttu-id="60ac4-162">次の例では、タイムアウトを設定してから、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-162">The following example sets a timeout, and then cancels it.</span></span>

```xpp
public void myJob() 
{ 
    int timerHandle = 0; 
    this.setTimeOut(identifierstr(workerFunction), 0); 
    //Perform some operations. 
    timerHandle = this.getTimeOutTimerHandle(); 
    this.cancelTimeOut( timerHandle ); 
}
```

## <a name="method-handle"></a><span data-ttu-id="60ac4-163">メソッド handle</span><span class="sxs-lookup"><span data-stu-id="60ac4-163">Method handle</span></span>

<span data-ttu-id="60ac4-164">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-164">Retrieves the handle of the class of the object.</span></span>

```xpp
public ClassId handle()
```

### <a name="return-value---handle"></a><span data-ttu-id="60ac4-165">戻り値 - handle</span><span class="sxs-lookup"><span data-stu-id="60ac4-165">Return Value - handle</span></span>

<span data-ttu-id="60ac4-166">現在のオブジェクトのクラスのハンドル、つまり classId プロパティです。</span><span class="sxs-lookup"><span data-stu-id="60ac4-166">The handle, that is, the classId property, of the class of the current object.</span></span>

### <a name="remarks---handle"></a><span data-ttu-id="60ac4-167">備考 - handle</span><span class="sxs-lookup"><span data-stu-id="60ac4-167">Remarks - handle</span></span>

<span data-ttu-id="60ac4-168">クラスの処理が後のリリースで変更されない、またはユーザー定義クラスのエクスポートまたはインポートの後に変更されないという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="60ac4-168">There is no guarantee that the handle of a class will remain unchanged in later releases, or after an export or import for user-defined classes.</span></span> <span data-ttu-id="60ac4-169">このメソッドによって返される値を、クラスを参照する永続的な定数として使用しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-169">It is strongly advised that the value that is returned by this method will not be used as a persistent constant to refer to the class.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="60ac4-170">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60ac4-170">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="60ac4-171">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60ac4-171">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="60ac4-172">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60ac4-172">Method SysObsoleteAttribute</span></span>

```xpp
public int SysObsoleteAttribute(str Method, int WaitTime, [boolean idle])
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="60ac4-173">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60ac4-173">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="60ac4-174">方法</span><span class="sxs-lookup"><span data-stu-id="60ac4-174">Method</span></span>  

<!-- -->

<span data-ttu-id="60ac4-175">WaitTime</span><span class="sxs-lookup"><span data-stu-id="60ac4-175">WaitTime</span></span>  

<!-- -->

<span data-ttu-id="60ac4-176">idle</span><span class="sxs-lookup"><span data-stu-id="60ac4-176">idle</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="60ac4-177">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60ac4-177">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-tostring"></a><span data-ttu-id="60ac4-178">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="60ac4-178">Method toString</span></span>

<span data-ttu-id="60ac4-179">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-179">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="60ac4-180">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="60ac4-180">Return Value - toString</span></span>

<span data-ttu-id="60ac4-181">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="60ac4-181">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="60ac4-182">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="60ac4-182">Remarks - toString</span></span>

<span data-ttu-id="60ac4-183">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-183">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="60ac4-184">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-184">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="60ac4-185">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-185">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="60ac4-186">例 - toString</span><span class="sxs-lookup"><span data-stu-id="60ac4-186">Examples - toString</span></span>

<span data-ttu-id="60ac4-187">次の例では、o のクラス名を出力します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-187">The following example prints out the class name of o.</span></span>

```xpp
static void Object_ToString_Job(Args _args) 
{ 
    Object o = new Object(); 
    print o.toString();  // Prints out: "Class Object" 
    pause; 
}
```

## <a name="method-usagecount"></a><span data-ttu-id="60ac4-188">メソッド usageCount</span><span class="sxs-lookup"><span data-stu-id="60ac4-188">Method usageCount</span></span>

<span data-ttu-id="60ac4-189">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-189">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span>

```xpp
public int usageCount()
```

### <a name="return-value---usagecount"></a><span data-ttu-id="60ac4-190">戻り値 - usageCount</span><span class="sxs-lookup"><span data-stu-id="60ac4-190">Return Value - usageCount</span></span>

<span data-ttu-id="60ac4-191">オブジェクトが持つ参照の現在の数。</span><span class="sxs-lookup"><span data-stu-id="60ac4-191">The current number of references that the object has.</span></span>

### <a name="remarks---usagecount"></a><span data-ttu-id="60ac4-192">備考 - usageCount</span><span class="sxs-lookup"><span data-stu-id="60ac4-192">Remarks - usageCount</span></span>

<span data-ttu-id="60ac4-193">オブジェクトが作成されると、その参照カウンターが 1 になります。</span><span class="sxs-lookup"><span data-stu-id="60ac4-193">When an object is created, its reference counter equals 1.</span></span> <span data-ttu-id="60ac4-194">新しい参照が作成されると、その値が増加します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-194">When a new reference is created, its value increases.</span></span> <span data-ttu-id="60ac4-195">スコープ外の参照は、値が減少します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-195">As a reference goes out of scope, its value decreases.</span></span>

### <a name="examples---usagecount"></a><span data-ttu-id="60ac4-196">例 - usageCount</span><span class="sxs-lookup"><span data-stu-id="60ac4-196">Examples - usageCount</span></span>

<span data-ttu-id="60ac4-197">次の例では、objA の参照の数を出力ウィンドウに出力します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-197">The following example prints the number of references for objA to the output window.</span></span>

```xpp
static void Object_UsageCount(Args _args) 
{ 
    Object objA = new Object(); 
    Object objB; 
    print objA.usageCount();    // Prints 1. 
    objB = objA;                // objB is a reference to objA. 
    print objA.usageCount();    // prints 2 
    pause; 
}
```

## <a name="method-xml"></a><span data-ttu-id="60ac4-198">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="60ac4-198">Method xml</span></span>

<span data-ttu-id="60ac4-199">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-199">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="60ac4-200">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="60ac4-200">Parameters - xml</span></span>

<span data-ttu-id="60ac4-201">インデント</span><span class="sxs-lookup"><span data-stu-id="60ac4-201">indent</span></span>  
<span data-ttu-id="60ac4-202">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="60ac4-202">The amount of indentation of the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="60ac4-203">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="60ac4-203">Return Value - xml</span></span>

<span data-ttu-id="60ac4-204">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="60ac4-204">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="60ac4-205">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="60ac4-205">Remarks - xml</span></span>

<span data-ttu-id="60ac4-206">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-206">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-equals"></a><span data-ttu-id="60ac4-207">メソッド Equals</span><span class="sxs-lookup"><span data-stu-id="60ac4-207">Method Equals</span></span>

```xpp
public boolean Equals(System.Object obj)
```

### <a name="parameters---equals"></a><span data-ttu-id="60ac4-208">パラメーター - Equals</span><span class="sxs-lookup"><span data-stu-id="60ac4-208">Parameters - Equals</span></span>

<span data-ttu-id="60ac4-209">obj</span><span class="sxs-lookup"><span data-stu-id="60ac4-209">obj</span></span>  

### <a name="return-value---equals"></a><span data-ttu-id="60ac4-210">戻り値 - Equals </span><span class="sxs-lookup"><span data-stu-id="60ac4-210">Return Value - Equals</span></span>

## <a name="method-gethashcode"></a><span data-ttu-id="60ac4-211">メソッド GetHashCode</span><span class="sxs-lookup"><span data-stu-id="60ac4-211">Method GetHashCode</span></span>

```xpp
public int GetHashCode()
```

### <a name="return-value---gethashcode"></a><span data-ttu-id="60ac4-212">戻り値 - GetHashCode</span><span class="sxs-lookup"><span data-stu-id="60ac4-212">Return Value - GetHashCode</span></span>

## <a name="method-finalize"></a><span data-ttu-id="60ac4-213">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="60ac4-213">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-wait"></a><span data-ttu-id="60ac4-214">メソッド wait</span><span class="sxs-lookup"><span data-stu-id="60ac4-214">Method wait</span></span>

<span data-ttu-id="60ac4-215">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-215">Pauses a process.</span></span>

```xpp
public void wait()
```

### <a name="remarks---wait"></a><span data-ttu-id="60ac4-216">備考 - wait</span><span class="sxs-lookup"><span data-stu-id="60ac4-216">Remarks - wait</span></span>

<span data-ttu-id="60ac4-217">このメソッドの最も一般的な使い方は、ユーザーに何らかの入力を求めるオブジェクトを開始し、そのオブジェクト (フォームなど) の wait メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="60ac4-217">The most common use for this method is to start an object that asks the user for some input and then call the wait method on that object, such as a form.</span></span> <span data-ttu-id="60ac4-218">次のコード行は、オブジェクトが notify メソッド または notifyAll メソッドを呼び出すまで実行されません。</span><span class="sxs-lookup"><span data-stu-id="60ac4-218">The next line of code is not executed until the object has called the notify or notifyAll method.</span></span> <span data-ttu-id="60ac4-219">フォームから wait メソッドが呼び出されるとき、ユーザーは通知メソッドを手動で呼び出す必要はありません。それは、ユーザーがフォームを閉じるか、または [適用] ボタンを押すと、フォームが Object.notifyAll メソッドを呼び出すためです。</span><span class="sxs-lookup"><span data-stu-id="60ac4-219">When the wait method is called from a form, you do not have to call the notify methods manually because forms call the Object.notifyAll method when the user either closes the form or presses the Apply button.</span></span> <span data-ttu-id="60ac4-220">このメソッドはスレッドの同期のためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="60ac4-220">This method is not meant for thread synchronization.</span></span> <span data-ttu-id="60ac4-221">代わりに waitUntilSignaled メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-221">Use the waitUntilSignaled method instead.</span></span>

### <a name="examples---wait"></a><span data-ttu-id="60ac4-222">例 - wait</span><span class="sxs-lookup"><span data-stu-id="60ac4-222">Examples - wait</span></span>

<span data-ttu-id="60ac4-223">次の例では、GetUserInput ダイアログを開き、ブロックし、ユーザーがフォームを閉じるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-223">The following example opens the GetUserInput dialog, blocks, and waits until the user has closed the form.</span></span>

```xpp
{ 
    Args a = new Args("GetUserInput"); 
    formRun fr = new formRun(a); 
    fr.init(); 
    fr.run(); 
    fr.wait(); 
    // Execution will resume at this point, only after 
    // the user has closed the form. 
}
```

## <a name="method-canceltimeout"></a><span data-ttu-id="60ac4-224">メソッド cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="60ac4-224">Method cancelTimeOut</span></span>

<span data-ttu-id="60ac4-225">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-225">Cancels a previous method call to the setTimeOut method.</span></span>

```xpp
public void cancelTimeOut(int timerHandle)
```

### <a name="parameters---canceltimeout"></a><span data-ttu-id="60ac4-226">パラメーター - cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="60ac4-226">Parameters - cancelTimeOut</span></span>

<span data-ttu-id="60ac4-227">timerHandle</span><span class="sxs-lookup"><span data-stu-id="60ac4-227">timerHandle</span></span>  
<span data-ttu-id="60ac4-228">削除する予定イベントのハンドル。</span><span class="sxs-lookup"><span data-stu-id="60ac4-228">The handle of the scheduled event to delete.</span></span> <span data-ttu-id="60ac4-229">ハンドルは、Object.setTimeOut メソッドによって返される値です。</span><span class="sxs-lookup"><span data-stu-id="60ac4-229">The handle is the value that is returned by the Object.setTimeOut method.</span></span>

### <a name="remarks---canceltimeout"></a><span data-ttu-id="60ac4-230">備考 - cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="60ac4-230">Remarks - cancelTimeOut</span></span>

<span data-ttu-id="60ac4-231">まだ処理されていないスケジュールされたタイムアウト呼び出しは、オブジェクト自体が削除されると自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="60ac4-231">Any scheduled time-out calls that have not yet been processed are automatically deleted when the object itself is deleted.</span></span>

### <a name="examples---canceltimeout"></a><span data-ttu-id="60ac4-232">例 - cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="60ac4-232">Examples - cancelTimeOut</span></span>

<span data-ttu-id="60ac4-233">次の例では、Object.setTimeOut メソッドを呼び出した後、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="60ac4-233">The following example calls the Object.setTimeOut method, and then cancels the time-out.</span></span>

```xpp
void Object_cancelTimeOut(Args _args) 
{ 
    int th; // timerHandle. 
    // timedMethod is a worker method. 
    th = this.setTimeOut( "timedMethod", 2000 ); 
    //.... 
    // Remove timeOut later. 
    CancelTimeOut(th); 
}
```

## <a name="method-new"></a><span data-ttu-id="60ac4-234">メソッド new</span><span class="sxs-lookup"><span data-stu-id="60ac4-234">Method new</span></span>

<span data-ttu-id="60ac4-235">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-235">Initializes a new instance of the Object class.</span></span>

```xpp
public void new()
```

## <a name="method-notify"></a><span data-ttu-id="60ac4-236">メソッド notify</span><span class="sxs-lookup"><span data-stu-id="60ac4-236">Method notify</span></span>

<span data-ttu-id="60ac4-237">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-237">Releases the hold on an object that has called the wait method on this object.</span></span>

```xpp
public void notify()
```

### <a name="examples---notify"></a><span data-ttu-id="60ac4-238">例 - notify</span><span class="sxs-lookup"><span data-stu-id="60ac4-238">Examples - notify</span></span>

<span data-ttu-id="60ac4-239">次の例では、オブジェクトをロックしてから解放します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-239">The following example locks an object, and then releases it.</span></span>

```xpp
public void doWork() 
{ 
    // Perform some actions. 
    this.setTimeOut(identifierstr(workerFunction), 0); 
    this.wait(); // Lock and wait for notify to be called. 
} 
public void workerFunction() 
{ 
    // Perform some actions. 
    // Work is done; unlock the doWork method. 
    this.notify(); 
}
```

## <a name="method-notifyall"></a><span data-ttu-id="60ac4-240">メソッド notifyAll</span><span class="sxs-lookup"><span data-stu-id="60ac4-240">Method notifyAll</span></span>

<span data-ttu-id="60ac4-241">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-241">Releases a lock on the object that was issued by the wait method on this object.</span></span>

```xpp
public void notifyAll()
```

### <a name="remarks---notifyall"></a><span data-ttu-id="60ac4-242">備考 - notifyAll </span><span class="sxs-lookup"><span data-stu-id="60ac4-242">Remarks - notifyAll</span></span>

<span data-ttu-id="60ac4-243">このメソッドの現在の実装では、notify メソッドと notifyAll メソッドの呼び出しに違いはありません。</span><span class="sxs-lookup"><span data-stu-id="60ac4-243">In the current implementation of this method, there is no difference between calling the notify method and the notifyAll method.</span></span> <span data-ttu-id="60ac4-244">フォームは、ユーザーがフォームを閉じるまたは「適用」ボタンを押す際に、notifyAll メソッドを自動で呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60ac4-244">Forms will automatically call the notifyAll method when the user closes the form or presses the Apply button.</span></span>

### <a name="examples---notifyall"></a><span data-ttu-id="60ac4-245">例 - notifyAll</span><span class="sxs-lookup"><span data-stu-id="60ac4-245">Examples - notifyAll</span></span>

<span data-ttu-id="60ac4-246">次の例では、notifyAll メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="60ac4-246">The following example demonstrates the usage of the notifyAll method.</span></span>

```xpp
public void doWork() 
{ 
      //Do some work. 
      this.setTimeOut(identifierstr(workerFunction), 0); 
      this.wait(); // block and wait for notify. 
} 
public void workerFunction() 
{ 
// Do some work. 
//... 
// Work is done. Notify an unblock. 
this.notify(); 
} 
```

