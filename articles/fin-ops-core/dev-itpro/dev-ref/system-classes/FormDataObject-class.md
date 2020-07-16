---
title: FormDataObject クラス
description: このトピックでは、FormDataObject クラスについて説明します。
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
ms.openlocfilehash: f719f470dd0076723e1eb0e5a23413ea914fb2b4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502631"
---
# <a name="class-formdataobject"></a><span data-ttu-id="88021-103">クラス FormDataObject</span><span class="sxs-lookup"><span data-stu-id="88021-103">Class FormDataObject</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class FormDataObject extends FormObject
```

<span data-ttu-id="88021-104">FormDataObject クラスは、フィールドを表しており、フィールドを参照するコントロールがフォーム データ ソースに表示される方法に影響を与えて、ルックアップと検証の動作を変更します。</span><span class="sxs-lookup"><span data-stu-id="88021-104">The FormDataObject class represents the fields, affects how controls that refer to a field are displayed on form data sources, and modifies lookup and validation behavior.</span></span>

## <a name="remarks"></a><span data-ttu-id="88021-105">備考</span><span class="sxs-lookup"><span data-stu-id="88021-105">Remarks</span></span>

<span data-ttu-id="88021-106">プロパティを変更すると、フィールドを参照するコントロールの表示方法に影響します。</span><span class="sxs-lookup"><span data-stu-id="88021-106">By changing the properties, you affect how controls that refer to the field are displayed.</span></span> <span data-ttu-id="88021-107">さらに、このクラスでメソッドを上書きした場合、ルックアップと検証での動作を変更できます。</span><span class="sxs-lookup"><span data-stu-id="88021-107">Furthermore, if you override the methods on this class, the behavior on lookup and validation can be modified.</span></span> <span data-ttu-id="88021-108">個々のコントロールのプロパティの代わりに FormDataObject クラスのプロパティを使用することにより、同じフィールドのさまざまな表現が一貫して処理されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88021-108">By using the properties on the FormDataObject class instead of properties on the individual controls, you make sure that the various representations of the same field are handled consistently.</span></span> <span data-ttu-id="88021-109">これにより、アップグレードも容易になります。</span><span class="sxs-lookup"><span data-stu-id="88021-109">This also makes upgrades easier.</span></span>

## <a name="examples"></a><span data-ttu-id="88021-110">例</span><span class="sxs-lookup"><span data-stu-id="88021-110">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="88021-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="88021-111">Methods</span></span>

| <span data-ttu-id="88021-112">方法</span><span class="sxs-lookup"><span data-stu-id="88021-112">Method</span></span>                                                                                                      | <span data-ttu-id="88021-113">説明</span><span class="sxs-lookup"><span data-stu-id="88021-113">Description</span></span>                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88021-114">public Common lookupReference(\[FormReferenceControl formReferenceControl\])</span><span class="sxs-lookup"><span data-stu-id="88021-114">public Common lookupReference(\[FormReferenceControl formReferenceControl\])</span></span>                                |                                                                                                                                                                         |
| <span data-ttu-id="88021-115">public Common resolveReference(\[FormReferenceControl formReferenceControl\])</span><span class="sxs-lookup"><span data-stu-id="88021-115">public Common resolveReference(\[FormReferenceControl formReferenceControl\])</span></span>                               |                                                                                                                                                                         |
| <span data-ttu-id="88021-116">public str resolveAmbiguousReference(\[FormControl formControl\])</span><span class="sxs-lookup"><span data-stu-id="88021-116">public str resolveAmbiguousReference(\[FormControl formControl\])</span></span>                                           |                                                                                                                                                                         |
| <span data-ttu-id="88021-117">public int allowAdd(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="88021-117">public int allowAdd(\[int value\])</span></span>                                                                          | <span data-ttu-id="88021-118">フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-118">Sets or returns the value of the allowAdd property for the form data object.</span></span>                                                                                            |
| <span data-ttu-id="88021-119">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-119">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="88021-120">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="88021-120">Determines whether the user can modify the contents of the control.</span></span>                                                                                                     |
| <span data-ttu-id="88021-121">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="88021-121">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                                                         |
| <span data-ttu-id="88021-122">public FormDataSource datasource()</span><span class="sxs-lookup"><span data-stu-id="88021-122">public FormDataSource datasource()</span></span>                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="88021-123">public boolean editAutoPostback(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-123">public boolean editAutoPostback(\[boolean value\])</span></span>                                                          |                                                                                                                                                                         |
| <span data-ttu-id="88021-124">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-124">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="88021-125">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="88021-125">Determines whether the object is enabled or disabled.</span></span>                                                                                                                   |
| <span data-ttu-id="88021-126">public FieldId fieldId()</span><span class="sxs-lookup"><span data-stu-id="88021-126">public FieldId fieldId()</span></span>                                                                                    |                                                                                                                                                                         |
| <span data-ttu-id="88021-127">public str helpField()</span><span class="sxs-lookup"><span data-stu-id="88021-127">public str helpField()</span></span>                                                                                      | <span data-ttu-id="88021-128">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="88021-128">Returns the Help text for the control.</span></span>                                                                                                                                  |
| <span data-ttu-id="88021-129">public str labelText()</span><span class="sxs-lookup"><span data-stu-id="88021-129">public str labelText()</span></span>                                                                                      | <span data-ttu-id="88021-130">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="88021-130">Returns the label text for the control.</span></span>                                                                                                                                 |
| <span data-ttu-id="88021-131">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-131">public boolean mandatory(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="88021-132">データ フィールドが必須であるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-132">Sets or returns a value that indicates whether the data field is mandatory.</span></span>                                                                                             |
| <span data-ttu-id="88021-133">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-133">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="88021-134">ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-134">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control that is associated with the data source.</span></span> |
| <span data-ttu-id="88021-135">public str toolTip()</span><span class="sxs-lookup"><span data-stu-id="88021-135">public str toolTip()</span></span>                                                                                        |                                                                                                                                                                         |
| <span data-ttu-id="88021-136">public boolean validate()</span><span class="sxs-lookup"><span data-stu-id="88021-136">public boolean validate()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="88021-137">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="88021-137">public boolean visible(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="88021-138">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-138">Sets or returns a value that indicates whether the control is visible.</span></span>                                                                                                  |
| <span data-ttu-id="88021-139">private void OnModified(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="88021-139">private void OnModified(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span></span>                            |                                                                                                                                                                         |
| <span data-ttu-id="88021-140">private void OnValidated(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="88021-140">private void OnValidated(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span></span>                           |                                                                                                                                                                         |
| <span data-ttu-id="88021-141">public void modified()</span><span class="sxs-lookup"><span data-stu-id="88021-141">public void modified()</span></span>                                                                                      | <span data-ttu-id="88021-142">フィールドが正常に検証され、現在のレコードで変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="88021-142">Indicates that the field has been successfully validated and modified in the current record.</span></span>                                                                            |
| <span data-ttu-id="88021-143">private void OnValidating(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="88021-143">private void OnValidating(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])</span></span>                          |                                                                                                                                                                         |
| <span data-ttu-id="88021-144">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="88021-144">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                                                         |
| <span data-ttu-id="88021-145">public void restore()</span><span class="sxs-lookup"><span data-stu-id="88021-145">public void restore()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="88021-146">public void lookup(FormControl formControl, str filterStr)</span><span class="sxs-lookup"><span data-stu-id="88021-146">public void lookup(FormControl formControl, str filterStr)</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="88021-147">public void dataChanged()</span><span class="sxs-lookup"><span data-stu-id="88021-147">public void dataChanged()</span></span>                                                                                   |                                                                                                                                                                         |
| <span data-ttu-id="88021-148">public void jumpRef()</span><span class="sxs-lookup"><span data-stu-id="88021-148">public void jumpRef()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="88021-149">public void context()</span><span class="sxs-lookup"><span data-stu-id="88021-149">public void context()</span></span>                                                                                       |                                                                                                                                                                         |
| <span data-ttu-id="88021-150">public void find()</span><span class="sxs-lookup"><span data-stu-id="88021-150">public void find()</span></span>                                                                                          |                                                                                                                                                                         |
| <span data-ttu-id="88021-151">public void filter(\[str filterStr\], \[NoYes clearPrev\])</span><span class="sxs-lookup"><span data-stu-id="88021-151">public void filter(\[str filterStr\], \[NoYes clearPrev\])</span></span>                                                  |                                                                                                                                                                         |
| <span data-ttu-id="88021-152">public void performFormLookup(xFormRun form, FormControl formControl)</span><span class="sxs-lookup"><span data-stu-id="88021-152">public void performFormLookup(xFormRun form, FormControl formControl)</span></span>                                       |                                                                                                                                                                         |

## <a name="method-lookupreference"></a><span data-ttu-id="88021-153">メソッド lookupReference</span><span class="sxs-lookup"><span data-stu-id="88021-153">Method lookupReference</span></span>

```xpp
public Common lookupReference([FormReferenceControl formReferenceControl])
```

### <a name="parameters---lookupreference"></a><span data-ttu-id="88021-154">パラメーター - lookupReference</span><span class="sxs-lookup"><span data-stu-id="88021-154">Parameters - lookupReference</span></span>

<span data-ttu-id="88021-155">formReferenceControl</span><span class="sxs-lookup"><span data-stu-id="88021-155">formReferenceControl</span></span>  

### <a name="return-value---lookupreference"></a><span data-ttu-id="88021-156">戻り値 - lookupReference</span><span class="sxs-lookup"><span data-stu-id="88021-156">Return Value - lookupReference</span></span>

## <a name="method-resolvereference"></a><span data-ttu-id="88021-157">メソッド resolveReference</span><span class="sxs-lookup"><span data-stu-id="88021-157">Method resolveReference</span></span>

```xpp
public Common resolveReference([FormReferenceControl formReferenceControl])
```

### <a name="parameters---resolvereference"></a><span data-ttu-id="88021-158">パラメーター - resolveReference</span><span class="sxs-lookup"><span data-stu-id="88021-158">Parameters - resolveReference</span></span>

<span data-ttu-id="88021-159">formReferenceControl</span><span class="sxs-lookup"><span data-stu-id="88021-159">formReferenceControl</span></span>  

### <a name="return-value---resolvereference"></a><span data-ttu-id="88021-160">戻り値 - resolveReference</span><span class="sxs-lookup"><span data-stu-id="88021-160">Return Value - resolveReference</span></span>

## <a name="method-resolveambiguousreference"></a><span data-ttu-id="88021-161">メソッド resolveAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="88021-161">Method resolveAmbiguousReference</span></span>

```xpp
public str resolveAmbiguousReference([FormControl formControl])
```

### <a name="parameters---resolveambiguousreference"></a><span data-ttu-id="88021-162">パラメーター - resolveAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="88021-162">Parameters - resolveAmbiguousReference</span></span>

<span data-ttu-id="88021-163">formControl</span><span class="sxs-lookup"><span data-stu-id="88021-163">formControl</span></span>  

### <a name="return-value---resolveambiguousreference"></a><span data-ttu-id="88021-164">戻り値 - resolveAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="88021-164">Return Value - resolveAmbiguousReference</span></span>

## <a name="method-allowadd"></a><span data-ttu-id="88021-165">メソッド allowAdd</span><span class="sxs-lookup"><span data-stu-id="88021-165">Method allowAdd</span></span>

<span data-ttu-id="88021-166">フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-166">Sets or returns the value of the allowAdd property for the form data object.</span></span>

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a><span data-ttu-id="88021-167">パラメーター - allowAdd</span><span class="sxs-lookup"><span data-stu-id="88021-167">Parameters - allowAdd</span></span>

<span data-ttu-id="88021-168">値</span><span class="sxs-lookup"><span data-stu-id="88021-168">value</span></span>  
<span data-ttu-id="88021-169">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="88021-169">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowadd"></a><span data-ttu-id="88021-170">戻り値 - allowAdd</span><span class="sxs-lookup"><span data-stu-id="88021-170">Return Value - allowAdd</span></span>

<span data-ttu-id="88021-171">allowAdd プロパティが No、Restricted もしくは Yes に設定されているかどうかを示す FormAllowAdd 列挙値。</span><span class="sxs-lookup"><span data-stu-id="88021-171">A FormAllowAdd enumeration value that indicates whether the allowAdd property is set to No, Restricted, or Yes.</span></span>

### <a name="examples---allowadd"></a><span data-ttu-id="88021-172">例 - allowAdd</span><span class="sxs-lookup"><span data-stu-id="88021-172">Examples - allowAdd</span></span>

<span data-ttu-id="88021-173">次の例は、allowAdd プロパティを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-173">The following example shows how to retrieve and set the allowAdd property.</span></span>

```xpp
// fdo previously assigned to a FormDataObject object. 
// Retrieve the allowAdd property. 
nAllowAdd = fdo.allowAdd(); 
// Set the allowAdd property. 
fdo.allowAdd(FormAllowAdd::Restricted);
```

## <a name="method-allowedit"></a><span data-ttu-id="88021-174">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="88021-174">Method allowEdit</span></span>

<span data-ttu-id="88021-175">ユーザーがコントロールの内容を修正できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="88021-175">Determines whether the user can modify the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="88021-176">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="88021-176">Parameters - allowEdit</span></span>

<span data-ttu-id="88021-177">値</span><span class="sxs-lookup"><span data-stu-id="88021-177">value</span></span>  
<span data-ttu-id="88021-178">allowEdit プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="88021-178">The value to assign to the allowEdit property.</span></span>

### <a name="return-value---allowedit"></a><span data-ttu-id="88021-179">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="88021-179">Return Value - allowEdit</span></span>

<span data-ttu-id="88021-180">コントロールを変更することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="88021-180">true if the control can be modified; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="88021-181">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="88021-181">Remarks - allowEdit</span></span>

<span data-ttu-id="88021-182">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="88021-182">If this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

### <a name="examples---allowedit"></a><span data-ttu-id="88021-183">例 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="88021-183">Examples - allowEdit</span></span>

<span data-ttu-id="88021-184">次の例は、allowEdit プロパティの値を取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-184">The following example shows how to retrieve and set the value of the allowEdit property.</span></span>

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-datafield"></a><span data-ttu-id="88021-185">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="88021-185">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="88021-186">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="88021-186">Parameters - dataField</span></span>

<span data-ttu-id="88021-187">値</span><span class="sxs-lookup"><span data-stu-id="88021-187">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="88021-188">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="88021-188">Return Value - dataField</span></span>

## <a name="method-datasource"></a><span data-ttu-id="88021-189">メソッド datasource</span><span class="sxs-lookup"><span data-stu-id="88021-189">Method datasource</span></span>

```xpp
public FormDataSource datasource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="88021-190">戻り値 - datasource</span><span class="sxs-lookup"><span data-stu-id="88021-190">Return Value - datasource</span></span>

