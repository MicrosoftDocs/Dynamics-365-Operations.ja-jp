---
title: CodeAccessPermission クラス
description: このトピックでは、CodeAccessPermission クラスについて説明します。
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
ms.openlocfilehash: e3f7f6d30d76a85d4c1120e22c46c1917e0d37b9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502745"
---
# <a name="class-codeaccesspermission"></a><span data-ttu-id="55d6a-103">クラス CodeAccessPermission</span><span class="sxs-lookup"><span data-stu-id="55d6a-103">Class CodeAccessPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CodeAccessPermission extends Object
```

<span data-ttu-id="55d6a-104">CodeAccessPermission クラスは、コード アクセス許可の基になる構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-104">The CodeAccessPermission class defines the underlying structure of code access permissions.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d6a-105">備考</span><span class="sxs-lookup"><span data-stu-id="55d6a-105">Remarks</span></span>

<span data-ttu-id="55d6a-106">次のクラスは、CodeAccessPermission クラスを拡張します: ExecutePermission、FileIOPermission、InteropPermission、RunAsPermission、SkipAOSValidationPermission、SqlDataDictionaryPermission、SqlStatementExecutePermission、および SysDatabaseLogPermission。</span><span class="sxs-lookup"><span data-stu-id="55d6a-106">The following classes extend the CodeAccessPermission class: ExecutePermission, FileIOPermission, InteropPermission, RunAsPermission, SkipAOSValidationPermission, SqlDataDictionaryPermission, SqlStatementExecutePermission, and SysDatabaseLogPermission.</span></span>

## <a name="examples"></a><span data-ttu-id="55d6a-107">例</span><span class="sxs-lookup"><span data-stu-id="55d6a-107">Examples</span></span>

<span data-ttu-id="55d6a-108">次のコード例は、CodeAccessPermission クラスから派生したクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-108">The following code example shows a class that is derived from the CodeAccessPermission class.</span></span>

```xpp
final class SysTestCodeAccessPermission extends CodeAccessPermission 
{ 
    str data; 
}
```

<span data-ttu-id="55d6a-109">このコード例は、API を保護するプロセスのステップを示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-109">This code example illustrates a step in the process of protecting an API.</span></span>

## <a name="methods"></a><span data-ttu-id="55d6a-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="55d6a-110">Methods</span></span>

| <span data-ttu-id="55d6a-111">方法</span><span class="sxs-lookup"><span data-stu-id="55d6a-111">Method</span></span>                                                 | <span data-ttu-id="55d6a-112">説明</span><span class="sxs-lookup"><span data-stu-id="55d6a-112">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d6a-113">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="55d6a-113">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="55d6a-114">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-114">Creates and returns a copy of a permission class object.</span></span>                                                                                          |
| <span data-ttu-id="55d6a-115">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="55d6a-115">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="55d6a-116">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-116">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>                         |
| <span data-ttu-id="55d6a-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="55d6a-117">public void new()</span></span>                                      | <span data-ttu-id="55d6a-118">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-118">Initializes a new instance of the CodeAccessPermission class.</span></span>                                                                                     |
| <span data-ttu-id="55d6a-119">public void assert()</span><span class="sxs-lookup"><span data-stu-id="55d6a-119">public void assert()</span></span>                                   | <span data-ttu-id="55d6a-120">呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-120">Declares that the calling code can invoke an API that is protected by a permission.</span></span>                                                               |
| <span data-ttu-id="55d6a-121">public void demand()</span><span class="sxs-lookup"><span data-stu-id="55d6a-121">public void demand()</span></span>                                   | <span data-ttu-id="55d6a-122">コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-122">Checks the call stack to determine whether the permission that is required to invoke an API has been granted to the calling code.</span></span>                 |
| <span data-ttu-id="55d6a-123">::public static void revertAssert()</span><span class="sxs-lookup"><span data-stu-id="55d6a-123">::public static void revertAssert()</span></span>                    | <span data-ttu-id="55d6a-124">CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="55d6a-124">Causes a previous call to the CodeAccessPermission.assert and CodeAccessPermission::assertMultiple methods to be removed and no longer in effect.</span></span> |
| <span data-ttu-id="55d6a-125">::public static void assertMultiple(Set permissionSet)</span><span class="sxs-lookup"><span data-stu-id="55d6a-125">::public static void assertMultiple(Set permissionSet)</span></span> | <span data-ttu-id="55d6a-126">呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-126">Declares that the calling code can invoke an API that is protected by any of the permissions in a specified collection.</span></span>                           |

## <a name="method-copy"></a><span data-ttu-id="55d6a-127">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="55d6a-127">Method copy</span></span>

<span data-ttu-id="55d6a-128">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-128">Creates and returns a copy of a permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="55d6a-129">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="55d6a-129">Return Value - copy</span></span>

<span data-ttu-id="55d6a-130">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="55d6a-130">A copy of the derived class object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="55d6a-131">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="55d6a-131">Remarks - copy</span></span>

<span data-ttu-id="55d6a-132">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-132">You can override this method as part of the process of making an API more secure.</span></span>

### <a name="examples---copy"></a><span data-ttu-id="55d6a-133">例 - copy</span><span class="sxs-lookup"><span data-stu-id="55d6a-133">Examples - copy</span></span>

<span data-ttu-id="55d6a-134">次のコード例は、copy メソッドを上書きして、CodeAccessPermission クラスから派生したクラスのコピーを作成して返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-134">The following code example shows how to override the copy method to create and return a copy of a class that is derived from the CodeAccessPermission class.</span></span>

```xpp
public CodeAccessPermission copy() 
{ 
    return new SysTestCodeAccessPermission(_data); 
}
```

## <a name="method-issubsetof"></a><span data-ttu-id="55d6a-135">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="55d6a-135">Method isSubsetOf</span></span>

<span data-ttu-id="55d6a-136">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-136">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="55d6a-137">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="55d6a-137">Parameters - isSubsetOf</span></span>

<span data-ttu-id="55d6a-138">target</span><span class="sxs-lookup"><span data-stu-id="55d6a-138">target</span></span>  
<span data-ttu-id="55d6a-139">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="55d6a-139">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="55d6a-140">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="55d6a-140">Return Value - isSubsetOf</span></span>

<span data-ttu-id="55d6a-141">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="55d6a-141">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="55d6a-142">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="55d6a-142">Remarks - isSubsetOf</span></span>

<span data-ttu-id="55d6a-143">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-143">You can override the method as part of the process of making an API more secure.</span></span>

### <a name="examples---issubsetof"></a><span data-ttu-id="55d6a-144">例 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="55d6a-144">Examples - isSubsetOf</span></span>

<span data-ttu-id="55d6a-145">次の例は、isSubsetOf メソッドを上書きして、現在のオブジェクトに格納されているアクセス権が \_target にあるかどうかを判断する方法を示しています。.</span><span class="sxs-lookup"><span data-stu-id="55d6a-145">The following example shows how to override the isSubsetOf method to determine whether permissions that are stored in the current object are located in \_target.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission _target) 
{ 
    SysTestCodeAccessPermission sysTarget = _target; 
    return this.handle() == _target.handle(); 
}
```

