---
title: "O クラス"
description: "文字 O で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52201
ms.assetid: 63f93d3d-54a5-46c2-b356-fe5863b6f927
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 629a4dfcdf1205bcb2c659039822c0a63f5e759c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="o-classes"></a><span data-ttu-id="cc9f3-103">O クラス</span><span class="sxs-lookup"><span data-stu-id="cc9f3-103">O classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc9f3-104">文字 O で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-104">System API classes that start with the letter O.</span></span>

<a name="class-object"></a><span data-ttu-id="cc9f3-105">クラス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cc9f3-105">Class Object</span></span>
------------

    class Object

<span data-ttu-id="cc9f3-106">Object クラスは、その他のすべてのクラスの派生元となる基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-106">The Object class is the base class from which all other classes are derived.</span></span>

### <a name="remarks"></a><span data-ttu-id="cc9f3-107">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-107">Remarks</span></span>

<span data-ttu-id="cc9f3-108">オブジェクト クラスのメソッドは、任意のオブジェクトに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-108">Methods in the Object class can be called for any object.</span></span> <span data-ttu-id="cc9f3-109">Object クラスは、開発者がオブジェクトの実際のタイプを知らなくても、割り当ておよび等価チェックを実行できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-109">The Object class is used to allow assignment and equality checks to be performed without the developer having to know the actual type of the object.</span></span> <span data-ttu-id="cc9f3-110">メソッドは 3 つのグループにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-110">The methods can be grouped into three groups:</span></span>

-   <span data-ttu-id="cc9f3-111">タイム アウト メソッド - 指定した時間が経過した後にメソッドをアクティブにするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-111">Time out methods - can be used to activate a method after a specified period of time has passed.</span></span>
-   <span data-ttu-id="cc9f3-112">プロセス フローを制御したり、別のオブジェクトがそのタスクを終了するを待機するために使用される、Wait、Notify、NotifyAll メソッドなどのメソッドを処理します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-112">Process methods, such as the Wait, Notify, and NotifyAll method - used to control process flow and to wait for another object to finish its task.</span></span>
-   <span data-ttu-id="cc9f3-113">クラス メソッド - オブジェクトに関する基本情報を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-113">Class methods - return basic information about the object.</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-114">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-114">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-115">Methods</span></span>

| <span data-ttu-id="cc9f3-116">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-116">Method</span></span>                                                                      | <span data-ttu-id="cc9f3-117">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-117">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-118">public boolean equal(Object object)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-118">public boolean equal(Object object)</span></span>                                         | <span data-ttu-id="cc9f3-119">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-119">Determines whether the specified object is equal to the current one.</span></span>                                        |
| <span data-ttu-id="cc9f3-120">public int getTimeOutTimerHandle()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-120">public int getTimeOutTimerHandle()</span></span>                                          | <span data-ttu-id="cc9f3-121">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-121">Returns the timer handle for the object.</span></span>                                                                    |
| <span data-ttu-id="cc9f3-122">public ClassId handle()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-122">public ClassId handle()</span></span>                                                     | <span data-ttu-id="cc9f3-123">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-123">Retrieves the handle of the class of the object.</span></span>                                                            |
| <span data-ttu-id="cc9f3-124">public boolean SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-124">public boolean SysObsoleteAttribute()</span></span>                                       |                                                                                                             |
| <span data-ttu-id="cc9f3-125">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span><span class="sxs-lookup"><span data-stu-id="cc9f3-125">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span></span> |                                                                                                             |
| <span data-ttu-id="cc9f3-126">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-126">public str toString()</span></span>                                                       | <span data-ttu-id="cc9f3-127">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-127">Returns a string that represents the current object.</span></span>                                                        |
| <span data-ttu-id="cc9f3-128">public int usageCount()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-128">public int usageCount()</span></span>                                                     | <span data-ttu-id="cc9f3-129">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-129">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span> |
| <span data-ttu-id="cc9f3-130">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="cc9f3-130">public str xml(\[int indent\])</span></span>                                              | <span data-ttu-id="cc9f3-131">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-131">Returns an XML string that represents the current object.</span></span>                                                   |
| <span data-ttu-id="cc9f3-132">public boolean Equals(System.Object obj)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-132">public boolean Equals(System.Object obj)</span></span>                                    |                                                                                                             |
| <span data-ttu-id="cc9f3-133">public int GetHashCode()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-133">public int GetHashCode()</span></span>                                                    |                                                                                                             |
| <span data-ttu-id="cc9f3-134">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-134">public void finalize()</span></span>                                                      |                                                                                                             |
| <span data-ttu-id="cc9f3-135">public void wait()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-135">public void wait()</span></span>                                                          | <span data-ttu-id="cc9f3-136">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-136">Pauses a process.</span></span>                                                                                           |
| <span data-ttu-id="cc9f3-137">public void cancelTimeOut(int timerHandle)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-137">public void cancelTimeOut(int timerHandle)</span></span>                                  | <span data-ttu-id="cc9f3-138">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-138">Cancels a previous method call to the setTimeOut method.</span></span>                                                    |
| <span data-ttu-id="cc9f3-139">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-139">public void new()</span></span>                                                           | <span data-ttu-id="cc9f3-140">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-140">Initializes a new instance of the Object class.</span></span>                                                             |
| <span data-ttu-id="cc9f3-141">public void notify()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-141">public void notify()</span></span>                                                        | <span data-ttu-id="cc9f3-142">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-142">Releases the hold on an object that has called the wait method on this object.</span></span>                              |
| <span data-ttu-id="cc9f3-143">public void notifyAll()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-143">public void notifyAll()</span></span>                                                     | <span data-ttu-id="cc9f3-144">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-144">Releases a lock on the object that was issued by the wait method on this object.</span></span>                            |

### <a name="method-equal"></a><span data-ttu-id="cc9f3-145">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="cc9f3-145">Method equal</span></span>

<span data-ttu-id="cc9f3-146">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-146">Determines whether the specified object is equal to the current one.</span></span>

    public boolean equal(Object object)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-147">Parameters</span></span>

<span data-ttu-id="cc9f3-148">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cc9f3-148">object</span></span>  
<span data-ttu-id="cc9f3-149">現在のオブジェクトと比較するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-149">The object to compare with the current object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cc9f3-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-150">Return Value</span></span>

<span data-ttu-id="cc9f3-151">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-151">true if the specified object is equal to the current object; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-152">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-152">Remarks</span></span>

<span data-ttu-id="cc9f3-153">Object :: equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-153">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="cc9f3-154">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-154">Derived classes can, however, override the Object::equal method to support value equality.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-155">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-155">Examples</span></span>

<span data-ttu-id="cc9f3-156">次の例では、現在のインスタンスと別のオブジェクトを比較します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-156">The following example compares the current instance with another object.</span></span>

    static void Object_Equal(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB = new Object(); 
        print objA.equal(objA);  // true. 
        print objA.equal(objB);  // false. 
        objA = objB; 
        print objA.equal(objB);  // true. 
     }

### <a name="method-gettimeouttimerhandle"></a><span data-ttu-id="cc9f3-157">メソッド getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-157">Method getTimeOutTimerHandle</span></span>

<span data-ttu-id="cc9f3-158">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-158">Returns the timer handle for the object.</span></span>

    public int getTimeOutTimerHandle()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-159">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-159">Return Value</span></span>

<span data-ttu-id="cc9f3-160">オブジェクトのタイマー ハンドル。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-160">The timer handle of the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-161">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-161">Remarks</span></span>

<span data-ttu-id="cc9f3-162">オブジェクトのタイマー ハンドルは、setTimeOut メソッドを呼び出すことによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-162">The timer handle of the object is set by calling the setTimeOut method.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-163">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-163">Examples</span></span>

<span data-ttu-id="cc9f3-164">次の例では、タイムアウトを設定してから、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-164">The following example sets a timeout, and then cancels it.</span></span>

    public void myJob() 
    { 
        int timerHandle = 0; 
        this.setTimeOut(identifierstr(workerFunction), 0); 
        //Perform some operations. 
        timerHandle = this.getTimeOutTimerHandle(); 
        this.cancelTimeOut( timerHandle ); 
    }

### <a name="method-handle"></a><span data-ttu-id="cc9f3-165">メソッド handle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-165">Method handle</span></span>

<span data-ttu-id="cc9f3-166">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-166">Retrieves the handle of the class of the object.</span></span>

    public ClassId handle()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-167">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-167">Return Value</span></span>

<span data-ttu-id="cc9f3-168">現在のオブジェクトのクラスのハンドル、つまり classId プロパティです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-168">The handle, that is, the classId property, of the class of the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-169">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-169">Remarks</span></span>

<span data-ttu-id="cc9f3-170">クラスの処理が後のリリースで変更されない、またはユーザー定義クラスのエクスポートまたはインポートの後に変更されないという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-170">There is no guarantee that the handle of a class will remain unchanged in later releases, or after an export or import for user-defined classes.</span></span> <span data-ttu-id="cc9f3-171">このメソッドによって返される値を、クラスを参照する永続的な定数として使用しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-171">It is strongly advised that the value that is returned by this method will not be used as a persistent constant to refer to the class.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="cc9f3-172">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="cc9f3-172">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-173">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-173">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="cc9f3-174">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="cc9f3-174">Method SysObsoleteAttribute</span></span>

    public int SysObsoleteAttribute(str Method, int WaitTime, [boolean idle])

#### <a name="parameters"></a><span data-ttu-id="cc9f3-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-175">Parameters</span></span>

<span data-ttu-id="cc9f3-176">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-176">Method</span></span>  

<!-- -->

<span data-ttu-id="cc9f3-177">WaitTime</span><span class="sxs-lookup"><span data-stu-id="cc9f3-177">WaitTime</span></span>  

<!-- -->

<span data-ttu-id="cc9f3-178">idle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-178">idle</span></span>  

#### <a name="return-value"></a><span data-ttu-id="cc9f3-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-179">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-180">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-180">Method toString</span></span>

<span data-ttu-id="cc9f3-181">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-181">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-182">Return Value</span></span>

<span data-ttu-id="cc9f3-183">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-183">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-184">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-184">Remarks</span></span>

<span data-ttu-id="cc9f3-185">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-185">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-186">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-186">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-187">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-187">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-188">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-188">Examples</span></span>

<span data-ttu-id="cc9f3-189">次の例では、o のクラス名を出力します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-189">The following example prints out the class name of o.</span></span>

    static void Object_ToString_Job(Args _args) 
    { 
        Object o = new Object(); 
        print o.toString();  // Prints out: "Class Object" 
        pause; 
    }

### <a name="method-usagecount"></a><span data-ttu-id="cc9f3-190">メソッド usageCount</span><span class="sxs-lookup"><span data-stu-id="cc9f3-190">Method usageCount</span></span>

<span data-ttu-id="cc9f3-191">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-191">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span>

    public int usageCount()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-192">Return Value</span></span>

<span data-ttu-id="cc9f3-193">オブジェクトが持つ参照の現在の数。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-193">The current number of references that the object has.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-194">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-194">Remarks</span></span>

<span data-ttu-id="cc9f3-195">オブジェクトが作成されると、その参照カウンターが 1 になります。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-195">When an object is created, its reference counter equals 1.</span></span> <span data-ttu-id="cc9f3-196">新しい参照が作成されると、その値が増加します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-196">When a new reference is created, its value increases.</span></span> <span data-ttu-id="cc9f3-197">スコープ外の参照は、値が減少します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-197">As a reference goes out of scope, its value decreases.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-198">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-198">Examples</span></span>

<span data-ttu-id="cc9f3-199">次の例では、objA の参照の数を出力ウィンドウに出力します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-199">The following example prints the number of references for objA to the output window.</span></span>

    static void Object_UsageCount(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB; 
        print objA.usageCount();    // Prints 1. 
        objB = objA;                // objB is a reference to objA. 
        print objA.usageCount();    // prints 2 
        pause; 
    }

