---
title: FormObjectSetNotify クラス
description: このトピックでは、FormObjectSetNotify クラスについて説明します。
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
ms.openlocfilehash: 221c3a33bf7eb41c82497a2cdd28267e3f63df1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502921"
---
# <a name="class-formobjectsetnotify"></a><span data-ttu-id="c205b-103">クラス FormObjectSetNotify</span><span class="sxs-lookup"><span data-stu-id="c205b-103">Class FormObjectSetNotify</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetNotify extends Object
```

## <a name="remarks"></a><span data-ttu-id="c205b-104">備考</span><span class="sxs-lookup"><span data-stu-id="c205b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c205b-105">例</span><span class="sxs-lookup"><span data-stu-id="c205b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c205b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c205b-106">Methods</span></span>

| <span data-ttu-id="c205b-107">方法</span><span class="sxs-lookup"><span data-stu-id="c205b-107">Method</span></span>                                                                                                                                                                               | <span data-ttu-id="c205b-108">説明</span><span class="sxs-lookup"><span data-stu-id="c205b-108">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c205b-109">public boolean onLeave(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="c205b-109">public boolean onLeave(FormObjectSet sender)</span></span>                                                                                                                                         |                                                              |
| <span data-ttu-id="c205b-110">public int onRequestCacheSize(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="c205b-110">public int onRequestCacheSize(FormObjectSet sender)</span></span>                                                                                                                                  |                                                              |
| <span data-ttu-id="c205b-111">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span><span class="sxs-lookup"><span data-stu-id="c205b-111">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span></span>                                                                                              |                                                              |
| <span data-ttu-id="c205b-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="c205b-112">public void new()</span></span>                                                                                                                                                                    | <span data-ttu-id="c205b-113">FormObjectSetNotify クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c205b-113">Initializes a new instance of the FormObjectSetNotify class.</span></span> |
| <span data-ttu-id="c205b-114">public void onCurrentChanged(FormObjectSet sender, int position)</span><span class="sxs-lookup"><span data-stu-id="c205b-114">public void onCurrentChanged(FormObjectSet sender, int position)</span></span>                                                                                                                     |                                                              |
| <span data-ttu-id="c205b-115">public void onActive(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="c205b-115">public void onActive(FormObjectSet sender)</span></span>                                                                                                                                           |                                                              |
| <span data-ttu-id="c205b-116">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="c205b-116">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span></span>                                                                  |                                                              |
| <span data-ttu-id="c205b-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="c205b-117">public void finalize()</span></span>                                                                                                                                                               |                                                              |
| <span data-ttu-id="c205b-118">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span><span class="sxs-lookup"><span data-stu-id="c205b-118">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span></span> |                                                              |
| <span data-ttu-id="c205b-119">public void onRefresh(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="c205b-119">public void onRefresh(FormObjectSet sender)</span></span>                                                                                                                                          |                                                              |
| <span data-ttu-id="c205b-120">public void onMarkingChanged(FormObjectSet sender, Array ids)</span><span class="sxs-lookup"><span data-stu-id="c205b-120">public void onMarkingChanged(FormObjectSet sender, Array ids)</span></span>                                                                                                                        |                                                              |

## <a name="method-onleave"></a><span data-ttu-id="c205b-121">メソッド onLeave</span><span class="sxs-lookup"><span data-stu-id="c205b-121">Method onLeave</span></span>

```xpp
public boolean onLeave(FormObjectSet sender)
```

### <a name="parameters---onleave"></a><span data-ttu-id="c205b-122">パラメーター - onLeave</span><span class="sxs-lookup"><span data-stu-id="c205b-122">Parameters - onLeave</span></span>

<span data-ttu-id="c205b-123">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-123">sender</span></span>  

### <a name="return-value---onleave"></a><span data-ttu-id="c205b-124">戻り値 - onLeave</span><span class="sxs-lookup"><span data-stu-id="c205b-124">Return Value - onLeave</span></span>

## <a name="method-onrequestcachesize"></a><span data-ttu-id="c205b-125">メソッド onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="c205b-125">Method onRequestCacheSize</span></span>

```xpp
public int onRequestCacheSize(FormObjectSet sender)
```

### <a name="parameters---onrequestcachesize"></a><span data-ttu-id="c205b-126">パラメーター - onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="c205b-126">Parameters - onRequestCacheSize</span></span>

<span data-ttu-id="c205b-127">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-127">sender</span></span>  

### <a name="return-value---onrequestcachesize"></a><span data-ttu-id="c205b-128">戻り値 - onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="c205b-128">Return Value - onRequestCacheSize</span></span>

## <a name="method-oncachechanged"></a><span data-ttu-id="c205b-129">メソッド onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-129">Method onCacheChanged</span></span>

```xpp
public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)
```

### <a name="parameters---oncachechanged"></a><span data-ttu-id="c205b-130">パラメーター - onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-130">Parameters - onCacheChanged</span></span>

<span data-ttu-id="c205b-131">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-131">sender</span></span>  

<!-- -->

<span data-ttu-id="c205b-132">cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="c205b-132">cacheChangeType</span></span>  

## <a name="method-new"></a><span data-ttu-id="c205b-133">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c205b-133">Method new</span></span>

<span data-ttu-id="c205b-134">FormObjectSetNotify クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c205b-134">Initializes a new instance of the FormObjectSetNotify class.</span></span>

```xpp
public void new()
```

## <a name="method-oncurrentchanged"></a><span data-ttu-id="c205b-135">メソッド onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-135">Method onCurrentChanged</span></span>

```xpp
public void onCurrentChanged(FormObjectSet sender, int position)
```

### <a name="parameters---oncurrentchanged"></a><span data-ttu-id="c205b-136">パラメーター - onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-136">Parameters - onCurrentChanged</span></span>

<span data-ttu-id="c205b-137">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-137">sender</span></span>  

<!-- -->

<span data-ttu-id="c205b-138">職位</span><span class="sxs-lookup"><span data-stu-id="c205b-138">position</span></span>  

## <a name="method-onactive"></a><span data-ttu-id="c205b-139">メソッド onActive</span><span class="sxs-lookup"><span data-stu-id="c205b-139">Method onActive</span></span>

```xpp
public void onActive(FormObjectSet sender)
```

### <a name="parameters---onactive"></a><span data-ttu-id="c205b-140">パラメーター - onActive</span><span class="sxs-lookup"><span data-stu-id="c205b-140">Parameters - onActive</span></span>

<span data-ttu-id="c205b-141">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-141">sender</span></span>  

## <a name="method-onpagingparameterschanged"></a><span data-ttu-id="c205b-142">メソッド onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-142">Method onPagingParametersChanged</span></span>

```xpp
public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---onpagingparameterschanged"></a><span data-ttu-id="c205b-143">パラメーター - onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-143">Parameters - onPagingParametersChanged</span></span>

