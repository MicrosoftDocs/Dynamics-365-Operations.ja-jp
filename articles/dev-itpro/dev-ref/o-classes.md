---
title: O クラス
description: 文字 O で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52201
ms.assetid: 63f93d3d-54a5-46c2-b356-fe5863b6f927
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 629a4dfcdf1205bcb2c659039822c0a63f5e759c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369721"
---
# <a name="o-classes"></a><span data-ttu-id="d5a45-103">O クラス</span><span class="sxs-lookup"><span data-stu-id="d5a45-103">O classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5a45-104">文字 O で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="d5a45-104">System API classes that start with the letter O.</span></span>

<a name="class-object"></a><span data-ttu-id="d5a45-105">クラス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d5a45-105">Class Object</span></span>
------------

    class Object

<span data-ttu-id="d5a45-106">Object クラスは、その他のすべてのクラスの派生元となる基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-106">The Object class is the base class from which all other classes are derived.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5a45-107">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-107">Remarks</span></span>

<span data-ttu-id="d5a45-108">オブジェクト クラスのメソッドは、任意のオブジェクトに対して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-108">Methods in the Object class can be called for any object.</span></span> <span data-ttu-id="d5a45-109">Object クラスは、開発者がオブジェクトの実際のタイプを知らなくても、割り当ておよび等価チェックを実行できるようにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-109">The Object class is used to allow assignment and equality checks to be performed without the developer having to know the actual type of the object.</span></span> <span data-ttu-id="d5a45-110">メソッドは 3 つのグループにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-110">The methods can be grouped into three groups:</span></span>

-   <span data-ttu-id="d5a45-111">タイム アウト メソッド - 指定した時間が経過した後にメソッドをアクティブにするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-111">Time out methods - can be used to activate a method after a specified period of time has passed.</span></span>
-   <span data-ttu-id="d5a45-112">プロセス フローを制御したり、別のオブジェクトがそのタスクを終了するを待機するために使用される、Wait、Notify、NotifyAll メソッドなどのメソッドを処理します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-112">Process methods, such as the Wait, Notify, and NotifyAll method - used to control process flow and to wait for another object to finish its task.</span></span>
-   <span data-ttu-id="d5a45-113">クラス メソッド - オブジェクトに関する基本情報を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-113">Class methods - return basic information about the object.</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-114">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-114">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-115">Methods</span></span>

| <span data-ttu-id="d5a45-116">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-116">Method</span></span>                                                                      | <span data-ttu-id="d5a45-117">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-117">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a45-118">public boolean equal(Object object)</span><span class="sxs-lookup"><span data-stu-id="d5a45-118">public boolean equal(Object object)</span></span>                                         | <span data-ttu-id="d5a45-119">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-119">Determines whether the specified object is equal to the current one.</span></span>                                        |
| <span data-ttu-id="d5a45-120">public int getTimeOutTimerHandle()</span><span class="sxs-lookup"><span data-stu-id="d5a45-120">public int getTimeOutTimerHandle()</span></span>                                          | <span data-ttu-id="d5a45-121">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-121">Returns the timer handle for the object.</span></span>                                                                    |
| <span data-ttu-id="d5a45-122">public ClassId handle()</span><span class="sxs-lookup"><span data-stu-id="d5a45-122">public ClassId handle()</span></span>                                                     | <span data-ttu-id="d5a45-123">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-123">Retrieves the handle of the class of the object.</span></span>                                                            |
| <span data-ttu-id="d5a45-124">public boolean SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="d5a45-124">public boolean SysObsoleteAttribute()</span></span>                                       |                                                                                                             |
| <span data-ttu-id="d5a45-125">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span><span class="sxs-lookup"><span data-stu-id="d5a45-125">public int SysObsoleteAttribute(str Method, int WaitTime, \[boolean idle\])</span></span> |                                                                                                             |
| <span data-ttu-id="d5a45-126">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-126">public str toString()</span></span>                                                       | <span data-ttu-id="d5a45-127">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-127">Returns a string that represents the current object.</span></span>                                                        |
| <span data-ttu-id="d5a45-128">public int usageCount()</span><span class="sxs-lookup"><span data-stu-id="d5a45-128">public int usageCount()</span></span>                                                     | <span data-ttu-id="d5a45-129">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-129">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span> |
| <span data-ttu-id="d5a45-130">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="d5a45-130">public str xml(\[int indent\])</span></span>                                              | <span data-ttu-id="d5a45-131">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-131">Returns an XML string that represents the current object.</span></span>                                                   |
| <span data-ttu-id="d5a45-132">public boolean Equals(System.Object obj)</span><span class="sxs-lookup"><span data-stu-id="d5a45-132">public boolean Equals(System.Object obj)</span></span>                                    |                                                                                                             |
| <span data-ttu-id="d5a45-133">public int GetHashCode()</span><span class="sxs-lookup"><span data-stu-id="d5a45-133">public int GetHashCode()</span></span>                                                    |                                                                                                             |
| <span data-ttu-id="d5a45-134">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d5a45-134">public void finalize()</span></span>                                                      |                                                                                                             |
| <span data-ttu-id="d5a45-135">public void wait()</span><span class="sxs-lookup"><span data-stu-id="d5a45-135">public void wait()</span></span>                                                          | <span data-ttu-id="d5a45-136">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-136">Pauses a process.</span></span>                                                                                           |
| <span data-ttu-id="d5a45-137">public void cancelTimeOut(int timerHandle)</span><span class="sxs-lookup"><span data-stu-id="d5a45-137">public void cancelTimeOut(int timerHandle)</span></span>                                  | <span data-ttu-id="d5a45-138">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-138">Cancels a previous method call to the setTimeOut method.</span></span>                                                    |
| <span data-ttu-id="d5a45-139">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-139">public void new()</span></span>                                                           | <span data-ttu-id="d5a45-140">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-140">Initializes a new instance of the Object class.</span></span>                                                             |
| <span data-ttu-id="d5a45-141">public void notify()</span><span class="sxs-lookup"><span data-stu-id="d5a45-141">public void notify()</span></span>                                                        | <span data-ttu-id="d5a45-142">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-142">Releases the hold on an object that has called the wait method on this object.</span></span>                              |
| <span data-ttu-id="d5a45-143">public void notifyAll()</span><span class="sxs-lookup"><span data-stu-id="d5a45-143">public void notifyAll()</span></span>                                                     | <span data-ttu-id="d5a45-144">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-144">Releases a lock on the object that was issued by the wait method on this object.</span></span>                            |

### <a name="method-equal"></a><span data-ttu-id="d5a45-145">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="d5a45-145">Method equal</span></span>

<span data-ttu-id="d5a45-146">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-146">Determines whether the specified object is equal to the current one.</span></span>

    public boolean equal(Object object)

#### <a name="parameters"></a><span data-ttu-id="d5a45-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-147">Parameters</span></span>

<span data-ttu-id="d5a45-148">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d5a45-148">object</span></span>  
<span data-ttu-id="d5a45-149">現在のオブジェクトと比較するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d5a45-149">The object to compare with the current object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d5a45-150">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-150">Return Value</span></span>

<span data-ttu-id="d5a45-151">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d5a45-151">true if the specified object is equal to the current object; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-152">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-152">Remarks</span></span>

<span data-ttu-id="d5a45-153">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-153">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="d5a45-154">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-154">Derived classes can, however, override the Object::equal method to support value equality.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-155">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-155">Examples</span></span>

<span data-ttu-id="d5a45-156">次の例では、現在のインスタンスと別のオブジェクトを比較します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-156">The following example compares the current instance with another object.</span></span>

    static void Object_Equal(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB = new Object(); 
        print objA.equal(objA);  // true. 
        print objA.equal(objB);  // false. 
        objA = objB; 
        print objA.equal(objB);  // true. 
     }

### <a name="method-gettimeouttimerhandle"></a><span data-ttu-id="d5a45-157">メソッド getTimeOutTimerHandle</span><span class="sxs-lookup"><span data-stu-id="d5a45-157">Method getTimeOutTimerHandle</span></span>

<span data-ttu-id="d5a45-158">オブジェクトのタイマー ハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-158">Returns the timer handle for the object.</span></span>

    public int getTimeOutTimerHandle()

#### <a name="return-value"></a><span data-ttu-id="d5a45-159">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-159">Return Value</span></span>

<span data-ttu-id="d5a45-160">オブジェクトのタイマー ハンドル。</span><span class="sxs-lookup"><span data-stu-id="d5a45-160">The timer handle of the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-161">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-161">Remarks</span></span>

<span data-ttu-id="d5a45-162">オブジェクトのタイマー ハンドルは、setTimeOut メソッドを呼び出すことによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-162">The timer handle of the object is set by calling the setTimeOut method.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-163">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-163">Examples</span></span>

<span data-ttu-id="d5a45-164">次の例では、タイムアウトを設定してから、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-164">The following example sets a timeout, and then cancels it.</span></span>

    public void myJob() 
    { 
        int timerHandle = 0; 
        this.setTimeOut(identifierstr(workerFunction), 0); 
        //Perform some operations. 
        timerHandle = this.getTimeOutTimerHandle(); 
        this.cancelTimeOut( timerHandle ); 
    }

### <a name="method-handle"></a><span data-ttu-id="d5a45-165">メソッド handle</span><span class="sxs-lookup"><span data-stu-id="d5a45-165">Method handle</span></span>

<span data-ttu-id="d5a45-166">オブジェクトのクラスのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-166">Retrieves the handle of the class of the object.</span></span>

    public ClassId handle()

#### <a name="return-value"></a><span data-ttu-id="d5a45-167">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-167">Return Value</span></span>

<span data-ttu-id="d5a45-168">現在のオブジェクトのクラスのハンドル、つまり classId プロパティです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-168">The handle, that is, the classId property, of the class of the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-169">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-169">Remarks</span></span>

<span data-ttu-id="d5a45-170">クラスの処理が後のリリースで変更されない、またはユーザー定義クラスのエクスポートまたはインポートの後に変更されないという保証はありません。</span><span class="sxs-lookup"><span data-stu-id="d5a45-170">There is no guarantee that the handle of a class will remain unchanged in later releases, or after an export or import for user-defined classes.</span></span> <span data-ttu-id="d5a45-171">このメソッドによって返される値を、クラスを参照する永続的な定数として使用しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-171">It is strongly advised that the value that is returned by this method will not be used as a persistent constant to refer to the class.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d5a45-172">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d5a45-172">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="d5a45-173">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-173">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="d5a45-174">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="d5a45-174">Method SysObsoleteAttribute</span></span>

    public int SysObsoleteAttribute(str Method, int WaitTime, [boolean idle])

#### <a name="parameters"></a><span data-ttu-id="d5a45-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-175">Parameters</span></span>

<span data-ttu-id="d5a45-176">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-176">Method</span></span>  

<!-- -->

<span data-ttu-id="d5a45-177">WaitTime</span><span class="sxs-lookup"><span data-stu-id="d5a45-177">WaitTime</span></span>  

<!-- -->

<span data-ttu-id="d5a45-178">idle</span><span class="sxs-lookup"><span data-stu-id="d5a45-178">idle</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d5a45-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-179">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-180">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-180">Method toString</span></span>

<span data-ttu-id="d5a45-181">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-181">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-182">Return Value</span></span>

<span data-ttu-id="d5a45-183">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-183">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-184">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-184">Remarks</span></span>

<span data-ttu-id="d5a45-185">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-185">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-186">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-186">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-187">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-187">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-188">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-188">Examples</span></span>

<span data-ttu-id="d5a45-189">次の例では、o のクラス名を出力します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-189">The following example prints out the class name of o.</span></span>

    static void Object_ToString_Job(Args _args) 
    { 
        Object o = new Object(); 
        print o.toString();  // Prints out: "Class Object" 
        pause; 
    }

### <a name="method-usagecount"></a><span data-ttu-id="d5a45-190">メソッド usageCount</span><span class="sxs-lookup"><span data-stu-id="d5a45-190">Method usageCount</span></span>

<span data-ttu-id="d5a45-191">オブジェクトが持つ参照 (つまり、参照カウンターの値) の現在の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-191">Returns the current number of references, that is, the value of the reference counter, that the object has.</span></span>

    public int usageCount()

#### <a name="return-value"></a><span data-ttu-id="d5a45-192">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-192">Return Value</span></span>

<span data-ttu-id="d5a45-193">オブジェクトが持つ参照の現在の数。</span><span class="sxs-lookup"><span data-stu-id="d5a45-193">The current number of references that the object has.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-194">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-194">Remarks</span></span>

<span data-ttu-id="d5a45-195">オブジェクトが作成されると、その参照カウンターが 1 になります。</span><span class="sxs-lookup"><span data-stu-id="d5a45-195">When an object is created, its reference counter equals 1.</span></span> <span data-ttu-id="d5a45-196">新しい参照が作成されると、その値が増加します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-196">When a new reference is created, its value increases.</span></span> <span data-ttu-id="d5a45-197">スコープ外の参照は、値が減少します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-197">As a reference goes out of scope, its value decreases.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-198">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-198">Examples</span></span>

<span data-ttu-id="d5a45-199">次の例では、objA の参照の数を出力ウィンドウに出力します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-199">The following example prints the number of references for objA to the output window.</span></span>

    static void Object_UsageCount(Args _args) 
    { 
        Object objA = new Object(); 
        Object objB; 
        print objA.usageCount();    // Prints 1. 
        objB = objA;                // objB is a reference to objA. 
        print objA.usageCount();    // prints 2 
        pause; 
    }

### <a name="method-xml"></a><span data-ttu-id="d5a45-200">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="d5a45-200">Method xml</span></span>

<span data-ttu-id="d5a45-201">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-201">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="d5a45-202">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-202">Parameters</span></span>