### <a name="method-xml"></a><span data-ttu-id="cc9f3-200">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="cc9f3-200">Method xml</span></span>

<span data-ttu-id="cc9f3-201">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-201">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="cc9f3-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-202">Parameters</span></span>

<span data-ttu-id="cc9f3-203">インデント</span><span class="sxs-lookup"><span data-stu-id="cc9f3-203">indent</span></span>  
<span data-ttu-id="cc9f3-204">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-204">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cc9f3-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-205">Return Value</span></span>

<span data-ttu-id="cc9f3-206">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-206">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-207">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-207">Remarks</span></span>

<span data-ttu-id="cc9f3-208">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-208">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-equals"></a><span data-ttu-id="cc9f3-209">メソッド Equals</span><span class="sxs-lookup"><span data-stu-id="cc9f3-209">Method Equals</span></span>

    public boolean Equals(System.Object obj)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-210">Parameters</span></span>

<span data-ttu-id="cc9f3-211">obj</span><span class="sxs-lookup"><span data-stu-id="cc9f3-211">obj</span></span>  

#### <a name="return-value"></a><span data-ttu-id="cc9f3-212">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-212">Return Value</span></span>

### <a name="method-gethashcode"></a><span data-ttu-id="cc9f3-213">メソッド GetHashCode</span><span class="sxs-lookup"><span data-stu-id="cc9f3-213">Method GetHashCode</span></span>

    public int GetHashCode()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-214">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-214">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="cc9f3-215">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="cc9f3-215">Method finalize</span></span>

    public void finalize()

### <a name="method-wait"></a><span data-ttu-id="cc9f3-216">メソッド wait</span><span class="sxs-lookup"><span data-stu-id="cc9f3-216">Method wait</span></span>

<span data-ttu-id="cc9f3-217">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-217">Pauses a process.</span></span>

    public void wait()

#### <a name="remarks"></a><span data-ttu-id="cc9f3-218">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-218">Remarks</span></span>

<span data-ttu-id="cc9f3-219">このメソッドの最も一般的な使い方は、ユーザーに何らかの入力を求めるオブジェクトを開始し、そのオブジェクト (フォームなど) の wait メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-219">The most common use for this method is to start an object that asks the user for some input and then call the wait method on that object, such as a form.</span></span> <span data-ttu-id="cc9f3-220">次のコード行は、オブジェクトが notify メソッド または notifyAll メソッドを呼び出すまで実行されません。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-220">The next line of code is not executed until the object has called the notify or notifyAll method.</span></span> <span data-ttu-id="cc9f3-221">フォームから wait メソッドが呼び出されるとき、ユーザーは通知メソッドを手動で呼び出す必要はありません。それは、ユーザーがフォームを閉じるか、または [適用] ボタンを押すと、フォームが Object.notifyAll メソッドを呼び出すためです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-221">When the wait method is called from a form, you do not have to call the notify methods manually because forms call the Object.notifyAll method when the user either closes the form or presses the Apply button.</span></span> <span data-ttu-id="cc9f3-222">このメソッドはスレッドの同期のためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-222">This method is not meant for thread synchronization.</span></span> <span data-ttu-id="cc9f3-223">代わりに waitUntilSignaled メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-223">Use the waitUntilSignaled method instead.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-224">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-224">Examples</span></span>

<span data-ttu-id="cc9f3-225">次の例では、GetUserInput ダイアログを開き、ブロックし、ユーザーがフォームを閉じるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-225">The following example opens the GetUserInput dialog, blocks, and waits until the user has closed the form.</span></span>

    { 
        Args a = new Args("GetUserInput"); 
        formRun fr = new formRun(a); 
        fr.init(); 
        fr.run(); 
        fr.wait(); 
        // Execution will resume at this point, only after 
        // the user has closed the form. 
    }

### <a name="method-canceltimeout"></a><span data-ttu-id="cc9f3-226">メソッド cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="cc9f3-226">Method cancelTimeOut</span></span>

<span data-ttu-id="cc9f3-227">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-227">Cancels a previous method call to the setTimeOut method.</span></span>

    public void cancelTimeOut(int timerHandle)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-228">Parameters</span></span>

<span data-ttu-id="cc9f3-229">timerHandle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-229">timerHandle</span></span>  
<span data-ttu-id="cc9f3-230">削除する予定イベントのハンドル。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-230">The handle of the scheduled event to delete.</span></span> <span data-ttu-id="cc9f3-231">ハンドルは、Object.setTimeOut メソッドによって返される値です。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-231">The handle is the value that is returned by the Object.setTimeOut method.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-232">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-232">Remarks</span></span>

<span data-ttu-id="cc9f3-233">まだ処理されていないスケジュールされたタイムアウト呼び出しは、オブジェクト自体が削除されると自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-233">Any scheduled time-out calls that have not yet been processed are automatically deleted when the object itself is deleted.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-234">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-234">Examples</span></span>

<span data-ttu-id="cc9f3-235">次の例では、Object.setTimeOut メソッドを呼び出した後、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-235">The following example calls the Object.setTimeOut method, and then cancels the time-out.</span></span>

    void Object_cancelTimeOut(Args _args) 
    { 
        int th; // timerHandle. 
        // timedMethod is a worker method. 
        th = this.setTimeOut( "timedMethod", 2000 ); 
        //.... 
        // Remove timeOut later. 
        CancelTimeOut(th); 
    }

### <a name="method-new"></a><span data-ttu-id="cc9f3-236">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-236">Method new</span></span>

<span data-ttu-id="cc9f3-237">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-237">Initializes a new instance of the Object class.</span></span>

    public void new()

### <a name="method-notify"></a><span data-ttu-id="cc9f3-238">メソッド notify</span><span class="sxs-lookup"><span data-stu-id="cc9f3-238">Method notify</span></span>

<span data-ttu-id="cc9f3-239">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-239">Releases the hold on an object that has called the wait method on this object.</span></span>

    public void notify()

#### <a name="examples"></a><span data-ttu-id="cc9f3-240">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-240">Examples</span></span>

<span data-ttu-id="cc9f3-241">次の例では、オブジェクトをロックしてから解放します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-241">The following example locks an object, and then releases it.</span></span>

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

### <a name="method-notifyall"></a><span data-ttu-id="cc9f3-242">メソッド notifyAll</span><span class="sxs-lookup"><span data-stu-id="cc9f3-242">Method notifyAll</span></span>

<span data-ttu-id="cc9f3-243">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-243">Releases a lock on the object that was issued by the wait method on this object.</span></span>

    public void notifyAll()

#### <a name="remarks"></a><span data-ttu-id="cc9f3-244">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-244">Remarks</span></span>

<span data-ttu-id="cc9f3-245">このメソッドの現在の実装では、notify メソッドと notifyAll メソッドの呼び出しに違いはありません。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-245">In the current implementation of this method, there is no difference between calling the notify method and the notifyAll method.</span></span> <span data-ttu-id="cc9f3-246">フォームは、ユーザーがフォームを閉じるまたは「適用」ボタンを押す際に、notifyAll メソッドを自動で呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-246">Forms will automatically call the notifyAll method when the user closes the form or presses the Apply button.</span></span>

#### <a name="examples"></a><span data-ttu-id="cc9f3-247">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-247">Examples</span></span>

<span data-ttu-id="cc9f3-248">次の例では、notifyAll メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-248">The following example demonstrates the usage of the notifyAll method.</span></span>

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

## <a name="class-objectident"></a><span data-ttu-id="cc9f3-249">クラス ObjectIdent</span><span class="sxs-lookup"><span data-stu-id="cc9f3-249">Class ObjectIdent</span></span>
    class ObjectIdent extends Object

### <a name="remarks"></a><span data-ttu-id="cc9f3-250">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-250">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-251">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-251">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-252">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-252">Methods</span></span>

| <span data-ttu-id="cc9f3-253">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-253">Method</span></span>                         | <span data-ttu-id="cc9f3-254">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-254">Description</span></span>                                     |
|--------------------------------|-------------------------------------------------|
| <span data-ttu-id="cc9f3-255">public Object object()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-255">public Object object()</span></span>         |                                                 |
| <span data-ttu-id="cc9f3-256">public void new(Object object)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-256">public void new(Object object)</span></span> | <span data-ttu-id="cc9f3-257">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-257">Initializes a new instance of the Object class.</span></span> |

### <a name="method-object"></a><span data-ttu-id="cc9f3-258">メソッド object</span><span class="sxs-lookup"><span data-stu-id="cc9f3-258">Method object</span></span>

    public Object object()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-259">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-260">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-260">Method new</span></span>

<span data-ttu-id="cc9f3-261">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-261">Initializes a new instance of the Object class.</span></span>

    public void new(Object object)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-262">Parameters</span></span>

<span data-ttu-id="cc9f3-263">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cc9f3-263">object</span></span>  

## <a name="class-objectrun"></a><span data-ttu-id="cc9f3-264">クラス ObjectRun</span><span class="sxs-lookup"><span data-stu-id="cc9f3-264">Class ObjectRun</span></span>
    class ObjectRun extends Object

<span data-ttu-id="cc9f3-265">FormRun クラスおよび ReportRun クラスの基本クラスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-265">Used as the base class for the FormRun and ReportRun classes.</span></span>

### <a name="remarks"></a><span data-ttu-id="cc9f3-266">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-266">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-267">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-267">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-268">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-268">Methods</span></span>

| <span data-ttu-id="cc9f3-269">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-269">Method</span></span>                      | <span data-ttu-id="cc9f3-270">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-270">Description</span></span>                                                                                                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-271">public xArgs args()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-271">public xArgs args()</span></span>         | <span data-ttu-id="cc9f3-272">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-272">Returns the arguments that the object was constructed with.</span></span>                                                                                                             |
| <span data-ttu-id="cc9f3-273">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-273">public boolean isDetached()</span></span> | <span data-ttu-id="cc9f3-274">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-274">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>                                                                                      |
| <span data-ttu-id="cc9f3-275">public void attach()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-275">public void attach()</span></span>        | <span data-ttu-id="cc9f3-276">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-276">Reverses a call to the method.</span></span> <span data-ttu-id="cc9f3-277">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-277">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="cc9f3-278">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-278">Reversing the call disallows any further switching of focus between windows.</span></span> |
| <span data-ttu-id="cc9f3-279">public void detach()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-279">public void detach()</span></span>        | <span data-ttu-id="cc9f3-280">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-280">Allows focus to be switched between windows.</span></span>                                                                                                                            |

### <a name="method-args"></a><span data-ttu-id="cc9f3-281">メソッド args</span><span class="sxs-lookup"><span data-stu-id="cc9f3-281">Method args</span></span>

<span data-ttu-id="cc9f3-282">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-282">Returns the arguments that the object was constructed with.</span></span>

    public xArgs args()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-283">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-283">Return Value</span></span>

<span data-ttu-id="cc9f3-284">オブジェクトの引数を含む Args クラス オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-284">An Args Class object that contains the arguments for the object.</span></span>

### <a name="method-isdetached"></a><span data-ttu-id="cc9f3-285">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="cc9f3-285">Method isDetached</span></span>

<span data-ttu-id="cc9f3-286">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-286">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>

    public boolean isDetached()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-287">Return Value</span></span>

<span data-ttu-id="cc9f3-288">デタッチが呼び出された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-288">true if detach has been called; otherwise, false.</span></span>

### <a name="method-attach"></a><span data-ttu-id="cc9f3-289">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="cc9f3-289">Method attach</span></span>

<span data-ttu-id="cc9f3-290">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-290">Reverses a call to the method.</span></span> <span data-ttu-id="cc9f3-291">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-291">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="cc9f3-292">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-292">Reversing the call disallows any further switching of focus between windows.</span></span>

    public void attach()

### <a name="method-detach"></a><span data-ttu-id="cc9f3-293">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="cc9f3-293">Method detach</span></span>

