---
title: xClassFactory クラス
description: このトピックでは、xClassFactory クラスについて説明します。
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
ms.openlocfilehash: b4cad1d4937dc48075020448ce02f7a38c6026e9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502766"
---
# <a name="class-xclassfactory"></a><span data-ttu-id="07111-103">クラス xClassFactory</span><span class="sxs-lookup"><span data-stu-id="07111-103">Class xClassFactory</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xClassFactory extends Object
```

## <a name="remarks"></a><span data-ttu-id="07111-104">備考</span><span class="sxs-lookup"><span data-stu-id="07111-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="07111-105">例</span><span class="sxs-lookup"><span data-stu-id="07111-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="07111-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="07111-106">Methods</span></span>

| <span data-ttu-id="07111-107">方法</span><span class="sxs-lookup"><span data-stu-id="07111-107">Method</span></span>                                                                                                                                               | <span data-ttu-id="07111-108">説明</span><span class="sxs-lookup"><span data-stu-id="07111-108">Description</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="07111-109">public xFormRun createAutoReportForm(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-109">public xFormRun createAutoReportForm(xArgs args)</span></span>                                                                                                     |                                                        |
| <span data-ttu-id="07111-110">public xFormRun createLabelForm(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-110">public xFormRun createLabelForm(xArgs args)</span></span>                                                                                                          |                                                        |
| <span data-ttu-id="07111-111">public xFormRun createRecInfoForm(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-111">public xFormRun createRecInfoForm(xArgs args)</span></span>                                                                                                        |                                                        |
| <span data-ttu-id="07111-112">public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, \[ReportRun reportRun\])</span><span class="sxs-lookup"><span data-stu-id="07111-112">public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, \[ReportRun reportRun\])</span></span>                                |                                                        |
| <span data-ttu-id="07111-113">public xFormRun createSetupForm(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-113">public xFormRun createSetupForm(xArgs args)</span></span>                                                                                                          |                                                        |
| <span data-ttu-id="07111-114">public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, \[ReportRun reportRun\])</span><span class="sxs-lookup"><span data-stu-id="07111-114">public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, \[ReportRun reportRun\])</span></span> |                                                        |
| <span data-ttu-id="07111-115">public Object createWebPageEditor()</span><span class="sxs-lookup"><span data-stu-id="07111-115">public Object createWebPageEditor()</span></span>                                                                                                                  |                                                        |
| <span data-ttu-id="07111-116">public xFormRun formRunClass(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-116">public xFormRun formRunClass(xArgs args)</span></span>                                                                                                             |                                                        |
| <span data-ttu-id="07111-117">public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span><span class="sxs-lookup"><span data-stu-id="07111-117">public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span></span>               |                                                        |
| <span data-ttu-id="07111-118">public QueryRun queryRunClass(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-118">public QueryRun queryRunClass(xArgs args)</span></span>                                                                                                            |                                                        |
| <span data-ttu-id="07111-119">public ReportRun reportRunClass(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="07111-119">public ReportRun reportRunClass(xArgs args)</span></span>                                                                                                          |                                                        |
| <span data-ttu-id="07111-120">public Object startAOTWizard(TreeNode parent)</span><span class="sxs-lookup"><span data-stu-id="07111-120">public Object startAOTWizard(TreeNode parent)</span></span>                                                                                                        |                                                        |
| <span data-ttu-id="07111-121">public void projectDeleted(str projectName)</span><span class="sxs-lookup"><span data-stu-id="07111-121">public void projectDeleted(str projectName)</span></span>                                                                                                          |                                                        |
| <span data-ttu-id="07111-122">public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span><span class="sxs-lookup"><span data-stu-id="07111-122">public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span></span>                 |                                                        |
| <span data-ttu-id="07111-123">public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span><span class="sxs-lookup"><span data-stu-id="07111-123">public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])</span></span>   |                                                        |
| <span data-ttu-id="07111-124">public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)</span><span class="sxs-lookup"><span data-stu-id="07111-124">public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)</span></span>                                                          |                                                        |
| <span data-ttu-id="07111-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="07111-125">public void new()</span></span>                                                                                                                                    | <span data-ttu-id="07111-126">xClassFactory クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="07111-126">Initializes a new instance of the xClassFactory class.</span></span> |

## <a name="method-createautoreportform"></a><span data-ttu-id="07111-127">メソッド createAutoReportForm</span><span class="sxs-lookup"><span data-stu-id="07111-127">Method createAutoReportForm</span></span>

```xpp
public xFormRun createAutoReportForm(xArgs args)
```

### <a name="parameters---createautoreportform"></a><span data-ttu-id="07111-128">パラメーター - createAutoReportForm</span><span class="sxs-lookup"><span data-stu-id="07111-128">Parameters - createAutoReportForm</span></span>

<span data-ttu-id="07111-129">args</span><span class="sxs-lookup"><span data-stu-id="07111-129">args</span></span>  

### <a name="return-value---createautoreportform"></a><span data-ttu-id="07111-130">戻り値 - createAutoReportForm</span><span class="sxs-lookup"><span data-stu-id="07111-130">Return Value - createAutoReportForm</span></span>

## <a name="method-createlabelform"></a><span data-ttu-id="07111-131">メソッド createLabelForm</span><span class="sxs-lookup"><span data-stu-id="07111-131">Method createLabelForm</span></span>

```xpp
public xFormRun createLabelForm(xArgs args)
```

### <a name="parameters---createlabelform"></a><span data-ttu-id="07111-132">パラメーター - createLabelForm</span><span class="sxs-lookup"><span data-stu-id="07111-132">Parameters - createLabelForm</span></span>

<span data-ttu-id="07111-133">args</span><span class="sxs-lookup"><span data-stu-id="07111-133">args</span></span>  

### <a name="return-value---createlabelform"></a><span data-ttu-id="07111-134">戻り値 - createLabelForm</span><span class="sxs-lookup"><span data-stu-id="07111-134">Return Value - createLabelForm</span></span>

## <a name="method-createrecinfoform"></a><span data-ttu-id="07111-135">メソッド createRecInfoForm</span><span class="sxs-lookup"><span data-stu-id="07111-135">Method createRecInfoForm</span></span>

```xpp
public xFormRun createRecInfoForm(xArgs args)
```

### <a name="parameters---createrecinfoform"></a><span data-ttu-id="07111-136">パラメーター - createRecInfoForm</span><span class="sxs-lookup"><span data-stu-id="07111-136">Parameters - createRecInfoForm</span></span>

<span data-ttu-id="07111-137">args</span><span class="sxs-lookup"><span data-stu-id="07111-137">args</span></span>  

### <a name="return-value---createrecinfoform"></a><span data-ttu-id="07111-138">戻り値 - createRecInfoForm</span><span class="sxs-lookup"><span data-stu-id="07111-138">Return Value - createRecInfoForm</span></span>

## <a name="method-createreportviewer"></a><span data-ttu-id="07111-139">メソッド createReportViewer</span><span class="sxs-lookup"><span data-stu-id="07111-139">Method createReportViewer</span></span>

```xpp
public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, [ReportRun reportRun])
```

### <a name="parameters---createreportviewer"></a><span data-ttu-id="07111-140">パラメーター - createReportViewer</span><span class="sxs-lookup"><span data-stu-id="07111-140">Parameters - createReportViewer</span></span>

<span data-ttu-id="07111-141">jobsCursor</span><span class="sxs-lookup"><span data-stu-id="07111-141">jobsCursor</span></span>  

<!-- -->

<span data-ttu-id="07111-142">pagesCursor</span><span class="sxs-lookup"><span data-stu-id="07111-142">pagesCursor</span></span>  

<!-- -->

<span data-ttu-id="07111-143">reportRun</span><span class="sxs-lookup"><span data-stu-id="07111-143">reportRun</span></span>  

### <a name="return-value---createreportviewer"></a><span data-ttu-id="07111-144">戻り値 - createReportViewer</span><span class="sxs-lookup"><span data-stu-id="07111-144">Return Value - createReportViewer</span></span>

## <a name="method-createsetupform"></a><span data-ttu-id="07111-145">メソッド createSetupForm</span><span class="sxs-lookup"><span data-stu-id="07111-145">Method createSetupForm</span></span>

```xpp
public xFormRun createSetupForm(xArgs args)
```

### <a name="parameters---createsetupform"></a><span data-ttu-id="07111-146">パラメーター - createSetupForm</span><span class="sxs-lookup"><span data-stu-id="07111-146">Parameters - createSetupForm</span></span>

<span data-ttu-id="07111-147">args</span><span class="sxs-lookup"><span data-stu-id="07111-147">args</span></span>  

### <a name="return-value---createsetupform"></a><span data-ttu-id="07111-148">戻り値 - createSetupForm</span><span class="sxs-lookup"><span data-stu-id="07111-148">Return Value - createSetupForm</span></span>

## <a name="method-createviewer"></a><span data-ttu-id="07111-149">メソッド createViewer</span><span class="sxs-lookup"><span data-stu-id="07111-149">Method createViewer</span></span>

```xpp
public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, [ReportRun reportRun])
```

### <a name="parameters---createviewer"></a><span data-ttu-id="07111-150">パラメーター - createViewer</span><span class="sxs-lookup"><span data-stu-id="07111-150">Parameters - createViewer</span></span>

<span data-ttu-id="07111-151">jobsCursor</span><span class="sxs-lookup"><span data-stu-id="07111-151">jobsCursor</span></span>  

<!-- -->

<span data-ttu-id="07111-152">pagesCursor</span><span class="sxs-lookup"><span data-stu-id="07111-152">pagesCursor</span></span>  

<!-- -->

<span data-ttu-id="07111-153">viewerType</span><span class="sxs-lookup"><span data-stu-id="07111-153">viewerType</span></span>  

<!-- -->

<span data-ttu-id="07111-154">reportRun</span><span class="sxs-lookup"><span data-stu-id="07111-154">reportRun</span></span>  

### <a name="return-value---createviewer"></a><span data-ttu-id="07111-155">戻り値 - createViewer</span><span class="sxs-lookup"><span data-stu-id="07111-155">Return Value - createViewer</span></span>

## <a name="method-createwebpageeditor"></a><span data-ttu-id="07111-156">メソッド createWebPageEditor</span><span class="sxs-lookup"><span data-stu-id="07111-156">Method createWebPageEditor</span></span>

```xpp
public Object createWebPageEditor()
```

### <a name="return-value---createwebpageeditor"></a><span data-ttu-id="07111-157">戻り値 - createWebPageEditor</span><span class="sxs-lookup"><span data-stu-id="07111-157">Return Value - createWebPageEditor</span></span>

## <a name="method-formrunclass"></a><span data-ttu-id="07111-158">メソッド formRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-158">Method formRunClass</span></span>

```xpp
public xFormRun formRunClass(xArgs args)
```

### <a name="parameters---formrunclass"></a><span data-ttu-id="07111-159">パラメーター - formRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-159">Parameters - formRunClass</span></span>

<span data-ttu-id="07111-160">args</span><span class="sxs-lookup"><span data-stu-id="07111-160">args</span></span>  

### <a name="return-value---formrunclass"></a><span data-ttu-id="07111-161">戻り値 - formRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-161">Return Value - formRunClass</span></span>

## <a name="method-lastvalueget"></a><span data-ttu-id="07111-162">メソッド lastValueGet</span><span class="sxs-lookup"><span data-stu-id="07111-162">Method lastValueGet</span></span>

```xpp
public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvalueget"></a><span data-ttu-id="07111-163">パラメーター - lastValueGet</span><span class="sxs-lookup"><span data-stu-id="07111-163">Parameters - lastValueGet</span></span>