<span data-ttu-id="d5a45-203">インデント</span><span class="sxs-lookup"><span data-stu-id="d5a45-203">indent</span></span>  
<span data-ttu-id="d5a45-204">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="d5a45-204">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d5a45-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-205">Return Value</span></span>

<span data-ttu-id="d5a45-206">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="d5a45-206">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-207">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-207">Remarks</span></span>

<span data-ttu-id="d5a45-208">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-208">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-equals"></a><span data-ttu-id="d5a45-209">メソッド Equals</span><span class="sxs-lookup"><span data-stu-id="d5a45-209">Method Equals</span></span>

    public boolean Equals(System.Object obj)

#### <a name="parameters"></a><span data-ttu-id="d5a45-210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-210">Parameters</span></span>

<span data-ttu-id="d5a45-211">obj</span><span class="sxs-lookup"><span data-stu-id="d5a45-211">obj</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d5a45-212">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-212">Return Value</span></span>

### <a name="method-gethashcode"></a><span data-ttu-id="d5a45-213">メソッド GetHashCode</span><span class="sxs-lookup"><span data-stu-id="d5a45-213">Method GetHashCode</span></span>

    public int GetHashCode()

#### <a name="return-value"></a><span data-ttu-id="d5a45-214">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-214">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="d5a45-215">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d5a45-215">Method finalize</span></span>

    public void finalize()

### <a name="method-wait"></a><span data-ttu-id="d5a45-216">メソッド wait</span><span class="sxs-lookup"><span data-stu-id="d5a45-216">Method wait</span></span>

<span data-ttu-id="d5a45-217">プロセスを一時停止します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-217">Pauses a process.</span></span>

    public void wait()

#### <a name="remarks"></a><span data-ttu-id="d5a45-218">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-218">Remarks</span></span>

<span data-ttu-id="d5a45-219">このメソッドの最も一般的な使い方は、ユーザーに何らかの入力を求めるオブジェクトを開始し、そのオブジェクト (フォームなど) の wait メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-219">The most common use for this method is to start an object that asks the user for some input and then call the wait method on that object, such as a form.</span></span> <span data-ttu-id="d5a45-220">次のコード行は、オブジェクトが notify メソッド または notifyAll メソッドを呼び出すまで実行されません。</span><span class="sxs-lookup"><span data-stu-id="d5a45-220">The next line of code is not executed until the object has called the notify or notifyAll method.</span></span> <span data-ttu-id="d5a45-221">フォームから wait メソッドが呼び出されるとき、ユーザーは通知メソッドを手動で呼び出す必要はありません。それは、ユーザーがフォームを閉じるか、または [適用] ボタンを押すと、フォームが Object.notifyAll メソッドを呼び出すためです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-221">When the wait method is called from a form, you do not have to call the notify methods manually because forms call the Object.notifyAll method when the user either closes the form or presses the Apply button.</span></span> <span data-ttu-id="d5a45-222">このメソッドはスレッドの同期のためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="d5a45-222">This method is not meant for thread synchronization.</span></span> <span data-ttu-id="d5a45-223">代わりに waitUntilSignaled メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-223">Use the waitUntilSignaled method instead.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-224">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-224">Examples</span></span>

<span data-ttu-id="d5a45-225">次の例では、GetUserInput ダイアログを開き、ブロックし、ユーザーがフォームを閉じるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-225">The following example opens the GetUserInput dialog, blocks, and waits until the user has closed the form.</span></span>

    { 
        Args a = new Args("GetUserInput"); 
        formRun fr = new formRun(a); 
        fr.init(); 
        fr.run(); 
        fr.wait(); 
        // Execution will resume at this point, only after 
        // the user has closed the form. 
    }

### <a name="method-canceltimeout"></a><span data-ttu-id="d5a45-226">メソッド cancelTimeOut</span><span class="sxs-lookup"><span data-stu-id="d5a45-226">Method cancelTimeOut</span></span>

<span data-ttu-id="d5a45-227">setTimeOut メソッドへ以前のメソッド呼び出しをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-227">Cancels a previous method call to the setTimeOut method.</span></span>

    public void cancelTimeOut(int timerHandle)

#### <a name="parameters"></a><span data-ttu-id="d5a45-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-228">Parameters</span></span>

<span data-ttu-id="d5a45-229">timerHandle</span><span class="sxs-lookup"><span data-stu-id="d5a45-229">timerHandle</span></span>  
<span data-ttu-id="d5a45-230">削除する予定イベントのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d5a45-230">The handle of the scheduled event to delete.</span></span> <span data-ttu-id="d5a45-231">ハンドルは、Object.setTimeOut メソッドによって返される値です。</span><span class="sxs-lookup"><span data-stu-id="d5a45-231">The handle is the value that is returned by the Object.setTimeOut method.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-232">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-232">Remarks</span></span>

<span data-ttu-id="d5a45-233">まだ処理されていないスケジュールされたタイムアウト呼び出しは、オブジェクト自体が削除されると自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-233">Any scheduled time-out calls that have not yet been processed are automatically deleted when the object itself is deleted.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-234">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-234">Examples</span></span>

<span data-ttu-id="d5a45-235">次の例では、Object.setTimeOut メソッドを呼び出した後、タイムアウトをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="d5a45-235">The following example calls the Object.setTimeOut method, and then cancels the time-out.</span></span>

    void Object_cancelTimeOut(Args _args) 
    { 
        int th; // timerHandle. 
        // timedMethod is a worker method. 
        th = this.setTimeOut( "timedMethod", 2000 ); 
        //.... 
        // Remove timeOut later. 
        CancelTimeOut(th); 
    }

### <a name="method-new"></a><span data-ttu-id="d5a45-236">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-236">Method new</span></span>

<span data-ttu-id="d5a45-237">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-237">Initializes a new instance of the Object class.</span></span>

    public void new()

### <a name="method-notify"></a><span data-ttu-id="d5a45-238">メソッド notify</span><span class="sxs-lookup"><span data-stu-id="d5a45-238">Method notify</span></span>

<span data-ttu-id="d5a45-239">このオブジェクトの待機メソッドを呼び出したオブジェクトのホールドを解放します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-239">Releases the hold on an object that has called the wait method on this object.</span></span>

    public void notify()

#### <a name="examples"></a><span data-ttu-id="d5a45-240">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-240">Examples</span></span>

<span data-ttu-id="d5a45-241">次の例では、オブジェクトをロックしてから解放します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-241">The following example locks an object, and then releases it.</span></span>

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

### <a name="method-notifyall"></a><span data-ttu-id="d5a45-242">メソッド notifyAll</span><span class="sxs-lookup"><span data-stu-id="d5a45-242">Method notifyAll</span></span>

<span data-ttu-id="d5a45-243">このオブジェクトの待機メソッドによって発行されたオブジェクトのロックを解放します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-243">Releases a lock on the object that was issued by the wait method on this object.</span></span>

    public void notifyAll()

#### <a name="remarks"></a><span data-ttu-id="d5a45-244">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-244">Remarks</span></span>

<span data-ttu-id="d5a45-245">このメソッドの現在の実装では、notify メソッドと notifyAll メソッドの呼び出しに違いはありません。</span><span class="sxs-lookup"><span data-stu-id="d5a45-245">In the current implementation of this method, there is no difference between calling the notify method and the notifyAll method.</span></span> <span data-ttu-id="d5a45-246">フォームは、ユーザーがフォームを閉じるまたは「適用」ボタンを押す際に、notifyAll メソッドを自動で呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-246">Forms will automatically call the notifyAll method when the user closes the form or presses the Apply button.</span></span>

#### <a name="examples"></a><span data-ttu-id="d5a45-247">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-247">Examples</span></span>

<span data-ttu-id="d5a45-248">次の例では、notifyAll メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d5a45-248">The following example demonstrates the usage of the notifyAll method.</span></span>

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

## <a name="class-objectident"></a><span data-ttu-id="d5a45-249">クラス ObjectIdent</span><span class="sxs-lookup"><span data-stu-id="d5a45-249">Class ObjectIdent</span></span>
    class ObjectIdent extends Object

### <a name="remarks"></a><span data-ttu-id="d5a45-250">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-250">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-251">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-251">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-252">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-252">Methods</span></span>

| <span data-ttu-id="d5a45-253">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-253">Method</span></span>                         | <span data-ttu-id="d5a45-254">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-254">Description</span></span>                                     |
|--------------------------------|-------------------------------------------------|
| <span data-ttu-id="d5a45-255">public Object object()</span><span class="sxs-lookup"><span data-stu-id="d5a45-255">public Object object()</span></span>         |                                                 |
| <span data-ttu-id="d5a45-256">public void new(Object object)</span><span class="sxs-lookup"><span data-stu-id="d5a45-256">public void new(Object object)</span></span> | <span data-ttu-id="d5a45-257">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-257">Initializes a new instance of the Object class.</span></span> |

### <a name="method-object"></a><span data-ttu-id="d5a45-258">メソッド object</span><span class="sxs-lookup"><span data-stu-id="d5a45-258">Method object</span></span>

    public Object object()

#### <a name="return-value"></a><span data-ttu-id="d5a45-259">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-259">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-260">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-260">Method new</span></span>

<span data-ttu-id="d5a45-261">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-261">Initializes a new instance of the Object class.</span></span>

    public void new(Object object)

#### <a name="parameters"></a><span data-ttu-id="d5a45-262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-262">Parameters</span></span>

<span data-ttu-id="d5a45-263">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d5a45-263">object</span></span>  

## <a name="class-objectrun"></a><span data-ttu-id="d5a45-264">クラス ObjectRun</span><span class="sxs-lookup"><span data-stu-id="d5a45-264">Class ObjectRun</span></span>
    class ObjectRun extends Object

<span data-ttu-id="d5a45-265">FormRun クラスおよび ReportRun クラスの基本クラスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-265">Used as the base class for the FormRun and ReportRun classes.</span></span>

### <a name="remarks"></a><span data-ttu-id="d5a45-266">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-266">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-267">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-267">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-268">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-268">Methods</span></span>

| <span data-ttu-id="d5a45-269">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-269">Method</span></span>                      | <span data-ttu-id="d5a45-270">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-270">Description</span></span>                                                                                                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a45-271">public xArgs args()</span><span class="sxs-lookup"><span data-stu-id="d5a45-271">public xArgs args()</span></span>         | <span data-ttu-id="d5a45-272">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-272">Returns the arguments that the object was constructed with.</span></span>                                                                                                             |
| <span data-ttu-id="d5a45-273">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="d5a45-273">public boolean isDetached()</span></span> | <span data-ttu-id="d5a45-274">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-274">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>                                                                                      |
| <span data-ttu-id="d5a45-275">public void attach()</span><span class="sxs-lookup"><span data-stu-id="d5a45-275">public void attach()</span></span>        | <span data-ttu-id="d5a45-276">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-276">Reverses a call to the method.</span></span> <span data-ttu-id="d5a45-277">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="d5a45-277">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="d5a45-278">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="d5a45-278">Reversing the call disallows any further switching of focus between windows.</span></span> |
| <span data-ttu-id="d5a45-279">public void detach()</span><span class="sxs-lookup"><span data-stu-id="d5a45-279">public void detach()</span></span>        | <span data-ttu-id="d5a45-280">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-280">Allows focus to be switched between windows.</span></span>                                                                                                                            |

### <a name="method-args"></a><span data-ttu-id="d5a45-281">メソッド args</span><span class="sxs-lookup"><span data-stu-id="d5a45-281">Method args</span></span>

<span data-ttu-id="d5a45-282">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-282">Returns the arguments that the object was constructed with.</span></span>

    public xArgs args()

#### <a name="return-value"></a><span data-ttu-id="d5a45-283">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-283">Return Value</span></span>

<span data-ttu-id="d5a45-284">オブジェクトの引数を含む Args クラス オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-284">An Args Class object that contains the arguments for the object.</span></span>

### <a name="method-isdetached"></a><span data-ttu-id="d5a45-285">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="d5a45-285">Method isDetached</span></span>

<span data-ttu-id="d5a45-286">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-286">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>

    public boolean isDetached()

#### <a name="return-value"></a><span data-ttu-id="d5a45-287">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-287">Return Value</span></span>

<span data-ttu-id="d5a45-288">デタッチが呼び出された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d5a45-288">true if detach has been called; otherwise, false.</span></span>

### <a name="method-attach"></a><span data-ttu-id="d5a45-289">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="d5a45-289">Method attach</span></span>

<span data-ttu-id="d5a45-290">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-290">Reverses a call to the method.</span></span> <span data-ttu-id="d5a45-291">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="d5a45-291">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="d5a45-292">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="d5a45-292">Reversing the call disallows any further switching of focus between windows.</span></span>

    public void attach()

### <a name="method-detach"></a><span data-ttu-id="d5a45-293">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="d5a45-293">Method detach</span></span>

<span data-ttu-id="d5a45-294">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-294">Allows focus to be switched between windows.</span></span>

    public void detach()

#### <a name="remarks"></a><span data-ttu-id="d5a45-295">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-295">Remarks</span></span>

<span data-ttu-id="d5a45-296">たとえば、新しいフォームの実行方法を呼び出すことにより、新しいフォームが既存のフォームから作成されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-296">For example, a new form is created from an existing form by calling the new form's run method.</span></span> <span data-ttu-id="d5a45-297">実行メソッドを呼び出すと、フォーカスが新しいフォームに変更されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-297">Calling a run method changes the focus to the new form.</span></span> <span data-ttu-id="d5a45-298">解除メソッドを呼び出すと、ユーザーは 2 番目のフォームを閉じることなく最初のフォームに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-298">Calling the detach method allows the user to return to the first form without closing the second form.</span></span> <span data-ttu-id="d5a45-299">ObjectRun.attach Method メソッドの呼び出しは、解除メソッドの影響を取り消します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-299">Calling the ObjectRun.attach Method method reverses the effects of the detach method.</span></span>