<span data-ttu-id="cc9f3-294">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-294">Allows focus to be switched between windows.</span></span>

    public void detach()

#### <a name="remarks"></a><span data-ttu-id="cc9f3-295">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-295">Remarks</span></span>

<span data-ttu-id="cc9f3-296">たとえば、新しいフォームの実行方法を呼び出すことにより、新しいフォームが既存のフォームから作成されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-296">For example, a new form is created from an existing form by calling the new form's run method.</span></span> <span data-ttu-id="cc9f3-297">実行メソッドを呼び出すと、フォーカスが新しいフォームに変更されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-297">Calling a run method changes the focus to the new form.</span></span> <span data-ttu-id="cc9f3-298">解除メソッドを呼び出すと、ユーザーは 2 番目のフォームを閉じることなく最初のフォームに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-298">Calling the detach method allows the user to return to the first form without closing the second form.</span></span> <span data-ttu-id="cc9f3-299">ObjectRun.attach Method メソッドの呼び出しは、解除メソッドの影響を取り消します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-299">Calling the ObjectRun.attach Method method reverses the effects of the detach method.</span></span>

## <a name="class-ociconnection"></a><span data-ttu-id="cc9f3-300">クラス OciConnection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-300">Class OciConnection</span></span>
    class OciConnection extends Connection

<span data-ttu-id="cc9f3-301">OciConnection クラスは、Oci (Oracle 呼び出しインターフェイス) を使用するデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-301">The OciConnection class establishes a database connection that uses Oci (Oracle Call Interface).</span></span>

### <a name="remarks"></a><span data-ttu-id="cc9f3-302">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-302">Remarks</span></span>

<span data-ttu-id="cc9f3-303">OciConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-303">In the context of an OciConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="cc9f3-304">LoginProperty インスタンスに対して指定されている情報を基に、接続を確立できない場合、例外および理由は、情報ログに転記されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-304">If the connection cannot be established based on the information that is specified for the LoginProperty instance, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="cc9f3-305">このクラスは、Oracle クライアント ソフトウェアがインストールされている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-305">This class can be used only when Oracle client software is installed.</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-306">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-306">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-307">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-307">Methods</span></span>

| <span data-ttu-id="cc9f3-308">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-308">Method</span></span>                               | <span data-ttu-id="cc9f3-309">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-309">Description</span></span>                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-310">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-310">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="cc9f3-311">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-311">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-312">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-312">Method new</span></span>

<span data-ttu-id="cc9f3-313">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-313">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span>

    public void new(LoginProperty Login)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-314">Parameters</span></span>

<span data-ttu-id="cc9f3-315">ログイン</span><span class="sxs-lookup"><span data-stu-id="cc9f3-315">Login</span></span>  
<span data-ttu-id="cc9f3-316">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-316">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

## <a name="class-odbcconnection"></a><span data-ttu-id="cc9f3-317">クラス OdbcConnection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-317">Class OdbcConnection</span></span>
    class OdbcConnection extends Connection

<span data-ttu-id="cc9f3-318">OdbcConnection クラスは、ODBC (Open Database Connectivity) を使用してデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-318">The OdbcConnection class establishes a database connection by using ODBC (Open Database Connectivity).</span></span>

### <a name="remarks"></a><span data-ttu-id="cc9f3-319">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-319">Remarks</span></span>

<span data-ttu-id="cc9f3-320">OdbcConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-320">In the context of an OdbcConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="cc9f3-321">ODBC データ ソースへの接続を確立できない場合、例外がスローされ、その原因が Infolog に転記されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-321">If a connection to the ODBC data source cannot be established, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="cc9f3-322">このクラスは、正しい ODBC ドライバーがインストールされ、コントロール パネルの ODBC マネージャーで構成されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-322">This class works only if the correct ODBC drivers have been installed and configured in ODBC Manager in Control Panel.</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-323">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-323">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-324">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-324">Methods</span></span>

| <span data-ttu-id="cc9f3-325">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-325">Method</span></span>                               | <span data-ttu-id="cc9f3-326">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-326">Description</span></span>                                                                                              |
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-327">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-327">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="cc9f3-328">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-328">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-329">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-329">Method new</span></span>

<span data-ttu-id="cc9f3-330">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-330">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span>

    public void new(LoginProperty Login)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-331">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-331">Parameters</span></span>

<span data-ttu-id="cc9f3-332">ログイン</span><span class="sxs-lookup"><span data-stu-id="cc9f3-332">Login</span></span>  
<span data-ttu-id="cc9f3-333">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-333">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

## <a name="class-olecommand"></a><span data-ttu-id="cc9f3-334">クラス OleCommand</span><span class="sxs-lookup"><span data-stu-id="cc9f3-334">Class OleCommand</span></span>
    class OleCommand extends Object

### <a name="remarks"></a><span data-ttu-id="cc9f3-335">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-335">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-336">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-336">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-337">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-337">Methods</span></span>

| <span data-ttu-id="cc9f3-338">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-338">Method</span></span>                                                                              | <span data-ttu-id="cc9f3-339">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-339">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="cc9f3-340">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-340">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span></span> |                                                 |
| <span data-ttu-id="cc9f3-341">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-341">public void finalize()</span></span>                                                              |                                                 |
| <span data-ttu-id="cc9f3-342">public void new(ComInterface comObject)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-342">public void new(ComInterface comObject)</span></span>                                             | <span data-ttu-id="cc9f3-343">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-343">Initializes a new instance of the Object class.</span></span> |

### <a name="method-exec"></a><span data-ttu-id="cc9f3-344">メソッド exec</span><span class="sxs-lookup"><span data-stu-id="cc9f3-344">Method exec</span></span>

    public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-345">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-345">Parameters</span></span>

<span data-ttu-id="cc9f3-346">cmdGroup</span><span class="sxs-lookup"><span data-stu-id="cc9f3-346">cmdGroup</span></span>  

<!-- -->

<span data-ttu-id="cc9f3-347">cmdId</span><span class="sxs-lookup"><span data-stu-id="cc9f3-347">cmdId</span></span>  

<!-- -->

<span data-ttu-id="cc9f3-348">cmdExecOption</span><span class="sxs-lookup"><span data-stu-id="cc9f3-348">cmdExecOption</span></span>  

<!-- -->

<span data-ttu-id="cc9f3-349">parm</span><span class="sxs-lookup"><span data-stu-id="cc9f3-349">parm</span></span>  

#### <a name="return-value"></a><span data-ttu-id="cc9f3-350">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-350">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="cc9f3-351">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="cc9f3-351">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="cc9f3-352">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-352">Method new</span></span>

<span data-ttu-id="cc9f3-353">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-353">Initializes a new instance of the Object class.</span></span>

    public void new(ComInterface comObject)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-354">Parameters</span></span>

<span data-ttu-id="cc9f3-355">comObject</span><span class="sxs-lookup"><span data-stu-id="cc9f3-355">comObject</span></span>  

## <a name="class-ouputsection"></a><span data-ttu-id="cc9f3-356">クラス OuputSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-356">Class OuputSection</span></span>
    class OuputSection extends Object

### <a name="remarks"></a><span data-ttu-id="cc9f3-357">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-357">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-358">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-358">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-359">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-359">Methods</span></span>

| <span data-ttu-id="cc9f3-360">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-360">Method</span></span>                                           | <span data-ttu-id="cc9f3-361">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-361">Description</span></span>                                           |
|--------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="cc9f3-362">public int arrangeMethod()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-362">public int arrangeMethod()</span></span>                       |                                                       |
| <span data-ttu-id="cc9f3-363">public int backgroundColor()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-363">public int backgroundColor()</span></span>                     |                                                       |
| <span data-ttu-id="cc9f3-364">public LineThickness borderWidth()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-364">public LineThickness borderWidth()</span></span>               |                                                       |
| <span data-ttu-id="cc9f3-365">public int bottomMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-365">public int bottomMargin()</span></span>                        |                                                       |
| <span data-ttu-id="cc9f3-366">public HeadingsStrategy columnHeadingsStrategy()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-366">public HeadingsStrategy columnHeadingsStrategy()</span></span> |                                                       |
| <span data-ttu-id="cc9f3-367">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-367">public str fontName()</span></span>                            |                                                       |
| <span data-ttu-id="cc9f3-368">public int leftMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-368">public int leftMargin()</span></span>                          |                                                       |
| <span data-ttu-id="cc9f3-369">public LineType lineBottom()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-369">public LineType lineBottom()</span></span>                     |                                                       |
| <span data-ttu-id="cc9f3-370">public LineType lineLeft()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-370">public LineType lineLeft()</span></span>                       |                                                       |
| <span data-ttu-id="cc9f3-371">public LineType lineRight()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-371">public LineType lineRight()</span></span>                      |                                                       |
| <span data-ttu-id="cc9f3-372">public LineType lineTop()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-372">public LineType lineTop()</span></span>                        |                                                       |
| <span data-ttu-id="cc9f3-373">public int nextVerticalPos()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-373">public int nextVerticalPos()</span></span>                     |                                                       |
| <span data-ttu-id="cc9f3-374">public int rightMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-374">public int rightMargin()</span></span>                         |                                                       |
| <span data-ttu-id="cc9f3-375">public ReportBlockType sectionType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-375">public ReportBlockType sectionType()</span></span>             |                                                       |
| <span data-ttu-id="cc9f3-376">public int topMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-376">public int topMargin()</span></span>                           |                                                       |
| <span data-ttu-id="cc9f3-377">public int type()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-377">public int type()</span></span>                                |                                                       |
| <span data-ttu-id="cc9f3-378">public int verticalPos()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-378">public int verticalPos()</span></span>                         |                                                       |
| <span data-ttu-id="cc9f3-379">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-379">public void new()</span></span>                                | <span data-ttu-id="cc9f3-380">OuputSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-380">Initializes a new instance of the OuputSection class.</span></span> |

### <a name="method-arrangemethod"></a><span data-ttu-id="cc9f3-381">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="cc9f3-381">Method arrangeMethod</span></span>

    public int arrangeMethod()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-382">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-382">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="cc9f3-383">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cc9f3-383">Method backgroundColor</span></span>

    public int backgroundColor()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-384">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-384">Return Value</span></span>

### <a name="method-borderwidth"></a><span data-ttu-id="cc9f3-385">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="cc9f3-385">Method borderWidth</span></span>

    public LineThickness borderWidth()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-386">Return Value</span></span>

### <a name="method-bottommargin"></a><span data-ttu-id="cc9f3-387">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-387">Method bottomMargin</span></span>

    public int bottomMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-388">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-388">Return Value</span></span>

### <a name="method-columnheadingsstrategy"></a><span data-ttu-id="cc9f3-389">メソッド columnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="cc9f3-389">Method columnHeadingsStrategy</span></span>

    public HeadingsStrategy columnHeadingsStrategy()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-390">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="cc9f3-391">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-391">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-392">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-392">Return Value</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="cc9f3-393">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-393">Method leftMargin</span></span>

    public int leftMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-394">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-394">Return Value</span></span>

### <a name="method-linebottom"></a><span data-ttu-id="cc9f3-395">メソッド lineBottom</span><span class="sxs-lookup"><span data-stu-id="cc9f3-395">Method lineBottom</span></span>

    public LineType lineBottom()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-396">Return Value</span></span>

### <a name="method-lineleft"></a><span data-ttu-id="cc9f3-397">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="cc9f3-397">Method lineLeft</span></span>

    public LineType lineLeft()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-398">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-398">Return Value</span></span>

### <a name="method-lineright"></a><span data-ttu-id="cc9f3-399">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="cc9f3-399">Method lineRight</span></span>

    public LineType lineRight()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-400">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-400">Return Value</span></span>

