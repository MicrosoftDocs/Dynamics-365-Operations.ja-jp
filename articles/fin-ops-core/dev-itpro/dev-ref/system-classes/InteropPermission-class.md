---
title: InteropPermission クラス
description: このトピックでは、InteropPermission クラスについて説明します。
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
ms.openlocfilehash: 599d2bfeba84107e6868732a64658e76b3f8409d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502596"
---
# <a name="class-interoppermission"></a><span data-ttu-id="4a6ea-103">クラス InteropPermission</span><span class="sxs-lookup"><span data-stu-id="4a6ea-103">Class InteropPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class InteropPermission extends CodeAccessPermission
```

<span data-ttu-id="4a6ea-104">InteropPermission クラスは、アンマネージド コードとマネージド コードを呼び出す機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-104">The InteropPermission class controls the ability to call unmanaged and managed code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6ea-105">備考</span><span class="sxs-lookup"><span data-stu-id="4a6ea-105">Remarks</span></span>

<span data-ttu-id="4a6ea-106">InteropPermission クラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-106">The InteropPermission class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="4a6ea-107">アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-107">For a list of all APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="4a6ea-108">保護された API を実行する前に、対応する CodeAccessPermission::demand メソッドが呼び出されている同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-108">Before the protected API is run, you must call the assert method on the same tier (usually the server tier) that the corresponding CodeAccessPermission::demand method is called on.</span></span> <span data-ttu-id="4a6ea-109">次のいずれかの方法でサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="4a6ea-109">Call a method on the server tier from one of the following methods:</span></span>

-   <span data-ttu-id="4a6ea-110">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="4a6ea-110">A server static method</span></span>
-   <span data-ttu-id="4a6ea-111">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-111">A class instance method that is set to run on the server by using the RunOn class property.</span></span>

## <a name="examples"></a><span data-ttu-id="4a6ea-112">例</span><span class="sxs-lookup"><span data-stu-id="4a6ea-112">Examples</span></span>

<span data-ttu-id="4a6ea-113">次のコード例は、InteropPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-113">The following code example shows a new instance of the InteropPermission class.</span></span> <span data-ttu-id="4a6ea-114">assert メソッドが呼び出され、コードが、Microsoft Windows ダイナミックリンク ライブラリ (DLL) と通信する機能を提供する DLL クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-114">The assert method is called to declare that the code can then instantiate the DLL class that provides the ability to communicate with a Microsoft Windows dynamic-link library (DLL).</span></span>

```xpp
server static void main(Args args) 
{ 
    InteropPermission _perm; 
    DLL _dll; 
    _perm = new InteropPermission(InteropKind::DllInterop); 
    _perm.assert(); 
    // Invoke the protected API. 
    _dll = new DLL('cfx2032.dll'); 
    // Optionally, call revertAssert() to limit the scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="4a6ea-115">方法</span><span class="sxs-lookup"><span data-stu-id="4a6ea-115">Methods</span></span>

| <span data-ttu-id="4a6ea-116">方法</span><span class="sxs-lookup"><span data-stu-id="4a6ea-116">Method</span></span>                                                 | <span data-ttu-id="4a6ea-117">説明</span><span class="sxs-lookup"><span data-stu-id="4a6ea-117">Description</span></span>                                                                        |
|--------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6ea-118">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="4a6ea-118">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="4a6ea-119">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-119">Creates and returns a copy of the current permission class object.</span></span>                 |
| <span data-ttu-id="4a6ea-120">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="4a6ea-120">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="4a6ea-121">現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-121">Determines whether the current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="4a6ea-122">public void new(InteropKind kind)</span><span class="sxs-lookup"><span data-stu-id="4a6ea-122">public void new(InteropKind kind)</span></span>                      | <span data-ttu-id="4a6ea-123">InteropPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-123">Creates a new instance of the InteropPermission class.</span></span>                            |

## <a name="method-copy"></a><span data-ttu-id="4a6ea-124">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="4a6ea-124">Method copy</span></span>

<span data-ttu-id="4a6ea-125">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-125">Creates and returns a copy of the current permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="4a6ea-126">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="4a6ea-126">Return Value - copy</span></span>

<span data-ttu-id="4a6ea-127">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-127">A copy of the current permission object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="4a6ea-128">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="4a6ea-128">Remarks - copy</span></span>

<span data-ttu-id="4a6ea-129">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-129">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="4a6ea-130">詳細については、「メソッドのコピー」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-130">For more information, see the copy method.</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="4a6ea-131">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4a6ea-131">Method isSubsetOf</span></span>

<span data-ttu-id="4a6ea-132">現在のアクセス許可が指定のアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-132">Determines whether the current permission is a subset of the specified permission.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="4a6ea-133">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4a6ea-133">Parameters - isSubsetOf</span></span>

<span data-ttu-id="4a6ea-134">target</span><span class="sxs-lookup"><span data-stu-id="4a6ea-134">target</span></span>  
<span data-ttu-id="4a6ea-135">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-135">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="4a6ea-136">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4a6ea-136">Return Value - isSubsetOf</span></span>

<span data-ttu-id="4a6ea-137">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-137">true if the current permission is a subset of the specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="4a6ea-138">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4a6ea-138">Remarks - isSubsetOf</span></span>

<span data-ttu-id="4a6ea-139">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-139">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="4a6ea-140">詳細については、「isSubsetOf メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-140">For more information, see the isSubsetOf method.</span></span>

## <a name="method-new"></a><span data-ttu-id="4a6ea-141">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4a6ea-141">Method new</span></span>

<span data-ttu-id="4a6ea-142">InteropPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-142">Creates a new instance of the InteropPermission class.</span></span>

```xpp
public void new(InteropKind kind)
```

### <a name="parameters---new"></a><span data-ttu-id="4a6ea-143">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="4a6ea-143">Parameters - new</span></span>

<span data-ttu-id="4a6ea-144">kind</span><span class="sxs-lookup"><span data-stu-id="4a6ea-144">kind</span></span>  
<span data-ttu-id="4a6ea-145">マネージドまたはアンマネージド コードへのアクセスを指定する InteropKind システム列挙値です。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-145">An InteropKind system enumeration value that specifies access to managed or unmanaged code.</span></span>

### <a name="examples---new"></a><span data-ttu-id="4a6ea-146">例 - new</span><span class="sxs-lookup"><span data-stu-id="4a6ea-146">Examples - new</span></span>

<span data-ttu-id="4a6ea-147">次のコード例は、Win32 DLL へのアクセス許可を指定する InteropPermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="4a6ea-147">The following code example shows a new instance of the InteropPermission class that specifies access to Win32 DLLs.</span></span>

```xpp
server static void main(Args args) 
{ 
    InteropPermission _perm; 
    _perm = new InteropPermission(InteropKind::DllInterop); 
}
```

