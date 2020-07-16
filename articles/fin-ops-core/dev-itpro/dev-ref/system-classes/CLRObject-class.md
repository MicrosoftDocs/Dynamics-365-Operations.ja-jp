---
title: CLRObject クラス
description: このトピックでは、CLRObject クラスについて説明します。
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
ms.openlocfilehash: d6edf1e79b28908a8079adff4459b2b6849ac0b1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502714"
---
# <a name="class-clrobject"></a><span data-ttu-id="71bb5-103">クラス CLRObject</span><span class="sxs-lookup"><span data-stu-id="71bb5-103">Class CLRObject</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CLRObject extends Object
```

<span data-ttu-id="71bb5-104">CLRObject クラスは、共通言語ランタイム (CLR) オブジェクトのインスタンスへの参照を保持し、X++ からの呼び出しを対応するラップされたマネージド インスタンスにディスパッチします。</span><span class="sxs-lookup"><span data-stu-id="71bb5-104">The CLRObject class holds a reference to an instance of a common language runtime (CLR) object and dispatches calls from X++ to the corresponding wrapped managed instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="71bb5-105">備考</span><span class="sxs-lookup"><span data-stu-id="71bb5-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="71bb5-106">例</span><span class="sxs-lookup"><span data-stu-id="71bb5-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="71bb5-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="71bb5-107">Methods</span></span>

| <span data-ttu-id="71bb5-108">方法</span><span class="sxs-lookup"><span data-stu-id="71bb5-108">Method</span></span>                                            | <span data-ttu-id="71bb5-109">説明</span><span class="sxs-lookup"><span data-stu-id="71bb5-109">Description</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="71bb5-110">private CLRObject dispatch(VarArg )</span><span class="sxs-lookup"><span data-stu-id="71bb5-110">private CLRObject dispatch(VarArg )</span></span>               | <span data-ttu-id="71bb5-111">予約済み: メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="71bb5-111">Reserved: Do not explicitly call this method.</span></span> |
| <span data-ttu-id="71bb5-112">public void new(str className, \[VarArg params\])</span><span class="sxs-lookup"><span data-stu-id="71bb5-112">public void new(str className, \[VarArg params\])</span></span> | <span data-ttu-id="71bb5-113">CLRObject クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-113">Creates an instance of the CLRObject class.</span></span>   |

## <a name="method-dispatch"></a><span data-ttu-id="71bb5-114">メソッド dispatch</span><span class="sxs-lookup"><span data-stu-id="71bb5-114">Method dispatch</span></span>

<span data-ttu-id="71bb5-115">予約済み: メソッドを明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="71bb5-115">Reserved: Do not explicitly call this method.</span></span>

```xpp
private CLRObject dispatch(VarArg )
```

### <a name="parameters---dispatch"></a><span data-ttu-id="71bb5-116">パラメーター - dispatch</span><span class="sxs-lookup"><span data-stu-id="71bb5-116">Parameters - dispatch</span></span>


### <a name="return-value---dispatch"></a><span data-ttu-id="71bb5-117">戻り値 - dispatch</span><span class="sxs-lookup"><span data-stu-id="71bb5-117">Return Value - dispatch</span></span>

### <a name="remarks---dispatch"></a><span data-ttu-id="71bb5-118">備考 - dispatch</span><span class="sxs-lookup"><span data-stu-id="71bb5-118">Remarks - dispatch</span></span>

<span data-ttu-id="71bb5-119">攻撃者が出荷メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-119">If an attacker can control input to the dispatch method, a security risk exists.</span></span> <span data-ttu-id="71bb5-120">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="71bb5-120">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="71bb5-121">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="71bb5-121">Calls to this method on the server require permission from the InteropPermission class.</span></span>

## <a name="method-new"></a><span data-ttu-id="71bb5-122">メソッド new</span><span class="sxs-lookup"><span data-stu-id="71bb5-122">Method new</span></span>

<span data-ttu-id="71bb5-123">CLRObject クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-123">Creates an instance of the CLRObject class.</span></span>

```xpp
public void new(str className, [VarArg params])
```

### <a name="parameters---new"></a><span data-ttu-id="71bb5-124">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="71bb5-124">Parameters - new</span></span>

<span data-ttu-id="71bb5-125">className</span><span class="sxs-lookup"><span data-stu-id="71bb5-125">className</span></span>  
<span data-ttu-id="71bb5-126">インスタンスを作成する CLR クラスのコンストラクターの引数。</span><span class="sxs-lookup"><span data-stu-id="71bb5-126">The arguments for the constructor of the CLR class to instantiate.</span></span>

<!-- -->

<span data-ttu-id="71bb5-127">params</span><span class="sxs-lookup"><span data-stu-id="71bb5-127">params</span></span>  
<span data-ttu-id="71bb5-128">インスタンスを作成する CLR クラスのコンストラクターの引数。</span><span class="sxs-lookup"><span data-stu-id="71bb5-128">The arguments for the constructor of the CLR class to instantiate.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="71bb5-129">備考 - new</span><span class="sxs-lookup"><span data-stu-id="71bb5-129">Remarks - new</span></span>

<span data-ttu-id="71bb5-130">CLRObject クラスのインスタンスは、CLR メソッドの呼び出しから返される値をラップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="71bb5-130">Instances of the CLRObject class are used to wrap values that are returned from calls to CLR methods.</span></span> <span data-ttu-id="71bb5-131">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-131">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="71bb5-132">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="71bb5-132">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="71bb5-133">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="71bb5-133">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="71bb5-134">ユーザーが新しいメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-134">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls the new method.</span></span> <span data-ttu-id="71bb5-135">新しい ClrObject オブジェクトをインスタンス化できない場合、例外: 例外内部はスローします。</span><span class="sxs-lookup"><span data-stu-id="71bb5-135">If a new ClrObject object cannot be instantiated, the Exception:Internal exception is thrown.</span></span> <span data-ttu-id="71bb5-136">元の CLR 例外を取得するには、CLRInterop::getLastException メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-136">To obtain the original CLR exception, call the CLRInterop::getLastException method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="71bb5-137">例 - new</span><span class="sxs-lookup"><span data-stu-id="71bb5-137">Examples - new</span></span>

<span data-ttu-id="71bb5-138">この例では、新しい System.Int32 CLR オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="71bb5-138">This example creates a new System.Int32 CLR object.</span></span>

```xpp
void ClrObjectExample() 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    anytype retVal; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    perm.assert(); 
```

```xpp
    clrObj = new CLRObject("System.Int32"); 
```

```xpp
    CodeAccessPermission::revertAssert(); 
}
```