## <a name="class-ociconnection"></a><span data-ttu-id="d5a45-300">クラス OciConnection</span><span class="sxs-lookup"><span data-stu-id="d5a45-300">Class OciConnection</span></span>
    class OciConnection extends Connection

<span data-ttu-id="d5a45-301">OciConnection クラスは、Oci (Oracle 呼び出しインターフェイス) を使用するデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-301">The OciConnection class establishes a database connection that uses Oci (Oracle Call Interface).</span></span>

### <a name="remarks"></a><span data-ttu-id="d5a45-302">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-302">Remarks</span></span>

<span data-ttu-id="d5a45-303">OciConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-303">In the context of an OciConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="d5a45-304">LoginProperty インスタンスに対して指定されている情報を基に、接続を確立できない場合、例外および理由は、情報ログに転記されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-304">If the connection cannot be established based on the information that is specified for the LoginProperty instance, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="d5a45-305">このクラスは、Oracle クライアント ソフトウェアがインストールされている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-305">This class can be used only when Oracle client software is installed.</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-306">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-306">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-307">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-307">Methods</span></span>

| <span data-ttu-id="d5a45-308">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-308">Method</span></span>                               | <span data-ttu-id="d5a45-309">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-309">Description</span></span>                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a45-310">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="d5a45-310">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="d5a45-311">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-311">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-312">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-312">Method new</span></span>

<span data-ttu-id="d5a45-313">ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-313">Establishes a connection to an Oracle database, based on logon properties such as the user name and password.</span></span>

    public void new(LoginProperty Login)

#### <a name="parameters"></a><span data-ttu-id="d5a45-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-314">Parameters</span></span>

<span data-ttu-id="d5a45-315">ログイン</span><span class="sxs-lookup"><span data-stu-id="d5a45-315">Login</span></span>  
<span data-ttu-id="d5a45-316">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="d5a45-316">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

## <a name="class-odbcconnection"></a><span data-ttu-id="d5a45-317">クラス OdbcConnection</span><span class="sxs-lookup"><span data-stu-id="d5a45-317">Class OdbcConnection</span></span>
    class OdbcConnection extends Connection

<span data-ttu-id="d5a45-318">OdbcConnection クラスは、ODBC (Open Database Connectivity) を使用してデータベース接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-318">The OdbcConnection class establishes a database connection by using ODBC (Open Database Connectivity).</span></span>

### <a name="remarks"></a><span data-ttu-id="d5a45-319">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-319">Remarks</span></span>

<span data-ttu-id="d5a45-320">OdbcConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-320">In the context of an OdbcConnection instance, SQL statements are run, and results are returned.</span></span> <span data-ttu-id="d5a45-321">ODBC データ ソースへの接続を確立できない場合、例外がスローされ、その原因が Infolog に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-321">If a connection to the ODBC data source cannot be established, an exception is thrown, and the reason is posted in the Infolog.</span></span> <span data-ttu-id="d5a45-322">このクラスは、正しい ODBC ドライバーがインストールされ、コントロール パネルの ODBC マネージャーで構成されている場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-322">This class works only if the correct ODBC drivers have been installed and configured in ODBC Manager in Control Panel.</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-323">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-323">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-324">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-324">Methods</span></span>

| <span data-ttu-id="d5a45-325">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-325">Method</span></span>                               | <span data-ttu-id="d5a45-326">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-326">Description</span></span>                                                                                              |
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a45-327">public void new(LoginProperty Login)</span><span class="sxs-lookup"><span data-stu-id="d5a45-327">public void new(LoginProperty Login)</span></span> | <span data-ttu-id="d5a45-328">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-328">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-329">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-329">Method new</span></span>

<span data-ttu-id="d5a45-330">ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-330">Establishes a connection to a data source, based on logon properties such as the user name and password.</span></span>

    public void new(LoginProperty Login)

#### <a name="parameters"></a><span data-ttu-id="d5a45-331">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-331">Parameters</span></span>

<span data-ttu-id="d5a45-332">ログイン</span><span class="sxs-lookup"><span data-stu-id="d5a45-332">Login</span></span>  
<span data-ttu-id="d5a45-333">ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="d5a45-333">A LoginProperty class instance that contains the user name, password, data source name, database, and so on.</span></span>

## <a name="class-olecommand"></a><span data-ttu-id="d5a45-334">クラス OleCommand</span><span class="sxs-lookup"><span data-stu-id="d5a45-334">Class OleCommand</span></span>
    class OleCommand extends Object

### <a name="remarks"></a><span data-ttu-id="d5a45-335">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-335">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-336">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-336">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-337">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-337">Methods</span></span>

| <span data-ttu-id="d5a45-338">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-338">Method</span></span>                                                                              | <span data-ttu-id="d5a45-339">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-339">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d5a45-340">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span><span class="sxs-lookup"><span data-stu-id="d5a45-340">public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)</span></span> |                                                 |
| <span data-ttu-id="d5a45-341">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d5a45-341">public void finalize()</span></span>                                                              |                                                 |
| <span data-ttu-id="d5a45-342">public void new(ComInterface comObject)</span><span class="sxs-lookup"><span data-stu-id="d5a45-342">public void new(ComInterface comObject)</span></span>                                             | <span data-ttu-id="d5a45-343">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-343">Initializes a new instance of the Object class.</span></span> |

### <a name="method-exec"></a><span data-ttu-id="d5a45-344">メソッド exec</span><span class="sxs-lookup"><span data-stu-id="d5a45-344">Method exec</span></span>

    public COMVariant exec(str cmdGroup, int cmdId, int cmdExecOption, COMVariant parm)

#### <a name="parameters"></a><span data-ttu-id="d5a45-345">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-345">Parameters</span></span>

<span data-ttu-id="d5a45-346">cmdGroup</span><span class="sxs-lookup"><span data-stu-id="d5a45-346">cmdGroup</span></span>  

<!-- -->

<span data-ttu-id="d5a45-347">cmdId</span><span class="sxs-lookup"><span data-stu-id="d5a45-347">cmdId</span></span>  

<!-- -->

<span data-ttu-id="d5a45-348">cmdExecOption</span><span class="sxs-lookup"><span data-stu-id="d5a45-348">cmdExecOption</span></span>  

<!-- -->

<span data-ttu-id="d5a45-349">parm</span><span class="sxs-lookup"><span data-stu-id="d5a45-349">parm</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d5a45-350">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-350">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="d5a45-351">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d5a45-351">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="d5a45-352">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-352">Method new</span></span>

<span data-ttu-id="d5a45-353">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-353">Initializes a new instance of the Object class.</span></span>

    public void new(ComInterface comObject)

#### <a name="parameters"></a><span data-ttu-id="d5a45-354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-354">Parameters</span></span>

<span data-ttu-id="d5a45-355">comObject</span><span class="sxs-lookup"><span data-stu-id="d5a45-355">comObject</span></span>  

## <a name="class-ouputsection"></a><span data-ttu-id="d5a45-356">クラス OuputSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-356">Class OuputSection</span></span>
    class OuputSection extends Object

### <a name="remarks"></a><span data-ttu-id="d5a45-357">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-357">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-358">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-358">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-359">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-359">Methods</span></span>

| <span data-ttu-id="d5a45-360">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-360">Method</span></span>                                           | <span data-ttu-id="d5a45-361">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-361">Description</span></span>                                           |
|--------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="d5a45-362">public int arrangeMethod()</span><span class="sxs-lookup"><span data-stu-id="d5a45-362">public int arrangeMethod()</span></span>                       |                                                       |
| <span data-ttu-id="d5a45-363">public int backgroundColor()</span><span class="sxs-lookup"><span data-stu-id="d5a45-363">public int backgroundColor()</span></span>                     |                                                       |
| <span data-ttu-id="d5a45-364">public LineThickness borderWidth()</span><span class="sxs-lookup"><span data-stu-id="d5a45-364">public LineThickness borderWidth()</span></span>               |                                                       |
| <span data-ttu-id="d5a45-365">public int bottomMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-365">public int bottomMargin()</span></span>                        |                                                       |
| <span data-ttu-id="d5a45-366">public HeadingsStrategy columnHeadingsStrategy()</span><span class="sxs-lookup"><span data-stu-id="d5a45-366">public HeadingsStrategy columnHeadingsStrategy()</span></span> |                                                       |
| <span data-ttu-id="d5a45-367">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-367">public str fontName()</span></span>                            |                                                       |
| <span data-ttu-id="d5a45-368">public int leftMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-368">public int leftMargin()</span></span>                          |                                                       |
| <span data-ttu-id="d5a45-369">public LineType lineBottom()</span><span class="sxs-lookup"><span data-stu-id="d5a45-369">public LineType lineBottom()</span></span>                     |                                                       |
| <span data-ttu-id="d5a45-370">public LineType lineLeft()</span><span class="sxs-lookup"><span data-stu-id="d5a45-370">public LineType lineLeft()</span></span>                       |                                                       |
| <span data-ttu-id="d5a45-371">public LineType lineRight()</span><span class="sxs-lookup"><span data-stu-id="d5a45-371">public LineType lineRight()</span></span>                      |                                                       |
| <span data-ttu-id="d5a45-372">public LineType lineTop()</span><span class="sxs-lookup"><span data-stu-id="d5a45-372">public LineType lineTop()</span></span>                        |                                                       |
| <span data-ttu-id="d5a45-373">public int nextVerticalPos()</span><span class="sxs-lookup"><span data-stu-id="d5a45-373">public int nextVerticalPos()</span></span>                     |                                                       |
| <span data-ttu-id="d5a45-374">public int rightMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-374">public int rightMargin()</span></span>                         |                                                       |
| <span data-ttu-id="d5a45-375">public ReportBlockType sectionType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-375">public ReportBlockType sectionType()</span></span>             |                                                       |
| <span data-ttu-id="d5a45-376">public int topMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-376">public int topMargin()</span></span>                           |                                                       |
| <span data-ttu-id="d5a45-377">public int type()</span><span class="sxs-lookup"><span data-stu-id="d5a45-377">public int type()</span></span>                                |                                                       |
| <span data-ttu-id="d5a45-378">public int verticalPos()</span><span class="sxs-lookup"><span data-stu-id="d5a45-378">public int verticalPos()</span></span>                         |                                                       |
| <span data-ttu-id="d5a45-379">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-379">public void new()</span></span>                                | <span data-ttu-id="d5a45-380">OuputSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-380">Initializes a new instance of the OuputSection class.</span></span> |

### <a name="method-arrangemethod"></a><span data-ttu-id="d5a45-381">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="d5a45-381">Method arrangeMethod</span></span>

    public int arrangeMethod()

#### <a name="return-value"></a><span data-ttu-id="d5a45-382">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-382">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="d5a45-383">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d5a45-383">Method backgroundColor</span></span>

    public int backgroundColor()

#### <a name="return-value"></a><span data-ttu-id="d5a45-384">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-384">Return Value</span></span>

### <a name="method-borderwidth"></a><span data-ttu-id="d5a45-385">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="d5a45-385">Method borderWidth</span></span>

    public LineThickness borderWidth()

#### <a name="return-value"></a><span data-ttu-id="d5a45-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-386">Return Value</span></span>

### <a name="method-bottommargin"></a><span data-ttu-id="d5a45-387">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-387">Method bottomMargin</span></span>

    public int bottomMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-388">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-388">Return Value</span></span>

### <a name="method-columnheadingsstrategy"></a><span data-ttu-id="d5a45-389">メソッド columnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="d5a45-389">Method columnHeadingsStrategy</span></span>

    public HeadingsStrategy columnHeadingsStrategy()

#### <a name="return-value"></a><span data-ttu-id="d5a45-390">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-390">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="d5a45-391">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="d5a45-391">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-392">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-392">Return Value</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="d5a45-393">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-393">Method leftMargin</span></span>

    public int leftMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-394">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-394">Return Value</span></span>

### <a name="method-linebottom"></a><span data-ttu-id="d5a45-395">メソッド lineBottom</span><span class="sxs-lookup"><span data-stu-id="d5a45-395">Method lineBottom</span></span>

    public LineType lineBottom()

#### <a name="return-value"></a><span data-ttu-id="d5a45-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-396">Return Value</span></span>

### <a name="method-lineleft"></a><span data-ttu-id="d5a45-397">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="d5a45-397">Method lineLeft</span></span>

    public LineType lineLeft()

#### <a name="return-value"></a><span data-ttu-id="d5a45-398">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-398">Return Value</span></span>

### <a name="method-lineright"></a><span data-ttu-id="d5a45-399">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="d5a45-399">Method lineRight</span></span>

    public LineType lineRight()

#### <a name="return-value"></a><span data-ttu-id="d5a45-400">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-400">Return Value</span></span>

### <a name="method-linetop"></a><span data-ttu-id="d5a45-401">メソッド lineTop</span><span class="sxs-lookup"><span data-stu-id="d5a45-401">Method lineTop</span></span>

    public LineType lineTop()

#### <a name="return-value"></a><span data-ttu-id="d5a45-402">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-402">Return Value</span></span>

### <a name="method-nextverticalpos"></a><span data-ttu-id="d5a45-403">メソッド nextVerticalPos</span><span class="sxs-lookup"><span data-stu-id="d5a45-403">Method nextVerticalPos</span></span>

    public int nextVerticalPos()

#### <a name="return-value"></a><span data-ttu-id="d5a45-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-404">Return Value</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="d5a45-405">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-405">Method rightMargin</span></span>

    public int rightMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-406">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-406">Return Value</span></span>

### <a name="method-sectiontype"></a><span data-ttu-id="d5a45-407">メソッド sectionType</span><span class="sxs-lookup"><span data-stu-id="d5a45-407">Method sectionType</span></span>

    public ReportBlockType sectionType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-408">Return Value</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="d5a45-409">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-409">Method topMargin</span></span>

    public int topMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-410">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-410">Return Value</span></span>