<span data-ttu-id="07111-164">会社</span><span class="sxs-lookup"><span data-stu-id="07111-164">company</span></span>  

<!-- -->

<span data-ttu-id="07111-165">ユーザー</span><span class="sxs-lookup"><span data-stu-id="07111-165">user</span></span>  

<!-- -->

<span data-ttu-id="07111-166">utilType</span><span class="sxs-lookup"><span data-stu-id="07111-166">utilType</span></span>  

<!-- -->

<span data-ttu-id="07111-167">名前</span><span class="sxs-lookup"><span data-stu-id="07111-167">name</span></span>  

<!-- -->

<span data-ttu-id="07111-168">design</span><span class="sxs-lookup"><span data-stu-id="07111-168">design</span></span>  

### <a name="return-value---lastvalueget"></a><span data-ttu-id="07111-169">戻り値 - lastValueGet</span><span class="sxs-lookup"><span data-stu-id="07111-169">Return Value - lastValueGet</span></span>

## <a name="method-queryrunclass"></a><span data-ttu-id="07111-170">メソッド queryRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-170">Method queryRunClass</span></span>

```xpp
public QueryRun queryRunClass(xArgs args)
```

### <a name="parameters---queryrunclass"></a><span data-ttu-id="07111-171">パラメーター - queryRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-171">Parameters - queryRunClass</span></span>

