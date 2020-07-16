---
title: xToastNotification クラス
description: このトピックでは、xToastNotification クラスについて説明します。
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
ms.openlocfilehash: 02801c0cf93b333bbd52f4abc134c21580d786c3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502756"
---
# <a name="class-xtoastnotification"></a><span data-ttu-id="9bab6-103">クラス xToastNotification</span><span class="sxs-lookup"><span data-stu-id="9bab6-103">Class xToastNotification</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xToastNotification extends Object
```

## <a name="remarks"></a><span data-ttu-id="9bab6-104">備考</span><span class="sxs-lookup"><span data-stu-id="9bab6-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9bab6-105">例</span><span class="sxs-lookup"><span data-stu-id="9bab6-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9bab6-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9bab6-106">Methods</span></span>

| <span data-ttu-id="9bab6-107">方法</span><span class="sxs-lookup"><span data-stu-id="9bab6-107">Method</span></span>                                      | <span data-ttu-id="9bab6-108">説明</span><span class="sxs-lookup"><span data-stu-id="9bab6-108">Description</span></span>                                                 |
|---------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="9bab6-109">public int duration(\[int duration\])</span><span class="sxs-lookup"><span data-stu-id="9bab6-109">public int duration(\[int duration\])</span></span>       |                                                             |
| <span data-ttu-id="9bab6-110">public int imageResId(\[int imageResId\])</span><span class="sxs-lookup"><span data-stu-id="9bab6-110">public int imageResId(\[int imageResId\])</span></span>   |                                                             |
| <span data-ttu-id="9bab6-111">public str messageText(\[str messageText\])</span><span class="sxs-lookup"><span data-stu-id="9bab6-111">public str messageText(\[str messageText\])</span></span> |                                                             |
| <span data-ttu-id="9bab6-112">public str subject(\[str subject\])</span><span class="sxs-lookup"><span data-stu-id="9bab6-112">public str subject(\[str subject\])</span></span>         |                                                             |
| <span data-ttu-id="9bab6-113">public void new()</span><span class="sxs-lookup"><span data-stu-id="9bab6-113">public void new()</span></span>                           | <span data-ttu-id="9bab6-114">xToastNotification クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9bab6-114">Initializes a new instance of the xToastNotification class.</span></span> |
| <span data-ttu-id="9bab6-115">public void onClosed()</span><span class="sxs-lookup"><span data-stu-id="9bab6-115">public void onClosed()</span></span>                      |                                                             |
| <span data-ttu-id="9bab6-116">public void show()</span><span class="sxs-lookup"><span data-stu-id="9bab6-116">public void show()</span></span>                          |                                                             |
| <span data-ttu-id="9bab6-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="9bab6-117">public void finalize()</span></span>                      |                                                             |
| <span data-ttu-id="9bab6-118">public void onClicked()</span><span class="sxs-lookup"><span data-stu-id="9bab6-118">public void onClicked()</span></span>                     |                                                             |

## <a name="method-duration"></a><span data-ttu-id="9bab6-119">メソッド duration</span><span class="sxs-lookup"><span data-stu-id="9bab6-119">Method duration</span></span>

```xpp
public int duration([int duration])
```

### <a name="parameters---duration"></a><span data-ttu-id="9bab6-120">パラメーター - duration</span><span class="sxs-lookup"><span data-stu-id="9bab6-120">Parameters - duration</span></span>

<span data-ttu-id="9bab6-121">duration</span><span class="sxs-lookup"><span data-stu-id="9bab6-121">duration</span></span>  

### <a name="return-value---duration"></a><span data-ttu-id="9bab6-122">戻り値 - duration</span><span class="sxs-lookup"><span data-stu-id="9bab6-122">Return Value - duration</span></span>

## <a name="method-imageresid"></a><span data-ttu-id="9bab6-123">メソッド imageResId</span><span class="sxs-lookup"><span data-stu-id="9bab6-123">Method imageResId</span></span>

```xpp
public int imageResId([int imageResId])
```

### <a name="parameters---imageresid"></a><span data-ttu-id="9bab6-124">パラメーター - imageResId</span><span class="sxs-lookup"><span data-stu-id="9bab6-124">Parameters - imageResId</span></span>

<span data-ttu-id="9bab6-125">imageResId</span><span class="sxs-lookup"><span data-stu-id="9bab6-125">imageResId</span></span>  

### <a name="return-value---imageresid"></a><span data-ttu-id="9bab6-126">戻り値 - imageResId</span><span class="sxs-lookup"><span data-stu-id="9bab6-126">Return Value - imageResId</span></span>

## <a name="method-messagetext"></a><span data-ttu-id="9bab6-127">メソッド messageText</span><span class="sxs-lookup"><span data-stu-id="9bab6-127">Method messageText</span></span>

```xpp
public str messageText([str messageText])
```

### <a name="parameters---messagetext"></a><span data-ttu-id="9bab6-128">パラメーター - messageText</span><span class="sxs-lookup"><span data-stu-id="9bab6-128">Parameters - messageText</span></span>

<span data-ttu-id="9bab6-129">messageText</span><span class="sxs-lookup"><span data-stu-id="9bab6-129">messageText</span></span>  

### <a name="return-value---messagetext"></a><span data-ttu-id="9bab6-130">戻り値 - messageText</span><span class="sxs-lookup"><span data-stu-id="9bab6-130">Return Value - messageText</span></span>

## <a name="method-subject"></a><span data-ttu-id="9bab6-131">メソッド subject</span><span class="sxs-lookup"><span data-stu-id="9bab6-131">Method subject</span></span>

```xpp
public str subject([str subject])
```

### <a name="parameters---subject"></a><span data-ttu-id="9bab6-132">パラメーター - subject</span><span class="sxs-lookup"><span data-stu-id="9bab6-132">Parameters - subject</span></span>

<span data-ttu-id="9bab6-133">subject</span><span class="sxs-lookup"><span data-stu-id="9bab6-133">subject</span></span>  

### <a name="return-value---subject"></a><span data-ttu-id="9bab6-134">戻り値 - subject</span><span class="sxs-lookup"><span data-stu-id="9bab6-134">Return Value - subject</span></span>

## <a name="method-new"></a><span data-ttu-id="9bab6-135">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9bab6-135">Method new</span></span>

<span data-ttu-id="9bab6-136">xToastNotification クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9bab6-136">Initializes a new instance of the xToastNotification class.</span></span>

```xpp
public void new()
```

## <a name="method-onclosed"></a><span data-ttu-id="9bab6-137">メソッド onClosed</span><span class="sxs-lookup"><span data-stu-id="9bab6-137">Method onClosed</span></span>

```xpp
public void onClosed()
```

## <a name="method-show"></a><span data-ttu-id="9bab6-138">メソッド show</span><span class="sxs-lookup"><span data-stu-id="9bab6-138">Method show</span></span>

```xpp
public void show()
```

## <a name="method-finalize"></a><span data-ttu-id="9bab6-139">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="9bab6-139">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-onclicked"></a><span data-ttu-id="9bab6-140">メソッド onClicked</span><span class="sxs-lookup"><span data-stu-id="9bab6-140">Method onClicked</span></span>

```xpp
public void onClicked()
```