### <a name="method-type"></a><span data-ttu-id="d5a45-411">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d5a45-411">Method type</span></span>

    public int type()

#### <a name="return-value"></a><span data-ttu-id="d5a45-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-412">Return Value</span></span>

### <a name="method-verticalpos"></a><span data-ttu-id="d5a45-413">メソッド verticalPos</span><span class="sxs-lookup"><span data-stu-id="d5a45-413">Method verticalPos</span></span>

    public int verticalPos()

#### <a name="return-value"></a><span data-ttu-id="d5a45-414">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-414">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-415">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-415">Method new</span></span>

<span data-ttu-id="d5a45-416">OuputSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-416">Initializes a new instance of the OuputSection class.</span></span>

    public void new()

## <a name="class-outputautolabelfield"></a><span data-ttu-id="d5a45-417">クラス OutputAutoLabelField</span><span class="sxs-lookup"><span data-stu-id="d5a45-417">Class OutputAutoLabelField</span></span>
    class OutputAutoLabelField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-418">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-418">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-419">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-419">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-420">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-420">Methods</span></span>

| <span data-ttu-id="d5a45-421">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-421">Method</span></span>                  | <span data-ttu-id="d5a45-422">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-422">Description</span></span>                                                   |
|-------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d5a45-423">public boolean leadIn()</span><span class="sxs-lookup"><span data-stu-id="d5a45-423">public boolean leadIn()</span></span> |                                                               |
| <span data-ttu-id="d5a45-424">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-424">public str toString()</span></span>   | <span data-ttu-id="d5a45-425">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-425">Returns a string that represents the current object.</span></span>          |
| <span data-ttu-id="d5a45-426">public str value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-426">public str value()</span></span>      |                                                               |
| <span data-ttu-id="d5a45-427">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-427">public void new()</span></span>       | <span data-ttu-id="d5a45-428">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-428">Initializes a new instance of the OutputAutoLabelField class.</span></span> |

### <a name="method-leadin"></a><span data-ttu-id="d5a45-429">メソッド leadIn</span><span class="sxs-lookup"><span data-stu-id="d5a45-429">Method leadIn</span></span>

    public boolean leadIn()

#### <a name="return-value"></a><span data-ttu-id="d5a45-430">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-430">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-431">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-431">Method toString</span></span>

<span data-ttu-id="d5a45-432">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-432">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-433">Return Value</span></span>

<span data-ttu-id="d5a45-434">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-434">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-435">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-435">Remarks</span></span>

<span data-ttu-id="d5a45-436">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-436">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-437">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-437">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-438">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-438">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-439">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-439">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-440">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-440">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-441">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-441">Method new</span></span>

<span data-ttu-id="d5a45-442">OutputAutoLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-442">Initializes a new instance of the OutputAutoLabelField class.</span></span>

    public void new()

## <a name="class-outputbitmapfield"></a><span data-ttu-id="d5a45-443">クラス OutputBitmapField</span><span class="sxs-lookup"><span data-stu-id="d5a45-443">Class OutputBitmapField</span></span>
    class OutputBitmapField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-444">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-444">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-445">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-445">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-446">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-446">Methods</span></span>

| <span data-ttu-id="d5a45-447">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-447">Method</span></span>                     | <span data-ttu-id="d5a45-448">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-448">Description</span></span>                                                |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d5a45-449">public str imageFileName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-449">public str imageFileName()</span></span> |                                                            |
| <span data-ttu-id="d5a45-450">public boolean resize()</span><span class="sxs-lookup"><span data-stu-id="d5a45-450">public boolean resize()</span></span>    |                                                            |
| <span data-ttu-id="d5a45-451">public int resourceId()</span><span class="sxs-lookup"><span data-stu-id="d5a45-451">public int resourceId()</span></span>    |                                                            |
| <span data-ttu-id="d5a45-452">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-452">public str toString()</span></span>      | <span data-ttu-id="d5a45-453">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-453">Returns a string that represents the current object.</span></span>       |
| <span data-ttu-id="d5a45-454">public container value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-454">public container value()</span></span>   |                                                            |
| <span data-ttu-id="d5a45-455">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-455">public void new()</span></span>          | <span data-ttu-id="d5a45-456">OutputBitmapField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-456">Initializes a new instance of the OutputBitmapField class.</span></span> |

### <a name="method-imagefilename"></a><span data-ttu-id="d5a45-457">メソッド imageFileName</span><span class="sxs-lookup"><span data-stu-id="d5a45-457">Method imageFileName</span></span>

    public str imageFileName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-458">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-458">Return Value</span></span>

### <a name="method-resize"></a><span data-ttu-id="d5a45-459">メソッド resize</span><span class="sxs-lookup"><span data-stu-id="d5a45-459">Method resize</span></span>

    public boolean resize()

#### <a name="return-value"></a><span data-ttu-id="d5a45-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-460">Return Value</span></span>

### <a name="method-resourceid"></a><span data-ttu-id="d5a45-461">メソッド resourceId</span><span class="sxs-lookup"><span data-stu-id="d5a45-461">Method resourceId</span></span>

    public int resourceId()

#### <a name="return-value"></a><span data-ttu-id="d5a45-462">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-462">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-463">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-463">Method toString</span></span>

<span data-ttu-id="d5a45-464">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-464">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-465">Return Value</span></span>

<span data-ttu-id="d5a45-466">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-466">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-467">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-467">Remarks</span></span>

<span data-ttu-id="d5a45-468">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-468">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-469">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-469">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-470">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-470">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-471">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-471">Method value</span></span>

    public container value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-472">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-472">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-473">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-473">Method new</span></span>

<span data-ttu-id="d5a45-474">OutputBitmapField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-474">Initializes a new instance of the OutputBitmapField class.</span></span>

    public void new()

## <a name="class-outputbodysection"></a><span data-ttu-id="d5a45-475">クラス OutputBodySection</span><span class="sxs-lookup"><span data-stu-id="d5a45-475">Class OutputBodySection</span></span>
    class OutputBodySection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-476">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-476">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-477">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-477">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-478">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-478">Methods</span></span>

| <span data-ttu-id="d5a45-479">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-479">Method</span></span>             | <span data-ttu-id="d5a45-480">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-480">Description</span></span>                                                |
|--------------------|------------------------------------------------------------|
| <span data-ttu-id="d5a45-481">public int recId()</span><span class="sxs-lookup"><span data-stu-id="d5a45-481">public int recId()</span></span> |                                                            |
| <span data-ttu-id="d5a45-482">public int table()</span><span class="sxs-lookup"><span data-stu-id="d5a45-482">public int table()</span></span> |                                                            |
| <span data-ttu-id="d5a45-483">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-483">public void new()</span></span>  | <span data-ttu-id="d5a45-484">OutputBodySection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-484">Initializes a new instance of the OutputBodySection class.</span></span> |

### <a name="method-recid"></a><span data-ttu-id="d5a45-485">メソッド recId</span><span class="sxs-lookup"><span data-stu-id="d5a45-485">Method recId</span></span>

    public int recId()

#### <a name="return-value"></a><span data-ttu-id="d5a45-486">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-486">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="d5a45-487">メソッド table</span><span class="sxs-lookup"><span data-stu-id="d5a45-487">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="d5a45-488">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-488">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-489">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-489">Method new</span></span>

<span data-ttu-id="d5a45-490">OutputBodySection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-490">Initializes a new instance of the OutputBodySection class.</span></span>

    public void new()

## <a name="class-outputcolumnheadingssection"></a><span data-ttu-id="d5a45-491">クラス OutputColumnHeadingsSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-491">Class OutputColumnHeadingsSection</span></span>
    class OutputColumnHeadingsSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-492">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-492">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-493">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-493">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-494">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-494">Methods</span></span>

| <span data-ttu-id="d5a45-495">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-495">Method</span></span>             | <span data-ttu-id="d5a45-496">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-496">Description</span></span>                                                          |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d5a45-497">public str table()</span><span class="sxs-lookup"><span data-stu-id="d5a45-497">public str table()</span></span> |                                                                      |
| <span data-ttu-id="d5a45-498">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-498">public void new()</span></span>  | <span data-ttu-id="d5a45-499">OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-499">Initializes a new instance of the OutputColumnHeadingsSection class.</span></span> |

### <a name="method-table"></a><span data-ttu-id="d5a45-500">メソッド table</span><span class="sxs-lookup"><span data-stu-id="d5a45-500">Method table</span></span>

    public str table()

#### <a name="return-value"></a><span data-ttu-id="d5a45-501">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-501">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-502">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-502">Method new</span></span>

<span data-ttu-id="d5a45-503">OutputColumnHeadingsSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-503">Initializes a new instance of the OutputColumnHeadingsSection class.</span></span>

    public void new()

## <a name="class-outputdatefield"></a><span data-ttu-id="d5a45-504">クラス OutputDateField</span><span class="sxs-lookup"><span data-stu-id="d5a45-504">Class OutputDateField</span></span>
    class OutputDateField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-505">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-505">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-506">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-506">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-507">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-507">Methods</span></span>

| <span data-ttu-id="d5a45-508">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-508">Method</span></span>                | <span data-ttu-id="d5a45-509">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-509">Description</span></span>                                              |
|-----------------------|----------------------------------------------------------|
| <span data-ttu-id="d5a45-510">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-510">public str toString()</span></span> | <span data-ttu-id="d5a45-511">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-511">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="d5a45-512">public Date value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-512">public Date value()</span></span>   |                                                          |
| <span data-ttu-id="d5a45-513">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-513">public void new()</span></span>     | <span data-ttu-id="d5a45-514">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-514">Initializes a new instance of the OutputDateField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-515">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-515">Method toString</span></span>

<span data-ttu-id="d5a45-516">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-516">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-517">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-517">Return Value</span></span>

<span data-ttu-id="d5a45-518">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-518">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-519">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-519">Remarks</span></span>

<span data-ttu-id="d5a45-520">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-520">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-521">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-521">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-522">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-522">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-523">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-523">Method value</span></span>

    public Date value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-524">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-524">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-525">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-525">Method new</span></span>

<span data-ttu-id="d5a45-526">OutputDateField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-526">Initializes a new instance of the OutputDateField class.</span></span>

    public void new()

## <a name="class-outputdatetimefield"></a><span data-ttu-id="d5a45-527">クラス OutputDateTimeField</span><span class="sxs-lookup"><span data-stu-id="d5a45-527">Class OutputDateTimeField</span></span>
    class OutputDateTimeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-528">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-528">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-529">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-529">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-530">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-530">Methods</span></span>

| <span data-ttu-id="d5a45-531">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-531">Method</span></span>                  | <span data-ttu-id="d5a45-532">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-532">Description</span></span>                                                  |
|-------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a45-533">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-533">public str toString()</span></span>   | <span data-ttu-id="d5a45-534">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-534">Returns a string that represents the current object.</span></span>         |
| <span data-ttu-id="d5a45-535">public DateTime value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-535">public DateTime value()</span></span> |                                                              |
| <span data-ttu-id="d5a45-536">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-536">public void new()</span></span>       | <span data-ttu-id="d5a45-537">OutputDateTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-537">Initializes a new instance of the OutputDateTimeField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-538">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-538">Method toString</span></span>

<span data-ttu-id="d5a45-539">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-539">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-540">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-540">Return Value</span></span>

<span data-ttu-id="d5a45-541">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-541">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-542">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-542">Remarks</span></span>

<span data-ttu-id="d5a45-543">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-543">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-544">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-544">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-545">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-545">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-546">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-546">Method value</span></span>

    public DateTime value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-547">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-547">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-548">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-548">Method new</span></span>

<span data-ttu-id="d5a45-549">OutputDateTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-549">Initializes a new instance of the OutputDateTimeField class.</span></span>

    public void new()

## <a name="class-outputenumfield"></a><span data-ttu-id="d5a45-550">クラス OutputEnumField</span><span class="sxs-lookup"><span data-stu-id="d5a45-550">Class OutputEnumField</span></span>
    class OutputEnumField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-551">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-551">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-552">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-552">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-553">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-553">Methods</span></span>

| <span data-ttu-id="d5a45-554">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-554">Method</span></span>                 | <span data-ttu-id="d5a45-555">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-555">Description</span></span>                                              |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d5a45-556">public str getString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-556">public str getString()</span></span> |                                                          |
| <span data-ttu-id="d5a45-557">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-557">public void new()</span></span>      | <span data-ttu-id="d5a45-558">OutputEnumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-558">Initializes a new instance of the OutputEnumField class.</span></span> |

### <a name="method-getstring"></a><span data-ttu-id="d5a45-559">メソッド getString</span><span class="sxs-lookup"><span data-stu-id="d5a45-559">Method getString</span></span>

    public str getString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-560">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-560">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-561">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-561">Method new</span></span>

<span data-ttu-id="d5a45-562">OutputEnumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-562">Initializes a new instance of the OutputEnumField class.</span></span>

    public void new()

## <a name="class-outputepilogsection"></a><span data-ttu-id="d5a45-563">クラス OutputEpilogSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-563">Class OutputEpilogSection</span></span>
    class OutputEpilogSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-564">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-564">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-565">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-565">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-566">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-566">Methods</span></span>

| <span data-ttu-id="d5a45-567">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-567">Method</span></span>            | <span data-ttu-id="d5a45-568">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-568">Description</span></span>                                                  |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a45-569">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-569">public void new()</span></span> | <span data-ttu-id="d5a45-570">OutputEpilogSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-570">Initializes a new instance of the OutputEpilogSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-571">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-571">Method new</span></span>

<span data-ttu-id="d5a45-572">OutputEpilogSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-572">Initializes a new instance of the OutputEpilogSection class.</span></span>

    public void new()

## <a name="class-outputfield"></a><span data-ttu-id="d5a45-573">クラス OutputField</span><span class="sxs-lookup"><span data-stu-id="d5a45-573">Class OutputField</span></span>
    class OutputField extends Object

