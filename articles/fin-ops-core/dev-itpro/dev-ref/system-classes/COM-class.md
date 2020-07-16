---
title: COM クラス
description: このトピックでは、COM クラスについて説明します。
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
ms.openlocfilehash: 361cdc27fcc0da6dd605381b45a14500760bee13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502715"
---
# <a name="class-com"></a><span data-ttu-id="ab121-103">クラス COM</span><span class="sxs-lookup"><span data-stu-id="ab121-103">Class COM</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class COM
```

<span data-ttu-id="ab121-104">COM クラスは、コンポーネント オブジェクト モデル (COM) オブジェクトを作成するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-104">The COM class is used to create Component Object Model (COM) objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab121-105">備考</span><span class="sxs-lookup"><span data-stu-id="ab121-105">Remarks</span></span>

<span data-ttu-id="ab121-106">COM クラスは、分散コンポーネント オブジェクト モデル (DCOM) もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab121-106">The COM class also supports Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="ab121-107">DCOM は、DCOM をサポートするオブジェクトをリモート コンピュータで実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ab121-107">DCOM enables objects that support DCOM to run on remote computers.</span></span> <span data-ttu-id="ab121-108">COM クラスを使用して COM オブジェクトがインスタンス化されると、そのメソッドおよびプロパティに、COMDispFunction クラスかまたは COM クラスの 拡張構文を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ab121-108">When a COM object has been instantiated by using the COM class, its methods and properties can be accessed by using either the COMDispFunction class or the extended syntax for the COM class.</span></span> <span data-ttu-id="ab121-109">拡張構文を使用すると、Lookup リストに表示されていなくても 、メソッドとプロパティを COM オブジェクトで直接呼び出すことができます (例: com.comMethod("Hello World");)。</span><span class="sxs-lookup"><span data-stu-id="ab121-109">The extended syntax enables methods and properties to be directly called on the COM object, even though they don't appear in the Lookup list (for example, com.comMethod("Hello World");).</span></span> <span data-ttu-id="ab121-110">拡張構文は、任意の数の引数を取るメソッドとプロパティへの呼び出しをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ab121-110">The extended syntax supports calls to methods and properties that take any number of arguments.</span></span> <span data-ttu-id="ab121-111">一部の COM オブジェクトは、省略可能な引数の概念をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab121-111">Some COM objects support the concept of optional arguments.</span></span> <span data-ttu-id="ab121-112">オプションのバリアント引数のみ省略できます。</span><span class="sxs-lookup"><span data-stu-id="ab121-112">Only optional variant arguments can be omitted.</span></span> <span data-ttu-id="ab121-113">オプションの引数を省略すると、COM オブジェクトは、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab121-113">If optional arguments are omitted, the COM object uses its default values.</span></span> <span data-ttu-id="ab121-114">COM オブジェクトの引数を省略し、強制的に既定値を使用するには、次の例に示すように、COMArgument::NoValue 列挙型を指定します。</span><span class="sxs-lookup"><span data-stu-id="ab121-114">To omit an argument for the COM object and force it to use its default value, specify the COMArgument::NoValue enumeration, as shown in the following example.</span></span>

```xpp
com.comMethod(COMArgument::NoValue, "Hello Another World");
```


<span data-ttu-id="ab121-115">COM オブジェクトから省略する引数が引数リストの最後に表示される場合は、コードから省略します。</span><span class="sxs-lookup"><span data-stu-id="ab121-115">If the arguments to omit from the COM object appear at the end of the argument list, omit them from the code.</span></span> <span data-ttu-id="ab121-116">COM クラスの引数型と戻り値型の拡張構文では、次の型がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ab121-116">The following types are supported for the extended syntax for the COM class argument type and return type:</span></span>

-   <span data-ttu-id="ab121-117">array</span><span class="sxs-lookup"><span data-stu-id="ab121-117">array</span></span>
-   <span data-ttu-id="ab121-118">COM</span><span class="sxs-lookup"><span data-stu-id="ab121-118">COM</span></span>
-   <span data-ttu-id="ab121-119">COMVariant</span><span class="sxs-lookup"><span data-stu-id="ab121-119">COMVariant</span></span>
-   <span data-ttu-id="ab121-120">日付</span><span class="sxs-lookup"><span data-stu-id="ab121-120">date</span></span>
-   <span data-ttu-id="ab121-121">列挙型</span><span class="sxs-lookup"><span data-stu-id="ab121-121">enum</span></span>
-   <span data-ttu-id="ab121-122">int</span><span class="sxs-lookup"><span data-stu-id="ab121-122">int</span></span>
-   <span data-ttu-id="ab121-123">real</span><span class="sxs-lookup"><span data-stu-id="ab121-123">real</span></span>
-   <span data-ttu-id="ab121-124">str</span><span class="sxs-lookup"><span data-stu-id="ab121-124">str</span></span>

<span data-ttu-id="ab121-125">COM オブジェクトが日付を返し、拡張構文が使用されている場合は、COM メソッドの戻り値を COM Variant クラス変数に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-125">If a COM object returns a date, and if the extended syntax is used, the return value of the COM method should be assigned to a COMVariant class variable.</span></span> <span data-ttu-id="ab121-126">そして、日付と時刻のプロパティを使用して、COMVariant クラスから実際の日時 (形式) を抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="ab121-126">The actual date and time (format) can then be extracted from the COMVariant class by using the date and time properties.</span></span> <span data-ttu-id="ab121-127">日付の戻り値に COMVariant クラスではなく日付変数が割り当てられている場合、日付の時間の部分は失われます。</span><span class="sxs-lookup"><span data-stu-id="ab121-127">If the date return value is assigned to a date variable instead of a COMVariant class, the time component of the date is lost.</span></span> <span data-ttu-id="ab121-128">拡張構文を使用するときは、オブジェクトに対して COM クラス メソッド (ルックアップ リストに表示されるメソッド) をまだ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ab121-128">When the extended syntax is used, you can still call the COM class methods (the methods that appear in the Lookup list) on the objects.</span></span> <span data-ttu-id="ab121-129">COM クラス メソッドは、実際の COM オブジェクトでのメソッドよりも優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="ab121-129">The COM class methods have a higher priority than the methods on the actual COM object.</span></span> <span data-ttu-id="ab121-130">COM オブジェクトのメソッドが COM クラスのメソッドと同じ名前 (たとえば、attach) である場合、そのメソッドを COM オブジェクトで呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="ab121-130">If a method on the COM object has the same name as a method on the COM class (for example, attach), you cannot call that method on the COM object.</span></span> <span data-ttu-id="ab121-131">COM クラスで同じ名前を持つメソッドを呼び出すのではなく、COM オブジェクトのメソッドを呼び出せるようにするには、重複するメソッド名の先頭にアンダースコアを付けます (たとえば、com.\_detach();)。</span><span class="sxs-lookup"><span data-stu-id="ab121-131">To be able to call the method on the COM object instead of the method that has the same name on the COM class, prefix the duplicate method name with an underscore (for example, com.\_detach();).</span></span> <span data-ttu-id="ab121-132">COM クラスの拡張構文は、コンパイル時ではなく実行時に評価され、パフォーマンスがわずかに低下します。</span><span class="sxs-lookup"><span data-stu-id="ab121-132">The extended syntax for the COM class is evaluated at run time, not compile time, which causes a slight decrease in performance.</span></span> <span data-ttu-id="ab121-133">パフォーマンスの高いコードが必要な場合は、COMDispFunction クラスを使用することを検討します。</span><span class="sxs-lookup"><span data-stu-id="ab121-133">If high-performance code is required, consider using the COMDispFunction class.</span></span> <span data-ttu-id="ab121-134">このクラスは、COM クラスの拡張構文よりもパフォーマンスが向上しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-134">This class offers performance improvements over the extended syntax for the COM class.</span></span>

## <a name="examples"></a><span data-ttu-id="ab121-135">例</span><span class="sxs-lookup"><span data-stu-id="ab121-135">Examples</span></span>

<span data-ttu-id="ab121-136">この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ab121-136">This example calls the GetFileName method from the Scripting.FileSystemObject COM object.</span></span>

```xpp
void COMExample() 
{ 
    COM               com; 
    str               result; 
    InteropPermission perm; 
    ; 
```

```xpp
    // Set code access permission to help protect the use of the 
    // COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    // Permission scope starts here. 
    perm.assert(); 
```

```xpp
    com = new COM("Scripting.FileSystemObject"); 
    if (com != null) 
    { 
        result = com.GetFileName(@"c:\boot.ini"); 
    } 
```

```xpp
    // Close code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="ab121-137">メソッド</span><span class="sxs-lookup"><span data-stu-id="ab121-137">Methods</span></span>

| <span data-ttu-id="ab121-138">方法</span><span class="sxs-lookup"><span data-stu-id="ab121-138">Method</span></span>                                                                                                      | <span data-ttu-id="ab121-139">説明</span><span class="sxs-lookup"><span data-stu-id="ab121-139">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab121-140">public AnyType dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="ab121-140">public AnyType dispatch(VarArg )</span></span>                                                                            | <span data-ttu-id="ab121-141">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ab121-141">Reserved.</span></span> <span data-ttu-id="ab121-142">メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="ab121-142">Do not explicitly call this method.</span></span>                                                                                                |
| <span data-ttu-id="ab121-143">public str documentationName()</span><span class="sxs-lookup"><span data-stu-id="ab121-143">public str documentationName()</span></span>                                                                              | <span data-ttu-id="ab121-144">COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-144">Returns the textual name of the COM object that is associated with the instance of the COM class.</span></span>                                            |
| <span data-ttu-id="ab121-145">public COMError error()</span><span class="sxs-lookup"><span data-stu-id="ab121-145">public COMError error()</span></span>                                                                                     | <span data-ttu-id="ab121-146">COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-146">Returns a COMError object that is associated with the instance of the COM class.</span></span>                                                             |
| <span data-ttu-id="ab121-147">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="ab121-147">public ComInterface interface()</span></span>                                                                             | <span data-ttu-id="ab121-148">COM オブジェクトに関連付けられているインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-148">Returns the interface that is associated with the COM object.</span></span>                                                                                |
| <span data-ttu-id="ab121-149">public int lcid(\[int lcid\])</span><span class="sxs-lookup"><span data-stu-id="ab121-149">public int lcid(\[int lcid\])</span></span>                                                                               |                                                                                                                                              |
| <span data-ttu-id="ab121-150">public str toString()</span><span class="sxs-lookup"><span data-stu-id="ab121-150">public str toString()</span></span>                                                                                       | <span data-ttu-id="ab121-151">COM クラスのインスタンスを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-151">Returns a string that represents the instance of the COM class.</span></span>                                                                              |
| <span data-ttu-id="ab121-152">::public static COM createFromInterface(ComInterface interface)</span><span class="sxs-lookup"><span data-stu-id="ab121-152">::public static COM createFromInterface(ComInterface interface)</span></span>                                             | <span data-ttu-id="ab121-153">指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-153">Creates an instance of the COM class by using the specified COM interface.</span></span>                                                                   |
| <span data-ttu-id="ab121-154">::public static COM createFromObject(COM object)</span><span class="sxs-lookup"><span data-stu-id="ab121-154">::public static COM createFromObject(COM object)</span></span>                                                            | <span data-ttu-id="ab121-155">指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-155">Creates an instance of the COM class by using the specified COM object.</span></span>                                                                      |
| <span data-ttu-id="ab121-156">::public static COM createFromVariant(COMVariant variant)</span><span class="sxs-lookup"><span data-stu-id="ab121-156">::public static COM createFromVariant(COMVariant variant)</span></span>                                                   | <span data-ttu-id="ab121-157">COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-157">Creates an instance of the COM class by using the specified instance of the COMVariant class.</span></span>                                                |
| <span data-ttu-id="ab121-158">::public static COM getObject(str className)</span><span class="sxs-lookup"><span data-stu-id="ab121-158">::public static COM getObject(str className)</span></span>                                                                | <span data-ttu-id="ab121-159">実行している COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-159">Returns an instance of a COM object that is running.</span></span>                                                                                         |
| <span data-ttu-id="ab121-160">::public static COM getObjectEx(str fileName)</span><span class="sxs-lookup"><span data-stu-id="ab121-160">::public static COM getObjectEx(str fileName)</span></span>                                                               | <span data-ttu-id="ab121-161">ファイル名で指定されている COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-161">Returns an instance of a COM object that is specified by its file name.</span></span>                                                                      |
| <span data-ttu-id="ab121-162">::public static AnyType unsupported(int action, \[AnyType param1\], \[AnyType param2\], \[AnyType param3\])</span><span class="sxs-lookup"><span data-stu-id="ab121-162">::public static AnyType unsupported(int action, \[AnyType param1\], \[AnyType param2\], \[AnyType param3\])</span></span> | <span data-ttu-id="ab121-163">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ab121-163">Reserved.</span></span>                                                                                                                                    |
| <span data-ttu-id="ab121-164">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ab121-164">public void finalize()</span></span>                                                                                      | <span data-ttu-id="ab121-165">COM クラスのインスタンスに関連付けられているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="ab121-165">Frees resources that are associated with the instance of the COM class.</span></span>                                                                      |
| <span data-ttu-id="ab121-166">public void new(\[str className\], \[str computerName\])</span><span class="sxs-lookup"><span data-stu-id="ab121-166">public void new(\[str className\], \[str computerName\])</span></span>                                                    | <span data-ttu-id="ab121-167">COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="ab121-167">Creates an instance of the COM class that can be attached to the COM class and optionally instantiates a COM object on a specified computer.</span></span> |
| <span data-ttu-id="ab121-168">public void attach(ComInterface interface)</span><span class="sxs-lookup"><span data-stu-id="ab121-168">public void attach(ComInterface interface)</span></span>                                                                  | <span data-ttu-id="ab121-169">COM クラスのインスタンスを COM インターフェイスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ab121-169">Attaches an instance of the COM class to a COM interface.</span></span>                                                                                    |
| <span data-ttu-id="ab121-170">public void detach()</span><span class="sxs-lookup"><span data-stu-id="ab121-170">public void detach()</span></span>                                                                                        | <span data-ttu-id="ab121-171">関連付けられているクラスから COM オブジェクトを解除します。</span><span class="sxs-lookup"><span data-stu-id="ab121-171">Detaches a COM object from the class that it was associated with.</span></span>                                                                            |

## <a name="method-dispatch"></a><span data-ttu-id="ab121-172">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="ab121-172">Method dispatch</span></span>

<span data-ttu-id="ab121-173">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ab121-173">Reserved.</span></span> <span data-ttu-id="ab121-174">メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="ab121-174">Do not explicitly call this method.</span></span>

```xpp
public AnyType dispatch(VarArg )
```

### <a name="parameters---dispatch"></a><span data-ttu-id="ab121-175">パラメーター - dispatch</span><span class="sxs-lookup"><span data-stu-id="ab121-175">Parameters - dispatch</span></span>


### <a name="return-value---dispatch"></a><span data-ttu-id="ab121-176">戻り値 - dispatch</span><span class="sxs-lookup"><span data-stu-id="ab121-176">Return Value - dispatch</span></span>

## <a name="method-documentationname"></a><span data-ttu-id="ab121-177">メソッド documentationName</span><span class="sxs-lookup"><span data-stu-id="ab121-177">Method documentationName</span></span>

<span data-ttu-id="ab121-178">COM クラスのインスタンスに関連付けられている COM オブジェクトの名前を表すテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-178">Returns the textual name of the COM object that is associated with the instance of the COM class.</span></span>

```xpp
public str documentationName()
```

### <a name="return-value---documentationname"></a><span data-ttu-id="ab121-179">戻り値 - documentationName</span><span class="sxs-lookup"><span data-stu-id="ab121-179">Return Value - documentationName</span></span>

<span data-ttu-id="ab121-180">COM クラスのインスタンスに関連付けられている COM オブジェクトのテキスト名。COM オブジェクトのドキュメント名がない場合は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ab121-180">The textual name of the COM object that is associated with the instance of the COM class; an empty string if there is no documentation name for the COM object.</span></span>

### <a name="remarks---documentationname"></a><span data-ttu-id="ab121-181">備考 - documentationName</span><span class="sxs-lookup"><span data-stu-id="ab121-181">Remarks - documentationName</span></span>

<span data-ttu-id="ab121-182">クラスのテキスト名は、そのクラスを記述するためにクラスによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-182">The textual name of a class is used by the class to describe itself.</span></span> <span data-ttu-id="ab121-183">テキスト名は、クラスをインスタンス化するために使用されるクラス名とは異なります。</span><span class="sxs-lookup"><span data-stu-id="ab121-183">The textual name differs from the class name that is used to instantiate the class.</span></span>

### <a name="examples---documentationname"></a><span data-ttu-id="ab121-184">例 - documentationName</span><span class="sxs-lookup"><span data-stu-id="ab121-184">Examples - documentationName</span></span>

<span data-ttu-id="ab121-185">次の例は、COM オブジェクトのドキュメント名を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-185">The following example shows how to retrieve the documentation name for a COM object.</span></span>

```xpp
str docName; 
; 
// The obj that was previously instantiated. 
docName = obj.documentationName(); 
info(strfmt("documentationName: %1", docName));
```

## <a name="method-error"></a><span data-ttu-id="ab121-186">メソッド error</span><span class="sxs-lookup"><span data-stu-id="ab121-186">Method error</span></span>

<span data-ttu-id="ab121-187">COM クラスのインスタンスに関連付けられている COMError オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-187">Returns a COMError object that is associated with the instance of the COM class.</span></span>

```xpp
public COMError error()
```

### <a name="return-value---error"></a><span data-ttu-id="ab121-188">戻り値 - error</span><span class="sxs-lookup"><span data-stu-id="ab121-188">Return Value - error</span></span>

<span data-ttu-id="ab121-189">COM クラスのインスタンスに関連付けられているエラーを表す COMError 値。</span><span class="sxs-lookup"><span data-stu-id="ab121-189">A COMError value that represents the error that is associated with the instance of the COM class.</span></span>

### <a name="examples---error"></a><span data-ttu-id="ab121-190">例 - error</span><span class="sxs-lookup"><span data-stu-id="ab121-190">Examples - error</span></span>

<span data-ttu-id="ab121-191">次の例は、COM クラスのインスタンスに関連付けられているエラー オブジェクトを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-191">The following example shows how to retrieve the error object that is associated with an instance of the COM class.</span></span>

```xpp
COMError err; 
```

```xpp
// The obj variable was previously instantiated. 
err = obj.error(); 
```

```xpp
// Output the error number. 
info(strfmt("Error: %1", err.number()))
```

## <a name="method-interface"></a><span data-ttu-id="ab121-192">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="ab121-192">Method interface</span></span>

<span data-ttu-id="ab121-193">COM オブジェクトに関連付けられているインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-193">Returns the interface that is associated with the COM object.</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="ab121-194">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="ab121-194">Return Value - interface</span></span>

<span data-ttu-id="ab121-195">COM オブジェクトに関連付けられているインターフェイス。インターフェイスが COM オブジェクトに関連付けられていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="ab121-195">The interface that is associated with the COM object; 0 (zero) if no interface is associated with the COM object.</span></span>

### <a name="examples---interface"></a><span data-ttu-id="ab121-196">例 - interface</span><span class="sxs-lookup"><span data-stu-id="ab121-196">Examples - interface</span></span>

<span data-ttu-id="ab121-197">次の例は、COM オブジェクトに関連付けられているインターフェイスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-197">The following example shows how to retrieve the interface that is associated with a COM object.</span></span>

```xpp
// The obj variable was previously instantiated. 
info(strfmt("Interface: %1", obj.interface()));
```

## <a name="method-lcid"></a><span data-ttu-id="ab121-198">メソッド lcid</span><span class="sxs-lookup"><span data-stu-id="ab121-198">Method lcid</span></span>

```xpp
public int lcid([int lcid])
```

### <a name="parameters---lcid"></a><span data-ttu-id="ab121-199">パラメーター - lcid</span><span class="sxs-lookup"><span data-stu-id="ab121-199">Parameters - lcid</span></span>

<span data-ttu-id="ab121-200">lcid</span><span class="sxs-lookup"><span data-stu-id="ab121-200">lcid</span></span>  

### <a name="return-value---lcid"></a><span data-ttu-id="ab121-201">戻り値 - lcid</span><span class="sxs-lookup"><span data-stu-id="ab121-201">Return Value - lcid</span></span>

## <a name="method-tostring"></a><span data-ttu-id="ab121-202">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="ab121-202">Method toString</span></span>

<span data-ttu-id="ab121-203">COM クラスのインスタンスを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-203">Returns a string that represents the instance of the COM class.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="ab121-204">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="ab121-204">Return Value - toString</span></span>

<span data-ttu-id="ab121-205">COM クラスのインスタンスの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="ab121-205">A string that contains a description of the instance of the COM class.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="ab121-206">例 - toString</span><span class="sxs-lookup"><span data-stu-id="ab121-206">Examples - toString</span></span>

<span data-ttu-id="ab121-207">次の例は、toString メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-207">The following example shows how to use the toString method.</span></span>

```xpp
print objCOM.toString();
```

## <a name="method-createfrominterface"></a><span data-ttu-id="ab121-208">メソッド createFromInterface</span><span class="sxs-lookup"><span data-stu-id="ab121-208">Method createFromInterface</span></span>

<span data-ttu-id="ab121-209">指定された COM インターフェイスを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-209">Creates an instance of the COM class by using the specified COM interface.</span></span>

```xpp
public static COM createFromInterface(ComInterface interface)
```

### <a name="parameters---createfrominterface"></a><span data-ttu-id="ab121-210">パラメーター - createFromInterface</span><span class="sxs-lookup"><span data-stu-id="ab121-210">Parameters - createFromInterface</span></span>

<span data-ttu-id="ab121-211">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ab121-211">interface</span></span>  
<span data-ttu-id="ab121-212">COM クラスの新しいインスタンスを作成するために使用するインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="ab121-212">The interface to use to create the new instance of the COM class.</span></span>

### <a name="return-value---createfrominterface"></a><span data-ttu-id="ab121-213">戻り値 - createFromInterface</span><span class="sxs-lookup"><span data-stu-id="ab121-213">Return Value - createFromInterface</span></span>

<span data-ttu-id="ab121-214">インターフェイス パラメーターで指定される COM インターフェイスの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="ab121-214">An instance of the COM class for the COM interface that is specified by the interface parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

### <a name="remarks---createfrominterface"></a><span data-ttu-id="ab121-215">備考 - createFromInterface</span><span class="sxs-lookup"><span data-stu-id="ab121-215">Remarks - createFromInterface</span></span>

<span data-ttu-id="ab121-216">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab121-216">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

## <a name="method-createfromobject"></a><span data-ttu-id="ab121-217">メソッド createFromObject</span><span class="sxs-lookup"><span data-stu-id="ab121-217">Method createFromObject</span></span>

<span data-ttu-id="ab121-218">指定された COM オブジェクトを使用して COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-218">Creates an instance of the COM class by using the specified COM object.</span></span>

```xpp
public static COM createFromObject(COM object)
```

### <a name="parameters---createfromobject"></a><span data-ttu-id="ab121-219">パラメーター - createFromObject</span><span class="sxs-lookup"><span data-stu-id="ab121-219">Parameters - createFromObject</span></span>

<span data-ttu-id="ab121-220">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ab121-220">object</span></span>  
<span data-ttu-id="ab121-221">COM クラスの新しいインスタンスを作成するために使用する COM クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="ab121-221">The instance of the COM class to use to create the new instance of the COM class.</span></span>

### <a name="return-value---createfromobject"></a><span data-ttu-id="ab121-222">戻り値 - createFromObject</span><span class="sxs-lookup"><span data-stu-id="ab121-222">Return Value - createFromObject</span></span>

<span data-ttu-id="ab121-223">オブジェクト パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="ab121-223">An instance of the COM class for the COM object that is specified by the object parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

### <a name="remarks---createfromobject"></a><span data-ttu-id="ab121-224">備考 - createFromObject</span><span class="sxs-lookup"><span data-stu-id="ab121-224">Remarks - createFromObject</span></span>

<span data-ttu-id="ab121-225">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab121-225">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

## <a name="method-createfromvariant"></a><span data-ttu-id="ab121-226">メソッド createFromVariant</span><span class="sxs-lookup"><span data-stu-id="ab121-226">Method createFromVariant</span></span>

<span data-ttu-id="ab121-227">COMVariant クラスの指定されたインスタンスを使用して、COM クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab121-227">Creates an instance of the COM class by using the specified instance of the COMVariant class.</span></span>

```xpp
public static COM createFromVariant(COMVariant variant)
```

### <a name="parameters---createfromvariant"></a><span data-ttu-id="ab121-228">パラメーター - createFromVariant</span><span class="sxs-lookup"><span data-stu-id="ab121-228">Parameters - createFromVariant</span></span>

<span data-ttu-id="ab121-229">バリアント</span><span class="sxs-lookup"><span data-stu-id="ab121-229">variant</span></span>  
<span data-ttu-id="ab121-230">COM クラスの新しいインスタンスを作成するために使用する COMVariant クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="ab121-230">The instance of the COMVariant class to use to create the new instance of the COM class.</span></span>

### <a name="return-value---createfromvariant"></a><span data-ttu-id="ab121-231">戻り値 - createFromVariant</span><span class="sxs-lookup"><span data-stu-id="ab121-231">Return Value - createFromVariant</span></span>

<span data-ttu-id="ab121-232">バリアント パラメーターで指定される COM オブジェクトの COM クラスのインスタンス。COM クラスのインスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="ab121-232">An instance of the COM class for the COM object that is specified by the variant parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance of the COM class could not be created.</span></span>

### <a name="remarks---createfromvariant"></a><span data-ttu-id="ab121-233">備考 - createFromVariant</span><span class="sxs-lookup"><span data-stu-id="ab121-233">Remarks - createFromVariant</span></span>

<span data-ttu-id="ab121-234">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab121-234">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

## <a name="method-getobject"></a><span data-ttu-id="ab121-235">メソッド getObject</span><span class="sxs-lookup"><span data-stu-id="ab121-235">Method getObject</span></span>

<span data-ttu-id="ab121-236">実行している COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-236">Returns an instance of a COM object that is running.</span></span>

```xpp
public static COM getObject(str className)
```

### <a name="parameters---getobject"></a><span data-ttu-id="ab121-237">パラメーター - getObject</span><span class="sxs-lookup"><span data-stu-id="ab121-237">Parameters - getObject</span></span>

<span data-ttu-id="ab121-238">className</span><span class="sxs-lookup"><span data-stu-id="ab121-238">className</span></span>  
<span data-ttu-id="ab121-239">COM クラスのインスタンスを作成するために使用される COM オブジェクトの ProgID 値またはクラス名。</span><span class="sxs-lookup"><span data-stu-id="ab121-239">The ProgID value or class name of the COM object that is used to create the instance of the COM class.</span></span>

### <a name="return-value---getobject"></a><span data-ttu-id="ab121-240">戻り値 - getObject</span><span class="sxs-lookup"><span data-stu-id="ab121-240">Return Value - getObject</span></span>

<span data-ttu-id="ab121-241">className パラメーターで指定されるクラスの COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="ab121-241">An instance of the COM class for the class that is specified by the className parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

### <a name="remarks---getobject"></a><span data-ttu-id="ab121-242">備考 - getObject</span><span class="sxs-lookup"><span data-stu-id="ab121-242">Remarks - getObject</span></span>

<span data-ttu-id="ab121-243">指定した COM オブジェクトの複数インスタンスが実行している場合は、getObject メソッドによってどのインスタンスが返されるかを保証できません。</span><span class="sxs-lookup"><span data-stu-id="ab121-243">If multiple instances of the specified COM object are running, we cannot guarantee which instance will be returned by the getObject method.</span></span> <span data-ttu-id="ab121-244">一部の COM オブジェクトは、このメソッドの呼び出しを可能にする拡張機能をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ab121-244">Some COM objects do not support the extended features that enable calls to this method.</span></span>

### <a name="examples---getobject"></a><span data-ttu-id="ab121-245">例 - getObject</span><span class="sxs-lookup"><span data-stu-id="ab121-245">Examples - getObject</span></span>

<span data-ttu-id="ab121-246">次の例は、実行中の COM オブジェクトのインスタンスを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-246">The following example shows how to retrieve an instance of a running COM object.</span></span>

```xpp
COM objExcel, objWorkBook, objWorkBooks; 
InteropPermission perm; 
```

```xpp
// Set code access permission to help protect the use of COM.new. 
perm = new InteropPermission(InteropKind::ComInterop); 
perm.assert(); 
```

```xpp
objExcel = COM::getObject("Excel.Application"); 
```

```xpp
if (!objExcel) 
{ 
    // Unable to connect to a running instance of Microsoft Excel. 
    // Try starting it. 
    objExcel = new COM("Excel.Application"); 
    if (!objExcel) 
    { 
        Info ("Unable to find or create an instance of Excel"); 
        return;  // Or other error action. 
    }  
} 
// Close code access permission scope. 
CodeAccessPermission::revertAssert(); 
```

```xpp
objExcel.visible(true); 
objWorkBooks = objExcel.workbooks(); 
if (objWorkBooks) 
{ 
    objWorkBook = objWorkBooks.open("d:\mydata\book1.xls"); 
}
```

## <a name="method-getobjectex"></a><span data-ttu-id="ab121-247">メソッド getObjectEx</span><span class="sxs-lookup"><span data-stu-id="ab121-247">Method getObjectEx</span></span>

<span data-ttu-id="ab121-248">ファイル名で指定されている COM オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="ab121-248">Returns an instance of a COM object that is specified by its file name.</span></span>

```xpp
public static COM getObjectEx(str fileName)
```

### <a name="parameters---getobjectex"></a><span data-ttu-id="ab121-249">パラメーター - getObjectEx</span><span class="sxs-lookup"><span data-stu-id="ab121-249">Parameters - getObjectEx</span></span>

<span data-ttu-id="ab121-250">fileName</span><span class="sxs-lookup"><span data-stu-id="ab121-250">fileName</span></span>  
<span data-ttu-id="ab121-251">COM クラスのインスタンスを作成するために使用される COM オブジェクトの機能を提供するファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="ab121-251">The name of the file that provides the functionality for the COM object that is used to create the instance of the COM class.</span></span>

### <a name="return-value---getobjectex"></a><span data-ttu-id="ab121-252">戻り値 - getObjectEx</span><span class="sxs-lookup"><span data-stu-id="ab121-252">Return Value - getObjectEx</span></span>

<span data-ttu-id="ab121-253">filename パラメーターで指定される COM クラスのインスタンス。インスタンスを作成できない場合は nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="ab121-253">An instance of the COM class that is specified by the filename parameter; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the instance could not be created.</span></span>

### <a name="remarks---getobjectex"></a><span data-ttu-id="ab121-254">備考 - getObjectEx</span><span class="sxs-lookup"><span data-stu-id="ab121-254">Remarks - getObjectEx</span></span>

<span data-ttu-id="ab121-255">アンマネージ コードに関連したセキュリティ リスクを軽減するには、このメソッドに渡されるオブジェクトを検証し、COM オブジェクトに使用されるすべての DLL がアクセス制御リストによって保護されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab121-255">To help reduce security risks that are associated with unmanaged code, make sure that you validate the objects that are passed to this method, and that all DLLs used for your COM objects are protected by access control lists.</span></span>

## <a name="method-unsupported"></a><span data-ttu-id="ab121-256">メソッド unsupported</span><span class="sxs-lookup"><span data-stu-id="ab121-256">Method unsupported</span></span>

<span data-ttu-id="ab121-257">予約済み。</span><span class="sxs-lookup"><span data-stu-id="ab121-257">Reserved.</span></span>

```xpp
public static AnyType unsupported(int action, [AnyType param1], [AnyType param2], [AnyType param3])
```

### <a name="parameters---unsupported"></a><span data-ttu-id="ab121-258">パラメーター - unsupported</span><span class="sxs-lookup"><span data-stu-id="ab121-258">Parameters - unsupported</span></span>

<span data-ttu-id="ab121-259">アクション</span><span class="sxs-lookup"><span data-stu-id="ab121-259">action</span></span>  

<!-- -->

<span data-ttu-id="ab121-260">param1</span><span class="sxs-lookup"><span data-stu-id="ab121-260">param1</span></span>  

<!-- -->

<span data-ttu-id="ab121-261">param2</span><span class="sxs-lookup"><span data-stu-id="ab121-261">param2</span></span>  

<!-- -->

<span data-ttu-id="ab121-262">param3</span><span class="sxs-lookup"><span data-stu-id="ab121-262">param3</span></span>  

### <a name="return-value---unsupported"></a><span data-ttu-id="ab121-263">戻り値 - unsupported</span><span class="sxs-lookup"><span data-stu-id="ab121-263">Return Value - unsupported</span></span>

## <a name="method-finalize"></a><span data-ttu-id="ab121-264">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ab121-264">Method finalize</span></span>

<span data-ttu-id="ab121-265">COM クラスのインスタンスに関連付けられているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="ab121-265">Frees resources that are associated with the instance of the COM class.</span></span>

```xpp
public void finalize()
```

### <a name="examples---finalize"></a><span data-ttu-id="ab121-266">例 - finalize</span><span class="sxs-lookup"><span data-stu-id="ab121-266">Examples - finalize</span></span>

<span data-ttu-id="ab121-267">次の例では、finalize メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab121-267">The following example how to use the finalize method.</span></span>

```xpp
objCOM.finalize();
```

## <a name="method-new"></a><span data-ttu-id="ab121-268">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ab121-268">Method new</span></span>

<span data-ttu-id="ab121-269">COM クラスに接続できる COM クラスのインスタンスを作成し、オプションで、指定されたコンピュータ上で COM オブジェクトをインスタンス化することができます。</span><span class="sxs-lookup"><span data-stu-id="ab121-269">Creates an instance of the COM class that can be attached to the COM class and optionally instantiates a COM object on a specified computer.</span></span>

```xpp
public void new([str className], [str computerName])
```

### <a name="parameters---new"></a><span data-ttu-id="ab121-270">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ab121-270">Parameters - new</span></span>

<span data-ttu-id="ab121-271">className</span><span class="sxs-lookup"><span data-stu-id="ab121-271">className</span></span>  
<span data-ttu-id="ab121-272">COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ab121-272">The name of the remote computer on which to instantiate the COM object; optional.</span></span> <span data-ttu-id="ab121-273">このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-273">If this parameter is omitted, the COM object is instantiated on the local computer.</span></span> <span data-ttu-id="ab121-274">コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-274">If the computer name is specified, the DCOM system component must be installed on both the local computer and the remote computer.</span></span> <span data-ttu-id="ab121-275">特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-275">The specific COM object must support DCOM, and it must be correctly configured on both the local computer and the remote computer.</span></span> <span data-ttu-id="ab121-276">システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="ab121-276">The system component is a standard component of Microsoft Windows 98, Windows NT, and later versions.</span></span> <span data-ttu-id="ab121-277">Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-277">In Windows 95, the DCOM system component must be installed.</span></span>

<!-- -->

<span data-ttu-id="ab121-278">computerName</span><span class="sxs-lookup"><span data-stu-id="ab121-278">computerName</span></span>  
<span data-ttu-id="ab121-279">COM オブジェクトをインスタンス化するリモート コンピューターの名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ab121-279">The name of the remote computer on which to instantiate the COM object; optional.</span></span> <span data-ttu-id="ab121-280">このパラメータを省略すると、COM オブジェクトはローカル コンピューターでインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-280">If this parameter is omitted, the COM object is instantiated on the local computer.</span></span> <span data-ttu-id="ab121-281">コンピューター名が指定されている場合は、ローカル コンピューターとリモート コンピューターの両方に DCOM システムのコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-281">If the computer name is specified, the DCOM system component must be installed on both the local computer and the remote computer.</span></span> <span data-ttu-id="ab121-282">特定の COM オブジェクトは DCOM をサポートする必要があり、ローカル コンピューターとリモート コンピューターの両方で正しく構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-282">The specific COM object must support DCOM, and it must be correctly configured on both the local computer and the remote computer.</span></span> <span data-ttu-id="ab121-283">システム コンポーネントは、Microsoft Windows 98、Windows NT、およびそれ以降のバージョンの標準コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="ab121-283">The system component is a standard component of Microsoft Windows 98, Windows NT, and later versions.</span></span> <span data-ttu-id="ab121-284">Windows 95 では、DCOM システム コンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab121-284">In Windows 95, the DCOM system component must be installed.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="ab121-285">備考 - new</span><span class="sxs-lookup"><span data-stu-id="ab121-285">Remarks - new</span></span>

<span data-ttu-id="ab121-286">COM オブジェクトのクラス名は、そのプログラム識別子 (ProgID) またはそのクラス識別子 (CLSID) です。</span><span class="sxs-lookup"><span data-stu-id="ab121-286">The class name of a COM object is either its programmatic identifier (ProgID) or its class identifier (CLSID):</span></span>

-   <span data-ttu-id="ab121-287">ProgID の形式: program.component.version</span><span class="sxs-lookup"><span data-stu-id="ab121-287">ProgIDs have the following format: program.component.version</span></span>
-   <span data-ttu-id="ab121-288">ClSID は 128 ビット値であり、その形式は {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} です。</span><span class="sxs-lookup"><span data-stu-id="ab121-288">CLSIDs are 128-bit values and have the following format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span>

<span data-ttu-id="ab121-289">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="ab121-289">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="ab121-290">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-290">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="ab121-291">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab121-291">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="ab121-292">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab121-292">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="ab121-293">例 - new</span><span class="sxs-lookup"><span data-stu-id="ab121-293">Examples - new</span></span>

<span data-ttu-id="ab121-294">この例では、Scripting.FileSystemObject COM オブジェクトから GetFileName メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ab121-294">This example calls the GetFileName method from the Scripting.FileSystemObject COM object.</span></span>

```xpp
void COMExample() 
{ 
    COM               com; 
    str               result; 
    InteropPermission perm; 
```

```xpp
    // Set the code access permission to help protect the use of the 
    // COM object. 
    perm = new InteropPermission(InteropKind::ComInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    // Permission scope starts here. 
    perm.assert(); 
```

```xpp
    com = new COM("Scripting.FileSystemObject"); 
    if (com != null) 
    { 
        result = com.GetFileName(@"c:\boot.ini"); 
    } 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-attach"></a><span data-ttu-id="ab121-295">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="ab121-295">Method attach</span></span>

<span data-ttu-id="ab121-296">COM クラスのインスタンスを COM インターフェイスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ab121-296">Attaches an instance of the COM class to a COM interface.</span></span>

```xpp
public void attach(ComInterface interface)
```

### <a name="parameters---attach"></a><span data-ttu-id="ab121-297">パラメーター - attach</span><span class="sxs-lookup"><span data-stu-id="ab121-297">Parameters - attach</span></span>

<span data-ttu-id="ab121-298">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ab121-298">interface</span></span>  
<span data-ttu-id="ab121-299">COM クラスのインスタンスに関連付けるインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="ab121-299">The interface to attach to the instance of the COM class.</span></span>

### <a name="remarks---attach"></a><span data-ttu-id="ab121-300">備考 - attach</span><span class="sxs-lookup"><span data-stu-id="ab121-300">Remarks - attach</span></span>

<span data-ttu-id="ab121-301">このメソッドは、一部の COM オブジェクトは他の COM オブジェクトによってのみインスタンス化されるが、COM クラスによって直接インスタンス化することができないため、用意されています。</span><span class="sxs-lookup"><span data-stu-id="ab121-301">This method is provided because some COM objects can be instantiated only by other COM objects and cannot be instantiated directly by the COM class.</span></span>

## <a name="method-detach"></a><span data-ttu-id="ab121-302">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="ab121-302">Method detach</span></span>

<span data-ttu-id="ab121-303">関連付けられているクラスから COM オブジェクトを解除します。</span><span class="sxs-lookup"><span data-stu-id="ab121-303">Detaches a COM object from the class that it was associated with.</span></span>

```xpp
public void detach()
```

### <a name="remarks---detach"></a><span data-ttu-id="ab121-304">備考 - detach</span><span class="sxs-lookup"><span data-stu-id="ab121-304">Remarks - detach</span></span>

<span data-ttu-id="ab121-305">たとえば、このメソッドは、接続または新しいメソッドの呼び出しから COM オブジェクトを切り離すために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ab121-305">For example, this method can be called to detach a COM object from a call to the attach or new method.</span></span>

