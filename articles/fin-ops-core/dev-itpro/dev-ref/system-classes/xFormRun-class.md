---
title: xFormRun クラス
description: このトピックでは、xFormRun クラスについて説明します。
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
ms.openlocfilehash: 7ce70d3e388e2a1d187b10fe8e22917bb89b9dbd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502762"
---
# <a name="class-xformrun"></a><span data-ttu-id="065f2-103">クラス xFormRun</span><span class="sxs-lookup"><span data-stu-id="065f2-103">Class xFormRun</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xFormRun extends ObjectRun
```

## <a name="remarks"></a><span data-ttu-id="065f2-104">備考</span><span class="sxs-lookup"><span data-stu-id="065f2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="065f2-105">例</span><span class="sxs-lookup"><span data-stu-id="065f2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="065f2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="065f2-106">Methods</span></span>

| <span data-ttu-id="065f2-107">方法</span><span class="sxs-lookup"><span data-stu-id="065f2-107">Method</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="065f2-108">説明</span><span class="sxs-lookup"><span data-stu-id="065f2-108">Description</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="065f2-109">public boolean allowPrimaryKeyPreview(\[boolean display\])</span><span class="sxs-lookup"><span data-stu-id="065f2-109">public boolean allowPrimaryKeyPreview(\[boolean display\])</span></span>                                                                                                                                                                                                                                                                                                     |             |
| <span data-ttu-id="065f2-110">public boolean canClose()</span><span class="sxs-lookup"><span data-stu-id="065f2-110">public boolean canClose()</span></span>                                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-111">public boolean canSubmitToWorkflow()</span><span class="sxs-lookup"><span data-stu-id="065f2-111">public boolean canSubmitToWorkflow()</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-112">public boolean checkViewOption(int viewOption)</span><span class="sxs-lookup"><span data-stu-id="065f2-112">public boolean checkViewOption(int viewOption)</span></span>                                                                                                                                                                                                                                                                                                                 |             |
| <span data-ttu-id="065f2-113">public boolean closed()</span><span class="sxs-lookup"><span data-stu-id="065f2-113">public boolean closed()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-114">public boolean closedCancel()</span><span class="sxs-lookup"><span data-stu-id="065f2-114">public boolean closedCancel()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-115">public boolean closedOk()</span><span class="sxs-lookup"><span data-stu-id="065f2-115">public boolean closedOk()</span></span>                                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-116">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="065f2-116">public boolean contains(FormControl control)</span></span>                                                                                                                                                                                                                                                                                                                   |             |
| <span data-ttu-id="065f2-117">public FormControl control(int controlId)</span><span class="sxs-lookup"><span data-stu-id="065f2-117">public FormControl control(int controlId)</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-118">public FormControl controlCallingMethod()</span><span class="sxs-lookup"><span data-stu-id="065f2-118">public FormControl controlCallingMethod()</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-119">public int controlId(str controlName)</span><span class="sxs-lookup"><span data-stu-id="065f2-119">public int controlId(str controlName)</span></span>                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-120">public boolean controlMethodOverload(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="065f2-120">public boolean controlMethodOverload(\[boolean value\])</span></span>                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-121">public Object controlMethodOverloadObject(\[Object value\])</span><span class="sxs-lookup"><span data-stu-id="065f2-121">public Object controlMethodOverloadObject(\[Object value\])</span></span>                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-122">public boolean copy()</span><span class="sxs-lookup"><span data-stu-id="065f2-122">public boolean copy()</span></span>                                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-123">public boolean cut()</span><span class="sxs-lookup"><span data-stu-id="065f2-123">public boolean cut()</span></span>                                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-124">public FormObjectSet dataSource(\[AnyType objectSet\])</span><span class="sxs-lookup"><span data-stu-id="065f2-124">public FormObjectSet dataSource(\[AnyType objectSet\])</span></span>                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-125">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="065f2-125">public int dataSourceCount()</span></span>                                                                                                                                                                                                                                                                                                                                   |             |
| <span data-ttu-id="065f2-126">public FormObjectSet defaultDataSource(\[FormObjectSet value\])</span><span class="sxs-lookup"><span data-stu-id="065f2-126">public FormObjectSet defaultDataSource(\[FormObjectSet value\])</span></span>                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-127">public boolean defaultInitialQueryValuesOnCreate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="065f2-127">public boolean defaultInitialQueryValuesOnCreate(\[boolean value\])</span></span>                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-128">public FormDesign design(\[int reserved\])</span><span class="sxs-lookup"><span data-stu-id="065f2-128">public FormDesign design(\[int reserved\])</span></span>                                                                                                                                                                                                                                                                                                                     |             |
| <span data-ttu-id="065f2-129">public Common docCursor()</span><span class="sxs-lookup"><span data-stu-id="065f2-129">public Common docCursor()</span></span>                                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-130">public boolean enableCountryRegion(\[boolean flag\])</span><span class="sxs-lookup"><span data-stu-id="065f2-130">public boolean enableCountryRegion(\[boolean flag\])</span></span>                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-131">public Form form()</span><span class="sxs-lookup"><span data-stu-id="065f2-131">public Form form()</span></span>                                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-132">public Common getActiveWorkflowConfiguration()</span><span class="sxs-lookup"><span data-stu-id="065f2-132">public Common getActiveWorkflowConfiguration()</span></span>                                                                                                                                                                                                                                                                                                                 |             |
| <span data-ttu-id="065f2-133">public Common getActiveWorkflowTrackingStatus()</span><span class="sxs-lookup"><span data-stu-id="065f2-133">public Common getActiveWorkflowTrackingStatus()</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-134">public Common getActiveWorkflowWorkItem()</span><span class="sxs-lookup"><span data-stu-id="065f2-134">public Common getActiveWorkflowWorkItem()</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-135">public container getAutoCompleteString(int startIdx, \[FormControl control\], \[str searchString\])</span><span class="sxs-lookup"><span data-stu-id="065f2-135">public container getAutoCompleteString(int startIdx, \[FormControl control\], \[str searchString\])</span></span>                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-136">public str getFormHelpTopic()</span><span class="sxs-lookup"><span data-stu-id="065f2-136">public str getFormHelpTopic()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-137">public FormControl getNextField(FormControl control, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-137">public FormControl getNextField(FormControl control, \[int flags\])</span></span>                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-138">public FormControl getPrevField(FormControl control, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-138">public FormControl getPrevField(FormControl control, \[int flags\])</span></span>                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-139">public boolean hasExecutedInit()</span><span class="sxs-lookup"><span data-stu-id="065f2-139">public boolean hasExecutedInit()</span></span>                                                                                                                                                                                                                                                                                                                               |             |
| <span data-ttu-id="065f2-140">public int hWnd()</span><span class="sxs-lookup"><span data-stu-id="065f2-140">public int hWnd()</span></span>                                                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-141">public int installMessageProc(int message, int handle, str method)</span><span class="sxs-lookup"><span data-stu-id="065f2-141">public int installMessageProc(int message, int handle, str method)</span></span>                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-142">public boolean inViewMode()</span><span class="sxs-lookup"><span data-stu-id="065f2-142">public boolean inViewMode()</span></span>                                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-143">public boolean isDataInteractionSupported()</span><span class="sxs-lookup"><span data-stu-id="065f2-143">public boolean isDataInteractionSupported()</span></span>                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-144">public boolean isPreloadedInstance()</span><span class="sxs-lookup"><span data-stu-id="065f2-144">public boolean isPreloadedInstance()</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-145">public boolean isFormPart()</span><span class="sxs-lookup"><span data-stu-id="065f2-145">public boolean isFormPart()</span></span>                                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-146">public boolean isFactBox()</span><span class="sxs-lookup"><span data-stu-id="065f2-146">public boolean isFactBox()</span></span>                                                                                                                                                                                                                                                                                                                                     |             |
| <span data-ttu-id="065f2-147">public boolean isLookupForm()</span><span class="sxs-lookup"><span data-stu-id="065f2-147">public boolean isLookupForm()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-148">public boolean isPartRemote()</span><span class="sxs-lookup"><span data-stu-id="065f2-148">public boolean isPartRemote()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-149">public boolean isPartLocal()</span><span class="sxs-lookup"><span data-stu-id="065f2-149">public boolean isPartLocal()</span></span>                                                                                                                                                                                                                                                                                                                                   |             |
| <span data-ttu-id="065f2-150">public boolean isWorkflowEnabled()</span><span class="sxs-lookup"><span data-stu-id="065f2-150">public boolean isWorkflowEnabled()</span></span>                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-151">public Common loadWorkflowConfiguration()</span><span class="sxs-lookup"><span data-stu-id="065f2-151">public Common loadWorkflowConfiguration()</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-152">public boolean lockWindowUpdate(boolean lock)</span><span class="sxs-lookup"><span data-stu-id="065f2-152">public boolean lockWindowUpdate(boolean lock)</span></span>                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-153">public str name()</span><span class="sxs-lookup"><span data-stu-id="065f2-153">public str name()</span></span>                                                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-154">public FormObjectSet objectSet(\[AnyType objectSet\])</span><span class="sxs-lookup"><span data-stu-id="065f2-154">public FormObjectSet objectSet(\[AnyType objectSet\])</span></span>                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-155">public boolean resetAsyncOperationsPendingState()</span><span class="sxs-lookup"><span data-stu-id="065f2-155">public boolean resetAsyncOperationsPendingState()</span></span>                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-156">public PageInteraction pageInteraction()</span><span class="sxs-lookup"><span data-stu-id="065f2-156">public PageInteraction pageInteraction()</span></span>                                                                                                                                                                                                                                                                                                                       |             |
| <span data-ttu-id="065f2-157">public boolean paste()</span><span class="sxs-lookup"><span data-stu-id="065f2-157">public boolean paste()</span></span>                                                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-158">public str recordingScopeId()</span><span class="sxs-lookup"><span data-stu-id="065f2-158">public str recordingScopeId()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-159">public boolean removeMessageProc(int message, int handle)</span><span class="sxs-lookup"><span data-stu-id="065f2-159">public boolean removeMessageProc(int message, int handle)</span></span>                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-160">public List rootFormDataSources()</span><span class="sxs-lookup"><span data-stu-id="065f2-160">public List rootFormDataSources()</span></span>                                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-161">public boolean selectControl(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="065f2-161">public boolean selectControl(FormControl control)</span></span>                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-162">public FormControl selectedControl()</span><span class="sxs-lookup"><span data-stu-id="065f2-162">public FormControl selectedControl()</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-163">public Common selectRecordModeSelectedRecord(\[Common selectedRecord\])</span><span class="sxs-lookup"><span data-stu-id="065f2-163">public Common selectRecordModeSelectedRecord(\[Common selectedRecord\])</span></span>                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-164">public FormControl selectTarget(\[FormControl target\])</span><span class="sxs-lookup"><span data-stu-id="065f2-164">public FormControl selectTarget(\[FormControl target\])</span></span>                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-165">public Array tabOrder(\[Array newValue\])</span><span class="sxs-lookup"><span data-stu-id="065f2-165">public Array tabOrder(\[Array newValue\])</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-166">public int task(int taskId)</span><span class="sxs-lookup"><span data-stu-id="065f2-166">public int task(int taskId)</span></span>                                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-167">public str toString()</span><span class="sxs-lookup"><span data-stu-id="065f2-167">public str toString()</span></span>                                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-168">public FormObjectSet workflowDataSource()</span><span class="sxs-lookup"><span data-stu-id="065f2-168">public FormObjectSet workflowDataSource()</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-169">public str workflowType()</span><span class="sxs-lookup"><span data-stu-id="065f2-169">public str workflowType()</span></span>                                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-170">public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[str callbackFormMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\])</span><span class="sxs-lookup"><span data-stu-id="065f2-170">public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[str callbackFormMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\])</span></span> |             |
| <span data-ttu-id="065f2-171">public System.Threading.Tasks.Task setTimeoutEx(\[str formMethodName\], \[container parms\], \[int delay\], \[System.Threading.CancellationToken cancellationToken\])</span><span class="sxs-lookup"><span data-stu-id="065f2-171">public System.Threading.Tasks.Task setTimeoutEx(\[str formMethodName\], \[container parms\], \[int delay\], \[System.Threading.CancellationToken cancellationToken\])</span></span>                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-172">public void setParentHandle(int hwnd)</span><span class="sxs-lookup"><span data-stu-id="065f2-172">public void setParentHandle(int hwnd)</span></span>                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-173">public void setFormHelpTopic(str formHelpTopic)</span><span class="sxs-lookup"><span data-stu-id="065f2-173">public void setFormHelpTopic(str formHelpTopic)</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-174">public void setFactBoxEditable()</span><span class="sxs-lookup"><span data-stu-id="065f2-174">public void setFactBoxEditable()</span></span>                                                                                                                                                                                                                                                                                                                               |             |
| <span data-ttu-id="065f2-175">public void setAutoCompleteString(str string, AnyType control)</span><span class="sxs-lookup"><span data-stu-id="065f2-175">public void setAutoCompleteString(str string, AnyType control)</span></span>                                                                                                                                                                                                                                                                                                 |             |
| <span data-ttu-id="065f2-176">public void RaiseOnClosing(\[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-176">public void RaiseOnClosing(\[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-177">public void inlineLoadingKey(FormControl parentControl)</span><span class="sxs-lookup"><span data-stu-id="065f2-177">public void inlineLoadingKey(FormControl parentControl)</span></span>                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-178">public void closeSelect(str selectString)</span><span class="sxs-lookup"><span data-stu-id="065f2-178">public void closeSelect(str selectString)</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-179">public void RaiseOnActivated(\[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-179">public void RaiseOnActivated(\[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-180">public void prevField(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-180">public void prevField(\[int flags\])</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-181">public void send()</span><span class="sxs-lookup"><span data-stu-id="065f2-181">public void send()</span></span>                                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-182">public void RaiseOnInitializing(\[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-182">public void RaiseOnInitializing(\[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-183">public void updateWorkflowControls()</span><span class="sxs-lookup"><span data-stu-id="065f2-183">public void updateWorkflowControls()</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-184">public void closeCancel()</span><span class="sxs-lookup"><span data-stu-id="065f2-184">public void closeCancel()</span></span>                                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-185">public void lastField(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-185">public void lastField(\[int flags\])</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-186">public void wait(\[boolean modal\])</span><span class="sxs-lookup"><span data-stu-id="065f2-186">public void wait(\[boolean modal\])</span></span>                                                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-187">public void unLock(\[boolean arrangeNow\])</span><span class="sxs-lookup"><span data-stu-id="065f2-187">public void unLock(\[boolean arrangeNow\])</span></span>                                                                                                                                                                                                                                                                                                                     |             |
| <span data-ttu-id="065f2-188">private void OnInitialized(\[xFormRun sender\], \[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-188">private void OnInitialized(\[xFormRun sender\], \[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-189">public void detach()</span><span class="sxs-lookup"><span data-stu-id="065f2-189">public void detach()</span></span>                                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-190">public void resetStatusBarBackgroundColor()</span><span class="sxs-lookup"><span data-stu-id="065f2-190">public void resetStatusBarBackgroundColor()</span></span>                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-191">private void OnClosing(\[xFormRun sender\], \[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-191">private void OnClosing(\[xFormRun sender\], \[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                               |             |
| <span data-ttu-id="065f2-192">public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, \[str dataSourceName\], \[boolean isTableDisplayMethod\])</span><span class="sxs-lookup"><span data-stu-id="065f2-192">public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, \[str dataSourceName\], \[boolean isTableDisplayMethod\])</span></span>                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-193">public void print()</span><span class="sxs-lookup"><span data-stu-id="065f2-193">public void print()</span></span>                                                                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-194">public void activate(boolean active)</span><span class="sxs-lookup"><span data-stu-id="065f2-194">public void activate(boolean active)</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-195">public void resize(int width, int height)</span><span class="sxs-lookup"><span data-stu-id="065f2-195">public void resize(int width, int height)</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-196">public void reload(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="065f2-196">public void reload(\[xArgs args\])</span></span>                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-197">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="065f2-197">public void finalize()</span></span>                                                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-198">public void RaiseOnInitialized(\[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-198">public void RaiseOnInitialized(\[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-199">public void resetSize()</span><span class="sxs-lookup"><span data-stu-id="065f2-199">public void resetSize()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-200">public void clientId(str clientId)</span><span class="sxs-lookup"><span data-stu-id="065f2-200">public void clientId(str clientId)</span></span>                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-201">public void createRecord(str formDataSourceName, \[boolean append\])</span><span class="sxs-lookup"><span data-stu-id="065f2-201">public void createRecord(str formDataSourceName, \[boolean append\])</span></span>                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-202">public void firstField(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-202">public void firstField(\[int flags\])</span></span>                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-203">public void savePersonalization(str controlName, str propertyKey, str propertyValue)</span><span class="sxs-lookup"><span data-stu-id="065f2-203">public void savePersonalization(str controlName, str propertyKey, str propertyValue)</span></span>                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-204">public void expandFactBoxPaneAtStart()</span><span class="sxs-lookup"><span data-stu-id="065f2-204">public void expandFactBoxPaneAtStart()</span></span>                                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-205">public void redraw()</span><span class="sxs-lookup"><span data-stu-id="065f2-205">public void redraw()</span></span>                                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-206">public void arrange()</span><span class="sxs-lookup"><span data-stu-id="065f2-206">public void arrange()</span></span>                                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-207">public void blockPersonalization(boolean blockPersonalization)</span><span class="sxs-lookup"><span data-stu-id="065f2-207">public void blockPersonalization(boolean blockPersonalization)</span></span>                                                                                                                                                                                                                                                                                                 |             |
| <span data-ttu-id="065f2-208">public void nextField(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="065f2-208">public void nextField(\[int flags\])</span></span>                                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-209">public void nextGroup()</span><span class="sxs-lookup"><span data-stu-id="065f2-209">public void nextGroup()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-210">public void prevGroup()</span><span class="sxs-lookup"><span data-stu-id="065f2-210">public void prevGroup()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-211">public void setFormPartStyle(boolean isFactBox)</span><span class="sxs-lookup"><span data-stu-id="065f2-211">public void setFormPartStyle(boolean isFactBox)</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-212">public void run()</span><span class="sxs-lookup"><span data-stu-id="065f2-212">public void run()</span></span>                                                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-213">public void setActive()</span><span class="sxs-lookup"><span data-stu-id="065f2-213">public void setActive()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-214">public void closeSelectRecord(Common selectedRecord)</span><span class="sxs-lookup"><span data-stu-id="065f2-214">public void closeSelectRecord(Common selectedRecord)</span></span>                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-215">public void registerFormSpecializedCustomControl(str customControlName)</span><span class="sxs-lookup"><span data-stu-id="065f2-215">public void registerFormSpecializedCustomControl(str customControlName)</span></span>                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-216">public void setApply(Object object, \[Object parm\])</span><span class="sxs-lookup"><span data-stu-id="065f2-216">public void setApply(Object object, \[Object parm\])</span></span>                                                                                                                                                                                                                                                                                                           |             |
| <span data-ttu-id="065f2-217">public void new(xArgs args)</span><span class="sxs-lookup"><span data-stu-id="065f2-217">public void new(xArgs args)</span></span>                                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-218">public void RegisterXppILImplementation(str className)</span><span class="sxs-lookup"><span data-stu-id="065f2-218">public void RegisterXppILImplementation(str className)</span></span>                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-219">public void sysColorChanged()</span><span class="sxs-lookup"><span data-stu-id="065f2-219">public void sysColorChanged()</span></span>                                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-220">public void selectRecordMode(\[FormControl control\])</span><span class="sxs-lookup"><span data-stu-id="065f2-220">public void selectRecordMode(\[FormControl control\])</span></span>                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-221">private void OnPostRun(\[xFormRun sender\], \[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-221">private void OnPostRun(\[xFormRun sender\], \[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                               |             |
| <span data-ttu-id="065f2-222">public void skipSaveUserSetting(boolean skip)</span><span class="sxs-lookup"><span data-stu-id="065f2-222">public void skipSaveUserSetting(boolean skip)</span></span>                                                                                                                                                                                                                                                                                                                  |             |
| <span data-ttu-id="065f2-223">public void selectMode(\[FormControl control\])</span><span class="sxs-lookup"><span data-stu-id="065f2-223">public void selectMode(\[FormControl control\])</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-224">public void printPreview()</span><span class="sxs-lookup"><span data-stu-id="065f2-224">public void printPreview()</span></span>                                                                                                                                                                                                                                                                                                                                     |             |
| <span data-ttu-id="065f2-225">private void OnActivated(\[xFormRun sender\], \[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-225">private void OnActivated(\[xFormRun sender\], \[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-226">public void collapseFactBoxPaneAtStart()</span><span class="sxs-lookup"><span data-stu-id="065f2-226">public void collapseFactBoxPaneAtStart()</span></span>                                                                                                                                                                                                                                                                                                                       |             |
| <span data-ttu-id="065f2-227">public void lock()</span><span class="sxs-lookup"><span data-stu-id="065f2-227">public void lock()</span></span>                                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-228">public void init()</span><span class="sxs-lookup"><span data-stu-id="065f2-228">public void init()</span></span>                                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-229">public void formOnTop()</span><span class="sxs-lookup"><span data-stu-id="065f2-229">public void formOnTop()</span></span>                                                                                                                                                                                                                                                                                                                                        |             |
| <span data-ttu-id="065f2-230">public void close()</span><span class="sxs-lookup"><span data-stu-id="065f2-230">public void close()</span></span>                                                                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-231">public void delAutoCompleteString(\[AnyType control\])</span><span class="sxs-lookup"><span data-stu-id="065f2-231">public void delAutoCompleteString(\[AnyType control\])</span></span>                                                                                                                                                                                                                                                                                                         |             |
| <span data-ttu-id="065f2-232">public void closeOk()</span><span class="sxs-lookup"><span data-stu-id="065f2-232">public void closeOk()</span></span>                                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-233">public void modeledQueryName(str queryName)</span><span class="sxs-lookup"><span data-stu-id="065f2-233">public void modeledQueryName(str queryName)</span></span>                                                                                                                                                                                                                                                                                                                    |             |
| <span data-ttu-id="065f2-234">public void initWorkflowControls()</span><span class="sxs-lookup"><span data-stu-id="065f2-234">public void initWorkflowControls()</span></span>                                                                                                                                                                                                                                                                                                                             |             |
| <span data-ttu-id="065f2-235">public void setOrder(FormControl control, FormControl control1, \[boolean before\])</span><span class="sxs-lookup"><span data-stu-id="065f2-235">public void setOrder(FormControl control, FormControl control1, \[boolean before\])</span></span>                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-236">public void allowCrossFormLinks(boolean allowCrossFormLinks)</span><span class="sxs-lookup"><span data-stu-id="065f2-236">public void allowCrossFormLinks(boolean allowCrossFormLinks)</span></span>                                                                                                                                                                                                                                                                                                   |             |
| <span data-ttu-id="065f2-237">public void RaiseOnPostRun(\[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-237">public void RaiseOnPostRun(\[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                                                |             |
| <span data-ttu-id="065f2-238">public void setStatusBarBackgroundColor(int a, int r, int g, int b)</span><span class="sxs-lookup"><span data-stu-id="065f2-238">public void setStatusBarBackgroundColor(int a, int r, int g, int b)</span></span>                                                                                                                                                                                                                                                                                            |             |
| <span data-ttu-id="065f2-239">public void loadPersonalization()</span><span class="sxs-lookup"><span data-stu-id="065f2-239">public void loadPersonalization()</span></span>                                                                                                                                                                                                                                                                                                                              |             |
| <span data-ttu-id="065f2-240">public void doApply()</span><span class="sxs-lookup"><span data-stu-id="065f2-240">public void doApply()</span></span>                                                                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-241">private void OnInitializing(\[xFormRun sender\], \[FormEventArgs e\])</span><span class="sxs-lookup"><span data-stu-id="065f2-241">private void OnInitializing(\[xFormRun sender\], \[FormEventArgs e\])</span></span>                                                                                                                                                                                                                                                                                          |             |
| <span data-ttu-id="065f2-242">public void flushCountryRegionCodeCache()</span><span class="sxs-lookup"><span data-stu-id="065f2-242">public void flushCountryRegionCodeCache()</span></span>                                                                                                                                                                                                                                                                                                                      |             |
| <span data-ttu-id="065f2-243">public void localRefresh()</span><span class="sxs-lookup"><span data-stu-id="065f2-243">public void localRefresh()</span></span>                                                                                                                                                                                                                                                                                                                                     |             |

## <a name="method-allowprimarykeypreview"></a><span data-ttu-id="065f2-244">メソッド allowPrimaryKeyPreview</span><span class="sxs-lookup"><span data-stu-id="065f2-244">Method allowPrimaryKeyPreview</span></span>

```xpp
public boolean allowPrimaryKeyPreview([boolean display])
```

### <a name="parameters---allowprimarykeypreview"></a><span data-ttu-id="065f2-245">パラメーター - allowPrimaryKeyPreview</span><span class="sxs-lookup"><span data-stu-id="065f2-245">Parameters - allowPrimaryKeyPreview</span></span>

<span data-ttu-id="065f2-246">表示</span><span class="sxs-lookup"><span data-stu-id="065f2-246">display</span></span>  

### <a name="return-value---allowprimarykeypreview"></a><span data-ttu-id="065f2-247">戻り値 - allowPrimaryKeyPreview</span><span class="sxs-lookup"><span data-stu-id="065f2-247">Return Value - allowPrimaryKeyPreview</span></span>

## <a name="method-canclose"></a><span data-ttu-id="065f2-248">メソッド canClose</span><span class="sxs-lookup"><span data-stu-id="065f2-248">Method canClose</span></span>

```xpp
public boolean canClose()
```

### <a name="return-value---canclose"></a><span data-ttu-id="065f2-249">戻り値 - canClose</span><span class="sxs-lookup"><span data-stu-id="065f2-249">Return Value - canClose</span></span>

## <a name="method-cansubmittoworkflow"></a><span data-ttu-id="065f2-250">メソッド canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="065f2-250">Method canSubmitToWorkflow</span></span>

```xpp
public boolean canSubmitToWorkflow()
```

### <a name="return-value---cansubmittoworkflow"></a><span data-ttu-id="065f2-251">戻り値 - canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="065f2-251">Return Value - canSubmitToWorkflow</span></span>

## <a name="method-checkviewoption"></a><span data-ttu-id="065f2-252">メソッド checkViewOption</span><span class="sxs-lookup"><span data-stu-id="065f2-252">Method checkViewOption</span></span>

```xpp
public boolean checkViewOption(int viewOption)
```

### <a name="parameters---checkviewoption"></a><span data-ttu-id="065f2-253">パラメーター - checkViewOption</span><span class="sxs-lookup"><span data-stu-id="065f2-253">Parameters - checkViewOption</span></span>

<span data-ttu-id="065f2-254">viewOption</span><span class="sxs-lookup"><span data-stu-id="065f2-254">viewOption</span></span>  

### <a name="return-value---checkviewoption"></a><span data-ttu-id="065f2-255">戻り値 - checkViewOption</span><span class="sxs-lookup"><span data-stu-id="065f2-255">Return Value - checkViewOption</span></span>

## <a name="method-closed"></a><span data-ttu-id="065f2-256">メソッド closed</span><span class="sxs-lookup"><span data-stu-id="065f2-256">Method closed</span></span>

```xpp
public boolean closed()
```

### <a name="return-value---closed"></a><span data-ttu-id="065f2-257">戻り値 - closed</span><span class="sxs-lookup"><span data-stu-id="065f2-257">Return Value - closed</span></span>

## <a name="method-closedcancel"></a><span data-ttu-id="065f2-258">メソッド closedCancel</span><span class="sxs-lookup"><span data-stu-id="065f2-258">Method closedCancel</span></span>

```xpp
public boolean closedCancel()
```

### <a name="return-value---closedcancel"></a><span data-ttu-id="065f2-259">戻り値 - closedCancel</span><span class="sxs-lookup"><span data-stu-id="065f2-259">Return Value - closedCancel</span></span>

## <a name="method-closedok"></a><span data-ttu-id="065f2-260">メソッド closedOk</span><span class="sxs-lookup"><span data-stu-id="065f2-260">Method closedOk</span></span>

```xpp
public boolean closedOk()
```

### <a name="return-value---closedok"></a><span data-ttu-id="065f2-261">戻り値 - closedOk</span><span class="sxs-lookup"><span data-stu-id="065f2-261">Return Value - closedOk</span></span>

## <a name="method-contains"></a><span data-ttu-id="065f2-262">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="065f2-262">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="065f2-263">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="065f2-263">Parameters - contains</span></span>

<span data-ttu-id="065f2-264">control</span><span class="sxs-lookup"><span data-stu-id="065f2-264">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="065f2-265">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="065f2-265">Return Value - contains</span></span>

## <a name="method-control"></a><span data-ttu-id="065f2-266">メソッド control</span><span class="sxs-lookup"><span data-stu-id="065f2-266">Method control</span></span>

```xpp
public FormControl control(int controlId)
```

### <a name="parameters---control"></a><span data-ttu-id="065f2-267">パラメーター - control</span><span class="sxs-lookup"><span data-stu-id="065f2-267">Parameters - control</span></span>

<span data-ttu-id="065f2-268">controlId</span><span class="sxs-lookup"><span data-stu-id="065f2-268">controlId</span></span>  

### <a name="return-value---control"></a><span data-ttu-id="065f2-269">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="065f2-269">Return Value - control</span></span>

## <a name="method-controlcallingmethod"></a><span data-ttu-id="065f2-270">メソッド controlCallingMethod</span><span class="sxs-lookup"><span data-stu-id="065f2-270">Method controlCallingMethod</span></span>

```xpp
public FormControl controlCallingMethod()
```

### <a name="return-value---controlcallingmethod"></a><span data-ttu-id="065f2-271">戻り値 - controlCallingMethod</span><span class="sxs-lookup"><span data-stu-id="065f2-271">Return Value - controlCallingMethod</span></span>

## <a name="method-controlid"></a><span data-ttu-id="065f2-272">メソッド controlId</span><span class="sxs-lookup"><span data-stu-id="065f2-272">Method controlId</span></span>

```xpp
public int controlId(str controlName)
```

### <a name="parameters---controlid"></a><span data-ttu-id="065f2-273">パラメーター - controlId</span><span class="sxs-lookup"><span data-stu-id="065f2-273">Parameters - controlId</span></span>

<span data-ttu-id="065f2-274">controlName</span><span class="sxs-lookup"><span data-stu-id="065f2-274">controlName</span></span>  

### <a name="return-value---controlid"></a><span data-ttu-id="065f2-275">戻り値 - controlId</span><span class="sxs-lookup"><span data-stu-id="065f2-275">Return Value - controlId</span></span>

## <a name="method-controlmethodoverload"></a><span data-ttu-id="065f2-276">メソッド controlMethodOverload</span><span class="sxs-lookup"><span data-stu-id="065f2-276">Method controlMethodOverload</span></span>

```xpp
public boolean controlMethodOverload([boolean value])
```

### <a name="parameters---controlmethodoverload"></a><span data-ttu-id="065f2-277">パラメーター - controlMethodOverload</span><span class="sxs-lookup"><span data-stu-id="065f2-277">Parameters - controlMethodOverload</span></span>

<span data-ttu-id="065f2-278">値</span><span class="sxs-lookup"><span data-stu-id="065f2-278">value</span></span>  

### <a name="return-value---controlmethodoverload"></a><span data-ttu-id="065f2-279">戻り値 - controlMethodOverload</span><span class="sxs-lookup"><span data-stu-id="065f2-279">Return Value - controlMethodOverload</span></span>

## <a name="method-controlmethodoverloadobject"></a><span data-ttu-id="065f2-280">メソッド controlMethodOverloadObject</span><span class="sxs-lookup"><span data-stu-id="065f2-280">Method controlMethodOverloadObject</span></span>

```xpp
public Object controlMethodOverloadObject([Object value])
```

### <a name="parameters---controlmethodoverloadobject"></a><span data-ttu-id="065f2-281">パラメーター - controlMethodOverloadObject</span><span class="sxs-lookup"><span data-stu-id="065f2-281">Parameters - controlMethodOverloadObject</span></span>

<span data-ttu-id="065f2-282">値</span><span class="sxs-lookup"><span data-stu-id="065f2-282">value</span></span>  

### <a name="return-value---controlmethodoverloadobject"></a><span data-ttu-id="065f2-283">戻り値 - controlMethodOverloadObject</span><span class="sxs-lookup"><span data-stu-id="065f2-283">Return Value - controlMethodOverloadObject</span></span>

## <a name="method-copy"></a><span data-ttu-id="065f2-284">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="065f2-284">Method copy</span></span>

```xpp
public boolean copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="065f2-285">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="065f2-285">Return Value - copy</span></span>

