---
title: FormObjectSetNotifyEvents クラス
description: このトピックでは、FormObjectSetNotifyEvents クラスについて説明します。
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
ms.openlocfilehash: e871ed6f5abb810462184fc79e6cf0df429453ea
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502920"
---
# <a name="class-formobjectsetnotifyevents"></a><span data-ttu-id="95796-103">クラス FormObjectSetNotifyEvents</span><span class="sxs-lookup"><span data-stu-id="95796-103">Class FormObjectSetNotifyEvents</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetNotifyEvents extends FormObjectSetNotify
```

## <a name="remarks"></a><span data-ttu-id="95796-104">備考</span><span class="sxs-lookup"><span data-stu-id="95796-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="95796-105">例</span><span class="sxs-lookup"><span data-stu-id="95796-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="95796-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="95796-106">Methods</span></span>

| <span data-ttu-id="95796-107">方法</span><span class="sxs-lookup"><span data-stu-id="95796-107">Method</span></span>                                                                                                                                                                               | <span data-ttu-id="95796-108">説明</span><span class="sxs-lookup"><span data-stu-id="95796-108">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="95796-109">public boolean onLeave(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="95796-109">public boolean onLeave(FormObjectSet sender)</span></span>                                                                                                                                         |                                                                    |
| <span data-ttu-id="95796-110">public int onRequestCacheSize(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="95796-110">public int onRequestCacheSize(FormObjectSet sender)</span></span>                                                                                                                                  |                                                                    |
| <span data-ttu-id="95796-111">public void new()</span><span class="sxs-lookup"><span data-stu-id="95796-111">public void new()</span></span>                                                                                                                                                                    | <span data-ttu-id="95796-112">FormObjectSetNotifyEvents クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95796-112">Initializes a new instance of the FormObjectSetNotifyEvents class.</span></span> |
| <span data-ttu-id="95796-113">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span><span class="sxs-lookup"><span data-stu-id="95796-113">public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)</span></span> |                                                                    |
| <span data-ttu-id="95796-114">public void onRefresh(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="95796-114">public void onRefresh(FormObjectSet sender)</span></span>                                                                                                                                          |                                                                    |
| <span data-ttu-id="95796-115">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="95796-115">public void finalize()</span></span>                                                                                                                                                               |                                                                    |
| <span data-ttu-id="95796-116">public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span><span class="sxs-lookup"><span data-stu-id="95796-116">public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span></span>                                                                                   |                                                                    |
| <span data-ttu-id="95796-117">public void onCurrentChanged(FormObjectSet sender, int position)</span><span class="sxs-lookup"><span data-stu-id="95796-117">public void onCurrentChanged(FormObjectSet sender, int position)</span></span>                                                                                                                     |                                                                    |
| <span data-ttu-id="95796-118">public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span><span class="sxs-lookup"><span data-stu-id="95796-118">public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)</span></span>                                                                                |                                                                    |
| <span data-ttu-id="95796-119">public void onMarkingChanged(FormObjectSet sender, Array ids)</span><span class="sxs-lookup"><span data-stu-id="95796-119">public void onMarkingChanged(FormObjectSet sender, Array ids)</span></span>                                                                                                                        |                                                                    |
| <span data-ttu-id="95796-120">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span><span class="sxs-lookup"><span data-stu-id="95796-120">public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)</span></span>                                                                  |                                                                    |
| <span data-ttu-id="95796-121">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span><span class="sxs-lookup"><span data-stu-id="95796-121">public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)</span></span>                                                                                              |                                                                    |
| <span data-ttu-id="95796-122">public void onActive(FormObjectSet sender)</span><span class="sxs-lookup"><span data-stu-id="95796-122">public void onActive(FormObjectSet sender)</span></span>                                                                                                                                           |                                                                    |

## <a name="method-onleave"></a><span data-ttu-id="95796-123">メソッド onLeave</span><span class="sxs-lookup"><span data-stu-id="95796-123">Method onLeave</span></span>

```xpp
public boolean onLeave(FormObjectSet sender)
```

### <a name="parameters---onleave"></a><span data-ttu-id="95796-124">パラメーター - onLeave</span><span class="sxs-lookup"><span data-stu-id="95796-124">Parameters - onLeave</span></span>

<span data-ttu-id="95796-125">sender</span><span class="sxs-lookup"><span data-stu-id="95796-125">sender</span></span>  

### <a name="return-value---onleave"></a><span data-ttu-id="95796-126">戻り値 - onLeave</span><span class="sxs-lookup"><span data-stu-id="95796-126">Return Value - onLeave</span></span>

## <a name="method-onrequestcachesize"></a><span data-ttu-id="95796-127">メソッド onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="95796-127">Method onRequestCacheSize</span></span>

```xpp
public int onRequestCacheSize(FormObjectSet sender)
```

### <a name="parameters---onrequestcachesize"></a><span data-ttu-id="95796-128">パラメーター - onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="95796-128">Parameters - onRequestCacheSize</span></span>

<span data-ttu-id="95796-129">sender</span><span class="sxs-lookup"><span data-stu-id="95796-129">sender</span></span>  

### <a name="return-value---onrequestcachesize"></a><span data-ttu-id="95796-130">戻り値 - onRequestCacheSize</span><span class="sxs-lookup"><span data-stu-id="95796-130">Return Value - onRequestCacheSize</span></span>

## <a name="method-new"></a><span data-ttu-id="95796-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="95796-131">Method new</span></span>

<span data-ttu-id="95796-132">FormObjectSetNotifyEvents クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="95796-132">Initializes a new instance of the FormObjectSetNotifyEvents class.</span></span>

```xpp
public void new()
```

## <a name="method-onruntimemetadatachanged"></a><span data-ttu-id="95796-133">メソッド onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="95796-133">Method onRuntimeMetadataChanged</span></span>

```xpp
public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)
```

### <a name="parameters---onruntimemetadatachanged"></a><span data-ttu-id="95796-134">パラメーター - onRuntimeMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="95796-134">Parameters - onRuntimeMetadataChanged</span></span>

<span data-ttu-id="95796-135">sender</span><span class="sxs-lookup"><span data-stu-id="95796-135">sender</span></span>  

<!-- -->

<span data-ttu-id="95796-136">changedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="95796-136">changedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="95796-137">referencedDatasourceName</span><span class="sxs-lookup"><span data-stu-id="95796-137">referencedDatasourceName</span></span>  

<!-- -->

<span data-ttu-id="95796-138">changedFieldId</span><span class="sxs-lookup"><span data-stu-id="95796-138">changedFieldId</span></span>  

<!-- -->

<span data-ttu-id="95796-139">changeType</span><span class="sxs-lookup"><span data-stu-id="95796-139">changeType</span></span>  

## <a name="method-onrefresh"></a><span data-ttu-id="95796-140">メソッド onRefresh</span><span class="sxs-lookup"><span data-stu-id="95796-140">Method onRefresh</span></span>

```xpp
public void onRefresh(FormObjectSet sender)
```

### <a name="parameters---onrefresh"></a><span data-ttu-id="95796-141">パラメーター - onRefresh</span><span class="sxs-lookup"><span data-stu-id="95796-141">Parameters - onRefresh</span></span>

<span data-ttu-id="95796-142">sender</span><span class="sxs-lookup"><span data-stu-id="95796-142">sender</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="95796-143">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="95796-143">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-addeventdelegate"></a><span data-ttu-id="95796-144">メソッド addEventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-144">Method addEventDelegate</span></span>

```xpp
public void addEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)
```

### <a name="parameters---addeventdelegate"></a><span data-ttu-id="95796-145">パラメーター - addEventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-145">Parameters - addEventDelegate</span></span>

<span data-ttu-id="95796-146">eventType</span><span class="sxs-lookup"><span data-stu-id="95796-146">eventType</span></span>  

<!-- -->

<span data-ttu-id="95796-147">eventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-147">eventDelegate</span></span>  

## <a name="method-oncurrentchanged"></a><span data-ttu-id="95796-148">メソッド onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="95796-148">Method onCurrentChanged</span></span>

```xpp
public void onCurrentChanged(FormObjectSet sender, int position)
```

### <a name="parameters---oncurrentchanged"></a><span data-ttu-id="95796-149">パラメーター - onCurrentChanged</span><span class="sxs-lookup"><span data-stu-id="95796-149">Parameters - onCurrentChanged</span></span>

<span data-ttu-id="95796-150">sender</span><span class="sxs-lookup"><span data-stu-id="95796-150">sender</span></span>  

<!-- -->

<span data-ttu-id="95796-151">職位</span><span class="sxs-lookup"><span data-stu-id="95796-151">position</span></span>  

## <a name="method-removeeventdelegate"></a><span data-ttu-id="95796-152">メソッド removeEventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-152">Method removeEventDelegate</span></span>

```xpp
public void removeEventDelegate(FormObjectSetEventType eventType, ManagedEventDelegate eventDelegate)
```

### <a name="parameters---removeeventdelegate"></a><span data-ttu-id="95796-153">パラメーター - removeEventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-153">Parameters - removeEventDelegate</span></span>

<span data-ttu-id="95796-154">eventType</span><span class="sxs-lookup"><span data-stu-id="95796-154">eventType</span></span>  

<!-- -->

<span data-ttu-id="95796-155">eventDelegate</span><span class="sxs-lookup"><span data-stu-id="95796-155">eventDelegate</span></span>  

## <a name="method-onmarkingchanged"></a><span data-ttu-id="95796-156">メソッド onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="95796-156">Method onMarkingChanged</span></span>

```xpp
public void onMarkingChanged(FormObjectSet sender, Array ids)
```

### <a name="parameters---onmarkingchanged"></a><span data-ttu-id="95796-157">パラメーター - onMarkingChanged</span><span class="sxs-lookup"><span data-stu-id="95796-157">Parameters - onMarkingChanged</span></span>

<span data-ttu-id="95796-158">sender</span><span class="sxs-lookup"><span data-stu-id="95796-158">sender</span></span>  

<!-- -->

<span data-ttu-id="95796-159">ids</span><span class="sxs-lookup"><span data-stu-id="95796-159">ids</span></span>  

## <a name="method-onpagingparameterschanged"></a><span data-ttu-id="95796-160">メソッド onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="95796-160">Method onPagingParametersChanged</span></span>

```xpp
public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---onpagingparameterschanged"></a><span data-ttu-id="95796-161">パラメーター - onPagingParametersChanged</span><span class="sxs-lookup"><span data-stu-id="95796-161">Parameters - onPagingParametersChanged</span></span>

