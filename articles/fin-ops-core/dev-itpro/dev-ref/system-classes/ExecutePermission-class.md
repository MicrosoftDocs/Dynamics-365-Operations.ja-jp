---
title: ExecutePermission クラス
description: このトピックでは、ExecutePermission クラスについて説明します。
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
ms.openlocfilehash: 5b6c6c35e9d20bad3afc2cdb451bde093a0e3629
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502668"
---
# <a name="class-executepermission"></a><span data-ttu-id="2e064-103">クラス ExecutePermission</span><span class="sxs-lookup"><span data-stu-id="2e064-103">Class ExecutePermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ExecutePermission extends CodeAccessPermission
```

<span data-ttu-id="2e064-104">ExecutePermission クラスは、X++ コードの実行を制御します。</span><span class="sxs-lookup"><span data-stu-id="2e064-104">The ExecutePermission class controls the execution of X++ code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e064-105">備考</span><span class="sxs-lookup"><span data-stu-id="2e064-105">Remarks</span></span>

<span data-ttu-id="2e064-106">このクラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="2e064-106">This class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="2e064-107">アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e064-107">For a list of all APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="2e064-108">保護された API が実行される前に、対応する CodeAccessPermission::dema メソッドが呼び出される同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e064-108">Before the protected API is executed, you must call the assert method on the same tier (which is usually the server tier) that the corresponding CodeAccessPermission::demand method is called on.</span></span> <span data-ttu-id="2e064-109">次のいずれかの方法でサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="2e064-109">Call a method on the server tier from one of the following methods:</span></span>

-   <span data-ttu-id="2e064-110">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="2e064-110">A server static method</span></span>
-   <span data-ttu-id="2e064-111">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="2e064-111">A class instance method that is set to run on the server by using the RunOn class property</span></span>

## <a name="examples"></a><span data-ttu-id="2e064-112">例</span><span class="sxs-lookup"><span data-stu-id="2e064-112">Examples</span></span>

<span data-ttu-id="2e064-113">次のコード例は、ExecutePermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="2e064-113">The following code example shows a new instance of the ExecutePermission class.</span></span> <span data-ttu-id="2e064-114">assert メソッドが呼び出され、コードが Thread.new メソッドを呼び出して新規スレッドを作成できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="2e064-114">The assert method is called to declare that the code can then call the Thread.new method to create a new thread.</span></span>

```xpp
server static void main(Args args) 
{ 
    Thread _t; 
    ExecutePermission _perm; 
    _perm = new ExecutePermission(); 
    if (!_perm) 
    { 
        return; 
    } 
    _perm.assert(); 
    // Invoke the protected API. 
     _t = new Thread(); 
    // Call member methods. 
    if (_t) 
    { 
        _t.removeOnComplete(true); 
        _t.run(classnum(SysCodeProfiler), identifierstr(transferFile)); 
    } 
    // Optionally, call revertAssert() to limit scope of assert. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a><span data-ttu-id="2e064-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="2e064-115">Methods</span></span>

| <span data-ttu-id="2e064-116">方法</span><span class="sxs-lookup"><span data-stu-id="2e064-116">Method</span></span>                                                 | <span data-ttu-id="2e064-117">説明</span><span class="sxs-lookup"><span data-stu-id="2e064-117">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e064-118">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="2e064-118">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="2e064-119">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="2e064-119">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="2e064-120">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="2e064-120">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="2e064-121">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e064-121">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="2e064-122">public void new()</span><span class="sxs-lookup"><span data-stu-id="2e064-122">public void new()</span></span>                                      | <span data-ttu-id="2e064-123">ExecutePermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2e064-123">Initializes a new instance of the ExecutePermission class.</span></span>                       |

## <a name="method-copy"></a><span data-ttu-id="2e064-124">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="2e064-124">Method copy</span></span>

<span data-ttu-id="2e064-125">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="2e064-125">Creates and returns a copy of the current permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="2e064-126">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="2e064-126">Return Value - copy</span></span>

<span data-ttu-id="2e064-127">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="2e064-127">A copy of the current permission object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="2e064-128">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="2e064-128">Remarks - copy</span></span>

<span data-ttu-id="2e064-129">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="2e064-129">You override this method when you derive a class from the CodeAccessPermission class.</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="2e064-130">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="2e064-130">Method isSubsetOf</span></span>

<span data-ttu-id="2e064-131">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2e064-131">Determines whether a current permission is a subset of the specified permission.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="2e064-132">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="2e064-132">Parameters - isSubsetOf</span></span>

<span data-ttu-id="2e064-133">target</span><span class="sxs-lookup"><span data-stu-id="2e064-133">target</span></span>  
<span data-ttu-id="2e064-134">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="2e064-134">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="2e064-135">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="2e064-135">Return Value - isSubsetOf</span></span>

<span data-ttu-id="2e064-136">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2e064-136">true if a current permission is a subset of the specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="2e064-137">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="2e064-137">Remarks - isSubsetOf</span></span>

<span data-ttu-id="2e064-138">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="2e064-138">You override this method when you derive a class from the CodeAccessPermission class.</span></span>

## <a name="method-new"></a><span data-ttu-id="2e064-139">メソッド new</span><span class="sxs-lookup"><span data-stu-id="2e064-139">Method new</span></span>

<span data-ttu-id="2e064-140">ExecutePermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2e064-140">Initializes a new instance of the ExecutePermission class.</span></span> <span data-ttu-id="2e064-141">終了。</span><span class="sxs-lookup"><span data-stu-id="2e064-141">End.</span></span>

```xpp
public void new()
```