## <a name="method-editautopostback"></a><span data-ttu-id="88021-191">メソッド editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="88021-191">Method editAutoPostback</span></span>

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a><span data-ttu-id="88021-192">パラメーター - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="88021-192">Parameters - editAutoPostback</span></span>

<span data-ttu-id="88021-193">値</span><span class="sxs-lookup"><span data-stu-id="88021-193">value</span></span>  

### <a name="return-value---editautopostback"></a><span data-ttu-id="88021-194">戻り値 - editAutoPostback</span><span class="sxs-lookup"><span data-stu-id="88021-194">Return Value - editAutoPostback</span></span>

## <a name="method-enabled"></a><span data-ttu-id="88021-195">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="88021-195">Method enabled</span></span>

<span data-ttu-id="88021-196">オブジェクトが有効か無効かを決定します。</span><span class="sxs-lookup"><span data-stu-id="88021-196">Determines whether the object is enabled or disabled.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="88021-197">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="88021-197">Parameters - enabled</span></span>

<span data-ttu-id="88021-198">値</span><span class="sxs-lookup"><span data-stu-id="88021-198">value</span></span>  
<span data-ttu-id="88021-199">コントロールが有効かどうかを指定するブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="88021-199">A Boolean value that specifies whether the control is enabled.</span></span>

