---
title: COMDispFunction クラス
description: このトピックでは、COMDispFunction クラスについて説明します。
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
ms.openlocfilehash: 05c71715d1bcfe33b2cbd3d30fe25779e46fbbda
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502717"
---
# <a name="class-comdispfunction"></a><span data-ttu-id="fd461-103">クラス COMDispFunction</span><span class="sxs-lookup"><span data-stu-id="fd461-103">Class COMDispFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class COMDispFunction extends Object
```

## <a name="remarks"></a><span data-ttu-id="fd461-104">備考</span><span class="sxs-lookup"><span data-stu-id="fd461-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fd461-105">例</span><span class="sxs-lookup"><span data-stu-id="fd461-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fd461-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fd461-106">Methods</span></span>

| <span data-ttu-id="fd461-107">方法</span><span class="sxs-lookup"><span data-stu-id="fd461-107">Method</span></span>                                                                   | <span data-ttu-id="fd461-108">説明</span><span class="sxs-lookup"><span data-stu-id="fd461-108">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd461-109">public int call(VarArg )</span><span class="sxs-lookup"><span data-stu-id="fd461-109">public int call(VarArg )</span></span>                                                 |                                                                                                      |
| <span data-ttu-id="fd461-110">public AnyType callContainerOfParms(container parms)</span><span class="sxs-lookup"><span data-stu-id="fd461-110">public AnyType callContainerOfParms(container parms)</span></span>                     |                                                                                                      |
| <span data-ttu-id="fd461-111">public str toString()</span><span class="sxs-lookup"><span data-stu-id="fd461-111">public str toString()</span></span>                                                    | <span data-ttu-id="fd461-112">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fd461-112">Returns a string that represents the current object.</span></span>                                                 |
| <span data-ttu-id="fd461-113">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="fd461-113">public void finalize()</span></span>                                                   |                                                                                                      |
| <span data-ttu-id="fd461-114">public void new(COM comObject, str functionName, COMDispContext context)</span><span class="sxs-lookup"><span data-stu-id="fd461-114">public void new(COM comObject, str functionName, COMDispContext context)</span></span> | <span data-ttu-id="fd461-115">オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fd461-115">Creates a COMDispFunction object, which is used to access the functionality in an Automation object.</span></span> |

## <a name="method-call"></a><span data-ttu-id="fd461-116">メソッド call</span><span class="sxs-lookup"><span data-stu-id="fd461-116">Method call</span></span>

```xpp
public int call(VarArg )
```

### <a name="parameters---call"></a><span data-ttu-id="fd461-117">パラメーター - call</span><span class="sxs-lookup"><span data-stu-id="fd461-117">Parameters - call</span></span>


### <a name="return-value---call"></a><span data-ttu-id="fd461-118">戻り値 - call</span><span class="sxs-lookup"><span data-stu-id="fd461-118">Return Value - call</span></span>

### <a name="remarks---call"></a><span data-ttu-id="fd461-119">備考 - call</span><span class="sxs-lookup"><span data-stu-id="fd461-119">Remarks - call</span></span>

<span data-ttu-id="fd461-120">攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="fd461-120">If an attacker can control input to the call method, a security risk exists.</span></span> <span data-ttu-id="fd461-121">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fd461-121">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="fd461-122">サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="fd461-122">Calls to this method on the server require permission from the InteropPermission class.</span></span> <span data-ttu-id="fd461-123">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd461-123">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-callcontainerofparms"></a><span data-ttu-id="fd461-124">メソッド callContainerOfParms</span><span class="sxs-lookup"><span data-stu-id="fd461-124">Method callContainerOfParms</span></span>

```xpp
public AnyType callContainerOfParms(container parms)
```

### <a name="parameters---callcontainerofparms"></a><span data-ttu-id="fd461-125">パラメーター - callContainerOfParms</span><span class="sxs-lookup"><span data-stu-id="fd461-125">Parameters - callContainerOfParms</span></span>

<span data-ttu-id="fd461-126">parms</span><span class="sxs-lookup"><span data-stu-id="fd461-126">parms</span></span>  

### <a name="return-value---callcontainerofparms"></a><span data-ttu-id="fd461-127">戻り値 - callContainerOfParms</span><span class="sxs-lookup"><span data-stu-id="fd461-127">Return Value - callContainerOfParms</span></span>

## <a name="method-tostring"></a><span data-ttu-id="fd461-128">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="fd461-128">Method toString</span></span>

<span data-ttu-id="fd461-129">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fd461-129">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="fd461-130">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="fd461-130">Return Value - toString</span></span>

<span data-ttu-id="fd461-131">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="fd461-131">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="fd461-132">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="fd461-132">Remarks - toString</span></span>

<span data-ttu-id="fd461-133">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="fd461-133">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="fd461-134">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="fd461-134">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="fd461-135">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="fd461-135">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="fd461-136">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="fd461-136">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="fd461-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="fd461-137">Method new</span></span>

<span data-ttu-id="fd461-138">オートメーション オブジェクトの機能にアクセスするために使用される COMDispFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="fd461-138">Creates a COMDispFunction object, which is used to access the functionality in an Automation object.</span></span>

```xpp
public void new(COM comObject, str functionName, COMDispContext context)
```

### <a name="parameters---new"></a><span data-ttu-id="fd461-139">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="fd461-139">Parameters - new</span></span>

<span data-ttu-id="fd461-140">comObject</span><span class="sxs-lookup"><span data-stu-id="fd461-140">comObject</span></span>  
<span data-ttu-id="fd461-141">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="fd461-141">The context of the functionality to access.</span></span> <span data-ttu-id="fd461-142">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="fd461-142">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

<!-- -->

<span data-ttu-id="fd461-143">functionName</span><span class="sxs-lookup"><span data-stu-id="fd461-143">functionName</span></span>  
<span data-ttu-id="fd461-144">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="fd461-144">The context of the functionality to access.</span></span> <span data-ttu-id="fd461-145">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="fd461-145">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

<!-- -->

<span data-ttu-id="fd461-146">context</span><span class="sxs-lookup"><span data-stu-id="fd461-146">context</span></span>  
<span data-ttu-id="fd461-147">アクセスする機能のコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="fd461-147">The context of the functionality to access.</span></span> <span data-ttu-id="fd461-148">次の値が使用されます: COMDispContext::METHOD、COMDispContext::PROPERTYGET、COMDispContext::PROPERTYPUT、および COMDispContext::PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="fd461-148">The following values are used: COMDispContext::METHOD, COMDispContext::PROPERTYGET, COMDispContext::PROPERTYPUT, and COMDispContext::PROPERTYPUTREF</span></span>

### <a name="remarks---new"></a><span data-ttu-id="fd461-149">備考 - new</span><span class="sxs-lookup"><span data-stu-id="fd461-149">Remarks - new</span></span>

<span data-ttu-id="fd461-150">COM オブジェクトは、同じ名前を使用する最大 4 つの機能を指定できるので、アクセスする COM オブジェクトで機能の正しいコンテキストを指定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="fd461-150">It is important that you specify the correct context of the functionality in the COM object that you want to access, because a COM object can supply up to four functions that use the same name.</span></span> <span data-ttu-id="fd461-151">使用可能な名前の衝突のため、コンテキストはメソッドまたはプロパティを区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd461-151">Because of the possible name clashing, the context is used to distinguish the method or properties.</span></span> <span data-ttu-id="fd461-152">正しいコンテキストを指定するには、アクセスする COM オブジェクトのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd461-152">To specify the correct context, see the documentation for the COM object that you want to access.</span></span>

### <a name="examples---new"></a><span data-ttu-id="fd461-153">例 - new</span><span class="sxs-lookup"><span data-stu-id="fd461-153">Examples - new</span></span>



```xpp
{ 
    InteropPermission perm; 
    COM com; 
    COMDispFunction funcShow; 
    COMDispFunction getValue; 
    COMDispFunction putValue; 
    ; 
```

```xpp
    perm = new InteropPermission(InteropKind::ComInterop); 
    perm.assert(); 
    com = new COM("MyCOM.Object"); 
    funcShow = 
        new COMDispFunction(com, "show",  COMDispContext::METHOD); 
    getValue = 
        new COMDispFunction(com, "value", COMDispContext::PROPERTYGET); 
    putValue = 
        new COMDispFunction(com, "value", COMDispContext::PROPERTYPUT); 
}
```

