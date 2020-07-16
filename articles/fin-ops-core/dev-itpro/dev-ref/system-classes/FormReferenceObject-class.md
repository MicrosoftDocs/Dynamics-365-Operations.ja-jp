---
title: FormReferenceObject クラス
description: このトピックでは、FormReferenceObject クラスについて説明します。
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
ms.openlocfilehash: 881776dd66f2531741d2e73152cfb02a343b16c6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502622"
---
# <a name="class-formreferenceobject"></a><span data-ttu-id="fdc0c-103">クラス FormReferenceObject</span><span class="sxs-lookup"><span data-stu-id="fdc0c-103">Class FormReferenceObject</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormReferenceObject extends FormDataObject
```

## <a name="remarks"></a><span data-ttu-id="fdc0c-104">備考</span><span class="sxs-lookup"><span data-stu-id="fdc0c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fdc0c-105">例</span><span class="sxs-lookup"><span data-stu-id="fdc0c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fdc0c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fdc0c-106">Methods</span></span>

| <span data-ttu-id="fdc0c-107">方法</span><span class="sxs-lookup"><span data-stu-id="fdc0c-107">Method</span></span>                                                                    | <span data-ttu-id="fdc0c-108">説明</span><span class="sxs-lookup"><span data-stu-id="fdc0c-108">Description</span></span>                                                                                                                                                             |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc0c-109">public int allowAdd(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-109">public int allowAdd(\[int value\])</span></span>                                        | <span data-ttu-id="fdc0c-110">フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-110">Sets or returns the value of the allowAdd property for the form data object.</span></span>                                                                                            |
| <span data-ttu-id="fdc0c-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-111">public boolean allowEdit(\[boolean value\])</span></span>                               | <span data-ttu-id="fdc0c-112">ユーザーがコントロールの内容を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-112">Indicates whether the user can change the contents of the control.</span></span>                                                                                                      |
| <span data-ttu-id="fdc0c-113">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-113">public FieldId dataField(\[FieldId value\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="fdc0c-114">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-114">public boolean enabled(\[boolean value\])</span></span>                                 | <span data-ttu-id="fdc0c-115">オブジェクトを有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-115">Indicates whether to enable or disable the object.</span></span>                                                                                                                      |
| <span data-ttu-id="fdc0c-116">public Common lookupReference(FormReferenceControl formReferenceControl)</span><span class="sxs-lookup"><span data-stu-id="fdc0c-116">public Common lookupReference(FormReferenceControl formReferenceControl)</span></span>  |                                                                                                                                                                         |
| <span data-ttu-id="fdc0c-117">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-117">public boolean mandatory(\[boolean value\])</span></span>                               | <span data-ttu-id="fdc0c-118">データ フィールドが必須であるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-118">Sets or returns a value that indicates whether the data field is mandatory.</span></span>                                                                                             |
| <span data-ttu-id="fdc0c-119">public Common resolveReference(FormReferenceControl formReferenceControl)</span><span class="sxs-lookup"><span data-stu-id="fdc0c-119">public Common resolveReference(FormReferenceControl formReferenceControl)</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="fdc0c-120">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-120">public boolean skip(\[boolean value\])</span></span>                                    | <span data-ttu-id="fdc0c-121">ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-121">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control that is associated with the data source.</span></span> |
| <span data-ttu-id="fdc0c-122">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fdc0c-122">public boolean visible(\[boolean value\])</span></span>                                 | <span data-ttu-id="fdc0c-123">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-123">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |

## <a name="method-allowadd"></a><span data-ttu-id="fdc0c-124">メソッド allowAdd</span><span class="sxs-lookup"><span data-stu-id="fdc0c-124">Method allowAdd</span></span>

<span data-ttu-id="fdc0c-125">フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-125">Sets or returns the value of the allowAdd property for the form data object.</span></span>

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a><span data-ttu-id="fdc0c-126">パラメーター - allowAdd</span><span class="sxs-lookup"><span data-stu-id="fdc0c-126">Parameters - allowAdd</span></span>

<span data-ttu-id="fdc0c-127">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-127">value</span></span>  
<span data-ttu-id="fdc0c-128">allowEdit プロパティに割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-128">The value that is assigned to the allowEdit property.</span></span>

### <a name="return-value---allowadd"></a><span data-ttu-id="fdc0c-129">戻り値 - allowAdd</span><span class="sxs-lookup"><span data-stu-id="fdc0c-129">Return Value - allowAdd</span></span>

<span data-ttu-id="fdc0c-130">allowAdd プロパティが No、Restricted もしくは Yes に設定されているかどうかを示す FormAllowAdd 列挙値。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-130">A FormAllowAdd enumeration value that indicates whether the allowAdd property is set to No, Restricted, or Yes.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="fdc0c-131">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="fdc0c-131">Method allowEdit</span></span>

<span data-ttu-id="fdc0c-132">ユーザーがコントロールの内容を変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-132">Indicates whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="fdc0c-133">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fdc0c-133">Parameters - allowEdit</span></span>

<span data-ttu-id="fdc0c-134">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-134">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="fdc0c-135">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fdc0c-135">Return Value - allowEdit</span></span>

<span data-ttu-id="fdc0c-136">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-136">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="fdc0c-137">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fdc0c-137">Remarks - allowEdit</span></span>

<span data-ttu-id="fdc0c-138">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-138">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-datafield"></a><span data-ttu-id="fdc0c-139">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="fdc0c-139">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="fdc0c-140">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="fdc0c-140">Parameters - dataField</span></span>

<span data-ttu-id="fdc0c-141">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-141">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="fdc0c-142">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="fdc0c-142">Return Value - dataField</span></span>

## <a name="method-enabled"></a><span data-ttu-id="fdc0c-143">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="fdc0c-143">Method enabled</span></span>

<span data-ttu-id="fdc0c-144">オブジェクトを有効または無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-144">Indicates whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="fdc0c-145">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="fdc0c-145">Parameters - enabled</span></span>

<span data-ttu-id="fdc0c-146">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-146">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="fdc0c-147">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="fdc0c-147">Return Value - enabled</span></span>

<span data-ttu-id="fdc0c-148">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-148">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="fdc0c-149">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="fdc0c-149">Remarks - enabled</span></span>

<span data-ttu-id="fdc0c-150">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-150">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="fdc0c-151">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-151">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="fdc0c-152">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-152">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-lookupreference"></a><span data-ttu-id="fdc0c-153">メソッド lookupReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-153">Method lookupReference</span></span>

```xpp
public Common lookupReference(FormReferenceControl formReferenceControl)
```

### <a name="parameters---lookupreference"></a><span data-ttu-id="fdc0c-154">パラメーター - lookupReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-154">Parameters - lookupReference</span></span>

<span data-ttu-id="fdc0c-155">formReferenceControl</span><span class="sxs-lookup"><span data-stu-id="fdc0c-155">formReferenceControl</span></span>  

### <a name="return-value---lookupreference"></a><span data-ttu-id="fdc0c-156">戻り値 - lookupReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-156">Return Value - lookupReference</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="fdc0c-157">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="fdc0c-157">Method mandatory</span></span>

<span data-ttu-id="fdc0c-158">データ フィールドが必須であるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-158">Sets or returns a value that indicates whether the data field is mandatory.</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="fdc0c-159">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="fdc0c-159">Parameters - mandatory</span></span>

<span data-ttu-id="fdc0c-160">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-160">value</span></span>  
<span data-ttu-id="fdc0c-161">フィールドの必須プロパティに割り当てられる値。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-161">The value that is assigned to the mandatory property of the field.</span></span>

### <a name="return-value---mandatory"></a><span data-ttu-id="fdc0c-162">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="fdc0c-162">Return Value - mandatory</span></span>

<span data-ttu-id="fdc0c-163">フィールドが必須項目である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-163">true if the field is mandatory; otherwise, false.</span></span>

## <a name="method-resolvereference"></a><span data-ttu-id="fdc0c-164">メソッド resolveReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-164">Method resolveReference</span></span>

```xpp
public Common resolveReference(FormReferenceControl formReferenceControl)
```

### <a name="parameters---resolvereference"></a><span data-ttu-id="fdc0c-165">パラメーター - resolveReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-165">Parameters - resolveReference</span></span>

<span data-ttu-id="fdc0c-166">formReferenceControl</span><span class="sxs-lookup"><span data-stu-id="fdc0c-166">formReferenceControl</span></span>  

### <a name="return-value---resolvereference"></a><span data-ttu-id="fdc0c-167">戻り値 - resolveReference</span><span class="sxs-lookup"><span data-stu-id="fdc0c-167">Return Value - resolveReference</span></span>

## <a name="method-skip"></a><span data-ttu-id="fdc0c-168">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="fdc0c-168">Method skip</span></span>

<span data-ttu-id="fdc0c-169">ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-169">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control that is associated with the data source.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="fdc0c-170">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="fdc0c-170">Parameters - skip</span></span>

<span data-ttu-id="fdc0c-171">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-171">value</span></span>  
<span data-ttu-id="fdc0c-172">コントロールに関連付けられているデータ ソースの skip プロパティに割り当てられている値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-172">The value that is assigned to the skip property of the data source that is associated with the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="fdc0c-173">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="fdc0c-173">Return Value - skip</span></span>

<span data-ttu-id="fdc0c-174">データ ソースに関連付けられているコントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-174">true if the control is skipped when the user presses the TAB key to move to the control associated with the data source; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="fdc0c-175">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="fdc0c-175">Remarks - skip</span></span>

<span data-ttu-id="fdc0c-176">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-176">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span> <span data-ttu-id="fdc0c-177">コントロールまたはデータ ソースのスキップ値が true の場合、コントロールはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-177">Controls are skipped if the skip value of either the control or the data source is true.</span></span>

## <a name="method-visible"></a><span data-ttu-id="fdc0c-178">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="fdc0c-178">Method visible</span></span>

<span data-ttu-id="fdc0c-179">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-179">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="fdc0c-180">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="fdc0c-180">Parameters - visible</span></span>

<span data-ttu-id="fdc0c-181">値</span><span class="sxs-lookup"><span data-stu-id="fdc0c-181">value</span></span>  
<span data-ttu-id="fdc0c-182">コントロールの表示設定に割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-182">The value that is assigned to the visibility setting for the control.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="fdc0c-183">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="fdc0c-183">Return Value - visible</span></span>

<span data-ttu-id="fdc0c-184">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-184">true if the control is visible; otherwise, false.</span></span> <span data-ttu-id="fdc0c-185">既定は true です。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-185">The default is true.</span></span>

### <a name="remarks---visible"></a><span data-ttu-id="fdc0c-186">備考 - visible</span><span class="sxs-lookup"><span data-stu-id="fdc0c-186">Remarks - visible</span></span>

<span data-ttu-id="fdc0c-187">データ ソース フィールドを参照するコントロールは、コントロールおよび基になるデータ ソース フィールドの両方で Visible プロパティが true に設定されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-187">Controls that refer to a data source field are visible only when the visible property is set to true on both the control and the underlying data source field.</span></span> <span data-ttu-id="fdc0c-188">コントロールの代わりにデータ ソース フィールドのプロパティを設定することにより、フォーム全体で一貫してフィールドが処理されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-188">By setting the property on the data source field instead of the control, you make sure that the field is handled consistently throughout the form.</span></span> <span data-ttu-id="fdc0c-189">これにより、アップグレードが容易になります。</span><span class="sxs-lookup"><span data-stu-id="fdc0c-189">This makes upgrades easier.</span></span>