### <a name="return-value---enabled"></a><span data-ttu-id="88021-200">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="88021-200">Return Value - enabled</span></span>

<span data-ttu-id="88021-201">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="88021-201">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="88021-202">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="88021-202">Remarks - enabled</span></span>

<span data-ttu-id="88021-203">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="88021-203">The enabled property lets you enable or disable a control at run time.</span></span> <span data-ttu-id="88021-204">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="88021-204">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="88021-205">また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="88021-205">You can also disable a control that is used only for display purposes, such as an error message that provides read-only information.</span></span>

### <a name="examples---enabled"></a><span data-ttu-id="88021-206">例 - enabled</span><span class="sxs-lookup"><span data-stu-id="88021-206">Examples - enabled</span></span>

<span data-ttu-id="88021-207">次の例は、コントロールの有効なプロパティを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-207">The following example shows how to retrieve and set the enabled property for a control.</span></span>

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1", this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-fieldid"></a><span data-ttu-id="88021-208">メソッド fieldId</span><span class="sxs-lookup"><span data-stu-id="88021-208">Method fieldId</span></span>

```xpp
public FieldId fieldId()
```

### <a name="return-value---fieldid"></a><span data-ttu-id="88021-209">戻り値 - fieldId</span><span class="sxs-lookup"><span data-stu-id="88021-209">Return Value - fieldId</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="88021-210">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="88021-210">Method helpField</span></span>

