---
title: SkipAOSValidationPermission クラス
description: このトピックでは、SkipAOSValidationPermission クラスについて説明します。
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
ms.openlocfilehash: 47015972341df712217dc11f6c8803a059dbec7e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502802"
---
# <a name="class-skipaosvalidationpermission"></a><span data-ttu-id="a4a6b-103">クラス SkipAOSValidationPermission</span><span class="sxs-lookup"><span data-stu-id="a4a6b-103">Class SkipAOSValidationPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SkipAOSValidationPermission extends CodeAccessPermission
```

<span data-ttu-id="a4a6b-104">SkipAOSValidationPermission クラスは、AOS 検証を省略して、特定の API のアクセス許可をチェックする機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-104">The SkipAOSValidationPermission class controls the ability to skip AOS validation and check permissions for specific APIs.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4a6b-105">備考</span><span class="sxs-lookup"><span data-stu-id="a4a6b-105">Remarks</span></span>

<span data-ttu-id="a4a6b-106">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-106">For a list of all protected APIs, see Secured APIs.</span></span> <span data-ttu-id="a4a6b-107">保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-107">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission.demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="a4a6b-108">次のいずれかでサーバー層のメソッドを呼び出します: サーバー静的メソッドまたは RunOn クラス プロパティを使用してサーバー上で実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-108">Call a method on the server tier from one of the following: A server static method �or� A class instance method that is set to run on the server by using the RunOn class property.</span></span>

## <a name="examples"></a><span data-ttu-id="a4a6b-109">例</span><span class="sxs-lookup"><span data-stu-id="a4a6b-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a4a6b-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="a4a6b-110">Methods</span></span>

| <span data-ttu-id="a4a6b-111">方法</span><span class="sxs-lookup"><span data-stu-id="a4a6b-111">Method</span></span>                                                 | <span data-ttu-id="a4a6b-112">説明</span><span class="sxs-lookup"><span data-stu-id="a4a6b-112">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a6b-113">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="a4a6b-113">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="a4a6b-114">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-114">Creates and returns a copy of a permission class object.</span></span>                                                            |
| <span data-ttu-id="a4a6b-115">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="a4a6b-115">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="a4a6b-116">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-116">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span> |
| <span data-ttu-id="a4a6b-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="a4a6b-117">public void new()</span></span>                                      | <span data-ttu-id="a4a6b-118">SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-118">Initializes a new instance of the SkipAOSValidationPermission class.</span></span>                                                |

## <a name="method-copy"></a><span data-ttu-id="a4a6b-119">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="a4a6b-119">Method copy</span></span>

<span data-ttu-id="a4a6b-120">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-120">Creates and returns a copy of a permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="a4a6b-121">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="a4a6b-121">Return Value - copy</span></span>

<span data-ttu-id="a4a6b-122">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-122">A copy of the derived class object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="a4a6b-123">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="a4a6b-123">Remarks - copy</span></span>

<span data-ttu-id="a4a6b-124">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-124">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="a4a6b-125">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-125">For more information, see .</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="a4a6b-126">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="a4a6b-126">Method isSubsetOf</span></span>

<span data-ttu-id="a4a6b-127">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-127">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="a4a6b-128">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="a4a6b-128">Parameters - isSubsetOf</span></span>

<span data-ttu-id="a4a6b-129">target</span><span class="sxs-lookup"><span data-stu-id="a4a6b-129">target</span></span>  
<span data-ttu-id="a4a6b-130">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-130">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="a4a6b-131">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="a4a6b-131">Return Value - isSubsetOf</span></span>

<span data-ttu-id="a4a6b-132">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-132">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="a4a6b-133">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="a4a6b-133">Remarks - isSubsetOf</span></span>

<span data-ttu-id="a4a6b-134">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-134">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="a4a6b-135">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-135">For more information, see .</span></span>

## <a name="method-new"></a><span data-ttu-id="a4a6b-136">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a4a6b-136">Method new</span></span>

<span data-ttu-id="a4a6b-137">SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-137">Initializes a new instance of the SkipAOSValidationPermission class.</span></span>

```xpp
public void new()
```

### <a name="examples---new"></a><span data-ttu-id="a4a6b-138">例 - new</span><span class="sxs-lookup"><span data-stu-id="a4a6b-138">Examples - new</span></span>

<span data-ttu-id="a4a6b-139">次のコード例は、SkipAOSValidationPermission クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a4a6b-139">The following code example demonstrates how to create an instance of the SkipAOSValidationPermission class.</span></span>

```xpp
server static void main(Args args) 
{ 
    SkipAOSValidationPermission perm; 
    ; 
    perm = new SkipAOSValidationPermission(); 
}
```