## <a name="method-cut"></a><span data-ttu-id="065f2-286">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="065f2-286">Method cut</span></span>

```xpp
public boolean cut()
```

### <a name="return-value---cut"></a><span data-ttu-id="065f2-287">戻り値 - cut</span><span class="sxs-lookup"><span data-stu-id="065f2-287">Return Value - cut</span></span>

## <a name="method-datasource"></a><span data-ttu-id="065f2-288">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-288">Method dataSource</span></span>

```xpp
public FormObjectSet dataSource([AnyType objectSet])
```

### <a name="parameters---datasource"></a><span data-ttu-id="065f2-289">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-289">Parameters - dataSource</span></span>

<span data-ttu-id="065f2-290">objectSet</span><span class="sxs-lookup"><span data-stu-id="065f2-290">objectSet</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="065f2-291">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-291">Return Value - dataSource</span></span>

## <a name="method-datasourcecount"></a><span data-ttu-id="065f2-292">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="065f2-292">Method dataSourceCount</span></span>

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a><span data-ttu-id="065f2-293">戻り値 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="065f2-293">Return Value - dataSourceCount</span></span>

## <a name="method-defaultdatasource"></a><span data-ttu-id="065f2-294">メソッド defaultDataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-294">Method defaultDataSource</span></span>

```xpp
public FormObjectSet defaultDataSource([FormObjectSet value])
```

