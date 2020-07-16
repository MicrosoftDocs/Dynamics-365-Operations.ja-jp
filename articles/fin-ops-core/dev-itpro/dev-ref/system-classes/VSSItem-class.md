---
title: VSSItem クラス
description: このトピックでは、VSSItem クラスについて説明します。
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
ms.openlocfilehash: bc0baed9c50a18e106990fd6467d4caa4346db91
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502777"
---
# <a name="class-vssitem"></a><span data-ttu-id="3e5ef-103">クラス VSSItem</span><span class="sxs-lookup"><span data-stu-id="3e5ef-103">Class VSSItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSSItem extends Object
```

## <a name="remarks"></a><span data-ttu-id="3e5ef-104">備考</span><span class="sxs-lookup"><span data-stu-id="3e5ef-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3e5ef-105">例</span><span class="sxs-lookup"><span data-stu-id="3e5ef-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3e5ef-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e5ef-106">Methods</span></span>

| <span data-ttu-id="3e5ef-107">方法</span><span class="sxs-lookup"><span data-stu-id="3e5ef-107">Method</span></span>                                                                               | <span data-ttu-id="3e5ef-108">説明</span><span class="sxs-lookup"><span data-stu-id="3e5ef-108">Description</span></span>                                      |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="3e5ef-109">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span><span class="sxs-lookup"><span data-stu-id="3e5ef-109">public boolean add(\[boolean keepCheckedout\], \[str comment\])</span></span>                      |                                                  |
| <span data-ttu-id="3e5ef-110">public boolean checkin(\[str comment\])</span><span class="sxs-lookup"><span data-stu-id="3e5ef-110">public boolean checkin(\[str comment\])</span></span>                                              |                                                  |
| <span data-ttu-id="3e5ef-111">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span><span class="sxs-lookup"><span data-stu-id="3e5ef-111">public boolean checkout(\[boolean allowMultipleCheckout\], \[boolean replaceLocal\])</span></span> |                                                  |
| <span data-ttu-id="3e5ef-112">public boolean delete()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-112">public boolean delete()</span></span>                                                              |                                                  |
| <span data-ttu-id="3e5ef-113">public boolean destroy()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-113">public boolean destroy()</span></span>                                                             |                                                  |
| <span data-ttu-id="3e5ef-114">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span><span class="sxs-lookup"><span data-stu-id="3e5ef-114">public Map get(\[boolean force\], \[int version\], \[str label\], \[str localFile\])</span></span> |                                                  |
| <span data-ttu-id="3e5ef-115">public str getActionText()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-115">public str getActionText()</span></span>                                                           |                                                  |
| <span data-ttu-id="3e5ef-116">public container getCheckedOutTo()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-116">public container getCheckedOutTo()</span></span>                                                   |                                                  |
| <span data-ttu-id="3e5ef-117">public int getCheckoutVersion()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-117">public int getCheckoutVersion()</span></span>                                                      |                                                  |
| <span data-ttu-id="3e5ef-118">public container getHistory()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-118">public container getHistory()</span></span>                                                        |                                                  |
| <span data-ttu-id="3e5ef-119">public ComInterface getIUnknown()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-119">public ComInterface getIUnknown()</span></span>                                                    |                                                  |
| <span data-ttu-id="3e5ef-120">public int getVersionNo()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-120">public int getVersionNo()</span></span>                                                            |                                                  |
| <span data-ttu-id="3e5ef-121">public str getVSSPath()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-121">public str getVSSPath()</span></span>                                                              |                                                  |
| <span data-ttu-id="3e5ef-122">public boolean isCheckedOut()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-122">public boolean isCheckedOut()</span></span>                                                        |                                                  |
| <span data-ttu-id="3e5ef-123">public boolean isRenamed()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-123">public boolean isRenamed()</span></span>                                                           |                                                  |
| <span data-ttu-id="3e5ef-124">public str name(str newName)</span><span class="sxs-lookup"><span data-stu-id="3e5ef-124">public str name(str newName)</span></span>                                                         |                                                  |
| <span data-ttu-id="3e5ef-125">public boolean rename(str newName)</span><span class="sxs-lookup"><span data-stu-id="3e5ef-125">public boolean rename(str newName)</span></span>                                                   |                                                  |
| <span data-ttu-id="3e5ef-126">public boolean undoCheckout()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-126">public boolean undoCheckout()</span></span>                                                        |                                                  |
| <span data-ttu-id="3e5ef-127">private void new()</span><span class="sxs-lookup"><span data-stu-id="3e5ef-127">private void new()</span></span>                                                                   | <span data-ttu-id="3e5ef-128">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e5ef-128">Initializes a new instance of the VSSItem class.</span></span> |

## <a name="method-add"></a><span data-ttu-id="3e5ef-129">メソッド add</span><span class="sxs-lookup"><span data-stu-id="3e5ef-129">Method add</span></span>

```xpp
public boolean add([boolean keepCheckedout], [str comment])
```

### <a name="parameters---add"></a><span data-ttu-id="3e5ef-130">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="3e5ef-130">Parameters - add</span></span>

<span data-ttu-id="3e5ef-131">keepCheckedout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-131">keepCheckedout</span></span>  

<!-- -->

<span data-ttu-id="3e5ef-132">comment</span><span class="sxs-lookup"><span data-stu-id="3e5ef-132">comment</span></span>  

### <a name="return-value---add"></a><span data-ttu-id="3e5ef-133">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="3e5ef-133">Return Value - add</span></span>

## <a name="method-checkin"></a><span data-ttu-id="3e5ef-134">メソッド checkin</span><span class="sxs-lookup"><span data-stu-id="3e5ef-134">Method checkin</span></span>

```xpp
public boolean checkin([str comment])
```

### <a name="parameters---checkin"></a><span data-ttu-id="3e5ef-135">パラメーター - checkin</span><span class="sxs-lookup"><span data-stu-id="3e5ef-135">Parameters - checkin</span></span>

<span data-ttu-id="3e5ef-136">comment</span><span class="sxs-lookup"><span data-stu-id="3e5ef-136">comment</span></span>  

### <a name="return-value---checkin"></a><span data-ttu-id="3e5ef-137">戻り値 - checkin</span><span class="sxs-lookup"><span data-stu-id="3e5ef-137">Return Value - checkin</span></span>

## <a name="method-checkout"></a><span data-ttu-id="3e5ef-138">メソッド checkout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-138">Method checkout</span></span>

```xpp
public boolean checkout([boolean allowMultipleCheckout], [boolean replaceLocal])
```

### <a name="parameters---checkout"></a><span data-ttu-id="3e5ef-139">パラメーター - checkout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-139">Parameters - checkout</span></span>

<span data-ttu-id="3e5ef-140">allowMultipleCheckout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-140">allowMultipleCheckout</span></span>  

<!-- -->

<span data-ttu-id="3e5ef-141">replaceLocal</span><span class="sxs-lookup"><span data-stu-id="3e5ef-141">replaceLocal</span></span>  

### <a name="return-value---checkout"></a><span data-ttu-id="3e5ef-142">戻り値 - checkout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-142">Return Value - checkout</span></span>

## <a name="method-delete"></a><span data-ttu-id="3e5ef-143">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="3e5ef-143">Method delete</span></span>

```xpp
public boolean delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="3e5ef-144">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="3e5ef-144">Return Value - delete</span></span>