### <a name="method-linetop"></a><span data-ttu-id="cc9f3-401">メソッド lineTop</span><span class="sxs-lookup"><span data-stu-id="cc9f3-401">Method lineTop</span></span>

    public LineType lineTop()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-402">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-402">Return Value</span></span>

### <a name="method-nextverticalpos"></a><span data-ttu-id="cc9f3-403">メソッド nextVerticalPos</span><span class="sxs-lookup"><span data-stu-id="cc9f3-403">Method nextVerticalPos</span></span>

    public int nextVerticalPos()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-404">Return Value</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="cc9f3-405">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-405">Method rightMargin</span></span>

    public int rightMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-406">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-406">Return Value</span></span>

### <a name="method-sectiontype"></a><span data-ttu-id="cc9f3-407">メソッド sectionType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-407">Method sectionType</span></span>

    public ReportBlockType sectionType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-408">Return Value</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="cc9f3-409">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-409">Method topMargin</span></span>

    public int topMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-410">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-410">Return Value</span></span>

### <a name="method-type"></a><span data-ttu-id="cc9f3-411">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="cc9f3-411">Method type</span></span>

    public int type()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-412">Return Value</span></span>

### <a name="method-verticalpos"></a><span data-ttu-id="cc9f3-413">メソッド verticalPos</span><span class="sxs-lookup"><span data-stu-id="cc9f3-413">Method verticalPos</span></span>

    public int verticalPos()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-414">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-414">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-415">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-415">Method new</span></span>

<span data-ttu-id="cc9f3-416">OuputSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-416">Initializes a new instance of the OuputSection class.</span></span>

    public void new()

## <a name="class-outputautolabelfield"></a><span data-ttu-id="cc9f3-417">クラス OutputAutoLabelField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-417">Class OutputAutoLabelField</span></span>
    class OutputAutoLabelField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-418">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-418">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-419">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-419">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-420">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-420">Methods</span></span>

| <span data-ttu-id="cc9f3-421">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-421">Method</span></span>                  | <span data-ttu-id="cc9f3-422">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-422">Description</span></span>                                                   |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cc9f3-423">public boolean leadIn()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-423">public boolean leadIn()</span></span> |                                                               |
| <span data-ttu-id="cc9f3-424">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-424">public str toString()</span></span>   | <span data-ttu-id="cc9f3-425">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-425">Returns a string that represents the current object.</span></span>          |
| <span data-ttu-id="cc9f3-426">public str value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-426">public str value()</span></span>      |                                                               |
| <span data-ttu-id="cc9f3-427">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-427">public void new()</span></span>       | <span data-ttu-id="cc9f3-428">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-428">Initializes a new instance of the OutputAutoLabelField class.</span></span> |

### <a name="method-leadin"></a><span data-ttu-id="cc9f3-429">メソッド leadIn</span><span class="sxs-lookup"><span data-stu-id="cc9f3-429">Method leadIn</span></span>

    public boolean leadIn()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-430">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-431">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-431">Method toString</span></span>

<span data-ttu-id="cc9f3-432">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-432">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-433">Return Value</span></span>

<span data-ttu-id="cc9f3-434">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-434">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-435">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-435">Remarks</span></span>

<span data-ttu-id="cc9f3-436">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-436">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-437">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-437">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-438">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-438">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-439">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-439">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-440">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-440">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-441">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-441">Method new</span></span>

<span data-ttu-id="cc9f3-442">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-442">Initializes a new instance of the OutputAutoLabelField class.</span></span>

    public void new()

## <a name="class-outputbitmapfield"></a><span data-ttu-id="cc9f3-443">クラス OutputBitmapField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-443">Class OutputBitmapField</span></span>
    class OutputBitmapField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-444">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-444">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-445">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-445">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-446">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-446">Methods</span></span>

| <span data-ttu-id="cc9f3-447">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-447">Method</span></span>                     | <span data-ttu-id="cc9f3-448">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-448">Description</span></span>                                                |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="cc9f3-449">public str imageFileName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-449">public str imageFileName()</span></span> |                                                            |
| <span data-ttu-id="cc9f3-450">public boolean resize()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-450">public boolean resize()</span></span>    |                                                            |
| <span data-ttu-id="cc9f3-451">public int resourceId()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-451">public int resourceId()</span></span>    |                                                            |
| <span data-ttu-id="cc9f3-452">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-452">public str toString()</span></span>      | <span data-ttu-id="cc9f3-453">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-453">Returns a string that represents the current object.</span></span>       |
| <span data-ttu-id="cc9f3-454">public container value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-454">public container value()</span></span>   |                                                            |
| <span data-ttu-id="cc9f3-455">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-455">public void new()</span></span>          | <span data-ttu-id="cc9f3-456">OutputBitmapField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-456">Initializes a new instance of the OutputBitmapField class.</span></span> |

### <a name="method-imagefilename"></a><span data-ttu-id="cc9f3-457">メソッド imageFileName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-457">Method imageFileName</span></span>

    public str imageFileName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-458">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-458">Return Value</span></span>

### <a name="method-resize"></a><span data-ttu-id="cc9f3-459">メソッド resize</span><span class="sxs-lookup"><span data-stu-id="cc9f3-459">Method resize</span></span>

    public boolean resize()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-460">Return Value</span></span>

### <a name="method-resourceid"></a><span data-ttu-id="cc9f3-461">メソッド resourceId</span><span class="sxs-lookup"><span data-stu-id="cc9f3-461">Method resourceId</span></span>

    public int resourceId()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-462">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-462">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-463">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-463">Method toString</span></span>

<span data-ttu-id="cc9f3-464">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-464">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-465">Return Value</span></span>

<span data-ttu-id="cc9f3-466">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-466">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-467">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-467">Remarks</span></span>

<span data-ttu-id="cc9f3-468">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-468">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-469">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-469">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-470">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-470">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-471">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-471">Method value</span></span>

    public container value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-472">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-472">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-473">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-473">Method new</span></span>

<span data-ttu-id="cc9f3-474">OutputBitmapField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-474">Initializes a new instance of the OutputBitmapField class.</span></span>

    public void new()

## <a name="class-outputbodysection"></a><span data-ttu-id="cc9f3-475">クラス OutputBodySection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-475">Class OutputBodySection</span></span>
    class OutputBodySection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-476">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-476">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-477">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-477">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-478">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-478">Methods</span></span>

| <span data-ttu-id="cc9f3-479">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-479">Method</span></span>             | <span data-ttu-id="cc9f3-480">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-480">Description</span></span>                                                |
|--------------------|------------------------------------------------------------|
| <span data-ttu-id="cc9f3-481">public int recId()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-481">public int recId()</span></span> |                                                            |
| <span data-ttu-id="cc9f3-482">public int table()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-482">public int table()</span></span> |                                                            |
| <span data-ttu-id="cc9f3-483">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-483">public void new()</span></span>  | <span data-ttu-id="cc9f3-484">OutputBodySection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-484">Initializes a new instance of the OutputBodySection class.</span></span> |

### <a name="method-recid"></a><span data-ttu-id="cc9f3-485">メソッド recId</span><span class="sxs-lookup"><span data-stu-id="cc9f3-485">Method recId</span></span>

    public int recId()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-486">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-486">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="cc9f3-487">メソッド table</span><span class="sxs-lookup"><span data-stu-id="cc9f3-487">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-488">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-488">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-489">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-489">Method new</span></span>

<span data-ttu-id="cc9f3-490">OutputBodySection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-490">Initializes a new instance of the OutputBodySection class.</span></span>

    public void new()

## <a name="class-outputcolumnheadingssection"></a><span data-ttu-id="cc9f3-491">クラス OutputColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-491">Class OutputColumnHeadingsSection</span></span>
    class OutputColumnHeadingsSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-492">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-492">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-493">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-493">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-494">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-494">Methods</span></span>

| <span data-ttu-id="cc9f3-495">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-495">Method</span></span>             | <span data-ttu-id="cc9f3-496">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-496">Description</span></span>                                                          |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-497">public str table()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-497">public str table()</span></span> |                                                                      |
| <span data-ttu-id="cc9f3-498">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-498">public void new()</span></span>  | <span data-ttu-id="cc9f3-499">OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-499">Initializes a new instance of the OutputColumnHeadingsSection class.</span></span> |

### <a name="method-table"></a><span data-ttu-id="cc9f3-500">メソッド table</span><span class="sxs-lookup"><span data-stu-id="cc9f3-500">Method table</span></span>

    public str table()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-501">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-501">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-502">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-502">Method new</span></span>

<span data-ttu-id="cc9f3-503">OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-503">Initializes a new instance of the OutputColumnHeadingsSection class.</span></span>

    public void new()

## <a name="class-outputdatefield"></a><span data-ttu-id="cc9f3-504">クラス OutputDateField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-504">Class OutputDateField</span></span>
    class OutputDateField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-505">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-505">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-506">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-506">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-507">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-507">Methods</span></span>

| <span data-ttu-id="cc9f3-508">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-508">Method</span></span>                | <span data-ttu-id="cc9f3-509">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-509">Description</span></span>                                              |
|-----------------------|----------------------------------------------------------|
| <span data-ttu-id="cc9f3-510">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-510">public str toString()</span></span> | <span data-ttu-id="cc9f3-511">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-511">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="cc9f3-512">public Date value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-512">public Date value()</span></span>   |                                                          |
| <span data-ttu-id="cc9f3-513">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-513">public void new()</span></span>     | <span data-ttu-id="cc9f3-514">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-514">Initializes a new instance of the OutputDateField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-515">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-515">Method toString</span></span>

<span data-ttu-id="cc9f3-516">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-516">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-517">Return Value</span></span>

<span data-ttu-id="cc9f3-518">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-518">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-519">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-519">Remarks</span></span>

<span data-ttu-id="cc9f3-520">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-520">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-521">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-521">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-522">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-522">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-523">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-523">Method value</span></span>

    public Date value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-524">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-524">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-525">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-525">Method new</span></span>

<span data-ttu-id="cc9f3-526">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-526">Initializes a new instance of the OutputDateField class.</span></span>

    public void new()

## <a name="class-outputdatetimefield"></a><span data-ttu-id="cc9f3-527">クラス OutputDateTimeField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-527">Class OutputDateTimeField</span></span>
    class OutputDateTimeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-528">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-528">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-529">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-529">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-530">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-530">Methods</span></span>

| <span data-ttu-id="cc9f3-531">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-531">Method</span></span>                  | <span data-ttu-id="cc9f3-532">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-532">Description</span></span>                                                  |
|-------------------------|--------------------------------------------------------------|
| <span data-ttu-id="cc9f3-533">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-533">public str toString()</span></span>   | <span data-ttu-id="cc9f3-534">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-534">Returns a string that represents the current object.</span></span>         |
| <span data-ttu-id="cc9f3-535">public DateTime value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-535">public DateTime value()</span></span> |                                                              |
| <span data-ttu-id="cc9f3-536">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-536">public void new()</span></span>       | <span data-ttu-id="cc9f3-537">OutputDateTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-537">Initializes a new instance of the OutputDateTimeField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-538">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-538">Method toString</span></span>

<span data-ttu-id="cc9f3-539">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-539">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-540">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-540">Return Value</span></span>

<span data-ttu-id="cc9f3-541">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-541">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-542">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-542">Remarks</span></span>

<span data-ttu-id="cc9f3-543">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-543">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-544">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-544">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-545">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-545">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-546">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-546">Method value</span></span>

    public DateTime value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-547">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-547">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-548">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-548">Method new</span></span>

<span data-ttu-id="cc9f3-549">OutputDateTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-549">Initializes a new instance of the OutputDateTimeField class.</span></span>

    public void new()

## <a name="class-outputenumfield"></a><span data-ttu-id="cc9f3-550">クラス OutputEnumField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-550">Class OutputEnumField</span></span>
    class OutputEnumField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-551">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-551">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-552">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-552">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-553">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-553">Methods</span></span>