### <a name="parameters---defaultdatasource"></a><span data-ttu-id="065f2-295">パラメーター - defaultDataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-295">Parameters - defaultDataSource</span></span>

<span data-ttu-id="065f2-296">値</span><span class="sxs-lookup"><span data-stu-id="065f2-296">value</span></span>  

### <a name="return-value---defaultdatasource"></a><span data-ttu-id="065f2-297">戻り値 - defaultDataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-297">Return Value - defaultDataSource</span></span>

## <a name="method-defaultinitialqueryvaluesoncreate"></a><span data-ttu-id="065f2-298">メソッド defaultInitialQueryValuesOnCreate</span><span class="sxs-lookup"><span data-stu-id="065f2-298">Method defaultInitialQueryValuesOnCreate</span></span>

```xpp
public boolean defaultInitialQueryValuesOnCreate([boolean value])
```

### <a name="parameters---defaultinitialqueryvaluesoncreate"></a><span data-ttu-id="065f2-299">パラメーター - defaultInitialQueryValuesOnCreate</span><span class="sxs-lookup"><span data-stu-id="065f2-299">Parameters - defaultInitialQueryValuesOnCreate</span></span>

<span data-ttu-id="065f2-300">値</span><span class="sxs-lookup"><span data-stu-id="065f2-300">value</span></span>  

### <a name="return-value---defaultinitialqueryvaluesoncreate"></a><span data-ttu-id="065f2-301">戻り値 - defaultInitialQueryValuesOnCreate</span><span class="sxs-lookup"><span data-stu-id="065f2-301">Return Value - defaultInitialQueryValuesOnCreate</span></span>

## <a name="method-design"></a><span data-ttu-id="065f2-302">メソッド design</span><span class="sxs-lookup"><span data-stu-id="065f2-302">Method design</span></span>

```xpp
public FormDesign design([int reserved])
```

### <a name="parameters---design"></a><span data-ttu-id="065f2-303">パラメーター - design</span><span class="sxs-lookup"><span data-stu-id="065f2-303">Parameters - design</span></span>

<span data-ttu-id="065f2-304">reserved</span><span class="sxs-lookup"><span data-stu-id="065f2-304">reserved</span></span>  

### <a name="return-value---design"></a><span data-ttu-id="065f2-305">戻り値 - design</span><span class="sxs-lookup"><span data-stu-id="065f2-305">Return Value - design</span></span>

## <a name="method-doccursor"></a><span data-ttu-id="065f2-306">メソッド docCursor</span><span class="sxs-lookup"><span data-stu-id="065f2-306">Method docCursor</span></span>

```xpp
public Common docCursor()
```

### <a name="return-value---doccursor"></a><span data-ttu-id="065f2-307">戻り値 - docCursor</span><span class="sxs-lookup"><span data-stu-id="065f2-307">Return Value - docCursor</span></span>

## <a name="method-enablecountryregion"></a><span data-ttu-id="065f2-308">メソッド enableCountryRegion</span><span class="sxs-lookup"><span data-stu-id="065f2-308">Method enableCountryRegion</span></span>

```xpp
public boolean enableCountryRegion([boolean flag])
```

### <a name="parameters---enablecountryregion"></a><span data-ttu-id="065f2-309">パラメーター - enableCountryRegion</span><span class="sxs-lookup"><span data-stu-id="065f2-309">Parameters - enableCountryRegion</span></span>

<span data-ttu-id="065f2-310">flag</span><span class="sxs-lookup"><span data-stu-id="065f2-310">flag</span></span>  