<span data-ttu-id="88021-211">コントロールのヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="88021-211">Returns the Help text for the control.</span></span>

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a><span data-ttu-id="88021-212">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="88021-212">Return Value - helpField</span></span>

<span data-ttu-id="88021-213">コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="88021-213">The Help text for the control; an empty string if there is no Help text for the control.</span></span>

### <a name="examples---helpfield"></a><span data-ttu-id="88021-214">例 - helpField</span><span class="sxs-lookup"><span data-stu-id="88021-214">Examples - helpField</span></span>

<span data-ttu-id="88021-215">次の例は、helpField メソッドの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-215">The following example shows how to use the helpField method.</span></span>

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-labeltext"></a><span data-ttu-id="88021-216">メソッド labelText</span><span class="sxs-lookup"><span data-stu-id="88021-216">Method labelText</span></span>

<span data-ttu-id="88021-217">コントロールのラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="88021-217">Returns the label text for the control.</span></span>

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a><span data-ttu-id="88021-218">戻り値 - labelText</span><span class="sxs-lookup"><span data-stu-id="88021-218">Return Value - labelText</span></span>

<span data-ttu-id="88021-219">コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="88021-219">The label text for the control; an empty string if there is no label text for the control.</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="88021-220">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="88021-220">Method mandatory</span></span>

