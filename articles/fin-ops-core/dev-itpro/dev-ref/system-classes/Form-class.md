---
title: Form クラス
description: このトピックでは、Form クラスについて説明します。
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
ms.openlocfilehash: 1a0c9f25d7529b393f401cf14989d8e59f7f53a4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502978"
---
# <a name="class-form"></a><span data-ttu-id="3e800-103">クラス フォーム</span><span class="sxs-lookup"><span data-stu-id="3e800-103">Class Form</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Form extends TreeNode
```

<span data-ttu-id="3e800-104">フォーム クラスは、デザイン時のフォームのインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="3e800-104">The Form class represents an instance of a design-time form.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e800-105">備考</span><span class="sxs-lookup"><span data-stu-id="3e800-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3e800-106">例</span><span class="sxs-lookup"><span data-stu-id="3e800-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3e800-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e800-107">Methods</span></span>

| <span data-ttu-id="3e800-108">方法</span><span class="sxs-lookup"><span data-stu-id="3e800-108">Method</span></span>                                                                                                                           | <span data-ttu-id="3e800-109">説明</span><span class="sxs-lookup"><span data-stu-id="3e800-109">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e800-110">public FormBuildControl addControl(FormControlType controlType, str controlName)</span><span class="sxs-lookup"><span data-stu-id="3e800-110">public FormBuildControl addControl(FormControlType controlType, str controlName)</span></span>                                                 |                                                                                                                           |
| <span data-ttu-id="3e800-111">public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span><span class="sxs-lookup"><span data-stu-id="3e800-111">public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span></span> |                                                                                                                           |
| <span data-ttu-id="3e800-112">public FormBuildDataSource addDataSource(str name, \[str tableName\])</span><span class="sxs-lookup"><span data-stu-id="3e800-112">public FormBuildDataSource addDataSource(str name, \[str tableName\])</span></span>                                                            |                                                                                                                           |
| <span data-ttu-id="3e800-113">public List rootFormDataSources()</span><span class="sxs-lookup"><span data-stu-id="3e800-113">public List rootFormDataSources()</span></span>                                                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-114">public FormBuildDesign addDesign(str name)</span><span class="sxs-lookup"><span data-stu-id="3e800-114">public FormBuildDesign addDesign(str name)</span></span>                                                                                       |                                                                                                                           |
| <span data-ttu-id="3e800-115">public Query query(str queryName)</span><span class="sxs-lookup"><span data-stu-id="3e800-115">public Query query(str queryName)</span></span>                                                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-116">public boolean allowPreLoading(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-116">public boolean allowPreLoading(\[boolean value\])</span></span>                                                                                | <span data-ttu-id="3e800-117">関連付けられた FormRun インスタンスの作成時にプリロードされたインスタンスを使用できるかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="3e800-117">A Boolean value that determines whether a preloaded instance can be used when the associated FormRun instance is created.</span></span> |
| <span data-ttu-id="3e800-118">public boolean autoCacheUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-118">public boolean autoCacheUpdate(\[boolean value\])</span></span>                                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-119">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-119">public str changedBy(\[str value\])</span></span>                                                                                              | <span data-ttu-id="3e800-120">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-120">Gets or sets the name of the user who last changed the application object.</span></span>                                                |
| <span data-ttu-id="3e800-121">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-121">public Date changedDate(\[Date value\])</span></span>                                                                                          | <span data-ttu-id="3e800-122">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-122">Gets or sets the date an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="3e800-123">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-123">public str changedTime(\[str value\])</span></span>                                                                                            | <span data-ttu-id="3e800-124">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-124">Gets or sets the time an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="3e800-125">public ChangeGroupMode changeGroupMode(\[ChangeGroupMode value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-125">public ChangeGroupMode changeGroupMode(\[ChangeGroupMode value\])</span></span>                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-126">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-126">public str createdBy(\[str value\])</span></span>                                                                                              | <span data-ttu-id="3e800-127">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-127">Gets or sets the name of the user who created the application object.</span></span>                                                     |
| <span data-ttu-id="3e800-128">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-128">public Date creationDate(\[Date value\])</span></span>                                                                                         | <span data-ttu-id="3e800-129">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-129">Gets or sets the date an application object was created.</span></span>                                                                  |
| <span data-ttu-id="3e800-130">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-130">public str creationTime(\[str value\])</span></span>                                                                                           |                                                                                                                           |
| <span data-ttu-id="3e800-131">public FormBuildDataSource dataSource(AnyType objectSet)</span><span class="sxs-lookup"><span data-stu-id="3e800-131">public FormBuildDataSource dataSource(AnyType objectSet)</span></span>                                                                         |                                                                                                                           |
| <span data-ttu-id="3e800-132">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="3e800-132">public int dataSourceCount()</span></span>                                                                                                     |                                                                                                                           |
| <span data-ttu-id="3e800-133">public FormBuildDesign design(\[int designNo\])</span><span class="sxs-lookup"><span data-stu-id="3e800-133">public FormBuildDesign design(\[int designNo\])</span></span>                                                                                  |                                                                                                                           |
| <span data-ttu-id="3e800-134">public int formTemplate(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-134">public int formTemplate(\[int value\])</span></span>                                                                                           |                                                                                                                           |
| <span data-ttu-id="3e800-135">public str interactionClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-135">public str interactionClass(\[str value\])</span></span>                                                                                       |                                                                                                                           |
| <span data-ttu-id="3e800-136">public boolean isLoadedForInference()</span><span class="sxs-lookup"><span data-stu-id="3e800-136">public boolean isLoadedForInference()</span></span>                                                                                            |                                                                                                                           |
| <span data-ttu-id="3e800-137">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-137">public str name(\[str value\])</span></span>                                                                                                   | <span data-ttu-id="3e800-138">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-138">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="3e800-139">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-139">public Guid origin(\[Guid value\])</span></span>                                                                                               |                                                                                                                           |
| <span data-ttu-id="3e800-140">::public static boolean formKernelObjectHasMethod (Object kernelObject, str methodName)</span><span class="sxs-lookup"><span data-stu-id="3e800-140">::public static boolean formKernelObjectHasMethod(Object kernelObject, str methodName)</span></span>                                           |                                                                                                                           |
| <span data-ttu-id="3e800-141">::public static boolean formObjectSetHasMethod (FormObjectSet formObjectSet, str methodName)</span><span class="sxs-lookup"><span data-stu-id="3e800-141">::public static boolean formObjectSetHasMethod(FormObjectSet formObjectSet, str methodName)</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="3e800-142">::public static boolean formRunHasMethod (xFormRun formRun, str methodName)</span><span class="sxs-lookup"><span data-stu-id="3e800-142">::public static boolean formRunHasMethod(xFormRun formRun, str methodName)</span></span>                                                       |                                                                                                                           |
| <span data-ttu-id="3e800-143">::public static str getSetupUserQueryElementName (MenuItemType menuItemType, str menuItemName)</span><span class="sxs-lookup"><span data-stu-id="3e800-143">::public static str getSetupUserQueryElementName(MenuItemType menuItemType, str menuItemName)</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="3e800-144">public void new(\[str name\], \[boolean buildMode\])</span><span class="sxs-lookup"><span data-stu-id="3e800-144">public void new(\[str name\], \[boolean buildMode\])</span></span>                                                                             | <span data-ttu-id="3e800-145">Form クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e800-145">Initializes a new instance of the Form class.</span></span>                                                                             |
| <span data-ttu-id="3e800-146">public void inInitializeDesign(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="3e800-146">public void inInitializeDesign(\[boolean value\])</span></span>                                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-147">public void save()</span><span class="sxs-lookup"><span data-stu-id="3e800-147">public void save()</span></span>                                                                                                               |                                                                                                                           |
| <span data-ttu-id="3e800-148">public void load(str name, \[boolean buildMode\])</span><span class="sxs-lookup"><span data-stu-id="3e800-148">public void load(str name, \[boolean buildMode\])</span></span>                                                                                |                                                                                                                           |
| <span data-ttu-id="3e800-149">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="3e800-149">public void finalize()</span></span>                                                                                                           |                                                                                                                           |

## <a name="method-addcontrol"></a><span data-ttu-id="3e800-150">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="3e800-150">Method addControl</span></span>

```xpp
public FormBuildControl addControl(FormControlType controlType, str controlName)
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="3e800-151">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="3e800-151">Parameters - addControl</span></span>