| <span data-ttu-id="cc9f3-554">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-554">Method</span></span>                 | <span data-ttu-id="cc9f3-555">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-555">Description</span></span>                                              |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="cc9f3-556">public str getString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-556">public str getString()</span></span> |                                                          |
| <span data-ttu-id="cc9f3-557">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-557">public void new()</span></span>      | <span data-ttu-id="cc9f3-558">OutputEnumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-558">Initializes a new instance of the OutputEnumField class.</span></span> |

### <a name="method-getstring"></a><span data-ttu-id="cc9f3-559">メソッド getString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-559">Method getString</span></span>

    public str getString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-560">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-560">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-561">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-561">Method new</span></span>

<span data-ttu-id="cc9f3-562">OutputEnumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-562">Initializes a new instance of the OutputEnumField class.</span></span>

    public void new()

## <a name="class-outputepilogsection"></a><span data-ttu-id="cc9f3-563">クラス OutputEpilogSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-563">Class OutputEpilogSection</span></span>
    class OutputEpilogSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-564">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-564">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-565">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-565">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-566">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-566">Methods</span></span>

| <span data-ttu-id="cc9f3-567">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-567">Method</span></span>            | <span data-ttu-id="cc9f3-568">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-568">Description</span></span>                                                  |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="cc9f3-569">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-569">public void new()</span></span> | <span data-ttu-id="cc9f3-570">OutputEpilogSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-570">Initializes a new instance of the OutputEpilogSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-571">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-571">Method new</span></span>

<span data-ttu-id="cc9f3-572">OutputEpilogSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-572">Initializes a new instance of the OutputEpilogSection class.</span></span>

    public void new()

## <a name="class-outputfield"></a><span data-ttu-id="cc9f3-573">クラス OutputField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-573">Class OutputField</span></span>
    class OutputField extends Object

### <a name="remarks"></a><span data-ttu-id="cc9f3-574">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-574">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-575">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-575">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-576">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-576">Methods</span></span>

| <span data-ttu-id="cc9f3-577">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-577">Method</span></span>                         | <span data-ttu-id="cc9f3-578">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-578">Description</span></span>                                          |
|--------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc9f3-579">public Alignment alignment()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-579">public Alignment alignment()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-580">public int backgroundColor()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-580">public int backgroundColor()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-581">public int borderWidth()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-581">public int borderWidth()</span></span>       |                                                      |
| <span data-ttu-id="cc9f3-582">public str CSSClass()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-582">public str CSSClass()</span></span>          |                                                      |
| <span data-ttu-id="cc9f3-583">public int dateFormat()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-583">public int dateFormat()</span></span>        |                                                      |
| <span data-ttu-id="cc9f3-584">public int decimals()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-584">public int decimals()</span></span>          |                                                      |
| <span data-ttu-id="cc9f3-585">public int extendedDataType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-585">public int extendedDataType()</span></span>  |                                                      |
| <span data-ttu-id="cc9f3-586">public FieldId fieldHandle()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-586">public FieldId fieldHandle()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-587">public str fieldName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-587">public str fieldName()</span></span>         |                                                      |
| <span data-ttu-id="cc9f3-588">public int fontHeight()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-588">public int fontHeight()</span></span>        |                                                      |
| <span data-ttu-id="cc9f3-589">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-589">public str fontName()</span></span>          |                                                      |
| <span data-ttu-id="cc9f3-590">public int foregroundColor()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-590">public int foregroundColor()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-591">public str formatValue()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-591">public str formatValue()</span></span>       |                                                      |
| <span data-ttu-id="cc9f3-592">public int height()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-592">public int height()</span></span>            |                                                      |
| <span data-ttu-id="cc9f3-593">public int heightMode()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-593">public int heightMode()</span></span>        |                                                      |
| <span data-ttu-id="cc9f3-594">public boolean hideZeros()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-594">public boolean hideZeros()</span></span>     |                                                      |
| <span data-ttu-id="cc9f3-595">public boolean isOneline()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-595">public boolean isOneline()</span></span>     |                                                      |
| <span data-ttu-id="cc9f3-596">public boolean isOverlapping()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-596">public boolean isOverlapping()</span></span> |                                                      |
| <span data-ttu-id="cc9f3-597">public boolean italic()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-597">public boolean italic()</span></span>        |                                                      |
| <span data-ttu-id="cc9f3-598">public LateEvalMode lateEval()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-598">public LateEvalMode lateEval()</span></span> |                                                      |
| <span data-ttu-id="cc9f3-599">public LineType lineBottom()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-599">public LineType lineBottom()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-600">public LineType lineLeft()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-600">public LineType lineLeft()</span></span>     |                                                      |
| <span data-ttu-id="cc9f3-601">public LineType lineRight()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-601">public LineType lineRight()</span></span>    |                                                      |
| <span data-ttu-id="cc9f3-602">public LineType lineTop()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-602">public LineType lineTop()</span></span>      |                                                      |
| <span data-ttu-id="cc9f3-603">public str menuFunctionHelp()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-603">public str menuFunctionHelp()</span></span>  |                                                      |
| <span data-ttu-id="cc9f3-604">public str menuFunctionName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-604">public str menuFunctionName()</span></span>  |                                                      |
| <span data-ttu-id="cc9f3-605">public int menuFunctionType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-605">public int menuFunctionType()</span></span>  |                                                      |
| <span data-ttu-id="cc9f3-606">public str menuFunctionWeb()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-606">public str menuFunctionWeb()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-607">public str name()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-607">public str name()</span></span>              |                                                      |
| <span data-ttu-id="cc9f3-608">public int recId()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-608">public int recId()</span></span>             |                                                      |
| <span data-ttu-id="cc9f3-609">public boolean showPrompt()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-609">public boolean showPrompt()</span></span>    |                                                      |
| <span data-ttu-id="cc9f3-610">public boolean strikeThrough()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-610">public boolean strikeThrough()</span></span> |                                                      |
| <span data-ttu-id="cc9f3-611">public TableId tableHandle()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-611">public TableId tableHandle()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-612">public str tableName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-612">public str tableName()</span></span>         |                                                      |
| <span data-ttu-id="cc9f3-613">public boolean turnSign()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-613">public boolean turnSign()</span></span>      |                                                      |
| <span data-ttu-id="cc9f3-614">public int type()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-614">public int type()</span></span>              |                                                      |
| <span data-ttu-id="cc9f3-615">public boolean underline()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-615">public boolean underline()</span></span>     |                                                      |
| <span data-ttu-id="cc9f3-616">public str webMenuItemName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-616">public str webMenuItemName()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-617">public int webMenuItemType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-617">public int webMenuItemType()</span></span>   |                                                      |
| <span data-ttu-id="cc9f3-618">public str webTarget()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-618">public str webTarget()</span></span>         |                                                      |
| <span data-ttu-id="cc9f3-619">public int weight()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-619">public int weight()</span></span>            |                                                      |
| <span data-ttu-id="cc9f3-620">public int width()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-620">public int width()</span></span>             |                                                      |
| <span data-ttu-id="cc9f3-621">public int widthMode()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-621">public int widthMode()</span></span>         |                                                      |
| <span data-ttu-id="cc9f3-622">public int xPos()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-622">public int xPos()</span></span>              |                                                      |
| <span data-ttu-id="cc9f3-623">public int yPos()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-623">public int yPos()</span></span>              |                                                      |
| <span data-ttu-id="cc9f3-624">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-624">public void new()</span></span>              | <span data-ttu-id="cc9f3-625">OutputField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-625">Initializes a new instance of the OutputField class.</span></span> |

### <a name="method-alignment"></a><span data-ttu-id="cc9f3-626">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="cc9f3-626">Method alignment</span></span>

    public Alignment alignment()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-627">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-627">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="cc9f3-628">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="cc9f3-628">Method backgroundColor</span></span>

    public int backgroundColor()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-629">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-629">Return Value</span></span>

### <a name="method-borderwidth"></a><span data-ttu-id="cc9f3-630">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="cc9f3-630">Method borderWidth</span></span>

    public int borderWidth()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-631">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-631">Return Value</span></span>

### <a name="method-cssclass"></a><span data-ttu-id="cc9f3-632">メソッド CSSClass</span><span class="sxs-lookup"><span data-stu-id="cc9f3-632">Method CSSClass</span></span>

    public str CSSClass()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-633">Return Value</span></span>

### <a name="method-dateformat"></a><span data-ttu-id="cc9f3-634">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="cc9f3-634">Method dateFormat</span></span>

    public int dateFormat()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-635">Return Value</span></span>

### <a name="method-decimals"></a><span data-ttu-id="cc9f3-636">メソッド decimals</span><span class="sxs-lookup"><span data-stu-id="cc9f3-636">Method decimals</span></span>

    public int decimals()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-637">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-637">Return Value</span></span>

### <a name="method-extendeddatatype"></a><span data-ttu-id="cc9f3-638">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-638">Method extendedDataType</span></span>

    public int extendedDataType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-639">Return Value</span></span>

### <a name="method-fieldhandle"></a><span data-ttu-id="cc9f3-640">メソッド fieldHandle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-640">Method fieldHandle</span></span>

    public FieldId fieldHandle()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-641">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="cc9f3-642">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-642">Method fieldName</span></span>

    public str fieldName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-643">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-643">Return Value</span></span>

### <a name="method-fontheight"></a><span data-ttu-id="cc9f3-644">メソッド fontHeight</span><span class="sxs-lookup"><span data-stu-id="cc9f3-644">Method fontHeight</span></span>

    public int fontHeight()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-645">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-645">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="cc9f3-646">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-646">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-647">Return Value</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="cc9f3-648">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="cc9f3-648">Method foregroundColor</span></span>

    public int foregroundColor()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-649">Return Value</span></span>

### <a name="method-formatvalue"></a><span data-ttu-id="cc9f3-650">メソッド formatValue</span><span class="sxs-lookup"><span data-stu-id="cc9f3-650">Method formatValue</span></span>

    public str formatValue()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-651">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-651">Return Value</span></span>

### <a name="method-height"></a><span data-ttu-id="cc9f3-652">メソッド height</span><span class="sxs-lookup"><span data-stu-id="cc9f3-652">Method height</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-653">Return Value</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="cc9f3-654">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="cc9f3-654">Method heightMode</span></span>

    public int heightMode()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-655">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-655">Return Value</span></span>

### <a name="method-hidezeros"></a><span data-ttu-id="cc9f3-656">メソッド hideZeros</span><span class="sxs-lookup"><span data-stu-id="cc9f3-656">Method hideZeros</span></span>

    public boolean hideZeros()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-657">Return Value</span></span>

### <a name="method-isoneline"></a><span data-ttu-id="cc9f3-658">メソッド isOneline</span><span class="sxs-lookup"><span data-stu-id="cc9f3-658">Method isOneline</span></span>

    public boolean isOneline()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-659">Return Value</span></span>

### <a name="method-isoverlapping"></a><span data-ttu-id="cc9f3-660">メソッド isOverlapping</span><span class="sxs-lookup"><span data-stu-id="cc9f3-660">Method isOverlapping</span></span>

    public boolean isOverlapping()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-661">Return Value</span></span>

### <a name="method-italic"></a><span data-ttu-id="cc9f3-662">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="cc9f3-662">Method italic</span></span>

    public boolean italic()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-663">Return Value</span></span>

### <a name="method-lateeval"></a><span data-ttu-id="cc9f3-664">メソッド lateEval</span><span class="sxs-lookup"><span data-stu-id="cc9f3-664">Method lateEval</span></span>

    public LateEvalMode lateEval()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-665">Return Value</span></span>

### <a name="method-linebottom"></a><span data-ttu-id="cc9f3-666">メソッド lineBottom</span><span class="sxs-lookup"><span data-stu-id="cc9f3-666">Method lineBottom</span></span>

    public LineType lineBottom()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-667">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-667">Return Value</span></span>

