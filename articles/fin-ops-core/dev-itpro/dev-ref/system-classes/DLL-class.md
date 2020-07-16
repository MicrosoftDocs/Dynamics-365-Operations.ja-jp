---
title: DLL クラス
description: このトピックでは、DLL クラスについて説明します。
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
ms.openlocfilehash: db06244b679d4e59bca6e1ab2841e2c5861014bb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502698"
---
# <a name="class-dll"></a><span data-ttu-id="1cbbb-103">クラス DLL</span><span class="sxs-lookup"><span data-stu-id="1cbbb-103">Class DLL</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DLL extends Object
```

<span data-ttu-id="1cbbb-104">DLL クラスでは、Microsoft Windows 動的リンク ライブラリ (DLL) との通信が有効になります。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-104">The DLL class enables communication with a Microsoft Windows dynamic-link library (DLL).</span></span>

## <a name="remarks"></a><span data-ttu-id="1cbbb-105">備考</span><span class="sxs-lookup"><span data-stu-id="1cbbb-105">Remarks</span></span>

<span data-ttu-id="1cbbb-106">Unicode DLL を使用している場合は、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-106">If you are using a Unicode DLL, do the following:</span></span>

-   <span data-ttu-id="1cbbb-107">ExtTypes::String の代わりに ExtTypes::WString を使用して、文字列型を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-107">Use ExtTypes::WString instead of ExtTypes::String to specify a string type.</span></span>
-   <span data-ttu-id="1cbbb-108">文字データがバイナリ構造に埋め込まれている場合は、Binary::String ではなく Binary::WString を使用します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-108">Use Binary::WString instead of Binary::String if you have character data embedded in a binary structure.</span></span>
-   <span data-ttu-id="1cbbb-109">バイナリオ オブジェクトから文字列を読み取る必要がある場合は、Binary.string メソッドの代わりに Binary.wstring メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-109">Use the Binary.wstring method instead of the Binary.string method if you have to read a string from a binary object.</span></span>

## <a name="examples"></a><span data-ttu-id="1cbbb-110">例</span><span class="sxs-lookup"><span data-stu-id="1cbbb-110">Examples</span></span>

<span data-ttu-id="1cbbb-111">次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-111">The following example uses the DLL and DLLFunction classes to interoperate with the GetVersion API in Kernel32.dll.</span></span> <span data-ttu-id="1cbbb-112">この例では、コードがサーバー上で実行されている場合にのみ必要な InteropPermission クラスの使用をアサートします。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-112">This example asserts the use of the InteropPermission class, which is required only if the code is running on the server.</span></span> <span data-ttu-id="1cbbb-113">DLL を読み込み、成功した場合は DLLFunction クラスの呼び出しから戻り値の型を設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-113">It loads the DLL and, if it is successful, sets the return type from the call to the DLLFunction class.</span></span>

```xpp
void DLLExample() 
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method.  
    // DLL.new runs under code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLLFunction.new method.  
    // DLLFunction.new runs under code access security. 
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

## <a name="methods"></a><span data-ttu-id="1cbbb-114">方法</span><span class="sxs-lookup"><span data-stu-id="1cbbb-114">Methods</span></span>

| <span data-ttu-id="1cbbb-115">方法</span><span class="sxs-lookup"><span data-stu-id="1cbbb-115">Method</span></span>                             | <span data-ttu-id="1cbbb-116">説明</span><span class="sxs-lookup"><span data-stu-id="1cbbb-116">Description</span></span>                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbbb-117">::public static int lastDLLError()</span><span class="sxs-lookup"><span data-stu-id="1cbbb-117">::public static int lastDLLError()</span></span> | <span data-ttu-id="1cbbb-118">DLL によって報告された最後のエラーを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-118">Sets or retrieves the last error that was reported by the DLL.</span></span>                            |
| <span data-ttu-id="1cbbb-119">public void new(str filename)</span><span class="sxs-lookup"><span data-stu-id="1cbbb-119">public void new(str filename)</span></span>      | <span data-ttu-id="1cbbb-120">DLL クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-120">Creates an instance of the DLL class.</span></span>                                                     |
| <span data-ttu-id="1cbbb-121">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="1cbbb-121">public void finalize()</span></span>             | <span data-ttu-id="1cbbb-122">リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-122">Releases resources and performs clean-up before an instance of the DLL class is released.</span></span> |

