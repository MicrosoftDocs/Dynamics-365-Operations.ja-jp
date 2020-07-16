---
title: FormRowDisplayOption クラス
description: このトピックでは、FormRowDisplayOption クラスについて説明します。
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
ms.openlocfilehash: 8cb3ab5c164cb788c414c6f7c773700f13772236
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502621"
---
# <a name="class-formrowdisplayoption"></a><span data-ttu-id="5f72d-103">クラス FormRowDisplayOption</span><span class="sxs-lookup"><span data-stu-id="5f72d-103">Class FormRowDisplayOption</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormRowDisplayOption extends Object
```

## <a name="remarks"></a><span data-ttu-id="5f72d-104">備考</span><span class="sxs-lookup"><span data-stu-id="5f72d-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5f72d-105">例</span><span class="sxs-lookup"><span data-stu-id="5f72d-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5f72d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5f72d-106">Methods</span></span>

| <span data-ttu-id="5f72d-107">方法</span><span class="sxs-lookup"><span data-stu-id="5f72d-107">Method</span></span>                                                            | <span data-ttu-id="5f72d-108">説明</span><span class="sxs-lookup"><span data-stu-id="5f72d-108">Description</span></span> |
|-------------------------------------------------------------------|-------------|
| <span data-ttu-id="5f72d-109">public int backColor(\[int color\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-109">public int backColor(\[int color\])</span></span>                               |             |
| <span data-ttu-id="5f72d-110">public boolean fontBold(\[boolean bold\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-110">public boolean fontBold(\[boolean bold\])</span></span>                         |             |
| <span data-ttu-id="5f72d-111">public boolean fontItalic(\[boolean italic\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-111">public boolean fontItalic(\[boolean italic\])</span></span>                     |             |
| <span data-ttu-id="5f72d-112">public boolean fontStrikethrough(\[boolean strikethrough\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-112">public boolean fontStrikethrough(\[boolean strikethrough\])</span></span>       |             |
| <span data-ttu-id="5f72d-113">public boolean fontUnderline(\[boolean underline\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-113">public boolean fontUnderline(\[boolean underline\])</span></span>               |             |
| <span data-ttu-id="5f72d-114">public int textColor(\[int color\])</span><span class="sxs-lookup"><span data-stu-id="5f72d-114">public int textColor(\[int color\])</span></span>                               |             |
| <span data-ttu-id="5f72d-115">public void clear()</span><span class="sxs-lookup"><span data-stu-id="5f72d-115">public void clear()</span></span>                                               |             |
| <span data-ttu-id="5f72d-116">public void clearTextColor()</span><span class="sxs-lookup"><span data-stu-id="5f72d-116">public void clearTextColor()</span></span>                                      |             |
| <span data-ttu-id="5f72d-117">public void affectedElementsByField(\[FieldId fieldId\], VarArg )</span><span class="sxs-lookup"><span data-stu-id="5f72d-117">public void affectedElementsByField(\[FieldId fieldId\], VarArg )</span></span> |             |
| <span data-ttu-id="5f72d-118">public void affectedElementsByControl(\[int controlId\], VarArg )</span><span class="sxs-lookup"><span data-stu-id="5f72d-118">public void affectedElementsByControl(\[int controlId\], VarArg )</span></span> |             |
| <span data-ttu-id="5f72d-119">public void clearBackColor()</span><span class="sxs-lookup"><span data-stu-id="5f72d-119">public void clearBackColor()</span></span>                                      |             |

## <a name="method-backcolor"></a><span data-ttu-id="5f72d-120">メソッド backColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-120">Method backColor</span></span>

```xpp
public int backColor([int color])
```

### <a name="parameters---backcolor"></a><span data-ttu-id="5f72d-121">パラメーター - backColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-121">Parameters - backColor</span></span>

<span data-ttu-id="5f72d-122">色</span><span class="sxs-lookup"><span data-stu-id="5f72d-122">color</span></span>  

### <a name="return-value---backcolor"></a><span data-ttu-id="5f72d-123">戻り値 - backColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-123">Return Value - backColor</span></span>

## <a name="method-fontbold"></a><span data-ttu-id="5f72d-124">メソッド fontBold</span><span class="sxs-lookup"><span data-stu-id="5f72d-124">Method fontBold</span></span>

```xpp
public boolean fontBold([boolean bold])
```

### <a name="parameters---fontbold"></a><span data-ttu-id="5f72d-125">パラメーター - fontBold</span><span class="sxs-lookup"><span data-stu-id="5f72d-125">Parameters - fontBold</span></span>

<span data-ttu-id="5f72d-126">太字</span><span class="sxs-lookup"><span data-stu-id="5f72d-126">bold</span></span>  

### <a name="return-value---fontbold"></a><span data-ttu-id="5f72d-127">戻り値 - fontBold</span><span class="sxs-lookup"><span data-stu-id="5f72d-127">Return Value - fontBold</span></span>

## <a name="method-fontitalic"></a><span data-ttu-id="5f72d-128">メソッド fontItalic</span><span class="sxs-lookup"><span data-stu-id="5f72d-128">Method fontItalic</span></span>

```xpp
public boolean fontItalic([boolean italic])
```

### <a name="parameters---fontitalic"></a><span data-ttu-id="5f72d-129">パラメーター - fontItalic</span><span class="sxs-lookup"><span data-stu-id="5f72d-129">Parameters - fontItalic</span></span>

<span data-ttu-id="5f72d-130">斜体</span><span class="sxs-lookup"><span data-stu-id="5f72d-130">italic</span></span>  

### <a name="return-value---fontitalic"></a><span data-ttu-id="5f72d-131">戻り値 - fontItalic</span><span class="sxs-lookup"><span data-stu-id="5f72d-131">Return Value - fontItalic</span></span>

## <a name="method-fontstrikethrough"></a><span data-ttu-id="5f72d-132">メソッド fontStrikethrough</span><span class="sxs-lookup"><span data-stu-id="5f72d-132">Method fontStrikethrough</span></span>

```xpp
public boolean fontStrikethrough([boolean strikethrough])
```

### <a name="parameters---fontstrikethrough"></a><span data-ttu-id="5f72d-133">パラメーター - fontStrikethrough</span><span class="sxs-lookup"><span data-stu-id="5f72d-133">Parameters - fontStrikethrough</span></span>

<span data-ttu-id="5f72d-134">取り消し線</span><span class="sxs-lookup"><span data-stu-id="5f72d-134">strikethrough</span></span>  

### <a name="return-value---fontstrikethrough"></a><span data-ttu-id="5f72d-135">戻り値 - fontStrikethrough</span><span class="sxs-lookup"><span data-stu-id="5f72d-135">Return Value - fontStrikethrough</span></span>

## <a name="method-fontunderline"></a><span data-ttu-id="5f72d-136">メソッド fontUnderline</span><span class="sxs-lookup"><span data-stu-id="5f72d-136">Method fontUnderline</span></span>

```xpp
public boolean fontUnderline([boolean underline])
```

### <a name="parameters---fontunderline"></a><span data-ttu-id="5f72d-137">パラメーター - fontUnderline</span><span class="sxs-lookup"><span data-stu-id="5f72d-137">Parameters - fontUnderline</span></span>

<span data-ttu-id="5f72d-138">下線</span><span class="sxs-lookup"><span data-stu-id="5f72d-138">underline</span></span>  

### <a name="return-value---fontunderline"></a><span data-ttu-id="5f72d-139">戻り値 - fontUnderline</span><span class="sxs-lookup"><span data-stu-id="5f72d-139">Return Value - fontUnderline</span></span>

## <a name="method-textcolor"></a><span data-ttu-id="5f72d-140">メソッド textColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-140">Method textColor</span></span>

```xpp
public int textColor([int color])
```

### <a name="parameters---textcolor"></a><span data-ttu-id="5f72d-141">パラメーター - textColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-141">Parameters - textColor</span></span>

<span data-ttu-id="5f72d-142">色</span><span class="sxs-lookup"><span data-stu-id="5f72d-142">color</span></span>  

### <a name="return-value---textcolor"></a><span data-ttu-id="5f72d-143">戻り値 - textColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-143">Return Value - textColor</span></span>

## <a name="method-clear"></a><span data-ttu-id="5f72d-144">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="5f72d-144">Method clear</span></span>

```xpp
public void clear()
```

## <a name="method-cleartextcolor"></a><span data-ttu-id="5f72d-145">メソッド clearTextColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-145">Method clearTextColor</span></span>

```xpp
public void clearTextColor()
```

## <a name="method-affectedelementsbyfield"></a><span data-ttu-id="5f72d-146">メソッド affectedElementsByField</span><span class="sxs-lookup"><span data-stu-id="5f72d-146">Method affectedElementsByField</span></span>

```xpp
public void affectedElementsByField([FieldId fieldId], VarArg )
```

### <a name="parameters---affectedelementsbyfield"></a><span data-ttu-id="5f72d-147">パラメーター - affectedElementsByField</span><span class="sxs-lookup"><span data-stu-id="5f72d-147">Parameters - affectedElementsByField</span></span>

<span data-ttu-id="5f72d-148">fieldId</span><span class="sxs-lookup"><span data-stu-id="5f72d-148">fieldId</span></span>  

<!-- -->


## <a name="method-affectedelementsbycontrol"></a><span data-ttu-id="5f72d-149">メソッド affectedElementsByControl</span><span class="sxs-lookup"><span data-stu-id="5f72d-149">Method affectedElementsByControl</span></span>

```xpp
public void affectedElementsByControl([int controlId], VarArg )
```

### <a name="parameters---affectedelementsbycontrol"></a><span data-ttu-id="5f72d-150">パラメーター - affectedElementsByControl</span><span class="sxs-lookup"><span data-stu-id="5f72d-150">Parameters - affectedElementsByControl</span></span>

<span data-ttu-id="5f72d-151">controlId</span><span class="sxs-lookup"><span data-stu-id="5f72d-151">controlId</span></span>  

<!-- -->


## <a name="method-clearbackcolor"></a><span data-ttu-id="5f72d-152">メソッド clearBackColor</span><span class="sxs-lookup"><span data-stu-id="5f72d-152">Method clearBackColor</span></span>

```xpp
public void clearBackColor()
```