### <a name="method-lineleft"></a><span data-ttu-id="cc9f3-668">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="cc9f3-668">Method lineLeft</span></span>

    public LineType lineLeft()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-669">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-669">Return Value</span></span>

### <a name="method-lineright"></a><span data-ttu-id="cc9f3-670">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="cc9f3-670">Method lineRight</span></span>

    public LineType lineRight()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-671">Return Value</span></span>

### <a name="method-linetop"></a><span data-ttu-id="cc9f3-672">メソッド lineTop</span><span class="sxs-lookup"><span data-stu-id="cc9f3-672">Method lineTop</span></span>

    public LineType lineTop()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-673">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-673">Return Value</span></span>

### <a name="method-menufunctionhelp"></a><span data-ttu-id="cc9f3-674">メソッド menuFunctionHelp</span><span class="sxs-lookup"><span data-stu-id="cc9f3-674">Method menuFunctionHelp</span></span>

    public str menuFunctionHelp()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-675">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-675">Return Value</span></span>

### <a name="method-menufunctionname"></a><span data-ttu-id="cc9f3-676">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-676">Method menuFunctionName</span></span>

    public str menuFunctionName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-677">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-677">Return Value</span></span>

### <a name="method-menufunctiontype"></a><span data-ttu-id="cc9f3-678">メソッド menuFunctionType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-678">Method menuFunctionType</span></span>

    public int menuFunctionType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-679">Return Value</span></span>

### <a name="method-menufunctionweb"></a><span data-ttu-id="cc9f3-680">メソッド menuFunctionWeb</span><span class="sxs-lookup"><span data-stu-id="cc9f3-680">Method menuFunctionWeb</span></span>

    public str menuFunctionWeb()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-681">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-681">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="cc9f3-682">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cc9f3-682">Method name</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-683">Return Value</span></span>

### <a name="method-recid"></a><span data-ttu-id="cc9f3-684">メソッド recId</span><span class="sxs-lookup"><span data-stu-id="cc9f3-684">Method recId</span></span>

    public int recId()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-685">Return Value</span></span>

### <a name="method-showprompt"></a><span data-ttu-id="cc9f3-686">メソッド showPrompt</span><span class="sxs-lookup"><span data-stu-id="cc9f3-686">Method showPrompt</span></span>

    public boolean showPrompt()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-687">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-687">Return Value</span></span>

### <a name="method-strikethrough"></a><span data-ttu-id="cc9f3-688">メソッド strikeThrough</span><span class="sxs-lookup"><span data-stu-id="cc9f3-688">Method strikeThrough</span></span>

    public boolean strikeThrough()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-689">Return Value</span></span>

### <a name="method-tablehandle"></a><span data-ttu-id="cc9f3-690">メソッド tableHandle</span><span class="sxs-lookup"><span data-stu-id="cc9f3-690">Method tableHandle</span></span>

    public TableId tableHandle()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-691">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-691">Return Value</span></span>

### <a name="method-tablename"></a><span data-ttu-id="cc9f3-692">メソッド tableName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-692">Method tableName</span></span>

    public str tableName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-693">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-693">Return Value</span></span>

### <a name="method-turnsign"></a><span data-ttu-id="cc9f3-694">メソッド turnSign</span><span class="sxs-lookup"><span data-stu-id="cc9f3-694">Method turnSign</span></span>

    public boolean turnSign()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-695">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-695">Return Value</span></span>

### <a name="method-type"></a><span data-ttu-id="cc9f3-696">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="cc9f3-696">Method type</span></span>

    public int type()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-697">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-697">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="cc9f3-698">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="cc9f3-698">Method underline</span></span>

    public boolean underline()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-699">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-699">Return Value</span></span>

### <a name="method-webmenuitemname"></a><span data-ttu-id="cc9f3-700">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-700">Method webMenuItemName</span></span>

    public str webMenuItemName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-701">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-701">Return Value</span></span>

### <a name="method-webmenuitemtype"></a><span data-ttu-id="cc9f3-702">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-702">Method webMenuItemType</span></span>

    public int webMenuItemType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-703">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-703">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="cc9f3-704">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="cc9f3-704">Method webTarget</span></span>

    public str webTarget()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-705">Return Value</span></span>

### <a name="method-weight"></a><span data-ttu-id="cc9f3-706">メソッド weight</span><span class="sxs-lookup"><span data-stu-id="cc9f3-706">Method weight</span></span>

    public int weight()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-707">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="cc9f3-708">メソッド width</span><span class="sxs-lookup"><span data-stu-id="cc9f3-708">Method width</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-709">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-709">Return Value</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="cc9f3-710">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="cc9f3-710">Method widthMode</span></span>

    public int widthMode()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-711">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-711">Return Value</span></span>

### <a name="method-xpos"></a><span data-ttu-id="cc9f3-712">メソッド xPos</span><span class="sxs-lookup"><span data-stu-id="cc9f3-712">Method xPos</span></span>

    public int xPos()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-713">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-713">Return Value</span></span>

### <a name="method-ypos"></a><span data-ttu-id="cc9f3-714">メソッド yPos</span><span class="sxs-lookup"><span data-stu-id="cc9f3-714">Method yPos</span></span>

    public int yPos()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-715">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-715">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-716">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-716">Method new</span></span>

<span data-ttu-id="cc9f3-717">OutputField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-717">Initializes a new instance of the OutputField class.</span></span>

    public void new()

## <a name="class-outputfootersection"></a><span data-ttu-id="cc9f3-718">クラス OutputFooterSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-718">Class OutputFooterSection</span></span>
    class OutputFooterSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-719">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-719">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-720">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-720">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-721">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-721">Methods</span></span>

| <span data-ttu-id="cc9f3-722">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-722">Method</span></span>                                | <span data-ttu-id="cc9f3-723">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-723">Description</span></span>                                                  |
|---------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="cc9f3-724">public int level()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-724">public int level()</span></span>                    |                                                              |
| <span data-ttu-id="cc9f3-725">public int level2field(\[int level\])</span><span class="sxs-lookup"><span data-stu-id="cc9f3-725">public int level2field(\[int level\])</span></span> |                                                              |
| <span data-ttu-id="cc9f3-726">public int niveau()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-726">public int niveau()</span></span>                   |                                                              |
| <span data-ttu-id="cc9f3-727">public int table()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-727">public int table()</span></span>                    |                                                              |
| <span data-ttu-id="cc9f3-728">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-728">public void new()</span></span>                     | <span data-ttu-id="cc9f3-729">OutputFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-729">Initializes a new instance of the OutputFooterSection class.</span></span> |

### <a name="method-level"></a><span data-ttu-id="cc9f3-730">メソッド level</span><span class="sxs-lookup"><span data-stu-id="cc9f3-730">Method level</span></span>

    public int level()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-731">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-731">Return Value</span></span>

### <a name="method-level2field"></a><span data-ttu-id="cc9f3-732">メソッド level2field</span><span class="sxs-lookup"><span data-stu-id="cc9f3-732">Method level2field</span></span>

    public int level2field([int level])

#### <a name="parameters"></a><span data-ttu-id="cc9f3-733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-733">Parameters</span></span>

<span data-ttu-id="cc9f3-734">level</span><span class="sxs-lookup"><span data-stu-id="cc9f3-734">level</span></span>  

#### <a name="return-value"></a><span data-ttu-id="cc9f3-735">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-735">Return Value</span></span>

### <a name="method-niveau"></a><span data-ttu-id="cc9f3-736">メソッド niveau</span><span class="sxs-lookup"><span data-stu-id="cc9f3-736">Method niveau</span></span>

    public int niveau()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-737">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-737">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="cc9f3-738">メソッド table</span><span class="sxs-lookup"><span data-stu-id="cc9f3-738">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-739">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-740">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-740">Method new</span></span>

<span data-ttu-id="cc9f3-741">OutputFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-741">Initializes a new instance of the OutputFooterSection class.</span></span>

    public void new()

## <a name="class-outputheadersection"></a><span data-ttu-id="cc9f3-742">クラス OutputHeaderSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-742">Class OutputHeaderSection</span></span>
    class OutputHeaderSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-743">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-743">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-744">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-744">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-745">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-745">Methods</span></span>

| <span data-ttu-id="cc9f3-746">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-746">Method</span></span>             | <span data-ttu-id="cc9f3-747">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-747">Description</span></span>                                                  |
|--------------------|--------------------------------------------------------------|
| <span data-ttu-id="cc9f3-748">public int table()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-748">public int table()</span></span> |                                                              |
| <span data-ttu-id="cc9f3-749">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-749">public void new()</span></span>  | <span data-ttu-id="cc9f3-750">OutputHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-750">Initializes a new instance of the OutputHeaderSection class.</span></span> |

### <a name="method-table"></a><span data-ttu-id="cc9f3-751">メソッド table</span><span class="sxs-lookup"><span data-stu-id="cc9f3-751">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-752">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-752">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-753">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-753">Method new</span></span>

<span data-ttu-id="cc9f3-754">OutputHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-754">Initializes a new instance of the OutputHeaderSection class.</span></span>

    public void new()

## <a name="class-outputintegerfield"></a><span data-ttu-id="cc9f3-755">クラス OutputIntegerField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-755">Class OutputIntegerField</span></span>
    class OutputIntegerField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-756">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-756">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-757">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-757">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-758">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-758">Methods</span></span>

| <span data-ttu-id="cc9f3-759">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-759">Method</span></span>                        | <span data-ttu-id="cc9f3-760">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-760">Description</span></span>                                                 |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cc9f3-761">public int displaceNegative()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-761">public int displaceNegative()</span></span> |                                                             |
| <span data-ttu-id="cc9f3-762">public boolean negative()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-762">public boolean negative()</span></span>     |                                                             |
| <span data-ttu-id="cc9f3-763">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-763">public str toString()</span></span>         | <span data-ttu-id="cc9f3-764">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-764">Returns a string that represents the current object.</span></span>        |
| <span data-ttu-id="cc9f3-765">public int value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-765">public int value()</span></span>            |                                                             |
| <span data-ttu-id="cc9f3-766">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-766">public void new()</span></span>             | <span data-ttu-id="cc9f3-767">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-767">Initializes a new instance of the OutputIntegerField class.</span></span> |

### <a name="method-displacenegative"></a><span data-ttu-id="cc9f3-768">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="cc9f3-768">Method displaceNegative</span></span>

    public int displaceNegative()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-769">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-769">Return Value</span></span>

### <a name="method-negative"></a><span data-ttu-id="cc9f3-770">メソッド negative</span><span class="sxs-lookup"><span data-stu-id="cc9f3-770">Method negative</span></span>

    public boolean negative()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-771">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-771">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-772">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-772">Method toString</span></span>

<span data-ttu-id="cc9f3-773">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-773">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-774">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-774">Return Value</span></span>

<span data-ttu-id="cc9f3-775">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-775">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-776">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-776">Remarks</span></span>

<span data-ttu-id="cc9f3-777">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-777">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-778">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-778">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-779">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-779">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-780">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-780">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-781">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-781">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-782">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-782">Method new</span></span>

<span data-ttu-id="cc9f3-783">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-783">Initializes a new instance of the OutputIntegerField class.</span></span>

    public void new()

## <a name="class-outputlabelfield"></a><span data-ttu-id="cc9f3-784">クラス OutputLabelField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-784">Class OutputLabelField</span></span>
    class OutputLabelField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-785">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-785">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-786">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-786">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-787">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-787">Methods</span></span>

| <span data-ttu-id="cc9f3-788">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-788">Method</span></span>                | <span data-ttu-id="cc9f3-789">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-789">Description</span></span>                                               |
|-----------------------|-----------------------------------------------------------|
| <span data-ttu-id="cc9f3-790">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-790">public str toString()</span></span> | <span data-ttu-id="cc9f3-791">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-791">Returns a string that represents the current object.</span></span>      |
| <span data-ttu-id="cc9f3-792">public str value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-792">public str value()</span></span>    |                                                           |
| <span data-ttu-id="cc9f3-793">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-793">public void new()</span></span>     | <span data-ttu-id="cc9f3-794">OutputLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-794">Initializes a new instance of the OutputLabelField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-795">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-795">Method toString</span></span>

