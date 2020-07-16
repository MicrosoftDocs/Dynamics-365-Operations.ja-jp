---
title: ManagedEventDelegate クラス
description: このトピックでは、ManagedEventDelegate クラスについて説明します。
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
ms.openlocfilehash: 1da338cabd388951d06ea65798d7084f96988397
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502885"
---
# <a name="class-managedeventdelegate"></a><span data-ttu-id="b530b-103">クラス ManagedEventDelegate</span><span class="sxs-lookup"><span data-stu-id="b530b-103">Class ManagedEventDelegate</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ManagedEventDelegate extends Object
```

## <a name="remarks"></a><span data-ttu-id="b530b-104">備考</span><span class="sxs-lookup"><span data-stu-id="b530b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b530b-105">例</span><span class="sxs-lookup"><span data-stu-id="b530b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b530b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b530b-106">Methods</span></span>

| <span data-ttu-id="b530b-107">方法</span><span class="sxs-lookup"><span data-stu-id="b530b-107">Method</span></span>                                                                    | <span data-ttu-id="b530b-108">説明</span><span class="sxs-lookup"><span data-stu-id="b530b-108">Description</span></span>                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b530b-109">public boolean marshalExceptionsToXPP(\[boolean marshalExceptionsToXPP\])</span><span class="sxs-lookup"><span data-stu-id="b530b-109">public boolean marshalExceptionsToXPP(\[boolean marshalExceptionsToXPP\])</span></span> |                                                               |
| <span data-ttu-id="b530b-110">private void new()</span><span class="sxs-lookup"><span data-stu-id="b530b-110">private void new()</span></span>                                                        | <span data-ttu-id="b530b-111">ManagedEventDelegate クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b530b-111">Initializes a new instance of the ManagedEventDelegate class.</span></span> |
| <span data-ttu-id="b530b-112">public void invoke(Object sender, ManagedEventArgs args)</span><span class="sxs-lookup"><span data-stu-id="b530b-112">public void invoke(Object sender, ManagedEventArgs args)</span></span>                  |                                                               |

## <a name="method-marshalexceptionstoxpp"></a><span data-ttu-id="b530b-113">メソッド marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="b530b-113">Method marshalExceptionsToXPP</span></span>

```xpp
public boolean marshalExceptionsToXPP([boolean marshalExceptionsToXPP])
```

### <a name="parameters---marshalexceptionstoxpp"></a><span data-ttu-id="b530b-114">パラメーター - marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="b530b-114">Parameters - marshalExceptionsToXPP</span></span>

<span data-ttu-id="b530b-115">marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="b530b-115">marshalExceptionsToXPP</span></span>  

### <a name="return-value---marshalexceptionstoxpp"></a><span data-ttu-id="b530b-116">戻り値 - marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="b530b-116">Return Value - marshalExceptionsToXPP</span></span>

## <a name="method-new"></a><span data-ttu-id="b530b-117">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b530b-117">Method new</span></span>

<span data-ttu-id="b530b-118">ManagedEventDelegate クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b530b-118">Initializes a new instance of the ManagedEventDelegate class.</span></span>

```xpp
private void new()
```

## <a name="method-invoke"></a><span data-ttu-id="b530b-119">メソッド invoke</span><span class="sxs-lookup"><span data-stu-id="b530b-119">Method invoke</span></span>

```xpp
public void invoke(Object sender, ManagedEventArgs args)
```

### <a name="parameters---invoke"></a><span data-ttu-id="b530b-120">パラメーター - invoke</span><span class="sxs-lookup"><span data-stu-id="b530b-120">Parameters - invoke</span></span>

<span data-ttu-id="b530b-121">sender</span><span class="sxs-lookup"><span data-stu-id="b530b-121">sender</span></span>  

<!-- -->

<span data-ttu-id="b530b-122">args</span><span class="sxs-lookup"><span data-stu-id="b530b-122">args</span></span>  