### <a name="remarks"></a><span data-ttu-id="d5a45-574">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-574">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-575">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-575">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-576">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-576">Methods</span></span>

| <span data-ttu-id="d5a45-577">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-577">Method</span></span>                         | <span data-ttu-id="d5a45-578">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-578">Description</span></span>                                          |
|--------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5a45-579">public Alignment alignment()</span><span class="sxs-lookup"><span data-stu-id="d5a45-579">public Alignment alignment()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-580">public int backgroundColor()</span><span class="sxs-lookup"><span data-stu-id="d5a45-580">public int backgroundColor()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-581">public int borderWidth()</span><span class="sxs-lookup"><span data-stu-id="d5a45-581">public int borderWidth()</span></span>       |                                                      |
| <span data-ttu-id="d5a45-582">public str CSSClass()</span><span class="sxs-lookup"><span data-stu-id="d5a45-582">public str CSSClass()</span></span>          |                                                      |
| <span data-ttu-id="d5a45-583">public int dateFormat()</span><span class="sxs-lookup"><span data-stu-id="d5a45-583">public int dateFormat()</span></span>        |                                                      |
| <span data-ttu-id="d5a45-584">public int decimals()</span><span class="sxs-lookup"><span data-stu-id="d5a45-584">public int decimals()</span></span>          |                                                      |
| <span data-ttu-id="d5a45-585">public int extendedDataType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-585">public int extendedDataType()</span></span>  |                                                      |
| <span data-ttu-id="d5a45-586">public FieldId fieldHandle()</span><span class="sxs-lookup"><span data-stu-id="d5a45-586">public FieldId fieldHandle()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-587">public str fieldName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-587">public str fieldName()</span></span>         |                                                      |
| <span data-ttu-id="d5a45-588">public int fontHeight()</span><span class="sxs-lookup"><span data-stu-id="d5a45-588">public int fontHeight()</span></span>        |                                                      |
| <span data-ttu-id="d5a45-589">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-589">public str fontName()</span></span>          |                                                      |
| <span data-ttu-id="d5a45-590">public int foregroundColor()</span><span class="sxs-lookup"><span data-stu-id="d5a45-590">public int foregroundColor()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-591">public str formatValue()</span><span class="sxs-lookup"><span data-stu-id="d5a45-591">public str formatValue()</span></span>       |                                                      |
| <span data-ttu-id="d5a45-592">public int height()</span><span class="sxs-lookup"><span data-stu-id="d5a45-592">public int height()</span></span>            |                                                      |
| <span data-ttu-id="d5a45-593">public int heightMode()</span><span class="sxs-lookup"><span data-stu-id="d5a45-593">public int heightMode()</span></span>        |                                                      |
| <span data-ttu-id="d5a45-594">public boolean hideZeros()</span><span class="sxs-lookup"><span data-stu-id="d5a45-594">public boolean hideZeros()</span></span>     |                                                      |
| <span data-ttu-id="d5a45-595">public boolean isOneline()</span><span class="sxs-lookup"><span data-stu-id="d5a45-595">public boolean isOneline()</span></span>     |                                                      |
| <span data-ttu-id="d5a45-596">public boolean isOverlapping()</span><span class="sxs-lookup"><span data-stu-id="d5a45-596">public boolean isOverlapping()</span></span> |                                                      |
| <span data-ttu-id="d5a45-597">public boolean italic()</span><span class="sxs-lookup"><span data-stu-id="d5a45-597">public boolean italic()</span></span>        |                                                      |
| <span data-ttu-id="d5a45-598">public LateEvalMode lateEval()</span><span class="sxs-lookup"><span data-stu-id="d5a45-598">public LateEvalMode lateEval()</span></span> |                                                      |
| <span data-ttu-id="d5a45-599">public LineType lineBottom()</span><span class="sxs-lookup"><span data-stu-id="d5a45-599">public LineType lineBottom()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-600">public LineType lineLeft()</span><span class="sxs-lookup"><span data-stu-id="d5a45-600">public LineType lineLeft()</span></span>     |                                                      |
| <span data-ttu-id="d5a45-601">public LineType lineRight()</span><span class="sxs-lookup"><span data-stu-id="d5a45-601">public LineType lineRight()</span></span>    |                                                      |
| <span data-ttu-id="d5a45-602">public LineType lineTop()</span><span class="sxs-lookup"><span data-stu-id="d5a45-602">public LineType lineTop()</span></span>      |                                                      |
| <span data-ttu-id="d5a45-603">public str menuFunctionHelp()</span><span class="sxs-lookup"><span data-stu-id="d5a45-603">public str menuFunctionHelp()</span></span>  |                                                      |
| <span data-ttu-id="d5a45-604">public str menuFunctionName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-604">public str menuFunctionName()</span></span>  |                                                      |
| <span data-ttu-id="d5a45-605">public int menuFunctionType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-605">public int menuFunctionType()</span></span>  |                                                      |
| <span data-ttu-id="d5a45-606">public str menuFunctionWeb()</span><span class="sxs-lookup"><span data-stu-id="d5a45-606">public str menuFunctionWeb()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-607">public str name()</span><span class="sxs-lookup"><span data-stu-id="d5a45-607">public str name()</span></span>              |                                                      |
| <span data-ttu-id="d5a45-608">public int recId()</span><span class="sxs-lookup"><span data-stu-id="d5a45-608">public int recId()</span></span>             |                                                      |
| <span data-ttu-id="d5a45-609">public boolean showPrompt()</span><span class="sxs-lookup"><span data-stu-id="d5a45-609">public boolean showPrompt()</span></span>    |                                                      |
| <span data-ttu-id="d5a45-610">public boolean strikeThrough()</span><span class="sxs-lookup"><span data-stu-id="d5a45-610">public boolean strikeThrough()</span></span> |                                                      |
| <span data-ttu-id="d5a45-611">public TableId tableHandle()</span><span class="sxs-lookup"><span data-stu-id="d5a45-611">public TableId tableHandle()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-612">public str tableName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-612">public str tableName()</span></span>         |                                                      |
| <span data-ttu-id="d5a45-613">public boolean turnSign()</span><span class="sxs-lookup"><span data-stu-id="d5a45-613">public boolean turnSign()</span></span>      |                                                      |
| <span data-ttu-id="d5a45-614">public int type()</span><span class="sxs-lookup"><span data-stu-id="d5a45-614">public int type()</span></span>              |                                                      |
| <span data-ttu-id="d5a45-615">public boolean underline()</span><span class="sxs-lookup"><span data-stu-id="d5a45-615">public boolean underline()</span></span>     |                                                      |
| <span data-ttu-id="d5a45-616">public str webMenuItemName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-616">public str webMenuItemName()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-617">public int webMenuItemType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-617">public int webMenuItemType()</span></span>   |                                                      |
| <span data-ttu-id="d5a45-618">public str webTarget()</span><span class="sxs-lookup"><span data-stu-id="d5a45-618">public str webTarget()</span></span>         |                                                      |
| <span data-ttu-id="d5a45-619">public int weight()</span><span class="sxs-lookup"><span data-stu-id="d5a45-619">public int weight()</span></span>            |                                                      |
| <span data-ttu-id="d5a45-620">public int width()</span><span class="sxs-lookup"><span data-stu-id="d5a45-620">public int width()</span></span>             |                                                      |
| <span data-ttu-id="d5a45-621">public int widthMode()</span><span class="sxs-lookup"><span data-stu-id="d5a45-621">public int widthMode()</span></span>         |                                                      |
| <span data-ttu-id="d5a45-622">public int xPos()</span><span class="sxs-lookup"><span data-stu-id="d5a45-622">public int xPos()</span></span>              |                                                      |
| <span data-ttu-id="d5a45-623">public int yPos()</span><span class="sxs-lookup"><span data-stu-id="d5a45-623">public int yPos()</span></span>              |                                                      |
| <span data-ttu-id="d5a45-624">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-624">public void new()</span></span>              | <span data-ttu-id="d5a45-625">OutputField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-625">Initializes a new instance of the OutputField class.</span></span> |

### <a name="method-alignment"></a><span data-ttu-id="d5a45-626">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="d5a45-626">Method alignment</span></span>

    public Alignment alignment()

#### <a name="return-value"></a><span data-ttu-id="d5a45-627">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-627">Return Value</span></span>

### <a name="method-backgroundcolor"></a><span data-ttu-id="d5a45-628">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="d5a45-628">Method backgroundColor</span></span>

    public int backgroundColor()

#### <a name="return-value"></a><span data-ttu-id="d5a45-629">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-629">Return Value</span></span>

### <a name="method-borderwidth"></a><span data-ttu-id="d5a45-630">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="d5a45-630">Method borderWidth</span></span>

    public int borderWidth()

#### <a name="return-value"></a><span data-ttu-id="d5a45-631">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-631">Return Value</span></span>

### <a name="method-cssclass"></a><span data-ttu-id="d5a45-632">メソッド CSSClass</span><span class="sxs-lookup"><span data-stu-id="d5a45-632">Method CSSClass</span></span>

    public str CSSClass()

#### <a name="return-value"></a><span data-ttu-id="d5a45-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-633">Return Value</span></span>

### <a name="method-dateformat"></a><span data-ttu-id="d5a45-634">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="d5a45-634">Method dateFormat</span></span>

    public int dateFormat()

#### <a name="return-value"></a><span data-ttu-id="d5a45-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-635">Return Value</span></span>

### <a name="method-decimals"></a><span data-ttu-id="d5a45-636">メソッド decimals</span><span class="sxs-lookup"><span data-stu-id="d5a45-636">Method decimals</span></span>

    public int decimals()

#### <a name="return-value"></a><span data-ttu-id="d5a45-637">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-637">Return Value</span></span>

### <a name="method-extendeddatatype"></a><span data-ttu-id="d5a45-638">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="d5a45-638">Method extendedDataType</span></span>

    public int extendedDataType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-639">Return Value</span></span>

### <a name="method-fieldhandle"></a><span data-ttu-id="d5a45-640">メソッド fieldHandle</span><span class="sxs-lookup"><span data-stu-id="d5a45-640">Method fieldHandle</span></span>

    public FieldId fieldHandle()

#### <a name="return-value"></a><span data-ttu-id="d5a45-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-641">Return Value</span></span>

### <a name="method-fieldname"></a><span data-ttu-id="d5a45-642">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="d5a45-642">Method fieldName</span></span>

    public str fieldName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-643">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-643">Return Value</span></span>

### <a name="method-fontheight"></a><span data-ttu-id="d5a45-644">メソッド fontHeight</span><span class="sxs-lookup"><span data-stu-id="d5a45-644">Method fontHeight</span></span>

    public int fontHeight()

#### <a name="return-value"></a><span data-ttu-id="d5a45-645">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-645">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="d5a45-646">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="d5a45-646">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-647">Return Value</span></span>

### <a name="method-foregroundcolor"></a><span data-ttu-id="d5a45-648">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="d5a45-648">Method foregroundColor</span></span>

    public int foregroundColor()

#### <a name="return-value"></a><span data-ttu-id="d5a45-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-649">Return Value</span></span>

### <a name="method-formatvalue"></a><span data-ttu-id="d5a45-650">メソッド formatValue</span><span class="sxs-lookup"><span data-stu-id="d5a45-650">Method formatValue</span></span>

    public str formatValue()

#### <a name="return-value"></a><span data-ttu-id="d5a45-651">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-651">Return Value</span></span>

### <a name="method-height"></a><span data-ttu-id="d5a45-652">メソッド height</span><span class="sxs-lookup"><span data-stu-id="d5a45-652">Method height</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="d5a45-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-653">Return Value</span></span>

### <a name="method-heightmode"></a><span data-ttu-id="d5a45-654">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="d5a45-654">Method heightMode</span></span>

    public int heightMode()

#### <a name="return-value"></a><span data-ttu-id="d5a45-655">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-655">Return Value</span></span>

### <a name="method-hidezeros"></a><span data-ttu-id="d5a45-656">メソッド hideZeros</span><span class="sxs-lookup"><span data-stu-id="d5a45-656">Method hideZeros</span></span>

    public boolean hideZeros()

#### <a name="return-value"></a><span data-ttu-id="d5a45-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-657">Return Value</span></span>

### <a name="method-isoneline"></a><span data-ttu-id="d5a45-658">メソッド isOneline</span><span class="sxs-lookup"><span data-stu-id="d5a45-658">Method isOneline</span></span>

    public boolean isOneline()

#### <a name="return-value"></a><span data-ttu-id="d5a45-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-659">Return Value</span></span>

### <a name="method-isoverlapping"></a><span data-ttu-id="d5a45-660">メソッド isOverlapping</span><span class="sxs-lookup"><span data-stu-id="d5a45-660">Method isOverlapping</span></span>

    public boolean isOverlapping()

#### <a name="return-value"></a><span data-ttu-id="d5a45-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-661">Return Value</span></span>

### <a name="method-italic"></a><span data-ttu-id="d5a45-662">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="d5a45-662">Method italic</span></span>

    public boolean italic()

#### <a name="return-value"></a><span data-ttu-id="d5a45-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-663">Return Value</span></span>

### <a name="method-lateeval"></a><span data-ttu-id="d5a45-664">メソッド lateEval</span><span class="sxs-lookup"><span data-stu-id="d5a45-664">Method lateEval</span></span>

    public LateEvalMode lateEval()

#### <a name="return-value"></a><span data-ttu-id="d5a45-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-665">Return Value</span></span>

### <a name="method-linebottom"></a><span data-ttu-id="d5a45-666">メソッド lineBottom</span><span class="sxs-lookup"><span data-stu-id="d5a45-666">Method lineBottom</span></span>

    public LineType lineBottom()

#### <a name="return-value"></a><span data-ttu-id="d5a45-667">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-667">Return Value</span></span>

### <a name="method-lineleft"></a><span data-ttu-id="d5a45-668">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="d5a45-668">Method lineLeft</span></span>

    public LineType lineLeft()