<span data-ttu-id="07111-172">args</span><span class="sxs-lookup"><span data-stu-id="07111-172">args</span></span>  

### <a name="return-value---queryrunclass"></a><span data-ttu-id="07111-173">戻り値 - queryRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-173">Return Value - queryRunClass</span></span>

## <a name="method-reportrunclass"></a><span data-ttu-id="07111-174">メソッド reportRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-174">Method reportRunClass</span></span>

```xpp
public ReportRun reportRunClass(xArgs args)
```

### <a name="parameters---reportrunclass"></a><span data-ttu-id="07111-175">パラメーター - reportRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-175">Parameters - reportRunClass</span></span>

<span data-ttu-id="07111-176">args</span><span class="sxs-lookup"><span data-stu-id="07111-176">args</span></span>  

### <a name="return-value---reportrunclass"></a><span data-ttu-id="07111-177">戻り値 - reportRunClass</span><span class="sxs-lookup"><span data-stu-id="07111-177">Return Value - reportRunClass</span></span>

## <a name="method-startaotwizard"></a><span data-ttu-id="07111-178">メソッド startAOTWizard</span><span class="sxs-lookup"><span data-stu-id="07111-178">Method startAOTWizard</span></span>

```xpp
public Object startAOTWizard(TreeNode parent)
```