## <a name="method-destroy"></a><span data-ttu-id="3e5ef-145">メソッド destroy</span><span class="sxs-lookup"><span data-stu-id="3e5ef-145">Method destroy</span></span>

```xpp
public boolean destroy()
```

### <a name="return-value---destroy"></a><span data-ttu-id="3e5ef-146">戻り値 - destroy</span><span class="sxs-lookup"><span data-stu-id="3e5ef-146">Return Value - destroy</span></span>

## <a name="method-get"></a><span data-ttu-id="3e5ef-147">メソッド get</span><span class="sxs-lookup"><span data-stu-id="3e5ef-147">Method get</span></span>

```xpp
public Map get([boolean force], [int version], [str label], [str localFile])
```

### <a name="parameters---get"></a><span data-ttu-id="3e5ef-148">パラメーター - get</span><span class="sxs-lookup"><span data-stu-id="3e5ef-148">Parameters - get</span></span>

<span data-ttu-id="3e5ef-149">force</span><span class="sxs-lookup"><span data-stu-id="3e5ef-149">force</span></span>  

<!-- -->

<span data-ttu-id="3e5ef-150">のバージョン</span><span class="sxs-lookup"><span data-stu-id="3e5ef-150">version</span></span>  

<!-- -->

<span data-ttu-id="3e5ef-151">ラベル</span><span class="sxs-lookup"><span data-stu-id="3e5ef-151">label</span></span>  