### <a name="return-value---enablecountryregion"></a><span data-ttu-id="065f2-311">戻り値 - enableCountryRegion</span><span class="sxs-lookup"><span data-stu-id="065f2-311">Return Value - enableCountryRegion</span></span>

## <a name="method-form"></a><span data-ttu-id="065f2-312">メソッド form</span><span class="sxs-lookup"><span data-stu-id="065f2-312">Method form</span></span>

```xpp
public Form form()
```

### <a name="return-value---form"></a><span data-ttu-id="065f2-313">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="065f2-313">Return Value - form</span></span>

## <a name="method-getactiveworkflowconfiguration"></a><span data-ttu-id="065f2-314">メソッド getActiveWorkflowConfiguration</span><span class="sxs-lookup"><span data-stu-id="065f2-314">Method getActiveWorkflowConfiguration</span></span>

```xpp
public Common getActiveWorkflowConfiguration()
```

### <a name="return-value---getactiveworkflowconfiguration"></a><span data-ttu-id="065f2-315">戻り値 - getActiveWorkflowConfiguration</span><span class="sxs-lookup"><span data-stu-id="065f2-315">Return Value - getActiveWorkflowConfiguration</span></span>

## <a name="method-getactiveworkflowtrackingstatus"></a><span data-ttu-id="065f2-316">メソッド getActiveWorkflowTrackingStatus</span><span class="sxs-lookup"><span data-stu-id="065f2-316">Method getActiveWorkflowTrackingStatus</span></span>

```xpp
public Common getActiveWorkflowTrackingStatus()
```

### <a name="return-value---getactiveworkflowtrackingstatus"></a><span data-ttu-id="065f2-317">戻り値 - getActiveWorkflowTrackingStatus</span><span class="sxs-lookup"><span data-stu-id="065f2-317">Return Value - getActiveWorkflowTrackingStatus</span></span>

## <a name="method-getactiveworkflowworkitem"></a><span data-ttu-id="065f2-318">メソッド getActiveWorkflowWorkItem</span><span class="sxs-lookup"><span data-stu-id="065f2-318">Method getActiveWorkflowWorkItem</span></span>

```xpp
public Common getActiveWorkflowWorkItem()
```

### <a name="return-value---getactiveworkflowworkitem"></a><span data-ttu-id="065f2-319">戻り値 - getActiveWorkflowWorkItem</span><span class="sxs-lookup"><span data-stu-id="065f2-319">Return Value - getActiveWorkflowWorkItem</span></span>

## <a name="method-getautocompletestring"></a><span data-ttu-id="065f2-320">メソッド getAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-320">Method getAutoCompleteString</span></span>

```xpp
public container getAutoCompleteString(int startIdx, [FormControl control], [str searchString])
```

### <a name="parameters---getautocompletestring"></a><span data-ttu-id="065f2-321">パラメーター - getAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-321">Parameters - getAutoCompleteString</span></span>

<span data-ttu-id="065f2-322">startIdx</span><span class="sxs-lookup"><span data-stu-id="065f2-322">startIdx</span></span>  

<!-- -->

<span data-ttu-id="065f2-323">control</span><span class="sxs-lookup"><span data-stu-id="065f2-323">control</span></span>  

<!-- -->

<span data-ttu-id="065f2-324">searchString</span><span class="sxs-lookup"><span data-stu-id="065f2-324">searchString</span></span>  

### <a name="return-value---getautocompletestring"></a><span data-ttu-id="065f2-325">戻り値 - getAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-325">Return Value - getAutoCompleteString</span></span>

## <a name="method-getformhelptopic"></a><span data-ttu-id="065f2-326">メソッド getFormHelpTopic</span><span class="sxs-lookup"><span data-stu-id="065f2-326">Method getFormHelpTopic</span></span>

```xpp
public str getFormHelpTopic()
```

### <a name="return-value---getformhelptopic"></a><span data-ttu-id="065f2-327">戻り値 - getFormHelpTopic</span><span class="sxs-lookup"><span data-stu-id="065f2-327">Return Value - getFormHelpTopic</span></span>

## <a name="method-getnextfield"></a><span data-ttu-id="065f2-328">メソッド getNextField</span><span class="sxs-lookup"><span data-stu-id="065f2-328">Method getNextField</span></span>

```xpp
public FormControl getNextField(FormControl control, [int flags])
```

### <a name="parameters---getnextfield"></a><span data-ttu-id="065f2-329">パラメーター - getNextField</span><span class="sxs-lookup"><span data-stu-id="065f2-329">Parameters - getNextField</span></span>

<span data-ttu-id="065f2-330">control</span><span class="sxs-lookup"><span data-stu-id="065f2-330">control</span></span>  

<!-- -->

<span data-ttu-id="065f2-331">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-331">flags</span></span>  

### <a name="return-value---getnextfield"></a><span data-ttu-id="065f2-332">戻り値 - getNextField</span><span class="sxs-lookup"><span data-stu-id="065f2-332">Return Value - getNextField</span></span>

## <a name="method-getprevfield"></a><span data-ttu-id="065f2-333">メソッド getPrevField</span><span class="sxs-lookup"><span data-stu-id="065f2-333">Method getPrevField</span></span>

```xpp
public FormControl getPrevField(FormControl control, [int flags])
```

### <a name="parameters---getprevfield"></a><span data-ttu-id="065f2-334">パラメーター - getPrevField</span><span class="sxs-lookup"><span data-stu-id="065f2-334">Parameters - getPrevField</span></span>

<span data-ttu-id="065f2-335">control</span><span class="sxs-lookup"><span data-stu-id="065f2-335">control</span></span>  

<!-- -->

<span data-ttu-id="065f2-336">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-336">flags</span></span>  

### <a name="return-value---getprevfield"></a><span data-ttu-id="065f2-337">戻り値 - getPrevField</span><span class="sxs-lookup"><span data-stu-id="065f2-337">Return Value - getPrevField</span></span>

## <a name="method-hasexecutedinit"></a><span data-ttu-id="065f2-338">メソッド hasExecutedInit</span><span class="sxs-lookup"><span data-stu-id="065f2-338">Method hasExecutedInit</span></span>

```xpp
public boolean hasExecutedInit()
```

### <a name="return-value---hasexecutedinit"></a><span data-ttu-id="065f2-339">戻り値 - hasExecutedInit</span><span class="sxs-lookup"><span data-stu-id="065f2-339">Return Value - hasExecutedInit</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="065f2-340">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="065f2-340">Method hWnd</span></span>

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a><span data-ttu-id="065f2-341">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="065f2-341">Return Value - hWnd</span></span>

## <a name="method-installmessageproc"></a><span data-ttu-id="065f2-342">メソッド installMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-342">Method installMessageProc</span></span>

```xpp
public int installMessageProc(int message, int handle, str method)
```

### <a name="parameters---installmessageproc"></a><span data-ttu-id="065f2-343">パラメーター - installMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-343">Parameters - installMessageProc</span></span>

<span data-ttu-id="065f2-344">メッセージ</span><span class="sxs-lookup"><span data-stu-id="065f2-344">message</span></span>  

<!-- -->

<span data-ttu-id="065f2-345">handle</span><span class="sxs-lookup"><span data-stu-id="065f2-345">handle</span></span>  

<!-- -->

<span data-ttu-id="065f2-346">メソッド</span><span class="sxs-lookup"><span data-stu-id="065f2-346">method</span></span>  

### <a name="return-value---installmessageproc"></a><span data-ttu-id="065f2-347">戻り値 - installMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-347">Return Value - installMessageProc</span></span>

## <a name="method-inviewmode"></a><span data-ttu-id="065f2-348">メソッド inViewMode</span><span class="sxs-lookup"><span data-stu-id="065f2-348">Method inViewMode</span></span>

```xpp
public boolean inViewMode()
```

### <a name="return-value---inviewmode"></a><span data-ttu-id="065f2-349">戻り値 - inViewMode</span><span class="sxs-lookup"><span data-stu-id="065f2-349">Return Value - inViewMode</span></span>

## <a name="method-isdatainteractionsupported"></a><span data-ttu-id="065f2-350">メソッド isDataInteractionSupported</span><span class="sxs-lookup"><span data-stu-id="065f2-350">Method isDataInteractionSupported</span></span>

```xpp
public boolean isDataInteractionSupported()
```

### <a name="return-value---isdatainteractionsupported"></a><span data-ttu-id="065f2-351">戻り値 - isDataInteractionSupported</span><span class="sxs-lookup"><span data-stu-id="065f2-351">Return Value - isDataInteractionSupported</span></span>

## <a name="method-ispreloadedinstance"></a><span data-ttu-id="065f2-352">メソッド isPreloadedInstance</span><span class="sxs-lookup"><span data-stu-id="065f2-352">Method isPreloadedInstance</span></span>

```xpp
public boolean isPreloadedInstance()
```

### <a name="return-value---ispreloadedinstance"></a><span data-ttu-id="065f2-353">戻り値 - isPreloadedInstance</span><span class="sxs-lookup"><span data-stu-id="065f2-353">Return Value - isPreloadedInstance</span></span>

## <a name="method-isformpart"></a><span data-ttu-id="065f2-354">メソッド isFormPart</span><span class="sxs-lookup"><span data-stu-id="065f2-354">Method isFormPart</span></span>

```xpp
public boolean isFormPart()
```

### <a name="return-value---isformpart"></a><span data-ttu-id="065f2-355">戻り値 - isFormPart</span><span class="sxs-lookup"><span data-stu-id="065f2-355">Return Value - isFormPart</span></span>

## <a name="method-isfactbox"></a><span data-ttu-id="065f2-356">メソッド isFactBox</span><span class="sxs-lookup"><span data-stu-id="065f2-356">Method isFactBox</span></span>

```xpp
public boolean isFactBox()
```

### <a name="return-value---isfactbox"></a><span data-ttu-id="065f2-357">戻り値 - isFactBox</span><span class="sxs-lookup"><span data-stu-id="065f2-357">Return Value - isFactBox</span></span>

## <a name="method-islookupform"></a><span data-ttu-id="065f2-358">メソッド isLookupForm</span><span class="sxs-lookup"><span data-stu-id="065f2-358">Method isLookupForm</span></span>

```xpp
public boolean isLookupForm()
```

### <a name="return-value---islookupform"></a><span data-ttu-id="065f2-359">戻り値 - isLookupForm</span><span class="sxs-lookup"><span data-stu-id="065f2-359">Return Value - isLookupForm</span></span>

## <a name="method-ispartremote"></a><span data-ttu-id="065f2-360">メソッド isPartRemote</span><span class="sxs-lookup"><span data-stu-id="065f2-360">Method isPartRemote</span></span>

```xpp
public boolean isPartRemote()
```

### <a name="return-value---ispartremote"></a><span data-ttu-id="065f2-361">戻り値 - isPartRemote</span><span class="sxs-lookup"><span data-stu-id="065f2-361">Return Value - isPartRemote</span></span>

## <a name="method-ispartlocal"></a><span data-ttu-id="065f2-362">メソッド isPartLocal</span><span class="sxs-lookup"><span data-stu-id="065f2-362">Method isPartLocal</span></span>

```xpp
public boolean isPartLocal()
```

### <a name="return-value---ispartlocal"></a><span data-ttu-id="065f2-363">戻り値 - isPartLocal</span><span class="sxs-lookup"><span data-stu-id="065f2-363">Return Value - isPartLocal</span></span>

## <a name="method-isworkflowenabled"></a><span data-ttu-id="065f2-364">メソッド isWorkflowEnabled</span><span class="sxs-lookup"><span data-stu-id="065f2-364">Method isWorkflowEnabled</span></span>

```xpp
public boolean isWorkflowEnabled()
```

### <a name="return-value---isworkflowenabled"></a><span data-ttu-id="065f2-365">戻り値 - isWorkflowEnabled</span><span class="sxs-lookup"><span data-stu-id="065f2-365">Return Value - isWorkflowEnabled</span></span>

## <a name="method-loadworkflowconfiguration"></a><span data-ttu-id="065f2-366">メソッド loadWorkflowConfiguration</span><span class="sxs-lookup"><span data-stu-id="065f2-366">Method loadWorkflowConfiguration</span></span>

```xpp
public Common loadWorkflowConfiguration()
```

### <a name="return-value---loadworkflowconfiguration"></a><span data-ttu-id="065f2-367">戻り値 - loadWorkflowConfiguration</span><span class="sxs-lookup"><span data-stu-id="065f2-367">Return Value - loadWorkflowConfiguration</span></span>

## <a name="method-lockwindowupdate"></a><span data-ttu-id="065f2-368">メソッド lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="065f2-368">Method lockWindowUpdate</span></span>