<span data-ttu-id="95796-162">sender</span><span class="sxs-lookup"><span data-stu-id="95796-162">sender</span></span>  

<!-- -->

<span data-ttu-id="95796-163">pagingEnabled</span><span class="sxs-lookup"><span data-stu-id="95796-163">pagingEnabled</span></span>  

<!-- -->

<span data-ttu-id="95796-164">startRowIndex</span><span class="sxs-lookup"><span data-stu-id="95796-164">startRowIndex</span></span>  

<!-- -->

<span data-ttu-id="95796-165">pageSize</span><span class="sxs-lookup"><span data-stu-id="95796-165">pageSize</span></span>  

## <a name="method-oncachechanged"></a><span data-ttu-id="95796-166">メソッド onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="95796-166">Method onCacheChanged</span></span>

```xpp
public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)
```

### <a name="parameters---oncachechanged"></a><span data-ttu-id="95796-167">パラメーター - onCacheChanged</span><span class="sxs-lookup"><span data-stu-id="95796-167">Parameters - onCacheChanged</span></span>

<span data-ttu-id="95796-168">sender</span><span class="sxs-lookup"><span data-stu-id="95796-168">sender</span></span>  

<!-- -->

<span data-ttu-id="95796-169">cacheChangeType</span><span class="sxs-lookup"><span data-stu-id="95796-169">cacheChangeType</span></span>  

## <a name="method-onactive"></a><span data-ttu-id="95796-170">メソッド onActive</span><span class="sxs-lookup"><span data-stu-id="95796-170">Method onActive</span></span>

```xpp
public void onActive(FormObjectSet sender)
```

### <a name="parameters---onactive"></a><span data-ttu-id="95796-171">パラメーター - onActive</span><span class="sxs-lookup"><span data-stu-id="95796-171">Parameters - onActive</span></span>

<span data-ttu-id="95796-172">sender</span><span class="sxs-lookup"><span data-stu-id="95796-172">sender</span></span>  