### <a name="parameters---startaotwizard"></a><span data-ttu-id="07111-179">パラメーター - startAOTWizard</span><span class="sxs-lookup"><span data-stu-id="07111-179">Parameters - startAOTWizard</span></span>

<span data-ttu-id="07111-180">parent</span><span class="sxs-lookup"><span data-stu-id="07111-180">parent</span></span>  

### <a name="return-value---startaotwizard"></a><span data-ttu-id="07111-181">戻り値 - startAOTWizard</span><span class="sxs-lookup"><span data-stu-id="07111-181">Return Value - startAOTWizard</span></span>

## <a name="method-projectdeleted"></a><span data-ttu-id="07111-182">メソッド projectDeleted</span><span class="sxs-lookup"><span data-stu-id="07111-182">Method projectDeleted</span></span>

```xpp
public void projectDeleted(str projectName)
```

### <a name="parameters---projectdeleted"></a><span data-ttu-id="07111-183">パラメーター - projectDeleted</span><span class="sxs-lookup"><span data-stu-id="07111-183">Parameters - projectDeleted</span></span>

<span data-ttu-id="07111-184">projectName</span><span class="sxs-lookup"><span data-stu-id="07111-184">projectName</span></span>  

## <a name="method-lastvaluedelete"></a><span data-ttu-id="07111-185">メソッド lastValueDelete</span><span class="sxs-lookup"><span data-stu-id="07111-185">Method lastValueDelete</span></span>