<span data-ttu-id="88021-221">データ フィールドが必須であるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-221">Sets or returns a value that indicates whether the data field is mandatory.</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="88021-222">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="88021-222">Parameters - mandatory</span></span>

<span data-ttu-id="88021-223">値</span><span class="sxs-lookup"><span data-stu-id="88021-223">value</span></span>  
<span data-ttu-id="88021-224">フィールドの必須プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="88021-224">The value to assign to the mandatory property of the field.</span></span>

### <a name="return-value---mandatory"></a><span data-ttu-id="88021-225">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="88021-225">Return Value - mandatory</span></span>

<span data-ttu-id="88021-226">フィールドが必須項目である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="88021-226">true if the field is mandatory; otherwise, false.</span></span>

### <a name="examples---mandatory"></a><span data-ttu-id="88021-227">例 - mandatory</span><span class="sxs-lookup"><span data-stu-id="88021-227">Examples - mandatory</span></span>

<span data-ttu-id="88021-228">次の例は、フィールドの必須プロパティを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-228">The following example shows how to retrieve and set the mandatory property for the field.</span></span>

```xpp
// Return the value of the mandatory property. 
info (strfmt("mandatory: %1", fdo.mandatory())); 
// Set the value of the mandatory property. 
fdo.mandatory(false);
```