## <a name="method-new"></a><span data-ttu-id="55d6a-146">メソッド new</span><span class="sxs-lookup"><span data-stu-id="55d6a-146">Method new</span></span>

<span data-ttu-id="55d6a-147">CodeAccessPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-147">Initializes a new instance of the CodeAccessPermission class.</span></span>

```xpp
public void new()
```

## <a name="method-assert"></a><span data-ttu-id="55d6a-148">メソッド assert</span><span class="sxs-lookup"><span data-stu-id="55d6a-148">Method assert</span></span>

<span data-ttu-id="55d6a-149">呼び出しコードがアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-149">Declares that the calling code can invoke an API that is protected by a permission.</span></span>

```xpp
public void assert()
```

### <a name="remarks---assert"></a><span data-ttu-id="55d6a-150">備考 - assert</span><span class="sxs-lookup"><span data-stu-id="55d6a-150">Remarks - assert</span></span>

<span data-ttu-id="55d6a-151">API を起動する前に、保護された API の派生クラスで assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="55d6a-151">You must call the assert method in the derived class for a protected API before you invoke the API.</span></span> <span data-ttu-id="55d6a-152">アクセス許可によって保護されている API の詳細については、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55d6a-152">For more information about APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="55d6a-153">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="55d6a-153">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="55d6a-154">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="55d6a-154">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="55d6a-155">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="55d6a-155">A server static method</span></span>
-   <span data-ttu-id="55d6a-156">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="55d6a-156">A class instance method that is set to run on the server by using the RunOn class property</span></span>