<!-- -->

<span data-ttu-id="3e5ef-152">localFile</span><span class="sxs-lookup"><span data-stu-id="3e5ef-152">localFile</span></span>  

### <a name="return-value---get"></a><span data-ttu-id="3e5ef-153">戻り値 - get</span><span class="sxs-lookup"><span data-stu-id="3e5ef-153">Return Value - get</span></span>

## <a name="method-getactiontext"></a><span data-ttu-id="3e5ef-154">メソッド getActionText</span><span class="sxs-lookup"><span data-stu-id="3e5ef-154">Method getActionText</span></span>

```xpp
public str getActionText()
```

### <a name="return-value---getactiontext"></a><span data-ttu-id="3e5ef-155">戻り値 - getActionText</span><span class="sxs-lookup"><span data-stu-id="3e5ef-155">Return Value - getActionText</span></span>

## <a name="method-getcheckedoutto"></a><span data-ttu-id="3e5ef-156">メソッド getCheckedOutTo</span><span class="sxs-lookup"><span data-stu-id="3e5ef-156">Method getCheckedOutTo</span></span>

```xpp
public container getCheckedOutTo()
```

### <a name="return-value---getcheckedoutto"></a><span data-ttu-id="3e5ef-157">戻り値 - getCheckedOutTo</span><span class="sxs-lookup"><span data-stu-id="3e5ef-157">Return Value - getCheckedOutTo</span></span>

## <a name="method-getcheckoutversion"></a><span data-ttu-id="3e5ef-158">メソッド getCheckoutVersion</span><span class="sxs-lookup"><span data-stu-id="3e5ef-158">Method getCheckoutVersion</span></span>

```xpp
public int getCheckoutVersion()
```

### <a name="return-value---getcheckoutversion"></a><span data-ttu-id="3e5ef-159">戻り値 - getCheckoutVersion</span><span class="sxs-lookup"><span data-stu-id="3e5ef-159">Return Value - getCheckoutVersion</span></span>

## <a name="method-gethistory"></a><span data-ttu-id="3e5ef-160">メソッド getHistory</span><span class="sxs-lookup"><span data-stu-id="3e5ef-160">Method getHistory</span></span>

```xpp
public container getHistory()
```

### <a name="return-value---gethistory"></a><span data-ttu-id="3e5ef-161">戻り値 - getHistory</span><span class="sxs-lookup"><span data-stu-id="3e5ef-161">Return Value - getHistory</span></span>

## <a name="method-getiunknown"></a><span data-ttu-id="3e5ef-162">メソッド getIUnknown</span><span class="sxs-lookup"><span data-stu-id="3e5ef-162">Method getIUnknown</span></span>

```xpp
public ComInterface getIUnknown()
```

### <a name="return-value---getiunknown"></a><span data-ttu-id="3e5ef-163">戻り値 - getIUnknown</span><span class="sxs-lookup"><span data-stu-id="3e5ef-163">Return Value - getIUnknown</span></span>