#### <a name="return-value"></a><span data-ttu-id="d5a45-669">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-669">Return Value</span></span>

### <a name="method-lineright"></a><span data-ttu-id="d5a45-670">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="d5a45-670">Method lineRight</span></span>

    public LineType lineRight()

#### <a name="return-value"></a><span data-ttu-id="d5a45-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-671">Return Value</span></span>

### <a name="method-linetop"></a><span data-ttu-id="d5a45-672">メソッド lineTop</span><span class="sxs-lookup"><span data-stu-id="d5a45-672">Method lineTop</span></span>

    public LineType lineTop()

#### <a name="return-value"></a><span data-ttu-id="d5a45-673">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-673">Return Value</span></span>

### <a name="method-menufunctionhelp"></a><span data-ttu-id="d5a45-674">メソッド menuFunctionHelp</span><span class="sxs-lookup"><span data-stu-id="d5a45-674">Method menuFunctionHelp</span></span>

    public str menuFunctionHelp()

#### <a name="return-value"></a><span data-ttu-id="d5a45-675">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-675">Return Value</span></span>

### <a name="method-menufunctionname"></a><span data-ttu-id="d5a45-676">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="d5a45-676">Method menuFunctionName</span></span>

    public str menuFunctionName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-677">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-677">Return Value</span></span>

### <a name="method-menufunctiontype"></a><span data-ttu-id="d5a45-678">メソッド menuFunctionType</span><span class="sxs-lookup"><span data-stu-id="d5a45-678">Method menuFunctionType</span></span>

    public int menuFunctionType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-679">Return Value</span></span>

### <a name="method-menufunctionweb"></a><span data-ttu-id="d5a45-680">メソッド menuFunctionWeb</span><span class="sxs-lookup"><span data-stu-id="d5a45-680">Method menuFunctionWeb</span></span>

    public str menuFunctionWeb()

#### <a name="return-value"></a><span data-ttu-id="d5a45-681">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-681">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="d5a45-682">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d5a45-682">Method name</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="d5a45-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-683">Return Value</span></span>

### <a name="method-recid"></a><span data-ttu-id="d5a45-684">メソッド recId</span><span class="sxs-lookup"><span data-stu-id="d5a45-684">Method recId</span></span>

    public int recId()

#### <a name="return-value"></a><span data-ttu-id="d5a45-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-685">Return Value</span></span>

### <a name="method-showprompt"></a><span data-ttu-id="d5a45-686">メソッド showPrompt</span><span class="sxs-lookup"><span data-stu-id="d5a45-686">Method showPrompt</span></span>

    public boolean showPrompt()

#### <a name="return-value"></a><span data-ttu-id="d5a45-687">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-687">Return Value</span></span>

### <a name="method-strikethrough"></a><span data-ttu-id="d5a45-688">メソッド strikeThrough</span><span class="sxs-lookup"><span data-stu-id="d5a45-688">Method strikeThrough</span></span>

    public boolean strikeThrough()

#### <a name="return-value"></a><span data-ttu-id="d5a45-689">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-689">Return Value</span></span>

### <a name="method-tablehandle"></a><span data-ttu-id="d5a45-690">メソッド tableHandle</span><span class="sxs-lookup"><span data-stu-id="d5a45-690">Method tableHandle</span></span>

    public TableId tableHandle()

#### <a name="return-value"></a><span data-ttu-id="d5a45-691">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-691">Return Value</span></span>

### <a name="method-tablename"></a><span data-ttu-id="d5a45-692">メソッド tableName</span><span class="sxs-lookup"><span data-stu-id="d5a45-692">Method tableName</span></span>

    public str tableName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-693">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-693">Return Value</span></span>

### <a name="method-turnsign"></a><span data-ttu-id="d5a45-694">メソッド turnSign</span><span class="sxs-lookup"><span data-stu-id="d5a45-694">Method turnSign</span></span>

    public boolean turnSign()

#### <a name="return-value"></a><span data-ttu-id="d5a45-695">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-695">Return Value</span></span>

### <a name="method-type"></a><span data-ttu-id="d5a45-696">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="d5a45-696">Method type</span></span>

    public int type()

#### <a name="return-value"></a><span data-ttu-id="d5a45-697">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-697">Return Value</span></span>

### <a name="method-underline"></a><span data-ttu-id="d5a45-698">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="d5a45-698">Method underline</span></span>

    public boolean underline()

#### <a name="return-value"></a><span data-ttu-id="d5a45-699">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-699">Return Value</span></span>

### <a name="method-webmenuitemname"></a><span data-ttu-id="d5a45-700">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="d5a45-700">Method webMenuItemName</span></span>

    public str webMenuItemName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-701">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-701">Return Value</span></span>

### <a name="method-webmenuitemtype"></a><span data-ttu-id="d5a45-702">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="d5a45-702">Method webMenuItemType</span></span>

    public int webMenuItemType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-703">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-703">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="d5a45-704">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="d5a45-704">Method webTarget</span></span>

    public str webTarget()

#### <a name="return-value"></a><span data-ttu-id="d5a45-705">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-705">Return Value</span></span>

### <a name="method-weight"></a><span data-ttu-id="d5a45-706">メソッド weight</span><span class="sxs-lookup"><span data-stu-id="d5a45-706">Method weight</span></span>

    public int weight()

#### <a name="return-value"></a><span data-ttu-id="d5a45-707">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-707">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="d5a45-708">メソッド width</span><span class="sxs-lookup"><span data-stu-id="d5a45-708">Method width</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="d5a45-709">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-709">Return Value</span></span>

### <a name="method-widthmode"></a><span data-ttu-id="d5a45-710">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="d5a45-710">Method widthMode</span></span>

    public int widthMode()

#### <a name="return-value"></a><span data-ttu-id="d5a45-711">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-711">Return Value</span></span>

### <a name="method-xpos"></a><span data-ttu-id="d5a45-712">メソッド xPos</span><span class="sxs-lookup"><span data-stu-id="d5a45-712">Method xPos</span></span>

    public int xPos()

#### <a name="return-value"></a><span data-ttu-id="d5a45-713">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-713">Return Value</span></span>

### <a name="method-ypos"></a><span data-ttu-id="d5a45-714">メソッド yPos</span><span class="sxs-lookup"><span data-stu-id="d5a45-714">Method yPos</span></span>

    public int yPos()

#### <a name="return-value"></a><span data-ttu-id="d5a45-715">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-715">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-716">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-716">Method new</span></span>

<span data-ttu-id="d5a45-717">OutputField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-717">Initializes a new instance of the OutputField class.</span></span>

    public void new()

## <a name="class-outputfootersection"></a><span data-ttu-id="d5a45-718">クラス OutputFooterSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-718">Class OutputFooterSection</span></span>
    class OutputFooterSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-719">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-719">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-720">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-720">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-721">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-721">Methods</span></span>

| <span data-ttu-id="d5a45-722">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-722">Method</span></span>                                | <span data-ttu-id="d5a45-723">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-723">Description</span></span>                                                  |
|---------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a45-724">public int level()</span><span class="sxs-lookup"><span data-stu-id="d5a45-724">public int level()</span></span>                    |                                                              |
| <span data-ttu-id="d5a45-725">public int level2field(\[int level\])</span><span class="sxs-lookup"><span data-stu-id="d5a45-725">public int level2field(\[int level\])</span></span> |                                                              |
| <span data-ttu-id="d5a45-726">public int niveau()</span><span class="sxs-lookup"><span data-stu-id="d5a45-726">public int niveau()</span></span>                   |                                                              |
| <span data-ttu-id="d5a45-727">public int table()</span><span class="sxs-lookup"><span data-stu-id="d5a45-727">public int table()</span></span>                    |                                                              |
| <span data-ttu-id="d5a45-728">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-728">public void new()</span></span>                     | <span data-ttu-id="d5a45-729">OutputFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-729">Initializes a new instance of the OutputFooterSection class.</span></span> |

### <a name="method-level"></a><span data-ttu-id="d5a45-730">メソッド level</span><span class="sxs-lookup"><span data-stu-id="d5a45-730">Method level</span></span>

    public int level()

#### <a name="return-value"></a><span data-ttu-id="d5a45-731">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-731">Return Value</span></span>

### <a name="method-level2field"></a><span data-ttu-id="d5a45-732">メソッド level2field</span><span class="sxs-lookup"><span data-stu-id="d5a45-732">Method level2field</span></span>

    public int level2field([int level])

#### <a name="parameters"></a><span data-ttu-id="d5a45-733">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-733">Parameters</span></span>

<span data-ttu-id="d5a45-734">level</span><span class="sxs-lookup"><span data-stu-id="d5a45-734">level</span></span>  

#### <a name="return-value"></a><span data-ttu-id="d5a45-735">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-735">Return Value</span></span>

### <a name="method-niveau"></a><span data-ttu-id="d5a45-736">メソッド niveau</span><span class="sxs-lookup"><span data-stu-id="d5a45-736">Method niveau</span></span>

    public int niveau()

#### <a name="return-value"></a><span data-ttu-id="d5a45-737">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-737">Return Value</span></span>

### <a name="method-table"></a><span data-ttu-id="d5a45-738">メソッド table</span><span class="sxs-lookup"><span data-stu-id="d5a45-738">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="d5a45-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-739">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-740">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-740">Method new</span></span>

<span data-ttu-id="d5a45-741">OutputFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-741">Initializes a new instance of the OutputFooterSection class.</span></span>

    public void new()

## <a name="class-outputheadersection"></a><span data-ttu-id="d5a45-742">クラス OutputHeaderSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-742">Class OutputHeaderSection</span></span>
    class OutputHeaderSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-743">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-743">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-744">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-744">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-745">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-745">Methods</span></span>

| <span data-ttu-id="d5a45-746">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-746">Method</span></span>             | <span data-ttu-id="d5a45-747">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-747">Description</span></span>                                                  |
|--------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a45-748">public int table()</span><span class="sxs-lookup"><span data-stu-id="d5a45-748">public int table()</span></span> |                                                              |
| <span data-ttu-id="d5a45-749">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-749">public void new()</span></span>  | <span data-ttu-id="d5a45-750">OutputHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-750">Initializes a new instance of the OutputHeaderSection class.</span></span> |

### <a name="method-table"></a><span data-ttu-id="d5a45-751">メソッド table</span><span class="sxs-lookup"><span data-stu-id="d5a45-751">Method table</span></span>

    public int table()

#### <a name="return-value"></a><span data-ttu-id="d5a45-752">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-752">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-753">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-753">Method new</span></span>

<span data-ttu-id="d5a45-754">OutputHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-754">Initializes a new instance of the OutputHeaderSection class.</span></span>

    public void new()

## <a name="class-outputintegerfield"></a><span data-ttu-id="d5a45-755">クラス OutputIntegerField</span><span class="sxs-lookup"><span data-stu-id="d5a45-755">Class OutputIntegerField</span></span>
    class OutputIntegerField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-756">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-756">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-757">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-757">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-758">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-758">Methods</span></span>

| <span data-ttu-id="d5a45-759">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-759">Method</span></span>                        | <span data-ttu-id="d5a45-760">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-760">Description</span></span>                                                 |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5a45-761">public int displaceNegative()</span><span class="sxs-lookup"><span data-stu-id="d5a45-761">public int displaceNegative()</span></span> |                                                             |
| <span data-ttu-id="d5a45-762">public boolean negative()</span><span class="sxs-lookup"><span data-stu-id="d5a45-762">public boolean negative()</span></span>     |                                                             |
| <span data-ttu-id="d5a45-763">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-763">public str toString()</span></span>         | <span data-ttu-id="d5a45-764">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-764">Returns a string that represents the current object.</span></span>        |
| <span data-ttu-id="d5a45-765">public int value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-765">public int value()</span></span>            |                                                             |
| <span data-ttu-id="d5a45-766">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-766">public void new()</span></span>             | <span data-ttu-id="d5a45-767">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-767">Initializes a new instance of the OutputIntegerField class.</span></span> |

### <a name="method-displacenegative"></a><span data-ttu-id="d5a45-768">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="d5a45-768">Method displaceNegative</span></span>

    public int displaceNegative()

#### <a name="return-value"></a><span data-ttu-id="d5a45-769">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-769">Return Value</span></span>

### <a name="method-negative"></a><span data-ttu-id="d5a45-770">メソッド negative</span><span class="sxs-lookup"><span data-stu-id="d5a45-770">Method negative</span></span>

    public boolean negative()

#### <a name="return-value"></a><span data-ttu-id="d5a45-771">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-771">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-772">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-772">Method toString</span></span>

<span data-ttu-id="d5a45-773">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-773">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-774">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-774">Return Value</span></span>

<span data-ttu-id="d5a45-775">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-775">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-776">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-776">Remarks</span></span>

<span data-ttu-id="d5a45-777">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-777">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-778">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-778">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-779">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-779">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-780">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-780">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-781">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-781">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-782">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-782">Method new</span></span>

<span data-ttu-id="d5a45-783">OutputIntegerField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-783">Initializes a new instance of the OutputIntegerField class.</span></span>

    public void new()

## <a name="class-outputlabelfield"></a><span data-ttu-id="d5a45-784">クラス OutputLabelField</span><span class="sxs-lookup"><span data-stu-id="d5a45-784">Class OutputLabelField</span></span>
    class OutputLabelField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-785">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-785">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-786">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-786">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-787">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-787">Methods</span></span>

| <span data-ttu-id="d5a45-788">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-788">Method</span></span>                | <span data-ttu-id="d5a45-789">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-789">Description</span></span>                                               |
|-----------------------|-----------------------------------------------------------|
| <span data-ttu-id="d5a45-790">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-790">public str toString()</span></span> | <span data-ttu-id="d5a45-791">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-791">Returns a string that represents the current object.</span></span>      |
| <span data-ttu-id="d5a45-792">public str value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-792">public str value()</span></span>    |                                                           |
| <span data-ttu-id="d5a45-793">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-793">public void new()</span></span>     | <span data-ttu-id="d5a45-794">OutputLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-794">Initializes a new instance of the OutputLabelField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-795">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-795">Method toString</span></span>