<span data-ttu-id="c205b-144">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-144">sender</span></span>  

<!-- -->

<span data-ttu-id="c205b-145">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="c205b-145">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="c205b-146">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="c205b-146">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="c205b-147">pageSize</span><span class="sxs-lookup"><span data-stu-id="c205b-147">pageSize</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="c205b-148">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="c205b-148">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-onruntimemetadatachanged"></a><span data-ttu-id="c205b-149">メソッド onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-149">Method onRuntimeMetadataChanged</span></span>

```xpp
public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)
```

### <a name="parameters---onruntimemetadatachanged"></a><span data-ttu-id="c205b-150">パラメーター - onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-150">Parameters - onRuntimeMetadataChanged</span></span>

<span data-ttu-id="c205b-151">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-151">sender</span></span>  

<!-- -->

<span data-ttu-id="c205b-152">changedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="c205b-152">changedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="c205b-153">referencedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="c205b-153">referencedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="c205b-154">changedFieldId</span><span class="sxs-lookup"><span data-stu-id="c205b-154">changedFieldId</span></span>  

<!-- -->

<span data-ttu-id="c205b-155">changeType</span><span class="sxs-lookup"><span data-stu-id="c205b-155">changeType</span></span>  

## <a name="method-onrefresh"></a><span data-ttu-id="c205b-156">メソッド onRefresh</span><span class="sxs-lookup"><span data-stu-id="c205b-156">Method onRefresh</span></span>

```xpp
public void onRefresh(FormObjectSet sender)
```

### <a name="parameters---onrefresh"></a><span data-ttu-id="c205b-157">パラメーター - onRefresh</span><span class="sxs-lookup"><span data-stu-id="c205b-157">Parameters - onRefresh</span></span>

<span data-ttu-id="c205b-158">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-158">sender</span></span>  

## <a name="method-onmarkingchanged"></a><span data-ttu-id="c205b-159">メソッド onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-159">Method onMarkingChanged</span></span>

```xpp
public void onMarkingChanged(FormObjectSet sender, Array ids)
```

### <a name="parameters---onmarkingchanged"></a><span data-ttu-id="c205b-160">パラメーター - onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="c205b-160">Parameters - onMarkingChanged</span></span>

<span data-ttu-id="c205b-161">sender</span><span class="sxs-lookup"><span data-stu-id="c205b-161">sender</span></span>  

<!-- -->

<span data-ttu-id="c205b-162">ids</span><span class="sxs-lookup"><span data-stu-id="c205b-162">ids</span></span>  