<span data-ttu-id="3e800-152">controlType</span><span class="sxs-lookup"><span data-stu-id="3e800-152">controlType</span></span>  

<!-- -->

<span data-ttu-id="3e800-153">controlName</span><span class="sxs-lookup"><span data-stu-id="3e800-153">controlName</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="3e800-154">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="3e800-154">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="3e800-155">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="3e800-155">Method addControlEx</span></span>

```xpp
public FormBuildControl addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="3e800-156">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="3e800-156">Parameters - addControlEx</span></span>

<span data-ttu-id="3e800-157">controlClass</span><span class="sxs-lookup"><span data-stu-id="3e800-157">controlClass</span></span>  

<!-- -->

<span data-ttu-id="3e800-158">controlName</span><span class="sxs-lookup"><span data-stu-id="3e800-158">controlName</span></span>  

<!-- -->

<span data-ttu-id="3e800-159">insertAfter</span><span class="sxs-lookup"><span data-stu-id="3e800-159">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="3e800-160">pushFront</span><span class="sxs-lookup"><span data-stu-id="3e800-160">pushFront</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="3e800-161">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="3e800-161">Return Value - addControlEx</span></span>

## <a name="method-adddatasource"></a><span data-ttu-id="3e800-162">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-162">Method addDataSource</span></span>

```xpp
public FormBuildDataSource addDataSource(str name, [str tableName])
```

### <a name="parameters---adddatasource"></a><span data-ttu-id="3e800-163">パラメーター - addDataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-163">Parameters - addDataSource</span></span>

<span data-ttu-id="3e800-164">名前</span><span class="sxs-lookup"><span data-stu-id="3e800-164">name</span></span>  

<!-- -->

<span data-ttu-id="3e800-165">tableName</span><span class="sxs-lookup"><span data-stu-id="3e800-165">tableName</span></span>  

### <a name="return-value---adddatasource"></a><span data-ttu-id="3e800-166">戻り値 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-166">Return Value - addDataSource</span></span>

## <a name="method-rootformdatasources"></a><span data-ttu-id="3e800-167">メソッド rootFormDataSources</span><span class="sxs-lookup"><span data-stu-id="3e800-167">Method rootFormDataSources</span></span>

```xpp
public List rootFormDataSources()
```

### <a name="return-value---rootformdatasources"></a><span data-ttu-id="3e800-168">戻り値 - rootFormDataSources</span><span class="sxs-lookup"><span data-stu-id="3e800-168">Return Value - rootFormDataSources</span></span>

## <a name="method-adddesign"></a><span data-ttu-id="3e800-169">メソッド addDesign</span><span class="sxs-lookup"><span data-stu-id="3e800-169">Method addDesign</span></span>

```xpp
public FormBuildDesign addDesign(str name)
```

### <a name="parameters---adddesign"></a><span data-ttu-id="3e800-170">パラメーター - addDesign</span><span class="sxs-lookup"><span data-stu-id="3e800-170">Parameters - addDesign</span></span>

<span data-ttu-id="3e800-171">名前</span><span class="sxs-lookup"><span data-stu-id="3e800-171">name</span></span>  

### <a name="return-value---adddesign"></a><span data-ttu-id="3e800-172">戻り値 - addDesign</span><span class="sxs-lookup"><span data-stu-id="3e800-172">Return Value - addDesign</span></span>

## <a name="method-query"></a><span data-ttu-id="3e800-173">メソッド query</span><span class="sxs-lookup"><span data-stu-id="3e800-173">Method query</span></span>

```xpp
public Query query(str queryName)
```

### <a name="parameters---query"></a><span data-ttu-id="3e800-174">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="3e800-174">Parameters - query</span></span>

<span data-ttu-id="3e800-175">queryName</span><span class="sxs-lookup"><span data-stu-id="3e800-175">queryName</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="3e800-176">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="3e800-176">Return Value - query</span></span>

## <a name="method-allowpreloading"></a><span data-ttu-id="3e800-177">メソッド allowPreLoading</span><span class="sxs-lookup"><span data-stu-id="3e800-177">Method allowPreLoading</span></span>

<span data-ttu-id="3e800-178">関連付けられた FormRun インスタンスの作成時にプリロードされたインスタンスを使用できるかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="3e800-178">A Boolean value that determines whether a preloaded instance can be used when the associated FormRun instance is created.</span></span>

```xpp
public boolean allowPreLoading([boolean value])
```

### <a name="parameters---allowpreloading"></a><span data-ttu-id="3e800-179">パラメーター - allowPreLoading</span><span class="sxs-lookup"><span data-stu-id="3e800-179">Parameters - allowPreLoading</span></span>

<span data-ttu-id="3e800-180">値</span><span class="sxs-lookup"><span data-stu-id="3e800-180">value</span></span>  
<span data-ttu-id="3e800-181">関連付けられた FormRun インスタンスが作成されるときにプリロードされたインスタンスを使用できる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3e800-181">true if a preloaded instance can be used when the associated FormRun instance is created; otherwise, false.</span></span>

### <a name="return-value---allowpreloading"></a><span data-ttu-id="3e800-182">戻り値 - allowPreLoading</span><span class="sxs-lookup"><span data-stu-id="3e800-182">Return Value - allowPreLoading</span></span>

<span data-ttu-id="3e800-183">関連付けられた FormRun インスタンスが作成されるときにプリロードされたインスタンスを使用できる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3e800-183">true if a preloaded instance can be used when the associated FormRun instance is created; otherwise, false.</span></span>

## <a name="method-autocacheupdate"></a><span data-ttu-id="3e800-184">メソッド autoCacheUpdate</span><span class="sxs-lookup"><span data-stu-id="3e800-184">Method autoCacheUpdate</span></span>

```xpp
public boolean autoCacheUpdate([boolean value])
```

### <a name="parameters---autocacheupdate"></a><span data-ttu-id="3e800-185">パラメーター - autoCacheUpdate</span><span class="sxs-lookup"><span data-stu-id="3e800-185">Parameters - autoCacheUpdate</span></span>

<span data-ttu-id="3e800-186">値</span><span class="sxs-lookup"><span data-stu-id="3e800-186">value</span></span>  

### <a name="return-value---autocacheupdate"></a><span data-ttu-id="3e800-187">戻り値 - autoCacheUpdate</span><span class="sxs-lookup"><span data-stu-id="3e800-187">Return Value - autoCacheUpdate</span></span>

## <a name="method-changedby"></a><span data-ttu-id="3e800-188">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="3e800-188">Method changedBy</span></span>

<span data-ttu-id="3e800-189">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-189">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="3e800-190">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="3e800-190">Parameters - changedBy</span></span>

<span data-ttu-id="3e800-191">値</span><span class="sxs-lookup"><span data-stu-id="3e800-191">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="3e800-192">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="3e800-192">Return Value - changedBy</span></span>

<span data-ttu-id="3e800-193">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="3e800-193">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="3e800-194">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="3e800-194">Method changedDate</span></span>

<span data-ttu-id="3e800-195">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-195">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="3e800-196">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="3e800-196">Parameters - changedDate</span></span>

<span data-ttu-id="3e800-197">値</span><span class="sxs-lookup"><span data-stu-id="3e800-197">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="3e800-198">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="3e800-198">Return Value - changedDate</span></span>

<span data-ttu-id="3e800-199">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="3e800-199">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="3e800-200">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="3e800-200">Method changedTime</span></span>

<span data-ttu-id="3e800-201">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-201">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="3e800-202">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="3e800-202">Parameters - changedTime</span></span>

<span data-ttu-id="3e800-203">値</span><span class="sxs-lookup"><span data-stu-id="3e800-203">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="3e800-204">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="3e800-204">Return Value - changedTime</span></span>

<span data-ttu-id="3e800-205">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="3e800-205">The time an application object was last changed.</span></span>

## <a name="method-changegroupmode"></a><span data-ttu-id="3e800-206">メソッド changeGroupMode</span><span class="sxs-lookup"><span data-stu-id="3e800-206">Method changeGroupMode</span></span>

```xpp
public ChangeGroupMode changeGroupMode([ChangeGroupMode value])
```

### <a name="parameters---changegroupmode"></a><span data-ttu-id="3e800-207">パラメーター - changeGroupMode</span><span class="sxs-lookup"><span data-stu-id="3e800-207">Parameters - changeGroupMode</span></span>

<span data-ttu-id="3e800-208">値</span><span class="sxs-lookup"><span data-stu-id="3e800-208">value</span></span>  

### <a name="return-value---changegroupmode"></a><span data-ttu-id="3e800-209">戻り値 - changeGroupMode</span><span class="sxs-lookup"><span data-stu-id="3e800-209">Return Value - changeGroupMode</span></span>

## <a name="method-createdby"></a><span data-ttu-id="3e800-210">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="3e800-210">Method createdBy</span></span>

<span data-ttu-id="3e800-211">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-211">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="3e800-212">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="3e800-212">Parameters - createdBy</span></span>

<span data-ttu-id="3e800-213">値</span><span class="sxs-lookup"><span data-stu-id="3e800-213">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="3e800-214">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="3e800-214">Return Value - createdBy</span></span>

<span data-ttu-id="3e800-215">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="3e800-215">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="3e800-216">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="3e800-216">Method creationDate</span></span>

<span data-ttu-id="3e800-217">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-217">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="3e800-218">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="3e800-218">Parameters - creationDate</span></span>

<span data-ttu-id="3e800-219">値</span><span class="sxs-lookup"><span data-stu-id="3e800-219">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="3e800-220">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="3e800-220">Return Value - creationDate</span></span>

<span data-ttu-id="3e800-221">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="3e800-221">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="3e800-222">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="3e800-222">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="3e800-223">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="3e800-223">Parameters - creationTime</span></span>

<span data-ttu-id="3e800-224">値</span><span class="sxs-lookup"><span data-stu-id="3e800-224">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="3e800-225">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="3e800-225">Return Value - creationTime</span></span>

## <a name="method-datasource"></a><span data-ttu-id="3e800-226">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-226">Method dataSource</span></span>

```xpp
public FormBuildDataSource dataSource(AnyType objectSet)
```

### <a name="parameters---datasource"></a><span data-ttu-id="3e800-227">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-227">Parameters - dataSource</span></span>

<span data-ttu-id="3e800-228">objectSet</span><span class="sxs-lookup"><span data-stu-id="3e800-228">objectSet</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="3e800-229">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="3e800-229">Return Value - dataSource</span></span>

## <a name="method-datasourcecount"></a><span data-ttu-id="3e800-230">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="3e800-230">Method dataSourceCount</span></span>

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a><span data-ttu-id="3e800-231">戻り値 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="3e800-231">Return Value - dataSourceCount</span></span>

## <a name="method-design"></a><span data-ttu-id="3e800-232">メソッド design</span><span class="sxs-lookup"><span data-stu-id="3e800-232">Method design</span></span>

```xpp
public FormBuildDesign design([int designNo])
```

### <a name="parameters---design"></a><span data-ttu-id="3e800-233">パラメーター - design</span><span class="sxs-lookup"><span data-stu-id="3e800-233">Parameters - design</span></span>

<span data-ttu-id="3e800-234">designNo</span><span class="sxs-lookup"><span data-stu-id="3e800-234">designNo</span></span>  

### <a name="return-value---design"></a><span data-ttu-id="3e800-235">戻り値 - design</span><span class="sxs-lookup"><span data-stu-id="3e800-235">Return Value - design</span></span>

## <a name="method-formtemplate"></a><span data-ttu-id="3e800-236">メソッド formTemplate</span><span class="sxs-lookup"><span data-stu-id="3e800-236">Method formTemplate</span></span>

```xpp
public int formTemplate([int value])
```

### <a name="parameters---formtemplate"></a><span data-ttu-id="3e800-237">パラメーター - formTemplate</span><span class="sxs-lookup"><span data-stu-id="3e800-237">Parameters - formTemplate</span></span>

<span data-ttu-id="3e800-238">値</span><span class="sxs-lookup"><span data-stu-id="3e800-238">value</span></span>  

### <a name="return-value---formtemplate"></a><span data-ttu-id="3e800-239">戻り値 - formTemplate</span><span class="sxs-lookup"><span data-stu-id="3e800-239">Return Value - formTemplate</span></span>

## <a name="method-interactionclass"></a><span data-ttu-id="3e800-240">メソッド interactionClass</span><span class="sxs-lookup"><span data-stu-id="3e800-240">Method interactionClass</span></span>

```xpp
public str interactionClass([str value])
```

### <a name="parameters---interactionclass"></a><span data-ttu-id="3e800-241">パラメーター - interactionClass</span><span class="sxs-lookup"><span data-stu-id="3e800-241">Parameters - interactionClass</span></span>

<span data-ttu-id="3e800-242">値</span><span class="sxs-lookup"><span data-stu-id="3e800-242">value</span></span>  

### <a name="return-value---interactionclass"></a><span data-ttu-id="3e800-243">戻り値 - interactionClass</span><span class="sxs-lookup"><span data-stu-id="3e800-243">Return Value - interactionClass</span></span>

## <a name="method-isloadedforinference"></a><span data-ttu-id="3e800-244">メソッド isLoadedForInference</span><span class="sxs-lookup"><span data-stu-id="3e800-244">Method isLoadedForInference</span></span>

```xpp
public boolean isLoadedForInference()
```

### <a name="return-value---isloadedforinference"></a><span data-ttu-id="3e800-245">戻り値 - isLoadedForInference</span><span class="sxs-lookup"><span data-stu-id="3e800-245">Return Value - isLoadedForInference</span></span>

## <a name="method-name"></a><span data-ttu-id="3e800-246">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3e800-246">Method name</span></span>

<span data-ttu-id="3e800-247">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3e800-247">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="3e800-248">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="3e800-248">Parameters - name</span></span>

<span data-ttu-id="3e800-249">値</span><span class="sxs-lookup"><span data-stu-id="3e800-249">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="3e800-250">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3e800-250">Return Value - name</span></span>

<span data-ttu-id="3e800-251">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="3e800-251">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="3e800-252">備考 - name</span><span class="sxs-lookup"><span data-stu-id="3e800-252">Remarks - name</span></span>

<span data-ttu-id="3e800-253">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e800-253">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="3e800-254">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="3e800-254">Begins with a letter.</span></span>
-   <span data-ttu-id="3e800-255">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="3e800-255">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="3e800-256">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3e800-256">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="3e800-257">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3e800-257">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="3e800-258">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="3e800-258">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="3e800-259">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="3e800-259">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="3e800-260">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="3e800-260">Parameters - origin</span></span>

<span data-ttu-id="3e800-261">値</span><span class="sxs-lookup"><span data-stu-id="3e800-261">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="3e800-262">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="3e800-262">Return Value - origin</span></span>

## <a name="method-formkernelobjecthasmethod"></a><span data-ttu-id="3e800-263">メソッド formKernelObjectHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-263">Method formKernelObjectHasMethod</span></span>

```xpp
public static boolean formKernelObjectHasMethod(Object kernelObject, str methodName)
```

### <a name="parameters---formkernelobjecthasmethod"></a><span data-ttu-id="3e800-264">パラメーター - formKernelObjectHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-264">Parameters - formKernelObjectHasMethod</span></span>

<span data-ttu-id="3e800-265">kernelObject</span><span class="sxs-lookup"><span data-stu-id="3e800-265">kernelObject</span></span>  

<!-- -->

<span data-ttu-id="3e800-266">methodName</span><span class="sxs-lookup"><span data-stu-id="3e800-266">methodName</span></span>  

### <a name="return-value---formkernelobjecthasmethod"></a><span data-ttu-id="3e800-267">戻り値 - formKernelObjectHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-267">Return Value - formKernelObjectHasMethod</span></span>

## <a name="method-formobjectsethasmethod"></a><span data-ttu-id="3e800-268">メソッド formObjectSetHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-268">Method formObjectSetHasMethod</span></span>

```xpp
public static boolean formObjectSetHasMethod(FormObjectSet formObjectSet, str methodName)
```

### <a name="parameters---formobjectsethasmethod"></a><span data-ttu-id="3e800-269">パラメーター - formObjectSetHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-269">Parameters - formObjectSetHasMethod</span></span>

<span data-ttu-id="3e800-270">formObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e800-270">formObjectSet</span></span>  

<!-- -->

<span data-ttu-id="3e800-271">methodName</span><span class="sxs-lookup"><span data-stu-id="3e800-271">methodName</span></span>  

### <a name="return-value---formobjectsethasmethod"></a><span data-ttu-id="3e800-272">戻り値 - formObjectSetHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-272">Return Value - formObjectSetHasMethod</span></span>

## <a name="method-formrunhasmethod"></a><span data-ttu-id="3e800-273">メソッド formRunHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-273">Method formRunHasMethod</span></span>

```xpp
public static boolean formRunHasMethod(xFormRun formRun, str methodName)
```

### <a name="parameters---formrunhasmethod"></a><span data-ttu-id="3e800-274">パラメーター - formRunHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-274">Parameters - formRunHasMethod</span></span>

<span data-ttu-id="3e800-275">formRun</span><span class="sxs-lookup"><span data-stu-id="3e800-275">formRun</span></span>  

<!-- -->

<span data-ttu-id="3e800-276">methodName</span><span class="sxs-lookup"><span data-stu-id="3e800-276">methodName</span></span>  

### <a name="return-value---formrunhasmethod"></a><span data-ttu-id="3e800-277">戻り値 - formRunHasMethod</span><span class="sxs-lookup"><span data-stu-id="3e800-277">Return Value - formRunHasMethod</span></span>

## <a name="method-getsetupuserqueryelementname"></a><span data-ttu-id="3e800-278">メソッド getSetupUserQueryElementName</span><span class="sxs-lookup"><span data-stu-id="3e800-278">Method getSetupUserQueryElementName</span></span>

```xpp
public static str getSetupUserQueryElementName(MenuItemType menuItemType, str menuItemName)
```

### <a name="parameters---getsetupuserqueryelementname"></a><span data-ttu-id="3e800-279">パラメーター - getSetupUserQueryElementName</span><span class="sxs-lookup"><span data-stu-id="3e800-279">Parameters - getSetupUserQueryElementName</span></span>

<span data-ttu-id="3e800-280">menuItemType</span><span class="sxs-lookup"><span data-stu-id="3e800-280">menuItemType</span></span>  

<!-- -->

<span data-ttu-id="3e800-281">menuItemName</span><span class="sxs-lookup"><span data-stu-id="3e800-281">menuItemName</span></span>  

### <a name="return-value---getsetupuserqueryelementname"></a><span data-ttu-id="3e800-282">戻り値 - getSetupUserQueryElementName</span><span class="sxs-lookup"><span data-stu-id="3e800-282">Return Value - getSetupUserQueryElementName</span></span>

## <a name="method-new"></a><span data-ttu-id="3e800-283">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3e800-283">Method new</span></span>

<span data-ttu-id="3e800-284">Form クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e800-284">Initializes a new instance of the Form class.</span></span>

```xpp
public void new([str name], [boolean buildMode])
```

### <a name="parameters---new"></a><span data-ttu-id="3e800-285">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="3e800-285">Parameters - new</span></span>

<span data-ttu-id="3e800-286">名前</span><span class="sxs-lookup"><span data-stu-id="3e800-286">name</span></span>  

<!-- -->

<span data-ttu-id="3e800-287">buildMode</span><span class="sxs-lookup"><span data-stu-id="3e800-287">buildMode</span></span>  

## <a name="method-ininitializedesign"></a><span data-ttu-id="3e800-288">メソッド inInitializeDesign</span><span class="sxs-lookup"><span data-stu-id="3e800-288">Method inInitializeDesign</span></span>

```xpp
public void inInitializeDesign([boolean value])
```

### <a name="parameters---ininitializedesign"></a><span data-ttu-id="3e800-289">パラメーター - inInitializeDesign</span><span class="sxs-lookup"><span data-stu-id="3e800-289">Parameters - inInitializeDesign</span></span>

<span data-ttu-id="3e800-290">値</span><span class="sxs-lookup"><span data-stu-id="3e800-290">value</span></span>  

## <a name="method-save"></a><span data-ttu-id="3e800-291">メソッド save</span><span class="sxs-lookup"><span data-stu-id="3e800-291">Method save</span></span>

```xpp
public void save()
```

## <a name="method-load"></a><span data-ttu-id="3e800-292">メソッド load</span><span class="sxs-lookup"><span data-stu-id="3e800-292">Method load</span></span>

```xpp
public void load(str name, [boolean buildMode])
```

### <a name="parameters---load"></a><span data-ttu-id="3e800-293">パラメーター - load</span><span class="sxs-lookup"><span data-stu-id="3e800-293">Parameters - load</span></span>

<span data-ttu-id="3e800-294">名前</span><span class="sxs-lookup"><span data-stu-id="3e800-294">name</span></span>  

<!-- -->

<span data-ttu-id="3e800-295">buildMode</span><span class="sxs-lookup"><span data-stu-id="3e800-295">buildMode</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="3e800-296">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="3e800-296">Method finalize</span></span>

```xpp
public void finalize()
```

