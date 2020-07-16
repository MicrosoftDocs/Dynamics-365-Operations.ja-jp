---
title: XppCompiler クラス
description: このトピックでは、XppCompiler クラスについて説明します。
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
ms.openlocfilehash: 14f88fa8bae3e8610f8b1b5d66ccb12de5a32872
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502772"
---
# <a name="class-xppcompiler"></a><span data-ttu-id="fbf31-103">クラス XppCompiler</span><span class="sxs-lookup"><span data-stu-id="fbf31-103">Class XppCompiler</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class XppCompiler extends Object
```

## <a name="remarks"></a><span data-ttu-id="fbf31-104">備考</span><span class="sxs-lookup"><span data-stu-id="fbf31-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fbf31-105">例</span><span class="sxs-lookup"><span data-stu-id="fbf31-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fbf31-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fbf31-106">Methods</span></span>

| <span data-ttu-id="fbf31-107">方法</span><span class="sxs-lookup"><span data-stu-id="fbf31-107">Method</span></span>                                 | <span data-ttu-id="fbf31-108">説明</span><span class="sxs-lookup"><span data-stu-id="fbf31-108">Description</span></span>                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf31-109">public boolean compile(str source)</span><span class="sxs-lookup"><span data-stu-id="fbf31-109">public boolean compile(str source)</span></span>     |                                                                                                                   |
| <span data-ttu-id="fbf31-110">public boolean compileExpr(str source)</span><span class="sxs-lookup"><span data-stu-id="fbf31-110">public boolean compileExpr(str source)</span></span> |                                                                                                                   |
| <span data-ttu-id="fbf31-111">public str dumpClass(str className)</span><span class="sxs-lookup"><span data-stu-id="fbf31-111">public str dumpClass(str className)</span></span>    | <span data-ttu-id="fbf31-112">クラスの X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-112">Creates an XML string that contains the X++ compiler information for a class.</span></span>                                     |
| <span data-ttu-id="fbf31-113">public str dumpEnums()</span><span class="sxs-lookup"><span data-stu-id="fbf31-113">public str dumpEnums()</span></span>                 | <span data-ttu-id="fbf31-114">現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-114">Creates an XML string that contains the X++ compiler information for all enumerations in the current application.</span></span> |
| <span data-ttu-id="fbf31-115">public str dumpTable(str tableName)</span><span class="sxs-lookup"><span data-stu-id="fbf31-115">public str dumpTable(str tableName)</span></span>    | <span data-ttu-id="fbf31-116">テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-116">Creates an XML string that contains the X++ compiler information for a table.</span></span>                                     |
| <span data-ttu-id="fbf31-117">public str errorText()</span><span class="sxs-lookup"><span data-stu-id="fbf31-117">public str errorText()</span></span>                 |                                                                                                                   |
| <span data-ttu-id="fbf31-118">public AnyType execute(VarArg )</span><span class="sxs-lookup"><span data-stu-id="fbf31-118">public AnyType execute(VarArg )</span></span>        |                                                                                                                   |
| <span data-ttu-id="fbf31-119">public AnyType executeEx()</span><span class="sxs-lookup"><span data-stu-id="fbf31-119">public AnyType executeEx()</span></span>             |                                                                                                                   |
| <span data-ttu-id="fbf31-120">public void setGuidArg(Guid arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-120">public void setGuidArg(Guid arg)</span></span>       |                                                                                                                   |
| <span data-ttu-id="fbf31-121">public void setInt64Arg(Int64 arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-121">public void setInt64Arg(Int64 arg)</span></span>     |                                                                                                                   |
| <span data-ttu-id="fbf31-122">public void setDateArg(Date arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-122">public void setDateArg(Date arg)</span></span>       |                                                                                                                   |
| <span data-ttu-id="fbf31-123">public void new()</span><span class="sxs-lookup"><span data-stu-id="fbf31-123">public void new()</span></span>                      | <span data-ttu-id="fbf31-124">XppCompiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-124">Initializes a new instance of the XppCompiler class.</span></span>                                                              |
| <span data-ttu-id="fbf31-125">public void endArgs()</span><span class="sxs-lookup"><span data-stu-id="fbf31-125">public void endArgs()</span></span>                  |                                                                                                                   |
| <span data-ttu-id="fbf31-126">public void startArgs()</span><span class="sxs-lookup"><span data-stu-id="fbf31-126">public void startArgs()</span></span>                |                                                                                                                   |
| <span data-ttu-id="fbf31-127">public void setRealArg(Real arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-127">public void setRealArg(Real arg)</span></span>       |                                                                                                                   |
| <span data-ttu-id="fbf31-128">public void setIntArg(int arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-128">public void setIntArg(int arg)</span></span>         |                                                                                                                   |
| <span data-ttu-id="fbf31-129">public void setStrArg(str arg)</span><span class="sxs-lookup"><span data-stu-id="fbf31-129">public void setStrArg(str arg)</span></span>         |                                                                                                                   |

## <a name="method-compile"></a><span data-ttu-id="fbf31-130">メソッド compile</span><span class="sxs-lookup"><span data-stu-id="fbf31-130">Method compile</span></span>

```xpp
public boolean compile(str source)
```

### <a name="parameters---compile"></a><span data-ttu-id="fbf31-131">パラメーター - compile</span><span class="sxs-lookup"><span data-stu-id="fbf31-131">Parameters - compile</span></span>

<span data-ttu-id="fbf31-132">ソース</span><span class="sxs-lookup"><span data-stu-id="fbf31-132">source</span></span>  

### <a name="return-value---compile"></a><span data-ttu-id="fbf31-133">戻り値 - compile</span><span class="sxs-lookup"><span data-stu-id="fbf31-133">Return Value - compile</span></span>

## <a name="method-compileexpr"></a><span data-ttu-id="fbf31-134">メソッド compileExpr</span><span class="sxs-lookup"><span data-stu-id="fbf31-134">Method compileExpr</span></span>

```xpp
public boolean compileExpr(str source)
```

### <a name="parameters---compileexpr"></a><span data-ttu-id="fbf31-135">パラメーター - compileExpr</span><span class="sxs-lookup"><span data-stu-id="fbf31-135">Parameters - compileExpr</span></span>

<span data-ttu-id="fbf31-136">ソース</span><span class="sxs-lookup"><span data-stu-id="fbf31-136">source</span></span>  

### <a name="return-value---compileexpr"></a><span data-ttu-id="fbf31-137">戻り値 - compileExpr</span><span class="sxs-lookup"><span data-stu-id="fbf31-137">Return Value - compileExpr</span></span>

## <a name="method-dumpclass"></a><span data-ttu-id="fbf31-138">メソッド dumpClass</span><span class="sxs-lookup"><span data-stu-id="fbf31-138">Method dumpClass</span></span>

<span data-ttu-id="fbf31-139">クラスの X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-139">Creates an XML string that contains the X++ compiler information for a class.</span></span>

```xpp
public str dumpClass(str className)
```

### <a name="parameters---dumpclass"></a><span data-ttu-id="fbf31-140">パラメーター - dumpClass</span><span class="sxs-lookup"><span data-stu-id="fbf31-140">Parameters - dumpClass</span></span>

<span data-ttu-id="fbf31-141">className</span><span class="sxs-lookup"><span data-stu-id="fbf31-141">className</span></span>  

### <a name="return-value---dumpclass"></a><span data-ttu-id="fbf31-142">戻り値 - dumpClass</span><span class="sxs-lookup"><span data-stu-id="fbf31-142">Return Value - dumpClass</span></span>

<span data-ttu-id="fbf31-143">指定したクラスの X++ コンパイラ情報</span><span class="sxs-lookup"><span data-stu-id="fbf31-143">The X++ compiler information for the specified class</span></span>

### <a name="remarks---dumpclass"></a><span data-ttu-id="fbf31-144">備考 - dumpClass</span><span class="sxs-lookup"><span data-stu-id="fbf31-144">Remarks - dumpClass</span></span>

<span data-ttu-id="fbf31-145">バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-145">General use of this method is discouraged, because the output format might change without warning from version to version.</span></span>

## <a name="method-dumpenums"></a><span data-ttu-id="fbf31-146">メソッド dumpEnums</span><span class="sxs-lookup"><span data-stu-id="fbf31-146">Method dumpEnums</span></span>

<span data-ttu-id="fbf31-147">現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-147">Creates an XML string that contains the X++ compiler information for all enumerations in the current application.</span></span>

```xpp
public str dumpEnums()
```

### <a name="return-value---dumpenums"></a><span data-ttu-id="fbf31-148">戻り値 - dumpEnums</span><span class="sxs-lookup"><span data-stu-id="fbf31-148">Return Value - dumpEnums</span></span>

<span data-ttu-id="fbf31-149">現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報</span><span class="sxs-lookup"><span data-stu-id="fbf31-149">The X++ compiler information for all enumerations in the current application</span></span>

### <a name="remarks---dumpenums"></a><span data-ttu-id="fbf31-150">備考 - dumpEnums</span><span class="sxs-lookup"><span data-stu-id="fbf31-150">Remarks - dumpEnums</span></span>

<span data-ttu-id="fbf31-151">バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-151">General use of this method is discouraged, because the output format might change without warning from version to version.</span></span>

## <a name="method-dumptable"></a><span data-ttu-id="fbf31-152">メソッド dumpTable</span><span class="sxs-lookup"><span data-stu-id="fbf31-152">Method dumpTable</span></span>

<span data-ttu-id="fbf31-153">テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-153">Creates an XML string that contains the X++ compiler information for a table.</span></span>

```xpp
public str dumpTable(str tableName)
```

### <a name="parameters---dumptable"></a><span data-ttu-id="fbf31-154">パラメーター - dumpTable</span><span class="sxs-lookup"><span data-stu-id="fbf31-154">Parameters - dumpTable</span></span>

<span data-ttu-id="fbf31-155">tableName</span><span class="sxs-lookup"><span data-stu-id="fbf31-155">tableName</span></span>  

### <a name="return-value---dumptable"></a><span data-ttu-id="fbf31-156">戻り値 - dumpTable</span><span class="sxs-lookup"><span data-stu-id="fbf31-156">Return Value - dumpTable</span></span>

<span data-ttu-id="fbf31-157">指定したテーブルの X++ コンパイラ情報</span><span class="sxs-lookup"><span data-stu-id="fbf31-157">The X++ compiler information for the specified table</span></span>

### <a name="remarks---dumptable"></a><span data-ttu-id="fbf31-158">備考 - dumpTable</span><span class="sxs-lookup"><span data-stu-id="fbf31-158">Remarks - dumpTable</span></span>

<span data-ttu-id="fbf31-159">バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-159">General use of this method is discouraged, because the output format might change without warning from version to version.</span></span>

## <a name="method-errortext"></a><span data-ttu-id="fbf31-160">メソッド errorText</span><span class="sxs-lookup"><span data-stu-id="fbf31-160">Method errorText</span></span>

```xpp
public str errorText()
```

### <a name="return-value---errortext"></a><span data-ttu-id="fbf31-161">戻り値 - errorText</span><span class="sxs-lookup"><span data-stu-id="fbf31-161">Return Value - errorText</span></span>

## <a name="method-execute"></a><span data-ttu-id="fbf31-162">メソッド execute</span><span class="sxs-lookup"><span data-stu-id="fbf31-162">Method execute</span></span>

```xpp
public AnyType execute(VarArg )
```

### <a name="parameters---execute"></a><span data-ttu-id="fbf31-163">パラメーター - execute</span><span class="sxs-lookup"><span data-stu-id="fbf31-163">Parameters - execute</span></span>


### <a name="return-value---execute"></a><span data-ttu-id="fbf31-164">戻り値 - execute</span><span class="sxs-lookup"><span data-stu-id="fbf31-164">Return Value - execute</span></span>

### <a name="remarks---execute"></a><span data-ttu-id="fbf31-165">備考 - execute</span><span class="sxs-lookup"><span data-stu-id="fbf31-165">Remarks - execute</span></span>

<span data-ttu-id="fbf31-166">XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-166">XppCompiler objects can compile code at run time.</span></span> <span data-ttu-id="fbf31-167">これはセキュリティ リスクをもたらします。</span><span class="sxs-lookup"><span data-stu-id="fbf31-167">This presents a security risk.</span></span> <span data-ttu-id="fbf31-168">したがって、メソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-168">Therefore, execute method runs under Code Access Security.</span></span> <span data-ttu-id="fbf31-169">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-169">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="fbf31-170">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-170">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---execute"></a><span data-ttu-id="fbf31-171">例 - execute</span><span class="sxs-lookup"><span data-stu-id="fbf31-171">Examples - execute</span></span>

<span data-ttu-id="fbf31-172">次の例では、execute メソッドを呼び出して、指定されたバッファをコンパイルして実行します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-172">The following example calls the execute method to compile and execute the supplied buffer.</span></span>

```xpp
void XppCompilerExecuteExample(Common _buf) 
{ 
    XppCompiler       xpp; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    xpp = new XppCompiler(); 
    if (xpp != null) 
    { 
        xpp.execute(_buf); 
    } 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-executeex"></a><span data-ttu-id="fbf31-173">メソッド executeEx</span><span class="sxs-lookup"><span data-stu-id="fbf31-173">Method executeEx</span></span>

```xpp
public AnyType executeEx()
```

### <a name="return-value---executeex"></a><span data-ttu-id="fbf31-174">戻り値 - executeEx</span><span class="sxs-lookup"><span data-stu-id="fbf31-174">Return Value - executeEx</span></span>

### <a name="remarks---executeex"></a><span data-ttu-id="fbf31-175">備考 - executeEx</span><span class="sxs-lookup"><span data-stu-id="fbf31-175">Remarks - executeEx</span></span>

<span data-ttu-id="fbf31-176">XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-176">XppCompiler objects can compile code at run time.</span></span> <span data-ttu-id="fbf31-177">これはセキュリティ リスクをもたらします。</span><span class="sxs-lookup"><span data-stu-id="fbf31-177">This presents a security risk.</span></span> <span data-ttu-id="fbf31-178">したがって、executeEx メソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-178">Therefore, the executeEx method runs under Code Access Security.</span></span> <span data-ttu-id="fbf31-179">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-179">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="fbf31-180">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-180">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---executeex"></a><span data-ttu-id="fbf31-181">例 - executeEx</span><span class="sxs-lookup"><span data-stu-id="fbf31-181">Examples - executeEx</span></span>

```xpp
void XppCompilerExecuteExExample() 
{ 
    XppCompiler       xpp; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    xpp = new XppCompiler(); 
    if (xpp != null) 
    { 
        xpp.executeEx(); 
    } 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-setguidarg"></a><span data-ttu-id="fbf31-182">メソッド setGuidArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-182">Method setGuidArg</span></span>

```xpp
public void setGuidArg(Guid arg)
```

### <a name="parameters---setguidarg"></a><span data-ttu-id="fbf31-183">パラメーター - setGuidArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-183">Parameters - setGuidArg</span></span>

<span data-ttu-id="fbf31-184">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-184">arg</span></span>  

## <a name="method-setint64arg"></a><span data-ttu-id="fbf31-185">メソッド setInt64Arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-185">Method setInt64Arg</span></span>

```xpp
public void setInt64Arg(Int64 arg)
```

### <a name="parameters---setint64arg"></a><span data-ttu-id="fbf31-186">パラメーター - setInt64Arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-186">Parameters - setInt64Arg</span></span>

<span data-ttu-id="fbf31-187">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-187">arg</span></span>  

## <a name="method-setdatearg"></a><span data-ttu-id="fbf31-188">メソッド setDateArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-188">Method setDateArg</span></span>

```xpp
public void setDateArg(Date arg)
```

### <a name="parameters---setdatearg"></a><span data-ttu-id="fbf31-189">パラメーター - setDateArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-189">Parameters - setDateArg</span></span>

<span data-ttu-id="fbf31-190">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-190">arg</span></span>  

## <a name="method-new"></a><span data-ttu-id="fbf31-191">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fbf31-191">Method new</span></span>

<span data-ttu-id="fbf31-192">XppCompiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fbf31-192">Initializes a new instance of the XppCompiler class.</span></span>

```xpp
public void new()
```

### <a name="remarks---new"></a><span data-ttu-id="fbf31-193">備考 - new</span><span class="sxs-lookup"><span data-stu-id="fbf31-193">Remarks - new</span></span>

<span data-ttu-id="fbf31-194">XppCompiler クラスのインスタンスは、実行時にコードをコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-194">Instances of the XppCompiler class can compile code at run time.</span></span> <span data-ttu-id="fbf31-195">これはセキュリティ リスクを提示するため、新しいメソッドはコード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fbf31-195">Because this presents a security risk, the new method runs under Code Access Security.</span></span> <span data-ttu-id="fbf31-196">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="fbf31-196">Calls to this method on the server require permission from the ExecutePermission Class.</span></span>

## <a name="method-endargs"></a><span data-ttu-id="fbf31-197">メソッド endArgs</span><span class="sxs-lookup"><span data-stu-id="fbf31-197">Method endArgs</span></span>

```xpp
public void endArgs()
```

## <a name="method-startargs"></a><span data-ttu-id="fbf31-198">メソッド startArgs</span><span class="sxs-lookup"><span data-stu-id="fbf31-198">Method startArgs</span></span>

```xpp
public void startArgs()
```

## <a name="method-setrealarg"></a><span data-ttu-id="fbf31-199">メソッド setRealArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-199">Method setRealArg</span></span>

```xpp
public void setRealArg(Real arg)
```

### <a name="parameters---setrealarg"></a><span data-ttu-id="fbf31-200">パラメーター - setRealArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-200">Parameters - setRealArg</span></span>

<span data-ttu-id="fbf31-201">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-201">arg</span></span>  

## <a name="method-setintarg"></a><span data-ttu-id="fbf31-202">メソッド setIntArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-202">Method setIntArg</span></span>

```xpp
public void setIntArg(int arg)
```

### <a name="parameters---setintarg"></a><span data-ttu-id="fbf31-203">パラメーター - setIntArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-203">Parameters - setIntArg</span></span>

<span data-ttu-id="fbf31-204">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-204">arg</span></span>  

## <a name="method-setstrarg"></a><span data-ttu-id="fbf31-205">メソッド setStrArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-205">Method setStrArg</span></span>

```xpp
public void setStrArg(str arg)
```

### <a name="parameters---setstrarg"></a><span data-ttu-id="fbf31-206">パラメーター - setStrArg</span><span class="sxs-lookup"><span data-stu-id="fbf31-206">Parameters - setStrArg</span></span>

<span data-ttu-id="fbf31-207">arg</span><span class="sxs-lookup"><span data-stu-id="fbf31-207">arg</span></span>  