<span data-ttu-id="55d6a-157">同じ呼び出しコードにおいて Assert メソッドに対する複数の連続した呼び出しはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="55d6a-157">Multiple, successive calls to the assert method in the same calling code are not supported.</span></span> <span data-ttu-id="55d6a-158">assert メソッドへの各呼び出し間で CodeAccessPermission::revertAssert メソッドを呼び出すか、または CodeAccessPermission::assertMultiple メソッドを呼び出すかのいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="55d6a-158">Either call the CodeAccessPermission::revertAssert method between each call to the assert method, or call the CodeAccessPermission::assertMultiple method.</span></span> <span data-ttu-id="55d6a-159">assertmethod を複数にわたり連続して呼び出すと、コードを実行するときに Infolog によってエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-159">If you make multiple, successive calls to the assertmethod, the Infolog displays an error when you execute the code.</span></span>

### <a name="examples---assert"></a><span data-ttu-id="55d6a-160">例 - assert</span><span class="sxs-lookup"><span data-stu-id="55d6a-160">Examples - assert</span></span>

<span data-ttu-id="55d6a-161">次のコード例は、アクセス許可で保護されている AsciiIo クラスが呼び出される前に assert メソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-161">The following code example shows a call to the assert method before the AsciiIo Class class that is protected by a permission is invoked.</span></span> <span data-ttu-id="55d6a-162">assert メソッドは、CodeAccessPermission クラスから派生した FileIOPermission クラスのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="55d6a-162">The assert method is a member of the FileIOPermission class that is derived from the CodeAccessPermission class.</span></span>

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
```


```xpp
    _perm = new FileIoPermission("c:\File.txt",'r'); 
    _perm.assert(); 
