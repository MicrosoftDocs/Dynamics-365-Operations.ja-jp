---
title: DLLFunction クラス
description: このトピックでは、DLLFunction クラスについて説明します。
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
ms.openlocfilehash: 9ef1ff41742eca42ab9cdad08ed94dfadb019fba
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502743"
---
# <a name="class-dllfunction"></a><span data-ttu-id="c3907-103">クラス DLLFunction</span><span class="sxs-lookup"><span data-stu-id="c3907-103">Class DLLFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DLLFunction extends Object
```

## <a name="remarks"></a><span data-ttu-id="c3907-104">備考</span><span class="sxs-lookup"><span data-stu-id="c3907-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c3907-105">例</span><span class="sxs-lookup"><span data-stu-id="c3907-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c3907-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c3907-106">Methods</span></span>

| <span data-ttu-id="c3907-107">方法</span><span class="sxs-lookup"><span data-stu-id="c3907-107">Method</span></span>                                           | <span data-ttu-id="c3907-108">説明</span><span class="sxs-lookup"><span data-stu-id="c3907-108">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="c3907-109">public AnyType call(VarArg )</span><span class="sxs-lookup"><span data-stu-id="c3907-109">public AnyType call(VarArg )</span></span>                     |                                                 |
| <span data-ttu-id="c3907-110">public ExtTypes returns(\[ExtTypes returnType\])</span><span class="sxs-lookup"><span data-stu-id="c3907-110">public ExtTypes returns(\[ExtTypes returnType\])</span></span> |                                                 |
| <span data-ttu-id="c3907-111">public void new(DLL dll, str functionname)</span><span class="sxs-lookup"><span data-stu-id="c3907-111">public void new(DLL dll, str functionname)</span></span>       | <span data-ttu-id="c3907-112">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c3907-112">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="c3907-113">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="c3907-113">public void finalize()</span></span>                           |                                                 |
| <span data-ttu-id="c3907-114">public void arg(VarArg )</span><span class="sxs-lookup"><span data-stu-id="c3907-114">public void arg(VarArg )</span></span>                         |                                                 |

## <a name="method-call"></a><span data-ttu-id="c3907-115">メソッド call</span><span class="sxs-lookup"><span data-stu-id="c3907-115">Method call</span></span>

```xpp
public AnyType call(VarArg )
```

### <a name="parameters---call"></a><span data-ttu-id="c3907-116">パラメーター - call</span><span class="sxs-lookup"><span data-stu-id="c3907-116">Parameters - call</span></span>


### <a name="return-value---call"></a><span data-ttu-id="c3907-117">戻り値 - call</span><span class="sxs-lookup"><span data-stu-id="c3907-117">Return Value - call</span></span>

### <a name="remarks---call"></a><span data-ttu-id="c3907-118">備考 - call</span><span class="sxs-lookup"><span data-stu-id="c3907-118">Remarks - call</span></span>

<span data-ttu-id="c3907-119">攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="c3907-119">If an attacker can control input to the call method, a security risk exists.</span></span> <span data-ttu-id="c3907-120">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="c3907-120">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="c3907-121">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="c3907-121">Calls to this method on the server require permission.</span></span> <span data-ttu-id="c3907-122">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3907-122">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---call"></a><span data-ttu-id="c3907-123">例 - call</span><span class="sxs-lookup"><span data-stu-id="c3907-123">Examples - call</span></span>

<span data-ttu-id="c3907-124">次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。</span><span class="sxs-lookup"><span data-stu-id="c3907-124">The following example uses the DLL and DLLFunction classes to interoperate with the GetVersion API in Kernel32.dll.</span></span> <span data-ttu-id="c3907-125">コードのアクセス保護を提供する InteropPermission クラスの使用をアサートして、DLL をロードします。</span><span class="sxs-lookup"><span data-stu-id="c3907-125">It asserts the use of the InteropPermission class to provide code access protection, and then it loads the DLL.</span></span> <span data-ttu-id="c3907-126">これが成功した場合は、戻り値の型は DLLFunction クラスの呼び出しからを設定されます。</span><span class="sxs-lookup"><span data-stu-id="c3907-126">If this is successful, the return type is set from the call to the DLLFunction class.</span></span>

```xpp
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method. 
    // DLL.new is protected by code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        // Grants permission to execute the DLLFunction.new method. 
        // DLLFunction.new is protected by code access security. 
        perm = new InteropPermission(InteropKind::DllInterop); 
        perm.assert(); 
        dllFunc = new DllFunction(dll, "GetVersion"); 
        if (dllFunc != null) 
         { 
            dllFunc.returns(ExtTypes::DWord); 
             retVal = dllFunc.call(); 
         } 
       // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    } 
}
```

## <a name="method-returns"></a><span data-ttu-id="c3907-127">メソッド returns</span><span class="sxs-lookup"><span data-stu-id="c3907-127">Method returns</span></span>

```xpp
public ExtTypes returns([ExtTypes returnType])
```

### <a name="parameters---returns"></a><span data-ttu-id="c3907-128">パラメーター - returns</span><span class="sxs-lookup"><span data-stu-id="c3907-128">Parameters - returns</span></span>

<span data-ttu-id="c3907-129">returnType</span><span class="sxs-lookup"><span data-stu-id="c3907-129">returnType</span></span>  

### <a name="return-value---returns"></a><span data-ttu-id="c3907-130">戻り値 - returns</span><span class="sxs-lookup"><span data-stu-id="c3907-130">Return Value - returns</span></span>

## <a name="method-new"></a><span data-ttu-id="c3907-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c3907-131">Method new</span></span>

<span data-ttu-id="c3907-132">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c3907-132">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(DLL dll, str functionname)
```

### <a name="parameters---new"></a><span data-ttu-id="c3907-133">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c3907-133">Parameters - new</span></span>

<span data-ttu-id="c3907-134">dll</span><span class="sxs-lookup"><span data-stu-id="c3907-134">dll</span></span>  

<!-- -->

<span data-ttu-id="c3907-135">functionname</span><span class="sxs-lookup"><span data-stu-id="c3907-135">functionname</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="c3907-136">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="c3907-136">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-arg"></a><span data-ttu-id="c3907-137">メソッド arg</span><span class="sxs-lookup"><span data-stu-id="c3907-137">Method arg</span></span>

```xpp
public void arg(VarArg )
```

### <a name="parameters---arg"></a><span data-ttu-id="c3907-138">パラメーター - arg</span><span class="sxs-lookup"><span data-stu-id="c3907-138">Parameters - arg</span></span>