## <a name="method-getversionno"></a><span data-ttu-id="3e5ef-164">メソッド getVersionNo</span><span class="sxs-lookup"><span data-stu-id="3e5ef-164">Method getVersionNo</span></span>

```xpp
public int getVersionNo()
```

### <a name="return-value---getversionno"></a><span data-ttu-id="3e5ef-165">戻り値 - getVersionNo</span><span class="sxs-lookup"><span data-stu-id="3e5ef-165">Return Value - getVersionNo</span></span>

## <a name="method-getvsspath"></a><span data-ttu-id="3e5ef-166">メソッド getVSSPath</span><span class="sxs-lookup"><span data-stu-id="3e5ef-166">Method getVSSPath</span></span>

```xpp
public str getVSSPath()
```

### <a name="return-value---getvsspath"></a><span data-ttu-id="3e5ef-167">戻り値 - getVSSPath</span><span class="sxs-lookup"><span data-stu-id="3e5ef-167">Return Value - getVSSPath</span></span>

## <a name="method-ischeckedout"></a><span data-ttu-id="3e5ef-168">メソッド isCheckedOut</span><span class="sxs-lookup"><span data-stu-id="3e5ef-168">Method isCheckedOut</span></span>

```xpp
public boolean isCheckedOut()
```

### <a name="return-value---ischeckedout"></a><span data-ttu-id="3e5ef-169">戻り値 - isCheckedOut</span><span class="sxs-lookup"><span data-stu-id="3e5ef-169">Return Value - isCheckedOut</span></span>

## <a name="method-isrenamed"></a><span data-ttu-id="3e5ef-170">メソッド isRenamed</span><span class="sxs-lookup"><span data-stu-id="3e5ef-170">Method isRenamed</span></span>

```xpp
public boolean isRenamed()
```

### <a name="return-value---isrenamed"></a><span data-ttu-id="3e5ef-171">戻り値 - isRenamed</span><span class="sxs-lookup"><span data-stu-id="3e5ef-171">Return Value - isRenamed</span></span>

## <a name="method-name"></a><span data-ttu-id="3e5ef-172">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3e5ef-172">Method name</span></span>

```xpp
public str name(str newName)
```

### <a name="parameters---name"></a><span data-ttu-id="3e5ef-173">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="3e5ef-173">Parameters - name</span></span>

<span data-ttu-id="3e5ef-174">newName</span><span class="sxs-lookup"><span data-stu-id="3e5ef-174">newName</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="3e5ef-175">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3e5ef-175">Return Value - name</span></span>

## <a name="method-rename"></a><span data-ttu-id="3e5ef-176">メソッド rename</span><span class="sxs-lookup"><span data-stu-id="3e5ef-176">Method rename</span></span>

```xpp
public boolean rename(str newName)
```

### <a name="parameters---rename"></a><span data-ttu-id="3e5ef-177">パラメーター - rename</span><span class="sxs-lookup"><span data-stu-id="3e5ef-177">Parameters - rename</span></span>

<span data-ttu-id="3e5ef-178">newName</span><span class="sxs-lookup"><span data-stu-id="3e5ef-178">newName</span></span>  

### <a name="return-value---rename"></a><span data-ttu-id="3e5ef-179">戻り値 - rename</span><span class="sxs-lookup"><span data-stu-id="3e5ef-179">Return Value - rename</span></span>

## <a name="method-undocheckout"></a><span data-ttu-id="3e5ef-180">メソッド undoCheckout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-180">Method undoCheckout</span></span>

```xpp
public boolean undoCheckout()
```

### <a name="return-value---undocheckout"></a><span data-ttu-id="3e5ef-181">戻り値 - undoCheckout</span><span class="sxs-lookup"><span data-stu-id="3e5ef-181">Return Value - undoCheckout</span></span>

## <a name="method-new"></a><span data-ttu-id="3e5ef-182">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3e5ef-182">Method new</span></span>

<span data-ttu-id="3e5ef-183">VSSItem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e5ef-183">Initializes a new instance of the VSSItem class.</span></span>

```xpp
private void new()
```