```

```xpp
    // Invoke the protected API. 
    a = new AsciiIo("c:\File.txt",'r'); 
}
```

## <a name="method-demand"></a><span data-ttu-id="55d6a-163">メソッド demand</span><span class="sxs-lookup"><span data-stu-id="55d6a-163">Method demand</span></span>

<span data-ttu-id="55d6a-164">コール スタックをチェックして、API を呼び出すために必要なアクセス許可が呼び出しコードに与えられているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-164">Checks the call stack to determine whether the permission that is required to invoke an API has been granted to the calling code.</span></span>

```xpp
public void demand()
```

### <a name="examples---demand"></a><span data-ttu-id="55d6a-165">例 - demand</span><span class="sxs-lookup"><span data-stu-id="55d6a-165">Examples - demand</span></span>

<span data-ttu-id="55d6a-166">次のコード例は、API 機能を実行する前に、API を呼び出すコードに data 変数で指定されたリソースへのアクセス許可が与えられているかどうかを判断するための、demand メソッドの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-166">The following code example shows a call to the demand method before the API functionality is executed, to determine whether permission to access the resource that is specified by the data variable has been granted to code that is calling the API.</span></span>

```xpp
public static void main(str data) 
{ 
    SysTestCodeAccessPermission p = new SysTestCodeAccessPermission(data); 
    p.demand(); 
```

```xpp
    //Add functionality 
}
```

<span data-ttu-id="55d6a-167">このコード例は、API を保護するプロセスのステップを示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-167">This code example illustrates a step in the process of protecting an API.</span></span>

## <a name="method-revertassert"></a><span data-ttu-id="55d6a-168">メソッド revertAssert</span><span class="sxs-lookup"><span data-stu-id="55d6a-168">Method revertAssert</span></span>

<span data-ttu-id="55d6a-169">CodeAccessPermission.assert および CodeAccessPermission::assertMultiple メソッドへの以前の呼び出しを削除し、無効にします。</span><span class="sxs-lookup"><span data-stu-id="55d6a-169">Causes a previous call to the CodeAccessPermission.assert and CodeAccessPermission::assertMultiple methods to be removed and no longer in effect.</span></span>

```xpp
public static void revertAssert()
```

### <a name="remarks---revertassert"></a><span data-ttu-id="55d6a-170">備考 - revertAssert</span><span class="sxs-lookup"><span data-stu-id="55d6a-170">Remarks - revertAssert</span></span>

<span data-ttu-id="55d6a-171">同じ呼び出しコードで assert メソッドに複数の呼び出しをするときは、それぞれの呼び出しの間に revertAssert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="55d6a-171">When you have multiple calls to the assert method in the same calling code, you must call the revertAssert method between each call.</span></span> <span data-ttu-id="55d6a-172">それ以外の場合、情報ログには、コードを実行するときにエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-172">Otherwise, the Infolog displays an error when you execute the code.</span></span> <span data-ttu-id="55d6a-173">assert メソッドを1回だけ呼び出すとき、または CodeAccessPermission::assertMultiple メソッドを呼び出すときは、保護された API の起動後にも revertAssert メソッドを呼び出して、アサートの範囲を制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="55d6a-173">When you call the assert method only one time, or when you call the CodeAccessPermission::assertMultiple method, we recommend that you still call the revertAssert method after you invoke the protected API to limit the scope of the assert.</span></span>

### <a name="examples---revertassert"></a><span data-ttu-id="55d6a-174">例 - revertAssert</span><span class="sxs-lookup"><span data-stu-id="55d6a-174">Examples - revertAssert</span></span>

<span data-ttu-id="55d6a-175">次のコード例は、ユーザーが CodeAccessPermission.assert メソッドとアクセス許可で保護されている AsciiIo クラスの呼び出しを呼び出した後の、 CodeAccessPermission::revertAssert メソッドへの呼び出しを示しています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-175">The following code example shows a call to the CodeAccessPermission::revertAssert method after the user calls the CodeAccessPermission.assert method and the AsciiIo class that is protected by a permission.</span></span>

```xpp
server static void main(Args args) 
{ 
    FileIoPermission _perm; 
    AsciiIo a; 
```


```xpp
    _perm = new FileIoPermission("c:\File.txt",'r'); 
    _perm.assert(); 
```

```xpp
    //invoke protected API 
    a = new AsciiIo("c:\File.txt",'r'); 
```

```xpp
    // Optionally call revertAssert() to limit scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-assertmultiple"></a><span data-ttu-id="55d6a-176">メソッド assertMultiple</span><span class="sxs-lookup"><span data-stu-id="55d6a-176">Method assertMultiple</span></span>

<span data-ttu-id="55d6a-177">呼び出しコードが指定されたコレクションでのアクセス許可によって保護されている API を呼び出すことができることを宣言します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-177">Declares that the calling code can invoke an API that is protected by any of the permissions in a specified collection.</span></span>

```xpp
public static void assertMultiple(Set permissionSet)
```

### <a name="parameters---assertmultiple"></a><span data-ttu-id="55d6a-178">パラメーター - assertMultiple</span><span class="sxs-lookup"><span data-stu-id="55d6a-178">Parameters - assertMultiple</span></span>

<span data-ttu-id="55d6a-179">permissionSet</span><span class="sxs-lookup"><span data-stu-id="55d6a-179">permissionSet</span></span>  
<span data-ttu-id="55d6a-180">アクセス許可のコレクションを含むセット クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="55d6a-180">A Set class object that contains a collection of permissions.</span></span>

### <a name="remarks---assertmultiple"></a><span data-ttu-id="55d6a-181">備考 - assertMultiple</span><span class="sxs-lookup"><span data-stu-id="55d6a-181">Remarks - assertMultiple</span></span>

<span data-ttu-id="55d6a-182">同じ呼び出しコードで CodeAccessPermission.assert および CodeAccessPermission::revertAssert メソッドに対する複数の連続する呼び出しをする代わりに、assertMultple メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-182">You call the assertMultple method instead of making multiple, successive calls to the CodeAccessPermission.assert and CodeAccessPermission::revertAssert methods in the same calling code.</span></span>

### <a name="examples---assertmultiple"></a><span data-ttu-id="55d6a-183">例 - assertMultiple</span><span class="sxs-lookup"><span data-stu-id="55d6a-183">Examples - assertMultiple</span></span>

<span data-ttu-id="55d6a-184">次のコード例は、CodeAccessPermission::assertMultple メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-184">The following code example calls the CodeAccessPermission::assertMultple method.</span></span> <span data-ttu-id="55d6a-185">このコード例は WinAPIServer::createFile メソッドを呼び出します。このメソッド、CodeAccessPermission::assertMultple メソッドへの事前の呼び出しがない場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="55d6a-185">Then the code example calls the WinAPIServer::createFile method, which would fail without the previous call to the CodeAccessPermission::assertMultple method.</span></span> <span data-ttu-id="55d6a-186">このコード例は、作成する新しいクラスに追加できる静的メソッドです。</span><span class="sxs-lookup"><span data-stu-id="55d6a-186">The code example is a static method that you can add to a new class that you create.</span></span> <span data-ttu-id="55d6a-187">MyClass::RunOnServerPermissionTest のようなコード行を使用して、X++ ジョブから静的メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-187">You can call this static method from an X++ job by using one line of code that resembles MyClass::RunOnServerPermissionTest.</span></span> <span data-ttu-id="55d6a-188">コードの例では、WinAPIServer クラスに、セキュリティで保護されたメソッドがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="55d6a-188">In the code example, the WinAPIServer class has several secure methods.</span></span> <span data-ttu-id="55d6a-189">WinAPIServer クラスは、クライアント層ではなく、サーバー層で実行されます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-189">The WinAPIServer class runs on the server tier, not on the client tier.</span></span> <span data-ttu-id="55d6a-190">したがって、コード例のメソッドはサーバー層でも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55d6a-190">Therefore the code example method must also run on the server tier.</span></span> <span data-ttu-id="55d6a-191">それ以外の場合、クライアント層で実行されたすべてのアクセス許可アサートは、サーバー層で実行されるメソッドにより無視されます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-191">Otherwise, any permission asserts that are made on the client tier are ignored by methods that run on the server tier.</span></span> <span data-ttu-id="55d6a-192">このため、サーバー キーワードはコード例のメソッド宣言に含まれています。</span><span class="sxs-lookup"><span data-stu-id="55d6a-192">This is why the server keyword is included in the method declaration of the code example.</span></span> <span data-ttu-id="55d6a-193">メソッドのサーバー キーワードは、クラスで指定された RunOn プロパティ値よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="55d6a-193">The server keyword on the method takes precedence over the RunOn property value that is specified on the class.</span></span>

```xpp
server
    static public void RunOnServerPermissionTest()
{
    Set permissionSet;
    str fileName = @"C:\TestFile75a.txt";
    boolean boolFileDeleted;
```

```xpp
    permissionSet =  new Set(Types::Class);
    permissionSet.add(new FileIoPermission(fileName,'rw'));
```

```xpp
    CodeAccessPermission::assertMultiple(permissionSet);
    //--- Permissions are set, now perform file operations.
```

```xpp
    WinAPIServer::createFile(fileName);
    boolFileDeleted = WinAPI::deleteFile(fileName);
```

```xpp
    if (boolFileDeleted)
    {
        info("The file was deleted. Good.");
    }
    else
    {
        error("The file was not deleted. Error.");
    }
}
```