<span data-ttu-id="cc9f3-796">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-796">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-797">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-797">Return Value</span></span>

<span data-ttu-id="cc9f3-798">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-798">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-799">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-799">Remarks</span></span>

<span data-ttu-id="cc9f3-800">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-800">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-801">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-801">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-802">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-802">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-803">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-803">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-804">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-804">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-805">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-805">Method new</span></span>

<span data-ttu-id="cc9f3-806">OutputLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-806">Initializes a new instance of the OutputLabelField class.</span></span>

    public void new()

## <a name="class-outputpage"></a><span data-ttu-id="cc9f3-807">クラス OutputPage</span><span class="sxs-lookup"><span data-stu-id="cc9f3-807">Class OutputPage</span></span>
    class OutputPage extends Object

### <a name="remarks"></a><span data-ttu-id="cc9f3-808">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-808">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-809">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-809">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-810">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-810">Methods</span></span>

| <span data-ttu-id="cc9f3-811">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-811">Method</span></span>                        | <span data-ttu-id="cc9f3-812">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-812">Description</span></span>                                         |
|-------------------------------|-----------------------------------------------------|
| <span data-ttu-id="cc9f3-813">public int bottomMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-813">public int bottomMargin()</span></span>     |                                                     |
| <span data-ttu-id="cc9f3-814">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-814">public str fontName()</span></span>         |                                                     |
| <span data-ttu-id="cc9f3-815">public int height()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-815">public int height()</span></span>           |                                                     |
| <span data-ttu-id="cc9f3-816">public boolean layoutRTL()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-816">public boolean layoutRTL()</span></span>    |                                                     |
| <span data-ttu-id="cc9f3-817">public int leftMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-817">public int leftMargin()</span></span>       |                                                     |
| <span data-ttu-id="cc9f3-818">public str pageNumber()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-818">public str pageNumber()</span></span>       |                                                     |
| <span data-ttu-id="cc9f3-819">public int rightMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-819">public int rightMargin()</span></span>      |                                                     |
| <span data-ttu-id="cc9f3-820">public int sectionNo()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-820">public int sectionNo()</span></span>        |                                                     |
| <span data-ttu-id="cc9f3-821">public int topMargin()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-821">public int topMargin()</span></span>        |                                                     |
| <span data-ttu-id="cc9f3-822">public int unusedBottom()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-822">public int unusedBottom()</span></span>     |                                                     |
| <span data-ttu-id="cc9f3-823">public int unusedLeft()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-823">public int unusedLeft()</span></span>       |                                                     |
| <span data-ttu-id="cc9f3-824">public int unusedRight()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-824">public int unusedRight()</span></span>      |                                                     |
| <span data-ttu-id="cc9f3-825">public int unusedTop()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-825">public int unusedTop()</span></span>        |                                                     |
| <span data-ttu-id="cc9f3-826">public int virtualPageWidth()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-826">public int virtualPageWidth()</span></span> |                                                     |
| <span data-ttu-id="cc9f3-827">public int width()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-827">public int width()</span></span>            |                                                     |
| <span data-ttu-id="cc9f3-828">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-828">public void new()</span></span>             | <span data-ttu-id="cc9f3-829">OutputPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-829">Initializes a new instance of the OutputPage class.</span></span> |

### <a name="method-bottommargin"></a><span data-ttu-id="cc9f3-830">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-830">Method bottomMargin</span></span>

    public int bottomMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-831">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="cc9f3-832">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="cc9f3-832">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-833">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-833">Return Value</span></span>

### <a name="method-height"></a><span data-ttu-id="cc9f3-834">メソッド height</span><span class="sxs-lookup"><span data-stu-id="cc9f3-834">Method height</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-835">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-835">Return Value</span></span>

### <a name="method-layoutrtl"></a><span data-ttu-id="cc9f3-836">メソッド layoutRTL</span><span class="sxs-lookup"><span data-stu-id="cc9f3-836">Method layoutRTL</span></span>

    public boolean layoutRTL()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-837">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-837">Return Value</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="cc9f3-838">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-838">Method leftMargin</span></span>

    public int leftMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-839">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-839">Return Value</span></span>

### <a name="method-pagenumber"></a><span data-ttu-id="cc9f3-840">メソッド pageNumber</span><span class="sxs-lookup"><span data-stu-id="cc9f3-840">Method pageNumber</span></span>

    public str pageNumber()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-841">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-841">Return Value</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="cc9f3-842">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-842">Method rightMargin</span></span>

    public int rightMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-843">Return Value</span></span>

### <a name="method-sectionno"></a><span data-ttu-id="cc9f3-844">メソッド sectionNo</span><span class="sxs-lookup"><span data-stu-id="cc9f3-844">Method sectionNo</span></span>

    public int sectionNo()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-845">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-845">Return Value</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="cc9f3-846">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="cc9f3-846">Method topMargin</span></span>

    public int topMargin()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-847">Return Value</span></span>

### <a name="method-unusedbottom"></a><span data-ttu-id="cc9f3-848">メソッド unusedBottom</span><span class="sxs-lookup"><span data-stu-id="cc9f3-848">Method unusedBottom</span></span>

    public int unusedBottom()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-849">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-849">Return Value</span></span>

### <a name="method-unusedleft"></a><span data-ttu-id="cc9f3-850">メソッド unusedLeft</span><span class="sxs-lookup"><span data-stu-id="cc9f3-850">Method unusedLeft</span></span>

    public int unusedLeft()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-851">Return Value</span></span>

### <a name="method-unusedright"></a><span data-ttu-id="cc9f3-852">メソッド unusedRight</span><span class="sxs-lookup"><span data-stu-id="cc9f3-852">Method unusedRight</span></span>

    public int unusedRight()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-853">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-853">Return Value</span></span>

### <a name="method-unusedtop"></a><span data-ttu-id="cc9f3-854">メソッド unusedTop</span><span class="sxs-lookup"><span data-stu-id="cc9f3-854">Method unusedTop</span></span>

    public int unusedTop()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-855">Return Value</span></span>

### <a name="method-virtualpagewidth"></a><span data-ttu-id="cc9f3-856">メソッド virtualPageWidth</span><span class="sxs-lookup"><span data-stu-id="cc9f3-856">Method virtualPageWidth</span></span>

    public int virtualPageWidth()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-857">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-857">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="cc9f3-858">メソッド width</span><span class="sxs-lookup"><span data-stu-id="cc9f3-858">Method width</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-859">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-860">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-860">Method new</span></span>

<span data-ttu-id="cc9f3-861">OutputPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-861">Initializes a new instance of the OutputPage class.</span></span>

    public void new()

## <a name="class-outputpagefootersection"></a><span data-ttu-id="cc9f3-862">クラス OutputPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-862">Class OutputPageFooterSection</span></span>
    class OutputPageFooterSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-863">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-863">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-864">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-864">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-865">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-865">Methods</span></span>

| <span data-ttu-id="cc9f3-866">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-866">Method</span></span>            | <span data-ttu-id="cc9f3-867">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-867">Description</span></span>                                                      |
|-------------------|------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-868">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-868">public void new()</span></span> | <span data-ttu-id="cc9f3-869">OutputPageFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-869">Initializes a new instance of the OutputPageFooterSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-870">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-870">Method new</span></span>

<span data-ttu-id="cc9f3-871">OutputPageFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-871">Initializes a new instance of the OutputPageFooterSection class.</span></span>

    public void new()

## <a name="class-outputpageheadersection"></a><span data-ttu-id="cc9f3-872">クラス OutputPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-872">Class OutputPageHeaderSection</span></span>
    class OutputPageHeaderSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-873">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-873">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-874">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-874">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-875">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-875">Methods</span></span>

| <span data-ttu-id="cc9f3-876">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-876">Method</span></span>            | <span data-ttu-id="cc9f3-877">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-877">Description</span></span>                                                      |
|-------------------|------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-878">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-878">public void new()</span></span> | <span data-ttu-id="cc9f3-879">OutputPageHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-879">Initializes a new instance of the OutputPageHeaderSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-880">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-880">Method new</span></span>

<span data-ttu-id="cc9f3-881">OutputPageHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-881">Initializes a new instance of the OutputPageHeaderSection class.</span></span>

    public void new()

## <a name="class-outputprogrammablesection"></a><span data-ttu-id="cc9f3-882">クラス OutputProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-882">Class OutputProgrammableSection</span></span>
    class OutputProgrammableSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-883">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-883">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-884">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-884">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-885">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-885">Methods</span></span>

| <span data-ttu-id="cc9f3-886">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-886">Method</span></span>              | <span data-ttu-id="cc9f3-887">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-887">Description</span></span>                                                        |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-888">public str number()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-888">public str number()</span></span> |                                                                    |
| <span data-ttu-id="cc9f3-889">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-889">public void new()</span></span>   | <span data-ttu-id="cc9f3-890">OutputProgrammableSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-890">Initializes a new instance of the OutputProgrammableSection class.</span></span> |

### <a name="method-number"></a><span data-ttu-id="cc9f3-891">メソッド number</span><span class="sxs-lookup"><span data-stu-id="cc9f3-891">Method number</span></span>

    public str number()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-892">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-892">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-893">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-893">Method new</span></span>

<span data-ttu-id="cc9f3-894">OutputProgrammableSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-894">Initializes a new instance of the OutputProgrammableSection class.</span></span>

    public void new()

## <a name="class-outputprologsection"></a><span data-ttu-id="cc9f3-895">クラス OutputPrologSection</span><span class="sxs-lookup"><span data-stu-id="cc9f3-895">Class OutputPrologSection</span></span>
    class OutputPrologSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="cc9f3-896">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-896">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-897">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-897">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-898">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-898">Methods</span></span>

| <span data-ttu-id="cc9f3-899">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-899">Method</span></span>            | <span data-ttu-id="cc9f3-900">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-900">Description</span></span>                                                  |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="cc9f3-901">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-901">public void new()</span></span> | <span data-ttu-id="cc9f3-902">OutputPrologSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-902">Initializes a new instance of the OutputPrologSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="cc9f3-903">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-903">Method new</span></span>

<span data-ttu-id="cc9f3-904">OutputPrologSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-904">Initializes a new instance of the OutputPrologSection class.</span></span>

    public void new()

## <a name="class-outputrealfield"></a><span data-ttu-id="cc9f3-905">クラス OutputRealField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-905">Class OutputRealField</span></span>
    class OutputRealField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-906">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-906">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-907">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-907">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-908">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-908">Methods</span></span>

| <span data-ttu-id="cc9f3-909">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-909">Method</span></span>                        | <span data-ttu-id="cc9f3-910">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-910">Description</span></span>                                              |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="cc9f3-911">public int displaceNegative()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-911">public int displaceNegative()</span></span> |                                                          |
| <span data-ttu-id="cc9f3-912">public boolean negative()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-912">public boolean negative()</span></span>     |                                                          |
| <span data-ttu-id="cc9f3-913">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-913">public str toString()</span></span>         | <span data-ttu-id="cc9f3-914">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-914">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="cc9f3-915">public Real value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-915">public Real value()</span></span>           |                                                          |
| <span data-ttu-id="cc9f3-916">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-916">public void new()</span></span>             | <span data-ttu-id="cc9f3-917">OutputRealField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-917">Initializes a new instance of the OutputRealField class.</span></span> |

### <a name="method-displacenegative"></a><span data-ttu-id="cc9f3-918">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="cc9f3-918">Method displaceNegative</span></span>

    public int displaceNegative()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-919">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-919">Return Value</span></span>