<span data-ttu-id="d5a45-796">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-796">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-797">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-797">Return Value</span></span>

<span data-ttu-id="d5a45-798">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-798">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-799">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-799">Remarks</span></span>

<span data-ttu-id="d5a45-800">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-800">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-801">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-801">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-802">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-802">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-803">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-803">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-804">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-804">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-805">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-805">Method new</span></span>

<span data-ttu-id="d5a45-806">OutputLabelField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-806">Initializes a new instance of the OutputLabelField class.</span></span>

    public void new()

## <a name="class-outputpage"></a><span data-ttu-id="d5a45-807">クラス OutputPage</span><span class="sxs-lookup"><span data-stu-id="d5a45-807">Class OutputPage</span></span>
    class OutputPage extends Object

### <a name="remarks"></a><span data-ttu-id="d5a45-808">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-808">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-809">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-809">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-810">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-810">Methods</span></span>

| <span data-ttu-id="d5a45-811">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-811">Method</span></span>                        | <span data-ttu-id="d5a45-812">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-812">Description</span></span>                                         |
|-------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d5a45-813">public int bottomMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-813">public int bottomMargin()</span></span>     |                                                     |
| <span data-ttu-id="d5a45-814">public str fontName()</span><span class="sxs-lookup"><span data-stu-id="d5a45-814">public str fontName()</span></span>         |                                                     |
| <span data-ttu-id="d5a45-815">public int height()</span><span class="sxs-lookup"><span data-stu-id="d5a45-815">public int height()</span></span>           |                                                     |
| <span data-ttu-id="d5a45-816">public boolean layoutRTL()</span><span class="sxs-lookup"><span data-stu-id="d5a45-816">public boolean layoutRTL()</span></span>    |                                                     |
| <span data-ttu-id="d5a45-817">public int leftMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-817">public int leftMargin()</span></span>       |                                                     |
| <span data-ttu-id="d5a45-818">public str pageNumber()</span><span class="sxs-lookup"><span data-stu-id="d5a45-818">public str pageNumber()</span></span>       |                                                     |
| <span data-ttu-id="d5a45-819">public int rightMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-819">public int rightMargin()</span></span>      |                                                     |
| <span data-ttu-id="d5a45-820">public int sectionNo()</span><span class="sxs-lookup"><span data-stu-id="d5a45-820">public int sectionNo()</span></span>        |                                                     |
| <span data-ttu-id="d5a45-821">public int topMargin()</span><span class="sxs-lookup"><span data-stu-id="d5a45-821">public int topMargin()</span></span>        |                                                     |
| <span data-ttu-id="d5a45-822">public int unusedBottom()</span><span class="sxs-lookup"><span data-stu-id="d5a45-822">public int unusedBottom()</span></span>     |                                                     |
| <span data-ttu-id="d5a45-823">public int unusedLeft()</span><span class="sxs-lookup"><span data-stu-id="d5a45-823">public int unusedLeft()</span></span>       |                                                     |
| <span data-ttu-id="d5a45-824">public int unusedRight()</span><span class="sxs-lookup"><span data-stu-id="d5a45-824">public int unusedRight()</span></span>      |                                                     |
| <span data-ttu-id="d5a45-825">public int unusedTop()</span><span class="sxs-lookup"><span data-stu-id="d5a45-825">public int unusedTop()</span></span>        |                                                     |
| <span data-ttu-id="d5a45-826">public int virtualPageWidth()</span><span class="sxs-lookup"><span data-stu-id="d5a45-826">public int virtualPageWidth()</span></span> |                                                     |
| <span data-ttu-id="d5a45-827">public int width()</span><span class="sxs-lookup"><span data-stu-id="d5a45-827">public int width()</span></span>            |                                                     |
| <span data-ttu-id="d5a45-828">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-828">public void new()</span></span>             | <span data-ttu-id="d5a45-829">OutputPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-829">Initializes a new instance of the OutputPage class.</span></span> |

### <a name="method-bottommargin"></a><span data-ttu-id="d5a45-830">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-830">Method bottomMargin</span></span>

    public int bottomMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-831">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="d5a45-832">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="d5a45-832">Method fontName</span></span>

    public str fontName()

#### <a name="return-value"></a><span data-ttu-id="d5a45-833">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-833">Return Value</span></span>

### <a name="method-height"></a><span data-ttu-id="d5a45-834">メソッド height</span><span class="sxs-lookup"><span data-stu-id="d5a45-834">Method height</span></span>

    public int height()

#### <a name="return-value"></a><span data-ttu-id="d5a45-835">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-835">Return Value</span></span>

### <a name="method-layoutrtl"></a><span data-ttu-id="d5a45-836">メソッド layoutRTL</span><span class="sxs-lookup"><span data-stu-id="d5a45-836">Method layoutRTL</span></span>

    public boolean layoutRTL()

#### <a name="return-value"></a><span data-ttu-id="d5a45-837">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-837">Return Value</span></span>

### <a name="method-leftmargin"></a><span data-ttu-id="d5a45-838">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-838">Method leftMargin</span></span>

    public int leftMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-839">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-839">Return Value</span></span>

### <a name="method-pagenumber"></a><span data-ttu-id="d5a45-840">メソッド pageNumber</span><span class="sxs-lookup"><span data-stu-id="d5a45-840">Method pageNumber</span></span>

    public str pageNumber()

#### <a name="return-value"></a><span data-ttu-id="d5a45-841">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-841">Return Value</span></span>

### <a name="method-rightmargin"></a><span data-ttu-id="d5a45-842">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-842">Method rightMargin</span></span>

    public int rightMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-843">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-843">Return Value</span></span>

### <a name="method-sectionno"></a><span data-ttu-id="d5a45-844">メソッド sectionNo</span><span class="sxs-lookup"><span data-stu-id="d5a45-844">Method sectionNo</span></span>

    public int sectionNo()

#### <a name="return-value"></a><span data-ttu-id="d5a45-845">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-845">Return Value</span></span>

### <a name="method-topmargin"></a><span data-ttu-id="d5a45-846">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="d5a45-846">Method topMargin</span></span>

    public int topMargin()

#### <a name="return-value"></a><span data-ttu-id="d5a45-847">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-847">Return Value</span></span>

### <a name="method-unusedbottom"></a><span data-ttu-id="d5a45-848">メソッド unusedBottom</span><span class="sxs-lookup"><span data-stu-id="d5a45-848">Method unusedBottom</span></span>

    public int unusedBottom()

#### <a name="return-value"></a><span data-ttu-id="d5a45-849">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-849">Return Value</span></span>

### <a name="method-unusedleft"></a><span data-ttu-id="d5a45-850">メソッド unusedLeft</span><span class="sxs-lookup"><span data-stu-id="d5a45-850">Method unusedLeft</span></span>

    public int unusedLeft()

#### <a name="return-value"></a><span data-ttu-id="d5a45-851">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-851">Return Value</span></span>

### <a name="method-unusedright"></a><span data-ttu-id="d5a45-852">メソッド unusedRight</span><span class="sxs-lookup"><span data-stu-id="d5a45-852">Method unusedRight</span></span>

    public int unusedRight()

#### <a name="return-value"></a><span data-ttu-id="d5a45-853">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-853">Return Value</span></span>

### <a name="method-unusedtop"></a><span data-ttu-id="d5a45-854">メソッド unusedTop</span><span class="sxs-lookup"><span data-stu-id="d5a45-854">Method unusedTop</span></span>

    public int unusedTop()

#### <a name="return-value"></a><span data-ttu-id="d5a45-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-855">Return Value</span></span>

### <a name="method-virtualpagewidth"></a><span data-ttu-id="d5a45-856">メソッド virtualPageWidth</span><span class="sxs-lookup"><span data-stu-id="d5a45-856">Method virtualPageWidth</span></span>

    public int virtualPageWidth()

#### <a name="return-value"></a><span data-ttu-id="d5a45-857">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-857">Return Value</span></span>

### <a name="method-width"></a><span data-ttu-id="d5a45-858">メソッド width</span><span class="sxs-lookup"><span data-stu-id="d5a45-858">Method width</span></span>

    public int width()

#### <a name="return-value"></a><span data-ttu-id="d5a45-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-859">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-860">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-860">Method new</span></span>

<span data-ttu-id="d5a45-861">OutputPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-861">Initializes a new instance of the OutputPage class.</span></span>

    public void new()

## <a name="class-outputpagefootersection"></a><span data-ttu-id="d5a45-862">クラス OutputPageFooterSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-862">Class OutputPageFooterSection</span></span>
    class OutputPageFooterSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-863">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-863">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-864">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-864">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-865">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-865">Methods</span></span>

| <span data-ttu-id="d5a45-866">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-866">Method</span></span>            | <span data-ttu-id="d5a45-867">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-867">Description</span></span>                                                      |
|-------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5a45-868">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-868">public void new()</span></span> | <span data-ttu-id="d5a45-869">OutputPageFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-869">Initializes a new instance of the OutputPageFooterSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-870">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-870">Method new</span></span>

<span data-ttu-id="d5a45-871">OutputPageFooterSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-871">Initializes a new instance of the OutputPageFooterSection class.</span></span>

    public void new()

## <a name="class-outputpageheadersection"></a><span data-ttu-id="d5a45-872">クラス OutputPageHeaderSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-872">Class OutputPageHeaderSection</span></span>
    class OutputPageHeaderSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-873">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-873">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-874">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-874">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-875">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-875">Methods</span></span>

| <span data-ttu-id="d5a45-876">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-876">Method</span></span>            | <span data-ttu-id="d5a45-877">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-877">Description</span></span>                                                      |
|-------------------|------------------------------------------------------------------|
| <span data-ttu-id="d5a45-878">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-878">public void new()</span></span> | <span data-ttu-id="d5a45-879">OutputPageHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-879">Initializes a new instance of the OutputPageHeaderSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-880">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-880">Method new</span></span>

<span data-ttu-id="d5a45-881">OutputPageHeaderSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-881">Initializes a new instance of the OutputPageHeaderSection class.</span></span>

    public void new()

## <a name="class-outputprogrammablesection"></a><span data-ttu-id="d5a45-882">クラス OutputProgrammableSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-882">Class OutputProgrammableSection</span></span>
    class OutputProgrammableSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-883">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-883">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-884">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-884">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-885">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-885">Methods</span></span>

| <span data-ttu-id="d5a45-886">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-886">Method</span></span>              | <span data-ttu-id="d5a45-887">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-887">Description</span></span>                                                        |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d5a45-888">public str number()</span><span class="sxs-lookup"><span data-stu-id="d5a45-888">public str number()</span></span> |                                                                    |
| <span data-ttu-id="d5a45-889">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-889">public void new()</span></span>   | <span data-ttu-id="d5a45-890">OutputProgrammableSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-890">Initializes a new instance of the OutputProgrammableSection class.</span></span> |

### <a name="method-number"></a><span data-ttu-id="d5a45-891">メソッド number</span><span class="sxs-lookup"><span data-stu-id="d5a45-891">Method number</span></span>

    public str number()

#### <a name="return-value"></a><span data-ttu-id="d5a45-892">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-892">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-893">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-893">Method new</span></span>

<span data-ttu-id="d5a45-894">OutputProgrammableSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-894">Initializes a new instance of the OutputProgrammableSection class.</span></span>

    public void new()

## <a name="class-outputprologsection"></a><span data-ttu-id="d5a45-895">クラス OutputPrologSection</span><span class="sxs-lookup"><span data-stu-id="d5a45-895">Class OutputPrologSection</span></span>
    class OutputPrologSection extends OuputSection

### <a name="remarks"></a><span data-ttu-id="d5a45-896">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-896">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-897">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-897">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-898">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-898">Methods</span></span>

| <span data-ttu-id="d5a45-899">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-899">Method</span></span>            | <span data-ttu-id="d5a45-900">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-900">Description</span></span>                                                  |
|-------------------|--------------------------------------------------------------|
| <span data-ttu-id="d5a45-901">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-901">public void new()</span></span> | <span data-ttu-id="d5a45-902">OutputPrologSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-902">Initializes a new instance of the OutputPrologSection class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="d5a45-903">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-903">Method new</span></span>

<span data-ttu-id="d5a45-904">OutputPrologSection クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-904">Initializes a new instance of the OutputPrologSection class.</span></span>

    public void new()

## <a name="class-outputrealfield"></a><span data-ttu-id="d5a45-905">クラス OutputRealField</span><span class="sxs-lookup"><span data-stu-id="d5a45-905">Class OutputRealField</span></span>
    class OutputRealField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-906">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-906">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-907">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-907">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-908">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-908">Methods</span></span>

| <span data-ttu-id="d5a45-909">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-909">Method</span></span>                        | <span data-ttu-id="d5a45-910">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-910">Description</span></span>                                              |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d5a45-911">public int displaceNegative()</span><span class="sxs-lookup"><span data-stu-id="d5a45-911">public int displaceNegative()</span></span> |                                                          |
| <span data-ttu-id="d5a45-912">public boolean negative()</span><span class="sxs-lookup"><span data-stu-id="d5a45-912">public boolean negative()</span></span>     |                                                          |
| <span data-ttu-id="d5a45-913">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-913">public str toString()</span></span>         | <span data-ttu-id="d5a45-914">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-914">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="d5a45-915">public Real value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-915">public Real value()</span></span>           |                                                          |
| <span data-ttu-id="d5a45-916">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-916">public void new()</span></span>             | <span data-ttu-id="d5a45-917">OutputRealField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-917">Initializes a new instance of the OutputRealField class.</span></span> |

