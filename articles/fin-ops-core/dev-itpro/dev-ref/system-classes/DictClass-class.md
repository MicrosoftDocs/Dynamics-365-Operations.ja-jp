---
title: DictClass クラス
description: このトピックでは、DictClass クラスについて説明します。
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
ms.openlocfilehash: 6cb92115e246d36b9a641a9941e11d944b3988f9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502729"
---
# <a name="class-dictclass"></a><span data-ttu-id="bcd22-103">クラス DictClass</span><span class="sxs-lookup"><span data-stu-id="bcd22-103">Class DictClass</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictClass extends Object
```

<span data-ttu-id="bcd22-104">DictClass クラスは、クラスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-104">The DictClass class provides information about a class.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcd22-105">備考</span><span class="sxs-lookup"><span data-stu-id="bcd22-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="bcd22-106">例</span><span class="sxs-lookup"><span data-stu-id="bcd22-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="bcd22-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="bcd22-107">Methods</span></span>

| <span data-ttu-id="bcd22-108">方法</span><span class="sxs-lookup"><span data-stu-id="bcd22-108">Method</span></span>                                                            | <span data-ttu-id="bcd22-109">説明</span><span class="sxs-lookup"><span data-stu-id="bcd22-109">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd22-110">public AnyType callObject(str methodName, Object Called, VarArg )</span><span class="sxs-lookup"><span data-stu-id="bcd22-110">public AnyType callObject(str methodName, Object Called, VarArg )</span></span> | <span data-ttu-id="bcd22-111">オブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-111">Calls a method on an object.</span></span>                                                                                                                  |
| <span data-ttu-id="bcd22-112">public AnyType callStatic(str methodName, VarArg )</span><span class="sxs-lookup"><span data-stu-id="bcd22-112">public AnyType callStatic(str methodName, VarArg )</span></span>                | <span data-ttu-id="bcd22-113">静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-113">Calls a static method.</span></span>                                                                                                                        |
| <span data-ttu-id="bcd22-114">public ClassId extend()</span><span class="sxs-lookup"><span data-stu-id="bcd22-114">public ClassId extend()</span></span>                                           | <span data-ttu-id="bcd22-115">指定されたクラスが拡張されるクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-115">Provides the ID for the class that a specified class extends.</span></span>                                                                                 |
| <span data-ttu-id="bcd22-116">public List extendedBy(\[boolean allLevels\])</span><span class="sxs-lookup"><span data-stu-id="bcd22-116">public List extendedBy(\[boolean allLevels\])</span></span>                     | <span data-ttu-id="bcd22-117">指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-117">Provides a List object for the classes that extend a specified class.</span></span>                                                                         |
| <span data-ttu-id="bcd22-118">public Array getAllAttributes()</span><span class="sxs-lookup"><span data-stu-id="bcd22-118">public Array getAllAttributes()</span></span>                                   | <span data-ttu-id="bcd22-119">クラスの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-119">Retrieves the full set of attributes for the class.</span></span>                                                                                           |
| <span data-ttu-id="bcd22-120">public Object getAttribute(str attribute)</span><span class="sxs-lookup"><span data-stu-id="bcd22-120">public Object getAttribute(str attribute)</span></span>                         | <span data-ttu-id="bcd22-121">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-121">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span> |
| <span data-ttu-id="bcd22-122">public Array getAttributes(str attribute)</span><span class="sxs-lookup"><span data-stu-id="bcd22-122">public Array getAttributes(str attribute)</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="bcd22-123">public ClassId id()</span><span class="sxs-lookup"><span data-stu-id="bcd22-123">public ClassId id()</span></span>                                               | <span data-ttu-id="bcd22-124">指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-124">Provides the ID for a specified class.</span></span>                                                                                                        |
| <span data-ttu-id="bcd22-125">public ClassId implements(int no)</span><span class="sxs-lookup"><span data-stu-id="bcd22-125">public ClassId implements(int no)</span></span>                                 | <span data-ttu-id="bcd22-126">クラスが実装する指定されたインターフェイスの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-126">Provides the ID for a specified interface that a class implements.</span></span>                                                                            |
| <span data-ttu-id="bcd22-127">public int implementsCnt()</span><span class="sxs-lookup"><span data-stu-id="bcd22-127">public int implementsCnt()</span></span>                                        | <span data-ttu-id="bcd22-128">クラスが実装するインターフェイスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-128">Indicates the number of interfaces that a class implements.</span></span>                                                                                   |
| <span data-ttu-id="bcd22-129">public boolean isAbstract()</span><span class="sxs-lookup"><span data-stu-id="bcd22-129">public boolean isAbstract()</span></span>                                       | <span data-ttu-id="bcd22-130">クラスが抽象であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-130">Indicates whether a class is abstract.</span></span>                                                                                                        |
| <span data-ttu-id="bcd22-131">public boolean isFinal()</span><span class="sxs-lookup"><span data-stu-id="bcd22-131">public boolean isFinal()</span></span>                                          | <span data-ttu-id="bcd22-132">クラスが最終であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-132">Indicates whether a class is final.</span></span>                                                                                                           |
| <span data-ttu-id="bcd22-133">public boolean isInterface()</span><span class="sxs-lookup"><span data-stu-id="bcd22-133">public boolean isInterface()</span></span>                                      | <span data-ttu-id="bcd22-134">オブジェクトがインターフェイスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-134">Indicates whether an object is an interface.</span></span>                                                                                                  |
| <span data-ttu-id="bcd22-135">public boolean isKernel()</span><span class="sxs-lookup"><span data-stu-id="bcd22-135">public boolean isKernel()</span></span>                                         | <span data-ttu-id="bcd22-136">クラスがカーネル クラスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-136">Indicates whether a class is a kernel class.</span></span>                                                                                                  |
| <span data-ttu-id="bcd22-137">public boolean isRunable()</span><span class="sxs-lookup"><span data-stu-id="bcd22-137">public boolean isRunable()</span></span>                                        | <span data-ttu-id="bcd22-138">クラスを実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-138">Indicates whether a class can be run.</span></span>                                                                                                         |
| <span data-ttu-id="bcd22-139">public Object makeObject(VarArg )</span><span class="sxs-lookup"><span data-stu-id="bcd22-139">public Object makeObject(VarArg )</span></span>                                 | <span data-ttu-id="bcd22-140">オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-140">Creates an object.</span></span>                                                                                                                            |
| <span data-ttu-id="bcd22-141">public str name()</span><span class="sxs-lookup"><span data-stu-id="bcd22-141">public str name()</span></span>                                                 | <span data-ttu-id="bcd22-142">クラスの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-142">Provides the name of a class.</span></span>                                                                                                                 |
| <span data-ttu-id="bcd22-143">public str objectMethod(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="bcd22-143">public str objectMethod(int methodNumber)</span></span>                         | <span data-ttu-id="bcd22-144">クラスの指定されたインスタンス メソッドの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-144">Provides the name of a specified instance method in a class.</span></span>                                                                                  |
| <span data-ttu-id="bcd22-145">public int objectMethodCnt()</span><span class="sxs-lookup"><span data-stu-id="bcd22-145">public int objectMethodCnt()</span></span>                                      | <span data-ttu-id="bcd22-146">クラスのインスタンス メソッドの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-146">Indicates the number of instance methods in a class.</span></span>                                                                                          |
| <span data-ttu-id="bcd22-147">public DictMethod objectMethodObject(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="bcd22-147">public DictMethod objectMethodObject(int methodNumber)</span></span>            | <span data-ttu-id="bcd22-148">DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-148">Provides information about a specified instance method in a class by returning a DictMethod object.</span></span>                                           |
| <span data-ttu-id="bcd22-149">public ClassRunMode RunMode()</span><span class="sxs-lookup"><span data-stu-id="bcd22-149">public ClassRunMode RunMode()</span></span>                                     | <span data-ttu-id="bcd22-150">クラスが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-150">Specifies where a class is executed.</span></span>                                                                                                          |
| <span data-ttu-id="bcd22-151">public str staticMethod(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="bcd22-151">public str staticMethod(int methodNumber)</span></span>                         | <span data-ttu-id="bcd22-152">クラスの指定された静的メソッドの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-152">Provides the name of a specified static method in a class.</span></span>                                                                                    |
| <span data-ttu-id="bcd22-153">public int staticMethodCnt()</span><span class="sxs-lookup"><span data-stu-id="bcd22-153">public int staticMethodCnt()</span></span>                                      | <span data-ttu-id="bcd22-154">クラスの静的メソッドの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-154">Indicates the number of static methods in a class.</span></span>                                                                                            |
| <span data-ttu-id="bcd22-155">public DictMethod staticMethodObject(int methodNumber)</span><span class="sxs-lookup"><span data-stu-id="bcd22-155">public DictMethod staticMethodObject(int methodNumber)</span></span>            | <span data-ttu-id="bcd22-156">DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-156">Provides information about a specified static method in a class by returning a DictMethod object.</span></span>                                             |
| <span data-ttu-id="bcd22-157">::public static Array getAttributedClasses(str attribute)</span><span class="sxs-lookup"><span data-stu-id="bcd22-157">::public static Array getAttributedClasses(str attribute)</span></span>         |                                                                                                                                               |
| <span data-ttu-id="bcd22-158">::public static Object createObject(str className, VarArg )</span><span class="sxs-lookup"><span data-stu-id="bcd22-158">::public static Object createObject(str className, VarArg )</span></span>       |                                                                                                                                               |
| <span data-ttu-id="bcd22-159">public void new(ClassId classId)</span><span class="sxs-lookup"><span data-stu-id="bcd22-159">public void new(ClassId classId)</span></span>                                  | <span data-ttu-id="bcd22-160">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-160">Initializes a new instance of the Object class.</span></span>                                                                                               |

## <a name="method-callobject"></a><span data-ttu-id="bcd22-161">メソッド callObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-161">Method callObject</span></span>

<span data-ttu-id="bcd22-162">オブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-162">Calls a method on an object.</span></span>

```xpp
public AnyType callObject(str methodName, Object Called, VarArg )
```

### <a name="parameters---callobject"></a><span data-ttu-id="bcd22-163">パラメータ - callObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-163">Parameters - callObject</span></span>

<span data-ttu-id="bcd22-164">methodName</span><span class="sxs-lookup"><span data-stu-id="bcd22-164">methodName</span></span>  

<!-- -->

<span data-ttu-id="bcd22-165">呼び出された</span><span class="sxs-lookup"><span data-stu-id="bcd22-165">Called</span></span>  

<!-- -->


### <a name="return-value---callobject"></a><span data-ttu-id="bcd22-166">戻り値 - callObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-166">Return Value - callObject</span></span>

<span data-ttu-id="bcd22-167">指定されたメソッドによって返される anytype データ型値です。</span><span class="sxs-lookup"><span data-stu-id="bcd22-167">An anytype data type value that is returned by the specified method.</span></span>

### <a name="remarks---callobject"></a><span data-ttu-id="bcd22-168">備考 - callObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-168">Remarks - callObject</span></span>

<span data-ttu-id="bcd22-169">callObject メソッドに渡すメソッドを含むクラスを使用して、DictClass オブジェクトのインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-169">You must create an instance of the DictClass object by using a class that contains the method that you pass to the callObject method.</span></span> <span data-ttu-id="bcd22-170">攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-170">If an attacker can control the input to the callObject method, a security risk exists.</span></span> <span data-ttu-id="bcd22-171">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcd22-171">Therefore, this method runs under code access security.</span></span> <span data-ttu-id="bcd22-172">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="bcd22-172">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="bcd22-173">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-173">Make sure that the user has development rights by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---callobject"></a><span data-ttu-id="bcd22-174">例 - callObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-174">Examples - callObject</span></span>

<span data-ttu-id="bcd22-175">この例では、このクラスのグローバル インスタンスの名前が infolog である Info クラスの toString インスタンス メソッドを呼び出し、呼び出しから返された値を出力します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-175">This example calls the toString instance method in the Info class, for which the global instance of this class is named infolog, and then prints the value that is returned from the call.</span></span>

```xpp
static void Job_Example_DictClass_CallObject(Args _args) 
{ 
    DictClass dictClass; 
    anytype   retVal; 
    str      resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictClass.callObject method. 
    // DictClass.callObject runs under code access security. 
    perm.assert(); 
    dictClass = new DictClass(classidget(infolog)); 
    if (dictClass != null) 
    { 
        retVal       = dictClass.callObject("toString", infolog); 
        resultOutput = strfmt("Return value is %1", retVal); 
        print resultOutput; 
        pause; 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-callstatic"></a><span data-ttu-id="bcd22-176">メソッド callStatic</span><span class="sxs-lookup"><span data-stu-id="bcd22-176">Method callStatic</span></span>

<span data-ttu-id="bcd22-177">静的メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-177">Calls a static method.</span></span>

```xpp
public AnyType callStatic(str methodName, VarArg )
```

### <a name="parameters---callstatic"></a><span data-ttu-id="bcd22-178">パラメーター - callStatic</span><span class="sxs-lookup"><span data-stu-id="bcd22-178">Parameters - callStatic</span></span>

<span data-ttu-id="bcd22-179">methodName</span><span class="sxs-lookup"><span data-stu-id="bcd22-179">methodName</span></span>  

<!-- -->


### <a name="return-value---callstatic"></a><span data-ttu-id="bcd22-180">戻り値 - callStatic</span><span class="sxs-lookup"><span data-stu-id="bcd22-180">Return Value - callStatic</span></span>

<span data-ttu-id="bcd22-181">指定されたメソッドによって返される anytype データ型値です。</span><span class="sxs-lookup"><span data-stu-id="bcd22-181">An anytype data type value that is returned by the specified method.</span></span>

### <a name="remarks---callstatic"></a><span data-ttu-id="bcd22-182">備考 - callStatic</span><span class="sxs-lookup"><span data-stu-id="bcd22-182">Remarks - callStatic</span></span>

<span data-ttu-id="bcd22-183">callStatic メソッドに渡されるメソッドを含むクラスを使用して、DictClass クラスのオブジェクトのインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-183">You must create an instance of an object of the DictClass class by using a class that contains the method passed to the callStatic method.</span></span> <span data-ttu-id="bcd22-184">攻撃者が callStatic メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-184">If an attacker can control the input to the callStatic method, a security risk exists.</span></span> <span data-ttu-id="bcd22-185">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcd22-185">Therefore, this method runs under the code access security.</span></span> <span data-ttu-id="bcd22-186">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="bcd22-186">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="bcd22-187">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-187">Make sure that the user has development rights by setting the security key to the SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---callstatic"></a><span data-ttu-id="bcd22-188">例 - callStatic</span><span class="sxs-lookup"><span data-stu-id="bcd22-188">Examples - callStatic</span></span>

<span data-ttu-id="bcd22-189">この例では、Session クラスの AOSClientMode メソッドを呼び出し、呼び出しから返された値を出力します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-189">This example calls the AOSClientMode method in the Session class and then prints the value returned from the call.</span></span>

```xpp
static void Job_Example_DictClass_CallStatic(Args _args) 
{ 
    DictClass dictClass; 
    anytype   retVal; 
    str       resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictClass.callStatic method. 
    // DictClass.callStatic runs under code access security. 
    perm.assert(); 
    dictClass = new DictClass(classnum(Session)); 
    if (dictClass != null) 
    { 
        retVal       = dictClass.callStatic("AOSClientMode"); 
        resultOutput = strfmt( 
            "Return value of AOSClientMode is %1",  
            retVal); 
        print resultOutput; 
        pause; 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-extend"></a><span data-ttu-id="bcd22-190">メソッド extend</span><span class="sxs-lookup"><span data-stu-id="bcd22-190">Method extend</span></span>

<span data-ttu-id="bcd22-191">指定されたクラスが拡張されるクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-191">Provides the ID for the class that a specified class extends.</span></span>

```xpp
public ClassId extend()
```

### <a name="return-value---extend"></a><span data-ttu-id="bcd22-192">戻り値 - extend</span><span class="sxs-lookup"><span data-stu-id="bcd22-192">Return Value - extend</span></span>

<span data-ttu-id="bcd22-193">クラス ID を示す classID システムデータ型の値、クラスが別のクラスを拡張していない場合は 0。</span><span class="sxs-lookup"><span data-stu-id="bcd22-193">A value of the classID system data type that indicates the class ID; 0 if a class does not extend another class.</span></span>

## <a name="method-extendedby"></a><span data-ttu-id="bcd22-194">メソッド extendedBy</span><span class="sxs-lookup"><span data-stu-id="bcd22-194">Method extendedBy</span></span>

<span data-ttu-id="bcd22-195">指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-195">Provides a List object for the classes that extend a specified class.</span></span>

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a><span data-ttu-id="bcd22-196">パラメーター - extendedBy</span><span class="sxs-lookup"><span data-stu-id="bcd22-196">Parameters - extendedBy</span></span>

<span data-ttu-id="bcd22-197">allLevels</span><span class="sxs-lookup"><span data-stu-id="bcd22-197">allLevels</span></span>  

### <a name="return-value---extendedby"></a><span data-ttu-id="bcd22-198">戻り値 - extendedBy</span><span class="sxs-lookup"><span data-stu-id="bcd22-198">Return Value - extendedBy</span></span>

<span data-ttu-id="bcd22-199">クラスを拡張するクラスのリスト オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="bcd22-199">A List object for the classes that extend the class.</span></span>

## <a name="method-getallattributes"></a><span data-ttu-id="bcd22-200">メソッド getAllAttributes</span><span class="sxs-lookup"><span data-stu-id="bcd22-200">Method getAllAttributes</span></span>

<span data-ttu-id="bcd22-201">クラスの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-201">Retrieves the full set of attributes for the class.</span></span>

```xpp
public Array getAllAttributes()
```

### <a name="return-value---getallattributes"></a><span data-ttu-id="bcd22-202">戻り値 - getAllAttributes</span><span class="sxs-lookup"><span data-stu-id="bcd22-202">Return Value - getAllAttributes</span></span>

<span data-ttu-id="bcd22-203">クラスの SysAttribute オブジェクトの配列。</span><span class="sxs-lookup"><span data-stu-id="bcd22-203">The array of SysAttribute objects for the class.</span></span>

## <a name="method-getattribute"></a><span data-ttu-id="bcd22-204">メソッド getAttribute</span><span class="sxs-lookup"><span data-stu-id="bcd22-204">Method getAttribute</span></span>

<span data-ttu-id="bcd22-205">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-205">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span>

```xpp
public Object getAttribute(str attribute)
```

### <a name="parameters---getattribute"></a><span data-ttu-id="bcd22-206">パラメーター - getAttribute</span><span class="sxs-lookup"><span data-stu-id="bcd22-206">Parameters - getAttribute</span></span>

<span data-ttu-id="bcd22-207">属性</span><span class="sxs-lookup"><span data-stu-id="bcd22-207">attribute</span></span>  
<span data-ttu-id="bcd22-208">検索の対象である属性。</span><span class="sxs-lookup"><span data-stu-id="bcd22-208">The attribute for which to search.</span></span>

### <a name="return-value---getattribute"></a><span data-ttu-id="bcd22-209">戻り値 - getAttribute</span><span class="sxs-lookup"><span data-stu-id="bcd22-209">Return Value - getAttribute</span></span>

<span data-ttu-id="bcd22-210">オブジェクト クラスのインスタンスとしての属性。</span><span class="sxs-lookup"><span data-stu-id="bcd22-210">The attribute as an instance of the Object class.</span></span>

## <a name="method-getattributes"></a><span data-ttu-id="bcd22-211">メソッド getAttributes</span><span class="sxs-lookup"><span data-stu-id="bcd22-211">Method getAttributes</span></span>

```xpp
public Array getAttributes(str attribute)
```

### <a name="parameters---getattributes"></a><span data-ttu-id="bcd22-212">パラメーター - getAttributes</span><span class="sxs-lookup"><span data-stu-id="bcd22-212">Parameters - getAttributes</span></span>

<span data-ttu-id="bcd22-213">属性</span><span class="sxs-lookup"><span data-stu-id="bcd22-213">attribute</span></span>  

### <a name="return-value---getattributes"></a><span data-ttu-id="bcd22-214">戻り値 - getAttributes</span><span class="sxs-lookup"><span data-stu-id="bcd22-214">Return Value - getAttributes</span></span>

## <a name="method-id"></a><span data-ttu-id="bcd22-215">メソッド id</span><span class="sxs-lookup"><span data-stu-id="bcd22-215">Method id</span></span>

<span data-ttu-id="bcd22-216">指定されたクラスの ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-216">Provides the ID for a specified class.</span></span>

```xpp
public ClassId id()
```

### <a name="return-value---id"></a><span data-ttu-id="bcd22-217">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="bcd22-217">Return Value - id</span></span>

<span data-ttu-id="bcd22-218">クラス ID を示す classId システムデータ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-218">A value of the classId system data type that indicates the class ID.</span></span>

## <a name="method-implements"></a><span data-ttu-id="bcd22-219">メソッド implements</span><span class="sxs-lookup"><span data-stu-id="bcd22-219">Method implements</span></span>

<span data-ttu-id="bcd22-220">クラスが実装する指定されたインターフェイスの ID を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-220">Provides the ID for a specified interface that a class implements.</span></span>

```xpp
public ClassId implements(int no)
```

### <a name="parameters---implements"></a><span data-ttu-id="bcd22-221">パラメーター - implements</span><span class="sxs-lookup"><span data-stu-id="bcd22-221">Parameters - implements</span></span>

<span data-ttu-id="bcd22-222">no</span><span class="sxs-lookup"><span data-stu-id="bcd22-222">no</span></span>  
<span data-ttu-id="bcd22-223">クラス宣言内のインターフェイスの順序に基づいて、インターフェイスを指定する整数データ型。</span><span class="sxs-lookup"><span data-stu-id="bcd22-223">An integer data type that specifies the interface, based on the order of the interfaces in the class declaration.</span></span>

### <a name="return-value---implements"></a><span data-ttu-id="bcd22-224">戻り値 - implements</span><span class="sxs-lookup"><span data-stu-id="bcd22-224">Return Value - implements</span></span>

<span data-ttu-id="bcd22-225">クラス ID を示す classID システムデータ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-225">A value of the classID system data type that indicates the class ID.</span></span>

## <a name="method-implementscnt"></a><span data-ttu-id="bcd22-226">メソッド implementsCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-226">Method implementsCnt</span></span>

<span data-ttu-id="bcd22-227">クラスが実装するインターフェイスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-227">Indicates the number of interfaces that a class implements.</span></span>

```xpp
public int implementsCnt()
```

### <a name="return-value---implementscnt"></a><span data-ttu-id="bcd22-228">戻り値 - implementsCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-228">Return Value - implementsCnt</span></span>

<span data-ttu-id="bcd22-229">クラスが実装するインターフェイスの数の整数データ型値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-229">An integer data type value for the number of interfaces that a class implements.</span></span>

## <a name="method-isabstract"></a><span data-ttu-id="bcd22-230">メソッド isAbstract</span><span class="sxs-lookup"><span data-stu-id="bcd22-230">Method isAbstract</span></span>

<span data-ttu-id="bcd22-231">クラスが抽象であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-231">Indicates whether a class is abstract.</span></span>

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a><span data-ttu-id="bcd22-232">戻り値 - isAbstract</span><span class="sxs-lookup"><span data-stu-id="bcd22-232">Return Value - isAbstract</span></span>

<span data-ttu-id="bcd22-233">クラスが抽象である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="bcd22-233">true if the class is abstract; otherwise, false.</span></span>

## <a name="method-isfinal"></a><span data-ttu-id="bcd22-234">メソッド isFinal</span><span class="sxs-lookup"><span data-stu-id="bcd22-234">Method isFinal</span></span>

<span data-ttu-id="bcd22-235">クラスが最終であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-235">Indicates whether a class is final.</span></span>

```xpp
public boolean isFinal()
```

### <a name="return-value---isfinal"></a><span data-ttu-id="bcd22-236">戻り値 - isFinal</span><span class="sxs-lookup"><span data-stu-id="bcd22-236">Return Value - isFinal</span></span>

<span data-ttu-id="bcd22-237">クラスが最終である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="bcd22-237">true if the class is final; otherwise, false.</span></span>

## <a name="method-isinterface"></a><span data-ttu-id="bcd22-238">メソッド isInterface</span><span class="sxs-lookup"><span data-stu-id="bcd22-238">Method isInterface</span></span>

<span data-ttu-id="bcd22-239">オブジェクトがインターフェイスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-239">Indicates whether an object is an interface.</span></span>

```xpp
public boolean isInterface()
```

### <a name="return-value---isinterface"></a><span data-ttu-id="bcd22-240">戻り値 - isInterface</span><span class="sxs-lookup"><span data-stu-id="bcd22-240">Return Value - isInterface</span></span>

<span data-ttu-id="bcd22-241">オブジェクトがインターフェイスである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="bcd22-241">true if the object is an interface; otherwise, false.</span></span>

## <a name="method-iskernel"></a><span data-ttu-id="bcd22-242">メソッド isKernel</span><span class="sxs-lookup"><span data-stu-id="bcd22-242">Method isKernel</span></span>

<span data-ttu-id="bcd22-243">クラスがカーネル クラスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-243">Indicates whether a class is a kernel class.</span></span>

```xpp
public boolean isKernel()
```

### <a name="return-value---iskernel"></a><span data-ttu-id="bcd22-244">戻り値 - isKernel</span><span class="sxs-lookup"><span data-stu-id="bcd22-244">Return Value - isKernel</span></span>

<span data-ttu-id="bcd22-245">クラスがカーネル クラスの場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="bcd22-245">true if the class is a kernel class; otherwise, false.</span></span>

## <a name="method-isrunable"></a><span data-ttu-id="bcd22-246">メソッド isRunable</span><span class="sxs-lookup"><span data-stu-id="bcd22-246">Method isRunable</span></span>

<span data-ttu-id="bcd22-247">クラスを実行できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-247">Indicates whether a class can be run.</span></span>

```xpp
public boolean isRunable()
```

### <a name="return-value---isrunable"></a><span data-ttu-id="bcd22-248">戻り値 - isRunable</span><span class="sxs-lookup"><span data-stu-id="bcd22-248">Return Value - isRunable</span></span>

<span data-ttu-id="bcd22-249">クラスを実行することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="bcd22-249">true if the class can be run; otherwise, false.</span></span>

## <a name="method-makeobject"></a><span data-ttu-id="bcd22-250">メソッド makeObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-250">Method makeObject</span></span>

<span data-ttu-id="bcd22-251">オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-251">Creates an object.</span></span>

```xpp
public Object makeObject(VarArg )
```

### <a name="parameters---makeobject"></a><span data-ttu-id="bcd22-252">パラメーター - makeObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-252">Parameters - makeObject</span></span>


### <a name="return-value---makeobject"></a><span data-ttu-id="bcd22-253">戻り値 - makeObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-253">Return Value - makeObject</span></span>

<span data-ttu-id="bcd22-254">オブジェクト クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="bcd22-254">An instance of the Object class.</span></span>

### <a name="remarks---makeobject"></a><span data-ttu-id="bcd22-255">備考 - makeObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-255">Remarks - makeObject</span></span>

<span data-ttu-id="bcd22-256">オブジェクト クラスのインスタンスを DictClass::callObject メソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="bcd22-256">You can pass an instance of the Object class to the DictClass::callObject method.</span></span>

## <a name="method-name"></a><span data-ttu-id="bcd22-257">メソッド名</span><span class="sxs-lookup"><span data-stu-id="bcd22-257">Method name</span></span>

<span data-ttu-id="bcd22-258">クラスの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-258">Provides the name of a class.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="bcd22-259">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="bcd22-259">Return Value - name</span></span>

<span data-ttu-id="bcd22-260">クラス名の文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-260">A string data type value for the class name.</span></span>

## <a name="method-objectmethod"></a><span data-ttu-id="bcd22-261">メソッド objectMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-261">Method objectMethod</span></span>

<span data-ttu-id="bcd22-262">クラスの指定されたインスタンス メソッドの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-262">Provides the name of a specified instance method in a class.</span></span>

```xpp
public str objectMethod(int methodNumber)
```

### <a name="parameters---objectmethod"></a><span data-ttu-id="bcd22-263">パラメーター - objectMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-263">Parameters - objectMethod</span></span>

<span data-ttu-id="bcd22-264">methodNumber</span><span class="sxs-lookup"><span data-stu-id="bcd22-264">methodNumber</span></span>  
<span data-ttu-id="bcd22-265">メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。</span><span class="sxs-lookup"><span data-stu-id="bcd22-265">An integer data type that specifies a method in a class, based on the order of the methods.</span></span>

### <a name="return-value---objectmethod"></a><span data-ttu-id="bcd22-266">戻り値 - objectMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-266">Return Value - objectMethod</span></span>

<span data-ttu-id="bcd22-267">メソッド名の文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-267">A string data type value for the method name.</span></span>

### <a name="remarks---objectmethod"></a><span data-ttu-id="bcd22-268">備考 - objectMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-268">Remarks - objectMethod</span></span>

<span data-ttu-id="bcd22-269">\_methodNumber パラメーターは 1 から始まります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-269">The \_methodNumber parameter starts counting at 1.</span></span>

## <a name="method-objectmethodcnt"></a><span data-ttu-id="bcd22-270">メソッド objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-270">Method objectMethodCnt</span></span>

<span data-ttu-id="bcd22-271">クラスのインスタンス メソッドの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-271">Indicates the number of instance methods in a class.</span></span>

```xpp
public int objectMethodCnt()
```

### <a name="return-value---objectmethodcnt"></a><span data-ttu-id="bcd22-272">戻り値 - objectMethodCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-272">Return Value - objectMethodCnt</span></span>

<span data-ttu-id="bcd22-273">クラス内のインスタンス メソッドの数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-273">An integer value that indicates the number of instance methods in a class.</span></span>

## <a name="method-objectmethodobject"></a><span data-ttu-id="bcd22-274">メソッド objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-274">Method objectMethodObject</span></span>

<span data-ttu-id="bcd22-275">DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-275">Provides information about a specified instance method in a class by returning a DictMethod object.</span></span>

```xpp
public DictMethod objectMethodObject(int methodNumber)
```

### <a name="parameters---objectmethodobject"></a><span data-ttu-id="bcd22-276">パラメーター - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-276">Parameters - objectMethodObject</span></span>

<span data-ttu-id="bcd22-277">methodNumber</span><span class="sxs-lookup"><span data-stu-id="bcd22-277">methodNumber</span></span>  
<span data-ttu-id="bcd22-278">メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。</span><span class="sxs-lookup"><span data-stu-id="bcd22-278">An integer data type that specifies a method in a class, based on the order of the methods.</span></span> <span data-ttu-id="bcd22-279">番号付けは 1 から開始します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-279">Numbering starts at 1.</span></span>

### <a name="return-value---objectmethodobject"></a><span data-ttu-id="bcd22-280">戻り値 - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-280">Return Value - objectMethodObject</span></span>

<span data-ttu-id="bcd22-281">クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="bcd22-281">A DictMethod object that contains information about a specified method in a class.</span></span>

### <a name="remarks---objectmethodobject"></a><span data-ttu-id="bcd22-282">備考 - objectMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-282">Remarks - objectMethodObject</span></span>

<span data-ttu-id="bcd22-283">\_methodNumber パラメーターは 1 から始まります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-283">The \_methodNumber parameter starts counting at 1.</span></span>

## <a name="method-runmode"></a><span data-ttu-id="bcd22-284">メソッド RunMode</span><span class="sxs-lookup"><span data-stu-id="bcd22-284">Method RunMode</span></span>

<span data-ttu-id="bcd22-285">クラスが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-285">Specifies where a class is executed.</span></span>

```xpp
public ClassRunMode RunMode()
```

### <a name="return-value---runmode"></a><span data-ttu-id="bcd22-286">戻り値 - RunMode</span><span class="sxs-lookup"><span data-stu-id="bcd22-286">Return Value - RunMode</span></span>

<span data-ttu-id="bcd22-287">クラスが実行される場所を示す ClassRunMode システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-287">A ClassRunMode system enumeration value that indicates where a class is executed.</span></span>

### <a name="remarks---runmode"></a><span data-ttu-id="bcd22-288">備考 - RunMode</span><span class="sxs-lookup"><span data-stu-id="bcd22-288">Remarks - RunMode</span></span>

<span data-ttu-id="bcd22-289">可能な戻り値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bcd22-289">The following are the possible return values:</span></span>

-   <span data-ttu-id="bcd22-290">呼び出された値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-290">The Called value.</span></span>
-   <span data-ttu-id="bcd22-291">Client 値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-291">The Client value.</span></span>
-   <span data-ttu-id="bcd22-292">ClientorServer 値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-292">The ClientorServer value.</span></span>
-   <span data-ttu-id="bcd22-293">サーバーの値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-293">The Server value.</span></span>

## <a name="method-staticmethod"></a><span data-ttu-id="bcd22-294">メソッド staticMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-294">Method staticMethod</span></span>

<span data-ttu-id="bcd22-295">クラスの指定された静的メソッドの名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-295">Provides the name of a specified static method in a class.</span></span>

```xpp
public str staticMethod(int methodNumber)
```

### <a name="parameters---staticmethod"></a><span data-ttu-id="bcd22-296">パラメーター - staticMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-296">Parameters - staticMethod</span></span>

<span data-ttu-id="bcd22-297">methodNumber</span><span class="sxs-lookup"><span data-stu-id="bcd22-297">methodNumber</span></span>  
<span data-ttu-id="bcd22-298">メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。</span><span class="sxs-lookup"><span data-stu-id="bcd22-298">An integer data type that specifies a method in a class, based on the order of the methods.</span></span>

### <a name="return-value---staticmethod"></a><span data-ttu-id="bcd22-299">戻り値 - staticMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-299">Return Value - staticMethod</span></span>

<span data-ttu-id="bcd22-300">メソッド名の文字列データ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-300">A string data type value for the method name.</span></span>

### <a name="remarks---staticmethod"></a><span data-ttu-id="bcd22-301">備考 - staticMethod</span><span class="sxs-lookup"><span data-stu-id="bcd22-301">Remarks - staticMethod</span></span>

<span data-ttu-id="bcd22-302">\_methodNumber パラメーターは 1 から始まります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-302">The \_methodNumber parameter starts counting at 1.</span></span>

## <a name="method-staticmethodcnt"></a><span data-ttu-id="bcd22-303">メソッド staticMethodCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-303">Method staticMethodCnt</span></span>

<span data-ttu-id="bcd22-304">クラスの静的メソッドの数を示します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-304">Indicates the number of static methods in a class.</span></span>

```xpp
public int staticMethodCnt()
```

### <a name="return-value---staticmethodcnt"></a><span data-ttu-id="bcd22-305">戻り値 - staticMethodCnt</span><span class="sxs-lookup"><span data-stu-id="bcd22-305">Return Value - staticMethodCnt</span></span>

<span data-ttu-id="bcd22-306">クラスの静的メソッドの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="bcd22-306">An integer that indicates the number of static methods in a class.</span></span>

## <a name="method-staticmethodobject"></a><span data-ttu-id="bcd22-307">メソッド staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-307">Method staticMethodObject</span></span>

<span data-ttu-id="bcd22-308">DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-308">Provides information about a specified static method in a class by returning a DictMethod object.</span></span>

```xpp
public DictMethod staticMethodObject(int methodNumber)
```

### <a name="parameters---staticmethodobject"></a><span data-ttu-id="bcd22-309">パラメーター - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-309">Parameters - staticMethodObject</span></span>

<span data-ttu-id="bcd22-310">methodNumber</span><span class="sxs-lookup"><span data-stu-id="bcd22-310">methodNumber</span></span>  
<span data-ttu-id="bcd22-311">メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。</span><span class="sxs-lookup"><span data-stu-id="bcd22-311">An integer data type that specifies a method in a class, based on the order of the methods.</span></span>

### <a name="return-value---staticmethodobject"></a><span data-ttu-id="bcd22-312">戻り値 - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-312">Return Value - staticMethodObject</span></span>

<span data-ttu-id="bcd22-313">クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="bcd22-313">A DictMethod object that contains information about a specified method in a class.</span></span>

### <a name="remarks---staticmethodobject"></a><span data-ttu-id="bcd22-314">備考 - staticMethodObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-314">Remarks - staticMethodObject</span></span>

<span data-ttu-id="bcd22-315">\_methodNumber パラメーターは 1 から始まります。</span><span class="sxs-lookup"><span data-stu-id="bcd22-315">The \_methodNumber parameter starts counting at 1.</span></span>

## <a name="method-getattributedclasses"></a><span data-ttu-id="bcd22-316">メソッド getAttributedClasses</span><span class="sxs-lookup"><span data-stu-id="bcd22-316">Method getAttributedClasses</span></span>

```xpp
public static Array getAttributedClasses(str attribute)
```

### <a name="parameters---getattributedclasses"></a><span data-ttu-id="bcd22-317">パラメーター - getAttributedClasses</span><span class="sxs-lookup"><span data-stu-id="bcd22-317">Parameters - getAttributedClasses</span></span>

<span data-ttu-id="bcd22-318">属性</span><span class="sxs-lookup"><span data-stu-id="bcd22-318">attribute</span></span>  

### <a name="return-value---getattributedclasses"></a><span data-ttu-id="bcd22-319">戻り値 - getAttributedClasses</span><span class="sxs-lookup"><span data-stu-id="bcd22-319">Return Value - getAttributedClasses</span></span>

## <a name="method-createobject"></a><span data-ttu-id="bcd22-320">メソッド createObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-320">Method createObject</span></span>

```xpp
public static Object createObject(str className, VarArg )
```

### <a name="parameters---createobject"></a><span data-ttu-id="bcd22-321">パラメーター - createObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-321">Parameters - createObject</span></span>

<span data-ttu-id="bcd22-322">className</span><span class="sxs-lookup"><span data-stu-id="bcd22-322">className</span></span>  

<!-- -->


### <a name="return-value---createobject"></a><span data-ttu-id="bcd22-323">戻り値 - createObject</span><span class="sxs-lookup"><span data-stu-id="bcd22-323">Return Value - createObject</span></span>

## <a name="method-new"></a><span data-ttu-id="bcd22-324">メソッド new</span><span class="sxs-lookup"><span data-stu-id="bcd22-324">Method new</span></span>

<span data-ttu-id="bcd22-325">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bcd22-325">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(ClassId classId)
```

### <a name="parameters---new"></a><span data-ttu-id="bcd22-326">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="bcd22-326">Parameters - new</span></span>

<span data-ttu-id="bcd22-327">classId</span><span class="sxs-lookup"><span data-stu-id="bcd22-327">classId</span></span>  
<span data-ttu-id="bcd22-328">クラスのシステム ID を示す classId システムデータ型の値。</span><span class="sxs-lookup"><span data-stu-id="bcd22-328">A value of the classId system data type that indicates the system ID of a class.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="bcd22-329">備考 - new</span><span class="sxs-lookup"><span data-stu-id="bcd22-329">Remarks - new</span></span>

<span data-ttu-id="bcd22-330">クラス ID は符号なし整数なので、常に 0 から 65535 の範囲です。</span><span class="sxs-lookup"><span data-stu-id="bcd22-330">Class IDs are unsigned integers and are therefore always in the range 0 to 65535.</span></span> <span data-ttu-id="bcd22-331">無効なクラス ID が渡された場合は、このメソッドは失敗しません。</span><span class="sxs-lookup"><span data-stu-id="bcd22-331">The method does not fail if an invalid class ID is passed.</span></span> <span data-ttu-id="bcd22-332">ClassNum 組み込み関数を使用して、クラス ID の代わりにクラス名をメソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="bcd22-332">You can pass a class name to the method instead of a class ID by using the classNum intrinsic function.</span></span> <span data-ttu-id="bcd22-333">詳細については、「組み込み関数」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bcd22-333">For more information, see �Intrinsic Functions.�</span></span>