## <a name="method-skip"></a><span data-ttu-id="88021-229">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="88021-229">Method skip</span></span>

<span data-ttu-id="88021-230">ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-230">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control that is associated with the data source.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="88021-231">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="88021-231">Parameters - skip</span></span>

<span data-ttu-id="88021-232">値</span><span class="sxs-lookup"><span data-stu-id="88021-232">value</span></span>  
<span data-ttu-id="88021-233">コントロールに関連付けられているデータ ソースの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="88021-233">The value to assign to the skip property of the data source that is associated with the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="88021-234">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="88021-234">Return Value - skip</span></span>

<span data-ttu-id="88021-235">データ ソースに関連付けられているコントロールに移動するためユーザーが TAB キーを押すと、コントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="88021-235">true if the control is skipped when the user presses the TAB key to move to the control that is associated with the data source; otherwise, false.</span></span>

### <a name="remarks---skip"></a><span data-ttu-id="88021-236">備考 - skip</span><span class="sxs-lookup"><span data-stu-id="88021-236">Remarks - skip</span></span>

<span data-ttu-id="88021-237">有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。</span><span class="sxs-lookup"><span data-stu-id="88021-237">If the enabled property is true, the allowEdit property is false, and the skip property is true, the user cannot change the contents of the control but can still copy the contents of the control.</span></span> <span data-ttu-id="88021-238">コントロールのスキップ値が true またはデータ ソースのスキップ値が true の場合、コントロールはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="88021-238">Controls are skipped if either the control's skip value is true or the data source's skip value is true.</span></span>

### <a name="examples---skip"></a><span data-ttu-id="88021-239">例 - skip</span><span class="sxs-lookup"><span data-stu-id="88021-239">Examples - skip</span></span>

<span data-ttu-id="88021-240">以下は、コントロールのデータ ソースのスキップ プロパティを取得および設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88021-240">The following shows how to retrieve and set the skip property of a data source for a control.</span></span>

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-tooltip"></a><span data-ttu-id="88021-241">メソッド toolTip</span><span class="sxs-lookup"><span data-stu-id="88021-241">Method toolTip</span></span>

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a><span data-ttu-id="88021-242">戻り値 - toolTip</span><span class="sxs-lookup"><span data-stu-id="88021-242">Return Value - toolTip</span></span>

## <a name="method-validate"></a><span data-ttu-id="88021-243">メソッド validate</span><span class="sxs-lookup"><span data-stu-id="88021-243">Method validate</span></span>

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a><span data-ttu-id="88021-244">戻り値 - validate</span><span class="sxs-lookup"><span data-stu-id="88021-244">Return Value - validate</span></span>

## <a name="method-visible"></a><span data-ttu-id="88021-245">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="88021-245">Method visible</span></span>

<span data-ttu-id="88021-246">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="88021-246">Sets or returns a value that indicates whether the control is visible.</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="88021-247">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="88021-247">Parameters - visible</span></span>

<span data-ttu-id="88021-248">値</span><span class="sxs-lookup"><span data-stu-id="88021-248">value</span></span>  
<span data-ttu-id="88021-249">コントロールの表示設定に割り当てられている値。</span><span class="sxs-lookup"><span data-stu-id="88021-249">The value that is assigned to the visibility setting for the control.</span></span>

### <a name="return-value---visible"></a><span data-ttu-id="88021-250">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="88021-250">Return Value - visible</span></span>

<span data-ttu-id="88021-251">コントロールが可視である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="88021-251">true if the control is visible; otherwise, false.</span></span> <span data-ttu-id="88021-252">既定は true です。</span><span class="sxs-lookup"><span data-stu-id="88021-252">The default is true.</span></span>