### <a name="method-displacenegative"></a><span data-ttu-id="d5a45-918">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="d5a45-918">Method displaceNegative</span></span>

    public int displaceNegative()

#### <a name="return-value"></a><span data-ttu-id="d5a45-919">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-919">Return Value</span></span>

### <a name="method-negative"></a><span data-ttu-id="d5a45-920">メソッド negative</span><span class="sxs-lookup"><span data-stu-id="d5a45-920">Method negative</span></span>

    public boolean negative()

#### <a name="return-value"></a><span data-ttu-id="d5a45-921">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-921">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-922">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-922">Method toString</span></span>

<span data-ttu-id="d5a45-923">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-923">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-924">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-924">Return Value</span></span>

<span data-ttu-id="d5a45-925">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-925">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-926">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-926">Remarks</span></span>

<span data-ttu-id="d5a45-927">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-927">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-928">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-928">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-929">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-929">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-930">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-930">Method value</span></span>

    public Real value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-931">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-932">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-932">Method new</span></span>

<span data-ttu-id="d5a45-933">OutputRealField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-933">Initializes a new instance of the OutputRealField class.</span></span>

    public void new()

## <a name="class-outputshapefield"></a><span data-ttu-id="d5a45-934">クラス OutputShapeField</span><span class="sxs-lookup"><span data-stu-id="d5a45-934">Class OutputShapeField</span></span>
    class OutputShapeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-935">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-935">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-936">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-936">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-937">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-937">Methods</span></span>

| <span data-ttu-id="d5a45-938">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-938">Method</span></span>                       | <span data-ttu-id="d5a45-939">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-939">Description</span></span>                                               |
|------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d5a45-940">public int borderWidth()</span><span class="sxs-lookup"><span data-stu-id="d5a45-940">public int borderWidth()</span></span>     |                                                           |
| <span data-ttu-id="d5a45-941">public LineType lineType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-941">public LineType lineType()</span></span>   |                                                           |
| <span data-ttu-id="d5a45-942">public ShapeType shapeType()</span><span class="sxs-lookup"><span data-stu-id="d5a45-942">public ShapeType shapeType()</span></span> |                                                           |
| <span data-ttu-id="d5a45-943">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-943">public str toString()</span></span>        | <span data-ttu-id="d5a45-944">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-944">Returns a string that represents the current object.</span></span>      |
| <span data-ttu-id="d5a45-945">public int value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-945">public int value()</span></span>           |                                                           |
| <span data-ttu-id="d5a45-946">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-946">public void new()</span></span>            | <span data-ttu-id="d5a45-947">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-947">Initializes a new instance of the OutputShapeField class.</span></span> |

### <a name="method-borderwidth"></a><span data-ttu-id="d5a45-948">メソッド borderWidth</span><span class="sxs-lookup"><span data-stu-id="d5a45-948">Method borderWidth</span></span>

    public int borderWidth()

#### <a name="return-value"></a><span data-ttu-id="d5a45-949">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-949">Return Value</span></span>

### <a name="method-linetype"></a><span data-ttu-id="d5a45-950">メソッド lineType</span><span class="sxs-lookup"><span data-stu-id="d5a45-950">Method lineType</span></span>

    public LineType lineType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-951">Return Value</span></span>

### <a name="method-shapetype"></a><span data-ttu-id="d5a45-952">メソッド shapeType</span><span class="sxs-lookup"><span data-stu-id="d5a45-952">Method shapeType</span></span>

    public ShapeType shapeType()

#### <a name="return-value"></a><span data-ttu-id="d5a45-953">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-953">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="d5a45-954">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-954">Method toString</span></span>

<span data-ttu-id="d5a45-955">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-955">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-956">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-956">Return Value</span></span>

<span data-ttu-id="d5a45-957">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-957">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-958">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-958">Remarks</span></span>

<span data-ttu-id="d5a45-959">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-959">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-960">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-960">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-961">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-961">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-962">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-962">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-963">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-963">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-964">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-964">Method new</span></span>

<span data-ttu-id="d5a45-965">OutputShapeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-965">Initializes a new instance of the OutputShapeField class.</span></span>

    public void new()

## <a name="class-outputstatictextfield"></a><span data-ttu-id="d5a45-966">クラス OutputStaticTextField</span><span class="sxs-lookup"><span data-stu-id="d5a45-966">Class OutputStaticTextField</span></span>
    class OutputStaticTextField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-967">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-967">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-968">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-968">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-969">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-969">Methods</span></span>

| <span data-ttu-id="d5a45-970">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-970">Method</span></span>                | <span data-ttu-id="d5a45-971">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-971">Description</span></span>                                                    |
|-----------------------|----------------------------------------------------------------|
| <span data-ttu-id="d5a45-972">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-972">public str toString()</span></span> | <span data-ttu-id="d5a45-973">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-973">Returns a string that represents the current object.</span></span>           |
| <span data-ttu-id="d5a45-974">public str value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-974">public str value()</span></span>    |                                                                |
| <span data-ttu-id="d5a45-975">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-975">public void new()</span></span>     | <span data-ttu-id="d5a45-976">OutputStaticTextField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-976">Initializes a new instance of the OutputStaticTextField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-977">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-977">Method toString</span></span>

<span data-ttu-id="d5a45-978">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-978">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-979">Return Value</span></span>

<span data-ttu-id="d5a45-980">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-980">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-981">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-981">Remarks</span></span>

<span data-ttu-id="d5a45-982">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-982">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-983">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-983">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-984">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-984">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-985">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-985">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-986">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-986">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-987">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-987">Method new</span></span>

<span data-ttu-id="d5a45-988">OutputStaticTextField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-988">Initializes a new instance of the OutputStaticTextField class.</span></span>

    public void new()

## <a name="class-outputstringfield"></a><span data-ttu-id="d5a45-989">クラス OutputStringField</span><span class="sxs-lookup"><span data-stu-id="d5a45-989">Class OutputStringField</span></span>
    class OutputStringField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-990">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-990">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-991">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-991">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-992">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-992">Methods</span></span>

| <span data-ttu-id="d5a45-993">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-993">Method</span></span>                | <span data-ttu-id="d5a45-994">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-994">Description</span></span>                                                |
|-----------------------|------------------------------------------------------------|
| <span data-ttu-id="d5a45-995">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-995">public str toString()</span></span> | <span data-ttu-id="d5a45-996">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-996">Returns a string that represents the current object.</span></span>       |
| <span data-ttu-id="d5a45-997">public str value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-997">public str value()</span></span>    |                                                            |
| <span data-ttu-id="d5a45-998">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-998">public void new()</span></span>     | <span data-ttu-id="d5a45-999">OutputStringField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-999">Initializes a new instance of the OutputStringField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-1000">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-1000">Method toString</span></span>

<span data-ttu-id="d5a45-1001">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1001">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1002">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1002">Return Value</span></span>

<span data-ttu-id="d5a45-1003">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1003">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-1004">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1004">Remarks</span></span>

<span data-ttu-id="d5a45-1005">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1005">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-1006">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1006">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-1007">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1007">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-1008">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-1008">Method value</span></span>

    public str value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1009">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1009">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-1010">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-1010">Method new</span></span>

<span data-ttu-id="d5a45-1011">OutputStringField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1011">Initializes a new instance of the OutputStringField class.</span></span>

    public void new()

## <a name="class-outputsumfield"></a><span data-ttu-id="d5a45-1012">クラス OutputSumField</span><span class="sxs-lookup"><span data-stu-id="d5a45-1012">Class OutputSumField</span></span>
    class OutputSumField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-1013">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1013">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-1014">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-1014">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-1015">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-1015">Methods</span></span>

| <span data-ttu-id="d5a45-1016">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-1016">Method</span></span>                | <span data-ttu-id="d5a45-1017">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-1017">Description</span></span>                                             |
|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="d5a45-1018">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1018">public str toString()</span></span> | <span data-ttu-id="d5a45-1019">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1019">Returns a string that represents the current object.</span></span>    |
| <span data-ttu-id="d5a45-1020">public Real value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1020">public Real value()</span></span>   |                                                         |
| <span data-ttu-id="d5a45-1021">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1021">public void new()</span></span>     | <span data-ttu-id="d5a45-1022">OutputSumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1022">Initializes a new instance of the OutputSumField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-1023">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-1023">Method toString</span></span>

<span data-ttu-id="d5a45-1024">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1024">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1025">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1025">Return Value</span></span>

<span data-ttu-id="d5a45-1026">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1026">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-1027">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1027">Remarks</span></span>

<span data-ttu-id="d5a45-1028">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1028">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-1029">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1029">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-1030">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1030">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-1031">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-1031">Method value</span></span>

    public Real value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1032">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-1033">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-1033">Method new</span></span>

<span data-ttu-id="d5a45-1034">OutputSumField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1034">Initializes a new instance of the OutputSumField class.</span></span>

    public void new()

## <a name="class-outputtimefield"></a><span data-ttu-id="d5a45-1035">クラス OutputTimeField</span><span class="sxs-lookup"><span data-stu-id="d5a45-1035">Class OutputTimeField</span></span>
    class OutputTimeField extends OutputField

### <a name="remarks"></a><span data-ttu-id="d5a45-1036">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1036">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-1037">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-1037">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-1038">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-1038">Methods</span></span>

| <span data-ttu-id="d5a45-1039">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-1039">Method</span></span>                | <span data-ttu-id="d5a45-1040">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-1040">Description</span></span>                                              |
|-----------------------|----------------------------------------------------------|
| <span data-ttu-id="d5a45-1041">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1041">public str toString()</span></span> | <span data-ttu-id="d5a45-1042">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1042">Returns a string that represents the current object.</span></span>     |
| <span data-ttu-id="d5a45-1043">public int value()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1043">public int value()</span></span>    |                                                          |
| <span data-ttu-id="d5a45-1044">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1044">public void new()</span></span>     | <span data-ttu-id="d5a45-1045">OutputTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1045">Initializes a new instance of the OutputTimeField class.</span></span> |

### <a name="method-tostring"></a><span data-ttu-id="d5a45-1046">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d5a45-1046">Method toString</span></span>

<span data-ttu-id="d5a45-1047">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1047">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1048">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1048">Return Value</span></span>

<span data-ttu-id="d5a45-1049">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1049">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-1050">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1050">Remarks</span></span>

<span data-ttu-id="d5a45-1051">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1051">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d5a45-1052">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1052">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="d5a45-1053">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1053">For example, an instance of the SysMethodInfo class returns the method name and the type of the method, such as instance or static.</span></span>

### <a name="method-value"></a><span data-ttu-id="d5a45-1054">メソッド value</span><span class="sxs-lookup"><span data-stu-id="d5a45-1054">Method value</span></span>

    public int value()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1055">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1055">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-1056">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-1056">Method new</span></span>

<span data-ttu-id="d5a45-1057">OutputTimeField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1057">Initializes a new instance of the OutputTimeField class.</span></span>

    public void new()

## <a name="class-overwritesystemfieldspermission"></a><span data-ttu-id="d5a45-1058">クラス OverwriteSystemfieldsPermission</span><span class="sxs-lookup"><span data-stu-id="d5a45-1058">Class OverwriteSystemfieldsPermission</span></span>
    class OverwriteSystemfieldsPermission extends CodeAccessPermission

### <a name="remarks"></a><span data-ttu-id="d5a45-1059">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1059">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d5a45-1060">例</span><span class="sxs-lookup"><span data-stu-id="d5a45-1060">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="d5a45-1061">メソッド</span><span class="sxs-lookup"><span data-stu-id="d5a45-1061">Methods</span></span>

| <span data-ttu-id="d5a45-1062">方法</span><span class="sxs-lookup"><span data-stu-id="d5a45-1062">Method</span></span>                                                 | <span data-ttu-id="d5a45-1063">説明</span><span class="sxs-lookup"><span data-stu-id="d5a45-1063">Description</span></span>                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a45-1064">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1064">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="d5a45-1065">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1065">Creates and returns a copy of a permission class object.</span></span>                                                                  |
| <span data-ttu-id="d5a45-1066">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="d5a45-1066">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="d5a45-1067">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1067">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span> |
| <span data-ttu-id="d5a45-1068">public void new()</span><span class="sxs-lookup"><span data-stu-id="d5a45-1068">public void new()</span></span>                                      | <span data-ttu-id="d5a45-1069">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1069">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>                                                  |

### <a name="method-copy"></a><span data-ttu-id="d5a45-1070">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="d5a45-1070">Method copy</span></span>

<span data-ttu-id="d5a45-1071">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1071">Creates and returns a copy of a permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="d5a45-1072">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1072">Return Value</span></span>

<span data-ttu-id="d5a45-1073">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1073">A copy of the derived class object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-1074">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1074">Remarks</span></span>

<span data-ttu-id="d5a45-1075">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1075">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="d5a45-1076">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1076">For more information, see “Securing an API that Executes on the Server Tier.”</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="d5a45-1077">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="d5a45-1077">Method isSubsetOf</span></span>

<span data-ttu-id="d5a45-1078">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1078">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="d5a45-1079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5a45-1079">Parameters</span></span>

<span data-ttu-id="d5a45-1080">target</span><span class="sxs-lookup"><span data-stu-id="d5a45-1080">target</span></span>  
<span data-ttu-id="d5a45-1081">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1081">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d5a45-1082">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5a45-1082">Return Value</span></span>

<span data-ttu-id="d5a45-1083">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1083">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5a45-1084">備考</span><span class="sxs-lookup"><span data-stu-id="d5a45-1084">Remarks</span></span>

<span data-ttu-id="d5a45-1085">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1085">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="d5a45-1086">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1086">For more information, see “Securing an API that Executes on the Server Tier.”</span></span>

### <a name="method-new"></a><span data-ttu-id="d5a45-1087">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d5a45-1087">Method new</span></span>

<span data-ttu-id="d5a45-1088">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d5a45-1088">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>

    public void new()