```xpp
public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvaluedelete"></a><span data-ttu-id="07111-186">パラメーター - lastValueDelete</span><span class="sxs-lookup"><span data-stu-id="07111-186">Parameters - lastValueDelete</span></span>

<span data-ttu-id="07111-187">会社</span><span class="sxs-lookup"><span data-stu-id="07111-187">company</span></span>  

<!-- -->

<span data-ttu-id="07111-188">ユーザー</span><span class="sxs-lookup"><span data-stu-id="07111-188">user</span></span>  

<!-- -->

<span data-ttu-id="07111-189">utilType</span><span class="sxs-lookup"><span data-stu-id="07111-189">utilType</span></span>  

<!-- -->

<span data-ttu-id="07111-190">名前</span><span class="sxs-lookup"><span data-stu-id="07111-190">name</span></span>  

<!-- -->

<span data-ttu-id="07111-191">design</span><span class="sxs-lookup"><span data-stu-id="07111-191">design</span></span>  

## <a name="method-lastvalueput"></a><span data-ttu-id="07111-192">メソッド lastValuePut</span><span class="sxs-lookup"><span data-stu-id="07111-192">Method lastValuePut</span></span>

```xpp
public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvalueput"></a><span data-ttu-id="07111-193">パラメーター - lastValuePut</span><span class="sxs-lookup"><span data-stu-id="07111-193">Parameters - lastValuePut</span></span>

<span data-ttu-id="07111-194">値</span><span class="sxs-lookup"><span data-stu-id="07111-194">value</span></span>  

<!-- -->

<span data-ttu-id="07111-195">会社</span><span class="sxs-lookup"><span data-stu-id="07111-195">company</span></span>  

<!-- -->

<span data-ttu-id="07111-196">ユーザー</span><span class="sxs-lookup"><span data-stu-id="07111-196">user</span></span>  

<!-- -->

<span data-ttu-id="07111-197">utilType</span><span class="sxs-lookup"><span data-stu-id="07111-197">utilType</span></span>  

<!-- -->

<span data-ttu-id="07111-198">名前</span><span class="sxs-lookup"><span data-stu-id="07111-198">name</span></span>  

<!-- -->

<span data-ttu-id="07111-199">design</span><span class="sxs-lookup"><span data-stu-id="07111-199">design</span></span>  

## <a name="method-drilldown"></a><span data-ttu-id="07111-200">メソッド drillDown</span><span class="sxs-lookup"><span data-stu-id="07111-200">Method drillDown</span></span>

```xpp
public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)
```

### <a name="parameters---drilldown"></a><span data-ttu-id="07111-201">パラメーター - drillDown</span><span class="sxs-lookup"><span data-stu-id="07111-201">Parameters - drillDown</span></span>

<span data-ttu-id="07111-202">outputField</span><span class="sxs-lookup"><span data-stu-id="07111-202">outputField</span></span>  

<!-- -->

<span data-ttu-id="07111-203">menuItemType</span><span class="sxs-lookup"><span data-stu-id="07111-203">menuItemType</span></span>  

<!-- -->

<span data-ttu-id="07111-204">menuItemName</span><span class="sxs-lookup"><span data-stu-id="07111-204">menuItemName</span></span>  

## <a name="method-new"></a><span data-ttu-id="07111-205">メソッド new</span><span class="sxs-lookup"><span data-stu-id="07111-205">Method new</span></span>

<span data-ttu-id="07111-206">xClassFactory クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="07111-206">Initializes a new instance of the xClassFactory class.</span></span>

```xpp
public void new()
```