```xpp
public boolean lockWindowUpdate(boolean lock)
```

### <a name="parameters---lockwindowupdate"></a><span data-ttu-id="065f2-369">パラメーター - lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="065f2-369">Parameters - lockWindowUpdate</span></span>

<span data-ttu-id="065f2-370">lock</span><span class="sxs-lookup"><span data-stu-id="065f2-370">lock</span></span>  

### <a name="return-value---lockwindowupdate"></a><span data-ttu-id="065f2-371">戻り値 - lockWindowUpdate</span><span class="sxs-lookup"><span data-stu-id="065f2-371">Return Value - lockWindowUpdate</span></span>

## <a name="method-name"></a><span data-ttu-id="065f2-372">メソッド名</span><span class="sxs-lookup"><span data-stu-id="065f2-372">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="065f2-373">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="065f2-373">Return Value - name</span></span>

## <a name="method-objectset"></a><span data-ttu-id="065f2-374">メソッド objectSet</span><span class="sxs-lookup"><span data-stu-id="065f2-374">Method objectSet</span></span>

```xpp
public FormObjectSet objectSet([AnyType objectSet])
```

### <a name="parameters---objectset"></a><span data-ttu-id="065f2-375">パラメーター - objectSet</span><span class="sxs-lookup"><span data-stu-id="065f2-375">Parameters - objectSet</span></span>

<span data-ttu-id="065f2-376">objectSet</span><span class="sxs-lookup"><span data-stu-id="065f2-376">objectSet</span></span>  

### <a name="return-value---objectset"></a><span data-ttu-id="065f2-377">戻り値 - objectSet</span><span class="sxs-lookup"><span data-stu-id="065f2-377">Return Value - objectSet</span></span>

## <a name="method-resetasyncoperationspendingstate"></a><span data-ttu-id="065f2-378">メソッド resetAsyncOperationsPendingState</span><span class="sxs-lookup"><span data-stu-id="065f2-378">Method resetAsyncOperationsPendingState</span></span>

```xpp
public boolean resetAsyncOperationsPendingState()
```

### <a name="return-value---resetasyncoperationspendingstate"></a><span data-ttu-id="065f2-379">戻り値 - resetAsyncOperationsPendingState</span><span class="sxs-lookup"><span data-stu-id="065f2-379">Return Value - resetAsyncOperationsPendingState</span></span>

## <a name="method-pageinteraction"></a><span data-ttu-id="065f2-380">メソッド pageInteraction</span><span class="sxs-lookup"><span data-stu-id="065f2-380">Method pageInteraction</span></span>

```xpp
public PageInteraction pageInteraction()
```

### <a name="return-value---pageinteraction"></a><span data-ttu-id="065f2-381">戻り値 - pageInteraction</span><span class="sxs-lookup"><span data-stu-id="065f2-381">Return Value - pageInteraction</span></span>

## <a name="method-paste"></a><span data-ttu-id="065f2-382">メソッド paste</span><span class="sxs-lookup"><span data-stu-id="065f2-382">Method paste</span></span>

```xpp
public boolean paste()
```

### <a name="return-value---paste"></a><span data-ttu-id="065f2-383">戻り値 - paste</span><span class="sxs-lookup"><span data-stu-id="065f2-383">Return Value - paste</span></span>

## <a name="method-recordingscopeid"></a><span data-ttu-id="065f2-384">メソッド recordingScopeId</span><span class="sxs-lookup"><span data-stu-id="065f2-384">Method recordingScopeId</span></span>

```xpp
public str recordingScopeId()
```

### <a name="return-value---recordingscopeid"></a><span data-ttu-id="065f2-385">戻り値 - recordingScopeId</span><span class="sxs-lookup"><span data-stu-id="065f2-385">Return Value - recordingScopeId</span></span>

## <a name="method-removemessageproc"></a><span data-ttu-id="065f2-386">メソッド removeMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-386">Method removeMessageProc</span></span>

```xpp
public boolean removeMessageProc(int message, int handle)
```

### <a name="parameters---removemessageproc"></a><span data-ttu-id="065f2-387">パラメーター - removeMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-387">Parameters - removeMessageProc</span></span>

<span data-ttu-id="065f2-388">メッセージ</span><span class="sxs-lookup"><span data-stu-id="065f2-388">message</span></span>  

<!-- -->

<span data-ttu-id="065f2-389">handle</span><span class="sxs-lookup"><span data-stu-id="065f2-389">handle</span></span>  

### <a name="return-value---removemessageproc"></a><span data-ttu-id="065f2-390">戻り値 - removeMessageProc</span><span class="sxs-lookup"><span data-stu-id="065f2-390">Return Value - removeMessageProc</span></span>

## <a name="method-rootformdatasources"></a><span data-ttu-id="065f2-391">メソッド rootFormDataSources</span><span class="sxs-lookup"><span data-stu-id="065f2-391">Method rootFormDataSources</span></span>

```xpp
public List rootFormDataSources()
```

### <a name="return-value---rootformdatasources"></a><span data-ttu-id="065f2-392">戻り値 - rootFormDataSources</span><span class="sxs-lookup"><span data-stu-id="065f2-392">Return Value - rootFormDataSources</span></span>

## <a name="method-selectcontrol"></a><span data-ttu-id="065f2-393">メソッド selectControl</span><span class="sxs-lookup"><span data-stu-id="065f2-393">Method selectControl</span></span>

```xpp
public boolean selectControl(FormControl control)
```

### <a name="parameters---selectcontrol"></a><span data-ttu-id="065f2-394">パラメーター - selectControl</span><span class="sxs-lookup"><span data-stu-id="065f2-394">Parameters - selectControl</span></span>

<span data-ttu-id="065f2-395">control</span><span class="sxs-lookup"><span data-stu-id="065f2-395">control</span></span>  

### <a name="return-value---selectcontrol"></a><span data-ttu-id="065f2-396">戻り値 - selectControl</span><span class="sxs-lookup"><span data-stu-id="065f2-396">Return Value - selectControl</span></span>

## <a name="method-selectedcontrol"></a><span data-ttu-id="065f2-397">メソッド selectedControl</span><span class="sxs-lookup"><span data-stu-id="065f2-397">Method selectedControl</span></span>

```xpp
public FormControl selectedControl()
```

### <a name="return-value---selectedcontrol"></a><span data-ttu-id="065f2-398">戻り値 - selectedControl</span><span class="sxs-lookup"><span data-stu-id="065f2-398">Return Value - selectedControl</span></span>

## <a name="method-selectrecordmodeselectedrecord"></a><span data-ttu-id="065f2-399">メソッド selectRecordModeSelectedRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-399">Method selectRecordModeSelectedRecord</span></span>

```xpp
public Common selectRecordModeSelectedRecord([Common selectedRecord])
```

### <a name="parameters---selectrecordmodeselectedrecord"></a><span data-ttu-id="065f2-400">パラメーター - selectRecordModeSelectedRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-400">Parameters - selectRecordModeSelectedRecord</span></span>

<span data-ttu-id="065f2-401">selectedRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-401">selectedRecord</span></span>  

### <a name="return-value---selectrecordmodeselectedrecord"></a><span data-ttu-id="065f2-402">戻り値 - selectRecordModeSelectedRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-402">Return Value - selectRecordModeSelectedRecord</span></span>

## <a name="method-selecttarget"></a><span data-ttu-id="065f2-403">メソッド selectTarget</span><span class="sxs-lookup"><span data-stu-id="065f2-403">Method selectTarget</span></span>

```xpp
public FormControl selectTarget([FormControl target])
```

### <a name="parameters---selecttarget"></a><span data-ttu-id="065f2-404">パラメーター - selectTarget</span><span class="sxs-lookup"><span data-stu-id="065f2-404">Parameters - selectTarget</span></span>

<span data-ttu-id="065f2-405">target</span><span class="sxs-lookup"><span data-stu-id="065f2-405">target</span></span>  

### <a name="return-value---selecttarget"></a><span data-ttu-id="065f2-406">戻り値 - selectTarget</span><span class="sxs-lookup"><span data-stu-id="065f2-406">Return Value - selectTarget</span></span>

## <a name="method-taborder"></a><span data-ttu-id="065f2-407">メソッド tabOrder</span><span class="sxs-lookup"><span data-stu-id="065f2-407">Method tabOrder</span></span>

```xpp
public Array tabOrder([Array newValue])
```

### <a name="parameters---taborder"></a><span data-ttu-id="065f2-408">パラメーター - tabOrder</span><span class="sxs-lookup"><span data-stu-id="065f2-408">Parameters - tabOrder</span></span>

<span data-ttu-id="065f2-409">newValue</span><span class="sxs-lookup"><span data-stu-id="065f2-409">newValue</span></span>  

### <a name="return-value---taborder"></a><span data-ttu-id="065f2-410">戻り値 - tabOrder</span><span class="sxs-lookup"><span data-stu-id="065f2-410">Return Value - tabOrder</span></span>

## <a name="method-task"></a><span data-ttu-id="065f2-411">メソッド task</span><span class="sxs-lookup"><span data-stu-id="065f2-411">Method task</span></span>

```xpp
public int task(int taskId)
```

### <a name="parameters---task"></a><span data-ttu-id="065f2-412">パラメーター - task</span><span class="sxs-lookup"><span data-stu-id="065f2-412">Parameters - task</span></span>

<span data-ttu-id="065f2-413">taskId</span><span class="sxs-lookup"><span data-stu-id="065f2-413">taskId</span></span>  

### <a name="return-value---task"></a><span data-ttu-id="065f2-414">戻り値 - task</span><span class="sxs-lookup"><span data-stu-id="065f2-414">Return Value - task</span></span>

## <a name="method-tostring"></a><span data-ttu-id="065f2-415">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="065f2-415">Method toString</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="065f2-416">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="065f2-416">Return Value - toString</span></span>

## <a name="method-workflowdatasource"></a><span data-ttu-id="065f2-417">メソッド workflowDataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-417">Method workflowDataSource</span></span>

```xpp
public FormObjectSet workflowDataSource()
```

### <a name="return-value---workflowdatasource"></a><span data-ttu-id="065f2-418">戻り値 - workflowDataSource</span><span class="sxs-lookup"><span data-stu-id="065f2-418">Return Value - workflowDataSource</span></span>

## <a name="method-workflowtype"></a><span data-ttu-id="065f2-419">メソッド workflowType</span><span class="sxs-lookup"><span data-stu-id="065f2-419">Method workflowType</span></span>

```xpp
public str workflowType()
```

### <a name="return-value---workflowtype"></a><span data-ttu-id="065f2-420">戻り値 - workflowType</span><span class="sxs-lookup"><span data-stu-id="065f2-420">Return Value - workflowType</span></span>

## <a name="method-runasync"></a><span data-ttu-id="065f2-421">メソッド runAsync</span><span class="sxs-lookup"><span data-stu-id="065f2-421">Method runAsync</span></span>

```xpp
public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [str callbackFormMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])
```

### <a name="parameters---runasync"></a><span data-ttu-id="065f2-422">パラメーター - runAsync</span><span class="sxs-lookup"><span data-stu-id="065f2-422">Parameters - runAsync</span></span>

<span data-ttu-id="065f2-423">runAsClassId</span><span class="sxs-lookup"><span data-stu-id="065f2-423">runAsClassId</span></span>  

<!-- -->

<span data-ttu-id="065f2-424">runAsStaticMethodName</span><span class="sxs-lookup"><span data-stu-id="065f2-424">runAsStaticMethodName</span></span>  

<!-- -->

<span data-ttu-id="065f2-425">parms</span><span class="sxs-lookup"><span data-stu-id="065f2-425">parms</span></span>  

<!-- -->

<span data-ttu-id="065f2-426">cancellationToken</span><span class="sxs-lookup"><span data-stu-id="065f2-426">cancellationToken</span></span>  

<!-- -->

<span data-ttu-id="065f2-427">callbackFormMethodName</span><span class="sxs-lookup"><span data-stu-id="065f2-427">callbackFormMethodName</span></span>  

<!-- -->

<span data-ttu-id="065f2-428">asyncState</span><span class="sxs-lookup"><span data-stu-id="065f2-428">asyncState</span></span>  

<!-- -->

<span data-ttu-id="065f2-429">userId</span><span class="sxs-lookup"><span data-stu-id="065f2-429">userId</span></span>  

<!-- -->

<span data-ttu-id="065f2-430">会社</span><span class="sxs-lookup"><span data-stu-id="065f2-430">company</span></span>  

<!-- -->

<span data-ttu-id="065f2-431">言語</span><span class="sxs-lookup"><span data-stu-id="065f2-431">language</span></span>  

<!-- -->