### <a name="method-negative"></a><span data-ttu-id="cc9f3-920">メソッド negative</span><span class="sxs-lookup"><span data-stu-id="cc9f3-920">Method negative</span></span>

    public boolean negative()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-921">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-922">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-922">Method toString</span></span>

<span data-ttu-id="cc9f3-923">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-923">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-924">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-924">Return Value</span></span>

<span data-ttu-id="cc9f3-925">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-925">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-926">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-926">Remarks</span></span>

<span data-ttu-id="cc9f3-927">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-927">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-928">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-928">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-929">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-929">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-930">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-930">Method value</span></span>

    public Real value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-931">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-932">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-932">Method new</span></span>

<span data-ttu-id="cc9f3-933">OutputRealField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-933">Initializes a new instance of the OutputRealField class.</span></span>

    public void new()

## <a name="class-outputshapefield"></a><span data-ttu-id="cc9f3-934">クラス OutputShapeField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-934">Class OutputShapeField</span></span>
    class OutputShapeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-935">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-935">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-936">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-936">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-937">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-937">Methods</span></span>

| <span data-ttu-id="cc9f3-938">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-938">Method</span></span>                       | <span data-ttu-id="cc9f3-939">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-939">Description</span></span>                                               |
|------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="cc9f3-940">public int borderWidth()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-940">public int borderWidth()</span></span>     |                                                           |
| <span data-ttu-id="cc9f3-941">public LineType lineType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-941">public LineType lineType()</span></span>   |                                                           |
| <span data-ttu-id="cc9f3-942">public ShapeType shapeType()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-942">public ShapeType shapeType()</span></span> |                                                           |
| <span data-ttu-id="cc9f3-943">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-943">public str toString()</span></span>        | <span data-ttu-id="cc9f3-944">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-944">Returns a string that represents the current object.</span></span>      |
| <span data-ttu-id="cc9f3-945">public int value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-945">public int value()</span></span>           |                                                           |
| <span data-ttu-id="cc9f3-946">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-946">public void new()</span></span>            | <span data-ttu-id="cc9f3-947">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-947">Initializes a new instance of the OutputShapeField class.</span></span> |

### <a name="method-borderwidth"></a><span data-ttu-id="cc9f3-948">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="cc9f3-948">Method borderWidth</span></span>

    public int borderWidth()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-949">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-949">Return Value</span></span>

### <a name="method-linetype"></a><span data-ttu-id="cc9f3-950">メソッド lineType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-950">Method lineType</span></span>

    public LineType lineType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-951">Return Value</span></span>

### <a name="method-shapetype"></a><span data-ttu-id="cc9f3-952">メソッド shapeType</span><span class="sxs-lookup"><span data-stu-id="cc9f3-952">Method shapeType</span></span>

    public ShapeType shapeType()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-953">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-953">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-954">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-954">Method toString</span></span>

<span data-ttu-id="cc9f3-955">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-955">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-956">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-956">Return Value</span></span>

<span data-ttu-id="cc9f3-957">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-957">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-958">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-958">Remarks</span></span>

<span data-ttu-id="cc9f3-959">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-959">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-960">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-960">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-961">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-961">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-962">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-962">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-963">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-963">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-964">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-964">Method new</span></span>

<span data-ttu-id="cc9f3-965">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-965">Initializes a new instance of the OutputShapeField class.</span></span>

    public void new()

## <a name="class-outputstatictextfield"></a><span data-ttu-id="cc9f3-966">クラス OutputStaticTextField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-966">Class OutputStaticTextField</span></span>
    class OutputStaticTextField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-967">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-967">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-968">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-968">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-969">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-969">Methods</span></span>

| <span data-ttu-id="cc9f3-970">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-970">Method</span></span>                | <span data-ttu-id="cc9f3-971">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-971">Description</span></span>                                                    |
|-----------------------|----------------------------------------------------------------|
| <span data-ttu-id="cc9f3-972">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-972">public str toString()</span></span> | <span data-ttu-id="cc9f3-973">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-973">Returns a string that represents the current object.</span></span>           |
| <span data-ttu-id="cc9f3-974">public str value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-974">public str value()</span></span>    |                                                                |
| <span data-ttu-id="cc9f3-975">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-975">public void new()</span></span>     | <span data-ttu-id="cc9f3-976">OutputStaticTextField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-976">Initializes a new instance of the OutputStaticTextField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-977">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-977">Method toString</span></span>

<span data-ttu-id="cc9f3-978">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-978">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-979">Return Value</span></span>

<span data-ttu-id="cc9f3-980">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-980">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-981">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-981">Remarks</span></span>

<span data-ttu-id="cc9f3-982">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-982">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-983">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-983">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-984">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-984">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-985">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-985">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-986">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-987">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-987">Method new</span></span>

<span data-ttu-id="cc9f3-988">OutputStaticTextField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-988">Initializes a new instance of the OutputStaticTextField class.</span></span>

    public void new()

## <a name="class-outputstringfield"></a><span data-ttu-id="cc9f3-989">クラス OutputStringField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-989">Class OutputStringField</span></span>
    class OutputStringField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-990">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-990">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-991">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-991">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-992">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-992">Methods</span></span>

| <span data-ttu-id="cc9f3-993">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-993">Method</span></span>                | <span data-ttu-id="cc9f3-994">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-994">Description</span></span>                                                |
|-----------------------|------------------------------------------------------------|
| <span data-ttu-id="cc9f3-995">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-995">public str toString()</span></span> | <span data-ttu-id="cc9f3-996">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-996">Returns a string that represents the current object.</span></span>       |
| <span data-ttu-id="cc9f3-997">public str value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-997">public str value()</span></span>    |                                                            |
| <span data-ttu-id="cc9f3-998">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-998">public void new()</span></span>     | <span data-ttu-id="cc9f3-999">OutputStringField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-999">Initializes a new instance of the OutputStringField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-1000">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1000">Method toString</span></span>

<span data-ttu-id="cc9f3-1001">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1001">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1002">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1002">Return Value</span></span>

<span data-ttu-id="cc9f3-1003">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1003">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-1004">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1004">Remarks</span></span>

<span data-ttu-id="cc9f3-1005">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1005">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-1006">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1006">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-1007">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1007">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-1008">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1008">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1009">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1009">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-1010">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1010">Method new</span></span>

<span data-ttu-id="cc9f3-1011">OutputStringField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1011">Initializes a new instance of the OutputStringField class.</span></span>

    public void new()

## <a name="class-outputsumfield"></a><span data-ttu-id="cc9f3-1012">クラス OutputSumField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1012">Class OutputSumField</span></span>
    class OutputSumField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-1013">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1013">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-1014">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1014">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1015">Methods</span></span>

| <span data-ttu-id="cc9f3-1016">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1016">Method</span></span>                | <span data-ttu-id="cc9f3-1017">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1017">Description</span></span>                                             |
|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="cc9f3-1018">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1018">public str toString()</span></span> | <span data-ttu-id="cc9f3-1019">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1019">Returns a string that represents the current object.</span></span>    |
| <span data-ttu-id="cc9f3-1020">public Real value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1020">public Real value()</span></span>   |                                                         |
| <span data-ttu-id="cc9f3-1021">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1021">public void new()</span></span>     | <span data-ttu-id="cc9f3-1022">OutputSumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1022">Initializes a new instance of the OutputSumField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-1023">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1023">Method toString</span></span>

<span data-ttu-id="cc9f3-1024">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1024">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1025">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1025">Return Value</span></span>

<span data-ttu-id="cc9f3-1026">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1026">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-1027">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1027">Remarks</span></span>

<span data-ttu-id="cc9f3-1028">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1028">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-1029">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1029">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-1030">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1030">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-1031">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1031">Method value</span></span>

    public Real value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1032">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-1033">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1033">Method new</span></span>

<span data-ttu-id="cc9f3-1034">OutputSumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1034">Initializes a new instance of the OutputSumField class.</span></span>

    public void new()

## <a name="class-outputtimefield"></a><span data-ttu-id="cc9f3-1035">クラス OutputTimeField</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1035">Class OutputTimeField</span></span>
    class OutputTimeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="cc9f3-1036">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1036">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-1037">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1037">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-1038">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1038">Methods</span></span>

| <span data-ttu-id="cc9f3-1039">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1039">Method</span></span>                | <span data-ttu-id="cc9f3-1040">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1040">Description</span></span>                                              |
|-----------------------|----------------------------------------------------------|
| <span data-ttu-id="cc9f3-1041">public str toString()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1041">public str toString()</span></span> | <span data-ttu-id="cc9f3-1042">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1042">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="cc9f3-1043">public int value()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1043">public int value()</span></span>    |                                                          |
| <span data-ttu-id="cc9f3-1044">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1044">public void new()</span></span>     | <span data-ttu-id="cc9f3-1045">OutputTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1045">Initializes a new instance of the OutputTimeField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="cc9f3-1046">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1046">Method toString</span></span>

<span data-ttu-id="cc9f3-1047">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1047">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1048">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1048">Return Value</span></span>

<span data-ttu-id="cc9f3-1049">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1049">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-1050">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1050">Remarks</span></span>

<span data-ttu-id="cc9f3-1051">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1051">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="cc9f3-1052">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1052">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="cc9f3-1053">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1053">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="cc9f3-1054">メソッド value</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1054">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1055">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1055">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-1056">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1056">Method new</span></span>

<span data-ttu-id="cc9f3-1057">OutputTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1057">Initializes a new instance of the OutputTimeField class.</span></span>

    public void new()

## <a name="class-overwritesystemfieldspermission"></a><span data-ttu-id="cc9f3-1058">クラス OverwriteSystemfieldsPermission</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1058">Class OverwriteSystemfieldsPermission</span></span>
    class OverwriteSystemfieldsPermission extends CodeAccessPermission

### <a name="remarks"></a><span data-ttu-id="cc9f3-1059">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1059">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="cc9f3-1060">例</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1060">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="cc9f3-1061">メソッド</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1061">Methods</span></span>

| <span data-ttu-id="cc9f3-1062">方法</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1062">Method</span></span>                                                 | <span data-ttu-id="cc9f3-1063">説明</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1063">Description</span></span>                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f3-1064">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1064">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="cc9f3-1065">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1065">Creates and returns a copy of a permission class object.</span></span>                                                                  |
| <span data-ttu-id="cc9f3-1066">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1066">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="cc9f3-1067">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1067">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span> |
| <span data-ttu-id="cc9f3-1068">public void new()</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1068">public void new()</span></span>                                      | <span data-ttu-id="cc9f3-1069">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1069">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>                                                  |

### <a name="method-copy"></a><span data-ttu-id="cc9f3-1070">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1070">Method copy</span></span>

<span data-ttu-id="cc9f3-1071">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1071">Creates and returns a copy of a permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1072">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1072">Return Value</span></span>

<span data-ttu-id="cc9f3-1073">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1073">A copy of the derived class object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-1074">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1074">Remarks</span></span>

<span data-ttu-id="cc9f3-1075">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1075">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="cc9f3-1076">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1076">For more information, see “Securing an API that Executes on the Server Tier.”</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="cc9f3-1077">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1077">Method isSubsetOf</span></span>

<span data-ttu-id="cc9f3-1078">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1078">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="cc9f3-1079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1079">Parameters</span></span>

<span data-ttu-id="cc9f3-1080">target</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1080">target</span></span>  
<span data-ttu-id="cc9f3-1081">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1081">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cc9f3-1082">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1082">Return Value</span></span>

<span data-ttu-id="cc9f3-1083">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1083">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc9f3-1084">備考</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1084">Remarks</span></span>

<span data-ttu-id="cc9f3-1085">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1085">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="cc9f3-1086">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1086">For more information, see “Securing an API that Executes on the Server Tier.”</span></span>

### <a name="method-new"></a><span data-ttu-id="cc9f3-1087">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1087">Method new</span></span>

<span data-ttu-id="cc9f3-1088">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cc9f3-1088">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>

    public void new()




