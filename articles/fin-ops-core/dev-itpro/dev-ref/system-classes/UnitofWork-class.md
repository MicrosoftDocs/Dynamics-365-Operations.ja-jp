---
title: UnitofWork クラス
description: このトピックでは、UnitofWork クラスについて説明します。
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
ms.openlocfilehash: 39d2c1f070dac147a8c96bfa2d4945df9bc2b409
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502785"
---
# <a name="class-unitofwork"></a><span data-ttu-id="bf4b0-103">クラス UnitofWork</span><span class="sxs-lookup"><span data-stu-id="bf4b0-103">Class UnitofWork</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class UnitofWork extends Object
```

## <a name="remarks"></a><span data-ttu-id="bf4b0-104">備考</span><span class="sxs-lookup"><span data-stu-id="bf4b0-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="bf4b0-105">例</span><span class="sxs-lookup"><span data-stu-id="bf4b0-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="bf4b0-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="bf4b0-106">Methods</span></span>

| <span data-ttu-id="bf4b0-107">方法</span><span class="sxs-lookup"><span data-stu-id="bf4b0-107">Method</span></span>                                                       | <span data-ttu-id="bf4b0-108">説明</span><span class="sxs-lookup"><span data-stu-id="bf4b0-108">Description</span></span>                                         |
|--------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="bf4b0-109">public boolean getByKey(Common record)</span><span class="sxs-lookup"><span data-stu-id="bf4b0-109">public boolean getByKey(Common record)</span></span>                       |                                                     |
| <span data-ttu-id="bf4b0-110">public void updateonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="bf4b0-110">public void updateonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="bf4b0-111">public void saveChanges(\[UserConnection user\_connection\])</span><span class="sxs-lookup"><span data-stu-id="bf4b0-111">public void saveChanges(\[UserConnection user\_connection\])</span></span> |                                                     |
| <span data-ttu-id="bf4b0-112">public void deleteonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="bf4b0-112">public void deleteonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="bf4b0-113">public void insertonSaveChanges(Common record)</span><span class="sxs-lookup"><span data-stu-id="bf4b0-113">public void insertonSaveChanges(Common record)</span></span>               |                                                     |
| <span data-ttu-id="bf4b0-114">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="bf4b0-114">public void finalize()</span></span>                                       |                                                     |
| <span data-ttu-id="bf4b0-115">public void new()</span><span class="sxs-lookup"><span data-stu-id="bf4b0-115">public void new()</span></span>                                            | <span data-ttu-id="bf4b0-116">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bf4b0-116">Initializes a new instance of the UnitofWork class.</span></span> |
| <span data-ttu-id="bf4b0-117">public void clear()</span><span class="sxs-lookup"><span data-stu-id="bf4b0-117">public void clear()</span></span>                                          |                                                     |

## <a name="method-getbykey"></a><span data-ttu-id="bf4b0-118">メソッド getByKey</span><span class="sxs-lookup"><span data-stu-id="bf4b0-118">Method getByKey</span></span>

```xpp
public boolean getByKey(Common record)
```

### <a name="parameters---getbykey"></a><span data-ttu-id="bf4b0-119">パラメーター - getByKey</span><span class="sxs-lookup"><span data-stu-id="bf4b0-119">Parameters - getByKey</span></span>

<span data-ttu-id="bf4b0-120">記録</span><span class="sxs-lookup"><span data-stu-id="bf4b0-120">record</span></span>  

### <a name="return-value---getbykey"></a><span data-ttu-id="bf4b0-121">戻り値 - getByKey</span><span class="sxs-lookup"><span data-stu-id="bf4b0-121">Return Value - getByKey</span></span>

## <a name="method-updateonsavechanges"></a><span data-ttu-id="bf4b0-122">メソッド updateonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-122">Method updateonSaveChanges</span></span>

```xpp
public void updateonSaveChanges(Common record)
```

### <a name="parameters---updateonsavechanges"></a><span data-ttu-id="bf4b0-123">パラメーター - updateonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-123">Parameters - updateonSaveChanges</span></span>

<span data-ttu-id="bf4b0-124">記録</span><span class="sxs-lookup"><span data-stu-id="bf4b0-124">record</span></span>  

## <a name="method-savechanges"></a><span data-ttu-id="bf4b0-125">メソッド saveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-125">Method saveChanges</span></span>

```xpp
public void saveChanges([UserConnection user_connection])
```

### <a name="parameters---savechanges"></a><span data-ttu-id="bf4b0-126">パラメータ－ - saveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-126">Parameters - saveChanges</span></span>

<span data-ttu-id="bf4b0-127">user\_connection</span><span class="sxs-lookup"><span data-stu-id="bf4b0-127">user\_connection</span></span>  

## <a name="method-deleteonsavechanges"></a><span data-ttu-id="bf4b0-128">メソッド deleteonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-128">Method deleteonSaveChanges</span></span>

```xpp
public void deleteonSaveChanges(Common record)
```

### <a name="parameters---deleteonsavechanges"></a><span data-ttu-id="bf4b0-129">パラメーター - deleteonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-129">Parameters - deleteonSaveChanges</span></span>

<span data-ttu-id="bf4b0-130">記録</span><span class="sxs-lookup"><span data-stu-id="bf4b0-130">record</span></span>  

## <a name="method-insertonsavechanges"></a><span data-ttu-id="bf4b0-131">メソッド insertonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-131">Method insertonSaveChanges</span></span>

```xpp
public void insertonSaveChanges(Common record)
```

### <a name="parameters---insertonsavechanges"></a><span data-ttu-id="bf4b0-132">パラメーター - insertonSaveChanges</span><span class="sxs-lookup"><span data-stu-id="bf4b0-132">Parameters - insertonSaveChanges</span></span>

<span data-ttu-id="bf4b0-133">記録</span><span class="sxs-lookup"><span data-stu-id="bf4b0-133">record</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="bf4b0-134">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="bf4b0-134">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="bf4b0-135">メソッド new</span><span class="sxs-lookup"><span data-stu-id="bf4b0-135">Method new</span></span>

<span data-ttu-id="bf4b0-136">UnitofWork クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bf4b0-136">Initializes a new instance of the UnitofWork class.</span></span>

```xpp
public void new()
```

## <a name="method-clear"></a><span data-ttu-id="bf4b0-137">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="bf4b0-137">Method clear</span></span>

```xpp
public void clear()
```

