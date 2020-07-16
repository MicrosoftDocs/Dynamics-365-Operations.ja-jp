---
title: FormObject クラス
description: このトピックでは、FormObject クラスについて説明します。
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
ms.openlocfilehash: fe27976739e8a42c1270e274759af48bf1b4a3a2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502927"
---
# <a name="class-formobject"></a><span data-ttu-id="1b5e8-103">クラス FormObject</span><span class="sxs-lookup"><span data-stu-id="1b5e8-103">Class FormObject</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormObject extends Object
```

## <a name="remarks"></a><span data-ttu-id="1b5e8-104">備考</span><span class="sxs-lookup"><span data-stu-id="1b5e8-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="1b5e8-105">例</span><span class="sxs-lookup"><span data-stu-id="1b5e8-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="1b5e8-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="1b5e8-106">Methods</span></span>

| <span data-ttu-id="1b5e8-107">方法</span><span class="sxs-lookup"><span data-stu-id="1b5e8-107">Method</span></span>                                        | <span data-ttu-id="1b5e8-108">説明</span><span class="sxs-lookup"><span data-stu-id="1b5e8-108">Description</span></span>                             |
|-----------------------------------------------|-----------------------------------------|
| <span data-ttu-id="1b5e8-109">public boolean getAllowEdit(\[int rowIndex\])</span><span class="sxs-lookup"><span data-stu-id="1b5e8-109">public boolean getAllowEdit(\[int rowIndex\])</span></span> |                                         |
| <span data-ttu-id="1b5e8-110">public AnyType getValue(\[int rowIndex\])</span><span class="sxs-lookup"><span data-stu-id="1b5e8-110">public AnyType getValue(\[int rowIndex\])</span></span>     |                                         |
| <span data-ttu-id="1b5e8-111">public boolean getVisible()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-111">public boolean getVisible()</span></span>                   |                                         |
| <span data-ttu-id="1b5e8-112">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-112">public str helpField()</span></span>                        | <span data-ttu-id="1b5e8-113">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-113">Returns the Help text for the control.</span></span>  |
| <span data-ttu-id="1b5e8-114">public str labelText()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-114">public str labelText()</span></span>                        | <span data-ttu-id="1b5e8-115">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-115">Returns the label text for the control.</span></span> |
| <span data-ttu-id="1b5e8-116">public boolean setValue(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="1b5e8-116">public boolean setValue(AnyType value)</span></span>        |                                         |
| <span data-ttu-id="1b5e8-117">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-117">public str toolTip()</span></span>                          |                                         |
| <span data-ttu-id="1b5e8-118">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-118">public boolean validate()</span></span>                     |                                         |
| <span data-ttu-id="1b5e8-119">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-119">public void jumpRef()</span></span>                         |                                         |
| <span data-ttu-id="1b5e8-120">public void modified()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-120">public void modified()</span></span>                        |                                         |
| <span data-ttu-id="1b5e8-121">public void restore()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-121">public void restore()</span></span>                         |                                         |
| <span data-ttu-id="1b5e8-122">public void find()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-122">public void find()</span></span>                            |                                         |
| <span data-ttu-id="1b5e8-123">public void context()</span><span class="sxs-lookup"><span data-stu-id="1b5e8-123">public void context()</span></span>                         |                                         |

## <a name="method-getallowedit"></a><span data-ttu-id="1b5e8-124">メソッド getAllowEdit</span><span class="sxs-lookup"><span data-stu-id="1b5e8-124">Method getAllowEdit</span></span>

```xpp
public boolean getAllowEdit([int rowIndex])
```

### <a name="parameters---getallowedit"></a><span data-ttu-id="1b5e8-125">パラメーター - getAllowEdit</span><span class="sxs-lookup"><span data-stu-id="1b5e8-125">Parameters - getAllowEdit</span></span>

<span data-ttu-id="1b5e8-126">rowIndex</span><span class="sxs-lookup"><span data-stu-id="1b5e8-126">rowIndex</span></span>  

### <a name="return-value---getallowedit"></a><span data-ttu-id="1b5e8-127">戻り値 - getAllowEdit</span><span class="sxs-lookup"><span data-stu-id="1b5e8-127">Return Value - getAllowEdit</span></span>

## <a name="method-getvalue"></a><span data-ttu-id="1b5e8-128">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-128">Method getValue</span></span>

```xpp
public AnyType getValue([int rowIndex])
```

### <a name="parameters---getvalue"></a><span data-ttu-id="1b5e8-129">パラメーター - getValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-129">Parameters - getValue</span></span>

<span data-ttu-id="1b5e8-130">rowIndex</span><span class="sxs-lookup"><span data-stu-id="1b5e8-130">rowIndex</span></span>  

### <a name="return-value---getvalue"></a><span data-ttu-id="1b5e8-131">戻り値 - getValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-131">Return Value - getValue</span></span>

## <a name="method-getvisible"></a><span data-ttu-id="1b5e8-132">メソッド getVisible</span><span class="sxs-lookup"><span data-stu-id="1b5e8-132">Method getVisible</span></span>

```xpp
public boolean getVisible()
```

### <a name="return-value---getvisible"></a><span data-ttu-id="1b5e8-133">戻り値 - getVisible</span><span class="sxs-lookup"><span data-stu-id="1b5e8-133">Return Value - getVisible</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="1b5e8-134">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="1b5e8-134">Method helpField</span></span>

<span data-ttu-id="1b5e8-135">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-135">Returns the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="1b5e8-136">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="1b5e8-136">Return Value - helpField</span></span>

<span data-ttu-id="1b5e8-137">コントロールのヘルプ テキスト。ヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-137">The Help text for the control; an empty string if there is no Help text.</span></span>

### <a name="examples---helpfield"></a><span data-ttu-id="1b5e8-138">例 - helpField</span><span class="sxs-lookup"><span data-stu-id="1b5e8-138">Examples - helpField</span></span>

<span data-ttu-id="1b5e8-139">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-139">The following example shows how to use the helpField method.</span></span>

```xpp
str strHelp;
strHelp = this.helpField();
```

## <a name="method-labeltext"></a><span data-ttu-id="1b5e8-140">メソッド labelText</span><span class="sxs-lookup"><span data-stu-id="1b5e8-140">Method labelText</span></span>

<span data-ttu-id="1b5e8-141">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-141">Returns the label text for the control.</span></span>

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a><span data-ttu-id="1b5e8-142">戻り値 - labelText</span><span class="sxs-lookup"><span data-stu-id="1b5e8-142">Return Value - labelText</span></span>

<span data-ttu-id="1b5e8-143">コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="1b5e8-143">The label text for the control; an empty string if there is no label text for the control.</span></span>

## <a name="method-setvalue"></a><span data-ttu-id="1b5e8-144">メソッド setValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-144">Method setValue</span></span>

```xpp
public boolean setValue(AnyType value)
```

### <a name="parameters---setvalue"></a><span data-ttu-id="1b5e8-145">パラメーター - setValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-145">Parameters - setValue</span></span>

<span data-ttu-id="1b5e8-146">値</span><span class="sxs-lookup"><span data-stu-id="1b5e8-146">value</span></span>  

### <a name="return-value---setvalue"></a><span data-ttu-id="1b5e8-147">戻り値 - setValue</span><span class="sxs-lookup"><span data-stu-id="1b5e8-147">Return Value - setValue</span></span>

## <a name="method-tooltip"></a><span data-ttu-id="1b5e8-148">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="1b5e8-148">Method toolTip</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="1b5e8-149">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="1b5e8-149">Return Value - toolTip</span></span>

## <a name="method-validate"></a><span data-ttu-id="1b5e8-150">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="1b5e8-150">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="1b5e8-151">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="1b5e8-151">Return Value - validate</span></span>

## <a name="method-jumpref"></a><span data-ttu-id="1b5e8-152">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="1b5e8-152">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-modified"></a><span data-ttu-id="1b5e8-153">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="1b5e8-153">Method modified</span></span>

```xpp
public void modified()
```

## <a name="method-restore"></a><span data-ttu-id="1b5e8-154">メソッド restore</span><span class="sxs-lookup"><span data-stu-id="1b5e8-154">Method restore</span></span>

```xpp
public void restore()
```

## <a name="method-find"></a><span data-ttu-id="1b5e8-155">メソッド find</span><span class="sxs-lookup"><span data-stu-id="1b5e8-155">Method find</span></span>

```xpp
public void find()
```

## <a name="method-context"></a><span data-ttu-id="1b5e8-156">メソッド context</span><span class="sxs-lookup"><span data-stu-id="1b5e8-156">Method context</span></span>

```xpp
public void context()
```