<span data-ttu-id="065f2-432">partitionKey</span><span class="sxs-lookup"><span data-stu-id="065f2-432">partitionKey</span></span>  

<!-- -->

<span data-ttu-id="065f2-433">オプション</span><span class="sxs-lookup"><span data-stu-id="065f2-433">options</span></span>  

### <a name="return-value---runasync"></a><span data-ttu-id="065f2-434">戻り値 - runAsync</span><span class="sxs-lookup"><span data-stu-id="065f2-434">Return Value - runAsync</span></span>

## <a name="method-settimeoutex"></a><span data-ttu-id="065f2-435">メソッド setTimeoutEx</span><span class="sxs-lookup"><span data-stu-id="065f2-435">Method setTimeoutEx</span></span>

```xpp
public System.Threading.Tasks.Task setTimeoutEx([str formMethodName], [container parms], [int delay], [System.Threading.CancellationToken cancellationToken])
```

### <a name="parameters---settimeoutex"></a><span data-ttu-id="065f2-436">パラメーター - setTimeoutEx</span><span class="sxs-lookup"><span data-stu-id="065f2-436">Parameters - setTimeoutEx</span></span>

<span data-ttu-id="065f2-437">formMethodName</span><span class="sxs-lookup"><span data-stu-id="065f2-437">formMethodName</span></span>  

<!-- -->

<span data-ttu-id="065f2-438">parms</span><span class="sxs-lookup"><span data-stu-id="065f2-438">parms</span></span>  

<!-- -->

<span data-ttu-id="065f2-439">遅延</span><span class="sxs-lookup"><span data-stu-id="065f2-439">delay</span></span>  

<!-- -->

<span data-ttu-id="065f2-440">cancellationToken</span><span class="sxs-lookup"><span data-stu-id="065f2-440">cancellationToken</span></span>  

### <a name="return-value---settimeoutex"></a><span data-ttu-id="065f2-441">戻り値 - setTimeoutEx</span><span class="sxs-lookup"><span data-stu-id="065f2-441">Return Value - setTimeoutEx</span></span>

## <a name="method-setparenthandle"></a><span data-ttu-id="065f2-442">メソッド setParentHandle</span><span class="sxs-lookup"><span data-stu-id="065f2-442">Method setParentHandle</span></span>

```xpp
public void setParentHandle(int hwnd)
```

### <a name="parameters---setparenthandle"></a><span data-ttu-id="065f2-443">パラメーター - setParentHandle</span><span class="sxs-lookup"><span data-stu-id="065f2-443">Parameters - setParentHandle</span></span>

<span data-ttu-id="065f2-444">hwnd</span><span class="sxs-lookup"><span data-stu-id="065f2-444">hwnd</span></span>  

## <a name="method-setformhelptopic"></a><span data-ttu-id="065f2-445">メソッド setFormHelpTopic</span><span class="sxs-lookup"><span data-stu-id="065f2-445">Method setFormHelpTopic</span></span>

```xpp
public void setFormHelpTopic(str formHelpTopic)
```

### <a name="parameters---setformhelptopic"></a><span data-ttu-id="065f2-446">パラメーター - setFormHelpTopic</span><span class="sxs-lookup"><span data-stu-id="065f2-446">Parameters - setFormHelpTopic</span></span>

<span data-ttu-id="065f2-447">formHelpTopic</span><span class="sxs-lookup"><span data-stu-id="065f2-447">formHelpTopic</span></span>  

## <a name="method-setfactboxeditable"></a><span data-ttu-id="065f2-448">メソッド setFactBoxEditable</span><span class="sxs-lookup"><span data-stu-id="065f2-448">Method setFactBoxEditable</span></span>

```xpp
public void setFactBoxEditable()
```

## <a name="method-setautocompletestring"></a><span data-ttu-id="065f2-449">メソッド setAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-449">Method setAutoCompleteString</span></span>

```xpp
public void setAutoCompleteString(str string, AnyType control)
```

### <a name="parameters---setautocompletestring"></a><span data-ttu-id="065f2-450">パラメーター - setAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-450">Parameters - setAutoCompleteString</span></span>

<span data-ttu-id="065f2-451">文字列</span><span class="sxs-lookup"><span data-stu-id="065f2-451">string</span></span>  

<!-- -->

<span data-ttu-id="065f2-452">control</span><span class="sxs-lookup"><span data-stu-id="065f2-452">control</span></span>  

## <a name="method-raiseonclosing"></a><span data-ttu-id="065f2-453">メソッド RaiseOnClosing</span><span class="sxs-lookup"><span data-stu-id="065f2-453">Method RaiseOnClosing</span></span>

```xpp
public void RaiseOnClosing([FormEventArgs e])
```

### <a name="parameters---raiseonclosing"></a><span data-ttu-id="065f2-454">パラメーター - RaiseOnClosing</span><span class="sxs-lookup"><span data-stu-id="065f2-454">Parameters - RaiseOnClosing</span></span>

<span data-ttu-id="065f2-455">e</span><span class="sxs-lookup"><span data-stu-id="065f2-455">e</span></span>  

## <a name="method-inlineloadingkey"></a><span data-ttu-id="065f2-456">メソッド inlineLoadingKey</span><span class="sxs-lookup"><span data-stu-id="065f2-456">Method inlineLoadingKey</span></span>

```xpp
public void inlineLoadingKey(FormControl parentControl)
```

### <a name="parameters---inlineloadingkey"></a><span data-ttu-id="065f2-457">パラメータ－ - inlineLoadingKey</span><span class="sxs-lookup"><span data-stu-id="065f2-457">Parameters - inlineLoadingKey</span></span>

<span data-ttu-id="065f2-458">parentControl</span><span class="sxs-lookup"><span data-stu-id="065f2-458">parentControl</span></span>  

## <a name="method-closeselect"></a><span data-ttu-id="065f2-459">メソッド closeSelect</span><span class="sxs-lookup"><span data-stu-id="065f2-459">Method closeSelect</span></span>

```xpp
public void closeSelect(str selectString)
```

### <a name="parameters---closeselect"></a><span data-ttu-id="065f2-460">パラメーター - closeSelect</span><span class="sxs-lookup"><span data-stu-id="065f2-460">Parameters - closeSelect</span></span>

<span data-ttu-id="065f2-461">selectString</span><span class="sxs-lookup"><span data-stu-id="065f2-461">selectString</span></span>  

## <a name="method-raiseonactivated"></a><span data-ttu-id="065f2-462">メソッド RaiseOnActivated</span><span class="sxs-lookup"><span data-stu-id="065f2-462">Method RaiseOnActivated</span></span>

```xpp
public void RaiseOnActivated([FormEventArgs e])
```

### <a name="parameters---raiseonactivated"></a><span data-ttu-id="065f2-463">パラメーター - RaiseOnActivated</span><span class="sxs-lookup"><span data-stu-id="065f2-463">Parameters - RaiseOnActivated</span></span>

<span data-ttu-id="065f2-464">e</span><span class="sxs-lookup"><span data-stu-id="065f2-464">e</span></span>  

## <a name="method-prevfield"></a><span data-ttu-id="065f2-465">メソッド prevField</span><span class="sxs-lookup"><span data-stu-id="065f2-465">Method prevField</span></span>

```xpp
public void prevField([int flags])
```

### <a name="parameters---prevfield"></a><span data-ttu-id="065f2-466">パラメーター - prevField</span><span class="sxs-lookup"><span data-stu-id="065f2-466">Parameters - prevField</span></span>

<span data-ttu-id="065f2-467">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-467">flags</span></span>  

## <a name="method-send"></a><span data-ttu-id="065f2-468">メソッド send</span><span class="sxs-lookup"><span data-stu-id="065f2-468">Method send</span></span>

```xpp
public void send()
```

## <a name="method-raiseoninitializing"></a><span data-ttu-id="065f2-469">メソッド RaiseOnInitializing</span><span class="sxs-lookup"><span data-stu-id="065f2-469">Method RaiseOnInitializing</span></span>

```xpp
public void RaiseOnInitializing([FormEventArgs e])
```

### <a name="parameters---raiseoninitializing"></a><span data-ttu-id="065f2-470">パラメーター - RaiseOnInitializing</span><span class="sxs-lookup"><span data-stu-id="065f2-470">Parameters - RaiseOnInitializing</span></span>

<span data-ttu-id="065f2-471">e</span><span class="sxs-lookup"><span data-stu-id="065f2-471">e</span></span>  

## <a name="method-updateworkflowcontrols"></a><span data-ttu-id="065f2-472">メソッド updateWorkflowControls</span><span class="sxs-lookup"><span data-stu-id="065f2-472">Method updateWorkflowControls</span></span>

```xpp
public void updateWorkflowControls()
```

## <a name="method-closecancel"></a><span data-ttu-id="065f2-473">メソッド closeCancel</span><span class="sxs-lookup"><span data-stu-id="065f2-473">Method closeCancel</span></span>

```xpp
public void closeCancel()
```

## <a name="method-lastfield"></a><span data-ttu-id="065f2-474">メソッド lastField</span><span class="sxs-lookup"><span data-stu-id="065f2-474">Method lastField</span></span>

```xpp
public void lastField([int flags])
```

### <a name="parameters---lastfield"></a><span data-ttu-id="065f2-475">パラメーター - lastField</span><span class="sxs-lookup"><span data-stu-id="065f2-475">Parameters - lastField</span></span>

<span data-ttu-id="065f2-476">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-476">flags</span></span>  

## <a name="method-wait"></a><span data-ttu-id="065f2-477">メソッド wait</span><span class="sxs-lookup"><span data-stu-id="065f2-477">Method wait</span></span>

```xpp
public void wait([boolean modal])
```

### <a name="parameters---wait"></a><span data-ttu-id="065f2-478">パラメーター - wait</span><span class="sxs-lookup"><span data-stu-id="065f2-478">Parameters - wait</span></span>

<span data-ttu-id="065f2-479">modal</span><span class="sxs-lookup"><span data-stu-id="065f2-479">modal</span></span>  

## <a name="method-unlock"></a><span data-ttu-id="065f2-480">メソッド unLock</span><span class="sxs-lookup"><span data-stu-id="065f2-480">Method unLock</span></span>

```xpp
public void unLock([boolean arrangeNow])
```

### <a name="parameters---unlock"></a><span data-ttu-id="065f2-481">パラメーター - unLock</span><span class="sxs-lookup"><span data-stu-id="065f2-481">Parameters - unLock</span></span>

<span data-ttu-id="065f2-482">arrangeNow</span><span class="sxs-lookup"><span data-stu-id="065f2-482">arrangeNow</span></span>  

## <a name="method-oninitialized"></a><span data-ttu-id="065f2-483">メソッド OnInitialized</span><span class="sxs-lookup"><span data-stu-id="065f2-483">Method OnInitialized</span></span>

