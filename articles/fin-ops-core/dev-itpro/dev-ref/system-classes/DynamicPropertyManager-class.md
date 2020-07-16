---
title: DynamicPropertyManager クラス
description: このトピックでは、DynamicPropertyManager クラスについて説明します。
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
ms.openlocfilehash: 4bd66ea7386ac06c3a81086771fa4cc5c2a1b27f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502670"
---
# <a name="class-dynamicpropertymanager"></a><span data-ttu-id="466f9-103">クラス DynamicPropertyManager</span><span class="sxs-lookup"><span data-stu-id="466f9-103">Class DynamicPropertyManager</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DynamicPropertyManager extends Object
```

## <a name="remarks"></a><span data-ttu-id="466f9-104">備考</span><span class="sxs-lookup"><span data-stu-id="466f9-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="466f9-105">例</span><span class="sxs-lookup"><span data-stu-id="466f9-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="466f9-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="466f9-106">Methods</span></span>

| <span data-ttu-id="466f9-107">方法</span><span class="sxs-lookup"><span data-stu-id="466f9-107">Method</span></span>                                                                                                                                                                                      | <span data-ttu-id="466f9-108">説明</span><span class="sxs-lookup"><span data-stu-id="466f9-108">Description</span></span>                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="466f9-109">public DynamicPropertyCallback callbackObject()</span><span class="sxs-lookup"><span data-stu-id="466f9-109">public DynamicPropertyCallback callbackObject()</span></span>                                                                                                                                             |                                                                 |
| <span data-ttu-id="466f9-110">public str getConfigString()</span><span class="sxs-lookup"><span data-stu-id="466f9-110">public str getConfigString()</span></span>                                                                                                                                                                | <span data-ttu-id="466f9-111">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-111">Microsoft internal use only.</span></span>                                    |
| <span data-ttu-id="466f9-112">public int hasSheetChanged()</span><span class="sxs-lookup"><span data-stu-id="466f9-112">public int hasSheetChanged()</span></span>                                                                                                                                                                | <span data-ttu-id="466f9-113">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-113">Microsoft internal use only.</span></span>                                    |
| <span data-ttu-id="466f9-114">public Struct propertyValues()</span><span class="sxs-lookup"><span data-stu-id="466f9-114">public Struct propertyValues()</span></span>                                                                                                                                                              |                                                                 |
| <span data-ttu-id="466f9-115">public void allowEdit(str name, boolean allow)</span><span class="sxs-lookup"><span data-stu-id="466f9-115">public void allowEdit(str name, boolean allow)</span></span>                                                                                                                                              |                                                                 |
| <span data-ttu-id="466f9-116">public void updateValue(str propertyname, str value)</span><span class="sxs-lookup"><span data-stu-id="466f9-116">public void updateValue(str propertyname, str value)</span></span>                                                                                                                                        |                                                                 |
| <span data-ttu-id="466f9-117">public void new()</span><span class="sxs-lookup"><span data-stu-id="466f9-117">public void new()</span></span>                                                                                                                                                                           | <span data-ttu-id="466f9-118">DynamicPropertyManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="466f9-118">Initializes a new instance of the DynamicPropertyManager class.</span></span> |
| <span data-ttu-id="466f9-119">public void getPropertySheet(str configString, boolean canWebletTypeChange)</span><span class="sxs-lookup"><span data-stu-id="466f9-119">public void getPropertySheet(str configString, boolean canWebletTypeChange)</span></span>                                                                                                                 | <span data-ttu-id="466f9-120">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-120">Microsoft internal use only.</span></span>                                    |
| <span data-ttu-id="466f9-121">public void noProperties()</span><span class="sxs-lookup"><span data-stu-id="466f9-121">public void noProperties()</span></span>                                                                                                                                                                  |                                                                 |
| <span data-ttu-id="466f9-122">public void allowDisplay(str name, boolean allow)</span><span class="sxs-lookup"><span data-stu-id="466f9-122">public void allowDisplay(str name, boolean allow)</span></span>                                                                                                                                           |                                                                 |
| <span data-ttu-id="466f9-123">public void refresh()</span><span class="sxs-lookup"><span data-stu-id="466f9-123">public void refresh()</span></span>                                                                                                                                                                       |                                                                 |
| <span data-ttu-id="466f9-124">public void setProperties(int propertySetId, str caption, Struct values, \[Struct defaultValues\], \[Struct categories\], \[DynamicPropertyCallback callbackObject\], \[boolean setFocus\])</span><span class="sxs-lookup"><span data-stu-id="466f9-124">public void setProperties(int propertySetId, str caption, Struct values, \[Struct defaultValues\], \[Struct categories\], \[DynamicPropertyCallback callbackObject\], \[boolean setFocus\])</span></span> |                                                                 |

## <a name="method-callbackobject"></a><span data-ttu-id="466f9-125">メソッド callbackObject</span><span class="sxs-lookup"><span data-stu-id="466f9-125">Method callbackObject</span></span>

```xpp
public DynamicPropertyCallback callbackObject()
```

### <a name="return-value---callbackobject"></a><span data-ttu-id="466f9-126">戻り値 - callbackObject</span><span class="sxs-lookup"><span data-stu-id="466f9-126">Return Value - callbackObject</span></span>

## <a name="method-getconfigstring"></a><span data-ttu-id="466f9-127">メソッド getConfigString</span><span class="sxs-lookup"><span data-stu-id="466f9-127">Method getConfigString</span></span>

<span data-ttu-id="466f9-128">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-128">Microsoft internal use only.</span></span>

```xpp
public str getConfigString()
```

### <a name="return-value---getconfigstring"></a><span data-ttu-id="466f9-129">戻り値 - getConfigString</span><span class="sxs-lookup"><span data-stu-id="466f9-129">Return Value - getConfigString</span></span>

<span data-ttu-id="466f9-130">コンフィギュレーションの文字列。</span><span class="sxs-lookup"><span data-stu-id="466f9-130">A configuration string.</span></span>

## <a name="method-hassheetchanged"></a><span data-ttu-id="466f9-131">メソッド hasSheetChanged</span><span class="sxs-lookup"><span data-stu-id="466f9-131">Method hasSheetChanged</span></span>

<span data-ttu-id="466f9-132">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-132">Microsoft internal use only.</span></span>

```xpp
public int hasSheetChanged()
```

### <a name="return-value---hassheetchanged"></a><span data-ttu-id="466f9-133">戻り値 - hasSheetChanged</span><span class="sxs-lookup"><span data-stu-id="466f9-133">Return Value - hasSheetChanged</span></span>

<span data-ttu-id="466f9-134">シートが変更されたかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="466f9-134">A value that indicates whether the sheet has changed.</span></span>

## <a name="method-propertyvalues"></a><span data-ttu-id="466f9-135">メソッド propertyValues</span><span class="sxs-lookup"><span data-stu-id="466f9-135">Method propertyValues</span></span>

```xpp
public Struct propertyValues()
```

### <a name="return-value---propertyvalues"></a><span data-ttu-id="466f9-136">戻り値 - propertyValues</span><span class="sxs-lookup"><span data-stu-id="466f9-136">Return Value - propertyValues</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="466f9-137">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="466f9-137">Method allowEdit</span></span>

```xpp
public void allowEdit(str name, boolean allow)
```

### <a name="parameters---allowedit"></a><span data-ttu-id="466f9-138">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="466f9-138">Parameters - allowEdit</span></span>

<span data-ttu-id="466f9-139">名前</span><span class="sxs-lookup"><span data-stu-id="466f9-139">name</span></span>  

<!-- -->

<span data-ttu-id="466f9-140">allow</span><span class="sxs-lookup"><span data-stu-id="466f9-140">allow</span></span>  

## <a name="method-updatevalue"></a><span data-ttu-id="466f9-141">メソッド updateValue</span><span class="sxs-lookup"><span data-stu-id="466f9-141">Method updateValue</span></span>

```xpp
public void updateValue(str propertyname, str value)
```

### <a name="parameters---updatevalue"></a><span data-ttu-id="466f9-142">パラメーター - updateValue</span><span class="sxs-lookup"><span data-stu-id="466f9-142">Parameters - updateValue</span></span>

<span data-ttu-id="466f9-143">propertyname</span><span class="sxs-lookup"><span data-stu-id="466f9-143">propertyname</span></span>  

<!-- -->

<span data-ttu-id="466f9-144">値</span><span class="sxs-lookup"><span data-stu-id="466f9-144">value</span></span>  

## <a name="method-new"></a><span data-ttu-id="466f9-145">メソッド new</span><span class="sxs-lookup"><span data-stu-id="466f9-145">Method new</span></span>

<span data-ttu-id="466f9-146">DynamicPropertyManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="466f9-146">Initializes a new instance of the DynamicPropertyManager class.</span></span>

```xpp
public void new()
```

## <a name="method-getpropertysheet"></a><span data-ttu-id="466f9-147">メソッド getPropertySheet</span><span class="sxs-lookup"><span data-stu-id="466f9-147">Method getPropertySheet</span></span>

<span data-ttu-id="466f9-148">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="466f9-148">Microsoft internal use only.</span></span>

```xpp
public void getPropertySheet(str configString, boolean canWebletTypeChange)
```

### <a name="parameters---getpropertysheet"></a><span data-ttu-id="466f9-149">パラメーター - getPropertySheet</span><span class="sxs-lookup"><span data-stu-id="466f9-149">Parameters - getPropertySheet</span></span>

<span data-ttu-id="466f9-150">configString</span><span class="sxs-lookup"><span data-stu-id="466f9-150">configString</span></span>  
<span data-ttu-id="466f9-151">Weblet タイプが変更されたかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="466f9-151">A value that indicates whether the weblet type can change.</span></span>

<!-- -->

<span data-ttu-id="466f9-152">canWebletTypeChange</span><span class="sxs-lookup"><span data-stu-id="466f9-152">canWebletTypeChange</span></span>  
<span data-ttu-id="466f9-153">Weblet タイプが変更されたかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="466f9-153">A value that indicates whether the weblet type can change.</span></span>

## <a name="method-noproperties"></a><span data-ttu-id="466f9-154">メソッド noProperties</span><span class="sxs-lookup"><span data-stu-id="466f9-154">Method noProperties</span></span>

```xpp
public void noProperties()
```

## <a name="method-allowdisplay"></a><span data-ttu-id="466f9-155">メソッド allowDisplay</span><span class="sxs-lookup"><span data-stu-id="466f9-155">Method allowDisplay</span></span>

```xpp
public void allowDisplay(str name, boolean allow)
```

### <a name="parameters---allowdisplay"></a><span data-ttu-id="466f9-156">パラメーター - allowDisplay</span><span class="sxs-lookup"><span data-stu-id="466f9-156">Parameters - allowDisplay</span></span>

<span data-ttu-id="466f9-157">名前</span><span class="sxs-lookup"><span data-stu-id="466f9-157">name</span></span>  

<!-- -->

<span data-ttu-id="466f9-158">allow</span><span class="sxs-lookup"><span data-stu-id="466f9-158">allow</span></span>  

## <a name="method-refresh"></a><span data-ttu-id="466f9-159">メソッド refresh</span><span class="sxs-lookup"><span data-stu-id="466f9-159">Method refresh</span></span>

```xpp
public void refresh()
```

## <a name="method-setproperties"></a><span data-ttu-id="466f9-160">メソッド setProperties</span><span class="sxs-lookup"><span data-stu-id="466f9-160">Method setProperties</span></span>

```xpp
public void setProperties(int propertySetId, str caption, Struct values, [Struct defaultValues], [Struct categories], [DynamicPropertyCallback callbackObject], [boolean setFocus])
```

### <a name="parameters---setproperties"></a><span data-ttu-id="466f9-161">パラメーター - setProperties</span><span class="sxs-lookup"><span data-stu-id="466f9-161">Parameters - setProperties</span></span>

<span data-ttu-id="466f9-162">propertySetId</span><span class="sxs-lookup"><span data-stu-id="466f9-162">propertySetId</span></span>  

<!-- -->

<span data-ttu-id="466f9-163">caption</span><span class="sxs-lookup"><span data-stu-id="466f9-163">caption</span></span>  

<!-- -->

<span data-ttu-id="466f9-164">値</span><span class="sxs-lookup"><span data-stu-id="466f9-164">values</span></span>  

<!-- -->

<span data-ttu-id="466f9-165">defaultValues</span><span class="sxs-lookup"><span data-stu-id="466f9-165">defaultValues</span></span>  

<!-- -->

<span data-ttu-id="466f9-166">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="466f9-166">categories</span></span>  

<!-- -->

<span data-ttu-id="466f9-167">callbackObject</span><span class="sxs-lookup"><span data-stu-id="466f9-167">callbackObject</span></span>  

<!-- -->

<span data-ttu-id="466f9-168">setFocus</span><span class="sxs-lookup"><span data-stu-id="466f9-168">setFocus</span></span>  



