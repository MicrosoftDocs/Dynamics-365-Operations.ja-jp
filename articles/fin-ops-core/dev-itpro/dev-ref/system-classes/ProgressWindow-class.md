---
title: ProgressWindow クラス
description: このトピックでは、ProgressWindow クラスについて説明します。
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
ms.openlocfilehash: 163866523c89da79004156066b290eafa523eb13
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502874"
---
# <a name="class-progresswindow"></a><span data-ttu-id="804df-103">クラス ProgressWindow</span><span class="sxs-lookup"><span data-stu-id="804df-103">Class ProgressWindow</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ProgressWindow extends Object
```

## <a name="remarks"></a><span data-ttu-id="804df-104">備考</span><span class="sxs-lookup"><span data-stu-id="804df-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="804df-105">例</span><span class="sxs-lookup"><span data-stu-id="804df-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="804df-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="804df-106">Methods</span></span>

| <span data-ttu-id="804df-107">方法</span><span class="sxs-lookup"><span data-stu-id="804df-107">Method</span></span>                                                      | <span data-ttu-id="804df-108">説明</span><span class="sxs-lookup"><span data-stu-id="804df-108">Description</span></span>                                             |
|-------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="804df-109">public int addProgressControl(\[int progressControlCount\])</span><span class="sxs-lookup"><span data-stu-id="804df-109">public int addProgressControl(\[int progressControlCount\])</span></span> |                                                         |
| <span data-ttu-id="804df-110">public void ProgressBarVisible(int index, int visible)</span><span class="sxs-lookup"><span data-stu-id="804df-110">public void ProgressBarVisible(int index, int visible)</span></span>      |                                                         |
| <span data-ttu-id="804df-111">public void ProgressValue(int index, int progressValue)</span><span class="sxs-lookup"><span data-stu-id="804df-111">public void ProgressValue(int index, int progressValue)</span></span>     |                                                         |
| <span data-ttu-id="804df-112">public void ControlMinMax(int index, int min, int max)</span><span class="sxs-lookup"><span data-stu-id="804df-112">public void ControlMinMax(int index, int min, int max)</span></span>      |                                                         |
| <span data-ttu-id="804df-113">public void ProgressTextVisible(int index, int visible)</span><span class="sxs-lookup"><span data-stu-id="804df-113">public void ProgressTextVisible(int index, int visible)</span></span>     |                                                         |
| <span data-ttu-id="804df-114">public void Animation(str animation)</span><span class="sxs-lookup"><span data-stu-id="804df-114">public void Animation(str animation)</span></span>                        |                                                         |
| <span data-ttu-id="804df-115">public void ControlText(int index, str text)</span><span class="sxs-lookup"><span data-stu-id="804df-115">public void ControlText(int index, str text)</span></span>                |                                                         |
| <span data-ttu-id="804df-116">public void FormCaption(str text)</span><span class="sxs-lookup"><span data-stu-id="804df-116">public void FormCaption(str text)</span></span>                           |                                                         |
| <span data-ttu-id="804df-117">public void ControlTime(str text)</span><span class="sxs-lookup"><span data-stu-id="804df-117">public void ControlTime(str text)</span></span>                           |                                                         |
| <span data-ttu-id="804df-118">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="804df-118">public void finalize()</span></span>                                      |                                                         |
| <span data-ttu-id="804df-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="804df-119">public void new()</span></span>                                           | <span data-ttu-id="804df-120">ProgressWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="804df-120">Initializes a new instance of the ProgressWindow class.</span></span> |

## <a name="method-addprogresscontrol"></a><span data-ttu-id="804df-121">メソッド addProgressControl</span><span class="sxs-lookup"><span data-stu-id="804df-121">Method addProgressControl</span></span>

```xpp
public int addProgressControl([int progressControlCount])
```

### <a name="parameters---addprogresscontrol"></a><span data-ttu-id="804df-122">パラメーター - addProgressControl</span><span class="sxs-lookup"><span data-stu-id="804df-122">Parameters - addProgressControl</span></span>

<span data-ttu-id="804df-123">progressControlCount</span><span class="sxs-lookup"><span data-stu-id="804df-123">progressControlCount</span></span>  

### <a name="return-value---addprogresscontrol"></a><span data-ttu-id="804df-124">戻り値 - addProgressControl</span><span class="sxs-lookup"><span data-stu-id="804df-124">Return Value - addProgressControl</span></span>

## <a name="method-progressbarvisible"></a><span data-ttu-id="804df-125">メソッド ProgressBarVisible</span><span class="sxs-lookup"><span data-stu-id="804df-125">Method ProgressBarVisible</span></span>

```xpp
public void ProgressBarVisible(int index, int visible)
```

### <a name="parameters---progressbarvisible"></a><span data-ttu-id="804df-126">パラメーター - ProgressBarVisible</span><span class="sxs-lookup"><span data-stu-id="804df-126">Parameters - ProgressBarVisible</span></span>

<span data-ttu-id="804df-127">指数</span><span class="sxs-lookup"><span data-stu-id="804df-127">index</span></span>  

<!-- -->

<span data-ttu-id="804df-128">表示</span><span class="sxs-lookup"><span data-stu-id="804df-128">visible</span></span>  

## <a name="method-progressvalue"></a><span data-ttu-id="804df-129">メソッド ProgressValue</span><span class="sxs-lookup"><span data-stu-id="804df-129">Method ProgressValue</span></span>

```xpp
public void ProgressValue(int index, int progressValue)
```

### <a name="parameters---progressvalue"></a><span data-ttu-id="804df-130">パラメーター - ProgressValue</span><span class="sxs-lookup"><span data-stu-id="804df-130">Parameters - ProgressValue</span></span>

<span data-ttu-id="804df-131">指数</span><span class="sxs-lookup"><span data-stu-id="804df-131">index</span></span>  

<!-- -->

<span data-ttu-id="804df-132">progressValue</span><span class="sxs-lookup"><span data-stu-id="804df-132">progressValue</span></span>  

## <a name="method-controlminmax"></a><span data-ttu-id="804df-133">メソッド ControlMinMax</span><span class="sxs-lookup"><span data-stu-id="804df-133">Method ControlMinMax</span></span>

```xpp
public void ControlMinMax(int index, int min, int max)
```

### <a name="parameters---controlminmax"></a><span data-ttu-id="804df-134">パラメーター - ControlMinMax</span><span class="sxs-lookup"><span data-stu-id="804df-134">Parameters - ControlMinMax</span></span>

<span data-ttu-id="804df-135">指数</span><span class="sxs-lookup"><span data-stu-id="804df-135">index</span></span>  

<!-- -->

<span data-ttu-id="804df-136">最小</span><span class="sxs-lookup"><span data-stu-id="804df-136">min</span></span>  

<!-- -->

<span data-ttu-id="804df-137">最大</span><span class="sxs-lookup"><span data-stu-id="804df-137">max</span></span>  

## <a name="method-progresstextvisible"></a><span data-ttu-id="804df-138">メソッド ProgressTextVisible</span><span class="sxs-lookup"><span data-stu-id="804df-138">Method ProgressTextVisible</span></span>

```xpp
public void ProgressTextVisible(int index, int visible)
```

### <a name="parameters---progresstextvisible"></a><span data-ttu-id="804df-139">パラメーター - ProgressTextVisible</span><span class="sxs-lookup"><span data-stu-id="804df-139">Parameters - ProgressTextVisible</span></span>

<span data-ttu-id="804df-140">指数</span><span class="sxs-lookup"><span data-stu-id="804df-140">index</span></span>  

<!-- -->

<span data-ttu-id="804df-141">表示</span><span class="sxs-lookup"><span data-stu-id="804df-141">visible</span></span>  

## <a name="method-animation"></a><span data-ttu-id="804df-142">メソッド アニメーション</span><span class="sxs-lookup"><span data-stu-id="804df-142">Method Animation</span></span>

```xpp
public void Animation(str animation)
```

### <a name="parameters---animation"></a><span data-ttu-id="804df-143">パラメーター - Animation</span><span class="sxs-lookup"><span data-stu-id="804df-143">Parameters - Animation</span></span>

<span data-ttu-id="804df-144">animation</span><span class="sxs-lookup"><span data-stu-id="804df-144">animation</span></span>  

## <a name="method-controltext"></a><span data-ttu-id="804df-145">メソッド ControlText</span><span class="sxs-lookup"><span data-stu-id="804df-145">Method ControlText</span></span>

```xpp
public void ControlText(int index, str text)
```

### <a name="parameters---controltext"></a><span data-ttu-id="804df-146">パラメーター - ControlText</span><span class="sxs-lookup"><span data-stu-id="804df-146">Parameters - ControlText</span></span>

<span data-ttu-id="804df-147">指数</span><span class="sxs-lookup"><span data-stu-id="804df-147">index</span></span>  

<!-- -->

<span data-ttu-id="804df-148">テキスト</span><span class="sxs-lookup"><span data-stu-id="804df-148">text</span></span>  

## <a name="method-formcaption"></a><span data-ttu-id="804df-149">メソッド FormCaption</span><span class="sxs-lookup"><span data-stu-id="804df-149">Method FormCaption</span></span>

```xpp
public void FormCaption(str text)
```

### <a name="parameters---formcaption"></a><span data-ttu-id="804df-150">パラメーター - FormCaption</span><span class="sxs-lookup"><span data-stu-id="804df-150">Parameters - FormCaption</span></span>

<span data-ttu-id="804df-151">テキスト</span><span class="sxs-lookup"><span data-stu-id="804df-151">text</span></span>  

## <a name="method-controltime"></a><span data-ttu-id="804df-152">メソッド ControlTime</span><span class="sxs-lookup"><span data-stu-id="804df-152">Method ControlTime</span></span>

```xpp
public void ControlTime(str text)
```

### <a name="parameters---controltime"></a><span data-ttu-id="804df-153">パラメーター - ControlTime</span><span class="sxs-lookup"><span data-stu-id="804df-153">Parameters - ControlTime</span></span>

<span data-ttu-id="804df-154">テキスト</span><span class="sxs-lookup"><span data-stu-id="804df-154">text</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="804df-155">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="804df-155">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="804df-156">メソッド new</span><span class="sxs-lookup"><span data-stu-id="804df-156">Method new</span></span>

<span data-ttu-id="804df-157">ProgressWindow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="804df-157">Initializes a new instance of the ProgressWindow class.</span></span>

```xpp
public void new()
```

