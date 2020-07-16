---
title: ObjectRun クラス
description: このトピックでは、ObjectRun クラスについて説明します。
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
ms.openlocfilehash: 7064d776ce636c4412c55f5e7a3aa0a98a928c93
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502565"
---
# <a name="class-objectrun"></a><span data-ttu-id="a587f-103">クラス ObjectRun</span><span class="sxs-lookup"><span data-stu-id="a587f-103">Class ObjectRun</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ObjectRun extends Object
```

<span data-ttu-id="a587f-104">FormRun クラスおよび ReportRun クラスの基本クラスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="a587f-104">Used as the base class for the FormRun and ReportRun classes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a587f-105">備考</span><span class="sxs-lookup"><span data-stu-id="a587f-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a587f-106">例</span><span class="sxs-lookup"><span data-stu-id="a587f-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a587f-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="a587f-107">Methods</span></span>

| <span data-ttu-id="a587f-108">方法</span><span class="sxs-lookup"><span data-stu-id="a587f-108">Method</span></span>                      | <span data-ttu-id="a587f-109">説明</span><span class="sxs-lookup"><span data-stu-id="a587f-109">Description</span></span>                                                                                                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a587f-110">public xArgs args()</span><span class="sxs-lookup"><span data-stu-id="a587f-110">public xArgs args()</span></span>         | <span data-ttu-id="a587f-111">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="a587f-111">Returns the arguments that the object was constructed with.</span></span>                                                                                                             |
| <span data-ttu-id="a587f-112">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="a587f-112">public boolean isDetached()</span></span> | <span data-ttu-id="a587f-113">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="a587f-113">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>                                                                                      |
| <span data-ttu-id="a587f-114">public void attach()</span><span class="sxs-lookup"><span data-stu-id="a587f-114">public void attach()</span></span>        | <span data-ttu-id="a587f-115">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="a587f-115">Reverses a call to the method.</span></span> <span data-ttu-id="a587f-116">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="a587f-116">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="a587f-117">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="a587f-117">Reversing the call disallows any further switching of focus between windows.</span></span> |
| <span data-ttu-id="a587f-118">public void detach()</span><span class="sxs-lookup"><span data-stu-id="a587f-118">public void detach()</span></span>        | <span data-ttu-id="a587f-119">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="a587f-119">Allows focus to be switched between windows.</span></span>                                                                                                                            |

## <a name="method-args"></a><span data-ttu-id="a587f-120">メソッド args</span><span class="sxs-lookup"><span data-stu-id="a587f-120">Method args</span></span>

<span data-ttu-id="a587f-121">オブジェクトが作成された引数を返します。</span><span class="sxs-lookup"><span data-stu-id="a587f-121">Returns the arguments that the object was constructed with.</span></span>

```xpp
public xArgs args()
```

### <a name="return-value---args"></a><span data-ttu-id="a587f-122">戻り値 - args</span><span class="sxs-lookup"><span data-stu-id="a587f-122">Return Value - args</span></span>

<span data-ttu-id="a587f-123">オブジェクトの引数を含む Args クラス オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a587f-123">An Args Class object that contains the arguments for the object.</span></span>

## <a name="method-isdetached"></a><span data-ttu-id="a587f-124">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="a587f-124">Method isDetached</span></span>

<span data-ttu-id="a587f-125">このオブジェクトに対して ObjectRun.detach メソッド呼び出しが行われたかどうかを通知します。</span><span class="sxs-lookup"><span data-stu-id="a587f-125">Communicates whether an ObjectRun.detach method call has been made on this object.</span></span>

```xpp
public boolean isDetached()
```

### <a name="return-value---isdetached"></a><span data-ttu-id="a587f-126">戻り値 - isDetached</span><span class="sxs-lookup"><span data-stu-id="a587f-126">Return Value - isDetached</span></span>

<span data-ttu-id="a587f-127">デタッチが呼び出された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a587f-127">true if detach has been called; otherwise, false.</span></span>

## <a name="method-attach"></a><span data-ttu-id="a587f-128">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="a587f-128">Method attach</span></span>

<span data-ttu-id="a587f-129">メソッドの呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="a587f-129">Reverses a call to the method.</span></span> <span data-ttu-id="a587f-130">これは、ObjectRun.detach メソッドの呼び出しの逆です。</span><span class="sxs-lookup"><span data-stu-id="a587f-130">This is the reverse of calling the ObjectRun.detach method.</span></span> <span data-ttu-id="a587f-131">呼び出しを取り消すと、ウィンドウ間で今後フォーカスを切り替えることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="a587f-131">Reversing the call disallows any further switching of focus between windows.</span></span>

```xpp
public void attach()
```

## <a name="method-detach"></a><span data-ttu-id="a587f-132">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="a587f-132">Method detach</span></span>

<span data-ttu-id="a587f-133">フォーカスをウィンドウ間で切り替えられるように許可します。</span><span class="sxs-lookup"><span data-stu-id="a587f-133">Allows focus to be switched between windows.</span></span>

```xpp
public void detach()
```

### <a name="remarks---detach"></a><span data-ttu-id="a587f-134">備考 - detach</span><span class="sxs-lookup"><span data-stu-id="a587f-134">Remarks - detach</span></span>

<span data-ttu-id="a587f-135">たとえば、新しいフォームの実行方法を呼び出すことにより、新しいフォームが既存のフォームから作成されます。</span><span class="sxs-lookup"><span data-stu-id="a587f-135">For example, a new form is created from an existing form by calling the new form's run method.</span></span> <span data-ttu-id="a587f-136">実行メソッドを呼び出すと、フォーカスが新しいフォームに変更されます。</span><span class="sxs-lookup"><span data-stu-id="a587f-136">Calling a run method changes the focus to the new form.</span></span> <span data-ttu-id="a587f-137">解除メソッドを呼び出すと、ユーザーは 2 番目のフォームを閉じることなく最初のフォームに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="a587f-137">Calling the detach method allows the user to return to the first form without closing the second form.</span></span> <span data-ttu-id="a587f-138">ObjectRun.attach Method メソッドの呼び出しは、解除メソッドの影響を取り消します。</span><span class="sxs-lookup"><span data-stu-id="a587f-138">Calling the ObjectRun.attach Method method reverses the effects of the detach method.</span></span>