## <a name="method-lastdllerror"></a><span data-ttu-id="1cbbb-123">メソッド lastDLLError</span><span class="sxs-lookup"><span data-stu-id="1cbbb-123">Method lastDLLError</span></span>

<span data-ttu-id="1cbbb-124">DLL によって報告された最後のエラーを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-124">Sets or retrieves the last error that was reported by the DLL.</span></span>

```xpp
public static int lastDLLError()
```

### <a name="return-value---lastdllerror"></a><span data-ttu-id="1cbbb-125">戻り値 - lastDLLError</span><span class="sxs-lookup"><span data-stu-id="1cbbb-125">Return Value - lastDLLError</span></span>

<span data-ttu-id="1cbbb-126">DLL によって報告された最後のエラー。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-126">The last error that was reported by the DLL.</span></span>

## <a name="method-new"></a><span data-ttu-id="1cbbb-127">メソッド new</span><span class="sxs-lookup"><span data-stu-id="1cbbb-127">Method new</span></span>

<span data-ttu-id="1cbbb-128">DLL クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-128">Creates an instance of the DLL class.</span></span>

```xpp
public void new(str filename)
```

### <a name="parameters---new"></a><span data-ttu-id="1cbbb-129">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="1cbbb-129">Parameters - new</span></span>

<span data-ttu-id="1cbbb-130">filename</span><span class="sxs-lookup"><span data-stu-id="1cbbb-130">filename</span></span>  
<span data-ttu-id="1cbbb-131">DLL クラスのインスタンスを作成するために使用する DLL のファイル名。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-131">The file name of the DLL to use to create the instance of the DLL class.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="1cbbb-132">備考 - new</span><span class="sxs-lookup"><span data-stu-id="1cbbb-132">Remarks - new</span></span>

<span data-ttu-id="1cbbb-133">DLL 関数にアクセスするには、DLLFunction::new メソッドの呼び出しで、その DLL クラスの作成されたインスタンスを使用します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-133">To access a DLL function, use a created instance of the DLL class in a call to the DLLFunction::new method.</span></span> <span data-ttu-id="1cbbb-134">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-134">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="1cbbb-135">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-135">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="1cbbb-136">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-136">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="1cbbb-137">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-137">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="1cbbb-138">例 - new</span><span class="sxs-lookup"><span data-stu-id="1cbbb-138">Examples - new</span></span>

<span data-ttu-id="1cbbb-139">次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-139">The following example uses the DLL and DLLFunction classes to interoperate with the GetVersion API in Kernel32.dll.</span></span> <span data-ttu-id="1cbbb-140">この例では、InteropPermission クラスの使用をアサートします。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-140">This example asserts the use of the InteropPermission class.</span></span> <span data-ttu-id="1cbbb-141">DLL を読み込み、成功した場合は DLLFunction クラスでの呼び出しから戻り値の型を設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-141">It loads the DLL and, if it is successful, sets the return type from the call in the DLLFunction class.</span></span>

```xpp
void DLLExample() 
{ 
    Dll               dll; 
    DllFunction       dllFunc; 
    anytype           retVal; 
    InteropPermission perm; 
    perm = new InteropPermission(InteropKind::DllInterop); 
    // Grants permission to execute the DLL.new method. 
    // DLL.new runs under code access security. 
    perm.assert(); 
    dll = new Dll("Kernel32.dll"); 
    // Closes the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    if (dll != null) 
    { 
        perm = new InteropPermission(InteropKind::DllInterop); 
       // Grants permission to execute the DLLFunction.new method. 
       // DLLFunction.new runs under code access security. 
        perm.assert(); 
        dllFunc = new DllFunction(dll, "GetVersion"); 
        if (dllFunc != null) 
        { 
             dllFunc.returns(ExtTypes::DWord); 
            retVal = dllFunc.call(); 
        } 
        // Close the code access permission scope. 
       CodeAccessPermission::revertAssert(); 
    } 
}
```

## <a name="method-finalize"></a><span data-ttu-id="1cbbb-142">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="1cbbb-142">Method finalize</span></span>

<span data-ttu-id="1cbbb-143">リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="1cbbb-143">Releases resources and performs clean-up before an instance of the DLL class is released.</span></span>

```xpp
public void finalize()
```