```xpp
private void OnInitialized([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---oninitialized"></a><span data-ttu-id="065f2-484">パラメーター - OnInitialized</span><span class="sxs-lookup"><span data-stu-id="065f2-484">Parameters - OnInitialized</span></span>

<span data-ttu-id="065f2-485">sender</span><span class="sxs-lookup"><span data-stu-id="065f2-485">sender</span></span>  

<!-- -->

<span data-ttu-id="065f2-486">e</span><span class="sxs-lookup"><span data-stu-id="065f2-486">e</span></span>  

## <a name="method-detach"></a><span data-ttu-id="065f2-487">メソッド detach</span><span class="sxs-lookup"><span data-stu-id="065f2-487">Method detach</span></span>

```xpp
public void detach()
```

## <a name="method-resetstatusbarbackgroundcolor"></a><span data-ttu-id="065f2-488">メソッド resetStatusBarBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="065f2-488">Method resetStatusBarBackgroundColor</span></span>

```xpp
public void resetStatusBarBackgroundColor()
```

## <a name="method-onclosing"></a><span data-ttu-id="065f2-489">メソッド OnClosing</span><span class="sxs-lookup"><span data-stu-id="065f2-489">Method OnClosing</span></span>

```xpp
private void OnClosing([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onclosing"></a><span data-ttu-id="065f2-490">パラメーター - OnClosing</span><span class="sxs-lookup"><span data-stu-id="065f2-490">Parameters - OnClosing</span></span>

<span data-ttu-id="065f2-491">sender</span><span class="sxs-lookup"><span data-stu-id="065f2-491">sender</span></span>  

<!-- -->

<span data-ttu-id="065f2-492">e</span><span class="sxs-lookup"><span data-stu-id="065f2-492">e</span></span>  

## <a name="method-adddisplaymethod"></a><span data-ttu-id="065f2-493">メソッド addDisplayMethod</span><span class="sxs-lookup"><span data-stu-id="065f2-493">Method addDisplayMethod</span></span>

```xpp
public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, [str dataSourceName], [boolean isTableDisplayMethod])
```

### <a name="parameters---adddisplaymethod"></a><span data-ttu-id="065f2-494">パラメーター - addDisplayMethod</span><span class="sxs-lookup"><span data-stu-id="065f2-494">Parameters - addDisplayMethod</span></span>

<span data-ttu-id="065f2-495">名前</span><span class="sxs-lookup"><span data-stu-id="065f2-495">name</span></span>  

<!-- -->

<span data-ttu-id="065f2-496">displayKind</span><span class="sxs-lookup"><span data-stu-id="065f2-496">displayKind</span></span>  

<!-- -->

<span data-ttu-id="065f2-497">displayType</span><span class="sxs-lookup"><span data-stu-id="065f2-497">displayType</span></span>  

<!-- -->

<span data-ttu-id="065f2-498">displayXType</span><span class="sxs-lookup"><span data-stu-id="065f2-498">displayXType</span></span>  

<!-- -->

<span data-ttu-id="065f2-499">displayRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-499">displayRecord</span></span>  

<!-- -->

<span data-ttu-id="065f2-500">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="065f2-500">dataSourceName</span></span>  

<!-- -->

<span data-ttu-id="065f2-501">isTableDisplayMethod</span><span class="sxs-lookup"><span data-stu-id="065f2-501">isTableDisplayMethod</span></span>  

## <a name="method-print"></a><span data-ttu-id="065f2-502">メソッド print</span><span class="sxs-lookup"><span data-stu-id="065f2-502">Method print</span></span>

```xpp
public void print()
```

## <a name="method-activate"></a><span data-ttu-id="065f2-503">メソッド activate</span><span class="sxs-lookup"><span data-stu-id="065f2-503">Method activate</span></span>

```xpp
public void activate(boolean active)
```

### <a name="parameters---activate"></a><span data-ttu-id="065f2-504">パラメーター - activate</span><span class="sxs-lookup"><span data-stu-id="065f2-504">Parameters - activate</span></span>

<span data-ttu-id="065f2-505">有効</span><span class="sxs-lookup"><span data-stu-id="065f2-505">active</span></span>  

## <a name="method-resize"></a><span data-ttu-id="065f2-506">メソッド resize</span><span class="sxs-lookup"><span data-stu-id="065f2-506">Method resize</span></span>

```xpp
public void resize(int width, int height)
```

### <a name="parameters---resize"></a><span data-ttu-id="065f2-507">パラメーター - resize</span><span class="sxs-lookup"><span data-stu-id="065f2-507">Parameters - resize</span></span>

<span data-ttu-id="065f2-508">width</span><span class="sxs-lookup"><span data-stu-id="065f2-508">width</span></span>  

<!-- -->

<span data-ttu-id="065f2-509">height</span><span class="sxs-lookup"><span data-stu-id="065f2-509">height</span></span>  

## <a name="method-reload"></a><span data-ttu-id="065f2-510">メソッド reload</span><span class="sxs-lookup"><span data-stu-id="065f2-510">Method reload</span></span>

```xpp
public void reload([xArgs args])
```

### <a name="parameters---reload"></a><span data-ttu-id="065f2-511">パラメーター - reload</span><span class="sxs-lookup"><span data-stu-id="065f2-511">Parameters - reload</span></span>

<span data-ttu-id="065f2-512">args</span><span class="sxs-lookup"><span data-stu-id="065f2-512">args</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="065f2-513">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="065f2-513">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-raiseoninitialized"></a><span data-ttu-id="065f2-514">メソッド RaiseOnInitialized</span><span class="sxs-lookup"><span data-stu-id="065f2-514">Method RaiseOnInitialized</span></span>

```xpp
public void RaiseOnInitialized([FormEventArgs e])
```

### <a name="parameters---raiseoninitialized"></a><span data-ttu-id="065f2-515">パラメーター - RaiseOnInitialized</span><span class="sxs-lookup"><span data-stu-id="065f2-515">Parameters - RaiseOnInitialized</span></span>

<span data-ttu-id="065f2-516">e</span><span class="sxs-lookup"><span data-stu-id="065f2-516">e</span></span>  

## <a name="method-resetsize"></a><span data-ttu-id="065f2-517">メソッド resetSize</span><span class="sxs-lookup"><span data-stu-id="065f2-517">Method resetSize</span></span>

```xpp
public void resetSize()
```

## <a name="method-clientid"></a><span data-ttu-id="065f2-518">メソッド clientId</span><span class="sxs-lookup"><span data-stu-id="065f2-518">Method clientId</span></span>

```xpp
public void clientId(str clientId)
```

### <a name="parameters---clientid"></a><span data-ttu-id="065f2-519">パラメーター - clientId</span><span class="sxs-lookup"><span data-stu-id="065f2-519">Parameters - clientId</span></span>

<span data-ttu-id="065f2-520">clientId</span><span class="sxs-lookup"><span data-stu-id="065f2-520">clientId</span></span>  

## <a name="method-createrecord"></a><span data-ttu-id="065f2-521">メソッド createRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-521">Method createRecord</span></span>

```xpp
public void createRecord(str formDataSourceName, [boolean append])
```

### <a name="parameters---createrecord"></a><span data-ttu-id="065f2-522">パラメーター - createRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-522">Parameters - createRecord</span></span>

<span data-ttu-id="065f2-523">formDataSourceName</span><span class="sxs-lookup"><span data-stu-id="065f2-523">formDataSourceName</span></span>  

<!-- -->

<span data-ttu-id="065f2-524">append</span><span class="sxs-lookup"><span data-stu-id="065f2-524">append</span></span>  

## <a name="method-firstfield"></a><span data-ttu-id="065f2-525">メソッド firstField</span><span class="sxs-lookup"><span data-stu-id="065f2-525">Method firstField</span></span>

```xpp
public void firstField([int flags])
```

### <a name="parameters---firstfield"></a><span data-ttu-id="065f2-526">パラメーター - firstField</span><span class="sxs-lookup"><span data-stu-id="065f2-526">Parameters - firstField</span></span>

<span data-ttu-id="065f2-527">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-527">flags</span></span>  

## <a name="method-savepersonalization"></a><span data-ttu-id="065f2-528">メソッド savePersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-528">Method savePersonalization</span></span>

```xpp
public void savePersonalization(str controlName, str propertyKey, str propertyValue)
```

### <a name="parameters---savepersonalization"></a><span data-ttu-id="065f2-529">パラメーター - savePersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-529">Parameters - savePersonalization</span></span>

<span data-ttu-id="065f2-530">controlName</span><span class="sxs-lookup"><span data-stu-id="065f2-530">controlName</span></span>  

<!-- -->

<span data-ttu-id="065f2-531">propertyKey</span><span class="sxs-lookup"><span data-stu-id="065f2-531">propertyKey</span></span>  

<!-- -->

<span data-ttu-id="065f2-532">propertyValue</span><span class="sxs-lookup"><span data-stu-id="065f2-532">propertyValue</span></span>  

## <a name="method-expandfactboxpaneatstart"></a><span data-ttu-id="065f2-533">メソッド expandFactBoxPaneAtStart</span><span class="sxs-lookup"><span data-stu-id="065f2-533">Method expandFactBoxPaneAtStart</span></span>

```xpp
public void expandFactBoxPaneAtStart()
```

## <a name="method-redraw"></a><span data-ttu-id="065f2-534">メソッド redraw</span><span class="sxs-lookup"><span data-stu-id="065f2-534">Method redraw</span></span>

```xpp
public void redraw()
```

## <a name="method-arrange"></a><span data-ttu-id="065f2-535">メソッド arrange</span><span class="sxs-lookup"><span data-stu-id="065f2-535">Method arrange</span></span>

```xpp
public void arrange()
```

## <a name="method-blockpersonalization"></a><span data-ttu-id="065f2-536">メソッド blockPersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-536">Method blockPersonalization</span></span>

```xpp
public void blockPersonalization(boolean blockPersonalization)
```

### <a name="parameters---blockpersonalization"></a><span data-ttu-id="065f2-537">パラメーター - blockPersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-537">Parameters - blockPersonalization</span></span>

<span data-ttu-id="065f2-538">blockPersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-538">blockPersonalization</span></span>  

## <a name="method-nextfield"></a><span data-ttu-id="065f2-539">メソッド nextField</span><span class="sxs-lookup"><span data-stu-id="065f2-539">Method nextField</span></span>

```xpp
public void nextField([int flags])
```

### <a name="parameters---nextfield"></a><span data-ttu-id="065f2-540">パラメーター - nextField</span><span class="sxs-lookup"><span data-stu-id="065f2-540">Parameters - nextField</span></span>

<span data-ttu-id="065f2-541">flags</span><span class="sxs-lookup"><span data-stu-id="065f2-541">flags</span></span>  

## <a name="method-nextgroup"></a><span data-ttu-id="065f2-542">メソッド nextGroup</span><span class="sxs-lookup"><span data-stu-id="065f2-542">Method nextGroup</span></span>

```xpp
public void nextGroup()
```

## <a name="method-prevgroup"></a><span data-ttu-id="065f2-543">メソッド prevGroup</span><span class="sxs-lookup"><span data-stu-id="065f2-543">Method prevGroup</span></span>

```xpp
public void prevGroup()
```

## <a name="method-setformpartstyle"></a><span data-ttu-id="065f2-544">メソッド setFormPartStyle</span><span class="sxs-lookup"><span data-stu-id="065f2-544">Method setFormPartStyle</span></span>

```xpp
public void setFormPartStyle(boolean isFactBox)
```

### <a name="parameters---setformpartstyle"></a><span data-ttu-id="065f2-545">パラメーター - setFormPartStyle</span><span class="sxs-lookup"><span data-stu-id="065f2-545">Parameters - setFormPartStyle</span></span>

<span data-ttu-id="065f2-546">isFactBox</span><span class="sxs-lookup"><span data-stu-id="065f2-546">isFactBox</span></span>  

## <a name="method-run"></a><span data-ttu-id="065f2-547">メソッド run</span><span class="sxs-lookup"><span data-stu-id="065f2-547">Method run</span></span>

```xpp
public void run()
```

## <a name="method-setactive"></a><span data-ttu-id="065f2-548">メソッド setActive</span><span class="sxs-lookup"><span data-stu-id="065f2-548">Method setActive</span></span>

```xpp
public void setActive()
```

## <a name="method-closeselectrecord"></a><span data-ttu-id="065f2-549">メソッド closeSelectRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-549">Method closeSelectRecord</span></span>

```xpp
public void closeSelectRecord(Common selectedRecord)
```

### <a name="parameters---closeselectrecord"></a><span data-ttu-id="065f2-550">パラメーター - closeSelectRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-550">Parameters - closeSelectRecord</span></span>

<span data-ttu-id="065f2-551">selectedRecord</span><span class="sxs-lookup"><span data-stu-id="065f2-551">selectedRecord</span></span>  

## <a name="method-registerformspecializedcustomcontrol"></a><span data-ttu-id="065f2-552">メソッド registerFormSpecializedCustomControl</span><span class="sxs-lookup"><span data-stu-id="065f2-552">Method registerFormSpecializedCustomControl</span></span>

```xpp
public void registerFormSpecializedCustomControl(str customControlName)
```

### <a name="parameters---registerformspecializedcustomcontrol"></a><span data-ttu-id="065f2-553">パラメーター - registerFormSpecializedCustomControl</span><span class="sxs-lookup"><span data-stu-id="065f2-553">Parameters - registerFormSpecializedCustomControl</span></span>

<span data-ttu-id="065f2-554">customControlName</span><span class="sxs-lookup"><span data-stu-id="065f2-554">customControlName</span></span>  

## <a name="method-setapply"></a><span data-ttu-id="065f2-555">メソッド setApply</span><span class="sxs-lookup"><span data-stu-id="065f2-555">Method setApply</span></span>

```xpp
public void setApply(Object object, [Object parm])
```

### <a name="parameters---setapply"></a><span data-ttu-id="065f2-556">パラメーター - setApply</span><span class="sxs-lookup"><span data-stu-id="065f2-556">Parameters - setApply</span></span>

<span data-ttu-id="065f2-557">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="065f2-557">object</span></span>  

<!-- -->

<span data-ttu-id="065f2-558">parm</span><span class="sxs-lookup"><span data-stu-id="065f2-558">parm</span></span>  

## <a name="method-new"></a><span data-ttu-id="065f2-559">メソッド new</span><span class="sxs-lookup"><span data-stu-id="065f2-559">Method new</span></span>

```xpp
public void new(xArgs args)
```

### <a name="parameters---new"></a><span data-ttu-id="065f2-560">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="065f2-560">Parameters - new</span></span>

<span data-ttu-id="065f2-561">args</span><span class="sxs-lookup"><span data-stu-id="065f2-561">args</span></span>  

## <a name="method-registerxppilimplementation"></a><span data-ttu-id="065f2-562">メソッド RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="065f2-562">Method RegisterXppILImplementation</span></span>

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a><span data-ttu-id="065f2-563">パラメーター - RegisterXppILImplementation</span><span class="sxs-lookup"><span data-stu-id="065f2-563">Parameters - RegisterXppILImplementation</span></span>

<span data-ttu-id="065f2-564">className</span><span class="sxs-lookup"><span data-stu-id="065f2-564">className</span></span>  

## <a name="method-syscolorchanged"></a><span data-ttu-id="065f2-565">メソッド sysColorChanged</span><span class="sxs-lookup"><span data-stu-id="065f2-565">Method sysColorChanged</span></span>

```xpp
public void sysColorChanged()
```

## <a name="method-selectrecordmode"></a><span data-ttu-id="065f2-566">メソッド selectRecordMode</span><span class="sxs-lookup"><span data-stu-id="065f2-566">Method selectRecordMode</span></span>

```xpp
public void selectRecordMode([FormControl control])
```

### <a name="parameters---selectrecordmode"></a><span data-ttu-id="065f2-567">パラメーター - selectRecordMode</span><span class="sxs-lookup"><span data-stu-id="065f2-567">Parameters - selectRecordMode</span></span>

<span data-ttu-id="065f2-568">control</span><span class="sxs-lookup"><span data-stu-id="065f2-568">control</span></span>  

## <a name="method-onpostrun"></a><span data-ttu-id="065f2-569">メソッド OnPostRun</span><span class="sxs-lookup"><span data-stu-id="065f2-569">Method OnPostRun</span></span>

```xpp
private void OnPostRun([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onpostrun"></a><span data-ttu-id="065f2-570">パラメーター - OnPostRun</span><span class="sxs-lookup"><span data-stu-id="065f2-570">Parameters - OnPostRun</span></span>

<span data-ttu-id="065f2-571">sender</span><span class="sxs-lookup"><span data-stu-id="065f2-571">sender</span></span>  

<!-- -->

<span data-ttu-id="065f2-572">e</span><span class="sxs-lookup"><span data-stu-id="065f2-572">e</span></span>  

## <a name="method-skipsaveusersetting"></a><span data-ttu-id="065f2-573">メソッド skipSaveUserSetting</span><span class="sxs-lookup"><span data-stu-id="065f2-573">Method skipSaveUserSetting</span></span>

```xpp
public void skipSaveUserSetting(boolean skip)
```

### <a name="parameters---skipsaveusersetting"></a><span data-ttu-id="065f2-574">パラメーター - skipSaveUserSetting</span><span class="sxs-lookup"><span data-stu-id="065f2-574">Parameters - skipSaveUserSetting</span></span>

<span data-ttu-id="065f2-575">skip</span><span class="sxs-lookup"><span data-stu-id="065f2-575">skip</span></span>  

## <a name="method-selectmode"></a><span data-ttu-id="065f2-576">メソッド selectMode</span><span class="sxs-lookup"><span data-stu-id="065f2-576">Method selectMode</span></span>

```xpp
public void selectMode([FormControl control])
```

### <a name="parameters---selectmode"></a><span data-ttu-id="065f2-577">パラメーター - selectMode</span><span class="sxs-lookup"><span data-stu-id="065f2-577">Parameters - selectMode</span></span>

<span data-ttu-id="065f2-578">control</span><span class="sxs-lookup"><span data-stu-id="065f2-578">control</span></span>  

## <a name="method-printpreview"></a><span data-ttu-id="065f2-579">メソッド printPreview</span><span class="sxs-lookup"><span data-stu-id="065f2-579">Method printPreview</span></span>

```xpp
public void printPreview()
```

## <a name="method-onactivated"></a><span data-ttu-id="065f2-580">メソッド OnActivated</span><span class="sxs-lookup"><span data-stu-id="065f2-580">Method OnActivated</span></span>

```xpp
private void OnActivated([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onactivated"></a><span data-ttu-id="065f2-581">パラメーター - OnActivated</span><span class="sxs-lookup"><span data-stu-id="065f2-581">Parameters - OnActivated</span></span>

<span data-ttu-id="065f2-582">sender</span><span class="sxs-lookup"><span data-stu-id="065f2-582">sender</span></span>  

<!-- -->

<span data-ttu-id="065f2-583">e</span><span class="sxs-lookup"><span data-stu-id="065f2-583">e</span></span>  

## <a name="method-collapsefactboxpaneatstart"></a><span data-ttu-id="065f2-584">メソッド collapseFactBoxPaneAtStart</span><span class="sxs-lookup"><span data-stu-id="065f2-584">Method collapseFactBoxPaneAtStart</span></span>

```xpp
public void collapseFactBoxPaneAtStart()
```

## <a name="method-lock"></a><span data-ttu-id="065f2-585">メソッド lock</span><span class="sxs-lookup"><span data-stu-id="065f2-585">Method lock</span></span>

```xpp
public void lock()
```

## <a name="method-init"></a><span data-ttu-id="065f2-586">メソッド init</span><span class="sxs-lookup"><span data-stu-id="065f2-586">Method init</span></span>

```xpp
public void init()
```

## <a name="method-formontop"></a><span data-ttu-id="065f2-587">メソッド formOnTop</span><span class="sxs-lookup"><span data-stu-id="065f2-587">Method formOnTop</span></span>

```xpp
public void formOnTop()
```

## <a name="method-close"></a><span data-ttu-id="065f2-588">メソッド close</span><span class="sxs-lookup"><span data-stu-id="065f2-588">Method close</span></span>

```xpp
public void close()
```

## <a name="method-delautocompletestring"></a><span data-ttu-id="065f2-589">メソッド delAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-589">Method delAutoCompleteString</span></span>

```xpp
public void delAutoCompleteString([AnyType control])
```

### <a name="parameters---delautocompletestring"></a><span data-ttu-id="065f2-590">パラメーター - delAutoCompleteString</span><span class="sxs-lookup"><span data-stu-id="065f2-590">Parameters - delAutoCompleteString</span></span>

<span data-ttu-id="065f2-591">control</span><span class="sxs-lookup"><span data-stu-id="065f2-591">control</span></span>  

## <a name="method-closeok"></a><span data-ttu-id="065f2-592">メソッド closeOk</span><span class="sxs-lookup"><span data-stu-id="065f2-592">Method closeOk</span></span>

```xpp
public void closeOk()
```

## <a name="method-modeledqueryname"></a><span data-ttu-id="065f2-593">メソッド modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="065f2-593">Method modeledQueryName</span></span>

```xpp
public void modeledQueryName(str queryName)
```

### <a name="parameters---modeledqueryname"></a><span data-ttu-id="065f2-594">パラメーター - modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="065f2-594">Parameters - modeledQueryName</span></span>

<span data-ttu-id="065f2-595">queryName</span><span class="sxs-lookup"><span data-stu-id="065f2-595">queryName</span></span>  

## <a name="method-initworkflowcontrols"></a><span data-ttu-id="065f2-596">メソッド initWorkflowControls</span><span class="sxs-lookup"><span data-stu-id="065f2-596">Method initWorkflowControls</span></span>

```xpp
public void initWorkflowControls()
```

## <a name="method-setorder"></a><span data-ttu-id="065f2-597">メソッド setOrder</span><span class="sxs-lookup"><span data-stu-id="065f2-597">Method setOrder</span></span>

```xpp
public void setOrder(FormControl control, FormControl control1, [boolean before])
```

### <a name="parameters---setorder"></a><span data-ttu-id="065f2-598">パラメーター - setOrder</span><span class="sxs-lookup"><span data-stu-id="065f2-598">Parameters - setOrder</span></span>

<span data-ttu-id="065f2-599">control</span><span class="sxs-lookup"><span data-stu-id="065f2-599">control</span></span>  

<!-- -->

<span data-ttu-id="065f2-600">control1</span><span class="sxs-lookup"><span data-stu-id="065f2-600">control1</span></span>  

<!-- -->

<span data-ttu-id="065f2-601">以前</span><span class="sxs-lookup"><span data-stu-id="065f2-601">before</span></span>  

## <a name="method-allowcrossformlinks"></a><span data-ttu-id="065f2-602">メソッド allowCrossFormLinks</span><span class="sxs-lookup"><span data-stu-id="065f2-602">Method allowCrossFormLinks</span></span>

```xpp
public void allowCrossFormLinks(boolean allowCrossFormLinks)
```

### <a name="parameters---allowcrossformlinks"></a><span data-ttu-id="065f2-603">パラメーター - allowCrossFormLinks</span><span class="sxs-lookup"><span data-stu-id="065f2-603">Parameters - allowCrossFormLinks</span></span>

<span data-ttu-id="065f2-604">allowCrossFormLinks</span><span class="sxs-lookup"><span data-stu-id="065f2-604">allowCrossFormLinks</span></span>  

## <a name="method-raiseonpostrun"></a><span data-ttu-id="065f2-605">メソッド RaiseOnPostRun</span><span class="sxs-lookup"><span data-stu-id="065f2-605">Method RaiseOnPostRun</span></span>

```xpp
public void RaiseOnPostRun([FormEventArgs e])
```

### <a name="parameters---raiseonpostrun"></a><span data-ttu-id="065f2-606">パラメーター - RaiseOnPostRun</span><span class="sxs-lookup"><span data-stu-id="065f2-606">Parameters - RaiseOnPostRun</span></span>

<span data-ttu-id="065f2-607">e</span><span class="sxs-lookup"><span data-stu-id="065f2-607">e</span></span>  

## <a name="method-setstatusbarbackgroundcolor"></a><span data-ttu-id="065f2-608">メソッド setStatusBarBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="065f2-608">Method setStatusBarBackgroundColor</span></span>

```xpp
public void setStatusBarBackgroundColor(int a, int r, int g, int b)
```

### <a name="parameters---setstatusbarbackgroundcolor"></a><span data-ttu-id="065f2-609">パラメーター - setStatusBarBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="065f2-609">Parameters - setStatusBarBackgroundColor</span></span>

<span data-ttu-id="065f2-610">a</span><span class="sxs-lookup"><span data-stu-id="065f2-610">a</span></span>  

<!-- -->

<span data-ttu-id="065f2-611">r</span><span class="sxs-lookup"><span data-stu-id="065f2-611">r</span></span>  

<!-- -->

<span data-ttu-id="065f2-612">g</span><span class="sxs-lookup"><span data-stu-id="065f2-612">g</span></span>  

<!-- -->

<span data-ttu-id="065f2-613">b</span><span class="sxs-lookup"><span data-stu-id="065f2-613">b</span></span>  

## <a name="method-loadpersonalization"></a><span data-ttu-id="065f2-614">メソッド loadPersonalization</span><span class="sxs-lookup"><span data-stu-id="065f2-614">Method loadPersonalization</span></span>

```xpp
public void loadPersonalization()
```

## <a name="method-doapply"></a><span data-ttu-id="065f2-615">メソッド doApply</span><span class="sxs-lookup"><span data-stu-id="065f2-615">Method doApply</span></span>

```xpp
public void doApply()
```

## <a name="method-oninitializing"></a><span data-ttu-id="065f2-616">メソッド OnInitializing</span><span class="sxs-lookup"><span data-stu-id="065f2-616">Method OnInitializing</span></span>

```xpp
private void OnInitializing([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---oninitializing"></a><span data-ttu-id="065f2-617">パラメーター - OnInitializing</span><span class="sxs-lookup"><span data-stu-id="065f2-617">Parameters - OnInitializing</span></span>

<span data-ttu-id="065f2-618">sender</span><span class="sxs-lookup"><span data-stu-id="065f2-618">sender</span></span>  

<!-- -->

<span data-ttu-id="065f2-619">e</span><span class="sxs-lookup"><span data-stu-id="065f2-619">e</span></span>  

## <a name="method-flushcountryregioncodecache"></a><span data-ttu-id="065f2-620">メソッド flushCountryRegionCodeCache</span><span class="sxs-lookup"><span data-stu-id="065f2-620">Method flushCountryRegionCodeCache</span></span>

```xpp
public void flushCountryRegionCodeCache()
```

## <a name="method-localrefresh"></a><span data-ttu-id="065f2-621">メソッド localRefresh</span><span class="sxs-lookup"><span data-stu-id="065f2-621">Method localRefresh</span></span>

```xpp
public void localRefresh()
```