### <a name="remarks---visible"></a><span data-ttu-id="88021-253">備考 - visible</span><span class="sxs-lookup"><span data-stu-id="88021-253">Remarks - visible</span></span>

<span data-ttu-id="88021-254">データ ソース フィールドを参照するコントロールは、コントロールおよび基になるデータ ソース フィールドの両方で Visible プロパティが true に設定されている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="88021-254">Controls that refer to a data source field are visible only when the visible property is set to true on both the control and the underlying data source field.</span></span> <span data-ttu-id="88021-255">コントロールの代わりに、データ ソース フィールドのプロパティを設定する場合、フォーム全体で、このフィールドは一貫して処理されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="88021-255">If you set the property on the data source field instead of on the control, you guarantee that the field is handled consistently throughout the form.</span></span> <span data-ttu-id="88021-256">これにより、アップグレードが容易になります。</span><span class="sxs-lookup"><span data-stu-id="88021-256">This makes upgrades easier.</span></span>

## <a name="method-onmodified"></a><span data-ttu-id="88021-257">メソッド OnModified</span><span class="sxs-lookup"><span data-stu-id="88021-257">Method OnModified</span></span>

```xpp
private void OnModified([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onmodified"></a><span data-ttu-id="88021-258">パラメーター - OnModified</span><span class="sxs-lookup"><span data-stu-id="88021-258">Parameters - OnModified</span></span>

<span data-ttu-id="88021-259">sender</span><span class="sxs-lookup"><span data-stu-id="88021-259">sender</span></span>  

<!-- -->

<span data-ttu-id="88021-260">e</span><span class="sxs-lookup"><span data-stu-id="88021-260">e</span></span>  

## <a name="method-onvalidated"></a><span data-ttu-id="88021-261">メソッド OnValidated</span><span class="sxs-lookup"><span data-stu-id="88021-261">Method OnValidated</span></span>

```xpp
private void OnValidated([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onvalidated"></a><span data-ttu-id="88021-262">パラメーター - OnValidated</span><span class="sxs-lookup"><span data-stu-id="88021-262">Parameters - OnValidated</span></span>

<span data-ttu-id="88021-263">sender</span><span class="sxs-lookup"><span data-stu-id="88021-263">sender</span></span>  

<!-- -->

<span data-ttu-id="88021-264">e</span><span class="sxs-lookup"><span data-stu-id="88021-264">e</span></span>  

## <a name="method-modified"></a><span data-ttu-id="88021-265">メソッド modified</span><span class="sxs-lookup"><span data-stu-id="88021-265">Method modified</span></span>

<span data-ttu-id="88021-266">フィールドが正常に検証され、現在のレコードで変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="88021-266">Indicates that the field has been successfully validated and modified in the current record.</span></span>

```xpp
public void modified()
```

### <a name="remarks---modified"></a><span data-ttu-id="88021-267">備考 - modified</span><span class="sxs-lookup"><span data-stu-id="88021-267">Remarks - modified</span></span>

<span data-ttu-id="88021-268">このメソッドは、検証メソッドが true を返した場合、コントロールの変更されたメソッドから呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="88021-268">This method is called from the modified method on controls if the validation methods returned true.</span></span> <span data-ttu-id="88021-269">このメソッドをオーバーライドして、修正された値に基づく他の値の再計算を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="88021-269">You can override this method to allow for recalculation of other values that are based on the modified values.</span></span> <span data-ttu-id="88021-270">super() メソッドの呼び出しは、テーブルの modifiedField メソッドが呼び出されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="88021-270">The call to the super() method guarantees that the modifiedField method on the table is called.</span></span> <span data-ttu-id="88021-271">変更済は現在のレコードのフィールドの値が変更されたことを意味しますが、レコードが保存されるまでこの値はデータベースに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="88021-271">Modified means that the value of the field on the current record has changed, but the value is not written to the database before the record is saved.</span></span>

## <a name="method-onvalidating"></a><span data-ttu-id="88021-272">メソッド OnValidating</span><span class="sxs-lookup"><span data-stu-id="88021-272">Method OnValidating</span></span>

```xpp
private void OnValidating([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onvalidating"></a><span data-ttu-id="88021-273">パラメーター - OnValidating</span><span class="sxs-lookup"><span data-stu-id="88021-273">Parameters - OnValidating</span></span>

<span data-ttu-id="88021-274">sender</span><span class="sxs-lookup"><span data-stu-id="88021-274">sender</span></span>  

<!-- -->

<span data-ttu-id="88021-275">e</span><span class="sxs-lookup"><span data-stu-id="88021-275">e</span></span>  

## <a name="method-registeroverridemethod"></a><span data-ttu-id="88021-276">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="88021-276">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="88021-277">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="88021-277">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="88021-278">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="88021-278">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="88021-279">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="88021-279">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="88021-280">overrideObject</span><span class="sxs-lookup"><span data-stu-id="88021-280">overrideObject</span></span>  

## <a name="method-restore"></a><span data-ttu-id="88021-281">メソッド restore</span><span class="sxs-lookup"><span data-stu-id="88021-281">Method restore</span></span>

```xpp
public void restore()
```

## <a name="method-lookup"></a><span data-ttu-id="88021-282">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="88021-282">Method lookup</span></span>

```xpp
public void lookup(FormControl formControl, str filterStr)
```

### <a name="parameters---lookup"></a><span data-ttu-id="88021-283">パラメーター - lookup</span><span class="sxs-lookup"><span data-stu-id="88021-283">Parameters - lookup</span></span>

<span data-ttu-id="88021-284">formControl</span><span class="sxs-lookup"><span data-stu-id="88021-284">formControl</span></span>  

<!-- -->

<span data-ttu-id="88021-285">filterStr</span><span class="sxs-lookup"><span data-stu-id="88021-285">filterStr</span></span>  

## <a name="method-datachanged"></a><span data-ttu-id="88021-286">メソッド dataChanged</span><span class="sxs-lookup"><span data-stu-id="88021-286">Method dataChanged</span></span>

```xpp
public void dataChanged()
```

## <a name="method-jumpref"></a><span data-ttu-id="88021-287">メソッド jumpRef</span><span class="sxs-lookup"><span data-stu-id="88021-287">Method jumpRef</span></span>

```xpp
public void jumpRef()
```

## <a name="method-context"></a><span data-ttu-id="88021-288">メソッド context</span><span class="sxs-lookup"><span data-stu-id="88021-288">Method context</span></span>

```xpp
public void context()
```

## <a name="method-find"></a><span data-ttu-id="88021-289">メソッド find</span><span class="sxs-lookup"><span data-stu-id="88021-289">Method find</span></span>

```xpp
public void find()
```

## <a name="method-filter"></a><span data-ttu-id="88021-290">メソッド filter</span><span class="sxs-lookup"><span data-stu-id="88021-290">Method filter</span></span>

```xpp
public void filter([str filterStr], [NoYes clearPrev])
```

### <a name="parameters---filter"></a><span data-ttu-id="88021-291">パラメーター - filter</span><span class="sxs-lookup"><span data-stu-id="88021-291">Parameters - filter</span></span>

<span data-ttu-id="88021-292">filterStr</span><span class="sxs-lookup"><span data-stu-id="88021-292">filterStr</span></span>  

<!-- -->

<span data-ttu-id="88021-293">clearPrev</span><span class="sxs-lookup"><span data-stu-id="88021-293">clearPrev</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="88021-294">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="88021-294">Method performFormLookup</span></span>

```xpp
public void performFormLookup(xFormRun form, FormControl formControl)
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="88021-295">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="88021-295">Parameters - performFormLookup</span></span>

<span data-ttu-id="88021-296">フォーム</span><span class="sxs-lookup"><span data-stu-id="88021-296">form</span></span>  

<!-- -->

<span data-ttu-id="88021-297">formControl</span><span class="sxs-lookup"><span data-stu-id="88021-297">formControl</span></span>  

